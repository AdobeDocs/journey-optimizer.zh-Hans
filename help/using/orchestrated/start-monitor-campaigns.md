---
solution: Journey Optimizer
product: journey optimizer
title: 使用Adobe Journey Optimizer启动和监控编排的营销活动
description: 了解如何使用Adobe Journey Optimizer启动和监控编排的营销活动。
hide: true
hidefromtoc: true
exl-id: 5fc2d1d6-75c3-4b45-bb2b-09982b9bd5ed
source-git-commit: 445194fcc08efacdbf5f97a425d01229f82d11ea
workflow-type: tm+mt
source-wordcount: '677'
ht-degree: 9%

---

# 启动和监测精心策划的营销活动 {#start-monitor}

>[!CONTEXTUALHELP]
>id="ajo_campaign_publication"
>title="发布精心策划的营销活动"
>abstract="要开始您的营销活动，您必须发布它。确保在发布之前清除所有警告。"

+++ 目录

| 欢迎使用编排的营销活动 | 启动第一个精心策划的营销活动 | 查询数据库 | 精心策划的营销活动 |
|---|---|---|---|
| [开始使用协调的营销活动](gs-orchestrated-campaigns.md)<br/><br/>[配置步骤](configuration-steps.md)<br/>&lt;br/[访问和管理协调的营销活动](access-manage-orchestrated-campaigns.md) | [创建编排营销活动的关键步骤](gs-campaign-creation.md)<br/><br/>[创建和计划营销活动](create-orchestrated-campaign.md)<br/><br/>[编排活动](orchestrate-activities.md)<br/><br/>[发送包含编排营销活动的消息](send-messages.md)<br/><br/><b>[开始和监控营销活动](start-monitor-campaigns.md)</b><br/><br/>[报告](reporting-campaigns.md) | [使用规则生成器](orchestrated-rule-builder.md)<br/><br/>[生成您的第一个查询](build-query.md)<br/><br/>[编辑表达式](edit-expressions.md) | [开始使用活动](activities/about-activities.md)<br/><br/>活动：<br/>[And-join](activities/and-join.md) - [生成受众](activities/build-audience.md) - [更改维度](activities/change-dimension.md) - [组合](activities/combine.md) - [重复数据删除](activities/deduplication.md) - [扩充](activities/enrichment.md) - [分支](activities/fork.md) - [协调](activities/reconciliation.md) - [拆分](activities/split.md) - [等待](activities/wait.md) |

{style="table-layout:fixed"}

+++

<br/>

创建经过编排的任务并设计好要在画布中执行的任务后，您就可以发布它并监控其执行方式。

## 启动编排的营销活动 {#start}

要启动编排的营销活动，请导航到&#x200B;**[!UICONTROL 营销活动]**&#x200B;菜单的&#x200B;**[!UICONTROL 编排]**&#x200B;选项卡，选择要启动的营销活动，然后单击画布右上角的&#x200B;**[!UICONTROL 播放]**&#x200B;按钮。

运行编排的活动后，画布中的每个活动都会按顺序执行，直到达到编排的活动结束为止。

您可以使用可视流量实时跟踪目标用户档案的进度。 这允许您快速识别每个活动的状态以及它们之间转换的用户档案数。

![](assets/workflow-execution.png){zoomable="yes"}

在编排的活动中，通过过渡从一个活动传输到另一个活动的数据存储在临时工作表中。 可以为每个过渡显示此数据。 要实现此目的，请选择过渡以在屏幕右侧打开其属性。

* 单击&#x200B;**[!UICONTROL 预览架构]**&#x200B;以显示工作表的架构。
* 单击&#x200B;**[!UICONTROL 预览结果]**&#x200B;以可视化在所选过渡中传输的数据。

![](assets/transition.png){zoomable="yes"}

## 监测活动执行

### 监测活动执行 {#activities}

通过每个活动框右上角的视觉指示器，可检查其执行情况：

| 视觉指示器 | 描述 |
|-----|------------|
| ![](assets/activity-status-pending.png){zoomable="yes"}{width="70%"} | 当前正在执行活动。 |
| ![](assets/activity-status-orange.png){zoomable="yes"}{width="70%"} | 该活动需要您注意。 这可能涉及确认发送投放或采取必要操作。 |
| ![](assets/activity-status-red.png){zoomable="yes"}{width="70%"} | 活动遇到错误。 要解决此问题，请打开编排的活动日志以了解更多信息。 |
| ![](assets/activity-status-green.png){zoomable="yes"}{width="70%"} | 已成功执行活动。 |

### 监测日志和任务 {#logs-tasks}

>[!CONTEXTUALHELP]
>id="ajo_campaign_logs"
>title="日志和任务"
>abstract="**日志和任务**&#x200B;屏幕提供了精心策划的营销活动执行的历史记录，记录了所有用户操作和遇到的错误。"

监测日志和任务是分析编排的营销活动并确保其正常运行的关键步骤。 可从操作工具栏中提供的&#x200B;**[!UICONTROL 日志]**&#x200B;图标以及每个活动的属性窗格中访问它们。

**[!UICONTROL 日志和任务]**&#x200B;菜单提供编排的活动执行的历史记录，记录所有用户操作和遇到的错误。

![](assets/workflow-logs.png){zoomable="yes"}

提供了两种类型的信息：

* **[!UICONTROL 日志]**&#x200B;选项卡包含所有编排的营销活动的执行历史记录。 它按时间顺序对执行的操作和执行错误进行索引。
* **[!UICONTROL 任务]**&#x200B;选项卡详细列出了活动的执行顺序。

在这两个选项卡中，您可以选择显示的列及其顺序，应用过滤器，并使用搜索字段快速查找所需信息。

## 编排的活动执行命令 {#execution-commands}

右上角的操作栏提供了一些命令，允许您管理编排的活动执行。 您可以：

* **[!UICONTROL 开始]** / **[!UICONTROL 继续]**&#x200B;执行   经过编排的营销活动，该营销活动随后会呈现进行中状态。 如果暂停了编排的营销活动，则会恢复该营销活动，否则会启动该营销活动并激活初始活动。

* **[!UICONTROL 暂停]**&#x200B;执行编排的营销活动，该活动随后会呈现“已暂停”状态。 在恢复之前，不会激活任何新活动，但不会暂停正在进行的操作。

* **[!UICONTROL 停止]**&#x200B;正在执行的编排营销活动，该活动随后将呈现“已完成”状态。 如果可能，正在执行的操作会被中断。 您无法从已停止的同一位置恢复编排的营销活动。
