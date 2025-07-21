---
solution: Journey Optimizer
product: journey optimizer
title: 编排的营销活动护栏和限制
description: 了解编排的活动护栏和限制
hide: true
hidefromtoc: true
exl-id: 82744db7-7358-4cc6-a9dd-03001759fef7
source-git-commit: 2ad659b391515c193418325c34a9dd56133b90d6
workflow-type: tm+mt
source-wordcount: '575'
ht-degree: 2%

---

# 护栏和限制 {#guardrails}

+++ 目录

| 欢迎使用编排的营销活动 | 启动第一个精心策划的营销活动 | 查询数据库 | 精心策划的营销活动 |
|---|---|---|---|
| [开始使用编排的营销活动](gs-orchestrated-campaigns.md)<br/><br/>创建和管理关系架构和数据集：</br> <ul><li>[架构和数据集入门](gs-schemas.md)</li><li>[手动架构](manual-schema.md)</li><li>[文件上载架构](file-upload-schema.md)</li><li>[摄取数据](ingest-data.md)</li></ul>[访问和管理编排的营销活动](access-manage-orchestrated-campaigns.md)<br/><br/>[创建编排的营销活动的关键步骤](gs-campaign-creation.md) | [创建和计划营销活动](create-orchestrated-campaign.md)<br/><br/>[编排活动](orchestrate-activities.md)<br/><br/>[启动并监视营销活动](start-monitor-campaigns.md)<br/><br/>[报告](reporting-campaigns.md) | [使用规则生成器](orchestrated-rule-builder.md)<br/><br/>[生成您的第一个查询](build-query.md)<br/><br/>[编辑表达式](edit-expressions.md)<br/><br/>[重新定位](retarget.md) | [开始使用活动](activities/about-activities.md)<br/><br/>活动：<br/>[并加入](activities/and-join.md) - [生成受众](activities/build-audience.md) - [更改维度](activities/change-dimension.md) - [渠道活动](activities/channels.md) - [组合](activities/combine.md) - [重复数据删除](activities/deduplication.md) - [扩充](activities/enrichment.md) - [分支](activities/fork.md) - [协调](activities/reconciliation.md) - [保存受众](activities/save-audience.md) - [拆分](activities/split.md) - [等待](activities/wait.md) |

{style="table-layout:fixed"}

+++

## 数据流到数据集的限制

Adobe Experience Platform中的每个数据集一次只能与一个活动数据流关联。 此1:1基数由平台严格强制执行。

如果您需要切换数据源(例如，从Amazon S3切换到Salesforce)：

您必须删除连接到数据集的现有数据流。

然后，创建一个新数据流，并将新源映射到同一数据集。

这确保了可靠的数据摄取，并且在使用变更数据捕获(CDC)时至关重要，CDC依赖于为增量更新定义的主键和版本控制属性（例如lastmodified）。


## 关系架构/数据摄取限制

* 关系数据存储中支持多达200个关系架构（表）。

* 用于Campaign Orchestration的关系架构的总大小不应超过100 GB。

* Campaign Orchestration的批量摄取的频率不应超过每15分钟一次。

* 对关系架构的每日更改应保持低于总记录计数的20%。

## 数据建模

* 版本描述符在所有架构上都是必需的，包括事实表。

* 每个表都需要一个主键。

* 在数据集创建期间分配的table_name可在分段UI和个性化功能中使用。

  此名称是永久性的，创建后无法更改。

* 当前不支持字段组。

## 数据引入

* 需要配置文件+关系数据摄取。

* 基于文件的摄取需要更改类型字段，而必须为云数据库摄取启用表日志记录。 这是变更数据捕获(CDC)所必需的。

* 在Snowflake中，从摄取到数据可用性的延迟从15分钟到2小时不等，具体取决于数据量、并发性和操作类型（插入比更新快）。

* Snowflake中的数据监控正在开发中；目前，无法针对成功摄取进行本机确认。

* 不支持直接更新Snowflake或数据集。 所有更改必须通过CDC源进行。

  查询服务是只读的。

* 不支持ETL — 客户必须以所需格式提供数据。

* 不允许进行部分更新。 每一行都必须作为完整记录提供。

* 摄取依赖于查询服务和数据Distiller。

## 区段

* 值列表(LOV)和枚举当前可用。

* 保存的受众是静态列表，其内容反映执行营销活动时可用的数据。

* 不支持附加到已保存的受众。 更新需要完全覆盖。

* 受众必须仅包含标量属性；不支持映射和数组。

* 分段主要支持关系数据。 虽然允许与配置文件数据混合，但引入大型配置文件数据集可能会影响性能。 要防止出现这种情况，请执行以下操作：

* 设置了护栏，例如限制在批量或流式受众中选择的用户档案属性的数量。

* 读取不缓存受众 — 每次活动运行都会触发完全读取。

  大型或复杂受众需要优化。