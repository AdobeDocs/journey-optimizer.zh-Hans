---
solution: Journey Optimizer
product: journey optimizer
title: Journey Optimizer中的跟踪入门
description: 了解Journey Optimizer中可用的跟踪和监控功能
feature: Monitoring
topic: Administration
role: User
level: Beginner
keywords: 跟踪，监测，分析，报告，可投放性
source-git-commit: 94350929bc9a6c2d33ac551429b844b97be04ae5
workflow-type: tm+mt
source-wordcount: '1837'
ht-degree: 3%

---

# Journey Optimizer中的跟踪入门 {#get-started-tracking}

了解客户如何与您的通信进行交互是创造有意义的体验和取得成效的关键。 Journey Optimizer提供全面的跟踪和监控功能，让您能够了解客户行为、交付性能和系统状况，同时尊重隐私和维护合规性。

>[!BEGINSHADEBOX]

**在Journey Optimizer中可以跟踪的内容：**

📧 **电子邮件交互** — 打开次数、点击次数和链接性能

🌐 **Web行为** — 页面查看次数、点击次数和参与模式

🛤️ **历程性能** — 自定义量度、步骤事件和转化路径

📊 **可投放性运行状况** — 退回率、垃圾邮件投诉和发件人信誉

⚙️ **系统操作** — 警报、错误和自定义操作性能

>[!ENDSHADEBOX]

## 跨渠道跟踪客户互动 {#tracking-by-channel}

Journey Optimizer提供特定于渠道的跟踪功能。 下面是如何为每个渠道配置和使用跟踪的。

### 电子邮件跟踪 {#email-tracking}

创建电子邮件时，会自动启用电子邮件跟踪。 默认情况下，Journey Optimizer会跟踪打开、点击和取消订阅次数，无需其他配置。

**配置跟踪选项：**

* **启用/禁用跟踪** — 在设计电子邮件时在邮件级别控制跟踪。 您可以选择跟踪打开次数、点击次数或同时跟踪两者。 [了解详情](../email/message-tracking.md)

* **设置URL跟踪参数** — 在表面级别配置跟踪参数以自动将营销活动标识符（utm_campaign、utm_source等）附加到所有电子邮件链接。 这支持在整个数字生态系统中进行归因跟踪。 [了解详情](../email/url-tracking.md)

* **跟踪片段中的链接** — 自动跟踪可重用内容片段中的所有链接，从而提供共享内容组件之间参与情况的完整视图。

* **添加镜像页面跟踪** — 启用镜像页面选项以创建电子邮件的Web版本，并自动跟踪查看该版本的用户。 [了解详情](../email/message-tracking.md#mirror-page)

**监测性能：**&#x200B;查看营销活动和历程报告中的实时量度，包括打开次数、点击次数和链接级别的性能。 [营销活动报告](../reports/campaign-global-report-cja-email.md) | [历程报告](../reports/journey-global-report-cja-email.md)

### Web 跟踪 {#web-tracking}

Web跟踪需要明确配置以跟踪用户与Web修改的交互。

**设置点击跟踪：**

在设计Web修改时，您可以选择要跟踪的特定元素（按钮、图像、链接）。 这样即可启用这些元素的点击跟踪，而无需其他代码。 [了解详情](../web/monitor-web-experiences.md)

* **跟踪任何可点击元素** — 选择Web个性化中的按钮、图像、链接或任何交互式元素
* **自动数据收集** — 配置后，Journey Optimizer会自动捕获点击事件并将它们与配置文件关联
* **实时监控** — 跟踪用户交互以验证个性化有效性

**查看跟踪数据：**&#x200B;访问报表中的显示量度、点进率和元素级性能。 [营销活动报告](../reports/campaign-global-report-cja-web.md) | [历程报告](../reports/journey-global-report-cja-web.md)

### 推送通知跟踪 {#push-tracking}

推送跟踪会自动启用，并捕获展示次数（已投放）、点击次数（已点按）和打开次数（已启动应用程序）。 要最大化跟踪值，请在推送内容中配置可单击元素。

**配置跟踪的元素：**

* **正文点击行为** — 设置用户点击通知时发生的情况：打开应用程序、导航到深层链接或打开Web URL。 系统会自动跟踪每个操作。 [了解详情](../push/design-push.md#on-click-behavior)

* **添加操作按钮** — 包含最多3个按钮(Android)或多个按钮(iOS)，每个按钮操作（打开应用程序、深层链接、Web URL）具有独立的跟踪。 [了解详情](../push/design-push.md#add-buttons-push)

* **启用跟踪** — 验证是否已在推送历程活动或营销活动跟踪设置中启用跟踪。 [了解详情](../push/create-push.md#create)

>[!NOTE]
>
>推送跟踪需要实施SDK移动设备。 确保您的应用程序正确配置了Adobe Experience Platform Mobile SDK。

**分析参与情况：**&#x200B;在报表中查看点进率、按钮性能和跟踪的链接详细信息。 [营销活动报告](../reports/campaign-global-report-cja-push.md) | [历程报告](../reports/journey-global-report-cja-push.md)

### 应用程序内消息跟踪 {#inapp-tracking}

应用程序内消息会自动跟踪显示和用户交互。 配置触发器和内容以最大限度地提高跟踪效率。

**配置跟踪：**

* **设置显示规则** — 使用触发器（应用程序启动、屏幕加载）、频率规则和受众条件定义应用程序内消息出现的时间和位置。 正确的配置可确保准确跟踪触发和显示的消息。 [了解详情](../in-app/create-in-app.md)

* **添加跟踪的元素** — 在消息内容中包含按钮、链接和交互式元素。 使用详细标签自动跟踪每个交互。

* **优化显示时间** — 配置星期几和星期几规则，以最大限度地提高触发的消息实际显示给用户的可能性。

**跟踪的内容：** Journey Optimizer自动捕获显示、按钮点击次数、解除、触发与显示的量度，以及链接性能。 [营销活动报告](../reports/campaign-global-report-cja-inapp.md) | [历程报告](../reports/journey-global-report-cja-inapp.md)

### 短信和彩信跟踪 {#sms-tracking}

短信跟踪需要最少的设置 — Journey Optimizer会自动缩短并跟踪您包含在消息中的链接。

**工作方式：**

* **自动链接跟踪** — 使用URL帮助程序函数将任何URL添加到您的SMS内容。 Journey Optimizer会自动缩短链接并跟踪点击，而无需额外配置。 要使用URL缩短功能，必须首先配置短信子域。 [了解详情](../sms/create-sms.md#sms-content)

* **入站邮件跟踪** — 自动捕获收件人的回复，允许您监视双向对话和响应模式。

**查看量度：**&#x200B;访问链接在报表中点击数据、入站消息卷和消息类型性能。 [营销活动报告](../reports/campaign-global-report-cja-sms.md) | [历程报告](../reports/journey-global-report-cja-sms.md)

### 基于代码的体验跟踪 {#code-based-tracking}

基于代码的体验需要设置实施，才能将跟踪数据发送到Adobe Experience Platform。

**先决条件：**

在进行跟踪之前，您需要配置实施以将交互事件（显示、单击）发送到Adobe Experience Platform。 这需要：

* 设置为Adobe Experience Platform配置的数据流
* 使用Web SDK或Mobile SDK在代码中实施事件收集
* 在用户查看或单击个性化内容时发送建议交互事件

[了解有关实施先决条件的更多信息](../code-based/code-based-prerequisites.md#reporting-prerequisites)

**跟踪的内容：**&#x200B;实施后，可以跨任何数字接触点（网站、移动应用程序、物联网设备等）跟踪显示、点击、点进率和元素级性能。 [营销活动报告](../reports/campaign-global-report-cja-code.md) | [历程报告](../reports/journey-global-report-cja-code.md)

### 内容卡跟踪 {#content-card-tracking}

内容卡会自动跟踪用户交互。 配置内容和显示规则以控制跟踪行为。

**如何实施：**

* **设计跟踪的内容** — 将按钮和链接添加到您的内容卡。 使用标签和URL自动跟踪每个交互式元素。

* **配置持久性** — 内容卡在应用程序会话之间持续存在，允许您跟踪长期参与模式。 设置过期规则以控制卡片可跟踪的时长。

* **设置显示规则** — 定义卡片出现的时间和位置，以确保准确跟踪显示内容与交互。

**监测参与情况：**&#x200B;跟踪多个会话中的显示次数、点击次数、点进率和参与模式。 [营销活动报告](../reports/campaign-global-report-cja-content.md) | [历程报告](../reports/journey-global-report-cja-content.md)

## 监控您的登陆页面 {#landing-page-tracking}

登陆页面带有内置跟踪，无需额外设置。 Journey Optimizer会自动捕获访问次数、转化率和跳出率。

**自动跟踪的内容：**

* **访问次数** — 用于测量访问范围的总访问次数和独特访问次数
* **转化** — 表单提交、订阅确认或其他定义的操作
* **跳出率** — 离开但未进行交互的访客百分比
* **性能趋势** — 显示量度如何演变的时间系列数据

**优化性能：**&#x200B;使用跟踪数据优化表单字段、测试内容变化、识别有效流量源并减少放弃。 [了解详情](../reports/lp-report-global-cja.md)

## 跟踪您的历程和营销活动 {#journey-campaign-tracking}

除了渠道级别跟踪之外，还可以配置跟踪以衡量整体绩效并了解客户在整个营销活动中的行为。

**设置营销活动跟踪：**
<!--
* **Configure optimization** - When setting up campaigns, enable experimentation or targeting to track which content variations perform best. [Learn more](../campaigns/campaigns-message-optimization.md)-->

* **定义转化量度** — 指定哪些操作会计为转化（购买、注册、下载），以衡量参与量度之外的促销活动有效性。

* **设置计划** — 配置发送时间优化以跟踪不同计时策略的性能并确定最佳发送窗口。 [了解详情](../building-journeys/send-time-optimization.md)

**设置历程跟踪：**

* **定义自定义成功量度** — 根据标准参与量度之外的业务目标（购买、注册、续订等）配置特定KPI。 [了解详情](../building-journeys/success-metrics.md)

* **启用历程步骤事件** — 激活客户在历程中执行的每项操作的详细跟踪。 这提供了入口/出口点、路径选择和放置位置的精细可见性。 [了解详情](../reports/journey-step-events-overview.md)

* **配置自定义操作监视** — 设置与外部系统集成的跟踪，以监视API调用、响应时间和错误模式。 [了解详情](../action/reporting.md)

* **自定义报告和数据导出** — 构建量身定制的报告并将跟踪数据导出到外部系统以进行更深入的分析。 [了解详情](../reports/sharing-overview.md)

**查看统一性能：**&#x200B;访问营销活动和历程的综合报告，比较电子邮件、推送、短信和其他渠道的性能，并了解哪些组合可产生最佳结果。 [营销活动报告](../reports/campaign-global-report-cja.md) | [历程报告](../reports/journey-global-report-cja.md)

## 管理优化性能 {#optimization-tracking}

Journey Optimizer会自动跟踪优化实验和定位策略。 配置优化以确保正确的数据收集。

**设置优化跟踪：**

* **配置实验** — 在创建实验或使用定位时，定义要跟踪的量度（转化率、点击量、自定义事件）。 Journey Optimizer会自动收集每个处理的性能数据。 [了解详情](../campaigns/campaigns-message-optimization.md)

* **设置路径优化** — 向历程添加&#x200B;**优化**&#x200B;活动并配置多个路径。 Journey Optimizer会自动跟踪用户档案采用的路径并衡量性能。 [了解详情](../building-journeys/optimize.md)

**分析结果：**&#x200B;在试验报告中查看转化率、统计显着性和治疗之间的提升。 [营销活动报告](../reports/campaign-global-report-cja-experimentation.md) | [历程报告](../reports/journey-global-report-cja-experimentation.md)

## 跟踪决策性能 {#decisioning-tracking}

使用Decisioning个性化内容时，Journey Optimizer会自动跟踪决策事件、展示次数和点击次数，而无需额外配置。

**跟踪的工作方式：**

* **自动事件捕获** — 每当为用户档案选择决策项时，Journey Optimizer都会自动捕获决策事件。
* **展示跟踪** — 对于电子邮件，展示会被自动跟踪。 对于基于代码的体验，您需要在代码中实施建议显示事件。
* **点击跟踪** — 在电子邮件中自动跟踪对决策项的点击；基于代码的体验需要实施点击事件。

**基于代码的跟踪的先决条件：**

要在基于代码的体验中跟踪决策，请确保您的实施使用Web SDK或Mobile SDK将建议交互事件（显示和单击）发送到Adobe Experience Platform。 [了解详情](../experience-decisioning/gs-experience-decisioning.md)

**分析性能：**&#x200B;查看决策KPI、比较决策项、分析选择策略并在报表中监视AI模型性能。 [了解详情](../experience-decisioning/cja-reporting.md)

## 控制跟踪数据的使用 {#data-governance}

通过数据治理策略，您可以控制如何在您的组织中使用跟踪数据：

* **为敏感跟踪数据设置标签** — 将治理标签应用于跟踪的行为数据（例如，对健康内容的点击、金融产品交互），以将其标记为敏感或受管制。

* **限制数据使用** — 创建策略，以防止将已标记的跟踪数据用于某些渠道、导出到第三方系统或用于特定的个性化方案。

* **自动实施** — 当您构建历程和营销活动时，Journey Optimizer会自动检查治理策略，如果跟踪的数据正在违反定义的策略的情况下使用，则阻止发布。

数据治理确保遵守GDPR和CCPA等法规，同时仍允许您跟踪和分析客户在批准的边界内的行为。 [了解详情](../action/action-privacy.md)

## 监测可投放性和系统运行状况 {#monitoring-capabilities}

除了跟踪参与外，还应配置监控以确保消息到达收件箱且系统以最佳方式运行。

**设置主动监控：**

* **配置警报** — 设置历程错误、自定义操作失败和严重问题的实时通知，以便快速响应问题。 [了解详情](../reports/alerts.md)

* **启用审核日志** — 激活审核日志记录以跟踪对资源的所有操作以实现合规性和故障排除。 [了解详情](../privacy/audit-logs.md)

* **监测集成** — 跟踪自定义操作性能和外部系统连接，以便及早发现集成问题。 [了解详情](../action/reporting.md)

**可投放性监视：**

* **定期查看禁止列表**&#x200B;以了解地址被阻止的原因并维护列表卫生。 [了解详情](../reports/suppression-list.md)

* **分析投放错误**&#x200B;以诊断故障并采取纠正措施。 [了解详情](../configuration/email-error-types.md)

* **遵循DMARC、SPF和DKIM的最佳实践**&#x200B;以最大限度地提高收件箱放置效果。 [了解详情](../reports/deliverability.md)

## 后续步骤：访问您的跟踪数据 {#access-tracking-data}

配置跟踪后，您可以通过Journey Optimizer的内置报告功能访问您的数据：

* **实时监控** — 将实时量度作为历程和营销活动执行查看，以快速识别问题
* **历史分析** — 分析过去的绩效，了解趋势并优化未来的营销活动
* **高级分析** — 连接到Customer Journey Analytics以进行复杂的跨渠道分析和归因建模

[开始使用报告](../reports/gs-reports.md) | [了解Customer Journey Analytics集成](../reports/cja-ajo.md)

## 探索关键主题 {#explore-topics}

<table style="table-layout:fixed">
<tr style="border: 0;">
  <td>
    <a href="../building-journeys/success-metrics.md">
    <img alt="量度" src="../assets/do-not-localize/success-metrics.jpeg">
    </a>
    <div>
    <a href="../building-journeys/success-metrics.md"><strong>配置成功量度</strong></a>
    </div>
    <p>
    <em>跟踪与您的业务目标相一致的自定义KPI</em>
    <p>
  </td>
  <td>
    <a href="../reports/deliverability.md">
    <img alt="可投放性" src="../assets/do-not-localize/deliverability.jpeg">
    </a>
    <div>
    <a href="../reports/deliverability.md"><strong>监测可投放性</strong></a>
    </div>
    <p>
    <em>确保您的邮件送达客户收件箱</em>
    <p>
  </td>
  <td>
    <a href="../reports/gs-reports.md">
    <img alt="报告" src="../assets/do-not-localize/reporting.jpeg">
    </a>
    <div>
    <a href="../reports/gs-reports.md"><strong>浏览报告</strong></a>
    </div>
    <p>
    <em>访问您的历程和营销活动的实时和历史报告</em>
    <p>
  </td>
</tr>
</table>

