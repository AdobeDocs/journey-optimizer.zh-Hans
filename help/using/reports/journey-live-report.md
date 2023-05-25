---
solution: Journey Optimizer
product: journey optimizer
title: 历程实时报告
description: 了解如何使用历程实时报告中的数据
feature: Reporting
topic: Content Management
role: User
level: Intermediate
exl-id: e3781f79-7c8d-4512-b44f-835639b1471f
source-git-commit: 0ec122bbf134c41f95755a3b6f08eb7ef68506df
workflow-type: tm+mt
source-wordcount: '1138'
ht-degree: 5%

---

# 历程实时报告 {#journey-live-report}

>[!CONTEXTUALHELP]
>id="ajo_journey_live_report"
>title="历程实时报告"
>abstract="使用历程实时报告，您可以实时衡量和可视化历程的影响和绩效（仅限过去 24 小时）。报告分为不同的构件，详细说明历程中的成功和错误。每个报告仪表板都可以修改，您可以调整构件大小或删除构件。"

历程实时报告可通过以下路径直接从您的历程访问： **[!UICONTROL 查看报告]** 按钮。

![](assets/report_journey.png)

历程 **[!UICONTROL 实时报告]** 页面将显示以下选项卡：

* [历程](#journey-live)
* [电子邮件](#email-live)
* [推送](#push-live)
* [短信](#sms-live)

历程 **[!UICONTROL 实时报告]** 分为多个构件，其中详细描述历程的成功和错误。 如果需要，可以调整每个小部件的大小并将其删除。 有关此内容的更多信息，请参阅此 [部分](live-report.md#modify-dashboard).

有关Adobe Journey Optimizer中可用的每个量度的详细列表，请参阅 [此页面](live-report.md#list-of-components-live).

## “历程”选项卡 {#journey-live}

从您的历程 **[!UICONTROL 实时报告]**，则 **[!UICONTROL 历程]** 选项卡让您清楚地了解历程的最重要的跟踪数据。

![](assets/journey_live_1.png)

+++了解有关历程报表可用的各种量度和小部件的更多信息。

**[!UICONTROL 历程性能]** 允许您查看目标用户档案的路径，以逐步了解您的历程。

此 **[!UICONTROL 历程统计数据]** 构件显示以下KPI：

* **[!UICONTROL 输入的配置文件]**：到达历程的进入事件的个人总数。

* **[!UICONTROL 退出的配置文件]**：退出历程的个人总数。

* **[!UICONTROL 失败的个人历程]**：未成功执行的各个历程的总数。

此 **[!UICONTROL 过去24小时内执行的事件]** 和 **[!UICONTROL 事件]** 利用小组件，您可以通过摘要编号、图表和表格查看成功执行了您的哪些事件。

此 **[!UICONTROL 过去24小时内执行的操作]** 和 **[!UICONTROL 执行的操作和错误]** 构件表示在触发操作时发生的最成功的操作和错误。 操作图形、表格和概要数字包含可用于操作的数据，例如：

* **[!UICONTROL 执行的操作]**：为历程成功执行的操作总数。

* **[!UICONTROL 操作出错]**：操作发生的错误总数。
+++

## “电子邮件”选项卡 {#email-live}

从您的历程 **[!UICONTROL 实时报告]**，则 **[!UICONTROL 电子邮件]** 选项卡详细列出了与旅程中发送的电子邮件投放相关的主要信息。

![](assets/journey_live_2.png)

+++了解有关电子邮件报表可用的不同量度和小部件的更多信息。

此 **[!UICONTROL 电子邮件发送统计数据]** 构件详细说明与报文相关的主要信息：

* **[!UICONTROL 已投放]**：成功发送的消息数。

* **[!UICONTROL 跳出次数]**：投放和自动返回处理期间累计的错误总数。

* **[!UICONTROL 错误]**：投放期间发生的阻止将投放发送到用户档案的错误总数。

此 **[!UICONTROL 按电子邮件发送指标]** 表格和 **[!UICONTROL 电子邮件摘要]** 图表详细说明了您的交付是否成功：

* **[!UICONTROL 已发送]**：投放的发送总数。

* **[!UICONTROL 已投放]**：成功发送的消息数。

* **[!UICONTROL 跳出次数]**：投放和自动返回处理期间累计的错误总数。

* **[!UICONTROL 错误]**：投放期间发生的阻止将投放发送到用户档案的错误总数。

* **[!UICONTROL 打开次数]**：消息在投放中打开的次数。

* **[!UICONTROL 点击次数]**：在投放中点击内容的次数。

* **[!UICONTROL 取消订阅]**：取消订阅链接的点击次数。

* **[!UICONTROL 垃圾邮件投诉]**：将邮件声明为垃圾邮件或垃圾邮件的次数。

此 **[!UICONTROL 退回原因]**， **[!UICONTROL 退回类别]** 和 **[!UICONTROL 硬退回 — 按电子邮件]** 小组件包含与退回邮件相关的可用数据，例如：

* **[!UICONTROL 硬退回]**：永久错误的总数，如错误的电子邮件地址。 这涉及显式声明地址无效的错误消息，例如“未知用户”。

* **[!UICONTROL 软退回]**：临时错误的总数，例如收件箱已满。

* **[!UICONTROL 已忽略]**：临时总数，例如外出或技术错误，例如，如果发件人类型为postmaster。

此 **[!UICONTROL 错误原因]** 和 **[!UICONTROL 排除原因]** 利用图形和表格，可查看在投放期间发生了哪些错误和排除项。

此 **[!UICONTROL 电子邮件 — 顶级收件人域]** 图表和表详细说明了收件人最常用于打开电子邮件的域。

>[!NOTE]
>
>仅在电子邮件中插入决策时，优惠小部件和量度才可用。 有关决策管理的更多信息，请参阅此 [页面](../offers/get-started/starting-offer-decisioning.md).

此 **[!UICONTROL 优惠统计数据]** 和 **[!UICONTROL 优惠统计数据]** 随着时间的推移，小组件会衡量您选件的成功及对目标受众的影响。 它通过KPI详细描述与消息相关的主要信息：

* **[!UICONTROL 已发送优惠]**：选件的发送总数。

* **[!UICONTROL 优惠展示]**：投放中打开选件的次数。

* **[!UICONTROL 优惠点击次数]**：在投放中点击优惠的次数。
+++

## “推送通知”选项卡 {#push-live}

从您的历程 **[!UICONTROL 实时报告]**，则 **[!UICONTROL 推送通知]** 选项卡详细列出了与历程中发送的推送投放相关的主要信息。

![](assets/journey_live_3.png)

+++了解有关可用于推送报表的不同量度和小部件的更多信息。

**[!UICONTROL 推送通知发送性能]**， **[!UICONTROL 推送通知摘要]** 和 **[!UICONTROL 发送指标 — 按推送]** 构件详细列出与您的消息相关的主要信息：

* **[!UICONTROL 已发送]**：投放的发送总数。

* **[!UICONTROL 已投放]**：成功发送的消息数。

* **[!UICONTROL 跳出次数]**：投放和自动返回处理期间累计的错误总数。

* **[!UICONTROL 错误]**：投放期间发生的阻止将投放发送到用户档案的错误总数。

* **[!UICONTROL 打开次数]**：消息在投放中打开的次数。

* **[!UICONTROL 操作]**：对已投放的推送通知执行的总操作数，例如按钮点击或解除。

* **[!UICONTROL 预订]**：此推送通知的打开和操作总数，即用户档案是否打开了推送或是否单击了按钮。

此 **[!UICONTROL 错误原因]** 和 **[!UICONTROL 排除原因]** 利用图形和表格，可查看在投放期间发生了哪些错误和排除项。

此 **[!UICONTROL 发送统计信息 — 失败]** 利用小组件，可查看发生了多少错误和退回。

此 **[!UICONTROL 按平台跟踪]**， **[!UICONTROL 按平台发送]** 和 **[!UICONTROL 按平台细分]** 图表和表格根据操作系统详细说明了推送通知的成功情况。
+++

## “短信”选项卡 {#sms-live}

![](assets/journey_live_4.png)

+++了解有关短信报表可用的不同量度和小部件的更多信息。

此 **[!UICONTROL 短信 — 发送统计数据]** 表详细说明了您的交付是否成功：

* **[!UICONTROL 已定位]**：有资格作为此投放的目标用户档案的用户档案数。

* **[!UICONTROL 已排除]**：从定向用户档案中排除且未收到消息的用户用户档案数。

* **[!UICONTROL 已发送]**：投放的发送总数。

* **[!UICONTROL 已投放]**：成功发送的消息数。

* **[!UICONTROL 打开次数]**：消息在投放中打开的次数。

* **[!UICONTROL 点击次数]**：在投放中点击内容的次数。

* **[!UICONTROL 跳出次数]**：投放和自动返回处理期间累计的错误总数。

* **[!UICONTROL 错误]**：投放期间发生的阻止将投放发送到用户档案的错误总数。

此 **[!UICONTROL 短信摘要]** 图表详细说明了您的交付是否成功：

* **[!UICONTROL 已投放]**：成功发送的消息数。

* **[!UICONTROL 跳出次数]**：投放和自动返回处理期间累计的错误总数。

* **[!UICONTROL 错误]**：投放期间发生的阻止将投放发送到用户档案的错误总数。

此 **[!UICONTROL 排除原因]** 利用图形和表格，可查看在投放期间发生了哪些错误和排除项。
+++
