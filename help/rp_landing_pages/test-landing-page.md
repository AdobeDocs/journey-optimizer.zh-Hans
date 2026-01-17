---
solution: Journey Optimizer
product: Journey Optimizer
title: 测试、验证和审批
description: 了解 Journey Optimizer 中的所有测试和审批功能。 在启动之前预览内容、模拟历程、验证电子邮件、运行实验、检测冲突并设置审批工作流。
feature: Get Started, Overview
role: User
level: Beginner, Intermediate
keywords: 测试，验证，批准，审批，质量保证， qa，测试轮廓，个性化，渲染，垃圾邮件检测，内容试验， a/b 测试，冲突检测，种子列表，校样，样本数据，审批工作流，电子邮件测试，验证工作流
redpen-status: CREATED_||_2025-08-11_20-30-59
exl-id: a770412f-2f80-459d-8cce-32212154d154
source-git-commit: c3535f39b351d671054031b9cc391bf6d9d83a09
workflow-type: ht
source-wordcount: '2328'
ht-degree: 100%

---

# 测试、验证和审批{#section-overview}

本节介绍 Journey Optimizer 中的所有测试和审批功能。 您将找到使用测试轮廓预览内容、验证历程逻辑、检查电子邮件渲染与垃圾邮件评分、运行 A/B 实验、检测冲突以及设置审批工作流等工具。

此登陆页面可帮助您根据正在构建的内容（营销活动与历程）选择正确的测试方法，引导您完成推荐的测试工作流，并提供对所有测试和审批资源的快速访问入口。 从下方[选择您的测试方法](#choose-your-testing-approach)开始，确定哪些工具适用于您的用例。 有关关键测试术语的定义，请参阅[关键术语](#key-terminology)。

## 测试和审批内容

:::: landing-cards-container
:::
![icon](https://cdn.experienceleague.adobe.com/icons/list-check.svg?lang=zh-Hans)

预览、测试和验证内容

学习如何使用测试轮廓、邮件渲染测试、垃圾邮件分数评估等功能，预览、测试和验证个性化内容。

[探索预览和测试内容](preview-test-landing-page.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/shield-halved.svg?lang=zh-Hans)

历程和营销活动的审批工作流

了解如何设置、管理和执行审批流程，以确保历程和营销活动的质量控制。

[了解审批工作流](approve-landing-page.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/bullseye.svg?lang=zh-Hans)

测试历程

使用特定配置文件测试历程，以便在发布之前验证历程，确保事件、条件和操作按预期运行。适用于使用命名空间的草稿历程。

[测试您的历程](../using/building-journeys/testing-the-journey.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/code-branch.svg?lang=zh-Hans)

历程试运行

执行试运行以模拟和验证历程的执行路径，在发布之前识别潜在问题。

[了解历程试运行](../using/building-journeys/journey-dry-run.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/chart-line.svg?lang=zh-Hans)

监控和故障排除

访问全面的故障排除资源、系统警报和错误代码，以解决历程执行和性能问题。

[查看监控和故障排除](troubleshoot-journey-landing-page.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/code.svg?lang=zh-Hans)

个性化游乐场

在安全环境中试验个性化表达式。 在应用到营销活动和历程之前，使用样本数据测试代码并预览结果。

[了解个性化游乐场](../using/personalization/personalize.md#playground)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/chart-line.svg?lang=zh-Hans)

内容试验和 A/B 测试

通过测试多个内容变体并衡量其表现，优化您的营销活动，从而确定效果最佳的内容方案。仅适用于营销活动（支持 A/B 和多臂老虎机试验）。

[了解内容试验](../using/content-management/get-started-experiment.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/envelope.svg?lang=zh-Hans)

利益相关者监控用种子列表

自动将内部利益相关者地址纳入投递列表，以监控实际发送给客户的消息，确保质量保证与合规性。仅适用于电子邮件渠道。

[配置种子列表](../using/configuration/seed-lists.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/bell.svg?lang=zh-Hans)

冲突检测

识别营销活动与旅程之间的潜在重叠，避免同时向客户发送过多沟通信息造成困扰。适用于营销活动和单一历程、受众资格筛选以及读取受众历程。

[检测冲突](../using/conflict-prioritization/conflicts.md)
:::

::::

## 为什么测试和审批很重要

测试与审批流程是至关重要的质量关卡，能保护您的品牌声誉并确保营销活动成功。以下是它们之所以重要的原因：

* **在错误触达客户前将其拦截** – 在可控环境中识别断链、个性化错误、渲染问题和逻辑缺陷，实现快速零风险的修复。

* **提升送达率** – 测试垃圾邮件评分、验证电子邮件认证配置、检查跨邮件客户端的渲染效果，以最大化收件箱抵达率和互动率。

* **确保品牌一致性** – 使用不同测试轮廓预览内容，验证个性化信息在各客户细分中正确显示，并保持品牌标准。

* **验证复杂历程** – 模拟多步骤历程流程，确认触发机制准确启动、条件判断正常执行，并确保客户在正确时间收到恰当信息。

* **建立责任机制** – 实施正式的审批工作流，要求利益相关者签字确认，从而明确权责归属，减少未经授权或过早启动的营销活动。

* **节省时间和资源** – 在开发周期早期发现问题，此时修复成本更低、速度更快，避免发布后昂贵的修正或客服升级成本。

<!--## Testing capabilities overview

**Testing types available:**

* Content testing: Preview and validate message content before sending → [Choose your testing approach](#choose-your-testing-approach)
* Journey logic testing: Simulate customer progression through journey paths → [Choose your testing approach](#choose-your-testing-approach)
* Technical testing: Validate rendering, deliverability, and authentication → [Technical validation](#2-technical-validation)
* Performance testing: Compare content variations using A/B experiments → [Content Experiments & A/B Testing](#test--approve-content)
* Conflict testing: Detect campaign and journey overlaps → [Conflict Detection](#test--approve-content)
* Approval testing: Structured review workflows before activation → [Approval Workflows](#test--approve-content)

**Key capabilities by context:**

| Capability | Applies to | Channel restrictions | Prerequisites | Primary purpose |
|------------|-----------|---------------------|--------------|-----------------|
| [Test profiles](../using/content-management/test-profiles.md) | Campaigns, Journeys | All channels | Test profiles created | Preview personalized content |
| [Sample input data](../using/test-approve/simulate-sample-input.md) | Campaigns, Journeys | Email, SMS, Push, Web, Code-based, In-app, Content cards | CSV/JSON file | Test multiple personalization variants |
| [Test mode](../using/building-journeys/testing-the-journey.md) | Journeys only | N/A | Draft journey, namespace configured | Simulate profile progression |
| [Dry run](../using/building-journeys/journey-dry-run.md) | Journeys only | N/A | Journey created | Analyze execution paths |
| [Email rendering](../using/content-management/rendering.md) | Campaigns, Journeys | Email only | Litmus integration | Verify display across clients |
| [Spam score](../using/content-management/spam-report.md) | Campaigns, Journeys | Email only | None | Deliverability validation |
| [Seed lists](../using/configuration/seed-lists.md) | Campaigns, Journeys | Email only | Seed list configured | Stakeholder monitoring |
| [Content experiments](../using/content-management/get-started-experiment.md) | Campaigns only | All channels | None | A/B and multi-armed bandit testing |
| [Conflict detection](../using/conflict-prioritization/conflicts.md) | Campaigns, Journeys (limited) | All channels | None | Prevent customer over-messaging |
| [Approval workflows](../using/test-approve/gs-approval.md) | Campaigns, Journeys | All channels | Approval policy created | Structured review process |
| [Personalization playground](../using/personalization/personalize.md#playground) | All | All channels | None | Learn and test personalization syntax |

**Common testing workflows:**

1. Pre-development: Use [personalization playground](#test--approve-content) to learn syntax
2. During development: Preview with [test profiles](#choose-your-testing-approach), validate with [sample input data](#choose-your-testing-approach)
3. Pre-launch: Run [technical tests](#2-technical-validation) (rendering, spam), check [conflicts](#test--approve-content), submit for [approval](#test--approve-content)
4. Post-launch: Monitor with live reports (see [Monitoring & Troubleshooting](#test--approve-content)), iterate based on results

-->

<!--
## Decision tree for testing method selection

Use this decision tree to quickly identify the right testing tools for your specific scenario. Answer each question based on your context (what you're building, what you need to validate, and which channel you're using) to navigate directly to the relevant capabilities and documentation.

+++ **Question 1: What are you testing?**

* Campaign → [Choose your testing approach](#choose-your-testing-approach)
* Journey → [Choose your testing approach](#choose-your-testing-approach)
* Personalization expressions → [Personalization playground](#test--approve-content)
+++

+++**Question 2: What aspect needs validation?**

* Content and personalization → [Test profiles](#choose-your-testing-approach) or [sample input data](#choose-your-testing-approach)
* Email display → [Email rendering tests](#2-technical-validation)
* Deliverability → [Spam score checks](#2-technical-validation)
* Journey logic and flow → [Test mode](#choose-your-testing-approach) or [dry run](#test--approve-content)
* Performance comparison → [Content experiment](#test--approve-content) (campaigns only)
* Timing conflicts → [Conflict detection](#test--approve-content)
* Stakeholder review → [Approval workflow](#test--approve-content)
+++

+++**Question 3: What channel?**

* Email → All testing methods available (see [Choose your testing approach](#choose-your-testing-approach))
* SMS, Push → [Content testing](#choose-your-testing-approach), [sample input data](#choose-your-testing-approach), [approval workflows](#test--approve-content)
* Web, In-app, Code-based → [Content testing](#choose-your-testing-approach), [sample input data](#choose-your-testing-approach), [approval workflows](#test--approve-content)
* Multiple channels → Test each channel separately
+++

+++**Question 4: When in the workflow?**

* Before building → [Personalization playground](#test--approve-content) for learning
* During building → [Test profiles](#choose-your-testing-approach) and [sample input data](#choose-your-testing-approach) for validation
* Before launch → [Rendering tests](#2-technical-validation), [spam checks](#2-technical-validation), [conflict detection](#test--approve-content), [approvals](#test--approve-content)
* After launch → [Live reports](../using/building-journeys/report-journey.md) and [monitoring](#test--approve-content)
+++

-->

## 选择测试方法

选择合适的测试方法取决于您构建的内容类型及需要验证的目标。请参考本指南，为您的场景确定最相关的测试工具。

>[!BEGINTABS]

>[!TAB 测试营销活动]

**对于所有营销活动：**

* 使用[测试轮廓](../using/content-management/test-profiles.md)或[样本输入数据](../using/test-approve/simulate-sample-input.md)预览和测试内容
* 跨设备和客户端检查[电子邮件渲染](../using/content-management/rendering.md)效果（仅限电子邮件渠道）
* 执行[垃圾邮件评分检查](../using/content-management/spam-report.md) （仅限电子邮件渠道）
* 查看[与其他营销活动和历程的冲突](../using/conflict-prioritization/conflicts.md)情况
* 设置用于利益相关者监控的[种子列表](../using/configuration/seed-lists.md)（仅限电子邮件渠道）
* 在激活前提交[审批](../using/test-approve/gs-approval.md)

**对于 A/B 测试和优化：**

* 创建[内容试验](../using/content-management/get-started-experiment.md)以测试多种内容方案并衡量其效果

**对于 API 触发的营销活动：**

* 使用[营销活动模拟 API](https://developer.adobe.com/journey-optimizer-apis/references/simulations/){target-&quot;_blank&quot;} 以编程方式触发校样任务

>[!TAB 测试历程]

**对于所有历程：**

* 使用[测试模式](../using/building-journeys/testing-the-journey.md)模拟轮廓推进（仅限草稿历程，需命名空间），或通过[试运行](../using/building-journeys/journey-dry-run.md)在不发送消息的情况下分析执行路径
* 使用[预览与校样](../using/content-management/preview-test.md)测试单个消息
* 检查[与其他历程和营销活动的冲突](../using/conflict-prioritization/conflicts.md)情况
* 发布前提交[审批](../using/test-approve/gs-approval.md)

**对于复杂历程：**

* 结合使用测试模式与试运行功能，全面验证分支逻辑与执行路径
* 系统性地测试不同的进入条件与轮廓属性

**注意：**&#x200B;冲突检测和历程上限仅适用于单一历程、受众资格筛选及读取受众历程。

>[!TAB 测试个性化]

**生成内容之前：**

* 在[个性化游乐场](../using/personalization/personalize.md#playground)中通过样本数据学习语法并测试表达式

**在内容创建期间：**

* 使用[测试轮廓](../using/content-management/test-profiles.md)预览内容，验证个性化渲染是否准确
* 使用 CSV/JSON 文件中的[样本输入数据](../using/test-approve/simulate-sample-input.md)测试多种场景（最多支持 30 种变体）

>[!ENDTABS]

## 测试最佳实践

为最大限度提升测试效果，请遵循以下推荐实践：

1. **尽早并频繁测试** – 切勿等到营销活动完全构建完成才开始。在开发过程中，逐步测试内容、个性化设置及逻辑功能。

1. **使用真实的测试轮廓** – [创建测试轮廓](../using/audience/creating-test-profiles.md)，使其准确代表您的目标受众区段，包含边缘案例和不同的个性化场景。

1. **跨设备与客户端测试** – 在主流电子邮件客户端 (Gmail、Outlook、Apple Mail) 和设备（桌面端、移动端、平板端）上[验证电子邮件渲染效果](../using/content-management/rendering.md)，确保显示一致性（仅限电子邮件渠道）。

1. **全面验证个性化效果** – 使用多个具有不同属性值的[测试轮廓](../using/content-management/test-profiles.md)进行测试，确保个性化标记正确渲染且备用值生效。利用[个性化操练场](../using/personalization/personalize.md#playground)试验个性化表达式，并在将其应用于营销活动之前使用样本数据测试代码。

1. **使用样本数据测试内容变体** – 通过[ CSV 或 JSON 文件中的样本输入数据](../using/test-approve/simulate-sample-input.md)，无需创建大量测试轮廓即可测试多达 30 种个性化场景，既节省时间又能确保全面覆盖。支持电子邮件、短信、推送、web、基于代码的体验、应用程序内和内容卡片等渠道。

1. **使用利益相关者监控用种子列表** – 配置[种子列表](../using/configuration/seed-lists.md)，在执行时自动包含将接收所有发送内容副本的内部利益相关者，用于质量监控与合规性验证（仅限电子邮件渠道）。

1. **模拟历程路径** – 对于具有多分支的复杂历程，使用[测试模式](../using/building-journeys/testing-the-journey.md)测试不同的进入条件和轮廓属性，以验证所有可能的路径。适用于使用命名空间的草稿历程。

1. **检查送达率指标** – 在大规模发送前，检查[垃圾邮件评分](../using/content-management/spam-report.md)、身份验证状态和电子邮件健康指标（仅限电子邮件渠道）。

1. **记录测试结果** – 保存测试结果、发现的问题及解决方案的记录，以优化未来的测试流程并与团队分享经验。

1. **尽早让利益相关者参与** – 在[正式审批之前，与利益相关者分享预览和测试结果](../using/test-approve/gs-approval.md)以收集反馈并统一期望。

## 建议的测试工作流程

请按照以下四阶段流程在发布前验证您的营销活动和历程：

| 阶段 | 测试内容 | 关键操作 |
|-------|-------------|-------------|
| **1. 内容验证** | 个性化，设计，渲染 | [使用测试轮廓预览](../using/content-management/preview-test.md)，通过 CSV/JSON 测试[多种变体](../using/test-approve/simulate-sample-input.md)，验证[跨设备渲染](../using/content-management/rendering.md)效果 |
| **2. 技术检查** | 送达率、链接、冲突 | 执行[垃圾邮件评分检查](../using/content-management/spam-report.md)，验证链接，检查与其他营销活动的[冲突](../using/conflict-prioritization/conflicts.md)情况 |
| **3. 历程逻辑** （仅限历程） | 进入条件、流程、分支 | 使用[测试模式](../using/building-journeys/testing-the-journey.md)模拟推进流程，执行[试运行](../using/building-journeys/journey-dry-run.md)分析复杂路径 |
| **4. 启动前** | 设置、批准、监控 | 提交[审批](../using/test-approve/gs-approval.md)，验证排期与受众设置，启用[警报](../using/reports/alerts.md)功能 |

**专业建议：**&#x200B;在构建内容前，先使用[个性化操练场](../using/personalization/personalize.md#playground)测试表达式；发布前务必检查[冲突检测](../using/conflict-prioritization/conflicts.md)，避免过度发送信息。

## 测试实战：用例

了解测试概念如何应用于实际场景：

<table style="table-layout:fixed"><tr style="border: 0;">
<td>
<a href="../using/building-journeys/journeys-uc.md">
<img alt="发送多渠道消息" src="../using/assets/do-not-localize/start-journey.jpeg">
</a>
<div>
<a href="../using/building-journeys/journeys-uc.md"><strong>发送多渠道消息</strong></a>
</div>
<p>
测试一个结合了“读取受众”、反应事件以及电子邮件/推送消息的历程。验证从受众目标选择到消息投放的完整流程。重点关注多渠道协调、反应事件、端到端流程验证以及测试与发布步骤。
</p>
</td>
<td>
<a href="../using/building-journeys/message-to-subscribers-uc.md">
<img alt="向订阅者发送消息" src="../using/assets/do-not-localize/start-quick.png">
</a>
<div>
<a href="../using/building-journeys/message-to-subscribers-uc.md"><strong>向订阅者发送消息</strong></a>
</div>
<p>
测试针对订阅列表并采用动态电子邮件地址的历程。验证个性化表达式能否准确锁定目标订阅者。重点关注个性化表达式、动态寻址以及订阅列表定向功能。
</p>
</td>
<td>
<a href="../using/building-journeys/weekday-email-uc.md">
<img alt="发送有时限的消息" src="../using/assets/do-not-localize/calendar.jpeg">
</a>
<div>
<a href="../using/building-journeys/weekday-email-uc.md"><strong>发送有时限的消息</strong></a>
</div>
<p>
测试含有基于时间的条件的历程，确保消息在指定日期发送。验证等待活动与排期逻辑。重点关注基于时间的条件、等待活动与排期验证。
</p>
</td>
</tr></table>

<table style="table-layout:fixed"><tr style="border: 0;">
<td>
<a href="../using/building-journeys/jo-use-cases.md">
<img alt="浏览更多历程用例" src="../using/assets/do-not-localize/icon-quick-start.svg">
</a>
<div>
<a href="../using/building-journeys/jo-use-cases.md"><strong>浏览更多历程用例</strong></a>
</div>
<p>
访问涵盖体验事件、多渠道消息推送及外部系统集成的全面实践案例库。探索各种场景、高级模式以及集成测试方法。
</p>
</td>
</tr></table>

## 关键术语

熟悉以下核心测试概念，以便更好地理解 Journey Optimizer 的测试与审批功能。每个术语均附有详细文档链接。

**[测试轮廓](../using/content-management/test-profiles.md)** – 用于预览个性化内容的模拟客户轮廓（非真实客户）。已在实时客户轮廓服务中标记。 测试模式和内容预览所需。[了解如何创建测试轮廓。](../using/audience/creating-test-profiles.md)

**[测试模式](../using/building-journeys/testing-the-journey.md)** – 通过历程路径发送测试轮廓的历程模拟功能。限制条件：仅适用于草稿历程、需命名空间、仅限测试轮廓。[请参阅测试模式文档](../using/building-journeys/testing-the-journey.md)

**[试运行](../using/building-journeys/journey-dry-run.md)** – 历程执行分析工具，可追踪路径但不会发送消息或调用 API。用例：验证逻辑而不占用资源。 [了解试运行](../using/building-journeys/journey-dry-run.md)

**[样本输入数据](../using/test-approve/simulate-sample-input.md)** – 包含轮廓属性值的 CSV 或 JSON 文件，用于测试个性化效果。最多支持 30 种变体。 这是创建测试轮廓的替代方法。 [如何模拟内容变体](../using/test-approve/simulate-sample-input.md)

**[种子列表](../using/configuration/seed-lists.md)** – 实际投放（而非测试发送）中自动包含的内部利益相关者的电子邮件地址。 仅限电子邮件渠道。 用例：质量监控和合规性。 [配置种子列表](../using/configuration/seed-lists.md)

**[内容试验](../using/content-management/get-started-experiment.md)** – 对比内容变体的 A/B 测试或多臂老虎机实验。仅限营销活动，在历程中不可用。 [试验入门](../using/content-management/get-started-experiment.md) | [创建试验](../using/content-management/content-experiment.md)

**[校样](../using/content-management/proofs.md)** – 使用测试轮廓数据向特定电子邮件地址发送的测试邮件。不同于种子列表（校样为手动测试发送，种子列表为自动向利益相关者发送副本）。[发送校样](../using/content-management/proofs.md)

**[冲突检测](../using/conflict-prioritization/conflicts.md)** – 识别针对同一受众的重叠营销活动与历程的工具。有限的历程支持：仅适用于单一历程、受众资格筛选及读取受众一类的历程。[了解冲突管理](../using/conflict-prioritization/gs-conflict-prioritization.md)

**[审批工作流](../using/test-approve/gs-approval.md)** – 需要利益相关者在激活前批准的多步骤审核流程。需要审批策略配置。 [设置审批](../using/test-approve/gs-approval.md) | [创建策略](../using/test-approve/approval-policies.md)

**[渲染测试](../using/content-management/rendering.md)** – 验证电子邮件在不同邮件客户端 (Gmail、Outlook、Apple Mail) 和设备上的显示效果。需要 Litmus 集成。 [测试电子邮件渲染](../using/content-management/rendering.md)

**[个性化游乐场](../using/personalization/personalize.md#playground)** – 用于试验个性化语法并使用样本数据测试表达式的交互式学习环境。无需实时数据集。[访问游乐场](../using/personalization/personalize.md#playground)

## 其他资源

>[!BEGINTABS]

>[!TAB 核心指南]

* [模拟内容变体](../using/test-approve/simulate-sample-input.md) – 使用 CSV 或 JSON 文件测试最多 30 种个性化场景。无需创建多个测试轮廓，即可实现多语言内容测试的理想方案。支持电子邮件、短信、推送、web、基于代码、应用程序内和内容卡片。

* [创建测试轮廓](../using/audience/creating-test-profiles.md) – 创建并管理测试轮廓，以模拟客户场景。了解如何标记测试用轮廓、设置属性并组织测试细分群体。

* [电子邮件垃圾邮件报告](../using/content-management/spam-report.md) – 发送前检查垃圾邮件评分，以提升送达率和收件箱抵达率。获取针对内容优化的可行建议。

* [历程常见问题](../using/building-journeys/journey-faq.md) – 关于历程测试、执行与故障排除的常见问题速查指南。

>[!TAB 依赖关系和关系]

了解测试功能之间如何相互关联，以及与您更广泛的 Journey Optimizer 工作流的衔接关系。本节将梳理先决条件、上下游依赖关系以及常见功能组合。

+++**先决条件（测试前必需满足）**

* 必须先创建测试轮廓，然后才能使用测试模式或内容预览
* 在提交审批之前，必须配置审批策略
* 在添加到营销活动/历程之前，必须创建种子列表
* 电子邮件渲染测试需要 Litmus 集成
* 历程必须处于草稿状态才能使用测试模式
* 历程必须已将命名空间配置为使用测试模式

+++

+++**测试的依赖项（上游）**

* 内容创建：需要营销活动或历程进行测试
* 测试轮廓：测试模式和内容预览所需
* 审批策略：审批工作流所必需
* 配置：渠道配置、电子邮件身份验证、域设置

+++

+++**依赖于测试的功能（下游）**

* 营销活动/历程激活：若未解决错误则无法激活
* 发布：发布前可能需要审批
* 实时监控：启动后的监控和报告
* 优化：利用测试结果优化未来的营销活动

+++

+++**相关功能**

* 测试 + 审批工作流 – 质量保证流程
* 测试 + 冲突检测 – 防止客户接收过多消息
* 测试 + 内容试验 – 性能优化
* 测试 + 报告 – 持续改进循环
* 测试轮廓 + 个性化 – 内容验证
* 试运行 + 测试模式 – 全面的历程验证

+++

+++**通用功能组合**

* 内容测试：测试轮廓 + 样本输入数据 + 个性化游乐场
* 电子邮件验证：渲染测试 + 垃圾邮件评分 + 测试轮廓 + 校样
* 历程验证：测试模式 + 试运行 + 测试轮廓
* 发布前检查清单：所有技术测试 + 冲突检测 + 审批工作流

+++

>[!TAB 常见问题]

+++**问：营销活动发布前需要进行哪些测试？**

**最低要求：**测试轮廓内容预览 + 垃圾邮件评分检查（邮件）
**推荐项：** + 电子邮件渲染测试 + 冲突检测 + 审批工作流
**最佳实践：** + 样本输入数据测试 + 种子列表 + A/B 试验（如进行优化）

+++

+++**问：如何在不创建大量测试轮廓的情况下测试个性化内容？**

**主要解决方案：**&#x200B;使用[ CSV/JSON 文件的样本输入数据](../using/test-approve/simulate-sample-input.md)（最多支持 30 种变体）
**备选方案：** 创建 3-5 个代表关键区段的[测试轮廓](../using/audience/creating-test-profiles.md)
**学习工具：**&#x200B;先在[个性化预览工具](../using/personalization/personalize.md#playground)中尝试

+++

+++**问：历程的测试模式与试运行有何区别？**

**测试模式：**将测试轮廓推入历程，触发实际操作并生成测试消息。需要草稿历程 + 命名空间。
**试运行：**跟踪执行路径而不发送任何内容。 适用于任何历程状态。 未发送消息，未执行操作。
**组合使用：**&#x200B;测试模式用于消息测试 + 试运行用于逻辑验证 – 实现全面覆盖。

+++

+++**问：我能否在生产/已发布状态下测试历程？**

**测试模式：**否 – 仅限草稿历程
**试运行：**是 – 适用于任何历程状态
**内容预览：**是 – 可随时预览单个消息
**替代方案：**&#x200B;将实时旅程复制为草稿，用于完整的测试模式验证

+++

+++**问：哪些测试功能需要外部集成？**

**电子邮件渲染测试：**需要 Litmus 集成（独立许可）
**其他所有测试：**均为 Journey Optimizer 内置功能，无需额外集成
**注意：**&#x200B;测试轮廓需要实时客户轮廓服务（已包含）

+++

+++**问：如何测试 API 触发的营销活动？**

**方案一：**&#x200B;使用[营销活动模拟 API](https://developer.adobe.com/journey-optimizer-apis/references/simulations/){target-&quot;_blank&quot;} 进行编程式测试
**方案二：**在界面中使用测试轮廓预览内容
**方案三：**向测试电子邮件地址发送校样
**最佳实践：**&#x200B;结合三种方式进行全面验证

+++

>[!ENDTABS]
