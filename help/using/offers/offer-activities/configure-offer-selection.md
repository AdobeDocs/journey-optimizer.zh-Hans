---
title: 在决策中配置优惠选择
description: 瞭解如何管理決定中的優惠選擇
feature: Offers
topic: Integrations
role: User
level: Intermediate
exl-id: 8c7135d7-bf5a-4671-afdf-afec60907a56
source-git-commit: 4f3d22c9ce3a5b77969a2a04dafbc28b53f95507
workflow-type: tm+mt
source-wordcount: '447'
ht-degree: 6%

---

# 在决策中配置优惠选择 {#offers-selection-in-decisions}

如果多個優惠方案符合指定位置的資格，您可以選擇在設定決定時，為每個設定檔選取最佳優惠方案的方法。 您可以依下列方式排名優惠方案：
* 優惠優先順序
* 排名公式
* [人工智能排名](#use-ranking-strategy)

![](../assets/offer-rank-by.png)

## 優惠優先順序 {#offer-priority}

依預設，當數個優惠方案符合在決定中指定位置的資格時，具有最高優惠方案 **優先順序** 會先傳送給客戶。

![](../assets/offer-priority.png)

建立優惠方案時會指派優惠方案的優先順序分數。 瞭解如何在中建立個人化優惠方案 [本節](../offer-library/creating-personalized-offers.md).

## 排名公式 {#assign-ranking-formula}

除了優惠優先順序之外，Journey Optimizer還允許您建立 **排名公式**. 這些公式可決定應先針對指定位置顯示哪個優惠，而不是考慮優惠的優先順序分數。

例如，您可以提升結束日期距離現在不足24小時的所有優惠方案的優先順序，或如果設定檔的興趣點為「執行中」，則提升「執行中」類別的優惠方案。

瞭解如何在中建立排名公式 [本節](../ranking/create-ranking-formulas.md).

建立公式後，您可以將其指派給決定中的位置。 为此，请执行以下步骤：

1. 建立決定或編輯現有決定。 请参阅[创建决策](../offer-activities/create-offer-activities.md)。

1. 新增將包含優惠方案的版位。 另請參閱 [建立版位](../offer-library/creating-placements.md).

1. 對於每個位置，新增一個集合。 另請參閱 [建立集合](../offer-library/creating-collections.md).

1. 選取 **[!UICONTROL 公式]** 作為排名方法，然後按一下 **[!UICONTROL 新增排名]**.

   ![](../assets/offer-activity-ranking.png)

1. 選取所需的公式，然後按一下 **[!UICONTROL 選取]**.

   ![](../assets/ranking-selection.png)

排名公式現在與位置相關聯。

如果在此位置中符合呈現多個優惠方案的資格，決策將使用選取的公式來計算要先傳送哪個優惠方案。

## 人工智能排名 {#use-ranking-strategy}

<!--If you are an [Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/landing/home.html){target="_blank"} user leveraging the **Offer Decisioning** application service,-->

您也可以使用經過訓練的模型系統，藉由選取排名策略，自動排名要針對指定設定檔顯示的優惠方案。 瞭解如何在中建立排名策略 [本節](../ranking/create-ranking-strategies.md).

建立排名策略後，您可以將其指派給決定中的位置。 若要這麼做，請遵循下列步驟：

1. 建立決定或編輯現有決定。 请参阅[创建决策](../offer-activities/create-offer-activities.md)。

1. 新增將包含優惠方案的版位。 另請參閱 [建立版位](../offer-library/creating-placements.md).

1. 對於每個位置，新增一個集合。 另請參閱 [建立集合](../offer-library/creating-collections.md).

1. 選擇優惠排名依據 **[!UICONTROL AI排名]** ，然後按一下「 」 **[!UICONTROL 新增排名]**.

   ![](../assets/ranking-selection-ai-ranking.png)

1. 選取您建立的排名策略。 會顯示排名策略的所有詳細資訊。

   ![](../assets/ranking-selection-ai-ranking-selected.png)

1. 单击&#x200B;**[!UICONTROL 选择]**。排名策略現在與位置相關聯。

如果多個優惠方案都符合條件，訓練有素的模型系統將決定應先針對指定位置顯示哪個優惠方案。

