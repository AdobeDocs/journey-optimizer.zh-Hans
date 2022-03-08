---
title: 关于 Adobe Experience Platform 区段
description: 了解如何配置Adobe Experience Platform区段
feature: Journeys
topic: Content Management
role: User
level: Intermediate
exl-id: 10d2de34-23c1-4a5e-b868-700b462312eb
source-git-commit: 882b99d9b49e1ae6d0f97872a74dc5a8a4639050
workflow-type: tm+mt
source-wordcount: '381'
ht-degree: 3%

---

# Adobe Experience Platform区段快速入门 {#about-segments}

[!DNL Journey Optimizer]  允许您直接从 **[!UICONTROL Segments]** ，并将它们用于您的历程。

请注意，区段也可以通过分段服务本身创建。 在 [Adobe Experience Platform Segmentation Service文档](https://experienceleague.adobe.com/docs/experience-platform/segmentation/home.html).

您可以在历程中以不同方式利用区段：

* 使用 **读取区段** 编排活动，使属于指定区段的所有个人都进入历程。 历程中包含的消息会发送给属于该区段的个人。 假设您拥有“白银客户”客户细分。通过此活动，您可以让所有白银客户进入旅程并向他们发送一系列个性化消息。

   有关如何使用的更多信息 **[!UICONTROL Read segment]** 活动，请参阅 [此部分](../building-journeys/read-segment.md#configuring-segment-trigger-activity).

* 使用 **区段鉴别** 事件活动，根据Adobe Experience Platform区段入口和出口，让个人进入历程或在历程中前进。 例如，您可以让所有新的白银客户进入历程并发送消息。 有关如何使用此活动的更多信息，请参阅 [此部分](../building-journeys/segment-qualification-events.md).

* 生成 **复杂条件** 使用简单或高级表达式编辑器在历程中访问。 在 [此部分](../building-journeys/condition-activity.md#using-a-segment).

## Adobe Journey Optimizer评价方法 {#evaluation-method-in-journey-optimizer}

在Adobe Journey Optimizer中，受众是使用以下评估方法之一从区段定义生成的：

* 流分段 — 当新数据流入系统时，区段的受众列表会实时保持为最新。
* 批量分段 — 区段的受众列表会根据过去一小时内到达的数据，每小时更新一次。

系统根据评估区段规则的复杂性和成本来确定每个区段定义的批处理分段和流式分段之间的确定。

您可以在 **[!UICONTROL Evaluation method]** 列。

首次定义区段后，用户档案会在符合条件时添加到受众。

从以前的数据回填受众最长可能需要24小时。 回填受众后，该受众会持续保持为最新状态，并始终准备进行定位。
