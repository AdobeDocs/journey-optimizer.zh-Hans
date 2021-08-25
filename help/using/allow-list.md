---
title: 允许列表
description: 了解如何使用允许列表。
feature: Deliverability
topic: Content Management
role: User
level: Intermediate
source-git-commit: 9408a93deecfb12f28a0a87c19fa0074c66844a9
workflow-type: tm+mt
source-wordcount: '560'
ht-degree: 0%

---

# 允许列表 {#allow-list}

现在，可以在[sandbox](administration/sandboxes.md)级别定义特定的发送安全列表，以便具有用于测试的安全环境。 在可能出现错误的非生产实例上，允许列表可确保您没有向客户发送不需要的消息的风险。

利用允许列表，可指定单独的电子邮件地址或域，这些地址或域将是唯一有权接收您从特定沙盒发送的电子邮件的收件人或域。 这样可以防止您在测试环境中意外地向实际的客户地址发送电子邮件。

>[!CAUTION]
>
>此功能在生产沙箱上可用，为&#x200B;**不**。 它仅适用于电子邮件渠道。

## 启用允许列表 {#enable-allow-list}

要在非生产沙盒上启用允许列表，您需要使用消息预设服务中的相应API端点更新常规设置。

* 使用此API，您还可以随时禁用该功能。

* 您可以在启用该功能之前或之后更新允许列表。

* 如果允许列表为&#x200B;**不**&#x200B;空，则在启用&#x200B;**和**&#x200B;功能时应用允许列表逻辑。 在[此部分](#logic)中了解详情。

<!--To enable this feature on a non-production sandbox, update the allowed list so that it is no longer empty. To disable it, clear up the allowed list so that it is again empty.

Learn more on the allowed list logic in this section.
-->

>[!NOTE]
>
>启用后，在执行历程时，以及在使用[校样](preview.md#send-proofs)测试消息和使用[测试模式](building-journeys/testing-the-journey.md)测试历程时，都将使用允许列表功能。

## 将实体添加到允许列表 {#add-entities}

要向特定沙盒的允许列表添加新的电子邮件地址或域，必须使用`listType`属性的`ALLOWED`值调用抑制API。 例如：

![](assets/allow-list-api.png)

您可以执行&#x200B;**Add**、**Delete**&#x200B;和&#x200B;**Get**&#x200B;操作。

>[!NOTE]
>
>允许列表最多可包含1,000个条目。

<!--
Learn more on making these API calls in the API reference documentation.
Found this link in Experience Platform documentation, but may not be the final one: (https://experienceleague.adobe.com/docs/experience-platform/landing/platform-apis/api-guide.html?lang=en).-->

## 允许列表逻辑 {#logic}

<!-- When the allowed list is enabled (enable-allow-list) at the sandbox level using the API call above, the following applies.-->

当允许列表为&#x200B;**empty**&#x200B;时，不应用允许列表逻辑。 这表示您可以向任何用户档案发送电子邮件，前提是这些用户档案未列在[抑制列表](suppression-list.md)中。

当允许列表为&#x200B;**不为空**&#x200B;时，将应用允许列表逻辑：

* 如果实体&#x200B;**不在允许列表**&#x200B;上，并且不在禁止列表上，则相应的收件人将不会收到电子邮件，原因是&#x200B;**[!UICONTROL Not allowed]**。

* 如果允许列表&#x200B;**上的实体是**，而不是禁止列表上的实体，则可以向相应的收件人发送电子邮件。 但是，如果实体也位于[抑制列表](suppression-list.md)中，则相应的收件人将不会收到电子邮件，原因为&#x200B;**[!UICONTROL Suppressed]**。

>[!NOTE]
>
>在消息发送过程中，将排除状态为&#x200B;**[!UICONTROL Not allowed]**&#x200B;的用户档案。 因此，虽然&#x200B;**历程报表**&#x200B;会将这些用户档案显示为已在历程（[读取区段](building-journeys/read-segment.md)和[消息](building-journeys/journeys-message.md)活动）中移动，但&#x200B;**电子邮件报表**&#x200B;不会在&#x200B;**[!UICONTROL Sent]**&#x200B;量度中包含这些用户档案，因为在发送电子邮件之前已将它们过滤掉。
>
>了解有关[实时报表](reports/live-report.md)和[全局报表](reports/global-report.md)的更多信息。

## 排除项报告 {#reporting}

在非生产沙盒上启用此功能后，您可以检索从发送中排除的电子邮件地址或域，因为这些地址或域不在允许列表上。 要实现此目的，您可以使用[Adobe Experience Platform查询服务](https://experienceleague.adobe.com/docs/experience-platform/query/api/getting-started.html){target=&quot;_blank&quot;}进行下面的API调用。

要获取因收件人不在允许列表上而未发送的&#x200B;**电子邮件数**，请使用以下查询：

```
SELECT count(distinct _id) from cjm_message_feedback_event_dataset WHERE
_experience.customerJourneyManagement.messageExecution.messageExecutionID = '<MESSAGE_EXECUTION_ID>' AND
_experience.customerJourneyManagement.messageDeliveryfeedback.feedbackStatus = 'exclude' AND
_experience.customerJourneyManagement.messageDeliveryfeedback.messageExclusion.reason = 'EmailNotAllowed'
```

要获取因收件人不在允许列表上而未发送的&#x200B;**电子邮件地址列表**，请使用以下查询：

```
SELECT distinct(_experience.customerJourneyManagement.emailChannelContext.address) from cjm_message_feedback_event_dataset WHERE
_experience.customerJourneyManagement.messageExecution.messageExecutionID IS NOT NULL AND
_experience.customerJourneyManagement.messageDeliveryfeedback.feedbackStatus = 'exclude' AND
_experience.customerJourneyManagement.messageDeliveryfeedback.messageExclusion.reason = 'EmailNotAllowed'
```

