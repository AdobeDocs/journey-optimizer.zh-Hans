---
title: 创建订阅列表
description: 了解如何在Journey Optimizer中设置订阅列表
feature: Landing Pages
topic: Content Management
role: User
level: Beginner
hidefromtoc: true
hide: true
exl-id: 5e5419a0-5121-4aa7-a975-b1f08e2918c9
source-git-commit: c988f0baa8b3c622dfb4f1ff060001a3462ed31e
workflow-type: tm+mt
source-wordcount: '352'
ht-degree: 3%

---

# 订阅列表 {#create-subscription-list}

## 什么是订阅列表？ {#subscription-list-definition}

A subscription service refers to marketing goods and services provided to customers who have opted in to receive communications on a specific subject/event/interest/etc. 不断进行。 In [!DNL Journey Optimizer], these opted-in customers are gathered into a subscription list.

订阅服务可以是：

* a newsletter, for example: &quot;Running series&quot;
* 例如：《2021年峰会》
* 网络研讨会，例如：“了解有关加密的更多信息”
* an interest on a particular product/sport/service/etc., for example: &quot;Interested to buy a house in the next 12 months&quot;
* a preference on how to be notified, for example: &quot;Receive new song notifications on email&quot;

The profiles can be added to a subscription list through a [landing page](create-lp.md). 示例请参见 [此部分](lp-use-cases.md#subscription-to-a-service).

## Define a subscription list {#define-subscription-list}

要创建订阅列表，请执行以下步骤。

1. To access the subscription lists, select **[!UICONTROL Customer]** > **[!UICONTROL Subscription list]**.

   ![](assets/lp_subscription-lists.png)

1. 选择 **[!UICONTROL Create subscription list]** 按钮。

   ![](assets/lp_create-subscription-list.png)

1. 添加名称和描述。 这些字段是必填字段。

1. 您可以定义开始日期和结束日期。

   ![](assets/lp_subscription-list-dates.png)

1. 单击 **[!UICONTROL Save]**。

该列表显示创建的所有订阅列表。 You can filter them based on the creation date or modification date, and their status.

![](assets/lp_subscription-filters.png)

The possible statuses are as follows:

* **[!UICONTROL Not started]**: You defined a start date that is later than the current day. 被订阅用户档案将不会接收与此订阅列表相关的通信。
* **[!UICONTROL Live]**:当天由订阅列表开始日期和结束日期之间组成，或者您未定义结束/开始日期，这意味着订阅列表始终处于活动状态。
* **[!UICONTROL Expired]**:结束日期已过，因此订阅列表不再有效。 任何订阅的用户档案将不会再收到与此订阅列表相关的任何通信。

创建订阅列表后，即可在登陆页面中使用该列表。 通过登陆页面表单选择加入的用户档案将添加到列表中。 [了解详情](design-lp.md)

在 [构建旅程](../building-journeys/journey-gs.md#jo-build) 和添加个性化。

>[!NOTE]
>
>您可以通过特定报告监控订阅列表的影响。 [了解详情](subscription-report.md)

<!--

**Questions**

* Can't see the newly created subscription list in UI because their name included spacing > bug - to follow up (should be fixed for Dec. release)

* Can you update the subscription list in a way other than through a LP? Not in UI but with APIs > to follow up with Fred

-->
