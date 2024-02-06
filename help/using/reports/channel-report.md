---
solution: Journey Optimizer
product: journey optimizer
title: 渠道级别报表
description: 了解如何使用渠道报表中的数据
feature: Reporting
topic: Content Management
role: User
level: Intermediate
exl-id: ead9359b-cdab-43ed-a469-d98b0ca19a17
source-git-commit: 5671f510d8be80b53d57b1ff90a101e500773243
workflow-type: tm+mt
source-wordcount: '3683'
ht-degree: 27%

---

# 渠道报告 {#channel-report}

>[!CONTEXTUALHELP]
>id="ajo_channel_level_report"
>title="渠道级报告"
>abstract="渠道报告全面概述所有渠道上的流量和参与量度。报告分为不同的构件，详细说明营销活动和历程的成功和错误。可通过调整构件大小或删除构件而修改每个报告仪表板。"

>[!IMPORTANT]
>
> 要访问 **报表** 菜单，您必须拥有 **[!UICONTROL 查看渠道报表]** 许可。 [了解详情](channel-report-gs.md#before-starting-manage-reports-prereq)

渠道报表可在渠道级别为用户提供流量和参与量度的全面概述。 这些量度将进行聚合，以显示来自所选渠道（跨各种促销活动和历程）的操作的合并值。

您可以通过导航到 **报表** 中的菜单 **历程管理** 部分。 它是完全可自定义的，您可以根据报表日期或操作筛选数据。 [了解详情](channel-report-gs.md)

此时将显示报告页面，其中包含以下选项卡：

* [电子邮件](#email)
* [推送通知](#push)
* [短信](#sms)
* [应用程序内](#inapp)
* [Web](#web)
* [直邮](#direct-mail)

➡️ [在视频中发现此功能](#channel-report-video)

## 电子邮件 {#email}

在渠道报表中，电子邮件菜单详细说明与促销活动和历程中发送的电子邮件相关的主要信息。 指标详见下文。

### 电子邮件 - 发送总数统计数据 {#email-total-sending}

>[!CONTEXTUALHELP]
>id="ajo_channel_email_sending_statistics"
>title="电子邮件 - 发送总数统计数据"
>abstract="“电子邮件 - 发送总数统计数据”KPI 汇总有关您的电子邮件的基本数据，如定向邮件或送达的邮件。"

![](assets/channel_email_total_sending.png)

此 **[!UICONTROL 电子邮件总发送统计数据]** 小组件提供了电子邮件性能的全面概述，其中显示关键性能指标(KPI)，概述了有关电子邮件的基本数据。

+++ 了解有关电子邮件发送总计统计量度的更多信息

* **[!UICONTROL 已定位]**：已处理的电子邮件总数。

* **[!UICONTROL 已发送]**：发送总数。

* **[!UICONTROL 已投放]**：成功发送的电子邮件数，与已发送消息的总数相关。

* **[!UICONTROL 投放率]**：成功发送的电子邮件百分比。

* **[!UICONTROL 跳出次数]**：与已发送消息总数相关的累积和自动返回处理的错误总数。

* **[!UICONTROL 跳出率]**：退回的电子邮件与发送的电子邮件相比的百分比。

* **[!UICONTROL 错误]**：阻止将其发送到用户档案的错误总数。

* **[!UICONTROL 错误率]**：与已发送的电子邮件相比，阻止发送该邮件发生的错误百分比。

* **[!UICONTROL 已排除]**：Adobe Journey Optimizer已排除的用户档案数。

* **[!UICONTROL 排除率]**：Adobe Journey Optimizer已排除的用户档案的百分比。

+++

### 电子邮件 - 跟踪总数统计数据 {#email-total-tracking}

>[!CONTEXTUALHELP]
>id="ajo_channel_email_tracking_statistics"
>title="电子邮件 - 跟踪总数统计数据"
>abstract="“电子邮件 - 跟踪总数统计数据”KPI 提供有关电子邮件的配置文件活动的数据。"

![](assets/channel_email_total_tracking.png)

此 **[!UICONTROL 电子邮件跟踪总数统计信息]** 小组件提供了与电子邮件绑定的用户档案活动的详细快照，提供了有关参与和电子邮件效率的重要见解。

+++ 了解关于电子邮件总计跟踪统计量度的更多信息

* **[!UICONTROL 打开次数]**：消息的打开次数。

* **[!UICONTROL 打开率]**：打开的电子邮件总数，与已投放的电子邮件数相比。

* **[!UICONTROL 点击次数]**：在消息中单击内容的次数。

* **[!UICONTROL 点击率]**：与电子邮件交互的用户百分比。

* **[!UICONTROL 垃圾邮件投诉数]**：将消息声明为垃圾邮件或垃圾邮件的次数。

* **[!UICONTROL 垃圾邮件投诉率]**：与已发送电子邮件数量相比，声明为垃圾邮件或垃圾邮件的百分比。

* **[!UICONTROL 取消订阅]**：订阅链接的点击次数。

* **[!UICONTROL 取消订阅率]**：与已发送电子邮件数量相比的退订百分比。

+++

### 电子邮件 - 一段时间内的发送统计数据 {#email-sending-statistics-overtime}

>[!CONTEXTUALHELP]
>id="ajo_channel_email_sending_statistics_overtime"
>title="电子邮件 - 一段时间内的发送统计数据"
>abstract="“电子邮件 - 一段时间内的发送统计数据”图表显示有关已发送电子邮件的数据，该数据按每小时、每天、每周或每月进行了细分。"

![](assets/channel_email_sending_statistics.png)

此 **[!UICONTROL 电子邮件 — 随时间变化的发送统计数据]** 图形提供动态表示形式，显示电子邮件活动的分析。 此图形表示提供已发送电子邮件的全面分类，允许您以每小时、每天、每周或每月为单位观察趋势和模式。

+++ 了解有关电子邮件 — 发送随时间变化的统计信息的更多信息

* **[!UICONTROL 已发送]**：发送总数。

* **[!UICONTROL 已投放]**：成功发送的电子邮件数，与已发送电子邮件总数相关。

* **[!UICONTROL 跳出次数]**：与已发送电子邮件总数相关的累积和自动返回处理的错误总数。

* **[!UICONTROL 错误]**：阻止将其发送到用户档案的错误总数。

+++

### 电子邮件 - 一段时间内的跟踪统计数据 {#email-tracking-statistics-overtime}

>[!CONTEXTUALHELP]
>id="ajo_channel_email_tracking_statistics_overtime"
>title="电子邮件 - 一段时间内的跟踪统计数据"
>abstract="“电子邮件 - 一段时间内的跟踪统计数据”图表提供有关您的电子邮件的配置文件活动的数据，该数据按每小时、每天、每周或每月进行了细分。"

![](assets/channel_email_tracking_overtime.png)

此 **[!UICONTROL 电子邮件 — 随时间变化的跟踪统计数据]** graph提供与您的电子邮件相关的用户档案活动的详细概述。 此图形表示法以每小时、每天、每周或每月为单位细分数据，从而提供收件人参与度在不同时间间隔内演变情况的宝贵见解。

+++ 详细了解电子邮件 — 随时间变化的跟踪统计数据

* **[!UICONTROL 打开次数]**：消息的打开次数。

* **[!UICONTROL 点击次数]**：在消息中单击内容的次数。

+++

### 电子邮件 - 退回类别和原因 {#bounce-categories}

>[!CONTEXTUALHELP]
>id="ajo_channel_email_bounce_categories"
>title="退回类别"
>abstract="“退回类别”图表提供有关临时错误和永久性错误的数据。"

>[!CONTEXTUALHELP]
>id="ajo_channel_email_bounce_reasons"
>title="退回原因"
>abstract="“退回原因”图表包含与退回邮件相关的可用数据。"

![](assets/channel_email_bounce_categories.png)

此 **[!UICONTROL 退回类别]** 和 **[!UICONTROL 退回原因]** 小组件封装与退回报文相关的数据，全面概述报文退回的各种类别和具体原因

有关退回的详细信息，请参阅 [禁止显示列表](../reports/suppression-list.md) 页面。

+++ 了解有关退回类别量度的更多信息

* **[!UICONTROL 硬退回]**：永久错误的总数，如错误的电子邮件地址。 这涉及显式声明地址无效的错误消息，例如“未知用户”。

* **[!UICONTROL 软退回]**：临时错误的总数，如收件箱已满。

* **[!UICONTROL 已忽略]**：临时总数，例如外出或技术错误，例如，如果发件人类型是邮递员。

+++

### 错误原因 {#error-reasons}

>[!CONTEXTUALHELP]
>id="ajo_channel_email_error_reasons"
>title="错误原因"
>abstract="通过“错误原因”图表，可了解在发送过程中发生的具体错误。"

![](assets/channel_email_error.png)

此 **[!UICONTROL 错误原因]** 利用图表和表格，您可以查明整个发送过程中发生的准确错误，从而帮助客户清楚地了解遇到的任何问题。

### 排除的原因 {#excluded-reasons}

>[!CONTEXTUALHELP]
>id="ajo_channel_email_excluded_reasons"
>title="排除的原因"
>abstract="“排除的原因”图表说明导致从目标受众中排除用户配置文件，从而收不到消息的各种因素。"

![](assets/channel_email_excluded.png)

此 **[!UICONTROL 排除的原因]** 图表和表格全面介绍了导致从目标受众中排除用户配置文件，从而导致未收到消息的不同因素。

请参阅 [此页面](exclusion-list.md) 以获取排除原因的完整列表。

### 按域列出的已发送和已送达邮件 {#sent-delivered-domains}

>[!CONTEXTUALHELP]
>id="ajo_channel_email_sending_delivered_domains"
>title="按域列出的已发送和已送达邮件"
>abstract="“按域列出的已发送和已送达邮件”图表表示所有重要电子邮件发送数据的域级细分。"

![](assets/channel_email_sent_domains.png)

此 **[!UICONTROL 按域发送和投放]** 表格和图形提供了域级别电子邮件投放的详细细分，提供了对电子邮件性能的全面洞察。

+++ 了解有关“按域发送和交付”指标的更多信息

* **[!UICONTROL 已发送]**：电子邮件的发送总数。

* **[!UICONTROL 已投放]**：成功发送的消息数，与已发送消息的总数相关。

+++

### 按域列出的退回和错误 {#bounces-errors-domains}

>[!CONTEXTUALHELP]
>id="ajo_channel_email_bounces_errors_domains"
>title="按域列出的退回和错误"
>abstract="“按域列出的退回和错误”图表按域细分地呈现在发送过程中发生的具体错误。"

![](assets/channel_email_bounces_domain.png)

此 **[!UICONTROL 按域列出的退回和错误]** 图表和表格提供了发送过程中遇到的特定错误的域级细分，提供了对所发生问题的详细分析。

+++ 详细了解按域列出的退回和错误量度

* **[!UICONTROL 跳出次数]**：在发送流程和自动返回处理期间累计的错误总数与已发送消息总数相关。

* **[!UICONTROL 错误]**：发送过程中发生的阻止将消息发送到用户档案的错误总数。

+++

### 按域列出的打开和点击数 {#open-clicks-domains}

>[!CONTEXTUALHELP]
>id="ajo_channel_email_open_clicks_domains"
>title="按域列出的打开和点击数"
>abstract="“按域列出的打开和点击数”图表按域细分地呈现访客与电子邮件的互动。"

![](assets/channel_email_open_domains.png)

此 **[!UICONTROL 按域打开和点击]** 图表显示了访客与您的电子邮件互动的域级细分，提供了有关不同域与您的内容如何互动的宝贵见解。

+++ 了解有关“按域列出的打开和点击次数”量度的更多信息

* **[!UICONTROL 打开次数]**：电子邮件的打开次数。

* **[!UICONTROL 点击次数]**：在电子邮件中点击内容的次数。

+++

### 按域列出的退回原因 {#bounce-reasons-domains}

>[!CONTEXTUALHELP]
>id="ajo_channel_email_bounce_reasons_domains"
>title="按域列出的退回原因"
>abstract="“按域列出的退回原因”图表按域细分地呈现临时错误和永久性错误数据。"

![](assets/channel_email_bounce_domain.png)

此 **[!UICONTROL 按域列出的退回原因]** 图表提供了有关临时和永久错误的域级数据细分，提供了有关退回消息原因的详细见解。

有关退回的详细信息，请参阅 [禁止显示列表](../reports/suppression-list.md) 页面。

## 推送通知 {#push}

在渠道报表中， **推送通知** 菜单详细说明与您的促销活动和历程中发送的推送通知相关的主要信息。 指标详见下文。

### 推送通知 - 发送总数统计数据 {#push-total-sending}

>[!CONTEXTUALHELP]
>id="ajo_channel_push_sending_statistics"
>title="推送通知 - 发送总数统计数据"
>abstract="“推送通知 - 发送总数统计数据”KPI 汇总有关推送通知的基本数据，如定向消息或已送达消息。"

![](assets/channel_push_total_sending.png)

此 **[!UICONTROL 推送通知 — 发送统计信息总数]** KPI可充当一个全面的摘要，封装与推送通知相关的基本数据。 这些量度包括对目标受众和实际投放状态的详细见解，从而更全面地了解推送通知的有效性和影响范围。

+++ 了解有关推送通知 — 发送总统计信息量度的更多信息

* **[!UICONTROL 已定位]**：已处理的推送通知总数。

* **[!UICONTROL 已发送]**：已发送推送通知的总数。

* **[!UICONTROL 已投放]**：成功发送的推送通知数，与已发送推送通知的总数相关。

* **[!UICONTROL 投放率]**：已成功发送的推送通知的百分比。

* **[!UICONTROL 跳出次数]**：与已发送消息总数相关的累积和自动返回处理的错误总数。

* **[!UICONTROL 跳出率]**：退回的推送通知与已发送的推送通知相比的百分比。

* **[!UICONTROL 错误]**：阻止将其发送到用户档案的错误总数。

* **[!UICONTROL 错误率]**：与发送的推送通知相比，阻止发送该请求所发生的错误百分比。

* **[!UICONTROL 已排除]**：Adobe Journey Optimizer已排除的用户档案数。

* **[!UICONTROL 排除率]**：Adobe Journey Optimizer已排除的用户档案的百分比。

+++

### 推送通知 - 跟踪总数统计数据 {#push-total-tracking}

>[!CONTEXTUALHELP]
>id="ajo_channel_push_tracking_statistics"
>title="推送通知 - 跟踪总数统计数据"
>abstract="“推送通知 - 跟踪总数统计数据”提供有关推送通知的配置文件活动的数据。"

此 **[!UICONTROL 推送通知 — 跟踪统计信息总数]** 构件提供与推送通知绑定的用户档案活动的详细快照，提供关于参与和推送通知有效性的基本见解。

+++ 了解有关推送通知 — 总跟踪统计量度的更多信息

* **[!UICONTROL 打开次数]**：推送通知的打开次数。

* **[!UICONTROL 打开率]**：已打开推送通知的百分比。

* **[!UICONTROL 操作]**：对已投放推送通知执行的总操作数，例如按钮点击或解除。

* **[!UICONTROL 操作率]**：已投放推送通知上的操作相对于已发送推送通知的百分比。

+++

### 推送通知 - 一段时间内的发送统计数据 {#push-sending-overtime}

>[!CONTEXTUALHELP]
>id="ajo_channel_push_sending_statistics_overtime"
>title="推送通知 - 一段时间内的发送统计数据"
>abstract="“一段时间内的推送通知发送统计数据”图表显示有关已发送推送通知的数据，该数据按每小时、每天、每周或每月进行了细分。"

![](assets/channel_push_sending_statistics.png)

此 **[!UICONTROL 推送通知 — 发送一段时间内的统计数据]** 图形提供动态表示形式，显示推送通知活动的分析。 此图形呈现方式提供了已发送推送通知的全面细分，允许您以每小时、每天、每周或每月为单位观察趋势和模式。

+++ 了解有关推送通知 — 发送一段时间量度的统计信息的更多信息

* **[!UICONTROL 已发送]**：已发送推送通知的总数。

* **[!UICONTROL 已投放]**：成功发送的推送通知数，与已发送推送通知的总数相关。

* **[!UICONTROL 跳出次数]**：与已发送消息总数相关的累积和自动返回处理的错误总数。

* **[!UICONTROL 错误]**：阻止将其发送到用户档案的错误总数。

+++

### 推送通知 - 一段时间内的跟踪统计数据 {#push-tracking-overtime}

>[!CONTEXTUALHELP]
>id="ajo_channel_push_tracking_statistics_overtime"
>title="推送通知 - 一段时间内的跟踪统计数据"
>abstract="“推送通知 - 一段时间内的跟踪统计数据”图表提供有关推送通知的配置文件活动的数据，该数据按每小时、每天、每周或每月进行了细分。"

此 **[!UICONTROL 推送通知 — 随时间变化的跟踪统计数据]** graph提供与推送通知相关的用户档案活动的详细概述。 此图形表示法以每小时、每天、每周或每月为单位细分数据，从而提供收件人参与度在不同时间间隔内演变情况的宝贵见解。

+++ 了解有关推送通知的更多信息 — 跟踪一段时间量度的统计数据

* **[!UICONTROL 打开次数]**：推送通知的打开次数。

* **[!UICONTROL 操作]**：对已投放推送通知执行的总操作数，例如按钮点击或解除。

+++

### 推送通知 - 排除的原因 {#push-excluded-reasons}

>[!CONTEXTUALHELP]
>id="ajo_channel_push_excluded_reasons"
>title="排除的原因"
>abstract="“排除的原因”图表说明导致从目标受众中排除用户配置文件，从而收不到消息的各种因素。"

![](assets/channel_push_excluded.png)

此 **[!UICONTROL 排除的原因]** 图形和表格显示了阻止从定向用户档案中排除的用户用户档案接收推送通知的不同原因。

请参阅 [此页面](exclusion-list.md) 以获取排除原因的完整列表。

### 推送通知 - 错误原因 {#push-error-reasons}

>[!CONTEXTUALHELP]
>id="ajo_channel_push_error_reasons"
>title="错误原因"
>abstract="通过“错误原因”图表，可了解在发送过程中发生的具体错误。"

![](assets/channel_push_error.png)

此 **[!UICONTROL 错误原因]** 利用图形和表格，可识别在发送推送通知过程中发生的特定错误，并针对发送过程中遇到的任何问题提供详细分析。

### 推送通知 - 各平台的跟踪 {#push-tracking-platform}

>[!CONTEXTUALHELP]
>id="ajo_channel_push_tracking_statistics_platform"
>title="按平台列出的跟踪统计数据"
>abstract="“按平台列出的跟踪统计数据”图表根据配置文件的操作系统提供有关推送通知的配置文件活动的数据。"

此 **[!UICONTROL 推送通知 — 按平台跟踪]** 图表和表格根据用户档案的操作系统，详细说明了推送通知的收件人活动。

### 推送通知 - 各平台的发送 {#push-sending-platform}

>[!CONTEXTUALHELP]
>id="ajo_channel_push_sending_statistics_platform"
>title="按平台列出的发送统计数据"
>abstract="“按平台列出的发送统计数据”图表显示有关已发送的推送通知的数据。"

![](assets/channel_push_sending_platform.png)

此 **[!UICONTROL 推送通知 — 按平台发送]** 图表和表格可提供全面的细分，详细描述推送通知相对于用户档案操作系统的成功情况。 这种全面的分析对于不同平台上的推送通知的有效性提供了宝贵的见解。

## 短信 {#sms}

来自您的 **渠道** 在报表中，短信菜单详细说明与促销活动和历程中发送的短信相关的主要信息。 指标详见下文。

### 短信 - 发送总数统计数据 {#sms-sending-statistics}

>[!CONTEXTUALHELP]
>id="ajo_channel_sms_sending_statistics"
>title="短信 - 发送总数统计数据"
>abstract="“短信 - 发送总数统计数据”KPI 汇总有关短信的基本数据，如定向消息或已送达消息。"

![](assets/channel_sms_total_sending.png)

此 **[!UICONTROL 短信 — 发送统计信息总数]** KPI可作为一个全面的摘要，封装与短信相关的基本数据。 这些量度包括对目标受众和实际投放状态的详细见解，从而全面地了解短信消息的有效性和影响范围。

+++ 了解有关推送通知 — 发送总统计信息量度的更多信息

* **[!UICONTROL 已定位]**：符合短信渠道目标配置文件资格的用户配置文件数。

* **[!UICONTROL 已发送]**：已发送的短信消息总数。

* **[!UICONTROL 已投放]**：成功发送的短信消息数，与已发送的短信消息总数相关。

* **[!UICONTROL 投放率]**：成功发送的短信消息的百分比。

* **[!UICONTROL 跳出次数]**：相对于已发送的短信消息总数，已累计和自动返回处理的错误总数。

* **[!UICONTROL 跳出率]**：退回的短信消息与发送的短信消息相比的百分比。

* **[!UICONTROL 错误]**：阻止将其发送到用户档案的错误总数。

* **[!UICONTROL 错误率]**：与已发送的短信消息相比，阻止发送该消息的错误百分比。

* **[!UICONTROL 已排除]**：从定向用户档案中排除且未收到消息的用户用户档案数。

* **[!UICONTROL 排除率]**：Adobe Journey Optimizer已排除的用户档案的百分比。

+++

### 短信 - 跟踪总数统计数据 {#sms-tracking-statistics}

>[!CONTEXTUALHELP]
>id="ajo_channel_sms_tracking_statistics"
>title="短信 - 跟踪总数统计数据"
>abstract="“短信 - 跟踪总数统计数据”提供有关短信的配置文件活动的数据。"

![](assets/channel_sms_tracking.png)

此 **[!UICONTROL 短信 — 跟踪统计信息总数]** 构件详细概述了与访客与您的URL参与度相关的关键信息，提供了有关短信消息有效性洞察：

* **[!UICONTROL 点击次数]**：内容在短信消息中被点击的次数。

### 短信 - 一段时间内的发送统计数据 {#sms-sending-statistics-overtime}

>[!CONTEXTUALHELP]
>id="ajo_channel_sms_sending_statistics_overtime"
>title="短信 - 一段时间内的发送统计数据"
>abstract="“短信 - 一段时间内的发送统计数据”图表显示有关已发送短信的数据，该数据按每小时、每天、每周或每月进行了细分。"

![](assets/channel_sms_sending_overtime.png)

此 **[!UICONTROL 短信 — 随时间变化的发送统计数据]** 图表提供了已发送短信消息的全面视图，提供每小时、每天、每周或每月细分的数据。 此图形表示允许您跟踪和分析短信消息传送活动在不同时间间隔内的趋势。

+++ 详细了解短信 — 发送一段时间量度的统计数据

* **[!UICONTROL 已发送]**：已发送的短信消息总数。

* **[!UICONTROL 跳出次数]**：相对于已发送的短信消息总数，已累计和自动返回处理的错误总数。

* **[!UICONTROL 错误]**：阻止将其发送到用户档案的错误总数。

+++

### 短信 - 一段时间内的跟踪统计数据 {#sms-tracking-statistics-overtime}

>[!CONTEXTUALHELP]
>id="ajo_channel_sms_tracking_statistics_overtime"
>title="短信 - 一段时间内的跟踪统计数据"
>abstract="“短信 - 一段时间内的跟踪统计数据”图表提供有关短信的配置文件活动的数据，该数据按每小时、每天、每周或每月进行了细分。"

![](assets/channel_sms_tracking_overtime.png)

此 **[!UICONTROL 短信 — 随时间变化的跟踪统计数据]** graph提供与短信消息相关的用户档案活动数据，提供每小时、每天、每周或每月的详细细分。 此图形表示允许您分析和了解不同时间间隔内的用户参与模式。

* **[!UICONTROL 点击次数]**：内容在短信消息中被点击的次数。

### 排除的原因 {#sms-excluded-reasons}

>[!CONTEXTUALHELP]
>id="ajo_channel_sms_excluded_reasons"
>title="排除的原因"
>abstract="“排除的原因”图表说明导致从目标受众中排除用户配置文件，从而收不到消息的各种因素。"

![](assets/channel_sms_excluded.png)

此 **[!UICONTROL 排除原因]** 图表和表格直观地描述了导致从目标受众中排除用户配置文件，阻止他们接收短信消息的各种因素。

请参阅 [此页面](exclusion-list.md) 以获取排除原因的完整列表。

### 退回原因 {#sms-bounce-reasons}

>[!CONTEXTUALHELP]
>id="ajo_channel_sms_bounce_reasons"
>title="退回原因"
>abstract="“退回原因”图表包含与退回邮件相关的可用数据。"

![](assets/channel_sms_bounce_reasons.png)

此 **[!UICONTROL 退回原因]** 图形和表格提供了与短信退回消息相关的数据的全面概述，从而针对SMS消息退回实例背后的具体原因提供了宝贵的见解。

### 错误原因 {#sms-error-reasons}

>[!CONTEXTUALHELP]
>id="ajo_channel_sms_error_reasons"
>title="错误原因"
>abstract="通过“错误原因”图表，可了解在发送过程中发生的具体错误。"

此 **[!UICONTROL 错误原因]** 利用图表和表格，可识别在短信消息发送过程中发生的特定错误，从而便于彻底分析遇到的任何问题。

## 直邮 {#direct-mail}

来自您的 **渠道** 报表、 **直邮** 菜单详细说明与在中发送的直邮消息相关的主要信息 **营销活动** 和 **历程**. 量度详见下文。

### 直邮 - 发送总数统计数据 {#direct-mail-total-sending}

>[!CONTEXTUALHELP]
>id="ajo_channel_direct_sending_statistics"
>title="直邮 - 发送总数统计数据"
>abstract="“直邮 - 发送总数统计数据”KPI 汇总有关直邮的基本数据，如定向邮件或已送达邮件。"

![](assets/channel_direct_sending.png)

此 **[!UICONTROL 直邮 — 发送统计信息总数]** 构件可提供直邮消息性能的全面概述，显示概述有关直邮消息基本数据的关键性能指标(KPI)。

+++ 了解有关直邮 — 发送总统计信息量度的更多信息

* **[!UICONTROL 已定位]**：符合直邮消息目标用户档案资格的用户档案数。

* **[!UICONTROL 已发送]**：发送总数。

* **[!UICONTROL 错误]**：阻止将其发送到用户档案的错误总数。

* **[!UICONTROL 错误率]**：与发送的推送通知相比，阻止发送该请求所发生的错误百分比。

* **[!UICONTROL 已排除]**：从定向用户档案中排除且未收到消息的用户用户档案数。

* **[!UICONTROL 排除率]**：Adobe Journey Optimizer已排除的用户档案的百分比。

+++

### 排除的原因 {#direct-mail-excluded-reasons}

>[!CONTEXTUALHELP]
>id="ajo_channel_direct_excluded_reasons"
>title="排除的原因"
>abstract="“排除的原因”图表说明导致从目标受众中排除用户配置文件，从而收不到消息的各种因素。"

![](assets/channel_direct_excluded.png)

此 **[!UICONTROL 直邮 — 排除的原因]** 图表和表格直观地说明了导致从目标受众中排除用户配置文件，从而阻止他们接收直邮消息的各种因素。

请参阅 [此页面](exclusion-list.md) 以获取排除原因的完整列表。

### 错误原因 {#direct-mail-error-reasons}

>[!CONTEXTUALHELP]
>id="ajo_channel_direct_error_reasons"
>title="错误原因"
>abstract="通过“错误原因”图表，可了解在发送过程中发生的具体错误。"

![](assets/channel_direct_error.png)

此 **[!UICONTROL 直邮 — 错误原因]** 提供用于识别在直邮消息发送过程中发生的特定错误的方法，从而允许对遇到的任何问题进行详细分析。

## 应用程序内 {#in-app}

在渠道报表中，应用程序内菜单详细列出与促销活动和历程中发送的应用程序内消息相关的主要信息。 指标详见下文。

### 应用程序内总参与次数 {#inapp-total-engagement}

>[!CONTEXTUALHELP]
>id="ajo_channel_inapp_engagement"
>title="应用程序内 - 总参与次数"
>abstract="“应用程序内 - 总参与次数”KPI 提供有关访客与应用程序内消息的交互情况的全面信息，包括展示次数和交互次数等量度。"

![](assets/channel_inapp_engagement.png)

此 **[!UICONTROL 应用程序内总参与度]** KPI可提供关于访客与应用程序内消息互动情况的全面分析，其中包括关键量度，例如 **展示次数** 和 **交互**.

+++ 了解有关应用程序内总参与量度的更多信息

* **[!UICONTROL 展示次数]**：交付给所有用户的应用程序内消息总数。

* **[!UICONTROL 交互]**：应用程序内消息的参与总数。 这包括用户执行的任何操作，例如单击、解除或任何其他交互。

+++

### 一段时间内的应用程序内参与次数 {#inapp-engagement-overtime}

>[!CONTEXTUALHELP]
>id="ajo_channel_inapp_engagement_overtime"
>title="一段时间内的应用程序内参与次数"
>abstract="“一段时间内的应用程序内参与次数”图表跟踪应用程序内展示次数和交互次数，并提供每小时、每日、每周和每月细分。"

![](assets/channel_inapp_engagement_overtime.png)

此 **[!UICONTROL 应用程序内参与加班]** 图形通过跟踪任何展示、拒绝或交互，显示了在相关时间段内应用程序内展示和交互的演变。

+++ 了解有关应用程序内参与超时量度的更多信息

* **[!UICONTROL 展示次数]**：交付给所有用户的应用程序内消息总数。

* **[!UICONTROL 交互]**：应用程序内消息的参与总数。 这包括用户执行的任何操作，例如单击、解除或任何其他交互。

+++

## Web {#web}

来自您的 **渠道** 报告，Web菜单详细说明与包含在您的报告中的Web页面相关的主要信息。 **营销活动** 和 **历程**. 指标详见下文。

### Web - 总参与次数 {#web-engagement-total}

>[!CONTEXTUALHELP]
>id="ajo_channel_web_engagement"
>title="Web - 总参与次数"
>abstract="“Web - 总参与次数”KPI 提供有关访客与网页的交互情况的全面信息，包括展示次数和交互次数等量度。"

![](assets/channel_web_engagement.png)

此 **[!UICONTROL Web总体参与度]** KPI可全面分析访客与网页的互动情况，包括关键量度，如展示和互动。

+++ 了解有关Web总参与量度的更多信息

* **[!UICONTROL 展示次数]**：交付给所有用户的Web体验总数。

* **[!UICONTROL 交互]**：与网页的互动总数。 这包括用户执行的任何操作，例如点击或任何其他交互。

+++

### Web - 一段时间内的总参与次数 {#web-engagement-total-overtime}

>[!CONTEXTUALHELP]
>id="ajo_channel_web_engagement_overtime"
>title="Web - 一段时间内的总参与次数"
>abstract="“Web - 一段时间内的参与次数”图表跟踪您的网页展示次数和交互次数，并提供每小时、每天、每周和每月细分。"

![](assets/channel_web_engagement_overtime.png)

此 **[!UICONTROL Web参与加班]** 图形监控 **展示次数** 和 **交互** ，提供每小时、每日、每周和每月的详细细分。

+++ 了解有关Web参与超时量度的更多信息

* **[!UICONTROL 展示次数]**：交付给所有用户的Web体验总数。

* **[!UICONTROL 交互]**：与网页的互动总数。 这包括用户执行的任何操作，例如点击或任何其他交互。

+++

## 渠道报表（视频） {#channel-report-video}

请在此视频中了解如何在渠道级别访问、导航和导出报告

>[!VIDEO](https://video.tv.adobe.com/v/3424537?quality=12)
