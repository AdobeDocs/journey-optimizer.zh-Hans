---
title: 在歷程中建立應用程式內通知
description: 瞭解如何在Journey Optimizer中建立應用程式內訊息
feature: Overview
topic: Content Management
role: User
level: Beginner
keywords: 应用程序内、消息、创建、入门
hide: true
hidefromtoc: true
exl-id: b774e34f-8225-41a0-a2ec-b91d3a86cf2b
source-git-commit: 252011710574122c1f321a388b65bdafb7c666df
workflow-type: tm+mt
source-wordcount: '553'
ht-degree: 5%

---

# 在历程中创建应用程序内消息 {#create-in-app-journey}

>[!AVAILABILITY]
>
>應用程式內活動目前僅供選取使用者使用，且為測試版。 要加入 Beta 版计划，请联系 Adobe 客户关怀团队。

1. 開啟您的歷程，然後拖放 **[!UICONTROL 應用程式內]** 活動來自 **[!UICONTROL 動作]** 區段。

   當設定檔到達其歷程結尾時，顯示給他們的任何應用程式內訊息都會自動過期。 因此，會在應用程式內活動後自動新增等待活動，以確保計時正確。

   ![](assets/in_app_journey_1.png)

1. 輸入 **[!UICONTROL 標籤]** 和 **[!UICONTROL 說明]** 以取得訊息。

1. 選擇 [應用程式內表面](inapp-configuration.md) 以使用。

   ![](assets/in_app_journey_2.png)

1. 您現在可以開始使用設計內容 **[!UICONTROL 編輯內容]** 按鈕。 [了解详情](design-in-app.md)

1. 按一下 **[!UICONTROL 編輯觸發程式]** 以設定您的觸發器。

   ![](assets/in_app_journey_4.png)

1. 選擇應用程式內訊息作用中時的觸發頻率：

   * **[!UICONTROL 每次都顯示]**：一律顯示中選取的事件時的訊息 **[!UICONTROL 行動應用程式觸發程式]** 下拉式清單隨即出現。
   * **[!UICONTROL 顯示一次]**：只會在中第一次選取事件時顯示此訊息 **[!UICONTROL 行動應用程式觸發程式]** 下拉式清單隨即出現。
   * **[!UICONTROL 顯示至點進為止]**：當在中選取事件時顯示此訊息 **[!UICONTROL 行動應用程式觸發程式]** 下拉式清單會一直出現，直到SDK以「已點按」的動作傳送互動事件為止。

1. 從 **[!UICONTROL 行動應用程式觸發程式]** 在下拉式清單中，選擇將觸發訊息的事件和條件：

   1. 從左側下拉式清單中，選取觸發訊息所需的事件。
   1. 從右側的下拉式清單中，選取所選事件所需的驗證。
   1. 按一下 **[!UICONTROL 新增]** 按鈕（如果要觸發器考慮多個事件或條件）。 然後，重複上述步驟。
   1. 選取事件的連結方式，例如，選擇 **[!UICONTROL 和]** 如果您需要 **兩者** 觸發器設為true，以便顯示或選擇訊息 **[!UICONTROL 或]** 如果您想要顯示訊息，如果 **兩者之一** 的觸發程式為true。
   1. 按一下 **[!UICONTROL 儲存]** 您的觸發器設定完成時。

   ![](assets/in_app_journey_3.png)

1. 如有必要，請拖放其他動作或事件以完成您的歷程流程。 [了解详情](../building-journeys/about-journey-activities.md)

1. 應用程式內訊息準備就緒後，請完成設定並發佈您的歷程以將其啟用。

有關如何設定歷程的詳細資訊，請參閱 [此頁面](../building-journeys/journey-gs.md).

## 應用程式內活動限制 {#in-app-activity-limitations}

* 此功能目前不適用於醫療保健客戶。

* 個人化只能包含設定檔屬性。

* 應用程式內顯示會與歷程期限繫結，這表示當設定檔的歷程結束時，該歷程中的所有應用程式內訊息將不再顯示該設定檔。  因此，無法直接從歷程活動停止應用程式內訊息。 相反地，您需要結束整個歷程，才能停止將應用程式內訊息顯示給設定檔。

* 在測試模式中，應用程式內顯示取決於歷程的有效期限。 為避免歷程在測試期間過早結束，請調整 **[!UICONTROL 等待時間]** 您的價值 **[!UICONTROL 等待]** 活動。

* **[!UICONTROL 反應]** 活動無法用於對應用程式內開啟或點按做出反應。

* 使用者設定檔到達畫布中的應用程式內活動時，與他們開始看到應用程式內訊息時，就會發生啟用延遲。 此延遲的範圍為15分鐘到1小時。

**相关主题：**

* [設計應用程式內訊息](design-in-app.md)
* [測試並傳送您的應用程式內訊息](send-in-app.md)
* [应用程序内报告](../reports/campaign-global-report.md#inapp-report)
* [應用程式內設定](inapp-configuration.md)
