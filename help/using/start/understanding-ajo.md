---
solution: Journey Optimizer
product: journey optimizer
title: 了解Journey Optimizer
description: 了解Adobe Journey Optimizer如何与Adobe Experience Platform配合使用以提供个性化的客户体验
feature: Get Started
topic: Content Management
role: Admin, Developer, User
level: Beginner
keywords: journey optimizer，工作原理，架构， experience platform，功能领域
exl-id: 9df179a0-a5f6-4dbd-a9db-a103731b1854
TQID: https://experienceleague.adobe.com/E2ksPVFZBggv1RgEri7jx30G2oSanpmNs77vH9Yuq78
product_v2: id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2: id: ad78185d-8f79-40ad-9bad-cbde74af74eeid: b3538224-471e-4c63-a444-9b19d89ae29cid: baecb07f-ce89-4ebb-9cd9-0f7c053f944fid: bb359667-ec7d-4d4b-8663-5850fc219d32id: d556b755-390a-43f0-be32-a08cf6236126id: d998adac-2f81-400b-a669-d07bb196e4ebid: dc22c819-3f29-4e91-8b7d-5c6719831141id: fe338112-e2ce-4876-8989-fc4d497613f1
subfeature_v2: id: af7571a6-3ddb-4c1c-abdf-4d4dde592140id: b32bb433-f8c6-4931-8e52-e657230a3bf2id: c6e980f5-2d4f-494f-beef-186b9ecf1513id: d2e8a157-b3b0-4143-9ff3-809bf400be56id: d595a60b-bcf5-4a63-a189-66a0be755cc7id: fdac7813-bd56-47ae-9f6d-fa94ad1c5dee
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: c66ffd68-0f65-42bb-aa23-b4020f12e0bdid: ff6a42d2-313e-452e-93a6-792e4fad9ff8
level_v2: id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2: id: aa2f3246-cb95-4b30-8899-fdf7d73550ccid: b5520579-b31f-4df7-9281-f0d9f91e2edcid: b5ce8718-c3af-4fdb-a1a9-fca32f83a87cid: bce87dde-a4ab-44c9-8a18-ad66e4ddb377id: c2be0313-b3ae-45e0-b454-d20bf54b23f2id: c7d04a2c-412a-4c9d-9d7a-4456eaa5adebid: cdd65e7e-8839-44a2-bc21-0e03623b5dd1id: d00e9f03-e50b-4162-b143-0c0817c937c2id: d095671a-1355-40aa-8b5f-06c33c68080bid: e0eb8757-182f-49f3-94a4-1587d16f5094id: e1e0219c-f879-479f-8427-888ed2a6e9c2id: ebde5b41-29c9-4f5e-9ef6-1197e85409e3id: eddd9b14-83bd-4ff4-9072-54a4a484abb7id: f4e6943a-c91a-4134-a2c7-f4f20cfff2f0id: fd2e3797-f2ea-4b36-a9af-52acf5e90513
source-git-commit: f9b8e1590f14cdcd00432295c653769f753b9b40
workflow-type: tm+mt
source-wordcount: 957
ht-degree: 3%

---

# 了解Journey Optimizer {#understanding-ajo}

本页介绍Adobe Experience Platform和Journey Optimizer如何协同工作，涵盖持续的数据到体验周期、关键功能领域、架构详细信息和集成点。

Adobe Journey Optimizer和Adobe Experience Platform可协同工作，实现大规模的数据驱动个性化。 此页面介绍这些系统如何运行以及它们的主要功能领域如何相结合以提供卓越的客户体验。 [了解关键功能](get-started.md) | [探索关键术语](terminology.md)

## Journey Optimizer的工作原理 {#how-it-works}

没有统一的数据基础，品牌就不得不依赖多个特定于渠道的工具，这使其难以保持对每个客户的一致视图或实时对其行为采取行动。 Journey Optimizer通过在Adobe Experience Platform的基础上将客户数据、内容创建和历程编排连接到一个连续的系统中来解决此问题。 其结果是打造有意义的品牌体验，进而提高客户忠诚度和实现存留期价值。

Adobe Journey Optimizer作为连续流运行，收集、分析和应用数据以创建个性化的客户历程。

![图表显示Adobe Experience Platform作为基础数据层，Journey Optimizer与Real-Time CDP、Customer Journey Analytics和Adobe Mix Modeler一起构建在顶部，所有服务共享实时客户个人资料、数据治理和身份解析等核心服务。](assets/ajo-aep-architecture-diagram.png)

### Adobe Experience Platform：基础 {#aep-foundation}

Adobe Experience Platform作为骨干，使品牌商能够集中客户数据并激活它以实现个性化体验：

* **Data Platform** — 用于收集、管理和构建客户数据的中心中心，以确保跨系统的一致性。 [了解架构和数据集](../data/get-started-schemas.md)
* **数据摄取（源）** — 使用预建连接器从CRM平台、网站、移动应用程序和云存储导入数据。 [浏览数据源](get-started-sources.md)
* **实时客户个人资料** — 通过合并来自多个来源的数据（电子邮件交互、店内购买、Web行为）来创建统一的个人资料。 [了解用户档案](../audience/get-started-profiles.md)
* **治理层** — 在遵守法规的同时管理数据访问、隐私合规性和安全性。 [查看隐私文档](../privacy/get-started-privacy.md)

### Adobe Journey Optimizer：编排引擎 {#ajo-orchestration}

Adobe Journey Optimizer运用Adobe Experience Platform提供的数据和见解，提供智能、个性化的客户体验：

* **客户了解** — 实时客户配置文件支持按受众细分目标消息传送。 [创建受众](../audience/about-audiences.md)
* **内容和选件** — 内置的可视化设计器、可重用模板和集中式资源库允许团队为任何渠道创作和个性化消息，而无需离开平台。 动态个性化根据客户属性、行为和上下文来调整内容。 然后，实时决策逻辑为每位个人选择最佳选件。 [设计内容](../../rp_landing_pages/content-management-landing-page.md) | [管理资源](../integrations/assets.md) | [管理优惠](../offers/get-started/starting-offer-decisioning.md)
* **历程和营销活动管理** — 自动处理交互（历程）序列或计划一次性定向消息（营销活动）。 [生成历程](../building-journeys/journey-gs.md) | [创建营销活动](../campaigns/get-started-with-campaigns.md)
* **投放（连接）** — 通过电子邮件、短信、推送通知和直邮等渠道发送消息；将数据导出到外部系统。 [配置渠道](../configuration/get-started-configuration.md)
* **测量和分析** — 通过报告跟踪客户参与和促销活动效果，以便持续改进。 [查看报告](../reports/campaign-global-report-cja.md)

### 持续优化周期 {#optimization-cycle}

该生态系统作为一个持续优化周期运行。 数据推动客户了解，从而形成个性化内容和决策。 这些功能经过精心编排为历程，跨渠道交付，进行有效性衡量并随着时间的推移而优化。

![图表显示了Journey Optimizer中的持续优化周期：数据摄取将馈送客户个人资料，这些资料会告知内容和优惠决策、编排到历程中、跨渠道交付、针对性能进行测量并随着时间的推移而优化。](../assets/do-not-localize/get-started-flow.png)

## 主要职能领域 {#functional-areas}

Journey Optimizer包括七个紧密结合的关键功能领域：

| 功能区 | 用途 | 关键活动 |
|-----------------|---------|----------------|
| **数据管理** | 组织客户数据 | 定义架构、创建数据集、从各种系统导入数据。 [了解详情](../data/get-started-schemas.md) |
| **客户管理** | 了解您的客户是谁 | 构建统一的用户档案、解析身份和创建受众。 [了解详情](../audience/get-started-profiles.md) |
| **内容管理** | 创建个性化消息 | 设计电子邮件、管理资产、构建模板和片段、个性化内容。 [了解详情](../../rp_landing_pages/content-management-landing-page.md) |
| **决策管理** | 实时选择最佳选件 | 管理优惠库、定义规则、应用约束、建立排名逻辑。 [了解详情](../offers/get-started/starting-offer-decisioning.md) |
| **历程管理** | 设计自动化客户体验 | 使用可视设计器创建历程、设置触发器、添加条件和等待步骤。 [了解详情](../building-journeys/journey-gs.md) |
| **连接** | 连接数据源和渠道 | 配置源连接器、设置通道、连接到外部平台。 [了解详情](../configuration/get-started-configuration.md) |
| **管理和隐私** | 控制设置和合规性 | 管理用户、配置沙盒、设置渠道和处理隐私请求。 [了解详情](../administration/permissions.md) |

### 这些领域如何协同工作 {#working-together}

这些职能领域以连续的周期运作：

1. **数据摄取** — 数据流入Adobe Experience Platform，由数据管理构建
2. **客户了解** - Real-time Customer Profiles统一数据；客户管理创建受众
3. **内容和优惠策略** — 内容管理创建消息；决策管理定义优惠逻辑
4. **编排** -历程管理使用客户数据、内容和决策映射跨渠道的交互
5. **传递** — 连接有助于通过渠道传递消息或与外部系统共享数据
6. **测量** — 性能数据将分析反馈回以优化受众、内容、决策和历程
7. **治理** — 管理和隐私控制确保整个过程中的合规性

## 架构详细信息 {#architecture-details}

Journey Optimizer是原生构建在Adobe Experience Platform上的四个应用程序之一，另外三个应用程序是Real-Time CDP、Customer Journey Analytics和Adobe Mix Modeler。 它共享AEP的核心服务 — 实时客户档案、身份图、数据治理和查询服务 — 因此它无需单独的集成即可访问统一的客户数据基础。 Journey Optimizer可以作为独立应用程序运行，也可以与其他AEP本机应用程序互操作。

要深入了解技术架构（包括集成模式、先决条件和系统数据流），请参阅[Adobe Journey Optimizer蓝图](https://experienceleague.adobe.com/en/docs/blueprints-learn/architecture/architecture-diagrams/customer-journeys/journey-optimizer/journey-optimizer-overview){target="_blank"}。 有关实施注意事项，[查看护栏和限制](guardrails.md)。

## 隐私和安全性 {#privacy-security}

Adobe Experience Cloud的隐私和安全实践适用于Adobe Journey Optimizer。 这些措施可确保遵守GDPR等隐私法规，从而使您能够提供个性化体验，同时维护客户信任。 [在Journey Optimizer中了解有关隐私的更多信息](../privacy/get-started-privacy.md)
