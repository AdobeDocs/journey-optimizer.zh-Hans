---
solution: Journey Optimizer
product: journey optimizer
title: 在Journey Optimizer中從頭開始設計內容
description: 瞭解如何從頭開始設計您的內容
feature: Overview
topic: Content Management
role: User
level: Intermediate
keywords: 內容，編輯器，電子郵件，開始
exl-id: 151594f2-85e4-4c79-9c15-334fbd3768c4
source-git-commit: 803c9f9f05669fad0a9fdeeceef58652b6dccf70
workflow-type: tm+mt
source-wordcount: '654'
ht-degree: 57%

---

# 从头开始设计内容 {#content-from-scratch}

>[!CONTEXTUALHELP]
>id="ac_structure_components_email"
>title="添加结构组件"
>abstract="结构组件定义电子邮件的版面。拖放&#x200B;**结构**&#x200B;组件到画布中，开始设计您的电子邮件内容。"

>[!CONTEXTUALHELP]
>id="ac_structure_components_landing_page"
>title="添加结构组件"
>abstract="结构组件定义登陆页面的版面。拖放&#x200B;**结构**&#x200B;组件到画布中，开始设计您的登陆页面内容。"

>[!CONTEXTUALHELP]
>id="ac_structure_components_fragment"
>title="添加结构组件"
>abstract="结构组件定义片段的版面。拖放&#x200B;**结构**&#x200B;组件到画布中，开始设计您的片段内容。"

>[!CONTEXTUALHELP]
>id="ac_structure_components_template"
>title="添加结构组件"
>abstract="结构组件定义模板的版面。拖放&#x200B;**结构**&#x200B;组件到画布中，开始设计您的模板内容。"


>[!CONTEXTUALHELP]
>id="ac_edition_columns_email"
>title="定义电子邮件列"
>abstract="使用电子邮件设计器，您可以通过选择列结构来轻松定义电子邮件的版面。"

>[!CONTEXTUALHELP]
>id="ac_edition_columns_landing_page"
>title="定义登陆页面列"
>abstract="使用电子邮件设计器，您可以通过选择列结构来轻松定义登陆页面的版面。"

>[!CONTEXTUALHELP]
>id="ac_edition_columns_fragment"
>title="定义片段列"
>abstract="使用电子邮件设计器，您可以通过选择列结构来轻松定义片段的版面。"

>[!CONTEXTUALHELP]
>id="ac_edition_columns_template"
>title="定义模板列"
>abstract="使用电子邮件设计器，您可以通过选择列结构来轻松定义模板的版面。"


使用Adobe Journey Optimizer Designer輕鬆定義內容的結構。 透過簡單的拖放動作來新增和移動結構元素，您可以在數秒內設計內容的形狀。

若要開始建立您的內容，請遵循下列步驟：

1. 從Designer首頁選取 **[!UICONTROL 從頭開始設計]** 選項。

   ![](assets/email_designer.png)

1. 透過拖放方式開始設計您的內容 **[!UICONTROL 結構]** 放入畫布以定義電子郵件的版面。

   >[!NOTE]
   >
   >堆叠列并非与所有电子邮件程序都兼容。當不支援時，欄將不會棧疊。

   <!--Once placed in the email, you cannot move nor remove your components unless there is already a content component or a fragment placed inside. This is not true in AJO - TBC?-->

1. 新增任意數量 **[!UICONTROL 結構]** 視需要並在右側的專用窗格中編輯其設定。

   ![](assets/email_designer_structure_components.png)

   选择 **[!UICONTROL n:n 列]**&#x200B;组件来定义所选列数（3 和 10 之间）。还可以通过移动每个列底部的箭头来定义该列的宽度。

   >[!NOTE]
   >
   >每个列的大小不能小于结构组件的总宽度的 10%。不能删除非空列。

1. 展開 **[!UICONTROL 內容]** 區段，並視需要將任意數量的元素新增至一或多個結構元件中。 [详细了解内容组件](content-components.md)

1. 每個元件都可進一步透過以下方式自訂： **[!UICONTROL 設定]** 或 **[!UICONTROL 樣式]** 索引標籤在右側功能表中。 例如，您可以更改每个组件的文本样式、内边距或边距。[了解有关对齐方式和内边距的更多信息](alignment-and-padding.md)

   ![](assets/email_designer_structure_component.png)

1. 從 **[!UICONTROL 資產選取器]**，您可以直接選取儲存在 **[!UICONTROL 資產庫]**. [進一步瞭解資產管理](assets-essentials.md)

   連按兩下包含資產的資料夾。 將其拖放至結構元件中。

   ![](assets/email_designer_asset_picker.png)

1. 插入個人化欄位，以從設定檔屬性、區段會籍、內容屬性等自訂內容。 [详细了解内容个性化](../personalization/personalize.md)

   ![](assets/email_designer_personalization.png)

1. 按一下 **[!UICONTROL 啟用條件內容]** 以新增動態內容，並根據條件規則將內容調整至目標設定檔。 [动态内容入门](../personalization/get-started-dynamic-content.md)

   ![](assets/email_designer_dynamic-content.png)

1. 按一下 **[!UICONTROL 連結]** 標籤，以顯示您要追蹤之內容的所有URL。 您可以修改其 **[!UICONTROL 追蹤型別]** 或 **[!UICONTROL 標籤]** 並新增 **[!UICONTROL 標籤]** 視需要而定。 [進一步瞭解連結和追蹤](message-tracking.md)

   ![](assets/email_designer_links.png)

1. 如果需要，可以通过单击高级菜单中的&#x200B;**[!UICONTROL 切换到代码编辑器]**&#x200B;来进一步个性化电子邮件。例如，这允许您编辑电子邮件源代码以添加跟踪或自定义 HTML 标记。[详细了解代码编辑器](code-content.md)

   >[!CAUTION]
   >
   >切换到代码编辑器后，无法恢复到此电子邮件的可视设计器。

1. 內容準備就緒後，請按一下 **[!UICONTROL 模擬內容]** 按鈕以檢查演算。 可以选择桌面或移动视图。[详细了解预览电子邮件](preview.md)

   ![](assets/email_designer_simulate_content.png)

1. 當您的內容準備就緒時，請按一下 **[!UICONTROL 儲存]**.

