---
solution: Journey Optimizer
product: journey optimizer
title: 配置您的自定义提供商
description: 了解如何配置您的环境，以通过自定义提供商使用Journey Optimizer发送短信
feature: SMS, Channel Configuration
role: Admin
level: Intermediate
source-git-commit: af03ad62c2c7b29d695670f083e0dfb6d0c71b93
workflow-type: tm+mt
source-wordcount: '250'
ht-degree: 3%

---

# 配置自定义提供程序（Beta 版） {#sms-configuration-custom}

>[!AVAILABILITY]
>
>自定义提供商目前仅作为测试版提供给选定用户。 请联系您的Adobe代表以将其纳入Beta。
>
>请注意，此Beta不支持用于选择启用/选择禁用同意管理和投放报告的入站消息。

要在Journey Optimizer中使用无法按Adobe立即使用的自定义提供商发送消息（例如，Sinch、Infobip、Twilio），请执行以下步骤：

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

创建和配置API凭据后，现在需要为SMS消息创建渠道平面。 [了解详情](sms-configuration-surface.md)

配置后，您可以利用所有现成的渠道功能，如消息创作、个性化、链接跟踪和报告。

## 操作方法视频 {#video}

>[!VIDEO](https://video.tv.adobe.com/v/3431625)
