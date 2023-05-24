---
title: 创建 Web 页面
description: 瞭解如何在Journey Optimizer中編寫網頁及編輯其內容
feature: Web Channel
topic: Content Management
role: User
level: Beginner
exl-id: 3847ac1d-2c0a-4f80-8df9-e8e304faf261
source-git-commit: 803c9f9f05669fad0a9fdeeceef58652b6dccf70
workflow-type: tm+mt
source-wordcount: '1623'
ht-degree: 14%

---

# 创建 Web 页面 {#author-web}

一旦您 [已新增網路動作](create-web.md#create-web-campaign) 對於促銷活動，您可以使用網頁設計工具編輯網站內容。

在 [!DNL Journey Optimizer]，網頁製作功能由 **Adobe Experience Cloud Visual Helper** chrome瀏覽器擴充功能。 [了解详情](web-prerequisites.md#visual-authoring-prerequisites)

>[!CAUTION]
>
>若要能夠存取及編寫中的網頁，請 [!DNL Journey Optimizer] 使用者介面，請務必遵循下列先決條件： [本節](web-prerequisites.md).

[透過此影片瞭解如何創作網路行銷活動](#video)

## 編輯網頁內容 {#edit-web-content}

>[!CONTEXTUALHELP]
>id="ajo_web_url_to_edit_surface"
>title="确认要编辑的 URL"
>abstract="确认特定网页的 URL，用于编辑将应用到上面定义的 Web 表面的内容。网页必须使用 Adobe Experience Platform Web SDK 实施。"
>additional-url="https://experienceleague.adobe.com/docs/platform-learn/implement-web-sdk/overview.html?lang=zh-Hans" text="了解详情"

>[!CONTEXTUALHELP]
>id="ajo_web_url_to_edit_rule"
>title="输入 URL 以进行编辑"
>abstract="输入特定网页的 URL，用于编辑将应用到与规则匹配的所有页面上的内容。网页必须使用 Adobe Experience Platform Web SDK 实施。"
>additional-url="https://experienceleague.adobe.com/docs/platform-learn/implement-web-sdk/overview.html?lang=zh-Hans" text="了解详情"

若要開始編寫您的網頁行銷活動，請遵循下列步驟。

1. 從 **[!UICONTROL 動作]** 的標籤 [行銷活動](create-web.md#create-web-campaign)，選取 **[!UICONTROL 編輯內容]**.<!--change screen with rule-->

   ![](assets/web-campaign-edit-content.png)

1. 如果您已建立符合規則的頁面，則必須輸入符合此規則的任何URL：變更將套用至符合規則的所有頁面。 頁面內容隨即顯示。

   >[!NOTE]
   >
   >如果您輸入單一URL作為網頁表面，則會填入個人化的URL。

   ![](assets/web-edit-enter-url.png)

   >[!CAUTION]
   >
   >網頁必須包含 [Adobe Experience Platform Web SDK](https://experienceleague.adobe.com/docs/platform-learn/implement-web-sdk/overview.html?lang=zh-Hans){target="_blank"}. [了解详情](web-prerequisites.md#implementation-prerequisites)

1. 按一下 **[!UICONTROL 編輯網頁]** 以開始編寫。 網頁設計工具隨即顯示。

   ![](assets/web-designer.png)

   >[!NOTE]
   >
   >如果您嘗試載入無法載入的網站，則會顯示一則訊息，建議您安裝 [Visual Editing Helper瀏覽器擴充功能](#install-visual-editing-helper). 請參閱中疑難排解的一些提示 [本節](web-prerequisites.md#troubleshooting).

1. 從畫布中選取任何元素，例如影像、按鈕、段落、文字、容器、標題、連結等。 [了解详情](#content-components)

1. 使用:

   * 內容選單，用於編輯其內容、配置、插入連結或個人化等。

      ![](assets/web-designer-contextual-bar.png)

   * 右側面板頂端的圖示可編輯、複製、刪除或隱藏每個元素。

      ![](assets/web-designer-right-panel-icons.png)

   * 根據所選元素動態變更的右側面板。 例如，您可以編輯元素的背景、印刷樣式、框線、大小、位置、間距、效果或內嵌樣式。

      ![](assets/web-designer-right-panel.png)

>[!NOTE]
>
>網頁內容設計工具主要類似於電子郵件設計工具。 進一步瞭解 [設計內容使用 [!DNL Journey Optimizer]](../email/get-started-email-design.md).

## 使用元件 {#content-components}

>[!CONTEXTUALHELP]
>id="ajo_web_designer_components"
>title="将组件添加到网页"
>abstract="可将许多组件添加到网页，然后根据需要编辑这些组件。"

1. 從 **[!UICONTROL 元件]** 左窗格中選取專案。 您可以將下列元件新增至網頁，並視需要加以編輯：

   * [分隔条](../email/content-components.md#divider)
   * [HTML](../email/content-components.md#HTML)
   * [图像](../email/content-components.md#image)
   * 標題 — 使用此元件與使用 **[!UICONTROL 文字]** 電子郵件設計工具中的元件。 [了解详情](../email/content-components.md#text)
   * 段落 — 使用此元件類似於使用 **[!UICONTROL 文字]** 電子郵件設計工具中的元件。 [了解详情](../email/content-components.md#text)
   * 链接
   * [優惠決定](../email/add-offers-email.md)

   ![](assets/web-designer-components.png)

1. 將滑鼠指標暫留在頁面上，然後按一下 **[!UICONTROL 插入在前]** 或 **[!UICONTROL 插入在後]** 按鈕以將元件附加至頁面上的現有元素。

   ![](assets/web-designer-insert-components.png)

   >[!NOTE]
   >
   >若要取消選取元件，請按一下 **[!UICONTROL ESC]** 在畫布上方顯示的內容藍色橫幅中的按鈕。

1. 視需要直接在頁面的內容中編輯元件。

   ![](assets/web-designer-edit-header.png)

1. 調整從右邊內容窗格顯示的樣式，例如背景、文字顏色、邊框、大小、位置等。  — 視選取的元件而定。

   ![](assets/web-designer-header-style.png)

## 新增個人化和優惠方案

若要新增個人化，請選取容器，然後從顯示的內容功能表列中選取個人化圖示。 使用運算式編輯器新增變更。 [了解详情](../personalization/personalization-build-expressions.md)

![](assets/web-designer-personalization.png)

使用 **[!UICONTROL 優惠決定]** 要插入元件 [優惠方案](../offers/get-started/starting-offer-decisioning.md) 放入您的網頁。 此程式與以下情況相同： [新增優惠方案至電子郵件](../email/add-offers-email.md). 它會運用決策管理，挑選最適合提供給客戶的優惠方案。

![](assets/web-designer-offer.png)

## 管理修改 {#manage-modifications}

>[!CONTEXTUALHELP]
>id="ajo_web_designer_modifications"
>title="轻松管理所有更改"
>abstract="使用此窗格，您可以浏览和管理您添加到网页的所有调整和样式。"

您可以輕鬆管理新增至網頁的所有元件、調整和樣式。

1. 選取 **[!UICONTROL 修改]** 圖示以在左側顯示對應的窗格。

   ![](assets/web-designer-modifications-pane.png)

1. 您可以檢閱對頁面所做的每項變更。

1. 選取不要的修改，然後按一下刪除圖示以移除它。

   ![](assets/web-designer-modifications-delete.png)

   >[!CAUTION]
   >
   >刪除動作時請謹慎操作，因為動作可能會影響後續動作。

1. 使用 **[!UICONTROL 更多動作]** 按鈕在頂端 **[!UICONTROL 修改]** 窗格，一次刪除所有修改。

   ![](assets/web-designer-delete-modifications.png)

1. 從 **[!UICONTROL 更多動作]** 功能表您也可以只刪除無效的修改，亦即被其他變更覆寫的變更。 例如，如果您修改文字的顏色，然後刪除該文字，則顏色修改會變成無效，因為該文字已不存在。

1. 您也可以使用取消和重做動作 **[!UICONTROL 還原/重做]** 按鈕。

   ![](assets/web-designer-undo-redo.png)

   按一下並按住按鈕，以在 **[!UICONTROL 還原]** 和 **[!UICONTROL 取消復原]** 選項。 然後按一下按鈕本身，套用所需的動作。

## 使用點選追蹤 {#use-click-tracing}

網頁設計工具中的這項功能可讓您選取網站的任何元素，並追蹤該元素上的點按次數。

一旦您的行銷活動上線，您就可以檢查行銷活動網頁報告中每個元素的點按次數。 此資訊有助於改善網站使用者的體驗。 例如，如果 [網站報告](../reports/campaign-global-report.md#web-tab) 顯示有許多使用者點按了實際上無法點按的元素，您可能會想要新增該元素的連結。

1. 在頁面中選取元素，然後選擇 **[!UICONTROL 點選追蹤元素]** 從內容功能表。

   ![](assets/web-designer-click-track.png)

   >[!NOTE]
   >
   >可以選取任何專案（無論是否可點按）。

1. 對應的追蹤動作會自動顯示在 **[!UICONTROL 點選追蹤]** 左側的窗格。

   ![](assets/web-designer-click-track-pane.png)

1. 新增有意義的標籤以管理所有追蹤的元素，並在報表中輕鬆找到它們。 此 **[!UICONTROL CSS選取器]** 欄位會顯示尋找所選元素的資訊。

1. 重複上述步驟，視需要選取點選追蹤所需數量的其他元素。 對應的動作會全部列在左窗格中。

   ![](assets/web-designer-click-tracking-actions.png)

1. 若要移除元素上的點選追蹤，請選取對應的刪除圖示。

一旦您的行銷活動開始運作，您就可以檢查行銷活動報告 **[!UICONTROL Web]** 索引標籤以比較曝光次數、點按率和依元素的點按次數。 [了解详情](../reports/campaign-global-report.md#web-tab)

## 瀏覽網頁設計工具 {#navigate-web-designer}

### 使用階層連結 {#breadcrumbs}

1. 從畫布中選取任何元素。

1. 按一下 **[!UICONTROL 展開/收合階層連結]** 按鈕來快速顯示有關所選元素的資訊。

   ![](assets/web-designer-breadcrumbs.png)

1. 當您將游標停留在階層連結上時，對應的元素會在編輯器中反白顯示。

1. 使用它，您可以輕鬆導覽至視覺化編輯器中的任何父項、同層級專案或子項元素。

### 切換至瀏覽模式 {#browse-mode}

>[!CONTEXTUALHELP]
>id="ajo_web_designer_browse"
>title="使用浏览模式"
>abstract="在此模式下，您可以从要个性化的选定表面导航到确切的页面。"

您可以從預設值交換 **[!UICONTROL 設計]** 模式切換成 **[!UICONTROL 瀏覽]** 模式使用「專用」按鈕。

![](assets/web-designer-browse-mode.png)

從 **[!UICONTROL 瀏覽]** 模式，您可以從您想要個人化的所選表面瀏覽至確切頁面。

在處理經過驗證或無法從某個URL開始的頁面時，此功能特別有用。 例如，您將能夠進行驗證、導覽至您的帳戶頁面或購物車頁面，然後切換回 **[!UICONTROL 設計]** 模式，以便在您需要的頁面上執行變更。

### 變更裝置大小 {#change-device-size}

您可以將網頁設計工具顯示的裝置大小變更為預先定義的大小，例如 **[!UICONTROL 平板電腦]** 或 **[!UICONTROL 行動裝置橫向]**，或輸入所需的畫素數，以定義自訂大小。

您也可以將縮放焦點從25%變更為400%。

![](assets/web-designer-device.png)

變更裝置大小的功能專為可在各種裝置、視窗和熒幕大小上良好呈現的回應式網站所設計。 响应式网站自动调整和适应任意屏幕大小，包括台式机、笔记本电脑、平板电脑或手机。

>[!CAUTION]
>
>您可以編輯具有特定裝置大小的網頁體驗。 不過，只要選取器相同，這些變更就會套用至所有大小和裝置，而不只是您正在使用的裝置大小。 同樣地，在標準案頭檢視中編輯體驗時，會將變更套用至所有熒幕大小，而不僅僅是案頭檢視。
>
>目前， [!DNL Journey Optimizer] 不支援裝置大小特定的頁面變更。 這表示，舉例來說，如果您有另一個行動網站具有不同的網站結構，您應針對不同促銷活動中的行動網站進行特定變更。

## 測試網頁行銷活動 {#test-web-campaign}

>[!CONTEXTUALHELP]
>id="ajo_web_designer_preview"
>title="预览 Web 体验"
>abstract="模拟您将获得的 Web 体验。"

若要顯示修改後Web體驗的預覽，請遵循下列步驟。

>[!CAUTION]
>
>您必須具備可用的測試設定檔，以模擬將傳送哪些優惠給他們。 瞭解如何 [建立測試設定檔](../segment/creating-test-profiles.md).

1. 從任一網路促銷活動編輯內容畫面中，選取 **[!UICONTROL 模擬內容]**.

   <!--![](assets/web-designer-simulate.png)-->

   ![](assets/web-campaign-simulate.png)

1. 按一下 **[!UICONTROL 管理測試設定檔]** 以選取一或多個測試設定檔。
1. 此時會顯示修改後網頁的預覽。

   ![](assets/web-designer-preview.png)

1. 您也可以在預設瀏覽器中開啟它，或複製測試URL以將其貼到任何瀏覽器中。 這可讓您與團隊和利害關係人共用連結，這些利害關係人將能夠在行銷活動上線之前在任何瀏覽器中預覽新的Web體驗。

   >[!NOTE]
   >
   >複製測試URL時，顯示的內容是在中產生內容模擬時所使用的測試設定檔的個人化內容 [!DNL Journey Optimizer].

## 操作方法视频{#video}

以下影片說明如何在中使用Web設計工具編寫Web體驗 [!DNL Journey Optimizer] 行銷活動。

>[!VIDEO](https://video.tv.adobe.com/v/3418803/?quality=12&learn=on)
