---
solution: Journey Optimizer
product: journey optimizer
title: 使用Adobe Journey Optimizer创建编排的营销活动
description: 了解如何使用Adobe Journey Optimizer构建编排的营销活动
badge: label="Alpha"
hide: true
hidefromtoc: true
exl-id: d1d64125-cf00-49c2-a71d-1494ede16f61
source-git-commit: 5ebc82f566d416a177a3278816c60d896a10eff6
workflow-type: tm+mt
source-wordcount: '896'
ht-degree: 1%

---

# 编排营销活动 {#orchestrate}

+++ 目录

| 欢迎使用编排的营销活动 | 启动第一个精心策划的营销活动 | 查询数据库 | 精心策划的营销活动 |
|---|---|---|---|
| [开始使用协调的营销活动](gs-orchestrated-campaigns.md)<br/><br/>[配置步骤](configuration-steps.md)<br/><br/>[访问和管理协调的营销活动](access-manage-orchestrated-campaigns.md) | [创建编排营销活动的关键步骤](gs-campaign-creation.md)<br/><br/>[创建和计划营销活动](create-orchestrated-campaign.md)<br/><br/><b>[编排活动](orchestrate-activities.md)</b><br/><br/>[启动和监控营销活动](start-monitor-campaigns.md)<br/><br/>[报告](reporting-campaigns.md) | [使用规则生成器](orchestrated-rule-builder.md)<br/><br/>[生成您的第一个查询](build-query.md)<br/><br/>[编辑表达式](edit-expressions.md)<br/><br/>[重新定位](retarget.md) | [开始使用活动](activities/about-activities.md)<br/><br/>活动：<br/>[并加入](activities/and-join.md) - [生成受众](activities/build-audience.md) - [更改维度](activities/change-dimension.md) - [渠道活动](activities/channels.md) - [组合](activities/combine.md) - [重复数据删除](activities/deduplication.md) - [扩充](activities/enrichment.md) - [分支](activities/fork.md) - [协调](activities/reconciliation.md) - [保存受众](activities/save-audience.md) - [拆分](activities/split.md) - [等待](activities/wait.md) |

{style="table-layout:fixed"}

+++

<br/>

[创建编排的营销活动](gs-campaign-creation.md)后，您就可以开始编排它将执行的不同任务。 为此，提供了一个可视画布，允许您构建编排的活动图表。 在此图表中，您可以添加各种活动并按顺序连接它们。

## 添加活动 {#add}

在配置的此阶段，将显示带有开始图标的图表，该图标表示编排的活动开始。 要添加您的第一个活动，请单击连接到开始图标的&#x200B;**+**&#x200B;按钮。

此时会显示可添加到图中的活动列表。 可用的活动取决于您在编排的活动图中的位置。 例如，添加第一个活动时，您可以通过以下方式启动编排的营销活动：定位受众、拆分编排的营销活动路径或设置&#x200B;**等待**&#x200B;活动以延迟编排的营销活动执行。 另一方面，在&#x200B;**构建受众**&#x200B;活动后，您可以通过定位活动优化目标，通过渠道活动向受众发送投放，或通过流量控制活动组织编排的营销活动流程。

![](assets/orchestrated-start.png){zoomable="yes"}

将活动添加到图后，将显示右侧窗格，允许您使用特定设置对其进行配置。 有关如何配置每个活动的详细信息，请参阅[此部分](activities/about-activities.md)。

![](assets/orchestrated-configure-activities.png){zoomable="yes"}

重复此过程，根据您希望编排的活动执行的任务，添加所需数量的活动。 请注意，您还可以在两个活动之间插入新活动。 为此，请在活动之间的过渡上单击&#x200B;**+**&#x200B;按钮，选择所需的活动并在右侧窗格中对其进行配置。

您可以选择为每个活动之间的过渡将名称个性化。 要实现此目的，请选择过渡，然后在右窗格中更改其标签。

![](assets/canvas-transition.png)

### 画布工具栏 {#toolbar}

画布工具栏提供了一些选项，用于轻松处理活动并在画布中导航：

![](assets/orchestrated-toolbar.png)

![多选模式图标](assets/do-not-localize/canvas-multiple.svg)选择多个活动以一次删除所有活动或复制并粘贴它们。 [了解如何复制粘贴活动](#copy)

![旋转图标](assets/do-not-localize/canvas-rotate.svg)垂直切换画布。

![适应屏幕图标](assets/do-not-localize/canvas-fit.svg)根据屏幕调整画布缩放级别。

![缩小图标](assets/do-not-localize/canvas-zoomout.svg) ![放大图标](assets/do-not-localize/canvas-zoomin.svg)缩小或进入画布。

![Campaign设置图标](assets/do-not-localize/canvas-map.svg)打开显示您所在位置的画布快照。

### 管理活动 {#manage}

添加活动时，属性窗格中提供了操作按钮，允许您执行多个操作。

![](assets/activity-action.png)

![删除图标](assets/do-not-localize/activity-delete.svg)从画布中删除活动。

![禁用图标](assets/do-not-localize/activity-disable.svg) ![启用图标](assets/do-not-localize/activity-enable.svg)禁用/启用活动。 执行编排的活动时，同一路径上禁用的活动和以下活动不会执行，并且编排的活动会停止。

![暂停图标](assets/do-not-localize/activity-pause.svg) ![恢复图标](assets/do-not-localize/activity-resume.svg)暂停/恢复活动。 执行编排的活动时，活动会在暂停的活动中暂停。 相应的任务以及在同一路径中跟随该任务的所有任务都不会执行。

![复制图标](assets/do-not-localize/activity-copy.svg)复制活动。 [了解如何复制粘贴活动](#copy)

![日志和任务图标](assets/do-not-localize/activity-logs.svg)访问活动的日志和任务。

若干&#x200B;**定位**&#x200B;活动（如&#x200B;**合并**&#x200B;或&#x200B;**重复数据删除**）允许您处理剩余群体，并将其包含到其他叫客过渡中。 例如，如果您使用&#x200B;**拆分**&#x200B;活动，则补数由与先前定义的任何子集都不匹配的群体组成。 若要使用此功能，请激活&#x200B;**[!UICONTROL 生成补码]**&#x200B;选项。

### 复制粘贴活动 {#copy}

您可以复制活动并将其粘贴到任何编排的活动画布中。 目标营销活动可以位于不同的浏览器选项卡中。

* 要复制一个活动，请单击活动属性窗格中的![复制图标](assets/do-not-localize/activity-copy.svg)按钮。
* 要复制多个活动，请单击画布工具栏中的![多选模式图标](assets/do-not-localize/canvas-multiple.svg)图标。

| 复制一个活动 | 复制多个活动 |
|  ---  |  ---  |
| ![](assets/orchestrated-copy-1.png){width="200" align="center" zoomable="yes"} | ![](assets/orchestrated-copy-2.png){width="200" align="center" zoomable="yes"} |

要粘贴活动，请单击过渡上的&#x200B;**+**&#x200B;按钮，然后选择“粘贴x活动”。

![](assets/orchestrated-copy-3.png){zoomable="yes"}{width="50%"}

## 图示例 {#example}

这是一个精心设计的营销活动示例，旨在向所有购买量至少为100$的客户发送电子邮件，但不包括忠诚度积分低于50的所有客户。

![](assets/canvas-example-diagram.png){zoomable="yes"}

为了实现这一目标，新增了以下活动：

* **[!UICONTROL 分支]**&#x200B;活动将编排的活动分为三个路径。
* **[!UICONTROL 构建受众]**&#x200B;活动针对以下三类客户：

   * 客户收到电子邮件，
   * 已购买至少100$的客户，
   * 忠诚度低于50分的客户。

* 将&#x200B;**[!UICONTROL 将]**&#x200B;个活动组与具有电子邮件的客户以及购买至少100$的客户组合在一起，
* **[!UICONTROL 合并]**&#x200B;活动不包括忠诚度积分低于50的客户，
* **[!UICONTROL 电子邮件投放]**&#x200B;活动会向生成的客户发送电子邮件。

## 后续步骤 {#next}

成功设计编排的活动图表后，您可以执行编排的活动并跟踪其各种任务的进度。 [了解如何启动编排的活动并监视其执行情况](start-monitor-campaigns.md)
