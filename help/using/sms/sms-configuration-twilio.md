---
solution: Journey Optimizer
product: journey optimizer
title: 配置 Twilio 提供程序
description: 了解如何使用Twilio配置您的环境以使用Journey Optimizer发送短信
feature: SMS, Channel Configuration
role: Admin
level: Intermediate
exl-id: d6f74566-c913-4727-83b9-473a798a0158
source-git-commit: b9208544b08b474db386cce3d4fab0a4429a5f54
workflow-type: tm+mt
source-wordcount: '178'
ht-degree: 4%

---

# 配置 Twilio 提供程序 {#sms-configuration-twilio}

要使用Journey Optimizer配置Twilio，您需要创建用于Twilio的新API凭据：

1. 在左边栏中，浏览到&#x200B;**[!UICONTROL 管理]** > **[!UICONTROL 渠道]** `>` **[!UICONTROL SMS设置]**&#x200B;并选择&#x200B;**[!UICONTROL API凭据]**&#x200B;菜单。 单击&#x200B;**[!UICONTROL 创建新API凭据]**&#x200B;按钮。

1. 配置您的SMS API凭据，如下所述：

   * **[!UICONTROL SMS供应商]**： Twilio。

   * **[!UICONTROL 名称]**：为您的API凭据选择一个名称。

   * **[!UICONTROL 帐户SID]**&#x200B;和&#x200B;**[!UICONTROL 身份验证令牌]**：访问Twilio控制台仪表板页面的&#x200B;**帐户信息**&#x200B;窗格以查找你的凭据。

   * **[!UICONTROL 消息SID]**：输入分配给Twilio API创建的每个消息的唯一标识符。 请参阅[Twilio文档](https://support.twilio.com/hc/en-us/articles/223134387-What-is-a-Message-SID-){target="_blank"}以了解详情。

   * **[!UICONTROL 入站编号]**：添加您的独特入站编号。 这允许您在不同沙盒中使用相同的API凭据，每个沙盒具有自己的入站编号。

1. 完成API凭据配置后，单击&#x200B;**[!UICONTROL 提交]**。

创建和配置API凭据后，现在需要为SMS和MMS消息创建渠道配置。 [了解详情](sms-configuration-surface.md)
