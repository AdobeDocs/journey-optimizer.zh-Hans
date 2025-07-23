---
solution: Journey Optimizer
product: journey optimizer
title: 使用“更改维度”活动
description: 了解如何使用“更改维度”活动
badge: label="Alpha"
hide: true
hidefromtoc: true
exl-id: 83e66f10-93dd-4759-840c-2c83abc42a28
source-git-commit: 1a9ea09fcbf304b1649a5ae88da34bd209e9ac8b
workflow-type: tm+mt
source-wordcount: '376'
ht-degree: 88%

---

# 更改维度 {#change-dimension}

>[!CONTEXTUALHELP]
>id="ajo_orchestration_dimension_complement"
>title="生成补集"
>abstract="可使用剩余群体（已排除的重复项）生成额外的出站过渡。为此，请打开生成补集选项为此，请打开&#x200B;**生成补集**&#x200B;选项。"

>[!CONTEXTUALHELP]
>id="ajo_orchestration_change_dimension"
>title="更改维度活动"
>abstract="通过此活动，可在生成受众时更改定位维度。它根据数据模板和输入维度移动轴。例如，您可以从“合同”维度切换到“客户”维度。"

+++ 目录

| 欢迎了解精心策划的营销活动 | 启动第一个精心策划的营销活动 | 查询数据库 | 精心策划的营销活动 |
|---|---|---|---|
| [开始使用编排的营销活动](../gs-orchestrated-campaigns.md)<br/><br/>创建和管理关系架构和数据集：</br> <ul><li>[架构和数据集入门](../gs-schemas.md)</li><li>[手动架构](../manual-schema.md)</li><li>[文件上载架构](../file-upload-schema.md)</li><li>[摄取数据](../ingest-data.md)</li></ul>[访问和管理编排的营销活动](../access-manage-orchestrated-campaigns.md) | [创建精心策划的营销活动的关键步骤](../gs-campaign-creation.md)<br/><br/>[创建和计划营销活动](../create-orchestrated-campaign.md)<br/><br/>[精心策划活动](../orchestrate-activities.md)<br/><br/>[启动和监控营销活动](../start-monitor-campaigns.md)<br/><br/>[报告](../reporting-campaigns.md) | [使用规则生成器](../orchestrated-rule-builder.md)<br/><br/>[生成您的第一个查询](../build-query.md)<br/><br/>[编辑表达式](../edit-expressions.md)<br/><br/>[重定向](../retarget.md) | [活动快速入门](about-activities.md)<br/><br/>活动：<br/>[并行汇聚](and-join.md) - [生成受众](build-audience.md) - <b>[更改维度](change-dimension.md)</b> - [渠道活动](channels.md) - [合并](combine.md) - [重复数据删除](deduplication.md) - [扩充](enrichment.md) - [分叉](fork.md) - [协调](reconciliation.md) - [保存受众](save-audience.md) - [拆分](split.md) - [等待](wait.md) |

{style="table-layout:fixed"}

+++

<br/>

>[!BEGINSHADEBOX]

</br>

此页面上的内容不是最终内容，可能会发生变化。

>[!ENDSHADEBOX]

作为营销人员，您可以在精心策划的营销活动中从一个数据实体转移到相关数据实体，从而增强受众目标选择。这使您能够越过轮廓并专注于特定行为，例如购买、预订或其他交互。

要实现此目的，请使用&#x200B;**[!UICONTROL 更改维度]**&#x200B;活动。通过该活动，您可以在精心策划的营销活动期间调整目标维度。

<!--
>[!IMPORTANT]
>
>Please note that the **[!UICONTROL Change Dimension]** and **[!UICONTROL Change Data source]** activities should not be added in one row. If you need to use both activities consecutively, make sure you include an **[!UICONTROL Enrichement]** activity in between them. This ensures proper execution and prevents potential conflicts or errors.-->

## 配置“更改维度”活动 {#configure}

请按照以下步骤配置&#x200B;**[!UICONTROL 更改维度]**&#x200B;活动：

1. 将&#x200B;**[!UICONTROL 更改维度]**&#x200B;活动添加到精心策划的营销活动中。

   ![](../assets/orchestrated-change-dimension.png)

1. 定义&#x200B;**[!UICONTROL 新目标维度]**。在维度更改期间，将保留所有记录。


## 示例 {#example}

在此用例中，主要是向在过去一个月内创建了愿望清单的轮廓发送短信。

在开始&#x200B;**[!UICONTROL 生成受众]**&#x200B;活动时，使用&#x200B;**[!UICONTROL 愿望清单]**&#x200B;目标维度识别所有相关愿望清单。

然后，添加&#x200B;**[!UICONTROL 更改维度]**&#x200B;活动，将目标维度从&#x200B;**[!UICONTROL 愿望清单]**&#x200B;切换为&#x200B;**[!UICONTROL 收件人]。**&#x200B;此步骤可确保精心策划的活动正确定向到与这些愿望清单关联的轮廓，从而将短信发送给预期的轮廓。

![](../assets/orchestrated-change-dimension-example.png)
