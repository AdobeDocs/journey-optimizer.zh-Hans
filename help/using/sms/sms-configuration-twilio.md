---
solution: Journey Optimizer
product: journey optimizer
title: 配置 Twilio 提供程序
description: 了解如何使用Twilio配置您的环境以使用Journey Optimizer发送短信
feature: SMS, Channel Configuration
role: Admin
level: Intermediate
exl-id: d6f74566-c913-4727-83b9-473a798a0158
source-git-commit: 4278d8c8294b1413788402cd8eac5959996ad3f5
workflow-type: tm+mt
source-wordcount: '518'
ht-degree: 2%

---

# 配置 Twilio 提供程序 {#sms-configuration-twilio}

通过将Twilio与Adobe Journey Optimizer集成，您可以向个人资料发送短信，作为历程和营销活动的一部分。

要将Twilio配置为您的短信提供商，请执行以下步骤：

1. [创建API凭据](#api-credential)
1. [创建 Webhook](sms-webhook.md)
1. [创建渠道配置](sms-configuration-surface.md)
1. [通过短信渠道操作创建历程或营销活动](create-sms.md)

## 为SMS/MMS配置API凭据 {#api-credential}

要使用Journey Optimizer配置Twilio，您需要为Twilio创建新的API凭据：

1. 在左边栏中，浏览到&#x200B;**[!UICONTROL 管理]** > **[!UICONTROL 渠道]** `>` **[!UICONTROL SMS设置]**&#x200B;并选择&#x200B;**[!UICONTROL API凭据]**&#x200B;菜单。 单击&#x200B;**[!UICONTROL 创建新API凭据]**&#x200B;按钮。

1. 配置您的SMS API凭据，如下所述：

   * **[!UICONTROL SMS供应商]**： Twilio。

   * **[!UICONTROL 名称]**：为您的API凭据选择一个名称。

   * **[!UICONTROL 帐户SID]**&#x200B;和&#x200B;**[!UICONTROL 身份验证令牌]**：访问Twilio控制台仪表板页面的&#x200B;**帐户信息**&#x200B;窗格以查找你的凭据。

   * **[!UICONTROL 消息SID]**：输入分配给Twilio API创建的每个消息的唯一标识符。 请参阅[Twilio文档](https://support.twilio.com/hc/en-us/articles/223134387-What-is-a-Message-SID-){target="_blank"}以了解详情。

   * **[!UICONTROL 入站编号]**：添加您的独特入站编号。 这允许您在不同沙盒中使用相同的API凭据，每个沙盒具有自己的入站编号。

1. 完成API凭据配置后，单击&#x200B;**[!UICONTROL 提交]**。

1. 在&#x200B;**[!UICONTROL API凭据]**&#x200B;菜单中，单击bin图标以删除您的API凭据。

1. 要修改现有凭据，请找到所需的API凭据，然后单击&#x200B;**[!UICONTROL 编辑]**&#x200B;选项以进行必要更改。

1. 单击现有API凭据中的&#x200B;**[!UICONTROL 验证SMS连接]**，通过向指定设备发送示例消息来测试和验证SMS API凭据。

1. 填写&#x200B;**数字**&#x200B;和&#x200B;**消息**&#x200B;字段，然后单击&#x200B;**[!UICONTROL 验证连接]**。

   >[!IMPORTANT]
   >
   >消息的结构必须与提供商的有效负荷格式保持一致。

   ![](assets/verify-connection.png)

创建和配置API凭据后，现在需要为SMS和MMS消息创建渠道配置。 [了解详情](sms-configuration-surface.md)

## 为RCS配置API凭据

Adobe Journey Optimizer使用[自定义SMS提供程序](sms-configuration-custom.md)功能，通过Twilio支持RCS消息传递。 这允许通过经验证的业务配置文件来交付丰富的交互式消息，并整合了诸如轮播、按钮和多媒体内容之类的元素。

➡️ [参阅Twilio文档，了解Twilio如何支持RCS](https://www.twilio.com/docs/rcs)

要通过Twilio启用RCS消息传递，必须通过自定义SMS提供商配置新的API凭据。 现有Twilio SMS凭据不兼容，因为RCS需要不同的有效负载格式。

使用Twilio配置RCS：

1. **在Twilio中注册RCS消息**

   首先在Twilio平台中完成RCS注册流程。 这包括设置您的企业配置文件并为您的帐户启用RCS功能。

1. **创建SMS Webhook**

   [配置可以接收传入RCS消息响应或传递更新的SMS Webhook](sms-configuration-custom.md#webhook)。 此webhook必须正确链接到您的Twilio设置以进行双向通信。

1. **使用自定义作为SMS供应商创建API凭据**

   在Journey Optimizer中，[使用“自定义”作为SMS供应商，专门为RCS定义新的API凭据](sms-configuration-custom.md#api-credential)。 使用适当的RCS端点身份验证方法、基本URL和标头。

创建和配置API凭据后，现在需要为RCS消息创建渠道配置。 [了解详情](sms-configuration-surface.md)







