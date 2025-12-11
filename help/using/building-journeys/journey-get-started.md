---
solution: Journey Optimizer
product: journey optimizer
title: Journey Orchestration — 完整指南
description: Adobe Journey Optimizer中的Journey Orchestration入门综合指南
feature: Journeys, Get Started, Overview
role: User
level: Beginner, Intermediate
hide: true
hidefromtoc: true
keywords: 历程，编排，快速入门，入门，功能
source-git-commit: 856f35ebd70f38065e9b116bb648de1f2c2d439a
workflow-type: tm+mt
source-wordcount: '896'
ht-degree: 47%

---


# Journey Orchestration — 完整指南{#journey-orchestration-guide}

Adobe Journey Optimizer 中的历程功能使您能够创建个性化的多步骤客户历程，实时响应受众行为与需求。使用直观的拖放画布，您可以跨多个渠道编排消息和操作，利用上下文数据和受众定位以实现最大影响。

无论您是探索实时触发器、管理历程属性，还是使用自定义操作和表达式等高级工具，本指南都提供了一个清晰的路线图，让您能够自信地设计和优化历程，从而提供有意义、及时的客户体验。

## 什么是历程？

借助 [!DNL Journey Optimizer]，可以利用存储在事件或数据源中的上下文数据构建实时编排用例。设计实时响应客户行为和业务事件的多步骤高级方案。

Journey Optimizer 历程设计器向营销人员和历程从业者提供了有关策划跨渠道多步骤 1:1 历程所需的一切。这包括直观的拖放式画布，可用于编排历程的每个步骤，定义目标受众，还包括目标受众成员根据行为、上下文数据和业务事件看到的跨渠道消息、产品建议和内容。

![带有调色板、画布和历程窗格的Property Designer界面](assets/journey38.png)

**准备开始生成？**&#x200B;在[此页面](journey-gs.md)上了解如何创建和设计您的第一个历程。

## 历程快速入门 {#section-getting-started}

探索在Adobe Journey Optimizer中掌握Journey Orchestration的关键领域。

>[!BEGINTABS]

>[!TAB 构建您的第一个历程]

了解如何从头开始创建和设计您的第一个历程，包括设置事件、添加活动以及在发布之前测试。

[![了解详情](../assets/do-not-localize/learn-more-button.svg)](journey-gs.md)

>[!TAB 重要功能]

了解您可以使用历程做什么：实时交付、上下文数据、内置和自定义操作、可视设计器以及测试功能。

[![了解详情](../assets/do-not-localize/learn-more-button.svg)](#capabilities)

>[!TAB 用例]

探索实际历程示例，包括欢迎电子邮件、发送时间优化、提升投放能力和工作日定位。

[![了解详情](../assets/do-not-localize/learn-more-button.svg)](#use-cases)

>[!TAB 学习资源]

访问视频教程、分步指南和文档，以掌握历程构建和疑难解答。

[![了解详情](../assets/do-not-localize/learn-more-button.svg)](#learning-resources)

>[!ENDTABS]

## 主要功能 {#capabilities}

:::: landing-cards-container

:::
![icon](https://cdn.experienceleague.adobe.com/icons/circle-play.svg?lang=zh-Hans)

**实时和批量交付**

使用 Adobe Experience Platform 受众在接收到事件时触发发送实时&#x200B;**单一投放**，或进行&#x200B;**批量**&#x200B;处理。

[了解历程条目](entry-management.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/database.svg?lang=zh-Hans)

**上下文数据**

利用来自事件的&#x200B;**上下文数据**、来自 Adobe Experience Platform 的信息或来自第三方 API 服务的数据。

[使用数据源](../datasource/about-data-sources.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/envelope.svg?lang=zh-Hans)

**内置操作**

使用&#x200B;**内置渠道操作**&#x200B;通过电子邮件、推送、SMS/MMS等发送在[!DNL Journey Optimizer]中设计的消息。

[在历程中发送消息](journeys-message.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/gear.svg?lang=zh-Hans)

**自定义操作**

如果您使用第三方系统发送消息或连接到外部API，请创建&#x200B;**自定义操作**。

[配置自定义操作](../action/about-custom-action-configuration.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/layout.svg)

**可视历程设计器**

使用&#x200B;**历程设计器**，构建分步式用例：轻松地拖放进入事件或读取受众活动、添加条件和发送个性化消息。

[浏览历程设计器](using-the-journey-designer.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/shield-halved.svg?lang=zh-Hans)

**测试和优化**

在发布之前测试您的历程，监控其性能，并使用高级功能（如发送时间优化）优化交付。

[测试和发布历程](testing-the-journey.md)
:::

::::

## 用例和示例 {#use-cases}

在历程设计器中，营销人员可以在事件发生时通过任何渠道发送实时触发的 1:1 消息。例如，当客户订阅服务时，它可以[触发欢迎电子邮件](message-to-subscribers-uc.md)，鼓励客户首次登录应用程序并设置首选项。可以通过完成购买、打开电子邮件和登录应用程序等操作，在整个历程为新客户提供引导。

### 热门历程用例

:::: landing-cards-container

:::
![icon](https://cdn.experienceleague.adobe.com/icons/envelope.svg?lang=zh-Hans)

**欢迎新订阅者**

在客户订阅您的服务时发送个性化的欢迎历程，指导他们完成入门培训步骤。

[了解详情](message-to-subscribers-uc.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/calendar-alt.svg?lang=zh-Hans)

**优化电子邮件发送时间**

在每个客户最有可能参与时，使用AI支持的发送时间优化来发送电子邮件。

[了解详情](send-time-optimization.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/chart-line.svg?lang=zh-Hans)

**增加投放**

逐步增加报文量，以提升您的发送信誉并避免可投放性问题。

[了解详情](ramp-up-deliveries-uc.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/bullseye.svg?lang=zh-Hans)

**按工作日**&#x200B;定位

根据客户进入历程的当天发送不同的内容。

[了解详情](weekday-email-uc.md)
:::

::::

### 更多用例

[历程设计器](using-the-journey-designer.md)提供[内置渠道操作](journeys-message.md)，支持出站消息（如电子邮件、推送通知和短信/彩信）以及入站渠道（包括直接在 Journey Optimizer 中构建的移动应用程序、网站和基于代码的体验）。您还可以使用第三方系统发送消息 — Journey Optimizer包含[自定义操作](using-custom-actions.md)，以允许直接从历程设计器将这些系统集成到历程中。

**在**&#x200B;此页面[上探索所有历程用例](jo-use-cases.md)以发现您可以实施的端到端方案。

>[!NOTE]
>
>可在[此页面](../start/guardrails.md)中找到有关历程护栏和限制的详细信息。

## 学习资源 {#learning-resources}

### 视频教程 {#video}

了解历程的组件，并了解在画布中构建历程的基础知识。

>[!VIDEO](https://video.tv.adobe.com/v/3430352?captions=chi_hans&quality=12)

### 按主题浏览

:::: landing-cards-container

:::
![icon](https://cdn.experienceleague.adobe.com/icons/list-check.svg?lang=zh-Hans)

**创建和管理历程**

设计、测试、发布和跟踪客户历程以构建个性化全渠道营销活动的分步指南。

[浏览历程创建](/help/rp_landing_pages/create-journey-landing-page.md) | [学习历程管理](/help/rp_landing_pages/manage-journey-landing-page.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/puzzle-piece.svg?lang=zh-Hans)

**历程活动**

了解如何在历程中配置和使用触发器、决策步骤、受众管理及个性化消息推送等活动。

[探索活动](/help/rp_landing_pages/about-journey-building-landing-page.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/code-branch.svg?lang=zh-Hans)

**表达式和条件**

掌握表达式创建技巧，运用强大工具与语法实现动态工作流、数据操作及高级历程编排。

[了解表达式](/help/rp_landing_pages/building-advanced-conditions-journeys-landing-page.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/bell.svg?lang=zh-Hans)

**故障排除和监测**

诊断和解决历程执行问题，包括调试和优化的工具、错误代码和最佳实践。

[疑难解答指南](/help/rp_landing_pages/troubleshoot-journey-landing-page.md)
:::

::::

### 其他资源

* **[历程常见问题](journey-faq.md)** - 有关历程的常见问题
* **[错误代码引用](error-codes-reference.md)** - 历程错误代码和故障排除步骤
* **[警报](../reports/alerts.md)** – 设置历程监控警报
* **[故障排除](troubleshooting.md)** - 常见历程问题和解决方案
* **[历程教程](https://experienceleague.adobe.com/zh-hans/docs/journey-optimizer-learn/tutorials/journeys/journey-designer-overview){target="_blank"}** — 通过动手视频教程了解构建历程

