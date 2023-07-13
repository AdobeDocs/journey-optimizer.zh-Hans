---
solution: Journey Optimizer
product: journey optimizer
title: 警报
description: 了解如何管理警报
feature: Alerts
topic: Administration
role: Admin
level: Intermediate
exl-id: 0855ca5b-c7af-41c4-ad51-bed820ae5ecf
source-git-commit: 72bd00dedb943604b2fa85f7173cd967c3cbe5c4
workflow-type: tm+mt
source-wordcount: '258'
ht-degree: 6%

---

# 警报入门 {#alerts}

Journey Optimizer可利用Adobe Experience Platform警报功能。 这允许您通过用户界面访问系统警报。 您可以查看可用的警报并订阅它们。

当达到操作中的特定条件集时（例如系统违反阈值时可能出现的问题），将向组织中订阅了警报消息的任何用户发送警报消息。 这些消息可在预定义的时间间隔内重复出现，直到警报得到解决为止。

了解有关Adobe Experience Platform中警报的更多信息 [文档](https://experienceleague.adobe.com/docs/experience-platform/observability/alerts/overview.html?lang=zh-Hans).
要了解如何订阅和配置警报，请参阅此 [页面](https://experienceleague.adobe.com/docs/experience-platform/observability/alerts/ui.html).

>[!AVAILABILITY]
>
>“读取受众触发器不成功”警报的一些设计更改正在进行中，因此该警报现已暂停，并且已从用户界面中临时删除。 发布这些更改后，警报将再次显示，您可以订阅它。
>

在左侧菜单的下方 **管理**，单击 **警报**.

<!--A pre-configured alert for Journey Optimizer is available. This alert will warn you if a read segment node has not processed any profile during the defined time frame.

![](assets/alerts1.png)-->

如果发生意外行为，将通过界面右上角的电子邮件向警报的订阅者发送警报通知。

<!--![](assets/alerts2.png)-->


时间 [在Adobe Experience Platform UI中查看警报规则](https://experienceleague.adobe.com/docs/experience-platform/observability/alerts/ui.html)，您可以单独订阅每个规则。 通过订阅警报时 [I/O事件通知](https://experienceleague.adobe.com/docs/experience-platform/observability/alerts/subscribe.html)但是，警报规则会整理到不同的订阅包中。

<!--The I/O event subscription name corresponding to the Read segment alert is: "Journey read segment Delays, Failures and Errors".

>[!WARNING]
>
>These alerts apply only to live journeys. Alerts will not be triggered for journeys in test mode.-->
