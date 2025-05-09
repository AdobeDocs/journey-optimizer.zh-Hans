---
solution: Journey Optimizer
product: journey optimizer
title: 使用Adobe Journey Optimizer创建编排的营销活动
description: 了解如何使用Adobe Journey Optimizer构建编排的营销活动
badge: label="Alpha"
hide: true
hidefromtoc: true
exl-id: d1d64125-cf00-49c2-a71d-1494ede16f61
source-git-commit: bdc584c1aae0c735d81dfc95e11f96f755bea26a
workflow-type: tm+mt
source-wordcount: '1213'
ht-degree: 1%

---

# 编排编排的营销活动 {#orchestrate}

在您[创建了编排的营销活动](gs-campaign-creation.md)后，无论是从编排的营销活动菜单还是在营销活动中，您都可以开始编排它将执行的不同任务。 为此，提供了一个可视画布，允许您构建编排的活动图表。 在此图表中，您可以添加各种活动并按顺序连接它们。

## 添加活动 {#add}

在配置的此阶段，将显示带有开始图标的图表，该图标表示编排的活动开始。 要添加您的第一个活动，请单击连接到开始图标的&#x200B;**+**&#x200B;按钮。

此时会显示可添加到图中的活动列表。 可用的活动取决于您在编排的活动图中的位置。 例如，添加第一个活动时，您可以通过以下方式启动编排的营销活动：定位受众、拆分编排的营销活动路径或设置&#x200B;**等待**&#x200B;活动以延迟编排的营销活动执行。 另一方面，在&#x200B;**构建受众**&#x200B;活动后，您可以通过定位活动优化目标，通过渠道活动向受众发送投放，或通过流量控制活动组织编排的营销活动流程。

![](assets/workflow-start.png){zoomable="yes"}

将活动添加到图后，将显示右侧窗格，允许您使用特定设置配置新添加的活动。 有关如何配置每个活动的详细信息，请参阅[此部分](activities/about-activities.md)。

![](assets/workflow-configure-activities.png){zoomable="yes"}

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

![](assets/workflow-toolbar.png){zoomable="yes"}{width="50%"}

## 管理活动 {#manage}

添加活动时，属性窗格中提供了操作按钮，允许您执行多个操作。

![](assets/activity-action.png){zoomable="yes"}

您可以：

* 从画布中&#x200B;**删除**&#x200B;活动。
* **禁用/启用**&#x200B;该活动。 执行编排的活动时，同一路径上禁用的活动和以下活动不会执行，并且编排的活动会停止。
* **暂停/继续**&#x200B;活动。 执行编排的活动时，活动会在暂停的活动中暂停。 相应的任务以及在同一路径中跟随该任务的所有任务都不会执行。
* **复制**&#x200B;活动。 请参阅[此小节](#copy)。
* **将**&#x200B;活动及其所有子节点移动到另一个过渡。 请参阅[此部分](#move)
* 访问活动的&#x200B;**执行选项**。
* 访问活动的&#x200B;**日志和任务**。

若干&#x200B;**定位**&#x200B;活动（如&#x200B;**合并**&#x200B;或&#x200B;**重复数据删除**）允许您处理剩余群体，并将其包含到其他叫客过渡中。 例如，如果您使用&#x200B;**拆分**&#x200B;活动，则补充包含与先前定义的任何子集都不匹配的群体。 若要使用此功能，请激活&#x200B;**生成补码**&#x200B;选项。

![](assets/workflow-split-complement.png)

## 移动或复制活动 {#move-copy}

### 复制粘贴活动 {#copy}

您可以复制编排的营销活动并将其粘贴到任何工作流中。 目标编排的营销活动可以位于其他浏览器选项卡中。

要复制活动，您有两个选择：

* 使用操作按钮复制一个活动。

  ![](assets/workflow-copy.png){zoomable="yes"}{width="70%"}

* 使用工具栏按钮复制多个活动。

  ![](assets/workflow-copy-2.png){zoomable="yes"}{width="70%"}

要粘贴复制的活动，请单击过渡上的&#x200B;**+**&#x200B;按钮，然后选择“粘贴X活动”。

![](assets/workflow-copy-3.png){zoomable="yes"}{width="50%"}

### 移动活动及其子节点 {#move}

Journey Optimizer允许您将活动及其子节点的全部内容（包括其中的所有过渡和活动）移动到同一编排的营销活动中的另一个过渡的末尾。

此流程会断开活动及其叫客过渡中所有内容与初始位置的连接，并将其移动到新目标过渡。

要移动活动，请执行以下操作：

1. 选择要移动的活动。
1. 在活动的属性窗格中，单击&#x200B;**移动**&#x200B;按钮。
1. 选择要放置活动及其叫客过渡的过渡，然后确认。

![](assets/activity-move.png)

## 执行选项 {#execution}

所有活动均允许您管理其执行选项。 选择一个活动，然后单击&#x200B;**执行选项**&#x200B;按钮。 这让您能够定义活动的执行模式和出现错误时的行为。

![](assets/workflow-execution-options.png){zoomable="yes"}{width="70%"}

### 属性

**执行**&#x200B;字段允许您定义启动任务时要执行的操作。

**最长执行持续时间**&#x200B;字段允许您指定持续时间，如“30s”或“1h”。 如果活动在指定的持续时间过后未完成，则会触发警报。 这不会对编排的营销活动的运行方式产生影响。

**时区**&#x200B;字段允许您选择活动的时区。 Adobe Journey Optimizer允许您在同一实例上管理多个国家/地区之间的时差。 应用的设置将在创建实例时配置。

**利用Affinity**&#x200B;字段，可强制在特定计算机上执行协调的活动或协调的活动活动。 为此，您必须为相关编排的营销活动或活动指定一个或多个任务相关性。

**行为**&#x200B;字段允许您定义在使用异步任务时要遵循的过程。

### 错误管理

**如果出现错误**&#x200B;字段，允许您指定活动遇到错误时要执行的操作。

### 初始化脚本

**初始化脚本**&#x200B;允许您初始化变量或修改活动属性。 单击&#x200B;**编辑代码**&#x200B;按钮并键入要执行的代码片段。 活动执行时将调用脚本。

## 示例 {#example}

这是一个精心设计的营销活动示例，旨在通过电子邮件向所有对咖啡机感兴趣的客户(VIP客户除外)发送电子邮件。

![](assets/workflow-example.png){zoomable="yes"}{zoomable="yes"}

为了实现这一目标，新增了以下活动：

* **[!UICONTROL 分支]**&#x200B;活动，将编排的活动分为三个路径（每组客户一个路径），
* **[!UICONTROL 构建受众]**&#x200B;活动以定位这三组客户：

   * 客户收到电子邮件，
   * 属于预先存在的“Interrested in Coffee Machine(s)”受众的客户，
   * 属于预先存在的“VIP或奖励”受众的客户。

* **[!UICONTROL 合并]**&#x200B;活动，将电子邮件中的客户和对咖啡机感兴趣的客户分组，
* 排除VIP客户的&#x200B;**[!UICONTROL 合并]**&#x200B;活动，
* **[!UICONTROL 电子邮件投放]**&#x200B;活动，向生成的客户发送电子邮件。

完成编排的活动后，在图末尾添加&#x200B;**[!UICONTROL 结束]**&#x200B;活动。 此活动允许您以可视方式标记工作流的结尾，对功能没有影响。

成功设计编排的活动图表后，您可以执行编排的活动并跟踪其各种任务的进度。 [了解如何启动编排的活动并监视其执行情况](start-monitor-campaigns.md)
