---
solution: Journey Optimizer
product: journey optimizer
title: 历程结束
description: 了解历程如何以Journey Optimizer结束
feature: Journeys
role: User
level: Intermediate
keywords: 重新进入、历程、结束、直播、停止
exl-id: ea1ecbb0-12b5-44e8-8e11-6d3b8bff06aa
source-git-commit: f8d62a702824bcfca4221c857acf1d1294427543
workflow-type: tm+mt
source-wordcount: '660'
ht-degree: 1%

---

# 结束历程{#journey-ending}

历程可以在两个特定上下文中为个人结束：

* 人员到达路径的最后一个活动。
* 人员到达 **条件** 活动(或 **等待** 活动（具有条件），且不匹配任何条件。

如果允许重新进入，人员可以重新进入历程。 请参阅 [此页面](../building-journeys/journey-gs.md#change-properties)

要终止实时历程，我们建议您将其关闭。 然后，将阻止新客户进入历程。 已进入历程的客户能够体验到结束为止。 请参阅 [本节](../building-journeys/journey.md#close-journey)

仅当发生紧急情况并且所有处理需要在历程中立即结束时，您才能停止历程。 已进入历程的用户都将在进度中停止。 请参阅 [本节](../building-journeys/journey.md#stop-journey)

>[!NOTE]
>
>请注意，您无法继续已关闭或已停止的历程。

## 历程结束标记{#end-tag}

创作历程时，每个路径的末尾显示“结束标记”。 用户无法添加此节点，无法删除此节点，只能更改其标签。 它标记历程的每个路径的结尾。 如果历程包含多个路径，我们建议您在每个末端添加一个标签，以使报告更易于阅读。 请参阅[此页](../reports/live-report.md)。

![](assets/journey-end.png)

<!--

### End activity{#journey-end-activity}

The **[!UICONTROL End]** activity allows you to mark the end of each path of the journey. It is not mandatory but recommended for visual clarity. See [this page](../building-journeys/end-activity.md)

![](assets/journey54.png)

-->

## 关闭历程{#close-journey}

旅程可能由于以下原因而关闭：

* 历程已通过手动关闭 **[!UICONTROL 对新进入关闭]** 按钮。
* 基于一次性区段的历程，该历程已完成执行。
* 最后一次发生基于受众的周期性历程后。

手动关闭历程可确保已进入历程的客户能够完成其路径，但新用户无法进入历程。 当历程关闭时（出于上述任何原因），它将具有状态 **[!UICONTROL 已关闭]**. 历程停止让新个人进入历程。 已处于历程中的人员可以正常完成历程。

30天后，读取受众历程将切换到 **已完成** 状态。 此行为仅设置为30天（即历程超时默认值），因为有关进入历程的用户档案的所有信息在进入30天后会被删除。 仍在历程中的人员会自动受到影响。 他们在30天超时后退出历程。

请参阅此[部分](../building-journeys/journey-gs.md#global_timeout)。

无法重新启动或删除已关闭的历程版本。 您可以创建新版本或复制该版本。 只能删除已完成的历程。

要从历程列表中关闭历程，请单击 **[!UICONTROL 省略号]** 位于历程名称右侧的按钮并选择 **[!UICONTROL 对新进入关闭]**.

![](assets/journey-finish-quick-action.png)

您还可以：

1. 在 **[!UICONTROL 历程]** 列表中，单击要关闭的历程。
1. 单击右上方的向下箭头。

   ![](assets/finish_drop_down_list.png)

1. 单击 **[!UICONTROL 对新进入关闭]**，并在对话框中确认。

## 停止历程{#stop-journey}

如果需要停止历程中所有个人的进度，可以停止它。 停止历程将超时历程中的所有个人。 但是，停止旅程的过程涉及所有已进入旅程的人员都在进程中停止。 旅程基本上是关闭的。 如果要结束历程，我们建议您将其关闭。

无法重新启动停止的历程版本。

停止后，历程状态将设置为 **[!UICONTROL 已停止]**.

例如，您可以停止历程，如果营销人员意识到历程定位了错误的受众，或应该投放消息的自定义操作无法正常工作。 要从历程列表中停止历程，请单击 **[!UICONTROL 省略号]** 位于历程名称右侧的按钮并选择 **[!UICONTROL 停止]**.

![](assets/journey-finish-quick-action.png)

您还可以：

1. 在 **[!UICONTROL 历程]** 列表中，单击要停止的历程。
1. 单击右上方的向下箭头。
   ![](assets/finish_drop_down_list.png)
1. 单击 **[!UICONTROL 停止]**，并在对话框中确认。
