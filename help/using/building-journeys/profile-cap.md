---
title: 配置文件上限
description: 配置文件上限
feature: Journeys
topic: Content Management
role: User
level: Intermediate
exl-id: 496c7666-a133-4aeb-be8e-c37b3b9bf5f9
hide: true
hidefromtoc: true
source-git-commit: b5ce2ea81d4091b4fa9c09e83573f9043c5e55a8
workflow-type: tm+mt
source-wordcount: '445'
ht-degree: 2%

---


# 建立发件人的声誉

如果您最近转移到其他电子邮件服务提供商、IP地址、电子邮件域或子域，则需要确立您作为发件人的声誉。 否则，您的投放可能会被阻止或移动到收件人邮箱的垃圾邮件文件夹中。

要预热IP，您可以逐步增加投放数量。 请参阅 [用例](../building-journeys/ramp-up-deliveries-uc.md).

## 配置文件上限条件类型 {#profile_cap}

下面详细介绍了其他条件类型 [部分](../building-journeys/condition-activity.md).

使用此条件类型为历程路径设置最大用户档案数。 达到此限制后，输入的用户档案会采用替代路径。

您可以使用此条件类型来增加投放的数量。 请参阅 [用例](../building-journeys/ramp-up-deliveries-uc.md).

默认上限为1000。 您可以设置一个介于1到20,000之间的整数值。

计数器仅适用于选定的历程版本。 计数器在一个月后重置为零。 重置后，进入的用户档案将再次采用标称路径，直到达到计数器限制。

即使您将替代路径移动到历程画布上的标称路径上方，标称路径始终比替代路径具有优先级。

![](../assets/profile-cap-condition.png)

## 用例：加快投放速度

如果您最近转移到其他电子邮件服务提供商、IP地址、电子邮件域或子域，则需要确立您作为发件人的声誉。 否则，您的投放可能会被阻止或移动到收件人邮箱的垃圾邮件文件夹中。 了解如何通过 [投放能力最佳实践指南](https://experienceleague.adobe.com/docs/deliverability-learn/deliverability-best-practice-guide/additional-resources/generic-resources/increase-reputation-with-ip-warming.html){target=&quot;_blank&quot;}。

要预热IP，您可以逐步增加投放数量。 有关更多信息 [优化Journey Optimizer的投放能力](../deliverability.md).

此用例的用途是创建历程以提升电子邮件投放。 要配置此历程，请执行以下步骤：

1. 创建历程. [了解更多信息](../building-journeys/journey-gs.md)。

1. 添加 **[!UICONTROL Condition]** 活动到历程。 [了解更多信息](../building-journeys/condition-activity.md)。

1. 在 **[!UICONTROL Condition]** 活动设置中，设置投放的最大收件人数：

   1. 在 **[!UICONTROL Condition]** 活动设置，请设置 **[!UICONTROL Type]** 字段 **[!UICONTROL Profile cap]**. [了解更多信息](profile-cap.md#profile_cap)。

   1. 设置 **[!UICONTROL Limit]** 字段，以限制此投放的收件人最大数量。

   ![](../assets/profile-cap-condition.png)

   您可以逐步将此限制增加到订阅者总数。

1. 添加 **[!UICONTROL Message]** 活动到 **[!UICONTROL Condition]** 活动。

   ![](../assets/ramp-up-deliveries-message.png)

   当历程运行时，将向输入的用户档案发送消息，最大数量为您指定的用户档案。 达到此限制后，进入的用户档案将采用替代路径。

1. 使用您选择的活动完成历程。

IP升温后，您可以删除此条件。

