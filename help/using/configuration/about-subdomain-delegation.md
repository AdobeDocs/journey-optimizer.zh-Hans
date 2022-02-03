---
title: 委派子域
description: 了解如何委派子域
internal: n
snippet: y
feature: Application Settings
topic: Administration
role: Admin
level: Intermediate
exl-id: 1b5ca4db-44d9-49e2-ab39-a1abba223ec7
source-git-commit: bbc2adabac63ffb813ea2630f29aec552fc3f4df
workflow-type: tm+mt
source-wordcount: '637'
ht-degree: 36%

---

# 中的子域委派 [!DNL Journey Optimizer] {#subdomain-delegation}

通过为电子邮件促销活动创建子域，品牌可以将不同类型的流量（例如，营销与公司流量）隔离到特定IP池中，并使用特定的域，从而加快IP升温过程并提高整体投放能力。 如果您共享域，并且该域被阻止或添加到阻止列表中，则可能会影响您的公司邮件投放。 但是，特定于电子邮件营销通信的域名存在的声誉问题或阻止，将仅影响电子邮件的流量。 如果将主域用作多个邮件流的发件人或“发件人”地址，则也可能会中断电子邮件身份验证，从而阻止您的邮件或将其置于垃圾邮件文件夹中。

## 为什么要设置子域？ {#why-setting-up-subdomains}

子域是域的一个分支，可用于隔离您的品牌或各种类型的流量（例如交易消息和营销通信）。

让我们以“mybrand.com”域为例，该域用于发送交易和营销通信。在这种情况下，您可以决定设置两个子域：

* “info.mybrand.com”子域，用于交易通信（购买确认、密码重置等），
* “marketing.mybrand.com”子域，用于您的潜在电子邮件。

这样，您将能够维护您的域和其他子域的声誉。例如，如果“marketing.mybrand.com”子域由于交付能力不佳而最终被互联网服务提供商加入阻止列表，这将阻止整个“mybrand.com”域和“info.mybrand.com”子域被加入阻止列表。

实施解决方案时，需要面向外部的组件：这些功能包括设置要跟踪的链接和网页、显示镜像页面等。

虽然这些要求通过由Adobe和客户托管的组件进行管理，但它们包含可供电子邮件收件人查看的URL。 为避免拥有指示底层技术解决方案或托管提供商的URL，可以设置子域以使其对电子邮件的收件人透明。

**了解详情**

* 了解如何 [委派子域](delegate-subdomain.md) 直接从界面
* 了解如何 [添加Google TXT记录](google-txt.md) 以确保将电子邮件成功发送到Gmail地址
* 了解如何 [访问PTR记录](ptr-records.md) 为子域生成，允许通过发送邮件服务器来验证

## 子域配置方法 {#subdomain-delegation-methods}

子域配置允许您配置域的子部分（技术上称为“DNS区域”）以与Adobe Campaign一起使用。 可用的设置方法包括：

* **将子域完全委派给 Adobe**（推荐）：将子域完全委派给 Adobe。Adobe能够控制和维护发送、渲染和跟踪消息所需的DNS的所有方面。 [了解有关完全子域委派的更多信息](delegate-subdomain.md#full-subdomain-delegation)

* **使用CNAME**:创建子域，并使用CNAME指向特定于Adobe的记录。 使用此设置，您和Adobe都有责任维护DNS。 [了解有关CNAME子域委派的更多信息](delegate-subdomain.md#cname-subdomain-delegation)

下表概述了这些方法的工作原理以及隐含的工作量：

| 配置方法 | 工作原理 | 工作量 |
|---|---|---|
| **完全委派** | 创建子域和命名空间记录。然后，Adobe 将配置 Adobe Campaign 所需的所有 DNS 记录。<br/><br/>在此设置中，Adobe 完全负责管理子域和所有 DNS 记录。 | 低 |
| **CNAME，自定义方法** | 创建子域和命名空间记录。然后，Adobe 将提供要放入 DNS 服务器的记录，并在 Adobe Campaign DNS 服务器中配置相应值。<br/><br/>在此设置中，您和 Adobe 共同负责维护 DNS。 | 高 |

有关域配置的其他信息，请参阅 [本文档](https://experienceleague.adobe.com/docs/deliverability-learn/deliverability-best-practice-guide/additional-resources/product-specific-resources/campaign/ac-domain-name-setup.html).

如果您对子域配置方法有任何疑问，请联系Adobe，或最终联系客户关怀团队以请求可交付性咨询。
