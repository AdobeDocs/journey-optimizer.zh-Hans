---
solution: Journey Optimizer
product: journey optimizer
title: AJO架构
description: 架构和与AEP的关系
feature: Get Started
role: Admin, Data Engineer, Developer, User
level: Beginner
redpen-status: PASS_||_2025-04-28_15-13-07
exl-id: f792fdf9-8038-4dd7-a7d5-d931dbf35c3e
hide: true
source-git-commit: f94067ffb421bfd095ed3fcb3001af0e5dc44ab3
workflow-type: tm+mt
source-wordcount: '463'
ht-degree: 0%

---

# 架构

## 全局视图：Adobe Journey Optimizer如何整合

Adobe Journey Optimizer (AJO)和Adobe Experience Platform (AEP)可协同工作，以实现大规模的数据驱动个性化。 此生态系统以持续流的形式运行，收集、分析和应用数据以创建个性化的客户历程。

![](../assets/do-not-localize/get-started-big-picture.png)


### 基础：Adobe Experience Platform (AEP)

Adobe Experience Platform作为骨干，使品牌商能够集中客户数据并激活它以实现个性化体验。

- **数据平台**： AEP作为中央中心运行，用于收集、管理和构建客户数据以确保跨系统的一致性。
- **数据摄取（源）**：品牌使用预建连接器从各种系统（如CRM平台、网站、移动应用程序和云存储）导入数据。 例如，Source连接器从电子商务平台摄取购买数据。
- **实时客户个人资料**：此功能通过合并来自多个来源的数据来创建统一的个人资料。 例如，用户档案将电子邮件交互和店内购买结合使用，可提供客户的完整视图。
- **治理层**：此层管理数据访问、隐私合规性和安全性。 它确保品牌在遵守法规的同时安全地利用客户数据。

### 编排引擎：Adobe Journey Optimizer (AJO)

Adobe Journey Optimizer运用AEP提供的数据和见解，跨各种渠道提供智能、个性化的客户体验。

- **客户了解**：实时客户配置文件允许将目标消息分段为受众。 例如，受众包括通过购买历史记录识别的频繁购物者。
- **内容和选件**：
   - **内容管理**：此功能提供了用于跨渠道创建、管理和个性化内容的工具。 例如，您可以为促销电子邮件标头构建可重复使用的内容片段。
   - **决策管理**：此系统使用实时逻辑为每个人选择最佳优惠或消息。 例如，符合条件的客户可能会根据其浏览历史记录接收折扣选件。
- **历程和促销活动管理**：此功能可自动处理交互序列(历程)或计划一次性定向消息（促销活动）。 例如，历程在产品查看后触发跟进电子邮件。
- **投放（连接）**：
   - **渠道**：此功能通过电子邮件、短信、推送通知和直邮等通信平台发送消息和优惠。
   - **目标**：此功能可将配置文件和受众数据导出到外部系统以进行激活或分析。 例如，将受众数据发送到社交媒体平台以进行广告定位。
- **Measurement &amp; Analysis**：此功能通过报表跟踪客户参与和促销活动效果。 这些见解支持持续改进。

## 连续优化周期

该生态系统作为一个持续优化周期运行。 数据推动客户了解，从而形成个性化内容和决策。 这些功能经过精心编排为历程，跨渠道交付，进行有效性衡量并随着时间的推移而优化。

![](../assets/do-not-localize/get-started-flow.png)

## 详细架构

![Adobe Journey Optimizer架构](assets/ajo-architecture.png)


## 隐私和安全性

Adobe Experience Cloud的隐私和安全实践适用于Adobe Journey Optimizer。 这些措施确保遵守隐私法规，使品牌能够在保持客户信任的同时提供个性化体验。
