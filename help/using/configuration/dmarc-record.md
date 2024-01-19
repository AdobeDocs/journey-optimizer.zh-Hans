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
source-git-commit: 49cb9734d66dc1aa2a3531c71a687aac00834d82
workflow-type: tm+mt
source-wordcount: '599'
ht-degree: 0%

---

# DMARC记录 {#dmarc-record}

>[!CONTEXTUALHELP]
>id="ajo_admin_dmarc_record"
>title="设置DMARC记录"
>abstract="设置DMARC记录以避免ISP出现可投放性问题"

>[!CAUTION]
>
>继最近在Gmail和Yahoo上宣布推出批量发件人功能后，Journey Optimizer现在支持DMARC身份验证技术。//您必须更新已在实例中创建的所有子域以包含DMARC支持。//

在2月1日前完成此任务很重要，Doc即将推出

开始日期

您有2个选项：

* 从现在开始，您自行完成：随时与IT部门一起设置

* 在AJO中执行此操作 — 但在这种情况下，您需要等待1月30日

   * 完全委派：您可以在1月30日执行该操作（AJO版本）

   * CNAME与您的IT部门一起进行规划，这样就不会太费时，但您需要对其进行规划

作为强制执行行业最佳实践的一部分，Google和雅虎都将要求您拥有DMARC记录，才能用于向其发送电子邮件。 此新要求开始于 **2024年2月1日**.

在中了解有关Google和雅虎对DMARC记录要求的更多信息 [本节](https://experienceleague.adobe.com/docs/deliverability-learn/deliverability-best-practice-guide/additional-resources/guidance-around-changes-to-google-and-yahoo.html?lang=en#dmarc%3A){target="_blank"}.

在Google和Yahoo上了解更多已宣布的更改 [此页面](https://experienceleague.adobe.com/docs/deliverability-learn/deliverability-best-practice-guide/additional-resources/guidance-around-changes-to-google-and-yahoo.html?lang=en#dmarc%3A){target="_blank"}.

DMARC，代表 **基于域的报文验证、报告和符合性**，是一种电子邮件身份验证协议，可帮助防止电子邮件欺骗、网络钓鱼和其他欺诈活动。

* 电子邮件身份验证：

   * SPF （发件人策略框架）： DMARC依赖SPF来验证发送邮件服务器的身份。 SPF通过根据域的授权IP地址列表检查发送服务器的IP地址，帮助验证电子邮件是否来自授权源。
   * DKIM (DomainKeys Identified Mail)： DMARC还使用DKIM向电子邮件添加数字签名，允许收件人验证邮件的完整性和真实性。

* DMARC有助于防止恶意行为者发送似乎来自您域的电子邮件。 通过设置DMARC，您可以指定电子邮件提供商应如何处理身份验证检查失败的消息，从而降低仿冒电子邮件送达收件人的可能性。

* DMARC为电子邮件提供商在遇到声称来自您的域的邮件时提供明确的策略，以帮助改进电子邮件可投放性。 这可以降低合法电子邮件被标记为垃圾邮件或拒绝的几率。

* 通过实施DMARC，您可以确保未经授权的各方不会滥用您的域进行网络钓鱼或其他恶意活动，从而保护您的品牌声誉。 对于依赖与客户和合作伙伴进行电子邮件通信的企业和组织来说，这一点尤其重要。

设置DMARC记录涉及将DNS TXT记录添加到域的DNS设置。 此记录指定您的DMARC策略，例如是隔离还是拒绝身份验证失败的邮件。 实施DMARC是增强电子邮件安全性并保护您的组织和收件人免受电子邮件威胁的主动步骤。

[在可投放性最佳实践指南中了解有关DMARC的更多信息](https://experienceleague.adobe.com/docs/deliverability-learn/deliverability-best-practice-guide/additional-resources/technotes/implement-dmarc.html#about){target="_blank"} 以更好地了解DMARC对电子邮件可投放性的影响。

如果不添加DMARC，您将至少被隔离。

请确保您拥有可控制的正版收件箱 — 您管理此收件箱(不应是Adobe收件箱)

建议为24，因为通常情况下，如果低于，请评估您的容量/检查您的>聊天GPT

Google和Yahoo，以及所有其他主要ISP

对于版本流中的CNAME，您需要再次下载CSV文件（不是为了完全委派）

新DMARC记录

在RN >中，首先必须使用DMARC支持更新所有子域



