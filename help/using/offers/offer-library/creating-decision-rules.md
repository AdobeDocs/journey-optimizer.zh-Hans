---
title: 创建决策规则
description: 瞭解如何建立決定規則，以定義可以顯示優惠的對象
feature: Offers
topic: Integrations
role: User
level: Intermediate
exl-id: 401ce05b-412b-4fa0-a516-bf75727f6387
source-git-commit: 1213a65c8a22a326e8294c51db53efb6e23fd6f9
workflow-type: tm+mt
source-wordcount: '327'
ht-degree: 13%

---

# 创建决策规则 {#create-decision-rules}

您可以根據Adobe Experience Platform中的可用資料來建立優惠決定規則。 決定規則會決定可向誰顯示優惠方案。

例如，您可以指定当（性别=“女性”）和（地区=“东北”）时仅显示“女士冬装选件”。

➡️ [在视频中发现此功能](#video)

建立的決定規則清單可在以下位置存取： **[!UICONTROL 元件]** 功能表。

![](../assets/decision_rules_list.png)

若要建立決定規則，請遵循下列步驟：

1. 前往 **[!UICONTROL 規則]** 標籤，然後按一下 **[!UICONTROL 建立規則]**.

   ![](../assets/offers_decision_rule_creation.png)

1. 為規則命名並提供說明，然後視需要設定規則。

   若要這麼做， **區段產生器** 可協助您建置規則的條件。 [了解详情](../../segment/about-segments.md)

   <!--In this example, the rule will target customers that have the "Gold" loyalty level.-->

   ![](../assets/offers_decision_rule_creation_segment.png)

   >[!NOTE]
   >
   >用來建立決定規則的區段產生器有些許特性，但與搭配使用時有所不同 **[!UICONTROL 細分]** 服務。 例如， **[!UICONTROL 區段]** 索引標籤無法使用。 不過，以下說明的全域程式： [區段產生器](../../segment/about-segments.md) 建立優惠決定規則時，檔案仍有效。 進一步瞭解 [Adobe Experience Platform Segmentation Service檔案](https://experienceleague.adobe.com/docs/experience-platform/segmentation/ui/segment-builder.html).

1. 當您在工作區中新增及設定新欄位時， **[!UICONTROL 區段屬性]** 窗格顯示屬於區段的預估設定檔資訊。 按一下 **[!UICONTROL 重新整理預估值]** 以更新資料。

   ![](../assets/offers_decision_rule_creation_estimate.png)

   >[!NOTE]
   >
   >當規則引數包含不在設定檔中的資料（例如內容資料）時，設定檔預估不可用。 例如，適用性規則要求目前天氣為≥80度。

1. 按一下 **[!UICONTROL 儲存]** 以確認。

1. 建立規則後，會顯示在 **[!UICONTROL 規則]** 清單。 您可以選取它以顯示其屬性，然後編輯或刪除它。

   ![](../assets/rule_created.png)

>[!CAUTION]
>
>事件型優惠方案目前不支援 [!DNL Journey Optimizer]. 如果您根據以下專案建立決定規則： [事件](https://experienceleague.adobe.com/docs/experience-platform/segmentation/ui/segment-builder.html?lang=en#events){target="_blank"}，您將無法在選件中運用它。

## 教學課程影片 {#video}

>[!VIDEO](https://video.tv.adobe.com/v/329373?quality=12)
