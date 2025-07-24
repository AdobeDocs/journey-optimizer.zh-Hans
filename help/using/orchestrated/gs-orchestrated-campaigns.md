---
solution: Journey Optimizer
product: journey optimizer
title: 精心策划的营销活动快速入门
description: 了解如何开始使用精心策划的营销活动
badge: label="Alpha"
hide: true
hidefromtoc: true
exl-id: 611dd06d-aa18-4fa3-a477-8a910cec21d8
source-git-commit: 15f5fdfde0e9f7c93739a624918838dbd6787833
workflow-type: tm+mt
source-wordcount: '540'
ht-degree: 19%

---

# 精心策划的营销活动快速入门 {#orchestrated-camp}

>[!CONTEXTUALHELP]
>id="campaigns_overview_orchestrated"
>title="精心策划的营销活动"
>abstract="**营销活动编排**<br/>&#x200B;拆分、组合、扩充和处理关系数据集以定义受众<br/><br/>"

**利用多实体数据**<br/>&#x200B;了解编排的活动如何利用关系数据集扩充分段和个性化数据&#x200B;<br/><br/>**临时分段和精确计数**<br/>&#x200B;使用精确计数逐步构建区段&#x200B;<br/><br/>**可用渠道**<br/>&#x200B;电子邮件、短信、推送通知、直邮”

+++ 目录

| 欢迎了解精心策划的营销活动 | 启动第一个精心策划的营销活动 | 查询数据库 | 精心策划的营销活动 |
|---|---|---|---|
| <b>[开始使用编排的营销活动](gs-orchestrated-campaigns.md)</b><br/><br/>创建和管理关系架构和数据集：</br> <ul><li>[架构和数据集入门](gs-schemas.md)</li><li>[手动架构](manual-schema.md)</li><li>[文件上载架构](file-upload-schema.md)</li><li>[摄取数据](ingest-data.md)</li></ul>[访问和管理编排的营销活动](access-manage-orchestrated-campaigns.md)<br/><br/>[创建编排的营销活动的关键步骤](gs-campaign-creation.md) | [创建和计划营销活动](create-orchestrated-campaign.md)<br/><br/>[精心策划活动](orchestrate-activities.md)<br/><br/>[启动和监控营销活动](start-monitor-campaigns.md)<br/><br/>[报告](reporting-campaigns.md) | [使用规则生成器](orchestrated-rule-builder.md)<br/><br/>[生成您的第一个查询](build-query.md)<br/><br/>[编辑表达式](edit-expressions.md)<br/><br/>[重定向](retarget.md) | [活动快速入门](activities/about-activities.md)<br/><br/>活动：<br/>[并行汇聚](activities/and-join.md) - [生成受众](activities/build-audience.md) - [更改维度](activities/change-dimension.md) - [渠道活动](activities/channels.md) - [合并](activities/combine.md) - [重复数据删除](activities/deduplication.md) - [扩充](activities/enrichment.md) - [分叉](activities/fork.md) - [协调](activities/reconciliation.md) - [保存受众](activities/save-audience.md) - [拆分](activities/split.md) - [等待](activities/wait.md) |

{style="table-layout:fixed"}

+++

<br/>

>[!BEGINSHADEBOX]

</br>

此页面上的内容不是最终内容，可能会发生变化。

>[!ENDSHADEBOX]

[!DNL Adobe Journey Optimizer]中的营销活动编排可跨渠道支持由品牌发起的复杂营销活动，从而帮助您大规模提高参与度、收入和客户忠诚度。

虽然跨渠道营销至关重要，但精心策划的活动可使其无缝化。 借助可视化拖放界面，您可以跨多个渠道设计和自动化从分段到消息投放在内的复杂营销工作流。 一切都在为速度、控制和效率而构建的直观环境中进行。

![](assets/canvas-example-diagram.png){zoomable="yes"}

## 核心功能

Campaign Orchestration围绕四个关键支柱构建：

<table style="table-layout:auto">
<tr style="border: 0;">
<td><img alt="按需受众" src="assets/do-not-localize/icon-audience.svg" width="50px"></a></td><td><b>按需受众</b><br/>即时跨数据集查询以使用数据类型和维度的任意组合创建受众区段。</td></tr>
<tr style="border: 0;">
<td><img alt="多实体分段和发送" src="assets/do-not-localize/icon-entity.svg" width="50px"></a></td><td><b>多实体分段和发送</b><br/>超越基于人员的营销活动 — 使用产品目录、商店位置或服务数据等实体来精确定位。</td></tr>
<tr style="border: 0;">
<td><img alt="预发送可见性和精确性" src="assets/do-not-localize/icon-visibility.svg" width="50px"></a></td><td><b>发送前可见性和精确度</b><br/>在启动前获取准确的分段计数和完整的促销活动范围，确保准确性和可信度。</td></tr>
<tr style="border: 0;">
<td><img alt="多步骤活动工作流" src="assets/do-not-localize/icon-multistep.svg" width="50px"></a></td><td><b>多步骤营销活动工作流</b><br/>设计多步骤营销活动，从每日消息到复杂的营销活动，如季节性促销活动或主要产品发布。</td></tr>
</table>

## 编排的营销活动和历程

尽管编排的营销活动可视化图表与历程具有相似之处，但它解决了不同的目的和用例：

* **历程** - 1到1个画布，每个个人资料将按照自己的速度在各个步骤中传递。 每个客户的状态都保留在其上下文中，以触发实时操作。

* **协调的营销活动** — 与历程不同，协调的营销活动使用计算区段的批次画布运行。 所有配置文件都会同时处理。

## 先决条件

在使用编排的营销活动之前，请务必确保您拥有适当的权限。 仅限分配给相关&#x200B;**[!UICONTROL 产品配置文件]**&#x200B;的用户访问编排的营销活动，例如编排的营销活动管理员、编排的营销活动审批者、编排的营销活动经理或编排的营销活动查看器。

如果您无法访问编排的活动功能，请联系管理员以请求必要的权限。

➡️ [了解有关协调营销活动的产品配置文件的更多信息](../administration/ootb-product-profiles.md)

## 让我们深入探究

现在，您已了解哪些是精心策划的营销活动，接下来该深入挖掘这些文档部分，以开始使用此功能。

<table><tr style="border: 0; text-align: center;">
<td>
<a href="gs-campaign-creation.md">
<img alt="访问和管理工作流" src="assets/do-not-localize/workflow-access.jpeg">
</a>
<div>
<a href="gs-campaign-creation.md"><strong>配置步骤</strong></a>
</div>
<p>
</td>
<td>
<a href="create-orchestrated-campaign.md">
<img alt="潜在客户" src="assets/do-not-localize/workflow-create.jpeg">
</a>
<div><a href="create-orchestrated-campaign.md"><strong>创建精心策划的营销活动</strong>
</div>
<p>
</td>
<td>
<a href="activities/about-activities.md">
<img alt="不频繁" src="assets/do-not-localize/workflow-activities.jpeg">
</a>
<div>
<a href="activities/about-activities.md"><strong>使用活动</strong></a>
</div>
<p></td>
</tr></table>
