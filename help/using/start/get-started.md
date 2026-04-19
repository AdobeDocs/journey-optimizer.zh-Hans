---
solution: Journey Optimizer
product: journey optimizer
title: Journey Optimizer
description: 探索 Adobe Journey Optimizer 的关键功能和用例
feature: Get Started
topic: Content Management
role: User
level: Beginner
keywords: journey optimizer，什么是ajo， adobe journey optimizer，入门，全渠道，个性化，客户历程
exl-id: 956178c0-9985-4ff8-a29e-17dd367ce4d4
source-git-commit: 0a87a3c689d9b623a00f0a3a257e4fe34152945d
workflow-type: tm+mt
source-wordcount: '1467'
ht-degree: 23%

---

# Journey Optimizer 入门 {#cjm-gs}

本页介绍Adobe Journey Optimizer：它的功能、用途、关键功能以及它如何适应Adobe Experience Platform架构。 这是新用户的建议起点。

## 什么是 [!DNL Adobe Journey Optimizer]？{#about-cjm}

[!DNL Adobe Journey Optimizer]是一个企业应用程序，用于跨所有渠道和接触点创建和提供互联、情境式和个性化的客户体验。 它原生构建于[!DNL Adobe Experience Platform]上，并利用统一的实时客户档案、API优先的开放框架、集中式Offer Decisioning和AI/ML功能。 借助Journey Optimizer，品牌商可通过单个应用程序大规模地编排计划营销活动和实时事件触发型通信。 其结果是提高客户忠诚度和存留期价值的有意义的品牌体验。

本指南适用于不熟悉Journey Optimizer的营销从业者、运营团队和管理员。

➡️ [了解 Journey Optimizer](https://experienceleague.adobe.com/docs/journey-optimizer-learn/tutorials/introduction-to-journey-optimizer/introduction.html?lang=zh-Hans){target="_blank"}（视频）


<!--
 Use [!DNL Adobe Journey Optimizer] to build multi-step customer journeys that initiate a sequence of interactions, offers, and messages across channels in real time. This approach ensures customers are engaged at the optimal moments based on their actions and relevant business signals. Learn how to build journeys in [this section](../building-journeys/journey-gs.md).

You can also create audience-based campaigns to send messages.
-->


## 用例 {#use-cases}

这些示例说明了Journey Optimizer的功能如何在不同的角色、行业和渠道中协同工作。

| 用例 | 角色 | 核心功能 |
|----------|------|----------------|
| 延迟装运恢复 | 营销人员 | [统一配置文件+受众排除](../audience/get-started-profiles.md) |
| 实时店内参与 | 营销人员 | [地理围栏触发+推送](../push/get-started-push.md) |
| 购物车放弃回收 | 营销人员 | [事件触发的多步历程](../building-journeys/journey-gs.md) |
| 流媒体服务欢迎系列 | 营销人员 | [事件触发的欢迎历程](../building-journeys/journey-gs.md) |
| 带说明的预订提醒 | 营销人员 | [已计划+位置感知消息](../campaigns/get-started-with-campaigns.md) |
| 主动服务中断通知 | 操作 | [大规模自动选择](../audience/about-audiences.md) |
| AI支持的促销活动 | 营销人员 | [AI内容生成+试验](ai-features.md) |
| 通过移动应用程序发送维护警报 | 操作 | [非营销编排](../building-journeys/journey-gs.md) |

+++**延迟装运恢复（营销人员）**

服装店通常会向上周购买过产品的所有客户发送购买后调查。 由于天气恶劣，少数货物的交付出现延误。服装店知道哪些客户尚未收到其货物，就可以将这些客户排除在计划的客户满意度调查之外，并另外发送一封个性化电子邮件，为延迟道歉并根据客户过去的购买情况提供折扣代码和产品推荐。

[营销活动快速入门](../campaigns/get-started-with-campaigns.md)

+++

+++**实时店内参与（营销人员）**

同一retailer可以通过向进入商店停车场的忠实客户发送一条符合其尺码的毛衣有现货的推送通知，来吸引这些客户。

[推送通知快速入门](../push/get-started-push.md)

+++

+++**购物车放弃恢复（营销人员）**

当客户将商品添加到在线购物车但未完成购买就离开时，Journey Optimizer会实时检测事件并自动开始恢复历程。 客户会收到一封个性化电子邮件，提醒他们留有哪些项目。 如果他们在24小时内未点进，则会发送后续推送通知 — 根据他们的浏览历史记录和忠诚度状态进行个性化。

[构建您的第一个历程](../building-journeys/journey-gs.md)

+++

+++**流媒体服务欢迎系列（营销人员）**

当客户订阅流服务时，Journey Optimizer会检测到注册事件并立即开始多步欢迎历程。 客户会收到一封欢迎电子邮件，鼓励他们首次打开应用程序。 如果在48小时内未检测到登录活动，则会发送后续推送通知，其中根据注册期间用户声明的兴趣提供个性化内容推荐 — 从第一天起，将被动订阅者转变为参与活跃的用户。

[构建您的第一个历程](../building-journeys/journey-gs.md)

+++

+++**带说明的预订提醒（营销人员）**

酒店品牌在每位客人预订前的一小时向其及时发送提醒。 通知包括访客姓名、预订时间以及基于地点的地点地点指示 — 自动从客户个人资料和预订数据拼合，无需营销团队手动操作。

[营销活动快速入门](../campaigns/get-started-with-campaigns.md)

+++

+++**主动服务中断通知（操作团队）**

当发生服务中断时，Journey Optimizer会根据其帐户数据和使用模式自动识别受影响的客户。 这些客户会收到主动通知，确认问题并概述后续步骤 — 将潜在的负面体验转化为大规模提供的透明度和信任时刻。

[构建您的第一个历程](../building-journeys/journey-gs.md)

+++

+++**AI支持的促销活动（营销人员）**

规划产品发布的零售品牌使用Journey Optimizer的AI Assistant在几分钟内生成多个主题行和正文变体，并遵循自然语言提示及其上传的品牌准则。 内置内容试验会自动在初始受众样本中识别表现最佳的变体。 然后，入选消息将部署到其余收件人，无需额外的撰稿工作即可最大程度地提高参与度。

[探索AI和智能功能](ai-features.md) | [了解内容试验](../content-management/experiment-accelerator-gs.md)

+++

+++**通过移动应用程序（运营团队）的维护警报**

非营销人员（如运营团队和客户支持人员）可以使用[!DNL Adobe Journey Optimizer]管理运营通知或监控入门流程。 例如，一个游乐园，其中的访客下载了移动设备应用程序作为其体验的一部分：维护人员可以使用Journey Optimizer将游乐设施当前因维护而关闭的情况通知园内访客。

[构建您的第一个历程](../building-journeys/journey-gs.md)

+++

## 主要功能 {#key-capabilities}

[!DNL Adobe Journey Optimizer] 是一款灵活的、可扩展的应用程序，能够创建并提供贴心且及时的个性化客户体验，可用于任意应用程序、设备或渠道中。

![图表显示了Journey Optimizer的三个核心功能领域：Real-time Customer Insights &amp; Engagement、Modern Omnicchannel Orchestration &amp; Execution以及Intelligent Decisioning &amp; Personalization，所有这些领域都构建于Adobe Experience Platform之上。](assets/ajo-capabilities.png)

主要功能包括：

### 实时客户洞察和参与

集成的用户档案可与来自客户接触点中的所有源头的数据（包括行为、交易、财务和运营数据）相融合，以优化客户当时的个人和情境体验。 [了解用户档案和受众](../audience/get-started-profiles.md)

### 现代全渠道编排和执行

在单个画布上协调和优化1:1客户参与和营销推广的客户历程，以帮助品牌厂商在整个客户生命周期中提供更多价值。 在[!DNL Adobe Journey Optimizer]中设计的客户历程可以是动态的、基于事件的，以帮助品牌厂商对实时信号做出反应，并将这些交互与计划的营销活动联系起来，从而就向客户发送的通信内容、发送时间以及发送渠道做出正确的决策。 嵌入式内容创建工具（包括拖放式可视设计器、可重用模板、内容片段和个性化编辑器）允许团队直接在同一工作流中创作、个性化和管理每个渠道的消息。 [构建您的第一个历程](../building-journeys/journey-gs.md) | [设计您的内容](../../rp_landing_pages/content-management-landing-page.md)

### Intelligent Decisioning和Personalization

品牌厂商可以应用集中化的决策，并采用人工智能和机器学习技术来配置客户体验中的预测洞察，从而更轻松地实现决策的自动化和大规模的体验优化。 决策功能支持通过[!DNL Adobe Journey Optimizer]对跨渠道的优惠进行规模化的集中管理。 [浏览Offer Decisioning](../offers/get-started/starting-offer-decisioning.md) | [发现AI功能](ai-features.md)


## 可用性和许可 {#availability}

本文档介绍Journey Optimizer的当前版本，除非另有说明，否则同时适用于B2C和B2B edition用户。 您的环境中可用的组件和功能取决于您的[权限](../administration/permissions.md)和[许可方案](https://helpx.adobe.com/cn/legal/product-descriptions/adobe-journey-optimizer.html){target="_blank"}。如有任何问题，请联系 Adobe 客户成功经理或 Adobe 代表。

Adobe Experience Cloud 一般隐私准则和程序适用于 [!DNL Journey Optimizer]。[进一步了解 Adobe Experience Cloud 隐私](https://www.adobe.com/cn/privacy/experience-cloud.html){target="_blank"}。


## 架构 {#architecture}

在下图中，了解 [!DNL Adobe Journey Optimizer] 的基本架构、集成点以及 [!DNL Journey Optimizer] 和 [!DNL Experience Platform] 之间的关系。

Adobe Experience Platform 是一个强大、灵活、开放的集中式数据基础平台，可以收集、标准化、管理数据，对数据应用 AI 洞察并整合数据，从而提供贴心且相关的数字化客户体验。

![图表显示Adobe Experience Platform作为基础数据层，其上方有四个本机构建的应用程序：Adobe Real-Time Customer Data Platform、Journey Optimizer、Customer Journey Analytics和Adobe Mix Modeler。 共享服务（如实时客户个人资料、数据管理和身份解析）支持所有四个应用程序。](assets/ajo-aep-architecture-diagram.png){width="70%" zoomable="yes"}

在 Experience Platform 的基础上，以原生方式构建了四个应用程序：Adobe Real-Time Customer Data Platform、Journey Optimizer、Customer Journey Analytics 和 Adobe Mix Modeler。

Journey Optimizer 的核心功能和服务独立于 Adobe Experience Platform 的基本组件，其中包括实时客户轮廓。虽然Journey Optimizer可无缝工作并与Real-Time CDP和Customer Journey Analytics互操作，但它也可以作为独立应用程序独立运行。

![图表显示Journey Optimizer的内部架构及其与Adobe Experience Platform服务的集成点，包括数据摄取、实时客户个人资料、决策引擎以及跨电子邮件、推送、短信和Web的出站渠道投放。](assets/ajo-architecture-diagram.png){width="70%" zoomable="yes"}


### Adobe Journey Optimizer 蓝图

数字体验蓝图提供系统与数据流架构图，助力深入理解 Adobe Experience Platform 与应用程序的集成及实施方式。蓝图通过可视化方式呈现系统间与组件的数据和内容流、操作序列及依赖关系，为 Adobe Experience Platform 及应用程序的用例设计和架构提供决策依据。

查看 [Adobe Journey Optimizer 蓝图](https://experienceleague.adobe.com/zh-hans/docs/blueprints-learn/architecture/architecture-diagrams/customer-journeys/journey-optimizer/journey-optimizer-overview){target="_blank"}。


>[!MORELIKETHIS]
>
>* [启动的关键步骤](quick-start.md) — 面向管理员、营销人员和数据工程师的基于角色的快速入门指南。
>* [数据管理入门](../data/gs-data.md) — 了解如何在Journey Optimizer中摄取、统一和激活数据。
>* [设计历程并发送消息](../building-journeys/journey-gs.md) — 构建您的第一个客户历程并配置渠道操作。
>* [实时报告](../reports/live-report.md) — 实时监控营销活动和历程表现。
>* [Journey Optimizer简介教程](https://experienceleague.adobe.com/zh-hans/docs/journey-optimizer-learn/tutorials/introduction-to-journey-optimizer/introduction){target="_blank"} — 核心Journey Optimizer概念的引导式视频演练。
>* [Journey Optimizer安全概述](https://www.adobe.com/content/dam/cc/en/security/pdfs/AJO_SecurityOverview.pdf) (PDF) — 安全架构、数据保护和合规性详细信息。
>* [Journey Optimizer产品说明](https://helpx.adobe.com/cn/legal/product-descriptions/adobe-journey-optimizer.html){target="_blank"} — 官方许可条款和版本功能细分。
