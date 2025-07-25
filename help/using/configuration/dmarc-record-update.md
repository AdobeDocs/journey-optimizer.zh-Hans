---
solution: Journey Optimizer
product: journey optimizer
title: 遵守新的 DMARC 要求
description: 了解必须在 Journey Optimizer 中设置 DMARC 记录的原因和时间
feature: Subdomains, Channel Configuration, Deliverability
topic: Administration
role: Admin
level: Experienced
keywords: 子域, 域, 邮件, dmarc, 记录
exl-id: 15b10a61-6ecd-4ffa-b1c2-21e862263f6d
source-git-commit: 8b755351e25ecae9a2058e63919d6512ea0bf153
workflow-type: tm+mt
source-wordcount: '431'
ht-degree: 96%

---

# 遵守新的 DMARC 要求 {#dmarc-record-update}

>[!CONTEXTUALHELP]
>id="ajo_admin_dmarc_banner_link"
>title="详细了解强制 DMARC 更新"
>abstract="自 **2024 年 2 月 1 日**&#x200B;起，作为执行行业最佳实践的举措之一，Google 和 Yahoo 都会要求您用于向它们发送电子邮件的任何域都必须有 **DMARC 记录**。<br>因此，您必须确保为您在 Journey Optimizer 中委托给 Adobe 的所有子域设置 DMARC 记录。"

基于域的消息身份验证、报告和符合性 (DMARC) 是一种电子邮件身份验证方法，允许域所有者保护其域免遭未经授权使用。向电子邮件提供商/ISP 提供明确的策略，这有助于防止恶意行为者假冒您的域发送电子邮件。实施 DMARC 可降低合法电子邮件被标记为垃圾邮件或拒绝的风险，并改进电子邮件可传递性。

作为执行行业最佳实践的举措之一，Google 和 Yahoo!都将要求为用于向其发送电子邮件的任何域设置 **DMARC 记录**。这一新要求自 **2024 年 2 月 1 日**&#x200B;起生效。

>[!CAUTION]
>
>若未能遵守 Gmail 和 Yahoo! 的新要求，可能导致电子邮件被标记为垃圾邮件或被阻止。

因此，Adobe 强烈建议您确保为您在 [!DNL Journey Optimizer] 中委派给 Adobe 的所有子域设置 DMARC 记录。请按照以下适用的步骤执行操作：

* 如果您已将发送子域[完全委派](delegate-subdomain.md#full-subdomain-delegation)给 Adobe，请执行以下操作之一：

   * **在您的托管解决方案中**，在已委派子域的父域上设置 DMARC。
或
   * 在 [!DNL Journey Optimizer]&#x200B;**配置用户界面中，在已委派子域上设置 DMARC**，无需对托管解决方案执行额外操作。[了解如何操作](dmarc-record.md#implement-dmarc)

* 如果您已通过 [CNAME](delegate-subdomain.md#cname-subdomain-setup) 设置发送子域，请执行以下操作之一：

   * **在您的托管解决方案中**，在子域或子域的父域上设置 DMARC。
或
   * 在 [!DNL Journey Optimizer]&#x200B;**配置用户界面中，在已委派子域上设置 DMARC**。[了解如何操作](dmarc-record.md#implement-dmarc)

  但是，CNAME 设置还需要在托管解决方案中执行其他一些输入操作。因此，请确保与 IT 部门进行协作，以便能够执行[本节](dmarc-record.md#implement-dmarc)中详述的更新。

<!--The most recent timelines shared by Google and Yahoo! are as follows:

* Google:

    * **February 2024** – Temporary bounces designed to provide warning of non-compliance will begin. Emails will still be delivered as normal after a short delay if you are not yet in compliance. If you are fully in compliance there will be no temporary bounces and you will not be affected.

    * **April 2024** – Blocks will begin for senders who are not in compliance with DMARC requirement. Only a portion of non-compliant email will be blocked at first, with the percentage blocked increasing over time.

    * **June 1st, 2024** – Any sender not in full compliance will experience blocking.

* Yahoo! has not provided exact dates, but has said "the rollout of enforcement will begin in February 2024. Enforcement will be gradually rolled out".
-->

>[!NOTE]
>
>如果您有任何问题或需要支持，请联系您的 Adobe 可传递性顾问或 Adobe 代表。

**有用链接**

* 在[可投放性最佳实践指南](https://experienceleague.adobe.com/docs/deliverability-learn/deliverability-best-practice-guide/additional-resources/technotes/implement-dmarc.html?lang=zh-Hans#about){target="_blank"}中了解有关DMARC的更多信息
* 阅读[Google Gmail公告](https://blog.google/products/gmail/gmail-security-authentication-spam-protection/){target="_blank"}
* 阅读 [Yahoo! 公告](https://blog.postmaster.yahooinc.com/post/730172167494483968/more-secure-less-spam){target="_blank"}

<!--Find more guidance about these changes in the [Deliverability Best Practice Guide]-->
