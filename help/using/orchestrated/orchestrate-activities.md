---
solution: Journey Optimizer
product: journey optimizer
title: 使用Adobe Journey Optimizer创建编排的营销活动
description: 了解如何使用Adobe Journey Optimizer构建编排的营销活动
badge: label="Alpha"
hide: true
hidefromtoc: true
exl-id: d1d64125-cf00-49c2-a71d-1494ede16f61
source-git-commit: 25b1e6050e0cec3ae166532f47626d99ed68fe80
workflow-type: tm+mt
source-wordcount: '738'
ht-degree: 2%

---

# 编排营销活动 {#orchestrate}

+++ 目录

| 欢迎使用编排的营销活动 | 启动第一个精心策划的营销活动 | 查询数据库 | 精心策划的营销活动 |
|---|---|---|---|
| [开始使用编排的营销活动](gs-orchestrated-campaigns.md)<br/><br/>[配置步骤](configuration-steps.md)<br/><br/>[访问和管理编排的营销活动](access-manage-orchestrated-campaigns.md) | [创建编排营销活动的关键步骤](gs-campaign-creation.md)<br/><br/>[创建和计划营销活动](create-orchestrated-campaign.md)<br/><br/><b>[编排活动](orchestrate-activities.md)</b><br/><br/>[发送包含编排营销活动的消息](send-messages.md)<br/><br/>[开始和监控营销活动](start-monitor-campaigns.md)<br/><br/>[报告](reporting-campaigns.md) | [使用规则生成器](orchestrated-rule-builder.md)<br/><br/>[生成您的第一个查询](build-query.md)<br/><br/>[编辑表达式](edit-expressions.md) | [开始使用活动](activities/about-activities.md)<br/><br/>活动：<br/>[And-join](activities/and-join.md) - [生成受众](activities/build-audience.md) - [更改维度](activities/change-dimension.md) - [组合](activities/combine.md) - [重复数据删除](activities/deduplication.md) - [扩充](activities/enrichment.md) - [分支](activities/fork.md) - [协调](activities/reconciliation.md) - [拆分](activities/split.md) - [等待](activities/wait.md) |

{style="table-layout:fixed"}

+++

<br/>

在您[创建了编排的营销活动](gs-campaign-creation.md)后，无论是从编排的营销活动菜单还是在营销活动中，您都可以开始编排它将执行的不同任务。 为此，提供了一个可视画布，允许您构建编排的活动图表。 在此图表中，您可以添加各种活动并按顺序连接它们。

## 添加活动 {#add}

在配置的此阶段，将显示带有开始图标的图表，该图标表示编排的活动开始。 要添加您的第一个活动，请单击连接到开始图标的&#x200B;**+**&#x200B;按钮。

此时会显示可添加到图中的活动列表。 可用的活动取决于您在编排的活动图中的位置。 例如，添加第一个活动时，您可以通过以下方式启动编排的营销活动：定位受众、拆分编排的营销活动路径或设置&#x200B;**等待**&#x200B;活动以延迟编排的营销活动执行。 另一方面，在&#x200B;**构建受众**&#x200B;活动后，您可以通过定位活动优化目标，通过渠道活动向受众发送投放，或通过流量控制活动组织编排的营销活动流程。

![](assets/orchestrated-start.png){zoomable="yes"}

将活动添加到图后，将显示右侧窗格，允许您使用特定设置配置新添加的活动。 有关如何配置每个活动的详细信息，请参阅[此部分](activities/about-activities.md)。

![](assets/orchestrated-configure-activities.png){zoomable="yes"}

重复此过程，根据您希望编排的活动执行的任务，添加所需数量的活动。 请注意，您还可以在两个活动之间插入新活动。 为此，请在活动之间的过渡上单击&#x200B;**+**&#x200B;按钮，选择所需的活动并在右侧窗格中对其进行配置。

要删除某个活动，请在画布中选择该活动，然后单击活动属性中的&#x200B;**删除**&#x200B;图标。

>[!TIP]
>
>您可以选择为每个活动之间的过渡将名称个性化。 要实现此目的，请选择过渡，然后在右窗格中更改其标签。

## 工具栏 {#toolbar}

位于画布右上角的工具栏提供了一些选项，用于轻松处理活动并在画布中导航：

* **多重选择模式**：选择多个活动以一次删除所有活动或复制并粘贴它们。 请参阅[此小节](#copy)。
* **旋转**：垂直切换画布。
* **适合屏幕**：根据屏幕调整画布缩放级别。
* **缩小** / **放大**：缩小或缩小画布。
* **显示映射**：打开显示您所在位置的画布快照。

![](assets/orchestrated-toolbar.png){zoomable="yes"}{width="50%"}

## 管理活动 {#manage}

添加活动时，属性窗格中提供了操作按钮，允许您执行多个操作。

![](assets/activity-action.png){zoomable="yes"}

您可以：

* 从画布中&#x200B;**删除**&#x200B;活动。
* **禁用/启用**&#x200B;该活动。 执行编排的活动时，同一路径上禁用的活动和以下活动不会执行，并且编排的活动会停止。
* **暂停/继续**&#x200B;活动。 执行编排的活动时，活动会在暂停的活动中暂停。 相应的任务以及在同一路径中跟随该任务的所有任务都不会执行。
* **复制**&#x200B;活动。 请参阅[此小节](#copy)。
* 访问活动的&#x200B;**日志和任务**。

若干&#x200B;**定位**&#x200B;活动（如&#x200B;**合并**&#x200B;或&#x200B;**重复数据删除**）允许您处理剩余群体，并将其包含到其他叫客过渡中。 例如，如果您使用&#x200B;**拆分**&#x200B;活动，则补数由与先前定义的任何子集都不匹配的群体组成。 若要使用此功能，请激活&#x200B;**生成补码**&#x200B;选项。

## 移动或复制活动 {#move-copy}

### 复制粘贴活动 {#copy}

您可以复制编排的营销活动并将其粘贴到任何工作流中。 目标编排的营销活动可以位于其他浏览器选项卡中。

要复制活动，您有两个选择：

* 使用操作按钮复制一个活动。

  ![](assets/orchestrated-copy-1.png){zoomable="yes"}{width="70%"}

* 使用工具栏按钮复制多个活动。

  ![](assets/orchestrated-copy-2.png){zoomable="yes"}{width="70%"}

要粘贴复制的活动，请单击过渡上的&#x200B;**+**&#x200B;按钮，然后选择“粘贴X活动”。

![](assets/orchestrated-copy-3.png){zoomable="yes"}{width="50%"}

<!--
### Move activities and their child nodes {#move}

Journey Optimizer allows you to move an activity, along with the entire content of its child nodes (including all transitions and activities within it) to the end of another transition within the same orchestrated campaign.

This process disconnects the activity and everything in its outbound transition from the initial location, moving it to the new target transition.

To move an activity:

1. Select the activity you wish to move.
1. In the activity's properties pane, click the **Move** button.
1. Select the transition where you want to place the activity and its outbound transition, then confirm.

![](assets/activity-move.png)


## Execution options {#execution}

All activities allow you to manage their execution options. Select an activity and click on the **Execution options** button. This lets you define the activity's execution mode and behavior in case of errors.

![](assets/workflow-execution-options.png){zoomable="yes"}{width="70%"}


### Properties

The **Execution** field allows you to define the action to be carried out when the task is started.

The **Maximum execution duration** field allows you to specify a duration such as "30s" or "1h". If the activity is not finished after the duration specified has been elapsed, an alert is triggered. This has no impact on how the orchestrated campaign functions.

The **Time zone** field allows you to select the time zone of the activity. Adobe Journey Optimizer allows you to manage the time differences between multiple countries on the same instance. The setting applied is configured when the instance is created.

**The Affinity** field allows you to force an orchestrated campaign or an orchestrated campaign activity to execute on a particular machine. To do this, you must specify one or several affinities for the orchestrated campaign or activity in question.

The **Behavior** field allows you to define the procedure to follow if asynchronous tasks are used.

### Error management

The **In case of error** field allows you to specify the action to be carried out should the activity encounter an error.

### Initialization script

The **Initialization script** lets you initialize variables or modify activity properties. Click the **Edit code** button and type the snippet of code to execute. The script is called when the activity executes. 

## Example {#example}

Here is an orchestrated campaign example designed to send an email to all customers (other than VIP customers) with an email who are interested in coffee machines.

![](assets/workflow-example.png){zoomable="yes"}{zoomable="yes"}

To achieve this, activities below have been added:

* A **[!UICONTROL Fork]** activity that divides the orchestrated campaign into three paths (one for each set of customer),
* **[!UICONTROL Build audience]** activities to target the three sets of customers:

    * Customers with an email,
    * Customers belonging to the pre-existing "Interrested in Coffee Machine(s)" audience,
    * Customers belonging to the pre-existing "VIP ro reward" audience.

* A **[!UICONTROL Combine]** activity that groups together customers with an email and those interested in coffee machines,
* A **[!UICONTROL Combine]** activity that excludes VIP customers,
* An **[!UICONTROL Email delivery]** activity that sends an email to the resulting customers. 

Once you have completed the orchestrated campaign, add en **[!UICONTROL End]** activity at the end of the diagram. This activity allow you to visually mark the end of a workflow and has no functional impact.

After successfully designing the orchestrated campaign diagram, you can execute the orchestrated campaign and track the progress of its various tasks. [Learn how to start an orchestrated campaign and monitor its execution](start-monitor-campaigns.md)
-->