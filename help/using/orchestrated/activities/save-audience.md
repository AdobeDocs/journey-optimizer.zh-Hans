---
solution: Journey Optimizer
product: journey optimizer
title: 使用保存受众活动
description: 了解如何在编排的活动中使用保存受众活动
badge: label="Alpha"
hide: true
hidefromtoc: true
source-git-commit: 6439be00315dfde7ab385d7f848b7031d95060f4
workflow-type: tm+mt
source-wordcount: '473'
ht-degree: 3%

---

# 保存受众 {#save-audience}

+++ 目录

| 欢迎使用编排的营销活动 | 启动第一个精心策划的营销活动 | 查询数据库 | 精心策划的营销活动 |
|---|---|---|---|
| [开始使用协调的营销活动](gs-orchestrated-campaigns.md)<br/><br/>[配置步骤](configuration-steps.md)<br/><br/>[访问和管理协调的营销活动](access-manage-orchestrated-campaigns.md) | [创建编排营销活动的关键步骤](gs-campaign-creation.md)<br/><br/>[创建和计划营销活动](create-orchestrated-campaign.md)<br/><br/>[编排活动](orchestrate-activities.md)<br/><br/><b>[启动和监控营销活动](start-monitor-campaigns.md)</b><br/><br/>[报告](reporting-campaigns.md) | [使用规则生成器](orchestrated-rule-builder.md)<br/><br/>[生成您的第一个查询](build-query.md)<br/><br/>[编辑表达式](edit-expressions.md)<br/><br/>[重新定位](retarget.md) | [开始使用活动](activities/about-activities.md)<br/><br/>活动：<br/>[并加入](activities/and-join.md) - [生成受众](activities/build-audience.md) - [更改维度](activities/change-dimension.md) - [渠道活动](activities/channels.md) - [组合](activities/combine.md) - [重复数据删除](activities/deduplication.md) - [扩充](activities/enrichment.md) - [分支](activities/fork.md) - [协调](activities/reconciliation.md) - [保存受众](save-audience.md) - [拆分](activities/split.md) - [等待](activities/wait.md) |

{style="table-layout:fixed"}

+++

**[!UICONTROL 保存受众]**&#x200B;活动是一个&#x200B;**[!UICONTROL 定位]**&#x200B;活动，通过该活动可更新现有受众或利用之前在编排的营销活动中生成的群体创建新受众。 创建受众后，这些受众将添加到应用程序受众列表中，并可从&#x200B;**[!UICONTROL 受众]**&#x200B;菜单访问。

此活动对于保留在同一编排的营销活动中计算的受众区段特别有用，以便将来营销活动中重复使用。 它通常连接到其他定向活动，如&#x200B;**[!UICONTROL 构建受众]**&#x200B;或&#x200B;**[!UICONTROL 组合]**，以捕获并保存生成的群体。

## 配置保存受众活动 {#save-audience-configuration}

按照以下步骤配置&#x200B;**保存受众**&#x200B;活动：

1. 将&#x200B;**保存受众**&#x200B;活动添加到您的编排的营销活动中。

1. 在&#x200B;**模式**&#x200B;下拉列表中，选择要执行的操作：

   * **创建或更新现有受众**：定义&#x200B;**受众标签**。 如果受众已存在，则会更新受众；否则，将创建新受众。

   * **更新现有受众**：从现有受众列表中选择要更新的&#x200B;**受众**。

1. 选择应用于现有受众的&#x200B;**更新模式**：

   * **使用新数据替换受众内容**：所有受众内容都将被替换，旧数据将丢失。 仅保留&#x200B;**保存受众**&#x200B;活动的集客过渡中的数据。 此选项会清除已更新受众的受众类型和定向维度。

   * **使用新数据完成受众**：保留旧受众内容，并将来自&#x200B;**保存受众**&#x200B;活动的集客过渡的数据添加到旧受众内容中。

1. 如果要在&#x200B;**保存受众**&#x200B;活动之后添加过渡，请选中&#x200B;**生成叫客过渡**&#x200B;选项。

随后，受众的详细信息视图中会提供所保存受众的内容，可通过&#x200B;**受众**&#x200B;菜单访问该视图。 此视图中可用的列对应于编排的营销活动&#x200B;**保存受众**&#x200B;活动的集客过渡的列。

## 示例 {#save-audience-example}

下方的示例展示了如何通过定位进行简单的受众更新。 调度程序每月运行一次编排的活动。 查询可检索订阅了不同可用应用程序的所有用户档案。 **保存受众**&#x200B;活动可通过删除自上次协调的活动执行以来取消订阅服务的用户档案并添加新订阅的用户档案来更新受众。
