---
solution: Journey Optimizer
product: journey optimizer
title: Journey Optimizer中的归档支持
description: 了解如何存档消息
feature: Channel Configuration
topic: Administration
role: Admin
level: Experienced
keywords: 存档，消息， HIPAA，密件抄送，电子邮件
exl-id: 186a5044-80d5-4633-a7a7-133e155c5e9f
source-git-commit: bbc64b4274cee083e6c35147314b230391b35317
workflow-type: tm+mt
source-wordcount: '1337'
ht-degree: 6%

---

# 存档支持 {#archiving-support}

## 如何存档消息 {#about-archiving}

HIPAA等法规要求[!DNL Journey Optimizer]应提供一种将发送给个人的邮件存档的方法。 事实上，如果您的客户提出索赔，他们应能够获取已发送消息的副本以进行验证。

* 对于电子邮件渠道，[!DNL Journey Optimizer]提供了内置的密件抄送电子邮件功能。 [了解详情](#bcc-email)

* 此外，对于所有渠道，您可以使用&#x200B;**实体数据集**&#x200B;中的“模板”字段，该字段包含非个性化消息模板的详细信息。 使用此字段导出数据集以保存元数据，例如：消息发送者、发送对象和时间。 请注意，不会导出个性化数据，而只会考虑模板（消息的格式和结构）。 [了解详情](../data/datasets-query-examples.md#entity-dataset)

>[!NOTE]
>
>[!DNL Journey Optimizer]不拥有对SMS存档要求的支持。 要获得专门的存档支持，请与您的SMS供应商（ Sinch 、 Infobip或Twilio ）合作。

## 如何使用密件抄送发送电子邮件 {#bcc-email}

>[!CONTEXTUALHELP]
>id="ajo_admin_preset_bcc"
>title="定义密件抄送电子邮件地址"
>abstract="您可以通过将电子邮件发送到密件抄送收件箱，保留所发送电子邮件的副本。输入您选择的电子邮件地址，这样发送的每封电子邮件都会被密送至此密件抄送地址。请注意，密件抄送地址域必须不同于委派给 Adobe 的任何子域。此功能属于可选功能。"

您可以将[!DNL Journey Optimizer]发送的电子邮件的密件抄送(BCC)发送至专用的密件抄送地址。 此可选功能允许您保留发送给用户的电子邮件通信副本，以便进行合规性和/或存档。 密件抄送地址对邮件的其他收件人不可见。

### 启用密件抄送电子邮件 {#enable-bcc}

要启用&#x200B;**[!UICONTROL 密件抄送电子邮件]**&#x200B;选项，请在[渠道配置](channel-surfaces.md)的专用字段中输入您选择的电子邮件地址（即消息预设）。 除了在委派给Adobe的子域上定义的电子邮件地址之外，您可以按正确的格式指定任何外部地址。 例如，如果您已将&#x200B;*marketing.luma.com*&#x200B;子域委派给Adobe，则禁止使用&#x200B;*abc@marketing.luma.com*&#x200B;等任何地址。

>[!CAUTION]
>
>您只能定义一个密件抄送电子邮件地址。 确保密件抄送地址有足够的接收容量来存储使用当前渠道配置发送的所有电子邮件。
>
>[此部分](#bcc-recommendations-limitations)中列出了更多推荐。

>[!NOTE]
>
>如果您已购买Healthcare Shield附加产品，则必须确保密件抄送地址的ISP支持TLS 1.2协议。

![](assets/preset-bcc.png)

完成配置后，基于此配置的所有电子邮件都将密件复制到您输入的密件抄送电子邮件地址。 从那里，可以使用外部系统处理和存档消息。

>[!CAUTION]
>
>密件抄送功能使用量根据您获得许可的邮件数计算。 因此，只能在用于要存档的关键通信的配置中启用它。 检查您的合同中是否有许可卷。

密件抄送电子邮件地址设置会立即在配置级别保存和处理。 使用此配置创建新邮件时，会自动显示密件抄送电子邮件地址。

![](assets/preset-bcc-in-msg.png)

但是，将拾取密件抄送地址以按照[此处](../email/email-settings.md)描述的逻辑发送通信。

### Recommendations和限制 {#bcc-recommendations-limitations}

* 为确保您的隐私合规性，密件抄送电子邮件必须由能够安全存储个人身份信息(PII)的归档系统处理。

* 由于邮件可能包含敏感或私有数据(如个人身份信息(PII))，请确保密件抄送地址正确无误，并保护对邮件的访问。

* 您用于密件抄送的收件箱应正确管理空间和投放。 如果收件箱返回退件，则可能无法接收某些电子邮件，因此将无法存档。

* 消息可在目标收件人之前传送到密件抄送电子邮件地址。 密件抄送邮件也可以发送，即使原始邮件可能有[退回](../reports/suppression-list.md#delivery-failures)。

  <!--OR: Only successfully sent emails are taken in account. [Bounces](../reports/suppression-list.md#delivery-failures) are not. TO CHECK -->

* 请勿打开或点击发送到BCC地址的电子邮件，因为发送分析的总打开数和点击数中已考虑该电子邮件，这可能会导致[报告](../reports/global-report.md)中的一些计算错误。

* 请勿在密件抄送收件箱中将邮件标记为垃圾邮件，因为它会影响发送到此地址的所有其他电子邮件。

>[!CAUTION]
>
>请勿单击发送到密件抄送地址的电子邮件中的取消订阅链接，因为您将立即取消订阅相应的收件人。

### GDPR合规性 {#gdpr-compliance}

GDPR等法规规定，数据主体应能够随时修改其同意书。 由于您通过Journey Optimizer发送的密件抄送电子邮件包含安全个人身份信息(PII)，因此您必须编辑&#x200B;**[!UICONTROL CJM电子邮件密件抄送反馈事件架构]**，以便能够按照GDPR和类似法规管理这些PII。

为此，请执行以下步骤。

1. 转到&#x200B;**[!UICONTROL 数据管理]** > **[!UICONTROL 架构]** > **[!UICONTROL 浏览]**&#x200B;并选择&#x200B;**[!UICONTROL CJM电子邮件BCC反馈事件架构]**。

   ![](assets/preset-bcc-schema.png)

1. 单击以展开&#x200B;**[!UICONTROL _experience]**、**[!UICONTROL customerJourneyManagment]**&#x200B;和&#x200B;**[!UICONTROL secondaryRecipientDetail]**。

1. 选择&#x200B;**[!UICONTROL originalRecipientAddress]**

1. 在右侧的&#x200B;**[!UICONTROL 字段属性]**&#x200B;中，向下滚动到&#x200B;**[!UICONTROL 标识]**&#x200B;复选框。

1. 选择它，同时选择&#x200B;**[!UICONTROL 主标识]**。

1. 从下拉列表中选择一个命名空间。

   ![](assets/preset-bcc-schema-identity.png)

1. 单击&#x200B;**[!UICONTROL 应用]**。

>[!NOTE]
>
>在[Experience Platform文档](https://experienceleague.adobe.com/docs/experience-platform/privacy/home.html?lang=zh-Hans){target="_blank"}中了解有关管理隐私和适用法规的更多信息。

### 密件抄送报表数据 {#bcc-reporting}

历程和消息报表中没有此类密件抄送报告。 但是，信息存储在名为&#x200B;**[!UICONTROL AJO密件抄送反馈事件数据集]**&#x200B;的系统数据集上。 您可以对此数据集运行查询，以查找用于调试的有用信息，例如。

若要通过用户界面访问此数据集，请选择&#x200B;**[!UICONTROL 数据管理]** > **[!UICONTROL 数据集]** > **[!UICONTROL 浏览]**。 在[本节](../data/get-started-datasets.md#access-datasets)中了解有关如何访问数据集的更多信息。

<!--![](assets/preset-bcc-dataset.png)-->

若要对此数据集运行查询，您可以使用[Adobe Experience Platform查询服务](https://experienceleague.adobe.com/docs/experience-platform/query/api/getting-started.html){target="_blank"}提供的查询编辑器。 若要访问它，请选择&#x200B;**[!UICONTROL 数据管理]** > **[!UICONTROL 查询]**，然后单击&#x200B;**[!UICONTROL 创建查询]**。 [了解详情](../data/get-started-queries.md)

![](assets/preset-bcc-queries.png)

根据您要查找的信息，可以运行以下查询。

1. 对于下面的所有其他查询，您将需要历程操作ID。 运行此查询以获取过去2天内与特定历程版本ID关联的所有操作ID：

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
   >要获取`<journey version id>`参数，请从&#x200B;**[!UICONTROL 历程管理]** > **[!UICONTROL 历程]**&#x200B;菜单中选择相应的[历程版本](../building-journeys/journey.md#journey-versions)。 历程版本ID显示在Web浏览器中显示的URL的末尾。
   >
   >![](assets/preset-bcc-action-id.png)

1. 运行此查询以获取针对特定用户在最近2天内定向的特定消息生成的所有消息反馈事件（尤其是反馈状态）：

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
   >要获取`<journey action id>`参数，请使用历程版本ID运行上述第一个查询。 `<recipient email address>`参数是目标或实际收件人的电子邮件地址。

1. 运行此查询以获取针对过去2天内特定用户的特定消息生成的所有密件抄送消息反馈事件：

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

1. 运行此查询以提取所有未收到消息，但过去30天内存在密件抄送条目的收件人地址：

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

### 使用邮件标头协调密件抄送副本和已发送电子邮件信息 {#bcc-header}

例如，当电子邮件密送副本在外部系统上存档时，您可以使用消息中包含的标头检索相应已发送电子邮件的信息。

现在，每封电子邮件都包含一个名为`x-message-profile-id`的标头。 每个用户档案的此标头的值各不相同：对于每个已发送的电子邮件及其相应的密件抄送电子邮件副本，它是唯一的。

`x-message-profile-id`标头还存储在以下系统数据集中：[AJO消息反馈事件数据集](../data/datasets-query-examples.md#message-feedback-event-dataset)（已发送电子邮件）和[AJO密件抄送反馈事件数据集](#bcc-reporting)（密件抄送副本）。 您可以查询这些数据集以协调密件抄送副本和相应的实际电子邮件。

* 若要通过用户界面访问这些数据集，请选择&#x200B;**[!UICONTROL 数据管理]** > **[!UICONTROL 数据集]** > **[!UICONTROL 浏览]**。 在[本节](../data/get-started-datasets.md#access-datasets)中了解有关如何访问数据集的更多信息。

* 使用[Adobe Experience Platform查询服务](https://experienceleague.adobe.com/docs/experience-platform/query/api/getting-started.html){target="_blank"}提供的查询编辑器。 若要访问它，请选择&#x200B;**[!UICONTROL 数据管理]** > **[!UICONTROL 查询]**，然后单击&#x200B;**[!UICONTROL 创建查询]**。 [了解详情](../data/get-started-queries.md)

以下是一些示例查询，您可以运行这些查询来检索与密件抄送副本对应的信息。

**查询1**

要将密件抄送事件与实际电子邮件的相应反馈事件与促销活动操作详细信息拼合，请执行以下操作：

```
SELECT
  mfe.timestamp as OriginalRecipientFeedbackEventTime,
  mfe._experience.customerJourneyManagement.emailChannelContext.address AS OriginalRecipientEmailAddress,
  mfe._experience.customerjourneymanagement.messagedeliveryfeedback.feedbackstatus AS OriginalRecipientMessageFeedbackStatus,
  mfe._experience.customerJourneyManagement.messageExecution.campaignID AS CampaignID,
  mfe._experience.customerJourneyManagement.messageExecution.campaignActionID AS CampaignActionID,
  mfe._experience.customerJourneyManagement.messageExecution.batchInstanceID AS BatchInstanceID,
  mfe._experience.customerJourneyManagement.messageExecution.messageID AS MessageID AS MessageID
FROM ajo_bcc_feedback_event_dataset bcc
LEFT JOIN cjm_message_feedback_event_dataset mfe
ON bcc._experience.customerJourneyManagement.messageProfile.messageProfileID =
    mfe._experience.customerJourneyManagement.messageProfile.messageProfileID AND 
    mfe.timestamp > now() - INTERVAL '30' day
WHERE 
  bcc.timestamp > now() - INTERVAL '30' DAY AND 
  bcc._experience.customerJourneyManagement.messageProfile.messageProfileID = 'x-message-profile-id'
ORDER BY timestamp DESC;
```

**查询2**

要将BCC事件与实际电子邮件的相应反馈事件与历程操作详细信息拼合，请执行以下操作：

```
SELECT
  mfe.timestamp as OriginalRecipientFeedbackEventTime,
  mfe._experience.customerJourneyManagement.emailChannelContext.address AS OriginalRecipientEmailAddress,
  mfe._experience.customerjourneymanagement.messagedeliveryfeedback.feedbackstatus AS OriginalRecipientMessageFeedbackStatus,
  mfe._experience.customerJourneyManagement.messageExecution.journeyVersionID AS JourneyVersionID,
  mfe._experience.customerJourneyManagement.messageExecution.journeyVersionInstanceID AS JourneyVersionInstanceID,
  mfe._experience.customerJourneyManagement.messageExecution.batchInstanceID AS BatchInstanceID,
  mfe._experience.customerJourneyManagement.messageExecution.messageID AS MessageID AS MessageID
FROM ajo_bcc_feedback_event_dataset bcc
LEFT JOIN cjm_message_feedback_event_dataset mfe
ON bcc._experience.customerJourneyManagement.messageProfile.messageProfileID =
    mfe._experience.customerJourneyManagement.messageProfile.messageProfileID AND 
    mfe.timestamp > now() - INTERVAL '30' day
WHERE 
  bcc.timestamp > now() - INTERVAL '30' DAY AND 
  bcc._experience.customerJourneyManagement.messageProfile.messageProfileID = 'x-message-profile-id'
ORDER BY timestamp DESC;
```
