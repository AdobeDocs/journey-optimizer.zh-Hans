---
solution: Journey Optimizer
product: journey optimizer
title: 营销活动实时报告
description: 了解如何使用Campaign实时报告中的数据
feature: Reporting
topic: Content Management
role: User
level: Intermediate
exl-id: 925494b6-e08a-4bd3-8a2f-96a5d9cbc387
source-git-commit: adcfff1cb8bb2ae98d41e4071f56a137e52ee56a
workflow-type: tm+mt
source-wordcount: '1859'
ht-degree: 4%

---

# 营销活动实时报告 {#campaign-live-report}

>[!CONTEXTUALHELP]
>id="ajo_campaign_live_report"
>title="营销活动实时报告"
>abstract="使用营销活动实时报告，您可以实时衡量和可视化营销活动的影响和绩效（仅限过去 24 小时）。报告分为不同的构件，详细说明您营销活动中的成功和错误。每个报告仪表板都可以修改，您可以调整构件大小或删除构件。"

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

来自您的营销活动 **[!UICONTROL 实时报告]**， **[!UICONTROL 电子邮件]** 选项卡详细列出了与您的营销活动中发送的电子邮件投放相关的主要信息。

![](assets/campaign_report_live_1.png)

+++了解有关电子邮件报表可用的不同量度和小组件的更多信息。

此 **[!UICONTROL 电子邮件发送统计数据]** 构件详述与报文相关的主要信息：

* **[!UICONTROL 已投放]**：成功发送的消息数。

* **[!UICONTROL 跳出次数]**：投放和自动返回处理期间累计的错误总数。

* **[!UICONTROL 错误]**：投放期间发生并阻止将其发送到用户档案的错误总数。

此 **[!UICONTROL 按电子邮件发送指标]** 表格和 **[!UICONTROL 电子邮件摘要]** 图表详细说明了您的交付是否成功：

* **[!UICONTROL 已发送]**：投放的发送总数。

* **[!UICONTROL 已投放]**：成功发送的消息数。

* **[!UICONTROL 跳出次数]**：投放和自动返回处理期间累计的错误总数。

* **[!UICONTROL 错误]**：投放期间发生并阻止将其发送到用户档案的错误总数。

* **[!UICONTROL 打开次数]**：投放中打开消息的次数。

* **[!UICONTROL 点击次数]**：在投放中单击内容的次数。

* **[!UICONTROL 取消订阅]**：取消订阅链接的点击次数。

* **[!UICONTROL 垃圾邮件投诉数]**：将消息声明为垃圾邮件或垃圾邮件的次数。

此 **[!UICONTROL 退回原因]**， **[!UICONTROL 退回类别]** 和 **[!UICONTROL 硬退回 — 按电子邮件]** 小组件包含与退回邮件相关的可用数据，例如：

* **[!UICONTROL 硬退回]**：永久错误的总数，如错误的电子邮件地址。 这涉及显式声明地址无效的错误消息，例如“未知用户”。

* **[!UICONTROL 软退回]**：临时错误的总数，如收件箱已满。

* **[!UICONTROL 已忽略]**：临时总数，例如外出或技术错误，例如，如果发件人类型是邮递员。

此 **[!UICONTROL 错误原因]** 和 **[!UICONTROL 排除原因]** 利用图形和表格，可查看在投放期间发生了哪些错误和排除项。

此 **[!UICONTROL 电子邮件 — 顶级收件人域]** 图表和表详细说明了收件人最常用于打开电子邮件的域。
+++

## “应用程序内”选项卡 {#inapp-live}

>[!CONTEXTUALHELP]
>id="ajo_campaign_live_inapp_performance"
>title="应用程序内性能"
>abstract="应用程序内性能KPI可提供有关访客在过去24小时内与应用程序内消息互动的重要信息。"

>[!CONTEXTUALHELP]
>id="ajo_campaign_live_inapp_interactions"
>title="按类型列出的交互"
>abstract="按类型划分的交互图表和表通过跟踪过去24小时内的任何点击、关闭或交互，详细介绍了用户如何与您的应用程序内消息进行交互。"

>[!CONTEXTUALHELP]
>id="ajo_campaign_live_inapp_summary"
>title="应用程序内摘要"
>abstract="应用程序内摘要图表说明了过去24小时内应用程序内展示和交互的进展情况。"

来自您的营销活动 **[!UICONTROL 实时报告]**， **[!UICONTROL 应用程序内]** 选项卡详细列出了与您的营销活动中发送的应用程序内投放相关的主要信息。

+++了解有关可用于应用程序内报表的不同量度和小组件的更多信息。

此 **[!UICONTROL 应用程序内性能]** KPI可详细列出与访客与应用程序内消息互动相关的主要信息，例如：

* **[!UICONTROL 展示次数]**：交付给所有用户的应用程序内消息总数。

* **[!UICONTROL 交互]**：应用程序内消息的参与总数。 这包括用户执行的任何操作，例如单击、解除或任何其他交互。

此 **[!UICONTROL 应用程序内摘要]** 图形可显示应用程序内展示次数和交互在相关时间段的演变。

此 **[!UICONTROL 按类型列出的交互]** 图表和表详细介绍了用户如何通过跟踪任何点击、解除或交互来与您的应用程序内消息进行交互。

+++

## “推送通知”选项卡 {#push-live}

>[!CONTEXTUALHELP]
>id="ajo_campaign_live_push_sending_performance"
>title="推送通知 — 发送性能"
>abstract="“推送通知发送性能”图概述了有关推送通知的基本数据，例如过去24小时内的错误或投放的消息。"

>[!CONTEXTUALHELP]
>id="ajo_campaign_live_push_statistics"
>title="推送通知 — 统计数据"
>abstract="“推送统计信息”表提供过去24小时内投放的收件人活动数据。"

>[!CONTEXTUALHELP]
>id="ajo_campaign_live_push_sending_summary"
>title="推送通知 — 发送摘要"
>abstract="推送通知发送摘要图形可显示过去24小时内已发送推送通知的可用数据。"

>[!CONTEXTUALHELP]
>id="ajo_campaign_live_push_excluded_reasons"
>title="推送通知 — 排除的原因"
>abstract="排除的原因图表和表说明了导致用户配置文件从目标受众中排除并在过去24小时内不接收消息的各种因素。"

>[!CONTEXTUALHELP]
>id="ajo_campaign_live_push_error_reasons"
>title="推送通知 — 错误原因"
>abstract="通过“错误原因”图形和表格，您可以识别在投放期间过去24小时内发生的特定错误。"

>[!CONTEXTUALHELP]
>id="ajo_campaign_live_push_breakdown_platform"
>title="推送通知 — 按平台细分"
>abstract="“按平台细分”图形和表格根据收件人的操作系统提供了过去24小时内推送通知成功情况的细分。"

来自您的营销活动 **[!UICONTROL 实时报告]**， **[!UICONTROL 推送通知]** 选项卡详细列出了与您的营销活动中发送的推送投放相关的主要信息。

![](assets/campaign_report_live_2.png)

+++了解有关可用于推送报表的不同量度和小组件的更多信息。

**[!UICONTROL 推送通知发送性能]**， **[!UICONTROL 推送通知摘要]** 和 **[!UICONTROL 推送通知 — 统计数据]** 构件详细列出与报文相关的主要信息：

* **[!UICONTROL 已发送]**：投放的发送总数。

* **[!UICONTROL 已投放]**：成功发送的消息数。

* **[!UICONTROL 跳出次数]**：投放和自动返回处理期间累计的错误总数。

* **[!UICONTROL 错误]**：投放期间发生并阻止将其发送到用户档案的错误总数。

* **[!UICONTROL 打开次数]**：投放中打开消息的次数。

* **[!UICONTROL 操作]**：对已投放推送通知执行的总操作数，例如按钮点击或解除。

* **[!UICONTROL 参与]**：此推送通知的打开和操作总数，即如果用户档案打开了推送或单击了按钮。

此 **[!UICONTROL 错误原因]** 和 **[!UICONTROL 排除原因]** 利用图形和表格，可查看在投放期间发生了哪些错误和排除项。

此 **[!UICONTROL 发送统计数据 — 失败]** 利用小组件，可查看发生了多少错误和退回。

此 **[!UICONTROL 按平台跟踪]**， **[!UICONTROL 按平台发送]** 和 **[!UICONTROL 按平台细分]** 图表和表格根据操作系统详细说明了推送通知的成功情况。
+++

## “短信”选项卡 {#sms-live}

>[!CONTEXTUALHELP]
>id="ajo_campaign_live_sms_statistics"
>title="短信 — 统计数据"
>abstract="SMS发送统计信息表汇总了有关SMS消息的基本数据，例如过去24小时内的定向或投放消息。"

>[!CONTEXTUALHELP]
>id="ajo_campaign_live_sms_performance"
>title="短信 — 按日期列出的性能"
>abstract="按日期划分的短信表现构件以图形呈现方式提供过去24小时内有关您消息的关键信息。"

>[!CONTEXTUALHELP]
>id="ajo_campaign_live_sms_error_reasons"
>title="短信 — 错误原因"
>abstract="短信 — 错误原因图表和表允许您识别投放过程中过去24小时内发生的特定错误。"

>[!CONTEXTUALHELP]
>id="ajo_campaign_live_sms_excluded_reasons"
>title="短信 — 排除的原因"
>abstract="排除的原因图表和表说明了导致用户配置文件从目标受众中排除并在过去24小时内不接收消息的各种因素。"

>[!CONTEXTUALHELP]
>id="ajo_campaign_live_sms_bounces_reasons"
>title="短信 — 退回原因"
>abstract="“退回原因”图表和表包含过去24小时内与退回消息相关的可用数据。"

来自您的营销活动 **[!UICONTROL 实时报告]**， **[!UICONTROL 短信]** 选项卡详细列出了与您的营销活动中发送的短信投放相关的主要信息。

![](assets/campaign_report_live_3.png)

+++了解有关短信报告可用的不同量度和小组件的更多信息。

此 **[!UICONTROL 短信 — 统计数据]** 该表详细说明了您的交付是否成功：

* **[!UICONTROL 已定位]**：有资格作为此投放的目标用户档案的用户档案数。

* **[!UICONTROL 已排除]**：从定向用户档案中排除且未收到消息的用户用户档案数。

* **[!UICONTROL 已发送]**：投放的发送总数。

* **[!UICONTROL 跳出次数]**：投放和自动返回处理期间累计的错误总数。

* **[!UICONTROL 错误]**：投放期间发生并阻止将其发送到用户档案的错误总数。

* **[!UICONTROL 点击次数]**：URL访问总数。

此 **[!UICONTROL 按日期划分的短信性能]** 构件以图表形式详细描述与消息相关的主要信息：

* **[!UICONTROL 已发送]**：投放的发送总数。

* **[!UICONTROL 跳出次数]**：投放和自动返回处理期间累计的错误总数。

* **[!UICONTROL 错误]**：投放期间发生并阻止将其发送到用户档案的错误总数。

此 **[!UICONTROL 排除原因]**， **[!UICONTROL 退回原因]** 和 **[!UICONTROL 错误原因]** 利用图形和表格，可查看在投放期间发生了哪些错误和排除项。
+++

## Web选项卡 {#web-tab}

>[!CONTEXTUALHELP]
>id="ajo_campaign_live_web_performance"
>title="Web性能"
>abstract="Web性能KPI提供关于访客过去24小时内与您的Web体验的互动情况的全面信息。"

>[!CONTEXTUALHELP]
>id="ajo_campaign_live_web_summary"
>title="Web摘要"
>abstract="Web摘要图形说明了您的Web体验从过去24小时的进展情况，包括展示次数、独特展示次数和交互。"

>[!CONTEXTUALHELP]
>id="ajo_campaign_live_web_interactions"
>title="按元素显示的交互"
>abstract="“按元素列出的交互”表提供了有关访客在过去24小时内与网页上不同元素的参与度的关键信息。"

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
>title="直邮 — 发送统计数据"
>abstract="“直邮发送统计数据”表汇总了过去24小时内有关直邮消息的基本数据，例如“目标”消息或“已投放”消息。"

>[!CONTEXTUALHELP]
>id="ajo_campaign_live_direct_error_reasons"
>title="直邮 — 错误原因"
>abstract="直邮 — 错误原因图表和表允许您识别过去24小时内发生的特定错误。"

>[!CONTEXTUALHELP]
>id="ajo_campaign_live_direct_excluded_reasons"
>title="直邮 — 排除的原因"
>abstract="直邮排除的原因图表和表说明了导致用户档案从目标受众中排除以及最近24小时内未接收消息的各种因素。"

来自您的营销活动 **[!UICONTROL 实时报告]**， **[!UICONTROL 直邮]** 选项卡详细列出了与直邮投放相关的主要信息。

![](assets/direct-mail-report_2.png)

+++了解有关直邮报表可用的不同量度和小组件的更多信息。

此 **[!UICONTROL 直邮 — 发送统计数据]** 该表详细说明了您的交付是否成功：

* **[!UICONTROL 已定位]**：有资格作为此投放的目标用户档案的用户档案数。

* **[!UICONTROL 已发送]**：投放的发送总数。

* **[!UICONTROL 错误]**：投放期间发生并阻止将其发送到用户档案的错误总数。

* **[!UICONTROL 已排除]**：从定向用户档案中排除且未收到投放的用户用户档案数。

此 **[!UICONTROL 直邮 — 排除的原因]** 和 **[!UICONTROL 直邮 — 错误原因]** 利用图形和表格，可查看在投放期间发生了哪些错误和排除项。
+++

## 其他资源

* [营销活动入门](../campaigns/get-started-with-campaigns.md)
* [创建营销活动](../campaigns/create-campaign.md)
* [创建API触发的营销活动](../campaigns/api-triggered-campaigns.md)
* [修改或停止营销活动](../campaigns/modify-stop-campaign.md)
* [营销活动全局报告](campaign-global-report.md)
