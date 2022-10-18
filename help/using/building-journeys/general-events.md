---
solution: Journey Optimizer
product: journey optimizer
title: 一般事件
description: 了解如何使用常规事件
feature: Journeys
topic: Content Management
role: User
level: Intermediate
exl-id: b1813122-7031-452e-9ac5-a4ea7c6dc57c
source-git-commit: 021cf48ab4b5ea8975135a20d5cef8846faa5991
workflow-type: tm+mt
source-wordcount: '437'
ht-degree: 2%

---

# 一般事件 {#general-events}

>[!CONTEXTUALHELP]
>id="ajo_journey_event_custom"
>title="一般事件"
>abstract="事件允许您触发旅程，以便实时向流入旅程的个人发送消息。 对于此类型的事件，您只能添加标签和描述。 事件配置由数据工程师执行，无法编辑。"

事件允许您触发旅程，以便实时向流入旅程的个人发送消息。

对于此类型的事件，您只能添加标签和描述。 无法编辑配置的其余部分。 由技术用户执行。 请参阅[此页](../event/about-events.md)。

![](assets/general-events.png)

当您删除业务事件时，它会自动添加 **读取区段** 活动。 有关业务事件的更多信息，请参阅 [此部分](../event/about-events.md)

## 在特定时间内侦听事件 {#events-specific-time}

位于历程中的事件活动会无限期地侦听事件。 要仅在特定时间内侦听事件，必须为该事件配置超时。

然后，历程将在超时中指定的时间内侦听事件。 如果在该时间段内收到事件，则人员将在事件路径中流动。 如果没有，客户将进入超时路径，或结束其历程。

要为事件配置超时，请执行以下步骤：

1. 激活 **[!UICONTROL 定义事件超时]** 选项。

1. 指定历程将等待事件的时长。

1. 如果要在指定的超时内未收到任何事件时将个人发送到超时路径，请启用 **[!UICONTROL 设置超时路径]** 选项。 如果未启用此选项，则到达超时后，个人的历程将结束。

   ![](assets/event-timeout.png)

在此示例中，历程向客户发送第一个欢迎推送。 然后，仅当客户在次日进入餐厅时，才会发送餐饮折扣推送。 因此，我们为餐厅事件配置了1天的超时：

* 如果在欢迎推送后不到1天收到餐馆事件，则会发送餐饮折扣推送活动。
* 如果第二天未收到餐馆事件，则人员将通过超时路径流动。

请注意，如果要对位于 **[!UICONTROL 等待]** 活动中，您只需要为其中一个事件配置超时。

超时将应用于位于 **[!UICONTROL 等待]** 活动。 如果在指定的超时前未收到任何事件，则这些个人将流入一个超时路径，或结束其历程。

![](assets/event-timeout-group.png)
