---
title: 自定义渠道入门
description: 了解如何使用 [!DNL Journey Optimizer]'s Channel Builder to bring any outbound messaging channel into [!DNL Journey Optimizer] 并将其用于营销活动、历程和编排的营销活动。
feature: Channel Configuration
topic: Content Management
role: User
level: Beginner
badge: label="有限发布版" type="Informative"
source-git-commit: 94ca2d9458152fb471e9590d053c4729a4a5134f
workflow-type: tm+mt
source-wordcount: '628'
ht-degree: 4%

---


# 自定义渠道入门 {#get-started-custom-channel}

>[!AVAILABILITY]
>
>此功能为限量发布版。 请联系 Adobe 代表获取访问权限。

<!--Multilingual support, business rules enforcement, and [!DNL Adobe Experience Decisioning] integration are planned for a future release.-->

[!DNL Journey Optimizer]的&#x200B;**自定义渠道**&#x200B;功能允许您将任何出站渠道引入[!DNL Journey Optimizer]，以便将其用于营销活动、历程和编排的营销活动 — 就像任何本机渠道一样。 通过使用&#x200B;**渠道生成器**，管理员可以创建和配置新渠道而无需工程部门参与，营销人员可以立即开始使用这些渠道与客户通信。

## 它能解决什么问题？ {#why-custom-channels}

[!DNL Journey Optimizer]本机支持电子邮件、短信、推送通知、WhatsApp、LINE和其他渠道。 但是，许多组织使用本身未集成的消息传送平台（如WeChat、Kakao Talk、Messenger或外部提供商），并希望在[!DNL Journey Optimizer]中使用它们进行编排和活动创建，同时仍由其自己的供应商提供。

<!--TBC: Another use case is when organizations have a legacy messaging gateway that exposes an HTTP endpoint, and they want to use it in [!DNL Journey Optimizer] without having to build a custom integration.-->

自定义渠道填补了这一空白：它们允许您使用任何出站HTTP端点作为完整的[!DNL Journey Optimizer]渠道，并解锁：

* **全渠道功能** — 优化（内容实验和定位）、OOTB报告和监控、同意和治理实施以及表达式片段。<!--Multilingual and business rules are planned for a future release.-->
* **统一编排** — 在单个位置管理您的所有消息传递渠道，而不管基础的投放提供商。
* **无代码设置** — 管理员通过Channel Builder UI配置渠道；无需自定义代码或工程操作。

## 自定义渠道与自定义操作 {#custom-channel-vs-custom-action}

如果您以前在[!DNL Journey Optimizer]历程中使用过[自定义操作](../action/action.md)，则自定义渠道会处理一组不同的用例。

**在**&#x200B;您需要通过[!DNL Journey Optimizer]本身不支持的平台（如WeChat、Kakao Talk或自定义消息传递网关）向最终用户发送消息时使用自定义渠道。 自定义渠道适用于营销活动、历程和编排的营销活动以及支持：

* 通过个性化编辑器实现完全个性化，与原生出站渠道类似
* 可视化/表单有效负载编辑器、预览和验证
* 内容实验和定位
* OOTB报告和监控
* 多个API凭据和渠道配置
* RBAC/ABAC

自定义渠道支持POST作为唯一的HTTP方法。

**在**&#x200B;您需要从外部系统（如呼叫中心、日志平台或离线数据库）检索数据或将信息推送到外部系统时，使用自定义操作作为历程中的步骤。 自定义操作仅在历程中可用，并支持GET、PUT和POST方法。

<!--
| | Custom Action | Custom Channel |
| --- | --- | --- |
| **Primary use case** | Retrieve data from or send information to external systems (call centers, offline systems, logging) | Send messages to end users through channels not natively supported in [!DNL Journey Optimizer] |
| **Available in** | Journeys only | Campaigns, journeys, and orchestrated campaigns |
| **Supported HTTP methods** | GET, PUT, POST | POST only |
| **Full personalization (PE)** | No | Yes, through the personalization editor, similar to native outbound channels |
| **Visual/form editor** | No | Yes |
| **Preview and proof** | No | Yes |
| **Content experimentation** | No | Yes |
| **Targeting** | No | Yes |
| **OOTB Reporting** | Yes | Yes |
| **Multiple API credentials and channel configurations** | No | Yes |
| **RBAC/ABAC** | No | Yes |
-->

>[!TIP]
>
>作为一般建议，请将自定义渠道用于向最终用户发送消息的渠道用例。 对于历程中需要的其他连接器样用例（例如检索数据或触发外部系统），您可以继续使用自定义操作。

## 用例 {#use-cases}

自定义渠道非常适合：

* **不受支持的消息传送平台** — 微信、Kakao Talk、Messenger、Telegram等频道或没有本机[!DNL Journey Optimizer]频道的地区消息传送服务。
* **自定义投放提供商** — 已投资于外部提供商且希望继续使用外部提供商进行邮件投放的组织，但更愿意利用[!DNL Journey Optimizer]进行编排、个性化和营销活动管理。
* **旧渠道** — 公开HTTP端点的专有或旧版消息传递网关。
* **特定于行业的渠道** — 医疗保健、银行警报系统或政府通知服务的安全消息。

## 工作原理 {#how-it-works}

设置和使用自定义渠道遵循以下主要阶段：

1. **配置** （管理员） — 管理员在&#x200B;**渠道生成器**&#x200B;中创建自定义渠道，定义终结点、身份验证、限制策略和消息有效负载结构。 然后，创建渠道配置并将其链接到自定义渠道。 [了解详情](configure-custom-channel.md)
1. **创建**（营销人员） — 营销人员将自定义渠道添加到历程、营销活动或编排的营销活动，选择渠道配置，并使用[!DNL Journey Optimizer]的个性化编辑器创作消息有效负载。 [了解详情](create-custom-experience.md)
1. **发送** — 当配置文件符合条件时，[!DNL Journey Optimizer]将个性化有效负载发送到配置的端点。 外部系统处理呼叫并传递消息。
1. **监视器** （管理员/营销人员） — 管理员和营销人员可以通过[!DNL Journey Optimizer]的报告和监视功能板监视自定义渠道的性能和可靠性。 [了解详情](monitor-custom-channel.md)

<!--
## Next steps {#next-steps}

* Review the prerequisites and permissions before setting up your first custom channel. [Learn more](custom-channel-prerequisites.md)
* Configure your first custom channel using the Channel Builder. [Learn more](custom-channel-configuration.md)
* Create a custom channel experience in a journey or campaign. [Learn more](create-custom-experience.md)
-->
