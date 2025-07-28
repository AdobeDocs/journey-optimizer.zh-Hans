---
solution: Journey Optimizer
product: journey optimizer
title: 电子邮件错误类型
description: 使用Journey Optimizer发送投放时，访问所有可能的电子邮件错误列表。
feature: Deliverability, Channel Configuration
topic: Administration
role: Admin
level: Experienced
keywords: 重试，退回，软，忽略，硬，优化器，错误
hide: true
hidefromtoc: true
source-git-commit: 817f7c88bfc2b40a7ce39575b4ad02fb372d429d
workflow-type: tm+mt
source-wordcount: '422'
ht-degree: 10%

---


# 电子邮件错误类型 {#email-error-types}

投放失败的可能原因有多种。 下表详细说明发送带有[!DNL Journey Optimizer]的电子邮件投放时可能发生的所有错误，以及它们的说明和错误类型。

这些错误可在[AJO消息反馈事件数据集](../data/datasets-query-examples.md#message-feedback-event-dataset)中找到，该数据集包含消息投放日志，包括来自[!DNL Journey Optimizer]的所有消息投放的信息以及来自电子邮件ISP的退件反馈记录。

| 错误标签 | 错误类型 | 技术价值 | 描述 |
| --- | --- | --- | --- |
| **未确定** | 已忽略 | 1 | 无法对从ISP接收的SMTP退回消息进行分类。 |
| **无效的收件人** | 硬退回 | 10 | 收件人的地址无效。 |
| **收件人已拒绝** | 硬退回 | 15 | 收件人的ISP已拒绝该消息，如果未禁止收件人，则ISP可能会阻止发件人。 |
| **软退回** | 软退回 | 20 | 消息遇到临时失败。 在未来的重试中它可能会成功。 |
| **DNS失败** | 软退回 | 21 | 消息投放遇到临时DNS故障。 在未来的重试中它可能会成功。 |
| **邮箱已满** | 软退回 | 22 | 由于收件人的邮箱已满，邮件遇到临时传递失败。 |
| **太大** | 已忽略 | 23 | 由于邮件大小超过收件人的限制，邮件遇到临时投放失败。 |
| **超时** | 已忽略 | 24 | 消息投放失败，可能是因为消息有效性已过期，或者发送到ISP所花费的时间太长。 |
| **管理失败** | 管理员 | 25 | 由于电子邮件发送基础架构中的一些策略配置，投放失败。 |
| **通用退回：无RCPT** | 已忽略 | 30 | 无法传递消息，因为未识别收件人。 |
| **通用退回** | 已忽略 | 40 | 由于未指明的原因，消息遇到临时投放失败。 |
| **邮件块** | 已忽略 | 50 | 由于ISP的高容量或速率限制，投放遇到临时故障。 |
| **垃圾邮件阻止** | 已忽略 | 51 | 由于ISP将发件人的域或IP视为已知的垃圾邮件来源，因此投放遇到临时失败。 |
| **垃圾邮件内容** | 已忽略 | 52 | 投放遇到临时失败，因为ISP将电子邮件的内容分类为垃圾邮件。 |
| **中继被拒绝** | 软退回 | 54 | 无法接受该消息，因为目标域未被列入允许中继列表。 |
| **自动回复** | 已忽略 | 60 | 除非启用了转发，否则接收时[!DNL Journey Optimizer]会丢弃这些邮件。 |
| **暂时性失败** | 已忽略 | 70 | 投放将按限制速率重试，在暂停时可能会延迟。 |
| **挑战 — 回应** | 软退回 | 100 | 由于[!DNL Journey Optimizer]不支持质询 — 响应身份验证机制，因此投放可能会永久失败。 |
