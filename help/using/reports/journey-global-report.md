---
solution: Journey Optimizer
product: journey optimizer
title: 历程全局报告
description: 了解如何使用历程全局报告中的数据
feature: Reporting
topic: Content Management
role: User
level: Intermediate
exl-id: e851646e-4cef-45e8-97c2-a8f4c9d2cc08
source-git-commit: 0ec122bbf134c41f95755a3b6f08eb7ef68506df
workflow-type: tm+mt
source-wordcount: '2022'
ht-degree: 2%

---

# 历程全局报告 {#journey-global-report}

>[!CONTEXTUALHELP]
>id="ajo_journey_global_report"
>title="历程全局报告"
>abstract="历程全局报告让您可以衡量您的历程在选定时段内产生的影响。报告分为不同的构件，详细说明历程中的成功和错误。每个报告仪表板都可以修改，您可以调整构件大小或删除构件。"

历程全局报告可直接从您的历程(使用 **[!UICONTROL 查看报表]** 按钮。

![](assets/report_journey.png)

历程 **[!UICONTROL 全局报告]** 页面中将显示以下选项卡：

* [历程](#journey-global)
* [电子邮件](#email-global)
* [推送](#push-global)
* [短信](#sms-global)

历程 **[!UICONTROL 全局报告]** 会分为不同的小组件，用于详细描述历程的成功和错误。 如果需要，可以调整每个小组件的大小并将其删除。 有关此内容的更多信息，请参阅此内容 [部分](global-report.md#modify-dashboard).

有关Adobe Journey Optimizer中可用的每个量度的详细列表，请参阅 [本页](global-report.md#list-of-components-global).

## 历程选项卡 {#journey-global}

从您的历程 **[!UICONTROL 全局报告]**, **[!UICONTROL 历程]** 选项卡可让您清楚地查看有关历程的最重要跟踪数据。

![](assets/journey_global_1.png)

+++了解有关可用于历程报表的不同量度和小组件的更多信息。

的 **[!UICONTROL 历程性能]** 小组件允许您逐步查看目标用户档案在历程中的路径。

的 **[!UICONTROL 历程统计]** 小组件显示以下KPI:

* **[!UICONTROL 输入的用户档案]**:到达历程的登入事件的个人总数。

* **[!UICONTROL 退出用户档案]**:退出历程的个人总数。

* **[!UICONTROL 失败的单个历程]**:未成功执行的各个历程的总数。

的 **[!UICONTROL 事件接收的事件]**, **[!UICONTROL 按来源划分的事件]** 和 **[!UICONTROL 热门事件]** 小组件允许您查看 **[!UICONTROL 事件]** 已成功通过图形和表执行。

**[!UICONTROL 操作性能]**, **[!UICONTROL 操作错误原因]** 和 **[!UICONTROL 热门操作]** 小组件代表在 **[!UICONTROL 操作]** 触发。

的 **[!UICONTROL 热门操作]** 表包含可用于 **[!UICONTROL 操作]**，例如：

* **[!UICONTROL 已成功执行操作]**:总数 **[!UICONTROL 操作]** 成功执行历程。

* **[!UICONTROL 操作错误]**:发生的错误总数 **[!UICONTROL 操作]**.

的 **[!UICONTROL 同意策略]** 表格和图形显示自定义操作中从每个策略中排除的用户档案数。
有关自定义操作的更多信息，请参阅 [详细文档](../action/about-custom-action-configuration.md).

请注意，要使这些小组件显示在您的历程报表中，您需要重置功能板。 为此，请单击 **[!UICONTROL 修改]** then **[!UICONTROL 重置]** 中。
+++

## “电子邮件”选项卡 {#email-global}

从您的历程 **[!UICONTROL 全局报告]**, **[!UICONTROL 电子邮件]** 选项卡详细列出了与历程中发送的电子邮件投放相关的主要信息。

![](assets/journey_global_2.png)

+++了解有关电子邮件报表可用的不同量度和小组件的更多信息。

的 **[!UICONTROL 电子邮件发送统计信息]** 图形详细说明了交付的成功：

* **[!UICONTROL 目标]**:AdobeJourney Orchestration为任何操作（如发送电子邮件或短信）定向的用户档案数

* **[!UICONTROL 已发送]**:投放的发送总数。

* **[!UICONTROL 已交付]**:已成功发送的消息数，与已发送消息的总数有关。

* **[!UICONTROL 投放率]**:成功发送的消息的百分比。

* **[!UICONTROL 跳出次数]**:在投放和自动回访处理过程中累积的与已发送消息总数有关的错误总数。

* **[!UICONTROL 跳出率]**:退回的电子邮件与发送的电子邮件的百分比。

* **[!UICONTROL 错误]**:投放期间发生的阻止将其发送到用户档案的错误总数。

* **[!UICONTROL 错误率]**:与发送的电子邮件相比，在阻止发送投放的投放期间发生的错误百分比。

的 **[!UICONTROL 电子邮件 — 跟踪统计信息]** 包含用于投放的收件人活动的可用数据：

* **[!UICONTROL 打开]**:投放中打开投放的次数。

* **[!UICONTROL 唯一打开数]**:已打开投放的百分比。

* **[!UICONTROL 唯一打开率]**:已打开的电子邮件总数与已投放电子邮件的数量相比较。

* **[!UICONTROL 点击次数]**:电子邮件中内容的点击次数。

* **[!UICONTROL 独特点击]**：点击了电子邮件中内容的收件人数。

* **[!UICONTROL 点进率]**:与历程进行交互的用户百分比。

* **[!UICONTROL 取消订阅]**:退订链接的点击次数。

* **[!UICONTROL 垃圾邮件投诉]**:将消息声明为垃圾邮件或垃圾邮件的次数。

的 **[!UICONTROL 发送统计信息]** 图表包含可用于已发送电子邮件的数据，例如：

* **[!UICONTROL 已交付]**:已成功发送的消息数，与已发送消息的总数有关。

* **[!UICONTROL 跳出次数]**:在投放和自动回访处理过程中累积的与已发送消息总数有关的错误总数。

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
>的 **[!UICONTROL 优化与非优化]** 和 **[!UICONTROL 发送时间优化]**  只有为您的投放激活了发送时间优化选项时，小组件才可用。 有关发送时间优化的详细信息，请参阅 [本页](../building-journeys/journeys-message.md#send-time-optimization).

的 **[!UICONTROL 优化与非优化]** 图表详细列出了与消息相关的主要信息（无论消息是否已优化）：

* **[!UICONTROL 已发送]**:投放的发送总数。
* **[!UICONTROL 打开]**:投放中打开投放的次数。
* **[!UICONTROL 点击次数]**:电子邮件中内容的点击次数。

的 **[!UICONTROL 发送时间优化]** 根据发送方法详细描述投放成功与否：已优化或正常。

* **[!UICONTROL 已交付]**:已成功发送的消息数，与已发送消息的总数有关。
* **[!UICONTROL 跳出次数]**:在投放和自动回访处理过程中累积的与已发送消息总数有关的错误总数。

>[!NOTE]
>
>仅当在电子邮件中插入决策时，选件小组件和量度才可用。 有关决策管理的详细信息，请参阅此 [页面](../offers/get-started/starting-offer-decisioning.md).

的 **[!UICONTROL 优惠统计]** 和 **[!UICONTROL 提供统计信息]** 随着时间的推移，小组件可衡量选件的成功以及对目标受众的影响。 它使用KPI详细描述与消息相关的主要信息：

* **[!UICONTROL 已发送选件]**:选件的发送总数。

* **[!UICONTROL 优惠展示]**:在投放中打开选件的次数。

* **[!UICONTROL 选件点击量]**:在投放中点击选件的次数。

的 **[!UICONTROL 选件详细统计信息]** 表包含与选件一起用于收件人活动的可用数据：

* **[!UICONTROL 版面名称]**:用于显示选件的版面名称。 有关版面的更多信息，请参阅 [页面](../offers/offer-library/creating-placements.md).

* **[!UICONTROL 选件名称]**:在投放中添加的选件的名称。 有关版面的更多信息，请参阅 [页面](../offers/offer-library/creating-personalized-offers.md).

* **[!UICONTROL 已发送选件]**:选件的发送总数。

* **[!UICONTROL 优惠展示率]**:已打开选件与已发送选件数的百分比。

* **[!UICONTROL 选件点击率]**:与选件进行交互的用户百分比。
+++

## “推送通知”选项卡 {#push-global}

从您的历程 **[!UICONTROL 全局报告]**, **[!UICONTROL 推送通知]** 选项卡详细列出了与历程中发送的推送投放相关的主要信息。

![](assets/journey_global_3.png)

+++了解有关可用于推送报表的不同量度和小组件的更多信息。

的 **[!UICONTROL 推送通知 — 发送统计信息]** 表格使用图形和KPI详细列出了与推送通知相关的主要信息：

* **[!UICONTROL 目标]**:AdobeJourney Orchestration为任何操作（如发送电子邮件或短信）定向的用户档案数

* **[!UICONTROL 已发送]**:投放的发送总数。

* **[!UICONTROL 已交付]**:已成功发送的消息数，与已发送消息的总数有关。

* **[!UICONTROL 投放率]**:成功发送的消息的百分比。

* **[!UICONTROL 跳出次数]**:在投放和自动回访处理过程中累积的与已发送消息总数有关的错误总数。

* **[!UICONTROL 跳出率]**:与发送的推送通知相比，已退回的推送通知的百分比。

* **[!UICONTROL 错误]**:投放期间发生的阻止将其发送到用户档案的错误总数。

* **[!UICONTROL 错误率]**:与发送的推送通知相比，在阻止发送投放的投放期间发生的错误百分比。

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
>的 **[!UICONTROL 优化与非优化]** 和 **[!UICONTROL 发送时间优化]**  只有为您的投放激活了发送时间优化选项时，小组件才可用。 有关发送时间优化的详细信息，请参阅 [本页](../building-journeys/journeys-message.md#send-time-optimization).

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

短信 **[!UICONTROL 全局报告]** 会分为不同的小组件，用于详细描述投放的成功和错误。 如果需要，可以调整每个小组件的大小并将其删除。 有关此内容的详细信息，请参阅 [部分](global-report.md#modify-dashboard).
+++

## “短信”选项卡 {#sms-global}

![](assets/journey_global_4.png)

+++了解有关可用于短信报表的不同量度和小组件的更多信息。

的 **[!UICONTROL 短信 — 发送统计信息]** 表格详细说明了交付的成功：

* **[!UICONTROL 目标]**:符合此投放目标用户档案的用户配置文件数。

* **[!UICONTROL 排除]**:未收到消息的从定向用户档案中排除的用户用户档案数。

* **[!UICONTROL 已发送]**:投放的发送总数。

* **[!UICONTROL 已交付]**:已成功发送的消息数，与已发送消息的总数有关。

* **[!UICONTROL 跳出次数]**:在投放和自动回访处理过程中累积的与已发送消息总数有关的错误总数。

* **[!UICONTROL 错误]**:投放期间发生的阻止将其发送到用户档案的错误总数。

的 **[!UICONTROL 短信摘要]** 小组件通过图形详细描述与您的消息相关的主要信息：

* **[!UICONTROL 已发送]**:投放的发送总数。

* **[!UICONTROL 已交付]**:已成功发送的消息数，与已发送消息的总数有关。

* **[!UICONTROL 跳出次数]**:在投放和自动回访处理过程中累积的与已发送消息总数有关的错误总数。

* **[!UICONTROL 错误]**:投放期间发生的阻止将其发送到用户档案的错误总数。

的 **[!UICONTROL 排除原因]** 图形和表格允许您查看在投放期间发生的错误和排除项。
+++
