---
title: 允许列表
description: 了解如何使用允许列表。
feature: 可投放性
topic: 内容管理
role: User
level: Intermediate
source-git-commit: 288c27d4fc64a6d0a6f07b634ed044a6e858d0c1
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---

# 允许列表 {#allow-list}

现在，可以在[sandbox](administration/sandboxes.md)级别定义特定的发送安全列表，以便具有用于测试的安全环境。 在可能出现错误的非生产实例上，允许列表可确保您没有向客户发送不需要的消息的风险。

>[!CAUTION]
>
>此功能在生产沙箱中不可用。

利用允许列表，可指定单独的电子邮件地址或域，这些地址或域将是唯一有权接收您从特定沙盒发送的电子邮件的收件人或域。 这样可以防止您在测试环境中意外地向实际的客户地址发送电子邮件。

>[!NOTE]
>
>此功能仅适用于电子邮件渠道。

## 启用允许列表 {#enable-allow-list}

要在非生产沙盒上启用允许列表，您需要发起AdobeAPI调用。

* 使用此API，您还可以随时禁用该功能。

* 您可以在启用该功能之前或之后更新允许列表。

* 允许列表逻辑在启用功能且允许列表不为空时应用。 在[此部分](#logic)中了解详情。

>[!NOTE]
>
>启用后，在执行历程时，以及在使用[校样](preview.md#send-proofs)测试消息和使用[测试模式](building-journeys/testing-the-journey.md)测试历程时，都将使用允许列表功能。

## 将实体添加到允许列表 {#add-entities}

>[!CAUTION]
>
>此功能在生产沙箱上可用，为&#x200B;**不**。 它仅适用于电子邮件渠道。

要向特定沙盒的允许列表添加新的电子邮件地址或域，必须使用`listType`属性的`ALLOWED`值调用抑制API。 例如：

![](assets/allow-list-api.png)

您可以执行&#x200B;**Add**、**Delete**&#x200B;和&#x200B;**Get**&#x200B;操作。

>[!NOTE]
>
>允许列表最多可包含1,000个条目。

在[Adobe文档](https://experienceleague.adobe.com/docs/experience-platform/landing/platform-apis/api-guide.html?lang=en)中了解有关进行Experience PlatformAPI调用的更多信息。

## 允许列表逻辑 {#logic}

<!-- When the allowed list is \[enabled\]\(\add link here\) at the sandbox level using the API call above, the following applies.-->

1. 当允许列表为&#x200B;**empty**&#x200B;时，不应用允许列表逻辑。 这表示您可以向任何用户档案发送电子邮件，前提是这些用户档案未列在[抑制列表](suppression-list.md)中。

1. 当允许列表为&#x200B;**不为空**&#x200B;时，将应用允许列表逻辑：

   * 如果实体&#x200B;**不在允许列表**&#x200B;上，并且不在禁止列表上，则相应的收件人将不会收到电子邮件，原因是&#x200B;**[!UICONTROL Not allowed]**。

   * 如果允许列表&#x200B;**上的实体是**，而不是禁止列表上的实体，则可以向相应的收件人发送电子邮件。 但是，如果实体也位于[抑制列表](suppression-list.md)中，则相应的收件人将不会收到电子邮件，原因为&#x200B;**[!UICONTROL Suppressed]**。




