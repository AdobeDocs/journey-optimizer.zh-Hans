---
title: 创建订阅列表
description: 了解如何在Journey Optimizer中设置订阅列表
feature: Landing Pages
topic: Content Management
role: User
level: Beginner
hidefromtoc: true
hide: true
source-git-commit: 4d564ff89a8cb6c6d76161f2e6cedf39d33e70a0
workflow-type: tm+mt
source-wordcount: '346'
ht-degree: 0%

---

# 创建订阅列表 {#create-subscription-list}

## 什么是订阅列表？

订购服务是指向选择接收特定主题/事件/兴趣等通信的客户提供的营销产品和服务。 不断进行。 在 [!DNL Journey Optimizer]，则这些选择加入的客户将被收集到订阅列表中。

订阅服务可以是：

* 新闻稿，例如“运行系列”
* 例如“2021年峰会”
* 网络研讨会，例如“了解有关加密密码的更多信息”
* 对特定产品/体育/服务/等的兴趣，例如“有兴趣在未来12个月内购买房子”
* 关于如何接收通知的首选项，例如“通过电子邮件接收新歌曲通知”

用户档案可以通过 [登陆页面](create-lp.md). 示例请参见 [此部分](get-started-lp.md#subscription-to-a-service).

## 定义订阅列表 {#define-subscription-list}

要创建订阅列表，请执行以下步骤。

1. 要访问订阅列表，请选择 **[!UICONTROL Customer]** > **[!UICONTROL Subscription list]**.

   ![](../assets/lp_subscription-lists.png)

1. 在订阅列表中，单击 **[!UICONTROL Create subscription]** 列表。

   ![](../assets/lp_create-subscription-list.png)

1. 添加名称和描述。 这些字段是必填字段。

1. 您可以定义开始日期和结束日期。

   ![](../assets/lp_subscription-list-dates.png)

1. 单击 **[!UICONTROL Save]**。

该列表显示创建的所有订阅列表。 您可以根据创建日期或修改日期对其进行筛选。

![](../assets/lp_subscription-filters.png)

可能的状态如下：

* **[!UICONTROL Not started]**:您定义的开始日期晚于当天。 订阅此列表的用户档案将不会收到与此订阅列表相关的通信。
* **[!UICONTROL Live]**:当天由订阅列表开始日期和结束日期之间组成，或者您未定义结束/开始日期，这意味着订阅列表始终处于活动状态。
* **[!UICONTROL Expired]**:结束日期已过，订阅列表不再有效。 订阅此列表的任何用户档案将不会再收到与此订阅列表相关的任何通信。

创建订阅列表后，您可以在登陆页面中使用该列表，以便用户档案可以通过表单选择加入并添加到列表中。 [了解详情](design-lp.md)

在构建历程和个性化时，您还可以将订阅列表用作区段。

<!--

**Questions**

* Can't see the newly created subscription list in UI because their name included spacing > bug - to follow up (should be fixed for Dec. release)

* How do you handle the different statuses? Live, Not started, Expired? Is it only through start/end dates?

* What does it mean when a subscription list is expired or not started? You can't use it in a LP? And if a user is subscribed to this service, then he won't receive communications any more?

* What else can you currently do with subscription lists apart from attach them to a landing page?

* Can you update the subscription list in a way other than through a LP? Not in UI but with APIs > to follow up with Fred

-->