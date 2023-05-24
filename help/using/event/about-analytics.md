---
solution: Journey Optimizer
product: journey optimizer
title: Adobe Analytics 集成
description: 瞭解如何在Journey Optimizer中運用Adobe Analytics資料
feature: Events
topic: Administration
role: Admin
level: Intermediate
keywords: analytics，整合， web sdk，平台
exl-id: 9d842722-e5eb-4743-849d-b7ba9448062f
source-git-commit: 16752d94647b25b4a86c34b77bda0f72fcfaf169
workflow-type: tm+mt
source-wordcount: '768'
ht-degree: 7%

---

# 使用Adobe Analytics資料 {#analytics-data}

您可以善用已透過Adobe Analytics或Web SDK擷取並串流至Adobe Experience Platform的所有網頁行為事件資料，以觸發歷程並自動化客戶體驗。

為了讓此功能與Adobe Analytics搭配使用，您必須：

1. 啟用您要使用的報表套裝。 [了解详情](#leverage-analytics-data)
1. 啟用Journey Optimizer以使用您的Adobe Analytics資料來源。 [了解详情](#activate-analytics-data)
1. 在歷程中新增特定事件。 [了解详情](#event-analytic)

>[!NOTE]
>
>本節僅適用於規則型事件，以及需要使用Adobe Analytics或Web SDK資料的客戶。
> 
>如果您使用Adobe Customer Journey Analytics，請參閱 [此頁面](../reports/cja-ajo.md).

## 設定Adobe Analytics或Web SDK資料 {#leverage-analytics-data}

您必須啟用來自Adobe Analytics或Adobe Experience Platform Web SDK的資料，才能在歷程中使用。

为此，请执行以下步骤：

1. 瀏覽至 **[!UICONTROL 來源]** 功能表。

1. 在Adobe Analytics區段中，選取 **[!UICONTROL 新增資料]**

   ![](assets/ajo-aa_1.png)

1. 從可用的Adobe Analytics報表套裝清單中，選取 **[!UICONTROL 報告套裝]** 以啟用。 然後，按一下 **[!UICONTROL 下一個]**.

   ![](assets/ajo-aa_2.png)

1. 選擇您要使用預設或自訂結構描述。

1. 從 **[!UICONTROL 資料流詳細資料]** 熒幕，選擇 **[!UICONTROL 資料流名稱]**.

1. 完成設定後，按一下 **[!UICONTROL 完成]**.

   ![](assets/ajo-aa_3.png)

如此將可啟用該報表套裝的Analytics來源聯結器。 只要有資料進來，就會轉換為體驗事件並傳送到Adobe Experience Platform。

![](assets/ajo-aa_4.png)

在中進一步瞭解Adobe Analytics來源聯結器  [Adobe Experience Platform檔案](https://experienceleague.adobe.com/docs/experience-platform/sources/connectors/adobe-applications/analytics.html?lang=zh-Hans){target="_blank"} and [tutorial](https://experienceleague.adobe.com/docs/experience-platform/sources/ui-tutorials/create/adobe-applications/analytics.html?lang=zh-Hans){target="_blank"}.

## 啟用此設定 {#activate-analytics-data}

完成此設定後，請聯絡Adobe以啟用您的Journey Optimizer環境來使用此資料來源。 只有Adobe Analytics資料來源才需要此步驟。 若要執行此動作：

1. 取得資料來源ID。 使用者介面中提供了此資訊：瀏覽至您從 **資料流** 的標籤 **來源** 功能表。 尋找此變數最簡單的方式是篩選Adobe Analytics來源。
1. 請聯絡Adobe客戶服務，提供下列詳細資料：

   * 主旨：為歷程啟用Adobe Analytics事件

   * 內容：請啟用我的環境以使用AA事件。

      * 組織ID： &quot;XXX@AdobeOrg&quot;

      * 資料來源ID： &quot;ID： xxxxx&quot;

1. 一旦您確認環境已就緒，便可在歷程中使用Adobe Analytics資料。

## 使用Adobe Analytics或Web SDK資料建立包含事件的歷程 {#event-analytics}

您現在可以根據Adobe Analytics或Adobe Experience Platform Web SDK資料建立事件，以便在歷程中使用。

在以下範例中，瞭解如何鎖定在購物車中新增產品的使用者：

* 如果訂單完成，使用者會在兩天後收到後續電子郵件，要求您提供意見。
* 如果訂單未完成，使用者會收到一封電子郵件，提醒他們完成訂單。

1. 從Adobe Journey Optimizer存取 **[!UICONTROL 設定]** 功能表。

1. 然後，選取 **[!UICONTROL 管理]** 從 **[!UICONTROL 事件]** 卡片。

   ![](assets/ajo-aa_5.png)

1. 按一下 **[!UICONTROL 建立事件]**. 事件配置窗格将在屏幕右侧打开。

1. 填入 **[!UICONTROL 事件]** 引數：

   * **[!UICONTROL 名稱]**：個人化您的名稱， **[!UICONTROL 事件]**.
   * **[!UICONTROL 型別]**：選擇 **[!UICONTROL 單一]** 型別。 [了解详情](../event/about-events.md)
   * **[!UICONTROL 事件ID型別]**：選擇 **[!UICONTROL 以規則為基礎]** 事件ID型別。 [了解详情](../event/about-events.md#event-id-type)
   * **[!UICONTROL 結構描述]**：選取Analytics或WebSDK結構描述 [建立於以下日期之前：](#leverage-analytics-data).
   * **[!UICONTROL 欄位]**：選取裝載欄位。 [了解详情](../event/about-creating.md#define-the-payload-fields)
   * **[!UICONTROL 事件ID條件]**：定義條件以識別將觸發您歷程的事件。

      在此，當客戶將專案新增至購物車時會觸發事件。
   * **[!UICONTROL 設定檔識別碼]**：從您的裝載欄位選擇欄位或定義公式，以識別與事件相關聯的人員。

   ![](assets/ajo-aa_6.png)

1. 設定後，選取 **[!UICONTROL 儲存]**.

現在事件已準備就緒，請建立歷程以使用它。

1. 從 **[!UICONTROL 歷程]** 功能表、開啟或建立歷程。 有关详细信息，请参阅[此部分](../building-journeys/journey-gs.md)。

1. 將先前設定的Analytics事件新增至您的歷程。

   ![](assets/ajo-aa_8.png)

1. 新增完成訂單時觸發的事件。

1. 從您的 **[!UICONTROL 事件功能表]**，選取 **[!UICONTROL 定義事件逾時]** 和 **[!UICONTROL 設定逾時路徑]** 選項。

   ![](assets/ajo-aa_9.png)

1. 從逾時路徑中新增 **[!UICONTROL 電子郵件]** 動作。 此路徑將用來傳送電子郵件給未完成訂單的客戶，以提醒他們仍可使用購物車。

1. 新增 **[!UICONTROL 等待]** 活動，並將其設定為所需的持續時間。

   ![](assets/ajo-aa_10.png)

1. 然後，新增 **[!UICONTROL 電子郵件動作]**. 在這封電子郵件中，將會提示客戶對所下訂單提供意見。

您現在可以測試並發佈您的歷程。 [了解详情](../building-journeys/publishing-the-journey.md)

![](assets/ajo-aa_7.png)
