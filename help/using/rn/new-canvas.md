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
source-git-commit: 596426f3b75a2e6f2d68e5b9218863c2d8887cca
workflow-type: tm+mt
source-wordcount: '568'
ht-degree: 1%

---

# 欢迎使用改进后的历程设计器 {#new-canvas}

>[!CONTEXTUALHELP]
>id="ajo_new_canvas"
>title="新增功能？"
>abstract="新画布"

欢迎使用改进的历程设计器！

我们已经开发了 **简化旅程模型** 旨在改善内部流程。 尽管此新模型是后端改进，但我们的团队利用这个机会添加了对Journey Optimizer用户可见且有益的功能：

* A **重新设计的历程画布** 专为现代化UI体验而打造
* A **实时报告** 历程画布中直接提供的UI

>[!AVAILABILITY]
>
>请注意，此功能的推出将是渐进式的。 您可能不会立即看到更改。

## 历程模型的更新

新的历程模型将与现有模型共存，这意味着将有历程使用 **两种不同的模型**：

* 旧的，称为“v1”
* 而新版本叫做“v2”

v1中的所有历程都将保留在v1中。 您仍然可以编辑、测试或发布它们。 从v1创建的任何新版本也将保留在v1中。 有 **无功能更改** v1历程左右。

如以下屏幕截图所示，节点为圆形，这是v1模型上旅程的旧UI。

![](assets/new-canvas.png)

但是，如果您&#x200B;**创建新历程** 或 **复制现有的一个**，这将是v2历程。  我们计划继续支持v1历程，直到大多数客户过渡到v2历程。

新历程模型有一个限制；它将会 **无法将活动从v1历程复制并粘贴到v2，反之亦然**. 如果您希望这样做，我们建议您复制v1历程以将其设置为v2，然后复制您的活动。

在以下屏幕截图中，您可以看到为历程画布重新设计的UI（仅适用于v2模型）：

![](assets/new-canvas2.png)

**添加到历程设计器的任何新功能（包括实时报告）将仅适用于从现在起的v2历程。**

## 改进了历程画布设计

通过新的旅程模式，我们将引入新的和改进的模型 **历程画布UI**，可以无缝地嵌入Adobe Experience Cloud解决方案和应用程序生态系统，从而提供直观、高效的用户体验。 v2栈栈中的任何旅程都将基于此新设计。

![](assets/new-canvas3.gif)

现在，活动将由具有以下功能的方框表示：

* 第一行表示活动类型，该活动类型通常会被更多情境信息（例如：在读取受众上，它将包含选定受众的名称）覆盖，或者，如果您定义了自定义标签，则会被覆盖。
* 第二行始终表示活动类型。

![](assets/new-canvas4.png)

此新UI通过提供以下内容改进了历程画布的可读性 **更清晰的活动标签和类型**.

它还允许产品团队通过较少的点击在画布上添加更多信息。 “更多信息”的一个示例是在历程画布中包含实时报告，您可以在其中查看因错误而进入和退出活动的用户档案。

![](assets/new-canvas5.png)


## 历程画布中的实时报告

在改进旅程画布设计的同时，我们还将引入 **最近24小时的报表指标** （称为“实时报告”）时，不会将反向链接计算两次。

![](assets/new-canvas6bis.png)

在新模型上的每个实时历程中，您将能够看到， **在每个活动上**，进入该活动的用户档案数以及因错误而退出的用户档案数：

![](assets/new-canvas8.png)

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

用户界面每分钟自动刷新一次。

<!--
Please note that you may see differences between the number of exported profiles and the number of profiles flowing through the journey. The exported profiles count only provides information about the last export job being made while the number of profiles entering an activity only contains profiles who did it in the last 24 hours. This can especially be visible on recurring daily journeys as there could be a data overlap between two days.
-->
