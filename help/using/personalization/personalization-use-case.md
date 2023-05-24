---
solution: Journey Optimizer
product: journey optimizer
title: 個人化使用案例&colon；訂單狀態通知
description: 瞭解如何使用設定檔、優惠決定和內容資訊個人化訊息。
feature: Personalization
topic: Personalization
role: Data Engineer
level: Intermediate
keywords: 運算式，編輯器，使用案例，個人化
exl-id: 7d9c3d31-af57-4f41-aa23-6efa5b785260
source-git-commit: c0afa3e2bc6dbcb0f2f2357eebc04285de8c5773
workflow-type: tm+mt
source-wordcount: '502'
ht-degree: 2%

---

# 個人化使用案例：訂單狀態通知 {#personalization-use-case}

在此使用案例中，您將瞭解如何在單一推播通知訊息中使用多種型別的個人化。 將使用三種型別的個人化：

* **設定檔**：根據設定檔欄位的訊息個人化
* **優惠決定**：以決策管理變數為基礎的個人化
* **內容**：根據歷程中的內容資料進行個人化

此範例的目標是將事件推送至 [!DNL Journey Optimizer] 每次更新客戶訂單時。 接著會傳送推播通知給客戶，其中包含訂單和個人化優惠的相關資訊。

對於此使用案例，需要下列先決條件：

* 設定包含訂單編號、狀態及料號名稱的訂單事件。 请参阅此[章节](../event/about-events.md)。
* 建立決定，請參閱此 [區段](../offers/offer-activities/create-offer-activities.md).

## 步驟1 — 建立歷程 {#create-journey}

1. 按一下 **[!UICONTROL 歷程]** 選單並建立新歷程。

   ![](assets/perso-uc4.png)

1. 新增您的登入事件，以及 **推播** 動作活動。

   ![](assets/perso-uc5.png)

1. 設定並設計您的推播通知訊息。 请参阅此[章节](../push/create-push.md)。

## 步驟2 — 在設定檔中新增個人化 {#add-perso}

1. 在 **推播** 活動，按一下 **編輯內容**.

1. 按一下 **標題** 欄位。

   ![](assets/perso-uc2.png)

1. 輸入主旨並新增個人化設定檔。 使用搜尋列來尋找設定檔的名字欄位。 在主旨文字中，將游標置於要插入個人化欄位的位置，然後按一下 **+** 圖示。 单击&#x200B;**保存**。

   ![](assets/perso-uc3.png)

## 步驟3 — 在內容資料上新增個人化 {#add-perso-contextual-data}

1. 在 **推播** 活動，按一下 **編輯內容** 並按一下 **標題** 欄位。

   ![](assets/perso-uc9.png)

1. 選取 **內容屬性** 功能表。 內容屬性僅在歷程將內容資料傳遞至訊息時可用。 按一下 **Journey Orchestration**. 下列內容資訊隨即顯示：

   * **事件**：此類別會重新分組位於歷程中管道動作活動之前之事件中的所有欄位。
   * **歷程屬性**：與指定設定檔的歷程相關的技術欄位，例如歷程ID或遇到的特定錯誤。 進一步瞭解 [Journey Orchestration檔案](../building-journeys/expression/journey-properties.md).

   ![](assets/perso-uc10.png)

1. 展開 **事件** 料號，並尋找與您事件相關的訂單編號欄位。 您也可以使用搜尋方塊。 按一下 **+** 圖示在主旨文字中插入個人化欄位。 单击&#x200B;**保存**。

   ![](assets/perso-uc11.png)

1. 現在按一下 **內文** 欄位。

   ![](assets/perso-uc12.png)

1. 輸入訊息並插入，從 **[!UICONTROL 內容屬性]** 功能表、訂單料號名稱與訂單進度。

   ![](assets/perso-uc13.png)

1. 從左側選單中選取 **優惠決定** 以插入決策變數。 選取位置並按一下 **+** 圖示加以新增，並新增至內文中。

   ![](assets/perso-uc14.png)

1. 按一下驗證以確定沒有錯誤，然後按一下 **儲存**.

   ![](assets/perso-uc15.png)

## 步驟4 — 測試並發佈歷程 {#test-publish}

1. 按一下 **測試** 按鈕，然後按一下 **觸發事件**.

   ![](assets/perso-uc17.png)

1. 輸入測試中要傳遞的不同值。 測試模式僅適用於測試設定檔。 設定檔識別碼必須對應至測試設定檔。 按一下 **傳送**.

   ![](assets/perso-uc18.png)

   推播通知會傳送並顯示在測試設定檔的行動電話上。

   ![](assets/perso-uc19.png)

1. 確認沒有錯誤並發佈歷程。
