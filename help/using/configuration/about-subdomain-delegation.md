---
solution: Journey Optimizer
product: journey optimizer
title: ' [!DNL Journey Optimizer]中的子域委派'
description: 了解如何委派子域
feature: Subdomains
topic: Administration
role: Admin
level: Experienced
keywords: 子域，优化器，委派
exl-id: 1b5ca4db-44d9-49e2-ab39-a1abba223ec7
source-git-commit: 8b755351e25ecae9a2058e63919d6512ea0bf153
workflow-type: tm+mt
source-wordcount: '982'
ht-degree: 28%

---

# [!DNL Journey Optimizer] 中的子域委派 {#subdomain-delegation}

>[!CONTEXTUALHELP]
>id="ajo_admin_delegated_subdomains"
>title="您委派的子域显示在此处。"
>abstract="委派您的首个子域。委派您的首个子域。委派完成后，将创建 PTR 记录并启用电子邮件渠道。"

为电子邮件促销活动创建子域后，品牌商可以将不同类型的流量（例如营销与公司流量）隔离到特定的IP池中以及特定域中，从而加快IP预热过程并全面提高可投放性。

如果您共享某个域，但该域被阻止或添加到阻止列表中，则可能会影响您的公司邮件投放。 但是，特定于您的电子邮件营销通信的域上的信誉问题或阻止将仅影响该电子邮件流。 将您的主域用作发件人或多个邮件流的“发件人”地址也可能破坏电子邮件身份验证，导致阻止您的邮件或将其放入垃圾邮件文件夹中。

>[!CAUTION]
>
>无法使用相同的发送域从[!DNL Adobe Journey Optimizer]和其他产品（如[!DNL Adobe Campaign]或[!DNL Adobe Marketo Engage]）发送消息。

## 为什么要设置子域？ {#why-set-up-subdomains}

子域是域的一个分支，可用于隔离您的品牌或各种类型的流量，例如事务性消息和营销通信。

让我们以“mybrand.com”域为例，该域用于发送交易和营销通信。在这种情况下，您可以决定设置两个子域：

* “info.mybrand.com”子域，用于交易通信（购买确认、密码重置等），
* “marketing.mybrand.com”子域，用于您的潜在电子邮件。

这样，您将能够维护您的域和其他子域的声誉。例如，如果“marketing.mybrand.com”子域由于交付能力不佳而最终被互联网服务提供商加入阻止列表，这将阻止整个“mybrand.com”域和“info.mybrand.com”子域被加入阻止列表。

实施解决方案时，需要针对面向外部的组件：这些组件包括设置要跟踪的链接和网页、显示镜像页面等。

虽然这些要求通过Adobe和客户托管的组件进行管理，但它们包含的URL可供电子邮件的收件人查看。 为避免具有指示底层技术解决方案或托管提供商的URL，可设置子域以使其对电子邮件的收件人透明。

**了解详情**

* 了解如何直接从界面[委派子域](delegate-subdomain.md)
* 了解如何[将Google TXT记录](google-txt.md)添加到子域，以确保将电子邮件成功发送到Gmail地址
* 了解如何[访问为您的子域生成的PTR记录](ptr-records.md)，从而可以通过发送邮件服务器对其进行验证

## 子域配置方法 {#subdomain-delegation-methods}

子域配置允许您配置域的子部分（技术上称为“DNS区域”）以与Adobe Campaign一起使用。

可用的设置方法如下。

### 将子域完全委派给Adobe（推荐） {#full-subdomain-delegation}

[!DNL Journey Optimizer]允许您直接从产品界面将子域完全委派给Adobe。 这样，Adobe将能够控制并维护发送、渲染和跟踪电子邮件营销活动所需的DNS的各个方面，从而作为托管服务来发送消息。

<!--The subdomain is fully delegated to Adobe. Adobe is able to control and maintain all aspects of DNS that are required for delivering, rendering and tracking messages.-->

您可以依靠Adobe来维护所需的DNS基础架构，以满足电子邮件营销发送域的行业标准可投放性要求，同时继续维护和控制内部电子邮件域的DNS。

>[!IMPORTANT]
>
>首选方法是完全子域委派。

在[本节](delegate-subdomain.md#set-up-subdomain)中了解如何将子域完全委派给Adobe。

### 使用 CNAME 设置子域 {#cname-subdomain-setup}

如果您有特定于域的限制策略，并且希望Adobe仅对DNS具有部分控制权，则可以选择在您的一侧执行所有与DNS相关的活动。

CNAME子域设置允许您创建子域，并使用CNAME指向Adobe特定的记录。 使用此配置，您和 Adobe 共同负责维护 DNS，以设置用于发送、渲染和跟踪电子邮件的环境。

>[!CAUTION]
>
>如果贵组织的策略限制完全子域委派方法，则建议使用CNAME方法。 此方法要求您自行维护和管理DNS记录。
>
>Adobe将无法协助更改、维护或管理通过CNAME方法配置的子域的DNS。

在[本节](delegate-subdomain.md#cname-subdomain-setup)中了解如何使用CNAME创建子域以指向Adobe特定的记录。

### 使用自定义子域 {#custom-subdomain-delegation}

通过自定义委派方法，您可以完全控制并维护投放、渲染和跟踪消息所需的DNS的各个方面。

在这种情况下，您完全拥有和管理我们自己的子域，并对在此过程中生成的证书具有完全控制权。

在[本节](delegate-custom-subdomain.md)中了解如何设置自定义域。

## 比较配置方法

下表概述了这些方法的工作原理以及隐含的工作量：

| 配置方法 | 工作原理 | 工作量 |
|---|---|---|
| **完全委派** | 创建子域和命名空间记录。然后，Adobe 将配置 Adobe Campaign 所需的所有 DNS 记录。<br/><br/>在此设置中，Adobe 完全负责管理子域和所有 DNS 记录。 | 低 |
| **CNAME方法** | 创建子域和命名空间记录。然后，Adobe 将提供要放入 DNS 服务器的记录，并在 Adobe Campaign DNS 服务器中配置相应值。<br/><br/>在此设置中，您和 Adobe 共同负责维护 DNS。 | 高 |
| **自定义委派方法** | 创建子域和命名空间记录 — Adobe随后将提供要放置在DNS服务器上的记录。 上传从证书颁发机构获得的SSL证书，并通过验证域所有权和报告电子邮件地址完成反馈循环步骤。<br/><br/>在此设置中，您完全负责维护DNS。 | 非常高 |

有关域委派的其他信息，请参阅[本文档](https://experienceleague.adobe.com/docs/deliverability-learn/deliverability-best-practice-guide/additional-resources/product-specific-resources/campaign/ac-domain-name-setup.html?lang=zh-Hans){target="_blank"}。

如果您对子域配置方法有任何疑问，请联系Adobe或联系客户关怀团队以请求可交付性咨询。


