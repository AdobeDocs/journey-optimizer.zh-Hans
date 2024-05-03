---
solution: Journey Optimizer
product: journey optimizer
title: 配置短信渠道
description: 了解如何配置环境以使用Journey Optimizer发送短信
feature: SMS, Channel Configuration
role: Admin
level: Intermediate
exl-id: 4dcd22ed-bf7e-4789-ab7b-33544c857db8
source-git-commit: 016b823161b162cb00e0eae27cd45873752425ba
workflow-type: tm+mt
source-wordcount: '343'
ht-degree: 36%

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
>abstract="在发送短信 (SMS/MMS) 之前，您必须将提供商设置与 Journey Optimizer 集成。完成后，您需要创建一个 SMS/MMS 表面。必须由 Adobe Journey Optimizer 系统管理员执行这些步骤。"
>additional-url="https://experienceleague.adobe.com/en/docs/journey-optimizer/using/sms/configure-sms/sms-configuration-surface" text="创建短信渠道表面"

>[!CONTEXTUALHELP]
>id="ajo_admin_sms_configuration"
>title="选择短信供应商配置"
>abstract="选择为您的短信供应商配置的 API 凭据。"

在发送短信或彩信之前，必须配置Adobe Journey Optimizer环境。 要执行此操作，请执行以下操作：

1. 将提供程序设置与Journey Optimizer集成：
   * [带有Sinch](sms-configuration-sinch.md)
   * [使用Infobip](sms-configuration-infobip.md)
   * [与Twilio](sms-configuration-twilio.md)
1. [创建短信表面](#message-preset-sms)

这些步骤必须由Adobe Journey Optimizer执行 [系统管理员](../start/path/administrator.md).

## 先决条件{#sms-prerequisites}

Adobe Journey Optimizer目前与第三方提供商集成，这些提供商独立于Adobe Journey Optimizer提供短信服务。 支持短信和MMS的提供商包括： **Sinch**， **Twilio** 和 **Infobip**.

在配置短信渠道之前，您必须使用这些提供商之一创建帐户，以获取 **api令牌** 和 **服务ID**，您需要配置Adobe Journey Optimizer与适用提供商之间的连接。

您对短信和MMS服务的使用受适用提供商提供的其他条款和条件的约束。 作为第三方解决方案，Adobe Journey Optimizer用户可通过集成使用Sinch、Twilio和Infobip。 Adobe不控制，也不对第三方产品负责。 有关文本消息服务(SMS/MMS)的任何问题或协助请求，请与提供商联系。

>[!CAUTION]
>
>要访问和编辑短信子域，您必须拥有 **[!UICONTROL 管理短信子域]** 生产沙盒的权限。 可在[此页面](../administration/high-low-permissions.md#administration-permissions)中详细了解权限。
>

