---
solution: Journey Optimizer
product: journey optimizer
title: 文档更新
description: 了解最新的文档更新
feature: Release Notes
topic: Content Management
role: User
level: Beginner, Intermediate
exl-id: 83c8f206-bce3-4cc8-94a3-575ec1d999bc
source-git-commit: 615f78d6a207e808aec91ac5b3fd5c008cb0c29c
workflow-type: tm+mt
source-wordcount: '4412'
ht-degree: 79%

---

# 文档更新 {#latest-updates}

此页面列出了 [!DNL Journey Optimizer] 文档中的所有最新更改，以及每月发布的功能和改进的相关更新。

## 2026 年 1 月 {#january-2026}

* 在个性化语法文档中添加了新章节，以阐明如何在个性化表达式中使用保留关键词。 在XDM架构中用作字段名称时，某些PQL关键字（如`next`、`last`和`this`）必须使用反撇号进行转义。 [了解详情](../personalization/personalization-syntax.md#reserved-keywords)

* [营销活动入门](../campaigns/get-started-with-campaigns.md)和[管理营销活动](../campaigns/manage-campaigns.md)页面已重新构建，并改进了信息架构，包括包含特定于类型的指南的综合工作流、增强的营销活动类型比较以及整合的状态表。

* 历程登录页面已重新设计，以便通过新的6步工作流进行载入，增强历程类型比较，并改进文档中的导航功能。 [了解详情](../building-journeys/journey.md)
* 添加了详细部分，以帮助用户在配置直邮的文件路由时为SFTP身份验证生成Base64编码的OpenSSH私钥，以避免连接错误。 [了解详情](../direct-mail/direct-mail-configuration.md#ssh-key-generation)

* 在子域委派文档中添加了注释，以告知用户在尝试委派到Adobe之前应允许在24-48小时内进行DNS传播。 [了解详情](../configuration/delegate-subdomain.md#set-up-subdomain)

## 2025 年 12 月 {#december-2025}

* 更新了决策自定义上传受众文档，以包含检索扩充数据所需的API标志。 在Offer Decisioning中使用CSV上传的受众时，您必须在API请求有效载荷中包含`"xdm:enrichedAudience": true`，以便在优惠决策响应中检索扩充属性。 [了解详情](../offers/custom-upload-decisioning.md#must-read)

* 在验证发送文档中添加了注释，以阐明频率上限规则适用于验证。 该页面现在包含一个“必读”部分，其中包含有关频率上限行为、镜像页面限制和资产可访问性规则的重要注意事项。 [了解详情](../content-management/proofs.md)

* 在“渠道快速入门”页面中新增了一个通信渠道可用性表，以显示支持的历程和营销活动（操作营销活动、API触发的营销活动以及编排的营销活动）渠道。 [了解详情](../channels/gs-channels.md#channels)

* 已创建新的全面跟踪登陆页面，以帮助用户发现并访问Journey Optimizer中提供的所有跟踪和监控功能。 [了解详情](../start/get-started-tracking.md)

* 电子邮件选择退出管理页面已得到增强，其中包含有关取消订阅流的详细信息，并说明了登陆页面选择退出的预期事件顺序。 [了解详情](../email/email-opt-out.md#send-message-unsubscribe-link)

* 更新了订阅列表文档，以包含有关流式客户细分资格标准的信息。 [了解详情](../landing-pages/subscription-list.md#define-subscription-list)

* 提供了新的IP预热可投放性指南，该指南在信誉基础知识、预检准备、监控量度和最佳实践方面提供了全面的指导，有助于从零信誉过渡到成功的收件箱放置。 [了解详情](../configuration/ip-warmup-deliverability-guide.md)

* 在登陆页面和电子邮件选择退出部分添加了警告，明确说明单击取消订阅链接只会打开登陆页面，但用户必须提交表单才能完成选择退出流程。 [了解详情](../landing-pages/lp-use-cases.md#configure-opt-out)

* 现在提供了新的历程用例库，该库将汇总一系列实践用例，包括战术模式（抑制逻辑、个性化技术、历程退出策略）和涵盖营销和技术工作流的完整端到端场景。 [了解详情](../building-journeys/jo-use-cases.md)

* 现在提供了一个新用例，演示如何配置历程，使其仅在工作日（星期一至星期五）发送电子邮件，并在指定时间自动排队等待星期一发送的周末条目。 [了解详情](../building-journeys/weekday-email-uc.md)

* 现在提供了一个新页面来解释Journey Optimizer的决策功能，包括新一代决策框架与已建立的决策管理解决方案之间的差异，以及它们在跨渠道提供个性化优惠方面的主要优势。 [了解详情](../experience-decisioning/gs-decision.md)

* Audience Activation文档中添加了一个新部分，用于说明如何通过在Audience Portal中的新区段定义中封装不受支持的受众类型(如Customer Journey Analytics受众)，来激活[!DNL Journey Optimizer]中的不受支持受众类型。 [了解详情](../audience/target-audiences.md#activation-non-supported)

* 等待活动文档中添加了新章节，用于说明驻留在读取受众历程中的等待活动的配置文件如何自动从统一配置文件服务(UPS)刷新其属性。 这阐明了在等待节点之后执行历程期间，配置文件数据可能会发生更改，如果您希望在整个历程中获取一致的快照数据，这可能会产生意外结果。 [了解详情](../building-journeys/wait-activity.md#profile-refresh)

* 在路径试验部分添加了警告说明，警告用户不要在路径试验发布后编辑其元数据，因为这会中断试验结果的计算和报告。 [了解详情](../building-journeys/optimize.md#experimentation)

* 在“创建表单预设”部分中添加了注释，以指定要在选择下拉列表中显示的流连接要求。 [了解详情](../landing-pages/lp-forms.md#create-form-preset)

* 现在，“决策”部分提供了新的页面，介绍如何配置数据收集以跟踪展示次数、点击量和自定义事件。 [了解详情](../experience-decisioning/data-collection/schema-requirement.md)

* 重新组织了使用AI助手文档生成内容，以提高清晰度和可用性。 前五个特定于渠道的页面（电子邮件、推送、短信、Web和登陆页面）已合并为三个生成类型的页面：[生成完整内容](../content-management/generative-full-content.md)、[生成文本](../content-management/generative-text.md)和[生成图像](../content-management/generative-image.md)。

## 2025 年 11 月 {#november-2025}

* 现已提供新的Decisioning常见问题解答页面，其中涵盖了上限规则、AI模型配置、流量要求和选件优化策略等主题。 [了解详情](../experience-decisioning/decisioning-faq.md)

* “电子邮件设计入门”页面已更新，明确说明如何访问电子邮件设计器。[了解详情](../email/get-started-email-design.md)

* “DMARC 记录”页面添加了故障排除部分，以解决 DNS 传播延迟问题。[了解详情](../configuration/dmarc-record.md#troubleshooting)

* “使用 GenStudio for Performance Marketing”页面已得到改进，新增了多个部分，包括关键功能、常见用例、先决条件和常见问题。[了解详情](../integrations/genstudio.md)

* “护栏和限制”页面新增了有关使用入站渠道将匿名轮廓选择为目标的护栏：将未经身份验证的访客选择为目标会增加可互动轮廓的总数量，因此 Adobe 建议设置生存时间 (TTL) 以自动删除轮廓，从而管理相关成本。[了解详情](../start/guardrails.md#profile-management-inbound)

* 为决策和基于代码的体验配置 Web SDK 的两个教程现在可在基于代码的实施方法示例页面上引用。[了解详情](../code-based/code-based-decisioning-implementations.md#tutorials)

* 已添加注释，详细说明从首次发布起到至多 2 年（730 天）内仍可访问资产和图像，并且过期后需要重新发布。[了解详情](../content-management/proofs.md)

* 现在提供全面的 AI 助手内容提示指南。本指南将教您如何给出有效的提示，以创建与品牌形象一致的高转化率营销内容。了解编写营销目标、使用品牌资产和针对不同渠道优化内容的最佳实践。[了解详情](../content-management/ai-assistant-prompting-guide.md)

* 在区段定义文档中添加了注释，明确说明不支持在区段定义中使用 `frequencyMap` 属性，不能将其用作受众细分标准。对于基于频率的目标选择，请考虑使用业务规则下的频率上限规则。[了解详情](../audience/creating-a-segment-definition.md)
* API 调用响应文档中添加了一个新示例，说明如何在原生渠道中使用自定义操作响应。该示例演示了如何在电子邮件、推送内容和短信消息中使用 Handlebars 语法，对自定义操作响应中的嵌套数组进行迭代。[了解详情](../action/action-response.md#response-in-channels)

* Campaign v7/v8 集成文档中添加了新章节，介绍在实时 (RT) 端点发生更改时如何更新现有自定义操作。此部分包含更新端点 URL、测试连接以及在保存之前验证更改的分步说明。[了解详情](../action/acc-action.md#update-action)

* 在可视化片段文档中添加了新限制和最佳实践部分，警告用户不支持将包含动态内容的片段嵌套在其他未锁定的片段中。该指南包括兼容性模式问题的故障排除步骤，以及有关正确电子邮件结构设计的建议。[了解详情](../email/use-visual-fragments.md#fragment-dynamic-content)

* 历程实时报告文档中添加了故障排除部分，帮助用户解决缺少报告数据的问题。该部分涵盖历程名称与报告数据集之间的同步、数据刷新时点、访问权限验证和历程状态要求。[了解详情](../building-journeys/report-journey.md#troubleshooting-missing-data)

* 资产文档中添加了三个新的常见问题，解释资产有效期限和生命周期管理。涵盖的主题包括 AEM 资产的生存时间 (TTL) 策略（730 天）、如何解决由于资产到期而失效的图像，以及即将对资产有效期限逻辑做出的改进。[了解详情](../integrations/assets.md#faq-assets)

* 在读取受众活动文档中添加了内容全面的故障排除部分，帮助解决进入历程的估计轮廓和实际轮廓之间的受众计数不匹配问题。此部分涵盖时点和数据传播问题、数据验证和监控技术，以及包括使用“批量受众评估后触发”选项在内的最佳实践。[了解详情](../building-journeys/read-audience.md#audience-count-mismatch)

* 受众资格筛选事件文档中添加了注释，介绍了流式分段延迟（最多 2 小时），并建议对时间敏感型历程添加等待活动或缓冲时间。[了解详情](../building-journeys/audience-qualification-events.md#streamed-speed-segment-qualification)

* 在电子邮件护栏中新增了一个部分，说明了历程发布的消息内容大小限制为 2MB，包括将创作内容保持在 1MB 以下的最佳实践，以便为后端处理留有余地。[了解详情](../start/guardrails.md#message-content-size)

* 增强了读取受众活动中增量读取选项的文档，以阐明快照时点依赖关系和 24 小时回顾限制，包括防止轮廓缺失的建议。[了解详情](../building-journeys/read-audience.md)

* 数据集查找护栏中增加了一条注释，指明查找无法链接在一起。[了解详情](../data/lookup-aep-data.md#guidelines)

* WhatsApp 和 LINE 渠道现在可用于“操作”营销活动。[了解详情](../campaigns/campaign-content.md)

* 在进入管理文档中新增了一个关于历程处理率的内容全面的小节，涵盖了轮廓进入率、历程中的事件和受众资格、等待活动的影响以及操作活动的影响。[了解详情](../building-journeys/entry-management.md#journey-processing-rate)

* 设计电子邮件时，系统现在会检查关键设置，并显示警告和错误警报。“护栏”页面中添加了有关电子邮件警报和验证要求的信息。[了解详情](../email/create-email.md#check-email-alerts)

* 在产品建议页面的“添加”约束条件中，删除了无法为先前创建的产品建议启用或禁用频率上限的警告注释。[了解详情](../offers/offer-library/add-constraints.md#capping)

* 现已发布有关如何使用历程步骤事件的文档。[了解详情](../reports/journey-step-events-overview.md)

* 现在提供了有关历程进入和退出标准的新综合指南，其中涵盖最佳实践、现实世界示例以及在Adobe Journey Optimizer中管理用户档案进入和退出历程时的实际指南。 [了解详情](../building-journeys/entry-exit-criteria-guide.md)

* 现在提供了新页面，其中说明如何对消息中的上下文数据进行迭代。 本指南介绍如何使用Handlebars语法显示个性化设置中事件、自定义操作响应、数据集查找和其他上下文源的动态列表。 [了解详情](../personalization/iterate-contextual-data.md)

* 用于识别历程中被丢弃事件的查询已更正，针对区段导出作业错误、调度程序丢弃和状态机丢弃添加了适当的过滤器。[了解详情](../reports/query-examples.md#common-queries)

* 为查询示例文档中的所有 37 个查询示例添加了介绍性语句，以提供更好的上下文并解释每个查询在呈现 SQL 代码之前的作用。这样可增进用户了解，并提供有关何时使用每个查询的更明确的指导。[了解详情](../reports/query-examples.md)

## 2025 年 10 月 {#october-2025}

* 您现在可以使用图像到 HTML 转换器，将图像转换为 HTML 模板。[了解详情](../email/image-to-html.md)

* 现在提供了有关 Adobe Journey Optimizer 发行周期的信息。[了解详情](releases.md)

* 现已提供新的历程常见问题页面。[了解详情](../building-journeys/journey-faq.md)

* 现已提供监控自定义操作功能。[了解详情](../action/reporting.md)

* 现已提供 API 触发的营销活动的高吞吐量模式。[了解详情](../campaigns/api-triggered-high-throughput.md)

* 现已提供历程的错误代码参考。[了解详情](../building-journeys/error-codes-reference.md)

* Journey Optimizer Experimentation Accelerator 文档现已发布。[了解详情](../content-management/experiment-accelerator-gs.md)

* **formatDate** 辅助函数文档中新增了一节内容。本节阐明了关键模式符号（如 y、Y、M、d 和D）的含义。[了解详情](../personalization/functions/dates.md#pattern-characters)

* 在决策排名公式部分添加了 PQL 示例，以说明如何根据轮廓的邮政编码和年收入改进产品建议。[了解详情](../experience-decisioning/ranking/ranking-formulas.md#ranking-formula-examples)

* 在历程测试模式部分中增添了一项限制，说明测试模式不支持自定义上传受众属性扩充。[了解详情](../building-journeys/testing-the-journey.md#important_notes)

* 在[决策管理护栏和限制](../offers/decision-management-guardrails.md#configurations)以及[决策护栏和限制](../experience-decisioning/decisioning-guardrails.md#configurations)页面中添加了一个新小节，用于说明支持的最大配置数 (20,000)，对应于您的沙盒中存在的上限规则总数。

* 在历程的“条件”活动部分中添加了注释，以说明包含两个以上跨设备身份的轮廓的条件评估将会失败。[了解详情](../building-journeys/condition-activity.md)

* 新增了一个页面，描述如何使用同意政策，根据客户的选择尊重他们的偏好，同时尊重他们的同意。 [了解详情](../action/preference-center.md)

* 轮廓快速入门和护栏页面中添加了注释，说明在摄取数据时电子邮件区分大小写，这意味着在选择相应的目标收件人时可能会创建和使用重复的轮廓。[了解详情](../audience/get-started-profiles.md)

* 个性化编辑器中引入了新的 `render` 属性。将其设置为 `false` 以隐藏表达式片段的内容。[了解详情](../personalization/use-expression-fragments.md#use-expression-fragment)

* 在描述如何在决策策略中利用附加到决策项的片段的部分中添加了护栏列表。[了解详情](../experience-decisioning/create-decision.md#guardrails-limitations)

* 添加了数据集查找的最佳做法：保持切换按钮打开以避免索引问题，然后了解批量删除对查找数据的影响。[了解详情](../data/lookup-aep-data.md#guidelines)

* 添加了限制，以说明在将读取受众历程与补充标识符结合使用时，仅支持统一轮廓服务受众。[了解详情](../building-journeys/supplemental-identifier.md#guardrails)

* Experimentation Accelerator 文档已移至单独的收藏集。[了解详情](https://experienceleague.adobe.com/zh-hans/docs/experimentation-accelerator/using/overview)

## 2025 年 9 月 {#september-2025}

* 在“护栏和限制”页面中新增了“入站渠道”部分，以收集适用于 Web、应用程序内、基于代码的体验和内容卡渠道的所有限制。这包括所有入站请求的峰值容量限制（每秒 5,000 个入站请求），以及最多 500 个活动入站操作。[了解详情](../start/guardrails.md#inbound-guardrails)

* 已针对编排的营销活动发布“常见问题解答”页面。[了解详情](../orchestrated/orchestrated-campaigns-faq.md)

* 历程步骤事件文档添加了故障排除部分，其中包含最常被丢弃的 eventTypes 的定义、常见原因和故障排除步骤。[了解详情](../reports/sharing-field-list.md#discarded-events)

* 有关如何在历程中使用补充标识符的文档现在包含一个表，详细说明在使用补充 ID 的历程中应用退出标准时轮廓的行为特点。[了解详情](../building-journeys/supplemental-identifier.md#exit-criteria)

* 新增了故障排除部分，以帮助理解暂停历程中的轮廓丢弃。[了解详情](../building-journeys/journey-pause.md#discards-troubleshoot)

* 架构概述文档中添加了信息，以区分用于编排的营销活动的标准架构和关系架构。[了解详情](../data/gs-data.md)

* 决策和决策管理文档中添加了有关成功训练[自动优化](../experience-decisioning/ranking/auto-optimization-model.md)和[个性化优化](../experience-decisioning/ranking/personalized-optimization-model.md)模型的要求的信息。

* 说明了交互式消息执行 REST API 调用设有 60 秒超时限制，并通过内部重试机制确保完成投放。[了解详情](../campaigns/trigger-campaigns.md)

* 更新了决策项集合页面，进一步说明定义规则时 **CONTAINS** 运算符的行为特性。[了解详情](../experience-decisioning/collections.md)

* 更新了分配优先级分数页面，新增在&#x200B;**操作**&#x200B;活动中为入站渠道操作定义优先级分数的具体步骤。[了解详情](../conflict-prioritization/priority-scores.md#priority-action)

## 2025 年 8 月 {#august-2025}

* 新增页面详细列出了使用 [!DNL Journey Optimizer] 设计无障碍电子邮件和登陆页面内容的最佳实践。[了解详情](../email/accessible-content.md)

* 更新了历程中的补充标识符的相关文档，提供了以下说明：

   * 将补充标识符添加到架构后，必须创建新事件（适用于事件触发的历程）或新字段组（适用于读取受众历程）。现有实体不会自动刷新，且将无法识别新标识符。

   * 不会根据数据使用标签和执行 (DULE) 策略对补充标识符进行验证，并且不在历程中的数据治理检查的考虑范围内。

[了解更多信息](../building-journeys/supplemental-identifier.md)

* 更新了营销活动页面中的“优化”部分，以反映优化功能现在也可用于历程的事实。[了解详情](../campaigns/campaigns-message-optimization.md)

* 添加了教程视频链接，描述如何在营销活动中利用消息优化。[了解详情](../campaigns/campaigns-message-optimization.md)

## 2025 年 7 月 {#july-2025}

* 营销活动界面现在具有两个单独的选项卡：**操作**&#x200B;和 **API 触发**。已对文档进行了相应更新，有关每种营销活动类型的信息将在多个专门的章节中阐述，以便提高清晰度和实用性。[了解详情](../campaigns/get-started-with-campaigns.md)

* [子域委派入门](../configuration/about-subdomain-delegation.md)和[委派子域](../configuration/delegate-subdomain.md)页面已更新，以更好地展示不同的委派方法和设置这些方法的步骤。

* 在“片段”部分中添加了注释，指出在历程或营销活动中启用跟踪时，如果您向某个片段添加链接，并且在消息中使用了该片段，则会跟踪这些链接，例如消息中包含的所有其他链接。[了解详情](../content-management/create-fragments.md#content)

* Journey Optimizer 中适用于子域委派的护栏和限制已扩充并整合到一个专门部分中。[了解详情](../configuration/delegate-subdomain.md#guardrails)

* 在“创建后备产品建议”和“创建决策”页面中添加了注释，指出后备产品建议应包含决策中使用的所有呈现。[了解详情](../offers/offer-library/creating-fallback-offers.md)

* 适用于片段的护栏已扩充。[了解详情](../start/guardrails.md#fragments-guardrails)。

* 添加了注释，指出添加到消息的链接会在 25 个月后过期，而指向镜像页面的链接会在 90 天后过期。[了解详情](../email/message-tracking.md)

<!--* The possible email error types that could happen upon sending email deliveries with are now listed in a dedicated section. [Read more](../configuration/email-error-types.md)-->

## 2025 年 6 月 {#june-2025}

* 添加了新的小节，介绍如何通过 HTML 组件添加和使用换行符、粗体、斜体等富文本，从而自定义片段。[了解详情](../content-management/customizable-fragments.md#rich-text)

* 更新了“决策”部分，添加了专门介绍 AI 模型构建的特定章节。[了解详情](../experience-decisioning/ranking/ai-models.md)

* 添加了关于在 journeyStep 事件操作中使用 `actionExecutionTime` 字段的建议。[了解详情](../reports/sharing-execution-fields.md#actionexecutiontime-field)

* 添加了关于 `messageID` 的注释，它对于每个单独投放来说可能并不是唯一的。[了解详情](../data/datasets-query-examples.md)

* 添加了关于数据卫生操作中的历史事件管理的建议。[了解详情](../privacy/data-hygiene.md#data-hygiene-recommendations)

* 添加了关于不支持在沙盒之间迁移登陆页面的护栏。[了解详情](../configuration/copy-objects-to-sandbox.md#global)

* 添加了关于自定义操作的自定义身份验证中不支持嵌套 JSON 对象的警告注释。[了解详情](../datasource/external-data-sources.md)

* 添加了关于电子邮件设计器中的条件内容变体命名的警告注释。[了解详情](../personalization/create-conditions.md)

* 更新了“取消委派登陆页面子域”部分。[了解详情](../landing-pages/lp-subdomains.md#undelegate-subdomain)

* 介绍了使用补充标识符时的历程重新进入规则。[了解详情](../building-journeys/supplemental-identifier.md#guardrails)

* 添加了新注释，明确说明在事件配置期间选择补充标识符属性时，必须在高级模式下使用表达式编辑器。[了解详情](../building-journeys/supplemental-identifier.md#add)

* 添加了关于历程重新进入和补充标识符的说明。[了解详情](../building-journeys/supplemental-identifier.md#guardrails)

## 2025 年 5 月 {#may-2025}

* “连接系统和环境”部分中现在列出了可用于 Journey Optimizer 的 Adobe 集成。[了解详情](../integrations/ajo-integrations.md)

* 内容集成现已归入“内容管理”部分。[了解详情](../integrations/content-integrations.md)

* Adobe Experience Platform 和 Journey Optimizer 的架构图已更新。[了解详情](../start/get-started.md#architecture)

* 添加了有关个性化编辑器游乐场的视频，以帮助您了解如何使用示例数据编写和测试个性化代码。[了解详情](../personalization/personalize.md#video-perso)

* 每个种子列表中的地址数量上限已由 50 个增至 300 个。[了解详情](../configuration/seed-lists.md#create-seed-list)

* 在“创建决策策略”页面中添加了一个新步骤，其中详细说明了在基于代码的体验编辑器中使用决策策略时如何封装代码。[了解详情](../experience-decisioning/create-decision.md#create-decision)

* 向基于代码的体验文档中添加了注释，说明了当在同一个表面上运行多个基于代码的体验操作时，如果最终用户符合多个操作的条件，则营销活动或历程的优先级分数将决定向最终用户投放的内容。[了解详情](../code-based/code-based-surface.md#surface-definition)

* 有关对历程入站操作进行故障排除的新页面提供了分步指南，可帮助用户在联系支持人员之前独立识别并解决问题。[了解详情](../building-journeys/troubleshooting-inbound.md)

* 添加了新的[页面](../code-based/code-based-decisioning-implementations.md)，说明在基于代码的体验中使用决策功能时，如何向客户端实施添加以下标志：

   * 将会把 `dryRun` 标志添加到基于代码的体验中的测试决策。[了解详情](../code-based/code-based-decisioning-implementations.md#code-based-test-decisions)

   * 将重复数据删除应用于基于代码的体验中的决策请求。[了解详情](../code-based/code-based-decisioning-implementations.md#code-based-decisioning-deduplication)

## 2025 年 4 月 {#apr-2025}

* 配置章节现在分为三章：[渠道配置](../configuration/get-started-configuration.md)、[历程配置](../configuration/about-data-sources-events-actions.md)和[连接系统](../configuration/ajo-apis.md)。
* 添加了有关在历程表达式和条件中使用体验事件的警告说明。[了解详情](../building-journeys/expression/expressionadvanced.md#discovering-the-interface)
* 在直邮配置页面上添加了有关输出文件临时存储的说明。[了解详情](../direct-mail/direct-mail-configuration.md)
* 在历程高级表达式编辑器部分中添加了有关条件格式准则的提示。[了解详情](../building-journeys/expression/expressionadvanced.md)
* 在 `inAudience` 函数部分中添加了关于重命名受众的影响和最佳实践的警告说明。[了解详情](../building-journeys/functions/functioninaudience.md)
* 添加了有关使用双向短信时本机关键词用法的建议。[了解详情](../sms/sms-opt-out.md)
* 更新了历程测试页面，其中包括需要在使用的事件中包含身份标识命名空间的说明。[了解详情](../building-journeys/testing-the-journey.md)
* 目前，您无法通过 [!UICONTROL Journey Optimizer] 用户界面取消委派子域，您必须联系 Adobe 代表。目前，已针对[电子邮件](../configuration/delegate-subdomain.md#undelegate-subdomain)、[短信](../sms/sms-subdomains.md#undelegate-subdomain)、[Web 体验](../web/web-delegated-subdomains.md#undelegate-subdomain)以及[登陆页](../landing-pages/lp-subdomains.md#undelegate-subdomain)详细阐述了取消委派子域的步骤。<!--[Read more](../configuration/delegate-subdomain.md#undelegate-subdomain)-->
* 添加了历程上限 API 中可选 `maxHttpConnections` 参数的说明，包括如何将其与同一端点的限制配置一起使用的指南。[了解详情](../configuration/throttling.md)
* 在“决策”部分中添加了指南，说明如果批准的优惠项目用在收藏集或决策中，则无法删除这些项目。 包括使用&#x200B;**[!UICONTROL 撤消批准]**&#x200B;选项将其状态更改为“草稿”的步骤。[了解详情](../experience-decisioning/items.md#manage)
* 有关沙盒的信息已分组到新的“沙盒管理”部分。本新部分提供了关于如何使用和分配沙盒的信息，以及如何借助资源包导出和导入功能，在多个沙盒之间复制诸如历程、内容模板或片段等对象。[了解详情](../administration/sandboxes.md)

## 2025 年 3 月 {#mar-2025}

* 更新了“受众资格”事件的相关页面，提供了新的建议。[了解详情](../building-journeys/audience-qualification-events.md)
* 现在，所有客户都可以使用自定义操作故障排除功能 (GA)。[了解详情](../action/troubleshoot-custom-action.md)
* 在产品用户界面中，“数据卫生”已更名为“数据生命周期”。更新了文档以反映此更改。[了解详情](../privacy/data-hygiene.md)
* 文档中新增了有关缺失的登陆页面内置权限的内容。[了解详情](../administration/ootb-permissions.md)
* 添加了有关安排定期营销活动的注释。[了解详情](../campaigns/create-campaign.md)
* 更新并重新组织了有关在电子邮件中插入链接和启用跟踪的部分。[了解详情](../email/message-tracking.md)
* 重新组织并改进了有关 Adobe Journey Optimizer 中的个性化功能的部分。[了解详情](../personalization/personalize.md)
* 更新了用于列出个性化优惠的决策管理API，新增了在响应中缺少多个个性化优惠时执行分页的示例。 [了解详情](../offers/api-reference/offers-api/personalized-offers/offers-list.md)
* 为使内容更加清晰易懂，创建了一个新页面，收集了有关列表取消订阅功能的所有信息。[了解详情](../email/list-unsubscribe.md)
* 频率上限部分已更新，除 Edge Decisioning API 外，其中包含关于如何为 Decisioning 和 Batch Decisioning API 更新频率上限计数器的信息。[了解详情](../offers/offer-library/add-constraints.md#frequency-capping)

## 2025 年 2 月 {#feb-2025}

* 更新了“读取受众”活动护栏，明确规定历程中只能使用一种活动，并且只能针对一个受众。[了解详情](../building-journeys/read-audience.md)
* 更新了使用 Adobe Campaign 活动时的历程护栏。[了解详情](../start/guardrails.md#ac-g)
* 详细介绍了创建第一个历程的步骤，并添加了文档部分的链接。[了解详情](../building-journeys/journey-gs.md)
* 现在提供了新页面，详细介绍了历程仪表板和筛选用户界面。[了解详情](../building-journeys/journey-ui.md)
* 更新并改进了&#x200B;**[!UICONTROL 发送时间优化]**&#x200B;的文档及其相关常见问题解答，且已将它们移至新的专门页面。[了解详情](../building-journeys/send-time-optimization.md)
* 为历程事件添加了新护栏。[了解详情](../start/guardrails.md#events-g)
* 重组了内置渠道操作页面。[了解详情](../building-journeys/journeys-message.md)
* 在“决策”和“决策管理”部分中添加了护栏和限制。
   * [决策护栏和限制](../experience-decisioning/decisioning-guardrails.md)
   * [决策管理护栏和限制](../offers/decision-management-guardrails.md)
* 在决策管理文档中添加了有关上下文数据的新部分。它介绍了如何在决策引擎中利用上下文数据，例如，设计一个要求在发出决策请求时当前天气 ≥80 度的决策规则。[了解详情](../offers/context-data.md)

## 2025 年 1 月 {#jan-2025}

* 新添加了一个有关电子邮件配置中的&#x200B;**[!UICONTROL 执行地址]**&#x200B;选项的部分。主地址是在沙盒级别定义的，但对于特定电子邮件配置，可以覆盖默认设置。[了解详情](../email/email-settings.md#execution-address)

* **可投放性入门**&#x200B;页面已更新，可以直接从用户界面创建 IP 预热工作流。[了解详情](../reports/deliverability.md#reputation)

* **标头参数**&#x200B;部分已更新，以反映用户界面中的新标签和更改。[了解详情](../email/email-settings.md#email-header)

* **转发电子邮件**&#x200B;部分已更新，以指定将所有发送到&#x200B;**发件电子邮件**&#x200B;地址的电子邮件转发到转发电子邮件地址。如果未指定转发电子邮件，则将丢弃这些电子邮件。[了解详情](../email/email-settings.md#email-settings)

* 传递到 API 触发营销活动请求的最大上下文属性大小已更新为 200 kb。[了解详情](../campaigns/api-triggered-campaigns.md#contextual)

* **管理片段**&#x200B;页面中添加了新部分，以说明如何向实时片段添加新属性。此外，对整个页面进行了改进。[了解详情](../content-management/manage-fragments.md#adding-new-attributes)

* 冲突管理和优先级设置工具文档中添加了“护栏和限制”部分。[了解详情](../conflict-prioritization/gs-conflict-prioritization.md)

* 添加了新的端到端用例，展示通过 [!DNL Journey Optimizer] 基于代码的体验渠道在内容试验中使用决策功能所需的所有步骤。[了解详情](../experience-decisioning/experience-decisioning-uc.md)

* 为了提高可读性，**配置电子邮件设置**&#x200B;页面已划分为多个子页面，包括专门介绍[列表取消订阅](../email/list-unsubscribe.md)、[标头参数](../email/header-parameters.md)和 [URL 跟踪](../email/url-tracking.md)的新独立页面。

## 2024 年 12 月 {#nov-2024}

* 添加了一个注释，在使用 Adobe Experience Platform 数据进行 API 调用以允许将数据集用于个性化时，这有助于解决可能出现的错误消息。[了解详情](../personalization/aep-data-perso.md)

## 2024 年 10 月 {#oct-2024}

* 文档中详细介绍了 [!DNL Journey Optimizer] 2024 年 10 月版的所有新增功能和改进。[了解详情](release-notes.md)
* [!DNL Journey Optimizer] 中可用的所有通信渠道现在都集中到文档的一个专门部分中。[了解详情](../channels/gs-channels.md)
* **配置基于代码的体验**&#x200B;页面已得到改进，流程更加清晰，包括说明什么是表面 URI 的部分。[了解详情](../code-based/code-based-configuration.md)
* **创建网页渠道配置**&#x200B;页面已更新，介绍了创建页面匹配规则时的步骤，这些步骤也适用于基于代码的体验配置。[了解详情](../web/web-configuration.md#web-page-matching-rule)
* 添加了关于即将推出的系统生成数据集的生存时间 (TTL) 护栏的说明。[了解详情](../data/get-started-datasets.md)
* 新增了一个部分，介绍如何在模拟历程或营销活动中的内容时，使用&#x200B;**在设备上预览**&#x200B;选项，在浏览器或移动设备上预览基于代码的个性化体验。[了解详情](../code-based/test-code-based.md#preview-on-device)
* 添加了有关如何利用自定义上传受众进行决策的新页面。[了解详情](../offers/custom-upload-decisioning.md)
* 添加了介绍 Journey Optimizer 中的决策功能的新页面。[了解详情](../experience-decisioning/gs-decision.md)
* 决策文档中添加了有关护栏和限制的内容。[了解详情](../experience-decisioning/gs-experience-decisioning.md#guardrails)

## 2024 年 9 月 {#sept-2024}

* 文档中详细介绍了 [!DNL Journey Optimizer] 2024 年 9 月版的所有新增功能和改进。[了解详情](release-notes.md)
* 添加了关于历程重试管理的部分。[了解详情](../building-journeys/read-audience.md#read-audience-retry)
* 更新了有关自定义操作上限/限制规则的常见问题解答，并介绍了默认的上限规则。[了解详情](../configuration/external-systems.md#faq)
* 更新了“控制访问权限”部分，其中包含与 AI 助手内容生成器相关的权限。[了解详情](../administration/high-low-permissions.md#ai-orchestrated-campaign)
* 添加了有关使用 AI 助手内容生成器生成电子邮件的视频。[了解详情](../content-management/generative-full-content.md#video)

<!--

## August 2024 {#aug-2024}

* All new features and improvements coming with [!DNL Journey Optimizer] August '24 release have been detailed in the documentation. [Read more](release-notes.md)
* Performance guardrails for Decision management have been updated to mention Decisioning APIs delivery throughputs with/without Edge Segmentation. [Read more](../start/guardrails.md#decision-management)
* Journey guardrails have been updated. [Read more](../start/guardrails.md#journeys-guardrails-journeys)


## July 2024 {#july-2024}

* All new features and improvements coming with [!DNL Journey Optimizer] July '24 release have been detailed in the documentation. [Read more](release-notes.md)
* A personalization use case has been added on how to personalize an email with information related health plans and prescriptions. [Read more](../personalization/perso-uc-plan-prescriptions.md)

## June 2024 {#june-2024}

* All new features and improvements coming with [!DNL Journey Optimizer] June '24 release have been detailed in the documentation. [Read more](release-notes.md)
* A note about the usage of merge policies in journeys has been added on [this page](../building-journeys/journey-properties.md#merge-policies).
* The page about how to configure a **Wait** activity in a journey has been reorganized and improved. [Read more](../building-journeys/wait-activity.md)
* A new page has been created to detail journey's properties. [Read more](../building-journeys/journey-properties.md)

## May 2024 {#may-2024}

* All new features and improvements coming with [!DNL Journey Optimizer] May '24 release have been detailed in the documentation. [Read more](release-notes.md)
* The section on seed lists has been updated regarding recurring journeys. [Read more](../configuration/seed-lists.md#use-seed-list)
* The setion on external data sources has been updated. [Read more](../datasource/external-data-sources.md#custom-authentication-access-token)
* The global journey timeout of 30 days has been added to the Guardrail and limitation page. [Read more](../start/guardrails.md#journeys-guardrails-journeys)
* The section on the Adobe Campaign v7/v8 integration has been updated with information on provisionning. [Read more](../action/acc-action.md#access)
* The expression editor used to personalize content has been renamed in the documentation to "personalization editor" to clearly differenciate it from the [Journey expression editor](../building-journeys/expression/expressionadvanced.md). [Read more](../personalization/personalization-build-expressions.md)

## April 2024 {#april-2024}

* All new features and improvements coming with [!DNL Journey Optimizer] April '24 release have been detailed in the documentation. [Read more](release-notes.md#apr-2024)
* Configuration steps for In-app messaging have been detailed. [Read more](../in-app/inapp-configuration.md)
* Documentation for [Offer decisioning APIs](../offers/api-reference/offer-delivery-api/decisioning-api.md) and [Batch decisioning APIs](../offers/api-reference/offer-delivery-api/batch-decisioning-api.md) have been updated.
* Information has been added in the Decision management documentation regarding edge and hub regions management when using frequency capping with the Edge Decisioning API. [Read more](../offers/offer-library/add-constraints.md#frequency-capping)
* Information has been added on identity creation with custom namespaces when working with API-triggered campaigns. [Read more](../campaigns/api-triggered-campaigns.md)
* Screeshots have been updated to reflect the improved Journey canvas.
* Naming constraints has been updated in the following page: [Configure a unitary event](../event/about-creating.md), [Configure a business event](../event/about-creating-business.md#gs-business-events), [Configure a custom action](../action/about-custom-action-configuration.md#configuration-steps), [External data sources](../datasource/external-data-sources.md)
* A note has been added on Send Time Optimization availability. [Read more](../building-journeys/send-time-optimization.md)
* A new technical use case has been added on how to create a custom action to send data to Experience Platform. [Read more](../building-journeys/custom-action-aep.md)

## March 2024 {#march-2024}
 
* A Frequently Asked Questions section has been added to address common questions regarding the use of audience composition and custom upload audiences in Journey Optimizer. [Read more](../audience/about-audiences.md#faq)
* All new features and improvements coming with [!DNL Journey Optimizer] March '24 release have been detailed in the documentation. [Read more](release-notes.md#mar-2024)
* The page on profile entrance management has been improved. [Read more](../building-journeys/entry-management.md)
* Troubleshooting information has been added to the Alerts page. [Read more](../reports/alerts.md#alert-profile-error-rate)
* Information on the Wait activity has been added to the page on journey reports. [Read more](../reports/sharing-overview.md)
* For Journeys in test mode, following shortcuts have been disabled:
    * T: Shortcut to toggle the test mode on or off.
    * E: Shortcut used to trigger an event in an event-based journey.
    * P: Shortcut to trigger an event in an audience-based journey for which the Single profile at a time option is turned on.
    * L: Shortcut designated to display the test logs.
* The Message frequency rules page has been updated with a new subsection on daily frequency cap, which is available on demand in addition to weekly or monthly capping.
* The Work with consent policies page has been improved and updated with useful links to the Experience Platform documentation. [Read more](../action/consent.md)
* A new section has been added to reflect the fact that you can display HTML email content templates as thumbnails with the Grid view mode (Limited Availability). [Read more](../content-management/content-templates.md#template-thumbnails)
* A new section has been added to the Deliverability page to explain what feedback loops are and how to leverage them. [Read more](../reports/deliverability.md#feedback-loops)
* A note has been added to the Create personalized offers section to specify that the size of an offer including all its representations cannot exceed 300KB. [Read more](../offers/offer-library/creating-personalized-offers.md#create-offer)

## February 2024 {#feb-2024}

* All new features and improvements coming with [!DNL Journey Optimizer] February '24 release have been detailed in the documentation. [Read more](release-notes.md#feb-2024)
* The Journey Optimizer + Workfront integration has been added to the integrations page. [Read more](../integrations/ajo-integrations.md)
* Information has been added on how to personalize offers' representations based on context data. [Read more](../offers/offer-library/add-representations.md#context-data)
* The guardrails page has ben updated with a note on custom actions which support JSON format only when using request or response payloads. [Read more](../start/guardrails.md#custom-actions-g)
* Additional information has been added about the basic authentication type in external datasources. [Read more](../datasource/external-data-sources.md)
* A note has been added to clearly differenciate the [Journey expression editor](../building-journeys/expression/expressionadvanced.md) from the [personalization editor](../personalization/functions/functions.md).
* The list of functions available in the advanced expression editor has been updated. [Read more](../building-journeys/expression/functions.md)
* The page on the Split function has been updated. [Read more](../building-journeys/functions/functioninaudience.md)
* Information has been added regarding the impact of the opt-in or opt-out of push notifications on In-app messages. [Read more](../in-app/create-in-app.md)
* The Message frequency rules page has been updated to reflect the Duration options available in the user interface (weekly or monthly).
* The Edit a PTR record section has been updated to clarify the fact that PTR records cannot be created manually and that you need to edit PTR records to assign them new subdomains. [Read more](../configuration/ptr-records.md#edit-ptr-record)

## January 2024 {#jan-2024}

* All new features and improvements coming with [!DNL Journey Optimizer] January '24 release have been detailed in the documentation. [Read more](release-notes.md)
* A guardrail about the journey size has been added. [Read more](../start/guardrails.md#journeys-guardrails-journeys)
* Journey timeout management has been detailed [in the following section](../building-journeys/journey-properties.md#global_timeout).
* Journey Optimizer [documentation home](../../ajo-home.md) page has been redesigned.
* Recommendations about the Update Profiles activity have been added. [Read more](../building-journeys/update-profiles.md) 
* Information has been added regarding the behavior of timeouts on event activities in journeys. When no event is received during the specified timeout period, individuals will continue the journey if no timeout path is defined. [Read more](../building-journeys/general-events.md#events-specific-time)
* In-app channel configuration prerequisites have been updated with a note about the usage of a custom Dataset preference merge policy. [Read more](../in-app/inapp-configuration.md)
* More details have been added about how to manipulate collections in a custom action response. [Read more](../action/action-response.md#exp-syntax).
* A link to the [Schema Dictionary for Adobe Journey Optimizer](https://experienceleague.adobe.com/tools/ajo-schemas/schema-dictionary.html) has been added to the home page.
* An outdated reference to the AJO Message resource has been removed from the list of resources available in the Audit Log. When an update is done on a message in a journey, a **Journey** log is created. [Read more](../privacy/audit-logs.md)
* Additional recommendations have been added about the usage of the **Read Audience** activity. [Read more](../building-journeys/read-audience.md#must-read)
* The Get started with Adobe Experience Platform audiences page has been improved with a list of audience generation methods. [Read more](../audience/about-audiences.md)
* Best practices have been added when choosing an endpoint to target using a custom action. [Read more](../action/about-custom-action-configuration.md)
* An note has been added to notify users that events cannot be fired from external systems using an API. [Read more](../building-journeys/testing-the-journey.md#important_notes)
* Information on the **currentActionField** function has been added to the list of [collection management functions](../building-journeys/expression/collection-management-functions.md). An expression sample leveraging the function has been added in the [Use API call reponses in custom actions](../action/action-response.md) page.
* Update custom authentication doc regarding cache duration. [Read more] (../datasource/external-data-sources.md)
* Support of `<listObject>` has been modified in multiple functions.
* Update the **duration** parameter in the `toString` function. [Read more](../building-journeys/functions/conversion-functions.md#toString)
* For some external data sources use-cases, usage of custom actions is recommended.
* Event field syntax has been updated. The following syntax is deprecated `@(my_event.myfield}` and replaced by `@event{my_event.myfield}`. [Read more](../building-journeys/expression/field-references.md)

+++ 2023

## November 2023 {#nov-2023}

* The guardrail that limits all custom actions has been changed from 150,000 calls over 30 seconds to 300,000 calls over one minute. In addition, the default capping no longer applies to each endpoint. It is now performed per host and per sandbox. For example, on a sandbox, if you have two endpoints with the same host (eg: `https://www.adobe.com/endpoint1` and `https://www.adobe.com/endpoint2`), the capping will apply for all endpoints under the adobe.com host. "endpoint1" and "endpoint2" will share the same capping configuration and having one endpoint reach the limit will have an impact on the other endpoint. [Read more](../action/about-custom-action-configuration.md)
* A new status for email campaigns has been added to the list of campaigns' statuses. [Read more](../campaigns/manage-campaigns.md#modify-an-action-campaign)
* The Get started with Adobe Experience Platform audiences section has been updated to reflect the audience evaluation methods available and how to select them. [Read more](../audience/about-audiences.md#evaluation-method-in-journey-optimizer)
* A new subsection has been added to specify which events should be avoided when building your audience if you are using the streaming segmentation evaluation method. [Read more](../audience/about-audiences.md#streaming-segmentation-events-guardrails)

## October 2023 {#oct-2023}

* All new features and improvements coming with [!DNL Journey Optimizer] October '23 release have been detailed in the documentation. [Read more](release-notes.md)
* Added GIFs to illustrate some key capabilities, such as: [Content templates](../content-management/content-templates.md), [Fragments](../content-management/fragments.md), [Computed attributes](../audience/computed-attributes.md), [Direct mail](../direct-mail/get-started-direct-mail.md), [Tags](../start/search-filter-categorize.md#tags), [Decision management optimization models](../offers/ranking/personalized-optimization-model.md), [API-triggered campaigns](../campaigns/api-triggered-campaigns.md), and [Content experiment](../content-management/content-experiment.md).
* The Schema creation process has been updated to reflect latest updates in the user interface, coming with Adobe Experience Platform changes. [Read more](../audience/creating-test-profiles.md) 
* Decision management guardrails have been added to the Guardrails and limitations page. [Read more](../start/guardrails.md#decision-management)
* The Header parameters section has been updated to reflect how out-of-office notifications and challenge responses are handled (they are received on the **[!UICONTROL Error email]**). [Read more](../email/email-settings.md#email-header)
* A new section on how to preview and test your content has been created. [Read more](../content-management/preview-test.md)
* The Implement single-page applications page has been moved to the Adobe Experience Paltform Web SDK documentation. [Read more](https://experienceleague.adobe.com/docs/experience-platform/edge/personalization/ajo/web-spa-implementation.html){target="_blank"}
* The Capping section has been updated to reflect the label changes relating to offer capping in the Decision management interface. [Read more](../offers/offer-library/add-constraints.md#capping)
* The Add dynamic content into emails has been updated with details on how to delete a variant. [Read more](../personalization/dynamic-content.md#emails)
* The example for capping & throttling configurations has been updated. [Read more](../configuration/external-systems.md)
* The limitation regarding scalar arrays has been removed from the external data source section. [Read more](../datasource/external-data-sources.md)
* The multi-channel journey use case has been updated. [Read more](../building-journeys/journeys-uc.md)
* The Journey Optimizer documentation set has been updated to reflect the new Experience Platform schema creation process. 

## September 2023 {#september-2023}

* All new features and improvements coming with [!DNL Journey Optimizer] September '23 release have been detailed in the documentation. [Read more](release-notes.md)
* A new page has been added with scaling best practices and real-time stitching guidance. [Read more](../start/best-practices.md)
* A Frequently-Asked-Questions section has been added for Send-Time Optimization. [Read more](../building-journeys/journeys-message.md#faq-send-time)
* A note has been added for the audience qualification activity. It may take up to 10 minutes to be active and listen to profiles entering or exiting the audience. [Read more](../building-journeys/audience-qualification-events.md#batch-speed-segment-qualification)
* A list of limitations to be aware of when creating decision rules has been added to the Decision management documentation. [Read more](../offers/offer-library/creating-decision-rules.md)
* Links to access control documentation have been updated. [Read more](../administration/permissions.md)
* In-app channel prerequisites have been updated with Adobe Experience Platform Data Collection details. [Read more](../in-app/inapp-configuration.md)
* Some expressions presented in ranking formula examples have been updated to avoid validation errors. [Read more](../offers/ranking/create-ranking-formulas.md#ranking-formula-examples)
* A warning has been added to the Define decision scopes section to specify that if AI model is used in an evaluation criteria group, all the evaluation criteria in that group must use the AI ranking method, with the same specific AI model. Moreover, only one evaluation criteria group can use AI model. [Read more](../offers/offer-activities/create-offer-activities.md#add-decision-scopes)

## August 2023 {#august-2023}

* All new features and improvements coming with [!DNL Journey Optimizer] August '23 release have been detailed in the documentation. [Read more](release-notes.md)
* The note about **authentication cache management** in journey has been updated to detail that the token is not shared between different journeys. [Read more](../datasource/external-data-sources.md#custom-authentication-mode)
* The page about journey **entry management** has been updated to clarify behavior. [Read more](../building-journeys/entry-management.md)
* Offer decisioning **export datasets** are now enabled by default. The note about the previous behavior has been removed.  [Read more](../offers/export-catalog/get-started-export.md)
* Various **campaign report metrics** have been renamed, in both Live and Global reports. [Read more](../reports/campaign-live-report.md)
* A new section has been added on content experiment prerequisites for the web channel. [Read more](../web/web-prerequisites.md#experiment-prerequisites)
* A warning has been added on the **Work with content templates** page to indicate that currently tracking is not supported when testing email content templates. To test tracking, you must use the content template in an email and send a proof. [Read more](../content-management/content-templates.md#content-templates)
* Several warnings have been added in the **Create and publish landing pages** section to specify that you cannot access your landing page by simply copy-pasting into a web browser the URL defined when creating the page, even if published. Instead you can test it using the preview function. [Read more](../landing-pages/create-lp.md)
* A new section has been added on how to **manage consent** for the direct mail channel. [Read more](../direct-mail/test-send-direct-mail.md)

## July 2023 {#july-2023}

* All new features and improvements coming with [!DNL Journey Optimizer] July '23 release have been detailed in the documentation. [Read more](release-notes.md)
* The wait activity documentation page has been improved with additional information and best practices related to the global timeout and reentrance usage. [Read more](../building-journeys/wait-activity.md)
* The page on entry management has been improved. [Read more](../building-journeys/entry-management.md)
* Additional information has been added about the throttling rate in the Read audience activity documentation. [Read more](../building-journeys/read-audience.md)
* Additional information has been added about retries. [Read more](../start/guardrails.md#general-actions-g)
* The **Implement personalization consent** section has been updated to describe how to manually enforce personalization consent in campaigns: you can use the segment rule builder to create an audience containing opt-out profiles or add a split activity to a composition workflow. [Read more](../privacy/opt-out.md#opt-out-expression-editor)

## June 2023 {#june-2023}

* All new features and improvements coming with [!DNL Journey Optimizer] June '23 release have been detailed in the documentation. [Read more](release-notes.md)
* Information has been added about the discard rate ratio in the Journeys overview screen. [Read more](../building-journeys/journey-gs.md#journey-access)
* A note has been added with the steps to follow if you modify your schema with new enumeration values after creating an event [Read more](../event/about-creating.md)
* A recommendation has been added to use journeyVersionID instead of journeyVersionName when querying journeys. [Read more](../reports/sharing-common-fields.md#journeyversionid-field)
* Additional examples on the evaluation criteria order have been added to the **Create decisions** section to illustrate cases where multiple criteria and multiple decision scopes are used. [Read more](../offers/offer-activities/create-offer-activities.md#evaluation-criteria-order)
* Decision management documentation has been clarified with a note specifying that the use of Object Level Access Control is not available for dynamic collections. [Read more](../offers/offer-library/creating-collections.md)

## May 2023 {#may-2023}

* All new features and improvements coming with [!DNL Journey Optimizer] May '23 release have been detailed in the documentation. [Read more](release-notes.md)
* A new page has been added to describe how to set up the subdomain that will be used to publish content coming from the Adobe Experience Manager Assets Essentials in your web experiences. [Read more](../web/web-delegated-subdomains.md)
* A new subsection has been added to explain how to add personalized tracking parameters to URLs in the Email Designer. [Read more](../email/message-tracking.md#url-tracking)
* A new section has been added to describe how to ensure that the choice of your customers who opt out from having their profile data used for personalization is honored. [Read more](../privacy/opt-out.md#opt-out-personalization)
* A note has been added about using special international characters in URLs included in email contents. [Read more](../email/message-tracking.md#insert-links)
* The permission needed to test and publish landing pages has been added. [Read more](../landing-pages/create-lp.md)
* A note has been added about the Adobe Experience Platform endpoints needed to have your custom events accounted for in Decision management frequency capping. [Read more](../offers/data-collection/schema-requirement.md#track-custom-events)

## April 2023 {#apr-2023}

* All new features and improvements coming with [!DNL Journey Optimizer] April '23 release have been detailed in the documentation. [Read more](release-notes.md)
* A note has been added to specify that built-in actions cannot be removed. [Read more](../start/guardrails.md#custom-actions-g)
* Information has been added on serviceEvents as well as a query example to check the details of a serviceEvent. [Read more](../reports/query-examples.md#common-queries) 
* A note has been added to specify that you cannot perform queries on time series. [Read more](../building-journeys/condition-activity.md)
* Adobe Experience Manager Assets Essentials and Adobe Stock have been added to the multi-solution integration page. [Read more](../integrations/ajo-integrations.md)
* The warning on multi-level email subdomains not being allowed has been removed as they are now supported. [Read more](../configuration/delegate-subdomain.md)
* A note has been added to specify that, if changes are made to an offer decision which is being used in a journey's message, you need to unpublish the journey and republish it. [Read more](../building-journeys/publish-journey.md)
* Explanation on how to make sure events are correctly accounted for in the capping counter has been clarified in the Decision management **Capping event** section. [Read more](../offers/offer-library/add-constraints.md#capping-event)
* A new section has been added to the **Change execution addresses** page. It specifies that it is possible to override the execution field set globally in the journey advanced parameters, but the email address override should only be used for specific use cases. Most of the time, the value defined as the primary address in the **Execution fields** is the one that should be used. [Read more](../configuration/primary-email-addresses.md#override-execution-address-journey)
* The **URL tracking** section now provides the list and description of all contextual attributes that can be set for URL tracking in an email channel configuration. [Read more](../email/email-settings.md#url-tracking)

## March 2023 {#march-2023}

* The Journey Optimizer schema dictionary is now available. You will find the complete list of fields and attributes for each schema.  [Read more](https://experienceleague.adobe.com/tools/ajo-schemas/schema-dictionary.html)
* All new features and improvements coming with [!DNL Journey Optimizer] March '23 release have been detailed in the documentation. [Read more](release-notes.md)
* Added a step to enable Adobe Analytics events in your journeys. [Read more](../event/about-analytics.md)
* A new section has been created in the Decision management guide on how to collect offer decisioning feedback in Adobe Experience Platform, including which offers are displayed and how users interact with them. [Read more](../offers/data-collection/data-collection.md)
* A new subsection has been added to the **Create decision** section to explain the difference between evaluating criteria in a sequential order or at the same time. [Read more](../offers/offer-activities/create-offer-activities.md#evaluation-criteria-order)
* A guardrail has been added for read audience journeys with incremental read. You cannot create a new version, you need to duplicate the journey. [Read more](../start/guardrails.md#journey-versions-g)
* The use case on how to limit throughput put has been updated with information on throttling capabilities. [Read more](../building-journeys/limit-throughput.md)
* A note has been added to specify that scalar arrays are not supported in response payload definition. [Read more](../datasource/external-data-sources.md)
* The section on profile cap conditions has been updated. [Read more](../building-journeys/condition-activity.md#profile_cap)

## February 2023 {#feb-2023}

* All new features and improvements coming with [!DNL Journey Optimizer] Feb '23 release have been detailed in the documentation. [Read more](release-notes.md)
* Information has been added about the canvas toolbar. [Read more](../building-journeys/using-the-journey-designer.md#gs-journey-design)
* Information has been added to state that internal Adobe addresses are not allowed in URLs and APIs. [Read more](../start/guardrails.md)
* A note has been added in the API-triggered campaigns documentation to specify that contextual attributes passed into the request cannot exceed 50kb. [Read more](../campaigns/api-triggered-campaigns.md#contextual)
* Information was added on how opt-out information is stored in the **Consent Service Dataset** after recipients are unsubscribed through a landing page. [Read more](../landing-pages/lp-use-cases.md#configure-opt-out)

## January 2023 {#jan-2023}

* All new features and improvements coming with [!DNL Journey Optimizer] Jan '23 release have been detailed in the documentation. [Read more](release-notes.md)
* Information has been added on custom authentication endpoints in the capping documentation. [Read more](../configuration/external-systems.md)
* A new custom authentication example has been added in the external datasources section. [Read more](../datasource/external-data-sources.md#custom-authentication-mode)
* A note has been added about Data Collection Core Service (DCCS) for event-triggered journeys. [Read more](../start/guardrails.md#events-g)
* A note on identity namespace retrieval has been added in the [Read audience](../building-journeys/read-audience.md), [Audience qualification](../building-journeys/audience-qualification-events.md) and [Event creation](../event/about-creating.md) sections.
* Accessibility features in [!DNL Journey Optimizer] are now grouped in a dedicated page. [Read more](../start/accessibility.md)
* The examples have been updated in the Operators section of the advanced expression editor documentation. [Read more](../building-journeys/expression/operators.md)
* A note has been added about the limitation on lookup with array of objects. [Read more](../event/experience-event-schema.md#relationships_limitations)
* Added a new page about data management in [!DNL Journey Optimizer]. [Read more](../data/gs-data.md)
* Added a table listing all codes that can be returned in the response when delivering offers using the Decisioning API. [Read more](../offers/api-reference/offer-delivery-api/decisioning-api.md)

+++

+++ 2022

## December 2022 {#december-2022}

* The Messages guide has been reorganized and split into dedicated guides for each channel:

    * [Email channel](../email/get-started-email.md)
    * [Push notification channel](../../rp_landing_pages/push-landing-page.md)
    * [SMS channel](../sms/get-started-sms.md)

* The Configuration guide has been reorganized for improved readability. [Read more](../configuration/get-started-configuration.md)

## November 2022 {#november-2022}

* Added a new page about Journey Optimizer integrations. [Read more](../integrations/ajo-integrations.md)
* Added a recommendation about the length of mirror pages URLs. [Read more](../email/message-tracking.md)
* A new subsection in the email settings configuration has been added on the reply to email address, including recommendations to ensure proper reply management. [Read more](../email/email-settings.md#send-to-suppressed-email-addresses)
* Added a section on how to modify the content of a message in a live journey. [Read more](../building-journeys/journeys-message.md#update-live-content)

## October 2022 {#october-2022}

* Added a journey use case on how to limit throughput using External Data Sources and Custom Actions. [Read more](../building-journeys/limit-throughput.md)
* The journey use case section has been reorganized into two categories: [Business use cases](../building-journeys/journeys-uc.md) and [Technical use cases](../building-journeys/collections.md).
* The **Entity Dataset** section has been updated with more details. [Read more](../data/datasets-query-examples.md#entity-dataset)
* The opt-out management and consent policies sections have been reorganized. [Read more](../privacy/opt-out.md)
* The section on advanced parameters in journey messages has been clarified and now specifies that email address override should only be used for specific use cases. Most of the time, the value defined as the primary address in the **Execution fields** is the one that should be used. 
* Added a note to the **Configure landing page subdomains** section to specify that capital letters are not allowed in landing page subdomains. [Read more](../landing-pages/lp-subdomains.md)

## September 2022 {#september-2022}

* All new features and improvements coming with [!DNL Journey Optimizer] September '22 release have been detailed in the documentation. [Read more](release-notes.md)
* Added a best practice related to the use of wait activities in recurring read audience journeys. [Read more](../building-journeys/read-audience.md#configuring-segment-trigger-activity)
* Added new step event query examples as well as information on the difference between id, instanceid and profileid. [Read more](../reports/query-examples.md).
* Updated the pages related to the [toDateOnly](../building-journeys/functions/conversion-functions.md#toDateOnly) and [toString](../building-journeys/functions/conversion-functions.md#toString) functions.
* Added details on the time condition parameters. [Read more](../building-journeys/condition-activity.md#time_condition)
* Added information on built-in datasets. [Read more](../data/get-started-datasets.md#access-datasets)
* The Global report and Live report sections have been improved and reorganized. [Read more](../reports/report-gs-cja.md)
* A list of every reporting metric available in Adobe Journey Optimizer has been added.
[Read more](../reports/report-gs-cja.md#email-and-sms-metrics)
* The BCC email section has been moved to the new Support for archiving page. [Read more](../configuration/archiving-support.md)

## August 2022 {#august-2022}

* All new features and improvements coming with [!DNL Journey Optimizer] August '22 release have been detailed in the documentation. [Read more](release-notes.md)
* The Frequency rules section has been updated to reflect the new in-line messaging flow.
* A video showing how to configure subscriptions and create landing pages is now referenced in the Get started with landing pages section. [Read more](../landing-pages/get-started-lp.md#video)
* A limitation has been added for journeys using Read Audience activities. [Read more](../building-journeys/read-audience.md)
* The expression editor operators page has been improved. [Read more](../building-journeys/expression/operators.md)
* A section on how to schedule a campaign has been added. [Read more](../campaigns/create-campaign.md)
* General syntax rules section for expression editor has been updated to take into account the new rule regarding the backslash symbol escaping in literal functions. The existing published messages are not impacted by this change. Only the new or draft messages must be updated. [Read more](../personalization/personalization-syntax.md#general-rules)

## July 2022 {#july-2022}

* All new features and improvements coming with [!DNL Journey Optimizer] July '22 release have been detailed in the documentation. [Read more](release-notes.md)
* The **Set up channel configurations** section has been clarified and updated with links to the page describing how to configure the SMS channel. [Read more](../configuration/channel-surfaces.md#create-channel-surface)
* In the journey properties, the **Profile Time zone** option is now disabled by default. [Read more](../building-journeys/timezone-management.md#timezone-from-profiles)
* In the **Wait** activity, the **Fixed date** option is no longer available. [Read more](../building-journeys/wait-activity.md)
* Added more information on the **Incremental read** option in the **Read audience** activity. [Read more](../building-journeys/read-audience.md#configuring-segment-trigger-activity)
* Added recommendations on the **Profile cap** condition type. [Read more](../building-journeys/condition-activity.md#profile_cap)
* Added a limitation on business events. [Read more](../start/guardrails.md#events-g)

## June 2022 {#june-2022}

* All new features and improvements coming with [!DNL Journey Optimizer] June '22 release have been detailed in the documentation. [Read more](release-notes.md)
* A new section about Privacy requests has been added to the documentation. [Read more](../privacy/requests.md)
* A new section about Audit logs on resources has been added to the documentation. [Read more](../privacy/audit-logs.md)
* A new section about how to add HTML or JSON content coming from Adobe Experience Cloud Asset library to an offer representation has been added to the documentation. [Read more](../offers/offer-library/add-representations.md#html-json)
* Added a new page on journey lifecyle. [Read more](../building-journeys/journey.md)
* Updated the Wait activity page. [Read more](../building-journeys/wait-activity.md)
* Added the list of Adobe Journey Optimizer datasets with query examples. [Read more](../data/datasets-query-examples.md)
* The Allowed list page has been moved to the Configuration section. [Read more](../configuration/allow-list.md)
* The Suppression list page has been updated to clarify some information, including the fact that all ASCII characters comprised between 32 and 126 are allowed in the reason for suppression field. [Read more](../configuration/manage-suppression-list.md)
* The link to guardrails and static limits for Decision management has been added. [Read more](../start/guardrails.md)
* Send-Time Optimization is now available for all customers. The beta mention has been removed. [Read more](../building-journeys/send-time-optimization.md)
* The Batch Decisioning API has been added to the list of available APIs to delivery personalized offers. [Read more](../offers/api-reference/offer-delivery-api/start-offer-delivery-apis.md)

## May 2022 {#may-2022}

* All new features and improvements coming with [!DNL Journey Optimizer] May '22 release have been detailed in the documentation. [Read more](release-notes.md)
* New query examples related to [audience qualification](../reports/query-examples.md#segment-qualification-queries) and [events](../reports/query-examples.md#event-based-queries) have been added.
* The email design section now mentions new built-in templates available to start content with. Related screenshots have been updated. [Read more](../email/get-started-email-design.md)
* Links to key resources have been updated in Journey Optimizer documentation home page.
* Screenshots for landing page and subscription reporting have been updated. [Read more](../reports/live-report.md)
* A note has been added stating that the Delete method is not supported in custom actions. [Read more](../action/about-custom-action-configuration.md)
* Links to how-to videos have been updated.
* The [Email configuration](../configuration/about-subdomain-delegation.md), [Message presets](../configuration/channel-surfaces.md) and [Configure landing pages](../landing-pages/lp-subdomains.md) sections have been reorganized for improved readability.
* The URL tracking section has been updated and improved with examples. [Read more](../email/email-settings.md#url-tracking)
* A new subsection on setting up a forward email address has been added. Note that you cannot do it through the user interface. [Read more](../email/email-settings.md#email-settings)

## April 2022 {#april-2022}

* All new features and improvements coming with [!DNL Journey Optimizer] April '22 release have been detailed in the documentation. [Read more](release-notes.md)
* The **reactions** event documentation page has been updated. [Read more](../building-journeys/reaction-events.md)
* Videos for Decision management capabilities have been updated to reflect Journey Optimizer user interface. [Read more](../offers/get-started/starting-offer-decisioning.md)
* The **Get Started with Datasets** section has been improved to detail how to access and create datasets. [Read more](../data/get-started-datasets.md)
* Links to help guides and product release notes have been added to the **Adobe Journey Optimizer Documentation** home page. [Read more](https://experienceleague.adobe.com/docs/journey-optimizer.html)
* The **Create message presets** section now specifies that you cannot proceed with preset creation while the selected IP pool is under edition (**[!UICONTROL Processing]** status) and has never been associated with the selected subdomain. [Read more](../configuration/channel-surfaces.md#subdomains-and-ip-pools)
* The message presets **URL tracking** section has been updated to reflect minor changes in the user interface. [Read more](../configuration/channel-surfaces.md#url-tracking)

## March 2022 {#march-2022}

* All new features and improvements coming with [!DNL Journey Optimizer] March '22 release have been detailed in the documentation. [Read more](release-notes.md)
* A new page on getting started with AI models has been added to the **Offer decisioning** section, including a thorough description of the [auto-optimization model](../offers/ranking/auto-optimization-model.md), the algorithm it uses and more technical details. [Read more](../offers/ranking/ai-models.md)
* The test profile creation page has been moved to the  **Audience, profiles and identity** section. [Read more](../audience/creating-test-profiles.md)
* Added an example on how to add an expression as a default value in the expression editor. [Read more](../building-journeys/expression/field-references.md#default-value)
* The **Create personalized offers** section has been reorganized for improved readability. [Read more](../offers/offer-library/creating-personalized-offers.md)
* A new section has been added to describe the impacts that changing an offer's start and/or end dates may have on this offer's frequency capping. [Read more](../offers/offer-library/add-constraints.md#capping-change-date)
* The **Change the primary email addresses** section has been updated to reflect the user interface changes. [Read more](../configuration/primary-email-addresses.md)

## February 2022 {#feb-2022}

* All new features and improvements coming with [!DNL Journey Optimizer] Feb '22 release have been detailed in the documentation. [Read more](release-notes.md)
* The [replace](../building-journeys/functions/string-functions.md#replace) and [replaceAll](../building-journeys/functions/string-functions.md#replaceAll) function documentation pages have been updated with additional information and examples regarding the target parameter.
* Best practices have been added to the [Operators](../building-journeys/expression/operators.md#important-notes) page.

## January 2022 {#january-2022}

* All new features and improvements coming with [!DNL Journey Optimizer] Jan '22 release have been detailed in the documentation. [Read more](release-notes.md)
* The **Offer decisioning AI rankings** section has been updated with a more detailed description of the auto-optimization model. [Read more](../offers/ranking/auto-optimization-model.md)
* A new section on the schema requirements needed to be able to send in event types when using an AI model has been added. [Read more](../offers/data-collection/schema-requirement.md)
* The section related to [!DNL Journey Optimizer] personalization capabilities has been reorganized for better readability. [Read more](../personalization/personalize.md)
* The **Create message presets** section has been divided into several sections for improved clarity. [Read more](../configuration/channel-surfaces.md#create-channel-surface)
* The **Opt-out management** section has been clarified and slightly reorganized. [Read more](../privacy/opt-out.md#opt-out-decision-management)
* The **Insert links** section has been updated to reflect the recent user interface changes. [Read more](../email/message-tracking.md#insert-links)

+++

+++ 2021

## November 2021 {#november-2021}

* A full description of the **advanced expression editor** used in journeys is now available. [Read more](../building-journeys/expression/expressionadvanced.md)
* A new section about **CNAME subdomain delegation method** has been added. [Read more](../configuration/delegate-subdomain.md#cname-subdomain-setup)

## October 2021 {#october-2021}

* All new features and improvements coming with [!DNL Journey Optimizer] Oct '21 release have been detailed in the documentation. [Read more](release-notes.md)
* Added **Date time function** list. [Read more](../personalization/functions/dates.md)
* New **Get Started sections per user persona**. Take your own path to get to your goals faster! [Read more](../start/quick-start.md)
* New **Edit a message preset** section. [Read more](../configuration/channel-surfaces.md#edit-channel-surface)
* New **Edit a PTR record** section. [Read more](../configuration/ptr-records.md#edit-ptr-record)
* New **Deactivate a message preset** section. [Read more](../configuration/channel-surfaces.md#edit-channel-surface)
* New limitations added to the **Decision Management API developer guide** on offer constraints not supported with the mobile [!DNL Experience Edge] workflows. [Read more](../offers/api-reference/offers-api/personalized-offers/create.md#limitations)
* New **Create simulations** section. [Read more](../offers/offer-activities/simulation.md)
* Updated **Add decision scopes** section. [Read more](../offers/offer-activities/create-offer-activities.md#add-decision-scopes)
* Updated **Define content for your representations** section, including a new [subsection](../offers/offer-library/creating-personalized-offers.md#custom-text) on how to define and personalize custom text. [Read more](../offers/offer-library/creating-personalized-offers.md#content)

## September 2021 {#september-2021}

* The following function pages have been updated: [sethours](../building-journeys/functions/date-functions.md#setHours), [getListItem](../building-journeys/functions/list-functions.md#getListItem), [inSegment](../building-journeys/functions/functioninaudience.md)

* The following functions have been added: [filter](../building-journeys/functions/list-functions.md#filter), [intersect](../building-journeys/functions/list-functions.md#intersect), [toDateOnly](../building-journeys/functions/conversion-functions.md#toDateOnly)

* The dateOnly date type has been added in the expression editor documentation. [Read more](../building-journeys/expression/data-types.md)

* Added details on custom action cache duration. [Read more](../datasource/external-data-sources.md#custom-authentication-mode)

* Added information on custom action default ports. [Read more](../action/about-custom-action-configuration.md#url-configuration)

* Added information on multiple business event use cases. [Read more](../event/about-creating-business.md#multiple-business-events)

* Added commonly used examples to query Journey Step Events in Data Lake. [Read more](../reports/query-examples.md)

* Added a new **Limitations** page. [Read more](../start/guardrails.md)

* Improved the **Quick start** page with steps for different personas. [Read more](../start/quick-start.md)

* Now all the Decision management features described in the dedicated section also apply to the Adobe Experience Platform users leveraging the Offer Decisioning application. [Read more](../offers/get-started/starting-offer-decisioning.md)

* Added a subsection to clarify the differences between using audiences versus decision rules when applying a constraint to restrict the selection of offers for a given placement. [Read more](../offers/offer-activities/create-offer-activities.md#decision-list)

* Added specific ranking formula examples to illustrate some real-life use cases. [Read more](../offers/ranking/create-ranking-formulas.md#ranking-formula-examples)

* Added a subsection on how to edit IP pools. [Read more](../configuration/ip-pools.md#edit-ip-pool)

## August 2021 {#august-2021}

* All new features and improvements coming with [!DNL Journey Optimizer] August '21 release have been detailed in the documentation. [Read more](release-notes.md)
* Updated Decision management permissions. [Read more](../administration/ootb-product-profiles.md)
* Updated Email Designer screenshots with latest UI.
* Updated the configuration procedure for custom actions with dynamic URL paths and dynamic headers. [Read more](../action/about-custom-action-configuration.md#url-configuration)
* Added a section about accessibility features and shortcuts. [Read more](../start/user-interface.md#accessibility)
* Added a section about audience evaluation methods. [Read more](../audience/about-audiences.md#evaluation-method-in-journey-optimizer)
* Added notes to the Suppression list, Allowed list and Email global/live report sections to specify that profiles with Suppressed and Not allowed statuses are excluded from the Email report Sent metrics. [Read more](../reports/report-gs-cja.md)
* Added a new section to describe how to retrieve email addresses or domains that were excluded from a sending because they were not on the allowed list. [Read more](../configuration/allow-list.md#reporting)
* Updated the Enable the allow list section. [Learn more](../configuration/allow-list.md#enable-allow-list)
* Updated the Monitor message presets section with the possible preset creation failure reasons and details on such errors. [Read more](../configuration/channel-surfaces.md#monitor-channel-surfaces)
* Updated and renamed the Retry time period section to reflect the fact that you can now adjust the email retry setting in the message presets. [Read more](../configuration/retries.md#retry-duration)
* Updated the Delegate a subdomain section with more detailed information on the validation process performed by Adobe. [Read more](../configuration/delegate-subdomain.md#subdomain-validation)
* Added a section to describe how to manually add email addresses and domains to the suppression list. [Read more](../configuration/manage-suppression-list.md#add-addresses-and-domains)
* Updated the [Access the suppression list](../configuration/manage-suppression-list.md#access-suppression-list) section and [Retries](../configuration/retries.md) sections to reflect the new user interface.
* The new flow to add and configure representations when creating an offer has been documented. [Read more](../offers/offer-library/creating-personalized-offers.md#representations)

## July 2021 {#july-2021}

* All new features and improvements coming with [!DNL Journey Optimizer] July '21 release have been detailed in the documentation. [Read more](release-notes.md)
* Added direct links to Experience Platform services documentation in [!DNL Journey Optimizer] home page and table of contents
* New landing pages for Experience Platform services available in [!DNL Journey Optimizer] 
* Added links to [!DNL Journey Optimizer] product description in the home page
* Added tutorial videos in multiple pages
* Optimized home page imagery
* Moved, improved and renamed 'Message tracking' section to 'Add links and track messages'. [Read more](../email/message-tracking.md)
* Added a subsection on mirror pages. [Read more](../email/message-tracking.md#mirror-page)
* Renamed 'offer activities' as 'decisions' and 'decisions' as 'decision scopes' in documentation and screens. [Read more](../offers/get-started/starting-offer-decisioning.md)
* New use case: [personalize a message with helper functions](../personalization/personalization-use-case-helper-functions.md)
* Updated the Read audience documentation to reflect materialized segment impacts. [Read more](../building-journeys/read-audience.md)
* Updated the Journey limitations. [Read more](../start/guardrails.md)
* Updated the Configure offers selection in decisions section. [Read more](../offers/offer-activities/configure-offer-selection.md)
* Added a warning to mention that event-based offers are not currently supported. [Read more](../offers/offer-library/creating-personalized-offers.md#eligibility)
* Documented the Decision management new **[!UICONTROL Overview]** tab. [Read more](../offers/get-started/user-interface.md#overview)
* Added new sections to describe the actions available from the offer and decision lists: [Offer list](../offers/offer-library/creating-personalized-offers.md#offer-list) and [Decision list](../offers/offer-activities/create-offer-activities.md#decision-list).

+++
-->
