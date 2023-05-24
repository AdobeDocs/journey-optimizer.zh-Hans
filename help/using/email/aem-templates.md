---
solution: Journey Optimizer
product: journey optimizer
title: 使用AEM範本
description: 瞭解如何在AEM中建立範本並將其匯出至Journey Optimizer
hide: true
hidefromtoc: true
feature: Overview
topic: Content Management
role: User
level: Beginner
badge: label="Beta" type="Informative"
exl-id: e4935129-c1cb-41b1-b84d-cd419053c303
source-git-commit: 803c9f9f05669fad0a9fdeeceef58652b6dccf70
workflow-type: tm+mt
source-wordcount: '768'
ht-degree: 3%

---

# 使用Adobe Experience Manager範本 {#aem-templates}

>[!AVAILABILITY]
>
>與Adobe Experience Manager的整合目前僅供特定使用者使用，且為測試版。
> 身為測試版使用者，請使用 [此表單](https://forms.office.com/pages/responsepage.aspx?id=Wht7-jR7h0OUrtLBeN7O4Wf0cbVTQ3tCpW_unE-w8-JUN1FaNlAzNkhPSUdaSkJXVFRCNTRJNVRFSy4u){target="_blank"} 以分享意見。

透過Adobe Journey Optimizer，您可以透過Adobe Experience Manager網站建立自訂的訊息。 首先，使用Adobe Experience Manager的內容來源設計範本，然後傳送至Adobe Journey Optimizer。 共用後，您就可以在Adobe Journey Optimizer的電子郵件設計工具中存取這些範本，以簡化製作及傳送訊息給所需對象的程式。

## 先决条件 {#prerequisites}

開始使用此功能之前，請確定您已符合下列需求：

* **Experience Manager設定**

   此功能適用於 [Adobe Experience Manager as a Cloud Service](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/overview/introduction.html){target="_blank"}.

   在Beta版計畫中，Cloud Service設定是由Adobe Experience Manager中的Adobe執行，以連線至Adobe Journey Optimizer。

* **Permissions**

   若要在Adobe Journey Optimizer中建立、編輯和刪除內容範本，您必須具備 **[!DNL Manage Library Items]** 許可權包含在 **[!DNL Content Library Manager]** 產品設定檔。 [了解详情](../administration/ootb-product-profiles.md#content-library-manager)

## 护栏和限制{#aem-templates-limitations}

若要進一步最佳化Adobe Experience Manager與Adobe Journey Optimizer搭配使用，請務必注意下列額外護欄和限制：

* Experience Manager範本中的個人化需使用正確的Journey Optimizer語法，才能生效。 [了解详情](../personalization/personalization-syntax.md)

* 目前不支援大量範本匯出，必須個別匯出範本。

* Experience Manager與Journey Optimizer之間目前無法同步。 如果Experience Manager範本在傳送至Journey Optimizer後有所變更，使用者必須重新匯出範本，並重新傳送至Journey Optimizer。

## 傳送範本至Journey Optimizer{#aem-templates-send}

若要將Adobe Experience Manager範本匯出至Adobe Journey Optimizer，請遵循下列步驟：

1. 在您的Adobe Experience Manager首頁中，選取 **[!UICONTROL 對外行銷]**.

   ![](assets/aem-outbound-menu.png)

1. 您可以從內容資料庫中使用先前設定的範本，或從頭開始建立範本。 [了解详情](https://experienceleague.adobe.com/docs/experience-manager-65/authoring/authoring/managing-pages.html?lang=en#creating-a-new-page)

1. 將Journey Optimizer個人化語法併入範本中，即可增強其自訂功能。 [了解详情](../personalization/personalization-syntax.md)

   ![](assets/aem_ajo_4.png)

1. 選取您要匯出至Journey Optimizer的範本，然後按一下 **[!UICONTROL 傳送至]** 進階功能表中的。

   ![](assets/aem-advanced-menu.png)

1. 輸入 **[!UICONTROL 名稱]** 並選取目標 **[!UICONTROL Sandbox]**.

   ![](assets/aem-send-template-settings.png)

1. 在您按一下 **[!UICONTROL 傳送]** 按鈕，匯出程式就會開始。 匯出完成後，您會在使用者介面中看到下列訊息：「範本「XX」已成功傳送至AJO」。

範本會新增至所選沙箱的Adobe Journey Optimizer內容範本。

## 使用及個人化Adobe Experience Manager範本{#aem-templates-perso}

在Journey Optimizer中提供Experience Manager範本作為內容範本後，您就可以識別並整合電子郵件的必要內容，包括個人化。

1. 在Journey Optimizer中，從 **[!UICONTROL 內容範本]** 功能表，存取您匯入的範本。

   ![](assets/aem_ajo_1.png)

1. 按一下 **[!UICONTROL 警報]** 按鈕時，您可以快速檢查是否有任何重要設定遺失。 這將有助於確保您的訊息已正確設定，並防止任何潛在錯誤或問題。

   ![](assets/aem_ajo_2.png)

1. 在 **[!UICONTROL 範本屬性]** 視窗，按一下 **[!UICONTROL 管理存取權]** 按鈕來指派自訂或核心資料使用標籤給您的範本。 [進一步瞭解物件層級存取控制(OLAC)](../administration/object-based-access.md)

1. 若要進一步個人化您的Experience Manager範本並新增自訂個人化至您的內容，請按一下 **[!UICONTROL 編輯內容]**. 這可讓您輕鬆進行變更，並根據您的特定需求量身打造範本。 [了解详情](get-started-email-design.md)

   >[!NOTE]
   >
   > 如果您想要編輯並個人化您的範本，則只能使用相容性模式。

1. 當您的內容範本準備就緒時， [測試及驗證](content-templates.md#test-template).

1. 定義內容後，您可以在建立新電子郵件時透過瀏覽 **[!UICONTROL 已儲存的範本]** 集合。 然後，選取 **[!UICONTROL 使用此範本]**.

   ![](assets/aem_ajo_3.png)

1. 您現在可以編輯及個人化您的內容。 有關如何建立電子郵件內容的詳細資訊，請參閱此 [頁面](content-from-scratch.md).

   ![](assets/aem_ajo_5.png)

1. 如果您已將個人化內容新增至Experience Manager範本，請按一下 **[!UICONTROL 模擬內容]** 以使用測試設定檔預覽其顯示在訊息中的方式。

[進一步瞭解預覽和測試設定檔](../email/preview.md)

   ![](assets/aem_ajo_6.png)

1. 檢視訊息預覽時，任何個人化元素都會自動取代為所選測試設定檔中的對應資料。

   如有需要，可透過新增其他測試設定檔 **[!UICONTROL 管理測試設定檔]** 按鈕。

   ![](assets/aem_ajo_7.png)

當您的電子郵件準備就緒時，請完成 [歷程](../building-journeys/journey-gs.md) 或 [行銷活動](../campaigns/create-campaign.md)，並啟動以傳送訊息。
