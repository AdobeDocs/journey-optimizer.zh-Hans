---
solution: Journey Optimizer
product: journey optimizer
title: 配置WhatsApp渠道
description: 了解如何配置您的环境以使用Journey Optimizer发送WhatsApp消息
feature: Whatsapp, Channel Configuration
role: Admin
level: Intermediate
hide: true
hidefromtoc: true
exl-id: d1f40cd8-f311-4df6-b401-8858095cef3e
source-git-commit: 78da5e017b5e3f39be1b613713f131d35260992b
workflow-type: tm+mt
source-wordcount: '748'
ht-degree: 5%

---

# WhatsApp 配置入门 {#whatsapp-config}

>[!BEGINSHADEBOX]

**目录**

* [WhatsApp 消息入门](get-started-whatsapp.md)
* **[开始使用WhatsApp配置](whatsapp-configuration.md)**
* [创建 WhatsApp 消息](create-whatsapp.md)
* [检查并发送 WhatsApp 消息](send-whatsapp.md)

>[!ENDSHADEBOX]

在发送WhatsApp消息之前，必须配置Adobe Journey Optimizer环境并与WhatsApp帐户关联。 要执行此操作，请执行以下操作：

1. [创建您的WhatsApp API凭据](#WhatsApp-credentials)
1. [创建WhatsApp Webhook](#WhatsApp-webhook)
1. [创建WhatsApp配置](#WhatsApp-configuration)

这些步骤必须由Adobe Journey Optimizer [系统管理员](../start/path/administrator.md)执行。

## 创建WhatsApp API凭据 {#whatsapp-credentials}

1. 在左边栏中，浏览到&#x200B;**[!UICONTROL 管理]** `>` **[!UICONTROL 渠道]**&#x200B;并选择&#x200B;**[!UICONTROL API凭据]**&#x200B;菜单。 单击&#x200B;**[!UICONTROL 创建新API凭据]**&#x200B;按钮。

1. 配置API凭据，如下所述：

   * **API令牌**：输入您的API令牌。 请参阅[元文档](https://developers.facebook.com/docs/facebook-login/guides/access-tokens/)以了解详情
   * **业务帐户ID**：输入与业务组合相关的唯一编号。 请参阅[元文档](https://www.facebook.com/business/help/1181250022022158?id=180505742745347)以了解详情。

   ![](assets/whatsapp-api.png)

1. 单击&#x200B;**[!UICONTROL 继续]**。

1. 选择要连接到WhatsApp API凭据的&#x200B;**商业帐户**。

   ![](assets/whatsapp-api-2.png)

1. 选择用于发送Whatsapp消息的&#x200B;**发件人名称**。

1. 您的电话号码设置会自动填写：

   * **质量评级**：反映客户对过去24小时内发送的邮件的反馈。
      * 绿色：高品质
      * 黄色：Medium品质
      * 红色：低品质

     了解有关[质量评级](https://www.facebook.com/business/help/766346674749731#)的更多信息

   * **吞吐量**：指示您的电话号码可以发送消息的速率。

1. 完成API凭据配置后，单击&#x200B;**[!UICONTROL 提交]**。

创建和配置API凭据后，现在需要为WhatsApp消息创建渠道配置。 [了解详情](#whatsapp-configuration)

## 创建Webhook {#WhatsApp-webhook}

>[!CONTEXTUALHELP]
>id="ajo_admin_whatsapp_webhook_inbound_keyword_category"
>title="入站关键词类别"
>abstract="<b>选择加入</b>：在用户订阅时发送您定义的自动响应。 <br/><b>选择退出</b>：在用户取消订阅时发送您定义的自动响应。 <br/><b>帮助</b>：在用户请求帮助或支持时发送您定义的自动响应。 <br/><b>默认</b>：在没有匹配关键字时发送您的回退自动响应。"

>[!CONTEXTUALHELP]
>id="ajo_admin_whatsapp_webhook_inbound_keyword"
>title="输入您的关键词"
>abstract= "You can define keywords to trigger specific auto-responses, such as for Opt-In, Opt-Out, Help, or Default, based on what users text. Keywords are not case-sensitive, e.g., "stop" and "STOP" are treated the same."

>[!CONTEXTUALHELP]
>id="ajo_admin_whatsapp_webhook_webhook_url"
>title=" 回调URL"
>abstract="此对象的验证请求和webhook通知将发送到指定的URL。"

>[!CONTEXTUALHELP]
>id="ajo_admin_whatsapp_webhook_verify_token"
>title="验证令牌"
>abstract="Meta在验证过程中回调以确认和验证回调URL的令牌。"

>[!NOTE]
>
>如果没有指定的选择加入或选择退出关键词，则不会启用标准同意消息。

成功创建WhatsApp API凭据和[Meta Webhook](https://developers.facebook.com/docs/whatsapp/webhooks/)后，下一步是创建webhook并配置入站设置。

1. 在左边栏中，导航到&#x200B;**[!UICONTROL 管理]** `>` **[!UICONTROL 渠道]**，选择&#x200B;**[!UICONTROL WhatsApp设置]**&#x200B;下的&#x200B;**[!UICONTROL WhatsApp Webhook]**&#x200B;菜单，然后单击&#x200B;**[!UICONTROL 创建Webhook]**&#x200B;按钮。

1. 输入webhook的[!UICONTROL 名称]。

1. 从下拉列表中，选择您之前创建的[API凭据](#whatsapp-credentials)。

1. 单击![添加](assets/do-not-localize/Smock_AddCircle_18_N.svg)开始配置&#x200B;**[!UICONTROL 入站关键字类别]**，例如：

   * **[!UICONTROL 选择加入关键字]**
   * **[!UICONTROL 选择退出关键字]**
   * **[!UICONTROL 帮助关键字]**

1. 输入您的&#x200B;**[!UICONTROL 关键字]**。

   要添加多个关键字，请单击![添加](assets/do-not-localize/Smock_AddCircle_18_N.svg)。

1. 指定在收到配置的关键字时要发送的&#x200B;**[!UICONTROL 回复消息]**。

<!--
1. Click **[!UICONTROL View payload editor]** to validate and customize your request payloads. 
    
    You can dynamically personalize your payload using profile attributes, and ensure accurate data is sent for processing and response generation with the help of built-in helper functions.
-->

1. 完成WhatsApp Webhook的配置后，单击&#x200B;**[!UICONTROL 提交]**。

1. 在&#x200B;**[!UICONTROL Webhooks]**&#x200B;菜单中，单击![bin图标](assets/do-not-localize/Smock_Delete_18_N.svg)以删除您的WhatsApp Webhook。

1. 要修改现有配置，请找到所需的Webhook，然后单击&#x200B;**[!UICONTROL 编辑]**&#x200B;选项以进行必要的更改。

1. 从您以前提交的&#x200B;**[!UICONTROL WhatsApp Webhook]**&#x200B;访问和复制新的&#x200B;**[!UICONTROL Webhook URL]**。

现在，您的Webhook已配置完毕，您可以创建WhatsApp配置了。

## 创建WhatsApp配置 {#whatsapp-configuration}

1. 在左边栏中，浏览到&#x200B;**[!UICONTROL 管理]** > **[!UICONTROL 渠道]**&#x200B;并选择&#x200B;**[!UICONTROL 常规设置]** > **[!UICONTROL 渠道配置]**。 单击&#x200B;**[!UICONTROL 创建渠道配置]**&#x200B;按钮。

   ![](assets/whatsapp-config-1.png)

1. 输入配置的名称和描述（可选），然后选择WhatsApp渠道。

   >[!NOTE]
   >
   > 名称必须以字母(A-Z)开头。 它只能包含字母数字字符。 您还可以使用下划线 `_`、点 `.` 和连字符 `-` 符号。

1. 选择&#x200B;**[!DNL WhatsApp]**&#x200B;作为您的渠道。

   ![](assets/whatsapp-config-2.png)

1. 选择&#x200B;**[!UICONTROL 营销操作]**&#x200B;以使用此配置将同意策略关联到消息。 所有与营销活动相关的同意政策均可利用，以尊重客户的偏好。 了解详情

1. 选择之前创建的&#x200B;**[!UICONTROL WhatsApp API配置]**。

   ![](assets/whatsapp-config-3.png)

1. 输入&#x200B;要用于通信的&#x200B;**[!UICONTROL 发件人号码]**。

1. 配置所有参数后，单击&#x200B;**[!UICONTROL 提交]**&#x200B;以确认。 您还可以将渠道配置另存为草稿，并稍后恢复其配置。

1. 创建渠道配置后，它将显示在状态为&#x200B;**[!UICONTROL 正在处理]**&#x200B;的列表中。

   >[!NOTE]
   >
   >如果检查不成功，请在[本节](../configuration/channel-surfaces.md)中进一步了解可能的失败原因。

1. 检查成功后，通道配置将获得&#x200B;**[!UICONTROL 活动]**&#x200B;状态。 它随时可用于投放消息。

配置后，您可以利用所有现成的渠道功能，如消息创作、个性化、链接跟踪和报告。

您现在可以使用Journey Optimizer发送WhatsApp消息了。