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
source-git-commit: 731eb471c5765b0d3efbc9354c64c32cc5e56516
workflow-type: tm+mt
source-wordcount: '210'
ht-degree: 8%

---

# 警报入门 {#alerts}

Journey Optimizer利用Adobe Experience Platform警报功能。 这允许您通过用户界面访问系统警报。 您可以查看可用的警报并订阅它们。当您操作中达到一组特定条件（例如，系统违反阈值时可能出现的问题）时，会向组织中订阅这些条件的任何用户发送警报消息。 这些消息可以在预定义的时间间隔内重复，直到警报得到解析。

在Adobe Experience Platform中了解有关警报的更多信息 [文档](https://experienceleague.adobe.com/docs/experience-platform/observability/alerts/overview.html?lang=zh-Hans).
要了解如何订阅和配置警报，请参阅此 [页面](https://experienceleague.adobe.com/docs/experience-platform/observability/alerts/ui.html).

在左侧菜单的 **管理**，单击 **警报**.

<!--A pre-configured alert for Journey Optimizer is available. This alert will warn you if a read segment node has not processed any profile during the defined time frame.

![](assets/alerts1.png)-->

如果发生此类意外行为，则会通过界面右上角的电子邮件向警报的订阅者发送警报通知。

<!--![](assets/alerts2.png)-->

When [在Adobe Experience Platform UI中查看警报规则](https://experienceleague.adobe.com/docs/experience-platform/observability/alerts/ui.html)，则可以单独订阅每个规则。 通过订阅警报时 [I/O事件通知](https://experienceleague.adobe.com/docs/experience-platform/observability/alerts/subscribe.html)但是，警报规则会组织到不同的订阅包中。

<!--The I/O event subscription name corresponding to the Read segment alert is: "Journey read segment Delays, Failures and Errors".

>[!WARNING]
>
>These alerts apply only to live journeys. Alerts will not be triggered for journeys in test mode.-->
