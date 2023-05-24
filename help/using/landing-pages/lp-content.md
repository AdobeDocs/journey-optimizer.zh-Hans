---
solution: Journey Optimizer
product: journey optimizer
title: 定義登入頁面特定內容
description: 瞭解如何在Journey Optimizer中設計登入頁面特定內容
feature: Landing Pages
topic: Content Management
role: User
level: Beginner
keywords: 登陸，登陸頁面，建立，頁面，表單，元件
exl-id: 5bf023b4-4218-4110-b171-3e70e0507fca
source-git-commit: cda4c1d88fedc75c7fded9971e45fdc9740346c4
workflow-type: tm+mt
source-wordcount: '1324'
ht-degree: 11%

---

# 定義登入頁面特定內容 {#lp-content}

>[!CONTEXTUALHELP]
>id="ac_lp_components"
>title="使用内容组件"
>abstract="内容组件是空的内容占位符，您可用它来创建登陆页面的版面。要定义特定内容使得用户能够进行选择并提交其选择内容，请使用表单组件。"
>additional-url="https://experienceleague.adobe.com/docs/journey-optimizer/using/email/design-email/add-content/content-components.html#add-content-components" text="添加内容组件"

若要設計登入頁面內容，您可以使用與電子郵件的相同元件。 [了解详情](../email/content-components.md#add-content-components)

若要設計特定內容，讓使用者能夠選取並提交其選擇， [使用表單元件](#use-form-component) 並定義其 [登入頁面特定樣式](#lp-form-styles).

>[!NOTE]
>
>您也可以建立點進登陸頁面，而不使用 **[!UICONTROL 表單]** 元件。 在此情況下，登入頁面會顯示給使用者，但使用者不需要提交任何表單。 如果您只想顯示登陸頁面，而不需要收件者採取任何動作（例如選擇加入或選擇退出），或想提供不需要使用者輸入的資訊，這個功能會很有用。

使用登入頁面內容設計工具，您也可以運用來自子頁面中主要頁面的內容資料。 [了解详情](#use-primary-page-context)

## 使用表單元件 {#use-form-component}

>[!CONTEXTUALHELP]
>id="ac_lp_formfield"
>title="设置表单组件字段"
>abstract="定义您的收件人如何从登陆页面查看和提交他们的选择。"
>additional-url="https://experienceleague.adobe.com/docs/journey-optimizer/using/landing-pages/landing-pages-design/lp-content.html#lp-form-styles" text="定义登陆页面表单样式"

>[!CONTEXTUALHELP]
>id="ac_lp_submission"
>title="单击按钮时会出现的情况"
>abstract="定义在用户提交登陆页面表单时将会出现的情况。"

若要定義可讓使用者從您的登入頁面選取並提交其選擇的特定內容，請使用 **[!UICONTROL 表單]** 元件。 若要這麼做，請遵循下列步驟。

1. 拖放登入頁面特定的 **[!UICONTROL 表單]** 元件從左側浮動視窗移入主工作區。

   ![](assets/lp_designer-form-component.png)

   >[!NOTE]
   >
   >此 **[!UICONTROL 表單]** 元件只能在同一個頁面上使用一次。

1. 选择模式。此 **[!UICONTROL 表單內容]** 標籤會顯示在右側的浮動視窗中，讓您編輯表單的不同欄位。

   ![](assets/lp_designer-form-content-options.png)

   >[!NOTE]
   >
   >切換至 **[!UICONTROL 樣式]** 標籤來編輯表單元件內容的樣式。 [了解详情](#define-lp-styles)

1. 從 **[!UICONTROL 核取方塊1]** 區段，您可以編輯對應至此核取方塊的標籤。

1. 定義此核取方塊是否要將使用者選擇加入或退出：他們是否同意接收通訊或要求不再聯絡？

   ![](assets/lp_designer-form-update.png)

   從下列三個選項中選取：

   * **[!UICONTROL 如果選取，則選擇加入]**：使用者需要核取方塊才能同意（選擇加入）。
   * **[!UICONTROL 如果選取，則選擇退出]**：使用者需要核取方塊以移除其同意（選擇退出）。
   * **[!UICONTROL 如果選取，則選擇加入；如果未選取，則選擇退出]**：此選項可讓您為選擇加入/選擇退出插入單一核取方塊。 用户需要选中复选框来表示同意（选择启用），取消选中该复选框以取消同意（选择禁用）。

1. 選擇要在下列三個選項之間更新的內容：

   ![](assets/lp_designer-form-update-options.png)

   * **[!UICONTROL 訂閱清單]**：如果設定檔選取此核取方塊，您必須選取將更新的訂閱清單。 進一步瞭解 [訂閱清單](subscription-list.md).

      <!--![](assets/lp_designer-form-subs-list.png)-->

   * **[!UICONTROL 頻道（電子郵件）]**：選擇加入或選擇退出會套用至整個管道。 例如，如果選擇退出的設定檔有兩個電子郵件地址，則這兩個地址都會從您的所有通訊中排除。

   * **[!UICONTROL 電子郵件身分]**：選擇加入或選擇退出僅適用於用來存取登入頁面的電子郵件地址。 例如，如果設定檔有兩個電子郵件地址，則只有用於選擇加入的電子郵件地址會收到您品牌的通訊。

1. 按一下 **[!UICONTROL 新增欄位]** > **[!UICONTROL 核取方塊]** 以新增另一個核取方塊。 重複上述步驟以定義其屬性。

   ![](assets/lp_designer-form-checkbox-2.png)

1. 您也可以新增 **[!UICONTROL 文字欄位]**.

   ![](assets/lp_designer-form-add-text-field.png)

   * 輸入 **[!UICONTROL 標籤]** 會顯示在表單中欄位頂端的欄位。

   * 輸入 **[!UICONTROL 預留位置]** 文字。 它將顯示在欄位中，然後使用者填寫欄位。

   * 檢查 **[!UICONTROL 將表單欄位設為必填]** 選項（如果需要）。 在此情況下，僅當使用者已填入此欄位時，才能提交登入頁面。 如果未填寫必填欄位，則當使用者提交頁面時將顯示錯誤訊息。

   ![](assets/lp_designer-form-text-field.png)

1. 新增所有需要的核取方塊和/或文字欄位後，請按一下 **[!UICONTROL 行動號召]** 以展開對應的區段。 它可讓您定義 **[!UICONTROL 表單]** 元件。

   ![](assets/lp_designer-form-call-to-action.png)

1. 定義按一下按鈕後會發生什麼事：

   * **[!UICONTROL 重新導向URL]**：輸入使用者將重新導向的頁面的URL。
   * **[!UICONTROL 確認文字]**：輸入將顯示的確認文字。
   * **[!UICONTROL 子頁面的連結]**：設定 [子頁面](create-lp.md#configure-subpages) 並從顯示的下拉式清單中選取它。

   ![](assets/lp_designer-form-confirmation-action.png)

1. 定義發生錯誤時，按一下按鈕後會發生什麼情況：

   * **[!UICONTROL 重新導向URL]**：輸入使用者將重新導向的頁面的URL。
   * **[!UICONTROL 錯誤文字]**：輸入將會顯示的錯誤文字。 定義「 」時，您可以預覽錯誤文字 [表單樣式](#define-lp-styles).

   * **[!UICONTROL 子頁面的連結]**：設定 [子頁面](create-lp.md#configure-subpages) 並從顯示的下拉式清單中選取它。

   ![](assets/lp_designer-form-error.png)

1. 如果您想在提交表單時進行其他更新，請選取 **[!UICONTROL 選擇加入]** 或 **[!UICONTROL 選擇退出]**，並定義您是否要更新訂閱清單、頻道或只是使用的電子郵件地址。

   ![](assets/lp_designer-form-additionnal-update.png)

1. 儲存內容並按一下頁面名稱旁的箭頭，即可返回 [登陸頁面屬性](create-lp.md#configure-primary-page).

   ![](assets/lp_designer-form-save.png)

## 定义登陆页面表单样式 {#lp-form-styles}

1. 若要修改表單元件內容的樣式，請隨時切換至 **[!UICONTROL 樣式]** 標籤。

   ![](assets/lp_designer-form-style.png)

1. 此 **[!UICONTROL 欄位]** 「區段」預設為展開，可讓您編輯文字欄位的外觀，例如標籤和預留位置字型、標籤位置、欄位背景顏色或欄位邊框。

   ![](assets/lp_designer-form-style-fields.png)

1. 展開 **[!UICONTROL 核取方塊]** 區段來定義核取方塊及對應文字的外觀。 例如，您可以調整字型系列或大小，或是核取方塊邊框顏色。

   ![](assets/lp_designer-form-style-checkboxes.png)

1. 展開 **[!UICONTROL 按鈕]** 截面來修改元件表單中按鈕的外觀。 例如，您可以變更字型、新增框線、在游標停留時編輯標籤顏色，或調整按鈕的對齊方式。

   ![](assets/lp_designer-form-style-buttons.png)

   您可以使用來預覽某些設定，例如暫留時的按鈕標籤顏色。 **[!UICONTROL 模擬內容]** 按鈕。 進一步瞭解測試登入頁面 [此處](create-lp.md#test-landing-page).

   <!--![](assets/lp_designer-form-style-buttons-preview.png)-->

1. 展開 **[!UICONTROL 表單版面配置]** 區段來編輯版面設定，例如背景顏色、邊框間距或邊界。

   ![](assets/lp_designer-form-style-layout.png)

1. 展開 **[!UICONTROL 表單錯誤]** 區段，調整發生問題時顯示的錯誤訊息顯示。 核取對應的選項以預覽表單上的錯誤文字。

   ![](assets/lp_designer-form-error-preview.png)

## 使用主要頁面內容 {#use-primary-page-context}

您可以使用來自相同登陸頁面中其他頁面的內容資料。

例如，如果您連結核取方塊 <!-- or the submission of the page--> 至 [訂閱清單](subscription-list.md) 在主要登陸頁面上，您可以使用「感謝您」子頁面上的訂閱清單。

假設您將主要頁面上的兩個核取方塊連結至兩個不同的訂閱清單。 如果使用者訂閱了其中一個，則您想要在提交表單時根據他們選取的核取方塊顯示特定訊息。

要实现此目的，请执行以下步骤：

1. 在首頁面上，連結 **[!UICONTROL 表單]** 元件至相關的訂閱清單。 [了解详情](#use-form-component)。

   ![](assets/lp_designer-form-luma-newsletter.png)

1. 在子頁面上，將滑鼠指標放在您要插入文字的位置，然後選取 **[!UICONTROL 新增個人化]** 從內容工具列。

   ![](assets/lp_designer-form-subpage-perso.png)

1. 在 **[!UICONTROL 編輯個人化]** 視窗，選取 **[!UICONTROL 內容屬性]** > **[!UICONTROL 登陸頁面]** > **[!UICONTROL 主要頁面內容]** > **[!UICONTROL 訂閱]**.

1. 主要頁面上選取的所有訂閱清單都會列出。 使用+圖示選取相關專案。

   ![](assets/lp_designer-form-add-subscription.png)

1. 使用運算式編輯器協助程式函式新增相關條件。 [了解详情](../personalization/functions/functions.md)

   ![](assets/lp_designer-form-add-subscription-condition.png)

   >[!CAUTION]
   >
   >如果運算式中有特殊字元（例如連字型大小），您必須將包含連字型大小的文字逸出。

1. 保存更改。

現在，當使用者選取其中一個核取方塊時，

![](assets/lp_designer-form-preview-checked-box.png)

提交表單時會顯示與所選核取方塊對應的訊息。

![](assets/lp_designer-form-thankyou-preview.png)

<!--![](assets/lp_designer-form-subscription-preview.png)-->

>[!NOTE]
>
>如果使用者選取兩個核取方塊，則兩個文字都會顯示。

<!--
## Use landing page additional data {#use-additional-data}

When [configuring the primary page](create-lp.md#configure-primary-page), you can create additional data to enable storing information when the landing page is being submitted.

>[!NOTE]
>
>This data may not be visible to users who visit the page.

If you defined one or more keys with their corresponding values when [configuring the primary page](create-lp.md#configure-primary-page), you can leverage these keys in the content of your primary page and subpages using the [Expression editor](../personalization/personalization-build-expressions.md).

///When you reuse the same text on a page, this enables you to dynamically change that text if needed, without going through each occurrence.

For example, if you define the company name as a key, you can quickly update it everywhere (on all the pages of a given landing page) by changing it only once in the [primary page settings](create-lp.md#configure-primary-page).///

To leverage these keys in a landing page, follow the steps below:

1. When configuring the primary page, define a key and its corresponding value in the **[!UICONTROL Additional data]** section. [Learn more](create-lp.md#configure-primary-page)

    ![](assets/lp_create-lp-additional-data.png)

1. When editing your primary page with the designer, place the pointer of your mouse where you want to insert your key and select **[!UICONTROL Add personalization]** from the contextual toolbar.

    ![](assets/lp_designer-context-add-perso.png)

1. In the **[!UICONTROL Edit Personalization]** window, select **[!UICONTROL Contextual attributes]** > **[!UICONTROL Landing Pages]** > **[!UICONTROL Additional Context]**.

    ![](assets/lp_designer-contextual-attributes.png)

1. All the keys that you created when configuring the primary page are listed. Select the key of your choice using the + icon.

    ![](assets/lp_designer-context-select-key.png)

1. Save your changes and repeat the steps above as many times as needed.

    ![](assets/lp_designer-context-keys-inserted.png)

    You can see that the personalization item corresponding to your key is now displayed everywhere you inserted it.
-->