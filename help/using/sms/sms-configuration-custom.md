---
solution: Journey Optimizer
product: journey optimizer
title: 配置您的自定义提供商
description: 了解如何配置您的环境，以通过自定义提供商使用Journey Optimizer发送短信
feature: SMS, Channel Configuration
badge: label="Beta 版" type="Informative"
role: Admin
level: Intermediate
exl-id: fd713864-96b9-4687-91bd-84e3533273ff
source-git-commit: 201d7d367540f7b36f27ca4a09b6f0ce12e3e22f
workflow-type: tm+mt
source-wordcount: '376'
ht-degree: 27%

---

# 配置自定义提供程序 {#sms-configuration-custom}

>[!CONTEXTUALHELP]
>id="ajo_admin_sms_api_byop_provider_url"
>title="提供程序 URL"
>abstract="指定您计划连接的外部 API 的 URL。此 URL 是访问 API 的特性和功能的端点。"

>[!CONTEXTUALHELP]
>id="ajo_admin_sms_api_byop_auth_type"
>title="身份验证类型"
>abstract="指定访问 API 所需的身份验证方法，例如 OAuth 或 Bearer 令牌。这确保了与外部服务的安全且经过授权的通信。"

>[!CONTEXTUALHELP]
>id="ajo_admin_sms_api_byop_header_parameters"
>title="标头参数"
>abstract="指定附加标头的标签、类型和值，以启用正确的身份验证、内容格式和有效的 API 通信。 "

>[!CONTEXTUALHELP]
>id="ajo_admin_sms_api_byop_provider_payload"
>title="提供程序负载"
>abstract="提供请求负载以确保发送正确的数据以供处理和生成响应。"

>[!AVAILABILITY]
>
>自定义提供商目前仅作为测试版提供给选定用户。 请联系您的Adobe代表以将其纳入Beta。
>
>请注意，此Beta不支持用于选择启用/选择禁用同意管理和投放报告的入站消息。

要在Journey Optimizer中使用Adobe无法立即提供的自定义提供商（例如Sinch、Infobip、Twilio）发送消息，请执行以下步骤：

1. 在左边栏中，浏览到&#x200B;**[!UICONTROL 管理]** > **[!UICONTROL 渠道]**&#x200B;并选择&#x200B;**[!UICONTROL API凭据]**&#x200B;菜单。

1. 单击&#x200B;**[!UICONTROL 创建新API凭据]**&#x200B;按钮。

   ![](assets/sms_byo_1.png)

1. 配置您的SMS API凭据，如下所述：

   * **[!UICONTROL SMS供应商]**：自定义。

   * **[!UICONTROL 名称]**：输入API凭据的名称。

   * **[!UICONTROL 提供程序AppId]**：输入您的SMS提供程序提供的应用程序ID。

   * **[!UICONTROL 提供商名称]**：输入短信提供商的名称。

   * **[!UICONTROL 提供程序URL]**：输入短信提供程序的URL。

   * **[!UICONTROL 身份验证类型&#x200B;]**：选择您的授权类型。 支持的授权类型为&#x200B;**持有者应用程序**&#x200B;或&#x200B;**基本**。

   * **[!UICONTROL API令牌]**：输入您的SMS提供商提供的API令牌。

   * **[!UICONTROL 提供程序有效负载]**：添加您的提供程序有效负载，如`{"from": "+1234XXXXXX", "to": "+1374XXXXXX", "content": "This is a test message", "contentType": "TEXT"}`。

     确保有效负载包括`{{toNumber}}`、`{{fromNumber}}`、`{{message}}`。

1. 完成API凭据配置后，单击&#x200B;**[!UICONTROL 提交]**。

1. 在&#x200B;**[!UICONTROL API凭据]**&#x200B;菜单中，单击bin图标以删除您的API凭据。

1. 要修改现有凭据，请找到所需的API凭据，然后单击&#x200B;**[!UICONTROL 编辑]**&#x200B;选项以进行必要更改。

创建和配置API凭据后，现在需要为SMS消息创建渠道平面。 [了解详情](sms-configuration-surface.md)

配置后，您可以利用所有现成的渠道功能，如消息创作、个性化、链接跟踪和报告。

## 操作方法视频 {#video}

>[!VIDEO](https://video.tv.adobe.com/v/3443616?captions=chi_hans)
