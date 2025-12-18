---
solution: Journey Optimizer
product: journey optimizer
title: 使用Journey Optimizer API
description: Journey Optimizer提供了RESTful API，允许您以编程方式在应用程序中执行关键操作。 了解如何访问和使用它们。
feature: Integrations, Data Ingestion
role: Developer
level: Intermediate
exl-id: 4c897c52-6eb2-4d6e-aaa9-9bd83608b2b6
source-git-commit: f0b9eb87608eb8183cf0b08926b1dee695634e11
workflow-type: tm+mt
source-wordcount: '529'
ht-degree: 7%

---

# 使用[!DNL Journey Optimizer] API {#apis-gs}

## 快速访问 {#quick-access}

浏览[完整API引用](https://developer.adobe.com/journey-optimizer-apis/){target="_blank"}以访问所有Journey Optimizer API并直接对其进行测试。 若要开始，请确保[设置身份验证](https://developer.adobe.com/journey-optimizer-apis/references/authentication/){target="_blank"}以收集所需的凭据。

## 概述 {#overview}

Adobe Journey Optimizer API允许您跨任何应用程序、设备或渠道提供个性化、互联且及时的客户体验，从而有效地管理端到端客户历程。 客户历程是客户与品牌互动的整个过程，从接触的第一刻起直到客户离开。 这个过程从认知阶段开始，在这个阶段，客户了解到品牌并开始接触品牌。然后，客户将进一步与品牌互动，访问在线和实体网站，进行购买、发送消息或发布评论。

Adobe Journey Optimizer原生构建于Adobe Experience Platform之上，它将统一的实时客户档案、API优先的开放框架、集中式Offer Decisioning、人工智能(AI)和机器学习(ML)整合在一起，以便进行个性化和优化。 通过与Journey Optimizer API集成，品牌厂商可以在整个客户历程中以智能化的方式，通过规模、速度和灵活性确定下一个最佳的互动。

**开始使用Journey Optimizer API：**

* **[浏览完整的API引用](https://developer.adobe.com/journey-optimizer-apis/){target="_blank"}** — 访问所有Journey Optimizer API并直接对其进行测试
* **[设置身份验证](https://developer.adobe.com/journey-optimizer-apis/references/authentication/){target="_blank"}** — 收集所需的凭据以开始使用API
* **[决策管理API](../offers/api-reference/getting-started.md)** — 以编程方式管理优惠和决策
* **[Experience Decisioning API](../experience-decisioning/api-reference/getting-started.md)** — 使用基于代码的体验交付个性化的决策项

## 身份验证 {#authentication}

在使用Journey Optimizer API之前，必须设置身份验证以访问API端点。

按照[身份验证指南](https://developer.adobe.com/journey-optimizer-apis/references/authentication/){target="_blank"}收集所有Journey Optimizer API所需的身份验证凭据。

## API文档 {#api-documentation}

完整的Adobe Journey Optimizer API文档包含有关所有可用端点、请求/响应格式和交互式测试功能的详细信息。

访问[Adobe Journey Optimizer API文档](https://developer.adobe.com/journey-optimizer-apis/){target="_blank"}并浏览&#x200B;**API引用**&#x200B;菜单以浏览所有可用的API。

## 决策管理API {#decision-management-apis}

Journey Optimizer为决策管理提供了专用的API，允许您以编程方式管理优惠、决策和投放。

请参阅[决策管理API开发人员指南](../offers/api-reference/getting-started.md)以开始使用Offer Decisioning API。

## Experience Decisioning API {#experience-decisioning-apis}

Journey Optimizer还提供Experience Decisioning API以通过基于代码的体验交付个性化的决策项目。 Experience Decisioning通过决策项目、资格规则和选择策略提供了一种简化的个性化方法。

**可用API操作：**

* **决策项** — 创建、读取、更新和删除决策项
* **选择策略** — 定义如何选择和排名决策项
* **资格规则** — 设置项目资格条件
* **项集合** — 将决策项组织到集合中
* **排名公式** — 配置自定义排名逻辑
* **投放位置** — 定义决策项可以出现的位置

在[Experience Decisioning API引用](../experience-decisioning/api-reference/getting-started.md)中了解更多信息，并探索如何[使用基于代码的体验来提供选件](../experience-decisioning/gs-experience-decisioning.md)。

## 相关主题 {#related-topics}

**API文档和指南**

* [Adobe Journey Optimizer API引用](https://developer.adobe.com/journey-optimizer-apis/){target="_blank"}
* [身份验证指南](https://developer.adobe.com/journey-optimizer-apis/references/authentication/){target="_blank"}
* [决策管理 API 开发人员指南](../offers/api-reference/getting-started.md)
* [Experience Decisioning API参考](../experience-decisioning/api-reference/getting-started.md)

**Journey Optimizer集成**

* [与其他解决方案集成](../integrations/ajo-integrations.md)
* [与Adobe Analytics集成](../event/about-analytics.md)
* [集成Adobe Campaign](../building-journeys/using-adobe-campaign-v7-v8.md)

**开发人员资源**

* [Adobe Experience Platform API](https://developer.adobe.com/experience-platform-apis/){target="_blank"}
* [Adobe Developer Console](https://developer.adobe.com/console){target="_blank"}
* [历程中的自定义操作](../action/about-custom-action-configuration.md)
