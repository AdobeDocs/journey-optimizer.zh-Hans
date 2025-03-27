---
solution: Journey Optimizer
product: journey optimizer
title: 使用多步骤营销活动
description: 了解如何多步营销活动活动
hide: true
hidefromtoc: true
exl-id: 02f986b2-8200-4e0e-8918-44e528a6a3ec
source-git-commit: 323472ef9d6203cbbadc44ceb17ddcc7f6207323
workflow-type: tm+mt
source-wordcount: '452'
ht-degree: 27%

---

# 关于多步骤营销活动 {#ms-campaign-activities}

多步骤营销活动分为三类。 根据具体情况，可用的活动可能会有所不同。

以下各章节详细介绍了所有活动：

* [定位和数据管理活动](#targeting)
* [渠道活动](#channel)
* [流量控制活动](#flow-control)

![](../assets/workflow-activities.png)

## 定位活动 {#targeting}

这些活动特定于定位。 利用这些活动，您可以通过定义受众并使用交集、并集或差集操作来拆分或合并这些受众，从而构建一个或多个目标。

* [构建受众](build-audience.md)：定义目标群体。 您可以选择现有受众，也可以使用查询建模器定义您自己的查询。
* [更改维度](change-dimension.md)：在构建多步营销活动时更改定向维度。
* [合并](combine.md)：对入站群体执行分段。 您可以使用并集、交集或差集。
* [重复数据删除](deduplication.md)：删除集客活动结果中的重复项。
* [扩充](enrichment.md)：定义要在多步骤营销活动中处理的附加数据。 通过此活动，您可以应用集客过渡并配置活动以使用附加数据填写输出过渡。
* [协调](reconciliation.md)：定义Journey Optimizer数据中的数据与工作表中的数据（例如从外部文件加载的数据）之间的链接。
* [保存受众](save-audience.md)：更新现有受众，或从多步骤营销活动中上游计算的群体创建新受众。
* [拆分](split.md)：将传入的群体划分到多个子集中。

## 数据管理活动 {#data}

这些活动专门用于操纵和丰富人口数据。

* [加载文件](load-file.md)：使用存储在外部文件中的配置文件和数据。
* [更新数据](update-data.md)：对数据库中的字段执行批量更新。 您可以通过多个选项将数据更新个性化。

## 渠道活动 {#channel}

通过Adobe Journey Optimizer，您可以跨多个渠道自动执行营销活动。 您可以将渠道活动合并到画布中，以创建跨渠道多步骤营销活动，从而根据客户行为触发操作。 以下&#x200B;**渠道**&#x200B;活动可用：电子邮件、短信、Android和iOS推送通知。 [了解如何在多步骤营销活动的上下文中设置投放](channels.md)。

## 流量控制活动 {#flow-control}

>[!CONTEXTUALHELP]
>id="ajo_orchestration_end"
>title="结束活动"
>abstract="您可以使用&#x200B;**结束**&#x200B;活动，以图形方式标记多步骤营销活动的终点。此活动没有功能影响，因此是可选的。"

以下活动特定于组织和执行多步骤营销活动。 这些活动的主要任务是协调其他活动：

* [And — 加入](and-join.md)：同步多步骤营销活动的多个执行分支。
* **结束**：以图形方式标记多步骤营销活动的结束。 此活动对功能没有影响，因此是可选的
* [分支](fork.md)：创建叫客过渡以同时启动多个活动。
* [计划程序](scheduler.md)：在多步骤活动启动时进行计划。
* [测试](test.md)：根据指定的条件启用转换。
* [等待](wait.md)：暂时暂停执行多步骤营销活动的一部分。
