---
solution: Journey Optimizer
product: journey optimizer
title: 允许的列表
description: 了解如何使用允许的列表
feature: Deliverability
topic: Content Management
role: User
level: Intermediate
exl-id: 70ab8f57-c132-4de1-847b-11f0ab14f422
source-git-commit: 020c4fb18cbd0c10a6eb92865f7f0457e5db8bc0
workflow-type: tm+mt
source-wordcount: '976'
ht-degree: 0%

---

# 允许的列表 {#allow-list}

可以在 [沙盒](../administration/sandboxes.md) 级别。

此允许列表允许您指定单个电子邮件地址或域，这些地址或域将是唯一有权接收您从特定沙盒发送的电子邮件的收件人或域。

>[!NOTE]
>
>此功能适用于生产沙箱和非生产沙箱。

例如，在可能发生错误的非生产实例上，允许的列表确保您没有向真实客户地址发送不需要的消息的风险，从而为测试提供安全的环境。

此外，如果允许的列表处于活动状态但为空，则不会发出任何邮件。 因此，如果您遇到一些主要问题，可以使用此功能阻止所有来自 [!DNL Journey Optimizer] 直到你解决问题。 了解 [允许列表逻辑](#logic).

>[!CAUTION]
>
>此功能仅适用于电子邮件渠道。

## 访问允许的列表 {#access-allowed-list}

要访问允许的电子邮件地址和域的详细列表，请转到 **[!UICONTROL Administration]** > **[!UICONTROL Channels]** > **[!UICONTROL Email configuration]**，然后选择 **[!UICONTROL Allowed list]**.

![](assets/allow-list-access.png)

>[!CAUTION]
>
>查看、导出和管理允许列表的权限限制为 [历程管理员](../administration/ootb-product-profiles.md#journey-administrator). 了解有关管理的更多信息 [!DNL Journey Optimizer] 用户在 [此部分](../administration/permissions-overview.md).

要将允许的列表导出为CSV文件，请选择 **[!UICONTROL Download CSV]** 按钮。

使用 **[!UICONTROL Delete]** 按钮以永久删除条目。

您可以搜索电子邮件地址或域，并在 **[!UICONTROL Address type]**. 选择后，您可以清除列表顶部显示的过滤器。

![](assets/allowed-list-filtering-example.png)

## 激活允许的列表 {#enable-allow-list}

要激活允许的列表，请执行以下步骤。

1. 访问  **[!UICONTROL Channels]** > **[!UICONTROL Email configuration]** > **[!UICONTROL Allow list]** 菜单。

1. 选择切换按钮。

   ![](assets/allow-list-edit.png)

1. 选择 **[!UICONTROL Activate allowed list]**. 允许的列表现在处于活动状态。

   ![](assets/allow-list-enable.png)

   >[!NOTE]
   >
   >激活允许的列表后，该列表会在您的历程和营销活动中有5分钟的延迟。

当功能处于活动状态时，允许的列表逻辑即适用。 在 [此部分](#logic).

>[!NOTE]
>
>激活后，执行历程时，以及通过测试消息时，都会使用允许的列表功能 [校样](../email/preview.md#send-proofs) 和使用 [测试模式](../building-journeys/testing-the-journey.md).

## 停用允许的列表 {#deactivate-allow-list}

要停用允许的列表，请执行以下步骤。

1. 访问  **[!UICONTROL Channels]** > **[!UICONTROL Email configuration]** > **[!UICONTROL Allow list]** 菜单。

1. 选择切换按钮。

   ![](assets/allow-list-edit-active.png)

1. 选择 **[!UICONTROL Deactivate allowed list]**. 允许的列表不再处于活动状态。

   ![](assets/allow-list-deactivate.png)

   >[!NOTE]
   >
   >停用允许的列表后，会有5分钟的延迟，以便该列表在您的历程和营销活动中生效。

停用该功能后，将不应用允许的列表逻辑。 在 [此部分](#logic).

## 将实体添加到允许的列表 {#add-entities}

要向特定沙盒的允许列表添加新电子邮件地址或域，您可以 [手动填充列表](#manually-populate-list)，或使用 [API调用](#api-call-allowed-list).

>[!NOTE]
>
>允许的列表最多可包含1,000个条目。

### 手动填充允许的列表 {#manually-populate-list}

>[!CONTEXTUALHELP]
>id="ajo_admin_allowed_list_add_header"
>title="将地址或域添加到允许的列表"
>abstract="您可以通过逐个选择新电子邮件地址或域来手动将其添加到允许列表中。"

>[!CONTEXTUALHELP]
>id="ajo_admin_allowed_list_add"
>title="将地址或域添加到允许的列表"
>abstract="您可以通过逐个选择新电子邮件地址或域来手动将其添加到允许列表中。"

您可以手动填充 [!DNL Journey Optimizer] 允许的列表。

>[!NOTE]
>
>一次只能添加一个电子邮件地址或域。

为此，请执行以下步骤。

1. 选择 **[!UICONTROL Add email or domain]** 按钮。

   ![](assets/allowed-list-add-email.png)

1. 选择地址类型： **[!UICONTROL Email address]** 或 **[!UICONTROL Domain address]**.

1. 输入要向其发送电子邮件的电子邮件地址或域。

   >[!NOTE]
   >
   >确保输入有效的电子邮件地址(如abc@company.com)或域名(如abc.company.com)。

1. 根据需要指定原因。

   ![](assets/allowed-list-add-email-address.png)

   >[!NOTE]
   >
   >在 **[!UICONTROL Reason]** 字段。 完整列表可在 [本页](https://en.wikipedia.org/wiki/Wikipedia:ASCII#ASCII_printable_characters)例如，{target=&quot;_blank&quot;}。

1. 单击 **[!UICONTROL Submit]**.

### 使用API调用添加实体 {#api-call-allowed-list}

要填充允许的列表，您还可以使用 `ALLOWED` 值 `listType` 属性。 例如：

![](assets/allow-list-api.png)

您可以执行 **添加**, **删除** 和 **获取** 操作。

进一步了解如何在 [Adobe Experience Platform API](https://experienceleague.adobe.com/docs/experience-platform/landing/platform-apis/api-guide.html){target=&quot;_blank&quot;}引用文档。

## 允许的列表逻辑 {#logic}

>[!CONTEXTUALHELP]
>id="ajo_admin_allowed_list_logic"
>title="管理允许的列表"
>abstract="激活允许列表后，只有允许列表中包含的收件人才会收到来自此沙盒的电子邮件。 停用后，所有收件人都将收到电子邮件。"

允许的列表为 [活动](#enable-allow-list)，则以下逻辑适用：

* 如果允许的列表为 **空**，则不会发送任何电子邮件。

* 如果实体为 **在允许的列表上**，而不是在抑制列表中，则会将电子邮件发送给相应的收件人。 但是，如果实体 [抑制列表](../reports/suppression-list.md)，相应的收件人将不会收到电子邮件，原因是 **[!UICONTROL Suppressed]**.

* 如果实体为 **不在允许的列表上** （且不在禁止列表中），相应的收件人将不会收到电子邮件，原因是 **[!UICONTROL Not allowed]**.

>[!NOTE]
>
>具有 **[!UICONTROL Not allowed]** 在消息发送过程中，状态将被排除。 因此，当 **历程报告** 会将这些用户档案显示为已在历程([读取区段](../building-journeys/read-segment.md) 和 [消息活动](../building-journeys/journeys-message.md))、 **电子邮件报表** 将不会在 **[!UICONTROL Sent]** 量度，因为在发送电子邮件之前，这些量度会被过滤掉。
>
>了解 [实时报表](../reports/live-report.md) 和 [全局报告](../reports/global-report.md).

允许的列表为 [停用](#deactivate-allow-list)，则您从当前沙盒发送的所有电子邮件都会发送给所有收件人（前提是这些收件人不在禁止列表中），包括真实的客户地址。

## 排除项报告 {#reporting}

当允许的列表处于活动状态时，您可以检索电子邮件地址或从发送中排除的域，因为这些地址或域不在允许的列表中。 为此，您可以使用 [Adobe Experience Platform查询服务](https://experienceleague.adobe.com/docs/experience-platform/query/api/getting-started.html){target=&quot;_blank&quot;}进行下面的API调用。

要获取 **电子邮件数量** 收件人不在允许列表中而未发送的收件人，请使用以下查询：

```sql
SELECT count(distinct _id) from cjm_message_feedback_event_dataset WHERE
_experience.customerJourneyManagement.messageExecution.messageExecutionID = '<MESSAGE_EXECUTION_ID>' AND
_experience.customerJourneyManagement.messageDeliveryfeedback.feedbackStatus = 'exclude' AND
_experience.customerJourneyManagement.messageDeliveryfeedback.messageExclusion.reason = 'EmailNotAllowed'
```

要获取 **电子邮件地址列表** 收件人不在允许列表中而未发送的收件人，请使用以下查询：

```sql
SELECT distinct(_experience.customerJourneyManagement.emailChannelContext.address) from cjm_message_feedback_event_dataset WHERE
_experience.customerJourneyManagement.messageExecution.messageExecutionID IS NOT NULL AND
_experience.customerJourneyManagement.messageDeliveryfeedback.feedbackStatus = 'exclude' AND
_experience.customerJourneyManagement.messageDeliveryfeedback.messageExclusion.reason = 'EmailNotAllowed'
```
