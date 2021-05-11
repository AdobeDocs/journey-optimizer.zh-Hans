---
title: 历程全局报告
description: 了解如何使用旅程全局报告中的数据
translation-type: tm+mt
source-git-commit: 55b9e5d8ed259ec6ed7746e835691d7d6261a8a4
workflow-type: tm+mt
source-wordcount: '934'
ht-degree: 0%

---

# 历程全局报告{#journey-global-report}

![](../assets/do-not-localize/badge.png)

历程全局报表可通过&#x200B;**[!UICONTROL Global report]**&#x200B;按钮从您的旅程直接访问。

![](../assets/global_report_1.png)

旅程&#x200B;**[!UICONTROL Global report]**&#x200B;页面将显示以下选项卡：

* [历程](#journey-global)
* [电子邮件](#email-global)
* [推送](#push-global)

旅程&#x200B;**[!UICONTROL Global report]**&#x200B;分为不同的构件，详细描述您旅程的成功和错误。 如果需要，可以调整和删除每个Widget。 有关此内容的详细信息，请参阅此[部分](global-report.md#modify-dashboard)。

## 历程选项卡{#journey-global}

在您的旅程&#x200B;**[!UICONTROL Global report]**&#x200B;中，**[!UICONTROL Journey]**&#x200B;选项卡可以清晰地视图旅程中最重要的跟踪数据。

![](../assets/global_report_2.png)

通过&#x200B;**[!UICONTROL Journey`s performance]**&#x200B;构件，您可以分步查看目标用户档案的旅程。

**[!UICONTROL Journey`s statistics]**&#x200B;小部件显示以下KPI:

* **[!UICONTROL Entered profiles]**:到达旅程入口事件的总人数。

* **[!UICONTROL Exited profiles]**:退出旅程的个人总数。

* **[!UICONTROL Failed individual journey]**:未成功执行的个人旅程总数。

**[!UICONTROL Event Performance]**&#x200B;和&#x200B;**[!UICONTROL Top events]**&#x200B;构件允许您查看哪个&#x200B;**[!UICONTROL Events]**&#x200B;通过图形和表成功执行。

**[!UICONTROL Action Performance]** 而 **[!UICONTROL Top Actions]** 构件代表触发时发生的最成功的操作 **[!UICONTROL Actions]** 和错误。**[!UICONTROL Top Actions]**&#x200B;表包含可用于&#x200B;**[!UICONTROL Actions]**&#x200B;的数据，例如：

* **[!UICONTROL Actions successfully executed]**:成功执 **[!UICONTROL Actions]** 行旅程的总数。

* **[!UICONTROL Error in action]**:发生的错误总数 **[!UICONTROL Actions]**。

**[!UICONTROL Error Reasons]**&#x200B;图表详细列出了&#x200B;**[!UICONTROL Actions]**&#x200B;发生的错误类型。

<!--Events by origin-->

## 电子邮件选项卡{#email-global}

在您的旅程&#x200B;**[!UICONTROL Global report]**&#x200B;中，**[!UICONTROL Email]**&#x200B;选项卡详细列出了与您旅程中发送的电子邮件投放相关的主要信息。

有关特定电子邮件投放的详细报告，请参阅[电子邮件全局报告](#email-global-report)部分。

**[!UICONTROL Email Sending Statistics]**&#x200B;图表详细说明了您的投放的成功：

* **[!UICONTROL Sent]**:投放的发送总数。

* **[!UICONTROL Delivered]**:成功发送的消息数，与已发送消息的总数有关。

* **[!UICONTROL Delivery Rate]**:已成功发送的邮件百分比。

* **[!UICONTROL Bounces]**:在投放和自动返回处理期间累积的与已发送消息总数相关的错误总数。

* **[!UICONTROL Bounce Rate]**:与发送的电子邮件相比，弹回的电子邮件的百分比。

* **[!UICONTROL Errors]**:在投放期间发生的错误总数，导致无法将错误发送给用户档案。

* **[!UICONTROL Error Rate]**:与发送的电子邮件相比，在阻止其发送的投放中发生的错误百分比。

**[!UICONTROL Email - Tracking statistics]**&#x200B;包含可用于收件人活动的投放数据：

* **[!UICONTROL Opens]**:投放在投放中打开的次数。

* **[!UICONTROL Unique Opens]**:已打开投放的百分比。

* **[!UICONTROL Open Rate]**:已打开电子邮件的总数与已发送电子邮件的数量相比。

* **[!UICONTROL Clicks]**:在电子邮件中单击内容的次数。

* **[!UICONTROL Unique Clicks]**：单击电子邮件中内容的收件人数。

* **[!UICONTROL Click through rate]**:与旅程互动的用户百分比。

**[!UICONTROL Sending Statistics]**&#x200B;图表包含可用于已发送电子邮件的数据，例如：

* **[!UICONTROL Delivered]**:成功发送的消息数，与已发送消息的总数有关。

* **[!UICONTROL Bounces]**:在投放和自动返回处理期间累积的与已发送消息总数相关的错误总数。

* **[!UICONTROL Errors]**:在投放期间发生的错误总数，导致无法将错误发送给用户档案。

**[!UICONTROL Bounce Reasons]**&#x200B;和&#x200B;**[!UICONTROL Bounce categories]**&#x200B;构件包含与弹回邮件相关的可用数据，例如：

* **[!UICONTROL Hard bounce]**:永久错误的总数，如错误的电子邮件地址。这涉及显式声明地址无效的错误消息，如未知用户。

* **[!UICONTROL Soft bounce]**:临时错误的总数，如完整的收件箱。

* **[!UICONTROL Ignored]**:临时的总数，如“外出”或技术错误（例如，如果发送者类型是邮政主管）。

有关弹回的详细信息，请参阅[管理抑制列表](../suppression-lists.md)页。

**[!UICONTROL Email - Top Url]**&#x200B;图表和表格详细信息，您的投放中访问次数最多的URL。

**[!UICONTROL Email - Best recipient domain]**&#x200B;图表和表格详细信息，收件人最常使用哪些域打开电子邮件。

## 推送选项卡{#push-global}

在您的旅程&#x200B;**[!UICONTROL Global report]**&#x200B;中，**[!UICONTROL Push]**&#x200B;选项卡详细列出了与您旅程中发送的推送投放相关的主要信息。

有关特定推送投放的详细报告，请参阅[推送全局报告](#push-global-report)。

**[!UICONTROL Push notification - Sending statistics]**&#x200B;表使用图表和KPI详细列出了与推送通知相关的主要信息：

* **[!UICONTROL Sent]**:投放的发送总数。

* **[!UICONTROL Delivered]**:成功发送的消息数，与已发送消息的总数有关。

* **[!UICONTROL Delivery Rate]**:已成功发送的邮件百分比。

* **[!UICONTROL Bounces]**:在投放和自动返回处理期间累积的与已发送消息总数相关的错误总数。

* **[!UICONTROL Bounce Rate]**:与发送的推送通知相比，退回的推送通知的百分比。

* **[!UICONTROL Errors]**:在投放期间发生的错误总数，导致无法将错误发送给用户档案。

* **[!UICONTROL Error Rate]**:与发送的推送通知相比，在阻止发送的投放中发生的错误百分比。

**[!UICONTROL Push - Tracking statistics]**&#x200B;包含可用于收件人活动的投放数据：

* **[!UICONTROL Opens]**:在投放中打开消息的次数。

* **[!UICONTROL Open Rate]**:已打开的推送通知的百分比。

* **[!UICONTROL Actions]**:已传递的推送通知操作总数，如按钮单击或解除。

* **[!UICONTROL Engagements]**:此推送通知的打开和操作总数，即用户档案打开推送或单击按钮时。

* **[!UICONTROL Engagement Rate]**:此推送通知的打开和操作百分比，即用户档案打开推送或单击按钮时。

**[!UICONTROL Push notification summary]**&#x200B;图表包含可用于发送的推送通知的数据，例如：

* **[!UICONTROL Opens]**:在投放中打开消息的次数。

* **[!UICONTROL Actions]**:已传递的推送通知操作总数，如按钮单击或解除。

* **[!UICONTROL Bounces]**:在投放和自动返回处理期间累积的与已发送消息总数相关的错误总数。

* **[!UICONTROL Delivered]**:成功发送的消息数，与已发送消息的总数有关。

* **[!UICONTROL Errors]**:在投放期间发生的错误总数，导致无法将错误发送给用户档案。

**[!UICONTROL Error Reasons]**&#x200B;图表和表允许您查看在投放期间发生的错误。

**[!UICONTROL Tracking by platform]**、**[!UICONTROL Sending by platform]**&#x200B;和&#x200B;**[!UICONTROL Breakdown by platform]**&#x200B;图表和表根据收件人的操作系统详细说明了推送通知的成功与否。
