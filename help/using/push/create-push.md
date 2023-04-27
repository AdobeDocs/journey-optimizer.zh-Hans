---
solution: Journey Optimizer
product: journey optimizer
title: 配置推送通知
description: 了解如何在Journey Optimizer中创建推送通知
feature: Overview
topic: Content Management
role: User
level: Beginner
exl-id: 2ebbcd7d-dcfc-4528-974d-6230fc0dca3d
source-git-commit: 803c9f9f05669fad0a9fdeeceef58652b6dccf70
workflow-type: tm+mt
source-wordcount: '699'
ht-degree: 15%

---

# 创建推送通知 {#create-push-notification}

>[!CONTEXTUALHELP]
>id="ajo_message_push"
>title="推送消息创建"
>abstract="添加您的推送消息，并使用表达式编辑器开始对其进行个性化设置。"

## 在历程或营销策划中创建推送通知 {#create}

要创建推送通知，请执行以下步骤：

>[!BEGINTABS]

>[!TAB 向历程添加推送]

1. 打开您的历程，然后从面板的“操作”部分拖放推送活动。

   ![](assets/push_create_1.png)

1. 提供有关消息的基本信息（标签、描述、类别），然后选择要使用的消息界面。 的 **[!UICONTROL 曲面]** 默认情况下，字段会预填充用户用于该渠道的最后一个曲面。

   ![](assets/push_create_2.png)

   >[!NOTE]
   >
   >如果您从历程发送推送通知，则可以利用Adobe Journey Optimizer的发送时间优化功能，根据历史打开率和点击率预测发送消息的最佳时间，以最大限度提高参与度。 [了解如何使用发送时间优化](../building-journeys/journeys-message.md#send-time-optimization)

   有关如何配置旅程的更多信息，请参阅 [本页](../building-journeys/journey-gs.md)

1. 在历程配置屏幕中，单击 **[!UICONTROL 编辑内容]** 按钮来配置推送内容。 [设计推送通知](design-push.md)

1. 定义消息内容后，即可使用测试配置文件对其进行预览和测试。

1. 在推送准备就绪后，完成 [历程](../building-journeys/journey-gs.md) 来发送。

   要通过推送开始和/或交互跟踪收件人的行为，请确保在 [电子邮件活动](../building-journeys/journeys-message.md).

>[!TAB 向营销活动添加推送]

1. 创建新的计划营销活动或API触发的营销活动，选择 **[!UICONTROL 推送通知]** 作为您的操作，然后选择 **[!UICONTROL 应用程序界面]** 。 [了解有关推送配置的更多信息](push-configuration.md).

   ![](assets/push_create_3.png)

1. 单击&#x200B;**[!UICONTROL 创建]**。

1. 从 **[!UICONTROL 属性]** ，编辑营销活动的 **[!UICONTROL 标题]** 和 **[!UICONTROL 描述]**.

   ![](assets/push_create_4.png)

1. 单击 **[!UICONTROL 选择受众]** 按钮，以从可用的Adobe Experience Platform区段列表中定义要定位的受众。 [了解详情](../segment/about-segments.md)。

1. 在 **[!UICONTROL 身份命名空间]** 字段中，选择要用于识别选定区段中个人的命名空间。 [了解详情](../event/about-creating.md#select-the-namespace)。

   ![](assets/push_create_5.png)

1. 营销活动设计为在特定日期或定期频率执行。 了解如何配置 **[!UICONTROL 计划]** 在 [此部分](../campaigns/create-campaign.md#schedule).

1. 从 **[!UICONTROL 操作触发器]** 菜单，选择 **[!UICONTROL 频率]** 在您的推送通知中：

   * 一次
   * 每日
   * 每周
   * 每月

1. 在营销活动配置屏幕中，单击 **[!UICONTROL 编辑内容]** 按钮来配置推送内容。 [设计推送通知](design-push.md)

1. 定义消息内容后，即可使用测试配置文件对其进行预览和测试。

1. 在推送准备就绪后，完成 [营销活动](../campaigns/create-campaign.md) 来发送。

   要通过推送开始和/或交互跟踪收件人的行为，请确保在 [营销活动](../campaigns/create-campaign.md).

>[!ENDTABS]

**相关主题**

* [配置推送渠道](push-gs.md)
* [在历程中添加消息](../building-journeys/journeys-message.md)

## 快速传递模式 {#rapid-delivery}

>[!CONTEXTUALHELP]
>id="ajo_campaigns_rapid_delivery"
>title="快速传递模式"
>abstract="快速传递模式让您可以在推送渠道上，在不超过 3000 万的受众规模下执行高速消息发送。"

快速交付模式（以前称为历程中的突发模式）是 [!DNL Journey Optimizer] 附加组件，允许通过营销活动以大量量发送非常快速的推送消息。

当消息投放的延迟对业务至关重要时，如果您想在手机上发送紧急推送警报（例如，向已安装您的新闻渠道应用程序的用户发送突发新闻），可使用快速投放。

有关使用快速投放模式时性能的更多信息，请参阅 [Adobe Journey Optimizer产品说明](https://helpx.adobe.com/cn/legal/product-descriptions/adobe-journey-optimizer.html).

### 先决条件 {#prerequisites}

快速投放消息具有以下要求：

* 快速交付适用于 **[!UICONTROL 已计划]** 仅限促销活动，且不适用于API触发的促销活动、
* 推送消息中不允许进行个性化，
* 目标受众必须包含少于3000个用户档案，
* 使用快速投放模式，最多可同时执行5个营销活动。

### 激活快速投放模式

1. 创建推送通知营销活动并打开 **[!UICONTROL 快速交付]** 选项。

![](assets/create-campaign-burst.png)

1. 配置消息内容并选择要定位的受众。 [了解如何创建营销活动](#create)

   >[!IMPORTANT]
   >
   >确保消息内容不包含任何个性化，并且受众包含的用户档案少于3000万。

1. 与往常一样，查看并激活您的营销活动。 请注意，在测试模式下，消息不会通过快速投放模式发送。