---
title: 新增代表至優惠方案
description: 瞭解如何為優惠方案新增呈現
feature: Offers
topic: Integrations
role: User
level: Intermediate
exl-id: 718af505-7b7c-495e-8974-bd9c35d796bb
source-git-commit: 9657862f1c6bdb2399fcf3e6384bb9dec5b8f32b
workflow-type: tm+mt
source-wordcount: '660'
ht-degree: 9%

---

# 新增代表至優惠方案 {#add-representations}

>[!CONTEXTUALHELP]
>id="ajo_decisioning_representation"
>title="呈现"
>abstract="添加呈现以定义您的优惠在消息中显示的位置。优惠的呈现越多，在不同的投放上下文中使用该优惠的机会就越多。"

選件可顯示在訊息中的不同位置：在含有影像的頂端橫幅中、作為段落中的文字、作為HTML區塊等。 优惠的呈现越多，在不同的投放上下文中使用该优惠的机会就越多。

## 設定優惠方案宣告 {#representations}

若要新增一或多個代表至優惠方案並加以設定，請遵循下列步驟。

1. 對於第一個表示，從選取 **[!UICONTROL 頻道]** 將會使用的區段。

   ![](../assets/channel-placement.png)

   >[!NOTE]
   >
   >只有所選頻道的可用版位會顯示在 **[!UICONTROL 刊登]** 下拉式清單。

1. 從清單中選取位置。

   您也可以使用「 」旁的按鈕 **[!UICONTROL 刊登]** 下拉式清單來瀏覽所有版位。

   ![](../assets/browse-button-placements.png)

   您仍然可以在此處根據版位頻道和/或內容型別篩選版位。 選擇位置並按一下 **[!UICONTROL 選取]**.

   ![](../assets/browse-placements.png)

1. 新增內容至您的表現。 瞭解如何在 [本節](#content).

1. 新增影像或URL等內容時，您可以指定 **[!UICONTROL 目的地連結]**：按一下選件的使用者將被導向相對應的頁面。

   ![](../assets/offer-destination-link.png)

1. 最後，選取您選擇的語言，以協助識別和管理要向使用者顯示的內容。

1. 若要新增其他表示法，請使用 **[!UICONTROL 新增表示方式]** 按鈕，並視需要新增任意數量的表示。

   ![](../assets/offer-add-representation.png)

1. 新增所有表示後，請選取 **[!UICONTROL 下一個]**.

## 定義表示的內容 {#content}

您可以將不同型別的內容新增到表現中。

>[!NOTE]
>
>只有與版位內容型別對應的內容才可供使用。

### 添加图像 {#images}

如果選取的位置是影像型別，您可以新增來自 **Adobe Experience Cloud資產** 資料庫，資產集中存放庫，由 [!DNL Adobe Experience Manager Assets Essentials].

>[!NOTE]
>
> 使用方式 [Adobe Experience Manager Assets Essentials](https://experienceleague.adobe.com/docs/experience-manager-assets-essentials/help/introduction.html){target="_blank"}, you need to deploy [!DNL Assets Essentials] for your organization and make sure that users are a part of the **Assets Essentials Consumer Users** or/and **Assets Essentials Users** Product profiles. Learn more on [this page](https://experienceleague.adobe.com/docs/experience-manager-assets-essentials/help/get-started-admins/deploy-administer.html){target="_blank"}.

1. 選擇 **[!UICONTROL 資產庫]** 選項。

1. 選取 **[!UICONTROL 瀏覽]**.

   ![](../assets/offer-browse-asset-library.png)

1. 瀏覽資產以選取您選擇的影像

1. 单击&#x200B;**[!UICONTROL 选择]**。

   ![](../assets/offer-select-asset.png)

### 新增HTML或JSON檔案 {#html-json}

如果所選版位為HTML型別，您也可以新增來自的HTML或JSON內容 [Adobe Experience Cloud資產庫](https://experienceleague.adobe.com/docs/experience-manager-assets-essentials/help/introduction.html){target="_blank"})。

例如，您已在以下位置建立HTML電子郵件範本： [Adobe Experience Manager](https://experienceleague.adobe.com/docs/experience-manager.html){target="_blank"} 而且您想要將該檔案用於您的選件內容。 與其建立新檔案，您只需將範本上傳到 **資產庫** 以便在優惠的表示中重複使用它。

若要在代表中重複使用您的內容，請瀏覽 **資產庫** 如所述 [本節](#images) 並選取您選擇的HTML或JSON檔案。

![](../assets/offer-browse-asset-library-json.png)

### 新增URL {#urls}

若要從外部公用位置新增內容，請選取「 」 **[!UICONTROL URL]**，然後輸入要新增內容的URL位址。

您可以使用運算式編輯器個人化URL。 進一步瞭解 [個人化](../../personalization/personalize.md#use-expression-editor).

![](../assets/offer-content-url.png)

例如，您想要個人化顯示為選件的影像。 你想讓喜歡城市度假的使用者看紐約天際線，也想讓喜歡海灘度假的使用者看夏威夷北岸。

使用運算式編輯器，使用聯合結構描述擷取儲存在Adobe Experience Platform中的設定檔屬性。 [了解详情](https://experienceleague.adobe.com/docs/experience-platform/profile/union-schemas/union-schemas-overview.html){target="_blank"}

![](../assets/offer-content-url-personalization.png)

如果您指定 **[!UICONTROL 目的地連結]**，您也可以個人化按一下選件的使用者將導向哪個URL。

### 新增自訂文字 {#custom-text}

您也可以在選取相容版位時插入文字型別內容。

1. 選取 **[!UICONTROL 自訂]** 選項並按一下 **[!UICONTROL 新增內容]**.

   ![](../assets/offer-add-content.png)

   >[!NOTE]
   >
   >此選項不適用於影像型別的位置。

1. 輸入要在優惠方案中顯示的文字。

   ![](../assets/offer-text-content.png)

   您可以使用運算式編輯器個人化您的內容。 進一步瞭解 [個人化](../../personalization/personalize.md#use-expression-editor).

   ![](../assets/offer-personalization.png)

   >[!NOTE]
   >
   >僅限 **[!UICONTROL 設定檔屬性]**， **[!UICONTROL 區段會籍]** 和 **[!UICONTROL 輔助函式]** 來源可用於「決定管理」。

