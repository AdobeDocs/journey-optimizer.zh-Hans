---
solution: Journey Optimizer
product: journey optimizer
title: 从您的目标开始 |Adobe Journey Optimizer
description: 探索Adobe Journey Optimizer设计的核心用例，并提供关于哪些AJO功能最适合各种情景的指导。
feature: Get Started
topic: Content Management
role: User
level: Beginner
keywords: journey optimizer，用例，决策指南，哪些功能，入门，从业者目标，教程
source-git-commit: 49146a29a474a240ca1fdb10b2a6ef175f44f595
workflow-type: tm+mt
source-wordcount: '3141'
ht-degree: 31%

---

# 从您的目标开始 {#ajo-use-case-guide}

>[!BEGINSHADEBOX]

**在此页面上：**&#x200B;从您希望完成的任务开始，然后跳转到可解决该问题的Adobe Journey Optimizer功能 — 无需首先知道功能名称。

>[!ENDSHADEBOX]

[!DNL Adobe Journey Optimizer]提供了许多功能，而正确的一点取决于您尝试实现的目标。 本指南按业务目标而非产品功能组织：查找符合您需求的目标，然后按照链接开始使用推荐的功能。

使用此页作为快速路由器 — 扫描您的目标并直接跳至正确的功能。 如果您刚刚入门，请从[Journey Optimizer入门](../../rp_landing_pages/get-started-landing-page.md)开始，找到适合您角色的入口点。

>[!NOTE]
>
>有关逐步实现示例，请参阅[历程用例库](../building-journeys/jo-use-cases.md)。

如果某个端到端教程不适用于特定场景，则链接会将您带到当前的最佳起点，帮助您了解该功能并开始学习。

AI内置到其中许多功能中 — 请在下表中查找&#x200B;**(AI)**&#x200B;标记。 对话式[AI助手](ai-features.md#ai-assistant)还可以随时回答有关您历程的产品问题和表面操作见解。 有关完整的智能功能集，请参阅[AI和智能功能](ai-features.md)。

>[!TIP]
>
>初次使用Journey Optimizer？ 从[开始使用Journey Optimizer](../../rp_landing_pages/get-started-landing-page.md)为您的角色选择正确的路径，然后阅读[Journey Optimizer是什么](get-started.md)对于要点。 若要建立实践置信度，请浏览[Journey Optimizer教程](https://experienceleague.adobe.com/zh-hans/docs/journey-optimizer-learn/tutorials/overview){target="_blank"}，观看专家策划的[视频播放列表](https://experienceleague.adobe.com/en/playlists?solution=Journey+Optimizer){target="_blank"}，并在[培训沙盒](https://experienceleague.adobe.com/zh-hans/docs/journey-optimizer-learn/configure-a-training-sandbox/introduction-and-prerequisites){target="_blank"}中或[实践挑战](https://experienceleague.adobe.com/zh-hans/docs/journey-optimizer-learn/challenges/introduction-and-prerequisites){target="_blank"}中练习。

## 为您的团队设置Journey Optimizer {#setup-admin}

适用于需要在构建历程或营销活动之前配置环境的管理员和技术用户。

| 我想…… | 推荐的功能 | 从这里开始 |
| --- | --- | --- |
| 在发送之前配置电子邮件、短信或推送渠道 | 渠道配置 | [开始使用渠道配置](../configuration/get-started-configuration.md) |
| 预热新的IP地址以发送电子邮件 | IP预热计划 | [开始使用IP预热功能](../configuration/ip-warmup-gs.md) |
| 设置角色、权限和访问控制 | 访问控制 | [开始使用访问控制](../administration/permissions-overview.md) |
| 跨多个环境或区域工作 | 沙盒 | [使用沙盒](../administration/sandboxes.md) |

## 发生事件时吸引客户 {#engage-real-time}

适用于对发生的客户操作或事件做出反应的场景。

| 我想…… | 推荐的功能 | 从这里开始 |
| --- | --- | --- |
| 自动欢迎新客户或订阅者 | 事件触发的历程 | [历程入门](../building-journeys/journey-gs.md) · [构建历程简介](https://experienceleague.adobe.com/zh-hans/docs/journey-optimizer-learn/tutorials/journeys/introduction-to-building-a-journey){target="_blank"} |

>[!BEGINSHADEBOX]

**在生成之前：**&#x200B;请确保您已(1)将[历程进入事件配置为捕获注册触发器](../event/about-events.md)，(2)为沙盒设置了[电子邮件或推送渠道界面](../configuration/channel-surfaces.md)，以及(3)至少有一个[测试配置文件](../audience/creating-test-profiles.md)可用于在发布之前验证历程。

>[!ENDSHADEBOX]

| 我想…… | 推荐的功能 | 从这里开始 |
| --- | --- | --- |
| 恢复放弃的购物车或浏览会话 | 事件触发的历程 | [开始使用历程](../building-journeys/journey-gs.md) · [放弃的浏览教程](https://experienceleague.adobe.com/zh-hans/docs/experience-platform/rtcdp/use-cases/personalization-insights-engagement/use-cases-luma){target="_blank"} |

>[!BEGINSHADEBOX]

**在生成**&#x200B;之前，您需要(1)一个[行为事件](../event/about-events.md)，用于从Web或移动设备SDK中捕获购物车或浏览操作，(2)一个[等待活动](../building-journeys/wait-activity.md)策略已决定（通常在第一次轻推之前的1-4个小时），以及(3)一个渠道平面可供后续消息使用。 注意：历程必须包含条件，以退出在等待期结束前完成购买的用户档案。

>[!ENDSHADEBOX]

| 我想…… | 推荐的功能 | 从这里开始 |
| --- | --- | --- |
| 从提交网站表单触发历程 | 事件触发的历程 | [开始使用历程](../building-journeys/journey-gs.md) · [教程](https://experienceleague.adobe.com/zh-hans/docs/journey-optimizer-learn/trigger-journey-on-form-submission/introduction){target="_blank"} |
| 对应用程序内行为（应用程序打开、屏幕查看）做出反应 | 历程+应用程序内 | [应用程序内入门](../in-app/get-started-in-app.md) |
| 发送订单、送货或预约确认 | API触发的营销活动 | [使用API触发的营销活动](../campaigns/api-triggered-campaigns.md) |
| 重新吸引不活跃或失效的客户 | 历程+受众 | [开始使用用户档案和受众](../audience/get-started-profiles.md) · [使用规则生成器创建受众](https://experienceleague.adobe.com/zh-hans/docs/journey-optimizer-learn/tutorials/profiles-audiences-subscriptions/create-audiences-using-the-rule-builder){target="_blank"} |

>[!BEGINSHADEBOX]

**在生成：**&#x200B;之前，您需要(1) Adobe Experience Platform中定义的[受众](../audience/about-audiences.md)来标识非活动配置文件（例如，60天内未购买或登录），(2)有关重新参与渠道（电子邮件、推送或短信）的决定，以及(3)禁止规则或[频率上限](../conflict-prioritization/channel-capping.md)，以避免联系最近发送消息的用户档案。 对此方案使用&#x200B;**读取受众**&#x200B;历程条目 — 不是事件。

>[!ENDSHADEBOX]

| 我想…… | 推荐的功能 | 从这里开始 |
| --- | --- | --- |
| 在激活历程之前，使用真实数据测试历程 | 历程练习 | [试用测试您的历程](../building-journeys/journey-dry-run.md) |
| 暂停实时历程以进行编辑，而不停止飞行中配置文件 | 历程暂停和继续 | [暂停并继续历程](../building-journeys/journey-pause.md) |
| 从自然语言提示符构建或优化历程 | Journey Agent **（人工智能）** | [AI代理](ai-features.md#ai-agents) · [Journey Agent教程](https://experienceleague.adobe.com/zh-hans/docs/journey-optimizer-learn/tutorials/journeys/journey-agent-overview){target="_blank"} |

## 大规模接触受众 {#reach-at-scale}

对于预定的、面向指定受众的一对多外联。

| 我想…… | 推荐的功能 | 从这里开始 |
| --- | --- | --- |
| 向区段发送新闻稿或促销活动 | 计划的营销活动 | [营销活动快速入门](../campaigns/get-started-with-campaigns.md) |

>[!BEGINSHADEBOX]

**在生成**&#x200B;之前，您需要(1) Adobe Experience Platform中的[已发布的受众区段](../audience/about-audiences.md)，(2)具有已验证发送域的[电子邮件渠道界面](../configuration/channel-surfaces.md)，以及(3)您计划重用的任何[内容片段或模板](../content-management/fragments.md)。 如果这是一次性发送或没有分支逻辑的定期发送，则计划的营销活动是这里的正确选择 — 不是历程。

>[!ENDSHADEBOX]

| 我想…… | 推荐的功能 | 从这里开始 |
| --- | --- | --- |
| 通过A/B测试启动产品 | 内容试验&#x200B;**(AI)** | [内容实验入门](../content-management/experiment-accelerator-gs.md) · [为电子邮件营销活动创建内容实验](https://experienceleague.adobe.com/en/docs/journey-optimizer-learn/tutorials/experimentation/content-experiments-for-emails){target="_blank"} |
| 通知客户服务中断或更新 | 计划的活动+受众 | [关于受众](../audience/about-audiences.md) |
| 使用分支逻辑设计多步营销活动 | 编排的营销活动 | [开始使用编排的营销活动](../orchestrated/gs-orchestrated-campaigns.md) |
| 仅定向自上次活动运行以来发生更改的用户档案 | 编排的营销活动 — 增量查询 | [在编排的营销活动中生成查询](../orchestrated/build-query.md) <!-- TODO: verify target — no dedicated "incremental query" page found; build-query.md ("Build your first rule") is the closest existing page --> |
| 在启动之前，检查有多少配置文件与我的受众匹配 | 受众预览 | [关于受众](../audience/about-audiences.md) <!-- TODO: verify target — no "create-compositions.md#preview" page/anchor exists; about-audiences.md used as placeholder --> |
| 大规模协调多个渠道之间的消息传递 | 编排 | [开始使用编排的营销活动](../orchestrated/gs-orchestrated-campaigns.md) · [将编排扩展到全渠道参与](https://experienceleague.adobe.com/zh-hans/docs/journey-optimizer-learn/scaling-orchestration-to-omnichannel-engagement/introduction){target="_blank"} |
| 在每个客户的最佳时间发送每条消息 | 发送时间优化&#x200B;**（人工智能）** | [发送时间优化](../building-journeys/send-time-optimization.md) |

## 将每位客户看到的内容个性化 {#personalize}

用于根据个人情况定制选件和内容。

| 我想…… | 推荐的功能 | 从这里开始 |
| --- | --- | --- |
| 为每位客户显示最佳选件 | 决策 | [开始使用Offer Decisioning](../offers/get-started/starting-offer-decisioning.md) · [Web优惠教程](https://experienceleague.adobe.com/zh-hans/docs/journey-optimizer-learn/use-decisioning-to-personalize-web-offers/introduction){target="_blank"} |

>[!BEGINSHADEBOX]

**生成之前：**&#x200B;决策需要特定的设置顺序。 您需要(1)使用资格规则和属性创建的[决策项（优惠）](../experience-decisioning/items.md)，(2)配置的[选择策略](../experience-decisioning/selection-strategies.md)或排名公式，以及(3)附加到优惠将显示到的表面的[决策策略](../experience-decisioning/create-decision.md)。 跳过此序列是首次决策设置无法返回结果的最常见原因。

>[!ENDSHADEBOX]

| 我想…… | 推荐的功能 | 从这里开始 |
| --- | --- | --- |
| 使用公式对优惠进行排名（邮政编码、收入、天气） | 决策 — 排名公式 | [排名公式](../experience-decisioning/ranking/ranking-formulas.md) · [排名公式教程](https://experienceleague.adobe.com/zh-hans/docs/journey-optimizer-learn/personalizing-offers-with-ranking-formulas-based-on-user-zip-code-and-income/introduction){target="_blank"} · [天气数据教程](https://experienceleague.adobe.com/zh-hans/docs/journey-optimizer-learn/personalizing-offers-with-real-time-weather-data/introduction){target="_blank"} |
| 使用外部产品或CRM数据使优惠个性化 | 决策 — AEP数据集查找 | [在决策中使用数据集查找](../experience-decisioning/context-data.md) |
| 根据用户档案数据定制消息内容 | 个性化 | [个性化您的内容](../personalization/personalize.md) |
| 生成副本、图像和消息变体 | AI内容生成&#x200B;**(AI)** | [AI内容生成](../content-management/gs-generative.md) · [教程](https://experienceleague.adobe.com/zh-hans/docs/journey-optimizer-learn/tutorials/content-management/ai-assistant/ai-assistant-for-content-generation-overview){target="_blank"} |
| 将设计图像转换为可编辑的电子邮件模板 | 图像到HTML转换器&#x200B;**(AI)** | [将图像转换为电子邮件模板](../content-management/image-to-html.md) |
| 自动排名和个性化优惠 | AI排名模型&#x200B;**(AI)** | 用于决策的[AI模型](../experience-decisioning/ranking/ai-models.md) |
| 提供始终在线的上下文内容（无营销活动） | 内容卡 | [开始使用内容卡](../content-card/get-started-content-card.md) · [创建内容卡](https://experienceleague.adobe.com/zh-hans/docs/journey-optimizer-learn/tutorials/channels/content-cards/create-content-cards){target="_blank"} |
| 通过API向任何应用程序或表面交付个性化内容 | 基于代码的体验 | [开始使用基于代码的体验](../code-based/get-started-code-based.md) |
| 控制我的团队可以编辑电子邮件模板的哪些部分 | 内容锁定 | [锁定电子邮件模板中的内容](../content-management/content-locking.md) |

## 协调并管理投放 {#coordinate-govern}

用于控制跨渠道联系客户的方式、时间和频率。

| 我想…… | 推荐的功能 | 从这里开始 |
| --- | --- | --- |
| 防止各渠道出现消息疲劳 | 频率上限 | [按渠道设置频率封顶](../conflict-prioritization/channel-capping.md) |
| 解决冲突或冲突的消息 | 冲突优先级 | [识别潜在冲突](../conflict-prioritization/conflicts.md) · [教程](https://experienceleague.adobe.com/zh-hans/docs/journey-optimizer-learn/tutorials/conflict-management/identify-potential-conflicts){target="_blank"} |
| 确定哪个历程优先 | 历程仲裁 | [使用公式对历程进行排名](../conflict-prioritization/journey-ranking-formulas.md) |
| 尊重安静时间和同意 | 安静时间/隐私 | [设置安静时间](../conflict-prioritization/quiet-hours.md) |
| 跨渠道实施同意策略和数据使用标签 | 同意和数据治理 | [隐私入门](../privacy/get-started-privacy.md) |
| 当历程出现高错误或丢弃率时收到警报 | 历程警报 | [设置历程警报](../reports/alerts.md) |

## 选择要投放的渠道 {#choose-channel}

| 我想发送…… | 渠道 | 从这里开始 |
| --- | --- | --- |
| 电子邮件新闻稿、促销或事务型消息 | 电子邮件 | [电子邮件入门](../email/get-started-email.md) |
| 移动推送通知（iOS和Android） | 推送 | [推送通知入门](../push/get-started-push.md) |
| 短信、彩信或RCS短信 | 短信/彩信/RCS | [开始使用SMS/MMS/RCS](../mobile/get-started-mobile.md) · [移动学习中心](https://experienceleague.adobe.com/zh-hans/docs/journey-optimizer-learn/mobile-learning-hub/overview){target="_blank"} |
| 通过Meta Cloud API发送WhatsApp消息 | WhatsApp | [开始使用 WhatsApp](../whatsapp/get-started-whatsapp.md) |
| 浏览器内或应用程序内叠加和横幅 | 应用程序内 | [应用程序内入门](../in-app/get-started-in-app.md) |
| 个性化网页内容 | Web | [开始使用Web渠道](../web/get-started-web.md) |
| 任何通过API的表面（信息亭、连接的设备、Headless应用程序） | 基于代码的体验 | [开始使用基于代码的体验](../code-based/get-started-code-based.md) |
| 从历程触发的实体邮件 | 直邮 | [直邮入门](../direct-mail/get-started-direct-mail.md) |

## 衡量和优化 {#measure-optimize}

用于跟踪性能、诊断问题并随时间改进结果。

| 我想…… | 推荐的功能 | 从这里开始 |
| --- | --- | --- |
| 查看实时历程或营销活动的绩效指标 | 实时报告 | [实时报告](../reports/live-report.md) · [使用实时报告监视和分析您的历程](https://experienceleague.adobe.com/zh-hans/docs/journey-optimizer-learn/tutorials/report-and-monitor/monitor-and-analyze-your-journey-with-live-reports){target="_blank"} |
| 报告营销活动或旅程结束后的完整执行情况 | 全局报告 | [开始使用报告](../reports/gs-reports.md) |
| 分析试验并获得下一步建议 | Experimentation Agent **（人工智能）** | [Experimentation Agent](ai-features.md#experimentation-agent) · [教程](https://experienceleague.adobe.com/zh-hans/docs/journey-optimizer-learn/tutorials/experimentation/experimentation-agent-overview){target="_blank"} |
| 监测我的历程中自定义操作的运行状况和延迟 | 自定义操作监控 | [使用自定义操作](../building-journeys/using-custom-actions.md) <!-- TODO: verify target — no dedicated "custom-action-monitoring.md" page found; using-custom-actions.md is the closest existing page --> |
| 当历程错误或丢弃率超过阈值时收到警报 | 历程警报 | [设置历程警报](../reports/alerts.md) |

## 入门流程 {#starter-flows}

下面的每个入门流程都是一组简短的、以结果为导向的步骤：您将构建什么、为谁构建以及如何实现目标。 选择与您的第一个项目匹配的目标，然后访问指向详细文档的链接。

### 欢迎新客户 {#flow-welcome}

**您将生成：**自动欢迎系列，该系列会向每个新订阅者问候并推播不活动的订阅者。
**最适合于：**&#x200B;营销人员· **功能：**&#x200B;事件触发的历程

1. 确认您的[统一用户档案和受众](../audience/get-started-profiles.md)正在接收注册事件。
1. [创建您的第一个历程](../building-journeys/journey-gs.md)并将注册事件用作条目。
1. 为尚未参与的用户档案添加欢迎[电子邮件](../email/get-started-email.md)，然后添加等待步骤和跟进[推送通知](../push/get-started-push.md)。
1. [使用个人资料属性（如名字和声明的兴趣）个性化内容](../personalization/personalize.md)。

➡️ [开始历程](../building-journeys/journey-gs.md)

### 恢复放弃的购物车 {#flow-cart}

**您将生成：**自动恢复流程，提醒客户留下的项目。
**最适合于：**&#x200B;营销人员· **功能：**&#x200B;事件触发的历程

1. 确保将放弃购物车事件发送到Journey Optimizer（如果需要，请与您的[数据团队](../data/gs-data.md)合作）。
1. [生成由放弃事件触发的历程](../building-journeys/journey-gs.md)。
1. 发送个性化提醒电子邮件；如果在24小时内没有点击，则分支到[推送](../push/get-started-push.md)跟进。
1. 使用放弃的项目和忠诚度状态[个性化](../personalization/personalize.md)。

➡️ [开始历程](../building-journeys/journey-gs.md)

### 发送事务型消息 {#flow-transactional}

**您将生成：**由外部系统触发的按需订单、送货或约会确认。
**最适合于：**&#x200B;营销人员和开发人员· **功能：**&#x200B;由外部系统触发的营销活动

1. 查看由外部系统](../campaigns/api-triggered-campaigns.md)触发的[营销活动的工作方式以及它们期望的有效负载。
1. 设计邮件模板并[使用事务详细信息对其进行个性化](../personalization/personalize.md)。
1. 让您的开发人员从您的订单或履行系统调用活动端点。

➡️ [使用由外部系统触发的营销活动](../campaigns/api-triggered-campaigns.md)

### 通过内容测试启动营销活动 {#flow-campaign}

**您将生成：**自动选择表现最佳内容的计划促销活动。
**最适合：**&#x200B;营销人员· **功能：**&#x200B;计划的营销活动+内容试验

1. [开始使用营销活动](../campaigns/get-started-with-campaigns.md)并定义您的受众。
1. 使用[内容生成](../content-management/gs-generative.md)来草稿主题行和复制变体。
1. 设置[内容试验](../content-management/experiment-accelerator-gs.md)以测试样本上的变体，然后将入选者发送给其余人。

➡️ [营销活动入门](../campaigns/get-started-with-campaigns.md)

### 根据客户个性化优惠 {#flow-offers}

**您将生成：**一个向每位客户显示单个最佳优惠的决定。
**最适合于：**&#x200B;营销人员· **功能：**&#x200B;决策

1. [开始使用Offer Decisioning](../offers/get-started/starting-offer-decisioning.md)，并创建优惠和资格规则。
1. 将决策添加到[历程](../building-journeys/journey-gs.md)或营销活动消息。
1. [智能功能](ai-features.md)中的层可自动对优惠进行排名和优化。

➡️ [开始使用Offer Decisioning](../offers/get-started/starting-offer-decisioning.md)

## 示例场景 {#example-scenarios}

这些示例说明 Journey Optimizer 的功能如何在不同的角色、行业和渠道中协同工作。

### 延迟发货恢复 {#scenario-delayed-shipment}

**角色：**&#x200B;营销人员 | **核心功能：**[统一轮廓 + 受众排除](../audience/get-started-profiles.md)

一家服装店通常会向过去一周内购买过产品的所有顾客发送购买后调查问卷。 由于天气恶劣，少数货物的交付出现延误。 服装店知道哪些客户尚未收到其货物，就可以将这些客户排除在计划的客户满意度调查之外，并另外发送一封个性化电子邮件，为延迟道歉并根据客户过去的购买情况提供折扣代码和产品推荐。

[营销活动快速入门](../campaigns/get-started-with-campaigns.md)

### 实时店内参与 {#scenario-instore}

**角色：**&#x200B;营销人员 | **核心功能：**[地理围栏触发 + 推送](../push/get-started-push.md)

同一retailer可以通过向进入商店停车场的忠实客户发送一条符合其尺码的毛衣有现货的推送通知来吸引他们。

[推送通知快速入门](../push/get-started-push.md)

### 放弃购物车订单挽回 {#scenario-cart}

**角色：**&#x200B;营销人员 | **核心功能：**[事件触发的多步历程](../building-journeys/journey-gs.md)

当客户将商品添加到在线购物车但未完成购买就离开时，Journey Optimizer会检测该事件并自动开始恢复历程。 客户会收到一封个性化电子邮件，提醒他们有哪些未完成购买的商品。 如果他们在 24 小时内未点击进入，则会发送后续推送通知 - 根据他们的浏览历史记录和忠诚度状态进行个性化定制。

[构建您的首个历程](../building-journeys/journey-gs.md)

### 流媒体服务欢迎系列 {#scenario-welcome}

**角色：**&#x200B;营销人员 | **核心功能：**[事件触发的欢迎历程](../building-journeys/journey-gs.md)

当客户订阅流媒体服务时，Journey Optimizer 会检测到注册事件并立即启动多步骤欢迎历程。 客户会收到一封欢迎电子邮件，鼓励他们首次打开应用程序。 如果在 48 小时内未检测到登录活动，则会发送后续推送通知，其中包含根据用户注册期间声明的兴趣提供个性化内容建议 - 从第一天起就将被动订阅者转变为参与活跃的用户。

[构建您的首个历程](../building-journeys/journey-gs.md)

### 带说明的预订提醒 {#scenario-reservation}

**角色：**&#x200B;营销人员 | **核心功能：**[计划 + 位置感知消息](../campaigns/get-started-with-campaigns.md)

一家酒店品牌会在每位客人预订时间前一小时，及时向他们发送提醒。 通知包括客人姓名、预订时间以及基于位置的达到路线 - 自动根据客户个人资料和预订数据拼合，无需营销团队手动操作。

[营销活动快速入门](../campaigns/get-started-with-campaigns.md)

### 主动服务中断通知 {#scenario-outage}

**角色：**&#x200B;运营 | **核心功能：**[大规模自动受众选择](../audience/about-audiences.md)

当发生服务中断时，Journey Optimizer 会根据客户的帐户数据和使用模式自动识别受影响的客户。 这些客户会收到主动通知，确认问题并说明后续步骤 - 将潜在的负面体验转化为大规模提供的透明度和信任时刻。

[构建您的首个历程](../building-journeys/journey-gs.md)

### 智能促销活动 {#scenario-ai-campaign}

**角色：**&#x200B;营销人员 | **核心功能：** [内容生成+试验](ai-features.md)

一个计划推出新品的零售品牌使用 Journey Optimizer 的 AI 助手在几分钟内生成多个主题行和正文变体，并遵循自然语言提示及其上传的品牌准则。 内置内容试验会自动在初始受众样本中识别表现最佳的变体。 然后，入选消息将部署到其余收件人，无需额外的撰稿工作即可最大程度地提高参与度。

[浏览智能功能](ai-features.md) | [了解内容试验](../content-management/experiment-accelerator-gs.md)

### 通过移动应用程序发送维护警报 {#scenario-maintenance}

**角色：**&#x200B;运营 | **核心功能：**[非营销历程编排](../building-journeys/journey-gs.md)

非营销人员（如运营团队和客户支持人员）可以使用[!DNL Adobe Journey Optimizer]管理运营通知或监控客户加入流程。 例如，在一个游客需要下载移动应用程序作为体验一部分的游乐园中：维护人员可以使用 Journey Optimizer 通知游客哪些游乐设施因维护而暂时关闭。

[构建您的首个历程](../building-journeys/journey-gs.md)

## 视频库 {#videos}

按主题浏览策划的视频内容。 每个选项卡都链接到Experience League上的相关教程和播放列表。

>[!BEGINTABS]

>[!TAB 快速入门]

* [Journey Optimizer简介](https://experienceleague.adobe.com/zh-hans/docs/journey-optimizer-learn/tutorials/introduction-to-journey-optimizer/introduction){target="_blank"} — 核心概念和产品导览。
* [Journey Optimizer教程概述](https://experienceleague.adobe.com/zh-hans/docs/journey-optimizer-learn/tutorials/overview){target="_blank"} — 指导视频的完整目录。

>[!TAB 历程和营销活动]

* [构建历程简介](https://experienceleague.adobe.com/zh-hans/docs/journey-optimizer-learn/tutorials/journeys/introduction-to-building-a-journey){target="_blank"} — 构建您的第一个事件触发历程。
* [使用Journey Agent构建历程](https://experienceleague.adobe.com/zh-hans/docs/journey-optimizer-learn/tutorials/journeys/journey-agent-overview){target="_blank"} — 从自然语言提示创建历程。

>[!TAB Personalization和智能]

* [用于生成内容的AI助手](https://experienceleague.adobe.com/zh-hans/docs/journey-optimizer-learn/tutorials/content-management/ai-assistant/ai-assistant-for-content-generation-overview){target="_blank"} — 生成副本、图像和变体。
* [使用Decisioning个性化Web优惠](https://experienceleague.adobe.com/zh-hans/docs/journey-optimizer-learn/use-decisioning-to-personalize-web-offers/introduction){target="_blank"} — 根据客户定制优惠。

>[!TAB 报告和优化]

* [使用实时报告监视和分析您的旅程](https://experienceleague.adobe.com/zh-hans/docs/journey-optimizer-learn/tutorials/report-and-monitor/monitor-and-analyze-your-journey-with-live-reports){target="_blank"} — 在旅程运行时跟踪性能。
* [为电子邮件营销活动创建内容实验](https://experienceleague.adobe.com/en/docs/journey-optimizer-learn/tutorials/experimentation/content-experiments-for-emails){target="_blank"} — 测试和优化内容。

>[!ENDTABS]

## 在历程、营销活动和编排的营销活动之间选择 {#choosing}

| 场景 | 使用 |
| -------- | --- |
| 行为导向的多步走制，每位客户按自己的步调行动 | 历程 |
| 向受众发送简单的计划消息或API触发的消息 | 促销活动 |
| 具有多实体分段的复杂批处理工作流 | 编排的营销活动 |

## 不确定？ {#not-sure}

如果您的目标映射到您不熟悉的术语，或您不确定表指向的功能，请从[Journey Optimizer关键术语](terminology.md)页面开始，以阐明每个功能背后的概念。

您还可以通过[Journey Optimizer教程](https://experienceleague.adobe.com/zh-hans/docs/journey-optimizer-learn/tutorials/overview){target="_blank"}中的端到端练习来建立实践信心。
