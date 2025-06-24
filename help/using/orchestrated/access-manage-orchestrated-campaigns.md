---
solution: Journey Optimizer
product: journey optimizer
title: 访问并管理编排式营销活动
description: 了解使用Adobe Journey Optimizer编排活动创建的主要原则
badge: label="Alpha"
hide: true
hidefromtoc: true
exl-id: 7b42d317-cd01-4c6a-b61e-5b03e5a8ff3c
source-git-commit: 7e378cbda6ee2379a8bd795588c328cb14107aa4
workflow-type: tm+mt
source-wordcount: '637'
ht-degree: 21%

---

# 访问并管理编排式营销活动 {#orchestrated-campaign-creation}

>[!CONTEXTUALHELP]
>id="ajo_targeting_workflow_list"
>title="协同营销活动"
>abstract="在此屏幕中可访问协同营销活动的完整列表，查看其当前状态、上次/下次执行日期，并创建新的协同营销活动。"

>[!CONTEXTUALHELP]
>id="ajo_orchestration_campaign_action"
>title="操作"
>abstract="本节列出了在编排的活动中使用的所有操作。"

+++ 目录

| 欢迎使用编排的营销活动 | 启动第一个精心策划的营销活动 | 查询数据库 | 精心策划的营销活动 |
|---|---|---|---|
| [开始使用编排的营销活动](gs-orchestrated-campaigns.md)<br/><br/>[配置步骤](configuration-steps.md)<br/><br/><b>[访问和管理编排的营销活动](access-manage-orchestrated-campaigns.md)</b> | [创建编排营销活动的关键步骤](gs-campaign-creation.md)<br/><br/>[创建和计划营销活动](create-orchestrated-campaign.md)<br/><br/>[编排活动](orchestrate-activities.md)<br/><br/>[发送包含编排营销活动的消息](send-messages.md)<br/><br/>[开始和监控营销活动](start-monitor-campaigns.md)<br/><br/>[报告](reporting-campaigns.md) | [使用规则生成器](orchestrated-rule-builder.md)<br/><br/>[生成您的第一个查询](build-query.md)<br/><br/>[编辑表达式](edit-expressions.md) | [开始使用活动](activities/about-activities.md)<br/><br/>活动：<br/>[And-join](activities/and-join.md) - [生成受众](activities/build-audience.md) - [更改维度](activities/change-dimension.md) - [组合](activities/combine.md) - [重复数据删除](activities/deduplication.md) - [扩充](activities/enrichment.md) - [分支](activities/fork.md) - [协调](activities/reconciliation.md) - [拆分](activities/split.md) - [等待](activities/wait.md) |

{style="table-layout:fixed"}

+++

<br/>

## 访问编排的营销活动

导航到&#x200B;**[!UICONTROL 营销活动]**&#x200B;菜单并选择&#x200B;**[!UICONTROL 编排]**&#x200B;选项卡以访问编排的营销活动的完整列表。

![显示编排的营销活动清单的图像](assets/inventory.png){zoomable="yes"}{zoomable="yes"}

列表中的每个编排营销活动都会显示相关信息，例如营销活动的当前[状态](#status)、关联的渠道和标记，或上次修改营销活动的时间。 您可以通过单击![配置布局按钮](assets/do-not-localize/inventory-configure-layout.svg)按钮自定义显示的列。

此外，还可使用搜索栏和过滤器以便在列表中轻松搜索。例如，您可以筛选编排的营销活动以仅显示与给定渠道或标记关联的营销活动，或显示在特定日期范围内创建的营销活动。

## 精心策划的活动包含哪些内容？ {#gs-ms-campaign-inside}

精心设计的竞选画布是预期结果的呈现。 它描述要执行的各种任务及其如何链接在一起。

![图像显示编排的活动画布](assets/canvas-example.png){zoomable="yes"}{zoomable="yes"}

每个编排的活动都包含：

* **活动**：活动是要执行的任务。在图上用图标表示各种活动。每个活动都有特定属性和所有活动共有的其他属性。

  在编排的活动图表中，给定活动可以生成多个任务，尤其是存在循环或重复操作时。

* **过渡**：过渡将源活动链接到目标活动并定义它们的顺序。

* **工作表**：工作表包含了过渡所携带的所有信息。每个编排的活动都使用几个工作表。 这些表中传送的数据可在整个编排的促销活动生命周期中使用。

## 营销活动状态 {#status}

编排的活动可以具有多种状态：

循环开始于执行者，fait une查询。单击close： va continuer et se termienr quand elle sera allée jusqu&#39;au bout du diagram


* **[!UICONTROL 草稿]**：已创建编排的营销活动。 它尚未发布。
* **[!UICONTROL 正在发布]**：正在发布编排的营销活动。
* **[!UICONTROL 实时]**：编排的活动已发布并正在执行。
* **[!UICONTROL 已计划]**：已计划协调的活动执行。
* **[!UICONTROL 已完成]**：编排的活动执行已完成。 在营销活动完成消息发送且无错误后，最多可在3天内自动分配“已完成”状态。
* **[!UICONTROL 已关闭]**：当定期营销活动已停止时，将显示此状态。
<!--Comment une campaign devient Closed?
[CPR] : A vérifier avec Fred si cette fonctionalité est toujours d'actualité. Normalement c'est sur action de l'utilisateur sur une campaine récurrente only
= pas trouvé--> cexui qsui sont déjà entrés ocnitnuent. on ferme les portes d'entrée.

* **[!UICONTROL 已存档]**：已存档编排的营销活动。 所有已存档的营销活动都将在上次修改日期后30天滚动重新计划删除。 您可以根据需要复制已存档的活动以继续处理。
<!--Comment une campaign devient Archived?
[CPR] : Soit par action manuel sur une campagne en statut "final" (Completed, Closed, Stopped, etc. ...) bouton bientôt visible. possible pour tout sauf les draft.
= pas trouvé -->
* **[!UICONTROL 已停止]**：编排的活动执行已停止。 要再次启动营销活动，您需要复制它。 错误，restera avec三角

## 复制和删除编排的营销活动 {#duplicate-delete}

在某些情况下，您可能需要复制编排好的营销活动，例如执行已停止的营销活动，或更改计划营销活动的执行频率。 为此，请单击营销活动清单中显示“更多操作”按钮![&#128279;](assets/do-not-localize/rule-builder-icon-more.svg)按钮的图像，然后选择&#x200B;**[!UICONTROL 复制]**

<!--Une fois une campaign Scheduled, on ne peut plus changer l'execution frequency = la solution est de dupliquer la campaign ?
[CPR] : Actuellement oui, mais on est en discussion pour pouvoir revenir en mode "draft" et quelles seraient les actions à nouveau disponibles. A vérifier avec Fred-->

要删除营销活动，请单击显示更多操作按钮![&#128279;](assets/do-not-localize/rule-builder-icon-more.svg)按钮的图像，然后选择&#x200B;**[!UICONTROL 删除]**。

>[!NOTE]
>
>只能删除&#x200B;**[!UICONTROL 草稿]**&#x200B;营销活动。
