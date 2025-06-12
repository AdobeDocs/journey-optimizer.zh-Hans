---
solution: Journey Optimizer
product: journey optimizer
title: 访问和订阅系统警报
description: 了解如何访问和订阅系统警报
feature: Journeys, Alerts
topic: Administration
role: User
level: Intermediate
exl-id: 0855ca5b-c7af-41c4-ad51-bed820ae5ecf
source-git-commit: da2fb137a8af82a8487638dc3d762377dd5dc506
workflow-type: tm+mt
source-wordcount: '654'
ht-degree: 0%

---

# 访问和订阅系统警报 {#alerts}

在构建历程和营销活动时，使用&#x200B;**警报**&#x200B;按钮在执行或发布之前检查和解决错误。 在[此页面](../building-journeys/troubleshooting.md)上了解如何对您的历程进行故障排除。 在[此页面](../campaigns/review-activate-campaign.md)上了解如何查看营销活动。

您还可以订阅Adobe Journey Optimizer系统警报，如本页所述。

## 访问和订阅警报 {#alerting-capabilities}

发生失败时，您可以在Journey Optimizer通知中心获取系统警报（应用程序内警报）和/或接收电子邮件。

从&#x200B;**警报**&#x200B;菜单中，可以查看可用的警报并订阅它们。 当您的操作达到特定条件集时（例如系统违反阈值时可能会出现问题），将向您组织中订阅警报消息的任何用户发送警报消息。

<!--These messages can repeat over a pre-defined time interval until the alert has been resolved.-->

在[Adobe Experience Platform文档](https://experienceleague.adobe.com/docs/experience-platform/observability/alerts/overview.html?lang=zh-Hans){target="_blank"}中了解有关Adobe Experience Platform中警报的更多信息。

在左侧菜单的&#x200B;**管理**&#x200B;下，单击&#x200B;**警报**。 有两个Journey Optimizer的预配置警报可用： [历程自定义操作失败](#alert-custom-actions)警报和[读取受众触发器不成功](#alert-read-audiences)警报。 这些警报详见下文。

您可以通过从&#x200B;**警报**&#x200B;仪表板中选择&#x200B;**订阅**&#x200B;选项，从用户界面中单独订阅每个警报。 使用相同的方法取消订阅。

![](assets/alert-subscribe.png)

您还可以通过[I/O事件通知](https://experienceleague.adobe.com/docs/experience-platform/observability/alerts/subscribe.html){target="_blank"}订阅警报。 警报规则将整理到不同的订阅包中。 下文详细介绍了与特定Journey Optimizer警报对应的事件订阅。

如果发生意外行为，则向订阅者发送警报通知。 根据用户首选项，警报会通过电子邮件发送和/或直接在用户界面的右上角的Journey Optimizer通知中心内发送。 默认情况下，仅启用应用程序内警报。 要启用电子邮件警报，请参阅[Adobe Experience Platform文档](https://experienceleague.adobe.com/docs/experience-platform/observability/alerts/ui.html#enable-email-alerts){target="_blank"}。

警报解决后，订阅者会收到“已解决”通知。

>[!CAUTION]
>
>Adobe Journey Optimizer特定警报仅适用于&#x200B;**实时**&#x200B;历程。 在测试模式下，历程不会触发警报。

## 历程自定义操作失败 {#alert-custom-actions}

如果自定义操作失败，此警报将警告您。 我们认为，过去5分钟内在特定自定义操作中发生超过1%的错误属于故障。 每30秒评估一次。

![](assets/alerts-custom-action.png)

过去5分钟内，出现以下情况时，将会解决自定义操作警报：

* 该自定义操作没有任何错误（或低于1%阈值的错误），

* 或者，没有任何配置文件达到该自定义操作。

与自定义操作警报对应的I/O事件订阅名称为&#x200B;**历程自定义操作失败**。

## 读取受众触发器不成功 {#alert-read-audiences}

如果&#x200B;**读取受众**&#x200B;活动在计划执行时间后的10分钟内未处理任何配置文件，则此警报会警告您。 此故障可能是由技术问题或受众为空导致的。 如果这种失败是由技术问题引起的，请注意，根据问题的类型，重试仍然可能发生（例如：如果导出作业创建失败，我们将每10mn重试一次，最长为1h）。

![](assets/alerts1.png)

有关&#x200B;**读取受众**&#x200B;活动的警报仅适用于定期历程。 **实时历程中的读取受众**&#x200B;活动计划运行&#x200B;**一次**&#x200B;或&#x200B;**尽快**&#x200B;被忽略。

当配置文件进入&#x200B;**读取受众**&#x200B;节点时，已解决&#x200B;**读取受众**&#x200B;上的警报。

与&#x200B;**读取受众触发器失败**&#x200B;警报对应的I/O事件订阅名称为&#x200B;**历程读取受众延迟、失败和错误**。

## 故障排除 {#alert-troubleshooting}

要对&#x200B;**读取受众**&#x200B;警报进行故障排除，请在Experience Platform界面中检查您的受众计数。

![](assets/alert-troubleshooting-0.png)

![](assets/alert-troubleshooting-1.png)

要对&#x200B;**自定义操作**&#x200B;警报进行故障排除，请执行以下操作：

* 使用其他历程上的测试模式检查您的自定义操作：

  ![](assets/alert-troubleshooting-2.png)

* 检查您的历程报告以查看操作中的错误原因。

  ![](assets/alert-troubleshooting-3.png)

* 检查您的历程stepEvents以查找有关“failureReason”的更多信息。

* 检查您的自定义操作配置，并验证身份验证是否仍然正常。 例如，使用Postman执行手动检查。
