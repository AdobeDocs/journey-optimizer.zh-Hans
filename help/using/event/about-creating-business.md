---
solution: Journey Optimizer
product: journey optimizer
title: 配置业务事件
description: 瞭解如何建立業務活動
feature: Events
topic: Administration
role: Admin
level: Intermediate
keywords: 事件，歷程，企業，設定
exl-id: 39eb40e1-d7f5-4a8e-9b64-c620940d5ff2
source-git-commit: c0afa3e2bc6dbcb0f2f2357eebc04285de8c5773
workflow-type: tm+mt
source-wordcount: '1141'
ht-degree: 15%

---

# 配置业务事件 {#configure-a-business-event}

>[!CONTEXTUALHELP]
>id="ajo_journey_event_business"
>title="业务事件"
>abstract="事件配置让您可以定义 Journey Optimizer 将作为事件接收的信息。您可以使用多个事件（在历程的不同步骤中），而多个历程可以使用相同的事件。与单一事件不同，业务事件不链接到特定的配置文件。事件 ID 类型始终基于规则。"

与单一事件不同，业务事件不链接到特定的配置文件。事件 ID 类型始终基于规则。深入瞭解中的商業事件 [本節](../event/about-events.md).

以讀取區段為基礎的歷程可由排程器定期觸發，或由事件發生時的業務事件觸發。

業務事件可以是「產品重新上架」、「公司股價達到特定值」等。

>[!NOTE]
>
>您也可以觀看業務事件使用案例 [教學課程](https://experienceleague.adobe.com/docs/journey-optimizer-learn/tutorials/create-journeys/use-case-business-event.html). 請注意，不需要為設定檔啟用此結構描述。

## 重要说明 {#important-notes}

* 僅時間序列結構描述可用。 體驗事件、決定事件和歷程步驟事件結構描述無法使用。
* 事件結構描述必須包含非以人員為基礎的主要身分。 定義事件時，必須選取下列欄位： `_id` 和 `timestamp`
* 業務事件只能作為歷程的第一步捨棄。
* 將商業事件捨棄為歷程的第一步時，歷程的排程器型別將為「商業事件」。
* 業務事件後只能捨棄讀取區段活動。 它會自動新增為下一個步驟。
* 若要允許多個業務事件執行，請啟動 **[!UICONTROL 執行]** 歷程屬性的區段。
* 觸發業務事件後，匯出區段的時間會延遲，由15分鐘延遲至最多1小時。
* 測試業務事件時，您必須傳遞事件引數，以及將進入測試中歷程之測試設定檔的識別碼。 此外，在測試業務事件型歷程時，您只能觸發單一設定檔入口。 请参阅[此小节](../building-journeys/testing-the-journey.md#test-business)。在測試模式中，沒有可用的「程式碼檢視」模式。
* 如果新的業務事件到來，目前處於歷程中的個人會發生什麼事？ 其行為與當新週期發生時個人仍處於週期性歷程中的情況相同。 其路徑已結束。 因此，行銷人員如果預期業務事件頻繁，必須注意避免建立太長的歷程。
* 业务事件无法与单一事件或区段资格活动结合使用。

## 多個業務事件 {#multiple-business-events}

以下為連續收到多個業務事件時適用的重要注意事項。

**處理歷程時，在接收業務事件時的行為是什麼？**

業務事件會遵循與單一事件相同的重新進入規則。 如果歷程允許重新進入，將處理下一個業務事件。

**有哪些護欄可避免過度載入具體化區段？**

如果是拍攝中的業務事件，對於指定的歷程，第一個事件工作推送的資料會在1小時時段內重複使用。 對於已排程的歷程，沒有護欄。 深入瞭解中的區段 [Adobe Experience Platform Segmentation Service檔案](https://experienceleague.adobe.com/docs/experience-platform/segmentation/home.html).

## 開始使用商業活動 {#gs-business-events}

以下是設定業務事件的第一步：

1. 在「管理」選單區段中，選取 **[!UICONTROL 設定]**. 在  **[!UICONTROL 事件]** 區段，按一下 **[!UICONTROL 管理]**. 将显示事件列表。

   ![](assets/jo-event1.png)

1. 按一下 **[!UICONTROL 建立事件]** 以建立新事件。 事件配置窗格将在屏幕右侧打开。

   ![](assets/jo-event2.png)

1. 輸入事件的名稱。 您也可以新增說明。

   ![](assets/jo-event3-business.png)

   >[!NOTE]
   >
   >请勿使用空格或特殊字符。请勿使用超过 30 个字符。

1. 在 **[!UICONTROL 型別]** 欄位，選擇 **企業**.

   ![](assets/jo-event3bis-business.png)

1. 使用此事件的歷程次數會顯示在 **[!UICONTROL 使用位置]** 欄位。 您可以按一下 **[!UICONTROL 檢視歷程]** 圖示來顯示使用此事件的歷程清單。

1. 定義結構和裝載欄位：您可以在此處選取歷程預期會收到的事件資訊（或裝載）。 您稍後將在歷程中使用這些資訊。 请参阅[此小节](../event/about-creating-business.md#define-the-payload-fields)。

   ![](assets/jo-event5-business.png)

   僅時間序列結構描述可用。 `Experience Events`， `Decision Events` 和 `Journey Step Events` 結構描述無法使用。 事件結構描述必須包含非以人員為基礎的主要身分。 定義事件時，必須選取下列欄位： `_id` 和 `timestamp`

   ![](assets/test-profiles-4.png)

1. 按一下 **[!UICONTROL 事件ID條件]** 欄位。 使用簡單運算式編輯器定義條件，系統使用此條件來識別觸發歷程的事件。

   ![](assets/jo-event6-business.png)

   在我們的範例中，我們會根據產品ID來撰寫條件。 這表示每當系統收到符合此條件的事件時，都會將其傳遞至歷程。

   >[!NOTE]
   >
   >在簡單運算式編輯器中，並非所有運運算元都可用，它們取決於資料型別。 例如，對於欄位的字串型別，您可以使用「包含」或「等於」。

1. 单击&#x200B;**[!UICONTROL 保存]**。

   ![](assets/journey7-business.png)

   事件现已配置完毕，可随时投入旅程。还需要其他配置步骤以接收事件。请参阅[此页面](../event/additional-steps-to-send-events-to-journey.md)以了解详情。

## 定義裝載欄位 {#define-the-payload-fields}

裝載定義可讓您選擇系統預期從歷程中的事件接收的資訊，以及識別與事件相關聯之人員的金鑰。 有效負載以Experience CloudXDM欄位定義為基礎。 如需XDM的詳細資訊，請參閱 [Adobe Experience Platform檔案](https://experienceleague.adobe.com/docs/experience-platform/xdm/home.html?lang=zh-Hans){target="_blank"}.

1. 從清單中選取XDM結構描述，然後按一下 **[!UICONTROL 欄位]** 欄位或位於 **[!UICONTROL 編輯]** 圖示。

   ![](assets/journey8-business.png)

   將顯示結構描述中定義的所有欄位。 欄位清單會因結構描述而異。 您可以搜尋特定欄位，或使用篩選器來顯示所有節點和欄位，或僅顯示選定的欄位。 根據結構描述定義，某些欄位可能是必填欄位並預先選定。 您無法取消選取它們。 依預設，系統會選取歷程正確接收事件所必要的所有欄位。

   ![](assets/journey9-business.png)

   >[!NOTE]
   >
   > 請確定已選取下列欄位： `_id` 和 `timestamp`

1. 選取您預期會從事件接收的欄位。 這些是業務使用者將在歷程中善用的欄位。

1. 選取完所需欄位後，按一下 **[!UICONTROL 儲存]** 或按 **[!UICONTROL 輸入]**.

   所選欄位的數量會顯示在 **[!UICONTROL 欄位]**.

   ![](assets/journey12-business.png)

## 預覽裝載 {#preview-the-payload}

使用裝載預覽來驗證裝載定義。

1. 按一下 **[!UICONTROL 檢視裝載]** 圖示以預覽系統預期的裝載。

   ![](assets/journey13-business.png)

   您可以注意到已選取的欄位已顯示。

   ![](assets/journey14-business.png)

1. 檢查預覽以驗證裝載定義。

1. 然後，您可以將裝載預覽與共用給負責事件傳送的人員。 此裝載可協助他們設計事件推送至的設定 [!DNL Journey Optimizer]. 请参阅[此页](../event/additional-steps-to-send-events-to-journey.md)。
