---
solution: Journey Optimizer
product: journey optimizer
title: 使用组合活动
description: 了解如何使用组合活动
badge: label="Alpha"
hide: true
hidefromtoc: true
exl-id: af3c3a9c-8172-43b0-bba1-4a3d068b9a9e
source-git-commit: 38b65200435e0b997e79aefbb66549b9168188fd
workflow-type: tm+mt
source-wordcount: '1121'
ht-degree: 78%

---

# 合并 {#combine}

>[!CONTEXTUALHELP]
>id="ajo_orchestration_combine"
>title="合并活动"
>abstract="通过&#x200B;**合并**&#x200B;活动，可对集客群体执行分段。因此，您可以合并多个群体、排除其中的一部分或者仅保留多个目标共有的数据。"

+++ 目录

| 欢迎使用编排的营销活动 | 启动第一个精心策划的营销活动 | 查询数据库 | 精心策划的营销活动 |
|---|---|---|---|
| [开始使用编排的营销活动](../gs-orchestrated-campaigns.md)<br/><br/>[配置步骤](../configuration-steps.md)<br/><br/>[创建编排的营销活动的关键步骤](../gs-campaign-creation.md) | [创建协调的营销活动](../create-orchestrated-campaign.md)<br/><br/>[协调活动](../orchestrate-activities.md)<br/><br/>[发送包含协调的营销活动的消息](../send-messages.md)<br/><br/>[开始并监视营销活动](../start-monitor-campaigns.md)<br/><br/>[报告](../reporting-campaigns.md) | [使用查询Modeler](../orchestrated-rule-builder.md)<br/><br/>[生成您的第一个查询](../build-query.md)<br/><br/>[编辑表达式](../edit-expressions.md) | [开始使用活动](about-activities.md)<br/><br/>活动：<br/>[And-join](and-join.md) - [生成受众](build-audience.md) - [更改维度](change-dimension.md) - [组合](combine.md) - [重复数据删除](deduplication.md) - [扩充](enrichment.md) - [分支](fork.md) - [协调](reconciliation.md) - [拆分](split.md) - [等待](wait.md) |

{style="table-layout:fixed"}

+++

<br/>

**[!UICONTROL 合并]**&#x200B;活动是&#x200B;**[!UICONTROL 定位]**&#x200B;活动。 此活动允许对集客群体进行分段。因此，您可以合并多个群体、排除其中的一部分或者仅保留多个目标共有的数据。下面显示了可用的分段类型：

<!--
The **Combine** activity can be placed after any other activity, but not at the beginning of the workflow. Any activity can be placed after the **Combine**.
-->

* **[!UICONTROL 并集]**&#x200B;可将多个活动的结果重组为单个目标。
* **[!UICONTROL 交集]**&#x200B;可仅在活动中保留不同集客群体的共有元素。
* **[!UICONTROL 差集]**&#x200B;可根据特定条件从一个群体中排除某些元素。

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

![](../assets/workflow-combine.png)

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

在&#x200B;**[!UICONTROL 合并]**&#x200B;活动中，您可以配置&#x200B;**[!UICONTROL 合并]**。 为此，您需要选择&#x200B;**[!UICONTROL 协调类型]**&#x200B;以定义如何处理重复项：

* **[!UICONTROL 仅键值]**：这是默认模式。当来自不同集客过渡的元素具有相同的键值时，该活动只保留一个元素。仅当集客群体具有同样的性质时，才能使用此选项。
* **[!UICONTROL 选择的列]**：选择此选项可定义应用数据协调的列的列表。 必须先选择主集（包含源数据的集），然后选择用于连接的列。

## 交集 {#combine-intersection}

>[!CONTEXTUALHELP]
>id="ajo_orchestration_intersection_reconciliation_options"
>title="交叉协调选项"
>abstract="选择&#x200B;**协调类型**&#x200B;以定义如何处理重复项。默认情况下，**键**&#x200B;选项处于激活状态，这意味着当来自不同入站过渡的元素具有相同的键时，该活动仅会保留一个元素。使用&#x200B;**选择列**&#x200B;选项定义应用数据协调的列的列表。"

在&#x200B;**[!UICONTROL 合并]**&#x200B;活动中，您可以配置&#x200B;**[!UICONTROL 交叉点]**。 为此，您需要执行以下额外步骤：

1. 选择&#x200B;**[!UICONTROL 协调类型]**&#x200B;以定义如何处理重复项。请参阅[并集](#union)部分。
1. 如果您想处理剩余的人群，可以选中&#x200B;**[!UICONTROL 生成补集]**&#x200B;选项。补集将包含所有集客活动减去交集的结果的并集。然后，一个额外的叫客过渡将添加到活动中。

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

在&#x200B;**[!UICONTROL 合并]**&#x200B;活动中，您可以配置&#x200B;**[!UICONTROL 排除项]**。 为此，您需要执行以下额外步骤：

1. 在&#x200B;**[!UICONTROL 要加入的集合]**&#x200B;部分中，从集客过渡中选择&#x200B;**[!UICONTROL 主要设置]**。这是排除了元素的集合。其他集合用于匹配从主要设置中排除之前的元素。
1. 必要时，您可以操作集客表。事实上，要从另一个维度排除一个目标，必须将该目标返回到与主目标相同的定位维度。为此，请单击&#x200B;**[!UICONTROL 差集规则]**&#x200B;部分中的&#x200B;**[!UICONTROL 添加规则]**，并指定维度更改条件。数据协调是通过属性或联接来执行的。
1. 如果您想处理剩余的人群，可以选中&#x200B;**[!UICONTROL 生成补集]**&#x200B;选项。请参阅[交集](#intersection)部分。

## 示例{#combine-examples}

在以下示例中，我们使用&#x200B;**[!UICONTROL Combine]**&#x200B;活动并添加&#x200B;**[!UICONTROL Union]**&#x200B;以检索两个查询的所有用户档案：18至27岁的人和34至40岁的人。

![](../assets/workflow-union-example.png)

以下示例显示两个查询活动之间的&#x200B;**[!UICONTROL 交集]**。 此处使用它来检索年龄在 18 至 27 岁之间且已提供电子邮件地址的人员的轮廓。

![](../assets/workflow-intersection-example.png)

以下&#x200B;**[!UICONTROL 排除项]**&#x200B;示例显示了两个查询，配置为筛选18到27岁之间且具有Adobe电子邮件域的用户档案。 随后，具有 Adobe 电子邮件域的轮廓将从第一个集合中排除。

![](../assets/workflow-exclusion-example.png)
