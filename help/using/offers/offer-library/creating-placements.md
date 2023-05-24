---
title: 创建投放位置
description: 瞭解如何為您的優惠方案建立刊登版位
feature: Offers
topic: Integrations
role: User
level: Intermediate
exl-id: dfaf887e-d4b3-45b0-8297-bffdb0abff4d
source-git-commit: 51f93270c969875e94cc3e98919149d67d764ed1
workflow-type: tm+mt
source-wordcount: '550'
ht-degree: 11%

---

# 创建投放位置 {#create-placements}

>[!CONTEXTUALHELP]
>id="ajo_decisioning_placement"
>title="版面"
>abstract="投放位置是用于展示优惠的容器。它有助于确保正确的优惠内容显示在消息中的正确位置。从“组件”菜单创建投放位置。"

版位有助於確保正確的選件內容顯示在訊息的正確位置。 向选件添加内容时，将要求您选择可以显示该内容的版面。

➡️ [在本影片中瞭解如何建立刊登版位](#video)

在下列範例中，有三個版位，分別對應至不同型別的內容(影像、文字、HTML)。

![](../assets/offers_placement_schema.png)

位置清單可在 **[!UICONTROL 元件]** 功能表。 篩選器可協助您根據特定管道或內容擷取版位。

![](../assets/placements_filter.png)

若要建立版位，請遵循下列步驟：

1. 按一下 **[!UICONTROL 建立位置]**.

   ![](../assets/offers_placement_creation.png)

1. 定義位置的屬性：

   * **[!UICONTROL 名稱]**：位置的名稱。 請務必定義有意義的名稱，以便更輕鬆地擷取它。
   * **[!UICONTROL 頻道型別]**：使用位置的管道。
   * **[!UICONTROL 內容型別]**：允許位置顯示的內容型別：文字、HTML、影像連結或JSON。
   * **[!UICONTROL 說明]**：位置的說明（選用）。

   ![](../assets/offers_placement_creation_properties.png)


1. 此 **[!UICONTROL 請求設定]** 和 **[!UICONTROL 回應格式]** 區段提供其他引數：

   * **[!UICONTROL 允許跨版位的重複專案]**：控制是否可以跨不同版位多次建議相同的選件。 如果啟用，系統會針對多個版位考慮相同的選件。 依預設，引數會設為false。

      如果決策請求中任何位置的此選項設為false，請求中的所有位置都將繼承「false」設定。

   * **[!UICONTROL 請求優惠]**：依預設，會為每個設定檔傳回一個決定範圍選件。 您可以使用此選項調整傳回的優惠方案數量。 例如，如果您選取2，則會針對所選決定範圍顯示最佳的2個優惠方案。

   * **[!UICONTROL 包含內容]** / **[!UICONTROL 包含中繼資料]**：指定是否應在API回應中傳回選件的內容和中繼資料。 您只能包含所有中繼資料或特定欄位。 依預設，「包含中繼資料」值會設為true。
   如果您使用，這些引數也可以直接設定到您的API請求中 [決策API](https://experienceleague.adobe.com/docs/journey-optimizer/using/offer-decisioning/api-reference/offer-delivery-api/decisioning-api.html). 不過，在使用者介面中設定這些變數有助於節省時間，因為您不需要在每個API請求中傳遞這些變數。 請注意，如果您同時在使用者介面和API要求中設定引數，API要求的值將會優先於介面的值。

   >[!NOTE]
   >
   >如果您使用 [Edge Decisioning API](https://experienceleague.adobe.com/docs/journey-optimizer/using/offer-decisioning/api-reference/offer-delivery-api/edge-decisioning-api.html?)，您無法在請求中設定這些引數。 您需要在此畫面中定義它們。
   >
   >如果您使用 [批次決策API](../api-reference/offer-delivery-api/batch-decisioning-api.md)，您可以在此畫面或API請求中設定這些引數。 如果畫面和APi請求之間的引數值不相符，則會使用請求值。

1. 按一下 **[!UICONTROL 儲存]** 以確認。

1. 位置建立後，會顯示在「位置」清單中。 您可以選取它以顯示其屬性並加以編輯。

   ![](../assets/placement_created.png)

## 操作方法视频{#video}

瞭解如何在決定管理中建立刊登版位。

>[!VIDEO](https://video.tv.adobe.com/v/329372?quality=12)

