---
solution: Journey Optimizer
product: journey optimizer
title: 配置步骤
description: 了解如何通过上传DDL在Adobe Experience Platform中创建基于模型的架构
exl-id: 327597f6-8a53-42dc-966a-baae49b58bb3
version: Campaign Orchestration
source-git-commit: e189bb6a52691770655a436e45c6788d1011a8ca
workflow-type: tm+mt
source-wordcount: '470'
ht-degree: 1%

---


# 开始使用基于模型的架构和数据集{#gs-schemas}

本指南将指导您完成以下过程：创建基于模型的架构、为编排的营销活动配置数据集以及摄取数据。

![架构](assets/do-not-localize/schema_admin.png){zoomable="yes"}

## 重要概念

在编排的营销活动上下文中，**数据集**&#x200B;是用于数据集合的存储和管理结构，通常是包含架构（行）和字段（列）的表。 成功引入Experience Platform的数据将作为数据集存储在数据湖中。

**架构**&#x200B;表示并验证数据的结构和格式。它提供了真实世界对象（如人）的抽象定义，并概述了该对象的每个实例中应包含哪些数据（如名称、生日等）。

**数据模型**&#x200B;是标准化数据的概念蓝图

它描述了：

* 实体（例如，客户、营销策划、区段）
* 这些实体的属性（例如，客户名称、促销活动开始日期）
* 实体之间的关系（例如，客户属于区段，营销活动针对区段）

数据模型是逻辑和概念性的，不与Orchestrated Campaign中的物理实施绑定

在基于模型的&#x200B;**数据模型**&#x200B;中，数据被组织到与其他表相关的表中。

* 每个表都有行（记录）和列（属性）
* 每个表都有一个用于唯一标识行的主键
* 表之间的关系使用外键表示

**基于模型的架构**&#x200B;是基于模型的数据模型的正式定义。

它指定：

* 表集
* 每个表中的列
* 约束
* 表之间的关系

在基于模型的数据模型中组织架构或表就是将您的数据结构化为多个表。 确保每个表存储一种类型的实体/架构

➡️ [在Adobe Experience Platform文档中了解有关架构的更多信息](https://experienceleague.adobe.com/en/docs/experience-platform/xdm/ui/resources/schemas#create-model-based-schema)

## 实施步骤 {#implementation}

要摄取数据并创建基于模型的架构，请执行以下步骤：

1. 使用DDL文件[手动创建](manual-schema.md)基于模型的架构[或](file-upload-schema.md)

   定义数据模型的结构，包括表、属性和关系。 选择在用户界面中手动构建架构，或上传DDL文件以加快设置。

   手动创建架构时，还必须手动创建和启用数据集。 使用DDL文件时，数据集创建和启用是自动执行的。

1. [链接架构](file-upload-schema.md)

   在架构之间建立关系以确保数据一致性并启用跨实体查询。 例如，将忠诚度交易关联到收件人，或将奖励关联到品牌。

1. [创建数据集](manual-schema.md#dataset)

   定义架构后，您需要基于该架构创建数据集。 此数据集将用作已摄取数据的存储。

1. [启用编排的营销活动](manual-schema.md#enable)

   数据集会存储您摄取的数据，必须为编排的营销活动启用该数据集，以确保在Adobe Journey Optimizer中可访问这些数据。

1. [摄取数据](ingest-data.md)

   将来自受支持源（如SFTP、云存储或数据库）的数据引入Adobe Experience Platform。

