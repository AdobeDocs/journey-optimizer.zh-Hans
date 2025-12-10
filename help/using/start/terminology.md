---
solution: Journey Optimizer
product: journey optimizer
title: 关键术语
description: Adobe Journey Optimizer中的基本术语和概念
feature: Get Started
role: Admin, Developer, User
level: Beginner
source-git-commit: 965bb76529f500d6fa4d89fa1d56979afe9d5bb0
workflow-type: tm+mt
source-wordcount: '753'
ht-degree: 8%

---

# 关键术语 {#key-terminology}

本参考指南定义了您在使用Adobe Journey Optimizer时将会遇到的基本术语。 了解这些概念有助于您放心地导航平台并与团队进行有效协作。

>[!TIP]
>
>有关功能和工作流的详细说明，请参阅本指南中链接的特定文档部分。

## 核心平台术语 {#core-terms}

| 术语 | 定义 |
|------|------------|
| **Adobe Journey Optimizer (AJO)** | 用于跨渠道（电子邮件、短信、推送通知、Web）为客户创建和投放个性化消息的应用程序。 它使您能够设计响应实时客户操作的客户历程。 |
| **Adobe Experience Platform (AEP)** | Adobe Journey Optimizer的基础，用于在一个位置收集并组织所有客户数据。 它会创建Journey Optimizer用于个性化的统一客户配置文件。 [了解详情](https://experienceleague.adobe.com/docs/experience-platform/landing/home.html?lang=zh-Hans){target="_blank"} |
| **实时客户轮廓** | 每个客户的统一实时视图，该视图将来自多个渠道的数据（包括在线、离线、CRM和第三方数据）整合在一起。 每个配置文件会随着客户与您的品牌互动而动态更新。 [了解详情](../audience/get-started-profiles.md) |
| **沙盒** | 用于测试和试验的单独工作区，不会影响实时客户通信。 Adobe Journey Optimizer为开发、测试和生产环境提供了多个沙盒。 [了解详情](../administration/sandboxes.md) |

## 历程和促销活动术语 {#journey-campaign-terms}

| 术语 | 定义 |
|------|------------|
| **历程** | 一系列相互关联的步骤，可指导客户逐步体验您的品牌。 每个步骤均基于客户操作或时间触发器执行，从而实现顺序的个性化交互。 [了解详情](../building-journeys/journey.md) |
| **Campaign** | 发送给特定受众的单个通信或一组通信。 与随时间变化的历程不同，营销活动按计划或触发器立即或在特定时间投放消息。 [了解详情](../campaigns/get-started-with-campaigns.md) |
| **活动** | 触发或推进历程的操作或发生次数。 事件可以是客户操作（购买、放弃购物车）或系统事件（日期/时间、数据更改）。 [了解详情](../event/about-events.md) |
| **频道** | 用于与客户通信的方法：电子邮件、短信、推送通知、应用程序内消息、Web或直邮。 每个渠道都需要进行特定的配置。 [了解详情](../configuration/get-started-configuration.md) |

## 客户和受众术语 {#customer-audience-terms}

| 术语 | 定义 |
|------|------------|
| **受众** | 一组具有共同特征或行为的客户，例如“过去30天内购买过的客户”或“忠诚度计划成员”。 受众用于定位特定的客户区段。 [了解详情](../audience/about-audiences.md) |
| **受众资格** | 客户加入或离开受众时发生的自动过程。 Journey Optimizer可以在用户进入或退出受众时触发操作，从而确保及时且相关的通信。 [了解详情](../building-journeys/audience-qualification-events.md) |
| **可参与受众** | 您可以根据许可协议通过Adobe Journey Optimizer积极联系的客户配置文件数。 这通常是指过去12个月内参与的用户档案。 |
| **测试配置文件** | 虚拟用户档案，用于在发送给真实客户之前测试和预览消息。 测试配置文件有助于验证个性化、内容和历程逻辑。 [了解详情](../audience/creating-test-profiles.md) |

## 内容和Personalization术语 {#content-terms}

| 术语 | 定义 |
|------|------------|
| **个性化** | 使用个人资料数据、偏好和行为为个人客户定制内容的过程。 例如，插入客户名称或显示基于浏览历史记录的产品推荐。 [了解详情](../personalization/personalize.md) |
| **内容模板** | 可重复使用的消息设计，可用于多个营销活动和历程，以维护品牌一致性并加快内容创建。 [了解详情](../content-management/content-templates.md) |
| **片段** | 可重复使用的内容块（如页眉、页脚或促销横幅），可用于多种消息，以确保一致性并启用集中更新。 [了解详情](../content-management/fragments.md) |
| **登陆页面** | 独立的网页，客户可以在其中选择加入或选择退出通信、订阅服务或通过在线表单提供信息。 [了解详情](../landing-pages/get-started-lp.md) |

## 决策和优惠条款 {#decision-terms}

| 术语 | 定义 |
|------|------------|
| **决策管理** | 一种功能，可根据实时配置文件数据、上下文和业务规则自动为每个客户选择最佳内容或选件。 [了解详情](../offers/get-started/starting-offer-decisioning.md) |
| **选件** | 可以向客户展示的营销消息、折扣或促销。 优惠包括资格规则，用于确定哪些客户可以接收这些优惠。 [了解详情](../offers/offer-library/creating-personalized-offers.md) |
| **决策策略** | 一组规则和策略，用于根据资格、优先级和上限规则等限制确定在什么时间向哪个客户显示哪个优惠。 [了解详情](../experience-decisioning/create-decision.md) |

## 数据和配置条款 {#data-config-terms}

| 术语 | 定义 |
|------|------------|
| **架构** | 定义如何在Adobe Experience Platform中组织数据的结构，包括字段名称、数据类型和关系。 架构可确保跨系统的数据一致性。 [了解详情](../data/get-started-schemas.md) |
| **数据集** | 遵循特定模式的数据集合（通常是表）。 数据集存储客户数据、交互事件以及用于个性化的其他信息。 [了解详情](../data/get-started-datasets.md) |

>[!NOTE]
>
>有关Adobe Experience Platform术语的完整术语表，请参阅[Adobe Experience Platform术语表](https://experienceleague.adobe.com/docs/experience-platform/landing/glossary.html){target="_blank"}。

## 相关主题 {#related-topics}

* [了解Journey Optimizer的工作原理](understanding-ajo.md)
* [用户界面入门](user-interface.md)
* [选择您的角色和学习路径](quick-start.md)

