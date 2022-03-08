---
title: 允许列表
description: 了解如何使用允许列表。
feature: Deliverability
topic: Content Management
role: User
level: Intermediate
exl-id: 70ab8f57-c132-4de1-847b-11f0ab14f422
source-git-commit: 882b99d9b49e1ae6d0f97872a74dc5a8a4639050
workflow-type: tm+mt
source-wordcount: '583'
ht-degree: 4%

---

# 允许列表 {#allow-list}

现在，可以在 [沙盒](../administration/sandboxes.md) 级别，以便拥有安全的环境进行测试。 在可能出现错误的非生产实例上，允许列表可确保不会出现向客户发送不必要消息的风险。

利用允许列表，可指定单独的电子邮件地址或域，这些地址或域将是唯一有权接收您从特定沙盒发送的电子邮件的收件人或域。 这样可以防止您在测试环境中意外地向实际的客户地址发送电子邮件。

>[!CAUTION]
>
>此功能为 **not** 可在生产沙箱中使用。 它仅适用于电子邮件渠道。

## 启用允许列表 {#enable-allow-list}

要在非生产沙盒上启用允许列表，您需要使用消息预设服务中的相应API端点更新常规设置。

* 使用此API，您还可以随时禁用该功能。

* 您可以在启用该功能之前或之后更新允许列表。

* 允许列表逻辑在启用该功能时应用 **和** 如果允许列表为 **not** 空。 在 [此部分](#logic).

<!--To enable this feature on a non-production sandbox, update the allowed list so that it is no longer empty. To disable it, clear up the allowed list so that it is again empty.

Learn more on the allowed list logic in this section.
-->

>[!NOTE]
>
>启用后，在执行允许列表时，以及通过测试消息时，都会使用“测试”功能 [校样](preview.md#send-proofs) 和使用 [测试模式](../building-journeys/testing-the-journey.md).

## 将实体添加到允许列表 {#add-entities}

要向特定沙盒的允许列表添加新的电子邮件地址或域，必须使用 `ALLOWED` 值 `listType` 属性。 例如：

![](assets/allow-list-api.png)

您可以执行 **添加**, **删除** 和 **获取** 操作。

>[!NOTE]
>
>允许列表最多可包含1,000个条目。

进一步了解如何在 [Adobe Experience Platform API](https://experienceleague.adobe.com/docs/experience-platform/landing/platform-apis/api-guide.html){target=&quot;_blank&quot;}引用文档。

## 允许列表逻辑 {#logic}

允许列表为 **空**，则不会应用允许列表逻辑。 这意味着，您可以向任何用户档案发送电子邮件，前提是这些用户档案不在 [抑制列表](suppression-list.md).

允许列表为 **不为空**，则会应用允许列表逻辑：

* 如果实体为 **不在允许列表上**，且不在抑制列表中，相应的收件人将不会收到电子邮件，原因是 **[!UICONTROL Not allowed]**.

* 如果实体为 **允许列表**，而不是在抑制列表中，则可以将电子邮件发送给相应的收件人。 但是，如果实体 [抑制列表](suppression-list.md)，相应的收件人将不会收到电子邮件，原因是 **[!UICONTROL Suppressed]**.

>[!NOTE]
>
>具有 **[!UICONTROL Not allowed]** 在消息发送过程中，状态将被排除。 因此，当 **历程报表** 会将这些用户档案显示为已在历程([读取区段](../building-journeys/read-segment.md) 和 [消息](../building-journeys/journeys-message.md) ) **电子邮件报表** 将不会在 **[!UICONTROL Sent]** 量度，因为在发送电子邮件之前，这些量度会被过滤掉。
>
>了解 [实时报表](../reports/live-report.md) 和 [全局报告](../reports/global-report.md).

## 排除项报告 {#reporting}

在非生产沙盒上启用此功能后，您可以检索从发送中排除的电子邮件地址或域，因为这些地址或域不在允许列表上。 为此，您可以使用 [Adobe Experience Platform查询服务](https://experienceleague.adobe.com/docs/experience-platform/query/api/getting-started.html){target=&quot;_blank&quot;}进行下面的API调用。

要获取 **电子邮件数量** 收件人不在允许列表上而未发送的收件人，请使用以下查询：

```sql
SELECT count(distinct _id) from cjm_message_feedback_event_dataset WHERE
_experience.customerJourneyManagement.messageExecution.messageExecutionID = '<MESSAGE_EXECUTION_ID>' AND
_experience.customerJourneyManagement.messageDeliveryfeedback.feedbackStatus = 'exclude' AND
_experience.customerJourneyManagement.messageDeliveryfeedback.messageExclusion.reason = 'EmailNotAllowed'
```

要获取 **电子邮件地址列表** 收件人不在允许列表上而未发送的收件人，请使用以下查询：

```sql
SELECT distinct(_experience.customerJourneyManagement.emailChannelContext.address) from cjm_message_feedback_event_dataset WHERE
_experience.customerJourneyManagement.messageExecution.messageExecutionID IS NOT NULL AND
_experience.customerJourneyManagement.messageDeliveryfeedback.feedbackStatus = 'exclude' AND
_experience.customerJourneyManagement.messageDeliveryfeedback.messageExclusion.reason = 'EmailNotAllowed'
```
