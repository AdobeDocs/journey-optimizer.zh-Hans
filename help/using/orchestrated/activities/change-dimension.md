---
solution: Journey Optimizer
product: journey optimizer
title: 使用更改维度活动
description: 了解如何使用更改维度活动
badge: label="Alpha"
hide: true
hidefromtoc: true
exl-id: 83e66f10-93dd-4759-840c-2c83abc42a28
source-git-commit: 32b13d4fd62abc8052c1bf64d8a2d5e97bd0f464
workflow-type: tm+mt
source-wordcount: '408'
ht-degree: 19%

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

| 欢迎使用编排的营销活动 | 启动您的第一个编排的营销活动 | 查询数据库  | 编排的营销活动活动 |
|---|---|---|---|
| [开始使用编排的营销活动](../gs-orchestrated-campaigns.md)<br/><br/>[配置步骤](../configuration-steps.md)<br/><br/>[创建编排的营销活动的关键步骤](../gs-campaign-creation.md) | [创建协调的营销活动](../create-orchestrated-campaign.md)<br/><br/>[协调活动](../orchestrate-activities.md)<br/><br/>[发送包含协调的营销活动的消息](../send-messages.md)<br/><br/>[开始并监视营销活动](../start-monitor-campaigns.md)<br/><br/>[报告](../reporting-campaigns.md) | [使用查询Modeler](../orchestrated-query-modeler.md)<br/><br/>[生成您的第一个查询](../build-query.md)<br/><br/>[编辑表达式](../edit-expressions.md) | [开始使用活动](about-activities.md)<br/><br/>活动：<br/>[And-join](and-join.md) - [生成受众](build-audience.md) - [更改维度](change-dimension.md) - [组合](combine.md) - [重复数据删除](deduplication.md) - [扩充](enrichment.md) - [分支](fork.md) - [协调](reconciliation.md) - [拆分](split.md) - [等待](wait.md) |

{style="table-layout:fixed"}

+++

<br/><br/>

作为营销人员，您可以在编排的营销活动中将定向维度从一个实体切换到另一个关联的实体，并根据不同的数据集优化受众定位，例如，从分析用户更改为定向其特定操作或预订。

要执行此操作，请使用&#x200B;**更改维度**&#x200B;定位活动。 利用此活动，可在构建编排的营销活动时更改定向维度。 它根据数据模板和输入维度移动轴。

例如，您可以将编排营销活动的目标维度从“用户档案”切换为“合同”，以便向目标合同所有者发送消息。

<!--
>[!IMPORTANT]
>
>Please note that the **[!UICONTROL Change Dimension]** and **[!UICONTROL Change Data source]** activities should not be added in one row. If you need to use both activities consecutively, make sure you include an **[!UICONTROL Enrichement]** activity in between them. This ensures proper execution and prevents potential conflicts or errors.-->

## 配置更改维度活动 {#configure}

按照以下步骤配置&#x200B;**更改维度**&#x200B;活动：

1. 将&#x200B;**更改维度**&#x200B;活动添加到您的编排的营销活动中。

   ![](../assets/change-dimension.png)

1. 定义&#x200B;**新目标维度**。 在维度更改期间，将保留所有记录。

1. 执行编排的活动以查看结果。 比较更改维度活动之前和之后表中的数据，并比较编排的活动表的结构。

## 示例 {#example}

在本例中，我们希望向所有已购买的用户档案发送短信投放。 为此，我们首先使用链接到自定义“购买”定向维度的&#x200B;**[!UICONTROL 构建受众]**&#x200B;活动来定向发生的所有购买。

然后，我们使用&#x200B;**[!UICONTROL 更改维度]**&#x200B;活动将编排的活动定向维度切换为“收件人”。 这样，我们便能够定位匹配查询的收件人。

![](../assets/change-dimension-example.png)
