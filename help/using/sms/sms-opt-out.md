---
solution: Journey Optimizer
product: journey optimizer
title: 短信选择退出管理
description: 了解如何使用短信消息管理选择退出
feature: Journeys
topic: Content Management
role: User
level: Intermediate
exl-id: 59ea67d9-e90c-4ad0-afb9-d0e0fd868855
source-git-commit: d1c11881654580247e8d7c92237cad130f11f749
workflow-type: tm+mt
source-wordcount: '415'
ht-degree: 0%

---

# 短信选择退出管理 {#sms-opt-out}

根据行业标准和法规，所有短信营销消息都必须包含一种方式，以便收件人轻松取消订阅。 [了解有关隐私和选择退出管理的更多信息](../privacy/opt-out.md)

默认情况下，Adobe Journey Optimizer会根据Sinch和Twilio等本机集成的行业标准，处理免费和长代码消息的标准英语回复消息，如STOP、UNSTOP和START。 这些关键字通常会触发来自第三方提供商的自动标准回复（例如Twilio、Sinch等）。 您可以直接与提供商或通过其文档网站确认此信息。

无需执行任何步骤，即可确保短信选择退出功能在Adobe Journey Optimizer中正常工作，因为关键词响应STOP、UNSTOP和START将被自动识别。

除了Adobe Journey Optimizer根据选择退出状态停止发送（用于与Twilio或Sinch的直接集成）之外，大多数短信网关提供商还会维护一个阻止列表，以确保短信消息不会发送给选择退出的个人。 如果您使用的是Sinch或Twilio以外的提供商，并通过发送短信 [自定义渠道](../building-journeys/using-custom-actions.md)，则需要与提供商确认。

>[!IMPORTANT]
>
>根据短信促销活动的性质、发送短信的位置以及收件人的位置，短信促销活动可能会受到各种法律合规性要求的约束。 <br>虽然Adobe Journey Optimizer将处理上述关于长代码和免费电话号码的消息，但您应当咨询您的法律顾问，以确保您的文本消息传送活动符合所有适用的法律合规要求。

## 短代码 {#short-codes}

默认情况下，Adobe Journey Optimizer将不处理短代码号的选择退出、选择加入或帮助关键词。

您必须确保您的简短代码符合所有选择退出处理的行业规则和法规。

## 字母数字发件人ID {#alphanumeric}

字母数字发件人ID仅用于单向消息传递，无法接收入站消息。 因此，Adobe Journey Optimizer的短信停止、开始、帮助关键字不适用于Alpha发送者ID。 您必须提供其他说明，例如写信给支持团队、拨打支持电话或发短信给其他电话号码或代码，以允许用户选择退出通过字母数字发件人ID发送的消息。

## 视频 {#video-sms}

要了解有关本机入站关键词支持（“开始”、“停止”和“停止”）如何用于短信的更多信息，请参阅以下视频：

>[!VIDEO](https://video.tv.adobe.com/v/344026?quality=12)
