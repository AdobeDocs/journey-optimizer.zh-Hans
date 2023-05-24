---
title: 批量决策
description: 瞭解如何將優惠決定傳遞至特定Adobe Experience Platform區段中的所有設定檔。
exl-id: 810c05b3-2bae-4368-bf12-3ea8c2f31c01
source-git-commit: 9657862f1c6bdb2399fcf3e6384bb9dec5b8f32b
workflow-type: tm+mt
source-wordcount: '833'
ht-degree: 2%

---

# 批量决策 {#deliver}

## 開始使用批次決策 {#start}

Journey Optimizer可讓您將優惠決定傳送給特定Adobe Experience Platform區段中的所有設定檔。

為此，您需要在Journey Optimizer中建立工作請求，其中包含要定位的區段資訊和要使用的優惠決定。 然後，區段中每個設定檔的選件內容會放入Adobe Experience Platform資料集，以供自訂批次工作流程使用。

也可以使用API執行批次傳送。 如需詳細資訊，請參閱 [批次決策API檔案](api-reference/offer-delivery-api/batch-decisioning-api.md).

## 先决条件 {#prerequisites}

在設定工作請求之前，請確定您已建立：

* **資料集** 在Adobe Experience Platform中。 此資料集將用於儲存使用「ODE DecisionEvents」結構描述的決策結果。 進一步瞭解 [資料集檔案](https://experienceleague.adobe.com/docs/experience-platform/catalog/datasets/overview.html?lang=zh-Hans).

* **區段** 在Adobe Experience Platform中。 應評估該區段並加以更新。 瞭解如何更新中的區段會籍評估 [Segment Service檔案](http://www.adobe.com/go/segmentation-overview-en)

   >[!NOTE]
   >
   >批次工作會以每天發生一次的設定檔快照為單位執行。 批次決策會限制頻率，並一律從最近的快照載入設定檔。 嘗試批次決策API之前，在建立區段後，請等候最多24小時。

* **決定** 在Adobe Journey Optimizer中。 [瞭解如何建立決定](offer-activities/create-offer-activities.md)

<!-- in API doc, remove these info and add ref here-->

## 建立工作請求

若要建立新的工作請求，請遵循下列步驟。

1. 在 **[!UICONTROL 選件]** 功能表，開啟 **[!UICONTROL 批次決策]** 索引標籤然後按一下 **[!UICONTROL 建立請求]**.

   ![](assets/batch-create.png)

1. 為您的工作請求命名，然後選取應將工作資料傳送到的資料集。

1. 選取要鎖定的Adobe Experience Platform區段。

1. 選取您要用來將優惠傳送至區段的一或多個優惠決定範圍：
   1. 從清單中選取位置。
   1. 所選位置可用的決定隨即顯示。 選取您選擇的決定並按一下 **[!UICONTROL 新增]**.
   1. 重複此作業，視需要新增儘可能多的決定範圍。

   ![](assets/batch-decision.png)

1. 依預設，會針對每個設定檔傳回一個決定範圍的選件。 您可以使用以下專案調整傳回的優惠方案數量 **[!UICONTROL 每個設定檔的請求優惠]** 選項。 例如，如果您選取2，則會針對所選決定範圍顯示最佳的2個優惠方案。

   >[!NOTE]
   >
   >每個決定範圍最多可請求30個優惠。

1. 如果您想要在資料集中包含選件內容，請切換 **[!UICONTROL 包含內容]** 選項開啟。 此選項預設為停用。

1. 按一下 **[!UICONTROL 建立]** 以執行工作要求。

## 監視批次作業

所有請求的批次工作都可從以下位置存取： **[!UICONTROL 批次決策]** 標籤。 此外，搜尋和篩選工具也可協助您調整清單。

![](assets/batch-list.png)

### 工作請求狀態

建立工作請求後，批次工作會經歷多種狀態：

>[!NOTE]
>
>為確保您取得有關工作請求狀態的最新資訊，請使用工作旁邊的省略符號按鈕以重新整理。

1. **[!UICONTROL 已排入佇列]**：工作請求已建立且已進入處理佇列。 每個資料集一次最多可執行5個批次工作。 具有相同輸出資料集的任何其他批次請求都會新增至佇列。 前一個工作執行完畢後，系統會擷取已排入佇列的工作進行處理。
1. **[!UICONTROL 處理中]**：正在處理工作要求
1. **[!UICONTROL 擷取]**：工作要求已執行，結果資料正在選取的資料集中擷取，
1. **[!UICONTROL 已完成]**：工作要求已執行，而結果資料現在已儲存至選取的資料集。

   >[!NOTE]
   >
   >您可以按一下工作清單中的名稱，存取儲存工作結果的資料集。

如果在執行工作請求時發生錯誤，將會取得 **[!UICONTROL 錯誤]** 狀態。 請嘗試複製批次工作，以建立新請求。 [瞭解如何複製批次作業](#duplicate)

### 批次工作處理時間

每個批次工作的端對端時間是從工作負載建立到輸出資料集中有決策結果時的期間。

區段大小是影響端對端批次決定時間的主要因素。 如果符合資格的優惠方案已啟用全域頻率上限，則批次決定需要額外的時間才能完成。 以下是其各自區段大小的端對端處理時間的一些近似值，包含和不包含合格優惠方案的頻率上限：

已為合格優惠方案啟用頻率上限：

| 區段大小 | 端對端處理時間 |
|--------------|----------------------------|
| 1萬個以下的設定檔 | 7 分钟 |
| 100萬個以下的設定檔 | 30 分钟 |
| 1500萬個以下的設定檔 | 50 分钟 |

符合資格的優惠方案沒有頻率上限：

| 區段大小 | 端對端處理時間 |
|--------------|----------------------------|
| 1萬個以下的設定檔 | 6 分钟 |
| 100萬個以下的設定檔 | 8 分钟 |
| 1500萬個以下的設定檔 | 16 分钟 |

## 複製工作請求 {#duplicate}

您可以重複使用現有工作的資訊來建立新請求。

若要這麼做，請按一下復製圖示，編輯工作資訊（如有必要），然後按一下 **[!UICONTROL 建立]** 以建立新請求。

![](assets/batch-duplicate.png)
