---
solution: Journey Optimizer
product: journey optimizer
title: 短信的选择退出管理
description: 了解如何使用短信/彩信消息管理选择退出
feature: SMS
topic: Content Management
role: User
level: Intermediate
exl-id: 59ea67d9-e90c-4ad0-afb9-d0e0fd868855
source-git-commit: 7973f56c26c01d4845138f70cd00bce8ab7fc09c
workflow-type: tm+mt
source-wordcount: '568'
ht-degree: 16%

---

# 短信的选择退出管理 {#sms-opt-out}

根据行业标准和法规，所有短信营销消息都必须包含一种让接收者能够轻松取消订阅的方式。[了解有关隐私和选择退出管理的更多信息](../privacy/opt-out.md)

>[!IMPORTANT]
>
>根据短信的性质、发送短信的位置以及收件人的位置，短信通信可能会受到各种法律合规性要求的约束。 虽然Adobe Journey Optimizer会处理下面详述的短代码、长代码和免费电话号码的消息，但请咨询您的法律顾问，以确保您的短信通信符合所有适用的法律合规要求。
>

## 本机入站关键词 {#sms-native-keywords}

>[!NOTE]
>
> 与Journey Optimizer一起使用时，只有Sinch和Infobip支持本机关键字。

默认情况下，Adobe Journey Optimizer会处理短代码、免费和长代码消息的以下标准英语回复消息：

* **选择退出**：停止、退出、取消、结束、取消订阅、否。
* **选择加入**：订阅、是、不停止、开始、继续、继续、开始。
* **帮助**：帮助。

这些关键字通常会触发来自第三方提供商的自动标准回复。 您可以直接与提供商或通过其文档网站确认此信息。

使用Infobip时，请确保将“转发”操作设置为“拉取”配置。

无需执行任何步骤，即可确保短信选择退出功能在Adobe Journey Optimizer中正常工作，因为关键词响应STOP、UNSTOP、START、QUIT、CANCEL、END和UNSUBSCRIBE会被自动识别。 在Adobe Journey Optimizer中实时更新用户档案选择退出状态。

请注意，如果客户对文本消息响应STOP，则提供商会阻止该特定发送者ID（短代码或长数字）中的所有后续SMS，包括事务型消息。 要确保事务性短信的投放不会出现中断，请使用之前未选择退出的单独发件人ID。


>[!NOTE]
>
>如果您计划使用双向短信（使用STOP、QUIT等回复），请确保您首先至少发送了一次单向短信，以建立电话号码与用户档案的映射。 提供程序凭据过期或配置错误将阻止入站关键词更新用户配置文件，从而导致选择退出记录丢失或延迟。


## 阻止列表 {#sms-blocklists}

除了根据选择退出状态停止Adobe Journey Optimizer列入阻止列表发送（用于与Twilio、Infobip或Sinch的直接集成）之外，大多数短信网关提供商还设有，确保您的短信消息不会发送给选择退出的个人。 如果您使用的是Sinch或Twilio以外的提供商，并通过[自定义渠道](../building-journeys/using-custom-actions.md)发送短信，则需要就此与提供商确认。


## 短代码 {#short-codes}

默认情况下，Adobe Journey Optimizer不处理短代码号的选择加入或帮助关键字。 要确保遵守行业法规和选择退出处理规则，必须验证您的短代码是否符合所有准则。

但是，Journey Optimizer不支持根据具有不同发件人ID的传入关键字来选择全局退出。

## 字母数字发件人 ID {#alphanumeric}

字母数字发件人 ID 仅用于单向消息传递，且无法接收入站消息。因此，Adobe Journey Optimizer的短信STOP、START、HELP关键字不适用于Alpha发件人ID。 您必须提供其他说明，例如写信给支持团队、拨打支持电话或发短信给其他电话号码或代码，以允许用户选择退出接收通过字母数字发件人 ID 发送的消息。

## 视频 {#video-sms}

* 以下视频可帮助您了解如何为短信配置双重选择加入。

+++ 观看视频

  >[!VIDEO](https://video.tv.adobe.com/v/3440290/?learn=on&captions=chi_hans)

+++
