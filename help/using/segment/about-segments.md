---
title: 关于Adobe Experience Platform区段
description: 了解如何配置Adobe Experience Platform区段
feature: 历程
topic: 内容管理
role: User
level: Intermediate
source-git-commit: b07970ff11f1ba7c4e6db30dc2eca1252a579ca4
workflow-type: tm+mt
source-wordcount: '383'
ht-degree: 2%

---

# 区段快速入门 {#about-segments}

[!DNL Journey Optimizer] 允许您直接从菜单中使用实时客户资料数据创建Adobe Experience Platform区 **[!UICONTROL Segments]** 段，并将其用于您的历程。

请注意，区段也可以通过分段服务本身创建。 请参阅[Adobe Experience Platform Segmentation Service文档](https://experienceleague.adobe.com/docs/experience-platform/segmentation/home.html){target=&quot;_blank&quot;}，以了解更多信息。

您可以在历程中以不同方式利用区段：

* 使用&#x200B;**读取区段**&#x200B;编排活动，使属于指定区段的所有个人都进入历程。 历程中包含的消息会发送给属于该区段的个人。 假设您拥有“白银客户”客户细分。通过此活动，您可以让所有白银客户进入旅程并向他们发送一系列个性化消息。

   有关如何使用&#x200B;**[!UICONTROL Read segment]**&#x200B;活动的更多信息，请参阅[此部分](../building-journeys/read-segment.md#configuring-segment-trigger-activity)。

* 使用&#x200B;**区段鉴别**&#x200B;事件活动，让个人根据Adobe Experience Platform区段入口和出口进入旅程或在旅程中前进。 例如，您可以让所有新的白银客户进入历程并发送消息。 有关如何使用此活动的更多信息，请参阅[此部分](../building-journeys/segment-qualification-events.md)。

* 使用简单或高级表达式编辑器在历程中生成&#x200B;**复杂条件**。 在[此部分](../building-journeys/condition-activity.md#using-a-segment)中了解详情。

## Adobe Journey Optimizer评价方法 {#evaluation-method-in-journey-optimizer}

在Adobe Journey Optimizer中，受众是使用以下评估方法之一从区段定义生成的：

* 流式分段 — 当新数据流入系统时，区段的受众列表会实时保持为最新。
* 批量分段 — 区段的受众列表会根据过去一小时内到达的数据，每小时更新一次。

系统根据评估区段规则的复杂性和成本来确定每个区段定义的批处理分段和流式分段之间的确定。

您可以在区段列表的&#x200B;**[!UICONTROL Evaluation method]**&#x200B;列中查看每个区段的评估方法。

首次定义区段后，用户档案会在符合条件时添加到受众。

从以前的数据回填受众最长可能需要24小时。 回填受众后，该受众会持续保持为最新状态，并始终准备进行定位。
