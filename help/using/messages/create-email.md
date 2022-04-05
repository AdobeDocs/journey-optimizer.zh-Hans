---
title: 创建电子邮件
description: 了解如何在Journey Optimizer中创建电子邮件
feature: Overview
topic: Content Management
role: User
level: Beginner
exl-id: c77dc420-a375-4376-ad86-ac740e214c3c
source-git-commit: 1d0e28583c500d5eddf9f88250f279d188c4784a
workflow-type: tm+mt
source-wordcount: '182'
ht-degree: 3%

---

# 创建电子邮件 {#configure-email}

>[!CONTEXTUALHELP]
>id="ajo_message_email"
>title="电子邮件创建"
>abstract="只需三个简单步骤即可定义电子邮件参数。"

一旦 [已创建消息](get-started-content.md)，则使用 **[!UICONTROL Email]** 选项卡，以定义电子邮件渠道的设置和内容。

![](assets/emails-configuration.png)

>[!NOTE]
>
>的 **[!UICONTROL From email]** 和 **[!UICONTROL From name]** 为只读，并由 **[!UICONTROL Preset]** 在 [创建消息](get-started-content.md).

配置电子邮件的步骤如下所示：

1. 在 **[!UICONTROL Subject line]** 字段。 为此，请单击右侧的按钮以打开表达式编辑器并撰写电子邮件主题。 了解如何在 [此部分](../personalization/personalize.md)

1. 单击 **[!UICONTROL Email Designer]** 按钮以设计电子邮件。 了解如何在 [此部分](../design/design-emails.md).

1. 如果要通过打开和/或单击链接来跟踪收件人的行为，请确保 **[!UICONTROL Open Tracking for email]** 和 **[!UICONTROL Click Tracking for email]** 选项。 了解有关跟踪的更多信息(位于 [此部分](../design/message-tracking.md).

>[!NOTE]
>
>营销类型的电子邮件必须包含 [选择退出链接](consent.md#opt-out-management)，事务型消息不需要此参数。 消息类别(**[!UICONTROL Marketing]** 或 **[!UICONTROL Transactional]**) [消息预设级别](../configuration/message-presets.md#email-type) 和时间 [创建消息](get-started-content.md#create-new-message).
