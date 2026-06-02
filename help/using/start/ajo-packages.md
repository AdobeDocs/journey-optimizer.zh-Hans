---
solution: Journey Optimizer
product: journey optimizer
title: Journey Optimizer功能（按包）
description: 根据您的许可证、包和已启用的渠道，了解哪些Adobe Journey Optimizer功能可用。
feature: Get Started
topic: Content Management
role: Admin, User
level: Beginner
keywords: journey optimizer，包，许可证，选择， prime， ultimate，功能，特性，模块，渠道
hide: true
source-git-commit: 5e9ffb790127aae281dd15ad0eac03dbe0bb05e2
workflow-type: tm+mt
source-wordcount: '966'
ht-degree: 6%

---


# 我的[!DNL Adobe Journey Optimizer]包中有哪些可用内容？ {#ajo-packages}

[!DNL Adobe Journey Optimizer]功能因您的许可协议、启用的渠道和用户权限而异。 使用本指南了解包中通常提供哪些功能，并直接导航到每个功能的产品文档。

可用性还取决于渠道配置、实施先决条件和购买的加载项。 选择与您的许可证模型匹配的选项卡。

>[!BEGINTABS]

>[!TAB 历程和营销活动]

此选项卡适用于按照当前[!DNL Adobe Journey Optimizer]模块化打包模型（Journey Optimizer — 促销活动、Journey Optimizer -历程或Journey Optimizer — 促销活动和历程）许可的客户。

## 基本包 {#current-packages}

| 包 | 其中包含的内容 |
|---------|----------------|
| **Journey Optimizer — 营销活动** | 活动编排：用于批量参与的单步或多步受众工作流。 通过电子邮件、推送和短信进行事务性消息传递。 |
| **Journey Optimizer -历程** | 实时Journey Orchestration：事件触发的历程，支持流式处理和批量处理。 通过电子邮件、推送和短信进行事务性消息传递。 |
| **Journey Optimizer — 营销活动和历程** | Campaign Orchestration和实时Journey Orchestration相结合。 通过电子邮件、推送和短信进行事务性消息传递。 |

>[!NOTE]
>
>总数据量权利因包而异：**促销活动**&#x200B;客户有权每个可寻址配置文件获得15 KB的权限；**历程**&#x200B;和&#x200B;**促销活动和历程**&#x200B;客户有权每个可寻址配置文件获得75 KB的权限。

以下插件在任何基本包之上扩展了渠道覆盖范围。 **All Channels**&#x200B;加载项将出站投放、移动和Web捆绑在一起。

| 加载项 | 渠道已解锁 |
|--------|----------------|
| **出站投放** | 电子邮件、推送通知、直邮。 包括可投放性基础知识。 |
| **移动设备** | 适用于移动界面的应用程序内消息传送、推送通知、内容卡和基于代码的渠道 |
| **Web** | 用于Web表面的Web渠道和基于代码的渠道 |
| **所有频道** | 包出站投放+移动+ Web |
| **决策** | Real-time offer decisioning和AI支持的优化 |

## 功能矩阵 {#capability-matrix-current}

| 功能 | 您可以做什么 | Journey Optimizer — 营销活动 | Journey Optimizer -历程 | Journey Optimizer — 促销活动和历程 | 需要加载项 | 了解详情 |
|-----------|----------------|:-----------------------------:|:----------------------------:|:----------------------------------------:|:---------------:|-----------|
| **交易型消息传递** | 通过电子邮件、推送或短信发送实时触发的消息 | ✓ | ✓ | ✓ | — | [了解事务性消息传递](../building-journeys/journey-gs.md) |
| **电子邮件** | 设计和发送个性化的电子邮件 | ✓ | ✓ | ✓ | 出站投放 | [了解如何发送电子邮件](../email/get-started-email.md) |
| **推送通知** | 发送移动推送警报 | ✓ | ✓ | ✓ | 出站投放 | [了解如何发送推送通知](../push/get-started-push.md) |
| **直邮** | 创建和发送实体邮件 | ✓ | ✓ | ✓ | 出站投放 | [了解如何使用直邮](../direct-mail/get-started-direct-mail.md) |
| **短信/彩信** | 发送文本和多媒体消息 | ✓ | ✓ | ✓ | 出站投放 | [了解如何发送移动消息](../mobile/get-started-mobile.md) |
| **应用程序内消息传送** | 在移动应用程序中显示消息 | ✓ | ✓ | ✓ | 移动 | [了解如何使用应用程序内消息传送](../in-app/get-started-in-app.md) |
| **内容卡片** | 提供持久、非侵入式的产品内消息 | ✓ | ✓ | ✓ | 移动 | [了解如何使用内容卡](../content-card/get-started-content-card.md) |
| **Web 渠道** | 实时个性化网页 | ✓ | ✓ | ✓ | Web | [了解如何使用Web渠道](../web/get-started-web.md) |
| **基于代码的体验** | 通过API或SDK个性化任何表面 | ✓ | ✓ | ✓ | 移动或Web | [了解如何使用基于代码的体验](../code-based/get-started-code-based.md) |
| **WhatsApp** | 通过WhatsApp Business发送消息 | ✓ | ✓ | ✓ | WhatsApp | [了解如何使用WhatsApp](../whatsapp/get-started-whatsapp.md) |
| **编排的营销活动** | 为批量参与设计多步骤受众工作流。 支持的渠道：仅限电子邮件、短信、推送和直邮。 | ✓ | — | ✓ | — | [了解如何使用协调的营销活动](../orchestrated/gs-orchestrated-campaigns.md) |
| **自动历程** | 设计事件触发的实时客户历程 | — | ✓ | ✓ | — | [了解如何构建历程](../building-journeys/journey-gs.md) |
| **实时触发器** | 在客户事件发生时作出反应 | — | ✓ | ✓ | — | [了解历程事件](../event/about-events.md) |
| **决策** | 实时为每个客户选择最佳选件 | 取决于您的许可证 | 取决于您的许可证 | 取决于您的许可证 | 决策 | [了解如何使用决策](../experience-decisioning/gs-experience-decisioning.md) |
| **AI支持的排名** | 使用机器学习优化优惠选择 | 取决于您的许可证 | 取决于您的许可证 | 取决于您的许可证 | 决策 | [了解AI模型](../offers/ranking/ai-models.md) |

>[!TAB 选择/Prime/Ultimate]

此选项卡适用于使用Select、Prime或Ultimate打包术语且已有许可协议的客户。

## 包概要 {#package-summaries}

+++**选择**

最适合组织批次和事务性消息传递快速入门：

- 计划的批量活动和事务性消息传递
- 核心营销活动和历程执行
- 电子邮件、短信、推送和自定义操作渠道基础
- 标准编排护栏

+++

+++**Prime**

包括Select中的所有内容，以及实时编排和入站渠道：

- 实时事件触发的历程编排
- 入站渠道：Web、应用程序内消息传送、基于代码的体验、内容卡和直邮
- 高级受众分段和定位

+++

+++**Ultimate**

包括Prime中的所有内容，以及决策和高级优化：

- Real-time offer decisioning和个性化
- AI支持的排名和优化模型
- 高级报告和试验功能

+++

## 功能矩阵 {#capability-matrix-legacy}

| 功能 | 您可以做什么 | 选择 | Prime | Ultimate | 了解详情 |
|-----------|----------------|:------:|:-----:|:--------:|-----------|
| **电子邮件** | 设计和发送个性化的电子邮件 | 已包含 | 已包含 | 已包含 | [了解如何发送电子邮件](../email/get-started-email.md) |
| **短信/彩信** | 发送文本和多媒体消息 | 已包含 | 已包含 | 已包含 | [了解如何发送移动消息](../mobile/get-started-mobile.md) |
| **推送通知** | 发送移动推送警报 | 已包含 | 已包含 | 已包含 | [了解如何发送推送通知](../push/get-started-push.md) |
| **批次营销活动** | 安排向受众发送消息 | 已包含 | 已包含 | 已包含 | [了解如何创建营销活动](../campaigns/get-started-with-campaigns.md) |
| **自动历程** | 设计事件触发的客户历程 | 已包含 | 已包含 | 已包含 | [了解如何构建历程](../building-journeys/journey-gs.md) |
| **实时历程触发器** | 对客户行为发生时的反应 | — | 已包含 | 已包含 | [了解历程事件](../event/about-events.md) |
| **应用程序内消息传送** | 在移动应用程序中显示消息 | — | 已包含 | 已包含 | [了解如何使用应用程序内消息传送](../in-app/get-started-in-app.md) |
| **Web 渠道** | 实时个性化网页 | — | 已包含 | 已包含 | [了解如何使用Web渠道](../web/get-started-web.md) |
| **基于代码的体验** | 通过API或SDK个性化任何表面 | — | 已包含 | 已包含 | [了解如何使用基于代码的体验](../code-based/get-started-code-based.md) |
| **内容卡片** | 提供持久、非侵入式的产品内消息 | — | 已包含 | 已包含 | [了解如何使用内容卡](../content-card/get-started-content-card.md) |
| **直邮** | 创建和发送实体邮件 | — | 适用于Prime及更高版本 | 已包含 | [了解如何使用直邮](../direct-mail/get-started-direct-mail.md) |
| **决策** | 实时为每个客户选择最佳选件 | — | — | 已包含 | [了解如何使用决策](../experience-decisioning/gs-experience-decisioning.md) |
| **AI支持的排名** | 使用机器学习优化优惠和内容选择 | — | — | 已包含 | [了解AI模型](../offers/ranking/ai-models.md) |
| **WhatsApp** | 通过WhatsApp Business发送消息 | 取决于您的许可证和渠道配置 | 取决于您的许可证和渠道配置 | 取决于您的许可证和渠道配置 | [了解如何使用WhatsApp](../whatsapp/get-started-whatsapp.md) |

>[!ENDTABS]
