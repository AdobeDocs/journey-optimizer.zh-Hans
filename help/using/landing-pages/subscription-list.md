---
solution: Journey Optimizer
product: journey optimizer
title: 创建订阅列表
description: 了解如何在Journey Optimizer中设置订阅列表
feature: Subscriptions
topic: Content Management
role: User
level: Beginner
keywords: 登录，登陆页面，列表，订阅，服务
exl-id: 5e5419a0-5121-4aa7-a975-b1f08e2918c9
source-git-commit: f63f9d6ffd28d276f8a3dadbf8dc6b947b8331e7
workflow-type: tm+mt
source-wordcount: '442'
ht-degree: 11%

---

# 订阅列表 {#create-subscription-list}

## 什么是订阅列表？ {#subscription-list-definition}

>[!CONTEXTUALHELP]
>id="ajo_subscription_list"
>title="设置订阅列表"
>abstract="创建订阅列表，用于收集已选择接收特定主题或事件通信的配置文件。 "
>additional-url="https://experienceleague.adobe.com/docs/journey-optimizer/using/landing-pages/subscription-list.html?lang=zh-Hans#define-subscription-list" text="创建订阅列表"

订阅服务是指向选择接收有关特定主题/事件/兴趣/等的通信的客户提供的营销商品和服务。 持续进行。 在[!DNL Journey Optimizer]中，这些选择加入的客户被收集到订阅列表中。

订阅服务可以是：

* 新闻稿，例如：“Running series”
* 例如，活动：“Summit 2021”
* 网络研讨会，例如：“了解有关加密编译的更多信息”
* 对特定产品/运动/服务/等的兴趣，例如：“有兴趣在未来12个月内购买房屋”
* 关于通知方式的首选项，例如：“通过电子邮件接收新歌曲通知”

可以通过[登陆页面](create-lp.md)将配置文件添加到订阅列表。 [此部分](lp-use-cases.md#subscription-to-a-service)中提供了一个示例。

## 创建订阅列表 {#define-subscription-list}

要创建订阅列表，请执行以下步骤。

1. 要访问订阅列表，请选择&#x200B;**[!UICONTROL 客户]** > **[!UICONTROL 订阅列表]**。

   ![](assets/lp_subscription-lists.png)

1. 选择&#x200B;**[!UICONTROL 创建订阅列表]**&#x200B;按钮。

   ![](assets/lp_create-subscription-list.png)

1. 添加标题和描述。 这些字段为必填字段。

   ![](assets/lp_subscription-list-name.png)

   >[!CAUTION]
   >
   >当前不能在&#x200B;**[!UICONTROL 标题]**&#x200B;字段中为其他订阅列表使用空格或输入已存在的名称。

1. 您可以定义开始日期和结束日期。

   ![](assets/lp_subscription-list-dates.png)

1. 从&#x200B;**[!UICONTROL 标记]**&#x200B;字段中选择或创建Adobe Experience Platform标记以对您的登陆页面进行分类，从而改进搜索。 [了解详情](../start/search-filter-categorize.md#tags)

1. 单击&#x200B;**[!UICONTROL 保存]**。

该列表显示了创建的所有订阅列表。 您可以根据创建日期或修改日期及其状态筛选它们。

![](assets/lp_subscription-filters.png)

可能的状态如下：

* **[!UICONTROL 未开始]**：您定义的开始日期晚于当前日期。 订阅的用户档案将尚未收到与此订阅列表相关的通信。
* **[!UICONTROL 实时]**：当天包含在订阅列表开始日期和结束日期之间，或者您未定义结束/开始日期，这意味着订阅列表始终实时。
* **[!UICONTROL 已过期]**：已超过结束日期，因此订阅列表不再有效。 任何订阅的配置文件都不会再收到与此订阅列表相关的任何通信。

创建订阅列表后，您可以在登陆页面中使用该列表。 选择通过登陆页面表单加入的用户档案将添加到列表中。 [了解详情](design-lp.md)

在[构建历程](../building-journeys/journey-gs.md#jo-build)并添加个性化设置时，您还可以将订阅列表用作受众。

>[!NOTE]
>
>您可以通过特定报告监控订阅列表的影响。 [了解详情](../reports/subscription-report-live.md)
