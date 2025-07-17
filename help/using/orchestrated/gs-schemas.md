---
solution: Journey Optimizer
product: journey optimizer
title: 配置步骤
description: 了解如何通过上传DDL在Adobe Experience Platform中创建关系架构
badge: label="Alpha"
hide: true
hidefromtoc: true
source-git-commit: 1a9ea09fcbf304b1649a5ae88da34bd209e9ac8b
workflow-type: tm+mt
source-wordcount: '272'
ht-degree: 5%

---

# 架构和数据集入门{#gs-schemas}

+++ 目录

| 欢迎使用编排的营销活动 | 启动第一个精心策划的营销活动 | 查询数据库 | 精心策划的营销活动 |
|---|---|---|---|
| [开始使用编排的营销活动](gs-orchestrated-campaigns.md)<br/><br/>创建和管理关系架构和数据集：</br> <ul><li>[架构和数据集入门](gs-schemas.md)</li><li>[手动架构](manual-schema.md)</li><li>[文件上载架构](file-upload-schema.md)</li><li>[摄取数据](ingest-data.md)</li></ul>[访问和管理编排的营销活动](access-manage-orchestrated-campaigns.md)<br/><br/>[创建编排的营销活动的关键步骤](gs-campaign-creation.md) | [创建和计划营销活动](create-orchestrated-campaign.md)<br/><br/>[编排活动](orchestrate-activities.md)<br/><br/>[启动并监视营销活动](start-monitor-campaigns.md)<br/><br/>[报告](reporting-campaigns.md) | [使用规则生成器](orchestrated-rule-builder.md)<br/><br/>[生成您的第一个查询](build-query.md)<br/><br/>[编辑表达式](edit-expressions.md)<br/><br/>[重新定位](retarget.md) | [开始使用活动](activities/about-activities.md)<br/><br/>活动：<br/>[并加入](activities/and-join.md) - [生成受众](activities/build-audience.md) - [更改维度](activities/change-dimension.md) - [渠道活动](activities/channels.md) - [组合](activities/combine.md) - [重复数据删除](activities/deduplication.md) - [扩充](activities/enrichment.md) - [分支](activities/fork.md) - [协调](activities/reconciliation.md) - [保存受众](activities/save-audience.md) - [拆分](activities/split.md) - [等待](activities/wait.md) |

{style="table-layout:fixed"}

+++

</br>

>[!BEGINSHADEBOX]

</br>

内容

此页面上的内容不是最终内容，可能会发生变化。

>[!ENDSHADEBOX]

本指南将指导您完成以下过程：创建关系架构、为编排的营销活动配置数据集、通过S3源摄取数据，以及在AP平台中查询摄取的数据。

在此示例中，设置包括集成两个关键实体&#x200B;**忠诚度交易**&#x200B;和&#x200B;**忠诚度奖励**，并将它们链接到现有核心实体&#x200B;**收件人**&#x200B;和&#x200B;**品牌**。

![](assets/do-not-localize/schema_admin.png)

1. [创建关系架构和相关数据集](#schema)

   为编排的营销活动定义关系数据模型，包括&#x200B;**忠诚度会员资格**、**忠诚度交易**&#x200B;和&#x200B;**忠诚度奖励**&#x200B;实体，以及所需的键和版本控制属性。

1. [链接架构](#link-schema)

   将&#x200B;**忠诚度交易**&#x200B;实体链接到&#x200B;**收件人**，将&#x200B;**忠诚度奖励**&#x200B;链接到&#x200B;**品牌**，以构建支持个性化客户历程的连接数据模型。

1. [引入数据](#ingest)

   将来自受支持源（如SFTP、云存储或数据库）的数据引入Adobe Experience Platform。


<!--### Setting Up Change data capture ingestion {#cdc-ingestion}

If you need to change the data source, you must delete the existing dataflow and create a new one pointing to the same dataset with the new source.

When using Change Data Capture (CDC), it is essential that the source and dataset remain in sync to ensure accurate incremental updates. Follow the steps below:

1. **Schema Requirements**
   - Your schema must include:
     - A **primary key** (e.g., `transaction_id`)
     - A **versioning field** (e.g., `lastmodified` or an incrementing `version_id`)
   - Enable the dataset for **Orchestrated Campaigns** if needed.

2. **CDC Dataflow Setup**
   - During dataflow creation, after choosing your source and files:
     - **Enable the CDC option**
     - Select your CDC-ready dataset
     - Confirm field mappings (especially version field)

3. **Keep Source and Target in Sync**
   - The source system must consistently update the version field so the platform can detect changes accurately.

Once set up, the platform will automatically ingest **only changed or new records** each time the flow runs.
-->
