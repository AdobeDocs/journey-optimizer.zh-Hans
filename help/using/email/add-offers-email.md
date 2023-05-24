---
solution: Journey Optimizer
product: journey optimizer
title: 添加个性化优惠
description: 瞭解如何將個人化優惠方案新增至您的訊息
feature: Journeys
topic: Content Management
role: User
level: Intermediate
keywords: 優惠，決定，電子郵件，個人化，決定
exl-id: 1e648eca-b5ca-4767-b45d-c179243e347f
source-git-commit: 803c9f9f05669fad0a9fdeeceef58652b6dccf70
workflow-type: tm+mt
source-wordcount: '641'
ht-degree: 1%

---

# 添加个性化优惠 {#deliver-personalized-offers}

在 [!DNL Journey Optimizer] 電子郵件中，您可以插入將運用決策管理引擎的決策，以挑選要提供給客戶的最佳優惠方案。

例如，您可以新增一項決定，該決定會在您的電子郵件中顯示特殊的折扣優惠，該優惠會根據收件者的忠誠度等級而有所不同。

>[!IMPORTANT]
>
>如果對歷程訊息中使用的優惠決定進行變更，您需要取消發佈歷程並重新發佈。  這將確保將變更納入歷程的訊息中，且訊息與最新更新一致。

* 有關如何建立和管理優惠方案的詳細資訊，請參閱 [本節](../offers/get-started/starting-offer-decisioning.md).
* 對於 **完整的端對端範例** 顯示如何設定優惠方案、在決定中使用優惠方案，以及在電子郵件中運用此決定、結帳 [本節](../offers/offers-e2e.md#insert-decision-in-email).

➡️ [瞭解如何在本影片中新增優惠方案作為個人化](#video-offers)

## 在電子郵件中插入決定 {#insert-offers}

>[!CAUTION]
>
>開始之前，您必須 [定義優惠決定](../offers/offer-activities/create-offer-activities.md).

若要將決定插入電子郵件訊息，請遵循下列步驟：

1. 建立您的電子郵件，然後開啟「電子郵件設計工具」以設定其內容。

1. 新增 **[!UICONTROL 優惠決定]** 內容元件。

   ![](assets/deliver-offer-component.png)

   瞭解如何在中使用內容元件 [本節](content-components.md).

1. 此 **[!UICONTROL 優惠決定]** 標籤會顯示在右方的浮動視窗中。 按一下 **[!UICONTROL 選取優惠決定]**：

   1. 在顯示的視窗中，選取與您要顯示之優惠方案對應的版位。

      [版位](../offers/offer-library/creating-placements.md) 是用來展示優惠方案的容器。 在此範例中，我們將使用「電子郵件上層影像」位置。 此版位已建立在選件資料庫中，用來顯示位於訊息頂端的影像型別選件。

   1. 與所選位置相符的決定隨即顯示。 選取要在內容元件中使用的決定，然後按一下 **[!UICONTROL 新增]**.

      >[!NOTE]
      >
      >清單中只會顯示與所選位置相容的決策。 在此範例中，只有一個優惠方案活動符合「電子郵件熱門影像」位置。

      ![](assets/deliver-offer-placement.png)

決定現在已新增至元件。 儲存變更後，您的優惠已準備好在傳送訊息作為歷程的一部分時顯示在相關的設定檔中。

>[!NOTE]
>
>當您更新訊息中直接或間接參考的優惠、遞補優惠、優惠集合或優惠決定時，更新會自動反映在相對應的訊息中。

## 預覽電子郵件中的優惠方案 {#preview-offers-in-email}

您可以使用來預覽屬於新增至電子郵件決定一部分的不同優惠方案 **[!UICONTROL 選件]** 區段或內容元件箭頭。

![](assets/deliver-offer-preview.png)

若要以客戶設定檔顯示屬於決策一部分的不同優惠，請遵循下列步驟。

>[!NOTE]
>
>您必須有可用的測試設定檔，才能預覽訊息。 瞭解如何 [建立測試設定檔](../segment/creating-test-profiles.md).

1. 選取要用於預覽選件的測試設定檔：

   1. 按一下 **[!UICONTROL 模擬內容按鈕]** 按鈕然後選擇名稱空間，以用於識別來自 **[!UICONTROL 身分名稱空間]** 欄位。

      >[!NOTE]
      >
      >在此範例中，我們使用 **電子郵件** 名稱空間。 進一步瞭解Adobe Experience Platform身分識別名稱空間 [在本節中](../segment/get-started-identity.md).

   1. 在 **[!UICONTROL 身分值]** 欄位，輸入值以識別測試設定檔。 在此範例中，輸入測試設定檔的電子郵件地址。

   <!--For example enter smith@adobe.com and click the **[!UICONTROL Add profile]** button.-->

   1. 新增其他設定檔，以便您根據設定檔資料測試訊息的不同變體。

      ![](assets/deliver-offer-test-profiles.png)


1. 按一下 **[!UICONTROL 預覽]** 索引標籤以測試您的訊息，然後選取測試設定檔。 將顯示與所選設定檔（女性）對應的優惠方案。

   ![](assets/deliver-offer-test-profile-female-preview.png)

   您可以選取其他測試設定檔，以預覽訊息每個變體的電子郵件內容。 訊息內容中現在會顯示與所選測試設定檔（現在為男性）對應的選件。

深入瞭解檢查訊息預覽的詳細步驟 [本節](#preview-your-messages).

## 操作方法视频{#video-offers}

瞭解如何在中新增決策管理元件至訊息 [!DNL Journey Optimizer].

>[!VIDEO](https://video.tv.adobe.com/v/334088?quality=12)
