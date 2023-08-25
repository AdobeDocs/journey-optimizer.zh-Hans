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
source-git-commit: 164a7376c362f67f82f7cf07ec21aa42b9b342cf
workflow-type: tm+mt
source-wordcount: '1352'
ht-degree: 6%

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

## “营销活动”选项卡 {#campaign-global}

### 交付 {#delivery-global}

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

来自您的营销活动 **[!UICONTROL 实时报告]**， **[!UICONTROL 应用程序内]** 选项卡详细列出了与您的营销活动中发送的应用程序内投放相关的主要信息。

+++了解有关可用于应用程序内报表的不同量度和小组件的更多信息。

此 **[!UICONTROL 应用程序内性能]** KPI可详细列出与访客与应用程序内消息互动相关的主要信息，例如：

* **[!UICONTROL 展示次数]**：交付给所有用户的应用程序内消息总数。

* **[!UICONTROL 交互]**：应用程序内消息的参与总数。 这包括用户执行的任何操作，例如单击、解除或任何其他交互。

此 **[!UICONTROL 应用程序内摘要]** 图形可显示应用程序内展示次数和交互在相关时间段的演变。

此 **[!UICONTROL 按类型列出的交互]** 图表和表详细介绍了用户如何通过跟踪任何点击、解除或交互来与您的应用程序内消息进行交互。

+++

## “推送通知”选项卡 {#push-live}

来自您的营销活动 **[!UICONTROL 实时报告]**， **[!UICONTROL 推送通知]** 选项卡详细列出了与您的营销活动中发送的推送投放相关的主要信息。

![](assets/campaign_report_live_2.png)

+++了解有关可用于推送报表的不同量度和小组件的更多信息。

**[!UICONTROL 推送通知发送性能]**， **[!UICONTROL 推送通知摘要]** 和 **[!UICONTROL 发送指标 — 按推送]** 构件详细列出与报文相关的主要信息：

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

来自您的营销活动 **[!UICONTROL 实时报告]**， **[!UICONTROL Web]** 选项卡详细列出了与您的网页相关的主要信息。

+++了解更多可用于Web报表的不同量度和小组件。

此 **[!UICONTROL Web性能]** KPI可详细列出与访客对Web体验的参与度相关的主要信息，例如：

* **[!UICONTROL 展示次数]**：交付给所有用户的Web体验总数。

* **[!UICONTROL 交互]**：与网页的互动总数。 这包括用户执行的任何操作，例如点击或任何其他交互。

此 **[!UICONTROL Web摘要]** 图形可显示过去24小时内您的Web体验（展示次数、独特展示次数和交互）的演变。

此 **[!UICONTROL 按元素显示的交互]** 该表详细列出了与访客对网页上各种元素的参与度相关的主要信息。
+++

## 直邮选项卡 {#direct-mail-tab}

来自您的营销活动 **[!UICONTROL 全局报告]**， **[!UICONTROL 直邮]** 选项卡详细列出了与直邮投放相关的主要信息。

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
