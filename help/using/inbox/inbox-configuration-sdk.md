---
title: 在Web SDK中配置收件箱支持
description: 了解如何通过Adobe Experience Platform Web SDK，使用内容卡和收件箱营销活动在Adobe Journey Optimizer中构建持久性消息收件箱。
feature: Content Cards
topic: Content Management
role: Developer
level: Experienced
source-git-commit: 1ee6fd3ed3523635ea7dbe46dbae0e2403246818
workflow-type: tm+mt
source-wordcount: '524'
ht-degree: 1%

---

# 在 Web SDK 中配置收件箱支持 {#inbox-configuration-sdk}

>[!BEGINSHADEBOX]

**在此页面上：**&#x200B;设置并运行一个示例，该示例将内容卡营销活动和收件箱营销活动与Adobe Experience Platform Web SDK相结合，以便在您的网站上传递持久性通知收件箱。

>[!ENDSHADEBOX]

消息收件箱是由针对同一表面的两个Adobe Journey Optimizer营销活动驱动的持久性通知收件箱：

* **内容卡营销活动**，用于向收件箱发送单个通知项目。
* **收件箱营销活动**，提供标题、空状态副本和布局等配置。


## 配置 Adobe Journey Optimizer {#ajo-setup}

在实施Web SDK之前，请在Journey Optimizer中设置数据流、渠道和营销活动，以将内容交付到收件箱。

1. 配置一个将&#x200B;**Adobe Experience Platform**&#x200B;配置为服务的&#x200B;**数据流**，其中启用了&#x200B;**Journey Optimizer**&#x200B;并选择了&#x200B;**事件数据集**。

1. 创建共享同一表面的两个渠道配置：一个&#x200B;**内容卡**&#x200B;渠道和一个&#x200B;**收件箱**&#x200B;渠道。 [了解如何配置内容卡渠道](../content-card/content-card-configuration.md)和[了解如何配置收件箱渠道](inbox-configuration.md)。

   将两个渠道的&#x200B;**页面URL**&#x200B;和&#x200B;**页面**&#x200B;上的位置设置为您在先决条件中定义的表面。 此位置必须与您在Web SDK代码中查询的表面匹配。

1. [创建内容卡营销活动](../content-card/create-content-card.md)，该营销活动将内容卡渠道用于其内容卡配置。

   对于应根据网页上的用户操作传递的消息，请启用相关操作上的&#x200B;**其他传递规则**，并设置用于确定消息何时出现的事件和值条件。 对收件箱应收到的每种类型的通知重复此操作。

1. [创建使用收件箱渠道的收件箱营销活动](inbox-create.md)。 此营销活动交付用于配置收件箱Shell本身的元数据。

   将收件箱营销活动的受众和计划设置与内容卡营销活动相匹配，以使两者对同一用户同时有效。

1. 激活这两个营销活动。

## 实施Web SDK {#web-sdk-implementation}

收件箱依赖于两个Web SDK命令：

* `subscribeRulesetItems`注册每次在建议符合显示更改条件时运行的回调。

* `sendEvent`获取这些建议。 您可以稍后发送其他事件，以更新哪些消息符合显示条件。

1. 定义内容卡和收件箱架构，以及与AJO渠道配置匹配的表面：

   ```javascript
   const CONTENT_CARD_SCHEMA = "https://ns.adobe.com/personalization/message/content-card";
   const INBOX_SCHEMA        = "https://ns.adobe.com/personalization/message/inbox";
   const SURFACE             = "web://your-site.example/#message-inbox";
   ```

1. 使用数据流配置Web SDK：

   ```javascript
   alloy("configure", {
     datastreamId: "YOUR_DATASTREAM_ID",
     orgId: "YOUR_ORG_ID@AdobeOrg",
     defaultConsent: "in", // May not be usable in your implementation, but should be used for testing
     personalizationStorageEnabled: true,
   })
   ```

1. 订阅表面和架构的规则集项目，并提供在内容卡建议发生更改时对其进行处理的回调：

   ```javascript
   alloy("subscribeRulesetItems", {
     surfaces: [SURFACE],
     schemas: [CONTENT_CARD_SCHEMA, INBOX_SCHEMA],
     callback: (result, collectEvent) => {
       const { propositions = [] } = result;
       const notifications = propositions
         .filter((p) => p.items?.[0]?.schema === CONTENT_CARD_SCHEMA)
         .map((proposition) => {
           const content = proposition.items[0]?.data?.content ?? {};
           return {
             id: proposition.scopeDetails.activity.id,
             title: content.title?.content ?? content.title ?? "",
             description: content.body?.content ?? content.body ?? "",
             proposition,
           };
         });
       renderNotifications(notifications, collectEvent);
     },
   });
   ```

1. 当用户与您的应用程序交互时，发送事件以更新应显示的内容卡建议：

   ```javascript
   alloy("sendEvent", {
     renderDecisions: true,
     personalization: { surfaces: [SURFACE] },
   });
   ```

1. 使用由`subscribeRulesetItems`回调提供的`collectEvent`函数将交互报告回AJO。 这可以保持促销活动报表的准确性：

   ```javascript
   // When a notification is displayed in the detail view:
   collectEvent("display", [notification.proposition]);
   
   // When a user clicks or interacts with a notification:
   collectEvent("interact", [notification.proposition]);
   
   // When a user dismisses a notification without reading it:
   collectEvent("dismiss", [notification.proposition]);
   
   // When a user deletes a notification:
   collectEvent("interact", [notification.proposition]);
   collectEvent("delete",   [notification.proposition]);
   ```

1. 对于具有其他投放规则（例如`action = deposit-funds`）的卡片，请使用匹配的`decisionContext`调用`evaluateRulesets`以触发它们，因为它们不会单独出现在`sendEvent`中：

   ```javascript
   alloy("evaluateRulesets", {
     renderDecisions: true,
     personalization: {
       decisionContext: { action: "deposit-funds" },
     },
   });
   ```

   `subscribeRulesetItems`回调将再次运行，其中现有卡旁包含任何新鉴定的卡。

1. 安装依赖项并启动示例服务器：

   ```bash
   npm install
   npm start
   ```

1. 在浏览器中打开`https://localhost`。

1. 在测试之前，更新`src/app/page.js`中的`datastreamId`、`orgId`和`SURFACE`常量以指向您的AJO环境。

{{$include /help/_includes/do-not-localize/inbox/ai-augmented-inbox-configuration-sdk.md}}
