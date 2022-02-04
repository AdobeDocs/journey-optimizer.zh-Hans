---
title: 监视消息执行
description: 了解监控和投放能力指南
feature: Deliverability
topic: Content Management
role: User
level: Intermediate
exl-id: 8f33dda7-9bd5-4293-8d0d-222205cbc7d5
source-git-commit: 06a7abc2ada930356cbaf45ce01eed5e3156f2e3
workflow-type: tm+mt
source-wordcount: '654'
ht-degree: 0%

---

# 管理投放能力 {#manage-deliverability}

投放能力是衡量您向收件人发送收件箱的成功程度。

**电子邮件投放能力** 是指一组特征，这些特征决定了消息在短时间内通过个人电子邮件地址到达其目的地的能力，并且在内容和格式方面具有预期的质量。 这些特征分为四大类：数据质量、消息和内容、发送基础结构和信誉。 它们共同构成了成功电子邮件投放能力计划的基础。

的 **投放率** 是点击收件人收件箱的消息数与已投放的消息数之比。 这取决于诸多因素，特别是：

* 有限的垃圾邮件投诉
* 低硬跳出率
* 目标地址的质量
* 消息内容
* 发件人声誉

优化 [!DNL Journey Optimizer] 体验时，我们建议您使用此部分中列出的最佳实践。 投放能力问题通常与互联网服务提供商(ISP)和邮件服务器管理员实施的防垃圾邮件保护有关。

要更深入地了解什么是可投放性，并了解有关关键可投放性术语、概念和方法的更多信息，请参阅 [Adobe投放能力最佳实践指南](https://experienceleague.adobe.com/docs/deliverability-learn/deliverability-best-practice-guide/introduction.html?lang=zh-Hans){target=&quot;_blank&quot;}。

## 降低投诉率 {#reduce-complaint-rate}

ISP通常以一种突出的方式将收到的消息报告为垃圾邮件。 这样就可以识别不可靠的来源。 通过快速响应选择退出请求并因此显示您是可靠的发件人，可以降低投诉率。 [了解有关选择退出管理的更多信息](consent.md#opt-out-management).

通常，请不要尝试通过要求收件人填写诸如其电子邮件地址或姓名之类的字段来阻止希望选择退出的收件人。 退订登陆页面应仅具有一个验证按钮。

在请求额外确认时，请格外小心：用户可能具有两个重定向到同一框的电子邮件地址(例如：firstname.lastname@club.com和firstname.lastname@internet-club.com)。 如果用户档案只能记住第一个地址，并希望通过发送给另一个地址的消息取消订阅，则表单将拒绝此请求，因为加密的标识符与输入的电子邮件地址不匹配。

## 利用抑制列表 {#suppression-lists}

[!DNL Journey Optimizer] 管理可收集持续发生的垃圾邮件投诉、硬退回和软退回的抑制列表。

为了保护您的投放能力，在默认情况下，所有将来投放中将排除地址在禁止列表中的收件人，因为发送给这些联系人可能会损害您的发送声誉。

[进一步了解抑制列表](suppression-list.md).

## 使用监控工具 {#monitoring-tools}

使用 [!DNL Journey Optimizer] 监控投放能力。

的 **[!UICONTROL Executions]** 利用消息列表的选项卡，可通过一组实时指示器检查投放的执行情况。 此选项卡还显示：
* 成功执行、发送和发送的消息数。
* 已打开的消息数量和已点击的消息/链接数量。

[了解有关监视消息执行的更多信息](message-monitoring.md).

## 调整消息内容 {#adapt-message-content}

在较小程度上，某些消息的内容可以被检测为垃圾邮件。

要提高投放能力并确保电子邮件已发送给收件人，请在设计邮件内容时遵循以下原则：

* **发件人姓名和地址**:地址必须明确地标识发件人。 域必须由发件人拥有并注册。 域注册表不得私有化。

* **取消订阅链接和登陆页面**:取消订阅链接至关重要。 它必须可见且有效，并且表单必须有效。

[了解有关设计电子邮件内容的更多信息](design-emails.md).

## 建立发件人的声誉

如果您最近转移到其他电子邮件服务提供商、IP地址、电子邮件域或子域，则需要确立您作为发件人的声誉。 否则，您的投放可能会被阻止或移动到收件人邮箱的垃圾邮件文件夹中。

要预热IP，您可以逐步增加投放数量。 请参阅 [用例](../building-journeys/ramp-up-deliveries-uc.md).
