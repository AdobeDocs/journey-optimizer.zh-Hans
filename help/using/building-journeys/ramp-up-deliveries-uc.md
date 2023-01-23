---
solution: Journey Optimizer
product: journey optimizer
title: 加快投放速度
description: 了解如何加快投放速度
feature: Journeys
topic: Content Management
role: User
level: Intermediate
keywords: 投放能力，历程，用例，电子邮件，声誉
exl-id: 83d1b68d-011a-4109-b5f0-6ca1ade2944d
source-git-commit: 1d30c6ae49fd0cac0559eb42a629b59708157f7d
workflow-type: tm+mt
source-wordcount: '271'
ht-degree: 3%

---

# 用例：加快投放速度{#use-case-ramp-up-your-deliveries}

如果您最近转移到其他电子邮件服务提供商、IP地址、电子邮件域或子域，则需要确立您作为发件人的声誉。 否则，您的投放可能会被阻止或移动到收件人邮箱的垃圾邮件文件夹中。 了解如何通过 [投放能力最佳实践指南](https://experienceleague.adobe.com/docs/deliverability-learn/deliverability-best-practice-guide/additional-resources/generic-resources/increase-reputation-with-ip-warming.html){target="_blank"}.

要预热IP，您可以逐步增加投放数量。 有关更多信息 [优化Journey Optimizer的投放能力](../reports/deliverability.md).

此用例的用途是创建历程以提升电子邮件投放。 要配置此历程，请执行以下步骤：

1. 创建历程. [了解更多信息](journey-gs.md)。

1. 添加 **[!UICONTROL 条件]** 活动到历程。 [了解更多信息](condition-activity.md)。

1. 在 **[!UICONTROL 条件]** 活动设置中，设置投放的最大收件人数：

   1. 在 **[!UICONTROL 条件]** 活动设置，请设置 **[!UICONTROL 类型]** 字段 **[!UICONTROL 配置文件上限]**. [了解更多信息](condition-activity.md#profile_cap)。

   1. 设置 **[!UICONTROL 限制]** 字段，以限制此投放的收件人最大数量。

   ![](assets/profile-cap-condition.png)

   您可以逐步将此限制增加到订阅者总数。

1. 添加 **[!UICONTROL 电子邮件]** 活动到标称路径 **[!UICONTROL 条件]** 活动。

   ![](assets/ramp-up-deliveries-message.png)

   当历程运行时，将向输入的用户档案发送消息，最大数量为您指定的用户档案。 达到此限制后，进入的用户档案将采用替代路径。

1. 使用您选择的活动完成历程。

IP升温后，您可以删除此条件。
