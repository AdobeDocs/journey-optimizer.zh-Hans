---
title: 监视消息执行
description: 了解监控和投放能力指南
source-git-commit: f04e73187439462fc1e22c6c66398a139fbeaa5a
workflow-type: tm+mt
source-wordcount: '553'
ht-degree: 0%

---

# 管理投放能力{#manage-deliverability}

![](assets/do-not-localize/badge.png)

投放能力是衡量您向收件人发送收件箱的成功程度。

**电子** 邮件投放能力是指一组特征，这些特征决定了邮件在短时间内通过个人电子邮件地址到达其目的地的能力，并在内容和格式方面具有预期质量。这些特征分为四大类：数据质量、消息和内容、发送基础结构和信誉。 它们共同构成了成功电子邮件投放能力计划的基础。

**投放能力率**&#x200B;是点击收件人收件箱的消息数，与投放的消息数相比。 这取决于诸多因素，特别是：

* 有限的垃圾邮件投诉
* 低硬跳出率
* 目标地址的质量
* 消息内容
* 发件人声誉

要优化[!DNL Journey Optimizer]体验的投放能力，我们建议使用此部分中列出的最佳实践。 投放能力问题通常与互联网服务提供商(ISP)和邮件服务器管理员实施的防垃圾邮件保护有关。

## 降低投诉率{#reduce-complaint-rate}

ISP通常以一种突出的方式将收到的消息报告为垃圾邮件。 这样就可以识别不可靠的来源。 通过快速响应选择退出请求并因此显示您是可靠的发件人，可以降低投诉率。 [了解有关选择退出管理的更多信息](consent.md#opt-out-management)。

通常，请不要尝试通过要求收件人填写诸如其电子邮件地址或姓名之类的字段来阻止希望选择退出的收件人。 退订登陆页面应仅具有一个验证按钮。

在请求额外确认时，请格外小心：用户可能具有两个重定向到同一框的电子邮件地址(例如：firstname.lastname@club.com和firstname.lastname@internet-club.com)。 如果用户档案只能记住第一个地址，并希望通过发送给另一个地址的消息取消订阅，则表单将拒绝此请求，因为加密的标识符与输入的电子邮件地址不匹配。

## 利用抑制列表{#suppression-lists}

[!DNL Journey Optimizer] 管理可收集持续发生的垃圾邮件投诉、硬退回和软退回的抑制列表。

为了保护您的投放能力，在默认情况下，所有将来投放中将排除地址在禁止列表中的收件人，因为发送给这些联系人可能会损害您的发送声誉。

[进一步了解抑制列表](suppression-list.md)。

## 使用监控工具{#monitoring-tools}

使用[!DNL Journey Optimizer]提供的功能监控投放能力。

利用消息列表的&#x200B;**[!UICONTROL Executions]**&#x200B;选项卡，可通过一组实时指示器检查投放的执行情况。 此选项卡还显示：
* 成功执行、发送和发送的消息数。
* 已打开的消息数量和已点击的消息/链接数量。

[了解有关监视消息执行的更多信息](message-monitoring.md)。

## 调整消息内容{#adapt-message-content}

在较小程度上，某些消息的内容可以被检测为垃圾邮件。

<!--The use of certain words or of exclamation points in the subject line and within the messages can be read as signs of spam.

Spammers are also known to replace text with images to stop offending text from being analyzed automatically by anti-spam filters. In response to this, a message (in HTML format) with a high proportion of images, or images as attachments, may end up being blocked.-->

要提高投放能力并确保电子邮件已发送给收件人，请在设计邮件内容时遵循以下原则：

* **发件人姓名和地址**:地址必须明确地标识发件人。域必须由发件人拥有并注册。 域注册表不得私有化。

<!--* **Subject**: Avoid excessive capitalization and punctuation, and words that are frequently used by spammers ("Win", "Free", etc.).
* **Personalize your email**: Personalizing the email increases the chances of your message being opened.
* **Images and text**: Respect a decent text/image ratio (for example 60% text and 40% images).-->
* **取消订阅链接和登陆页面**:取消订阅链接至关重要。它必须可见且有效，并且表单必须有效。

<!--**Use tools** offered by Journey Optimizer to optimize the content of your email (delivery analysis, anti-spam analysis).-->

[了解有关设计电子邮件内容的更多信息](design-emails.md)。
