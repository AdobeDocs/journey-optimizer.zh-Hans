---
solution: Journey Optimizer
product: journey optimizer
title: 营销活动全局报告
description: 了解如何使用Campaign全局报告中的数据
feature: Reporting
topic: Content Management
role: User
level: Intermediate
exl-id: fa64f5b8-75f2-40e6-8566-5766fafe6cd6
source-git-commit: 0d8a19568e52952f3bc8af3c768cef4804a31749
workflow-type: tm+mt
source-wordcount: '2283'
ht-degree: 4%

---

# 营销活动全局报告 {#campaign-global-report}

>[!CONTEXTUALHELP]
>id="ajo_campaign_global_report"
>title="营销活动全局报告"
>abstract="营销活动全局报告可以衡量您的营销活动在选定时段内产生的影响。报告分为不同的构件，详细说明您营销活动中的成功和错误。每个报告仪表板都可以修改，您可以调整构件大小或删除构件。"

全局报告可从“所有时间”选项卡访问，它显示至少两个小时前发生的事件，并涵盖选定时间段内的事件。 相比之下，实时报表侧重于过去24小时内发生的事件，距事件发生的最小时间间隔为2分钟。

Campaign全局报告可通过以下方式直接从您的Campaign访问： **[!UICONTROL 查看报告]** 按钮。

![](assets/campaign_report_global_5.png)

营销活动 **[!UICONTROL 全局报告]** 页面将显示以下选项卡：

* [Campaign](#campaign-global)
* [电子邮件](#email-global)
* [应用程序内](#inapp-global)
* [推送](#push-global)
* [短信](#sms-global)
* [Web](#web-tab)

营销活动 **[!UICONTROL 全局报告]** 将被划分为多个构件，这些构件详细描述营销活动的成功和错误。 如果需要，可以调整每个小部件的大小并将其删除。 有关此内容的更多信息，请参阅此 [部分](../reports/global-report.md#modify-dashboard).

有关Adobe Journey Optimizer中可用的每个量度的详细列表，请参阅 [此页面](global-report.md#list-of-components-global.md)

## “营销活动”选项卡 {#campaign-global}

### 交付 {#delivery-global}

![](assets/campaign_report_global_1.png)

此 **[!UICONTROL 营销活动的统计数据]** 构件详细列出了与您的营销活动相关的主要信息：

* **[!UICONTROL 输入的配置文件]**：启动历程的用户档案数。

* **[!UICONTROL 已交付操作]**：历程中交付操作的唯一总次数。

* **[!UICONTROL 操作失败百分比]**：与已交付操作的独特次数总数相比，历程中操作的独特失败总次数。

<!--
### Objectives report {#objectives-global}

![](assets/performance_report.gif)

The **[!UICONTROL Objectives]** tab allows you to better fine-tune your deliveries' reports by targeting one specific metric.

The **[!UICONTROL Objectives]** listed are linked to **[!UICONTROL Datasets]** that define a connection to a system in order to retrieve additional information. A list of built-in **[!UICONTROL Objectives]** is available but you can add your own by adding new **[!UICONTROL Dataset]**. For the detailed procedure, refer to this [section](../campaigns/reporting-configuration.md).

After selecting the Objectives you want to target on, the two **[!UICONTROL Performance overview]** and **[!UICONTROL Campaign objective]** widgets will provide a detailed summary of your delivery performance. 

With the **[!UICONTROL Campaign objective]** widget, you can also choose to compare your main objective with another metric.
-->

### 试验报告 {#experimentation-global}

>[!CONTEXTUALHELP]
>id="ajo_campaigns_content_experiment_click"
>title="成功量度"
>abstract="您之前在创建试验时选择的成功量度的总值，除以配置文件数。"

![](assets/experimentation_report_3.png)

此 **[!UICONTROL 试验]** 选项卡提供了有关每个变体的性能的关键分析，并标识了最成功的变体。

请注意，定义最佳业绩者可能需要一些时间，它将由此图标表示 ![](assets/experimentation_report_1.png).

+++了解有关试验报表可用的不同量度和小部件的更多信息。

此 **[!UICONTROL 实验结果]** 构件详细说明每个变体的性能。 通过从中选择处理方法之一，可以更改基线 **[!UICONTROL 基线]** 下拉列表。 最佳处理方式将以星形图标表示。

下表显示了以下量度：

* **[!UICONTROL 提升度超过基线]**：衡量给定疗法的转化率相对于基线的提高百分比。

* **[!UICONTROL 置信度]**：表明给定治疗与基线治疗相同的证据。 [了解详情](../campaigns/experiment-calculations.md#understand-confidence)

* **[!UICONTROL 独特出站点击次数]**：跨出站渠道的点击总数。

* **[!UICONTROL 配置文件]**：针对此处理的用户档案数。

* **[!UICONTROL 独特出站点击次数/个人资料]**：成功量度的总值（之前创建实验时选择）除以用户档案数。

此 **[!UICONTROL 置信区间]** 图表衡量改进的不确定性。 它详细说明了基线和最佳业绩处理之间的业绩差异百分比。 [了解详情](../campaigns/experiment-calculations.md#confidence-intervals)。
+++

要深入了解这些结果以及如何解释这些结果，请参阅 [此页面](../campaigns/get-started-experiment.md#interpret-results).

## “电子邮件”选项卡 {#email-global}

![](assets/campaign_report_global_2.png)

来自您的营销活动 **[!UICONTROL 全局报告]**，则 **[!UICONTROL 电子邮件]** 选项卡详细列出了与在Campaign中发送的电子邮件投放相关的主要信息。

+++了解有关电子邮件报表可用的不同量度和小部件的更多信息。

此 **[!UICONTROL 电子邮件发送统计数据]** 图表详细说明了您的交付是否成功：

* **[!UICONTROL 已定位]**：投放分析期间处理的消息总数。

* **[!UICONTROL 已发送]**：投放的发送总数。

* **[!UICONTROL 已投放]**：成功发送的消息数，与已发送消息的总数相关。

* **[!UICONTROL 投放率]**：成功发送的消息百分比。

* **[!UICONTROL 跳出次数]**：投放和自动返回处理期间累计的错误总数与已发送消息的总数相关。

* **[!UICONTROL 跳出率]**：与已发送电子邮件相比退回的电子邮件百分比。

* **[!UICONTROL 错误]**：投放期间发生的阻止将投放发送到用户档案的错误总数。

* **[!UICONTROL 错误率]**：与已发送电子邮件相比，投放期间发生阻止发送该投放的错误百分比。

* **[!UICONTROL 重试]**：重试队列中的电子邮件数。

* **[!UICONTROL 已排除]**：Adobe Journey Optimizer已排除的用户档案数。

此 **[!UICONTROL 电子邮件 — 跟踪统计数据]** 构件包含投放的收件人活动可用数据：

* **[!UICONTROL 打开次数]**：投放在投放中打开的次数。

* **[!UICONTROL 独特打开次数]**：已打开投放的百分比。

* **[!UICONTROL 打开率]**：已打开的电子邮件总数，与已投放的电子邮件数相比。

* **[!UICONTROL 点击次数]**：内容在电子邮件中的点击次数。

* **[!UICONTROL 独特点击次数]**：单击电子邮件中内容的收件人数量。

* **[!UICONTROL 独特点击率]**：与投放交互的用户百分比。

* **[!UICONTROL 取消订阅]**：取消订阅链接的点击次数。

* **[!UICONTROL 垃圾邮件投诉]**：将邮件声明为垃圾邮件或垃圾邮件的次数。

此 **[!UICONTROL 发送统计数据]** 图形包含可用于已发送电子邮件的数据，例如：

* **[!UICONTROL 已投放]**：成功发送的消息数，与已发送消息的总数相关。

* **[!UICONTROL 跳出次数]**：投放和自动返回处理期间累计的错误总数与已发送消息的总数相关。

* **[!UICONTROL 重试]**：重试队列中的电子邮件数。

* **[!UICONTROL 错误]**：投放期间发生的阻止将投放发送到用户档案的错误总数。

此 **[!UICONTROL 退回原因]** 和 **[!UICONTROL 退回类别]** 小组件包含与退回邮件相关的可用数据，例如：

* **[!UICONTROL 硬退回]**：永久错误的总数，如错误的电子邮件地址。 这涉及显式声明地址无效的错误消息，例如“未知用户”。

* **[!UICONTROL 软退回]**：临时错误的总数，例如收件箱已满。

* **[!UICONTROL 已忽略]**：临时总数，例如外出或技术错误，例如，如果发件人类型为postmaster。

有关退回的详细信息，请参阅 [禁止显示列表](../reports/suppression-list.md) 页面。

此 **[!UICONTROL 错误原因]** 图表和表格允许您查看在交付过程中发生的错误。

此 **[!UICONTROL 排除的原因]** 图表和表格显示了阻止从目标用户档案中排除的用户配置文件接收消息的不同原因。

此 **[!UICONTROL 电子邮件 — 顶部URL]** 图表和表详细说明了投放中访问次数最多的URL。

此 **[!UICONTROL 电子邮件 — 顶级收件人域]** 图表和表详细说明了收件人最常用于打开电子邮件的域。

>[!NOTE]
>
>此 **[!UICONTROL 已优化和未优化]** 和 **[!UICONTROL 发送时间优化]**  仅当为投放激活发送时间优化选项时，构件才可用。 有关发送时间优化的详细信息，请参阅 [此页面](../building-journeys/journeys-message.md#send-time-optimization).

此 **[!UICONTROL 已优化和未优化]** 图表详细说明与报文相关的主要信息，无论它们是否已优化：

* **[!UICONTROL 已发送]**：投放的发送总数。
* **[!UICONTROL 打开次数]**：投放在投放中打开的次数。
* **[!UICONTROL 点击次数]**：内容在电子邮件中的点击次数。

此 **[!UICONTROL 发送时间优化]** 根据发送方法（已优化或正常）详细描述投放的成功情况。

* **[!UICONTROL 已投放]**：成功发送的消息数，与已发送消息的总数相关。
* **[!UICONTROL 跳出次数]**：投放和自动返回处理期间累计的错误总数与已发送消息的总数相关。
+++

## “应用程序内”选项卡 {#inapp-global}

来自您的营销活动 **[!UICONTROL 全局报告]**，则 **[!UICONTROL 应用程序内]** 选项卡详细列出了与您的营销活动中发送的应用程序内投放相关的主要信息。

![](assets/campaign_report_global_6.png)

+++了解有关可用于应用程序内报表的不同量度和小部件的更多信息。

此 **[!UICONTROL 应用程序内性能]** KPI详细列出与访客对应用程序内消息的参与度相关的主要信息，例如：

* **[!UICONTROL 独特展示次数]**：向其传递应用程序内消息的独特用户数。

* **[!UICONTROL 展示次数]**：交付给所有用户的应用程序内消息总数。

* **[!UICONTROL 点击率]**：与查看了消息的用户相比，与应用程序内消息中包含的按钮进行交互的用户百分比。

* **[!UICONTROL 解除率]**：收件人已解除的应用程序内消息的百分比。

此 **[!UICONTROL 应用程序内摘要]** 图形可显示相关时段内应用程序内展示的演变。

此 **[!UICONTROL 按按钮显示的点击次数]** 图表和表包含每个按钮的收件人行为的可用数据：

* **[!UICONTROL 点击次数]**：与应用程序内消息中包含的按钮进行交互的收件人总数。

* **[!UICONTROL 点击率]**：与查看了消息的用户相比，与应用程序内消息中包含的按钮进行交互的用户百分比。
+++

## “推送通知”选项卡 {#push-global}

来自您的营销活动 **[!UICONTROL 全局报告]**，则 **[!UICONTROL 推送通知]** 选项卡详细列出了与您的营销活动中发送的推送投放相关的主要信息。

![](assets/campaign_report_global_3.png)

+++了解有关可用于推送报表的不同量度和小部件的更多信息。

此 **[!UICONTROL 推送通知 — 发送统计数据]** 该表通过图表和KPI详细列出了与推送通知相关的主要信息：

* **[!UICONTROL 已定位]**：投放分析期间处理的消息总数。

* **[!UICONTROL 已发送]**：投放的发送总数。

* **[!UICONTROL 已投放]**：成功发送的消息数，与已发送消息的总数相关。

* **[!UICONTROL 投放率]**：成功发送的消息百分比。

* **[!UICONTROL 跳出次数]**：投放和自动返回处理期间累计的错误总数与已发送消息的总数相关。

* **[!UICONTROL 跳出率]**：退回的推送通知相对于已发送的推送通知的百分比。

* **[!UICONTROL 错误]**：投放期间发生的阻止将投放发送到用户档案的错误总数。

* **[!UICONTROL 错误率]**：与发送的推送通知相比，在投放期间发生阻止发送该投放的错误百分比。

* **[!UICONTROL 已排除]**：Adobe Journey Optimizer已排除的用户档案数。

此 **[!UICONTROL 推送 — 跟踪统计数据]** 包含投放的收件人活动的可用数据：

* **[!UICONTROL 打开次数]**：消息在投放中打开的次数。

* **[!UICONTROL 打开率]**：已打开推送通知的百分比。

* **[!UICONTROL 操作]**：对已投放的推送通知执行的总操作数，例如按钮点击或解除。

* **[!UICONTROL 预订]**：此推送通知的打开和操作总数，即用户档案是否打开了推送或是否单击了按钮。

* **[!UICONTROL 参与率]**：此推送通知的打开和操作百分比，即用户档案是否已打开推送或是否单击了按钮。

此 **[!UICONTROL 推送通知摘要]** 图形包含可用于已发送推送通知的数据，例如：

* **[!UICONTROL 打开次数]**：消息在投放中打开的次数。

* **[!UICONTROL 操作]**：对已投放的推送通知执行的总操作数，例如按钮点击或解除。

* **[!UICONTROL 跳出次数]**：投放和自动返回处理期间累计的错误总数与已发送消息的总数相关。

* **[!UICONTROL 已投放]**：成功发送的消息数，与已发送消息的总数相关。

* **[!UICONTROL 错误]**：投放期间发生的阻止将投放发送到用户档案的错误总数。

>[!NOTE]
>
>此 **[!UICONTROL 已优化和未优化]** 和 **[!UICONTROL 发送时间优化]**  仅当为投放激活发送时间优化选项时，构件才可用。 有关发送时间优化的详细信息，请参阅 [此页面](../building-journeys/journeys-message.md#send-time-optimization).

此 **[!UICONTROL 已优化和未优化]** 图表详细说明与报文相关的主要信息，无论它们是否已优化：

* **[!UICONTROL 已投放]**：成功发送的消息数，与已发送消息的总数相关。
* **[!UICONTROL 打开次数]**：投放在投放中打开的次数。
* **[!UICONTROL 操作]**：对已投放的推送通知执行的总操作数，例如按钮点击或解除。

此 **[!UICONTROL 发送时间优化]** 根据发送方法（已优化或正常）详细描述投放的成功情况。

* **[!UICONTROL 已投放]**：成功发送的消息数，与已发送消息的总数相关。
* **[!UICONTROL 跳出次数]**：投放和自动返回处理期间累计的错误总数与已发送消息的总数相关。

此 **[!UICONTROL 错误原因]** 图表和表格允许您查看在交付过程中发生的错误。

此 **[!UICONTROL 排除的原因]** 图表和表格显示了阻止从目标用户档案中排除的用户配置文件接收消息的不同原因。

此 **[!UICONTROL 按平台跟踪]**， **[!UICONTROL 按平台发送]** 和 **[!UICONTROL 按平台细分]** 图表和表格根据收件人的操作系统详细说明了推送通知的成功情况。
+++

## “短信”选项卡 {#sms-global}

来自您的营销活动 **[!UICONTROL 全局报告]**，则 **[!UICONTROL 短信]** 选项卡详细列出了与您的营销活动中发送的短信投放相关的主要信息。

![](assets/campaign_report_global_4.png)

+++了解有关短信报表可用的不同量度和小部件的更多信息。

此 **[!UICONTROL 短信 — 发送统计数据]** 表详细说明了您的交付是否成功：

* **[!UICONTROL 已定位]**：有资格作为此投放的目标用户档案的用户档案数。

* **[!UICONTROL 已排除]**：从定向用户档案中排除且未收到消息的用户用户档案数。

* **[!UICONTROL 已发送]**：投放的发送总数。

* **[!UICONTROL 跳出次数]**：投放和自动返回处理期间累计的错误总数与已发送消息的总数相关。

* **[!UICONTROL 错误]**：投放期间发生的阻止将投放发送到用户档案的错误总数。

此 **[!UICONTROL 短信性能（按日期）]** 构件以图表形式详细描述与报文相关的主要信息：

* **[!UICONTROL 已发送]**：投放的发送总数。

* **[!UICONTROL 跳出次数]**：投放和自动返回处理期间累计的错误总数与已发送消息的总数相关。

* **[!UICONTROL 错误]**：投放期间发生的阻止将投放发送到用户档案的错误总数。

此 **[!UICONTROL 排除原因]**， **[!UICONTROL 退回原因]** 和 **[!UICONTROL 错误原因]** 利用图形和表格，可查看在投放期间发生了哪些错误和排除项。

此 **[!UICONTROL 短信 — 按链接显示的点击次数]** 和 **[!UICONTROL 短信 — 跟踪统计数据]** 小组件详细介绍了与访客对您的URL的参与度相关的主要信息。

+++

## Web选项卡 {#web-tab}

来自您的营销活动 **[!UICONTROL 全局报告]**，则 **[!UICONTROL Web]** 选项卡详细列出了与您的网页相关的主要信息。

![](assets/web-report.png)

+++了解有关Web报表可用的不同量度和小部件的更多信息。

此 **[!UICONTROL Web性能]** KPI详细列出了与访客对Web体验的参与度相关的主要信息，例如：

* **[!UICONTROL 独特展示次数]**：将Web体验提供给的独特用户数。

* **[!UICONTROL 展示次数]**：交付给所有用户的Web体验总数。

* **[!UICONTROL 点击率]**：与网页上的各种元素进行交互的访客百分比。

此 **[!UICONTROL Web摘要]** 图形可显示相关时段内Web体验（展示次数、独特展示次数和点击次数）的演变。

此 **[!UICONTROL 按元素显示的点击次数]** 该表详细列出了与访客对网页上各种元素的参与度相关的主要信息。
+++

## 其他资源

* [营销活动入门](../campaigns/get-started-with-campaigns.md)
* [创建营销活动](../campaigns/create-campaign.md)
* [创建API触发的营销活动](../campaigns/api-triggered-campaigns.md)
* [修改或停止营销活动](../campaigns/modify-stop-campaign.md)
* [营销活动实时报告](campaign-live-report.md)
