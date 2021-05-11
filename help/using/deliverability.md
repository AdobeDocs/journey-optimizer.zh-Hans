---
title: 监视消息执行
description: 了解监控和交付能力指南
translation-type: tm+mt
source-git-commit: 55b9e5d8ed259ec6ed7746e835691d7d6261a8a4
workflow-type: tm+mt
source-wordcount: '552'
ht-degree: 0%

---

# 管理可交付性{#manage-deliverability}

![](assets/do-not-localize/badge.png)

可交付性是衡量您的投放在进入收件人收件箱时是否成功的指标。

**电子** 邮件传送能力是指一系列特征，这些特征决定了邮件在短时间内通过个人电子邮件地址到达其目的地的能力，并在内容和格式方面达到了预期的质量。这些特征分为四个主要类别:数据质量、消息和内容、发送基础架构和声誉。 它们共同构成了成功的电子邮件交付项目的基础。

**可发送性率**&#x200B;是点击收件人收件箱的消息数，与已发送的消息数相比。 这取决于诸多因素，尤其是：

* 有限的垃圾邮件投诉
* 低硬反弹率
* 目标地址的质量
* 消息内容
* 发件人声誉

要优化您的[!DNL Journey Optimizer]体验的可交付性，我们建议使用本节中列出的最佳实践。 传送能力问题通常与由Internet服务提供商(ISP)和邮件服务器管理员实施的防垃圾邮件保护有关。

## 降低投诉率{#reduce-complaint-rate}

ISP通常将收到的消息报告为垃圾邮件。 这使得能够识别不可靠的来源。 通过快速满足选择退出请求并因此表明您是可靠的发件人，您可以降低投诉率。 [了解有关退出管理的更多信息](consent.md#opt-out-management)。

通常情况下，不要试图阻碍希望退出的收件人，例如要求他们填写电子邮件地址或姓名等字段。 退订登陆页应仅包含一个验证按钮。

请求额外确认时，请格外小心：用户可能有两个电子邮件地址被重定向到同一框(例如：firstname.lastname@club.com和firstname.lastname@internet-club.com)。 如果用户档案只能记住第一个地址，并希望通过发送给另一个地址的消息取消订阅，则表单将拒绝此请求，因为输入的加密标识符和电子邮件地址不匹配。

## 利用抑制列表{#suppression-lists}

[!DNL Journey Optimizer] 管理一个抑制列表，可收集一致发生的垃圾邮件投诉、硬弹回和软弹回。

为保护您的可交付性，默认情况下，其地址位于抑制列表的收件人将被排除在所有将来投放之外，因为发送到这些联系人可能会损害您的发送信誉。

[进一步了解抑制列表](suppression-lists.md)。

## 使用监视工具{#monitoring-tools}

使用[!DNL Journey Optimizer]提供的功能监控您的交付能力。

消息列表的&#x200B;**[!UICONTROL Executions]**&#x200B;选项卡允许您通过一组实时指示器检查投放的执行情况。 此选项卡还显示：
* 成功执行、发送和传递的消息数。
* 已打开的消息数和已单击的消息/链接数。

[了解有关监视消息执行的更多信息](message-monitoring.md)。

## 调整消息内容{#adapt-message-content}

在较小程度上，某些消息的内容可被检测为垃圾邮件。

<!--The use of certain words or of exclamation points in the subject line and within the messages can be read as signs of spam.

Spammers are also known to replace text with images to stop offending text from being analyzed automatically by anti-spam filters. In response to this, a message (in HTML format) with a high proportion of images, or images as attachments, may end up being blocked.-->

要提高您的投放率并确保您的电子邮件触及收件人，请在设计邮件内容时遵循以下原则：

* **发件人姓名和地址**:地址必须明确标识发件人。域必须由发送方拥有并注册。 域注册不得私有化。

<!--* **Subject**: Avoid excessive capitalization and punctuation, and words that are frequently used by spammers ("Win", "Free", etc.).
* **Personalize your email**: Personalizing the email increases the chances of your message being opened.
* **Images and text**: Respect a decent text/image ratio (for example 60% text and 40% images).-->
* **取消订阅链接和登陆页**:取消订阅链接是必备的。它必须可见且有效，并且表单必须能够正常工作。

<!--**Use tools** offered by Journey Optimizer to optimize the content of your email (delivery analysis, anti-spam analysis).-->

[了解有关设计电子邮件内容的更多信息](design-emails.md)。
