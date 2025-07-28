---
solution: Journey Optimizer
product: journey optimizer
title: 访问和管理编排的营销活动
description: 了解使用Adobe Journey Optimizer创建编排营销活动的主要原则
badge: label="Alpha"
hide: true
hidefromtoc: true
exl-id: 7b42d317-cd01-4c6a-b61e-5b03e5a8ff3c
source-git-commit: 3be1b238962fa5d0e2f47b64f6fa5ab4337272a5
workflow-type: tm+mt
source-wordcount: '723'
ht-degree: 48%

---

# 访问和管理编排的营销活动 {#orchestrated-campaign-creation}

>[!CONTEXTUALHELP]
>id="ajo_targeting_workflow_list"
>title="协同营销活动"
>abstract="在此屏幕中，您可以访问编排的营销活动的完整列表，检查其当前状态、上次/下次执行日期，以及创建新的编排的营销活动。"

>[!CONTEXTUALHELP]
>id="ajo_orchestration_campaign_action"
>title="操作"
>abstract="本节列出了在编排的营销策划中使用的所有操作。"

+++ 目录

| 欢迎使用编排的营销活动 | 启动您的第一个编排的营销活动 | 查询数据库 | 精心策划的营销活动 |
|---|---|---|---|
| [开始使用协调的营销活动](gs-orchestrated-campaigns.md)<br/><br/>创建和管理关系架构和数据集：</br> <ul><li>[架构和数据集入门](gs-schemas.md)</li><li>[手动架构](manual-schema.md)</li><li>[文件上载架构](file-upload-schema.md)</li><li>[摄取数据](ingest-data.md)</li></ul><br/><br/><b>[访问和管理编排的营销活动](access-manage-orchestrated-campaigns.md)</b><br/><br/>[创建编排的营销活动的关键步骤](gs-campaign-creation.md) | [创建和计划营销活动](create-orchestrated-campaign.md)<br/><br/>[精心策划活动](orchestrate-activities.md)<br/><br/>[启动和监控营销活动](start-monitor-campaigns.md)<br/><br/>[报告](reporting-campaigns.md) | [使用规则生成器](orchestrated-rule-builder.md)<br/><br/>[生成您的第一个查询](build-query.md)<br/><br/>[编辑表达式](edit-expressions.md)<br/><br/>[重定向](retarget.md) | [活动快速入门](activities/about-activities.md)<br/><br/>活动：<br/>[并行汇聚](activities/and-join.md) - [生成受众](activities/build-audience.md) - [更改维度](activities/change-dimension.md) - [渠道活动](activities/channels.md) - [合并](activities/combine.md) - [重复数据删除](activities/deduplication.md) - [扩充](activities/enrichment.md) - [分叉](activities/fork.md) - [协调](activities/reconciliation.md) - [保存受众](activities/save-audience.md) - [拆分](activities/split.md) - [等待](activities/wait.md) |

{style="table-layout:fixed"}

+++

<br/>

>[!BEGINSHADEBOX]

</br>

此页面上的内容不是最终内容，可能会发生变化。

>[!ENDSHADEBOX]

## 访问编排的营销活动

导航到&#x200B;**[!UICONTROL 营销活动]**&#x200B;菜单并选择&#x200B;**[!UICONTROL 编排]**&#x200B;选项卡以访问编排的营销活动的完整列表。

![显示编排的营销活动库存的图像](assets/inventory.png){zoomable="yes"}{zoomable="yes"}

列表中的每个编排营销活动都会显示相关信息，例如营销活动的当前[状态](#status)、关联的渠道和标记，或上次修改营销活动的时间。 您可以通过单击![配置布局按钮](assets/do-not-localize/inventory-configure-layout.svg)来自定义显示的列。

此外，还可使用搜索栏和过滤器，以便在列表中轻松搜索。例如，您可以对编排的营销活动进行筛选，以仅显示与给定渠道或标记关联的营销活动，或显示在特定日期范围内创建的营销活动。

可通过使用营销活动清单中的 ![显示“更多操作”按钮的图像](assets/do-not-localize/rule-builder-icon-more.svg) 按钮执行下文详述的各项操作。

![营销活动清单图像](assets/inventory-actions.png)

* **[!UICONTROL 查看所有时间报告]**/**[!UICONTROL 查看过去 24 小时报告]** - 访问报告以衡量和可视化精心策划的营销活动的影响和表现。[了解更多有关协调营销活动报告的信息](../orchestrated/reporting-campaigns.md)
* **[!UICONTROL 编辑标记]** - 编辑与营销活动关联的标记。
* **[!UICONTROL 复制]** — 在某些情况下，您可能需要复制编排的营销活动，例如，执行已停止的营销活动，或更改计划营销活动的执行频率。
* **[!UICONTROL 删除]** - 删除营销活动。此操作仅适用于&#x200B;**[!UICONTROL 草稿]**&#x200B;营销活动。
* **[!UICONTROL 存档]** - 对营销活动进行存档。按照滚动的重新安排，所有存档的营销活动将在上次修改日期的 30 天后删除。此操作适用于除&#x200B;**[!UICONTROL 草稿]**&#x200B;营销活动之外的所有营销活动。

## 精心策划的营销活动包含哪些内容？ {#gs-ms-campaign-inside}

精心策划的竞选活动画布代表了将要发生的事情。 它描述要执行的各种任务及其如何关联在一起。

![图像显示编排的活动画布](assets/canvas-example.png)

每个编排的活动都包含：

* **活动**：活动是要执行的任务。在图上用图标表示各种活动。每个活动都有特定属性和所有活动共有的其他属性。

  在编排的活动图中，给定活动可以生成多个任务，尤其是存在循环或重复操作时。

* **过渡**：过渡将源活动链接到目标活动并定义它们的顺序。

* **工作表**：工作表包含了过渡所携带的所有信息。每个编排的活动都使用几个工作表。 这些表中传送的数据可在整个编排营销活动的生命周期中使用。

## 营销活动状态 {#status}

精心策划的营销活动可以有多种状态：

* **[!UICONTROL 草稿]**：已创建编排的营销活动。 它尚未发布。
* **[!UICONTROL 发布]**：正在发布编排的营销活动。
* **[!UICONTROL 实时]**：已发布并正在执行编排的营销活动。
* **[!UICONTROL 已计划]**：已计划执行编排的营销活动。
* **[!UICONTROL 已完成]**：协调的活动执行已完成。 当营销活动完成消息发送且无错误后，系统将在 3 天内自动将其状态标记为已完成。
* **[!UICONTROL 已关闭]**：当定期营销活动已关闭时，系统将显示此状态。营销活动会继续执行直至其所有活动均已完成，但不再允许新的轮廓进入营销活动。
* **[!UICONTROL 已存档]**：已存档编排的营销活动。 按照滚动的重新安排，所有存档的营销活动将在上次修改日期的 30 天后删除。如需继续使用，您可以复制已存档的营销活动。
* **[!UICONTROL 已停止]**：已停止执行编排的营销活动。 要再次启动营销活动，您需要复制它。
