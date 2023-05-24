---
solution: Journey Optimizer
product: journey optimizer
title: 创建内容模板
description: 瞭解如何建立範本以重複使用Journey Optimizer行銷活動和歷程中的內容
feature: Overview
topic: Content Management
role: User
level: Beginner
exl-id: 327de13a-1c99-4d5e-86cf-8180fb7aaf23
source-git-commit: cda4c1d88fedc75c7fded9971e45fdc9740346c4
workflow-type: tm+mt
source-wordcount: '985'
ht-degree: 12%

---

# 使用內容範本 {#content-templates}

為了加速並改善設計流程，您可以建立獨立的範本，以輕鬆地重複使用中的自訂內容 [!DNL Journey Optimizer] 行銷活動和歷程。

此功能可讓內容導向的使用者使用行銷活動或歷程以外的範本。 行銷使用者可在自己的歷程或行銷活動中重複使用並調整這些獨立內容範本。

例如，您公司內的使用者僅負責內容，因此無權存取行銷活動或歷程。 不過，這類使用者可建立電子郵件範本，組織的行銷人員可選取該範本以用於所有電子郵件作為起點。

➡️ [在本影片中瞭解如何建立和使用範本](#video-templates)

>[!CAUTION]
>
>若要建立、編輯和刪除內容範本，您必須擁有 **[!DNL Manage Library Items]** 許可權包含在 **[!DNL Content Library Manager]** 產品設定檔。 [了解详情](../administration/ootb-product-profiles.md#content-library-manager)

## 存取和管理範本 {#access-manage-templates}

若要存取內容範本清單，請選取 **[!UICONTROL 內容管理]** > **[!UICONTROL 內容範本]** 從左側功能表。

![](assets/content-template-list.png)

在目前沙箱上建立的所有範本 — 來自歷程或使用促銷活動 [另存為範本](#save-as-template) 選項，可以從 **[!UICONTROL 內容範本]** 功能表 — 顯示。

您可以依建立或修改日期來排序內容範本。 您也可以選擇只顯示您建立或修改的專案。

![](assets/content-template-list-filters.png)

若要編輯範本內容，請從清單中按一下所需的專案並選取 **[!UICONTROL 編輯內容]**.

![](assets/content-template-list-edit.png)

若要刪除範本，請選取所需範本旁的垃圾桶圖示。

![](assets/content-template-list-delete.png)

>[!NOTE]
>
>編輯或刪除範本時，使用此範本建立的行銷活動或歷程（包括電子郵件）不受影響。

## 创建内容模板 {#create-content-templates}

>[!CONTEXTUALHELP]
>id="ajo_create_template"
>title="定义您自己的内容模板"
>abstract="从头开始创建独立的自定义模板，这样您的内容便可在多个历程和营销活动中重复使用。"

建立內容範本的方式有兩種：

* 使用左側邊欄，從頭開始建立內容範本 **[!UICONTROL 內容範本]** 功能表。 [了解如何操作](#create-template-from-scratch)

* 在行銷活動或歷程中設計電子郵件時，請將電子郵件內容儲存為範本。 [了解如何操作](#save-as-template)

儲存後，您的內容範本即可用於行銷活動或歷程。 無論是從頭開始建立，還是從先前的電子郵件建立，您現在都可以在建立任何範本時使用此範本 [電子郵件](get-started-email-design.md) 範圍 [!DNL Journey Optimizer]. [了解如何操作](email-templates.md)

>[!NOTE]
>
>* 對內容範本所做的變更不會傳播至行銷活動或歷程，無論它們是即時或草稿。
>
>* 同樣地，當範本用於行銷活動或歷程時，您對行銷活動和歷程內容所做的任何編輯都不會影響先前使用的內容範本。


### 從頭開始建立範本 {#create-template-from-scratch}

若要從頭開始建立內容範本，請遵循下列步驟。

1. 透過存取內容範本清單 **[!UICONTROL 內容管理]** > **[!UICONTROL 內容範本]** 左側功能表。

   ![](assets/content-template-list.png)

1. 選取 **[!UICONTROL 建立範本]**.

1. 填寫範本詳細資訊。

   ![](assets/content-template-details.png)

   >[!NOTE]
   >
   >目前僅限 **電子郵件** 頻道和 **HTML** 型別受到支援。

1. 若要將自訂或核心資料使用標籤指派給範本，請選取 **[!UICONTROL 管理存取權]**. [進一步瞭解物件層級存取控制(OLAC)](../administration/object-based-access.md).

1. 按一下 **[!UICONTROL 建立]** 並從不同選項中選擇要如何設計電子郵件：

   * [從頭開始設計您的電子郵件](content-from-scratch.md) 透過電子郵件設計工具的介面。

   * [程式碼或複製貼上原始HTML](code-content.md) 直接放入電子郵件設計工具。

   * 从文件或 .zip 文件夹[导入现有 HTML 内容](existing-content.md)。

   * 使用內建或自訂範本清單中的現有內容。 有關在電子郵件中使用內容範本的步驟，請參閱 [本節](email-templates.md).

   ![](assets/content-template-design.png)

1. 此 [電子郵件設計工具](get-started-email-design.md) 顯示。 視需要編輯您的內容，就像根據您選取的選項對歷程或行銷活動中的任何電子郵件所做的那樣。

   您可以視需要測試內容。 [了解如何操作](#test-template)

1. 範本準備就緒後，請按一下 **[!UICONTROL 儲存]**.

1. 如有需要，請按一下範本名稱旁的箭頭，返回 **[!UICONTROL 詳細資料]** 畫面並編輯您的範本。

   ![](assets/content-template-designer-back.png)

現在，在內建置任何電子郵件時，即可使用此範本 [!DNL Journey Optimizer]. [了解如何操作](email-templates.md)

### 另存为模板 {#save-as-template}

>[!CONTEXTUALHELP]
>id="ajo_messages_depecrated_inventory"
>title="了解如何迁移您的消息"
>abstract="从 2022 年 7 月 25 日开始，消息菜单取消，现在直接在历程中创作消息。如果您重用历程中的旧消息，则需要将它们另存为模板。"

設計 [電子郵件](get-started-email-design.md) 在行銷活動或歷程中，您可以儲存電子郵件內容以供日後重複使用。 为此，请执行以下步骤。

1. 在電子郵件設計工具中，按一下畫面右上方的省略符號。

1. 選取 **[!UICONTROL 另存為內容範本]** 從下拉式功能表。

   ![](assets/email_designer-save-template.png)

1. 新增此範本的名稱和說明。

   ![](assets/email_designer-template-name.png)

1. 单击&#x200B;**[!UICONTROL 保存]**。

1. 範本會儲存至 **[!UICONTROL 內容範本]** 清單，可從以下位置存取： [!DNL Journey Optimizer] 專用功能表。 它會變成獨立的內容範本，可以像該清單上的任何其他專案一樣加以存取、編輯和刪除。 [了解详情](#access-manage-templates)

您現在可以在建立任何範本時使用此範本 [電子郵件](get-started-email-design.md) 範圍 [!DNL Journey Optimizer]. [了解如何操作](email-templates.md)

>[!NOTE]
>
>對該新範本所做的任何變更都不會傳播到該範本所來自的電子郵件。 同樣地，在該電子郵件中編輯原始內容時，不會修改新範本。

## 測試您的內容範本 {#test-template}

您可以測試任何電子郵件內容範本的轉譯，無論是從草稿還是從電子郵件建立。 若要這麼做，請遵循下列步驟。

>[!CAUTION]
>
>若要模擬內容，您必須具備 **[!DNL Manage Simulate Content]** 許可權包含在 **[!DNL Content Library Manager]** 產品設定檔。 [了解详情](../administration/ootb-product-profiles.md#content-library-manager)

1. 透過存取內容範本清單 **[!UICONTROL 內容管理]** > **[!UICONTROL 內容範本]** 功能表並選取任何範本。

1. 按一下 **[!UICONTROL 編輯內容]** 從 **[!UICONTROL 範本屬性]**.

1. 按一下 **[!UICONTROL 模擬內容]** 並選取測試設定檔以檢查電子郵件呈現。 可以选择桌面或移动视图。[了解详情](preview.md)

   ![](assets/content-template-stimulate.png)

1. 您可以傳送校樣以測試您的內容，並在將其用於歷程或行銷活動之前，先獲得一些內部使用者的核准。

   * 若要這麼做，請按一下 **[!UICONTROL 傳送證明]** 按鈕並依照中所述的步驟操作 [本節](preview.md#send-proofs).

   * 在傳送校樣之前，您必須選取 [電子郵件表面](../configuration/channel-surfaces.md) 將用於測試您的內容。

      ![](assets/content-template-stimulate-proof-surface.png)

## 操作方法视频 {#video-templates}

瞭解如何在中建立、編輯和使用內容範本 [!DNL Journey Optimizer].

>[!VIDEO](https://video.tv.adobe.com/v/3413743/?quality=12)
