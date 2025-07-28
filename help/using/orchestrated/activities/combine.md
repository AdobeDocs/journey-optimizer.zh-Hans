---
solution: Journey Optimizer
product: journey optimizer
title: 使用“合并”活动
description: 了解如何使用“合并”活动
badge: label="Alpha"
hide: true
hidefromtoc: true
exl-id: af3c3a9c-8172-43b0-bba1-4a3d068b9a9e
source-git-commit: 3be1b238962fa5d0e2f47b64f6fa5ab4337272a5
workflow-type: tm+mt
source-wordcount: '1135'
ht-degree: 93%

---

# 合并 {#combine}

>[!CONTEXTUALHELP]
>id="ajo_orchestration_combine"
>title="合并活动"
>abstract="通过&#x200B;**合并**&#x200B;活动，可对集客群体执行分段。因此，您可以合并多个群体、排除其中的一部分或者仅保留多个目标共有的数据。"

+++ 目录

| 欢迎使用编排的营销活动 | 启动您的第一个编排的营销活动 | 查询数据库 | 精心策划的营销活动 |
|---|---|---|---|
| [开始使用协调的营销活动](../gs-orchestrated-campaigns.md)<br/><br/>创建和管理关系架构和数据集：</br> <ul><li>[架构和数据集入门](../gs-schemas.md)</li><li>[手动架构](../manual-schema.md)</li><li>[文件上载架构](../file-upload-schema.md)</li><li>[摄取数据](../ingest-data.md)</li></ul>[访问和管理编排的营销活动](../access-manage-orchestrated-campaigns.md) | [创建编排营销活动的关键步骤](../gs-campaign-creation.md)<br/><br/>[创建和计划营销活动](../create-orchestrated-campaign.md)<br/><br/>[编排活动](../orchestrate-activities.md)<br/><br/>[开始和监控营销活动](../start-monitor-campaigns.md)<br/><br/>[报告](../reporting-campaigns.md) | [使用规则生成器](../orchestrated-rule-builder.md)<br/><br/>[生成您的第一个查询](../build-query.md)<br/><br/>[编辑表达式](../edit-expressions.md)<br/><br/>[重定向](../retarget.md) | [活动快速入门](about-activities.md)<br/><br/>活动：<br/>[并行汇聚](and-join.md) - [生成受众](build-audience.md) - [更改维度](change-dimension.md) - [渠道活动](channels.md) - <b>[合并](combine.md)</b> - [重复数据删除](deduplication.md) - [扩充](enrichment.md) - [分叉](fork.md) - [协调](reconciliation.md) - [保存受众](save-audience.md) - [拆分](split.md) - [等待](wait.md) |

{style="table-layout:fixed"}

+++

<br/>

>[!BEGINSHADEBOX]

</br>

此页面上的内容不是最终内容，可能会发生变化。

>[!ENDSHADEBOX]

**[!UICONTROL 合并]**&#x200B;活动是一种&#x200B;**[!UICONTROL 目标选择]**&#x200B;活动，可以让您有效地对入站群体进行细分。利用该功能，可合并多个群体、排除特定区段或仅保留在多个目标之间共享的数据。

可以使用以下细分选项：

* **[!UICONTROL 并集]**：将多个活动的结果合并为单个统一目标。

* **[!UICONTROL 交叉]**：仅保留所有入站群体中共同的元素。

* **[!UICONTROL 排除]**：根据指定的条件，从一个群体中移除元素。

## 配置合并活动 {#combine-configuration}

>[!CONTEXTUALHELP]
>id="ajo_orchestration_intersection_merging_options"
>title="交叉合并选项"
>abstract="交集可仅在活动中保留不同集客群体的共有元素。在“要加入的集合”部分中，选中您之前希望加入的所有活动。"

>[!CONTEXTUALHELP]
>id="ajo_orchestration_exclusion_merging_options"
>title="排除合并选项"
>abstract="差集可根据特定条件从一个群体中排除某些元素。在“要加入的集合”部分中，选中您之前希望加入的所有活动。"

>[!CONTEXTUALHELP]
>id="ajo_orchestration_combine_options"
>title="选择分段类型"
>abstract="选择如何合并受众。**并集**&#x200B;可将多个活动的结果重组为单个目标。**交集**&#x200B;可仅在活动中保留不同集客群体的共有元素。**差集**&#x200B;可根据特定条件从一个群体中排除某些元素。 "

请按照以下常见步骤操作，开始配置&#x200B;**[!UICONTROL 合并]**&#x200B;活动：

![](../assets/orchestrated-union.png)

1. 添加多项活动（例如&#x200B;**[!UICONTROL 生成受众]**&#x200B;活动），来构成至少两个不同的执行分支。
1. 向先前的任何分支添加一个&#x200B;**[!UICONTROL 合并]**&#x200B;活动。
1. 选择分段类型：[并集](#union)、[交集](#intersection)或[差集](#exclusion)。
1. 单击&#x200B;**[!UICONTROL 继续]**。
1. 在&#x200B;**[!UICONTROL 要加入的集合]**&#x200B;部分中，选中您之前希望加入的所有活动。

## 并集 {#combine-union}

>[!CONTEXTUALHELP]
>id="ajo_orchestration_combine_reconciliation"
>title="协调选项"
>abstract="选择&#x200B;**协调类型**&#x200B;以定义如何处理重复项。默认情况下，**键**&#x200B;选项处于激活状态，这意味着当来自不同入站过渡的元素具有相同的键时，该活动仅会保留一个元素。使用&#x200B;**选择列**&#x200B;选项定义应用数据协调的列的列表。"

在&#x200B;**[!UICONTROL 合并]**&#x200B;活动中，您可以通过选择&#x200B;**[!UICONTROL 协调类型]**&#x200B;来配置&#x200B;**[!UICONTROL 并集]**，从而决定管理重复记录的方式：

* **[!UICONTROL 仅键]**（默认）：当多个入站过渡共享同一键时，将保留单个记录。仅当入站群体具有同样的性质时，才能使用此选项。

* **[!UICONTROL 列的选择]**：可以让您指定用于数据协调的列。选择&#x200B;**[!UICONTROL 添加属性]**。

在下面的示例中，同时使用&#x200B;**[!UICONTROL 合并]**&#x200B;活动与&#x200B;**[!UICONTROL 并集]**，以将两个查询的结果（**忠诚度会员**&#x200B;和&#x200B;**购买者**）合并到一个更大的受众中，包含两个区段中的轮廓。

![](../assets/orchestrated-union-example.png)

## 交集 {#combine-intersection}

>[!CONTEXTUALHELP]
>id="ajo_orchestration_intersection_reconciliation_options"
>title="交叉协调选项"
>abstract="选择&#x200B;**协调类型**&#x200B;以定义如何处理重复项。默认情况下，**键**&#x200B;选项处于激活状态，这意味着当来自不同入站过渡的元素具有相同的键时，该活动仅会保留一个元素。使用&#x200B;**选择列**&#x200B;选项定义应用数据协调的列的列表。"

在&#x200B;**[!UICONTROL 合并]**&#x200B;活动中，您可以配置&#x200B;**[!UICONTROL 交叉]**。为此，您需要执行以下额外步骤：

1. 选择&#x200B;**[!UICONTROL 协调类型]**，定义如何处理重复项。

   * **[!UICONTROL 仅键]**（默认）：当多个入站过渡共享同一键时，将保留单个记录。仅当入站群体具有同样的性质时，才能使用此选项。

   * **[!UICONTROL 列的选择]**：可以让您指定用于数据协调的列。选择&#x200B;**[!UICONTROL 添加属性]**。

1. 如果要处理其余群体，请启用&#x200B;**[!UICONTROL 生成补集]**。补集包含所有入站活动的并集减去交集的结果。一个额外的出站过渡将添加到活动中。

下方示例展示了两个查询活动之间的&#x200B;**[!UICONTROL 交叉]**&#x200B;的使用。这用于标识属于&#x200B;**忠诚会员**&#x200B;并在上个月内购买过产品的轮廓。

![](../assets/orchestrated-intersection-example.png)


## 差集 {#combine-exclusion}

>[!CONTEXTUALHELP]
>id="ajo_orchestration_exclusion_options"
>title="差集规则"
>abstract="必要时，您可以操作集客表。事实上，要从另一个维度排除一个目标，必须将该目标返回到与主目标相同的定位维度。为此，请单击“差集规则”部分中的“添加规则”，并指定维度更改条件。数据协调是通过属性或联接来执行的。"

>[!CONTEXTUALHELP]
>id="ajo_orchestration_combine_sets"
>title="选择要合并的集合"
>abstract="在&#x200B;**要加入的集合**&#x200B;部分中，从集客过渡中选择&#x200B;**主要设置**。这是排除了元素的集合。其他集合用于匹配从主要设置中排除之前的元素。"

>[!CONTEXTUALHELP]
>id="ajo_orchestration_combine_exclusion"
>title="差集规则"
>abstract="必要时，您可以操作集客表。事实上，要从另一个维度排除一个目标，必须将该目标返回到与主目标相同的定位维度。为此，请单击“差集规则”部分中的“添加规则”，并指定维度更改条件。数据协调是通过属性或联接来执行的。"

>[!CONTEXTUALHELP]
>id="ajo_orchestration_combine_complement"
>title="合并生成补集"
>abstract="开启“生成补集”选项以在额外的过渡中处理剩余群体。"

在&#x200B;**[!UICONTROL 合并]**&#x200B;活动中，您可以配置&#x200B;**[!UICONTROL 排除]**。为此，您需要执行以下额外步骤：

1. 在&#x200B;**[!UICONTROL 要加入的集]**&#x200B;部分中，选择代表主要群体的&#x200B;**[!UICONTROL 主集]**。在其他集中找到的记录将从此主集中排除。

1. 如果需要，您可以调整入站表以对齐不同维度的目标。要在另一个维度中排除某个目标，必须首先将其带回到与主要群体相同的目标维度。为此，请单击&#x200B;**[!UICONTROL 添加规则]**&#x200B;并定义更改维度的条件。然后，使用属性或联接进行协调。

1. 如果要处理剩余的群体，请启用&#x200B;**[!UICONTROL 生成补集]**。补集包含所有入站活动的并集减去交集的结果。一个额外的出站过渡将添加到活动中。

以下&#x200B;**[!UICONTROL 排除]**&#x200B;示例显示了两个查询，它们配置为筛选购买产品的轮廓。然后，从第一组集中排除不是忠诚会员的轮廓。

![](../assets/orchestrated-exclusion-example.png)

