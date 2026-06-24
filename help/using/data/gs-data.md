---
solution: Journey Optimizer
product: journey optimizer
title: Journey Optimizer 中的数据管理快速入门
description: 了解数据如何流入和流出 Adobe Journey Optimizer，包括关键概念、设置步骤和护栏。
feature: Data Management
role: Developer, Admin, User
level: Beginner, Intermediate
exl-id: 25519acb-a017-446a-992b-653d3a8a3d96
TQID: https://experienceleague.adobe.com/Dq8mzkfuxvcoAPI1vjq9lFHjz4Z5j9s42-kfMy59PeI
product_v2: id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2: id: aeebb91a-f216-4d5f-8da1-3a7e6f696ed0
subfeature_v2: id: a1cdc218-59b7-4eef-b5cf-2a7ad74b3371id: d6e5c7fd-c1d6-4137-98cd-138ccde6752fid: cf3fbcd7-c075-4ae4-8de5-96e736ab2ea3id: e30b0a1a-b594-47b8-af94-1e3a2be6df11
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554
level_v2: id: b5a62a22-46f7-4f0d-b151-3fc640bef588
topic_v2: id: bce87dde-a4ab-44c9-8a18-ad66e4ddb377id: c7d04a2c-412a-4c9d-9d7a-4456eaa5adebid: cc72dcf1-72e1-48cc-b434-e7c27d62d67cid: d095671a-1355-40aa-8b5f-06c33c68080bid: ebde5b41-29c9-4f5e-9ef6-1197e85409e3id: f4e6943a-c91a-4134-a2c7-f4f20cfff2f0
source-git-commit: 79b0c44fffb4297a9a5675200f086c5de544ec88
workflow-type: tm+mt
source-wordcount: 2696
ht-degree: 96%

---

# 数据管理快速入门 {#about-data}

>[!BEGINSHADEBOX]

**在此页面上：**&#x200B;获取有关数据如何进出Adobe Journey Optimizer的实际概述，包括架构、数据集、身份、配置文件和数据源，以便您的团队可以在构建历程和营销活动之前完成数据准备步骤。

>[!ENDSHADEBOX]

数据是您通过 [!DNL Adobe Journey Optimizer] 交付的每个历程、决策和消息的基础。

本页面提供了一个实用的入门起点，帮助您了解以下内容：

* Journey Optimizer 使用的核心数据构建块（架构、数据集、身份标识、轮廓）
* Journey Optimizer 如何使用 Adobe Experience Platform 数据
* 在构建历程和营销活动之前，您的团队必须完成哪些数据设置步骤
* 有关详细配置和最佳做法的后续指引

请与您的数据工程师、管理员和营销人员一起使用本指南，以便大家对数据如何流入和流出 Journey Optimizer 形成共同的认识。

>[!TIP]
>刚开始接触 Journey Optimizer 中的数据管理？ 观看[设置数据概述教程](https://experienceleague.adobe.com/zh-hans/docs/journey-optimizer-learn/tutorials/data-management/set-up-data-overview){target="_blank"}，了解适合初学者的有关架构、数据集和源的实用分步指导。

## Journey Optimizer 如何使用 Adobe Experience Platform 数据 {#aep-data}

[!DNL Adobe Journey Optimizer] 是基于 [!DNL Adobe Experience Platform] 构建的。 它不维护单独的、隔离的数据存储。 相反，它使用与其他[!DNL CX Enterprise]应用程序相同的数据基础。

架构和数据集均驻留在 Adobe Experience Platform 中。 身份标识和[实时客户轮廓](../audience/get-started-profiles.md)由身份标识服务和轮廓服务管理。 Journey Optimizer 从 Adobe Experience Platform 中读取轮廓和事件数据以评估历程条件、个性化消息并选择产品建议。 它将交互数据（例如发送、打开、点击和退回事件，以及历程步骤事件）写回到 Experience Platform 数据集。 它还可以在运行时查找其他数据集，而无需将该数据复制到轮廓中。

>[!TIP]
>可以将 Adobe Experience Platform 视为中心数据层，而将 Journey Optimizer 视为使用该共享数据基础来编排历程和消息的应用程序。

➡️[详细了解 Journey Optimizer 架构](https://experienceleague.adobe.com/zh-hans/docs/journey-optimizer/using/get-started/essentials/understanding-ajo#architecture-details){target="_blank"}

## Journey Optimizer 中的关键数据概念 {#key-concepts}

在 Journey Optimizer 中处理数据时，您将遇到几个相关概念。 下表为您提供了快速概览；后面的部分将更详细地解释每个概念。

| 概念 | 内容 | 在 Journey Optimizer 中的主要用途 |
|---|---|---|
| XDM 架构 | 用于表示、验证和格式化数据的规则（由类别 + 字段组构建而成） | 对轮廓属性和行为事件进行建模 |
| 数据集 | 用于符合架构的数据的存储表 | 保留轮廓、事件和系统生成的数据 |
| 源连接器 | 以流式或批量的方式将外部系统中的数据传输到 AEP 中 | 摄取 CRM、分析和 Web 数据 |
| 数据源 | 在历程中公开 AEP 或外部字段 | 支持历程条件和消息个性化 |
| 身份标识 | 唯一代表单个客户的标识符 | 跨渠道拼合轮廓 |
| 查找数据集 | 对 AEP 数据的运行时引用，不进行轮廓存储 | 使用实时参考数据扩充消息 |

### 架构（XDM 架构） {#schema}

架构是一组用于表示、验证和格式化数据的规则。 它由一个&#x200B;**类**（定义基本行为：记录型或时间序列型）和可选的&#x200B;**字段组**（用于添加特定字段）组成。 架构是使用 Experience Data Model (XDM) 标准定义的，并且驻留在 Adobe Experience Platform 中。

XDM 的存在是为了解决一个实际问题：同一概念（客户、购买行为、产品）在不同的源系统中有不同的命名和结构。 XDM 提供了一种共享语言，可在单个定义下统一这些概念，而不管数据来自何处。 这使得 Journey Optimizer 能够以一致的方式处理来自 CRM、网站、移动设备应用程序和数据仓库的数据。

在 Journey Optimizer 中，您通常使用 **XDM 个体轮廓**&#x200B;架构来处理客户属性（姓名、偏好设置、同意），使用 **XDM 体验事件**&#x200B;架构来处理行为事件（购买、页面查看、注册）。

➡️[详细了解架构](get-started-schemas.md)

### 数据集 {#dataset}

数据集是用于符合架构的数据的存储和管理结构，可将其视为具有一组已定义的列和行的表。 Journey Optimizer 使用的所有数据都存储在 Adobe Experience Platform 数据集中。 这些数据集可以是轮廓数据集（用于构建实时客户轮廓）、事件数据集（存储行为数据以用于历程和分析），或是 Journey Optimizer 自动创建的用于跟踪、反馈和历程步骤事件的系统数据集。

➡️[详细了解数据集](get-started-datasets.md)

### 源连接器 {#source-connector}

源连接器（也称为&#x200B;**源**）可帮助您将数据从多个系统 – 例如 Adobe Analytics、Adobe Experience Platform Web SDK、云存储（S3、Azure Blob）或 CRM 数据库 – 摄取到 Adobe Experience Platform 中。 除了原始摄取，连接器还支持使用 Experience Platform 服务来构建、标记和增强数据，包括将字段映射到 XDM 架构以及进行数据治理标记。

➡️[详细了解源连接器](../start/get-started-sources.md)

### 数据源 (Journey Optimizer) {#data-source}

Journey Optimizer 中的数据源定义了 Adobe Experience Platform（或外部 API）中的哪些字段会在历程和消息中公开。 在 Journey Optimizer UI 中配置的数据源通常包括内置的 Adobe Experience Platform 数据源（公开实时客户轮廓属性），以及在历程运行时调用的可选外部或自定义数据源，用于进一步扩充数据。 它们用于历程条件、自定义操作和消息个性化。

➡️[详细了解数据源](../datasource/about-data-sources.md)

>[!NOTE]
>[Adobe Experience Platform 术语表](https://experienceleague.adobe.com/zh-hans/docs/experience-platform/landing/glossary){target="_blank"}将“数据源”泛指为数据的来源（CRM、移动设备应用程序等）。 在 Journey Optimizer 中，**数据源**&#x200B;具有特定含义：它是一种 UI 配置，用于控制在历程和消息中公开哪些字段。

### 身份标识和实时客户轮廓 {#identity}

身份标识是唯一代表单个客户的标识符，如 Cookie ID、设备 ID、电子邮件地址或 CRM ID。 身份标识被划分到不同的命名空间（电子邮件、ECID、CRMID）中，并且同一人员的多个身份标识会被拼合到一个统一的身份标识图中。 实时客户轮廓利用该图来维护单个客户的整体视图 – 通过整合来自多个渠道（包括在线、离线、CRM 和第三方来源）的数据。

对于初学者来说，一个关键概念是&#x200B;**轮廓片段**&#x200B;模型。 每次客户在特定的设备或渠道（您的网站、移动设备应用程序、店面）上与您的品牌互动时，该互动就会被记录为轮廓片段：即基于特定接触点的该客户的部分视图。 实时客户轮廓根据共享身份值不断将这些片段拼合在一起，从而构建一个完整、最新的轮廓。 Journey Optimizer 从这一组合而成的轮廓中读取信息，以实时评估条件、选择产品建议并个性化消息。

➡️[详细了解 Journey Optimizer 中的身份标识](../audience/get-started-identity.md)

### 查找数据集 {#lookup-dataset}

借助查找数据集，Journey Optimizer 可在运行时从 Adobe Experience Platform 数据集检索引用或事务性数据，而无需将数据存储在实时客户轮廓中。 这很适合那些经常变动的参考数据（价格、库存、营业时间），或者是处理消息时需要用到、但又不应归入轮廓的事务性数据。 Journey Optimizer 在历程或消息执行期间会基于产品 ID 等键值进行查找。

➡️[详细了解查找数据集](lookup-aep-data.md)

## 数据准备清单 {#checklist}

在营销人员开始构建历程和营销活动之前，您的组织应完成一组数据准备步骤。 这可以确保 Journey Optimizer 在正确的时间以合规的方式使用正确的数据。

>[!NOTE]
>以下步骤涉及多个角色：数据工程师、管理员和营销人员。 使用本清单作为团队共同遵循的计划来准备环境。 步骤 1-4 在 Adobe Experience Platform 中完成；步骤 5-6 在 Journey Optimizer 中配置。

以下六个步骤将指导您完成整个数据设置过程，从身份标识配置到验证数据是否正确流入 Journey Optimizer：

1. 定义您的身份标识策略
1. 针对轮廓和事件数据设计架构
1. 创建启用了轮廓的数据集
1. 从源中摄取数据
1. 在 Journey Optimizer 中配置数据源
1. 验证跟踪、反馈和历程数据集

+++ 定义您的身份标识策略

为您的客户选择一个主要身份标识（例如 ECID、电子邮件或 CRMID），然后在 Adobe Experience Platform 身份标识服务中配置相应的命名空间。 确保启用了轮廓的架构中存在身份标识字段，并验证轮廓是否被正确拼合到身份标识图中。

➡️[详细了解 Journey Optimizer 中的身份标识](../audience/get-started-identity.md)

+++

+++ 针对轮廓和事件数据设计架构

创建 **XDM 个体轮廓**&#x200B;架构以捕获客户属性，例如姓名和联系信息、偏好和兴趣，以及生命周期阶段或同意状态。 创建 **XDM 体验事件**&#x200B;架构以捕获行为和事务性数据，例如 Web 和应用程序事件、购买行为和离线交互。 在适当的情况下，将正确的字段标记为身份标识和轮廓属性。

➡️[详细了解架构](get-started-schemas.md)\
➡️ [配置文件启用计划](https://experienceleague.adobe.com/en/docs/experience-platform/xdm/schema/profile-enablement-planning){target="_blank"}

+++

+++ 创建启用了轮廓的数据集

在 Adobe Experience Platform 中，根据您的 XDM 架构创建数据集，并对任何应为实时客户轮廓提供数据的数据集启用轮廓。 确认 Journey Optimizer 创建的系统生成数据集在数据集工作区中可见。

➡️[详细了解数据集](get-started-datasets.md)\
➡️ [配置文件启用计划](https://experienceleague.adobe.com/en/docs/experience-platform/xdm/schema/profile-enablement-planning){target="_blank"}\
➡️ [管理启用配置文件的架构](https://experienceleague.adobe.com/en/docs/experience-platform/xdm/schema/best-practices#managing-profile-enabled-schemas){target="_blank"}

+++

+++ 从源中摄取数据

为企业系统（例如 Adobe Analytics、Adobe Experience Platform Web SDK 或 CRM 和 POS 平台）配置源连接器，并将传入字段映射到 XDM 架构。 验证数据是否落入正确的数据集，并按预期出现在实时客户轮廓中。

➡️[详细了解源连接器](../start/get-started-sources.md)

➡️[教程：创建数据集并摄取数据](https://experienceleague.adobe.com/zh-hans/docs/journey-optimizer-learn/tutorials/data-management/create-datasets-and-ingest-data){target="_blank"}

+++

+++ 在 Journey Optimizer 中配置数据源

数据源是 Journey Optimizer 特有的概念：它们并不是数据所在的位置，而是用来声明在历程和消息执行期间允许 Journey Optimizer 读取哪些字段的位置。 在历程可以评估“客户是忠诚会员吗？”之类的条件 或者使用名字对消息进行个性化之前，必须通过数据源配置公开相关的轮廓字段。

Journey Optimizer 包含内置的 [Adobe Experience Platform 数据源](../datasource/adobe-experience-platform-data-source.md)，该数据源允许直接访问实时客户轮廓属性。 这涵盖了绝大多数用例：读取用于个性化的轮廓属性或检查同意和偏好设置字段。 您还可以将[外部数据源](../datasource/external-data-sources.md)配置为在历程运行时调用第三方 API – 例如，检索未存储在 Adobe Experience Platform 中的实时忠诚度分数、产品推荐或店面库存水平。

>[!NOTE]
>通过内置的 Adobe Experience Platform 数据源直接访问体验事件数据的方法已被弃用，并正在被逐步禁用。 [了解详情](https://experienceleague.adobe.com/zh-hans/docs/journey-optimizer/using/orchestrate-journeys/journey-use-cases/exp-event-lookup){target="_blank"}。

配置数据源是一项管理任务，可为历程作者和营销人员解锁完整数据层。 字段通过数据源公开后，便可在历程条件生成器、消息个性化编辑器和产品建议决策规则中使用，无需在构建历程时执行任何额外的工程工作。

➡️[详细了解数据源配置](../datasource/about-data-sources.md)

+++

+++ 验证跟踪、反馈和历程数据集

确认 Journey Optimizer 系统生成的数据集在数据集工作区中可用。 运行测试历程和营销活动，然后使用查询编辑器验证是否记录了发送、打开、点击和退回事件，以及是否正确捕获了历程步骤事件和状态。 使用这些数据集进行持续监控、故障排除和历程优化。

➡️[详细了解 Journey Optimizer 中的查询](get-started-queries.md)

+++

## 护栏和数据设计注意事项 {#guardrails}

某些产品护栏和限制可能会影响您设计数据模型和历程的方式。 请尽早查看这些文档，避免后期返工。

>[!IMPORTANT]
>有关最新信息，请始终参考 [Journey Optimizer 护栏和限制](../start/guardrails.md)页面。 以下摘要重点介绍了关键项目，但它们可能会随着时间的推移而变化。

### Journey Optimizer 系统数据集和 TTL {#datasets-ttl}

Journey Optimizer 会创建多个系统生成的数据集，用于跟踪、反馈和历程步骤事件。 自 2025 年 2 月起，会针对其中一些数据集推出生存时间 (TTL) 护栏，这可能会影响为进行分析和故障排除而保留数据的时长。

➡️[详细了解数据集 TTL 护栏](datasets-ttl.md)

### 流式分段和 Journey Optimizer 事件 {#streaming-segmentation}

自 2024 年 11 月 1 日起，流式分段已不再支持来自 Journey Optimizer 跟踪和反馈数据集的发送事件和打开事件。 对于频率上限和疲劳管理等用例，请使用[业务规则](../conflict-prioritization/rule-sets.md)，而不是基于发送/打开事件的流式分段。

➡️[详细了解数据集](get-started-datasets.md)

### 数据集查找和决策 {#lookup-guardrails}

数据集查找适用于频繁变化的属性（库存、定价、天气）或不需要存储在实时客户轮廓中的数据。 在设计查找策略之前，请查看相关文档中的特定于产品的护栏，例如数据集大小限制和查询上限。

➡️ [详细了解查找数据集](lookup-aep-data.md)

## 示例：为欢迎历程准备数据 {#example}

下面的示例展示了本页所述概念如何在一个简单场景中协同工作。

1. 数据工程师创建一个用于客户属性（姓名、电子邮件、忠诚度级别、同意）的 [XDM 个体轮廓架构](get-started-schemas.md)，以及一个用于网站注册事件的 XDM 体验事件架构。
1. 为每个架构创建[启用了轮廓的数据集](get-started-datasets.md)：一个用于 CRM 属性，一个用于注册事件。
1. Web 和移动端团队通过 Adobe Experience Platform Web SDK 流式处理注册事件；而 CRM 数据则通过[源连接器](../start/get-started-sources.md)来摄取。
1. 管理员在 Journey Optimizer 中配置 [Adobe Experience Platform 数据源](../datasource/adobe-experience-platform-data-source.md)，并公开 `profile.person.name.firstName`、`profile.personalEmail.address` 和 `profile.loyaltyTier` 等字段。
1. 营销人员[创建欢迎历程](../building-journeys/journey-gs.md)，该历程侦听注册事件并利用这些轮廓属性对[欢迎电子邮件进行个性化设置](../personalization/personalize.md)。 Journey Optimizer 将发送和打开事件写入跟踪数据集，并将历程进度记录在历程步骤事件数据集中。
1. 开发人员使用[查询编辑器](get-started-queries.md)验证事件是否正确流动并分析效果（打开次数、点击次数、发送时间）。 团队根据这些洞察调整历程和内容。

此流程展示了在完整的、适合初学者的用例中，架构、数据集、源、数据源和查询是如何协同工作的。

## 相关资源 {#related-resources}

:::: landing-cards-container

:::
![icon](https://cdn.experienceleague.adobe.com/icons/code-branch.svg)

**架构快速入门**

了解如何在 Adobe Experience Platform 中创建 XDM 架构，选择正确的类和字段组，并对轮廓属性和行为事件进行建模。

[了解详情](get-started-schemas.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/database.svg)

**使用数据集**

了解如何创建启用了轮廓的数据集和事件数据集，如何监测数据摄取，并探索 Journey Optimizer 为跟踪、反馈和历程步骤事件自动创建的系统生成数据集。

[了解详情](get-started-datasets.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/gear.svg)

**配置数据源**

提供的分步指南说明了如何设置内置 Adobe Experience Platform 数据源和可选的外部数据源，以在历程中公开轮廓字段和外部 API 响应。

[了解详情](../datasource/about-data-sources.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/puzzle-piece.svg)

**使用 Adobe Experience Platform 数据（查找）**

了解如何在运行时使用 AEP 数据集中的引用或事务性数据扩充消息，而无需将数据存储在实时客户轮廓中。

[了解详情](lookup-aep-data.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/chart-line.svg)

**查询快速入门**

使用查询服务分析 Journey Optimizer 数据集，验证事件是否正确流动，并就发送、打开、点击和退回数据构建报告查询。

[了解详情](get-started-queries.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/bullseye.svg)

**轮廓快速入门**

了解实时客户轮廓在 Journey Optimizer 中的工作方式，以及如何在 Platform UI 中浏览、检查和验证各个客户轮廓。

[了解详情](../audience/get-started-profiles.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/circle-play.svg)

**设置数据概述教程**

针对初学者的视频演示，全面讲解 Journey Optimizer 中的数据设置，涵盖模式、数据集和数据源的完整流程。

[观看教程](https://experienceleague.adobe.com/zh-hans/docs/journey-optimizer-learn/tutorials/data-management/set-up-data-overview){target="_blank"}
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/circle-play.svg)

**创建数据集并摄取数据教程**

一个实践式教程，演示如何在 Adobe Experience Platform 中创建数据集和使用源连接器摄取数据，其中包含您在自己的沙盒中操作时可以遵循的分步说明。

[观看教程](https://experienceleague.adobe.com/zh-hans/docs/journey-optimizer-learn/tutorials/data-management/create-datasets-and-ingest-data){target="_blank"}
:::

::::
