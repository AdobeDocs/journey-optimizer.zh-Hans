---
solution: Journey Optimizer
product: journey optimizer
title: 配置Twilio提供程序
description: 了解如何使用Twilio配置您的环境以使用Journey Optimizer发送短信
feature: SMS, Channel Configuration
role: Admin
level: Intermediate
source-git-commit: 0571a11eabffeb5e318bebe341a8df18da7db598
workflow-type: tm+mt
source-wordcount: '148'
ht-degree: 1%

---

# 配置Twilio提供程序 {#sms-configuration-twilio}

要使用Journey Optimizer配置Twilio，您需要创建用于Twilio的新API凭据：

1. 在左边栏中，浏览 **[!UICONTROL 管理]** > **[!UICONTROL 渠道]** 并选择 **[!UICONTROL API凭据]** 菜单。 单击 **[!UICONTROL 创建新的API凭据]** 按钮。

   ![](assets/sms_6.png)

1. 配置您的SMS API凭据，如下所述：

   * **[!UICONTROL 名称]**：选择API凭据的名称。

   * **[!UICONTROL 帐户SID]** 和 **[!UICONTROL 身份验证令牌]**：访问 **帐户信息** “Twilio控制台仪表板”页面的窗格，用于查找您的凭据。

   * **[!UICONTROL 消息SID]**：输入分配给Twilio API创建的每条消息的唯一标识符。 了解详情，请参阅 [Twilio文档](https://support.twilio.com/hc/en-us/articles/223134387-What-is-a-Message-SID-){target="_blank"}.

1. 单击 **[!UICONTROL 提交]** 完成API凭据配置时。

创建和配置API凭据后，现在需要为SMS和MMS消息创建渠道平面。 [了解详情](sms-configuration-surface.md)

