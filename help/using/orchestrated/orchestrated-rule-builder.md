---
solution: Journey Optimizer
product: journey optimizer
title: 使用规则生成器
description: 了解如何为您精心策划的营销活动创建规则
badge: label="Alpha"
hide: true
hidefromtoc: true
exl-id: fb7a0eb2-b2ff-49fa-af1f-f1c10f219b00
source-git-commit: 1a9ea09fcbf304b1649a5ae88da34bd209e9ac8b
workflow-type: tm+mt
source-wordcount: '421'
ht-degree: 87%

---


# 使用规则生成器 {#orchestrated-rule-builder}

+++ 目录

| 欢迎了解精心策划的营销活动 | 启动第一个精心策划的营销活动 | 查询数据库 | 精心策划的营销活动 |
|---|---|---|---|
| [开始使用编排的营销活动](gs-orchestrated-campaigns.md)<br/><br/>创建和管理关系架构和数据集：</br> <ul><li>[架构和数据集入门](gs-schemas.md)</li><li>[手动架构](manual-schema.md)</li><li>[文件上载架构](file-upload-schema.md)</li><li>[摄取数据](ingest-data.md)</li></ul>[访问和管理编排的营销活动](access-manage-orchestrated-campaigns.md)<br/><br/>[创建编排的营销活动的关键步骤](gs-campaign-creation.md) | [创建和计划营销活动](create-orchestrated-campaign.md)<br/><br/>[精心策划活动](orchestrate-activities.md)<br/><br/>[启动和监控营销活动](start-monitor-campaigns.md)<br/><br/>[报告](reporting-campaigns.md) | <b>[使用规则生成器](orchestrated-rule-builder.md)</b><br/><br/>[生成您的第一个查询](build-query.md)<br/><br/>[编辑表达式](edit-expressions.md)<br/><br/>[重定向](retarget.md) | [活动快速入门](activities/about-activities.md)<br/><br/>活动：<br/>[并行汇聚](activities/and-join.md) - [生成受众](activities/build-audience.md) - [更改维度](activities/change-dimension.md) - [渠道活动](activities/channels.md) - [合并](activities/combine.md) - [重复数据删除](activities/deduplication.md) - [扩充](activities/enrichment.md) - [分叉](activities/fork.md) - [协调](activities/reconciliation.md) - [保存受众](activities/save-audience.md) - [拆分](activities/split.md) - [等待](activities/wait.md) |

{style="table-layout:fixed"}

+++

<br/>

>[!BEGINSHADEBOX]

</br>

此页面上的内容不是最终内容，可能会发生变化。

>[!ENDSHADEBOX]

精心策划的营销活动附带规则生成器，可简化根据各种标准筛选数据库的过程。规则生成器可高效处理极其复杂的长查询，提供更强的灵活性与精准度。

它还支持在条件中使用预定义过滤器，让您能轻松优化查询，同时借助高级表达式和运算符实现全面的受众目标选择与细分策略。

## 访问规则生成器

在每个需要定义规则以过滤数据的环境下都有查询建模器可用。

| 使用情况 | 示例 |
|  ---  |  ---  |
| **生成受众**：通过&#x200B;**[!UICONTROL 生成受众]**&#x200B;活动，在精心策划的营销活动中精准定位目标人群，并轻松创建符合需求的全新受众。[了解如何生成受众](../orchestrated/activities/build-audience.md) | ![显示如何访问受众创建界面的图像](assets/query-access-audience.png){width="200" align="center" zoomable="yes"} |
| **在营销活动画布中创建条件**：使用&#x200B;**[!UICONTROL 拆分]**&#x200B;活动在营销活动画布中应用规则，以满足您的特定要求。[了解如何使用“拆分”活动](../orchestrated/activities/split.md) | ![显示如何访问工作流自定义选项的图像](assets/query-access-split.png){width="200" align="center" zoomable="yes"} |
| **创建高级过滤器**：生成规则以筛选列表中显示的数据，例如工作流日志或目标维度。 | ![显示如何自定义列表过滤器的图像](assets/query-access-advanced-filters.png){width="200" align="center" zoomable="yes"} |

## 规则生成器界面 {#interface}

规则生成器提供了一个中央画布用于生成查询，并提供一个显示规则详情的属性窗格。

![显示规则生成器界面的图像](assets/rule-builder-interface.png)

* **中央画布**&#x200B;是添加和组合各类组件以生成规则的操作区域。[了解如何生成规则](../orchestrated/build-query.md)

* **[!UICONTROL 规则属性]**&#x200B;窗格提供有关规则的信息。它支持执行各种操作来检查规则，确保其符合您的需求。

  在生成查询以创建受众时，会显示此窗格。[了解如何检查和验证您的查询](build-query.md#check-and-validate-your-query)
