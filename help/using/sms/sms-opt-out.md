---
solution: Journey Optimizer
product: journey optimizer
title: 短信选择禁用管理
description: 了解如何使用短信消息管理选择退出
feature: Journeys
topic: Content Management
role: User
level: Intermediate
source-git-commit: 020c4fb18cbd0c10a6eb92865f7f0457e5db8bc0
workflow-type: tm+mt
source-wordcount: '415'
ht-degree: 96%

---

# 短信选择禁用管理 {#sms-opt-out}

根据行业标准和法规，所有短信营销消息都必须包含一种让接收者能够轻松取消订阅的方式。[了解有关隐私和选择退出管理的更多信息](../privacy/opt-out.md)

默认情况下，Adobe Journey Optimizer 会根据 Sinch 和 Twilio 等原生集成的行业标准，处理免费和长代码消息的标准英语回复消息，如 STOP、UNSTOP 和 START。这些关键字通常会触发来自第三方提供商的自动标准回复（例如 Twilio、Sinch 等）。您可以直接与提供商或通过其文档网站确认此信息。

无需执行任何步骤，即可确保短信选择退出功能在 Adobe Journey Optimizer 中正常工作，因为关键词响应 STOP、UNSTOP 和 START 将被自动识别。

除了 Adobe Journey Optimizer 根据选择退出状态停止发送（用于与 Twilio 或 Sinch 的直接集成）之外，大多数短信网关提供商还设有一个阻止列表，确保您的短信消息不会被发送给选择退出的个人。如果您使用的是 Sinch 或 Twilio 以外的提供商，并通过 [自定义渠道](../building-journeys/using-custom-actions.md)发送短信，则需要就此与提供商确认。

>[!IMPORTANT]
>
>根据短信活动的性质、发送短信的位置以及收件人的位置，短信活动可能会受到各种法律合规性要求的约束。<br>虽然 Adobe Journey Optimizer 将处理使用上述长代码和免费电话号码的消息，但您应咨询您的法律顾问，以确保您的短信活动符合所有适用的法律合规要求。

## 短代码 {#short-codes}

默认情况下，Adobe Journey Optimizer 将不处理短代码号的选择退出、选择加入或帮助关键词。

您必须确保您的短代码符合所有选择退出处理方面的行业规则和法规。

## 字母数字发件人 ID {#alphanumeric}

字母数字发件人 ID 仅用于单向消息传递，且无法接收入站消息。因此，Adobe Journey Optimizer 的短信 STOP、START、HELP 关键字不适用于字母发件人 ID。您必须提供其他说明，例如写信给支持团队、拨打支持电话或发短信给其他电话号码或代码，以允许用户选择退出接收通过字母数字发件人 ID 发送的消息。

## 视频 {#video-sms}

要详细了解原生入站关键词支持（START、STOP 和 UNSTOP）如何用于短信，请参阅以下视频：

>[!VIDEO](https://video.tv.adobe.com/v/344026?quality=12)
