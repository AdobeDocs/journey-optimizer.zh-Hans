---
solution: Journey Optimizer
product: journey optimizer
title: 短信选择禁用管理
description: 了解如何使用短信消息管理选择退出
feature: Journeys
topic: Content Management
role: User
level: Intermediate
exl-id: 59ea67d9-e90c-4ad0-afb9-d0e0fd868855
source-git-commit: 63237c02f632d289dba845acdcd0859f2d6de9c9
workflow-type: tm+mt
source-wordcount: '442'
ht-degree: 31%

---

# 短信选择禁用管理 {#sms-opt-out}

根据行业标准和法规，所有短信营销消息都必须包含一种让接收者能够轻松取消订阅的方式。[了解有关隐私和选择退出管理的更多信息](../privacy/opt-out.md)

>[!IMPORTANT]
>
>根据短信通信的性质、发送短信的位置以及收件人的位置，短信通信可能会受到各种法律合规要求的约束。 虽然Adobe Journey Optimizer会按照下文详细处理长代码和免费电话号码的报文，但请咨询您的法律顾问，确保您的短信通信符合所有适用的法律合规要求。

## 本机入站关键词{#sms-native-keywords}

默认情况下，Adobe Journey Optimizer会为免费电话和长码电文处理以下标准英语回复消息：停止、取消停止、开始、退出、取消、结束和取消订阅。 请注意，与Journey Optimizer一起使用时，只有Sinch支持本机关键字。

这些关键字通常会触发来自第三方提供商的自动标准回复。 您可以直接与提供商或通过其文档网站确认此信息。

无需执行任何步骤，即可确保短信选择退出功能在Adobe Journey Optimizer中正常工作，因为关键词响应STOP、UNSTOP、START、QUIT、CANCEL、END和UNSUBSCRIBE会被自动识别。 配置文件选择退出状态会在Adobe Journey Optimizer中实时更新。


## 阻止列表{#sms-blocklists}

除了Adobe Journey Optimizer根据选择退出状态停止发送（用于与Twilio或Sinch的直接集成）之外，大多数短信网关提供商还维护一个，确保短信消息不会发送给选择退出的个人。 如果您使用的是Sinch或Twilio以外的提供商，并通过 [自定义渠道](../building-journeys/using-custom-actions.md)，则需要与提供商确认。


## 短代码 {#short-codes}

默认情况下，短代码号的选择加入或帮助关键字不由Adobe Journey Optimizer处理。 要确保符合选择退出处理的行业法规和规则，必须验证您的简短代码是否遵守所有准则。

但是，Journey Optimizer支持基于具有不同发件人ID的传入关键词的全局选择退出。

## 字母数字发件人 ID {#alphanumeric}

字母数字发件人 ID 仅用于单向消息传递，且无法接收入站消息。因此，Adobe Journey Optimizer 的短信 STOP、START、HELP 关键字不适用于字母发件人 ID。您必须提供其他说明，例如写信给支持团队、拨打支持电话或发短信给其他电话号码或代码，以允许用户选择退出接收通过字母数字发件人 ID 发送的消息。

## 视频 {#video-sms}

要详细了解原生入站关键词支持（START、STOP 和 UNSTOP）如何用于短信，请参阅以下视频：

>[!VIDEO](https://video.tv.adobe.com/v/344026?quality=12)
