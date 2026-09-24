---
solution: Journey Optimizer
product: journey optimizer
title: 文档更新
description: 了解 Adobe Journey Optimizer 的最新文档更新，包括新页面、重组和说明。
keywords: 文档更新、发行说明、journey optimizer、更改日志
feature: Release Notes
topic: Content Management
role: User
level: Beginner, Intermediate
exl-id: 83c8f206-bce3-4cc8-94a3-575ec1d999bc
feature_v2:
  - id: bb359667-ec7d-4d4b-8663-5850fc219d32
    internal-label: Administration
subfeature_v2:
  - id: a7b2bfc5-be71-4740-b371-76fa6be8df02
    internal-label: Journey Optimizer release notes
source-git-commit: d11d44f6d1237f9435c8c811023869e795222045
workflow-type: tm+mt
source-wordcount: '7221'
ht-degree: 81%
---

# 文档更新 {#latest-updates}

此页面列出了 [!DNL Journey Optimizer] 文档中的所有最新更改，以及每月发布的功能和改进的相关更新。

## 2026年9月 {#september-2026}

* `inAudience`护栏现在包含具有5,000个以上受众的沙盒的解决方法，在历程创作期间，可以拒绝较旧的受众，因为验证仅检查5,000个最近更新的受众。 [了解更多](../building-journeys/functions/functioninaudience.md#guardrails)

* 扩展了电子邮件镜像页面的指南：文档现在说明了无法通过公共API或数据集检索镜像页面URL，建议使用消息导出或密送归档来保留已发送的内容，并阐明镜像页面链接在验证和模拟中处于非活动状态。 [了解更多](../email/message-tracking.md#mirror-page)

* 新的&#x200B;**交互式演示**&#x200B;页面现在可用于忠诚度挑战，该页面链接到可单击的自引导演示，该演示涵盖营销人员的挑战创建流程（包括自带数据和见解仪表板）、最终客户体验以及CX Coworker中的忠诚度挑战管理。 [了解更多](../loyalty-challenges/loyalty-challenges-demo.md)

* **个性化您的电子邮件背景**&#x200B;页面已扩展和改进。 它现在记录了背景图像的完整&#x200B;**图像投放位置**&#x200B;下拉列表，并添加了背景颜色和图像的新最佳实践，包括跨实际的电子邮件客户端测试背景图像的建议，而不是仅依赖电子邮件Designer预览。 [了解更多](../email/backgrounds.md)

* 重新组织并阐明了&#x200B;**使用电子邮件Designer**&#x200B;页面从头开始的设计内容：它将&#x200B;**[!UICONTROL n:n列]**&#x200B;结构与固定预设结构区分开来，提供了可以增加结构的列数而不会丢失现有内容的文档，解释了移动设备上的列栈叠行为，并添加了使用&#x200B;**[!UICONTROL 模块]**&#x200B;快速启动电子邮件创建的新步骤。 [了解更多](../email/content-from-scratch.md)

* **设计您的历程**&#x200B;页面现在包含有关新画布体验的完整教程部分，其中包括如何添加活动、使用工具栏图标、选择多个活动以进行批量操作、复制和粘贴活动以及加入或分离分支。 [了解更多](../building-journeys/using-the-journey-designer.md#canvas-capabilities)

* 新增了验证自定义操作交付的指南：**数据集查询示例**&#x200B;页面现在说明了如何根据操作类型在邮件反馈事件、电子邮件跟踪和历程步骤事件数据集之间进行选择，并说明了如何解决“未为数据集设置表”错误。 **历程步骤事件概述**&#x200B;和&#x200B;**实时历程执行疑难解答**&#x200B;页面已相应地更新，明确指出成功的自定义操作调用仅确认Journey Optimizer执行了操作，而不是外部系统传递了消息。 [了解更多](../data/datasets-query-examples.md#choose-the-correct-dataset)

* 有关CX Coworker的信息已添加到&#x200B;**使用AI**&#x200B;页面，涵盖了CX Coworker是什么、它与AI助手的关系以及对正式同事文档的引用。 每个功能指南中也添加了专门的技能页面 — [历程的CX Coworker技能](../building-journeys/journeys-coworker-skills.md)、[忠诚度的CX Coworker技能](../loyalty-challenges/loyalty-coworker-skills.md)和[CX Coworker内容管理工具](../content-management/content-management-coworker-skills.md)。 [了解更多](../start/ai-features.md#cx-coworker)

* 已在CX Coworker页面的&#x200B;**历程分析**&#x200B;下记录了一种新的&#x200B;**分析历程异常**&#x200B;技能。 它会检测历程的进入、退出或发送计数中相对于历史基线的意外尖峰、下降或扁平化，并运行只读诊断来找出可能的根本原因。 [了解更多](../building-journeys/journeys-coworker-skills.md#journey-analyze)

* 已更新&#x200B;**护栏和限制**&#x200B;和&#x200B;**历程属性**&#x200B;页，以将默认历程有效负载限制记录为&#x200B;**2 MB （2,000,000字节）**，阐明该值反映序列化的历程定义，而不是仅活动计数，并解释90%警告和100%阻止阈值。 [了解更多](../start/guardrails.md#journey-payload-size)和[了解更多](../building-journeys/journey-properties.md#journey-payload-size)

* **护栏和限制**&#x200B;页面已更正，以反映超过100 KB的可视化片段或超过200 KB的表达式片段不再会导致电子邮件投放中出现截断问题：现在单个700 KB片段大小护栏适用。 [了解更多](../start/guardrails.md#fragments-guardrails)

* **创建实时活动**&#x200B;页面已更正：`executionMetadata`字段仅适用于&#x200B;**API触发的事务性**&#x200B;营销活动，而不适用于之前所述的API触发的营销活动。 [了解更多](../mobile-live/create-mobile-live.md#metadata)

* **AJO消息反馈事件数据集**&#x200B;文档已扩展，明确说明该数据集涵盖所有渠道（电子邮件、SMS/RCS/MMS、直邮）的消息投放反馈，而不只是电子邮件和推送，现在包含&#x200B;**对测试和非测试执行进行分类**&#x200B;部分，说明如何解释`isTestExecution`字段，包括`NULL`或缺失的值。 [了解更多](../data/datasets-query-examples.md#classify-test-executions)

* 已为CX Coworker记录新的&#x200B;**内容管理**&#x200B;功能，该功能由15个读/写MCP工具提供支持，允许您使用自然语言提示发现、创建、更新、克隆和发布内容模板、片段、登陆页以及历程/营销活动内联消息内容。 [了解更多](../content-management/content-management-coworker-skills.md#content-management)

* **将内容添加到登陆页面**&#x200B;文档现在描述了同意复选框的&#x200B;**将表单字段设为必填**&#x200B;选项：启用时，除非选中该复选框，并且同时在客户端和服务器端强制实施该检查，否则无法提交表单。 [了解更多](../landing-pages/lp-content.md#use-form-component)

* 已更新&#x200B;**历程模拟入门**&#x200B;页面，以记录模拟现在支持Content Decision节点和&#x200B;**Optimize**&#x200B;活动的定位规则方法（以前列为阻止），新增了&#x200B;**决策行为**&#x200B;表，详细说明了模拟运行期间如何评估优惠资格、资格规则和受众以及排名方法。 [了解更多](../building-journeys/simulate-journey-gs.md#limitations)

* 已更正&#x200B;**将图像转换为电子邮件内容模板**&#x200B;页面，删除不准确的权限要求：访问和创建包含图像到HTML转换器的模板不需要&#x200B;**管理内容模板**&#x200B;权限 — 只需要&#x200B;**生成内容**&#x200B;权限。 [了解更多](../content-management/image-to-html.md#access-image-to-html)

* 已更正&#x200B;**外部系统（自定义操作）**&#x200B;页面：现在，当120秒窗口内超过20%的调用超过&#x200B;**5秒**（以前记录为10秒）时，将激活适用于慢速自定义操作端点的断路器。 [了解更多](../configuration/external-systems.md#response-time)

* **配置渠道配置**&#x200B;页面现在包含一条注释，其中澄清用于辅助维度的架构必须具有主键，并且不支持复合主键。 [了解更多](../orchestrated/channel-config.md)

* **忠诚度数据和数据集**&#x200B;和&#x200B;**来源入门**&#x200B;页面已更新，将LAVA作为受支持的忠诚度和奖励连接器与Talon.One、Chariceline和Kobie一起包含在内。 [了解更多](../loyalty-challenges/loyalty-data-and-datasets.md)

## 2026 年 8 月 {#august-2026}

* **向电子邮件添加可视化片段**&#x200B;页面现在阐明了“电子邮件Designer”中默认状态为空且包含动态内容的片段显示为空 — 使用匹配的配置文件模拟以预览内容。 [了解更多](../email/use-visual-fragments.md#fragment-dynamic-content)

* **跟踪您的消息**&#x200B;页面已更新，以阐明不支持的URL字符（例如撇号）必须采用百分比编码，未编码这些URL字符可能会破坏跟踪链接和URL跟踪参数。 [了解更多](../email/message-tracking.md#insert-links)

* 已更新&#x200B;**使用批次**&#x200B;发送，以记录读取受众历程中的最后一个批次必须安排在历程开始的&#x200B;**6天和18小时**&#x200B;内。 超过此窗口会触发验证错误，并阻止历程进入测试模式或进入实时状态。 [了解更多](../delivery/send-using-waves.md#limitations-guardrails)

* 新的&#x200B;**禁止反馈事件**&#x200B;部分已添加到&#x200B;**决策管理数据收集**&#x200B;页面，该部分记录了如何在测试期间使用`dryRun`标志禁止决策事件以及防止为报告和频率上限计数器捕获反馈。 [了解更多](../offers/data-collection/data-collection.md#suppress-feedback)

* 新&#x200B;**选择验证方法**&#x200B;页面现已可用。 它会比较历程模拟、测试模式和历程练习，即每次使用的数据、是否发送真正的消息、要避免的常见错误以及在构建旅程的每个阶段选择正确方法的决策指南。 [了解更多](../building-journeys/choose-validation-method.md)

* **护栏和限制**&#x200B;页面已更新，以明确受众资格活动和事件护栏：措辞现在一致地引用受众资格&#x200B;**活动**（而不是节点），包括在用作退出条件时，并且两个护栏现在都明确涵盖&#x200B;**实时、关闭、暂停、测试模式和试运行**&#x200B;历程。 [了解更多](../start/guardrails.md#audience-qualif-g)

* 已向&#x200B;**测试HTML大小优化**&#x200B;部分添加注释，以阐明校样大小反映的是HTML模板大小（具有最小值的Handlebars），而不是最终投放的电子邮件大小，在投放时解析动态表达式后，最终投放的电子邮件大小可能会更大。 [了解更多](../email/create-email.md#optimize-html-proof)

* 已在&#x200B;**电子邮件设计入门**&#x200B;页面中新增了&#x200B;**移动Web浏览器限制**&#x200B;部分，记录了在通过移动浏览器访问时，电子邮件在Gmail或Outlook中呈现不同形式的原因，并提供解决方法提示。 [了解更多](../email/get-started-email-design.md#mobile-web-limitations)

* 新的 **Outlook 渲染注意事项**&#x200B;部分已添加到&#x200B;**电子邮件设计快速入门**&#x200B;页面，其中列出了设计中需要考虑的常见 Outlook 问题：内边距和宽度使用偶数、表宽度以像素为单位、HTML 图像宽度属性、备选文本、表单元格边框和圆角。 [了解更多](../email/get-started-email-design.md#outlook-tips)

* **数据集生存时间 (TTL) 护栏**&#x200B;页面已更新，其中&#x200B;**受影响的数据集**&#x200B;表已大幅扩展，现在该表涵盖了所有 Journey Optimizer 系统生成的数据集（包括以前未列出的多个数据集，如 AJO 同意服务、交互式消息配置文件、推送配置文件和消息导出数据集），以及新的&#x200B;**可用性**&#x200B;列，该列指示每个数据集是默认包含，还是需要特定的附加组件或许可证。 **护栏和限制**&#x200B;页面也已更新，以反映此护栏的确认强制实施日期：将从&#x200B;**2026年10月1日**&#x200B;开始，在&#x200B;**现有客户沙盒**&#x200B;上强制实施更改。 [了解更多](../data/datasets-ttl.md#datasets)

* 新的&#x200B;**使用图像设置模式**&#x200B;部分已添加到生成内容文档。 该部分说明了&#x200B;**[!UICONTROL 图像设置]**&#x200B;下可用的&#x200B;**平衡**、**DAM** 和&#x200B;**创意**&#x200B;模式，这些模式控制 AI 生成内容的图像来源：是从您的数字资产管理库中获取，由 AI 生成，还是二者混合使用。 [了解更多](../content-management/generative-uc.md#image-mode)

* **左侧导航>主要部分**&#x200B;下的&#x200B;**目标**&#x200B;描述已更新，请注意，具有[!DNL Real-Time CDP]或[!DNL Adobe Journey Optimizer]的组织还可以从Experience Platform目标目录中将受众激活到符合条件的个性化目标，如[!DNL Adobe Target]。 [了解更多](../start/user-interface.md#main-sections)

* 在“忠诚度挑战”文档中添加了操作方法视频，介绍如何创建挑战、设置奖励提供商和监控挑战表现。 [观看挑战视频](../loyalty-challenges/create-challenges.md#video)、[观看奖励提供商视频](../loyalty-challenges/reward-definition-guide.md#video)和[观看报告视频](../loyalty-challenges/loyalty-reporting.md#video)。

## 2026 年 7 月 {#july-2026}

* 新的&#x200B;**投放设置**&#x200B;部分已添加到文档导航中。 它将适用于历程、营销活动和编排营销活动的与投放相关的功能分组：**使用批次发送**、**发送时间优化**&#x200B;和&#x200B;**渠道优化**&#x200B;已从历程部分移至该处。

* 历程和操作营销活动的单独&#x200B;**使用批次**&#x200B;发送文档页面已合并到单个页面中，现在还涵盖编排的营销活动。 [了解更多](../delivery/send-using-waves.md)

* **设计您的历程**&#x200B;页面中添加了一个提示，其中指向有关&#x200B;**如何分离和重新加入新历程画布中的节点**&#x200B;的Experience League社区文章。 [了解更多](../building-journeys/using-the-journey-designer.md)

* **网格**&#x200B;组件部分已添加到&#x200B;**使用电子邮件Designer内容组件**&#x200B;页面。 使用网格组件，您可以将内容组织到由行和列构成的结构化网格中，其中每个单元格可以包含其他内容组件。 [了解更多](../email/content-components.md#grid)

* **Decisioning迁移API**&#x200B;文档已更新，其中明确了目标沙盒&#x200B;**可以与源沙盒**&#x200B;相同。 迁移过程可处理此方案并确保数据完整性，无论对象是迁移至同一沙盒还是另一个沙盒。 [了解更多](../experience-decisioning/decisioning-migration-api.md#target-sandbox-preparation)

* **Decisioning迁移API**&#x200B;文档已得到增强，现在提供了有关将决策管理对象迁移到Decisioning的全面指南。 新部分包括：具有10种命名约定的实体映射引用、范围内与范围外覆盖率、详细的请求/响应模型比较、具有Cookie处理的三种实施模式（客户端、服务器端、混合）、包含5个事件JSON示例的事件跟踪要求、跨沙盒迁移先决条件、端到端5步迁移流程和迁移常见问题解答。 [了解更多](../experience-decisioning/decisioning-migration-api.md)

* 现已提供新的&#x200B;**CX 同事技能**&#x200B;页面。 它提供了 Journey Optimizer 中所有可用历程技能（包括历程创建、渠道内容创建、忠诚度挑战管理和历程分析）的综合文档，以及每种技能的用例、示例提示和最佳实践。 [了解更多](../start/ai-features.md#cx-coworker)

* **To Precision**&#x200B;函数文档已更新，以阐明`toPrecision`的行为类似于 JavaScript`toFixed()`：它返回一个字符串，该字符串具有固定数量的小数，包括在需要时使用零填充。 [了解更多](../personalization/functions/math.md#to-precision)

* **结束历程**&#x200B;页面已更新，以明确非周期性读取受众历程的自动停止时间：在计划运行（24 小时空闲窗口 + 72 小时静默时段宽限）后约 **96 小时（约 4 天）**&#x200B;的安全缓冲期，在此期间历程可以保持&#x200B;**运行中**&#x200B;状态，然后在缓冲期结束后不久转为&#x200B;**已停止**&#x200B;状态。 页面现在还阐明，基于波次（多波次）的历程和使用发送时间优化的历程将从此自动停止中排除，而是遵循标准的91天历程超时。 [了解更多](../building-journeys/end-journey.md#auto-stop-non-recurring)

* **创建IP预热活动**&#x200B;页面已更新，以阐明可以将定位规则应用于 IP 预热活动，并记录评估行为：受众成员资格在运行时激活（每日批处理分段）时是固定的，而配置文件属性在运行时从最近摄取的批处理数据读取。 [了解更多](../configuration/ip-warmup-campaign.md)

* 在&#x200B;**编辑 PTR记录**&#x200B;页面中添加了一个警告，以通知客户在将新的转发DNS记录添加到其平台时，必须等到移动完成之后才能删除旧子域的转发DNS记录，因为这样做会导致编辑失败。 [了解更多](../configuration/ptr-records.md#edit-ptr-subdomains-cname)

* 已更新&#x200B;**使用批次发送**&#x200B;页面，以阐明跨批次的受众重新评估行为：受众成员资格在激活时是固定的（快照），但在每个批次处理时都会评估配置文件属性和同意。 这意味着系统会遵循批次之间发生的选择退出。 在[常见问题部分](../delivery/send-using-waves.md#faq)中了解更多。

* **数据治理**&#x200B;页面已更新，以阐明 DULE 策略实施仅适用于&#x200B;**配置文件属性字段**。 不支持基于事件的字段（历程事件字段等上下文属性）：应用于 UI 中这些字段的标签将不会限制数据使用。 [了解更多](../action/action-privacy.md)

* **发送时间优化**&#x200B;文档已更新，以反映&#x200B;**[!UICONTROL 在接下来的时间内发送]**&#x200B;的新限制为 **2-100 小时**（以前为 1-168），并记录此功能支持的 AEP 中心区域。 [了解更多](../building-journeys/send-time-optimization.md#use-send-time-optimization)


* 更新了&#x200B;**个性化优化模型**&#x200B;页面，以反映最新的模型改进，包括集成模型的工作方式、数据集要求、用例、关键假设和冷启动行为。 有关更多信息，请参阅 [体验决策](../experience-decisioning/ranking/personalized-optimization-model.md) 和 [产品建议决策](../offers/ranking/personalized-optimization-model.md) 部分。

* 已在&#x200B;**历程仲裁排名公式**&#x200B;页面中添加一条注释，说明排名公式仅适用于已购买 **Decisioning** 附加产品的组织。 [了解更多](../conflict-prioritization/journey-ranking-formulas.md)

* 现已提供新的&#x200B;**动态片段**&#x200B;页面。 它记录了如何在 [!DNL Journey Optimizer] 中使用动态片段解析，根据轮廓属性、数据集查找或在发送时传递的上下文数据，在运行时选择将哪个已发布的片段注入消息中。 [了解更多](../content-management/dynamic-fragments.md)

## 2026 年 6 月 {#june-2026}

* **检查并发送直邮邮件**&#x200B;页面已更新，以阐明直邮导出时间和批处理行为，包括固定的 4 小时 UTC 导出计划，为何在历程中执行&#x200B;**[!UICONTROL 更新轮廓]**&#x200B;时一天可以生成多个文件，以及针对每天一个文件的情形的建议。 [了解更多](../direct-mail/test-send-direct-mail.md#dm-export-timing)

* 现已提供新的&#x200B;**历程类型：选择正确的类型**&#x200B;页面。 它将所有历程入口点（读取受众、受众资格、单一事件和业务事件）与决策指南和功能兼容性矩阵进行比较，以帮助您为用例选择正确的类型。 [了解更多](../building-journeys/journey-types-selection.md)

* 现已提供新的&#x200B;**历程与营销活动**&#x200B;页面。 它从执行方式、数据模型和用例等方面比较了历程、操作营销活动和 API 触发的营销活动，包括用于低延迟边缘个性化的入站渠道激活、多界面入站投放，以及关于何时使用编排的营销活动（临时受众构成、联合数据）的指导。 [了解更多](../start/journeys-vs-campaigns.md)

* **高吞吐量模式**&#x200B;页面已更新，以反映已扩展的区域可用性：该功能现已在所有区域提供（瑞士除外），适用于拥有高吞吐量事务性消息附加产品许可证的组织。 [了解更多](../campaigns/api-triggered-high-throughput.md)

* 新的&#x200B;**可参与互动的轮廓和许可证使用情况**&#x200B;部分已添加到&#x200B;**轮廓快速入门**&#x200B;页面，作为此概念的单一可信来源，并在“受众”、“营销活动”和“决策”部分添加了相应的引用内容。 [了解更多](../audience/get-started-profiles.md#engageable-profiles)

* 已更新&#x200B;**拆分**&#x200B;活动文档，以记录每个子集设置中可用的&#x200B;**[!UICONTROL 区段代码]**&#x200B;字段，该字段允许您为每个受众区段分配唯一标识符以进行跟踪和报告。 [了解更多](../orchestrated/activities/split.md)

* **配置目标维度**&#x200B;页面已更新，以记录编排的营销活动中可用的两种目标维度类型：内置的&#x200B;**轮廓定向温度**（无需配置）和基于关系架构的&#x200B;**自定义目标维度**。 [了解更多](../orchestrated/target-dimension.md)

* **在片段中利用主题**&#x200B;文档已明确说明：主题的兼容性限制（包括 Adobe 默认主题约束）为 5 个，并且当电子邮件主题不是片段关联主题之一时，将阻止插入片段。 [了解更多](../email/apply-email-themes.md#leverage-themes-fragment)

* **数据集快速入门**&#x200B;和&#x200B;**架构快速入门**&#x200B;页面已更新，其中包含有关为实时客户轮廓启用数据集和架构的指导，包括关键注意事项、禁用数据集与其底层架构之间的区别，以及指向 Adobe Experience Platform 规划和最佳做法文档的链接。 [详细了解数据集](../data/get-started-datasets.md)和[详细了解架构](../data/get-started-schemas.md)

* 现已推出新的 **Adobe Journey Optimizer 快速入门**&#x200B;引导中心。 新用户可以按角色选择路径、探索基础知识，或（如果已完成入门）直接跳转至日常操作区域，无需事先了解该从何处入手。 [了解更多](../../rp_landing_pages/get-started-landing-page.md)

* 通过新的&#x200B;**从您的目标开始**&#x200B;页面，您可以从希望完成的任务入手，而不是从功能名称开始。 它将业务目标映射到设置、历程、营销活动、个性化、决策和报告方面的推荐 [!DNL Journey Optimizer] 功能。 [了解更多](../start/ajo-use-case-guide.md)

* **开发人员入门**&#x200B;角色指南已更新，每个部分都有更清晰的介绍，并改进了&#x200B;**跨角色协作**&#x200B;选项卡，这些选项卡引用历程并链接到关键实施页面。 [了解更多](../start/path/developer.md)

* 新的&#x200B;**历程重入时的路径分配**&#x200B;小节已添加到&#x200B;**路径试验**&#x200B;文档中。 它已明确说明：同一历程版本内，一个轮廓多次进入时的路径分配是持久的，但仅限于该版本内。 发布新历程版本时，分配会重置，并且历程中的每个路径试验活动都会应用独立的随机分配。 [了解更多](../building-journeys/path-experimentation.md#path-assignment)
* 在 [!DNL Journey Optimizer] 文档中，对 **Adobe Experience Cloud** 的引用已与 **[!DNL Adobe CX Enterprise]** 品牌保持一致。

* **`nowWithDelta()`日期函数**&#x200B;文档已更新，以阐明月末行为：当目标月份的天数少于当前日期时，结果将规范化为该月份的最后一个有效日期。 [了解更多](../building-journeys/functions/date-functions.md#nowWithDelta)

* **可投放性入门**&#x200B;页面已更新，新增了一个&#x200B;**无按收件人反馈循环的提供商**&#x200B;小节。 它列出了那些不返回按收件人垃圾邮件投诉的主要邮箱提供商 — Gmail / Google Workspace、Apple iCloud 以及企业版 Microsoft 365 / Exchange Online — 并解释了为什么使用这些服务的收件人不会在禁止列表中出现相应的条目。 [了解更多信息](../reports/deliverability.md#providers-no-fbl)

* **体验决策现在可用于直邮渠道。** 直邮中的新&#x200B;**批量决策**&#x200B;页面介绍了如何使用决策引擎来个性化直邮提取文件，或导出配置文件及其决策结果以供下游系统使用。 **直邮**&#x200B;已添加为决策文档中的受支持渠道（开始使用、创建决策策略、在消息中使用决策策略、决策策略入门），包括通过&#x200B;**[!UICONTROL 项目数]**&#x200B;字段为每个配置文件返回多个决策项目的功能。 [了解更多信息](../experience-decisioning/batch-decisioning-direct-mail.md)

* **历程片段**&#x200B;文档不再标记为有限可用。 此页面现在包含一条注释，用以区分历程片段与内容&#x200B;**[!UICONTROL 片段]**&#x200B;和&#x200B;**AEM 内容片段**（从所有三个页面交叉链接），并记录了有关&#x200B;**沙盒工具**、**审核日志**&#x200B;和&#x200B;**标记**&#x200B;的支持内容。 历程片段也已添加到&#x200B;**历程入门**&#x200B;页面。 [了解更多信息](../building-journeys/journey-fragments.md)

* 已更新自定义身份验证的&#x200B;**外部数据源**&#x200B;和&#x200B;**自定义操作**&#x200B;文档。 `tokenInResponse` 字段现在允许您指定当端点返回两者时，`access_token` 或 `id_token` 是否用作身份验证凭据。 对于基于证书的自定义身份验证，`subType` 和 `aud` 字段现在为必填字段，令牌端点 `method` 必须为 `POST`，并且对“Azure Entra ID”的引用已更正为“Microsoft Entra ID”。 [了解更多信息](../datasource/external-data-sources.md#certificate-credential)

* **决策入门**&#x200B;页面已更新，新增了一个流程图，总结了从管理决策项和配置选择策略，到将决策策略嵌入历程或营销活动的端到端决策工作流。 [了解更多信息](../experience-decisioning/gs-experience-decisioning.md#process)

* **发件人标头**&#x200B;文档现在阐明了&#x200B;**[!UICONTROL 发件人姓名]**&#x200B;和&#x200B;**[!UICONTROL 发件人电子邮件]**&#x200B;必须同时设置或同时留空，否则历程和营销活动将无法发布。 [了解更多信息](../email/header-parameters.md#sender-header)

## 2026 年 5 月 {#may-2026}

* 在可视化片段中使用动态内容时的限制和最佳做法已合并到单个&#x200B;**管理片段中的条件内容**&#x200B;部分，以提高可读性。 [了解更多](../email/use-visual-fragments.md#fragment-dynamic-content)

* 已添加两个新的高级权限：**管理密钥注册表**&#x200B;和&#x200B;**查看密钥注册表**，前者允许用户查看、创建、轮换和撤销密钥注册表中的密钥，后者允许用户查看密钥注册表列表和密钥详细信息。 [了解更多信息](../administration/high-low-permissions.md#administration-permissions)

* **在消息中使用决策策略**&#x200B;文档现在描述了如何从营销活动摘要中查看决策策略的完整结构，以及如何将 JSON 技术摘要复制到剪贴板以进行故障排除。 [了解更多信息](../experience-decisioning/use-decision-policy.md#decision-policy-summary)

* 旧版&#x200B;**决策管理**[自动优化模型](../offers/ranking/auto-optimization-model.md)页面已重写以与更新的 Decisioning 文档保持一致，包括增强学习概述、要求和限制、优化与学习的平衡以及汤普森采样详细信息。 [了解更多信息](../offers/ranking/auto-optimization-model.md)

* **发行说明**&#x200B;页面已重新构建，布局基于主题。 更改现在按产品区域分组，而不是按更改类型分组，并新增了专用&#x200B;**可用性改进**&#x200B;部分。 即将推出的条目在每个主题内显示为可扩展的折叠面板。 [了解更多](release-notes.md)

* **精心策划的营销活动护栏和限制**&#x200B;页面现在记录了每个精心策划的营销活动的&#x200B;**渠道活动**&#x200B;限制。 [了解更多](../orchestrated/guardrails.md#activities-limitations)

* **在沙盒之间复制 Journey Optimizer 对象**&#x200B;文档现已包含有关&#x200B;**精心策划的营销活动**&#x200B;的重要说明：导入后，请在目标沙盒中复制该营销活动并使用副本执行，以确保报告正确捕获反馈和跟踪数据。 [了解更多信息](../configuration/copy-objects-to-sandbox.md#copy-to-sandbox)

* **关键术语**&#x200B;页面已全面修订：添加了六个新术语，引入了新的&#x200B;**冲突和优先级术语**&#x200B;部分，并添加了新的&#x200B;**当术语相似时**&#x200B;消除歧义指南，用于区分四组常被混淆的术语对。 已删除 Adobe Experience Platform 特定术语，并替换为链接到 Adobe Experience Platform 术语表的注释。 [了解更多信息](../start/terminology.md)

* **深度链接**&#x200B;文档已扩展，新增了&#x200B;**创作深度链接**&#x200B;部分，其中详细说明了可用于电子邮件的两个选项（电子邮件设计器 UI 和个性化编辑器代码）以及短信的 URL 函数语法。 **创建短信消息**&#x200B;页面现已在内容创作流程中包含深度链接步骤。 [了解更多](../email/deeplinks.md)

* **URL** 辅助函数引用已在个性化文档中使用专用部分进行了更新。 [了解更多信息](../personalization/functions/helpers.md#url)

* **执行元数据**&#x200B;辅助函数文档添加了限制：入站渠道（Web、基于代码的体验、应用程序内消息、内容卡）不支持该函数。 [了解更多](../personalization/functions/helpers.md#execution-metadata)

* 新增&#x200B;**个性化方法**&#x200B;页面，为 [!DNL Journey Optimizer] 中的最常见用例提供即用型个性化模式。 它涵盖日期和时间方法（当前日期格式、到期倒计时、计算前的天数、仅限时间的显示、周末与工作日检测）、字符串方法（将`replaceAll`用于变量分配）以及条件回退方法（使用`isEmpty`的空字段回退）。 [了解详情](../personalization/personalization-recipes.md)

* **个性化语法**&#x200B;文档已更新，该文档扩展了简介，阐明 Handlebars (`{{...}}`) 和 PQL (`{%= ... %}`) 语法之间的区别，包括用法表、转义字面量双引号的指南以及新增的&#x200B;**适用于特殊属性键的 PQL 语法规则**&#x200B;部分，其中涵盖保留关键字、连字符属性键和数值事件 ID。 关于反引号转义的说明也已更正：可以在`{{...}}`块中直接引用连字符字段名称；只有反引号语法在此处无效。 [了解详情](../personalization/personalization-syntax.md)

* **日期时间函数**&#x200B;文档扩充了新的实际示例：针对 `dateDiff` 的倒计时模式、针对 `dayOfWeek` 的周末与工作日条件设置（其中包含使用历程条件活动来处理路由用例的说明），以及一个结合 `extractHours` 和 `extractMinutes` 并带有前导零保护机制的仅显示时间的模式。 [了解详情](../personalization/functions/dates.md)

* **字符串函数**&#x200B;文档已更新，新增关于`replaceAll`的示例，显示如何将结果分配给`{% let %}`变量以供同一模板中的多个表达式重复使用。 [了解详情](../personalization/functions/string.md#replace-all)

* **数组函数**&#x200B;文档已更新，新增了&#x200B;**对数组进行迭代**&#x200B;部分，其中说明了 Handlebars `{{#each}}` 块辅助函数的使用，并包含一条注释，阐明 `{{#each}}` 仅在个性化编辑器中受支持，无法在历程条件活动中使用。 [了解详情](../personalization/functions/arrays-list.md#each-loop)

* **数据集入门**&#x200B;页面已更新，在系统数据集部分新增了一个&#x200B;**入站**&#x200B;条目，其中说明了 _AJO 入站活动事件数据集_。 已添加注释，阐明轮廓必须至少从[!DNL Journey Optimizer]发送一条消息，才能在此数据集中捕获传入消息。 [了解详情](../data/get-started-datasets.md#system-datasets)

* **导出消息内容**&#x200B;文档已扩展，其中包含&#x200B;**消息导出常见问题**（个性化内容、图像和媒体、跟踪链接、PII、保留、用例等），并包含针对短信和电子邮件的&#x200B;**导出 JSON** 示例。 [了解详情](../configuration/message-export.md)

* 新增 **AJO 消息导出架构**&#x200B;页面记录了 AJO 消息导出数据集中的每个字段，以及导出的电子邮件和短信负载的数据类型和层级。 [了解详情](../configuration/message-export-schema.md)

* 新增&#x200B;**在电子邮件中个性化 URL** 页面，整合了关于动态 URL 个性化、完整/基本 URL 个性化、URL 跟踪参数个性化和关键护栏的指南。 [了解详情](../email/url-personalization.md)

* 新增&#x200B;**业务规则查询**&#x200B;部分已添加到查询示例页面，提供数据湖查询以检查特定日期后特定历程上由于历程频率上限排除而放弃的所有轮廓。 查询包含`eventCodeReason`字段，用于识别由于达到上限 (`CAP_REACHED`) 还是较低优先级 (`LOWER_PRIORITY`) 从而排除轮廓。 [了解详情](../reports/query-examples.md#business-rules-queries)

* **历程属性**&#x200B;文档已更新，以便在历程属性面板中记录新的&#x200B;**当前历程负载大小**&#x200B;指示器。 此只读字段显示与配置的限制相比的历程负载的当前大小（例如 1.5 MB/2 MB），可帮助您在发布之前监测历程复杂性并避免与大小相关的发布错误。 [了解详情](../building-journeys/journey-properties.md#journey-payload-size)

## 2026 年 4 月 {#april-2026}

* **更改维度**&#x200B;活动文档已更新，阐明了活动会使用外部连接并在维度更改步骤中保留所有记录，但在投放消息时，那些在新目标维度中没有匹配轮廓的记录将被静默排除。 [了解详情](../orchestrated/activities/change-dimension.md)

* **向电子邮件添加抄送字段**&#x200B;文档中的护栏已得到增强。 他们现在明确规定，不会根据同意书或屏蔽名单检查抄送地址，并且发送至抄送地址的电子邮件的打开和点进次数将计入发送分析的总打开和点进次数中。 [了解详情](../configuration/cc-email-field.md)

* **渠道活动**&#x200B;文档已更新，其中新增了&#x200B;**营销与事务性消息**&#x200B;部分，对两种渠道类别在行为上的差异进行了说明：选择启用要求、业务规则应用、渠道配置类型和推荐的用例。 [了解详情](../orchestrated/activities/channels.md#marketing-vs-transactional)

* **分支活动**&#x200B;文档新增了&#x200B;**示例**&#x200B;部分，其中阐述了如何使用分支活动在单个营销活动运行中将受众拆分到两个并行的电子邮件分支（一个属于营销类，一个属于事务性）。 [了解详情](../orchestrated/activities/fork.md#fork-examples)

* **构建受众活动**&#x200B;文档已新增一个示例，显示如何使用规则生成器按订阅计划属性筛选用户档案。 [了解详情](../orchestrated/activities/build-audience.md#build-audience-examples)

* **编排的营销活动快速入门**&#x200B;页面在&#x200B;**编排的营销活动包含哪些内容？**&#x200B;部分中介绍了入门级的&#x200B;**生成受众 → 分支 → 渠道 A + 渠道 B**&#x200B;模式，并包含指向分支活动以及营销与事务性消息页面的交叉引用。 [了解详情](../orchestrated/gs-orchestrated-campaigns.md#gs-ms-campaign-inside)

* **使用高级 HTML 编辑器编辑电子邮件内容**&#x200B;页面已从“内容管理”部分移至文档的&#x200B;**电子邮件**&#x200B;部分。 该页面现在说明，高级 HTML 编辑器可在电子邮件设计器中用于电子邮件消息以及电子邮件内容模板。 [了解详情](../email/email-expert-mode.md)

* **开始和监视编排的营销活动**&#x200B;文档已更新，添加了新章节，详细介绍内部发布时间执行顺序、营销活动生命周期状态表、发布前核对清单以及非重复营销活动的发送确认警告。 [了解详情](../orchestrated/start-monitor-campaigns.md#publication-sequence)

* **保存受众**&#x200B;活动文档已更新，并附注阐明：在发布时，“保存受众”活动始终在消息活动之前执行。 [了解详情](../orchestrated/activities/save-audience.md)

* **编排的营销活动常见问题解答**&#x200B;中新增了三个问题：发布时内部发生的情况、发布后消息可能无法发送的 7 点原因清单，以及档案快照查找与实时档案解析有何不同。 [了解详情](../orchestrated/orchestrated-campaigns-faq.md)

* 已在历程疑难解答文档中新增了&#x200B;**[因受阻的历程实例而丢弃的事件](../building-journeys/troubleshooting-execution.md#max-instance-stack-events-reached)**，说明了`maxInstanceStackEventsReached`丢弃原因、丢弃时间以及缓解措施。 护栏和步骤事件字段列表页面也已相应更新。

* **在决策策略中利用片段**&#x200B;文档现在包含针对&#x200B;**电子邮件**&#x200B;渠道的护栏说明：**[!UICONTROL 模拟内容]**&#x200B;不会显示决策项中的表达式片段，而&#x200B;**[!UICONTROL 发送校样]**&#x200B;和激活的营销活动则会显示。 该页面还声明&#x200B;**[!UICONTROL 可视化片段]**&#x200B;不能分配给决策项 - 此上下文中仅支持&#x200B;**表达式片段**。 [了解详情](../experience-decisioning/fragments-decision-policies.md)

## 2026年3月 {#march-2026}

* 有关&#x200B;**使用体验决策预览基于代码的体验**&#x200B;的文档现在澄清&#x200B;**[!UICONTROL 模拟内容]**&#x200B;仅是内容预览。 创作预览中不模拟实时 Edge 请求的上下文数据。 [了解详情](../code-based/test-code-based.md#preview-code-based)

* **使用 Adobe Experience Platform 数据**&#x200B;文档已更新：护栏不再说明无法链接数据集查找，这反映了当前的产品行为。 [了解详情](../data/lookup-aep-data.md)

* 已更新&#x200B;**更新用户档案**&#x200B;活动文档，以记录支持在单个操作中更新最多五个用户档案属性。 [了解详情](../building-journeys/update-profiles.md)

* 已更新&#x200B;**读取受众**&#x200B;活动和&#x200B;**历程属性**&#x200B;文档，以阐明始终运行定期历程的 91 天历程生命周期。 计划部分现在明确确认，没有结束日期的定期历程保持过去 91 天的实时状态，并且全局超时常见问题解答已得到扩展，以区分 91 天用户档案 TTL 与 91 天报告窗口。 [了解详情](../building-journeys/read-audience.md#schedule)

* **数据集查找**&#x200B;活动文档已更新，以阐明必须在高级模式下配置查找密钥，才能使`@datasetLookup{}`语法在下游条件活动中工作。 添加了疑难解答部分，其中包含有关解决“未找到数据集查找”错误的指南。 [了解详情](../building-journeys/dataset-lookup.md#troubleshooting)

* **日期时间函数**&#x200B;文档已更新，其中新增了一个示例，展示如何根据上下文事件属性设置时间戳的格式，包括`toDateTime()`要求、数字事件 ID 的反引号语法以及 PQL“输入不匹配”错误的常见错误标注。 [了解详情](../personalization/functions/dates.md#format-date)

* **编排的营销活动护栏和限制**&#x200B;和&#x200B;**源连接器入门**&#x200B;文档已更新，以阐明对于基于文件的变更数据捕获，`_change_request_type` 字段是必需项，其值必须为小写 `u` (upsert) 或 `d` (delete)，而不是大写。 [了解详情](../orchestrated/guardrails.md)

* **添加链接和跟踪消息**&#x200B;文档已更新，其中包含有关如何生成跟踪标识符 (urlID) 的指南：仅当 URL 和标签均唯一时，才分配唯一的 urlID。 要在多个电子邮件中跟踪同一 URL（或在一封电子邮件中跟踪多次），用户必须对每个类似的 URL 使用唯一标签；否则，[!DNL Journey Optimizer]无法确定点击了哪个链接。 [了解详情](../email/message-tracking.md#track-across-multiple-emails)

* **创建测试配置文件**&#x200B;文档已更新，其中包含有关身份标识描述符要求的重要说明：删除并重新创建数据集时，架构必须在主身份标识字段上保留正确的身份标识描述符。 如果没有此描述符，即使摄取成功完成，摄取的用户档案也不会标记为`testProfile = true`。 添加了疑难解答核对清单。 [了解详情](../audience/creating-test-profiles.md)

* 已更新&#x200B;**读取受众**&#x200B;活动文档，以阐明&#x200B;**业务事件**&#x200B;活动是“读取受众”必须是历程中第一个活动规则的例外。 还添加了引用&#x200B;**优化**&#x200B;活动的注释，将其作为控制受众定位的高级替代方法。 [了解详情](../building-journeys/read-audience.md)

* 在历程中&#x200B;**使用波次发送**&#x200B;功能现已正式可用。 已从文档中移除有限范围发布标志。 [了解详情](../delivery/send-using-waves.md)

* 已向&#x200B;**跳转**&#x200B;活动文档添加新的设计策略部分（**小型子历程**），该部分介绍如何将复杂的端到端流分解为通过“跳转”活动连接的更小、重点突出的子历程。 [了解详情](../building-journeys/jump.md#jump-strategy)

* **标记**&#x200B;文档已更新，其中包含有关使用标记类别作为复杂命名惯例的替代方法的指南。 新部分将介绍如何为可伸缩历程管理设置标记类别。 [了解详情](../building-journeys/tags.md)

* **关于数据源**&#x200B;文档现在包含一个新的部分，可帮助从业人员在三种数据访问策略之间进行选择：通过自定义操作访问外部数据，使用未启用配置文件的数据集或使用启用配置文件的数据集。 每个选项都说明了折衷方案和推荐的用例。 [了解详情](../datasource/about-data-sources.md#data-access-strategy)

* **推送通知设计**&#x200B;文档已更新，其中附有注释，明确说明通用链接在 iOS 上的行为：如果将通知 URL 注册为通用链接，则无论选择哪个 Web URL 操作，关联的应用程序都将打开。 已添加有关如何强制打开浏览器的指南。 [了解详情](../push/design-push.md)

* Decisioning 文档中现在提供新的&#x200B;**监控您的 AI 模型**&#x200B;页面。 它介绍了如何直接在[!DNL Journey Optimizer]中跟踪个性化优化模型的运行状况、培训状态和性能。 [了解详情](../experience-decisioning/ranking/ai-model-observability.md)

* 电子邮件模板的&#x200B;**高级 HTML 编辑器**（专家模式）现在以“有限可用性”模式上线。 文档页面现已可公开访问。 此功能允许您直接通过电子邮件设计器查看和编辑电子邮件内容模板的原始 HTML 源代码。 [了解详情](../email/email-expert-mode.md)

* 已更新 **URL跟踪**&#x200B;和&#x200B;**历程疑难解答**&#x200B;文档，以记录`context.system.source.actionId`在已关闭历程中的行为。 已关闭或未重新发布的历程可能会在跟踪 URL 中生成空`{}`占位符。 已添加有关如何通过重新发布历程或移除受影响的参数来解决问题的指南。 [了解详情](../email/url-tracking.md)

* **Adobe Experience Platform 数据源**&#x200B;文档已更新，并附上注释，指出数据源配置中仅支持基于 XDM 个人配置文件的架构。 [了解详情](../datasource/adobe-experience-platform-data-source.md)

* **数据集生存时间 (TTL) 护栏**&#x200B;文档已增强，并新增一个常见问题解答条目，以明确识别哪些数据集须遵循 TTL。 TTL 仅适用于时间序列数据集 - 记录类型数据集（如实体数据集、分类数据集和决策对象存储库）不受 TTL 约束，并且不会受到护栏转出的影响。 [了解详情](../data/datasets-ttl.md)

* 已更新&#x200B;**历程属性**&#x200B;和&#x200B;**暂停历程**&#x200B;文档，以记录历程技术详细信息中现在提供的新暂停和恢复字段。 除了现有的 `pausedJourneySettings` 块之外，**复制技术详细信息**&#x200B;按钮现在还包含 `lastPausedAt`、`lastPausedBy`、`lastPausedById`、`lastResumedAt`、`lastResumedBy` 和 `lastResumedById`。 还向&#x200B;**暂停历程**&#x200B;页面新增一个部分，说明如何直接通过历程属性查看暂停和恢复时间戳。 [了解详情](../building-journeys/journey-properties.md)

## 2026 年 2 月 {#february-2026}

* 决策管理现在新增了一个页面。 它列出了使用个性化编辑器个性化产品建议内容（展现方案）时支持的所有运算符、辅助函数和函数。 使用此列表可避免运行时错误。 在产品建议决策中对内容进行个性化处理时，仅支持文档中已列出的函数。 [了解详情](../offers/offer-library/personalization-editor-supported-functions.md)

* 已针对电子邮件更新了&#x200B;**创建决策策略**&#x200B;和&#x200B;**在邮件中使用决策策略**&#x200B;文档：请注意，当电子邮件正文中的多个决策策略可以选择同一优惠时，引擎会删除重复优惠（每个投放位置都会收到不同的优惠）。 要在多个投放位置（例如，页眉和页脚）中显示相同的优惠，请使用&#x200B;**重复使用决策输出**。 [了解详情](../experience-decisioning/create-decision-policy.md)

* 更新了“决策项”页面，其中包含有关推送渠道和自定义事件上限的信息。 [了解详情](../experience-decisioning/items.md#capping)

* **历程中的体验事件查找**&#x200B;文档已更新，并增加了弃用时间线：自 2026 年 4 月 1 日开始，过去 90 天内未在历程表达式中使用体验事件属性的组织将无法再访问此功能。 常见问题解答现在侧重于停用时间线和受影响的人员，同时已对体验事件架构页面进行调整，并提供指向替代方法的直接链接。 [了解详情](../building-journeys/exp-event-lookup.md)

* **Decisioning** 文档已更新，内容为使用 Adobe Experience Platform 数据进行&#x200B;**数据集查找**：支持的渠道护栏现在规定，数据集查找适用于决策可用的所有渠道（历程中基于代码的体验、电子邮件、推送、短信和内容决策活动）。 已从“决策规则”、“排名公式”和“决策项”页面中移除有限可用性和公共测试版说明。 [了解详情](../experience-decisioning/aep-data-exd.md)

* 外部系统集成页面已更新，其中包含指向自定义数据源和自定义操作的链接，并阐明出口代理为从&#x200B;**自定义操作**&#x200B;到外部系统的出站调用提供静态 IP。 [了解详情](../configuration/external-systems.md)

* 历程试运行文档已予以明确：步骤事件属性 `inDryRun` 和 `dryRunID` 现已注明，在试运行模式下会返回 `true`/实例 ID，而在测试或实时历程中则返回 `null`。 相应更新了在报告查询中排除试运行步骤事件的指南。 [了解详情](../building-journeys/journey-dry-run.md)

* **Web 推送**&#x200B;现已正式发布。 推送通知文档已重组并相应地更新（入门、设计、发送、创建）。 [了解详情](../push/get-started-push.md)

* 现在，文档中提供了 Web 推送配置页面。 [了解详情](../push/push-configuration-web.md)

* 有关在决策中使用片段的文档已更新：在“片段”和“决策”部分中添加了注释，并更新了“决策策略中的片段”页面。 [了解详情](../experience-decisioning/fragments-decision-policies.md)

* 短信 Webhook 文档已更新：Twilio Webhook 内容已被移除。 [了解详情](../mobile/mobile-webhook.md)

* **将图像转换为内容模板**&#x200B;文档已增强，新增了扩展的护栏和建议、常见用例以及更清晰的指南，说明如何将图像设计转换为可编辑的 HTML 内容模板。 文档还提到，您现在可以使用主题作为转换的输入。 [了解详情](../content-management/image-to-html.md)

* 更新了 Decisioning 迁移 API 文档。 [了解详情](../experience-decisioning/decisioning-migration-api.md)

* **内容决策**&#x200B;活动现已正式发布。 “内容决策活动”页面已更新，其中新增了一个部分，介绍步骤事件中可用的 Decisioning 数据。 [了解详情](../building-journeys/content-decision.md)

* “忠诚度挑战”部分已添加指向忠诚度挑战 API 文档的链接（入门、创建挑战、创建任务、访问忠诚度挑战）。 [了解详情](../loyalty-challenges/get-started.md)

* 营销活动创建向导文档中有关受支持的渠道信息已更正。 “渠道入门”和“编排的营销活动常见问题解答”页面也进行了相应更新。 [了解详情](../campaigns/get-started-with-campaigns.md)

* 权限文档中关于&#x200B;**历程管理**&#x200B;和&#x200B;**审批**&#x200B;权限的内容已得到更正。 [了解详情](../administration/ootb-permissions.md)

* AEM (Adobe Experience Manager) 集成文档已更新并使用修订后的命名（AEM 动态内容和 AEM 片段）。 [了解详情](../integrations/aem-fragments.md)

* 排除列表中已新增一个排除原因：**UnsubscribeLinkNotValid**（错误代码 050081）。 当 List-Unsubscribe mailTo 主题长度大于 RFC 限制的 998 个字符时，将生成此排除项。 [了解详情](../reports/exclusion-list.md)

* formatDate 辅助函数文档已得到增强，其中的注释指出该函数需要日期时间字段类型（而非字符串），并提供了多个示例：设置日期时间字段的格式、将字符串首先转换为日期、使用日期名称表示完整日期、使用系统时间表示动态日期，以及包含小写输出的每周日期格式。 [了解详情](../personalization/functions/dates.md#format-date)

* 文本版本电子邮件文档已得到增强，其中包含全面的用例指南，包括何时使用自定义纯文本与自动同步的决策标准、包含真实场景的实用示例以及包含常见问题的常见问题解答部分。 [了解详情](../email/text-version-email.md#when-to-use)

* 电子邮件设计器主题文档已更新，其中包含有关 Web 字体支持限制和回退字体重要性的信息。 [了解详情](../email/apply-email-themes.md#themes-guardrails)

* 在执行元数据辅助函数文档添加了限制，以明确说明不会对从操作中排除的用户档案捕获元数据。 [了解详情](../personalization/functions/helpers.md#execution-metadata)

* 基于代码的实现示例文档已更新，以在 propositionAction 中包含令牌字段，以便在 Decisioning 中进行准确跟踪和归因。 [了解详情](../code-based/code-based-implementation-samples.md#client-side-how)

* 在 URL 跟踪和列表取消订阅文档中添加了注释，以明确说明附加到 URL 的 URL 跟踪参数的顺序是随机的，无法控制。 [了解详情](../email/url-tracking.md)

## 2026 年 1 月 {#january-2026}

* 许可证使用情况仪表板文档已更新，明确了有关&#x200B;**可参与用户档案**&#x200B;的指南说明，包括定义详细信息和疑难解答指南。 [了解详情](../audience/license-usage.md#what-is-engageable-profile)

* 在电子邮件设计器主题文档中添加了注释，以阐明 Web 字体支持限制。 [了解详情](../email/apply-email-themes.md#themes-guardrails)

* 新增了一个护栏部分，用于说明历程负载大小验证，包括警告和错误阈值以及有关如何优化历程的指导。 [了解详情](../start/guardrails.md#journey-payload-size)

* 更新了 Decisioning 护栏文档，其中包括决策项大小限制（包含属性的决策项不得超过 1KB，且属性数量上限为 30 个）。 [了解详情](../experience-decisioning/decisioning-guardrails.md)

* 在决策策略创建文档中添加了注释，以告知用户，在创建决策策略后，任何更改都可能需要 15 分钟才能传播到所有数据区域，而加拿大最多需要 30 分钟。 [了解详情](../experience-decisioning/create-decision-policy.md#review)

* 在片段文档中添加了注释，以警告在片段中同时编辑按钮标签和 URL 时，跟踪数据集会记录 URL 值，而不是标签值。 [了解详情](../content-management/customizable-fragments.md#visual)

* 现已推出一个新页面，其中介绍从决策管理迁移到 Decisioning 的好处，包括有关即将推出的迁移工具 API 的信息。 [了解详情](../experience-decisioning/migrate-to-decisioning.md)

* 添加了护栏，以明确说明查找数据集仅适用于数据集沙盒所属区域中基于边缘的入站激活。 [了解详情](../data/lookup-aep-data.md#guidelines)

* 在编排的营销活动渠道配置文档中新增了一个部分，说明如何在 URL 跟踪参数中使用上下文属性（例如营销活动 ID、名称和操作详细信息）进行分析和报告。 [了解详情](../orchestrated/channel-config.md#url-tracking)

* 对内容优化文档进行了重组，使其更加清晰明了。 主优化页面已拆分为四个专题子页面：一个快速入门页面、一个专门介绍目标选择的页面、一个介绍实验的页面，还有一个介绍结合使用两种方法的页面。 [了解详情](../content-management/gs-message-optimization.md)

* 已从三个旅程警报（已发布历程、已完成历程和已触发自定义操作上限设置）中移除“有限发布版”说明，因为这些功能现已正式发布。 [了解详情](../reports/alerts.md)

* 测试、验证与审批登陆页面现已优化升级，新增了测试能力概述、常见问题解答、带导航链接的决策树，以及附有文档链接的强化术语表等板块。 [了解详情](../../rp_landing_pages/test-landing-page.md)

* 个性化语法文档中新增了一个章节，专门阐明如何在个性化表达式中使用保留关键字。 某些 PQL 关键字（例如 `next`、`last` 和 `this`）在 XDM 架构中作为字段名称使用时，必须使用反引号进行转义。 [了解详情](../personalization/personalization-syntax.md#reserved-keywords)

* [营销活动入门](../campaigns/get-started-with-campaigns.md)和[管理营销活动](../campaigns/manage-campaigns.md)页面已重新构建，采用改进的信息架构，其中包含完整全面的工作流（附带针对特定类型的指南）、优化的营销活动类型对比表以及整合的状态说明表。

* 历程登陆页面已重新设计，新增六步上手指引工作流，优化历程类型对比表，并全面提升文档内的导航体验。 [了解详情](../building-journeys/journey.md)

* 新增详细章节，指导用户在配置直邮文件路由时为 SFTP 认证生成 Base64 编码的 OpenSSH 私钥，以避免连接错误。 [了解详情](../direct-mail/direct-mail-configuration.md#ssh-key-generation)

* 子域名委派文档中已添加说明，提示用户在尝试向 Adobe 委派前，需预留 24-48 小时等待 DNS 传播生效。 [了解详情](../configuration/delegate-subdomain.md#set-up-subdomain)
