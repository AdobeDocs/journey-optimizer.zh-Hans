---
solution: Journey Optimizer
product: journey optimizer
title: 使用“分叉”活动
description: 了解如何在精心策划的营销活动中使用“分叉”活动
badge: label="Alpha"
hide: true
hidefromtoc: true
exl-id: 52e8057b-dac1-45f5-9dd0-1b28a59adde9
source-git-commit: 1a9ea09fcbf304b1649a5ae88da34bd209e9ac8b
workflow-type: tm+mt
source-wordcount: '255'
ht-degree: 82%

---

# 分叉 {#fork}

>[!CONTEXTUALHELP]
>id="ajo_orchestration_fork"
>title="分叉活动"
>abstract="利用&#x200B;**分叉**&#x200B;活动，可创建叫客过渡以同时开始若干活动。"

>[!CONTEXTUALHELP]
>id="ajo_orchestration_fork_transitions"
>title="分叉活动过渡"
>abstract="默认情况下，使用&#x200B;**分叉**&#x200B;活动创建两个过渡。单击&#x200B;**添加过渡**&#x200B;按钮以定义其他叫客过渡并输入其标签。"

+++ 目录

| 欢迎了解精心策划的营销活动 | 启动第一个精心策划的营销活动 | 查询数据库 | 精心策划的营销活动 |
|---|---|---|---|
| [开始使用编排的营销活动](../gs-orchestrated-campaigns.md)<br/><br/>创建和管理关系架构和数据集：</br> <ul><li>[架构和数据集入门](../gs-schemas.md)</li><li>[手动架构](../manual-schema.md)</li><li>[文件上载架构](../file-upload-schema.md)</li><li>[摄取数据](../ingest-data.md)</li></ul>[访问和管理编排的营销活动](../access-manage-orchestrated-campaigns.md) | [创建精心策划的营销活动的关键步骤](../gs-campaign-creation.md)<br/><br/>[创建和计划营销活动](../create-orchestrated-campaign.md)<br/><br/>[精心策划活动](../orchestrate-activities.md)<br/><br/>[启动和监控营销活动](../start-monitor-campaigns.md)<br/><br/>[报告](../reporting-campaigns.md) | [使用规则生成器](../orchestrated-rule-builder.md)<br/><br/>[生成您的第一个查询](../build-query.md)<br/><br/>[编辑表达式](../edit-expressions.md)<br/><br/>[重定向](../retarget.md) | [活动快速入门](about-activities.md)<br/><br/>活动：<br/>[并行汇聚](and-join.md) - [生成受众](build-audience.md) - [更改维度](change-dimension.md) - [渠道活动](channels.md) - [合并](combine.md) - [重复数据删除](deduplication.md) - [扩充](enrichment.md) - <b>[分叉](fork.md)</b> - [协调](reconciliation.md) - [保存受众](save-audience.md) - [拆分](split.md) - [等待](wait.md) |

{style="table-layout:fixed"}

+++


<br/>

>[!BEGINSHADEBOX]

</br>

此页面上的内容不是最终内容，可能会发生变化。

>[!ENDSHADEBOX]

**[!UICONTROL 分叉]**&#x200B;活动是一个&#x200B;**[!UICONTROL 流程控制]**&#x200B;组件，可用于创建多个出站过渡，实现多个活动的并行运行。

## 配置“分叉”活动{#fork-configuration}

请按照以下步骤操作，配置&#x200B;**[!UICONTROL 分叉]**&#x200B;活动：

![](../assets/workflow-fork.png)

1. 向精心策划的营销活动添加一个&#x200B;**[!UICONTROL 分叉]**&#x200B;活动。

1. 定义一个&#x200B;**[!UICONTROL 标签]**。

1. 为每个出站过渡分配标签。默认提供两个过渡。

1. 要移除过渡，请单击 ![](../assets/do-not-localize/Smock_Delete_18_N.svg) 图标。

1. 如果需要，请单击&#x200B;**[!UICONTROL 添加过渡]**&#x200B;以添加其他出站过渡。
