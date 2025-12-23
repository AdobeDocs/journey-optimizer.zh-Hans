---
solution: Journey Optimizer
product: journey optimizer
title: 历程入门
description: 历程入门
feature: Journeys, Get Started, Overview
role: User
level: Beginner, Intermediate
keywords: 历程，探索，入门
exl-id: 73cfd48b-72e6-4b72-bbdf-700a32a34bda
version: Journey Orchestration
source-git-commit: a6c80e4326454868d60e9ba335e509f806d3220f
workflow-type: tm+mt
source-wordcount: '1099'
ht-degree: 38%

---


# 历程入门{#jo-general-principle}

Adobe Journey Optimizer 中的历程功能使您能够创建个性化的多步骤客户历程，实时响应受众行为与需求。通过直观的拖放式画布，您可以跨多个渠道编排消息与行动，利用上下文数据和受众定向实现最大影响力。无论您是探索实时触发器、管理历程属性，还是使用自定义操作和表达式等高级工具，本节都提供了一个清晰的路线图，帮助您设计和优化历程，从而提供有意义、及时的客户体验。

借助 [!DNL Journey Optimizer]，可以利用存储在事件或数据源中的上下文数据构建实时编排用例。您可以设计具有以下功能的分步式高级方案：

* 发送在收到&#x200B;**事件**&#x200B;时触发的实时[单一投放](general-events.md)，或使用Adobe Experience Platform **受众**&#x200B;在批次[中发送](read-audience.md)。

* 通过&#x200B;**数据源**&#x200B;利用[事件](../event/about-events.md)中的[上下文数据](../datasource/about-data-sources.md)、Adobe Experience Platform中的信息或第三方API服务中的数据。

* 使用&#x200B;**[内置操作](journeys-message.md)**&#x200B;发送在 [!DNL Journey Optimizer] 中设计的消息；或者，如果您使用第三方系统，可以创建&#x200B;**[自定义操作](using-custom-actions.md)**&#x200B;来发送消息。

* 使用&#x200B;**[历程设计器](using-the-journey-designer.md)**，构建分步式用例：轻松拖放进入事件或[读取受众活动](read-audience.md)，添加[条件](condition-activity.md)并发送个性化消息。

Journey Optimizer [旅程设计器](using-the-journey-designer.md)提供了营销人员和旅程从业人员跨渠道编排多步骤1:1旅程所需的一切。 这包括直观的拖放画布，以编排历程的每个步骤，定义目标受众，并包括目标受众成员将根据行为、上下文数据和业务事件看到的跨渠道消息、选件和内容。 探索[实际用例](jo-use-cases.md)以了解如何应用这些功能。

➡️ [通过视频了解 Journey Optimizer](#video)

## 历程类型

Adobe Journey Optimizer支持四种历程类型，每种类型针对不同的用例和进入机制而设计。 根据您希望用户档案输入的方式选择正确的类型，并逐步了解您的客户体验。

>[!BEGINTABS]

>[!TAB 单一历程]

**单一历程**&#x200B;由事件发生时单独触发，具体操作包括购买、应用程序登录或表单提交。 配置文件在收到事件时实时进入历程，因此非常适合个性化、行为驱动的体验。

**关键特性：**

* 实时事件驱动型录入
* 单个配置文件处理
* 非常适合事务性消息和即时响应
* 支持来自触发事件的上下文数据

**用例：**

* 购买后的订单确认
* 有人订阅时收到欢迎电子邮件
* 浏览行为触发的购物车放弃率
* 密码重置通知

➡️ [了解事件配置](../event/about-events.md) | [常规事件](general-events.md) | [发送给订阅者的消息使用案例](message-to-subscribers-uc.md)

>[!TAB 读取受众历程]

**读取受众历程**&#x200B;从Adobe Experience Platform中的受众开始，并将消息批量发送到该受众中的所有用户档案。 此历程类型同时处理整个受众，非常适合计划活动和定期通信。

**关键特性：**

* 批量处理受众区段
* 已计划或一次性执行
* 所有配置文件同时输入
* 支持大规模通信

**用例：**

* 每月快讯
* 针对目标区段的促销活动
* 面向所有客户的产品公告
* 季节性营销活动

➡️ [了解读取受众活动](read-audience.md) | [开始使用受众](../audience/about-audiences.md) | [多渠道消息传递用例](journeys-uc.md)

>[!TAB 受众资格历程]

当配置文件符合（或退出）特定受众区段资格时，会触发&#x200B;**受众资格历程**。 用户档案在满足受众标准时实时单独进入历程，从而在客户行为发生更改时实现即时参与。

**关键特性：**

* 基于实时鉴别的条目
* 持续监控受众会员资格
* 符合条件的个人配置文件处理
* 最适合流受众

**用例：**

* VIP层升级通知
* 客户停用时重新参与
* 首次购买庆祝消息
* 客户移动时的地理定位

➡️ [了解受众资格](audience-qualification-events.md) | [条件活动](condition-activity.md) | [正在创建区段定义](../audience/creating-a-segment-definition.md)

>[!TAB 商业活动历程]

**业务事件历程**&#x200B;由同时影响多个配置文件的业务事件（如库存更新、天气警报或价格变化）触发。 这些历程不是对单个客户行为做出反应，而是对更广泛的业务环境或外部因素做出反应。

**关键特性：**

* 由业务级事件触发，而非单个操作
* 同时影响多个配置文件
* 发生事件时定位特定受众
* 将事件驱动计时与受众定位相结合

**用例：**

* 向感兴趣的客户发出低库存警报
* 快闪销售公告
* 基于天气的促销活动
* 降价通知
* 产品缺货警报

➡️ [了解业务活动](general-events.md) | [配置业务事件](../event/about-creating-business.md) | [条目管理](entry-management.md)

>[!ENDTABS]

## 历程概述

:::: landing-cards-container
:::
![icon](https://cdn.experienceleague.adobe.com/icons/circle-play.svg)

历程创建入门

设计、测试、发布和跟踪客户历程以构建个性化全渠道营销活动的分步指南。

[创建您的第一个历程](journey-gs.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/list-check.svg)

Journey Orchestration — 完整指南

涵盖Adobe Journey Optimizer中旅程创建、管理和优化所有方面的综合文档。

[浏览完整的指南](journey-get-started.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/gear.svg)

管理历程

运用筛选工具、用户档案管理、时区配置及优化技术，高效管理客户历程。

[学习历程管理](/help/rp_landing_pages/manage-journey-landing-page.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/puzzle-piece.svg)

历程活动

了解如何在历程中配置和使用触发器、决策步骤、受众管理及个性化消息推送等活动。

[探索活动](/help/rp_landing_pages/about-journey-building-landing-page.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/code-branch.svg)

构建表达式

掌握表达式创建技巧，运用强大工具与语法实现动态工作流、数据操作及高级历程编排。

[了解表达式](/help/rp_landing_pages/building-advanced-conditions-journeys-landing-page.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/bullseye.svg)

历程用例

探索 Adobe Journey Optimizer 的实际应用场景，包括多渠道消息传递及与外部系统的集成方案。

[探索用例](/help/rp_landing_pages/journey-use-cases-landing-page.md)
:::

::::

## 用例{#uc-journey}

在历程设计器中，营销人员可以在事件发生时通过任何渠道发送实时触发的 1:1 消息。例如，当客户订阅服务时，它可以[触发欢迎电子邮件](message-to-subscribers-uc.md)，鼓励客户首次登录应用程序并设置首选项。可以通过完成购买、打开电子邮件和登录应用程序等操作，在整个历程为新客户提供引导。

[历程设计器](using-the-journey-designer.md)提供[内置渠道操作](journeys-message.md)，支持出站消息（如电子邮件、推送通知和短信/彩信）以及入站渠道（包括直接在 Journey Optimizer 中构建的移动应用程序、网站和基于代码的体验）。您还可以使用第三方系统发送消息（无论是通过电子邮件、文本还是其他渠道），Journey Optimizer 包含[自定义操作](using-custom-actions.md)，允许直接从历程设计器将这些系统集成到历程中。

了解如何[在以下端到端用例中](jo-use-cases.md)构建历程。

>[!NOTE]
>
>可在[此页面](../start/guardrails.md)中找到有关历程护栏和限制的详细信息。

## 操作说明视频 {#video}

了解历程的组件，并了解在画布中构建历程的基础知识。

>[!VIDEO](https://video.tv.adobe.com/v/3424996?quality=12)

## 其他资源 {#additional-resources}

* **[客户历程疑难解答](/help/rp_landing_pages/troubleshoot-journey-landing-page.md)** — 诊断并解决历程执行问题，包括调试和优化的工具、错误代码和最佳实践
* **[历程常见问题](journey-faq.md)** - 有关历程的常见问题
* **[历程警报](../reports/alerts.md)** — 设置历程监控警报，并订阅实时更新通知
* **[错误代码引用](error-codes-reference.md)** - 历程错误代码和故障排除步骤
* **[故障排除](troubleshooting.md)** - 常见历程问题和解决方案
* **[历程教程（视频）](https://experienceleague.adobe.com/zh-hans/docs/journey-optimizer-learn/tutorials/journeys/journey-designer-overview){target="_blank"}** — 通过涵盖特性、功能和最佳实践的动手视频教程了解如何构建历程
