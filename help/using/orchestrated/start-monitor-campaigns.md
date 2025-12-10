---
solution: Journey Optimizer
product: journey optimizer
title: 使用Adobe Journey Optimizer启动和监控编排的营销活动
description: 了解如何使用Adobe Journey Optimizer启动和监控编排的营销活动。
feature: Monitoring
exl-id: 5fc2d1d6-75c3-4b45-bb2b-09982b9bd5ed
version: Campaign Orchestration
source-git-commit: 619db0a371b96fbe9480300a874839b7b919268d
workflow-type: tm+mt
source-wordcount: '761'
ht-degree: 53%

---


# 启动和监测精心编排的营销活动 {#start-monitor}

>[!CONTEXTUALHELP]
>id="ajo_campaign_publication"
>title="发布精心编排的营销活动"
>abstract="要开始您的营销活动，您必须发布它。请确保在发布前清除所有错误。"

在画布中创建了要执行的经过精心策划和设计的任务后，即可发布任务并监控任务的执行情况。

您还可以在测试模式下执行营销活动，以检查其执行情况和不同活动的结果。

## 发布前测试营销活动 {#test}

[!DNL Journey Optimizer]允许您在启动之前测试编排的营销活动。 创建营销策划后，其默认处于&#x200B;**草稿**&#x200B;状态。 在此状态下，您可以手动执行营销活动以测试流量。

>[!IMPORTANT]
>
>除&#x200B;**[!UICONTROL 保存受众]**&#x200B;活动和渠道活动外，画布中的所有活动都会执行。 这不会对您的数据或受众产生任何功能上的影响。

要测试编排的营销活动，请打开该营销活动并选择&#x200B;**[!UICONTROL 开始]**。

![](assets/campaign-start.png){zoomable="yes"}

营销活动中的每个活动都按顺序执行，直到到达画布结尾为止。 在测试期间，您可以使用画布中的操作栏控制活动执行。 从那里，您可以：

* 随时&#x200B;**停止**&#x200B;执行。
* 再次&#x200B;**开始**&#x200B;执行。
* **恢复**&#x200B;先前暂停的执行。

画布工具栏中的&#x200B;**[!UICONTROL 警报]** / **[!UICONTROL 警告]**&#x200B;图标会通知您问题，包括在执行之前可能主动出现的警告以及在执行期间或执行之后发生的错误。

![](assets/campaign-warning.png){zoomable="yes"}

您还可以使用直接显示在每个活动上的[可视化状态指示器](#activities)快速识别失败的活动。有关详细的故障排除信息，请打开[营销活动的日志](#logs-tasks)，其中提供了有关错误及其上下文的深入信息。

如果您在画布中添加了渠道活动，则可以使用&#x200B;**[!UICONTROL 模拟内容]**&#x200B;按钮预览和测试消息的内容。 [了解如何使用渠道活动](activities/channels.md)

验证后，即可发布营销活动。

## 发布营销活动 {#publish}

营销活动测试完成并准备就绪后，单击&#x200B;**[!UICONTROL 发布]**&#x200B;即可使其上线。

![](assets/campaign-publish.png){zoomable="yes"}

>[!NOTE]
>
>如果&#x200B;**[!UICONTROL Publish]**&#x200B;按钮已禁用（灰显），请从操作栏访问日志并检查错误消息。 必须修复所有错误，然后才能发布营销活动。

可视化流程会重新启动，真实轮廓开始实时进入历程流转。

如果发布操作失败（例如，由于缺少消息内容），您将收到警报，必须在重试之前修复问题。 成功发布后，营销活动将开始执行（立即或按计划），从&#x200B;**草稿**&#x200B;状态移动到&#x200B;**实时**&#x200B;状态，并变为“只读”。

## 监控营销活动执行情况 {#monitor}

### 可视化流程监控 {#flow}

在测试或实时模式下运行时，可视化流程会显示轮廓如何在历程中实时移动。此时会显示在任务之间过渡的轮廓数。

![](assets/workflow-execution.png){zoomable="yes"}

通过过渡在活动之间传递的数据将暂存于临时工作表中。可以为每个过渡显示此数据。要检查在活动之间传递的数据，请执行以下操作：

1. 选择过渡。
1. 在属性窗格中，单击&#x200B;**[!UICONTROL 预览架构]**&#x200B;以查看工作表架构。选择&#x200B;**[!UICONTROL 预览结果]**&#x200B;以查看传输的数据。

   ![](assets/transition.png){zoomable="yes"}

### 活动执行指示器 {#activities}

可视化状态指示器可帮助您了解每个活动的执行情况：

| 可视化指示器 | 描述 |
|-----|------------|
| ![](assets/activity-status-pending.png){zoomable="yes"}{width="70%"} | 当前正在执行活动。 |
| ![](assets/activity-status-orange.png){zoomable="yes"}{width="70%"} | 该活动需要您注意。这可能涉及确认发送投放或执行必要操作。 |
| ![](assets/activity-status-red.png){zoomable="yes"}{width="70%"} | 活动遇到错误。要解决此问题，请打开编排的活动日志以了解更多信息。 |
| ![](assets/activity-status-green.png){zoomable="yes"}{width="70%"} | 已成功执行活动。 |

### 日志和任务 {#logs-tasks}

>[!CONTEXTUALHELP]
>id="ajo_campaign_logs"
>title="日志和任务"
>abstract="**日志和任务**&#x200B;屏幕提供了精心编排的营销活动的执行历史记录，其中记录了所有用户操作和遇到的错误。"

监测日志和任务是分析编排的营销活动并确保其正常运行的关键步骤。 可从画布工具栏的测试模式和实时模式下的&#x200B;**[!UICONTROL 日志]**&#x200B;按钮访问日志和任务。

![](assets/logs-button.png){zoomable="yes"}

**[!UICONTROL 日志和任务]**&#x200B;屏幕提供营销活动执行的完整历史记录，记录了所有用户操作和遇到的错误。

![](assets/workflow-logs.png){zoomable="yes"}

有两种类型的信息可用：

* **[!UICONTROL 日志]**&#x200B;选项卡包含按时间顺序记录的所有操作和错误的历史记录。
* **[!UICONTROL 任务]**&#x200B;选项卡详细列出了活动的逐步执行顺序。

在这两个选项卡中，您可以选择显示的列及其顺序，应用过滤器，并使用搜索字段快速查找所需信息。

## 后续步骤 {#next}

开始编排的活动画布后，您可以使用Journey Optimizer报表功能获得见解，例如了解受众行为并衡量客户历程中每个步骤的表现。 [了解更多有关协调营销活动报告的信息](../orchestrated/reporting-campaigns.md)
