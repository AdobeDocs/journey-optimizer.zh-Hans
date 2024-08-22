---
solution: Journey Optimizer
product: journey optimizer
title: 配置短信渠道
description: 了解如何配置环境以使用Journey Optimizer发送短信
feature: SMS, Channel Configuration
role: Admin
level: Intermediate
exl-id: 4dcd22ed-bf7e-4789-ab7b-33544c857db8
source-git-commit: b9208544b08b474db386cce3d4fab0a4429a5f54
workflow-type: tm+mt
source-wordcount: '345'
ht-degree: 33%

---

# 短信配置入门 {#sms-configuration}

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
>title="使用 Journey Optimizer 配置 SMS/MMS 供应商"
>abstract="在发送短信 (SMS/MMS) 之前，您必须将提供商设置与 Journey Optimizer 集成。完成后，您需要创建短信/彩信配置。 必须由 Adobe Journey Optimizer 系统管理员执行这些步骤。"
>additional-url="https://experienceleague.adobe.com/zh-hans/docs/journey-optimizer/using/sms/configure-sms/sms-configuration-surface" text="创建短信渠道配置"

>[!CONTEXTUALHELP]
>id="ajo_admin_sms_configuration"
>title="选择短信供应商配置"
>abstract="选择为您的短信供应商配置的 API 凭据。"

在发送短信或彩信之前，必须配置Adobe Journey Optimizer环境。 要执行此操作，请执行以下操作：

1. 将提供程序设置与Journey Optimizer集成：
   * [带有Sinch](sms-configuration-sinch.md)
   * [使用Infobip](sms-configuration-infobip.md)
   * [使用自定义提供商](sms-configuration-custom.md)
1. [创建短信表面](sms-configuration-surface.md)

这些步骤必须由Adobe Journey Optimizer [系统管理员](../start/path/administrator.md)执行。

## 先决条件{#sms-prerequisites}

Adobe Journey Optimizer目前与第三方提供商集成，这些提供商独立于Adobe Journey Optimizer提供短信服务。 支持短信和MMS的提供程序为： **Sinch**、**Twilio**&#x200B;和&#x200B;**Infobip**。

在配置SMS渠道之前，您必须与这些提供商之一创建帐户以获取您的&#x200B;**API令牌**&#x200B;和&#x200B;**服务ID**，您需要配置这些Adobe Journey Optimizer与适用提供商之间的连接。

您对短信和MMS服务的使用受适用提供商提供的其他条款和条件的约束。 作为第三方解决方案，Adobe Journey Optimizer用户可通过集成使用Sinch、Twilio和Infobip。 Adobe不控制，也不对第三方产品负责。 有关文本消息服务(SMS/MMS)的任何问题或协助请求，请与提供商联系。

>[!CAUTION]
>
>要访问和编辑SMS子域，您必须对生产沙盒具有&#x200B;**[!UICONTROL 管理SMS子域]**&#x200B;权限。 可在[此页面](../administration/high-low-permissions.md#administration-permissions)中详细了解权限。
>

