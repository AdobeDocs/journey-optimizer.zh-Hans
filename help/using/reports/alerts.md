---
solution: Journey Optimizer
product: journey optimizer
title: 警报
description: 了解如何管理警报
feature: Alerts
topic: Administration
role: Admin
level: Intermediate
source-git-commit: 63c52f04da9fd1a5fafc36ffb5079380229f885e
workflow-type: tm+mt
source-wordcount: '277'
ht-degree: 6%

---

# 警报入门 {#alerts}

Journey Optimizer利用Adobe Experience Platform警报功能。 这允许您通过用户界面访问系统警报。 您可以查看可用的警报并订阅它们。当您操作中达到一组特定条件（例如，系统违反阈值时可能出现的问题）时，会向组织中订阅这些条件的任何用户发送警报消息。 这些消息可以在预定义的时间间隔内重复，直到警报得到解析。

在Adobe Experience Platform中了解有关警报的更多信息 [文档](https://experienceleague.adobe.com/docs/experience-platform/observability/alerts/overview.html?lang=zh-Hans).
要了解如何订阅和配置警报，请参阅此 [页面](https://experienceleague.adobe.com/docs/experience-platform/observability/alerts/ui.html).

在左侧菜单的 **管理**，单击 **警报**. 提供了预配置的Journey Optimizer警报。 如果读取区段节点在定义的时间范围内未处理任何配置文件，则此警报将警告您。

![](assets/alerts1.png)

如果发生此类意外行为，则会通过界面右上角的电子邮件和应用程序内通知向警报的订阅者发送警报通知。

![](assets/alerts2.png)

When [在平台UI中查看警报规则](https://experienceleague.adobe.com/docs/experience-platform/observability/alerts/ui.html)，则可以单独订阅每个规则。 通过订阅警报时 [I/O事件通知](https://experienceleague.adobe.com/docs/experience-platform/observability/alerts/subscribe.html)但是，警报规则会组织到不同的订阅包中。 与读取区段警报对应的I/O事件订阅名称为：“历程读取区段延迟、失败和错误”。

>[!WARNING]
>
>这些警报仅适用于实时历程。 在测试模式下，不会触发历程的警报。