---
solution: Journey Optimizer
product: journey optimizer
title: 历程入门
description: 历程入门
feature: Journeys
role: User
level: Beginner
exl-id: 73cfd48b-72e6-4b72-bbdf-700a32a34bda
source-git-commit: f6db4f7cbb1951c009fa7915f340da96eea74120
workflow-type: tm+mt
source-wordcount: '577'
ht-degree: 29%

---


# 历程入门{#jo-general-principle}

使用 [!DNL Journey Optimizer] 使用存储在事件或数据源中的情境数据构建实时编排用例。

设计由以下功能提供支持的分步式高级方案：

* 实时发送由事件接收触发的&#x200B;**单一投放** ，或使用 Adobe Experience Platform 区段&#x200B;**批量**&#x200B;发送。

* 利用来自事件的&#x200B;**上下文数据**、来自 Adobe Experience Platform 的信息或来自第三方 API 服务的数据。

* 使用 **内置操作** 发送 [!DNL Journey Optimizer] 或创建 **自定义操作** 如果您使用第三方系统来发送消息。

* 使用&#x200B;**历程设计器**，构建分步式用例：轻松地拖放进入事件或读取区段活动、添加条件和发送个性化消息。

## 创建历程的步骤{#steps-journey}

使用Adobe Journey Optimizer从单个画布设计和编排个性化历程。

Adobe Journey Optimizer包含全渠道编排画布，使营销人员能够将营销推广与一对一客户参与相协调。 利用用户界面，可轻松地将活动从面板拖放到画布中，以构建历程。

![](assets/interface-journeys.png)

了解如何在 [本页](journey-gs.md).

全渠道历程设计器通过直观的拖放界面，帮助您通过目标受众、基于实时客户或业务交互的更新以及全渠道消息构建多步历程。

![](assets/journey38.png)

有关更多信息，请参阅 [此部分](using-the-journey-designer.md).

作为数据工程师，有关配置您的历程（包括数据源、事件和操作）的详细步骤，请参见 [此部分](../configuration/about-data-sources-events-actions.md).


## 用例{#uc-journey}

在以下端到端用例中了解如何构建历程。

商业用例:

* [发送多渠道消息](journeys-uc.md)
* [使用 Campaign v7/v8 发送消息](ajo-ac.md)
* [向订阅者发送消息](message-to-subscribers-uc.md)

技术用例:

* [使用自定义操作动态传递集合](collections.md)
* [增加投放数量](ramp-up-deliveries-uc.md)
* [使用外部数据源和自定义操作限制吞吐量](limit-throughput.md)

## 历程版本{#journey-versions}

在历程列表中，所有历程版本均显示版本号。 请参阅[此页](../building-journeys/using-the-journey-designer.md)。

当您搜索历程时，最新版本会在首次打开应用程序时显示在列表顶部。 然后，您可以定义所需的排序方式，应用程序会将其保留为用户首选项。 历程版本还显示在历程版界面的顶部，画布上方。

![](assets/journeyversions1.png)

>[!NOTE]
>
>通常，同一历程中无法同时存在多个用户档案。如果启用了重新进入，则用户档案可以重新进入历程，但只有在完全退出该历程的上一个实例后才能重新进入历程。[了解详情](end-journey.md)。

如果您需要修改到实时历程，请创建历程的新版本。

1. 打开实时历程的最新版本，单击 **[!UICONTROL 创建新版本]** 确认。

   ![](assets/journeyversions2.png)

   >[!NOTE]
   >
   >您只能从历程的最新版本创建新版本。

1. 进行修改，单击 **[!UICONTROL 发布]** 确认。

   ![](assets/journeyversions3.png)

从历程发布之日起，个人将开始流入历程的最新版本。 已输入以前版本的用户将一直保留在该版本中，直到他们完成历程。 如果他们稍后重新进入同一历程，则将进入最新版本。

历程版本可以单独停止。 历程的所有版本都具有相同的名称。

当您发布新版本的历程时，之前的版本会自动结束并切换到 **已关闭** 状态。 旅程中不可能进入。 即使停止最新版本，以前的版本仍会保持关闭状态。

>[!NOTE]
>
>在 [本页](../start/guardrails.md#journey-versions-limitations)