---
solution: Journey Optimizer
product: journey optimizer
title: 编排的营销活动护栏和限制
description: 了解编排的活动护栏和限制
hide: true
hidefromtoc: true
exl-id: 82744db7-7358-4cc6-a9dd-03001759fef7
source-git-commit: 1aa4f3e24a4cb7594232c0b25da8c9fd2e62c1de
workflow-type: tm+mt
source-wordcount: '272'
ht-degree: 5%

---

# 护栏和限制 {#guardrails}

+++ 目录

| 欢迎使用编排的营销活动 | 启动第一个精心策划的营销活动 | 查询数据库 | 精心策划的营销活动 |
|---|---|---|---|
| [开始使用编排的营销活动](gs-orchestrated-campaigns.md)<br/><br/>创建和管理关系架构和数据集：</br> <ul><li>[手动架构](manual-schema.md)</li><li>[文件上载架构](file-upload-schema.md)</li><li>[摄取数据](ingest-data.md)</li></ul><br/><br/>[访问和管理编排的营销活动](access-manage-orchestrated-campaigns.md)<br/><br/>[创建编排的营销活动的关键步骤](gs-campaign-creation.md) | [创建和计划营销活动](create-orchestrated-campaign.md)<br/><br/>[编排活动](orchestrate-activities.md)<br/><br/>[启动并监视营销活动](start-monitor-campaigns.md)<br/><br/>[报告](reporting-campaigns.md) | [使用规则生成器](orchestrated-rule-builder.md)<br/><br/>[生成您的第一个查询](build-query.md)<br/><br/>[编辑表达式](edit-expressions.md)<br/><br/>[重新定位](retarget.md) | [开始使用活动](activities/about-activities.md)<br/><br/>活动：<br/>[并加入](activities/and-join.md) - [生成受众](activities/build-audience.md) - [更改维度](activities/change-dimension.md) - [渠道活动](activities/channels.md) - [组合](activities/combine.md) - [重复数据删除](activities/deduplication.md) - [扩充](activities/enrichment.md) - [分支](activities/fork.md) - [协调](activities/reconciliation.md) - [保存受众](activities/save-audience.md) - [拆分](activities/split.md) - [等待](activities/wait.md) |

{style="table-layout:fixed"}

+++

## 数据流到数据集的限制

Adobe Experience Platform中的每个数据集一次只能与一个活动数据流关联。 此1:1基数由平台严格执行。

如果您需要切换数据源(例如，从Amazon S3切换到Salesforce)：

您必须删除连接到数据集的现有数据流。

然后，创建一个新数据流，并将新源映射到同一数据集。

这确保了可靠的数据摄取，并且在使用变更数据捕获(CDC)时至关重要，CDC依赖于为增量更新定义的主键和版本控制属性（例如lastmodified）。


## 关系架构/数据摄取限制

* 架构数 — 关系架构（关系数据存储中的表）的最大数量为200
* 关系架构大小 — Campaign Orchestration的最大关系架构大小将为100 GB。
* 数据摄取频率 — 活动编排的批量数据摄取频率不得超过每15分钟一次。
* 更改/更新 — 对于给定的关系架构，每日更新/更改应少于总记录的20%
