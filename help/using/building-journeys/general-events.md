---
solution: Journey Optimizer
product: journey optimizer
title: 一般事件
description: 了解如何使用一般事件
feature: Journeys
topic: Content Management
role: User
level: Intermediate
keywords: 自定义、常规、事件、历程
exl-id: b1813122-7031-452e-9ac5-a4ea7c6dc57c
source-git-commit: 72bd00dedb943604b2fa85f7173cd967c3cbe5c4
workflow-type: tm+mt
source-wordcount: '441'
ht-degree: 20%

---

# 一般事件 {#general-events}

>[!CONTEXTUALHELP]
>id="ajo_journey_event_custom"
>title="一般事件"
>abstract="事件允许您统一触发历程，向流入历程的个人实时发送消息。对于此类事件，只能添加标签和描述。事件配置由数据工程师执行，不可编辑。"

事件允许您统一触发历程，向流入历程的个人实时发送消息。

对于此类事件，只能添加标签和描述。配置的其他部分无法编辑。 该操作由技术用户执行。 请参阅[此页](../event/about-events.md)。

![](assets/general-events.png)

删除业务事件时，会自动添加 **读取受众** 活动。 有关业务事件的详细信息，请参阅 [本节](../event/about-events.md)

## 在特定时间监听事件 {#events-specific-time}

位于历程中的事件活动可无限期地侦听事件。 要仅在特定时间内侦听事件，必须为事件配置超时。

然后，该历程将在超时指定的时间内侦听事件。 如果在该时间段内收到事件，则该人员将流入事件路径。 否则，客户将流入超时路径或结束其历程。

要为事件配置超时，请执行以下步骤：

1. 激活 **[!UICONTROL 定义事件超时]** 事件属性中的选项。

1. 指定历程将等待事件的时间量。

1. 如果在指定的超时内未收到任何事件时要将个人发送到超时路径中，请启用 **[!UICONTROL 设置超时路径]** 选项。 如果未启用此选项，则到达超时后个人将结束历程。

   ![](assets/event-timeout.png)

在本例中，历程向客户发送第一个欢迎推送。 然后，仅当客户第二天进入餐厅时，它才会发送餐点折扣推送。 因此，我们将restaurant事件配置为1天超时：

* 如果在欢迎推送后不到1天收到餐厅事件，则发送餐饮折扣推送活动。
* 如果在第二天未收到餐馆事件，则该人员将流过超时路径。

请注意，如果要对位于之后的多个事件配置超时， **[!UICONTROL 等待]** 活动，您只需在这些事件之一上配置超时。

超时将应用于 **[!UICONTROL 等待]** 活动。 如果在指定的超时之前未收到任何事件，则个人将流入单个超时路径或将结束其历程。

![](assets/event-timeout-group.png)
