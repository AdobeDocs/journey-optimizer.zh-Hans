---
solution: Journey Optimizer
product: journey optimizer
title: AEM内容片段
description: 了解如何访问和管理AEM内容片段
topic: Content Management
role: User
level: Beginner
source-git-commit: 4f7e36a6cc19e4138e867950e34c5a5e6452b364
workflow-type: tm+mt
source-wordcount: '239'
ht-degree: 20%

---

# Adobe Experience Manager内容片段入门 {#aem-fragments}

>[!AVAILABILITY]
>
>对于医疗保健客户，只有在许可Journey Optimizer Healthcare Shield和Adobe Experience Manager增强安全性附加产品后，才会启用集成。

通过将 Adobe Experience Manager as a Cloud Service 与 Adobe Journey Optimizer 集成，您现在可以将 AEM 内容片段无缝纳入到 Journey Optimizer 内容中。这种简单的连接方式可简化访问和利用 AEM 内容的流程，从而能够创建个性化的动态营销活动和历程。

要了解有关AEM内容片段的更多信息，请参阅Experience Manager文档中的[使用内容片段](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/sites/administering/content-fragments/content-fragments-with-journey-optimizer){target="_blank"}。

## 内容片段生命周期

![](assets/do-not-localize/AEM_CF.png)

内容片段根据它们所在的Adobe Experience Manager层而遵循不同的生命周期阶段。 [请参阅Adobe Experience Manager文档以了解详情](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/sites/authoring/author-publish)

内容在&#x200B;**创作层**&#x200B;中创建和管理，其中片段可以具有状态，如“新建”、“草稿”、“已发布”、“已修改”或“未发布”。 这些状态仅适用于&#x200B;**创作层**，并且支持内容创建和审阅。

发布内容片段时，会在&#x200B;**发布层**&#x200B;上创建一个副本，并通过未经身份验证的公共端点公开。 Journey Optimizer与此&#x200B;**发布层**&#x200B;独占集成。

因此，Journey Optimizer只会显示已发布或已修改的内容片段，并且始终使用最新发布的版本。 在重新发布内容片段之前，发布后所做的任何更改都不会反映在Journey Optimizer中。
