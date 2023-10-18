---
solution: Journey Optimizer
product: journey optimizer
title: 营销活动实时报告
description: 了解如何使用Campaign实时报告中的数据
feature: Reporting, Campaigns
topic: Content Management
role: User
level: Intermediate
exl-id: 925494b6-e08a-4bd3-8a2f-96a5d9cbc387
source-git-commit: 03c714833930511fa734662b637d2416728073c2
workflow-type: tm+mt
source-wordcount: '2063'
ht-degree: 39%

---

# 营销活动实时报告 {#campaign-live-report}

>[!CONTEXTUALHELP]
>id="ajo_campaign_live_report"
>title="营销活动实时报告"
>abstract="使用营销活动实时报告，您可以实时衡量和可视化营销活动的影响和绩效（仅限过去 24 小时）。报告分为不同的构件，详细说明您营销活动中的成功和错误。可通过调整构件大小或删除构件而修改每个报告仪表板。"

实时报告可从“最近24小时”选项卡访问，它显示过去24小时内发生的事件，最小时间间隔为距事件发生两分钟。 相比之下，全局报告重点关注至少两小时前发生的事件，并涵盖选定时间段内的事件。

营销活动实时报告可以通过以下方式直接从您的营销活动访问 **[!UICONTROL 实时视图]** 按钮。

营销活动 **[!UICONTROL 实时报告]** 页面将显示以下选项卡：

* [Campaign](#campaign-live)
* [电子邮件](#email-live)
* [应用程序内](#inapp-live)
* [推送](#push-live)
* [短信](#sms-live)
* [Web](#web-tab)
* [直邮](#direct-mail-tab)

营销活动 **[!UICONTROL 实时报告]** 将分为多个构件，每个构件详细描述营销活动的成功和错误。 如果需要，可以调整每个小部件的大小并将其删除。 有关详细信息，请参阅此 [部分](../reports/live-report.md#modify-dashboard).

有关Adobe Journey Optimizer中可用的每个量度的详细列表，请参阅 [此页面](live-report.md#list-of-components-live).

## “营销活动”选项卡 {#campaign-live}

### 交付 {#delivery-live}

此 **[!UICONTROL 营销活动统计数据]** 构件详细列出了与您的营销活动相关的主要信息：

* **[!UICONTROL 输入的配置文件]**：启动历程的用户档案数。

<!--
### Experimentation tab (#experimentation-live)

From your Campaign **[!UICONTROL Live report]**, the **[!UICONTROL Experimentation]** tab details the main information relative to how each variant is performing and if there is was winner during the test.
-->

## “电子邮件”选项卡 {#email-live}

>[!CONTEXTUALHELP]
>id="ajo_campaign_live_email_sending_statistics"
>title="电子邮件 - 发送统计数据"
>abstract="“电子邮件 - 发送统计数据”图表汇总有关电子邮件的基本数据，如过去 24 小时内定向邮件或已送达邮件。"

>[!CONTEXTUALHELP]
>id="ajo_campaign_live_email_statistics"
>title="电子邮件 - 统计数据"
>abstract="“电子邮件 - 统计数据”表提供有关过去 24 小时内电子邮件的配置文件活动的数据。"

>[!CONTEXTUALHELP]
>id="ajo_campaign_live_email_bounce_categories"
>title="电子邮件 - 退回类别"
>abstract="“电子邮件 - 退回类别”图表提供有关过去 24 小时内临时错误和永久性错误的数据。"

>[!CONTEXTUALHELP]
>id="ajo_campaign_live_email_performance_bydate"
>title="电子邮件 - 按日期列出的效果"
>abstract="“电子邮件 - 按日期列出的效果”图表显示过去 24 小时内有关已发送电子邮件的全面数据，提供针对送达和退回等关键量度的见解，从而可详细地分析电子邮件送达过程。"

>[!CONTEXTUALHELP]
>id="ajo_campaign_live_email_bounce_reasons"
>title="电子邮件 - 退回原因"
>abstract="“电子邮件 - 退回原因”图表包含与过去 24 小时内退回邮件相关的可用数据。"

>[!CONTEXTUALHELP]
>id="ajo_campaign_live_email_error_reasons"
>title="电子邮件 - 错误原因"
>abstract="通过“电子邮件 - 错误原因”图表，可了解过去 24 小时内在发送过程中发生的具体错误。"

>[!CONTEXTUALHELP]
>id="ajo_campaign_live_email_excluded_reasons"
>title="电子邮件 - 排除原因"
>abstract="“排除原因”图表说明过去 24 小时内导致从目标受众中排除用户配置文件，从而收不到消息的各种因素。"

>[!CONTEXTUALHELP]
>id="ajo_campaign_live_email_best_recipient"
>title="电子邮件 - 最佳收件人域"
>abstract="“电子邮件 - 最佳收件人域”图表详细地细分过去 24 小时内收件人最常用于打开电子邮件的域，并提供针对收件人行为的宝贵见解。"

来自您的营销活动 **[!UICONTROL 实时报告]**， **[!UICONTROL 电子邮件]** 选项卡详细列出了与您的营销活动中发送的电子邮件相关的主要信息。

![](assets/campaign_report_live_1.png)

+++了解有关电子邮件报表可用的不同量度和小组件的更多信息。

此 **[!UICONTROL 电子邮件发送统计数据]** 构件详述与报文相关的主要信息：

* **[!UICONTROL 已投放]**：成功发送的消息数。

* **[!UICONTROL 跳出次数]**：发送流程和自动返回处理期间累计的错误总数。

* **[!UICONTROL 错误]**：发送过程中发生的阻止将消息发送到用户档案的错误总数。

此 **[!UICONTROL 按电子邮件发送指标]** 表格和 **[!UICONTROL 电子邮件摘要]** 图表详细说明了您的电子邮件是否成功：

* **[!UICONTROL 已发送]**：发送总数。

* **[!UICONTROL 已投放]**：成功发送的消息数。

* **[!UICONTROL 跳出次数]**：发送流程和自动返回处理期间累计的错误总数。

* **[!UICONTROL 错误]**：发送过程中发生的阻止将消息发送到用户档案的错误总数。

* **[!UICONTROL 打开次数]**：消息的打开次数。

* **[!UICONTROL 点击次数]**：内容被单击的次数。

* **[!UICONTROL 取消订阅]**：取消订阅链接的点击次数。

* **[!UICONTROL 垃圾邮件投诉数]**：将消息声明为垃圾邮件或垃圾邮件的次数。

此 **[!UICONTROL 退回原因]** 和 **[!UICONTROL 退回类别]** 小组件包含与退回邮件相关的可用数据，例如：

* **[!UICONTROL 硬退回]**：永久错误的总数，如错误的电子邮件地址。 这涉及显式声明地址无效的错误消息，例如“未知用户”。

* **[!UICONTROL 软退回]**：临时错误的总数，如收件箱已满。

* **[!UICONTROL 已忽略]**：临时总数，例如外出或技术错误，例如，如果发件人类型是邮递员。

此 **[!UICONTROL 错误原因]** 和 **[!UICONTROL 排除原因]** 利用图形和表格，可查看在发送过程中发生了哪些错误和排除。

此 **[!UICONTROL 电子邮件 — 最佳收件人域]** 图表和表详细说明了收件人最常用于打开电子邮件的域。
+++

## “应用程序内”选项卡 {#inapp-live}

>[!CONTEXTUALHELP]
>id="ajo_campaign_live_inapp_performance"
>title="应用程序内性能"
>abstract="“应用程序内性能”KPI 提供有关过去 24 小时内访客与应用程序内消息的互动的基本见解。"

>[!CONTEXTUALHELP]
>id="ajo_campaign_live_inapp_interactions"
>title="按类型列出的交互"
>abstract="“按类型列出的交互”图表通过跟踪过去 24 小时内的任何点击、取消或交互而详述用户如何通过与应用程序内消息交互。"

>[!CONTEXTUALHELP]
>id="ajo_campaign_live_inapp_summary"
>title="应用程序内摘要"
>abstract="“应用程序内摘要”图表显示过去 24 小时内应用程序内展示和交互的进展。"

来自您的营销活动 **[!UICONTROL 实时报告]**， **[!UICONTROL 应用程序内]** 选项卡详细列出了与您的促销活动中发送的应用程序内消息相关的主要信息。

+++了解有关可用于应用程序内报表的不同量度和小组件的更多信息。

此 **[!UICONTROL 应用程序内性能]** KPI可详细列出与访客与应用程序内消息互动相关的主要信息，例如：

* **[!UICONTROL 展示次数]**：发送给所有用户的应用程序内消息总数。

* **[!UICONTROL 交互]**：应用程序内消息的参与总数。 这包括用户执行的任何操作，例如单击、解除或任何其他交互。

此 **[!UICONTROL 应用程序内摘要]** 图形可显示应用程序内展示次数和交互在相关时间段的演变。

此 **[!UICONTROL 按类型列出的交互]** 图表和表详细介绍了用户如何通过跟踪任何点击、解除或交互来与您的应用程序内消息进行交互。

+++

## “推送通知”选项卡 {#push-live}

>[!CONTEXTUALHELP]
>id="ajo_campaign_live_push_sending_performance"
>title="推送通知 - 发送性能"
>abstract="“推送通知发送性能”图表总结了有关推送通知的基本数据，例如过去 24 小时内的错误或已送达消息。"

>[!CONTEXTUALHELP]
>id="ajo_campaign_live_push_statistics"
>title="推送通知 - 统计数据"
>abstract="“推送统计数据”表提供有关过去 24 小时内推送通知的收件人活动的数据。"

>[!CONTEXTUALHELP]
>id="ajo_campaign_live_push_sending_summary"
>title="推送通知 - 发送摘要"
>abstract="“推送通知发送摘要”图表显示过去 24 小时内发送的推送通知的可用数据。"

>[!CONTEXTUALHELP]
>id="ajo_campaign_live_push_excluded_reasons"
>title="推送通知 - 排除原因"
>abstract="“排除原因”图表说明过去 24 小时内导致从目标受众中排除用户配置文件，从而收不到消息的各种因素。"

>[!CONTEXTUALHELP]
>id="ajo_campaign_live_push_error_reasons"
>title="推送通知 - 错误原因"
>abstract="通过“错误原因”图表，可了解过去 24 小时内在发送过程中发生的具体错误。"

>[!CONTEXTUALHELP]
>id="ajo_campaign_live_push_breakdown_platform"
>title="推送通知 - 按平台细分"
>abstract="“按平台细分”图表根据收件人的操作系统提供细分过去 24 小时内推送通知的成功情况。"

来自您的营销活动 **[!UICONTROL 实时报告]**， **[!UICONTROL 推送通知]** 选项卡详细说明与您的营销活动中发送的推送通知相关的主要信息。

![](assets/campaign_report_live_2.png)

+++了解有关可用于推送报表的不同量度和小组件的更多信息。

**[!UICONTROL 推送通知发送性能]**， **[!UICONTROL 推送通知摘要]** 和 **[!UICONTROL 推送通知 — 统计数据]** 构件详细列出与报文相关的主要信息：

* **[!UICONTROL 已发送]**：发送总数。

* **[!UICONTROL 已投放]**：成功发送的消息数。

* **[!UICONTROL 跳出次数]**：发送流程和自动返回处理期间累计的错误总数。

* **[!UICONTROL 错误]**：发送过程中发生的阻止将消息发送到用户档案的错误总数。

* **[!UICONTROL 打开次数]**：消息的打开次数。

* **[!UICONTROL 操作]**：对已投放推送通知执行的总操作数，例如按钮点击或解除。

* **[!UICONTROL 参与]**：此推送通知的打开和操作总数，即如果用户档案打开了推送或单击了按钮。

此 **[!UICONTROL 错误原因]** 和 **[!UICONTROL 排除原因]** 利用图形和表格，可查看在发送过程中发生的错误和排除情况。

此 **[!UICONTROL 发送统计数据 — 失败]** 利用小组件，可查看发生了多少错误和退回。

此 **[!UICONTROL 按平台跟踪]**， **[!UICONTROL 按平台发送]** 和 **[!UICONTROL 按平台细分]** 图表和表格根据操作系统详细说明了推送通知的成功情况。
+++

## “短信”选项卡 {#sms-live}

>[!CONTEXTUALHELP]
>id="ajo_campaign_live_sms_statistics"
>title="短信 - 统计数据"
>abstract="“短信发送统计数据”表汇总有关短信的基本数据，如过去 24 小时内定向消息或已送达消息。"

>[!CONTEXTUALHELP]
>id="ajo_campaign_live_sms_performance"
>title="短信 - 按日期显示效果"
>abstract="“短信 - 按日期显示效果”构件以图形表示形式提供有关过去 24 小时内消息的关键信息。"

>[!CONTEXTUALHELP]
>id="ajo_campaign_live_sms_error_reasons"
>title="短信 - 错误原因"
>abstract="通过“短信 - 错误原因”图表，可了解过去 24 小时内在发送过程中发生的具体错误。"

>[!CONTEXTUALHELP]
>id="ajo_campaign_live_sms_excluded_reasons"
>title="短信 - 排除原因"
>abstract="“排除原因”图表说明过去 24 小时内导致从目标受众中排除用户配置文件，从而收不到消息的各种因素。"

>[!CONTEXTUALHELP]
>id="ajo_campaign_live_sms_bounces_reasons"
>title="短信 - 退回原因"
>abstract="“退回原因”图表包含与过去 24 小时内与退回消息相关的可用数据。"

来自您的营销活动 **[!UICONTROL 实时报告]**， **[!UICONTROL 短信]** 选项卡详细说明与您的营销活动中发送的短信消息相关的主要信息。

![](assets/campaign_report_live_3.png)

+++了解有关短信报告可用的不同量度和小组件的更多信息。

此 **[!UICONTROL 短信 — 统计数据]** 该表详细列出了短信消息的成功情况：

* **[!UICONTROL 已定位]**：符合目标配置文件资格的用户配置文件数。

* **[!UICONTROL 已排除]**：从定向用户档案中排除且未收到消息的用户用户档案数。

* **[!UICONTROL 已发送]**：发送总数。

* **[!UICONTROL 跳出次数]**：发送流程和自动返回处理期间累计的错误总数。

* **[!UICONTROL 错误]**：发送过程中发生的阻止将消息发送到用户档案的错误总数。

* **[!UICONTROL 点击次数]**：URL访问总数。

此 **[!UICONTROL 按日期划分的短信性能]** 构件以图表形式详细描述与消息相关的主要信息：

* **[!UICONTROL 已发送]**：发送总数。

* **[!UICONTROL 跳出次数]**：发送流程和自动返回处理期间累计的错误总数。

* **[!UICONTROL 错误]**：发送过程中发生的阻止将消息发送到用户档案的错误总数。

此 **[!UICONTROL 排除原因]**， **[!UICONTROL 退回原因]** 和 **[!UICONTROL 错误原因]** 利用图形和表格，可查看在发送过程中发生的错误和排除情况。
+++

## Web选项卡 {#web-tab}

>[!CONTEXTUALHELP]
>id="ajo_campaign_live_web_performance"
>title="Web 性能"
>abstract="“Web 性能”KPI 提供有关过去 24 小时内访客与 Web 体验的互动的全面信息。"

>[!CONTEXTUALHELP]
>id="ajo_campaign_live_web_summary"
>title="Web 摘要"
>abstract="“Web 摘要”图表展示过去 24 小时内 Web 体验的进展情况，包括展示次数、独特展示次数和交互次数。"

>[!CONTEXTUALHELP]
>id="ajo_campaign_live_web_interactions"
>title="按元素列出的交互"
>abstract="“按元素列出的交互”表提供有关过去 24 小时内访客与网页上不同元素进行互动的关键信息。"

来自您的营销活动 **[!UICONTROL 实时报告]**， **[!UICONTROL Web]** 选项卡详细列出了与您的网页相关的主要信息。

+++了解更多可用于Web报表的不同量度和小组件。

此 **[!UICONTROL Web性能]** KPI可详细列出与访客对Web体验的参与度相关的主要信息，例如：

* **[!UICONTROL 展示次数]**：交付给所有用户的Web体验总数。

* **[!UICONTROL 交互]**：与网页的互动总数。 这包括用户执行的任何操作，例如点击或任何其他交互。

此 **[!UICONTROL Web摘要]** 图形可显示过去24小时内您的Web体验（展示次数、独特展示次数和交互）的演变。

此 **[!UICONTROL 按元素显示的交互]** 该表详细列出了与访客对网页上各种元素的参与度相关的主要信息。
+++

## 直邮选项卡 {#direct-mail-tab}

>[!CONTEXTUALHELP]
>id="ajo_campaign_live_direct_sending_statistics"
>title="直邮 - 发送统计数据"
>abstract="“直邮发送统计数据”表汇总过去 24 小时内有关直邮的基本数据，如定向邮件或已送达邮件。"

>[!CONTEXTUALHELP]
>id="ajo_campaign_live_direct_error_reasons"
>title="直邮 - 错误原因"
>abstract="通过“直邮 - 错误原因”图表，可了解过去 24 小时内发生的具体错误。"

>[!CONTEXTUALHELP]
>id="ajo_campaign_live_direct_excluded_reasons"
>title="直邮 - 排除原因"
>abstract="“直邮排除原因”图表说明导致过去 24 小时内从目标受众中排除用户配置文件，从而收不到消息的各种因素。"

来自您的营销活动 **[!UICONTROL 实时报告]**， **[!UICONTROL 直邮]** 选项卡详细列出了与直邮相关的主要信息。

![](assets/direct-mail-report_2.png)

+++了解有关直邮报表可用的不同量度和小组件的更多信息。

此 **[!UICONTROL 直邮 — 发送统计数据]** 该表详细列出了直邮的成功情况：

* **[!UICONTROL 已定位]**：符合目标配置文件资格的用户配置文件数。

* **[!UICONTROL 已发送]**：发送总数。

* **[!UICONTROL 错误]**：发送过程中发生的阻止将消息发送到用户档案的错误总数。

* **[!UICONTROL 已排除]**：从定向用户档案中排除、未收到直邮的用户用户档案数。

此 **[!UICONTROL 直邮 — 排除的原因]** 和 **[!UICONTROL 直邮 — 错误原因]** 利用图形和表格，可查看在发送过程中发生了哪些错误和排除。
+++

## 其他资源

* [营销活动入门](../campaigns/get-started-with-campaigns.md)
* [创建营销活动](../campaigns/create-campaign.md)
* [创建API触发的营销活动](../campaigns/api-triggered-campaigns.md)
* [修改或停止营销活动](../campaigns/modify-stop-campaign.md)
* [营销活动全局报告](campaign-global-report.md)
