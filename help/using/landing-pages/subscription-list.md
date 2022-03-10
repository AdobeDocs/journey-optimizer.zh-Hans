---
title: 创建订阅列表
description: 了解如何在Journey Optimizer中设置订阅列表
feature: Landing Pages
topic: Content Management
role: User
level: Beginner
exl-id: 5e5419a0-5121-4aa7-a975-b1f08e2918c9
source-git-commit: 8f0e85a08a0ab510f02aab3787f30933e430e3e4
workflow-type: tm+mt
source-wordcount: '352'
ht-degree: 3%

---

# 订阅列表 {#create-subscription-list}

## 什么是订阅列表？ {#subscription-list-definition}

订购服务是指向选择接收特定主题/事件/兴趣等通信的客户提供的营销产品和服务。 不断进行。 在 [!DNL Journey Optimizer]，则这些选择加入的客户将被收集到订阅列表中。

订阅服务可以是：

* 例如，新闻稿：&quot;运行系列&quot;
* 例如：《2021年峰会》
* 网络研讨会，例如：“了解有关加密的更多信息”
* 对特定产品/体育/服务/等的兴趣，例如：“有兴趣在未来12个月内买房”
* 例如，关于如何通知的首选项：“通过电子邮件接收新歌曲通知”

用户档案可以通过 [登陆页面](create-lp.md). 示例请参见 [此部分](lp-use-cases.md#subscription-to-a-service).

## 定义订阅列表 {#define-subscription-list}

要创建订阅列表，请执行以下步骤。

1. 要访问订阅列表，请选择 **[!UICONTROL Customer]** > **[!UICONTROL Subscription list]**.

   ![](assets/lp_subscription-lists.png)

1. 选择 **[!UICONTROL Create subscription list]** 按钮。

   ![](assets/lp_create-subscription-list.png)

1. 添加名称和描述。 这些字段是必填字段。

1. 您可以定义开始日期和结束日期。

   ![](assets/lp_subscription-list-dates.png)

1. 单击 **[!UICONTROL Save]**。

该列表显示创建的所有订阅列表。 您可以根据创建日期或修改日期及其状态进行筛选。

![](assets/lp_subscription-filters.png)

可能的状态如下：

* **[!UICONTROL Not started]**:您定义的开始日期晚于当天。 订阅的用户档案将不会接收与此订阅列表相关的通信。
* **[!UICONTROL Live]**:当天由订阅列表开始日期和结束日期之间组成，或者您未定义结束/开始日期，这意味着订阅列表始终处于活动状态。
* **[!UICONTROL Expired]**:结束日期已过，因此订阅列表不再有效。 任何订阅的用户档案将不会再收到与此订阅列表相关的任何通信。

创建订阅列表后，即可在登陆页面中使用该列表。 通过登陆页面表单选择加入的用户档案将添加到列表中。 [了解详情](design-lp.md)

在 [构建旅程](../building-journeys/journey-gs.md#jo-build) 和添加个性化。

>[!NOTE]
>
>您可以通过特定报告监控订阅列表的影响。 [了解详情](subscription-report.md)
