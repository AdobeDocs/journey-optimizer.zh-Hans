---
title: Leverage context data in Decisioning
description: Learn how to leverage context data in Decisioning
feature: Experience Decisioning
topic: Integrations
role: User
level: Intermediate
badge: label="有限发布版"
exl-id: ddc4b681-020b-4433-b4b3-3791c41907c9
source-git-commit: ac8ccb52bd16a26c14dea148f989256e28170765
workflow-type: tm+mt
source-wordcount: '284'
ht-degree: 0%

---

# Leverage context data in Decisioning {#context}

[](rules.md)[](ranking.md)For example, you can design a decision rule that requires the current weather to be ≥80 degrees at the time the decision request is made.

>[!NOTE]
>
>Context data is defined in Adobe Experience Platform and is sent in at the time of a decision request. It does not include historical data.

To use context data, you first need to define the data you want to make available in Decisioning. **** You can also leverage the data when editing a ranking formula.

![](assets/decision-rules-context.png)

The steps to feed Decisioning with Adobe Experience Platform data are as follows:

1. ********[](https://experienceleague.adobe.com/en/docs/experience-platform/xdm/ui/resources/schemas){target="_blank"}

1. Create a new Adobe Experience Platform datastream:

   1. ********

   1. ********

      ![](assets/decision-rule-context-datastream.png)

   1. ************

      ![](assets/decision-rules-context-datastream-service.png)

Once the datastream is saved, the selected dataset&#39;s information is automatically fetched and integrated into Decisioning, typically becoming available within approximately 24 hours.

For further guidance on how to work with Adobe Experience Platform, explore the following resources:

* [](https://experienceleague.adobe.com/en/docs/experience-platform/xdm/schema/composition){target="_blank"}
* [](https://experienceleague.adobe.com/en/docs/experience-platform/catalog/datasets/overview){target="_blank"}
* [](https://experienceleague.adobe.com/en/docs/experience-platform/datastreams/overview){target="_blank"}
