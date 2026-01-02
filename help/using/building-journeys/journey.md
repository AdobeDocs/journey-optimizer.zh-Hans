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
source-git-commit: 87351e845c7a6267cc78c26c838e69e77325f2b8
workflow-type: tm+mt
source-wordcount: '1420'
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

## 选择您的历程类型 {#journey-types}

**在开始构建**&#x200B;之前，请务必了解哪种类型的历程适合您的用例。 Adobe Journey Optimizer支持四种历程类型，每种类型针对不同的进入机制和业务方案而设计：

>[!BEGINTABS]

>[!TAB 单一历程]

**何时使用：**&#x200B;事件触发的实时体验

当发生特定操作（购买、应用程序登录、表单提交）时，**单独触发单一历程**。 用户档案一次实时输入一个用户档案，因此非常适合用于即时、行为驱动的响应。

**最适合：**

* 购买后的订单确认
* 有人订阅时的欢迎电子邮件
* 浏览触发的购物车放弃率
* 密码重置通知

➡️ [了解事件](../event/about-events.md) | [发送给订阅者的消息使用案例](message-to-subscribers-uc.md)

>[!TAB 读取受众历程]

**何时使用：**&#x200B;预定促销活动到受众区段

**读取受众历程**&#x200B;从Adobe Experience Platform受众开始，并同时向所有配置文件批量发送消息。 此历程类型非常适合于定期的大规模通信。

**最适合：**

* 每月快讯
* 针对目标区段的促销活动
* 产品公告
* 季节性营销活动

➡️ [了解读取受众](read-audience.md) | [开始使用受众](../audience/about-audiences.md)

>[!TAB 受众资格历程]

**何时使用：**&#x200B;对受众成员资格更改的实时响应

当配置文件符合（或退出）特定受众的资格时，**受众资格历程**&#x200B;会触发。 用户档案在满足标准时实时单独输入，从而在客户行为发生更改时实现即时参与。

**最适合：**

* VIP层升级通知
* 客户停用时重新参与
* 首次购买庆祝消息
* 客户移动时的地理定位

➡️ [了解受众资格](audience-qualification-events.md) | [创建受众](../audience/creating-a-segment-definition.md)

>[!TAB 商业活动历程]

**何时使用：**&#x200B;影响多个客户的业务情况

**业务事件历程**&#x200B;由同时影响多个配置文件的业务级事件（库存更新、天气警报、价格变化）触发。 这些策略应对更广泛的业务环境，而不是单个行动。

**最适合：**

* 向感兴趣的客户发出低库存警报
* 快闪销售公告
* 基于天气的促销活动
* 降价通知
* 产品缺货警报

➡️ [了解业务活动](../event/about-creating-business.md) | [条目管理](entry-management.md)

>[!ENDTABS]

>[!NOTE]
>
>不确定选择哪种类型？ 对于基于事件的体验，从&#x200B;**单一历程**&#x200B;开始，对于计划的营销活动，从&#x200B;**读取受众历程**&#x200B;开始 — 这些涵盖最常见的使用案例。

## 使用历程设计器构建 {#journey-designer}

**[历程设计器](using-the-journey-designer.md)**&#x200B;是您用于创建客户体验的可视画布。 借助直观的拖放界面，您无需编写代码即可编排历程的每个步骤。

![带有调色板、画布和历程窗格的Property Designer界面](assets/journey38.png)

### 可在设计器中执行的操作：

:::: landing-cards-container

:::
![icon](https://cdn.experienceleague.adobe.com/icons/circle-play.svg)

**定义入口点**

选择客户输入的方式：通过事件、受众区段或受众资格。

[了解进入管理](entry-management.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/envelope.svg)

**发送消息**

为电子邮件、推送、短信/彩信、应用程序内、Web等使用内置渠道操作，所有这些操作都在Journey Optimizer中设计。

[在历程中发送消息](journeys-message.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/code-branch.svg)

**添加逻辑和条件**

根据用户档案属性、受众会员资格或实时事件来分支您的历程。

[使用条件](condition-activity.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/database.svg)

**利用数据**

使用来自事件、Adobe Experience Platform或第三方API服务的上下文数据。

[使用数据源](../datasource/about-data-sources.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/gear.svg)

**连接外部系统**

创建自定义操作以集成用于发送消息或触发工作流的第三方系统。

[配置自定义操作](../action/about-custom-action-configuration.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/puzzle-piece.svg)

**添加编排活动**

使用等待时间、跳转、配置文件更新和受众管理来创建复杂的流程。

[浏览所有活动](about-journey-activities.md)
:::

::::

➡️ **实践学习：** [观看历程设计器视频](#video)或[探索端到端用例](jo-use-cases.md)

## 您的历程创建工作流 {#workflow}

构建成功的历程会遵循清晰、可重复的流程。 以下是您的分步工作流：

**1。 计划**→**2。 设计**→**3。 测试** → **4。 将**&#x200B;发布→**5。 监视器**→**6。 优化**

### &#x200B;1. **规划您的旅程** {#plan}

在打开设计器之前，请阐明您的目标：

* **目标是什么？** （例如，载入新客户，重新吸引非活动用户）
* **受众是谁？** （特定区段，事件驱动的个人）
* **哪种历程类型适合？** （请参阅上面的[历程类型](#journey-types)）
* **您将使用哪些渠道？**（电子邮件、推送、短信等）

### &#x200B;2. **在画布中进行设计** {#design}

使用历程设计器构建流：

1. **设置进入条件** — 定义用户档案的进入方式（事件、受众、资格）
2. **添加编排逻辑** — 包括等待时间、条件和决策点
3. **配置邮件** — 设计通信或利用现有模板
4. **设置操作** — 配置要执行的内置或自定义操作
5. **定义退出条件** — 指定用户档案完成历程的时间和方式

[了解如何使用历程设计器→](using-the-journey-designer.md)

### &#x200B;3. **上线前测试** {#test}

在客户遇到问题之前，请始终测试您的历程以发现问题：

* 使用&#x200B;**测试模式**&#x200B;模拟包含测试配置文件的历程
* 使用&#x200B;**练习**&#x200B;预览历程执行，而不影响实际数据或发送消息
* 验证所有条件、消息和操作是否按预期工作
* 检查时间、数据流和个性化

[测试您的历程→](testing-the-journey.md) | [了解试运行→](journey-dry-run.md)

### &#x200B;4. **发布您的历程** {#publish}

测试完成后，发布以使您的旅程上线：

* 查看最终设置和属性
* 发布以激活真实客户
* 注意：实时历程可以停止，但不能编辑（您必须创建新版本）

[发布您的历程→](publish-journey.md)

### &#x200B;5. **监视性能** {#monitor}

跟踪您的旅程在现实世界的表现：

* 查看历程报告和分析
* 监控输入、完成和错误率
* 设置严重问题的警报

[监视和报告→](report-journey.md) | [设置警报→](../reports/alerts.md)

### &#x200B;6. **优化和迭代** {#optimize}

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
![icon](https://cdn.experienceleague.adobe.com/icons/envelope.svg)

**欢迎新订阅者**

当客户订阅您的服务时，会触发欢迎历程，鼓励他们完成载入步骤。

[查看用例→](message-to-subscribers-uc.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/calendar-alt.svg)

**发送时间优化**

使用人工智能在每个客户最有可能参与时发送电子邮件，以最大限度地提高打开率和点击率。

[查看用例→](send-time-optimization.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/chart-line.svg)

**增加投放**

逐步增加报文量，以提升您的发送信誉并避免可投放性问题。

[查看用例→](ramp-up-deliveries-uc.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/bullseye.svg)

**按工作日**&#x200B;定位

根据客户进入历程一周中的哪一天发送不同的内容，以提高相关性。

[查看用例→](weekday-email-uc.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/puzzle-piece.svg)

**多渠道营销活动**

在单个历程中跨电子邮件、推送、短信和Web渠道编排无缝体验。

[查看用例→](journeys-uc.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/book.svg)

**所有用例**

探索包含分步实施的完整历程用例库。

[浏览所有→](jo-use-cases.md) | [用例库→](/help/rp_landing_pages/journey-use-cases-landing-page.md)
:::

::::

## 探索历程功能 {#capabilities}

当您更习惯于构建历程时，请探索这些强大的功能以创建复杂的客户体验：

:::: landing-cards-container

:::
![icon](https://cdn.experienceleague.adobe.com/icons/chart-line.svg)

**高级表达式**

使用表达式编辑器为数据操作和复杂逻辑构建动态条件和个性化。

[了解表达式](/help/rp_landing_pages/building-advanced-conditions-journeys-landing-page.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/clock.svg)

**时区管理**

通过自动时区调整和最佳发送时间处理全局受众。

[管理时区](timezone-management.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/shield-halved.svg)

**测试模式和试运行**

在正式启用之前使用测试用户档案验证历程，并预览执行而不影响实际数据。

[使用练习](journey-dry-run.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/database.svg)

**复制到沙盒**

跨沙盒复制历程以简化测试和部署工作流。

[复制历程](copy-to-sandbox.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/book.svg)

**标记和组织**

使用标记对历程进行分类和筛选，以便更好地进行大规模管理。

[使用标记组织](tags.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/gear.svg)

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
