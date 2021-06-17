---
title: 通过电邮发送全局报告
description: 了解如何使用电子邮件全局报告中的数据
feature: 报表
topic: 内容管理
role: User
level: Intermediate
source-git-commit: 42e5cdec54339f65cddd79df4deabbf28292d16b
workflow-type: tm+mt
source-wordcount: '489'
ht-degree: 1%

---

# 电子邮件全局报告{#email-global-report}

电子邮件&#x200B;**[!UICONTROL Global report]**&#x200B;仅定向特定的电子邮件投放。

从&#x200B;**[!UICONTROL Messages]**&#x200B;菜单的&#x200B;**[!UICONTROL Executions]**&#x200B;选项卡中，选择&#x200B;**[!UICONTROL Global view]** ，然后从选定投放的高级菜单中选择&#x200B;**[!UICONTROL Global report]**。

![](../assets/global_report_3.png)

电子邮件&#x200B;**[!UICONTROL Global report]**&#x200B;分为不同的小组件，用于详细描述投放成功和错误。 如果需要，可以调整每个小组件的大小并将其删除。 有关此内容的详细信息，请参阅此[部分](global-report.md#modify-dashboard)。

![](../assets/global_report_4.png)

**[!UICONTROL Email performance]** 使用KPI详细描述与消息相关的主要信息：

* **[!UICONTROL Sent]**:投放的发送总数。

* **[!UICONTROL Delivery Rate]**:成功发送的消息的百分比。

* **[!UICONTROL Bounce Rate]**:退回的电子邮件与发送的电子邮件的百分比。

* **[!UICONTROL Error Rate]**:与发送的电子邮件相比，在阻止发送投放的投放期间发生的错误百分比。

* **[!UICONTROL Open Rate]**:已打开消息的百分比。

* **[!UICONTROL Click Rate]**:投放中的点击次数百分比。

* **[!UICONTROL Spam Complaint Rate]**:收件人标记为垃圾邮件的电子邮件与已发送邮件的百分比。有关投诉的更多信息，请参阅此[页面](https://experienceleague.adobe.com/docs/deliverability-learn/deliverability-best-practice-guide/metrics-for-deliverability/complaints.html#metrics-for-deliverability)。

* **[!UICONTROL Unsubscribe Rate]**:独特退订与已投放消息数量的百分比。此指示器不依赖于退订链接的点击次数，而是基于收件人启动的退订次数。 在此[page](../consent.md)中了解有关取消订阅的更多信息。

**[!UICONTROL Email - Tracking statistics]**&#x200B;包含用于投放的收件人活动的可用数据：

* **[!UICONTROL Opens]**:投放中打开投放的次数。

* **[!UICONTROL Unique Opens]**:已打开投放的百分比。

* **[!UICONTROL Open Rate]**:已打开的电子邮件总数与已投放电子邮件的数量相比较。

* **[!UICONTROL Clicks]**:电子邮件中内容的点击次数。

* **[!UICONTROL Unique Clicks]**：点击了电子邮件中内容的收件人数。

* **[!UICONTROL Click through rate]**:与历程进行交互的用户百分比。

**[!UICONTROL Sending Statistics]**&#x200B;图表详细列出了交付的成功情况：

* **[!UICONTROL Delivered]**:已成功发送的消息数，与已发送消息的总数有关。

* **[!UICONTROL Bounces]**:在投放和自动回访处理过程中累积的与已发送消息总数有关的错误总数。

* **[!UICONTROL Errors]**:投放期间发生的阻止将其发送到用户档案的错误总数。

![](../assets/global_report_5.png)

**[!UICONTROL Bounce Reasons]**&#x200B;和&#x200B;**[!UICONTROL Bounce categories]**&#x200B;小组件包含与弹回消息相关的可用数据，例如：

* **[!UICONTROL Hard bounce]**:永久错误的总数，如错误的电子邮件地址。这涉及显式声明地址无效的错误消息，如未知用户。

* **[!UICONTROL Soft bounce]**:临时错误（如完整收件箱）的总数。

* **[!UICONTROL Ignored]**:临时（如外出）或技术错误（例如，如果发件人类型为邮递员）的总数。

有关退回的更多信息，请参阅[禁止列表](../suppression-list.md)页面。

**[!UICONTROL Error Reasons]**&#x200B;图表和表允许您查看在投放期间发生的错误。

![](../assets/global_report_6.png)

**[!UICONTROL Email - Top recipient domain]**&#x200B;图表和表格详细列出了收件人最常用于打开电子邮件的域。

**[!UICONTROL Email - Top Url]**&#x200B;图表和表格详细列出了投放中哪些URL的访问次数最多。

**[!UICONTROL Open vs Click]**&#x200B;标识收件人与投放的交互：

* **[!UICONTROL Unique Clicks]**：点击了电子邮件中内容的收件人数。

* **[!UICONTROL Unique Opens]**:打开投放的收件人数。


