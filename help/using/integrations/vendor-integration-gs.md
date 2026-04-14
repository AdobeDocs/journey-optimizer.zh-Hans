---
solution: Journey Optimizer
product: journey optimizer
title: 供应商集成
description: 将Adobe Journey Optimizer与任何公开有效API的外部平台以及经过工程测试的供应商模式集成使用，以便在您设计设置时提高信心。
feature: Integrations
topic: Content Management
role: User
level: Intermediate
hide: true
keywords: 集成，供应商，第三方
source-git-commit: 9d839f8ac20b80e4abf5bedb881908f4e24964fc
workflow-type: tm+mt
source-wordcount: '370'
ht-degree: 1%

---


# 供应商集成入门 {#vendor-integration}

>[!BEGINSHADEBOX]

目录：

* [使用集成](external-sources.md)
* **[开始使用供应商集成](vendor-integration-gs.md)**
* [可用的供应商](vendor-integration.md)
* [常见问题解答](vendor-integration-faq.md)

>[!ENDSHADEBOX]


当每个系统公开&#x200B;**API终结点**&#x200B;且与集成发出请求和使用响应的方式兼容时，您可在Adobe Journey Optimizer中使用&#x200B;**集成**&#x200B;通过HTTP **调用**&#x200B;外部系统。 有关完整的工作流，请参阅[使用集成](external-sources.md)。

所描述的第三方解决方案列表是说明性的，并非详尽无遗。 在满足产品要求的情况下，可以使用其他平台。

## 作战护栏 {#operational-guardrails}

当您在本指南或类似供应商中配置任何集成时，请应用以下内容：

* **响应格式：**&#x200B;集成映射来自&#x200B;**JSON**&#x200B;响应的字段。 设计调用，以便API返回适合在创作时映射的JSON。
* **有效负载和字段：**&#x200B;仅请求和映射您需要的属性。 较小的响应可减少延迟并限制敏感数据的泄露。
* **终结点形状：**&#x200B;当产品需要目标查找时，首选通过广泛列表或分页终结点进行稳定、**单一资源**&#x200B;检索（例如，一个条目、产品或成员）。 请参阅[限制和排除](#limitations-exclusions)和[使用集成](external-sources.md)。
* **卷和可靠性：**&#x200B;遵守供应商的&#x200B;**速率限制**。 为您的渠道配置&#x200B;**timeout**、**retry**&#x200B;和&#x200B;**cache**&#x200B;策略（例如，批处理电子邮件与事务性发送），并在加载下进行验证。
* **安全性：**&#x200B;根据您组织的策略存储和轮换令牌、API密钥和OAuth凭据。 请勿在消息内容中嵌入密钥。

## 限制和排除 {#limitations-exclusions}

第三方解决方案列表是&#x200B;**说明性的**，而不是详尽的。 供应商API、主机、速率限制和JSON响应形状可能会发生变化。 使用供应商的当前文档和您的订阅确认端点、身份验证和字段映射。 此处的模式假定适合个性化的&#x200B;**面向读取的**&#x200B;调用。 除非另有说明，否则回写、批量导出或非JSON响应可能不在此范围内。

## 快速导航 {#quick-navigation}

使用这些分组链接快速跳转到相关的供应商模式：

* **内容和CMS：** [内容](#contentful)，[Sitecore](#sitecore)，[Salsify](#salsify)，[Contentstack](#contentstack)，[Akeneo](#akeneo)，[木兰](#magnolia)
* **忠诚度和奖励：** [Voucherify](#voucherify)，[Talon.One](#talon-one)，[Antavo](#antavo)，[Salesforce忠诚度](#salesforce-loyalty)，[毛细管](#capillary)
* **模板和消息：** [Stensul](#stensul)，[Marigold](#marigold)，[Adobe Target建议](#adobe-target-recommendations)
* **数据、天气和操作：** [AccuWeather](#accuweather)，[ShipStation](#shipstation)，[RevenueCat](#revenuecat)，[数据库](#databricks)
* **审核、同意和社交：** [Bynder](#bynder)，[Trustpilot](#trustpilot)，[Bazaarvoice](#bazaarvoice)，[OneTrust](#onetrust)，[Meta](#meta)，[Aprimo](#aprimo)，[Epsilon (Epsilon3)](#epsilon)
