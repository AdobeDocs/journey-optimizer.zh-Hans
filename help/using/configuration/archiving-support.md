---
solution: Journey Optimizer
product: journey optimizer
title: Journey Optimizer的封存支援
description: 瞭解如何封存訊息
feature: Application Settings
topic: Administration
role: Admin
level: Intermediate
keywords: 封存，訊息， HIPAA，密件副本，電子郵件
exl-id: 186a5044-80d5-4633-a7a7-133e155c5e9f
source-git-commit: 9657862f1c6bdb2399fcf3e6384bb9dec5b8f32b
workflow-type: tm+mt
source-wordcount: '1133'
ht-degree: 7%

---

# 存档支持 {#archiving-support}

## 如何封存訊息 {#about-archiving}

HIPAA等法規規定 [!DNL Journey Optimizer] 應提供一種封存傳送給個人的訊息的方式。 事實上，如果您的客戶提出索賠，他們應該能夠取得已傳送訊息的副本以進行驗證。

* 對於電子郵件頻道， [!DNL Journey Optimizer] 提供內建的密件副本電子郵件功能。 [了解详情](#bcc-email)

* 此外，對於所有管道，您可以使用 **實體資料集**，其中包含非個人化訊息範本的詳細資料。 使用此欄位匯出資料集以儲存中繼資料，例如：傳送訊息的對象、收件者和時間。 請注意，不會匯出個人化資料，而只會考慮範本（訊息的格式和結構）。 [了解详情](../data/datasets-query-examples.md#entity-dataset)

>[!NOTE]
>
>[!DNL Journey Optimizer] 不支援SMS封存需求。 如需專屬的封存支援，請與您的SMS供應商（Synch或Twilio）合作。

## 如何使用密件副本處理電子郵件 {#bcc-email}

>[!CONTEXTUALHELP]
>id="ajo_admin_preset_bcc"
>title="定义密件抄送电子邮件地址"
>abstract="您可以通过将电子邮件发送到密件抄送收件箱，保留所发送电子邮件的副本。输入您选择的电子邮件地址，这样发送的每封电子邮件都会被密送至此密件抄送地址。请注意，密件抄送地址域不应与委派给 Adobe 的任何子域相同。此功能属于可选功能。"

您可以傳送所傳送電子郵件的相同復本（或密件副本） [!DNL Journey Optimizer] 至密件副本收件匣。 此選擇性功能可讓您保留傳送給使用者的電子郵件通訊復本，以供合規性和/或封存之用。 傳遞收件者將無法看到此訊息。

### 啟用密件副本電子郵件 {#enable-bcc}

若要啟用 **[!UICONTROL 密件副本電子郵件]** 選項，請在的專屬欄位中輸入您選擇的電子郵件地址 [管道表面](channel-surfaces.md) （即訊息預設集）。 您可以指定正確格式的任何外部地址，但委派給Adobe的子網域上定義的電子郵件地址除外。 例如，如果您委派 *marketing.luma.com* 要Adobe的子網域，任何位址，例如 *abc@marketing.luma.com* 為禁止。

>[!CAUTION]
>
>您只能定義一個密件副本電子郵件地址。 請確定密件副本位址有足夠的接收容量，以儲存使用目前頻道介面傳送的所有電子郵件。
>
>下列清單中列出更多建議 [本節](#bcc-recommendations-limitations).

>[!NOTE]
>
>如果您已購買Healthcare Shield附加產品，您必須確保密件副本位址的ISP支援TLS 1.2通訊協定。

![](assets/preset-bcc.png)

使用此介面的所有電子郵件訊息都將密件副本至您輸入的密件副本電子郵件地址。 從那裡，可以使用外部系統處理和封存它們。

>[!CAUTION]
>
>密件副本功能的使用量將根據您獲授權的訊息數量計算。 因此，只能在用於要封存的關鍵通訊的表面中啟用它。 檢查您的合約以取得授權磁碟區。

密件副本電子郵件地址設定會立即在表面層級儲存和處理。 當您使用此介面建立新訊息時，會自動顯示密件副本電子郵件地址。

![](assets/preset-bcc-in-msg.png)

不過，系統會擷取密件副本位址，以便依照所述的邏輯傳送通訊 [此處](../email/email-settings.md).

### Recommendations和限制 {#bcc-recommendations-limitations}

* 為確保您的隱私權合規性，密件副本電子郵件必須由能夠安全地儲存個人識別資訊(PII)的封存系統處理。

* 由於郵件可能包含敏感或私人資料(例如個人識別資訊(PII))，請確定BCC位址正確，並保護對郵件的存取權。

* 您用於密件副本的收件匣應可妥善管理空間和傳遞。 如果收件匣傳回跳出，則可能無法接收某些電子郵件，因此無法封存。

* 訊息可在目標收件者之前傳遞至密件副本電子郵件地址。 密件副本訊息也可以傳送，即使原始訊息可能有 [已退回](../reports/suppression-list.md#delivery-failures).

   <!--OR: Only successfully sent emails are taken in account. [Bounces](../reports/suppression-list.md#delivery-failures) are not. TO CHECK -->

* 請勿開啟或點選傳送至密件副本地址的電子郵件，因為傳送分析的總開啟次數和點按次數會將其列入考量，這可能會導致計算錯誤 [報告](../reports/global-report.md).

* 請勿在密件副本收件匣中將郵件標示為垃圾郵件，因為它會影響傳送至此地址的所有其他電子郵件。

>[!CAUTION]
>
>請勿在傳送至密件副本地址的電子郵件中按一下取消訂閱連結，因為您將立即取消訂閱對應的收件者。

### GDPR法規遵循 {#gdpr-compliance}

GDPR等法規規定，資料主體應能隨時修改其同意。 由於您使用Journey Optimizer傳送的密件副本電子郵件包含安全的個人識別資訊(PII)，因此您必須編輯 **[!UICONTROL CJM電子郵件BCC回饋事件結構描述]** 能夠根據GDPR和類似法規管理這些PII。

为此，请执行以下步骤。

1. 前往 **[!UICONTROL 資料管理]** > **[!UICONTROL 結構描述]** > **[!UICONTROL 瀏覽]** 並選取 **[!UICONTROL CJM電子郵件BCC回饋事件結構描述]**.

   ![](assets/preset-bcc-schema.png)

1. 按一下以展開 **[!UICONTROL 體驗(_E)]**， **[!UICONTROL customerJourneyManagement]** 則 **[!UICONTROL secondaryRecipientDetail]**.

1. 選取 **[!UICONTROL originalRepientAddress]**.

1. 在 **[!UICONTROL 欄位屬性]** 在右側，向下捲動至 **[!UICONTROL 身分]** 核取方塊。

1. 請選取它，也請選取 **[!UICONTROL 主要身分]**.

1. 從下拉式清單中選取名稱空間。

   ![](assets/preset-bcc-schema-identity.png)

1. 单击&#x200B;**[!UICONTROL 应用]**。

>[!NOTE]
>
>進一步瞭解管理隱私權和 [Experience Platform檔案](https://experienceleague.adobe.com/docs/experience-platform/privacy/home.html?lang=zh-Hans){target="_blank"}.

### 密件副本報告資料 {#bcc-reporting}

歷程和訊息報表中沒有密件副本的相關報表。 不過，資訊會儲存在名為的系統資料集中 **[!UICONTROL AJO密件副本意見事件資料集]**. 您可以針對此資料集執行查詢，以尋找有用的資訊，例如用於偵錯。

您可以透過使用者介面存取此資料集。 選取 **[!UICONTROL 資料管理]** > **[!UICONTROL 資料集]** > **[!UICONTROL 瀏覽]** 並啟用 **[!UICONTROL 顯示系統資料集]** 從篩選器切換以顯示系統產生的資料集。 進一步瞭解如何存取中的資料集 [本節](../data/get-started-datasets.md#access-datasets).

![](assets/preset-bcc-dataset.png)

若要針對此資料集執行查詢，您可以使用 [Adobe Experience Platform查詢服務](https://experienceleague.adobe.com/docs/experience-platform/query/api/getting-started.html){target="_blank"}. 若要存取，請選取「 」 **[!UICONTROL 資料管理]** > **[!UICONTROL 查詢]** 並按一下 **[!UICONTROL 建立查詢]**. [了解详情](../data/get-started-queries.md)

![](assets/preset-bcc-queries.png)

根據您要尋找的資訊，您可以執行下列查詢。

1. 對於以下所有其他查詢，您將需要歷程動作ID。 執行此查詢以擷取過去2天內與特定歷程版本ID相關聯的所有動作ID：

   ```
   SELECT
   DISTINCT
   CAST(TIMESTAMP AS DATE) AS EventTime,
   _experience.journeyOrchestration.stepEvents.journeyVersionID,
   _experience.journeyOrchestration.stepEvents.actionName, 
   _experience.journeyOrchestration.stepEvents.actionID 
   FROM journey_step_events 
   WHERE 
   _experience.journeyOrchestration.stepEvents.journeyVersionID = '<journey version id>' AND 
   _experience.journeyOrchestration.stepEvents.actionID is not NULL AND 
   TIMESTAMP > NOW() - INTERVAL '2' DAY 
   ORDER BY EventTime DESC;
   ```

   >[!NOTE]
   >
   >若要取得 `<journey version id>`引數，選取對應的 [歷程版本](../building-journeys/journey.md#journey-versions) 從 **[!UICONTROL 歷程管理]** > **[!UICONTROL 歷程]** 功能表。 歷程版本ID會顯示在網頁瀏覽器中顯示的URL結尾。
   >
   >![](assets/preset-bcc-action-id.png)

1. 執行此查詢以擷取針對特定使用者在過去2天內的特定訊息產生的所有訊息回饋事件（尤其是回饋狀態）：

   ```
   SELECT  
   _experience.customerJourneyManagement.messageExecution.journeyVersionID AS JourneyVersionID, 
   _experience.customerJourneyManagement.messageExecution.journeyActionID AS JourneyActionID, 
   timestamp AS EventTime, 
   _experience.customerJourneyManagement.emailChannelContext.address AS RecipientAddress, 
   _experience.customerjourneymanagement.messagedeliveryfeedback.feedbackStatus AS FeedbackStatus,
   CASE _experience.customerjourneymanagement.messagedeliveryfeedback.feedbackStatus
       WHEN 'sent' THEN 'Sent'
       WHEN 'delay' THEN 'Retry'
       WHEN 'out_of_band' THEN 'Bounce' 
       WHEN 'bounce' THEN 'Bounce'
   END AS FeedbackStatusCategory
   FROM cjm_message_feedback_event_dataset 
   WHERE  
       timestamp > now() - INTERVAL '2' day  AND
       _experience.customerJourneyManagement.messageExecution.journeyVersionID = '<journey version id>' AND 
       _experience.customerJourneyManagement.messageExecution.journeyActionID = '<journey action id>' AND  
       _experience.customerJourneyManagement.emailChannelContext.address = '<recipient email address>'
       ORDER BY EventTime DESC;
   ```

   >[!NOTE]
   >
   >若要取得 `<journey action id>` 引數，使用歷程版本id執行上述第一個查詢。 此 `<recipient email address>` parameter是目標或實際收件者的電子郵件地址。

1. 執行此查詢以擷取針對過去2天內特定使用者為目標的特定訊息所產生的所有BCC訊息回饋事件：

   ```
   SELECT   
   _experience.customerJourneyManagement.messageExecution.journeyVersionID AS JourneyVersionID, 
   _experience.customerJourneyManagement.messageExecution.journeyActionID AS JourneyActionID, 
   _experience.customerJourneyManagement.emailChannelContext.address AS BccEmailAddress,
   timestamp AS EventTime, 
   _experience.customerJourneyManagement.secondaryRecipientDetail.originalRecipientAddress AS RecipientAddress, 
   _experience.customerjourneymanagement.messagedeliveryfeedback.feedbackStatus AS FeedbackStatus,
   CASE _experience.customerjourneymanagement.messagedeliveryfeedback.feedbackStatus
               WHEN 'sent' THEN 'Sent'
               WHEN 'delay' THEN 'Retry'
               WHEN 'out_of_band' THEN 'Bounce' 
               WHEN 'bounce' THEN 'Bounce'
           END AS FeedbackStatusCategory 
   FROM ajo_bcc_feedback_event_dataset  
   WHERE  
   timestamp > now() - INTERVAL '2' day  AND
   _experience.customerJourneyManagement.messageExecution.journeyVersionID = '<journey version id>' AND 
   _experience.customerJourneyManagement.messageExecution.journeyActionID = '<journeyaction id>' AND 
   _experience.customerJourneyManagement.secondaryRecipientDetail.originalRecipientAddress = '<recipient email address>'
   ORDER BY EventTime DESC;
   ```

1. 執行此查詢以擷取所有未收到訊息（但密件副本專案在過去30天內存在）的收件者地址：

   ```
    SELECT
        DISTINCT 
    bcc._experience.customerJourneyManagement.secondaryRecipientDetail.originalRecipientAddress AS RecipientAddressesNotRecievedMessage
    FROM ajo_bcc_feedback_event_dataset bcc
    LEFT JOIN cjm_message_feedback_event_dataset mfe
    ON 
   bcc._experience.customerJourneyManagement.messageExecution.journeyVersionID =
            mfe._experience.customerJourneyManagement.messageExecution.journeyVersionID AND    bcc._experience.customerJourneyManagement.messageExecution.journeyActionID = mfe._experience.customerJourneyManagement.messageExecution.journeyActionID AND 
   bcc._experience.customerJourneyManagement.secondaryRecipientDetail.originalRecipientAddress = mfe._experience.customerJourneyManagement.emailChannelContext.address AND
   mfe._experience.customerJourneyManagement.messageExecution.journeyVersionID = '<journey version id>' AND 
   mfe._experience.customerJourneyManagement.messageExecution.journeyActionID = '<journey action id>' AND
   mfe.timestamp > now() - INTERVAL '30' DAY AND
   mfe._experience.customerjourneymanagement.messagedeliveryfeedback.feedbackstatus IN ('bounce', 'out_of_band') 
    WHERE bcc.timestamp > now() - INTERVAL '30' DAY;
   ```
