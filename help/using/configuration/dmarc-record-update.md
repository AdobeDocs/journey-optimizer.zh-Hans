---
solution: Journey Optimizer
product: journey optimizer
title: 强制性DMARC更新
description: 了解必须在Journey Optimizer中设置DMARC记录的原因和时间
feature: Subdomains, Channel Configuration
topic: Administration
role: Admin
level: Experienced
keywords: 子域，域，邮件， dmarc，记录
source-git-commit: 7d5a2a9b80110505688b5bfda2e286c7a6432441
workflow-type: tm+mt
source-wordcount: '520'
ht-degree: 0%

---

# 强制性DMARC更新 {#dmarc-record-update}

>[!CONTEXTUALHELP]
>id="ajo_admin_dmarc_banner_link"
>title="了解有关强制DMARC更新的更多信息"
>abstract="作为执行行业最佳实践的一部分，Google和雅虎都将要求您拥有 **DMARC记录** ，适用于您用来向其发送电子邮件的任何域，从 **2024年2月1日**. <br>因此，您必须确保为已在Journey Optimizer中委派给Adobe的所有子域设置了DMARC记录。"

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
>如果您有任何问题或需要支持，请联系您的Adobe可投放性顾问或您的Adobe代表。

Google和雅虎共享的最新时间表如下：

* Google：

   * **2024年2月**  — 旨在发出不合规警告的临时退回将开始。 如果您尚未遵守相关规定，则在短暂延迟后，电子邮件仍会正常发送。 如果您完全遵循相关说明，将不会出现临时退回，并且您不会受到影响。

   * **2024年4月**  — 对于不符合DMARC要求的发件人，将开始阻止。 最初只会阻止一部分不符合标准的电子邮件，阻止的百分比会随着时间的推移而增加。

   * **2024年6月1日**  — 任何未完全合规的发件人都将遇到阻止问题。

* 雅虎尚未提供具体日期，但表示“将从2024年2月开始实施该法案。 执法将逐步展开”。

>[!NOTE]
>
>了解有关在中实施DMARC的更多信息 [可投放性最佳实践指南](https://experienceleague.adobe.com/docs/deliverability-learn/deliverability-best-practice-guide/additional-resources/technotes/implement-dmarc.html#about){target="_blank"} 以更好地了解对电子邮件可投放性的影响。
