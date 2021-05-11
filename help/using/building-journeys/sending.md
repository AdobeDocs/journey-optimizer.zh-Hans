---
title: 开始旅程执行
description: 了解如何开始旅程和发送消息
translation-type: tm+mt
source-git-commit: 4ff255b6b57823a1a4622dbc62b4b8886fd956a0
workflow-type: tm+mt
source-wordcount: '304'
ht-degree: 0%

---


# 历程执行{#message-execution}

![](../assets/do-not-localize/badge.png)

## 测试您的旅程

您可以使用测试用户档案测试您的旅程。 建议执行此步骤以验证您的设置和消息。

请阅读此[部分](testing-the-journey.md)了解更多信息。

## 激活您的旅程

您必须发布您的旅程以激活它。

![](../assets/jo-journeyuc2_32bis.png)

请阅读此[部分](publishing-the-journey.md)了解更多信息。


发布后，您可以使用专用的报告工具监控您的旅程，以衡量您旅程的有效性。

![](../assets/jo-dynamic_report_journey_12.png)

[了解有关报告的更多信息](../reports/live-report.md)

## 发送邮件 {#send-messages}

当您的邮件定义并发布了内容时，可以通过[旅程](journey.md)发送该邮件。

>[!NOTE]
>
>您可以向旅程添加仍处于草稿模式的消息，但请确保在发布该旅程之前已发布该消息。

发送消息后，您可以通过多个指示器监视其执行。 [了解有关监视消息执行的更多信息](../message-monitoring.md)。

## 计划消息{#schedule-messages}

可以通过[旅程](journey.md)中的&#x200B;**[!UICONTROL Read segment]**&#x200B;活动安排消息。 您可以指定区段将何时进入旅程。 [进一步了解阅读细分活动](read-segment.md)。

为此，请按照以下步骤操作：

1. 编辑旅程，拖放&#x200B;**[!UICONTROL Read segment]**&#x200B;活动并配置开始。 [了解有关配置“阅读”区段活动的更多信息](read-segment.md#configuring-segment-trigger-activity)。

1. 单击&#x200B;**[!UICONTROL Edit journey schedule]**&#x200B;链接以访问旅程的属性。

   ![](../assets/message-read-segment-schedule.png)

1. 配置&#x200B;**[!UICONTROL Scheduler type]**&#x200B;字段：从列表中选择所需的值，以使区段在特定日期/时间或循环的基础上进入旅程。

   >[!NOTE]
   >
   >**[!UICONTROL Schedule]**&#x200B;部分仅在&#x200B;**[!UICONTROL Read Segment]**&#x200B;活动已放入画布时可用。

   ![](../assets/message-read-segment-scheduler.png)

1. 如果您选择&#x200B;**[!UICONTROL Once]**，请定义段将进入旅程的特定日期和时间。

   ![](../assets/message-read-segment-scheduler-once.png)

1. 如果选择循环方法，请编辑开始日期和时间。 您还可以定义可选的结束日期和时间。

   ![](../assets/message-read-segment-scheduler-daily.png)

   >[!NOTE]
   >
   >默认情况下，区段会输入旅程&#x200B;**[!UICONTROL As soon as possible]**，即在旅程发布后1小时。

1. 单击&#x200B;**[!UICONTROL OK]**&#x200B;保存更改。

<!--Unitary messages that are triggered by an event within a journey cannot be scheduled.-->
