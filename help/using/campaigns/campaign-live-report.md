---
title: 营销活动实时报告
description: 了解如何使用Campaign实时报告中的数据
feature: Reporting
topic: Content Management
role: User
level: Intermediate
hide: true
hidefromtoc: true
exl-id: 925494b6-e08a-4bd3-8a2f-96a5d9cbc387
source-git-commit: 0e978d0eab570a28c187f3e7779c450437f16cfb
workflow-type: tm+mt
source-wordcount: '586'
ht-degree: 4%

---

# 营销活动实时报告 {#campaign-live-report}

营销活动实时报告可通过 **[!UICONTROL Live view]** 按钮。

营销活动 **[!UICONTROL Live report]** 页面中将显示以下选项卡：

* [Campaign](#campaign-live)
* [电子邮件](#email-live)
* [推送](#push-live)

营销活动 **[!UICONTROL Live report]** 会被分为不同的小组件，用于详细说明营销活动的成功和错误。 如果需要，可以调整每个小组件的大小并将其删除。 有关此内容的更多信息，请参阅此内容 [部分](../reports/live-report.md#modify-dashboard).

## “营销活动”选项卡 {#campaign-global}

### 交付 {#delivery-global}

的 **[!UICONTROL Campaign Statistics]** 小组件详细介绍与您的营销活动相关的主要信息：

* **[!UICONTROL Entered profiles]**:开始历程的用户档案数。

<!--
### Experimentation tab (#experimentation-live)

From your Campaign **[!UICONTROL Live report]**, the **[!UICONTROL Experimentation]** tab details the main information relative to how each variant is performing and if there is was winner during the test.
-->
## “电子邮件”选项卡 {#email-live}

从营销策划 **[!UICONTROL Live report]**, **[!UICONTROL Email]** 选项卡详细列出了与营销活动中发送的电子邮件投放相关的主要信息。

的 **[!UICONTROL Email Sending Statistics]** 小组件详细介绍与您的消息相关的主要信息：

* **[!UICONTROL Delivered]**:已成功发送的消息数，与已发送消息的总数有关。

* **[!UICONTROL Bounces]**:在投放和自动回访处理过程中累积的与已发送消息总数有关的错误总数。

* **[!UICONTROL Errors]**:投放期间发生的阻止将其发送到用户档案的错误总数。

的 **[!UICONTROL Sending metrics by Email]** 表格和 **[!UICONTROL Email Summary]** 图形详细说明了交付的成功：

* **[!UICONTROL Sent]**:投放的发送总数。

* **[!UICONTROL Delivered]**:已成功发送的消息数，与已发送消息的总数有关。

* **[!UICONTROL Bounces]**:在投放和自动回访处理过程中累积的与已发送消息总数有关的错误总数。

* **[!UICONTROL Errors]**:投放期间发生的阻止将其发送到用户档案的错误总数。

* **[!UICONTROL Opens]**:投放中消息打开的次数。

* **[!UICONTROL Clicks]**:在投放中点击内容的次数。

* **[!UICONTROL Unsubscribe]**:退订链接的点击次数。

* **[!UICONTROL Spam complaints]**:将消息声明为垃圾邮件或垃圾邮件的次数。

的 **[!UICONTROL Bounce Reasons]**, **[!UICONTROL Bounce categories]** 和 **[!UICONTROL Hard and bounce - by Email]** 小组件包含与弹回的消息相关的可用数据，例如：

* **[!UICONTROL Hard bounce]**:永久错误的总数，如错误的电子邮件地址。 这涉及显式声明地址无效的错误消息，如未知用户。

* **[!UICONTROL Soft bounce]**:临时错误（如完整收件箱）的总数。

* **[!UICONTROL Ignored]**:临时（如“不在办公室”）或技术错误（例如，如果发件人类型为邮递员）的总数。

的 **[!UICONTROL Error Reasons]** 和 **[!UICONTROL Exclude Reasons]** 图形和表格允许您查看在投放期间发生的错误和排除项。

的 **[!UICONTROL Email - Top recipient domain]** 图表和表格详细列出了收件人最常使用哪些域来打开电子邮件。

## “推送”选项卡 {#push-live}

从营销策划 **[!UICONTROL Live report]**, **[!UICONTROL Push]** 选项卡详细列出了与营销活动中发送的推送投放相关的主要信息。

**[!UICONTROL Push notification sending performance]**, **[!UICONTROL Push notification summary]** 和 **[!UICONTROL Sending metrics - by Push]** 小组件详细介绍与您的消息相关的主要信息：

* **[!UICONTROL Sent]**:投放的发送总数。

* **[!UICONTROL Delivered]**:已成功发送的消息数，与已发送消息的总数有关。

* **[!UICONTROL Bounces]**:在投放和自动回访处理过程中累积的与已发送消息总数有关的错误总数。

* **[!UICONTROL Errors]**:投放期间发生的阻止将其发送到用户档案的错误总数。

* **[!UICONTROL Opens]**:投放中消息打开的次数。

* **[!UICONTROL Actions]**:已送达推送通知的操作总数，例如按钮单击或解除。

* **[!UICONTROL Engagements]**:此推送通知的打开和操作总数，例如用户档案打开推送或单击按钮时。

的 **[!UICONTROL Error Reasons]** 和 **[!UICONTROL Exclude Reasons]** 图形和表格允许您查看在投放期间发生的错误和排除项。

的 **[!UICONTROL Sending statistics - Failed]** 小组件允许您查看发生了多少错误和跳出。

的 **[!UICONTROL Tracking by platform]**, **[!UICONTROL Sending by platform]** 和 **[!UICONTROL Breakdown by platform]** 图形和表格根据操作系统详细列出了推送通知的成功情况。

## 其他资源

* [营销活动入门](get-started-with-campaigns.md)
* [创建营销活动](create-campaign.md)
* [创建API触发的营销活动](api-triggered-campaigns.md)
* [修改或停止营销活动](modify-stop-campaign.md)
* [营销活动全局报告](campaign-global-report.md)
