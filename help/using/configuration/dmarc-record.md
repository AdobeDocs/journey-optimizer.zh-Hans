---
solution: Journey Optimizer
product: journey optimizer
title: DMARC 记录
description: 了解如何在Journey Optimizer中设置DMARC记录
feature: Subdomains, Channel Configuration, Deliverability
topic: Administration
role: Admin
level: Experienced
keywords: 子域, 域, 邮件, dmarc, 记录
source-git-commit: 745474d6232f01ee959db8d706110477ed0220e2
workflow-type: tm+mt
source-wordcount: '1349'
ht-degree: 13%

---

# DMARC 记录 {#dmarc-record}

>[!CONTEXTUALHELP]
>id="ajo_admin_dmarc_record"
>title="设置 DMARC 记录"
>abstract="DMARC 是一种电子邮件身份验证方法，它使域所有者可保护其域免遭未经授权的使用，并避免邮箱提供商出现送达问题。<br>作为执行行业最佳实践的举措之一，Google 和 Yahoo!都会要求您用于向它们发送电子邮件的任何域都必须有 DMARC 记录。"

## 什么是DMARC？ {#what-is-dmarc}

基于域的消息身份验证、报告和符合性 (DMARC) 是一种电子邮件身份验证方法，允许域所有者保护其域免遭未经授权使用。向电子邮件提供商/ISP 提供明确的策略，这有助于防止恶意行为者假冒您的域发送电子邮件。实施 DMARC 可降低合法电子邮件被标记为垃圾邮件或拒绝的风险，并改进电子邮件可传递性。

DMARC还提供了对身份验证失败的消息的报告，以及对未通过DMARC验证的电子邮件的处理控制。 根据实施的 [DMARC策略](#dmarc-policies)，则可以监视、隔离或拒绝这些电子邮件。 利用这些功能，可采取措施来缓解和解决潜在错误。

为了帮助您防止出现可投放性问题，同时控制身份验证失败的邮件， [!DNL Journey Optimizer] 现在直接在其管理界面中支持DMARC技术。 [了解详情](#implement-dmarc)

### DMARC的工作原理 {#how-dmarc-works}

SPF和DKIM均用于将电子邮件与域相关联，并共同验证电子邮件。 DMARC更进一步，通过匹配DKIM和SPF检查的域，帮助防止欺骗。

>[!NOTE]
>
>在Journey Optimizer中，为您配置了SPF和DKIM。

要传递DMARC，必须传递SPF或DKIM：

* SPF （Sender Policy Framework，发件人策略框架）可通过检查发送服务器的IP地址（根据域的授权IP地址列表），帮助验证电子邮件是否来自授权来源。
* DKIM (DomainKeys Identified Mail)为电子邮件添加数字签名，允许收件人验证邮件的完整性和真实性。

如果这两种身份验证或其中一种都失败，则DMARC将失败，并根据您选择的DMARC策略发送电子邮件。

<!--DMARC requires alignment between the 'From" and 'Return-Path' address.-->

### DMARC策略 {#dmarc-policies}

如果电子邮件通过DMARC身份验证，您可以决定对该邮件应用哪个操作。 DMARC有三个政策选项：

* 监视(p=none)：指示邮箱提供商/ISP对邮件执行正常操作。
* 隔离（p=隔离）：指示邮箱提供商/ISP传送不会将DMARC传递到收件人的垃圾邮件或垃圾邮件文件夹的邮件。
* 拒绝(p=reject)：指示邮箱提供商/ISP阻止未通过DMARC的邮件，从而导致反弹。

>[!NOTE]
>
>了解如何使用设置DMARC策略 [!DNL Journey Optimizer] 在 [本节](#set-up-dmarc).

## DMARC要求更新 {#dmarc-update}

作为执行行业最佳实践的举措之一，Google 和 Yahoo!都要求您拥有 **DMARC记录** 用于向其发送电子邮件的任何域。 此新要求适用于起始日期 **2024年2月1日**.

>[!CAUTION]
>
>若未能遵守 Gmail 和 Yahoo! 的新要求，可能导致电子邮件被标记为垃圾邮件或被阻止。

因此，Adobe强烈建议您执行以下操作：

* 确保具有 **DMARC记录** 设置 **您已委派的所有子域** Adobe位置 [!DNL Journey Optimizer]. [了解如何操作](#check-subdomains-for-dmarc)

* 时间 **委派任何新子域** Adobe，您可以 **设置DMARC** 直接 **在 [!DNL Journey Optimizer] 管理界面**. [了解如何操作](#implement-dmarc)

## 在中实施DMARC [!DNL Journey Optimizer] {#implement-dmarc}

此 [!DNL Journey Optimizer] 管理界面允许您为已委派或正在委派给Adobe的所有子域设置DMARC记录。 详细步骤如下所述。

### 检查DMARC的现有子域 {#check-subdomains-for-dmarc}

确保为您已委派的所有子域设置了DMARC记录 [!DNL Journey Optimizer]，请按照以下步骤操作。

1. 访问 **[!UICONTROL 管理]** > **[!UICONTROL 渠道]** > **[!UICONTROL 子域]** 菜单，然后单击 **[!UICONTROL 设置子域]**.

1. 对于每个已委派的子域，请检查 **[!UICONTROL DMARC记录]** 列。 如果没有找到给定子域的记录，则会显示警报。

   ![](assets/dmarc-record-alert.png)

   >[!CAUTION]
   >
   >为了符合Gmail和Yahoo！的新要求，并避免顶级ISP出现可投放性问题，建议为所有委派的子域设置DMARC记录。 [了解详情](dmarc-record-update.md)

1. 选择未关联DMARC记录的子域，并填写 **[!UICONTROL DMARC记录]** 部分。 有关填充DMARC记录字段的详细步骤，请参见 [本节](#implement-dmarc).

1. 请考虑以下两个选项：

   * 如果您编辑的子域设置为 [CNAME](delegate-subdomain.md#cname-subdomain-delegation)，您必须将DMARC的DNS记录复制到您的托管解决方案中才能生成匹配的DNS记录。

     ![](assets/dmarc-record-edit-cname.png)

     确保DNS记录已生成到您的域托管解决方案中，并选中“我确认……”框。

   * 如果您正在编辑子域 [已完全委派](delegate-subdomain.md#full-subdomain-delegation) 要Adobe，只需填写 **[!UICONTROL DMARC记录]** 字段中详述 [本节](#implement-dmarc). 无需执行其他操作。

     ![](assets/dmarc-record-edit-full.png)

1. 保存更改。

### 为新子域设置DMARC {#set-up-dmarc}

委派新子域以在中进行Adobe时 [!DNL Journey Optimizer]，则将为您的域在DNS中创建一个DMARC记录。 按照以下步骤实施DMARC。

>[!CAUTION]
>
>为了符合Gmail和Yahoo！的新要求，并避免顶级ISP出现可投放性问题，建议为所有委派的子域设置DMARC记录。 [了解详情](dmarc-record-update.md)

<!--If you fail to comply with the new requirement from Gmail and Yahoo! to have DMARC record for all sending domains, your emails are expected to land into the spam folder or to get blocked.-->

1. 设置新子域。 [了解如何操作](delegate-subdomain.md)

1. 转到 **[!UICONTROL DMARC记录]** 部分。

   如果子域具有现有DMARC记录，并且它是由获取的 [!DNL Journey Optimizer]，则可以使用界面中突出显示的相同值，也可以根据需要更改这些值。

   ![](assets/dmarc-record-found.png)

   >[!NOTE]
   >
   >如果不添加任何值，将使用预填充的默认值。

1. 定义在DMARC失败时收件人服务器将执行的操作。 根据 [DMARC策略](#dmarc-policies) 要应用，请选择以下三个选项之一：

   * **[!UICONTROL 无]** （默认值）：告知接收者不对未通过DMARC身份验证的消息执行任何操作，但仍会向发件人发送电子邮件报告。
   * **[!UICONTROL 隔离]**：通知接收电子邮件服务器隔离未通过DMARC身份验证的电子邮件 — 这通常意味着将这些邮件置于收件人的垃圾邮件或垃圾邮件文件夹中。
   * **[!UICONTROL 拒绝]**：告知接收者完全拒绝（退回）未通过身份验证的域的任何电子邮件。 启用此策略后，只有经域验证为100%经过身份验证的电子邮件才有机会放置收件箱。

   >[!NOTE]
   >
   >作为最佳实践，建议通过将DMARC策略升级至 **无**，至 **隔离**，至 **拒绝** 当您了解DMARC的潜在影响时。

1. （可选）添加您选择的一个或多个电子邮件地址以指示位置 **DMARC报表** 在电子邮件中 [身份验证失败](#how-dmarc-works) 应该加入你的组织。 您最多可以为每个报表添加五个地址。

   >[!NOTE]
   >
   >确保您的控制中有一个正版收件箱(不是Adobe)，您可以在其中接收这些报告。

   ISP生成了两种不同的报告，发件人可以通过其DMARC策略中的RUA/RUF标记接收这些报告：

   * **汇总报表** (RUA)：它们不包含任何可能对GDPR敏感的PII（个人身份信息）。
   * **取证失败报告** (RUF)：它们包含对GDPR敏感的电子邮件地址。 在使用之前，请在内部检查如何处理需要符合GDPR的信息。

   >[!NOTE]
   >
   >这些技术性很强的报告概述了尝试欺骗的电子邮件。 最好通过第三方工具来消化这些术语。

1. 选择 **适用百分比** DMARC的电子邮件数量。

   此百分比取决于您对电子邮件基础架构的信心以及对误报（标记为欺诈的合法电子邮件）的容忍度。 组织通常先将DMARC策略设置为 **无**，逐步提高DMARC策略百分比，并密切监控对合法电子邮件投放的影响。

   >[!NOTE]
   >
   >随着您对电子邮件身份验证实践的信心，请与您的电子邮件管理员和IT团队合作，逐步提高此百分比。

   作为最佳实践，请力争实现高DMARC合规率（最好接近100%），以便在最大限度地提高安全性的同时最大限度地降低误报风险。

1. 选择 **报告间隔** 从24小时到168小时。 它允许域所有者定期接收有关电子邮件身份验证结果的更新，并采取必要措施提高电子邮件安全性。

   <!--The DMARC reporting interval is specified in the DMARC policy published in the DNS (Domain Name System) records for a domain. The reporting interval can be set to daily, weekly, or another specified frequency, depending on the domain owner's preferences.

    The default value (24 hours) is generally the email providers' expectation.-->


<!--

Setting up a DMARC record involves adding a DNS TXT record to your domain's DNS settings. This record specifies your DMARC policy, such as whether to quarantine or reject messages that fail authentication. Implementing DMARC is a proactive step towards enhancing email security and protecting both your organization and your recipients from email-based threats.

DMARC helps prevent malicious actors from sending emails that appear to come from your domain. By setting up DMARC, you can specify how email providers should handle messages that fail authentication checks, reducing the likelihood that phishing emails will reach recipients.

DMARC helps improve email deliverability by providing a clear policy for email providers to follow when encountering messages claiming to be from your domain. This can reduce the chances of legitimate emails being marked as spam or rejected.

DMARC helps protect against email spoofing, phishing, and other fraudulent activities.

It allows you to decide how a mailbox provider should handle emails that fail SPF and DKIM checks, providing a way to authenticate the sender's domain and prevent unauthorized use of the domain for malicious purposes.

## What are the benefits of DMARC? {#dmarc-benefits}

The key benefits or DMARC are as folllows:

* DMARC allows email receivers to easily identify the authentication of emails, which could potentially improve delivery.

* It offers reporting on which messages fail SPF and/or DKIM, enabling senders to gain visibility.

* This increased visibility allows for steps to be taken to mitigate further errors. It gives senders a degree of control over what happens with mail that does not pass either of these authentication methods.

-->







