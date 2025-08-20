---
solution: Journey Optimizer
product: journey optimizer
title: 配置短信渠道
description: 了解如何配置环境以使用Journey Optimizer发送短信
feature: SMS, Channel Configuration
role: Admin
level: Intermediate
exl-id: 4dcd22ed-bf7e-4789-ab7b-33544c857db8
source-git-commit: 37e86b2c9d7f1587fefa2927949a13cac24c34ad
workflow-type: tm+mt
source-wordcount: '411'
ht-degree: 34%

---

# 短信/彩信/RCS 配置快速入门 {#sms-configuration}

>[!CONTEXTUALHELP]
>id="ajo_admin_sms_api_header"
>title="用 Journey Optimizer 配置您的短信提供商"
>abstract="Adobe Journey Optimizer 通过短信服务提供商发送短信。选择提供商并填写 API 凭据。"

>[!CONTEXTUALHELP]
>id="ajo_admin_mms_api_header"
>title="用 Journey Optimizer 配置您的彩信提供商"
>abstract="Adobe Journey Optimizer 通过彩信服务提供商发送媒体内容。选择提供商并填写 API 凭据。"

>[!CONTEXTUALHELP]
>id="ajo_admin_sms_api"
>title="使用 Journey Optimizer 配置短信/多媒体短信供应商"
>abstract="在发送短信 (SMS/MMS) 之前，您必须将提供商设置与 Journey Optimizer 集成。完成后，您需要创建一个 SMS/MMS 配置。必须由 Adobe Journey Optimizer 系统管理员执行这些步骤。"
>additional-url="https://experienceleague.adobe.com/zh-hans/docs/journey-optimizer/using/channels/sms/configure-sms/sms-configuration-surface" text="创建短信渠道配置"

>[!CONTEXTUALHELP]
>id="ajo_admin_sms_configuration"
>title="选择短信供应商配置"
>abstract="选择为您的短信供应商配置的 API 凭据。"

>[!CONTEXTUALHELP]
>id="ajo_admin_fuzzy_opt_out"
>title="模糊选择退出"
>abstract="启用后，模糊选择退出会检测与定义的选择退出关键词（例如CANCIL）非常相似的入站消息，并自动发送确认回复以验证用户的取消订阅意图。 如果用户通过定义的提示进行确认，系统将执行取消订阅操作。"

在发送短信、彩信或RCS之前，必须配置Adobe Journey Optimizer环境。 要执行此操作，请执行以下操作：

1. 将提供程序设置与Journey Optimizer集成。
具体步骤取决于您的短信提供商。 浏览以下链接以访问详细文档：
   * [Infobip](sms-configuration-infobip.md)
   * [Sinch](sms-configuration-sinch.md)
   * [Twilio](sms-configuration-twilio.md)
   * [自定义提供商](sms-configuration-custom.md)
1. [创建短信配置](sms-configuration-surface.md)

这些步骤必须由Adobe Journey Optimizer [系统管理员](../start/path/administrator.md)执行。

## 先决条件{#sms-prerequisites}

Adobe Journey Optimizer目前与第三方提供商集成，这些提供商独立于Adobe Journey Optimizer提供短信服务。 支持短信和MMS的提供程序为： **Sinch**、**Twilio**&#x200B;和&#x200B;**Infobip**。 请注意，您可以使用[自定义提供程序配置](sms-configuration-custom.md)配置其他消息提供程序。

在配置SMS渠道之前，您必须与这些提供商之一创建帐户以获取您的&#x200B;**API令牌**&#x200B;和&#x200B;**服务ID**，您需要配置这些Adobe Journey Optimizer与适用提供商之间的连接。

您对短信和MMS服务的使用受适用提供商提供的其他条款和条件的约束。 作为第三方解决方案，Adobe Journey Optimizer用户可通过集成使用Sinch、Twilio和Infobip。 Adobe不控制，也不负责第三方产品。 有关文本消息服务(SMS/MMS)的任何问题或协助请求，请与提供商联系。

>[!CAUTION]
>
>要访问和编辑SMS子域，您必须对生产沙盒具有&#x200B;**[!UICONTROL 管理SMS子域]**&#x200B;权限。 在[此页面](../administration/high-low-permissions.md#administration-permissions)上了解有关权限的详细信息。
>

