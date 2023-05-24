---
solution: Journey Optimizer
product: journey optimizer
title: 關於歷程事件的ExperienceEvent結構描述
description: 瞭解歷程事件的ExperienceEvent結構描述
feature: Schemas
topic: Administration
role: Admin
level: Intermediate
keywords: 結構描述， XDM，平台，串流，擷取，歷程
exl-id: f19749c4-d683-4db6-bede-9360b9610eef
source-git-commit: f4068450dde5f85652096c09e7f817dbab40a3d8
workflow-type: tm+mt
source-wordcount: '840'
ht-degree: 3%

---

# 關於的ExperienceEvent結構描述 [!DNL Journey Optimizer] 事件 {#about-experienceevent-schemas}

[!DNL Journey Optimizer] 事件是指透過串流擷取傳送至Adobe Experience Platform的XDM體驗事件。

因此，設定事件的重要先決條件 [!DNL Journey Optimizer] 您是否熟悉Adobe Experience Platform的Experience Data Model （或XDM）、如何組成XDM Experience Event結構描述，以及如何將XDM格式的資料串流到Adobe Experience Platform。

## 的結構描述需求 [!DNL Journey Optimizer] 事件  {#schema-requirements}

設定事件的第一步 [!DNL Journey Optimizer] 是用來確保您定義了XDM結構描述來代表事件，並建立了一個資料集來記錄Adobe Experience Platform上的事件例項。 擁有事件的資料集並非絕對必要，但將事件傳送至特定資料集可讓您維護使用者的事件歷史記錄，以供日後參考及分析，因此總是對的。 如果您還沒有適合事件的結構描述和資料集，這兩項工作都可以在Adobe Experience Platform網頁介面中完成。

![](assets/schema1.png)

任何將用於以下專案的XDM結構描述 [!DNL Journey Optimizer] 事件應符合下列要求：

* 結構描述必須是XDM ExperienceEvent類別。

   ![](assets/schema2.png)

* 對於系統產生的事件，結構描述必須包括Orchestration eventID欄位群組。 [!DNL Journey Optimizer] 使用此欄位來識別歷程中使用的事件。

   ![](assets/schema3.png)

* 宣告識別事件中個別設定檔的身分欄位。 如果未指定身分，則可使用身分對應。 不建议采取此做法。

   ![](assets/schema4.png)

* 如果您希望此資料稍後可在歷程中查詢，請標籤設定檔的結構描述和資料集。

   ![](assets/schema5.png)

   ![](assets/schema6.png)

* 您可以隨意加入資料欄位，以擷取您要與事件一起加入的任何其他內容資料，例如關於使用者的資訊、產生事件的裝置、位置或與事件相關的任何其他有意義的情況。

   ![](assets/schema7.png)

   ![](assets/schema8.png)

## 利用架构关系{#leverage_schema_relationships}

Adobe Experience Platform 让您可以定义架构之间的关系，以便将一个数据集用作另一个数据集的查询表。

假設您的品牌資料模型有一個擷取購買資料的結構描述。 您也有產品目錄的結構描述。 您可以在購買結構描述中擷取產品ID，並使用關係從產品目錄中查詢更完整的產品詳細資訊。 舉例來說，這可讓您為所有購買筆記型電腦的客戶建立區段，而無須明確列出所有筆記型電腦ID，或擷取異動系統中的每個單一產品詳細資訊。

若要定義關係，來源結構描述中必須有專用欄位，在此案例中是購買結構描述中的產品ID欄位。 此欄位需要參考目的地結構描述中的產品ID欄位。 必須為設定檔啟用來源和目的地資料表，而且目的地結構描述必須將該通用欄位定義為其主要身分。

以下是已為設定檔啟用的產品目錄結構，產品ID已定義為主要身分。

![](assets/schema9.png)

以下是產品ID欄位中定義的購買結構描述。

![](assets/schema10.png)

>[!NOTE]
>
>進一步瞭解 [Experience Platform檔案](https://experienceleague.adobe.com/docs/platform-learn/tutorials/schemas/configure-relationships-between-schemas.html?lang=en).

在Journey Optimizer中，您可以善用連結表格中的所有欄位：

* 設定企業或單一事件時， [瞭解詳情](../event/experience-event-schema.md#unitary_event_configuration)
* 在歷程中使用條件時， [瞭解詳情](../event/experience-event-schema.md#journey_conditions_using_event_context)
* 在訊息個人化中， [瞭解詳情](../event/experience-event-schema.md#message_personalization)
* 在自訂動作個人化中， [瞭解詳情](../event/experience-event-schema.md#custom_action_personalization_with_journey_event_context)

### 数组{#relationships_limitations}

您可以在字串陣列上定義結構描述關係，例如，產品ID清單。

![](assets/schema15.png)

不過，您不可以物件陣列內的屬性定義結構描述關係，例如購買資訊清單（產品ID、產品名稱、價格、折扣）。 查閱值將無法在歷程中使用（條件、自訂動作等） 和訊息個人化。

![](assets/schema16.png)

### 事件配置{#unitary_event_configuration}

連結的結構描述欄位可用於單一和商業事件設定：

* 瀏覽事件設定畫面中的事件結構描述欄位時。
* 定義系統產生事件的條件時。

![](assets/schema11.png)

連結的欄位無法使用：

* 在事件索引鍵公式中
* 在事件id條件中（規則型事件）

若要瞭解如何設定單一事件，請參閱此 [頁面](../event/about-creating.md).

### 使用事件內容的歷程條件{#journey_conditions_using_event_context}

您可以使用查詢表格中的資料，連結至歷程中使用的事件，以進行條件建置（運算式編輯器）。

在歷程中新增條件、編輯運算式，並在運算式編輯器中展開事件節點。

![](assets/schema12.png)

若要瞭解如何定義歷程條件，請參閱此 [頁面](../building-journeys/condition-activity.md).

### 訊息個人化{#message_personalization}

個人化訊息時，可使用連結的欄位。 相關欄位會顯示在從歷程傳遞至訊息的內容中。

![](assets/schema14.png)

若要瞭解如何使用內容歷程資訊個人化訊息，請參閱此 [頁面](../personalization/personalization-use-case.md).

### 使用歷程事件內容進行自訂動作個人化{#custom_action_personalization_with_journey_event_context}

設定歷程自訂動作活動的動作引數時，可使用連結的欄位。

![](assets/schema13.png)

若要瞭解如何使用自訂動作，請參閱此 [頁面](../building-journeys/using-custom-actions.md).
