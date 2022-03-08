---
title: 开始历程执行
description: 了解如何开始您的历程并发送消息
source-git-commit: 51254efaab08a572def118d475dc18f74c9d29b7
workflow-type: tm+mt
source-wordcount: '304'
ht-degree: 3%

---


# 历程执行 {#message-execution}

## 测试您的历程

您可以使用测试用户档案测试您的历程。 建议此步骤验证您的设置和消息。

在中了解详情 [部分](testing-the-journey.md).

## 激活您的历程

您必须发布历程才能激活它。

![](../assets/jo-journeyuc2_32bis.png)

在中了解详情 [部分](publishing-the-journey.md).


发布后，您可以使用专用的报告工具监控您的历程以衡量历程的有效性。

![](../assets/jo-dynamic_report_journey_12.png)

[了解有关报表的更多信息](../reports/live-report.md)

## 发送邮件 {#send-messages}

在消息定义了内容并发布后，即可通过 [历程](journey.md).

>[!NOTE]
>
>您可以向历程添加仍处于草稿模式的消息，但请确保在发布历程之前发布了该消息。

发送消息后，您可以通过多个指示器监控其执行情况。 [了解有关监视消息执行的更多信息](../message-monitoring.md).

## 计划消息发送 {#schedule-messages}

可以通过 **[!UICONTROL Read Segment]** 活动 [历程](journey.md). 您可以指定区段将何时进入历程。 [了解有关读取区段活动的更多信息](read-segment.md).

为此，请执行以下步骤：

1. 编辑历程，拖放 **[!UICONTROL Read Segment]** 活动并开始配置。 [了解有关配置读取区段活动的更多信息](read-segment.md#configuring-segment-trigger-activity).

1. 单击 **[!UICONTROL Edit journey schedule]** 用于访问历程属性的链接。

   ![](../assets/message-read-segment-schedule.png)

1. 配置 **[!UICONTROL Scheduler type]** 字段：从列表中选择所需的值，以使区段在特定日期/时间或定期进入历程。

   >[!NOTE]
   >
   >的 **[!UICONTROL Schedule]** 部分仅在 **[!UICONTROL Read Segment]** 活动已放入画布中。

   ![](../assets/message-read-segment-scheduler.png)

1. 如果您选择 **[!UICONTROL Once]**，定义区段进入历程的特定日期和时间。

   ![](../assets/message-read-segment-scheduler-once.png)

1. 如果选择循环方法，请编辑开始日期和时间。 您还可以定义可选的结束日期和时间。

   ![](../assets/message-read-segment-scheduler-daily.png)

   >[!NOTE]
   >
   >默认情况下，区段会进入历程 **[!UICONTROL As soon as possible]**，表示历程发布1小时后。

1. 单击 **[!UICONTROL OK]** 以保存更改。

<!--Unitary messages that are triggered by an event within a journey cannot be scheduled.-->
