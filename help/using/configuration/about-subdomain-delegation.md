---
solution: Journey Optimizer
product: journey optimizer
title: 中的子域委派 [!DNL Journey Optimizer]
description: 了解如何委派子域
feature: Application Settings
topic: Administration
role: Admin
level: Intermediate
keywords: 子域，优化器，委派
exl-id: 1b5ca4db-44d9-49e2-ab39-a1abba223ec7
source-git-commit: b8065a68ed73102cb2c9da2c2d2675ce8e5fbaad
workflow-type: tm+mt
source-wordcount: '900'
ht-degree: 26%

---

# 中的子域委派 [!DNL Journey Optimizer] {#subdomain-delegation}

为电子邮件促销活动创建子域后，品牌商可以将不同类型的流量（例如营销与公司流量）隔离到特定的IP池中以及特定域中，从而加快IP预热过程并提高整体可投放性。 如果您共享某个域，但该域被阻止或添加到阻止列表中，则可能会影响您的公司邮件投放。 但是，特定于您的电子邮件营销通信的域上的信誉问题或阻止将仅影响该电子邮件流。 将您的主域用作发件人或多个邮件流的“发件人”地址也可能破坏电子邮件身份验证，导致阻止您的邮件或将其放入垃圾邮件文件夹中。

>[!NOTE]
>
>无法使用相同的发送域发送消息 [!DNL Adobe Journey Optimizer] 以及从其他产品(如 [!DNL Adobe Campaign] 或 [!DNL Adobe Marketo Engage].

## 为什么要设置子域？ {#why-set-up-subdomains}

子域是域的一个分支，可用于隔离您的品牌或各种类型的流量，例如事务性消息和营销通信。

让我们以“mybrand.com”域为例，该域用于发送交易和营销通信。在这种情况下，您可以决定设置两个子域：

* “info.mybrand.com”子域，用于交易通信（购买确认、密码重置等），
* “marketing.mybrand.com”子域，用于您的潜在电子邮件。

这样，您将能够维护您的域和其他子域的声誉。例如，如果“marketing.mybrand.com”子域由于交付能力不佳而最终被互联网服务提供商加入阻止列表，这将阻止整个“mybrand.com”域和“info.mybrand.com”子域被加入阻止列表。

实施解决方案时，需要针对面向外部的组件：这些组件包括设置要跟踪的链接和网页、显示镜像页面等。

虽然这些要求通过Adobe和客户托管的组件进行管理，但它们包含的URL可供电子邮件的收件人查看。 为避免具有指示底层技术解决方案或托管提供商的URL，可设置子域以使其对电子邮件的收件人透明。

**了解详情**

* 了解如何 [委派子域](delegate-subdomain.md) 直接从界面
* 了解如何 [添加Google TXT记录](google-txt.md) 子域，以确保将电子邮件成功发送到Gmail地址
* 了解如何 [访问PTR记录](ptr-records.md) 为子域生成，允许通过发送邮件服务器来验证它们

## 子域配置方法 {#subdomain-delegation-methods}

子域配置允许您配置域的子部分（技术上称为“DNS区域”）以与Adobe Campaign一起使用。 可用的设置方法包括：

* **将子域完全委派给 Adobe**（推荐）：将子域完全委派给 Adobe。Adobe能够控制和维护投放、渲染和跟踪消息所需的DNS的各个方面。 [了解有关完全子域委派的更多信息](delegate-subdomain.md#full-subdomain-delegation)

* **CNAME的使用**：创建子域并使用CNAME指向Adobe特定的记录。 使用此设置，您和Adobe共同负责维护DNS。 [了解有关CNAME子域委派的更多信息](delegate-subdomain.md#cname-subdomain-delegation)

>[!CAUTION]
>
>* 首选方法是完全子域委派。
>
>* 如果贵组织的策略限制完全子域委派方法，则建议使用CNAME方法。 此方法要求您自行维护和管理DNS记录。 Adobe将无法协助更改、维护或管理通过CNAME方法配置的子域的DNS。

下表概述了这些方法的工作原理以及隐含的工作量：

| 配置方法 | 工作原理 | 工作量 |
|---|---|---|
| **完全委派** | 创建子域和命名空间记录。然后，Adobe 将配置 Adobe Campaign 所需的所有 DNS 记录。<br/><br/>在此设置中，Adobe 完全负责管理子域和所有 DNS 记录。 | 低 |
| **CNAME，自定义方法** | 创建子域和命名空间记录。然后，Adobe 将提供要放入 DNS 服务器的记录，并在 Adobe Campaign DNS 服务器中配置相应值。<br/><br/>在此设置中，您和 Adobe 共同负责维护 DNS。 | 高 |

有关域配置的其他信息，请参见 [本文档](https://experienceleague.adobe.com/docs/deliverability-learn/deliverability-best-practice-guide/additional-resources/product-specific-resources/campaign/ac-domain-name-setup.html).

如果您对子域配置方法有任何疑问，请联系Adobe，或最终联系客户关怀团队以请求可交付性咨询。

## 访问委派的子域 {#access-delegated-subdomains}

您委派的所有子域都将显示在 **[!UICONTROL 管理]** > **[!UICONTROL 渠道]** > **[!UICONTROL 子域]** 菜单。 筛选器可帮助您优化列表（委派日期、用户或状态）。

![](assets/subdomain-list.png)

此 **[!UICONTROL 状态]** 列提供了有关子域委派过程的信息：

* **[!UICONTROL 草稿]**：子域委派已另存为草稿。 单击子域名以继续执行委派过程，
* **[!UICONTROL 正在处理]**：子域在可以使用之前将进行多次配置检查，
* **[!UICONTROL 成功]**：子域已成功通过检查，可用于投放消息，
* **[!UICONTROL 失败]**：提交子域委派后，一项或多项检查失败。

要访问子域的详细信息，请使用 **[!UICONTROL 成功]** 状态，从列表中将其打开。

![](assets/subdomain-delegated.png)

您可以：

* 检索在委派过程中配置的子域名（只读），以及生成的URL（资源、镜像页面、跟踪URL），

* 将Google网站验证TXT记录添加到子域，以确保对其进行验证(请参阅 [将Google TXT记录添加到子域](google-txt.md))。


>[!CAUTION]
>
>子域配置对所有环境通用。 因此，对子域的任何修改也会影响生产沙箱。
