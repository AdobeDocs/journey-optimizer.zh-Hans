---
title: 通过电邮发送全局报告
description: 了解如何使用电子邮件全局报告中的数据
feature: Reporting
topic: Content Management
role: User
level: Intermediate
exl-id: 2bead395-082a-4fea-ad10-b2b2c5f484e9
source-git-commit: 284d95976ab1b58aaea2a4c41db20a3ea5a9b761
workflow-type: tm+mt
source-wordcount: '734'
ht-degree: 0%

---

# 通过电邮发送全局报告 {#email-global-report}

电子邮件 **[!UICONTROL Global report]** 仅定向特定电子邮件投放。

从 **[!UICONTROL Executions]** 选项卡 **[!UICONTROL Messages]** 菜单，选择 **[!UICONTROL Global view]** 然后，从选定投放的高级菜单中选择 **[!UICONTROL Global report]**.

![](assets/global_report_3.png)

电子邮件 **[!UICONTROL Global report]** 会分为不同的小组件，用于详细描述投放的成功和错误。 如果需要，可以调整每个小组件的大小并将其删除。 有关此内容的详细信息，请参阅 [部分](global-report.md#modify-dashboard).

![](assets/global_report_4.png)

**[!UICONTROL Email performance]** 使用KPI详细描述与消息相关的主要信息：

* **[!UICONTROL Sent]**:投放的发送总数。

* **[!UICONTROL Delivery Rate]**:成功发送的消息的百分比。

* **[!UICONTROL Bounce Rate]**:退回的电子邮件与发送的电子邮件的百分比。

* **[!UICONTROL Error Rate]**:与发送的电子邮件相比，在阻止发送投放的投放期间发生的错误百分比。

* **[!UICONTROL Open Rate]**:已打开消息的百分比。

* **[!UICONTROL Click Rate]**:投放中的点击次数百分比。

* **[!UICONTROL Spam Complaint Rate]**:收件人标记为垃圾邮件的电子邮件与已发送邮件的百分比。 有关投诉的更多信息，请参阅 [投放能力最佳实践指南](https://experienceleague.adobe.com/docs/deliverability-learn/deliverability-best-practice-guide/metrics-for-deliverability/complaints.html#metrics-for-deliverability){target=&quot;_blank&quot;}。

* **[!UICONTROL Unsubscribe Rate]**:独特退订与已投放消息数量的百分比。 此指示器不依赖于退订链接的点击次数，而是基于收件人启动的退订次数。 在此处了解有关取消订阅的更多信息 [页面](../messages/consent.md).

的 **[!UICONTROL Email - Tracking statistics]** 包含用于投放的收件人活动的可用数据：

* **[!UICONTROL Opens]**:投放中打开投放的次数。

* **[!UICONTROL Unique Opens]**:已打开投放的百分比。

* **[!UICONTROL Open Rate]**:已打开的电子邮件总数与已投放电子邮件的数量相比较。

* **[!UICONTROL Clicks]**:电子邮件中内容的点击次数。

* **[!UICONTROL Unique Clicks]**：点击了电子邮件中内容的收件人数。

* **[!UICONTROL Click through rate]**:与历程进行交互的用户百分比。

的 **[!UICONTROL Sending Statistics]** 图形详细说明了交付的成功：

* **[!UICONTROL Delivered]**:已成功发送的消息数，与已发送消息的总数有关。

* **[!UICONTROL Bounces]**:在投放和自动回访处理过程中累积的与已发送消息总数有关的错误总数。

* **[!UICONTROL Errors]**:投放期间发生的阻止将其发送到用户档案的错误总数。

![](assets/global_report_5.png)

的 **[!UICONTROL Bounce Reasons]** 和 **[!UICONTROL Bounce categories]** 小组件包含与弹回的消息相关的可用数据，例如：

* **[!UICONTROL Hard bounce]**:永久错误的总数，如错误的电子邮件地址。 这涉及显式声明地址无效的错误消息，如未知用户。

* **[!UICONTROL Soft bounce]**:临时错误（如完整收件箱）的总数。

* **[!UICONTROL Ignored]**:临时（如外出）或技术错误（例如，如果发件人类型为邮递员）的总数。

有关退回的更多信息，请参阅 [禁止列表](../reports/suppression-list.md) 页面。

的 **[!UICONTROL Error Reasons]** 和 **[!UICONTROL Exclude Reasons]** 图形和表格允许您查看在投放期间发生的错误和排除项。

![](assets/global_report_6.png)

的 **[!UICONTROL Email - Top recipient domain]** 图表和表格详细列出了收件人最常使用哪些域来打开电子邮件。

的 **[!UICONTROL Email - Top Url]** 图表和表格详细列出了投放中哪些URL的访问次数最多。

的 **[!UICONTROL Open vs Click]** 标识收件人与投放的交互：

* **[!UICONTROL Unique Clicks]**：点击了电子邮件中内容的收件人数。

* **[!UICONTROL Unique Opens]**:打开投放的收件人数。

![](assets/global_report_20.png)

>[!NOTE]
>
>仅当在电子邮件中插入决策时，选件小组件和量度才可用。 有关决策管理的详细信息，请参阅此 [页面](../offers/get-started/starting-offer-decisioning.md).

的 **[!UICONTROL Offers statistic]** 和 **[!UICONTROL Offers statistics]** 随着时间的推移，小组件可衡量选件的成功以及对目标受众的影响。 它使用KPI详细描述与消息相关的主要信息：

* **[!UICONTROL Offer sent]**:选件的发送总数。

* **[!UICONTROL Offer impression]**:在投放中打开选件的次数。

* **[!UICONTROL Offer clicks]**:在投放中点击选件的次数。

的 **[!UICONTROL Offers detailed statistic]** 表包含与选件一起用于收件人活动的可用数据：

* **[!UICONTROL Placement name]**:用于显示选件的版面名称。 有关版面的更多信息，请参阅 [页面](../offers/offer-library/creating-placements.md).

* **[!UICONTROL Offer name]**:在投放中添加的选件的名称。 有关版面的更多信息，请参阅 [页面](../offers/offer-library/creating-personalized-offers.md).

* **[!UICONTROL Offer sent]**:选件的发送总数。

* **[!UICONTROL Offer impression rate]**:已打开选件与已发送选件数的百分比。

* **[!UICONTROL Offer click rate]**:与选件进行交互的用户百分比。

>[!NOTE]
>
>具有 **[!UICONTROL Suppressed]** 或 **[!UICONTROL Not allowed]** 在消息发送过程中，状态将被排除。 因此，当 **历程报表** 会将这些用户档案显示为已在历程([读取区段](../building-journeys/read-segment.md) 和 [消息](../building-journeys/journeys-message.md) ) **电子邮件报表** 将不会在 **[!UICONTROL Sent]** 量度，因为在发送电子邮件之前，这些量度会被过滤掉。
>
>了解 [禁止列表](../reports/suppression-list.md) 和 [允许列表](allow-list.md). 要找出所有排除案例的原因，您可以使用 [Adobe Experience Platform查询服务](https://experienceleague.adobe.com/docs/experience-platform/query/api/getting-started.html){target=&quot;_blank&quot;}。
