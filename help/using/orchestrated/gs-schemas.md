---
solution: Journey Optimizer
product: journey optimizer
title: 配置步骤
description: 了解如何通过上传DDL在Adobe Experience Platform中创建关系架构
badge: label="Alpha"
hide: true
hidefromtoc: true
exl-id: 327597f6-8a53-42dc-966a-baae49b58bb3
source-git-commit: 3be1b238962fa5d0e2f47b64f6fa5ab4337272a5
workflow-type: tm+mt
source-wordcount: '243'
ht-degree: 25%

---

# 架构和数据集入门{#gs-schemas}

+++ 目录

| 欢迎使用编排的营销活动 | 启动您的第一个编排的营销活动 | 查询数据库 | 精心策划的营销活动 |
|---|---|---|---|
| [开始使用协调的营销活动](gs-orchestrated-campaigns.md)<br/><br/>创建和管理关系架构和数据集：</br> <ul><li>[架构和数据集入门](gs-schemas.md)</li><li>[手动架构](manual-schema.md)</li><li>[文件上载架构](file-upload-schema.md)</li><li>[摄取数据](ingest-data.md)</li></ul>[访问和管理编排的营销活动](access-manage-orchestrated-campaigns.md)<br/><br/>[创建编排的营销活动的关键步骤](gs-campaign-creation.md) | [创建和计划营销活动](create-orchestrated-campaign.md)<br/><br/>[精心策划活动](orchestrate-activities.md)<br/><br/>[启动和监控营销活动](start-monitor-campaigns.md)<br/><br/>[报告](reporting-campaigns.md) | [使用规则生成器](orchestrated-rule-builder.md)<br/><br/>[生成您的第一个查询](build-query.md)<br/><br/>[编辑表达式](edit-expressions.md)<br/><br/>[重定向](retarget.md) | [活动快速入门](activities/about-activities.md)<br/><br/>活动：<br/>[并行汇聚](activities/and-join.md) - [生成受众](activities/build-audience.md) - [更改维度](activities/change-dimension.md) - [渠道活动](activities/channels.md) - [合并](activities/combine.md) - [重复数据删除](activities/deduplication.md) - [扩充](activities/enrichment.md) - [分叉](activities/fork.md) - [协调](activities/reconciliation.md) - [保存受众](activities/save-audience.md) - [拆分](activities/split.md) - [等待](activities/wait.md) |

{style="table-layout:fixed"}

+++

</br>

>[!BEGINSHADEBOX]

</br>

此页面上的内容不是最终内容，可能会发生变化。

>[!ENDSHADEBOX]

本指南将指导您完成以下过程：创建关系架构、为编排的营销活动配置数据集以及摄取数据。

![](assets/do-not-localize/schema_admin.png)

1. 使用DDL文件[手动创建](manual-schema.md)关系架构[或](file-upload-schema.md)

   定义数据模型的结构，包括表、属性和关系。 选择在用户界面中手动构建架构，或上传DDL文件以加快设置。

1. [关联架构](file-upload-schema.md)

   在架构之间建立关系以确保数据一致性并启用跨实体查询。 例如，将忠诚度交易关联到收件人，或将奖励关联到品牌。

1. [摄取数据](ingest-data.md)

   将来自受支持源（如SFTP、云存储或数据库）的数据引入Adobe Experience Platform。

