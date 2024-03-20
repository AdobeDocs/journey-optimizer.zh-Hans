---
solution: Journey Optimizer
product: journey optimizer
title: 可投放性入门
description: 了解可投放性准则
feature: Deliverability
topic: Content Management
role: Admin
level: Intermediate, Experienced
exl-id: 8f33dda7-9bd5-4293-8d0d-222205cbc7d5
source-git-commit: f8d62a702824bcfca4221c857acf1d1294427543
workflow-type: tm+mt
source-wordcount: '966'
ht-degree: 1%

---

# 可投放性入门 {#manage-deliverability}

可投放性是衡量投放到收件人收件箱中是否成功的指标。

>[!NOTE]
>
>对于许可Healthcare Shield的客户，Adobe使用传输层安全性(TLS) 1.2来保护用户系统（收件人）和Journey Optimizer（发件人）之间的数据交换。 如果接收邮件服务器不支持TLS 1.2，客户将遇到可投放性问题，包括电子邮件退回给原始发件人。

**电子邮件可投放性** 指一组特征，这些特征可确定消息在短时间内通过个人电子邮件地址达到其目的地的能力，以及在内容和格式方面达到预期质量。 这些特征可分为四大类：数据质量、报文和内容、发送基础架构和信誉。 它们共同构成了成功的电子邮件可投放性计划的基础。

此 **可投放性比率** 与已投放的消息数相比，点击收件人收件箱的消息数。 这取决于多种因素，特别是：

* 垃圾邮件投诉数量有限
* 硬退回率低
* 目标地址的质量
* 消息内容
* 发件人信誉

优化贵机构的 [!DNL Journey Optimizer] 体验，我们建议使用本节中列出的最佳实践。 可投放性问题通常与Internet服务提供商(ISP)和邮件服务器管理员实施的垃圾邮件防护有关。

要更深入地了解什么是可投放性，并详细了解可投放性的关键术语、概念和方法，请参阅 [Adobe可投放性最佳实践指南](https://experienceleague.adobe.com/docs/deliverability-learn/deliverability-best-practice-guide/introduction.html?lang=zh-Hans){target="_blank"}.

## 降低投诉率 {#reduce-complaint-rate}

ISP通常具有将收到的消息报告为垃圾邮件的显着方法。 这就有可能查明不可靠的来源。 通过快速响应选择退出请求，并显示您是可靠的发件人，您可以降低投诉率。 [了解有关选择退出管理的更多信息](../privacy/opt-out.md#opt-out-management)

通常，不要试图通过要求希望选择退出的收件人（例如，填写其电子邮件地址或姓名等字段）来妨碍他们。 退订登陆页面应仅具有一个验证按钮。

请求额外确认时请格外小心：用户可能有两个电子邮件地址被重定向到同一个框(例如：firstname.lastname@club.com和firstname.lastname@internet-club.com)。 如果配置文件只能记住第一个地址，并且希望通过发送给另一个配置文件的消息取消订阅，则表单将拒绝此操作，因为加密标识符和输入的电子邮件地址不匹配。

## 利用禁止显示列表 {#suppression-lists}

[!DNL Journey Optimizer] 管理收集垃圾邮件投诉、硬退回和一致发生的软退回的禁止列表。

为了保护您的可投放性，默认情况下将从所有未来投放中排除其地址在禁止列表上的收件人，因为发送给这些联系人可能会损害您的发送信誉。

[了解有关禁止列表的详细信息](suppression-list.md)

## 使用监控工具 {#monitoring-tools}

使用提供的功能 [!DNL Journey Optimizer] 以监控您的可投放性。

此 **[!UICONTROL 执行]** 利用消息列表的选项卡，可通过一组实时指示器检查投放的执行情况。 除其他事项外，此选项卡将显示：
* 成功执行、发送和投放的消息数。
* 已打开的邮件数和已点击的邮件/链接数。

## 调整消息内容 {#adapt-message-content}

在较小程度上，某些消息的内容可被检测为垃圾邮件。

为了提高可投放性并确保电子邮件可送达收件人，请在设计消息内容时遵循以下原则：

* **发件人姓名和地址**：地址必须明确标识发件人。 域必须由发件人拥有并向其注册。 域注册表不得私有化。

* **取消订阅链接和登陆页面**：取消订阅链接至关重要。 它必须可见且有效，并且表单必须有效。

[了解有关设计电子邮件内容的更多信息](../email/get-started-email-design.md)

## 建立您作为发件人的声誉 {#reputation}

如果您最近已移至其他电子邮件服务提供商、IP地址或电子邮件域或子域，则需要建立您作为发件人的声誉。 否则，您的投放可能会被阻止或移至收件人邮箱的垃圾邮件文件夹。

要预热您的IP，您可以逐渐增加投放的数量。 在本节中了解详情 [用例](../building-journeys/ramp-up-deliveries-uc.md).

## 实施 DMARC {#dmarc}

为了帮助您降低将合法电子邮件标记为垃圾邮件或拒绝的风险，并防止投放能力问题， [!DNL Journey Optimizer] 允许您为委派给Adobe的所有子域设置DMARC记录。

基于域的消息身份验证、报告和符合性(DMARC)是一种电子邮件身份验证方法，它允许域所有者保护其域不被恶意行为者未经授权使用。

[了解有关DMARC记录的更多信息](../configuration/dmarc-record.md)

## 了解反馈循环 {#feedback-loops}

反馈循环(FBL)是由某些ISP提供的服务，当收到电子邮件的用户选择将其标记为垃圾邮件（也称为“投诉”）时，该服务会自动通知电子邮件发件人。

最终用户提出由ISP发回Adobe的投诉后，电子邮件地址会自动添加到 [禁止显示列表](../reports/suppression-list.md) 并从将来的投放中排除。 事实上，向标记为垃圾邮件的用户发送电子邮件会对发件人的信誉产生负面影响，并可能导致可投放性问题。 [了解有关垃圾邮件投诉的更多信息](../reports/suppression-list.md#spam-complaints)

>[!IMPORTANT]
>
>并非所有ISP都提供传统的FBL，例如Gmail。 Gmail不提供个人级别的反馈，并且无法用于跟踪针对个人收件人的垃圾邮件投诉，而是侧重于其Google Postmaster工具中的汇总级别报告。 [了解详情](https://support.google.com/a/answer/6254652?hl=en){target="_blank"}

所有Adobe客户都会自动注册以下ISP的传统FBL：

* 1&amp;1

* AOL

* 蓝领带

* Comcast

* Fastmail

* 甘迪

* 意大利在线

* 拉波斯特

* Liberty Global (Chello、UPC、Unity Media)

* Locaweb

* Mail.RU

* Microsoft

* OpenSRS

* Rackspace

* SEZNM

* SFR

* SilverSky

* Swisscom

* Synacor

* 意大利电信

* Telenet

* Telenor

* Telstra

* Terra

* UOL

* 维珍媒体

* Yahoo

* Ziggo

Adobe会定期审核这些FBL，以确保添加最新的可用FBL。
