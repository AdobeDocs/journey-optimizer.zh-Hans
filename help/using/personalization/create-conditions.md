---
solution: Journey Optimizer
product: journey optimizer
title: 创建条件
description: 瞭解如何建立條件
feature: Personalization
topic: Personalization
role: Data Engineer
level: Intermediate
keywords: 運算式，編輯器，條件，規則
exl-id: 246a4a55-059e-462c-ac1e-43b90f4abda4
source-git-commit: 9657862f1c6bdb2399fcf3e6384bb9dec5b8f32b
workflow-type: tm+mt
source-wordcount: '595'
ht-degree: 8%

---

# 使用條件式規則 {#conditions}

條件規則是一組規則，用來定義應在訊息中顯示哪些內容，需視各種條件而定，例如設定檔屬性、區段成員資格或內容相關事件。

條件式規則是使用運算式編輯器建立的，如果您想要在整個內容中重複使用它們，可以儲存這些規則。 [瞭解如何將條件規則儲存至程式庫](#save)

>[!NOTE]
>
>個人需要 [管理程式庫專案](../administration/ootb-product-profiles.md) 儲存或刪除條件規則的許可權。 已儲存的條件可供組織內的所有使用者使用。

## 存取條件式規則產生器 {#access}

條件式規則是從以下專案建立： **[!UICONTROL 條件]** 運算式編輯器中的功能表，您可透過以下任一方式存取：

* 從電子郵件設計工具，為電子郵件內文中的元件啟用動態內容時。 [瞭解如何將動態內容新增至電子郵件](dynamic-content.md#emails)

   ![](assets/conditions-access-email.png)

* 在任何您可以使用來新增個人化的欄位中 [運算式編輯器](personalization-build-expressions.md).

   ![](assets/conditions-access-editor.png)

## 建立條件規則 {#create-condition}

>[!CONTEXTUALHELP]
>id="ajo_expression_editor_conditions_create"
>title="创建条件"
>abstract="结合配置文件属性、上下文事件或受众来构建规则，以定义应在消息中显示哪些内容。"

>[!CONTEXTUALHELP]
>id="ajo_expression_editor_conditions"
>title="创建条件"
>abstract="结合配置文件属性、上下文事件或受众来构建规则，以定义应在消息中显示哪些内容。"

建立條件式規則的步驟如下：

1. 存取 **[!UICONTROL 條件]** 運算式編輯器或電子郵件設計工具中的功能表，然後按一下 **[!UICONTROL 新建]**.

1. 根據您的需求建置條件式規則。 若要這麼做，請從左側選單拖放並排列所需的屬性至畫布中。

   將屬性結合至畫布的步驟與區段建置體驗類似。 有關如何使用規則產生器畫布的詳細資訊，請參閱 [本檔案](https://experienceleague.adobe.com/docs/experience-platform/segmentation/ui/segment-builder.html?lang=en#rule-builder-canvas).

   ![](assets/conditions-create.png)

   屬性會組織成三個標籤：

   * **[!UICONTROL 配置文件]**:
      * **[!UICONTROL 區段會籍]** 列出所有區段屬性（即狀態、版本等） 的 [Adobe Experience Platform Segmentation service](https://experienceleague.adobe.com/docs/experience-platform/segmentation/home.html)，
      * **[!UICONTROL XDM個別設定檔]** 列出所有與相關的設定檔屬性 [體驗資料模型(XDM)結構描述](https://experienceleague.adobe.com/docs/experience-platform/xdm/home.html?lang=zh-Hans) 在Adobe Experience Platform中定義。
   * **[!UICONTROL 情境]**：當您的訊息用於歷程時，內容歷程欄位可透過此索引標籤使用。
   * **[!UICONTROL 受眾]**：列出從建立的區段產生的所有對象 [Adobe Experience Platform Segmentation service](https://experienceleague.adobe.com/docs/experience-platform/segmentation/home.html).

1. 條件式規則準備就緒後，您就可以將其新增至訊息，以建立動態內容。 [瞭解如何新增動態內容](dynamic-content.md)

   您也可以儲存規則以允許進一步重複使用。 [瞭解如何儲存條件](#save)

## 儲存條件規則 {#save}

如果經常會重複使用某些條件規則，您可以將其儲存至條件程式庫。 所有已儲存的規則會共用，並可由組織內的個人存取及使用。

>[!NOTE]
>
>使用歷程內容屬性的條件式規則無法儲存至程式庫。

1. 在條件版本畫面中，按一下 **[!UICONTROL 儲存條件]** 按鈕。

1. 為規則提供名稱和說明（選用），然後按一下 **[!UICONTROL 新增]**.

   ![](assets/conditions-name-description.png)

1. 條件式規則會儲存至程式庫。 您現在可以使用它在訊息中建立動態內容。 [瞭解如何新增動態內容](dynamic-content.md)

## 編輯和刪除儲存的條件規則 {#edit-delete}

您可以隨時使用省略符號按鈕刪除條件規則。

![](assets/conditions-open.png)

無法修改儲存至程式庫的條件式規則。 不過，您仍然可以使用它們來建立新規則。 若要這麼做，請開啟條件規則，進行所需的變更，然後儲存至程式庫。 [瞭解如何將條件儲存至資料庫](#save)
