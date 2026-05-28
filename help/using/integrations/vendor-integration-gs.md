---
solution: Journey Optimizer
product: journey optimizer
title: 供应商集成
description: 将Adobe Journey Optimizer与任何公开有效API的外部平台以及经过工程测试的供应商模式集成，以便在您设计设置时提高信心。
feature: Integrations
topic: Content Management
role: User
level: Intermediate
keywords: 集成，供应商，第三方
subfeature_v2: []
feature_v2:
  - id: fe96aceb-8194-4a8a-a6b0-75302d02804d
source-git-commit: 0ee10a0689d38c22b1180b197796b08a10c286cf
workflow-type: tm+mt
source-wordcount: 375
ht-degree: 0%

---


# 供应商集成 {#vendor-integration}

当每个系统公开&#x200B;**API终结点**&#x200B;且与集成发出请求和使用响应的方式兼容时，您可在Adobe Journey Optimizer中使用&#x200B;**集成**&#x200B;通过HTTP **调用**&#x200B;外部系统。 有关完整的工作流，请参阅[使用集成](integrations.md)。

所描述的第三方解决方案列表是说明性的，并非详尽无遗。 在满足产品要求的情况下，可以使用其他平台。

## 作战护栏 {#operational-guardrails}

当您在本指南或类似供应商中配置任何集成时，请应用以下内容：

* **响应格式：**&#x200B;集成映射来自&#x200B;**JSON**&#x200B;或&#x200B;**HTML**&#x200B;响应的字段。 设计调用，以便API返回适合在创作时映射的JSON或HTML。
* **有效负载和字段：**&#x200B;仅请求和映射您需要的属性。 较小的响应可减少延迟并限制敏感数据的泄露。
* **终结点形状：**&#x200B;当产品需要目标查找时，首选通过广泛列表或分页终结点进行稳定、**单一资源**&#x200B;检索（例如，一个条目、产品或成员）。 请参阅[限制和排除](#limitations-exclusions)和[使用集成](integrations.md)。
* **卷和可靠性：**&#x200B;遵守供应商的&#x200B;**速率限制**。 为您的渠道配置&#x200B;**timeout**、**retry**&#x200B;和&#x200B;**cache**&#x200B;策略（例如，批处理电子邮件与事务性发送），并在加载下进行验证。
* **安全性：**&#x200B;根据您组织的策略存储和轮换令牌、API密钥和OAuth凭据。 请勿在消息内容中嵌入密钥。


## 限制和排除 {#limitations-exclusions}

第三方解决方案列表是&#x200B;**说明性的**，而不是详尽的。 供应商API、主机、速率限制以及JSON或HTML响应形状可能会发生变化。 使用供应商的当前文档和您的订阅确认端点、身份验证和字段映射。 此处的模式假定适合个性化的&#x200B;**面向读取的**&#x200B;调用。 集成仅支持从&#x200B;**JSON**&#x200B;和&#x200B;**HTML**&#x200B;响应进行映射。 不支持&#x200B;**回写**、**批处理导出**&#x200B;以及任何其他格式的响应。

## 快速导航 {#quick-navigation}

使用这些分组链接快速跳转到相关的供应商模式：

* **内容管理系统：** [内容](vendor-integration.md#contentful)，[Sitecore](vendor-integration.md#sitecore)，[Salsify](vendor-integration.md#salsify)，[内容栈栈](vendor-integration.md#contentstack)，[Akeneo](vendor-integration.md#akeneo)，[Magnolia](vendor-integration.md#magnolia)
* **忠诚度和奖励：** [Voucherify](vendor-integration.md#voucherify)，[Talon.One](vendor-integration.md#talon-one)，[Antavo](vendor-integration.md#antavo)，[Salesforce忠诚度](vendor-integration.md#salesforce-loyalty)，[毛细管](vendor-integration.md#capillary)
* **模板、个性化和推荐：** [Stensul](vendor-integration.md#stensul)，[Marigold](vendor-integration.md#marigold)，[Adobe Target推荐](vendor-integration.md#adobe-target-recommendations)
* **数据、天气和操作：** [AccuWeather](vendor-integration.md#accuweather)，[ShipStation](vendor-integration.md#shipstation)，[RevenueCat](vendor-integration.md#revenuecat)，[数据库](vendor-integration.md#databricks)
* **评论、同意和社交：** [Bynder](vendor-integration.md#bynder)，[Trustpilot](vendor-integration.md#trustpilot)，[Bazaarvoice](vendor-integration.md#bazaarvoice)，[OneTrust](vendor-integration.md#onetrust)，[Meta](vendor-integration.md#meta)，[Aprimo](vendor-integration.md#aprimo)，[Epsilon (Epsilon3)](vendor-integration.md#epsilon)
