---
solution: Journey Optimizer
product: journey optimizer
title: 全新历程界面
feature: Release Notes
topic: Content Management
description: 全新历程界面
hide: true
hidefromtoc: true
exl-id: 03828fca-dde7-4b3b-b890-2c007d1245cc
source-git-commit: 6b9044117dcdd7554dea0c5f791a6dcfb0218010
workflow-type: tm+mt
source-wordcount: '556'
ht-degree: 2%

---

# 欢迎使用改进的历程设计器 {#new-canvas}

Journey Optimizer现在提供旨在改善用户体验和内部流程的&#x200B;**简化旅程模型**。 从4月版开始，您可以受益于以下功能：

* 为现代化UI体验重新设计的&#x200B;**历程画布**
* 历程画布中直接可用的&#x200B;**实时报告** UI

>[!NOTE]
>
>请注意，此功能的推出将是渐进式的。 您可能不会立即看到更改。

## 历程模型的更新

新历程模型将和现有模型一起运行，这意味着将有使用&#x200B;**两个不同模型**&#x200B;的历程：

* 旧模型
* 新模型

旧版模型中的所有历程都将保留在其中。 您仍然可以编辑、测试或发布它们。 在旧模型上通过历程创建的任何新版本也将保留在该版本中。 这些历程没有&#x200B;**功能更改**。

如以下屏幕截图所示，节点为圆形，这是旧模型上旅程的旧UI。

![](assets/new-canvas.png)

但是，当您&#x200B;**创建新历程**&#x200B;或&#x200B;**复制现有历程**&#x200B;时，它将位于新模型上。 在大部分客户过渡到新模型之前，仍支持旧模型上的历程。

新历程模型有一个限制；将&#x200B;**无法将活动从旧模型复制并粘贴到新模型，反之亦然**。 如果您希望执行此操作，我们建议您复制旧版历程以将其切换到新模型，然后复制您的活动。

在以下屏幕截图中，您可以看到为历程画布重新设计的UI（仅适用于新模型）：

![](assets/new-canvas2.png)

**添加到历程设计器的任何新功能（包括实时报告）将仅适用于从此刻起的新模型上的历程。**

## 改进了历程画布设计

通过新的历程模型，我们将引入新的经过改进的&#x200B;**历程画布UI**，该用户界面无缝地融入Adobe Experience Cloud解决方案和应用程序生态系统，从而提供直观且高效的用户体验。 新模型中的任何历程都将基于新设计。

![](assets/new-canvas3.gif)

现在，活动将由具有以下功能的方框表示：

* 第一行表示活动类型，该活动类型经常被更多情境信息（在读取受众上，它将包含所选受众的名称）覆盖，或者，如果您定义了自定义标签，则会覆盖该活动类型。
* 第二行始终表示活动类型。

![](assets/new-canvas4.png)

此新UI提供了&#x200B;**更清晰的活动标签和类型**，从而提高了历程画布的可读性。

它还允许产品团队通过较少的点击在画布上添加更多信息。 “更多信息”的一个示例是在历程画布中包含实时报告，您可以在其中查看因错误而进入和退出活动的用户档案。

![](assets/new-canvas5.png)

## 历程画布中的实时报告

除了改进的历程画布布局外，还引入了一项新功能，允许用户直接在历程画布中查看过去&#x200B;**24小时**&#x200B;的实时报告量度（称为实时报告）。

对于使用新模型的每个实时历程中的每个活动，您均有权访问：


* 进入此活动的用户档案计数。
* 因错误退出此活动的用户档案计数。

![](assets/new-canvas6bis.png)

<!--`
With every live journey on the new model, you will be able to see two types of "last 24 hours" reporting information:

* On a **new insert**, you will see:
    * The number of profiles that have been exported for audience-triggered journeys. You will see the number of profiles available in the last export job alongside the time when that export has been made.
    * The number of profiles who exited the journey
    * The percentage of errors
    ![](assets/new-canvas7.png)
* **On each activity**, you will see the number of profiles who entered that activity and the number who exited because of an error:
    ![](assets/new-canvas8.png)
-->
<!--
Please note that you may see differences between the number of exported profiles and the number of profiles flowing through the journey. The exported profiles count only provides information about the last export job being made while the number of profiles entering an activity only contains profiles who did it in the last 24 hours. This can especially be visible on recurring daily journeys as there could be a data overlap between two days.
-->
