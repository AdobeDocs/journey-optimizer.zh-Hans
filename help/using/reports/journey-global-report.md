---
title: 历程全局报告
description: 了解如何使用历程全局报告中的数据
feature: 报表
topic: 内容管理
role: User
level: Intermediate
source-git-commit: 42e5cdec54339f65cddd79df4deabbf28292d16b
workflow-type: tm+mt
source-wordcount: '944'
ht-degree: 0%

---

# 历程全局报告{#journey-global-report}

历程全局报告可通过&#x200B;**[!UICONTROL Global report]**&#x200B;按钮直接从历程访问。

![](../assets/global_report_1.png)

将显示历程&#x200B;**[!UICONTROL Global report]**&#x200B;页面，其中包含以下选项卡：

* [历程](#journey-global)
* [电子邮件](#email-global)
* [推送](#push-global)

历程&#x200B;**[!UICONTROL Global report]**&#x200B;分为不同的小组件，用于详细描述历程的成功和错误。 如果需要，可以调整每个小组件的大小并将其删除。 有关此内容的详细信息，请参阅此[部分](global-report.md#modify-dashboard)。

## 历程选项卡{#journey-global}

在历程&#x200B;**[!UICONTROL Global report]**&#x200B;中， **[!UICONTROL Journey]**&#x200B;选项卡可以清晰地显示有关历程最重要的跟踪数据。

![](../assets/global_report_2.png)

**[!UICONTROL Journey`s performance]**&#x200B;小组件允许您逐步查看目标用户档案在历程中的路径。

**[!UICONTROL Journey`s statistics]**&#x200B;小组件显示以下KPI:

* **[!UICONTROL Entered profiles]**:到达历程的登入事件的个人总数。

* **[!UICONTROL Exited profiles]**:退出历程的个人总数。

* **[!UICONTROL Failed individual journey]**:未成功执行的各个历程的总数。

![](../assets/global_report_12.png)

**[!UICONTROL Events received by event]**、**[!UICONTROL Events by origin]**&#x200B;和&#x200B;**[!UICONTROL Top events]**&#x200B;小组件允许您查看通过图形和表成功执行了&#x200B;**[!UICONTROL Events]**&#x200B;中的哪个小组件。

![](../assets/global_report_13.png)

**[!UICONTROL Action Performance]**、和 **[!UICONTROL Action Error Reasons]** 小 **[!UICONTROL Top Actions]** 组件表示在触发时发生的最成功的操作和 **[!UICONTROL Actions]** 错误。

**[!UICONTROL Top Actions]**&#x200B;表包含可用于&#x200B;**[!UICONTROL Actions]**&#x200B;的数据，例如：

* **[!UICONTROL Actions successfully executed]**:成功为历 **[!UICONTROL Actions]** 程执行的总次数。

* **[!UICONTROL Error in action]**:发生的错误总数。  **[!UICONTROL Actions]**

## 电子邮件选项卡{#email-global}

在您的历程&#x200B;**[!UICONTROL Global report]**&#x200B;中， **[!UICONTROL Email]**&#x200B;选项卡详细介绍了与在历程中发送的电子邮件投放相关的主要信息。

有关特定电子邮件投放的详细报告，请参阅[电子邮件全局报告](#email-global-report)一节。

![](../assets/global_report_14.png)

**[!UICONTROL Email Sending Statistics]**&#x200B;图表详细列出了交付的成功情况：

* **[!UICONTROL Sent]**:投放的发送总数。

* **[!UICONTROL Delivered]**:已成功发送的消息数，与已发送消息的总数有关。

* **[!UICONTROL Delivery Rate]**:成功发送的消息的百分比。

* **[!UICONTROL Bounces]**:在投放和自动回访处理过程中累积的与已发送消息总数有关的错误总数。

* **[!UICONTROL Bounce Rate]**:退回的电子邮件与发送的电子邮件的百分比。

* **[!UICONTROL Errors]**:投放期间发生的阻止将其发送到用户档案的错误总数。

* **[!UICONTROL Error Rate]**:与发送的电子邮件相比，在阻止发送投放的投放期间发生的错误百分比。

**[!UICONTROL Email - Tracking statistics]**&#x200B;包含用于投放的收件人活动的可用数据：

* **[!UICONTROL Opens]**:投放中打开投放的次数。

* **[!UICONTROL Unique Opens]**:已打开投放的百分比。

* **[!UICONTROL Open Rate]**:已打开的电子邮件总数与已投放电子邮件的数量相比较。

* **[!UICONTROL Clicks]**:电子邮件中内容的点击次数。

* **[!UICONTROL Unique Clicks]**：点击了电子邮件中内容的收件人数。

* **[!UICONTROL Click through rate]**:与历程进行交互的用户百分比。

* **[!UICONTROL Unsubscribe]**:退订链接的点击次数。

* **[!UICONTROL Spam complaints]**:将消息声明为垃圾邮件或垃圾邮件的次数。

**[!UICONTROL Sending Statistics]**&#x200B;图表包含可用于已发送电子邮件的数据，例如：

* **[!UICONTROL Delivered]**:已成功发送的消息数，与已发送消息的总数有关。

* **[!UICONTROL Bounces]**:在投放和自动回访处理过程中累积的与已发送消息总数有关的错误总数。

* **[!UICONTROL Errors]**:投放期间发生的阻止将其发送到用户档案的错误总数。

![](../assets/global_report_15.png)

**[!UICONTROL Bounce Reasons]**&#x200B;和&#x200B;**[!UICONTROL Bounce categories]**&#x200B;小组件包含与弹回消息相关的可用数据，例如：

* **[!UICONTROL Hard bounce]**:永久错误的总数，如错误的电子邮件地址。这涉及显式声明地址无效的错误消息，如未知用户。

* **[!UICONTROL Soft bounce]**:临时错误（如完整收件箱）的总数。

* **[!UICONTROL Ignored]**:临时（如“不在办公室”）或技术错误（例如，如果发件人类型为邮递员）的总数。

有关退回的更多信息，请参阅[禁止列表](../suppression-list.md)页面。

![](../assets/global_report_16.png)

**[!UICONTROL Email - Top Url]**&#x200B;图表和表格详细列出了投放中哪些URL的访问次数最多。

**[!UICONTROL Email - Top recipient domain]**&#x200B;图表和表格详细列出了收件人最常用于打开电子邮件的域。

## 推送选项卡{#push-global}

在您的历程&#x200B;**[!UICONTROL Global report]**&#x200B;中， **[!UICONTROL Push]**&#x200B;选项卡详细介绍了与在历程中发送的推送投放相关的主要信息。

有关特定推送投放的详细报告，请参阅[推送全局报告](#push-global-report)。

![](../assets/global_report_17.png)

**[!UICONTROL Push notification - Sending statistics]**&#x200B;表使用图表和KPI详细列出了与推送通知相关的主要信息：

* **[!UICONTROL Sent]**:投放的发送总数。

* **[!UICONTROL Delivered]**:已成功发送的消息数，与已发送消息的总数有关。

* **[!UICONTROL Delivery Rate]**:成功发送的消息的百分比。

* **[!UICONTROL Bounces]**:在投放和自动回访处理过程中累积的与已发送消息总数有关的错误总数。

* **[!UICONTROL Bounce Rate]**:与发送的推送通知相比，已退回的推送通知的百分比。

* **[!UICONTROL Errors]**:投放期间发生的阻止将其发送到用户档案的错误总数。

* **[!UICONTROL Error Rate]**:与发送的推送通知相比，在阻止发送投放的投放期间发生的错误百分比。

**[!UICONTROL Push - Tracking statistics]**&#x200B;包含用于投放的收件人活动的可用数据：

* **[!UICONTROL Opens]**:投放中消息打开的次数。

* **[!UICONTROL Open Rate]**:打开的推送通知的百分比。

* **[!UICONTROL Actions]**:已送达推送通知的操作总数，例如按钮单击或解除。

* **[!UICONTROL Engagements]**:此推送通知的打开和操作总数，例如用户档案打开推送或单击按钮时。

* **[!UICONTROL Engagement Rate]**:此推送通知的打开次数和操作的百分比，例如用户档案打开了推送或单击了按钮。

**[!UICONTROL Push notification summary]**&#x200B;图表包含可用于已发送推送通知的数据，例如：

* **[!UICONTROL Opens]**:投放中消息打开的次数。

* **[!UICONTROL Actions]**:已送达推送通知的操作总数，例如按钮单击或解除。

* **[!UICONTROL Bounces]**:在投放和自动回访处理过程中累积的与已发送消息总数有关的错误总数。

* **[!UICONTROL Delivered]**:已成功发送的消息数，与已发送消息的总数有关。

* **[!UICONTROL Errors]**:投放期间发生的阻止将其发送到用户档案的错误总数。

![](../assets/global_report_18.png)

**[!UICONTROL Error Reasons]**&#x200B;图表和表允许您查看在投放期间发生的错误。

![](../assets/global_report_19.png)

**[!UICONTROL Tracking by platform]**、**[!UICONTROL Sending by platform]**&#x200B;和&#x200B;**[!UICONTROL Breakdown by platform]**&#x200B;图表和表格根据收件人的操作系统详细列出了推送通知的成功情况。
