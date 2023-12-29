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
source-git-commit: 82b8c9032d6c377cb76acce4d5cc45afb0ddd6ba
workflow-type: tm+mt
source-wordcount: '3359'
ht-degree: 24%

---

# 营销活动全局报告 {#campaign-global-report}

>[!CONTEXTUALHELP]
>id="ajo_campaign_global_report"
>title="营销活动全局报告"
>abstract="营销活动全局报告可以衡量您的营销活动在选定时段内产生的影响。报告分为不同的构件，详细说明您营销活动中的成功和错误。可通过调整构件大小或删除构件而修改每个报告仪表板。"

全局报告，可从访问 **所有时间** 选项卡，显示至少两小时前发生的事件，并涵盖选定时间段内的事件。 相比之下，实时报表侧重于过去24小时内发生的事件，距事件发生的最小时间间隔为2分钟。

您可以使用直接从Campaign访问Campaign全局报告 **[!UICONTROL 查看报告]** 按钮。

![](assets/campaign_report_global_5.png)

营销活动 **[!UICONTROL 全局报告]** 页面将显示以下选项卡：

* [Campaign](#campaign-global)
* [电子邮件](#email-global)
* [应用程序内](#inapp-global)
* [推送](#push-global)
* [短信](#sms-global)
* [Web](#web-tab)
* [直邮](#direct-mail-global)

营销活动 **[!UICONTROL 全局报告]** 将分为多个构件，每个构件详细描述营销活动的成功和错误。 如果需要，可以调整每个小部件的大小并将其删除。 有关详细信息，请参阅此 [部分](../reports/global-report.md#modify-dashboard).

有关Adobe Journey Optimizer中可用的每个量度的详细列表，请参阅 [此页面](global-report.md#list-of-components-global.md)

## “营销活动”选项卡 {#campaign-global}

### 投放 {#delivery-global}

>[!CONTEXTUALHELP]
>id="ajo_campaign_delivery_global"
>title="营销活动的统计数据"
>abstract="“营销活动的统计数据”构件详述与您的营销活动相关的主要信息，如“进入的配置文件”和“已交付操作”。"

![](assets/campaign_report_global_1.png)

此 **[!UICONTROL 营销活动的统计数据]** 构件详细列出了与您的营销活动相关的主要信息：

* **[!UICONTROL 输入的配置文件]**：启动历程的用户档案数。

* **[!UICONTROL 已交付操作]**：历程中某个操作已交付的不重复总次数。

* **[!UICONTROL 操作失败百分比]**：与提交操作的独特次数总数相比，历程中操作失败的总独特次数。

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

此 **[!UICONTROL 试验]** 选项卡提供了有关每个变体性能的关键分析，并标识了最成功的变体。

请注意，定义最佳业绩者可能需要一些时间，该图标将代表最佳业绩者 ![](assets/experimentation_report_1.png).

+++了解有关试验报告中可用的不同量度和小组件的更多信息。

此 **[!UICONTROL 试验结果]** 构件详细说明了每个变体的性能。 您可以从中选择处理方法之一，以更改基线 **[!UICONTROL 基线]** 下拉菜单。 最佳处理方式将以星形图标表示。

下表显示了以下量度：

* **[!UICONTROL 提升度超过基线]**：衡量给定治疗的转化率相对于基线的改进百分比。

* **[!UICONTROL 置信度]**：表明给定治疗与基线治疗相同的证据。 [了解详情](../campaigns/experiment-calculations.md#understand-confidence)

* **[!UICONTROL 独特出站点击次数]**：跨出站渠道的点击总数。

* **[!UICONTROL 配置文件]**：针对此处理的用户档案数。

* **[!UICONTROL 独特出站点击次数/配置文件]**：之前创建实验时选择的成功量度的总值除以配置文件数。

此 **[!UICONTROL 置信区间]** 图表衡量改进的不确定性。 它详细说明了基线和最佳业绩处理之间的业绩差异百分比。 [了解详情](../campaigns/experiment-calculations.md#confidence-intervals)。

![](assets/experimentation_report_4.png)

最后一个小组件提供与 **[!UICONTROL 成功量度]** 您之前已为“Threads（处理）”选择了。 您可以选择从中选择其他目标量度 **[!UICONTROL 量度]** 用于跟踪替代数据的下拉菜单。

>[!CAUTION]
>
>处理试验的筛选量度时，请注意，从试验的比较页面上的下拉列表中更改量度选择将不保留筛选值。 例如，从“点击量”切换到“唯一点击量”会导致应用的过滤器丢失，导致比较不准确或无效。

+++

有关这些结果以及如何解释这些结果的深入研究，请参阅 [此页面](../campaigns/get-started-experiment.md#interpret-results).

## 电子邮件选项卡 {#email-global}

>[!CONTEXTUALHELP]
>id="ajo_campaign_global_email_sending_statistics"
>title="电子邮件 - 发送统计数据"
>abstract="“电子邮件 - 发送统计数据”表汇总有关电子邮件的基本数据，如定向邮件或已送达邮件。"

>[!CONTEXTUALHELP]
>id="ajo_campaign_global_email_tracking_statistics"
>title="电子邮件 - 跟踪统计数据"
>abstract="“电子邮件 - 跟踪统计数据”表提供有关电子邮件的配置文件活动的数据。"

>[!CONTEXTUALHELP]
>id="ajo_campaign_global_email_sending_performance"
>title="电子邮件 - 发送性能"
>abstract="“电子邮件 - 发送性能”图表呈现有关已发送电子邮件的全面数据，其中提供针对送达数和退回数等关键量度的见解，从而可详细地分析电子邮件送达过程。"

>[!CONTEXTUALHELP]
>id="ajo_campaign_global_email_bounce_categories"
>title="电子邮件 - 退回类别"
>abstract="“电子邮件 - 退回类别”图表提供有关临时错误和永久性错误的数据。"

>[!CONTEXTUALHELP]
>id="ajo_campaign_global_email_bounce_reasons"
>title="电子邮件 - 退回原因"
>abstract="“电子邮件 - 退回原因”图表包含与退回的邮件相关的可用数据。"

>[!CONTEXTUALHELP]
>id="ajo_campaign_global_email_error_reasons"
>title="电子邮件 - 错误原因"
>abstract="通过“电子邮件 - 错误原因”图表，可了解在发送过程中发生的具体错误。"

>[!CONTEXTUALHELP]
>id="ajo_campaign_global_email_excluded_reasons"
>title="电子邮件 - 排除原因"
>abstract="“排除原因”图表说明导致从目标受众中排除用户配置文件，从而收不到消息的各种因素。"

>[!CONTEXTUALHELP]
>id="ajo_campaign_global_email_top_url"
>title="电子邮件 - 热门 URL"
>abstract="“电子邮件 - 热门 URL”图表全面概述电子邮件中获得访客流量最高的 URL，从而可找出最热门的链接。"

>[!CONTEXTUALHELP]
>id="ajo_campaign_global_email_best_recipient"
>title="电子邮件 - 最佳收件人域"
>abstract="“电子邮件 - 最佳收件人域”图表详细地细分收件人最常用于打开电子邮件的域，并提供针对收件人行为的宝贵见解。"

![](assets/campaign_report_global_2.png)

来自您的营销活动 **[!UICONTROL 全局报告]**， **[!UICONTROL 电子邮件]** 选项卡详细列出了与在Campaign中发送的电子邮件投放相关的主要信息。

+++了解有关电子邮件报表可用的不同量度和小组件的更多信息。

此 **[!UICONTROL 电子邮件发送统计数据]** 图表详细说明了您的电子邮件是否成功：

* **[!UICONTROL 执行时间]**：定期电子邮件的每次执行的开始时间。 要仅定向一个或多个定期电子邮件，请从中选择它 **[!UICONTROL 执行时间]** 下拉菜单。

* **[!UICONTROL 已定位]**：发送过程中处理的消息总数。

* **[!UICONTROL 已发送]**：电子邮件的发送总数。

* **[!UICONTROL 已投放]**：成功发送的消息数，与已发送消息的总数相关。

* **[!UICONTROL 投放率]**：成功发送的消息百分比。

* **[!UICONTROL 跳出次数]**：在发送流程和自动返回处理期间累计的错误总数与已发送消息总数相关。

* **[!UICONTROL 跳出率]**：退回的电子邮件与发送的电子邮件相比的百分比。

* **[!UICONTROL 错误]**：发送过程中发生的阻止将消息发送到用户档案的错误总数。

* **[!UICONTROL 错误率]**：与已发送电子邮件相比，发送过程中发生阻止发送该邮件的错误百分比。

* **[!UICONTROL 重试]**：重试队列中的电子邮件数。

* **[!UICONTROL 已排除]**：Adobe Journey Optimizer已排除的用户档案数。

此 **[!UICONTROL 电子邮件 — 跟踪统计数据]** 小组件包含您电子邮件的用户档案活动的可用数据：

* **[!UICONTROL 执行时间]**：定期电子邮件的每次执行的开始时间。 要仅定向一个或多个定期电子邮件，请从中选择它 **[!UICONTROL 执行时间]** 下拉菜单。

* **[!UICONTROL 打开次数]**：电子邮件的打开次数。

* **[!UICONTROL 独特打开次数]**：已打开电子邮件的百分比。

* **[!UICONTROL 打开率]**：打开的电子邮件总数，与已投放的电子邮件数相比。

* **[!UICONTROL 点击次数]**：在电子邮件中点击内容的次数。

* **[!UICONTROL 独特点击]**：单击电子邮件中内容的用户档案数。

* **[!UICONTROL 独特点击率]**：与您的电子邮件交互的用户百分比。

* **[!UICONTROL 取消订阅]**：取消订阅链接的点击次数。

* **[!UICONTROL 垃圾邮件投诉数]**：将消息声明为垃圾邮件或垃圾邮件的次数。

此 **[!UICONTROL 发送性能]** 图形包含可用于已发送电子邮件的数据，例如：

* **[!UICONTROL 已投放]**：成功发送的消息数，与已发送消息的总数相关。

* **[!UICONTROL 跳出次数]**：在发送流程和自动返回处理期间累计的错误总数与已发送消息总数相关。

* **[!UICONTROL 重试]**：重试队列中的电子邮件数。

* **[!UICONTROL 错误]**：发送过程中发生的阻止将消息发送到用户档案的错误总数。

此 **[!UICONTROL 退回原因]** 和 **[!UICONTROL 退回类别]** 小组件包含与退回邮件相关的可用数据，例如：

* **[!UICONTROL 硬退回]**：永久错误的总数，如错误的电子邮件地址。 这涉及显式声明地址无效的错误消息，例如“未知用户”。

* **[!UICONTROL 软退回]**：临时错误的总数，如收件箱已满。

* **[!UICONTROL 已忽略]**：临时总数，例如外出或技术错误，例如，如果发件人类型是邮递员。

有关退回的详细信息，请参阅 [禁止显示列表](../reports/suppression-list.md) 页面。

此 **[!UICONTROL 错误原因]** 利用图表和表格，可查看在发送过程中发生的错误。

此 **[!UICONTROL 排除的原因]** 图形和表格可显示阻止从定向用户档案中排除的用户用户档案接收消息的不同原因。

此 **[!UICONTROL 电子邮件 — 顶部URL]** 图表和表详细列出了电子邮件中访问次数最多的URL。

此 **[!UICONTROL 电子邮件 — 顶级收件人域]** 图表和表详细说明了用户档案最常用于打开电子邮件的域。

>[!CAUTION]
>
> 此 **[!UICONTROL 电子邮件 — 顶级收件人域]** 构件的准确率为99.95%。

此 **[!UICONTROL 电子邮件 — 已优化与普通]** 图表详细列出了与报文相关的主要信息，无论它们是否已优化：

* **[!UICONTROL 已发送]**：发送总数。

* **[!UICONTROL 打开次数]**：消息的打开次数。

* **[!UICONTROL 点击次数]**：在电子邮件中点击内容的次数。

此 **[!UICONTROL 电子邮件 — 发送时间优化]** 根据发送方法详细描述电子邮件的成功情况：已优化或正常。

* **[!UICONTROL 已投放]**：成功发送的消息数，与已发送消息的总数相关。

* **[!UICONTROL 跳出次数]**：在发送流程和自动返回处理期间累计的错误总数与已发送消息总数相关。

>[!NOTE]
>
>此 **[!UICONTROL 已优化和未优化]** 和 **[!UICONTROL 发送时间优化]**  仅当为电子邮件激活发送时间优化选项时，小组件才可用。 有关发送时间优化的详细信息，请参阅 [此页面](../building-journeys/journeys-message.md#send-time-optimization).

+++

## 应用程序内选项卡 {#inapp-global}

>[!CONTEXTUALHELP]
>id="ajo_campaign_global_inapp_performance"
>title="应用程序内性能"
>abstract="“应用程序内性能”KPI 提供针对访客与应用程序内消息互动的基本见解。"

>[!CONTEXTUALHELP]
>id="ajo_campaign_global_inapp_interactions"
>title="按类型列出的交互"
>abstract="“按类型列出的交互”图表通过跟踪任何点击、取消或交互而详述用户如何与应用程序内消息交互。"

>[!CONTEXTUALHELP]
>id="ajo_campaign_global_inapp_summary"
>title="应用程序内摘要"
>abstract="“应用程序内摘要”图表显示指定时段内应用程序内展示和交互的进展。"

来自您的营销活动 **[!UICONTROL 全局报告]**， **[!UICONTROL 应用程序内]** 选项卡详细列出了与您的营销活动中发送的应用程序内投放相关的主要信息。

![](assets/campaign_report_global_6.png)

+++了解有关可用于应用程序内报表的不同量度和小组件的更多信息。

此 **[!UICONTROL 应用程序内性能]** KPI可详细列出与访客与应用程序内消息互动相关的主要信息，例如：

* **[!UICONTROL 独特展示次数]**：将应用程序内消息传递到的独特用户数。

* **[!UICONTROL 展示次数]**：交付给所有用户的应用程序内消息总数。

* **[!UICONTROL 交互率]**：与应用程序内消息互动的百分比。 这包括用户执行的任何操作，例如单击、解除或任何其他交互。

此 **[!UICONTROL 按类型列出的交互]** 图表和表详细介绍了用户如何通过跟踪任何点击、解除或交互来与您的应用程序内消息进行交互。

此 **[!UICONTROL 应用程序内摘要]** 图形可显示应用程序内展示次数和交互在相关时间段的演变。
+++

## 推送通知选项卡 {#push-global}

>[!CONTEXTUALHELP]
>id="ajo_campaign_global_push_sending_statistics"
>title="推送通知 - 发送统计数据"
>abstract="“推送通知发送统计数据”表汇总有关推送通知的基本数据，如定向消息或已送达消息。"

>[!CONTEXTUALHELP]
>id="ajo_campaign_global_push_tracking_statistics"
>title="推送通知 – 跟踪统计数据"
>abstract="“推送跟踪统计数据”提供有关推送通知的配置文件活动的数据。"

>[!CONTEXTUALHELP]
>id="ajo_campaign_global_push_sending_summary"
>title="推送通知 - 发送摘要"
>abstract="“推送通知发送摘要”图表显示对于已发送的推送通知可用的数据。"

>[!CONTEXTUALHELP]
>id="ajo_campaign_global_push_excluded_reasons"
>title="推送通知 - 排除原因"
>abstract="“排除原因”图表说明导致从目标受众中排除用户配置文件，从而收不到消息的各种因素。"

>[!CONTEXTUALHELP]
>id="ajo_campaign_global_push_error_reasons"
>title="推送通知 - 错误原因"
>abstract="通过“错误原因”图表，可了解在发送过程中发生的具体错误。"

>[!CONTEXTUALHELP]
>id="ajo_campaign_global_push_breakdown_platform"
>title="推送通知 - 按平台细分"
>abstract="“按平台细分”图表根据配置文件的操作系统细分推送通知的成功情况。"

来自您的营销活动 **[!UICONTROL 全局报告]**， **[!UICONTROL 推送通知]** 选项卡详细列出了与您的营销活动中发送的推送投放相关的主要信息。

![](assets/campaign_report_global_3.png)应用程序内性能KPI可详细列出与访客对应用程序内消息的参与度相关的主要信息。

+++了解有关可用于推送报表的不同量度和小组件的更多信息。

此 **[!UICONTROL 推送通知 — 发送统计数据]** 该表详细列出了与推送通知相关的主要信息：

* **[!UICONTROL 执行时间]**：每次执行定期推送通知的开始时间。 要仅定位一个或多个定期推送通知，请从以下位置选择通知： **[!UICONTROL 执行时间]** 下拉菜单。

* **[!UICONTROL 已定位]**：分析期间处理的消息总数。

* **[!UICONTROL 已发送]**：推送通知的发送总数。

* **[!UICONTROL 已投放]**：成功发送的消息数，与已发送消息的总数相关。

* **[!UICONTROL 投放率]**：成功发送的消息百分比。

* **[!UICONTROL 跳出次数]**：在发送流程和自动返回处理期间累计的错误总数与已发送消息总数相关。

* **[!UICONTROL 跳出率]**：退回的推送通知与已发送的推送通知相比的百分比。

* **[!UICONTROL 错误]**：阻止将其发送到用户档案的错误总数。

* **[!UICONTROL 错误率]**：与发送的推送通知相比，在阻止发送该通知期间发生的错误百分比。

* **[!UICONTROL 已排除]**：Adobe Journey Optimizer已排除的用户档案数。

此 **[!UICONTROL 推送 — 跟踪统计数据]** 包含推送通知的用户档案活动的可用数据：

* **[!UICONTROL 执行时间]**：每次执行定期推送通知的开始时间。 要仅定位一个或多个定期推送通知，请从以下位置选择通知： **[!UICONTROL 执行时间]** 下拉菜单。

* **[!UICONTROL 打开次数]**：推送通知的打开次数。

* **[!UICONTROL 打开率]**：已打开推送通知的百分比。

* **[!UICONTROL 操作]**：对已投放推送通知执行的总操作数，例如按钮点击或解除。

* **[!UICONTROL 参与]**：此推送通知的打开和操作总数，即如果用户档案打开了推送或单击了按钮。

* **[!UICONTROL 参与率]**：此推送通知的打开和操作百分比，即如果用户档案打开了推送或单击了按钮。

此 **[!UICONTROL 推送通知摘要]** 图形包含可用于已发送推送通知的数据，例如：

* **[!UICONTROL 打开次数]**：推送通知的打开次数。

* **[!UICONTROL 操作]**：对已投放推送通知执行的总操作数，例如按钮点击或解除。

* **[!UICONTROL 跳出次数]**：与已发送消息总数相关的累积和自动返回处理的错误总数。

* **[!UICONTROL 已投放]**：成功发送的消息数，与已发送消息的总数相关。

* **[!UICONTROL 错误]**：阻止将其发送到用户档案的错误总数。

>[!NOTE]
>
>此 **[!UICONTROL 已优化和未优化]** 和 **[!UICONTROL 发送时间优化]**  仅当为推送通知激活发送时间优化选项时，构件才可用。 有关发送时间优化的详细信息，请参阅 [此页面](../building-journeys/journeys-message.md#send-time-optimization).

此 **[!UICONTROL 已优化和未优化]** 图表详细列出了与报文相关的主要信息，无论它们是否已优化：

* **[!UICONTROL 已投放]**：成功发送的消息数，与已发送消息的总数相关。

* **[!UICONTROL 打开次数]**：推送通知的打开次数。

* **[!UICONTROL 操作]**：对已投放推送通知执行的总操作数，例如按钮点击或解除。

此 **[!UICONTROL 发送时间优化]** 根据发送方法（已优化或正常）详细描述推送通知的成功情况。

* **[!UICONTROL 已投放]**：成功发送的消息数，与已发送消息的总数相关。

* **[!UICONTROL 跳出次数]**：在发送流程和自动返回处理期间累计的错误总数与已发送消息总数相关。

此 **[!UICONTROL 错误原因]** 图表和表格允许您查看发生的错误。

此 **[!UICONTROL 排除的原因]** 图形和表格可显示阻止从定向用户档案中排除的用户用户档案接收消息的不同原因。

此 **[!UICONTROL 按平台细分]** 图表和表会根据用户档案的操作系统详细描述推送通知的成功情况。
+++

## 短信选项卡 {#sms-global}

>[!CONTEXTUALHELP]
>id="ajo_campaign_global_sms_sending_statistics"
>title="短信 - 发送统计数据"
>abstract="“短信发送统计数据”表汇总有关短信的基本数据，如定向消息或已送达消息。"

>[!CONTEXTUALHELP]
>id="ajo_campaign_global_sms_error_reasons"
>title="短信 - 错误原因"
>abstract="通过“短信 - 错误原因”图表，可了解在发送过程中发生的具体错误。"

>[!CONTEXTUALHELP]
>id="ajo_campaign_global_sms_performance"
>title="短信 - 按日期显示效果"
>abstract="“短信 - 按日期显示效果”构件以图形表示形式提供有关消息的关键信息。"

>[!CONTEXTUALHELP]
>id="ajo_campaign_global_sms_excluded_reasons"
>title="短信 - 排除原因"
>abstract="“排除原因”图表说明导致从目标受众中排除用户配置文件，从而收不到消息的各种因素。"

>[!CONTEXTUALHELP]
>id="ajo_campaign_global_sms_bounces_reasons"
>title="短信 - 退回原因"
>abstract="“退回原因”图表包含与退回邮件相关的可用数据。"

>[!CONTEXTUALHELP]
>id="ajo_campaign_global_sms_clicks_links"
>title="短信 - 按链接显示的点击次数"
>abstract="“短信 - 按链接显示的点击次数”构件提供有关访客与消息中的 URL 互动的基本见解"

来自您的营销活动 **[!UICONTROL 全局报告]**， **[!UICONTROL 短信]** 选项卡详细列出了与您的营销活动中发送的短信投放相关的主要信息。

![](assets/campaign_report_global_4.png)

+++了解有关短信报告可用的不同量度和小组件的更多信息。

此 **[!UICONTROL 短信 — 发送统计数据]** 该表详细列出了短信消息的成功情况：

* **[!UICONTROL 执行时间]**：每次执行定期短信消息的开始时间。 要仅定向一条或多条定期短信消息，请从中选择它 **[!UICONTROL 执行时间]** 下拉菜单。

* **[!UICONTROL 已定位]**：符合目标配置文件资格的用户配置文件数。

* **[!UICONTROL 已排除]**：从定向用户档案中排除且未收到消息的用户用户档案数。

* **[!UICONTROL 已发送]**：短信消息的发送总数。

* **[!UICONTROL 跳出次数]**：在发送流程和自动返回处理期间累计的错误总数与已发送消息总数相关。

* **[!UICONTROL 错误]**：阻止将其发送到用户档案的错误总数。

此 **[!UICONTROL 按日期划分的短信性能]** 构件以图表形式详细描述与消息相关的主要信息：

* **[!UICONTROL 已发送]**：短信消息的发送总数。

* **[!UICONTROL 跳出次数]**：在发送流程和自动返回处理期间累计的错误总数与已发送消息总数相关。

* **[!UICONTROL 错误]**：阻止将其发送到用户档案的错误总数。

此 **[!UICONTROL 排除原因]** 和 **[!UICONTROL 退回原因]** 和 **[!UICONTROL 错误原因]** 利用图形和表格，可查看在发送过程中发生的错误和排除情况。

此 **[!UICONTROL 短信 — 按链接显示的点击次数]** 小组件提供了与访客对您的URL的参与度相关的主要信息的详细信息。

+++

## Web 选项卡 {#web-tab}

>[!CONTEXTUALHELP]
>id="ajo_campaign_global_web_performance"
>title="Web 性能"
>abstract="“Web 性能”KPI 提供有关访客与 Web 体验的互动的全面信息。"

>[!CONTEXTUALHELP]
>id="ajo_campaign_global_web_summary"
>title="Web 摘要"
>abstract="“Web 摘要”图表说明指定时段内 Web 体验的进展情况，包括展示次数、独特展示次数和交互次数。"

>[!CONTEXTUALHELP]
>id="ajo_campaign_global_web_interactions"
>title="按元素列出的交互"
>abstract="“按元素列出的交互”表提供有关访客与网页上不同元素进行互动的关键信息。"

来自您的营销活动 **[!UICONTROL 全局报告]**， **[!UICONTROL Web]** 选项卡详细列出了与您的网页相关的主要信息。

![](assets/web-report.png)

+++了解更多可用于Web报表的不同量度和小组件。

此 **[!UICONTROL Web性能]** KPI可详细列出与访客对Web体验的参与度相关的主要信息，例如：

* **[!UICONTROL 独特展示次数]**：将Web体验交付给的独特用户数。

* **[!UICONTROL 展示次数]**：交付给所有用户的Web体验总数。

* **[!UICONTROL 互动率]**：与网页互动的百分比。 这包括用户执行的任何操作，例如点击或任何其他交互。

此 **[!UICONTROL Web摘要]** 图形可显示相关时间段内Web体验（展示次数、独特展示次数和交互）的演变。

此 **[!UICONTROL 按元素显示的交互]** 该表详细列出了与访客对网页上各种元素的参与度相关的主要信息。
+++

## 直邮选项卡 {#direct-mail-global}

>[!CONTEXTUALHELP]
>id="ajo_campaign_global_direct_sending_statistics"
>title="直邮 - 发送统计数据"
>abstract="“直邮发送统计数据”表汇总有关直邮的基本数据，如定向邮件或已送达邮件。"

>[!CONTEXTUALHELP]
>id="ajo_campaign_global_direct_error_reasons"
>title="直邮 - 错误原因"
>abstract="通过“直邮 - 错误原因”图表，可了解在发送过程中发生的具体错误。"

>[!CONTEXTUALHELP]
>id="ajo_campaign_global_direct_excluded_reasons"
>title="直邮 - 排除原因"
>abstract="“直邮排除原因”图表说明导致从目标受众中排除用户配置文件，从而收不到消息的各种因素。"

来自您的营销活动 **[!UICONTROL 全局报告]**， **[!UICONTROL 直邮]** 选项卡详细列出了与直邮投放相关的主要信息。

![](assets/direct-mail-report_1.png)

+++了解有关直邮报表可用的不同量度和小组件的更多信息。

此 **[!UICONTROL 直邮 — 发送统计数据]** 该表详细列出了直邮的成功情况：

* **[!UICONTROL 执行时间]**：每次执行定期直邮的开始时间。 要仅定向一封或多封定期直邮，请从 **[!UICONTROL 执行时间]** 下拉菜单。

* **[!UICONTROL 已定位]**：有资格作为此直邮的目标用户档案的用户档案数。

* **[!UICONTROL 已发送]**：此直邮的发送总数。

* **[!UICONTROL 错误]**：发送过程中发生的阻止将消息发送到用户档案的错误总数。

* **[!UICONTROL 已排除]**：从定向用户档案中排除、未收到直邮的用户用户档案数。

此 **[!UICONTROL 直邮 — 排除的原因]** 和 **[!UICONTROL 直邮 — 错误原因]** 利用图形和表格，可查看在发送过程中发生的错误和排除情况。
+++

## 其他资源

* [营销活动入门](../campaigns/get-started-with-campaigns.md)
* [创建营销活动](../campaigns/create-campaign.md)
* [创建API触发的营销活动](../campaigns/api-triggered-campaigns.md)
* [修改或停止营销活动](../campaigns/modify-stop-campaign.md)
* [营销活动实时报告](campaign-live-report.md)
