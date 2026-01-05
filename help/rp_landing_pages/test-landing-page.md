---
solution: Journey Optimizer
product: Journey Optimizer
title: 测试、验证和批准
description: 了解Journey Optimizer中的所有测试和批准功能。 在启动之前预览内容、模拟历程、验证电子邮件、运行实验、检测冲突并设置审批工作流。
feature: Get Started, Overview
role: User
level: Beginner, Intermediate
keywords: 测试，验证，批准，审批，质量保证， qa，测试用户档案，个性化，呈现，垃圾邮件检查，内容试验， a/b测试，冲突检测，种子列表，验证，示例数据，审批工作流，电子邮件测试，验证工作流
redpen-status: CREATED_||_2025-08-11_20-30-59
exl-id: a770412f-2f80-459d-8cce-32212154d154
source-git-commit: 1b774d95a117903695e6954fb2c820adfdf0d3bb
workflow-type: tm+mt
source-wordcount: '2768'
ht-degree: 5%

---

# 测试、验证和批准{#section-overview}

本节介绍Journey Optimizer中的所有测试和批准功能。 您将找到用于预览测试用户档案内容的工具、验证历程逻辑、检查电子邮件渲染和垃圾邮件分数、运行A/B实验、检测冲突以及设置审批工作流。

此登陆页面可帮助您根据正在构建的内容（营销活动与历程）选择正确的测试方法，引导您完成推荐的测试工作流，并提供对所有测试和审批资源的快速访问。 从下面的[选择测试方法](#choose-your-testing-approach)开始，以确定哪些工具适用于您的用例。

## 为什么测试和批准很重要

测试和批准流程是重要的质量关卡，可保护您的品牌声誉并确保活动取得成功。 以下是它们之所以重要的原因：

* **在错误到达客户之前捕获错误** — 在修复快速且无风险的受控环境中识别断开的链接、不正确的个性化、渲染问题和逻辑缺陷。

* **提高可投放性** — 测试垃圾邮件分数、验证电子邮件身份验证并检查跨电子邮件客户端的呈现，以最大限度地提高收件箱放置和参与率。

* **确保品牌一致性** — 预览包含不同测试配置文件的内容，以验证是否为各种客户区段正确显示个性化并维护品牌标准。

* **验证复杂历程** — 模拟多步历程流以确认触发器正确触发，条件正确评估，客户在正确的时间收到正确的消息。

* **建立责任制** — 实施需要利益相关者签署的正式审批工作流，创建明确的所有权并减少未经授权或过早启动的活动情况。

* **节省时间和资源** — 在开发周期早期发现修复更便宜和更快的问题，从而防止代价高昂的启动后更正或客户服务升级。

## 测试功能概述

**可用的测试类型：**

* 内容测试：在发送→[测试营销活动](#testing-campaigns)、[测试个性化](#testing-personalization)之前，预览并验证消息内容
* 历程逻辑测试：在[测试历程](#testing-journeys)→模拟客户通过历程路径的进度
* 技术测试：验证[技术验证](#2-technical-validation)→的渲染、可投放性和身份验证
* 性能测试：使用A/B实验→[内容实验](#content-experiments--ab-testing)比较内容变化
* 冲突测试：检测营销活动和历程重叠→[冲突检测](#conflict-detection)
* 审批测试：激活[审批工作流](#approval-workflows-for-journeys-and-campaigns)之前→结构化审核工作流

按上下文&#x200B;**键功能：**

| 功能 | 应用于 | 渠道限制 | 先决条件 | 主要目的 |
|------------|-----------|---------------------|--------------|-----------------|
| [测试用户档案](../using/content-management/test-profiles.md) | 促销活动、历程 | 所有渠道 | 已创建测试用户档案 | 预览个性化内容 |
| [示例输入数据](../using/test-approve/simulate-sample-input.md) | 促销活动、历程 | 电子邮件、短信、推送、Web、基于代码、应用程序内、内容卡 | CSV/JSON文件 | 测试多个个性化变量 |
| [测试模式](../using/building-journeys/testing-the-journey.md) | 仅限历程 | 不适用 | 草稿历程，已配置命名空间 | 模拟配置文件进度 |
| [练习](../using/building-journeys/journey-dry-run.md) | 仅限历程 | 不适用 | 已创建历程 | 分析执行路径 |
| [电子邮件渲染](../using/content-management/rendering.md) | 促销活动、历程 | 仅电子邮件 | Litmus集成 | 跨客户端验证显示 |
| [垃圾邮件分数](../using/content-management/spam-report.md) | 促销活动、历程 | 仅电子邮件 | None | 可投放性验证 |
| [种子列表](../using/configuration/seed-lists.md) | 促销活动、历程 | 仅电子邮件 | 已配置种子列表 | 利益相关者监控 |
| [内容实验](../using/content-management/get-started-experiment.md) | 仅限营销活动 | 所有渠道 | None | A/B和多臂老虎机测试 |
| [冲突检测](../using/conflict-prioritization/conflicts.md) | 营销活动、历程（有限） | 所有渠道 | None | 防止客户过度发送消息 |
| [审批工作流](../using/test-approve/gs-approval.md) | 促销活动、历程 | 所有渠道 | 审批策略已创建 | 结构化审查流程 |
| [Personalization游乐场](../using/personalization/personalize.md#playground) | 全部 | 所有渠道 | None | 了解并测试个性化语法 |

**常见测试工作流：**

1. 预开发：使用[个性化游乐场](#testing-personalization)学习语法
2. 开发期间：使用[测试配置文件](#testing-campaigns)预览，使用[示例输入数据](#simulate-content-variations)验证
3. 启动前：运行[技术测试](#2-technical-validation) （呈现，垃圾邮件），检查[冲突](#conflict-detection)，提交[审批](#approval-workflows-for-journeys-and-campaigns)
4. 启动后：使用实时报告进行监视（请参阅[监视和疑难解答](#monitoring--troubleshooting)），根据结果迭代


## 关键术语

**[测试配置文件](../using/content-management/test-profiles.md)** =用于预览个性化内容的合成客户配置文件（不是真正的客户）。 在实时客户资料服务中标记。 测试模式和内容预览需要。 [了解如何创建测试用户档案](../using/audience/creating-test-profiles.md)

**[测试模式](../using/building-journeys/testing-the-journey.md)** =通过历程路径发送历程配置文件的测试模拟功能。 限制：仅草稿历程，需要命名空间，仅测试用户档案。 [请参阅测试模式文档](../using/building-journeys/testing-the-journey.md)

**[试运行](../using/building-journeys/journey-dry-run.md)** =跟踪路径的历程执行分析工具，不发送消息或进行API调用。 用例：验证逻辑而不占用资源。 [了解试运行](../using/building-journeys/journey-dry-run.md)

**[示例输入数据](../using/test-approve/simulate-sample-input.md)** =包含用于测试个性化的配置文件属性值的CSV或JSON文件。 最多支持30种变体。 这是创建测试用户档案的替代方法。 [如何模拟内容变体](../using/test-approve/simulate-sample-input.md)

**[种子列表](../using/configuration/seed-lists.md)** =实际投放（而非测试发送）中自动包含内部利益相关者的电子邮件地址。 仅限电子邮件渠道。 用例：质量监控和合规性。 [配置种子列表](../using/configuration/seed-lists.md)

**[内容实验](../using/content-management/get-started-experiment.md)** = A/B测试或多臂赌博机实验比较内容变化。 仅限营销活动，在历程中不可用。 [实验入门](../using/content-management/get-started-experiment.md) | [创建试验](../using/content-management/content-experiment.md)

**[验证](../using/content-management/proofs.md)** =使用测试配置文件数据测试发送到特定电子邮件地址的电子邮件投放。 与种子列表不同（验证是手动测试发送，种子列表是利益相关者自动副本）。 [发送校样](../using/content-management/proofs.md)

**[冲突检测](../using/conflict-prioritization/conflicts.md)** =用于识别针对相同受众的重叠营销活动和历程的工具。 有限历程支持：仅限单一、受众资格和读取受众类型。 [了解冲突管理](../using/conflict-prioritization/gs-conflict-prioritization.md)

**[审批工作流](../using/test-approve/gs-approval.md)** =需要利益相关者审批才能激活的多步审核流程。 需要审批策略配置。 [设置审批](../using/test-approve/gs-approval.md) | [创建策略](../using/test-approve/approval-policies.md)

**[渲染测试](../using/content-management/rendering.md)** =跨电子邮件客户端(Gmail、Outlook、Apple Mail)和设备的电子邮件显示验证。 需要Litmus集成。 [测试电子邮件渲染](../using/content-management/rendering.md)

**[Personalization playground](../using/personalization/personalize.md#playground)** =交互式学习环境，用于试验个性化语法和使用示例数据测试表达式。 不需要实时数据集。 [访问游乐场](../using/personalization/personalize.md#playground)

## 用于测试方法选择的决策树

使用此决策树可快速确定适合您的特定方案的测试工具。 根据上下文（正在构建的内容、需要验证的内容以及使用的渠道）回答每个问题，以直接导航到相关功能和文档。

+++ **问题1：您正在测试什么？**

* 营销活动→ [测试营销活动](#testing-campaigns)
* 历程→[测试历程](#testing-journeys)
* Personalization表达式→ [Personalization游乐场](#testing-personalization)
+++

+++**问题2：哪个方面需要验证？**

* [测试配置文件](#testing-campaigns)或[示例输入数据](#simulate-content-variations)→的内容和个性化
* 电子邮件显示→[电子邮件渲染测试](#2-technical-validation)
* 可投放性→ [垃圾邮件分数检查](#2-technical-validation)
* 历程逻辑和流→[测试模式](#testing-journeys)或[试运行](#journey-dry-run)
* →[内容试验](#content-experiments--ab-testing)进行的性能比较（仅限营销活动）
* 时间冲突→[冲突检测](#conflict-detection)
* 利益相关者审核→[审批工作流](#approval-workflows-for-journeys-and-campaigns)
+++

+++**问题3：哪个频道？**

* 电子邮件→所有可用的测试方法（请参阅[测试营销活动](#testing-campaigns)）
* SMS、推送→ [内容测试](#testing-campaigns)、[示例输入数据](#simulate-content-variations)、[审批工作流](#approval-workflows-for-journeys-and-campaigns)
* Web、应用程序内、基于代码的→ [内容测试](#testing-campaigns)、[示例输入数据](#simulate-content-variations)、[审批工作流](#approval-workflows-for-journeys-and-campaigns)
* 多个渠道→分别测试每个渠道
+++

+++**问题4：何时在工作流程中？**

* 在建→[Personalization游乐场](#personalization-playground)以进行学习之前
* 生成[→测试配置文件](#testing-campaigns)和[示例输入数据](#simulate-content-variations)以进行验证期间
* 在启动之前→[渲染测试](#2-technical-validation)，[垃圾邮件检查](#email-spam-report)，[冲突检测](#conflict-detection)，[审批](#approval-workflows-for-journeys-and-campaigns)
* 启动→[实时报告](../using/building-journeys/report-journey.md)和[监控](#monitoring--troubleshooting)后
+++


## 选择测试方法

正确的测试方法取决于您构建的内容以及需要验证的内容。 使用本指南为您的方案确定最相关的测试工具。

>[!BEGINTABS]

>[!TAB 测试营销活动]

对于所有营销活动：**&#x200B;**

* 使用[测试配置文件](../using/content-management/test-profiles.md)或[示例输入数据](../using/test-approve/simulate-sample-input.md)预览和测试内容
* 跨设备和客户端检查[电子邮件渲染](../using/content-management/rendering.md)（仅限电子邮件渠道）
* 运行[垃圾邮件分数检查](../using/content-management/spam-report.md) （仅限电子邮件渠道）
* 查看[与其他营销活动和历程的冲突](../using/conflict-prioritization/conflicts.md)
* 设置[种子列表](../using/configuration/seed-lists.md)以进行利益相关者监控（仅限电子邮件渠道）
* 在激活前提交[审批](../using/test-approve/gs-approval.md)

用于A/B测试和优化的&#x200B;**：**

* 创建[个内容实验](../using/content-management/get-started-experiment.md)以测试多个处理并测量性能

**对于API触发的营销活动：**

* 使用[Campaign模拟API](https://developer.adobe.com/journey-optimizer-apis/references/simulations/){target="_blank"}以编程方式触发验证作业

>[!TAB 测试历程]

**对于所有历程：**

* 使用[测试模式](../using/building-journeys/testing-the-journey.md)模拟用户档案进度（仅草稿历程，需要命名空间）或[练习](../using/building-journeys/journey-dry-run.md)分析执行路径而不发送消息
* 使用[预览和验证](../using/content-management/preview-test.md)测试单个邮件
* 检查[与其他历程和营销活动的冲突](../using/conflict-prioritization/conflicts.md)
* 发布前提交[审批](../using/test-approve/gs-approval.md)

**对于复杂历程：**

* 使用测试模式并一起练习以彻底验证分支逻辑和执行路径
* 系统地测试不同的进入条件和用户档案属性

**注意：**&#x200B;冲突检测和历程上限仅适用于单一、受众资格和读取受众历程。

>[!TAB 正在测试个性化]

**生成内容之前：**

* 在[个性化游乐场](../using/personalization/personalize.md#playground)中试验，学习语法和测试包含示例数据的表达式

**内容创建期间：**

* 使用[测试用户档案](../using/content-management/test-profiles.md)预览，以验证个性化正确呈现
* 使用CSV/JSON文件中的[示例输入数据](../using/test-approve/simulate-sample-input.md)测试多个方案（最多支持30个变体）

>[!ENDTABS]

## 测试最佳实践

要最大限度地提高测试工作的有效性，请遵循以下建议的做法：

1. **提前测试，通常为** — 不要等到营销活动完全生成。 在开发时以递增方式测试内容、个性化和逻辑。

1. **使用真实的测试用户档案** - [创建可准确表示目标受众区段的测试用户档案](../using/audience/creating-test-profiles.md)，包括边缘案例和不同的个性化方案。

1. **跨设备和客户端进行测试** — 验证常用电子邮件客户端(Gmail、Outlook、Apple Mail)和设备（桌面、移动设备、平板电脑）上的[电子邮件渲染](../using/content-management/rendering.md)以确保显示的一致性（仅限电子邮件渠道）。

1. **彻底验证个性化** — 使用多个[具有不同属性值的测试配置文件](../using/content-management/test-profiles.md)进行测试，以确认个性化令牌正确呈现并可以使用回退值。 使用[个性化游乐场](../using/personalization/personalize.md#playground)试验个性化表达式，并在将其应用于营销活动之前使用示例数据测试代码。

1. **使用示例数据测试内容变体** — 使用CSV或JSON文件中的[示例输入数据](../using/test-approve/simulate-sample-input.md)测试最多30个个性化方案，无需创建大量测试配置文件，从而节省时间并确保全面的覆盖范围。 支持电子邮件、短信、推送、Web、基于代码的体验、应用程序内和内容卡渠道。

1. **使用种子列表进行利益相关者监控** — 配置[种子列表](../using/configuration/seed-lists.md)以自动包含内部利益相关者，这些利益相关者将在执行时接收所有投放的副本以进行质量监控和合规性验证（仅限电子邮件渠道）。

1. **模拟历程路径** — 对于具有多个分支的复杂历程，请使用[测试模式](../using/building-journeys/testing-the-journey.md)测试不同的进入条件和配置文件属性以验证所有可能的路径。 适用于使用命名空间的草稿历程。

1. **检查可投放性指标** — 在发送大量邮件之前查看[垃圾邮件分数](../using/content-management/spam-report.md)、身份验证状态和电子邮件运行状况指标（仅限电子邮件渠道）。

1. **记录测试结果** — 保留测试结果、发现的问题和解决方案的记录，以改进未来的测试流程并与您的团队分享学习经验。

1. **尽早让利益相关者参与** — 在[正式批准之前，与利益相关者共享预览和测试结果](../using/test-approve/gs-approval.md)以收集反馈并调整期望。

## 建议的测试工作流程

遵循此系统化方法以确保全面测试和顺利批准：

### 1.内容开发和预览

首先，创建内容并使用预览功能验证初始设计和个性化：

* 设计您的[电子邮件](../using/email/create-email.md)、[短信](../using/sms/create-sms.md)、[推送通知](../using/push/create-push.md)或其他渠道内容

* 使用&#x200B;**[模拟内容](../using/content-management/preview-test.md)**&#x200B;功能预览测试用户档案

* 检查[个性化令牌](../using/personalization/personalization-syntax.md)、动态内容和回退值

* 在&#x200B;**[个性化游乐场](../using/personalization/personalize.md#playground)**&#x200B;中试验个性化表达式，在应用于实时内容之前使用示例数据测试和优化代码

* 使用CSV/JSON文件中的&#x200B;**[示例输入数据](../using/test-approve/simulate-sample-input.md)**&#x200B;测试多个变体，以验证各种配置文件方案中的个性化

* 验证跨不同屏幕大小和电子邮件客户端的[渲染](../using/content-management/rendering.md)

### 2.技术验证

验证影响可投放性和功能的技术方面：

* 运行[垃圾邮件分数检查](../using/content-management/spam-report.md)以识别潜在的可投放性问题

* 测试链接以确保它们未损坏并正确跟踪

* 验证[电子邮件身份验证](../using/configuration/dmarc-record.md) (SPF、DKIM、DMARC)配置

* 查看HTML渲染并检查CSS兼容性问题

* 在移动和桌面设备上测试[响应式设计](../using/email/content-from-scratch.md)

* 检查与其他营销活动和历程的[潜在冲突](../using/conflict-prioritization/conflicts.md)，以防止客户消息疲劳和时间问题

### 3.历程测试（仅限旅程）

如果您正在测试历程，请验证编排逻辑：

* 激活&#x200B;**[测试模式](../using/building-journeys/testing-the-journey.md)**&#x200B;以模拟配置文件在历程中的进度

* 测试不同的[进入条件](../using/building-journeys/entry-management.md)和受众资格

* 验证[等待活动](../using/building-journeys/wait-activity.md)、[条件](../using/building-journeys/condition-activity.md)和分支逻辑是否正常工作

* 对复杂历程使用&#x200B;**[练习](../using/building-journeys/journey-dry-run.md)**&#x200B;以分析执行路径而不发送消息

* 检查[事件](../using/event/about-events.md)是否正确触发以及[自定义操作](../using/action/about-custom-action-configuration.md)是否按预期执行

### 4.提交审批

测试完成并解决问题后：

* 根据您组织的[审批策略](../using/test-approve/approval-policies.md)提交营销活动或历程以供审批

* 在[审批请求](../using/test-approve/request-approval.md)中包含测试结果和文档

* 处理[批准者](../using/test-approve/review-approve-request.md)的任何反馈或更改请求

* 进行必要的修订，如果更改比较大，则进行重新测试

### 5.发射前验证

在激活活动或历程之前：

* 对所有设置、受众和[计划执行最终审核](../using/building-journeys/journey-properties.md)

* 验证所有批准均已到位并记录在案

* 确认发送时间和[时区](../using/building-journeys/timezone-management.md)正确

* 启用[监控和警报](../using/reports/alerts.md)以跟踪启动后的性能

### 6.监测和迭代

启动后，继续监测以及早发现任何问题：

* 为历程错误、高跳出率或低参与度设置[系统警报](../using/reports/alerts.md)

* 审核[实时报告](../using/building-journeys/report-journey.md)以跟踪性能是否符合预期

* 如果出现严重问题，请准备[暂停或修改](../using/building-journeys/journey-pause.md)历程

* 记录经验教训，以改进今后的测试流程

## 正在测试：用例

了解测试概念如何应用于现实场景：

| 用例 | 您将学习的内容 | 关键测试焦点 |
|----------|-------------------|-------------------|
| **[发送多渠道消息](../using/building-journeys/journeys-uc.md)** | 测试结合读取受众、反应事件和电子邮件/推送消息的历程。 验证从受众定位到消息投放的整个流程。 | 多渠道协调、反应事件、端到端流量验证、测试和发布步骤 |
| **[向订阅者发送消息](../using/building-journeys/message-to-subscribers-uc.md)** | 使用动态电子邮件地址测试目标订阅列出的历程。 验证个性化表达式以正确定向订阅者。 | Personalization表达式、动态寻址、订阅列表定位 |
| **[发送时间限制邮件](../using/building-journeys/weekday-email-uc.md)** | 测试历程及基于时间的条件，以确保在特定日期发送消息。 验证等待活动和计划逻辑。 | 基于时间的条件、等待活动、计划验证 |
| **[探索更多历程用例](../using/building-journeys/jo-use-cases.md)** | 访问涵盖体验事件、多渠道消息传递和外部系统集成的全方位实践示例集合。 | 各种场景、高级模式、集成测试 |

## 测试和审批内容

:::: landing-cards-container
:::
![icon](https://cdn.experienceleague.adobe.com/icons/list-check.svg)

预览、测试和验证内容

学习如何使用测试轮廓、邮件渲染测试、垃圾邮件分数评估等功能，预览、测试和验证个性化内容。

[探索预览和测试内容](preview-test-landing-page.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/shield-halved.svg)

历程和营销活动的审批工作流

了解如何设置、管理和执行审批流程，以确保历程和营销活动的质量控制。

[了解审批工作流](approve-landing-page.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/bullseye.svg)

测试历程

使用特定配置文件测试您的历程，以确保事件、条件和操作按预期工作，从而在发布之前验证您的历程。 适用于使用命名空间的草稿历程。

[测试您的历程](../using/building-journeys/testing-the-journey.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/code-branch.svg)

历程试运行

执行试运行以模拟和验证历程的执行路径，在发布之前识别潜在问题。

[了解历程试运行](../using/building-journeys/journey-dry-run.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/chart-line.svg)

监控和故障排除

访问全面的故障排除资源、系统警报和错误代码，以解决历程执行和性能问题。

[查看监控和故障排除](troubleshoot-journey-landing-page.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/code.svg)

Personalization游乐场

在安全环境中试验个性化表达式。 在应用到营销活动和历程之前，使用示例数据测试代码并预览结果。

[了解Personalization游乐场](../using/personalization/personalize.md#playground)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/data.svg)

内容实验和A/B测试

通过测试多个内容变体并测量性能以确定表现最佳的处理方法来优化活动。 仅适用于营销活动（支持A/B和多臂老虎机试验）。

[了解内容实验](../using/content-management/get-started-experiment.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/envelope.svg)

用于利益相关者监控的种子列表

在投放中自动包含内部利益相关者地址，以监控发送给客户的实际消息，确保质量和合规性。 仅适用于电子邮件渠道。

[配置种子列表](../using/configuration/seed-lists.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/bell.svg)

冲突检测

识别营销活动和历程之间的潜在重叠，以防止客户过多地同时进行通信。 可用于营销活动和单一、受众资格和读取受众历程。

[检测冲突](../using/conflict-prioritization/conflicts.md)
:::

::::

## 其他资源

### 基本测试和验证指南

* [模拟内容变体](../using/test-approve/simulate-sample-input.md) — 使用CSV或JSON文件测试最多30个个性化方案。 非常适合多语言内容测试，无需创建多个测试用户档案。 支持电子邮件、短信、推送、Web、基于代码、应用程序内和内容卡。

* [创建测试配置文件](../using/audience/creating-test-profiles.md) — 创建和管理测试配置文件以模拟客户方案。 了解如何标记用户档案以进行测试、设置属性和组织测试区段。

* [电子邮件垃圾邮件报告](../using/content-management/spam-report.md) — 在发送之前检查垃圾邮件分数，以改善可投放性和收件箱放置。 获取切实可行的内容优化推荐。

* [历程常见问题解答](../using/building-journeys/journey-faq.md) — 有关旅程测试、执行和疑难解答的常见问题快速参考。

<!-- ### Dependencies and relationships

Understand how testing capabilities connect to each other and to your broader Journey Optimizer workflows. This section maps prerequisites, upstream/downstream dependencies, and common capability combinations.

+++**Prerequisites (required before testing)**

* Test profiles must be created before using test mode or content preview
* Approval policies must be configured before submitting for approval
* Seed lists must be created before adding to campaigns/journeys
* Litmus integration required for email rendering tests
* Journey must be in draft status to use test mode
* Journey must have namespace configured to use test mode

+++

+++**What testing depends on (upstream)**

* Content creation: Need campaigns or journeys to test
* Test profiles: Required for test mode and content preview
* Approval policies: Required for approval workflows
* Configuration: Channel configurations, email authentication, domain settings

+++

+++**What depends on testing (downstream)**

* Campaign/journey activation: Cannot activate without resolving errors
* Publishing: Approval may be required before publishing
* Live monitoring: Post-launch monitoring and reporting
* Optimization: Use test results to refine future campaigns

+++

+++**Related capabilities**

* Testing + Approval workflows = Quality assurance process
* Testing + Conflict detection = Preventing customer over-messaging
* Testing + Content experiments = Performance optimization
* Testing + Reporting = Continuous improvement cycle
* Test profiles + Personalization = Content validation
* Dry run + Test mode = Comprehensive journey validation

+++

+++**Common capability combinations**

* Content testing: Test profiles + Sample input data + Personalization playground
* Email validation: Rendering tests + Spam scores + Test profiles + Proofs
* Journey validation: Test mode + Dry run + Test profiles
* Pre-launch checklist: All technical tests + Conflict detection + Approval workflows

+++
-->

### 常见问题

+++**问：启动营销活动之前需要什么测试？**

**最小值：**&#x200B;包含测试用户档案的内容预览+垃圾邮件分数检查（电子邮件）
**建议：** +电子邮件渲染+冲突检测+审批工作流
**最佳实践：** +样本输入数据测试+种子列表+ A/B试验（如果优化）

+++

+++**问：如何在不创建多个测试配置文件的情况下测试个性化？**

**主要解决方案：**&#x200B;将[示例输入数据](../using/test-approve/simulate-sample-input.md)用于CSV/JSON文件（最多支持30个变体）
**替代方案：**&#x200B;创建3-5个代表性[测试用户档案](../using/audience/creating-test-profiles.md)涵盖关键区段
**学习工具：**&#x200B;首先在[个性化游乐场](../using/personalization/personalize.md#playground)中进行试验

+++

+++**问：历程的测试模式与试运行模式有何区别？**

**测试模式：**&#x200B;通过历程发送测试配置文件，触发实际操作，生成测试消息。 需要草稿历程+命名空间。
**试运行：**&#x200B;跟踪执行路径而不发送任何内容。 适用于任何历程状态。 未发送消息，未执行操作。
**一起使用：**&#x200B;消息测试的测试模式+逻辑验证的试运行=全面覆盖。

+++

+++**问：我能否在生产/实时状态下测试历程？**

**测试模式：**&#x200B;否 — 仅草稿历程
**练习：**&#x200B;是 — 适用于任何历程状态
**内容预览：**&#x200B;是 — 随时预览单个消息
**解决方法：**&#x200B;将实时历程复制到草稿以进行完整测试模式验证

+++

+++**问：哪些测试功能需要外部集成？**

**电子邮件渲染：**&#x200B;需要Litmus集成（单独的许可证）
**所有其他：**&#x200B;内置到Journey Optimizer，无需其他集成
**注意：**&#x200B;测试配置文件需要实时客户配置文件服务（包含）

+++

+++**问：如何测试API触发的营销活动？**

**选项1：**&#x200B;使用[Campaign模拟API](https://developer.adobe.com/journey-optimizer-apis/references/simulations/){target="_blank"}进行编程测试
**选项2：**&#x200B;在UI中使用测试配置文件预览内容
**选项3：**&#x200B;发送验证以测试电子邮件地址
**最佳实践：**&#x200B;将这三者合并进行综合验证

+++

