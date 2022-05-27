---
title: 配置电子邮件设置
description: 了解如何在消息预设级别配置电子邮件设置
feature: Application Settings
topic: Administration
role: Admin
level: Intermediate
exl-id: 13536962-7541-4eb6-9ccb-4f97e167734a
source-git-commit: c48d083445d4e4c7cdbed1a61cee13ed3fcfcc8b
workflow-type: tm+mt
source-wordcount: '2166'
ht-degree: 2%

---

# 配置电子邮件设置 {#email-settings}

在消息预设配置的专用部分中定义电子邮件设置。 了解如何在 [此部分](message-presets.md).

![](assets/preset-email.png)

## 电子邮件类型 {#email-type}

>[!CONTEXTUALHELP]
>id="ajo_admin_presets_emailtype"
>title="定义电子邮件类别"
>abstract="选择使用此预设时将发送的消息类型：促销消息的营销（需要用户同意）或非商业消息的事务型消息，也可以在特定环境中发送给未订阅的用户档案。"

在 **电子邮件类型** ，选择要随预设一起发送的消息类型： **营销** 或 **事务型**.

* 选择 **营销** 对于促销消息：这些消息需要用户同意。

* 选择 **事务型** 例如，对于订单确认、密码重置通知或投放信息等非商业性消息。

>[!CAUTION]
>
>**事务型** 消息可发送给从营销通信中取消订阅的用户档案。 这些消息只能在特定上下文中发送。

When [创建消息](../messages/get-started-content.md#create-new-message)，则必须选择与您为消息选择的类别匹配的有效消息预设。

## 子域和IP池 {#subdomains-and-ip-pools}

在 **子域和IP池详细信息** 部分，您必须：

1. 选择要用于发送电子邮件的子域。 [了解详情](about-subdomain-delegation.md)

1. 选择要与预设关联的IP池。 [了解详情](ip-pools.md)

![](assets/preset-subdomain-ip-pool.png)

当选定的IP池位于下时，无法继续创建预设 [版本](ip-pools.md#edit-ip-pool) (**[!UICONTROL Processing]** 状态)且从未与选定的子域关联。 否则，仍将使用IP池/子域关联的最旧版本。 如果出现这种情况，请将预设另存为草稿，然后在IP池具有 **[!UICONTROL Success]** 状态。

>[!NOTE]
>
>对于非生产环境，Adobe不会创建现成的测试子域，也不会授予对共享发送IP池的访问权限。 您需要 [委派您自己的子域](delegate-subdomain.md) 并使用分配给贵组织的池中的IP。

## 列表取消订阅 {#list-unsubscribe}

On [选择子域](#subdomains-and-ip-pools) 在列表中， **[!UICONTROL Enable List-Unsubscribe]** 选项。

![](assets/preset-list-unsubscribe.png)

默认启用此选项。

如果保持启用状态，则取消订阅链接将自动包含在电子邮件标题中，例如：

![](assets/preset-list-unsubscribe-header.png)

如果禁用此选项，则电子邮件标题中不会显示取消订阅链接。

取消订阅链接包含两个元素：

* 安 **取消订阅电子邮件地址**，所有取消订阅请求都将发送到该服务器。

   在 [!DNL Journey Optimizer]，则取消订阅电子邮件地址为默认地址 **[!UICONTROL Mailto (unsubscribe)]** 消息预设中显示的地址(基于 [选定子域](#subdomains-and-ip-pools).

   ![](assets/preset-list-unsubscribe-mailto.png)

* 的 **取消订阅URL**，取消订阅后，用户将被重定向到的登陆页面的URL。

   如果您添加 [一键式选择退出链接](../messages/consent.md#one-click-opt-out) 对于使用此预设创建的消息，取消订阅URL将是为一键单击选择退出链接定义的URL。

   ![](assets/preset-list-unsubscribe-opt-out-url.png)

   >[!NOTE]
   >
   >如果您没有在消息内容中添加一键单击选择退出链接，则不会向用户显示登陆页面。

在 [此部分](../messages/consent.md#unsubscribe-header).

<!--Select the **[!UICONTROL Custom List-Unsubscribe]** option to enter your own Unsubscribe URL and/or your own Unsubscribe email address.(to add later)-->

## 标头参数{#email-header}

在 **[!UICONTROL HEADER PARAMETERS]** 部分，输入与使用该预设发送的消息类型关联的发件人名称和电子邮件地址。

>[!CAUTION]
>
>电子邮件地址必须使用当前选定的 [委派子域](about-subdomain-delegation.md).

* **[!UICONTROL Sender name]**:发件人的名称，如您的品牌名称。

* **[!UICONTROL Sender email]**:要用于通信的电子邮件地址。 例如，如果委派的子域为 *marketing.luma.com*，您可以使用 *contact@marketing.luma.com*.

* **[!UICONTROL Reply to (name)]**:收件人单击 **回复** 按钮。

* **[!UICONTROL Reply to (email)]**:收件人单击 **回复** 按钮。 您必须使用在委派子域上定义的地址(例如， *reply@marketing.luma.com*)，否则将删除电子邮件。

* **[!UICONTROL Error email]**:收到ISP在收到几天邮件后（异步退回）生成的所有错误，均位于此地址。

![](assets/preset-header.png)

>[!NOTE]
>
>地址必须以字母(A-Z)开头，且只能包含字母数字字符。 还可以使用下划线 `_`，点`.` 和连字符 `-` 字符。

### 转发电子邮件 {#forward-email}

如果您希望将收到的所有电子邮件转发到特定电子邮件地址 [!DNL Journey Optimizer] 对于委派的子域，请联系Adobe客户关怀团队。 您需要提供：

* 您选择的转发电子邮件地址。 请注意，转发电子邮件地址域与委派给Adobe的任何子域都不匹配。
* 您的沙盒名称。
* 将使用转发电子邮件（或“回复”）地址的预设名称。
* 当前 **[!UICONTROL Reply to (email)]** 在预设级别设置的地址。

>[!NOTE]
>
>每个子域只能有一个转发电子邮件地址。 因此，如果多个预设使用相同的子域，则所有预设都必须使用相同的转发电子邮件地址。

转发电子邮件地址将由Adobe设置。 这可能需要3到4天。

## 密送电子邮件 {#bcc-email}

>[!CONTEXTUALHELP]
>id="ajo_admin_preset_bcc"
>title="定义密送电子邮件地址"
>abstract="您可以通过将已发送的电子邮件发送到密件抄送收件箱来保留其副本。 输入您选择的电子邮件地址，以便发送的每封电子邮件都会被盲目复制到此密件抄送地址。 此功能属于可选功能。"

您可以发送由 [!DNL Journey Optimizer] 发送到密件抄送收件箱。 此可选功能允许您保留您发送给用户的电子邮件通信副本，以便符合规范和/或进行存档。 投放收件人将看不到该内容。

>[!CAUTION]
>
>此功能将从 **5月31日**.

### 启用密送电子邮件 {#enable-bcc}

启用 **[!UICONTROL BCC email]** 选项，在专用字段中输入您选择的电子邮件地址。 除了在委派的子域上定义的电子邮件地址之外，您可以以正确的格式指定任何外部地址。 例如，如果委派的子域为 *marketing.luma.com*，任何地址，如 *abc@marketing.luma.com* 禁止。

>[!NOTE]
>
>您只能定义一个密件抄送电子邮件地址。 确保密件抄送地址具有足够的接收容量，以存储使用当前预设发送的所有电子邮件。
>
>中列出了更多推荐 [此部分](#bcc-recommendations-limitations).

![](assets/preset-bcc.png)

使用此预设的所有电子邮件都将被盲目复制到您输入的密件抄送电子邮件地址。 在此处，可以使用外部系统处理和存档它们。

>[!CAUTION]
>
>您的密件抄送功能使用情况将根据您获得许可的消息数量进行计数。 因此，请仅在要存档的关键通信所使用的预设中启用它。 检查您的合同中是否有许可的卷。

“密件抄送”电子邮件地址设置会立即在预设级别保存和处理。 当您 [创建新消息](../messages/get-started-content.md#create-new-message) 使用此预设时，会自动显示密送电子邮件地址。

![](assets/preset-bcc-in-msg.png)

但是，密送地址会按照以下逻辑接收以发送通信：

* 对于批处理和拆分历程，它不适用于在进行密送设置之前已启动的批处理或拆分执行。 更改将在下次重复或新执行时被提取。

* 对于事务型消息，将立即接收更改，以便进行下次通信（最多延迟一分钟）。

>[!NOTE]
>
>您无需重新发布消息或旅程，即可接收密送设置。

### Recommendations和限制 {#bcc-recommendations-limitations}

* 为确保您的隐私合规性，密件抄送电子邮件必须由能够安全存储个人身份信息(PII)的归档系统进行处理。

* 由于消息可以包含敏感或私有数据，如个人身份信息(PII)，因此请确保密件抄送地址正确，并确保消息的访问安全。

* 对于空间和投放，应正确管理用于密件抄送的收件箱。 如果收件箱返回退回，则可能未收到某些电子邮件，因此将无法存档。

* 在目标收件人之前，可以将邮件发送到密送电子邮件地址。 即使原始消息可能已发送，也会发送密送消息 [已退回](../reports/suppression-list.md#delivery-failures).

   <!--OR: Only successfully sent emails are taken in account. [Bounces](../reports/suppression-list.md#delivery-failures) are not. TO CHECK -->

* 请勿打开或点进发送到密件抄送地址的电子邮件，因为在总打开数和发送分析的点击量中，会考虑这些事件，这可能会导致 [报告](../reports/message-monitoring.md).

* 请勿在密件抄送收件箱中将邮件标记为垃圾邮件，因为这会影响发送到此地址的所有其他电子邮件。


>[!CAUTION]
>
>请勿在发送给密件抄送地址的电子邮件中单击取消订阅链接，因为您将立即取消订阅相应的收件人。

### GDPR合规 {#gdpr-compliance}

GDPR等法规规定，数据主体应能够随时修改其同意。 由于您随Journey Optimizer发送的密件抄送电子邮件包含安全的个人身份信息(PII)，因此您必须编辑 **[!UICONTROL CJM Email BCC Feedback Event Schema]** 以便能够按照GDPR及类似法规管理这些PII。

为此，请执行以下步骤：

1. 转到 **[!UICONTROL Data management]** > **[!UICONTROL Schemas]** > **[!UICONTROL Browse]** 选择 **[!UICONTROL CJM Email BCC Feedback Event Schema]**.

   ![](assets/preset-bcc-schema.png)

1. 单击可展开 **[!UICONTROL _experience]**, **[!UICONTROL customerJourneyManagment]** then **[!UICONTROL secondaryRecipientDetail]**.

1. 选择 **[!UICONTROL originalRecipientAddress]**。

1. 在 **[!UICONTROL Field properties]** 在右侧，向下滚动到 **[!UICONTROL Identity]** 复选框。

1. 选择它，然后选择 **[!UICONTROL Primary identity]**.

1. 从下拉列表中选择一个命名空间。

   ![](assets/preset-bcc-schema-identity.png)

1. 单击 **[!UICONTROL Apply]**。

>[!NOTE]
>
>在 [Experience Platform 文档](https://experienceleague.adobe.com/docs/experience-platform/privacy/home.html?lang=zh-Hans){target=&quot;_blank&quot;}中进一步了解管理隐私和适用的法规。

### 密送报表数据 {#bcc-reporting}

历程和消息报表中不提供密送的此类报告。 但是，信息存储在名为 **[!UICONTROL AJO BCC Feedback Event Dataset]**. 您可以对此数据集运行查询，以查找用于调试的有用信息，例如。

您可以通过用户界面访问此数据集。 选择 **[!UICONTROL Data management]** > **[!UICONTROL Datasets]** > **[!UICONTROL Browse]** 并启用 **[!UICONTROL Show system datasets]** 从筛选器中切换以显示系统生成的数据集。 了解有关如何访问 [此部分](../start/get-started-datasets.md#access-datasets).

![](assets/preset-bcc-dataset.png)

要对此数据集运行查询，您可以使用 [Adobe Experience Platform查询服务](https://experienceleague.adobe.com/docs/experience-platform/query/api/getting-started.html){target=&quot;_blank&quot;}。 要访问它，请选择 **[!UICONTROL Data management]** > **[!UICONTROL Queries]** 单击 **[!UICONTROL Create query]**. [了解详情](../start/get-started-queries.md)

![](assets/preset-bcc-queries.png)

根据要查找的信息，您可以运行以下查询。

1. 对于以下所有其他查询，您将需要历程操作ID。 运行此查询以获取在过去2天内与特定历程版本ID关联的所有操作ID:

       &quot;
       选择
       DISTINCT
       将时间戳转换为日期，
       _experience.journeyOrchestration.stepEvents.journeyVersionID，
       _experience.journeyOrchestration.stepEvents.actionName，
       _experience.journeyOrchestration.stepEvents.actionID
       FROM journey_step_events
       其中
       _experience.journeyOrchestration.stepEvents.journeyVersionID = &#39;&lt;journey version=&quot;&quot; id=&quot;&quot;>“和
       _experience.journeyOrchestration.stepEvents.actionID不为NULL且
       时间戳> NOW() — 时间间隔“2”天
       按事件时间DESC排序；
       &quot;
   
   >[!NOTE]
   >
   >要获取 `<journey version id>`参数，选择相应的 [历程版本](../building-journeys/journey-versions.md) 从 **[!UICONTROL Journey management]** > **[!UICONTROL Journeys]** 菜单。 历程版本ID显示在Web浏览器中显示的URL的末尾。
   >
   >![](assets/preset-bcc-action-id.png)

1. 运行此查询以获取在过去2天内为特定用户定向的特定消息生成的所有消息反馈事件（特别是反馈状态）：

       &quot;
       选择
       _experience.customerJourneyManagement.messageExecution.journeyVersionID作为JourneyVersionID，
       _experience.customerJourneyManagement.messageExecution.journeyActionID作为JourneyActionID，
       时间戳AS EventTime，
       _experience.customerJourneyManagement.emailChannelContext.address AS RecipientAddress，
       _experience.customerjourneymanagement.messagedeliveryfeedback.feedbackStatus AS FeedbackStatus，
       CASE _experience.customerjourneymanagement.messagedeliveryfeedback.feedbackStatus
       “已发送”时，然后“已发送”
       当为“delay”时，然后为“Retry”
       WHEN &#39;out_of_band&#39; THEN &#39;Bounce&#39;
       “跳出”后“跳出”
       END AS FeedbackStatusCategory
       从cjm_message_feedback_event_dataset
       其中
       timestamp > now() — 时间间隔“2”天和
       _experience.customerJourneyManagement.messageExecution.journeyVersionID = &#39;&lt;journey version=&quot;&quot; id=&quot;&quot;>“和
       _experience.customerJourneyManagement.messageExecution.journeyActionID = &#39;&lt;journey action=&quot;&quot; id=&quot;&quot;>“和
       _experience.customerJourneyManagement.emailChannelContext.address = &#39;&lt;recipient email=&quot;&quot; address=&quot;&quot;>&#39;
       按事件时间DESC排序；
       &quot;
   
   >[!NOTE]
   >
   >要获取 `<journey action id>` 参数，使用历程版本id运行上述第一个查询。 的 `<recipient email address>` 参数是目标或实际收件人的电子邮件地址。

1. 运行此查询以获取在过去2天内为特定用户定向的特定消息生成的所有密送消息反馈事件：

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

1. 运行此查询以获取所有未收到消息的收件人地址，而其密件抄送条目在最近30天内存在：

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

## 电子邮件重试参数 {#email-retry}

>[!CONTEXTUALHELP]
>id="ajo_admin_presets_retryperiod"
>title="调整重试时间段"
>abstract="当电子邮件由于临时软退件错误而失败时，将执行3.5天（84小时）的重试。 您可以调整此默认的重试时间段，以更好地满足您的需求。"
>additional-url="https://experienceleague.adobe.com/docs/journey-optimizer/using/configuration/configuration-message/email-configuration/monitor-reputation/retries.html" text="关于重试"

您可以配置 **电子邮件重试参数**.

![](assets/preset-retry-parameters.png)

默认情况下， [重试时段](retries.md#retry-duration) 设置为84小时，但您可以根据自己的需求调整此设置。

您必须在以下范围内输入整数值（以小时或分钟为单位）：

* 对于营销电子邮件，最短重试期限为6小时。
* 对于事务型电子邮件，最短重试期限为10分钟。
* 对于这两种电子邮件类型，最大重试时间段为84小时（或5040分钟）。

了解有关重试的更多信息(位于 [此部分](retries.md).

## URL跟踪 {#url-tracking}

>[!CONTEXTUALHELP]
>id="ajo_admin_preset_utm"
>title="URL跟踪参数"
>abstract="使用此部分可自动将跟踪参数附加到电子邮件内容中存在的促销活动URL。"

您可以使用 **[!UICONTROL URL Tracking Parameters]** 来衡量您跨渠道营销工作的有效性。 此功能属于可选功能。

此部分中定义的参数将附加到电子邮件内容中包含的URL的末尾。 然后，您可以在Web分析工具(如Adobe Analytics或Google Analytics)中捕获这些参数，并创建各种性能报表。

![](assets/preset-url-tracking.png)

例如，在创建消息预设时，会自动填充三个URL跟踪参数。 您可以编辑这些参数，并使用 **[!UICONTROL Add new parameter]** 按钮。

要配置URL跟踪参数，您可以直接在 **[!UICONTROL Name]** 和 **[!UICONTROL Value]** 字段，或通过导航到以下对象从预定义值列表中进行选择：

* 历程属性： **源ID**, **源名称**, **源版本ID**
* 操作属性： **操作ID**, **操作名称**
* Offer decisioning属性： **选件ID**, **选件名称**

![](assets/preset-url-tracking-source.png)

>[!CAUTION]
>
>请勿选择文件夹：确保浏览到必要的文件夹并选择要用作跟踪参数值的配置文件属性。

以下是与Adobe Analytics和Google Analytics兼容的URL的示例。

* Adobe Analytics兼容URL: `www.YourLandingURL.com?cid=email_AJO_{{context.system.source.id}}_image_{{context.system.source.name}}`

* Google Analytics兼容URL: `www.YourLandingURL.com?utm_medium=email&utm_source=AJO&utm_campaign={{context.system.source.id}}&utm_content=image`

>[!NOTE]
>
>您可以组合键入文本值和选择预定义值。 每个 **[!UICONTROL Value]** 字段最多可包含255个字符。
