---
solution: Journey Optimizer
product: journey optimizer
title: 一般事件
description: 了解如何使用一般事件
feature: Journeys, Events
topic: Content Management
role: User
level: Intermediate
keywords: 自定义、常规、事件、历程
exl-id: b1813122-7031-452e-9ac5-a4ea7c6dc57c
source-git-commit: 343e7bbebf35711259d2f3392f1ce5658865599a
workflow-type: tm+mt
source-wordcount: '603'
ht-degree: 21%

---

# 一般事件 {#general-events}

>[!CONTEXTUALHELP]
>id="ajo_journey_event_custom"
>title="单一事件"
>abstract="事件允许您统一触发历程，向流入历程的个人实时发送消息。对于此类事件，只能添加标签和描述。事件配置由数据工程师执行，不可编辑。"

>[!CONTEXTUALHELP]
>id="ajo_journey_event_business_canvas"
>title="业务事件"
>abstract="这些事件允许您使用非轮廓相关事件启动历程。当该事件触发时，您将能够向轮廓受众发送消息。对于此类事件，只能添加标签和描述。事件配置由技术用户执行，不可编辑。"

事件允许您统一触发历程，向流入历程的个人实时发送消息。

对于此类事件，只能添加标签和描述。配置的其他部分无法编辑。 该操作由技术用户执行。 请参阅[此页](../event/about-events.md)。

![](assets/general-events.png)

删除业务活动时，该活动会自动添加&#x200B;**读取受众**&#x200B;活动。 有关业务活动的详细信息，请参阅[此部分](../event/about-events.md)

## 在特定时间监听事件 {#events-specific-time}

位于历程中的事件活动可无限期地侦听事件。 要仅在特定时间内侦听事件，必须为事件配置超时。

然后，该历程将在超时指定的时间内侦听事件。 如果在该时间段内收到事件，则该人员将流入事件路径。 如果没有，则客户将流入超时路径（如果已定义），或将继续该历程。

如果未定义超时路径，则超时设置将充当等待活动，从而使配置文件等待一段时间，如果事件发生在该等待结束之前，则该时间可能会停止。 如果要在超时后从历程中排除用户档案，则必须设置超时路径。

要为事件配置超时，请执行以下步骤：

1. 从事件属性激活&#x200B;**[!UICONTROL 定义事件超时]**&#x200B;选项。

1. 指定历程将等待事件的时间量。 最长持续时间为&#x200B;**90天**。

1. 如果在指定的超时时间内未收到任何事件，则最佳实践是将个人发送到超时路径中。 为此，启用&#x200B;**[!UICONTROL 设置超时路径]**&#x200B;选项。 在这种情况下，一旦达到超时，个人将继续该历程。 我们建议您始终启用&#x200B;**[!UICONTROL 设置超时路径]**&#x200B;选项。

   ![](assets/event-timeout.png)

在此示例中，历程在客户进入大厅后向客户发送第一封欢迎电子邮件。 然后，仅当客户在隔天进入餐厅时，它才会发送餐饮折扣电子邮件。 因此，我们将restaurant事件配置为1天超时：

* 如果在欢迎电子邮件后不到1天收到餐厅事件，则发送餐饮折扣电子邮件。
* 如果在第二天未收到餐馆事件，则该人员将流过超时路径。

请注意，如果要在&#x200B;**[!UICONTROL 等待]**&#x200B;活动之后放置的多个事件上配置超时，则只需在这些事件之一上配置超时。

定义的超时适用于位于&#x200B;**[!UICONTROL 等待]**&#x200B;活动之后的所有事件：

* 如果在超时持续时间内收到一个事件，则单个事件将流入所接收事件的路径。
* 如果在超时持续时间内未收到任何事件，则单个事件将流入已定义超时的事件的超时分支。

![](assets/event-timeout-group.png)
