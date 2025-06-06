---
solution: Journey Optimizer
product: journey optimizer
title: 使用规则生成器
description: 了解如何为您的编排的活动创建规则
badge: label="Alpha"
hide: true
hidefromtoc: true
exl-id: fb7a0eb2-b2ff-49fa-af1f-f1c10f219b00
source-git-commit: 72bceb03a3e94b0f3c13dddb22c8d3b4de0fcb44
workflow-type: tm+mt
source-wordcount: '303'
ht-degree: 4%

---


# 使用规则生成器 {#orchestrated-rule-builder}

+++ 目录

| 欢迎使用编排的营销活动 | 启动您的第一个编排的营销活动 | 查询数据库  | 编排的营销活动活动 |
|---|---|---|---|
| [开始使用编排的营销活动](gs-orchestrated-campaigns.md)<br/><br/>[配置步骤](configuration-steps.md)<br/><br/>[创建编排的营销活动的关键步骤](gs-campaign-creation.md) | [创建协调的营销活动](create-orchestrated-campaign.md)<br/><br/>[协调活动](orchestrate-activities.md)<br/><br/>[发送包含协调的营销活动的消息](send-messages.md)<br/><br/>[开始并监视营销活动](start-monitor-campaigns.md)<br/><br/>[报告](reporting-campaigns.md) | [使用规则生成器](orchestrated-rule-builder.md)<br/><br/>[生成您的第一个查询](build-query.md)<br/><br/>[编辑表达式](edit-expressions.md) | [开始使用活动](activities/about-activities.md)<br/><br/>活动：<br/>[And-join](activities/and-join.md) - [生成受众](activities/build-audience.md) - [更改维度](activities/change-dimension.md) - [组合](activities/combine.md) - [重复数据删除](activities/deduplication.md) - [扩充](activities/enrichment.md) - [分支](activities/fork.md) - [协调](activities/reconciliation.md) - [拆分](activities/split.md) - [等待](activities/wait.md) |

{style="table-layout:fixed"}

+++

<br/>

编排的营销活动附带规则生成器，可简化根据各种标准筛选数据库的过程。 规则生成器可以高效地管理非常复杂和长的查询，从而提供增强的灵活性和精确度。

它还支持条件中的预定义过滤器，使用户能够轻松优化查询，同时利用高级表达式和运算符实现全面的受众定位和分段策略。

## 访问规则生成器

在&#x200B;**[!UICONTROL 构建受众]**&#x200B;活动中构建查询以定位受众时，可以使用规则生成器。 它允许您指定要定位的群体，并根据您的需求轻松地创建新受众。

![图像显示生成受众活动](assets/rule-builder-query.png)

## 规则生成器界面 {#interface}

规则生成器提供了一个中央画布（可在其中生成查询）和一个属性窗格（提供有关规则的信息）。

![显示规则生成器界面的图像](assets/rule-builder-interface.png)

* **中央画布**&#x200B;是您添加和组合不同组件以构建规则的地方。 [了解如何构建规则](../orchestrated/build-query.md)

* **[!UICONTROL 规则属性]**&#x200B;窗格提供有关规则的信息。 它允许您执行各种操作来检查规则并确保它符合您的需求。

  构建查询以创建受众时，显示此窗格。 [了解如何检查和验证您的查询](build-query.md#check-and-validate-your-query)
