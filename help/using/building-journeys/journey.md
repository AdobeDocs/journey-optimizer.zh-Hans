---
solution: Journey Optimizer
product: journey optimizer
title: 历程入门
description: 历程入门 — 了解历程类型、工作流、功能和最佳实践，以便在Adobe Journey Optimizer中创建个性化客户体验
feature: Journeys, Get Started, Overview
role: User
level: Beginner, Intermediate
keywords: 历程，发现，开始，单一，读取受众，受众鉴别，业务事件，实时，已计划，批处理，事件触发，工作流，编排，个性化，多渠道
exl-id: 73cfd48b-72e6-4b72-bbdf-700a32a34bda
version: Journey Orchestration
source-git-commit: 8ea2a0fe685678d41004d549443a1757eb30c765
workflow-type: tm+mt
source-wordcount: '1465'
ht-degree: 3%

---


# 历程入门{#jo-general-principle}

Adobe Journey Optimizer允许您创建个性化的多步客户历程，这些历程会实时适应受众的行为和需求。 使用直观的拖放画布，您可以跨多个渠道编排消息和操作，利用上下文数据和受众定位以实现最大影响。

本指南提供了一个清晰的路线图，以帮助您了解历程基础知识，为您的用例选择正确的历程类型，并自信地设计可提供有意义、及时的客户体验的历程。

## 什么是历程？

**历程**&#x200B;是自动的多步客户体验，可以跨渠道编排个性化交互，以响应客户行为、业务活动或计划的营销活动。

使用[!DNL Journey Optimizer]可以：

* 使用存储在事件或数据源中的上下文数据构建&#x200B;**实时编排**&#x200B;用例
* 设计可动态响应客户行为和业务事件的&#x200B;**多步骤高级方案**
* 跨电子邮件、推送、短信、应用程序内、Web等大规模交付&#x200B;**1:1个性化体验**

![带有调色板、画布和历程窗格的Property Designer界面](assets/journey38.png)

➡️ **准备开始生成？** [在5分钟内创建您的第一个历程](journey-gs.md)。

### 历程与促销活动：何时使用各个 {#journeys-vs-campaigns-intro}

Adobe Journey Optimizer提供了三种联系客户的方法：**历程** （1:1实时编排）、**营销活动** （简单批处理或API触发的投放）和&#x200B;**编排的营销活动** （具有多实体数据的批处理画布工作流）。

**快速决策：**

* 使用&#x200B;**历程**&#x200B;获得多步的、行为驱动的体验，其中每个客户都按照自己的进度前进
* 使用&#x200B;**Action/API营销活动**&#x200B;向受众进行简单、计划或触发的消息传递
* 对于需要多实体分段和精确预发送计数的复杂批处理工作流，请使用&#x200B;**编排的营销活动**

<!-- waiting for DOCAC-13912
➡️ **[View detailed comparison: Journeys vs Campaigns](../start/journeys-vs-campaigns.md)** - Includes decision guide, use cases, and feature availability-->

## 选择您的历程类型 {#journey-types}

Adobe Journey Optimizer支持四种历程类型，每种类型针对不同的进入机制和业务方案而设计：

* **单一历程**：实时、事件触发的体验（订单确认、欢迎电子邮件）
* **读取受众历程**：与受众区段（新闻稿、促销活动）的计划批量通信
* **受众资格历程**：实时响应受众成员资格更改(VIP升级、重新参与)
* **业务事件历程**：业务状况影响多个客户（库存警报、闪电销售）

➡️ **[历程类型和选择指南](journey-types-selection.md)** — 详细比较、决策树和功能兼容性矩阵

## 使用历程设计器构建 {#journey-designer}

**[历程设计器](using-the-journey-designer.md)**&#x200B;是您用于创建客户体验的可视画布。 借助直观的拖放界面，您无需编写代码即可编排历程的每个步骤。

![带有调色板、画布和历程窗格的Property Designer界面](assets/journey38.png)

### 可在设计器中执行的操作：

:::: landing-cards-container

:::
![icon](https://cdn.experienceleague.adobe.com/icons/circle-play.svg?lang=zh-Hans)

**定义入口点**

选择客户输入的方式：通过事件、受众区段或受众资格。

[了解进入管理](entry-management.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/envelope.svg?lang=zh-Hans)

**发送消息**

为电子邮件、推送、短信/彩信、应用程序内、Web等使用内置渠道操作，所有这些操作都在Journey Optimizer中设计。

[在历程中发送消息](journeys-message.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/code-branch.svg?lang=zh-Hans)

**添加逻辑和条件**

根据用户档案属性、受众会员资格或实时事件来分支您的历程。

[使用条件](condition-activity.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/database.svg?lang=zh-Hans)

**利用数据**

使用来自事件、Adobe Experience Platform或第三方API服务的上下文数据。

[使用数据源](../datasource/about-data-sources.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/gear.svg?lang=zh-Hans)

**连接外部系统**

创建自定义操作以集成用于发送消息或触发工作流的第三方系统。

[配置自定义操作](../action/about-custom-action-configuration.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/puzzle-piece.svg?lang=zh-Hans)

**添加编排活动**

使用等待时间、跳转、配置文件更新和受众管理来创建复杂的流程。

[浏览所有活动](about-journey-activities.md)
:::

::::

➡️ **实践学习：** [观看历程设计器视频](#video)或[探索端到端用例](jo-use-cases.md)

## 您的历程创建工作流 {#workflow}

构建成功的历程会遵循清晰、可重复的流程。 以下是您的分步工作流：

**1。 计划**→**2。 设计**→**3。 测试** → **4。 将**&#x200B;发布→**5。 监视器**→**6。 优化**

### 1.规划您的旅程 {#plan}

在打开设计器之前，请阐明您的目标：

* **目标是什么？** （例如，载入新客户，重新吸引非活动用户）
* **受众是谁？** （特定区段，事件驱动的个人）
* **哪种历程类型适合？** （请参阅上面的[历程类型](#journey-types)）
* **您将使用哪些渠道？**（电子邮件、推送、短信等）

### 2.在画布中进行设计 {#design}

使用历程设计器构建流：

1. **设置进入条件** — 定义用户档案的进入方式（事件、受众、资格）
2. **添加编排逻辑** — 包括等待时间、条件和决策点
3. **配置邮件** — 设计通信或利用现有模板
4. **设置操作** — 配置要执行的内置或自定义操作
5. **定义退出条件** — 指定用户档案完成历程的时间和方式

[了解如何使用历程设计器→](using-the-journey-designer.md)

### 3.上线前测试 {#test}

在客户遇到问题之前，请始终测试您的历程以发现问题：

* 使用&#x200B;**测试模式**&#x200B;模拟包含测试配置文件的历程
* 使用&#x200B;**练习**&#x200B;预览历程执行，而不影响实际数据或发送消息
* 验证所有条件、消息和操作是否按预期工作
* 检查时间、数据流和个性化

[测试您的历程→](testing-the-journey.md) | [了解试运行→](journey-dry-run.md)

### 4.发布您的历程 {#publish}

测试完成后，发布以使您的旅程上线：

* 查看最终设置和属性
* 发布以激活真实客户
* 注意：实时历程可以停止，但不能编辑（您必须创建新版本）

[发布您的历程→](publish-journey.md)

### 5.监控性能 {#monitor}

跟踪您的旅程在现实世界的表现：

* 查看历程报告和分析
* 监控输入、完成和错误率
* 设置严重问题的警报

[监视和报告→](report-journey.md) | [设置警报→](../reports/alerts.md)

### 6.优化和迭代 {#optimize}

使用见解改进：

* 分析参与量度和转化率
* 测试发送时间优化
* 通过改进创建新的历程版本
* 使用AI支持的推荐

[优化您的历程→](optimize.md) | [发送时间优化→](send-time-optimization.md)

➡️ **准备开始？** [立即创建您的第一个历程→](journey-gs.md)

## 实际用例 {#use-cases}

从实践示例中学习，这些示例演示如何应用历程概念来解决常见的营销挑战：

:::: landing-cards-container

:::
![icon](https://cdn.experienceleague.adobe.com/icons/envelope.svg?lang=zh-Hans)

**欢迎新订阅者**

当客户订阅您的服务时，会触发欢迎历程，鼓励他们完成载入步骤。

[查看用例→](message-to-subscribers-uc.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/calendar-alt.svg?lang=zh-Hans)

**发送时间优化**

使用人工智能在每个客户最有可能参与时发送电子邮件，以最大限度地提高打开率和点击率。

[查看用例→](send-time-optimization.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/chart-line.svg?lang=zh-Hans)

**增加投放**

逐步增加报文量，以提升您的发送信誉并避免可投放性问题。

[查看用例→](ramp-up-deliveries-uc.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/bullseye.svg?lang=zh-Hans)

**按工作日**&#x200B;定位

根据客户进入历程一周中的哪一天发送不同的内容，以提高相关性。

[查看用例→](weekday-email-uc.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/puzzle-piece.svg?lang=zh-Hans)

**多渠道营销活动**

在单个历程中跨电子邮件、推送、短信和Web渠道编排无缝体验。

[查看用例→](journeys-uc.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/book.svg?lang=zh-Hans)

**所有用例**

探索包含分步实施的完整历程用例库。

[浏览所有→](jo-use-cases.md) | [用例库→](/help/rp_landing_pages/journey-use-cases-landing-page.md)
:::

::::

## 探索历程功能 {#capabilities}

当您更习惯于构建历程时，请探索这些强大的功能以创建复杂的客户体验：

:::: landing-cards-container

:::
![icon](https://cdn.experienceleague.adobe.com/icons/chart-line.svg?lang=zh-Hans)

**高级表达式**

使用表达式编辑器为数据操作和复杂逻辑构建动态条件和个性化。

[了解表达式](/help/rp_landing_pages/building-advanced-conditions-journeys-landing-page.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/clock.svg?lang=zh-Hans)

**时区管理**

通过自动时区调整和最佳发送时间处理全局受众。

[管理时区](timezone-management.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/shield-halved.svg?lang=zh-Hans)

**测试模式和试运行**

在正式启用之前使用测试用户档案验证历程，并预览执行而不影响实际数据。

[使用练习](journey-dry-run.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/database.svg?lang=zh-Hans)

**复制到沙盒**

跨沙盒复制历程以简化测试和部署工作流。

[复制历程](copy-to-sandbox.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/book.svg?lang=zh-Hans)

**标记和组织**

使用标记对历程进行分类和筛选，以便更好地进行大规模管理。

[使用标记组织](tags.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/gear.svg?lang=zh-Hans)

**吞吐量控制**

限制消息吞吐量以管理发送信誉并避免系统过载。

[控制吞吐量](limit-throughput.md)
:::

::::

[查看所有历程功能→](/help/rp_landing_pages/manage-journey-landing-page.md)

## 通过观看学习 {#video}

获取历程组件的可视化简介，并了解在画布中构建历程的基础知识：

>[!VIDEO](https://video.tv.adobe.com/v/3424996?quality=12)

➡️ **想要更多视频？** [浏览历程视频教程](https://experienceleague.adobe.com/zh-hans/docs/journey-optimizer-learn/tutorials/journeys/journey-designer-overview){target="_blank"}

## 常见问题 {#common-questions}

**问：历程和营销活动之间有何区别？**

答：Adobe Journey Optimizer提供了三种方法：

* **历程**： 1:1实时编排，每个用户档案按照自己的进度逐个浏览。 最适合具有条件逻辑（例如，载入、购物车放弃）的行为驱动型多步骤体验。

* **营销活动（操作和API触发）**：向受众简单消息投放，按计划或通过API触发器同时执行所有用户档案。 最适合促销活动、新闻稿、事务型消息。

* **协调的营销活动**：使用关系数据（用户档案+产品/商店/预订）进行复杂分段的多步骤批处理工作流。 处理的所有配置文件以及准确的预发送计数。 最适合季节性促销活动、产品发布，以及需要多实体数据的促销活动。

**主要区别**：历程维护各个客户状态以进行实时操作；操作/API营销活动批量交付简单消息；编排的活动提供具有多实体分段功能的批量工作流画布。

&#x200B;<!-- waiting for DOCAC-13912 [See detailed comparison](#journeys-vs-campaigns) | -->[了解编排的营销活动](../orchestrated/gs-orchestrated-campaigns.md)

<!-- Waiting for DOCAC-13912
**Q: Which journey type should I use?**

A: Use the [decision guide](#decision-guide) or [comparison table](#journey-types-comparison) to choose between Unitary, Read Audience, Audience Qualification, and Business Event journeys based on your trigger mechanism and use case.
-->

**问：是否可以编辑实时历程？**

答：您可以编辑有限的元素（名称、消息内容），但结构更改需要创建新版本。 [了解历程版本](publish-journey.md#journey-versions)

➡️ **更多问题？** [查看包含40多个详细答案的完整历程常见问题解答](journey-faq.md)

## 需要帮助？ {#help}

### 常见任务的快速链接

* **[创建您的第一个历程](journey-gs.md)** — 初学者分步指南
* **[历程常见问题解答](journey-faq.md)** — 已回答的常见问题
* **[故障排除](/help/rp_landing_pages/troubleshoot-journey-landing-page.md)** — 诊断和修复问题
* **[错误代码引用](error-codes-reference.md)** — 了解错误消息
* **[护栏和限制](../start/guardrails.md)** — 技术边界和最佳实践

### 获取有关问题的通知

设置&#x200B;**[历程警报](../reports/alerts.md)**&#x200B;以在历程遇到错误或异常模式时接收实时通知。

### 其他资源

* **[历程管理中心](/help/rp_landing_pages/manage-journey-landing-page.md)** — 用于筛选、优化和配置文件管理的工具
* **[历程活动引用](/help/rp_landing_pages/about-journey-building-landing-page.md)** — 所有活动类型的完整指南
* **[执行问题疑难解答](troubleshooting-execution.md)** — 调试历程执行问题
* **[入站活动故障诊断](troubleshooting-inbound.md)** — 修复输入和资格问题

**准备好构建您的第一个历程吗？** [立即开始→](journey-gs.md)
