---
solution: Journey Optimizer
product: journey optimizer
title: 使用分支活动
description: 了解如何在编排的活动中使用分支活动
badge: label="Alpha"
hide: true
hidefromtoc: true
exl-id: 52e8057b-dac1-45f5-9dd0-1b28a59adde9
source-git-commit: 6439be00315dfde7ab385d7f848b7031d95060f4
workflow-type: tm+mt
source-wordcount: '222'
ht-degree: 30%

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

| 欢迎使用编排的营销活动 | 启动第一个精心策划的营销活动 | 查询数据库 | 精心策划的营销活动 |
|---|---|---|---|
| [开始使用协调的营销活动](gs-orchestrated-campaigns.md)<br/><br/>[配置步骤](configuration-steps.md)<br/><br/>[访问和管理协调的营销活动](access-manage-orchestrated-campaigns.md) | [创建编排营销活动的关键步骤](gs-campaign-creation.md)<br/><br/>[创建和计划营销活动](create-orchestrated-campaign.md)<br/><br/>[编排活动](orchestrate-activities.md)<br/><br/><b>[启动和监控营销活动](start-monitor-campaigns.md)</b><br/><br/>[报告](reporting-campaigns.md) | [使用规则生成器](orchestrated-rule-builder.md)<br/><br/>[生成您的第一个查询](build-query.md)<br/><br/>[编辑表达式](edit-expressions.md)<br/><br/>[重新定位](retarget.md) | [开始使用活动](activities/about-activities.md)<br/><br/>活动：<br/>[并加入](activities/and-join.md) - [生成受众](activities/build-audience.md) - [更改维度](activities/change-dimension.md) - [渠道活动](activities/channels.md) - [组合](activities/combine.md) - [重复数据删除](activities/deduplication.md) - [扩充](activities/enrichment.md) - [分支](activities/fork.md) - [协调](activities/reconciliation.md) - [保存受众](save-audience.md) - [拆分](activities/split.md) - [等待](activities/wait.md) |

{style="table-layout:fixed"}

+++

<br/>

**[!UICONTROL Fork]**&#x200B;活动是一个&#x200B;**[!UICONTROL 流控制]**&#x200B;组件，可让您创建多个叫客过渡，使多个活动能够并行运行。

## 配置分支活动{#fork-configuration}

请按照以下步骤操作，配置&#x200B;**[!UICONTROL 分叉]**&#x200B;活动：

![](../assets/workflow-fork.png)

1. 将&#x200B;**[!UICONTROL 分支]**&#x200B;活动添加到您的编排营销活动中。

1. 定义&#x200B;**[!UICONTROL 标签]**。

1. 为每个叫客过渡分配标签。 默认情况下，提供两个过渡。

1. 要删除过渡，请单击![](../assets/do-not-localize/Smock_Delete_18_N.svg)图标。

1. 如果需要，请单击&#x200B;**[!UICONTROL 添加过渡]**&#x200B;以添加其他出站过渡。
