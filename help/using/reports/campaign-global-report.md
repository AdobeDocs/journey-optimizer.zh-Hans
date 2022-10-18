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
source-git-commit: 63c52f04da9fd1a5fafc36ffb5079380229f885e
workflow-type: tm+mt
source-wordcount: '1660'
ht-degree: 1%

---

# 营销活动全局报告 {#campaign-global-report}

营销活动全局报告可直接通过 **[!UICONTROL 所有时间]** 按钮。

![](assets/campaign_report_global_5.png)

营销活动 **[!UICONTROL 全局报告]** 页面中将显示以下选项卡：

* [Campaign](#campaign-global)
* [电子邮件](#email-global)
* [推送](#push-global)
* [短信](#sms-global)

营销活动 **[!UICONTROL 全局报告]** 会被分为不同的小组件，用于详细说明营销活动的成功和错误。 如果需要，可以调整每个小组件的大小并将其删除。 有关此内容的更多信息，请参阅此内容 [部分](../reports/global-report.md#modify-dashboard).

有关Adobe Journey Optimizer中可用的每个量度的详细列表，请参阅 [本页](global-report.md#list-of-components-global.md)

## “营销活动”选项卡 {#campaign-global}

### 交付 {#delivery-global}

![](assets/campaign_report_global_1.png)

的 **[!UICONTROL Campaign的统计信息]** 小组件详细介绍与您的营销活动相关的主要信息：

* **[!UICONTROL 输入的用户档案]**:开始历程的用户档案数。

* **[!UICONTROL 已交付的操作]**:历程中某个操作被交付的唯一次数总数。

* **[!UICONTROL 操作在%中失败]**:与提交操作的独特总次数相比，历程中操作失败的独特总次数。

## “电子邮件”选项卡 {#email-global}

![](assets/campaign_report_global_2.png)

从营销策划 **[!UICONTROL 全局报告]**, **[!UICONTROL 电子邮件]** 选项卡详细列出了与营销活动中发送的电子邮件投放相关的主要信息。

+++了解有关电子邮件报表可用的不同量度和小组件的更多信息。

的 **[!UICONTROL 电子邮件发送统计信息]** 图形详细说明了交付的成功：

* **[!UICONTROL 目标]**:在投放分析期间处理的消息总数。

* **[!UICONTROL 已发送]**:投放的发送总数。

* **[!UICONTROL 已交付]**:已成功发送的消息数，与已发送消息的总数有关。

* **[!UICONTROL 投放率]**:成功发送的消息的百分比。

* **[!UICONTROL 跳出次数]**:在投放和自动回访处理过程中累积的与已发送消息总数有关的错误总数。

* **[!UICONTROL 跳出率]**:退回的电子邮件与发送的电子邮件的百分比。

* **[!UICONTROL 错误]**:投放期间发生的阻止将其发送到用户档案的错误总数。

* **[!UICONTROL 错误率]**:与发送的电子邮件相比，在阻止发送投放的投放期间发生的错误百分比。

* **[!UICONTROL 重试]**:队列中要重试的电子邮件数量。

* **[!UICONTROL 排除]**:已被Adobe Journey Optimizer排除的用户档案数。

的 **[!UICONTROL 电子邮件 — 跟踪统计信息]** 小组件包含用于投放的收件人活动的可用数据：

* **[!UICONTROL 打开]**:投放中打开投放的次数。

* **[!UICONTROL 唯一打开数]**:已打开投放的百分比。

* **[!UICONTROL 打开率]**:已打开的电子邮件总数与已投放电子邮件的数量相比较。

* **[!UICONTROL 点击次数]**:电子邮件中内容的点击次数。

* **[!UICONTROL 独特点击]**：点击了电子邮件中内容的收件人数。

* **[!UICONTROL 独特点击率]**:与投放进行交互的用户百分比。

* **[!UICONTROL 取消订阅]**:退订链接的点击次数。

* **[!UICONTROL 垃圾邮件投诉]**:将消息声明为垃圾邮件或垃圾邮件的次数。

的 **[!UICONTROL 发送统计信息]** 图表包含可用于已发送电子邮件的数据，例如：

* **[!UICONTROL 已交付]**:已成功发送的消息数，与已发送消息的总数有关。

* **[!UICONTROL 跳出次数]**:在投放和自动回访处理过程中累积的与已发送消息总数有关的错误总数。

* **[!UICONTROL 重试]**:队列中要重试的电子邮件数量。

* **[!UICONTROL 错误]**:投放期间发生的阻止将其发送到用户档案的错误总数。

的 **[!UICONTROL 退回原因]** 和 **[!UICONTROL 跳出类别]** 小组件包含与弹回的消息相关的可用数据，例如：

* **[!UICONTROL 硬退回]**:永久错误的总数，如错误的电子邮件地址。 这涉及显式声明地址无效的错误消息，如未知用户。

* **[!UICONTROL 软退回]**:临时错误（如完整收件箱）的总数。

* **[!UICONTROL 已忽略]**:临时（如“不在办公室”）或技术错误（例如，如果发件人类型为邮递员）的总数。

有关退回的更多信息，请参阅 [禁止列表](../reports/suppression-list.md) 页面。

的 **[!UICONTROL 错误原因]** 通过图表和表格，可查看在投放期间发生的错误。

的 **[!UICONTROL 排除的原因]** 图形和表格显示阻止从定向用户档案中排除的用户配置文件接收消息的不同原因。

的 **[!UICONTROL 电子邮件 — 顶部Url]** 图表和表格详细列出了投放中哪些URL的访问次数最多。

的 **[!UICONTROL 电子邮件 — 热门收件人域]** 图表和表格详细列出了收件人最常使用哪些域来打开电子邮件。

>[!NOTE]
>
>的 **[!UICONTROL 优化与非优化]** 和 **[!UICONTROL 发送时间优化]**  只有为您的投放激活了发送时间优化选项时，小组件才可用。 有关发送时间优化的详细信息，请参阅 [本页](../messages/send-time-optimization.md).

的 **[!UICONTROL 优化与非优化]** 图表详细列出了与消息相关的主要信息（无论消息是否已优化）：

* **[!UICONTROL 已发送]**:投放的发送总数。
* **[!UICONTROL 打开]**:投放中打开投放的次数。
* **[!UICONTROL 点击次数]**:电子邮件中内容的点击次数。

的 **[!UICONTROL 发送时间优化]** 根据发送方法详细描述投放成功与否：已优化或正常。

* **[!UICONTROL 已交付]**:已成功发送的消息数，与已发送消息的总数有关。
* **[!UICONTROL 跳出次数]**:在投放和自动回访处理过程中累积的与已发送消息总数有关的错误总数。
+++

## “推送通知”选项卡 {#push-global}

从营销策划 **[!UICONTROL 全局报告]**, **[!UICONTROL 推送通知]** 选项卡详细列出了与营销活动中发送的推送投放相关的主要信息。

![](assets/campaign_report_global_3.png)

+++了解有关可用于推送报表的不同量度和小组件的更多信息。

的 **[!UICONTROL 推送通知 — 发送统计信息]** 表格使用图形和KPI详细列出了与推送通知相关的主要信息：

* **[!UICONTROL 目标]**:在投放分析期间处理的消息总数。

* **[!UICONTROL 已发送]**:投放的发送总数。

* **[!UICONTROL 已交付]**:已成功发送的消息数，与已发送消息的总数有关。

* **[!UICONTROL 投放率]**:成功发送的消息的百分比。

* **[!UICONTROL 跳出次数]**:在投放和自动回访处理过程中累积的与已发送消息总数有关的错误总数。

* **[!UICONTROL 跳出率]**:与发送的推送通知相比，已退回的推送通知的百分比。

* **[!UICONTROL 错误]**:投放期间发生的阻止将其发送到用户档案的错误总数。

* **[!UICONTROL 错误率]**:与发送的推送通知相比，在阻止发送投放的投放期间发生的错误百分比。

* **[!UICONTROL 排除]**:已被Adobe Journey Optimizer排除的用户档案数。

的 **[!UICONTROL 推送 — 跟踪统计信息]** 包含用于投放的收件人活动的可用数据：

* **[!UICONTROL 打开]**:投放中消息打开的次数。

* **[!UICONTROL 打开率]**:打开的推送通知的百分比。

* **[!UICONTROL 操作]**:已送达推送通知的操作总数，例如按钮单击或解除。

* **[!UICONTROL 参与]**:此推送通知的打开和操作总数，例如用户档案打开推送或单击按钮时。

* **[!UICONTROL 参与率]**:此推送通知的打开次数和操作的百分比，例如用户档案打开了推送或单击了按钮。

的 **[!UICONTROL 推送通知摘要]** 图表包含可用于已发送推送通知的数据，例如：

* **[!UICONTROL 打开]**:投放中消息打开的次数。

* **[!UICONTROL 操作]**:已送达推送通知的操作总数，例如按钮单击或解除。

* **[!UICONTROL 跳出次数]**:在投放和自动回访处理过程中累积的与已发送消息总数有关的错误总数。

* **[!UICONTROL 已交付]**:已成功发送的消息数，与已发送消息的总数有关。

* **[!UICONTROL 错误]**:投放期间发生的阻止将其发送到用户档案的错误总数。

>[!NOTE]
>
>的 **[!UICONTROL 优化与非优化]** 和 **[!UICONTROL 发送时间优化]**  只有为您的投放激活了发送时间优化选项时，小组件才可用。 有关发送时间优化的详细信息，请参阅 [本页](../messages/send-time-optimization.md).

的 **[!UICONTROL 优化与非优化]** 图表详细列出了与消息相关的主要信息（无论消息是否已优化）：

* **[!UICONTROL 已交付]**:已成功发送的消息数，与已发送消息的总数有关。
* **[!UICONTROL 打开]**:投放中打开投放的次数。
* **[!UICONTROL 操作]**:已送达推送通知的操作总数，例如按钮单击或解除。

的 **[!UICONTROL 发送时间优化]** 根据发送方法详细描述投放成功与否：已优化或正常。

* **[!UICONTROL 已交付]**:已成功发送的消息数，与已发送消息的总数有关。
* **[!UICONTROL 跳出次数]**:在投放和自动回访处理过程中累积的与已发送消息总数有关的错误总数。

的 **[!UICONTROL 错误原因]** 通过图表和表格，可查看在投放期间发生的错误。

的 **[!UICONTROL 排除的原因]** 图形和表格显示阻止从定向用户档案中排除的用户配置文件接收消息的不同原因。

的 **[!UICONTROL 按平台跟踪]**, **[!UICONTROL 按平台发送]** 和 **[!UICONTROL 按平台划分]** 图形和表格根据收件人的操作系统详细列出了推送通知的成功情况。
+++

## “短信”选项卡 {#sms-global}

从营销策划 **[!UICONTROL 全局报告]**, **[!UICONTROL 短信]** 选项卡详细列出了与营销活动中发送的短信投放相关的主要信息。

![](assets/campaign_report_global_4.png)

+++了解有关可用于短信报表的不同量度和小组件的更多信息。

的 **[!UICONTROL 短信 — 发送统计信息]** 表格详细说明了交付的成功：

* **[!UICONTROL 目标]**:符合此投放目标用户档案的用户配置文件数。

* **[!UICONTROL 排除]**:未收到消息的从定向用户档案中排除的用户用户档案数。

* **[!UICONTROL 已发送]**:投放的发送总数。

* **[!UICONTROL 已交付]**:已成功发送的消息数，与已发送消息的总数有关。

* **[!UICONTROL 跳出次数]**:在投放和自动回访处理过程中累积的与已发送消息总数有关的错误总数。

* **[!UICONTROL 错误]**:投放期间发生的阻止将其发送到用户档案的错误总数。

的 **[!UICONTROL 按日期划分的短信性能]** 小组件通过图形详细描述与您的消息相关的主要信息：

* **[!UICONTROL 已发送]**:投放的发送总数。

* **[!UICONTROL 已交付]**:已成功发送的消息数，与已发送消息的总数有关。

* **[!UICONTROL 跳出次数]**:在投放和自动回访处理过程中累积的与已发送消息总数有关的错误总数。

* **[!UICONTROL 错误]**:投放期间发生的阻止将其发送到用户档案的错误总数。

的 **[!UICONTROL 排除原因]**, **[!UICONTROL 退回原因]** 和 **[!UICONTROL 错误原因]** 图形和表格允许您查看在投放期间发生的错误和排除项。
+++

## 其他资源

* [营销活动入门](../campaigns/get-started-with-campaigns.md)
* [创建营销活动](../campaigns/create-campaign.md)
* [创建API触发的营销活动](../campaigns/api-triggered-campaigns.md)
* [修改或停止营销活动](../campaigns/modify-stop-campaign.md)
* [营销活动实时报告](campaign-live-report.md)
