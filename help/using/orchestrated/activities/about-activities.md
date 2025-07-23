---
solution: Journey Optimizer
product: journey optimizer
title: 使用精心策划的营销活动
description: 了解如何精心策划营销活动
badge: label="Alpha"
hide: true
hidefromtoc: true
exl-id: 02f986b2-8200-4e0e-8918-44e528a6a3ec
source-git-commit: 1a9ea09fcbf304b1649a5ae88da34bd209e9ac8b
workflow-type: tm+mt
source-wordcount: '500'
ht-degree: 91%

---

# 关于精心策划的营销活动 {#orchestrated-campaign-activities}


+++ 目录

| 欢迎了解精心策划的营销活动 | 启动第一个精心策划的营销活动 | 查询数据库 | 精心策划的营销活动 |
|---|---|---|---|
| [开始使用编排的营销活动](../gs-orchestrated-campaigns.md)<br/><br/>创建和管理关系架构和数据集：</br> <ul><li>[架构和数据集入门](../gs-schemas.md)</li><li>[手动架构](../manual-schema.md)</li><li>[文件上载架构](../file-upload-schema.md)</li><li>[摄取数据](../ingest-data.md)</li></ul>[访问和管理编排的营销活动](../access-manage-orchestrated-campaigns.md) | [创建精心策划的营销活动的关键步骤](../gs-campaign-creation.md)<br/><br/>[创建和计划营销活动](../create-orchestrated-campaign.md)<br/><br/>[精心策划活动](../orchestrate-activities.md)<br/><br/>[启动和监控营销活动](../start-monitor-campaigns.md)<br/><br/>[报告](../reporting-campaigns.md) | [使用规则生成器](../orchestrated-rule-builder.md)<br/><br/>[生成您的第一个查询](../build-query.md)<br/><br/>[编辑表达式](../edit-expressions.md)<br/><br/>[重定向](../retarget.md) | <b>[活动快速入门](about-activities.md)</b><br/><br/>活动：<br/>[并行汇聚](and-join.md) - [生成受众](build-audience.md) - [更改维度](change-dimension.md) - [渠道活动](channels.md) - [合并](combine.md) - [重复数据删除](deduplication.md) - [扩充](enrichment.md) - [分叉](fork.md) - [协调](reconciliation.md) - [保存受众](save-audience.md) - [拆分](split.md) - [等待](wait.md) |

{style="table-layout:fixed"}

+++

<br/>

>[!BEGINSHADEBOX]

</br>

此页面上的内容不是最终内容，可能会发生变化。

>[!ENDSHADEBOX]

精心策划的营销活动分为三类。根据具体情况，可用的活动可能会有所不同。

以下各章节详细介绍了所有活动：

* [目标选择活动](#targeting)
* [渠道活动](#channel)
* [流程控制活动](#flow-control)

![画布中可用的活动列表](../assets/orchestrated-activities.png){width="80%" align="left"}

## 目标选择活动 {#targeting}

这些活动特定于目标选择。利用这些活动，您可以通过定义受众并使用交叉、组合或排除操作来拆分或组合这些受众，从而生成一个或多个目标。

![目标选择活动列表](../assets/targeting-activities.png){width="40%" align="left"}

* [生成受众](build-audience.md)：定义目标群体。您可以选择现有受众或使用查询建模器来定义您自己的查询。
* [更改维度](change-dimension.md)：在生成精心策划的营销活动时更改目标维度。
* [合并](combine.md)：对入站群体执行细分。您可以使用合并、交叉或排除。
* [重复数据删除](deduplication.md)：删除入站活动结果中的重复项。
* [扩充](enrichment.md)：定义要在精心策划的营销活动中处理的其他数据。通过此活动，您可以应用入站过渡并配置活动以使用其他数据完成输出过渡的设置。
* [协调](reconciliation.md)：定义 Journey Optimizer 数据与工作表数据（例如从外部文件加载的数据）之间的关联。
* [拆分](split.md)：将传入的群体划分到多个子集中。

## 渠道活动 {#channel}

Adobe Journey Optimizer 允许您跨多个渠道自动化和执行营销活动。您可以将渠道活动组合到画布中，以创建可根据客户行为触发操作的精心策划的跨渠道营销活动。可以使用以下&#x200B;**渠道**&#x200B;活动：电子邮件和短信。[了解如何在精心策划的营销活动上下文中创建渠道操作](channels.md)。

## 流程控制活动 {#flow-control}

>[!CONTEXTUALHELP]
>id="ajo_orchestration_end"
>title="结束活动"
>abstract="您可以使用&#x200B;**结束**&#x200B;活动，以图形方式标记协同营销活动的结束。此活动无功能性影响，因此为可选活动。"

![流程控制活动列表](../assets/flow-control-activities.png){width="30%" align="left"}

以下活动特定于组织和执行精心策划的营销活动。这些活动的主要任务是协调其他活动：

* [并行汇聚](and-join.md)：同步精心策划的营销活动的多个执行分支。
* [分叉](fork.md)：创建出站过渡以同时启动多个活动。
* [等待](wait.md)：暂时暂停执行精心策划的营销活动的一部分。
  <!--* [Test](test.md): Enable transitions based on specified conditions.-->

>[!NOTE]
>您可以使用&#x200B;**结束**&#x200B;活动以图形方式标记精心策划的营销活动的结束。此活动对功能没有影响，因此是可选项
