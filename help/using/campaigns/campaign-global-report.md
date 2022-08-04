---
title: 促销活动全局报告
description: 了解如何使用Campaign全局报告中的数据
feature: Reporting
topic: Content Management
role: User
level: Intermediate
hide: true
hidefromtoc: true
exl-id: fa64f5b8-75f2-40e6-8566-5766fafe6cd6
source-git-commit: 0036c905b9344a6f99e8525acbe9caab5932f361
workflow-type: tm+mt
source-wordcount: '1542'
ht-degree: 2%

---

# 促销活动全局报告 {#campaign-global-report}

营销活动全局报告可直接通过 **[!UICONTROL Global view]** 按钮。

营销活动 **[!UICONTROL Global report]** 页面中将显示以下选项卡：

* [Campaign](#campaign-global)
* [电子邮件](#email-global)
* [推送](#push-global)

营销活动 **[!UICONTROL Global report]** 会被分为不同的小组件，用于详细说明营销活动的成功和错误。 如果需要，可以调整每个小组件的大小并将其删除。 有关此内容的更多信息，请参阅此内容 [部分](../reports/global-report.md#modify-dashboard).

## “营销活动”选项卡 {#campaign-global}

### 交付 {#delivery-global}

![](assets/campaign_report_global_1.png)

的 **[!UICONTROL Campaign's Statistics]** 小组件详细介绍与您的营销活动相关的主要信息：

* **[!UICONTROL Entered profiles]**:开始历程的用户档案数。

* **[!UICONTROL Actions delivered]**:历程中某个操作被交付的唯一次数总数。

* **[!UICONTROL Actions failed in %]**:与提交操作的独特总次数相比，历程中操作失败的独特总次数。

### 目标(#objectives-global)

>[!AVAILABILITY]
>
>内容实验功能当前仅适用于一组组织（有限可用性）。 有关更多信息，请与您的 Adobe 代表联系。

![](assets/performance_report.gif)

的 **[!UICONTROL Objectives]** 选项卡，通过定位一个特定量度来优化投放报表。

的 **[!UICONTROL Objectives]** 已列出，链接到 **[!UICONTROL Datasets]** 定义与系统的连接以检索其他信息。 内置列表 **[!UICONTROL Objectives]** 可用，但您可以通过添加新来添加自己的 **[!UICONTROL Dataset]**. 有关详细过程，请参阅此文档。

选择要定位的目标后，这两个 **[!UICONTROL Performance overview]** 和 **[!UICONTROL Campaign objective]** 小组件将提供您交付性能的详细摘要。

使用 **[!UICONTROL Campaign objective]** 小组件中，您还可以选择将主要目标与其他量度进行比较。

请注意，如果需要，可以调整每个小组件的大小并将其删除。 有关此内容的更多信息，请参阅此内容 [部分](../reports/global-report.md#modify-dashboard).

### 实验(#experimentation-global)

>[!AVAILABILITY]
>
>内容实验功能当前仅适用于一组组织（有限可用性）。 有关更多信息，请与您的 Adobe 代表联系。

![](assets/experimentation_report_3.png)

从营销策划 **[!UICONTROL Global report]**, **[!UICONTROL Experimentation]** 选项卡详细列出了与每个变体的执行方式以及是否存在最佳执行者相关的主要信息。

请注意，定义最佳表演可能需要一些时间，它将由此图标表示 ![](assets/experimentation_report_1.png).

的 **[!UICONTROL Experiment result]** 小组件详细介绍每个变体的性能。 您可以通过从 **[!UICONTROL Baseline]** 下拉菜单。 最佳待遇将用星形图标表示。

下表显示了以下量度：

* **[!UICONTROL Profiles]**:针对此治疗的用户档案数。

* **[!UICONTROL Unique outbound clicks]**:出站渠道的总点击次数。

* **[!UICONTROL Count per profile]**:实验目标量度的总值除以用户档案数。

* **[!UICONTROL Confidence interval]**:基线与最佳处理之间性能差异的百分比。 [了解详情](../campaigns/experiment-calculations.md#confidence-intervals)。

* **[!UICONTROL Average lift]**:给定治疗相对于基准线的转化率提高的百分比。 [了解详情](../campaigns/experiment-calculations.md#understand-lift)

* **[!UICONTROL Confidence]**:有证据表明，给定治疗与基准治疗相同。 [了解详情](../campaigns/experiment-calculations.md#understand-confidence)

要深入了解这些结果以及如何解释它们，请参阅 [本页](../campaigns/get-started-experiment.md#interpret-results).

## “电子邮件”选项卡 {#email-global}

从营销策划 **[!UICONTROL Global report]**, **[!UICONTROL Email]** 选项卡详细列出了与营销活动中发送的电子邮件投放相关的主要信息。

的 **[!UICONTROL Email Sending Statistics]** 图形详细说明了交付的成功：

* **[!UICONTROL Targeted]**:在投放分析期间处理的消息总数。

* **[!UICONTROL Sent]**:投放的发送总数。

* **[!UICONTROL Delivered]**:已成功发送的消息数，与已发送消息的总数有关。

* **[!UICONTROL Delivery Rate]**:成功发送的消息的百分比。

* **[!UICONTROL Bounces]**:在投放和自动回访处理过程中累积的与已发送消息总数有关的错误总数。

* **[!UICONTROL Bounce Rate]**:退回的电子邮件与发送的电子邮件的百分比。

* **[!UICONTROL Errors]**:投放期间发生的阻止将其发送到用户档案的错误总数。

* **[!UICONTROL Error Rate]**:与发送的电子邮件相比，在阻止发送投放的投放期间发生的错误百分比。

* **[!UICONTROL Retries]**:队列中要重试的电子邮件数量。

* **[!UICONTROL Excluded]**:已被Adobe Journey Optimizer排除的用户档案数。

的 **[!UICONTROL Email - Tracking statistics]** 小组件包含用于投放的收件人活动的可用数据：

* **[!UICONTROL Opens]**:投放中打开投放的次数。

* **[!UICONTROL Unique Opens]**:已打开投放的百分比。

* **[!UICONTROL Open Rate]**:已打开的电子邮件总数与已投放电子邮件的数量相比较。

* **[!UICONTROL Clicks]**:电子邮件中内容的点击次数。

* **[!UICONTROL Unique Clicks]**：点击了电子邮件中内容的收件人数。

* **[!UICONTROL Unique Click Rate]**:与投放进行交互的用户百分比。

* **[!UICONTROL Unsubscriptions]**:退订链接的点击次数。

* **[!UICONTROL Spam complaints]**:将消息声明为垃圾邮件或垃圾邮件的次数。

的 **[!UICONTROL Sending Statistics]** 图表包含可用于已发送电子邮件的数据，例如：

* **[!UICONTROL Delivered]**:已成功发送的消息数，与已发送消息的总数有关。

* **[!UICONTROL Bounces]**:在投放和自动回访处理过程中累积的与已发送消息总数有关的错误总数。

* **[!UICONTROL Retries]**:队列中要重试的电子邮件数量。

* **[!UICONTROL Errors]**:投放期间发生的阻止将其发送到用户档案的错误总数。

的 **[!UICONTROL Bounce Reasons]** 和 **[!UICONTROL Bounce categories]** 小组件包含与弹回的消息相关的可用数据，例如：

* **[!UICONTROL Hard bounce]**:永久错误的总数，如错误的电子邮件地址。 这涉及显式声明地址无效的错误消息，如未知用户。

* **[!UICONTROL Soft bounce]**:临时错误（如完整收件箱）的总数。

* **[!UICONTROL Ignored]**:临时（如“不在办公室”）或技术错误（例如，如果发件人类型为邮递员）的总数。

有关退回的更多信息，请参阅 [禁止列表](../reports/suppression-list.md) 页面。

的 **[!UICONTROL Error Reasons]** 通过图表和表格，可查看在投放期间发生的错误。

的 **[!UICONTROL Excluded reasons]** 图形和表格显示阻止从定向用户档案中排除的用户配置文件接收消息的不同原因。

的 **[!UICONTROL Email - Top Url]** 图表和表格详细列出了投放中哪些URL的访问次数最多。

的 **[!UICONTROL Email - Top recipient domain]** 图表和表格详细列出了收件人最常使用哪些域来打开电子邮件。

>[!NOTE]
>
>的 **[!UICONTROL Optimized vs non optimized]** 和 **[!UICONTROL Send time optimization]**  只有为您的投放激活了发送时间优化选项时，小组件才可用。 有关发送时间优化的详细信息，请参阅 [本页](../messages/send-time-optimization.md).

的 **[!UICONTROL Optimized vs non optimized]** 图表详细列出了与消息相关的主要信息（无论消息是否已优化）：

* **[!UICONTROL Sent]**:投放的发送总数。
* **[!UICONTROL Opens]**:投放中打开投放的次数。
* **[!UICONTROL Clicks]**:电子邮件中内容的点击次数。

的 **[!UICONTROL Send time optimization]** 根据发送方法详细描述投放成功与否：已优化或正常。

* **[!UICONTROL Delivered]**:已成功发送的消息数，与已发送消息的总数有关。
* **[!UICONTROL Bounces]**:在投放和自动回访处理过程中累积的与已发送消息总数有关的错误总数。

## “推送”选项卡 {#push-global}

从营销策划 **[!UICONTROL Global report]**, **[!UICONTROL Push]** 选项卡详细列出了与营销活动中发送的推送投放相关的主要信息。

的 **[!UICONTROL Push notification - Sending statistics]** 表格使用图形和KPI详细列出了与推送通知相关的主要信息：

* **[!UICONTROL Targeted]**:在投放分析期间处理的消息总数。

* **[!UICONTROL Sent]**:投放的发送总数。

* **[!UICONTROL Delivered]**:已成功发送的消息数，与已发送消息的总数有关。

* **[!UICONTROL Delivery Rate]**:成功发送的消息的百分比。

* **[!UICONTROL Bounces]**:在投放和自动回访处理过程中累积的与已发送消息总数有关的错误总数。

* **[!UICONTROL Bounce Rate]**:与发送的推送通知相比，已退回的推送通知的百分比。

* **[!UICONTROL Errors]**:投放期间发生的阻止将其发送到用户档案的错误总数。

* **[!UICONTROL Error Rate]**:与发送的推送通知相比，在阻止发送投放的投放期间发生的错误百分比。

* **[!UICONTROL Excluded]**:已被Adobe Journey Optimizer排除的用户档案数。

的 **[!UICONTROL Push - Tracking statistics]** 包含用于投放的收件人活动的可用数据：

* **[!UICONTROL Opens]**:投放中消息打开的次数。

* **[!UICONTROL Open Rate]**:打开的推送通知的百分比。

* **[!UICONTROL Actions]**:已送达推送通知的操作总数，例如按钮单击或解除。

* **[!UICONTROL Engagements]**:此推送通知的打开和操作总数，例如用户档案打开推送或单击按钮时。

* **[!UICONTROL Engagement Rate]**:此推送通知的打开次数和操作的百分比，例如用户档案打开了推送或单击了按钮。

的 **[!UICONTROL Push notification summary]** 图表包含可用于已发送推送通知的数据，例如：

* **[!UICONTROL Opens]**:投放中消息打开的次数。

* **[!UICONTROL Actions]**:已送达推送通知的操作总数，例如按钮单击或解除。

* **[!UICONTROL Bounces]**:在投放和自动回访处理过程中累积的与已发送消息总数有关的错误总数。

* **[!UICONTROL Delivered]**:已成功发送的消息数，与已发送消息的总数有关。

* **[!UICONTROL Errors]**:投放期间发生的阻止将其发送到用户档案的错误总数。

>[!NOTE]
>
>的 **[!UICONTROL Optimized vs non optimized]** 和 **[!UICONTROL Send time optimization]**  只有为您的投放激活了发送时间优化选项时，小组件才可用。 有关发送时间优化的详细信息，请参阅 [本页](../messages/send-time-optimization.md).

的 **[!UICONTROL Optimized vs non optimized]** 图表详细列出了与消息相关的主要信息（无论消息是否已优化）：

* **[!UICONTROL Delivered]**:已成功发送的消息数，与已发送消息的总数有关。
* **[!UICONTROL Opens]**:投放中打开投放的次数。
* **[!UICONTROL Actions]**:已送达推送通知的操作总数，例如按钮单击或解除。

的 **[!UICONTROL Send time optimization]** 根据发送方法详细描述投放成功与否：已优化或正常。

* **[!UICONTROL Delivered]**:已成功发送的消息数，与已发送消息的总数有关。
* **[!UICONTROL Bounces]**:在投放和自动回访处理过程中累积的与已发送消息总数有关的错误总数。

的 **[!UICONTROL Error Reasons]** 通过图表和表格，可查看在投放期间发生的错误。

的 **[!UICONTROL Excluded reasons]** 图形和表格显示阻止从定向用户档案中排除的用户配置文件接收消息的不同原因。

的 **[!UICONTROL Tracking by platform]**, **[!UICONTROL Sending by platform]** 和 **[!UICONTROL Breakdown by platform]** 图形和表格根据收件人的操作系统详细列出了推送通知的成功情况。

## 其他资源

* [营销活动入门](get-started-with-campaigns.md)
* [创建营销活动](create-campaign.md)
* [创建API触发的营销活动](api-triggered-campaigns.md)
* [修改或停止营销活动](modify-stop-campaign.md)
* [营销活动实时报告](campaign-live-report.md)
