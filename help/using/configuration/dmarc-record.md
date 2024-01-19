---
solution: Journey Optimizer
product: journey optimizer
title: DMARC记录
description: 了解如何在Journey Optimizer中设置DMARC记录
feature: Subdomains, Channel Configuration
topic: Administration
role: Admin
level: Experienced
keywords: 子域，域，邮件， dmarc，记录
source-git-commit: f9d3234a64ad659660c2d2c4ad24ab5c240cb857
workflow-type: tm+mt
source-wordcount: '680'
ht-degree: 1%

---

# DMARC记录 {#dmarc-record}

>[!CONTEXTUALHELP]
>id="ajo_admin_dmarc_record"
>title="设置DMARC记录"
>abstract="设置DMARC记录以避免ISP出现可投放性问题。 作为强制执行行业最佳实践的一部分，Google和雅虎都要求您拥有DMARC记录，才能使用任何域向它们发送电子邮件。"

>[!CAUTION]
>
>继最近在Gmail和Yahoo上宣布推出批量发件人功能后，Journey Optimizer现在支持DMARC身份验证技术。

<!--TO ADD TO AJO HOME PAGE (first tab)

>[!TAB Mandatory DMARC update]

As part of their enforcing industry best practices, Google and Yahoo will both be requiring that you have a DMARC record for any domain you use to send email to them, starting on **February 1st, 2024**. Make sure that you have DMARC record set up for all the subdomains that you have delegated to Adobe in Journey Optimizer.

[![image](using/assets/do-not-localize/learn-more-button.svg)](using/configuration/dmarc-record-update.md)
-->

作为执行行业最佳实践的一部分，Google和雅虎都将要求您拥有 **DMARC记录** 用于向其发送电子邮件的任何域。 此新要求开始于 **2024年2月1日**.

在中了解有关Google和Yahoo要求的更多信息 [本节](https://experienceleague.adobe.com/docs/deliverability-learn/deliverability-best-practice-guide/additional-resources/guidance-around-changes-to-google-and-yahoo.html?lang=en#dmarc%3A){target="_blank"}.

>[!CAUTION]
>
>如果不遵循Gmail和Yahoo的新要求，则电子邮件可能会流入垃圾邮件文件夹或被阻止。

因此，Adobe强烈建议您确保为您已委派给Adobe的所有子域设置DMARC记录 [!DNL Journey Optimizer]. 请遵循以下两个选项之一：

* 在您的子域或子域的父域上设置DMARC， **在您的托管解决方案中**.

* 在委派的子域上设置DMARC **使用中的新功能 [!DNL Journey Optimizer] 管理UI**  — 无需对托管解决方案执行额外操作。 [了解详情](#implement-dmarc)

  >[!CAUTION]
  >
  >如果您已设置 [CNAME委派](delegate-subdomain.md#cname-subdomain-delegation) 对于要发送的子域，还需要在托管解决方案中输入一些内容。 确保与IT部门协调，以便他们能够在 [!DNL Journey Optimizer] 功能已推出（2024年1月30日）。 <!--and be ready on February 1st, 2024-->

>[!NOTE]
>
>了解有关在中实施DMARC的更多信息 [可投放性最佳实践指南](https://experienceleague.adobe.com/docs/deliverability-learn/deliverability-best-practice-guide/additional-resources/technotes/implement-dmarc.html#about){target="_blank"} 以更好地了解对电子邮件可投放性的影响。

## 什么是DMARC？

DMARC，代表 **基于域的报文验证、报告和符合性**，是一种电子邮件身份验证协议，可帮助防止电子邮件欺骗、网络钓鱼和其他欺诈活动。

* 电子邮件身份验证：

   * SPF （发件人策略框架）： DMARC依赖SPF来验证发送邮件服务器的身份。 SPF通过根据域的授权IP地址列表检查发送服务器的IP地址，帮助验证电子邮件是否来自授权源。
   * DKIM (DomainKeys Identified Mail)： DMARC还使用DKIM向电子邮件添加数字签名，允许收件人验证邮件的完整性和真实性。

* DMARC有助于防止恶意行为者发送似乎来自您域的电子邮件。 通过设置DMARC，您可以指定电子邮件提供商应如何处理身份验证检查失败的消息，从而降低仿冒电子邮件送达收件人的可能性。

* DMARC为电子邮件提供商在遇到声称来自您的域的邮件时提供明确的策略，以帮助改进电子邮件可投放性。 这可以降低合法电子邮件被标记为垃圾邮件或拒绝的几率。

* 通过实施DMARC，您可以确保未经授权的各方不会滥用您的域进行网络钓鱼或其他恶意活动，从而保护您的品牌声誉。 对于依赖与客户和合作伙伴进行电子邮件通信的企业和组织来说，这一点尤其重要。

设置DMARC记录涉及将DNS TXT记录添加到域的DNS设置。 此记录指定您的DMARC策略，例如是隔离还是拒绝身份验证失败的邮件。 实施DMARC是增强电子邮件安全性并保护您的组织和收件人免受电子邮件威胁的主动步骤。

## 实施 DMARC {#implement-dmarc}

* 如果不添加DMARC，您将至少被隔离。

* 确保您有一个可以接收邮件的正版收件箱 — 您可以管理此收件箱(不应是Adobe收件箱)

推荐值为24，因为通常这是ISP具有的内容。
如果低于，则评估您的容量/查看您的>聊天GPT

如果检测到DMARC记录，则可以复制粘贴与列出的值相同的值，或者在需要时更改这些值。

如果不输入任何内容，则使用默认值。

### 完全委派的子域

### 使用CNAME委派的子域

对于版本流中的CNAME，您需要再次下载CSV文件（不是为了完全委派）





