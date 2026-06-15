---
solution: Journey Optimizer
product: journey optimizer
title: 关键术语
description: Adobe Journey Optimizer中的基本术语和概念
feature: Get Started
role: Admin, Developer, User
level: Beginner
exl-id: 14e72376-87ad-4fae-bf8c-f347109d7903
TQID: https://experienceleague.adobe.com/-aDvt4RUXyf0EnPfFTJkG1CvWgte-1Fr6YaWvgcNNu4
product_v2: id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2: id: d998adac-2f81-400b-a669-d07bb196e4eb
subfeature_v2: id: fdac7813-bd56-47ae-9f6d-fa94ad1c5dee
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: c66ffd68-0f65-42bb-aa23-b4020f12e0bdid: ff6a42d2-313e-452e-93a6-792e4fad9ff8
level_v2: id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2: id: bcc5edb5-84c3-4940-9f84-ed88b6c16274id: d00e9f03-e50b-4162-b143-0c0817c937c2id: e0eb8757-182f-49f3-94a4-1587d16f5094id: fd2e3797-f2ea-4b36-a9af-52acf5e90513
source-git-commit: 46a5a6dc0a3486633a1a71f8bba8a3cd53aaa618
workflow-type: tm+mt
source-wordcount: 1595
ht-degree: 7%

---

# 关键术语 {#key-terminology}

>[!BEGINSHADEBOX]

**在此页面上：**&#x200B;查找基本的Adobe Journey Optimizer术语和概念，以便您能够放心地导航平台并与团队进行有效协作。

>[!ENDSHADEBOX]

本参考指南定义了您在使用Adobe Journey Optimizer时将会遇到的基本术语。 了解这些概念有助于您放心地导航平台并与团队进行有效协作。

对于经常混淆的听起来相似的术语对，例如&#x200B;**决策与决策管理**&#x200B;或&#x200B;**内容卡与应用程序内消息**，请参阅本页底部的[当术语看起来相似时](#disambiguation)。

>[!NOTE]
>
>Adobe Journey Optimizer基于&#x200B;**Adobe Experience Platform**&#x200B;构建。 您将遇到的许多基本概念（例如实时客户个人资料、沙盒、架构和数据集）是Adobe Experience Platform概念，而不是特定于Journey Optimizer的概念。 有关这些术语的定义，请参阅[Adobe Experience Platform术语表](https://experienceleague.adobe.com/docs/experience-platform/landing/glossary.html){target="_blank"}。

## 历程和促销活动术语 {#journey-campaign-terms}

| 术语 | 定义 |
|------|------------|
| **历程** | 一系列相互关联的步骤，可指导客户逐步体验您的品牌。 每个步骤均基于客户操作或时间触发器执行，从而实现顺序的个性化交互。 [了解详情](../building-journeys/journey.md) |
| **Campaign** | 协调的营销操作，通过一个或多个渠道向特定受众提供内容。 与历程不同，活动会同时执行操作。 Journey Optimizer支持三种营销活动类型：**操作营销活动**（计划的批量发送）、**API触发的营销活动**（通过API进行实时事件驱动消息传递）和&#x200B;**编排的营销活动**（带有可视画布的复杂多步骤工作流）。 [了解详情](../campaigns/get-started-with-campaigns.md) |
| **活动** | 触发或推进历程的操作或发生次数。 事件可以是客户操作（购买、放弃购物车）或系统事件（日期/时间、数据更改）。 [了解详情](../event/about-events.md) |
| **频道** | 用于与客户通信的方法：电子邮件、短信、推送通知、应用程序内消息、Web或直邮。 每个渠道都需要进行特定的配置。 [了解详情](../configuration/get-started-configuration.md) |

## 客户和受众术语 {#customer-audience-terms}

| 术语 | 定义 |
|------|------------|
| **受众** | 一组具有共同特征或行为的客户，例如“过去30天内购买过的客户”或“忠诚度计划成员”。 受众用于定位特定的客户区段。 [了解详情](../audience/about-audiences.md) |
| **受众资格** | 客户加入或离开受众时发生的自动过程。 Journey Optimizer可以在用户进入或退出受众时触发操作，从而确保及时且相关的通信。 [了解详情](../building-journeys/audience-qualification-events.md) |
| **可参与受众** | 您可以根据许可协议通过Adobe Journey Optimizer积极联系的客户配置文件数。 这通常是指过去12个月内参与的用户档案。 |
| **测试配置文件** | 虚拟用户档案，用于在发送给真实客户之前测试和预览消息。 测试配置文件有助于验证个性化、内容和历程逻辑。 [了解详情](../audience/creating-test-profiles.md) |

## 内容和个性化术语 {#content-terms}

| 术语 | 定义 |
|------|------------|
| **个性化** | 使用个人资料数据、偏好和行为为个人客户定制内容的过程。 例如，插入客户名称或显示基于浏览历史记录的产品推荐。 [了解详情](../personalization/personalize.md) |
| **内容模板** | 可重复使用的消息设计，可用于多个营销活动和历程，以维护品牌一致性并加快内容创建。 [了解详情](../content-management/content-templates.md) |
| **片段** | 可重复使用的内容块（如页眉、页脚或促销横幅），可用于多种消息，以确保一致性并启用集中更新。 [了解详情](../content-management/fragments.md) |
| **登陆页面** | 独立的网页，客户可以在其中选择加入或选择退出通信、订阅服务或通过在线表单提供信息。 [了解详情](../landing-pages/get-started-lp.md) |
| **内容试验** | A/B测试框架将受众拆分为随机组，并向每个组提供不同的消息变体（内容、主题行或选件），然后根据定义的成功量度识别性能最佳的变体。 [了解详情](../content-management/get-started-experiment.md) |
| **正在试验** | Journey Optimizer中用于测试和优化决策的更广泛功能：内容实验测试营销活动和历程中的消息变体，而决策实验测试提供选择策略。 两者都使用统计分析来确定入选方法。 [了解详情](../content-management/get-started-experiment.md) |

## 决策和优惠条款 {#decision-terms}

| 术语 | 定义 |
|------|------------|
| **决策** | Journey Optimizer中的最新一代决策框架，为新实施推荐。 提供基于架构的项目目录管理、灵活的收集规则、可重用的决策组件和试验功能。 可用于基于代码的体验、推送、短信和电子邮件。 [了解详情](../experience-decisioning/gs-experience-decisioning.md) |
| **决策管理** | Journey Optimizer中的旧版Offer Decisioning功能。 使用集中的营销优惠库和基于规则的决策引擎，将限制条件应用于实时客户档案。 虽然现有实施仍受支持，但新实施应改用Decisioning。 支持电子邮件、应用程序内、推送、短信和直邮。 [了解详情](../offers/get-started/starting-offer-decisioning.md) |
| **选件** | 可以向客户展示的营销消息、折扣或促销。 优惠包括资格规则，用于确定哪些客户可以接收这些优惠。 [了解详情](../offers/offer-library/creating-personalized-offers.md) |
| **决策策略** | 一组规则和策略，用于根据资格、优先级和上限规则等限制确定在什么时间向哪个客户显示哪个优惠。 [了解详情](../experience-decisioning/create-decision.md) |

## 数据和配置条款 {#data-config-terms}

| 术语 | 定义 |
|------|------------|
| **渠道配置** | 用于定义在特定渠道中如何投放消息的设置 — 包括发件人详细信息、子域、IP池和消息类型（营销或事务性）。 以前在以前的文档中称为“表面”或“预设”。 [了解详情](../configuration/channel-surfaces.md) |
| **禁止列表** | 由于硬退回、垃圾邮件投诉或手动添加，自动从邮件投放中排除的电子邮件地址和域的列表。 为了保护可投放性和发件人信誉，阻止向禁止的地址发送。 [了解详情](../reports/suppression-list.md) |

## 冲突和优先级术语 {#conflict-terms}

| 术语 | 定义 |
|------|------------|
| **规则集** | 一组应用于历程和营销策划的命名业务规则，用于管理消息传递行为。 规则集可以将频率封顶、历程进入限制和静默小时合并到一个可重用策略中。 [了解详情](../conflict-prioritization/rule-sets.md) |
| **频率封顶** | 规则集中的规则，用来限制在给定时间段内，每个渠道或通信类型（销售、促销等）用户档案可以接收的消息数。 超出上限的用户档案会自动从投放中排除。 [了解详情](../conflict-prioritization/channel-capping.md) |

## 当术语相似时：消除歧义指南 {#disambiguation}

Adobe Journey Optimizer经历了几年的发展，这意味着一些功能领域有着相似的名字。 使用下表快速确定哪些功能符合您的需求。

### 决策与决策管理 {#decisioning-vs-dm}

这两种功能都选择并提供选件，但它们服务于产品生命周期的不同阶段。

| | 决策 | 决策管理 |
|---|---|---|
| **状态** | 当前 — 建议用于所有新实施 | **旧版** — 仍受支持，但不再建议用于新实施 |
| **项目目录** | 基于架构、灵活的元数据 | 集中式优惠库 |
| **支持的渠道** | 基于代码的体验、推送、短信、电子邮件 | 电子邮件、应用程序内、推送、短信、直邮 |
| **关键区分因素** | 可重复使用的决策组件、实验、更广泛的渠道路线图 | 行之有效的限制引擎；针对新项目迁移到Decisioning |
| **入门** | [决策](../experience-decisioning/gs-experience-decisioning.md) | [决策管理](../offers/get-started/starting-offer-decisioning.md) |

如果您当前正在使用决策管理并且想要切换，请参阅[迁移指南](../experience-decisioning/migrate-to-decisioning.md)。

### 营销活动类型 {#campaign-types-disambiguation}

Journey Optimizer提供三种激活方式不同的营销活动类型，分别用于不同的用例。

| | 操作营销活动（计划的营销活动） | API 触发的营销活动 | 编排的营销活动 |
|---|---|---|---|
| **激活** | 手动或计划 | 外部API调用 | 可视化工作流画布 |
| **最适合** | 一次性或定期批量发送（新闻稿、促销活动） | 实时事件驱动报文传送（订单确认、密码重置） | 复杂的多步骤跨渠道程序 |
| **Personalization源** | 轮廓属性 | 配置文件属性+ API有效负载上下文 | 配置文件属性+关系数据 |
| **入门** | [操作营销活动](../campaigns/create-campaign.md) | [API触发的营销活动](../campaigns/api-triggered-campaigns.md) | [编排的营销活动](../orchestrated/gs-orchestrated-campaigns.md) |

有关所有营销活动类型以及何时使用每种营销活动的完整概述，请参阅[营销活动入门](../campaigns/get-started-with-campaigns.md)。

### 频率上限与历程仲裁 {#capping-vs-arbitration}

两者都是冲突和优先化工具集下的规则集机制，但它们解决的问题不同。

| | 频率上限 | 历程仲裁 |
|---|---|---|
| **它解决的问题** | 随着时间的推移，用户档案会接收太多的消息 | 用户档案同时符合多个历程的条件 |
| **作用域** | 每个渠道和通信类型（销售、促销等） | 历程注册 — 并发旅程数或获胜的旅程 |
| **机制** | 限制每个期间的消息数量；自动排除过度请求的配置文件 | 使用优先级得分和上限规则来确定用户档案进入的历程 |
| **配置于** | 规则集→频率封顶 | 规则集历程上限和仲裁 |
| **了解详情** | [按渠道设置频率封顶](../conflict-prioritization/channel-capping.md) | [管理历程上限和仲裁](../conflict-prioritization/journey-capping.md) |

### 内容卡与应用程序内消息 {#content-cards-vs-in-app}

两个渠道在移动或Web应用程序中传递消息，但它们具有不同的渲染模型和持久性行为。

| | 内容卡 | 应用程序内消息 |
|---|---|---|
| **显示模型** | 嵌入到应用程序UI（信息源、收件箱或自定义表面）中的持久卡片 | 应用程序顶部显示的临时叠加图、横幅或模式 |
| **持久性** | 在显式取消或过期之前保持可见 | 用户交互或关闭后消失 |
| **触发器** | SDK在加载时渲染；规则控制显示和删除 | 历程或活动中的实时事件会触发投放 |
| **最适合** | 持续促销、忠诚度状态、持续警报 | 载入提示、限时优惠、临时通知 |
| **入门** | [内容卡](../content-card/create-content-card.md) | [应用程序内消息](../in-app/get-started-in-app.md) |

>[!NOTE]
>
>**Adobe Journey Optimizer与Journey Optimizer B2B edition：**&#x200B;它们是同一品牌系列中的两个独立产品。 Adobe Journey Optimizer（此文档）面向B2C客户历程。 Journey Optimizer B2B edition专为基于帐户的营销而构建，可与购买组和客户受众合作。 如果要查找B2B edition文档，请访问[Journey Optimizer B2B edition指南](https://experienceleague.adobe.com/zh-hans/docs/journey-optimizer-b2b/user/guide-overview){target="_blank"}。

## 相关主题 {#related-topics}

* [了解Journey Optimizer的工作方式](understanding-ajo.md) — 了解历程、营销活动、用户档案和渠道如何在产品架构中组合。
* [决策功能入门](../experience-decisioning/gs-decision.md) — 并排比较决策和决策管理，选择适合您的实施方法。
* [历程入门](../building-journeys/journey.md) — 了解如何分步构建事件触发的顺序客户体验。
* [营销活动入门](../campaigns/get-started-with-campaigns.md) — 了解三种营销活动类型（操作、API触发、编排）以及何时使用各类型。
* [冲突管理和优先化](../conflict-prioritization/gs-conflict-prioritization.md) — 了解如何使用规则集、频率上限、优先级分数和无讯息小时以避免过度消息传送。
* [通信渠道入门](../channels/gs-channels.md) — 浏览所有可用的渠道、其先决条件以及如何配置它们。
