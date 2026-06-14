---
solution: Journey Optimizer
product: journey optimizer
title: 使用编排的营销活动
description: 了解如何编排营销活动
exl-id: 02f986b2-8200-4e0e-8918-44e528a6a3ec
version: Campaign Orchestration
TQID: https://experienceleague.adobe.com/OUKBJeSTaPJKav-NNCCxKZ8esY-62JkdRMmcwoJpZJ0
product_v2:
  - id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2:
  - id: b3538224-471e-4c63-a444-9b19d89ae29c
topic_v2:
  - id: b5ce8718-c3af-4fdb-a1a9-fca32f83a87c
subfeature_v2:
  - id: b5e335a9-0e5f-4dda-8845-c4ac5dca2be4
source-git-commit: 77cddc86596959e06b20154c1e51c6b84375b39b
workflow-type: tm+mt
source-wordcount: 551
ht-degree: 54%

---

# 关于编排的营销活动 {#orchestrated-campaign-activities}

>[!BEGINSHADEBOX]

**在此页面上：**&#x200B;了解画布上可用的定位、渠道和流量控制活动，以构建跨渠道编排的营销活动。

>[!ENDSHADEBOX]

精心策划的营销活动分为三类。 根据具体情况，可用的活动可能会有所不同。

以下各章节详细介绍了所有活动：

* [目标选择活动](#targeting)
* [渠道活动](#channel)
* [流程控制活动](#flow-control)

![画布中可用的活动列表](../assets/orchestrated-activities.png){width="80%"}

>[!NOTE]
>
>根据您的许可模式、权限和实施，可用活动可能会有所不同。

## 护栏和限制 {#activity-guardrails}

* **渠道活动限制** — 编排的营销活动在发布时最多支持10个渠道活动（电子邮件、短信、推送或直邮）。 定位和流量控制活动不计入此限制。

* **画布活动限制** — 画布上的活动数限制为500。 为了提高可维护性和性能，请将工作流限制在实践中的100个以内。

有关所有编排的活动护栏和限制，请参阅[护栏和限制](../guardrails.md)。

## 目标选择活动 {#targeting}

这些活动特定于目标选择。 利用这些活动，您可以通过定义受众并使用交叉、组合或排除操作来拆分或组合这些受众，从而生成一个或多个目标。

![目标选择活动列表](../assets/targeting-activities.png){width="40%"}

可用的定位活动包括：

* [生成受众](build-audience.md)：定义目标群体。 您可以选择现有受众或使用规则生成器来定义您自己的查询。
* [更改维度](change-dimension.md)：在构建编排的营销活动时更改定向维度。
* [合并](combine.md)：对入站群体执行细分。 您可以使用合并、交叉或排除。
* [重复数据删除](deduplication.md)：删除入站活动结果中的重复项。
* [扩充](enrichment.md)：定义要在您的编排营销活动中处理的附加数据。 通过此活动，您可以应用入站过渡并配置活动以使用其他数据完成输出过渡的设置。
* [协调](reconciliation.md)：定义 Journey Optimizer 数据与工作表数据（例如从外部文件加载的数据）之间的关联。
* [拆分](split.md)：将传入的群体划分到多个子集中。

## 渠道活动 {#channel}

Adobe Journey Optimizer 允许您跨多个渠道自动化和执行营销活动。 您可以将[渠道活动](channels.md)合并到画布中，以创建可以根据客户行为触发操作的跨渠道编排营销活动。

了解如何[在编排的营销活动](channels.md)中创建渠道操作。

## 流程控制活动 {#flow-control}

>[!CONTEXTUALHELP]
>id="ajo_orchestration_end"
>title="结束活动"
>abstract="**结束**&#x200B;活动用于标记画布中某个分支的结束。 您还可以使用&#x200B;**外部信号**&#x200B;在分支完成时启动下游编排营销活动并传递参数。 [了解详情](../trigger-orchestrated-campaign.md#signal-end)"

>[!CONTEXTUALHELP]
>id="ajo_orchestration_signal"
>title="外部信号"
>abstract="选择在此分支结束时启动的下游编排营销活动，并映射要在信号中发送的参数名称和值。 下游营销活动必须设置为&#x200B;**由信号触发**，并在此营销活动到达“结束”活动之前发布。 [了解详情](../trigger-orchestrated-campaign.md#signal-end)"

以下活动特定于组织和执行编排的营销活动。 他们的主要任务是协调其他活动。

![流程控制活动列表](../assets/flow-control-activities.png){width="20%"}

可用的流量控制活动包括：

* [And-join](and-join.md)：同步编排营销活动的多个执行分支。
* [分叉](fork.md)：创建出站过渡以同时启动多个活动。
* [等待](wait.md)：暂时暂停执行编排营销活动的一部分。
  <!--* [Test](test.md): Enable transitions based on specified conditions.-->

* **[!UICONTROL End]**：标记画布上分支的结尾。 您可以选择使用此插件向另一个根据信号启动的编排活动发送信号。 [了解详情](../trigger-orchestrated-campaign.md#signal-end)
