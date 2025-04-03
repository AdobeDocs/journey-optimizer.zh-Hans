---
solution: Journey Optimizer
product: journey optimizer
title: 使用Adobe Journey Optimizer启动和监控多步营销活动
description: 了解如何使用Adobe Journey Optimizer启动和监控多步营销活动
hide: true
hidefromtoc: true
exl-id: 5fc2d1d6-75c3-4b45-bb2b-09982b9bd5ed
source-git-commit: 990d49202a790b5a117a7da665ed32f52f27b554
workflow-type: tm+mt
source-wordcount: '571'
ht-degree: 1%

---

# 开始并监控编排的营销活动 {#start-monitor}

<!--
<audio controls><source src="../ms/assets/do-not-localize/sound.mp3" type="audio/mpeg">Your browser does not support the audio element.</audio> -->

>[!CONTEXTUALHELP]
>id="ajo_campaign_publication"
>title="发布精心策划的营销活动"
>abstract="要启动营销策划，您必须发布它。 确保在发布之前清除所有警告。"


创建经过编排的任务并设计好要在画布中执行的任务后，您就可以发布它并监控其执行方式。

## 启动多步营销活动 {#start}

要启动多步骤营销活动，请导航到&#x200B;**[!UICONTROL 营销活动]**&#x200B;菜单的&#x200B;**[!UICONTROL 多步骤]**&#x200B;选项卡，选择要启动的营销活动，然后单击画布右上角的&#x200B;**[!UICONTROL 开始]**&#x200B;按钮。

运行多步骤营销活动后，画布中的每个活动会按顺序执行，直到到达多步骤营销活动结束为止。

您可以使用可视流量实时跟踪目标用户档案的进度。 这允许您快速识别每个活动的状态以及它们之间转换的用户档案数。

![](assets/workflow-execution.png){zoomable="yes"}

## 多步骤营销活动过渡 {#transitions}

在多步营销活动中，通过过渡从一个活动传输到另一个活动的数据存储在临时工作表中。 可以为每个过渡显示此数据。 要实现此目的，请选择过渡以在屏幕右侧打开其属性。

* 单击&#x200B;**[!UICONTROL 预览架构]**&#x200B;以显示工作表的架构。
* 单击&#x200B;**[!UICONTROL 预览结果]**&#x200B;以可视化在所选过渡中传输的数据。

![](assets/transition.png){zoomable="yes"}

## 监测活动执行 {#activities}

通过每个活动框右上角的视觉指示器，可检查其执行情况：

| 视觉指示器 | 描述 |
|-----|------------|
| ![](assets/activity-status-pending.png){zoomable="yes"}{width="70%"} | 当前正在执行活动。 |
| ![](assets/activity-status-orange.png){zoomable="yes"}{width="70%"} | 该活动需要您注意。 这可能涉及确认发送投放或采取必要操作。 |
| ![](assets/activity-status-red.png){zoomable="yes"}{width="70%"} | 活动遇到错误。 要解决此问题，请打开多步骤活动日志以了解更多信息。 |
| ![](assets/activity-status-green.png){zoomable="yes"}{width="70%"} | 已成功执行活动。 |

## 监测日志和任务 {#logs-tasks}

监测工作流日志和任务是分析多步营销活动并确保其正常运行的关键步骤。 可从操作工具栏中提供的&#x200B;**[!UICONTROL 日志]**&#x200B;图标以及每个活动的属性窗格中访问它们。

**[!UICONTROL 日志和任务]**菜单提供多步骤活动执行的历史记录，记录所有用户操作和遇到的错误。
![](assets/workflow-logs.png){zoomable="yes"}

提供了两种类型的信息：

* **[!UICONTROL 日志]**&#x200B;选项卡包含所有多步骤营销活动的执行历史记录。 它按时间顺序对执行的操作和执行错误进行索引。
* **[!UICONTROL 任务]**&#x200B;选项卡详细列出了活动的执行顺序。

在这两个选项卡中，您可以选择显示的列及其顺序，应用过滤器，并使用搜索字段快速查找所需信息。

## 多步骤营销活动执行命令 {#execution-commands}

右上角的操作栏提供了用于管理多步骤营销活动执行的命令。 您可以：

* **[!UICONTROL 开始]** / **[!UICONTROL 继续]**&#x200B;执行   多步骤营销活动，然后会呈现进行中状态。 如果暂停了多步营销活动，则会恢复它，否则会启动它并激活初始活动。

* **[!UICONTROL 暂停]**&#x200B;执行多步骤营销活动，该活动随后会呈现“已暂停”状态。 在恢复之前，不会激活任何新活动，但不会暂停正在进行的操作。

* **[!UICONTROL 停止]**&#x200B;正在执行的多步营销活动，该活动随后将呈现“已完成”状态。 如果可能，正在执行的操作会被中断。 您无法从多步骤营销活动停止的位置继续执行该营销活动。
