---
solution: Journey Optimizer
product: journey optimizer
title: 配置短信渠道
description: 了解如何配置环境以使用Journey Optimizer发送移动消息
feature: SMS, Channel Configuration
role: Admin
level: Intermediate
exl-id: 4dcd22ed-bf7e-4789-ab7b-33544c857db8
TQID: https://experienceleague.adobe.com/dO8HoRdGLuYVFN2YVjRCiFJQHmWHApROU8qz2-hKmTs
product_v2: id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2: id: d0a62d3c-b79e-47e4-929e-40ef3cffa037
subfeature_v2: id: e30b0a1a-b594-47b8-af94-1e3a2be6df11id: b3b09fe1-10f1-4793-9f6b-1ca0269eebe7id: cf64c7f6-7428-4ae5-b158-8df9771f38f4
role_v2: id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
level_v2: id: b5a62a22-46f7-4f0d-b151-3fc640bef588
topic_v2: id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: 4c82775044b5a0a3a48920f59b0afb8a3c6a6d80
workflow-type: tm+mt
source-wordcount: 456
ht-degree: 40%

---

# 开始配置移动设备消息 {#sms-configuration}

>[!BEGINSHADEBOX]

**在此页面上：**&#x200B;了解如何通过集成Sinch、Twilio或Infobip等提供商、创建webhook并设置移动配置，将Adobe Journey Optimizer环境配置为发送SMS、MMS和RCS消息。

>[!ENDSHADEBOX]

>[!CONTEXTUALHELP]
>id="ajo_admin_sms_api_header"
>title="用 Journey Optimizer 配置您的短信提供商"
>abstract="Adobe Journey Optimizer 通过 SMS 服务提供商发送移动设备消息。 选择提供商并填写 API 凭据。"

>[!CONTEXTUALHELP]
>id="ajo_admin_mms_api_header"
>title="用 Journey Optimizer 配置您的彩信提供商"
>abstract="Adobe Journey Optimizer 通过彩信服务提供商发送媒体内容。 选择提供商并填写 API 凭据。"

>[!CONTEXTUALHELP]
>id="ajo_admin_sms_api"
>title="使用 Journey Optimizer 配置您的 SMS/RCS/MMS 提供商"
>abstract="在发送移动设备消息（SMS/RCS/MMS）之前，您必须将提供商设置与 Journey Optimizer 集成。 完成后，您需要创建 SMS/RCS/MMS 配置。 必须由 Adobe Journey Optimizer 系统管理员执行这些步骤。"
>additional-url="https://experienceleague.adobe.com/zh-hans/docs/journey-optimizer/using/channels/sms/configure-sms/sms-configuration-surface" text="创建短信渠道配置"

>[!CONTEXTUALHELP]
>id="ajo_admin_sms_configuration"
>title="选择短信供应商配置"
>abstract="选择为您的短信供应商配置的 API 凭据。"

>[!CONTEXTUALHELP]
>id="ajo_admin_fuzzy_opt_out"
>title="模糊选择退出"
>abstract="启用模糊选择退出后，会检测与已定义的退出关键词（如“CANCIL”）非常相似的入站消息，并会自动发送一条确认回复，以验证用户是否要取消订阅。 如果用户通过定义的提示进行确认，系统将执行取消订阅操作。"

在发送短信、彩信或RCS之前，必须配置Adobe Journey Optimizer环境。 要执行此操作，请执行以下操作：

1. 将提供程序设置与Journey Optimizer集成。
具体步骤取决于您的短信提供商。浏览以下链接以访问详细文档：
   * [Infobip](mobile-configuration-infobip.md)
   * [Sinch](mobile-configuration-sinch.md)
   * [Twilio](mobile-configuration-twilio.md)
   * [自定义提供商](mobile-configuration-custom.md)
1. [创建 Webhook](mobile-webhook.md)
1. [创建移动设备配置](mobile-configuration-surface.md)

这些步骤必须由Adobe Journey Optimizer [系统管理员](../start/path/administrator.md)执行。

## 先决条件{#sms-prerequisites}

Adobe Journey Optimizer目前与提供独立于Adobe Journey Optimizer的移动消息服务的第三方提供商集成。 移动消息和MMS支持的提供商为：**Sinch**、**Twilio**&#x200B;和&#x200B;**Infobip**。 请注意，您可以使用[自定义提供程序配置](mobile-configuration-custom.md)配置其他消息提供程序。

在配置移动渠道之前，您必须与这些提供商之一创建帐户以获取您的&#x200B;**API令牌**&#x200B;和&#x200B;**服务ID**，您需要配置这两个提供商之间的Adobe Journey Optimizer连接。

您对Mobile Messaging和MMS服务的使用受适用提供商提供的其他条款和条件的约束。 作为第三方解决方案，Adobe Journey Optimizer用户可通过集成使用Sinch、Twilio和Infobip。 Adobe不控制，也不负责第三方产品。 如有任何与Mobile Messaging Services相关的问题或协助请求，请与提供商联系。

>[!CAUTION]
>
>要访问和编辑SMS子域，您必须对生产沙盒具有&#x200B;**[!UICONTROL 管理SMS子域]**&#x200B;权限。 在[此页面](../administration/high-low-permissions.md#administration-permissions)上了解有关权限的详细信息。
>

