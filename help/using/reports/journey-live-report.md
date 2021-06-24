---
title: 历程实时报告
description: 了解如何使用历程实时报告中的数据
feature: 报表
topic: 内容管理
role: User
level: Intermediate
source-git-commit: c883930674b3856f1f7857f4072419be8c9d8738
workflow-type: tm+mt
source-wordcount: '698'
ht-degree: 1%

---

# 历程实时报告 {#journey-live-report}

历程实时报告可使用&#x200B;**[!UICONTROL Live report]**&#x200B;按钮直接从历程访问。

![](../assets/report_1.png)

将显示历程&#x200B;**[!UICONTROL Live report]**&#x200B;页面，其中包含以下选项卡：

* [历程](#journey-live)
* [电子邮件](#email-live)
* [推送](#push-live)

历程&#x200B;**[!UICONTROL Live report]**&#x200B;分为不同的小组件，用于详细描述历程的成功和错误。 如果需要，可以调整每个小组件的大小并将其删除。 有关此内容的详细信息，请参阅此[部分](live-report.md#modify-dashboard)。

## 历程选项卡 {#journey-live}

在历程&#x200B;**[!UICONTROL Live report]**&#x200B;中， **[!UICONTROL Journey]**&#x200B;选项卡可以清晰地显示有关历程最重要的跟踪数据。

![](../assets/report_journey_2.png)

**[!UICONTROL Journey Performance]** 允许您分步查看目标用户档案在历程中的路径。

**[!UICONTROL Journey Statistics]**&#x200B;小组件显示以下KPI:

* **[!UICONTROL Entered profiles]**:到达历程的登入事件的个人总数。

* **[!UICONTROL Exited profiles]**:退出历程的个人总数。

* **[!UICONTROL Failed individual journey]**:未成功执行的各个历程的总数。

![](../assets/report_journey_3.png)

通过&#x200B;**[!UICONTROL Event executed over the last 24 hours]**、**[!UICONTROL Events executed]**&#x200B;和&#x200B;**[!UICONTROL Events]**&#x200B;小组件，您可以通过概要数字、图表和表格查看成功执行了其中某个事件。

![](../assets/report_journey_4.png)

**[!UICONTROL Action executed over the last 24 hours]** 和小 **[!UICONTROL Actions executed and errors]** 组件表示在触发操作时发生的最成功的操作和错误。操作图、表和概要数字包含可用于操作的数据，例如：

* **[!UICONTROL Actions successfully executed]**:为历程成功执行的操作总数。

* **[!UICONTROL Error in action]**:操作发生的错误总数。

## “电子邮件”选项卡 {#email-live}

在您的历程&#x200B;**[!UICONTROL Live report]**&#x200B;中， **[!UICONTROL Email]**&#x200B;选项卡详细介绍了与在历程中发送的电子邮件投放相关的主要信息。

有关特定电子邮件投放的详细报告，请参阅[电子邮件实时报告](email-live-report.md)一节。

![](../assets/report_email_1.png)

**[!UICONTROL Email Sending Statistics]**&#x200B;小组件详细列出了与您的消息相关的主要信息：

* **[!UICONTROL Delivered]**:已成功发送的消息数，与已发送消息的总数有关。

* **[!UICONTROL Bounces]**:在投放和自动回访处理过程中累积的与已发送消息总数有关的错误总数。

* **[!UICONTROL Errors]**:投放期间发生的阻止将其发送到用户档案的错误总数。

**[!UICONTROL Sending metrics by Email]**&#x200B;表和&#x200B;**[!UICONTROL Email Summary]**&#x200B;图详细说明了交付的成功：

* **[!UICONTROL Sent]**:投放的发送总数。

* **[!UICONTROL Delivered]**:已成功发送的消息数，与已发送消息的总数有关。

* **[!UICONTROL Bounces]**:在投放和自动回访处理过程中累积的与已发送消息总数有关的错误总数。

* **[!UICONTROL Errors]**:投放期间发生的阻止将其发送到用户档案的错误总数。

* **[!UICONTROL Opens]**:投放中消息打开的次数。

* **[!UICONTROL Clicks]**:在投放中点击内容的次数。

* **[!UICONTROL Unsubscribe]**:退订链接的点击次数。

* **[!UICONTROL Spam complaints]**:将消息声明为垃圾邮件或垃圾邮件的次数。

![](../assets/report_email_2.png)

**[!UICONTROL Bounce Reasons]**、**[!UICONTROL Bounce categories]**&#x200B;和&#x200B;**[!UICONTROL Hard and bounce - by Email]**&#x200B;小组件包含与弹回消息相关的可用数据，例如：

* **[!UICONTROL Hard bounce]**:永久错误的总数，如错误的电子邮件地址。这涉及显式声明地址无效的错误消息，如未知用户。

* **[!UICONTROL Soft bounce]**:临时错误（如完整收件箱）的总数。

* **[!UICONTROL Ignored]**:临时（如“不在办公室”）或技术错误（例如，如果发件人类型为邮递员）的总数。

**[!UICONTROL Error Reasons]**&#x200B;图表和表允许您查看在投放期间发生的错误。

## “推送”选项卡 {#push-live}

在您的历程&#x200B;**[!UICONTROL Live report]**&#x200B;中， **[!UICONTROL Push]**&#x200B;选项卡详细介绍了与在历程中发送的推送投放相关的主要信息。

有关特定推送投放的详细报告，请参阅[推送实时报告](push-live-report.md)一节。

![](../assets/report_push_1.png)

**[!UICONTROL Push notification sending performance]**、和小 **[!UICONTROL Push notification summary]** 组 **[!UICONTROL Sending metrics - by Push]** 件会详细介绍与您的消息相关的主要信息：

* **[!UICONTROL Sent]**:投放的发送总数。

* **[!UICONTROL Delivered]**:已成功发送的消息数，与已发送消息的总数有关。

* **[!UICONTROL Bounces]**:在投放和自动回访处理过程中累积的与已发送消息总数有关的错误总数。

* **[!UICONTROL Errors]**:投放期间发生的阻止将其发送到用户档案的错误总数。

* **[!UICONTROL Opens]**:投放中消息打开的次数。

* **[!UICONTROL Actions]**:已送达推送通知的操作总数，例如按钮单击或解除。

* **[!UICONTROL Engagements]**:此推送通知的打开和操作总数，例如用户档案打开推送或单击按钮时。

**[!UICONTROL Error Reasons]**&#x200B;图表和表允许您查看在投放期间发生的错误。

![](../assets/report_push_2.png)

**[!UICONTROL Tracking by platform]**、**[!UICONTROL Sending by platform]**&#x200B;和&#x200B;**[!UICONTROL Breakdown by platform]**&#x200B;图表和表格根据操作系统详细列出了推送通知的成功情况。

**[!UICONTROL Sending statistics - Failed]**&#x200B;小组件允许您查看发生了多少错误和跳出。
