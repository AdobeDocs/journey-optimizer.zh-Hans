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
source-git-commit: 7d5a2a9b80110505688b5bfda2e286c7a6432441
workflow-type: tm+mt
source-wordcount: '905'
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

因此，Adobe强烈建议您确保为您已委派给Adobe的所有子域设置DMARC记录 [!DNL Journey Optimizer]. 请按照以下适用于您的案例的步骤执行操作：

* 如果您拥有 [已完全委派](delegate-subdomain.md#full-subdomain-delegation) 按照以下两个选项之一，将子域发送至Adobe：

   * 在委派的子域的父域上设置DMARC **在您的托管解决方案中**.

   * 在委派的子域上设置DMARC **使用中即将推出的功能 [!DNL Journey Optimizer] 管理UI**  — 无需对托管解决方案执行额外操作。

* 如果您已设置 [CNAME委派](delegate-subdomain.md#cname-subdomain-delegation) 对于正在发送的子域，请遵循以下两个选项之一：

   * 在子域或子域的父域上设置DMARC **在您的托管解决方案中**.

   * 在委派的子域上设置DMARC **使用中即将推出的功能 [!DNL Journey Optimizer] 管理UI**. 但是，它还需要在托管解决方案中输入。 因此，请确保与IT部门进行协调，以便他们能够在 [!DNL Journey Optimizer] 功能现已推出（1月30日）。 <!--and be ready on February 1st, 2024-->

**更多有关 [!DNL Journey Optimizer] DMARC即将推出的功能即将推出。**

>[!NOTE]
>
>了解有关在中实施DMARC的更多信息 [可投放性最佳实践指南](https://experienceleague.adobe.com/docs/deliverability-learn/deliverability-best-practice-guide/additional-resources/technotes/implement-dmarc.html#about){target="_blank"} 以更好地了解对电子邮件可投放性的影响。

## 什么是DMARC？

DMARC，代表 **基于域的报文验证、报告和符合性**，是一种电子邮件身份验证方法/协议，它允许域所有者保护其域免遭未经授权的使用。

它提供了一种验证发件人域的方法，有助于防止恶意行为者发送似乎来自您域的电子邮件。

DMARC还提供了电子邮件身份验证状态的反馈，并允许发件人控制身份验证失败的电子邮件会发生什么情况。 这包括监视、隔离或拒绝邮件的选项，具体取决于已实施的DMARC策略。

<!--Setting up a DMARC record involves adding a DNS TXT record to your domain's DNS settings. This record specifies your DMARC policy, such as whether to quarantine or reject messages that fail authentication. Implementing DMARC is a proactive step towards enhancing email security and protecting both your organization and your recipients from email-based threats.-->

DMARC有三个政策选项：

* 监视(p=none)：指示邮箱提供商/ISP对邮件执行正常操作。
* 隔离（p=隔离）：指示邮箱提供商/ISP传送不会将DMARC传递到收件人的垃圾邮件或垃圾邮件文件夹的邮件。
* 拒绝(p=reject)：指示邮箱提供商/ISP阻止未通过DMARC的邮件，从而导致反弹。

## DMARC的工作原理

SPF和DKIM均用于将电子邮件与域相关联，并共同验证电子邮件。 DMARC更进一步，通过匹配DKIM和SPF检查的域，帮助防止欺骗。 要传递DMARC，必须传递SPF或DKIM。 如果这两种身份验证都失败，DMARC将失败，并且电子邮件将根据您选择的DMARC策略进行投放。

* SPF （发件人策略框架）： DMARC依赖SPF来验证发送邮件服务器的身份。 SPF通过根据域的授权IP地址列表检查发送服务器的IP地址，帮助验证电子邮件是否来自授权源。
* DKIM (DomainKeys Identified Mail)： DMARC还使用DKIM向电子邮件添加数字签名，允许收件人验证邮件的完整性和真实性。

>[!NOTE]
>
>DMARC要求在“发件人”和“返回路径”地址之间保持一致。


<!--

* DMARC helps prevent malicious actors from sending emails that appear to come from your domain. By setting up DMARC, you can specify how email providers should handle messages that fail authentication checks, reducing the likelihood that phishing emails will reach recipients.

* DMARC helps improve email deliverability by providing a clear policy for email providers to follow when encountering messages claiming to be from your domain. This can reduce the chances of legitimate emails being marked as spam or rejected.

DMARC helps protect against email spoofing, phishing, and other fraudulent activities.

It allows you to decide how a mailbox provider should handle emails that fail SPF and DKIM checks, providing a way to authenticate the sender's domain and prevent unauthorized use of the domain for malicious purposes.

-->


## 实施 DMARC {#implement-dmarc}

要实施DMARC，请按照以下适用于您的案例的步骤操作。

* 如果不添加DMARC，您将至少被隔离。

### 完全委派的子域

设置在DMARC失败时收件人服务器将执行的操作。

DMARC有三个政策选项：

* 监视(p=none)：指示邮箱提供商/ISP对邮件执行正常操作。 这是默认值。
* 隔离（p=隔离）：指示邮箱提供商/ISP传送不会将DMARC传递到收件人的垃圾邮件或垃圾邮件文件夹的邮件。
* 拒绝(p=reject)：指示邮箱提供商/ISP阻止未通过DMARC的邮件，从而导致反弹。

用于接收汇总DMARC报告和鉴证DMARC故障报告的电子邮件：最多可添加5个地址。

* 确保您有一个可以接收邮件的正版收件箱 — 您可以管理此收件箱(不应是Adobe收件箱)

要应用DMARC的电子邮件的适用百分比：

报告间隔：建议为24，因为通常这是ISP具有的值。
如果低于，则评估您的容量/查看您的>聊天GPT

如果检测到DMARC记录，则可以复制粘贴与列出的值相同的值，或者在需要时更改这些值。

如果不输入任何内容，则使用默认值。

### 使用CNAME委派的子域

对于版本流中的CNAME，您需要再次下载CSV文件（不是为了完全委派）





