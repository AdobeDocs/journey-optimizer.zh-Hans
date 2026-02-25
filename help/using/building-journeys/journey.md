---
solution: Journey Optimizer
product: journey optimizer
title: 历程入门
description: 历程入门 — 了解历程类型、工作流、功能和最佳实践，以便在 [!DNL Adobe Journey Optimizer]中创建个性化客户体验
feature: Journeys, Get Started, Overview
role: User
level: Beginner, Intermediate
keywords: 历程, 探索, 入门, 单一化, 读取受众, 受众资格筛选, 业务事件, 实时, 定时, 批量, 事件触发, 工作流, 编排, 个性化, 多渠道
exl-id: 73cfd48b-72e6-4b72-bbdf-700a32a34bda
version: Journey Orchestration
source-git-commit: 97fa287d94efb7fb95817fc15268e736517cb629
workflow-type: tm+mt
source-wordcount: '1439'
ht-degree: 93%

---


# 历程入门{#jo-general-principle}

[!DNL Adobe Journey Optimizer]使您能够创建实时适应受众行为和需求的个性化的多步骤客户历程。 通过直观的拖放式画布，您可以跨多个渠道编排消息与行动，利用上下文数据和受众目标选择实现最大影响力。

本指南提供了一个清晰的路线图，以帮助您了解历程基础知识，为您的用例选择正确的历程类型，并自信地设计出可提供有意义、及时的客户体验的历程。

## 什么是历程？

**历程**&#x200B;是自动化的多步骤客户体验，可根据客户行为、业务事件或预定营销活动，跨渠道编排个性化互动。

使用[!DNL Journey Optimizer]历程以：

* 利用事件或数据源中存储的上下文数据，构建&#x200B;**实时编排**&#x200B;用例
* 设计可动态响应客户行为和业务事件的&#x200B;**多步骤进阶场景**
* 跨电子邮件、推送通知、短信、应用程序内、Web 等渠道大规模提供&#x200B;**:1个性化体验**。

![带有调色板、画布及属性窗格的历程设计器界面](assets/journey38.png)

➡️**准备好开始构建了吗？**&#x200B;[在 5 分钟内创建您的第一个历程](journey-gs.md)。

### 历程与营销活动：分别是何时使用 {#journeys-vs-campaigns-intro}

[!DNL Adobe Journey Optimizer]提供了三种联系客户的方法：**历程** （1:1实时编排）、**营销活动** （简单批处理或API触发的投放）和&#x200B;**编排的营销活动** （具有多实体数据的批处理画布工作流）。

**快速决策：**

* 使用&#x200B;**历程**&#x200B;来设计多步骤、行为驱动的体验，让每位客户按自己的节奏前进
* 使用&#x200B;**行动/API 营销活动**&#x200B;来向受众进行简单的、定时或触发的消息投放。
* 使用&#x200B;**编排式营销活动**&#x200B;来执行需要多实体细分和精确发送前计数的复杂批量工作流。

<!-- waiting for DOCAC-13912
➡️ **[View detailed comparison: Journeys vs Campaigns](../start/journeys-vs-campaigns.md)** - Includes decision guide, use cases, and feature availability-->

## 选择您的历程类型 {#journey-types}

[!DNL Adobe Journey Optimizer]支持四种历程类型，每种历程类型针对不同的进入机制和业务方案而设计：

* **单一历程**：实时、事件触发的体验（订单确认、欢迎电子邮件）
* **读取受众历程**：定时批量触达细分受众（新闻通讯、促销活动）
* **受众资格筛选历程**：对受众成员资格变化的实时响应（VIP 升级、重新互动）
* **业务事件历程**：影响多客户群体的业务条件（库存预警、限时闪购）

<!-- waiting for DOCAC-13912 
➡️ **[Journey types and selection guide](journey-types-selection.md)** - Detailed comparison, decision tree, and feature compatibility matrix -->

## 使用历程设计器构建 {#journey-designer}

**[历程设计器](using-the-journey-designer.md)**&#x200B;是您用于创建客户体验的可视画布。 借助直观的拖放界面，您无需编写代码即可编排历程的每个步骤。

![带有调色板、画布和历程窗格的历程设计器界面](assets/journey38.png)

### 可在设计器中执行的操作：

:::: landing-cards-container

:::
![icon](https://cdn.experienceleague.adobe.com/icons/circle-play.svg?lang=zh-Hans)

**定义进入点**

选择客户进入方式：通过事件、受众区段或受众资格筛选。

[了解进入管理](entry-management.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/envelope.svg?lang=zh-Hans)

**发送消息**

为电子邮件、推送、短信/彩信、应用程序内、Web 等使用内置渠道操作，所有这些操作都在 Journey Optimizer 中设计。

[在历程中发送消息](journey-action.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/code-branch.svg?lang=zh-Hans)

**添加逻辑和条件**

根据轮廓属性、受众会员资格或实时事件对历程进行分支处理。

[使用条件](condition-activity.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/database.svg?lang=zh-Hans)

**利用数据**

使用来自事件、[!DNL Adobe Experience Platform]或第三方API服务的上下文数据。

[使用数据源](../datasource/about-data-sources.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/gear.svg?lang=zh-Hans)

**连接外部系统**

创建自定义操作，以集成第三方系统，用于发送消息或触发工作流。

[配置自定义操作](../action/about-custom-action-configuration.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/puzzle-piece.svg?lang=zh-Hans)

**添加编排活动**

利用等待时间、跳转、轮廓更新和受众管理功能，构建复杂的流程。

[探索所有活动](about-journey-activities.md)
:::

::::

➡️**动手实践：**&#x200B;[观看历程设计器视频](#video)或[探索端到端用例](jo-use-cases.md)

## 您的历程创建工作流 {#workflow}

构建成功的历程须遵循清晰、可重复的流程。 以下是您的分步工作流：

**1. 计划** → **2.设计**→**3.测试** → **4.发布**→**5.监控** → **6.优化**

### 1.规划您的历程 {#plan}

在打开设计器之前，先明确您的目标：

* **目标是什么？** （例如，新客户注册引导，重新吸引非活动用户）
* **受众是谁？** （特定区段、事件驱动的个人）
* **适合哪种历程类型？** （请参阅上面的[历程类型](#journey-types)）
* **您将使用哪些渠道？**（电子邮件、推送、短信等）

### 2.在画布中进行设计 {#design}

使用历程设计器构建流：

* **设置进入条件** – 定义轮廓的进入方式（事件、受众、资格筛选）
* **添加编排逻辑** - 包括等待时间、条件和决策点
* **配置消息** - 设计通信内容或利用现有模板
* **设置操作** - 配置要执行的内置或自定义操作
* **定义退出条件** - 指定轮廓完成历程的时间和方式

[了解如何使用历程设计器→](using-the-journey-designer.md)

### 3.发布前测试 {#test}

务必在客户进行体验前测试历程，以便及时发现问题：

* 使用&#x200B;**测试模式**&#x200B;模拟包含测试轮廓的历程
* 使用&#x200B;**试运行**&#x200B;预览历程执行效果，无需影响真实数据或发送消息
* 验证所有条件、消息和操作是否均按预期运行
* 检查时序、数据流和个性化设置

[测试您的历程→](testing-the-journey.md) | [了解试运行→](journey-dry-run.md)

### &#x200B;4. 发布您的历程 {#publish}

测试完成后，通过发布使历程生效：

* 查看最终设置和属性
* 发布以激活真实客户
* 注意：实时历程可以停止，但不能编辑（您必须创建新版本）

[发布您的历程→](publish-journey.md)

### 5.监控表现 {#monitor}

跟踪历程在现实环境中的表现：

* 查看历程报告和分析
* 监控进入率、完成率及错误率
* 针对重要问题设置警报

[监控和报告→](report-journey.md) | [设置警报→](../reports/alerts.md)

### &#x200B;9. 优化和迭代 {#optimize}

利用洞察持续优化：

* 分析参与度指标与转化率
* 测试发送时间优化策略
* 创建改进后的新版历程
* 运用 AI 驱动的建议

[优化您的历程→](optimize.md) | [发送时间优化→](send-time-optimization.md)

➡️ **准备开始？**&#x200B;[立即创建您的第一个历程→](journey-gs.md)

## 实际用例 {#use-cases}

通过实际案例学习如何应用历程概念解决常见的营销难题：

:::: landing-cards-container

:::
![icon](https://cdn.experienceleague.adobe.com/icons/envelope.svg?lang=zh-Hans)

**欢迎新订阅者**

当客户订阅您的服务时，会触发欢迎历程，引导他们完成加入步骤。

[查看用例→](message-to-subscribers-uc.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/calendar-alt.svg?lang=zh-Hans)

**发送时间优化**

利用 AI 在每位客户最可能互动的时间发送电子邮件，从而最大化打开率和点击率。

[查看用例→](send-time-optimization.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/chart-line.svg?lang=zh-Hans)

**增加投放数量**

逐步增加发送量，以提升您的发件信誉并避免送达率问题。

[查看用例→](ramp-up-deliveries-uc.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/bullseye.svg?lang=zh-Hans)

**按工作日定向投放**

根据客户进入历程的星期几发送不同内容，以提高相关性。

[查看用例→](weekday-email-uc.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/puzzle-piece.svg?lang=zh-Hans)

**多渠道营销活动**

在单个历程中跨电子邮件、推送、短信和 web 渠道编排无缝体验。

[查看用例→](journeys-uc.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/book.svg?lang=zh-Hans)

**所有用例**

探索完整的历程用例库，获取分步实现指南。

[浏览所有→](jo-use-cases.md) | [用例库→](../../rp_landing_pages/journey-use-cases-landing-page.md)
:::

::::

## 探索历程功能 {#capabilities}

当您对历程构建更加熟悉后，可探索以下强大功能，打造更精细的客户体验：

:::: landing-cards-container

:::
![icon](https://cdn.experienceleague.adobe.com/icons/chart-line.svg?lang=zh-Hans)

**高级表达式**

利用表达式编辑器构建动态条件和个性化内容，实现数据操作与复杂逻辑处理。

[了解表达式](../../rp_landing_pages/building-advanced-conditions-journeys-landing-page.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/clock.svg?lang=zh-Hans)

**时区管理**

通过自动时区调整与最佳发送时间设置，高效触达全球受众。

[管理时区](timezone-management.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/shield-halved.svg?lang=zh-Hans)

**测试模式和试运行**

在发布前使用测试轮廓验证旅程，并预览执行效果而不影响真实数据。

[使用试运行](journey-dry-run.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/database.svg?lang=zh-Hans)

**复制到沙盒**

跨沙盒复制历程以简化测试和部署工作流。

[复制历程](copy-to-sandbox.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/book.svg?lang=zh-Hans)

**标签和组织**

利用标签对历程进行分类和筛选，以便大规模高效管理。

[使用标签进行组织管理](tags.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/gear.svg?lang=zh-Hans)

**吞吐量控制**

限制消息吞吐量以维护发件信誉，避免系统过载。

[控制吞吐量](limit-throughput.md)
:::

::::

[查看所有历程功能→](../../rp_landing_pages/manage-journey-landing-page.md)

## 通过观看学习 {#video}

通过视觉导览了解历程组件，并学习在画布中构建历程的基础知识：

>[!VIDEO](https://video.tv.adobe.com/v/3424996?quality=12)

➡️ **想要更多视频？** [浏览历程视频教程](https://experienceleague.adobe.com/zh-hans/docs/journey-optimizer-learn/tutorials/journeys/journey-designer-overview){target="_blank"}

## 常见问题 {#common-questions}

+++ 历程和营销活动之间有何区别？

[!DNL Adobe Journey Optimizer]提供三种方法：

* **历程** – 一对一:1实时编排，每个轮廓按自己的节奏逐步推进。最适合行为驱动、包含条件逻辑的多步骤体验（例如新用户引导、购物车弃单）。

* **营销活动（行动与 API 触发）**：向受众进行简单的消息投放，按计划或通过 API 触发同时向所有轮廓执行。最适合促销活动、新闻通讯、交易型消息。

* **编排式营销活动**：利用关系型数据（轮廓 + 产品/门店/预订）进行复杂细分，实现多步骤批量工作流。所有轮廓统一处理，提供精确的发送前计数。最适合季节性促销活动、产品发布，以及需要多实体数据的促销活动。

**主要区别**：历程为实时操作维护独立的客户状态；行动/API 营销活动批量发送简单消息；编排式营销活动提供支持多实体细分的批量工作流画布。

<!-- waiting for DOCAC-13912 - [See detailed comparison](#journeys-vs-campaigns) -->
[了解编排式营销活动](../orchestrated/gs-orchestrated-campaigns.md)

+++

<!-- Waiting for DOCAC-13912
+++ Which journey type should I use?

Use the [decision guide](#decision-guide) or [comparison table](#journey-types-comparison) to choose between Unitary, Read Audience, Audience Qualification, and Business Event journeys based on your trigger mechanism and use case.

+++
-->

+++ 我可以编辑已生效的历程吗？

您可以编辑部分元素（名称、消息内容），但结构性修改需创建新版本。[了解历程版本](publish-journey.md#journey-versions)

+++

➡️ **更多疑问？**&#x200B;[查看完整的历程常见问题](journey-faq.md)，内含 40 多个详细答案

## 需要帮助？ {#help}

使用这些链接查找指南、故障排除和资源。

### 常见任务快速链接

* **[创建您的第一个历程](journey-gs.md)** - 新手分步指南
* **[历程常见问题](journey-faq.md)** - 已回答的常见问题
* **[故障排除](../../rp_landing_pages/troubleshoot-journey-landing-page.md)** - 诊断和修复问题
* **[错误代码引用](error-codes-reference.md)** - 了解错误消息
* **[护栏和限制](../start/guardrails.md)** - 技术边界和最佳实践

### 获取有关问题的通知

设置&#x200B;**[历程警报](../reports/alerts.md)**&#x200B;以在历程出现错误或异常模式时接收实时通知。

### 其他资源

* **[历程管理中心](../../rp_landing_pages/manage-journey-landing-page.md)** - 用于筛选、优化和轮廓管理的工具
* **[历程活动引用](../../rp_landing_pages/about-journey-building-landing-page.md)** - 所有活动类型的完整指南
* **[排查执行问题](troubleshooting-execution.md)** - 调试历程执行故障
* **[排查入站活动问题](troubleshooting-inbound.md)** - 解决进入点与资格判定故障

**准备好构建您的第一个历程吗？**&#x200B;[现在就开始→](journey-gs.md)
