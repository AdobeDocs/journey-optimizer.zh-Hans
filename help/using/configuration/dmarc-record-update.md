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
hide: true
hidefromtoc: true
source-git-commit: 5565c98e41e0abc9ae93f85cb12679e372e6d36f
workflow-type: tm+mt
source-wordcount: '440'
ht-degree: 0%

---

# DMARC记录重要更新{#dmarc-record}


>[!CAUTION]
>
>继最近在Gmail和Yahoo上宣布推出批量发件人功能后，Journey Optimizer现在支持DMARC身份验证技术。

作为强制执行行业最佳实践的一部分，Google和雅虎都将要求您拥有DMARC记录，才能用于向其发送电子邮件。 此新要求开始于 **2024年2月1日**.

在中了解有关Google和雅虎对DMARC记录要求的更多信息 [本节](https://experienceleague.adobe.com/docs/deliverability-learn/deliverability-best-practice-guide/additional-resources/guidance-around-changes-to-google-and-yahoo.html?lang=en#dmarc%3A){target="_blank"}.

在Google和Yahoo上了解更多已宣布的更改 [此页面](https://experienceleague.adobe.com/docs/deliverability-learn/deliverability-best-practice-guide/additional-resources/guidance-around-changes-to-google-and-yahoo.html?lang=en#dmarc%3A){target="_blank"}.

接下来，您将看到一个操作或下一步骤，其中将声明：

您必须为所有子域设置它
* 如果您已将域完全委派给我们，则您有两个选项
   * 在您的托管解决方案中的委派域的父域上设置DMARC，或者
   * 使用我们即将在管理员UI中使用的功能在委派域上设置DMARC，无需在托管解决方案上额外工作
* 如果您为发送域设置了CNAME，则您有两个选项
   * 在托管解决方案的子域或子域的父域上设置DMARC，或者
   * 使用我们即将在管理员UI中使用的功能设置DMARC。 但是，它不仅需要我们的UI，还需要输入托管解决方案。

有关我们即将推出的功能的更多详细信息即将推出。

此外，如果未设置，则可以通过从以下部分（从上面的链接复制）复制与DMARC相关的部分来包含影响。 要么我们只拿出与DMARC相关的东西。 或者，您可以在此处了解此公告适用于DMARC和一次单击取消订阅，以下是这两项功能的最新时间线。

自今年10月最初宣布以来，有关时间表一直更新。

最新的时间表如下所示：

Gmail：

* 2024年2月 — 旨在发出不合规警告的临时退回将开始。 如果您尚未遵守相关规定，则在短暂延迟后，电子邮件仍会正常发送。 如果您完全符合要求，则不会出现临时退回，也不会有任何发现。
* 2024年4月 — 对于除List-Unsubscribe 1-Click之外的所有其他内容都不合规的发件人，将开始阻止这些发件人。 最初只会阻止一部分不合规的电子邮件，阻止的%会随着时间的推移而增加。
* 2024年6月1日 — 任何未完全合规的发件人（包括List-Unsubscribe 1-Click）都将遇到阻止问题。

雅虎：

尚未提供具体日期，但已表示“执法将从2024年2月开始。 执法将逐步展开”。
