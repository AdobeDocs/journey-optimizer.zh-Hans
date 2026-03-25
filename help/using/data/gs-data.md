---
solution: Journey Optimizer
product: journey optimizer
title: Journey Optimizer 中的数据管理入门
description: 了解数据如何进出Adobe Journey Optimizer，包括关键概念、设置步骤和护栏。
feature: Data Management
role: Developer, Admin, User
level: Beginner, Intermediate
exl-id: 25519acb-a017-446a-992b-653d3a8a3d96
source-git-commit: 7094cb2717f36042fa0aec1c6442f8d00c593823
workflow-type: tm+mt
source-wordcount: '2442'
ht-degree: 1%

---


# 数据管理入门 {#about-data}

数据是您通过[!DNL Adobe Journey Optimizer]交付的每个历程、决策和消息的基础。

本页为您提供了一个实用的起点，以了解：

* Journey Optimizer使用的核心数据构建块（架构、数据集、身份、配置文件）
* Journey Optimizer如何使用Adobe Experience Platform数据
* 在构建历程和营销活动之前，您的团队必须完成哪些数据设置步骤
* 下一步何处了解详细配置和最佳实践

本指南与您的数据工程师、管理员和营销人员结合使用，让每个人都能共享数据如何进出Journey Optimizer的通用图片。

>[!TIP]
>初次使用Journey Optimizer中的数据管理？ 观看[设置数据概述教程](https://experienceleague.adobe.com/en/docs/journey-optimizer-learn/tutorials/data-management/set-up-data-overview){target="_blank"}，了解适合初学者使用的实际架构、数据集和源演练。

## Journey Optimizer如何使用Adobe Experience Platform数据 {#aep-data}

[!DNL Adobe Journey Optimizer]生成于[!DNL Adobe Experience Platform]。 它不维护单独的、隔离的数据存储。 相反，它使用与其他Experience Cloud应用程序相同的数据基础。

架构和数据集位于Adobe Experience Platform中。 身份和[实时客户配置文件](../audience/get-started-profiles.md)由身份服务和配置文件服务管理。 Journey Optimizer从Adobe Experience Platform中读取配置文件和事件数据以评估旅程条件、个性化消息并选择选件。 它将交互数据（例如发送、打开、点击和退回事件，以及历程步骤事件）写入回Experience Platform数据集。 它还可以在运行时查找其他数据集，而无需将该数据复制到配置文件中。

>[!TIP]
>请将Adobe Experience Platform视为中心数据层，将Journey Optimizer视为使用该共享数据基础来协调历程和消息的应用程序。

➡️ [了解有关Journey Optimizer架构的更多信息](https://experienceleague.adobe.com/en/docs/journey-optimizer/using/get-started/essentials/understanding-ajo#architecture-details){target="_blank"}

## Journey Optimizer中的关键数据概念 {#key-concepts}

在Journey Optimizer中处理数据时，您将遇到几个相关的概念。 下表为您提供了快速概览；后面的部分将更详细地解释每个概念。

| 概念 | 内容 | Journey Optimizer中的主要用途 |
|---|---|---|
| XDM架构 | 表示、验证和格式化数据的规则（从类+字段组构建） | 模型配置文件属性和行为事件 |
| 数据集 | 用于符合模式的数据的存储表 | 保留配置文件、事件和系统生成的数据 |
| Source连接器 | 将外部系统中的数据流式传输或批处理到AEP中 | 摄取CRM、分析和Web数据 |
| 数据源 | 在历程中公开AEP或外部字段 | Power Journey条件和消息个性化 |
| 身份标识 | 唯一代表单个客户的标识符 | 跨渠道拼合用户档案 |
| 查找数据集 | 对AEP数据的运行时引用，不含配置文件存储 | 使用实时参考数据扩充消息 |

### 架构（XDM架构） {#schema}

架构是一组用于表示、验证您的数据并设置其格式的规则。 它由一个&#x200B;**类**（定义基本行为：记录或时间序列）和可选的&#x200B;**字段组**（添加特定字段）组成。 架构使用Experience Data Model (XDM)标准定义并在Adobe Experience Platform中启用。

XDM的存在是为了解决一个真正的问题：同一概念（客户、购买、产品）的名称和结构在源系统中有所不同。 XDM提供了一种共享语言，可在单个定义下统一这些概念，而不管数据来自何处。 这使得Journey Optimizer可同时处理来自CRM、网站、移动设备应用程序和数据仓库的数据。

在Journey Optimizer中，您通常使用客户属性（名称、偏好设置、同意）的&#x200B;**XDM Individual Profile**&#x200B;架构以及行为事件（购买、页面查看、注册）的&#x200B;**XDM ExperienceEvent**&#x200B;架构。

➡️ [了解有关架构的更多信息](get-started-schemas.md)

### 数据集 {#dataset}

数据集是用于符合架构的数据的存储和管理结构 — 可将其视为具有一组已定义的列和行的表。 Journey Optimizer使用的所有数据都存储在Adobe Experience Platform数据集中。 这些数据集可以是配置文件数据集（有助于实时客户配置文件）、事件数据集（存储行为数据以供历程和分析），或Journey Optimizer自动创建的用于跟踪、反馈和历程步骤事件的系统数据集。

➡️ [了解有关数据集的更多信息](get-started-datasets.md)

### Source连接器 {#source-connector}

源连接器（也称为&#x200B;**源**）可帮助您将数据从多个系统(如Adobe Analytics、Adobe Experience Platform Web SDK、云存储(S3、Azure Blob)或CRM数据库)摄取到Adobe Experience Platform中。 除了原始摄取，连接器还支持使用Experience Platform服务来构建、标记和增强数据，包括字段映射到XDM架构和数据治理标记。

➡️ [了解有关源连接器的更多信息](../start/get-started-sources.md)

### 数据源(Journey Optimizer) {#data-source}

Journey Optimizer中的数据源定义Adobe Experience Platform（或外部API）中的哪些字段在历程和消息中公开。 在Journey Optimizer UI中配置的数据源通常包括内置的Adobe Experience Platform数据源（公开实时客户配置文件属性）和在Journey Runtime调用的可选外部或自定义数据源，以进行其他扩充。 它们用于历程条件、自定义操作和消息个性化。

➡️ [了解有关数据源的更多信息](../datasource/about-data-sources.md)

>[!NOTE]
>[Adobe Experience Platform术语表](https://experienceleague.adobe.com/en/docs/experience-platform/landing/glossary){target="_blank"}将“数据源”一般定义为数据的来源（CRM、移动设备应用程序等）。 在Journey Optimizer中，**数据源**&#x200B;具有特定含义：控制历程和消息中公开哪些字段的UI配置。

### Identity和Real-time Customer Profile {#identity}

身份是唯一表示单个客户的标识符，如Cookie ID、设备ID、电子邮件地址或CRM ID。 身份将整理到多个命名空间（电子邮件、ECID、CRMID）中，并且同一人员的多个身份会拼合到一个统一的身份图中。 实时客户配置文件使用该图表通过组合来自多个渠道（包括在线、离线、CRM和第三方来源）的数据来维护每个客户的整体视图。

初学者的一个关键概念是&#x200B;**配置文件片段**&#x200B;模型。 每次客户在特定的设备或渠道（您的网站、移动设备应用程序、商店）上与您的品牌互动时，该互动记录为配置文件片段：基于特定接触点的该客户的部分视图。 Real-time Customer Profile根据共享身份值不断将这些片段拼合在一起，从而构建一个完整、最新的配置文件。 Journey Optimizer从此组合的用户档案中读取，以实时评估条件、选择优惠并个性化消息。

➡️ [了解有关Journey Optimizer中标识的更多信息](../audience/get-started-identity.md)

### 查找数据集 {#lookup-dataset}

借助查找数据集，Journey Optimizer可在运行时从Adobe Experience Platform数据集检索引用或事务性数据，而无需将数据存储在实时客户档案中。 这对于频繁更改在消息时间需要但不属于用户档案的引用数据（价格、库存、存储时间）或事务型数据非常有用。 Journey Optimizer在历程或消息执行期间根据键（如产品ID）执行查找。

➡️ [了解有关查找数据集的更多信息](lookup-aep-data.md)

## 数据准备清单 {#checklist}

在营销人员开始构建历程和营销活动之前，您的组织应完成一组数据准备步骤。 这可确保Journey Optimizer在正确的时间以合规的方式使用正确的数据。

>[!NOTE]
>以下步骤涉及多个角色：数据工程师、管理员和营销人员。 使用此核对清单作为共享计划来准备环境。 步骤1-4在Adobe Experience Platform中完成；步骤5-6在Journey Optimizer中配置。

以下六个步骤将指导您完成完整的数据设置过程，从身份配置到验证数据是否正确流入Journey Optimizer：

1. 定义您的身份策略
1. 设计用户档案和事件数据的架构
1. 创建支持配置文件的数据集
1. 从源中摄取数据
1. 在Journey Optimizer中配置数据源
1. 验证跟踪、反馈和历程数据集

+++ 定义您的身份策略

为您的客户选择一个主要身份（如ECID、电子邮件或CRMID），然后在Adobe Experience Platform Identity Service中配置相应的命名空间。 确保启用配置文件的架构中存在身份字段，并验证配置文件是否正确拼合到身份图中。

➡️ [了解有关Journey Optimizer中标识的更多信息](../audience/get-started-identity.md)

+++

+++ 设计用户档案和事件数据的架构

创建&#x200B;**XDM Individual Profile**&#x200B;架构以捕获客户属性，如姓名和联系信息、偏好和兴趣以及生命周期阶段或同意状态。 创建&#x200B;**XDM ExperienceEvent**&#x200B;架构以捕获行为和交易数据，如Web和应用程序事件、购买和离线交互。 根据需要，将正确的字段标记为身份和配置文件属性。

➡️ [了解有关架构的更多信息](get-started-schemas.md)

+++

+++ 创建支持配置文件的数据集

在Adobe Experience Platform中，根据您的XDM架构创建数据集，并对任何应有助于实时客户个人资料的数据集启用个人资料。 确认Journey Optimizer创建的系统生成数据集在数据集工作区中可见。

➡️ [了解有关数据集的更多信息](get-started-datasets.md)

+++

+++ 从源中摄取数据

为企业系统（如Adobe Analytics、Adobe Experience Platform Web SDK或CRM和POS平台）配置源连接器，并将传入字段映射到XDM架构。 验证数据是否登陆正确的数据集，并在实时客户资料中显示预期的数据。

➡️ [了解有关源连接器的更多信息](../start/get-started-sources.md)

➡️ [教程：创建数据集并摄取数据](https://experienceleague.adobe.com/en/docs/journey-optimizer-learn/tutorials/data-management/create-datasets-and-ingest-data){target="_blank"}

+++

+++ 在Journey Optimizer中配置数据源

数据源是Journey Optimizer特定的概念：它们不是数据所在的位置，而是您声明在历程和消息执行期间Journey Optimizer可以读取哪些字段的位置。 在历程可以评估“客户是忠诚会员吗？”等条件之前 或者使用名字对消息进行个性化，必须通过数据源配置公开相关的用户档案字段。

Journey Optimizer包含内置[Adobe Experience Platform数据源](../datasource/adobe-experience-platform-data-source.md)，该数据源允许直接访问实时客户配置文件属性。 这涵盖了绝大多数用例：读取用于个性化的配置文件属性或检查同意和偏好设置字段。 您还可以将[外部数据源](../datasource/external-data-sources.md)配置为在历程运行时调用第三方API — 例如，检索未存储在Adobe Experience Platform中的实时忠诚度分数、产品推荐或商店库存级别。

>[!NOTE]
>通过内置的Adobe Experience Platform数据源直接访问体验事件数据的方法已被弃用，并正在逐步禁用。 [了解详情](https://experienceleague.adobe.com/en/docs/journey-optimizer/using/orchestrate-journeys/journey-use-cases/exp-event-lookup){target="_blank"}。

配置数据源是一项管理任务，可为历程作者和营销人员解锁完整数据层。 字段通过数据源公开后，便可在历程条件生成器、消息个性化编辑器和Offer Decisioning规则中使用 — 无需在历程构建时执行任何其他工程工作。

➡️ [了解有关数据源配置的更多信息](../datasource/about-data-sources.md)

+++

+++ 验证跟踪、反馈和历程数据集

确认Journey Optimizer系统生成的数据集在数据集工作区中可用。 运行测试历程和营销活动，然后使用查询编辑器验证是否记录了发送、打开、点击和退回事件，以及是否正确捕获了历程步骤事件和状态。 使用这些数据集进行持续监控、故障排除和历程优化。

➡️ [了解有关Journey Optimizer中查询的更多信息](get-started-queries.md)

+++

## 护栏和数据设计注意事项 {#guardrails}

某些产品护栏和限制可能会影响您设计数据模型和历程的方式。 请尽早查看这些文档以避免以后重新工作。

>[!IMPORTANT]
>有关最新信息，请始终参考[Journey Optimizer护栏和限制](../start/guardrails.md)页面。 下面的摘要重点介绍一些关键项目，但这些项目可能会随着时间的推移而不断变化。

### Journey Optimizer系统数据集和TTL {#datasets-ttl}

Journey Optimizer为跟踪、反馈和旅程步骤事件创建多个系统生成的数据集。 自2025年2月起，其中一些数据集的生存时间(TTL)护栏将推出，这可能会影响为分析和故障排除而保留数据的时间。

➡️ [了解有关数据集TTL护栏的更多信息](datasets-ttl.md)

### 流式分段和Journey Optimizer事件 {#streaming-segmentation}

自2024年11月1日起，流式分段不再支持来自Journey Optimizer跟踪和反馈数据集的发送和打开事件。 对于频率上限和疲劳管理等用例，请使用[业务规则](../conflict-prioritization/rule-sets.md)，而不是基于发送/打开事件的流式处理区段。

➡️ [了解有关数据集的更多信息](get-started-datasets.md)

### 数据集查找和决策 {#lookup-guardrails}

数据集查找适用于频繁变化的属性（库存、定价、天气）或不需要存储在Real-time Customer Profile上的数据。 在设计查找策略之前，请查看相关文档中的产品特定护栏，例如数据集大小限制和查询上限。

➡️ [了解有关查找数据集的更多信息](lookup-aep-data.md)

## 示例：为欢迎历程准备数据 {#example}

以下示例演示了此页面上的概念如何在简单场景中协同工作。

1. 数据工程师为客户属性（名称、电子邮件、忠诚度级别、同意）创建[XDM个人配置文件架构](get-started-schemas.md)，并为Web注册事件创建XDM ExperienceEvent架构。
1. [为每个架构创建了启用配置文件的数据集](get-started-datasets.md)：一个用于CRM属性，一个用于注册事件。
1. Web和移动团队通过Adobe Experience Platform Web SDK流式处理注册事件；CRM数据通过[源连接器](../start/get-started-sources.md)摄取。
1. 管理员在Journey Optimizer中配置[Adobe Experience Platform数据源](../datasource/adobe-experience-platform-data-source.md)，并公开`profile.person.name.firstName`、`profile.personalEmail.address`和`profile.loyaltyTier`等字段。
1. 营销人员[创建欢迎历程](../building-journeys/journey-gs.md)，该历程侦听注册事件并使用这些配置文件属性[个性化欢迎电子邮件](../personalization/personalize.md)。 Journey Optimizer将发送和打开事件写入跟踪数据集，并将旅程进度记录在旅程步骤事件数据集中。
1. 开发人员使用[查询编辑器](get-started-queries.md)验证事件是否正确流动并分析性能（打开、点击、发送时间）。 团队根据这些见解调整历程和内容。

此流程说明了架构、数据集、源、数据源和查询如何在完整、初学者友好的用例中协同工作。

## 相关资源 {#related-resources}

:::: landing-cards-container

:::
![icon](https://cdn.experienceleague.adobe.com/icons/code-branch.svg)

**开始使用架构**

了解如何在Adobe Experience Platform中创建XDM架构，选择正确的类和字段组，并对您的配置文件属性和行为事件进行建模。

[了解详情](get-started-schemas.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/database.svg)

**使用数据集**

了解如何创建支持配置文件的数据集和事件数据集、监测数据摄取，以及探索Journey Optimizer自动创建的系统生成数据集，以便跟踪、反馈和历程步骤事件。

[了解详情](get-started-datasets.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/gear.svg)

**配置数据源**

关于设置内置Adobe Experience Platform数据源和可选外部数据源以在历程中公开配置文件字段和外部API响应的分步指南。

[了解详情](../datasource/about-data-sources.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/puzzle-piece.svg)

**使用Adobe Experience Platform数据（查找）**

了解如何在运行时使用AEP数据集中的引用或事务数据扩充消息，而无需将数据存储在实时客户档案中。

[了解详情](lookup-aep-data.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/chart-line.svg)

**查询入门**

使用查询服务分析Journey Optimizer数据集，验证事件是否正确流动，并就发送、打开、单击和退回数据构建报表查询。

[了解详情](get-started-queries.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/bullseye.svg)

**开始使用配置文件**

了解Real-time Customer Profile在Journey Optimizer中的工作方式，以及如何在Platform UI中浏览、检查和验证各个客户配置文件。

[了解详情](../audience/get-started-profiles.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/circle-play.svg)

**设置数据概述教程**

对Journey Optimizer中的数据设置进行的一次入门级友好的视频演练，端到端地涵盖了架构、数据集和源。

[观看教程](https://experienceleague.adobe.com/en/docs/journey-optimizer-learn/tutorials/data-management/set-up-data-overview){target="_blank"}
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/circle-play.svg)

**创建数据集并摄取数据教程**

一个动手教程，演示如何在Adobe Experience Platform中创建数据集以及使用源连接器摄取数据，其中包含您可以在自己的沙盒中遵循的分步说明。

[观看教程](https://experienceleague.adobe.com/en/docs/journey-optimizer-learn/tutorials/data-management/create-datasets-and-ingest-data){target="_blank"}
:::

::::
