---
solution: Journey Optimizer
product: journey optimizer
title: 历程入门
description: 历程入门
feature: Journeys
role: User
level: Beginner
keywords: 历程，发现，开始
exl-id: 73cfd48b-72e6-4b72-bbdf-700a32a34bda
source-git-commit: 417eea2a52d4fb38ae96cf74f90658f87694be5a
workflow-type: tm+mt
source-wordcount: '588'
ht-degree: 24%

---


# 历程入门{#jo-general-principle}

使用 [!DNL Journey Optimizer] 使用存储在事件或数据源中的情境数据构建实时编排用例。

设计由以下功能提供支持的分步式高级方案：

* 使用 Adobe Experience Platform 受众在接收到事件时触发发送实时&#x200B;**单一投放**，或进行&#x200B;**批量**&#x200B;处理。

* 利用来自事件的&#x200B;**上下文数据**、来自 Adobe Experience Platform 的信息或来自第三方 API 服务的数据。

* 使用 **内置操作** 发送在中设计的消息 [!DNL Journey Optimizer] 或创建 **自定义操作** 如果您使用第三方系统来发送消息。

* 使用&#x200B;**历程设计器**，构建分步式用例：轻松地拖放进入事件或读取受众活动、添加条件和发送个性化消息。


>[!NOTE]
>
>有关历程护栏和限制的详情，请参见 [此页面](../start/guardrails.md)

## 创建历程的步骤{#steps-journey}

使用Adobe Journey Optimizer从单个画布设计和编排个性化历程。 创建历程的主要步骤如下：

![](assets/journey-creation-process.png)

Adobe Journey Optimizer包括全渠道编排画布，允许营销人员协调营销外联活动与一对一客户参与。 利用用户界面，可轻松地将活动从面板拖放到画布中以构建历程。

![](assets/interface-journeys.png)

了解如何在中开始和创建您的第一个历程 [此页面](journey-gs.md).

全渠道历程设计器帮助您使用直观的拖放界面通过目标受众构建多步骤历程、基于实时客户或业务交互的更新以及全渠道消息。

![](assets/journey38.png)

有关更多信息，请参阅 [本节](using-the-journey-designer.md).

作为数据工程师，有关配置历程（包括数据源、事件和操作）的步骤详情，请参见 [本节](../configuration/about-data-sources-events-actions.md).


## 用例{#uc-journey}

了解如何在以下端到端用例中构建历程。

商业用例:

* [发送多渠道消息](journeys-uc.md)
* [使用 Campaign v7/v8 发送消息](ajo-ac.md)
* [向订阅者发送消息](message-to-subscribers-uc.md)

技术用例:

* [使用自定义操作动态传递集合](collections.md)
* [增加投放数量](ramp-up-deliveries-uc.md)
* [使用外部数据源和自定义操作限制吞吐量](limit-throughput.md)

## 历程版本{#journey-versions}

在历程列表中，所有历程版本都随版本号一起显示。 请参阅[此页](../building-journeys/using-the-journey-designer.md)。

搜索历程时，当应用程序首次打开时，最新版本会显示在列表顶部。 然后，您可以定义所需的排序，应用程序会将其保留为用户首选项。 历程的版本也显示在历程版本界面的顶部，位于画布上方。

![](assets/journeyversions1.png)

>[!NOTE]
>
>通常，同一历程中无法同时存在多个用户档案。如果启用了重新进入，则用户档案可以重新进入历程，但只有在完全退出该历程的上一个实例后才能重新进入历程。 [了解更多信息](end-journey.md)。

如果您需要修改到实时历程，请创建历程的新版本。

1. 打开实时历程的最新版本，单击 **[!UICONTROL 创建新版本]** 并确认。

   ![](assets/journeyversions2.png)

   >[!NOTE]
   >
   >您只能从历程的最新版本创建新版本。

1. 进行修改，单击 **[!UICONTROL Publish]** 并确认。

   ![](assets/journeyversions3.png)

从历程发布的那一刻起，个人将开始流入历程的最新版本。 已输入先前版本的用户将保留在该版本中，直到完成该历程。 如果他们稍后重新进入同一历程，则将进入最新版本。

可以单独停止历程版本。 历程的所有版本具有相同的名称。

当您发布历程的新版本时，先前版本会自动结束并切换到 **已关闭** 状态。 无法在历程中进入。 即使您停止了最新版本，先前版本仍保持关闭状态。
