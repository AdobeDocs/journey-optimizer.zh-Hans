---
solution: Journey Orchestration
title: 一般事件
description: 了解如何使用常规事件
translation-type: tm+mt
source-git-commit: 55b9e5d8ed259ec6ed7746e835691d7d6261a8a4
workflow-type: tm+mt
source-wordcount: '358'
ht-degree: 1%

---

# 一般事件 {#section_ofg_jss_dgb}

![](../assets/do-not-localize/badge.png)

对于此类事件，只能添加标签和说明。 其他配置无法编辑。 由技术用户执行。 请参阅[此页](../event/about-events.md)。

![](../assets/general-events.png)

当您删除业务事件时，系统会自动添加&#x200B;**读取区段**&#x200B;活动。 有关业务事件的详细信息，请参阅[本节](../event/about-events.md)

## 在特定时间{#events-specific-time}侦听事件

位于旅程中的事件活动会无限期地监听事件。 要仅在特定时间内侦听事件，必须为事件配置超时。

然后，该旅程将在超时中指定的时间内侦听事件。 如果在此期间收到事件，则人员将流入事件路径。 否则，客户将进入超时路径，或结束其旅程。

要为事件配置超时，请执行以下步骤：

1. 从事件属性中激活&#x200B;**[!UICONTROL Enable the event timeout]**&#x200B;选项。

1. 指定旅程等待事件的时间。

1. 如果要在指定的超时内未收到事件时将个人发送到超时路径，请启用&#x200B;**[!UICONTROL Set the timeout path]**&#x200B;选项。 如果未启用此选项，则到达超时后，单个的旅程将结束。

   ![](../assets/event-timeout.png)

在此示例中，旅程向客户发送第一个欢迎推送。 然后，只有当顾客在次日进入餐厅时，它才会发送餐费折扣促销。 因此，我们为餐厅事件配置了1天超时：

* 如果在欢迎推送后不到1天内收到餐厅事件，则发送餐点折扣推送消息。
* 如果第二天没有收到餐馆事件，则该人将通过超时路径。

请注意，如果要在&#x200B;**[!UICONTROL Wait]**&#x200B;活动后对定位的多个事件配置超时，则只需在这些事件中配置一个超时。

超时将应用于&#x200B;**[!UICONTROL Wait]**&#x200B;活动之后所有事件。 如果在指定超时后未收到任何事件，则这些个人将流入一个超时路径，或结束其旅程。

![](../assets/event-timeout-group.png)
