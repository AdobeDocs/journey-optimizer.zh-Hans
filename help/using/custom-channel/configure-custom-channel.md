---
title: 配置自定义渠道 — 概述
description: 了解管理员在Adobe Journey Optimizer中配置自定义渠道时必须完成的步骤，从创建渠道到设置渠道配置。
feature: Channel Configuration
topic: Content Management
role: Admin
level: Experienced
badge: label="有限发布版" type="Informative"
source-git-commit: 4556e8b50fe71cf9d703d034a3c5772b8fea9d33
workflow-type: tm+mt
source-wordcount: '355'
ht-degree: 9%

---


# 配置自定义渠道 {#custom-channel-configuration}

>[!AVAILABILITY]
>
>此功能为限量发布版。 请联系 Adobe 代表获取访问权限。

配置自定义渠道是管理员任务，每个渠道发生一次。 配置渠道后，营销人员可以立即在营销活动、历程和编排的营销活动中选择它 — 就像任何本机[!DNL Journey Optimizer]渠道一样。

配置过程包括四个步骤：定义渠道本身（端点、身份验证、有效负载），管理用于验证请求的API凭据，可以选择委派子域进行链接跟踪，以及最终创建营销人员将在创作时选择的渠道配置。

>[!NOTE]
>
>在开始之前，请查看自定义渠道的先决条件和护栏，包括所需的权限和支持的身份验证方法。

## 配置步骤 {#steps}

自定义渠道的配置过程包括四个步骤。 以下链接文章详细介绍了每个步骤。

| 步骤 | 您所做的工作 | 为什么这很重要 | 链接 |
| --- | --- | --- | --- |
| **1. 创建自定义渠道** | 在渠道生成器中定义端点URL、标头、限制策略、身份验证类型和消息有效负载结构。 | 这是渠道的核心定义。 它可告知[!DNL Journey Optimizer]如何发送消息以及该消息的外观。 | [了解详情](create-custom-channel.md) |
| **2. 管理API凭据** | 创建和管理用于向端点验证请求的凭据集。 | 通过多个凭据集，您可以跨不同的品牌或环境重复使用相同的渠道定义，而无需复制渠道。 | [了解详情](custom-channel-api-credentials.md) |
| **3. 委派子域** *（可选）* | 专门为您的自定义渠道委派子域。 | 仅当消息有效负载包含可跟踪链接时才需要。 如果没有委派的子域，此渠道将无法进行链接跟踪。 | [了解详情](custom-channel-subdomains.md) |
| **4. 创建渠道配置** | 创建命名预设，将自定义渠道链接到一组特定的凭据、子域和可选的有效负载默认值。 | 在构建营销活动或历程时，营销人员会选择一个自定义渠道和一个关联的渠道配置。 您可以为同一渠道创建多个配置（例如，每个品牌或区域一个配置）。 | [了解详情](custom-channel-configuration.md) |

<!--
## Get started {#get-started}

1. [Create the custom channel](create-custom-channel.md) by defining its endpoint, authentication method, and message payload structure in the Channel Builder.
1. [Set up API credentials](custom-channel-api-credentials.md) to authenticate requests sent to your endpoint — required for all authentication types other than **None**.
1. [Delegate a subdomain](custom-channel-subdomains.md) if your message payload includes trackable links and you want them served from a branded domain.
1. [Create a channel configuration](custom-channel-configuration.md) to produce the named preset that marketers will select when building campaigns and journeys.


-->