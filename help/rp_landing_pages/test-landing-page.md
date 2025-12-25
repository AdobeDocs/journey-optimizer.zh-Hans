---
solution: Journey Optimizer
product: Journey Optimizer
title: 测试和审批
description: 测试和审批
redpen-status: CREATED_||_2025-08-11_20-30-59
exl-id: a770412f-2f80-459d-8cce-32212154d154
source-git-commit: dd3d91266c0edea562f75ceb1f75974c7242ee1a
workflow-type: tm+mt
source-wordcount: '1296'
ht-degree: 11%

---

# 测试和审批{#section-overview}

质量保证对于提供卓越的客户体验至关重要。 Adobe Journey Optimizer提供全面的测试和审批功能，以帮助您验证内容、验证历程逻辑，并确保营销活动在到达受众之前符合质量标准。 从使用测试用户档案预览个性化消息到模拟复杂的历程流，这些工具使您能够尽早识别和解决问题、降低风险并维护品牌完整性。 无论您是跨设备测试电子邮件渲染、验证多步历程还是建立正式批准工作流，此部分都指导您学习最佳实践和分步流程，以建立对营销活动和历程的信心。 通过实施彻底的测试和结构化批准，您将最大限度地减少错误，提高可投放性，并创建无缝体验以引起客户的共鸣。

## 为什么测试和批准很重要

测试和批准流程是重要的质量关卡，可保护您的品牌声誉并确保活动取得成功。 以下是它们之所以重要的原因：

* **在错误到达客户之前捕获错误** — 在修复快速且无风险的受控环境中识别断开的链接、不正确的个性化、渲染问题和逻辑缺陷。

* **提高可投放性** — 测试垃圾邮件分数、验证电子邮件身份验证并检查跨电子邮件客户端的呈现，以最大限度地提高收件箱放置和参与率。

* **确保品牌一致性** — 预览包含不同测试配置文件的内容，以验证是否为各种客户区段正确显示个性化并维护品牌标准。

* **验证复杂历程** — 模拟多步历程流以确认触发器正确触发，条件正确评估，客户在正确的时间收到正确的消息。

* **建立责任制** — 实施需要利益相关者签署的正式审批工作流，创建明确的所有权并减少未经授权或过早启动的活动情况。

* **节省时间和资源** — 在开发周期早期发现修复更便宜和更快的问题，从而防止代价高昂的启动后更正或客户服务升级。

## 测试最佳实践

要最大限度地提高测试工作的有效性，请遵循以下建议的做法：

1. **提前测试，通常为** — 不要等到营销活动完全生成。 在开发时以递增方式测试内容、个性化和逻辑。

1. **使用真实的测试用户档案** - [创建可准确表示目标受众区段的测试用户档案](../using/audience/creating-test-profiles.md)，包括边缘案例和不同的个性化方案。

1. **跨设备和客户端进行测试** — 验证常用电子邮件客户端(Gmail、Outlook、Apple Mail)和设备（桌面、移动设备、平板电脑）上的[电子邮件渲染](../using/content-management/rendering.md)以确保显示的一致性。

1. **彻底验证个性化** — 使用多个[具有不同属性值的测试配置文件](../using/content-management/test-profiles.md)进行测试，以确认个性化令牌正确呈现并可以使用回退值。

1. **模拟历程路径** — 对于具有多个分支的复杂历程，请使用[测试模式](../using/building-journeys/testing-the-journey.md)测试不同的进入条件和配置文件属性以验证所有可能的路径。

1. **检查可投放性指标** — 在大发送之前查看[垃圾邮件分数](../using/content-management/spam-report.md)、身份验证状态和电子邮件运行状况量度。

1. **记录测试结果** — 保留测试结果、发现的问题和解决方案的记录，以改进未来的测试流程并与您的团队分享学习经验。

1. **尽早让利益相关者参与** — 在[正式批准之前，与利益相关者共享预览和测试结果](../using/test-approve/gs-approval.md)以收集反馈并调整期望。

## 建议的测试工作流程

遵循此系统化方法以确保全面测试和顺利批准：

### 1.内容开发和预览

首先，创建内容并使用预览功能验证初始设计和个性化：

* 设计您的[电子邮件](../using/email/create-email.md)、[短信](../using/sms/create-sms.md)、[推送通知](../using/push/create-push.md)或其他渠道内容
* 使用&#x200B;**[模拟内容](../using/content-management/preview-test.md)**&#x200B;功能预览测试用户档案
* 检查[个性化令牌](../using/personalization/personalization-syntax.md)、动态内容和回退值
* 验证跨不同屏幕大小和电子邮件客户端的[渲染](../using/content-management/rendering.md)

### 2.技术验证

验证影响可投放性和功能的技术方面：

* 运行[垃圾邮件分数检查](../using/content-management/spam-report.md)以识别潜在的可投放性问题
* 测试链接以确保它们未损坏并正确跟踪
* 验证[电子邮件身份验证](../using/configuration/dmarc-record.md) (SPF、DKIM、DMARC)配置
* 查看HTML渲染并检查CSS兼容性问题
* 在移动和桌面设备上测试[响应式设计](../using/email/content-from-scratch.md)

### 3.历程测试

对于历程，请验证编排逻辑：

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

* **[发送多渠道消息](../using/building-journeys/journeys-uc.md)** — 此用例演示了如何测试结合读取受众、反应事件和电子邮件/推送消息的历程。 了解如何验证从受众定位到消息投放的整个流程，并查看实际操作中的测试和发布步骤。

* **[向订阅者发送消息](../using/building-journeys/message-to-subscribers-uc.md)** — 了解如何使用动态电子邮件地址测试该目标订阅列表的历程。 此示例说明如何验证个性化表达式并确保消息到达正确的订阅者。

* **[发送有时限的消息](../using/building-journeys/weekday-email-uc.md)** — 了解如何使用基于时间的条件测试历程，以确保在特定日期发送消息。 请参阅如何验证等待活动和计划逻辑。

* **[探索更多历程用例](../using/building-journeys/jo-use-cases.md)** — 访问涵盖体验事件、多渠道消息传递和外部系统集成的全套实际示例。

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

使用特定配置文件测试历程，以便在发布之前验证历程，确保事件、条件和操作按预期运行。

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

::::

## 其他资源

### 基本测试和验证指南

* [历程中的实时报告](../using/building-journeys/report-journey.md) — 实时监视历程量度以跟踪性能并识别执行期间的问题。 访问配置文件进度、事件触发器和操作完成率的详细细分。

* [创建测试配置文件](../using/audience/creating-test-profiles.md) — 创建和管理测试配置文件以模拟真实的客户方案并验证个性化。 了解如何标记用户档案以进行测试、设置属性值以及组织测试用户档案区段。

* [电子邮件垃圾邮件报告](../using/content-management/spam-report.md) — 在发送之前检查您的电子邮件垃圾邮件分数，以改善可投放性和收件箱放置。 了解垃圾邮件过滤器如何评估您的内容并获得改进建议。

* [历程常见问题解答](../using/building-journeys/journey-faq.md) — 查找有关历程创建、测试、执行和故障排除的常见问题解答。 解决常见问题和了解历程行为的快速参考。

### 相关主题

* [内容管理](content-management-landing-page.md) — 了解如何使用模板、片段和电子邮件Designer设计、预览和管理内容。 掌握内容创建最佳实践，以实现一致的品牌化。

* [Reporting &amp; Analytics](reporting-landing-page.md) — 使用全面的报告、功能板和量度分析营销活动和历程表现。 制定数据驱动型决策以优化客户体验。

* [历程配置](configure-journeys-landing-page.md) — 配置数据源、事件和自定义操作以启用复杂的Journey Orchestration。 为历程创建建立技术基础。

* [营销活动管理](../using/campaigns/get-started-with-campaigns.md) — 探索不同的营销活动类型，了解如何创建、计划和优化批量活动和实时营销活动，以便产生最大影响。
