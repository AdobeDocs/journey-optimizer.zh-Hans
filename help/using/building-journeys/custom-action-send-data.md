---
solution: Journey Optimizer
product: journey optimizer
title: 将数据发送到AEP
description: 了解如何将数据发送到AEP
feature: Journeys, Use Cases
topic: Content Management
role: User, Data Engineer
level: Intermediate, Experienced
keywords: 历程，用例
source-git-commit: f8d62a702824bcfca4221c857acf1d1294427543
workflow-type: tm+mt
source-wordcount: '268'
ht-degree: 2%

---

# 用例：创建自定义操作以将数据发送到Adobe Experience Platform{#send-data-to-aep}

如果您最近已移至其他电子邮件服务提供商、IP地址或电子邮件域或子域，则需要建立您作为发件人的声誉。 否则，您的投放可能会被阻止或移至收件人邮箱的垃圾邮件文件夹。 了解如何在中利用IP预热提高您的电子邮件声誉 [可投放性最佳实践指南](https://experienceleague.adobe.com/docs/deliverability-learn/deliverability-best-practice-guide/additional-resources/generic-resources/increase-reputation-with-ip-warming.html?lang=zh-Hans){target="_blank"}.

要预热您的IP，您可以逐渐增加投放的数量。 详细了解 [在Journey Optimizer中优化可投放性](../reports/deliverability.md).

此用例的目的是创建历程以加快电子邮件投放。 要配置此历程，请执行以下步骤：

1. 创建旅程。 [了解详情](journey-gs.md)。

1. 添加 **[!UICONTROL 条件]** 历程的活动。 [了解详情](condition-activity.md)。

1. 在 **[!UICONTROL 条件]** 活动设置，设置投放的最大收件人数：

   1. 在 **[!UICONTROL 条件]** 活动设置，设置 **[!UICONTROL 类型]** 字段至 **[!UICONTROL 配置文件上限]**. [了解详情](condition-activity.md#profile_cap)。

   1. 设置 **[!UICONTROL 限制]** 字段为此投放的最大收件人数。

   ![](assets/profile-cap-condition.png)

   您可以逐渐提高此限制，直至达到订阅者的总数。

1. 添加 **[!UICONTROL 电子邮件]** 操作活动，指向以下路径之后的名义路径 **[!UICONTROL 条件]** 活动。

   ![](assets/ramp-up-deliveries-message.png)

   当历程运行时，将向输入的配置文件发送消息，发送数量最多为您指定的最大配置文件数。 当达到此限制时，输入的用户档案将采用替代路径。

1. 使用您选择的活动完成历程。

在IP预热后，您可以删除此条件。