---
title: 关于Adobe Experience Platform细分
description: 了解如何配置Adobe Experience Platform区段
translation-type: tm+mt
source-git-commit: 55b9e5d8ed259ec6ed7746e835691d7d6261a8a4
workflow-type: tm+mt
source-wordcount: '224'
ht-degree: 3%

---

# 关于Adobe Experience Platform区段{#about-segments}

![](../assets/do-not-localize/badge.png)

Journey Optimizer允许您直接从&#x200B;**[!UICONTROL Segments]**&#x200B;菜单使用实时客户用户档案数据创建Adobe Experience Platform细分，并将其用于您的旅程。

请注意，区段也可以从分段服务本身创建。 请阅读[Adobe Experience Platform分段服务文档](https://experienceleague.adobe.com/docs/experience-platform/segmentation/home.html)了解更多信息。

您可以在旅程中以不同方式利用细分：

* 使用&#x200B;**读取区段**&#x200B;业务流程活动，使属于指定区段的所有个人都进入旅程。 您旅程中包含的消息将发送给属于该细分的个人。 假设您拥有“白银客户”客户细分。通过此活动，您可以让所有银质客户进入一个旅程并向他们发送一系列个性化信息。

   有关如何使用&#x200B;**[!UICONTROL Read segment]**&#x200B;活动的详细信息，请参阅[本节](../building-journeys/read-segment.md#configuring-segment-trigger-activity)。

* 使用&#x200B;**区段资格**&#x200B;事件活动，让个人根据Adobe Experience Platform区段的入口和出口进入或前进旅程。 例如，您可以让所有新的银质客户进入一个旅程并发送消息。 有关如何使用此活动的详细信息，请参阅[此部分](../building-journeys/segment-qualification-events.md)。

* 使用简单或高级表达式编辑器在旅程中构建&#x200B;**复杂条件**。 请阅读[本节](../building-journeys/condition-activity.md#using-a-segment)了解更多信息。
