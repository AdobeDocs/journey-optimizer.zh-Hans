---
solution: Journey Optimizer
product: journey optimizer
title: 短信成本优化最佳实践
description: 了解如何在Journey Optimizer中通过管理字符限制、编码和个性化来优化短信消息成本
feature: SMS
topic: Content Management
role: User
level: Intermediate
source-git-commit: 13b3c8aa7fce85029167ef31feb7272e4877b7b0
workflow-type: tm+mt
source-wordcount: '521'
ht-degree: 1%

---

# 短信成本优化的最佳实践 {#sms-cost-optimization}

SMS消息通常由提供商根据每条消息160个字符的限制计费。 如果短信消息被拆分为多个部分，则发送短信消息可能会产生额外费用。

遵循这些准则以优化您的报文传送策略并减少费用。

## 保持短消息 {#keep-messages-short}

Journey Optimizer在短信消息正文中最多可包含1,500个字符。 超过此限制时会显示警告，超过此阈值的消息将触发错误。

大多数短信提供商都支持GSM 7位编码，其中单个短信最多可包含160个字符。 超过此长度的消息会自动拆分为多个SMS部分（连接）：

* **少于160个字符**： 1个短信部分
* **161-306个字符**：2个SMS部件
* **307-459个字符**： 3个SMS部分

**为了将成本降至最低**，将消息长度限制在160个字符以内，以便作为单个SMS部分计费。

例如，1,600字符的消息可能占用10个短信积分，即使它在Journey Optimizer中显示为单个消息也是如此。

## 避免使用会增加长度的特殊字符 {#avoid-special-characters}

某些字符（如`| ^ € { } [ ] ~ \`）在GSM编码中将被计为两个字符。 包含这些字符可能会导致消息更快地超过&#x200B;**160个字符的限制**。

## 阻止UCS-2编码 {#prevent-ucs2-encoding}

如果消息包含非GSM字符，例如中文或阿拉伯文文本、商标符号或丰富格式工具的硬退回，则提供商将使用UCS-2对消息进行编码，该工具仅支持每条短信70个字符。

使用UCS-2编码可能会增加字符数，从而影响服务提供商的报文计费。

例如，一个200字符的Unicode消息将以3个短信部分发送。

## 创作最佳实践 {#authoring-best-practices}

直接在Journey Optimizer中撰写最终短信消息，或从纯文本应用程序中粘贴该消息。

避免使用富文本应用程序，因为它们可能会引入触发UCS-2编码的隐藏字符或换行符，从而可能增加SMS部件的数量和相关成本。

## 发送前检查字符数 {#check-character-count}

使用纯文本应用程序或Journey Optimizer **[!UICONTROL 模拟内容]**&#x200B;菜单来验证字符计数。

虽然Journey Optimizer会在内容模拟期间显示字符计数（包括空格），但请注意：

* 它&#x200B;**不**&#x200B;包含通过动态个性化生成的字符或某些特殊字符。

* **x/1500计数**&#x200B;用作技术有效负载限制的可视指示器，而不是每消息限制，例如160字符的GSM 7位限制。

* Adobe支持编辑器中的UTF-8编码，该编码不同于GSM-7位编码。

## 了解报告 {#understanding-reporting}

**Journey Optimizer报表**&#x200B;将完整消息计为一次发送，而不考虑SMS部分。

**提供商报告**&#x200B;反映了用于投放的SMS消息部件的实际数量，应参考这些数量以确认帐单和任何潜在超额。 如果Adobe是通过Sinch的短信提供商，则您将每月单独收到此账单报告。

## Personalization注意事项 {#personalization-considerations}

动态个性化可能会增加消息的长度。 例如，用长名字替换变量可以添加其他字符。

## 其他资源 {#additional-resources}

查看[Sinch字符支持指南](https://developers.sinch.com/docs/sms/resources/message-info/character-support/)中支持的字符和编码规则

