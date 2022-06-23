---
title: 历程实时报告
description: 了解如何使用历程实时报告中的数据
feature: Reporting
topic: Content Management
role: User
level: Intermediate
exl-id: e3781f79-7c8d-4512-b44f-835639b1471f
source-git-commit: 47b1c2832f82a5c168cd03f1d1b43a9223c945b3
workflow-type: tm+mt
source-wordcount: '896'
ht-degree: 1%

---

# 历程实时报告 {#journey-live-report}

历程实时报表可直接从您的历程中通过 **[!UICONTROL Live report]** 按钮。

![](assets/report_1.png)

历程 **[!UICONTROL Live report]** 页面中将显示以下选项卡：

* [历程](#journey-live)
* [电子邮件](#email-live)
* [推送](#push-live)
* [短信](#sms-live)

历程 **[!UICONTROL Live report]** 会分为不同的小组件，用于详细描述历程的成功和错误。 如果需要，可以调整每个小组件的大小并将其删除。 有关此内容的更多信息，请参阅此内容 [部分](live-report.md#modify-dashboard).

## 历程选项卡 {#journey-live}

从您的历程 **[!UICONTROL Live report]**, **[!UICONTROL Journey]** 选项卡可让您清楚地查看有关历程的最重要跟踪数据。

![](assets/report_journey_2.png)

**[!UICONTROL Journey Performance]** 允许您分步查看目标用户档案在历程中的路径。

的 **[!UICONTROL Journey Statistics]** 小组件显示以下KPI:

* **[!UICONTROL Entered profiles]**:到达历程的登入事件的个人总数。

* **[!UICONTROL Exited profiles]**:退出历程的个人总数。

* **[!UICONTROL Failed individual journeys]**:未成功执行的各个历程的总数。

![](assets/report_journey_3.png)

的 **[!UICONTROL Event executed over the last 24 hours]** 和 **[!UICONTROL Events]** 小组件允许您通过概要数字、图表和表格查看哪些事件成功执行。

![](assets/report_journey_4.png)

的 **[!UICONTROL Action executed over the last 24 hours]** 和 **[!UICONTROL Actions executed and errors]** 小组件表示在触发操作时发生的最成功操作和错误。 操作图、表和概要数字包含可用于操作的数据，例如：

* **[!UICONTROL Actions executed]**:为历程成功执行的操作总数。

* **[!UICONTROL Error in actions]**:操作发生的错误总数。

## “电子邮件”选项卡 {#email-live}

从您的历程 **[!UICONTROL Live report]**, **[!UICONTROL Email]** 选项卡详细列出了与历程中发送的电子邮件投放相关的主要信息。

有关特定电子邮件投放的详细报告，请参阅 [电子邮件实时报表](email-live-report.md) 中。

![](assets/report_email_1.png)

的 **[!UICONTROL Email Sending Statistics]** 小组件详细介绍与您的消息相关的主要信息：

* **[!UICONTROL Delivered]**:成功发送的消息数。

* **[!UICONTROL Bounces]**:在投放和自动回访处理过程中累积的错误总数。

* **[!UICONTROL Errors]**:投放期间发生的阻止将其发送到用户档案的错误总数。

的 **[!UICONTROL Sending metrics by Email]** 表格和 **[!UICONTROL Email Summary]** 图形详细说明了交付的成功：

* **[!UICONTROL Sent]**:投放的发送总数。

* **[!UICONTROL Delivered]**:成功发送的消息数。

* **[!UICONTROL Bounces]**:在投放和自动回访处理过程中累积的错误总数。

* **[!UICONTROL Errors]**:投放期间发生的阻止将其发送到用户档案的错误总数。

* **[!UICONTROL Opens]**:投放中消息打开的次数。

* **[!UICONTROL Clicks]**:在投放中点击内容的次数。

* **[!UICONTROL Unsubscribe]**:退订链接的点击次数。

* **[!UICONTROL Spam complaints]**:将消息声明为垃圾邮件或垃圾邮件的次数。

![](assets/report_email_2.png)

的 **[!UICONTROL Bounce Reasons]**, **[!UICONTROL Bounce categories]** 和 **[!UICONTROL Hard and bounce - by Email]** 小组件包含与弹回的消息相关的可用数据，例如：

* **[!UICONTROL Hard bounce]**:永久错误的总数，如错误的电子邮件地址。 这涉及显式声明地址无效的错误消息，如未知用户。

* **[!UICONTROL Soft bounce]**:临时错误（如完整收件箱）的总数。

* **[!UICONTROL Ignored]**:临时（如“不在办公室”）或技术错误（例如，如果发件人类型为邮递员）的总数。

![](assets/report_email_3.png)

的 **[!UICONTROL Error Reasons]** 和 **[!UICONTROL Exclude Reasons]** 图形和表格允许您查看在投放期间发生的错误和排除项。

的 **[!UICONTROL Email - Top recipient domain]** 图表和表格详细列出了收件人最常使用哪些域来打开电子邮件。

![](assets/live_report_7.png)

>[!NOTE]
>
>仅当在电子邮件中插入决策时，选件小组件和量度才可用。 有关决策管理的详细信息，请参阅此 [页面](../offers/get-started/starting-offer-decisioning.md).

的 **[!UICONTROL Offers statistic]** 和 **[!UICONTROL Offers statistics]** 随着时间的推移，小组件可衡量选件的成功以及对目标受众的影响。 它使用KPI详细描述与消息相关的主要信息：

* **[!UICONTROL Offer sent]**:选件的发送总数。

* **[!UICONTROL Offer impression]**:在投放中打开选件的次数。

* **[!UICONTROL Offer clicks]**:在投放中点击选件的次数。

## “推送”选项卡 {#push-live}

从您的历程 **[!UICONTROL Live report]**, **[!UICONTROL Push]** 选项卡详细列出了与历程中发送的推送投放相关的主要信息。

有关特定推送投放的详细报告，请参阅 [推送实时报表](push-live-report.md) 中。

![](assets/report_push_1.png)

**[!UICONTROL Push notification sending performance]**, **[!UICONTROL Push notification summary]** 和 **[!UICONTROL Sending metrics - by Push]** 小组件详细介绍与您的消息相关的主要信息：

* **[!UICONTROL Sent]**:投放的发送总数。

* **[!UICONTROL Delivered]**:成功发送的消息数。

* **[!UICONTROL Bounces]**:在投放和自动回访处理过程中累积的错误总数。

* **[!UICONTROL Errors]**:投放期间发生的阻止将其发送到用户档案的错误总数。

* **[!UICONTROL Opens]**:投放中消息打开的次数。

* **[!UICONTROL Actions]**:已送达推送通知的操作总数，例如按钮单击或解除。

* **[!UICONTROL Engagements]**:此推送通知的打开和操作总数，例如用户档案打开推送或单击按钮时。

![](assets/report_push_3.png)

的 **[!UICONTROL Error Reasons]** 和 **[!UICONTROL Exclude Reasons]** 图形和表格允许您查看在投放期间发生的错误和排除项。

的 **[!UICONTROL Sending statistics - Failed]** 小组件允许您查看发生了多少错误和跳出。

![](assets/report_push_2.png)

的 **[!UICONTROL Tracking by platform]**, **[!UICONTROL Sending by platform]** 和 **[!UICONTROL Breakdown by platform]** 图形和表格根据操作系统详细列出了推送通知的成功情况。

## “短信”选项卡 {#sms-live}

的 **[!UICONTROL SMS - Sending statistics]** 表格详细说明了交付的成功：

* **[!UICONTROL Targeted]**:符合此投放目标用户档案的用户配置文件数。

* **[!UICONTROL Excluded]**:未收到消息的从定向用户档案中排除的用户用户档案数。

* **[!UICONTROL Sent]**:投放的发送总数。

* **[!UICONTROL Delivered]**:成功发送的消息数。

* **[!UICONTROL Opens]**:投放中消息打开的次数。

* **[!UICONTROL Clicks]**:在投放中点击内容的次数。

* **[!UICONTROL Bounces]**:在投放和自动回访处理过程中累积的错误总数。

* **[!UICONTROL Errors]**:投放期间发生的阻止将其发送到用户档案的错误总数。

的 **[!UICONTROL SMS Summary]** 图形详细说明了交付的成功：

* **[!UICONTROL Delivered]**:成功发送的消息数。

* **[!UICONTROL Bounces]**:在投放和自动回访处理过程中累积的错误总数。

* **[!UICONTROL Errors]**:投放期间发生的阻止将其发送到用户档案的错误总数。

的 **[!UICONTROL Exclude Reasons]** 图形和表格允许您查看在投放期间发生的错误和排除项。
