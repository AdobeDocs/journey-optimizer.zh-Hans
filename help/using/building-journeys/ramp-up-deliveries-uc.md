---
solution: Journey Optimizer
product: journey optimizer
title: 加快投放速度
description: 了解如何加快投放速度
feature: Journeys, Use Cases, IP Warmup Plans
topic: Content Management
role: User, Data Engineer
level: Intermediate, Experienced
hide: true
hidefromtoc: true
keywords: 可交付性、历程、用例、电子邮件、声誉
exl-id: 83d1b68d-011a-4109-b5f0-6ca1ade2944d
source-git-commit: e34c39c02f71361277f28b1a116a54390875f93d
workflow-type: tm+mt
source-wordcount: '264'
ht-degree: 2%

---

# 用例：增加投放数量{#use-case-ramp-up-your-deliveries}

如果您最近已移至其他电子邮件服务提供商、IP地址或电子邮件域或子域，则需要建立您作为发件人的声誉。 否则，您的投放可能会被阻止或移至收件人邮箱的垃圾邮件文件夹。 请参阅[可投放性最佳实践指南](https://experienceleague.adobe.com/docs/deliverability-learn/deliverability-best-practice-guide/additional-resources/generic-resources/increase-reputation-with-ip-warming.html?lang=zh-Hans){target="_blank"}以了解如何利用IP预热提高您的电子邮件信誉。

要预热您的IP，您可以逐渐增加投放的数量。 阅读有关[在Journey Optimizer](../reports/deliverability.md)中优化可投放性的更多信息。

此用例的目的是创建历程以加快电子邮件投放。 要配置此历程，请执行以下步骤：

1. 创建旅程。 [了解详情](journey-gs.md)。

1. 向历程添加&#x200B;**[!UICONTROL 条件]**&#x200B;活动。 [了解详情](condition-activity.md)。

1. 在&#x200B;**[!UICONTROL 条件]**&#x200B;活动设置中，设置投放的最大收件人数：

   1. 在&#x200B;**[!UICONTROL 条件]**&#x200B;活动设置中，将&#x200B;**[!UICONTROL 类型]**&#x200B;字段设置为&#x200B;**[!UICONTROL 配置文件上限]**。 [了解详情](condition-activity.md#profile_cap)。

   1. 将&#x200B;**[!UICONTROL Limit]**&#x200B;字段设置为此投放的最大收件人数。

   ![](assets/profile-cap-condition.png)

   您可以逐渐提高此限制，直至达到订阅者的总数。

1. 在&#x200B;**[!UICONTROL 条件]**&#x200B;活动之后，将&#x200B;**[!UICONTROL 电子邮件]**&#x200B;操作活动添加到名义路径。

   ![](assets/ramp-up-deliveries-message.png)

   当历程运行时，将向输入的配置文件发送消息，发送数量最多为您指定的最大配置文件数。 当达到此限制时，输入的用户档案将采用替代路径。

1. 使用您选择的活动完成历程。

在IP预热后，您可以删除此条件。
