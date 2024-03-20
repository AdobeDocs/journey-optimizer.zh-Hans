---
solution: Journey Optimizer
product: journey optimizer
title: 警报
description: 了解如何管理警报
feature: Journeys, Alerts
topic: Administration
role: User
level: Intermediate
exl-id: 0855ca5b-c7af-41c4-ad51-bed820ae5ecf
source-git-commit: f8d62a702824bcfca4221c857acf1d1294427543
workflow-type: tm+mt
source-wordcount: '553'
ht-degree: 0%

---

# 警报入门 {#alerts}

## 访问和订阅警报 {#alerting-capabilities}

发生失败时，您可以在Journey Optimizer通知中心获取系统警报（应用程序内警报）和/或接收电子邮件。

从 **警报** 菜单，您可以查看可用的警报并订阅它们。 当您的操作达到特定条件集时（例如系统违反阈值时可能会出现问题），将向您组织中订阅警报消息的任何用户发送警报消息。

<!--These messages can repeat over a pre-defined time interval until the alert has been resolved.-->

要了解有关Adobe Experience Platform中警报的更多信息，请参阅 [Adobe Experience Platform文档](https://experienceleague.adobe.com/docs/experience-platform/observability/alerts/overview.html?lang=zh-Hans){target="_blank"}.

在左侧菜单的下方 **管理**，单击 **警报**. 提供了两个针对Journey Optimizer的预配置警报： [历程自定义操作失败](#alert-custom-actions) 警报和 [读取区段触发器不成功](#alert-read-audiences) 警报。 这些警报详见下文。

您可以通过选择 **订阅** 选项来自 **警报** 仪表板。 使用相同的方法取消订阅。

![](assets/alert-subscribe.png)

您还可以通过以下方式订阅警报 [I/O事件通知](https://experienceleague.adobe.com/docs/experience-platform/observability/alerts/subscribe.html){target="_blank"}. 警报规则将整理到不同的订阅包中。 下文详细介绍了与特定Journey Optimizer警报对应的事件订阅。

如果发生意外行为，则向订阅者发送警报通知。 根据用户首选项，警报会通过电子邮件发送和/或直接在用户界面的右上角的Journey Optimizer通知中心内发送。 默认情况下，仅启用应用程序内警报。 要启用电子邮件警报，请参阅 [Adobe Experience Platform文档](https://experienceleague.adobe.com/docs/experience-platform/observability/alerts/ui.html#enable-email-alerts){target="_blank"}.

警报解决后，订阅者会收到“已解决”通知。

>[!CAUTION]
>
>特定于Adobe Journey Optimizer的警报仅适用于 **实时** 历程。 在测试模式下，历程不会触发警报。

## 历程自定义操作失败 {#alert-custom-actions}

如果自定义操作失败，此警报将警告您。 我们认为，过去5分钟内在特定自定义操作中发生超过1%的错误属于故障。 每30秒评估一次。

![](assets/alerts-custom-action.png)

过去5分钟内，出现以下情况时，将会解决自定义操作警报：

* 该自定义操作没有任何错误（或低于1%阈值的错误），

* 或者，没有任何配置文件达到该自定义操作。

对应于自定义操作警报的I/O事件订阅名称为 **历程自定义操作失败**.

## 读取受众触发器不成功 {#alert-read-audiences}

此警报会在以下情况下警告您 **读取受众** 活动在计划的执行时间后10分钟未处理任何配置文件。 此故障可能是由技术问题或受众为空导致的。

![](assets/alerts1.png)

警报 **读取受众** 活动仅适用于定期历程。 **读取受众** 实时历程中安排运行的活动 **一次** 或 **尽快** 将被忽略。

警报 **读取受众** 在配置文件进入 **读取受众** 节点。

与对应的I/O事件订阅名称 **读取区段触发器不成功** 警报为 **历程读取区段延迟、失败和错误**.

## 故障排除 {#alert-troubleshooting}

疑难解答 **读取受众** 警报，在Experience Platform界面中检查受众计数。

![](assets/alert-troubleshooting-0.png)

![](assets/alert-troubleshooting-1.png)

疑难解答 **自定义操作** 警报：

* 使用其他历程上的测试模式检查您的自定义操作：

  ![](assets/alert-troubleshooting-2.png)

* 检查您的历程报告以查看操作中的错误原因。

  ![](assets/alert-troubleshooting-3.png)

* 检查您的历程stepEvents以查找有关“failureReason”的更多信息。
* 检查您的自定义操作配置，并验证身份验证是否仍然正常。 例如，使用Postman执行手动检查。
