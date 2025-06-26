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
source-git-commit: fa46397b87ae3a81cd016d95afd3e09bb002cfaa
workflow-type: tm+mt
source-wordcount: '753'
ht-degree: 0%

---

# 结束历程 {#journey-ending}

## 实时历程如何结束

在达到全局历程超时或在最后一次发生基于受众的定期历程后，历程将关闭。 [了解历程的结束方式](#close-journey)。

如果您需要终止实时历程，我们建议[您手动关闭它](#close-to-new-entrances)。 然后，新客户进入旅程会被阻止。 已进入历程的用户档案将能够体验到历程的结尾。

您还可以[停止历程](#stop-journey)，但仅限于紧急情况下且必须立即结束所有历程处理的情况下。 已进入历程的用户都将在进度中停止。

>[!IMPORTANT]
>
>* 您无法重新启动或删除[已关闭](#close-journey)或[已停止](#stop-journey)历程。 您可以[创建其新版本](publishing-the-journey.md#journey-versions-journey-versions)或[复制它](journey-ui.md#duplicate-a-journey-duplicate-a-journey)。
>
>* 只能删除已完成的历程。

## 用户档案如何结束历程

历程在以下两个特定上下文中为个人结束：

* 个人到达路径的最后一个活动，然后移至[结束标记](#end-tag)。
* 个人达到&#x200B;**条件**&#x200B;活动（或具有条件的&#x200B;**等待**&#x200B;活动）并且不匹配任何条件。

之后，如果允许重新进入，个人可以重新进入历程。 [了解有关进入/重新进入管理的更多信息](../building-journeys/journey-properties.md#entrance)

## 历程结束标记 {#end-tag}

创作历程时，每个路径的末尾会显示一个结束标记。 用户无法添加此节点，无法删除此节点，只能更改其标签。 它标记历程的每个路径的结尾。

如果历程包含多个路径，我们建议您在每个末端添加一个标签，以使报告更易于阅读。 了解有关[历程报告](../reports/live-report.md)的更多信息。

![](assets/journey-end.png)

## 关闭历程 {#close-journey}

旅程可能由于以下原因而关闭：

* 基于单次区段的历程，该历程已完成执行并达到91天的全局超时。
* 最后一次发生基于受众的周期性历程后。
* 历程已通过[**[!UICONTROL 关闭新入口]**](#close-to-new-entrances)按钮手动关闭。

在&#x200B;**91天历程全局超时**&#x200B;后，读取受众历程将切换到&#x200B;**已完成**&#x200B;状态。 此行为设置为91天，因为有关进入历程的用户档案的所有信息在进入91天后会被删除。 仍在历程中的人员会自动受到影响。 他们在91天超时后退出历程。  了解有关[历程全局超时](../building-journeys/journey-properties.md#global_timeout)的更多信息。

>[!TIP]
>
>基于单次区段的历程即使在运行一次后仍保持&#x200B;**实时**&#x200B;状态。 配置文件完成后，无法重新输入，但在默认全局超时过期之前，历程仍处于&#x200B;**实时**&#x200B;状态。 您可以使用&#x200B;**关闭新入口**&#x200B;选项更快地手动关闭它。

### 对新进入关闭 {#close-to-new-entrances}

手动关闭历程可确保已进入历程的客户能够完成其路径，但新用户无法进入历程。 当历程关闭时（由于上述任何原因），其状态为&#x200B;**[!UICONTROL 已关闭]**。 历程停止让新个人进入历程。 历程中已有的用户档案可以正常完成历程。 在默认全局超时91天后，历程将切换到&#x200B;**已完成**&#x200B;状态。

要从历程列表中关闭历程，请单击历程名称右侧的&#x200B;**[!UICONTROL 省略号]**&#x200B;按钮，然后选择&#x200B;**[!UICONTROL 关闭新入口]**。

![](assets/journey-finish-quick-action.png)

您还可以：

1. 在&#x200B;**[!UICONTROL 历程]**&#x200B;列表中，单击要关闭的旅程。
1. 单击右上方的向下箭头。

   ![](assets/finish_drop_down_list.png){width="50%" align="left" zoomable="yes"}

1. 单击&#x200B;**[!UICONTROL 关闭新入口]**，然后在对话框中确认。




## 停止历程 {#stop-journey}

如果需要停止历程中所有个人的进度，可以停止它。 停止历程超时：历程中的所有个人。 但是，停止旅程的过程涉及所有已进入旅程的人员都在进程中停止。 旅程基本上是关闭的。 如果要结束历程，最佳实践是[关闭历程](#close-journey)。


例如，您可以停止历程，如果营销人员意识到历程定位了错误的受众，或应该投放消息的自定义操作无法正常工作。 要从历程列表中停止历程，请单击历程名称右侧的&#x200B;**[!UICONTROL 省略号]**&#x200B;按钮，然后选择&#x200B;**[!UICONTROL 停止]**。

![](assets/journey-finish-quick-action.png)

您还可以：

1. 在&#x200B;**[!UICONTROL 历程]**&#x200B;列表中，单击要停止的旅程。
1. 单击右上方的向下箭头。

   ![](assets/finish_drop_down_list2.png){width="50%" align="left" zoomable="yes"}

1. 单击&#x200B;**[!UICONTROL 停止]**，然后在对话框中确认。

停止时，历程状态将设置为&#x200B;**[!UICONTROL 已停止]**。
