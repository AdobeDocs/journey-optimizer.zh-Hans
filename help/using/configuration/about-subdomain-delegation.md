---
solution: Journey Optimizer
product: journey optimizer
title: 中的子域委派 [!DNL Journey Optimizer]
description: 了解如何委派子域
feature: Application Settings
topic: Administration
role: Admin
level: Intermediate
exl-id: 1b5ca4db-44d9-49e2-ab39-a1abba223ec7
source-git-commit: c6498633fdfdc9442203a3bf980f1b12bd1c6a6b
workflow-type: tm+mt
source-wordcount: '880'
ht-degree: 0%

---

# 中的子域委派 [!DNL Journey Optimizer] {#subdomain-delegation}

通过为电子邮件促销活动创建子域，品牌可以将不同类型的流量（例如，营销与公司流量）隔离到特定IP池中，并使用特定的域，从而加快IP升温过程并提高整体投放能力。 如果您共享某个域，并且该域被阻止或添加到拒绝列表，则可能会影响您的公司邮件投放。 但是，特定于电子邮件营销通信的域名存在的声誉问题或阻止，将仅影响电子邮件的流量。 如果将主域用作多个邮件流的发件人或“发件人”地址，则也可能会中断电子邮件身份验证，从而阻止您的邮件或将其置于垃圾邮件文件夹中。

>[!NOTE]
>
>您不能使用相同的发送域从 [!DNL Adobe Journey Optimizer] 和来自其他产品，例如 [!DNL Adobe Campaign] 或 [!DNL Adobe Marketo Engage].

## 为何设置子域？ {#why-setting-up-subdomains}

子域是域的一个分支，可用于隔离您的品牌或各种类型的流量（例如交易消息和营销通信）。

让我们以“mybrand.com”域为例，该域用于发送交易和营销通信。 在这种情况下，您可以决定设置两个子域：

* “info.mybrand.com”子域，用于交易通信（购买确认、密码重置等），
* “marketing.mybrand.com”子域，用于您的潜在电子邮件。

这样，您将有助于维护您的域和其他子域的声誉。 例如，如果“marketing.mybrand.com”子域由于交付能力不佳而最终被互联网服务提供商添加到阻止列表中，这将阻止整个“mybrand.com”域和“info.mybrand.com”子域被添加到阻止列表中。

实施解决方案时，需要面向外部的组件：这些功能包括设置要跟踪的链接和网页、显示镜像页面等。

虽然这些要求通过Adobe和客户托管的组件进行管理，但它们包含可供电子邮件收件人查看的URL。 为避免拥有指示底层技术解决方案或托管提供商的URL，可以设置子域以使其对电子邮件的收件人透明。

**了解更多**

* 了解如何 [委派子域](delegate-subdomain.md) 直接从界面
* 了解如何 [添加Google TXT记录](google-txt.md) 以确保将电子邮件成功发送到Gmail地址
* 了解如何 [访问PTR记录](ptr-records.md) 为子域生成，允许通过发送邮件服务器来验证

## 子域配置方法 {#subdomain-delegation-methods}

子域配置允许您配置域的子部分（技术上称为“DNS区域”），以与Adobe Campaign一起使用。 可用的设置方法包括：

* **将子域完全委派给Adobe** （推荐）：子域已完全委派给Adobe。 Adobe能够控制和维护发送、渲染和跟踪消息所需的DNS的所有方面。 [了解有关完全子域委派的更多信息](delegate-subdomain.md#full-subdomain-delegation)

* **使用CNAME**:创建子域，并使用CNAME指向Adobe特定的记录。 使用此设置，您和Adobe共同负责维护DNS。 [了解有关CNAME子域委派的更多信息](delegate-subdomain.md#cname-subdomain-delegation)

>[!CAUTION]
>
>* 首选方法是完全子域委派。
>
>* 如果贵组织的策略限制了完整的子域委派方法，则建议使用CNAME方法。 这种方法要求您自行维护和管理DNS记录。 Adobe将无法协助更改、维护或管理通过CNAME方法配置的子域的DNS。


下表概述了这些方法的工作原理以及隐含的工作量：

| 配置方法 | 工作原理 | 工作量 |
|---|---|---|
| **完全委派** | 创建子域和命名空间记录。 然后，Adobe将配置Adobe Campaign所需的所有DNS记录。<br/><br/>在此设置中，Adobe完全负责管理子域和所有DNS记录。 | 低 |
| **CNAME，自定义方法** | 创建子域和命名空间记录。 然后，Adobe将提供要放入DNS服务器的记录，并在Adobe Campaign DNS服务器中配置相应的值。<br/><br/>在此设置中，您和Adobe共同负责维护DNS。 | 高 |

有关域配置的其他信息，请参阅 [本文档](https://experienceleague.adobe.com/docs/deliverability-learn/deliverability-best-practice-guide/additional-resources/product-specific-resources/campaign/ac-domain-name-setup.html).

如果您对子域配置方法有任何疑问，请联系Adobe，或最终联系客户关怀团队以请求可交付性咨询。

## 访问委派的子域 {#access-delegated-subdomains}

所有委派的子域都显示在 **[!UICONTROL Administration]** > **[!UICONTROL Channels]** > **[!UICONTROL Subdomains]** 菜单。 过滤器可帮助您优化列表（委派日期、用户或状态）。

![](assets/subdomain-list.png)

的 **[!UICONTROL Status]** 列提供有关子域委派过程的信息：

* **[!UICONTROL Draft]**:子域委派已另存为草稿。 单击子域名以恢复委派过程，
* **[!UICONTROL Processing]**:子域在使用之前会先执行多项配置检查，
* **[!UICONTROL Success]**:子域已成功完成检查，并可用于投放消息。
* **[!UICONTROL Failed]**:提交子域委派后，一个或多个检查失败。

要使用 **[!UICONTROL Success]** 状态，从列表中将其打开。

![](assets/subdomain-delegated.png)

您可以：

* 检索在委派过程中配置的子域名（只读），以及生成的URL（资源、镜像页面、跟踪URL），

* 将Google网站验证TXT记录添加到子域，以确保对其进行验证(请参阅 [将Google TXT记录添加到子域](google-txt.md))。


>[!CAUTION]
>
>子域配置对所有环境都是通用的。 因此，对子域的任何修改也会影响生产沙箱。
