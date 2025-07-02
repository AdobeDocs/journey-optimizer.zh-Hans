---
solution: Journey Optimizer
product: journey optimizer
title: 使用Adobe Journey Optimizer启动和监控编排的营销活动
description: 了解如何使用Adobe Journey Optimizer启动和监控编排的营销活动。
hide: true
hidefromtoc: true
exl-id: 5fc2d1d6-75c3-4b45-bb2b-09982b9bd5ed
source-git-commit: d8b83bc46526f721d4dfaf62cf8ba4cbf5a56ce7
workflow-type: tm+mt
source-wordcount: '667'
ht-degree: 6%

---

# 启动和监测精心策划的营销活动 {#start-monitor}

>[!CONTEXTUALHELP]
>id="ajo_campaign_publication"
>title="发布精心策划的营销活动"
>abstract="要开始您的营销活动，您必须发布它。确保在发布之前清除所有警告。"

+++ 目录

| 欢迎使用编排的营销活动 | 启动第一个精心策划的营销活动 | 查询数据库 | 精心策划的营销活动 |
|---|---|---|---|
| [开始使用协调的营销活动](gs-orchestrated-campaigns.md)<br/><br/>[配置步骤](configuration-steps.md)<br/><br/>[访问和管理协调的营销活动](access-manage-orchestrated-campaigns.md) | [创建编排营销活动的关键步骤](gs-campaign-creation.md)<br/><br/>[创建和计划营销活动](create-orchestrated-campaign.md)<br/><br/>[编排活动](orchestrate-activities.md)<br/><br/><b>[启动和监控营销活动](start-monitor-campaigns.md)</b><br/><br/>[报告](reporting-campaigns.md) | [使用规则生成器](orchestrated-rule-builder.md)<br/><br/>[生成您的第一个查询](build-query.md)<br/><br/>[编辑表达式](edit-expressions.md) | [开始使用活动](activities/about-activities.md)<br/><br/>活动：<br/>[并加入](activities/and-join.md) - [生成受众](activities/build-audience.md) - [更改维度](activities/change-dimension.md) - [渠道活动](activities/channels.md) - [组合](activities/combine.md) - [重复数据删除](activities/deduplication.md) - [扩充](activities/enrichment.md) - [分支](activities/fork.md) - [协调](activities/reconciliation.md) - [拆分](activities/split.md) - [等待](activities/wait.md) |

{style="table-layout:fixed"}

+++

<br/>

创建经过编排的任务并设计好要在画布中执行的任务后，您就可以发布它并监控其执行方式。

您还可以在测试模式下执行营销活动，以检查其执行和不同活动的结果。

## 发布前测试活动 {#test}

Journey Optimizer允许您在启动之前测试编排的营销活动。 在测试模式下，将执行画布中的所有活动，但&#x200B;**[!UICONTROL 保存受众]**&#x200B;活动和渠道活动除外。 不会对您的数据或受众产生功能影响。

要测试活动，请执行以下操作：

1. 打开编排的营销活动。
2. 单击&#x200B;**[!UICONTROL 开始]**。

![](assets/campaign-start.png){zoomable="yes"}

营销活动中的每个活动都按顺序执行，直到到达图表末尾。 在测试执行期间，您可以使用画布中的操作栏管理营销活动。 从那里，您可以：

* 随时停止&#x200B;**执行**。
* **再次开始**&#x200B;执行。
* **恢复**&#x200B;执行（如果先前由于问题而暂停）。

如果在执行过程中出现错误或警告，您会通过画布工具栏中的&#x200B;**[!UICONTROL 警报]** / **[!UICONTROL 警告]**&#x200B;图标收到通知。

![](assets/campaign-warning.png){zoomable="yes"}

您还可以使用直接显示在每个活动上的[可视状态指示器](#activities)快速识别失败的活动。 有关详细的疑难解答，请打开[营销活动的日志](#logs-tasks)，其中提供了有关错误及其上下文的深入信息。

## 发布营销活动 {#publish}

测试营销活动并准备就绪后，单击&#x200B;**[!UICONTROL 发布]**&#x200B;以使其上线。

![](assets/campaign-publish.png){zoomable="yes"}

视觉流量重新启动，并且真实配置文件开始实时流过历程。

## 监测活动执行 {#monitor}

### 可视流量监控 {#flow}

在运行时（在测试或实时模式下），可视流量会显示用户档案如何实时在历程中移动。 此时会显示任务之间转换的配置文件数。

![](assets/workflow-execution.png){zoomable="yes"}

通过过渡从一个活动传输到另一个活动的数据存储在临时工作表中。 可以为每个过渡显示此数据。 要检查在活动之间传递的数据，请执行以下操作：

1. 选择过渡。
1. 在属性窗格中，单击&#x200B;**[!UICONTROL 预览架构]**&#x200B;以查看工作表架构。 选择&#x200B;**[!UICONTROL 预览结果]**&#x200B;以查看传输的数据。

![](assets/transition.png){zoomable="yes"}

### 活动执行指示器 {#activities}

视觉状态指示器可帮助您了解每个活动的执行情况：

| 视觉指示器 | 描述 |
|-----|------------|
| ![](assets/activity-status-pending.png){zoomable="yes"}{width="70%"} | 当前正在执行活动。 |
| ![](assets/activity-status-orange.png){zoomable="yes"}{width="70%"} | 该活动需要您注意。 这可能涉及确认发送投放或采取必要操作。 |
| ![](assets/activity-status-red.png){zoomable="yes"}{width="70%"} | 活动遇到错误。 要解决此问题，请打开编排的活动日志以了解更多信息。 |
| ![](assets/activity-status-green.png){zoomable="yes"}{width="70%"} | 已成功执行活动。 |

### 日志和任务 {#logs-tasks}

>[!CONTEXTUALHELP]
>id="ajo_campaign_logs"
>title="日志和任务"
>abstract="**日志和任务**&#x200B;屏幕提供了编排的活动执行的历史记录，记录了所有用户操作和遇到的错误。"

监测日志和任务是分析编排的营销活动并确保其正常运行的关键步骤。 日志和任务可从&#x200B;**[!UICONTROL 日志]**&#x200B;按钮访问，该按钮在画布工具栏或每个活动的属性窗格中的测试和实时模式下均可用。

**[!UICONTROL 日志和任务]**&#x200B;屏幕提供了活动执行的完整历史记录，记录了所有用户操作和遇到的错误。

![](assets/workflow-logs.png){zoomable="yes"}

提供了两种类型的信息：

* **[!UICONTROL 日志]**&#x200B;选项卡包含所有操作和错误的时间顺序历史记录。
* **[!UICONTROL 任务]**&#x200B;选项卡详细列出了活动的逐步执行顺序。

在这两个选项卡中，您可以选择显示的列及其顺序，应用过滤器，并使用搜索字段快速查找所需信息。
