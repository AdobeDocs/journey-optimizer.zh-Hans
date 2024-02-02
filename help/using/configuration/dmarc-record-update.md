---
solution: Journey Optimizer
product: journey optimizer
title: 遵守新的 DMARC 要求
description: 了解必须在Journey Optimizer中设置DMARC记录的原因和时间
feature: Subdomains, Channel Configuration, Deliverability
topic: Administration
role: Admin
level: Experienced
keywords: 子域，域，邮件， dmarc，记录
source-git-commit: cdc3e0ffaddb2ad83ad1703c1858773d09557859
workflow-type: tm+mt
source-wordcount: '575'
ht-degree: 8%

---

# 遵守新的 DMARC 要求 {#dmarc-record-update}

>[!CONTEXTUALHELP]
>id="ajo_admin_dmarc_banner_link"
>title="详细了解强制 DMARC 更新"
>abstract="作为强制执行行业最佳实践的一部分，Google和雅虎都要求您拥有 **DMARC记录** ，适用于您用来向其发送电子邮件的任何域，从 **2024年2月1日**.<br>因此，您必须确保为您在 Journey Optimizer 中委托给 Adobe 的所有子域设置 DMARC 记录。"

基于域的消息身份验证、报告和符合性(DMARC)是一种电子邮件身份验证方法，它允许域所有者保护其域免遭未经授权的使用。 通过向电子邮件提供商/ISP提供明确的策略，它有助于防止恶意行为者发送声称来自您的域的电子邮件。 实施DMARC可降低合法电子邮件被标记为垃圾邮件或拒绝的风险，并改进电子邮件可投放性。

作为强制执行行业最佳实践的一部分，Google和Yahoo！ 都要求 **DMARC记录** 用于向其发送电子邮件的任何域。 此新要求适用于起始日期 **2024年2月1日**. [了解详情](https://experienceleague.adobe.com/docs/deliverability-learn/deliverability-best-practice-guide/additional-resources/guidance-around-changes-to-google-and-yahoo.html#dmarc){target="_blank"}

>[!CAUTION]
>
>未能遵守Gmail和Yahoo的新要求！ 可能导致电子邮件登陆垃圾邮件文件夹或被阻止。

因此，Adobe强烈建议您确保为您已委派给Adobe的所有子域设置DMARC记录 [!DNL Journey Optimizer]. 请按照以下适用于您的案例的步骤执行操作：

* 如果您拥有 [已完全委派](delegate-subdomain.md#full-subdomain-delegation) 按照以下选项之一，将子域发送至Adobe：

   * 在委派的子域的父域上设置DMARC **在您的托管解决方案中**.
或
   * 在委派的子域上设置DMARC **在[!DNL Journey Optimizer]** 配置用户界面 — 无需对托管解决方案执行额外操作。 [了解如何操作](dmarc-record.md#implement-dmarc)

* 如果您已通过设置发送子域 [CNAME](delegate-subdomain.md#cname-subdomain-delegation)，请遵循以下任一选项：

   * 在子域或子域的父域上设置DMARC **在您的托管解决方案中**.
或
   * 在委派的子域上设置DMARC **在[!DNL Journey Optimizer]** 配置用户界面。 [了解如何操作](dmarc-record.md#implement-dmarc)

  但是，通过CNAME委派，您还需要在托管解决方案中输入。 因此，请确保与您的IT部门进行协调，以便他们能够执行中详述的更新 [本节](dmarc-record.md#implement-dmarc).


Google和Yahoo！ 如下所示：

* Google：

   * **2024年2月**  — 旨在发出不合规警告的临时退回将开始。 如果您尚未遵守相关规定，则在短暂延迟后，电子邮件仍会正常发送。 如果您完全遵循相关说明，将不会出现临时退回，并且您不会受到影响。

   * **2024年4月**  — 对于不符合DMARC要求的发件人，将开始阻止。 最初只会阻止一部分不符合标准的电子邮件，阻止的百分比会随着时间的推移而增加。

   * **2024年6月1日**  — 任何未完全合规的发件人都将遇到阻止问题。

* 雅虎！ 尚未提供具体日期，但已表示“执法将从2024年2月开始。 执法将逐步展开”。

>[!NOTE]
>
>如果您有任何问题或需要支持，请联系您的Adobe可投放性顾问或您的Adobe代表。

**有用的链接**

* 要了解有关DMARC的更多信息，请参阅 [可投放性最佳实践指南](https://experienceleague.adobe.com/docs/deliverability-learn/deliverability-best-practice-guide/additional-resources/technotes/implement-dmarc.html#about){target="_blank"}
* 有关这些更改的更多信息，请参阅 [可投放性最佳实践指南](https://experienceleague.adobe.com/docs/deliverability-learn/deliverability-best-practice-guide/additional-resources/guidance-around-changes-to-google-and-yahoo.html){target="_blank"}
* 读取 [Google Gmail公告](https://blog.google/products/gmail/gmail-security-authentication-spam-protection/){target="_blank"}
* 读取 [雅虎！ 公告](https://blog.postmaster.yahooinc.com/post/730172167494483968/more-secure-less-spam){target="_blank"}
