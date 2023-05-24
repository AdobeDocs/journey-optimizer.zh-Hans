---
solution: Journey Optimizer
product: journey optimizer
title: 使用电子邮件设计器内容组件
description: 了解如何在电子邮件中使用内容组件
feature: Overview
topic: Content Management
role: User
level: Intermediate
keywords: 元件，電子郵件設計工具，編輯器，電子郵件
exl-id: a4aaa814-3fd4-439e-8f34-faf97208378a
source-git-commit: cda4c1d88fedc75c7fded9971e45fdc9740346c4
workflow-type: tm+mt
source-wordcount: '1353'
ht-degree: 54%

---

# 使用電子郵件設計工具內容元件 {#content-components}

>[!CONTEXTUALHELP]
>id="ac_content_components_email"
>title="关于内容组件"
>abstract="内容组件是空的内容占位符，您可用它来创建电子邮件的版面。"

>[!CONTEXTUALHELP]
>id="ac_content_components_landing_page"
>title="关于内容组件"
>abstract="内容组件是空的内容占位符，您可用它来创建登陆页面的版面。"

>[!CONTEXTUALHELP]
>id="ac_content_components_fragment"
>title="关于内容组件"
>abstract="内容组件是空的内容占位符，您可用它来创建片段的版面。"

>[!CONTEXTUALHELP]
>id="ac_content_components_template"
>title="关于内容组件"
>abstract="内容组件是空的内容占位符，您可用它来创建模板的版面。"

建立電子郵件內容時， **[!UICONTROL 內容元件]** 可讓您使用原始元件來進一步個人化電子郵件，這些元件一旦放入電子郵件中即可編輯。

您可以視需要在定義電子郵件版面的一或多個結構元件內新增任意數量的內容元件。

## 添加内容组件 {#add-content-components}

要将内容组件添加到您的电子邮件中，并根据您的需要调整这些内容组件，请执行以下步骤。

1. 在电子邮件设计器中，使用现有内容或将&#x200B;**[!UICONTROL 结构组件]**&#x200B;拖放到空白内容中以定义电子邮件版面。[了解如何操作](content-from-scratch.md)

1. 要访问&#x200B;**[!UICONTROL 内容组件]**&#x200B;部分，请从电子邮件设计器左窗格中选择相应的按钮。

   ![](assets/email_designer_content_components.png)

1. 将所选内容组件拖放到相关的结构组件中。

   ![](assets/email_designer_add_content_components.png)

   >[!NOTE]
   >
   >您可以将多个组件添加到单个结构组件中，也可以将它们添加到结构组件的每个列中。

1. 使用調整每個元件的樣式屬性 **[!UICONTROL 設定]** 和 **[!UICONTROL 樣式]** 索引標籤在右側。 例如，您可以更改每个组件的文本样式、内边距或边距。[了解有关对齐方式和内边距的更多信息](alignment-and-padding.md)

   ![](assets/email_designer_content_components_settings.png)

1. 從的進階功能表 **[!UICONTROL 內容元件]**，您可以視需要輕鬆刪除或複製任何內容元件。

   ![](assets/email_designer_content_components_settings_2.png)

## 容器 {#container}

若要將特定樣式套用至一組內容元件，您可以新增 **[!UICONTROL 容器]** 元件，然後在其中新增所需的內容元件。 這可讓您將不同的樣式套用至容器，這會與套用至內部內容元件的樣式不同。

例如，添加一个&#x200B;**[!UICONTROL 容器]**&#x200B;组件，然后在该容器中添加一个[按钮](#button)组件。可以为该容器使用一个特定背景，并为按钮使用另一个背景。

![](assets/email_designer_container_component.png)

## 按钮 {#button}

使用&#x200B;**[!UICONTROL 按钮]**&#x200B;组件可将一个或多个按钮插入电子邮件中，并将电子邮件受众重定向到另一个页面。

1. 从&#x200B;**[!UICONTROL 内容组件]**&#x200B;中，将&#x200B;**[!UICONTROL 按钮]**&#x200B;组件拖放到&#x200B;**[!UICONTROL 结构组件]**&#x200B;中。

1. 按一下您新新增的按鈕，個人化文字並存取 **[!UICONTROL 設定]** 和 **[!UICONTROL 樣式]** 索引標籤在電子郵件設計工具右窗格中。

   ![](assets/email_designer_button_component.png)

1. 從 **[!UICONTROL 連結]** 功能表，新增您要在按一下按鈕時重新導向的URL。

1. 選擇將使用「 」將您的對象重新導向的方式 **[!UICONTROL Target]** 下拉式清單：

   * **[!UICONTROL 无]**：单击时在同一框架中打开链接（默认）。
   * **[!UICONTROL 空白]**：在新窗口或标签页中打开链接。
   * **[!UICONTROL 自身]**：单击时在同一框架中打开链接。
   * **[!UICONTROL 父]**：在父框架中打开链接。
   * **[!UICONTROL 顶部]**：在窗口的整个正文中打开链接。

   ![](assets/email_designer_button_link.png)

1. 您可以通过从以下位置更改样式属性（例如&#x200B;**[!UICONTROL 边框]**、**[!UICONTROL 大小]**、**[!UICONTROL 边距]**&#x200B;等）来进一步个性化您的按钮：**[!UICONTROL 组件设置]**&#x200B;窗格。

## 文本 {#text}

使用&#x200B;**[!UICONTROL 文本]**&#x200B;组件将文本插入电子邮件中，并使用 **[!UICONTROL 樣式]** 標籤。

![](assets/email_designer_text_component.png)

1. 從 **[!UICONTROL 內容元件]**，拖放 **[!UICONTROL 文字]** 元件移入 **[!UICONTROL 結構元件]**.

1. 按一下您新新增的元件，以個人化文字並存取 **[!UICONTROL 設定]** 和 **[!UICONTROL 樣式]** 索引標籤位於電子郵件設計工具的右窗格中。

1. 使用工具栏中的以下可用选项更改文本：

   ![](assets/email_designer_27.png)

   * **[!UICONTROL 更改文本样式]**：对文本应用粗体、斜体、下划线或删除线。
   * **更改对齐方式**：为文本选择左对齐、右对齐、居中对齐或两端对齐。
   * **[!UICONTROL 创建列表]**：将项目符号或编号列表添加到文本中。
   * **[!UICONTROL 设置标题]**：向文本添加最多六个标题级别。
   * **字体大小**：选择文本的字体大小（以像素为单位）。
   * **[!UICONTROL 變更字型顏色]**：選擇字型的顏色。
   * **[!UICONTROL 插入連結]**：新增任何型別的連結至您的內容。
   * **[!UICONTROL 编辑图像]**：将图像或资产添加到文本组件。[進一步瞭解資產管理](assets-essentials.md)
   * **[!UICONTROL 變更字型顏色]**：選擇字型的顏色。
   * **[!UICONTROL 添加个性化]**：添加个性化字段以自定义配置文件数据中的内容。[详细了解内容个性化](../personalization/personalize.md)
   * **[!UICONTROL 显示源代码]**：显示文本的源代码。不能修改。
   * **[!UICONTROL 启用条件内容]**：添加条件内容以使组件内容适应目标配置文件。[進一步瞭解動態內容](../personalization/get-started-dynamic-content.md)
   * **[!UICONTROL 复制]**：添加文本组件的副本。
   * **[!UICONTROL 删除]**：从电子邮件中删除选定的文本组件。

1. 从以下位置调整其他样式属性，例如文本颜色、字体系列、边框、内边距、边距等：從 **[!UICONTROL 樣式]** 標籤。

   ![](assets/email_designer_text_component_2.png)

## 分隔条 {#divider}

使用&#x200B;**[!UICONTROL 分隔条]**&#x200B;组件可插入分隔线来整理电子邮件的版面和内容。

您可以從以下位置調整樣式屬性，例如線條的顏色、樣式和高度： **[!UICONTROL 設定]** 和 **[!UICONTROL 樣式]** 索引標籤。

![](assets/email_designer_divider.png)

## HTML {#HTML}

使用 **[!UICONTROL HTML]** 组件可复制并粘贴现有 HTML 的不同部分。这使您能够创建免费的模块化 HTML 组件以重用某些外部内容。

1. 从&#x200B;**[!UICONTROL 内容组件]**&#x200B;中，将 **[!UICONTROL HTML]** 组件拖放到&#x200B;**[!UICONTROL 结构组件]**&#x200B;中。

1. 单击新添加的组件，然后从上下文工具栏中选择&#x200B;**[!UICONTROL 显示源代码]**&#x200B;以添加 HTML。

   ![](assets/email_designer_html_component.png)

1. 複製並貼上您要新增至電子郵件的HTML代碼，然後按一下 **[!UICONTROL 儲存]**.

   ![](assets/email_designer_html_content.png)

>[!NOTE]
>
>要简单地使外部内容与电子邮件设计器兼容，Adobe 建议从头开始创建邮件并将现有电子邮件中的内容复制到组件中。

## 图像 {#image}

使用 **[!UICONTROL 影像]** 將影像檔案從電腦插入電子郵件內容的元件。

1. 從 **[!UICONTROL 內容元件]**，拖放 **[!UICONTROL 影像]** 元件移入 **[!UICONTROL 結構元件]**.

   ![](assets/email_designer_image_content.png)

1. 单击&#x200B;**[!UICONTROL 浏览]**&#x200B;可从您的资产中选择图像文件。

   若要深入瞭解 [!DNL Assets Essentials]，請參閱 [Adobe Experience Manager Assets Essentials檔案](https://experienceleague.adobe.com/docs/experience-manager-assets-essentials/help/introduction.html){target="_blank"}.

1. 按一下新新增的元件，然後從「 」設定影像屬性 **[!UICONTROL 設定]** 標籤：

   * 使用&#x200B;**[!UICONTROL 图像标题]**&#x200B;可以定义图像的标题。
   * 使用&#x200B;**[!UICONTROL 替代文字]**&#x200B;可以定义链接到图像的题注。这对应于 alt HTML 属性。

   ![](assets/email_designer_10.png)

1. 您也可以選擇 **[!UICONTROL 尋找類似的Stock像片]**. [了解详情](stock.md)

1. 從 **[!UICONTROL 樣式]** 標籤，調整其他樣式屬性，例如邊界、邊框等。 或者从&#x200B;**[!UICONTROL 组件设置]**&#x200B;窗格中添加链接，以将受众重定向到其他内容。

## 社交 {#social}

使用&#x200B;**[!UICONTROL 社交]**&#x200B;组件可将指向社交媒体页面的链接插入到电子邮件内容中。

1. 从&#x200B;**[!UICONTROL 内容组件]**&#x200B;中，将&#x200B;**[!UICONTROL 社交]**&#x200B;组件拖放到&#x200B;**[!UICONTROL 结构组件]**&#x200B;中。

1. 選取您新新增的元件。

1. 在 **[!UICONTROL 社交]** 的欄位 **[!UICONTROL 設定]** 標籤中，選擇要新增或移除的社群媒體。

   ![](assets/email_designer_20.png)

1. 透過專用欄位選擇圖示的大小。

1. 按一下您的每個社群媒體圖示以設定 **[!UICONTROL URL]** 您的對象將重新導向的目標位置。

   ![](assets/email_designer_21.png)

1. 如有需要，您也可以從「資產」變更每個社群媒體的圖示。

1. 从以下位置调整其他样式属性（例如样式、边距、边框等）：從 **[!UICONTROL 樣式]** 標籤。

## 優惠決定 {#offer-decision}

使用 **[!UICONTROL 優惠決定]** 元件以將選件插入訊息。 此 [決策管理](../offers/get-started/starting-offer-decisioning.md) engine會挑選最適合提供給客戶的優惠方案。

1. 從 **[!UICONTROL 內容元件]**，拖放 **[!UICONTROL 優惠決定]** 元件移入 **[!UICONTROL 結構元件]**.

1. 按一下 **[!UICONTROL 新增]** 以選取 **[!UICONTROL 優惠決定]**.

   ![](assets/component_offers.png)

1. 從下拉式清單中，選取 **[!UICONTROL 版位]**.  然後，選取 **[!UICONTROL 優惠決定]** 您想要新增至內容並按一下 **[!UICONTROL 新增]**.

   ![](assets/component_offers_2.png)

1. 從 **[!UICONTROL 優惠決定]** 索引標籤上，您可以預覽或變更插入的選件。

瞭解如何在中將個人化優惠方案新增至電子郵件 [本節](add-offers-email.md).

>[!IMPORTANT]
>
>如果對歷程訊息中使用的優惠決定進行變更，您需要取消發佈歷程並重新發佈。  這將確保將變更納入歷程的訊息中，且訊息與最新更新一致。
