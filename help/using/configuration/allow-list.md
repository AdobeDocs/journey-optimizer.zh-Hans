---
solution: Journey Optimizer
product: journey optimizer
title: 允许列表
description: 瞭解如何使用允許清單
feature: Deliverability
topic: Content Management
role: User
level: Intermediate
keywords: 允許清單，清單，安全，設定
exl-id: 70ab8f57-c132-4de1-847b-11f0ab14f422
source-git-commit: 9657862f1c6bdb2399fcf3e6384bb9dec5b8f32b
workflow-type: tm+mt
source-wordcount: '1129'
ht-degree: 14%

---

# 允许列表 {#allow-list}

您可在以下位置定義特定的傳送安全清單： [沙箱](../administration/sandboxes.md) 層級。

此允許清單可讓您指定個別電子郵件地址或網域，這些地址或網域將是唯一獲授權接收您從特定沙箱傳送之電子郵件的收件者或網域。

>[!NOTE]
>
>此功能適用於生產及非生產沙箱。

例如，在可能發生錯誤的非生產執行個體上，允許清單可確保您將不需要的訊息傳送至真實客戶地址的風險降至最低，因此會提供用於測試用途的安全環境。

此外，當允許清單為作用中但空白時，不會傳出任何郵件。 因此，如果您遇到一些重大問題，可以使用此功能來停止所有來自的傳出通訊 [!DNL Journey Optimizer] 直到您修正問題為止。 進一步瞭解 [允許清單邏輯](#logic).

>[!CAUTION]
>
>此功能僅適用於電子郵件頻道。

## 存取允許清單 {#access-allowed-list}

若要存取允許的電子郵件地址和網域的詳細清單，請前往 **[!UICONTROL 管理]** > **[!UICONTROL 頻道]** > **[!UICONTROL 電子郵件設定]**，並選取 **[!UICONTROL 允許清單]**.

![](assets/allow-list-access.png)

>[!CAUTION]
>
>檢視、匯出和管理允許清單的許可權僅限於 [歷程管理員](../administration/ootb-product-profiles.md#journey-administrator). 進一步瞭解管理 [!DNL Journey Optimizer] 使用者在中的存取許可權 [本節](../administration/permissions-overview.md).

若要將允許清單匯出為CSV檔案，請選取 **[!UICONTROL 下載CSV]** 按鈕。

使用 **[!UICONTROL 刪除]** 按鈕以永久移除專案。

您可以搜尋電子郵件地址或網域，並篩選 **[!UICONTROL 地址型別]**. 選取後，您可以清除顯示在清單頂端的篩選器。

![](assets/allowed-list-filtering-example.png)

## 啟用允許清單 {#enable-allow-list}

若要啟用允許清單，請遵循下列步驟。

1. 存取  **[!UICONTROL 頻道]** > **[!UICONTROL 電子郵件設定]** > **[!UICONTROL 允許清單]** 功能表。

1. 選取切換按鈕。

   ![](assets/allow-list-edit.png)

1. 選取 **[!UICONTROL 啟用允許清單]**. 允許清單現在已啟用。

   ![](assets/allow-list-enable.png)

   >[!NOTE]
   >
   >啟用允許清單後，有5分鐘的延遲時間，它就會在您的歷程和行銷活動中生效。

當功能作用中時，允許清單邏輯適用。 有关详细信息，请参阅[此部分](#logic)。

>[!NOTE]
>
>啟用時，允許清單功能在執行歷程時執行，但也在使用測試訊息時執行 [校樣](../email/preview.md#send-proofs) 和測試歷程，使用 [測試模式](../building-journeys/testing-the-journey.md).

## 停用允許清單 {#deactivate-allow-list}

若要停用允許清單，請遵循下列步驟。

1. 存取  **[!UICONTROL 頻道]** > **[!UICONTROL 電子郵件設定]** > **[!UICONTROL 允許清單]** 功能表。

1. 選取切換按鈕。

   ![](assets/allow-list-edit-active.png)

1. 選取 **[!UICONTROL 停用允許清單]**. 允許清單不再有效。

   ![](assets/allow-list-deactivate.png)

   >[!NOTE]
   >
   >停用允許清單後，有5分鐘的延遲時間，它就會在您的歷程和行銷活動中生效。

停用功能時，允許清單邏輯不適用。 有关详细信息，请参阅[此部分](#logic)。

## 將實體新增至允許清單 {#add-entities}

若要將新的電子郵件地址或網域新增到特定沙箱的允許清單，您可以 [手動填入清單](#manually-populate-list)，或使用 [API呼叫](#api-call-allowed-list).

>[!NOTE]
>
>允許清單最多可包含1,000個專案。

### 手動填入允許清單 {#manually-populate-list}

>[!CONTEXTUALHELP]
>id="ajo_admin_allowed_list_add_header"
>title="将地址或域添加到允许列表"
>abstract="您可以通过逐个选择新电子邮件地址或域，将它们手动添加到允许列表中。"

>[!CONTEXTUALHELP]
>id="ajo_admin_allowed_list_add"
>title="将地址或域添加到允许列表"
>abstract="您可以通过逐个选择新电子邮件地址或域，将它们手动添加到允许列表中。"

您可以手動填入 [!DNL Journey Optimizer] 透過使用者介面新增電子郵件地址或網域來允許清單。

>[!NOTE]
>
>您一次只能新增一個電子郵件地址或網域。

为此，请执行以下步骤。

1. 選取 **[!UICONTROL 新增電子郵件或網域]** 按鈕。

   ![](assets/allowed-list-add-email.png)

1. 选择地址类型：**[!UICONTROL 电子邮件地址]**&#x200B;或&#x200B;**[!UICONTROL 域地址]**。

1. 輸入您要傳送電子郵件的電子郵件地址或網域。

   >[!NOTE]
   >
   >确保输入有效的电子邮件地址（例如 abc@company.com）或域（例如 abc.company.com）。

1. 如果需要，请指定原因。

   ![](assets/allowed-list-add-email-address.png)

   >[!NOTE]
   >
   >包含在32到126之間的所有ASCII字元都允許在 **[!UICONTROL 原因]** 欄位。 可在[此页面](https://en.wikipedia.org/wiki/Wikipedia:ASCII#ASCII_printable_characters){target="_blank"}上找到完整列表以供参考。

1. 单击&#x200B;**[!UICONTROL 提交]**。

### 使用API呼叫新增實體 {#api-call-allowed-list}

若要填入允許清單，您也可以使用呼叫隱藏API `ALLOWED` 的值 `listType` 屬性。 例如：

![](assets/allow-list-api.png)

您可以執行 **新增**， **刪除** 和 **取得** 作業。

進一步瞭解在中進行API呼叫 [ADOBE EXPERIENCE PLATFORM API](https://experienceleague.adobe.com/docs/experience-platform/landing/platform-apis/api-guide.html){target="_blank"} 參考檔案。

## 下載允許清單 {#download-allowed-list}

若要將允許清單匯出為CSV檔案，請執行以下步驟：

1. 選取 **[!UICONTROL 下載CSV]** 按鈕。

   ![](assets/allowed-list-download-csv.png)

1. 等候檔案產生。

   ![](assets/allowed-list-download-generate.png)

   >[!NOTE]
   >
   >下載時間取決於檔案大小，亦即允許清單中的位址數量。
   >
   >對於指定的沙箱，一次可以處理一個下載請求。

1. 檔案產生後，您會收到通知。 按一下畫面右上方的鈴鐺圖示即可顯示。

1. 按一下通知本身以下載檔案。

   ![](assets/allowed-list-download-notification.png)

   >[!NOTE]
   >
   >連結的有效期限為24小時。

## 允許清單邏輯 {#logic}

>[!CONTEXTUALHELP]
>id="ajo_admin_allowed_list_logic"
>title="管理允许列表"
>abstract="激活允许列表后，只有包含在允许列表中的收件人才能收到来自此沙盒的电子邮件。如果停用，则所有收件人都将收到电子邮件。"

當允許清單為 [作用中](#enable-allow-list)，則套用下列邏輯：

* 如果允許清單為 **空白**，不會傳送任何電子郵件。

* 如果實體為 **在允許清單上**，而不是在隱藏清單上，電子郵件會傳送給相對應的收件者。 但是，如果實體也在 [隱藏清單](../reports/suppression-list.md)，對應的收件者將不會收到電子郵件，原因為 **[!UICONTROL 已隱藏]**.

* 如果實體為 **不在允許清單上** （不在隱藏清單上），對應的收件者將不會收到電子郵件，原因為 **[!UICONTROL 不允許]**.

>[!NOTE]
>
>設定檔具有 **[!UICONTROL 不允許]** 在訊息傳送過程中會排除狀態。 因此，當 **歷程報告** 會將這些設定檔顯示為已移動通過歷程([讀取區段](../building-journeys/read-segment.md) 和 [訊息活動](../building-journeys/journeys-message.md))， **以電子郵件傳送報告** 不會將其納入 **[!UICONTROL 已傳送]** 量度，因為這些量度在傳送電子郵件前會被篩選掉。
>
>進一步瞭解 [即時報告](../reports/live-report.md) 和 [全域報告](../reports/global-report.md).

當允許清單為 [已停用](#deactivate-allow-list)，您從目前沙箱傳送的所有電子郵件都會傳送給所有收件者（前提是這些電子郵件不在隱藏清單中），包括真實的客戶地址。

## 排除報告 {#reporting}

當允許清單作用中時，您可以擷取由於不在允許清單中而未傳送的電子郵件地址或網域。 若要這麼做，您可以使用 [Adobe Experience Platform查詢服務](https://experienceleague.adobe.com/docs/experience-platform/query/api/getting-started.html){target="_blank"} 進行下列API呼叫。

若要取得 **電子郵件數量** 因為收件者不在允許清單中而未傳送的郵件，請使用以下查詢：

```sql
SELECT count(distinct _id) from cjm_message_feedback_event_dataset WHERE
_experience.customerJourneyManagement.messageExecution.messageExecutionID = '<MESSAGE_EXECUTION_ID>' AND
_experience.customerJourneyManagement.messageDeliveryfeedback.feedbackStatus = 'exclude' AND
_experience.customerJourneyManagement.messageDeliveryfeedback.messageExclusion.reason = 'EmailNotAllowed'
```

若要取得 **電子郵件地址清單** 因為收件者不在允許清單中而未傳送的郵件，請使用以下查詢：

```sql
SELECT distinct(_experience.customerJourneyManagement.emailChannelContext.address) from cjm_message_feedback_event_dataset WHERE
_experience.customerJourneyManagement.messageExecution.messageExecutionID IS NOT NULL AND
_experience.customerJourneyManagement.messageDeliveryfeedback.feedbackStatus = 'exclude' AND
_experience.customerJourneyManagement.messageDeliveryfeedback.messageExclusion.reason = 'EmailNotAllowed'
```
