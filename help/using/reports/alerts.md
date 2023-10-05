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
source-git-commit: 6386a5ee5a0d1f221beab67f43636c599531736a
workflow-type: tm+mt
source-wordcount: '378'
ht-degree: 4%

---

# 警报入门 {#alerts}

Journey Optimizer可利用Adobe Experience Platform的警报功能。 这允许您通过用户界面访问系统警报。 您可以查看可用的警报并订阅它们。

当您的操作达到特定条件集时（例如系统违反阈值时可能会出现问题），将向组织中订阅警报消息的任何用户发送警报消息。

<!--These messages can repeat over a pre-defined time interval until the alert has been resolved.-->

在Adobe Experience Platform中了解关于警报的更多信息 [文档](https://experienceleague.adobe.com/docs/experience-platform/observability/alerts/overview.html?lang=zh-Hans).

要了解如何订阅和配置警报，请参阅此 [页面](https://experienceleague.adobe.com/docs/experience-platform/observability/alerts/ui.html).

>[!AVAILABILITY]
>
>“读取受众触发器失败”警报的一些设计更改正在进行中，因此此警报暂时暂停，并从用户界面中暂时删除。 发布这些更改后，警报将再次显示，您可以订阅它。

在左侧菜单的下方 **管理**，单击 **警报**. 适用于Journey Optimizer的预配置警报可用。 如果自定义操作失败，此警报将警告您。 我们认为，过去5分钟内在特定自定义操作中发生超过1%的错误属于故障。 每30秒评估一次。

![](assets/alerts-custom-action.png)


<!--A pre-configured alert for Journey Optimizer is available. This alert will warn you if a read segment node has not processed any profile during the defined time frame.

![](assets/alerts1.png)-->

如果发生意外行为，将根据用户首选项，通过电子邮件或直接在界面右上角的Journey Optimizer中，向警报的订阅者发送警报通知。

警报解决后，您会收到“已解决”通知。 对于自定义操作警报，发生这种情况有两个原因：
* 在过去5分钟内，该自定义操作没有任何错误（或低于1%阈值的错误）。
* 没有配置文件达到该自定义操作。

时间 [在Adobe Experience Platform UI中查看警报规则](https://experienceleague.adobe.com/docs/experience-platform/observability/alerts/ui.html)，您可以单独订阅每个规则。 通过订阅警报时 [I/O事件通知](https://experienceleague.adobe.com/docs/experience-platform/observability/alerts/subscribe.html)但是，警报规则会整理到不同的订阅包中。 与自定义操作警报相对应的I/O事件订阅名称为“历程自定义操作失败”。

<!--The I/O event subscription name corresponding to the Read segment alert is: "Journey read segment Delays, Failures and Errors".-->

>[!WARNING]
>
>这些警报仅适用于实时历程。 在测试模式下，历程不会触发警报。

