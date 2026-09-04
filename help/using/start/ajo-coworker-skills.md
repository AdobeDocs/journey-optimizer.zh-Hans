---
solution: Journey Optimizer
product: journey optimizer
title: CX Co-worker 中的 Journey Optimizer 技能
description: 通过深入的指导和示例提示，了解CX Co-worker中提供的Adobe Journey Optimizer技能。
feature: Overview
topic: Artificial Intelligence
role: User
level: Beginner
mini-toc-levels: 2
source-git-commit: 565af0d1f7350ea5eec93a8e4c826539bc0326b5
workflow-type: tm+mt
source-wordcount: '3995'
ht-degree: 6%

---


# CX Co-worker 中的 Journey Optimizer 技能 {#ajo-coworker-skills}

>[!BEGINSHADEBOX]

**在此页面上：**&#x200B;通过针对每种技能的详细指导、示例提示和最佳实践，了解CX Co-worker中可用的Adobe Journey Optimizer技能 — 从创建和分析历程到生成渠道内容和管理内容资源。

>[!ENDSHADEBOX]

## 概述 {#overview}

CX Co-worker为Adobe Journey Optimizer提供了AI支持的功能。 [CX Co-worker](https://experienceleague.adobe.com/zh-hans/docs/cx-enterprise-coworker/content/home){target="_blank"}是Adobe的对话体验，可与您的业务应用程序集成，帮助您更高效地工作。

凭借AI支持的技能， CX Co-worker使Journey Optimizer用户能够使用自然语言界面创建、分析和优化营销历程。 借助历程技能，从业人员可以快速构建历程，检测和解决计划或受众冲突，分析绩效和流失点，并确定表现最佳的历程以复制到未来的营销活动。 它使从业者能够做出数据驱动型决策、提高客户参与度并简化历程编排。

CX Co-worker提供了多种管理历程和忠诚度难题的技能：

**以历程为主的技能：**

* **历程创建**：通过自然语言提示生成和配置营销历程
* **渠道内容创建**：使用AI支持的内容生成功能生成、编辑和管理历程的渠道特定内容（电子邮件、推送、短信）
* **历程分析**：分析旅程、检测问题、揭示见解并优化旅程性能

**注重忠诚度的技能：**

* **忠诚度挑战管理**：使用自然语言提示创建和管理忠诚度挑战
* **忠诚度代理 — 数据Insight技能**：使用自然语言查询和分析忠诚度计划绩效数据

CX Co-worker还包括一组&#x200B;**内容管理MCP工具**，用于发现、创建和管理Journey Optimizer内容模板、片段、登陆页以及历程/营销活动内联消息内容。 [了解详情](#content-management)

<!--
feedback from Ivan: Need to remove Simulate skill from docs until Nico confirms the release timeline.

In addition, **Journey Simulation** is a Journey Optimizer feature that includes [Journey Simulate](https://experienceleague.adobe.com/zh-hans/docs/journey-optimizer/using/orchestrate-journeys/create-journey/simulate-journey/simulate-journey-gs), an in-product agentic skill, non conversational, with three capabilities: 

* Generating simulated users
* Generating event values
* Quick simulation
-->

## 历程技能 {#journey-skills}

### 历程创建 {#journey-create}

通过历程创建，Journey Optimizer用户可以使用自然语言界面构建和配置营销历程。 借助历程创建，从业者可以通过在对话提示中描述其要求来快速创建历程。 该技能向用户介绍创建历程的不同选项，允许营销人员专注于策略而不是技术配置。

>[!AVAILABILITY]
>
>要充分利用历程创建功能，您需要以下权限：
>
>**管理历程**：此权限允许您直接在CX Co-worker中创建新历程。
>
>**查看历程事件、数据源和操作**：此权限确保CX Co-worker可以搜索历程事件和自定义操作。
>
>**查看区段**：此权限可确保CX Co-worker在创建历程时能够搜索受众区段。
>
>**管理区段**：此权限允许您直接在CX Co-worker中创建新受众。

#### 主要用例

历程创建可加快营销执行的优惠功能：

1. **事件触发的历程创建**

   * 创建根据特定客户事件激活的历程。
   * 实时设计对客户行为的自动化响应。
   * 基于客户行为构建个性化的通信流。

   **商店访问历程：**
   “创建在用户进入我的商店位置时开始的历程。 发送推送通知以欢迎用户访问应用商店。 等待2天并检查用户是否具有有效的电子邮件地址。 如果用户拥有有效的电子邮件地址，请发送电子邮件调查来询问其商店体验。 如果用户没有有效的电子邮件地址，请发送推送通知以提示注册。”

   **购买后历程：**
   “创建客户在线购买时开始的历程。 发送推送通知以感谢他们购买。 接下来，检查他们是否是忠诚会员。 如果用户是忠诚度奖励会员，请发送带有10%折扣代码的第二个推送通知。 如果用户不是忠诚度奖励成员，请发送推送，邀请他们注册忠诚度计划。 请等待2天，然后发送后续推送信息，其中包含有关其购买体验的调查。”

   **基于事件的促销活动：**
   “创建游戏分数达到50时触发的历程。 向忠诚会员发送一条短信消息，称他们有资格从合作伙伴赞助商那里免费分到披萨。”

1. **面向受众的历程创建**

   * 构建以特定受众区段为目标的历程。
   * 设计具有策略时间的多步通信序列。

   **季节性营销活动：**
   “我想创建一个以日间徒步旅行者为目标的历程。 我想发送一封电子邮件，提醒此受众我即将到来的假期促销，其中包括各种徒步旅行必需品。 在发送第一封电子邮件后等待3天，然后再发送一封包含15%优惠券且免运费的第二封电子邮件。 等待一周，然后发送第3封电子邮件展示我们的新睡袋和帐篷收藏。 安排在12月20日开始历程。”

   **忠诚度感谢：**
   “为SUV车主打造忠诚度提升历程，包括提供免费洗车优惠的感谢推送通知以及后续推送通知提醒（如果第一个通知未在1天内进行交互）。”

1. **业务事件触发的历程创建**

   * 创建根据特定业务事件激活的历程，并以指定受众为目标（例如，产品回售或游戏分数更改）
   * 当业务状况发生变化时，触发及时的上下文感知消息。

1. **受众资格历程创建**

   * 创建历程，并在用户档案进入或退出受众区段定义时激活。
   * 自动发送登录和退出消息，以支持上线、保留和回馈目标。

1. **条件历程流**

   * 根据客户属性创建决策分支。
   * 根据客户喜好设计拆分路径。

1. **从图像创建历程**

   * 将参考图像上传到同事中，并要求使用该图像作为参考创建历程
   * 历程创建技能将从参考图像中提取可编辑提示

凭借此技能，自然语言要求将转换为结构化的历程配置。

#### 范围技能

历程创建支持以下功能：

* **自然语言历程创建**：允许用户以对话语言描述历程流程。
* **基于事件和基于受众的历程**：支持基于触发器和计划的历程类型，以及业务事件和受众资格。
* **条件逻辑**：根据客户属性处理决策拆分和分支。
* **多渠道消息传递**：支持推送通知、电子邮件和短信渠道。
* **历程计划**：配置计划历程的开始日期和时间。

#### 超出范围技能

目前不支持以下功能：

* 高级历程分析
* Cross-journey orchestration
* A/B测试配置
* InAudience表达式生成
* 数据集查找节点
* 波形发送设置
* 计划循环选项
* 受众的命名空间选择
* 自定义操作字段映射
* 复杂的数据转换

#### 提示最佳实践

要最大限度地提高历程创建效率，请遵循以下最佳实践：

1. **具体**：提供有关历程目标、目标受众和所需操作的清晰详细信息。 包括有关渠道、计时和条件的信息。
1. **指定时间**：明确指示操作之间的等待时间以及历程应何时开始。
1. **定义条件**：使用条件逻辑时，请说明每个分支路径的条件。
1. **包括渠道**：指定要使用的通信渠道（推送、电子邮件、短信）。
1. **提及计划**：对于计划的历程，请提供所需的开始日期和时间。
1. **自定义操作**：如果您在工作流中使用自定义操作，则需要指定您使用的是自定义操作以及自定义操作的确切名称。 示例：
当用户进入我的商店位置时，使用自定义操作ExternalPush发送欢迎消息。 等待2天，然后使用自定义操作ExternalEmail发送跟进消息，其中包含有关其访问情况的调查。
1. **验证表达式**：确保检查并验证历程技能创建的任何表达式，以确保使用正确的字段和值。

#### 设置最佳实践

* **定义明确的目标**：在创建历程之前，请建立明确的目标（提高维系率、促进转化、提高参与度）。
* **准备受众**：确保已创建目标受众并正确分段。
* **规划消息内容**：在创建历程之前定义消息传递策略。
* **考虑客户体验**：设计尊重客户偏好并避免过度沟通的历程流程。

### 渠道内容创建 {#channel-content-create}

<!--Ivan : Need to speak with Amar on new options for content generation as this skill has changed. -->

>[!AVAILABILITY]
>
>此功能仅对有限可用的所有客户可用。 请联系 Adobe 代表获取访问权限。

渠道内容创建使Journey Optimizer用户能够使用AI支持的内容生成来生成、编辑和管理历程的特定于渠道的内容。

#### 主要用例

1. **特定于渠道的内容生成**：使用自然语言提示生成电子邮件、推送通知、SMS和其他渠道的内容。

   “为我的欢迎历程生成电子邮件内容。 用友好的语气为新客户创建欢迎电子邮件，并包含10%的折扣优惠。”

   &quot;为我的商店访问历程生成推送通知。 创建欢迎消息，鼓励客户登记并接收特惠。”

   “为事件触发的历程生成短信内容。 使用call-to-action创建一条短消息，通知客户闪购。”

1. **基于模板的内容创建**：通过预览功能浏览并选择可用模板。

   “向我显示季节性活动历程的可用电子邮件模板。”

   “为我的电子邮件选择一个设计新颖、简洁的模板。”

1. **多渠道内容管理**：在同一历程工作流中为多个渠道生成和管理内容。

1. **In-context内容编辑**：在Content Designer中打开生成的内容进行编辑和细化。

   “在Content Designer中打开电子邮件内容，以便我可以自定义设计。”

1. **内容精简和迭代**：使用重新生成操作重新生成具有不同色调或样式的内容。

   “重新生成推送通知内容，语调更加随意。”

   “更新电子邮件内容以包含促销代码。”

1. **历程画布集成**：从清单中选择历程并查看关联的渠道。

#### 范围技能

渠道内容创建支持以下功能：

* **AI支持的内容生成**：使用自然语言提示生成电子邮件、推送、SMS和其他渠道的内容。
* **模板管理**：浏览并从具有预览功能的可用模板中进行选择。
* **In-context editing**：在Content Designer中打开生成的内容以进行编辑和细化。
* **内容重新生成**：使用“重新生成”操作重新生成具有不同色调、样式或消息传递的内容。
* **多渠道支持**：在同一历程工作流中为多个渠道生成和管理内容。
* **历程库存访问**：从库存中选择历程并查看关联的渠道。

#### 超出范围技能

目前不支持以下功能：

* **品牌一致性和内容质量检查**
* **将内容节点直接插入历程画布**
* **模板导入**

#### 提示最佳实践

1. **明确**：提供有关内容类型、语调、目标受众和关键消息的清晰详细信息。
1. **指定渠道**：明确指示您正在为哪个渠道创建内容（电子邮件、推送、短信）。
1. **定义音调**：指定所需的音调（友好、正式、休闲、紧急）。
1. **迭代并优化**：使用重新生成操作优化内容，直到满足您的要求为止。

### 历程分析 {#journey-analyze}

历程技能将使Journey Optimizer用户能够使用自然语言界面分析和优化旅程。 借助历程技能，从业人员可以快速识别并解决计划和/或受众冲突，检测历程中的用户放弃点并提供见解或建议。 它使从业者能够做出数据驱动型决策、提高客户参与度并简化历程编排。

>[!AVAILABILITY]
>
>所有有权访问CX Co-worker的客户都可以使用历程技能。 但是，您需要以下权限才能充分利用历程技能功能：
>
>**查看历程**：此权限允许您直接在CX Co-worker中查看历程见解。
>
>**管理历程**：此权限允许您直接在CX Co-worker中创建新历程。
>
>**查看区段**：此权限允许您直接在CX Co-worker中查看受众的分析。
>
>**管理区段**：此权限允许您直接在CX Co-worker中创建新受众。

#### 主要用例

历程分析提供了一系列可用于优化营销工作的功能：

1. **历程流失分析**

   * 确定客户在历程中的何处流失以及原因。
   * 识别导致客户停止参与的行为模式。
   * 利用洞察来改进历程设计，提高保留率。

   示例提示：
   * “我想按节点分析7月4日营销活动旅程的流失。”
   * “为7月4日营销活动的历程执行流失分析。”
   * “在‘七月四日’营销活动的历程中，用户档案丢失情况如何？”
   * “展示7月4日营销活动在旅程中用户流失的位置。”

1. **历程受众重叠分析**

   * 分析多个历程中的受众重叠。
   * 防止因目标选择过度而导致受众疲劳。
   * 优化分段，以确保均衡的参与度。

   示例提示：
   * “超过X个历程中使用了哪些受众？”
   * “使用[受众名称]受众列出所有历程。”
   * “向我显示历程[受众名称]的历程重叠冲突。”
   * “显示历程[历程名称]和其他历程的重叠受众。”

1. **历程计划重叠分析**

   * 识别针对同一受众群体的预定的历程之间的时间冲突。
   * 避免过度沟通，提高计划效率。
   * 确保历程在最佳时间运行，最大限度地发挥受众影响力。

   示例提示：
   * “历程[历程名称]是否存在任何计划冲突？”
   * “检查与历程[历程名称]有关的计划冲突。”
   * “突出显示历程[历程名称]和实时历程之间的计划重叠。”
   * “历程[历程名称]是否正在运行与任何其他历程冲突？”

1. **运营洞察**

   * 基于提示的历程见解 — 有关历程的表面运营见解，即“显示所有实时历程”。

   示例提示：
   * “[历程名称]何时发布？”
   * “[历程名称]何时停止？”
   * “列出当前处于测试模式的所有历程”
   * “我有多少个实时历程？”
   * “向我提供所有计划定期历程及其预期运行时间的列表。”

1. **自定义操作错误历程**

   * 识别历程中的自定义操作何时失败或错误率何时激增。
   * 在故障演变成更广泛的历程中断之前诊断根本原因。
   * 使用特定的修正步骤快速恢复自定义操作的可靠性。

   示例提示：
   * “为什么自定义操作在历程[历程名称]中失败？”
   * “历程[历程名称]中的自定义操作[自定义操作名称]的错误率是多少？”
   * “显示历程[历程名称]中自定义操作失败的根本原因。”
   * “当前是否存在影响历程[历程名称]的自定义操作错误？”

#### 范围技能

历程分析支持以下功能：

* **回应式查询**：允许用户询问有关历程表现、受众使用情况和时间计划冲突的具体问题。
* **与其他技能集成**：与受众和数据分析功能协作以进行更深入的分析。
* **响应结构**：推理（解释逻辑）、分析摘要（突出显示关键点）、问题详细信息（描述问题）和推荐（建议后续步骤）。
* **自定义操作错误分析**：检测和诊断历程中的自定义操作失败和错误峰值。

#### 超出范围技能

目前不支持以下功能：

* **自动创建历程**
* **实时异常检测**
* **渠道重叠**
* **历程进入分析**
* **技术问题分析**
* **疲劳分析**

#### 提示最佳实践

要最大限度地提高历程分析的有效性，请遵循以下最佳实践：

1. **描述具体**：使用清晰简洁的提示来获得有针对性的见解。 例如，请指定“列出上个月创建的所有历程”，而不是询问“我的历程是什么？”。
1. **结合见解**：集成受众的见解和数据见解功能，全面了解历程性能。
1. **迭代改进**：使用流失和重叠分析来迭代改进历程设计和时间计划。

#### 设置最佳实践

* **定义明确目标**：在分析历程之前，先确定明确的目标（例如提高保留率、增加转化率）。
* **定期监测**：计划好定期查看历程表现，以识别趋势和异常。
* **优化分段**：确保受众细分均衡，以避免疲劳以及最大限度地提高参与度。

## 忠诚度技能 {#loyalty-skills}

>[!AVAILABILITY]
>
>CX Co-worker为符合条件的组织提供了忠诚度技能。 拥有忠诚度许可证的客户可以访问这些忠诚度技能，即使他们没有额外的CX Co-worker许可证也是如此。

忠诚度技能使忠诚度管理员和分析人员能够使用自然语言创建、管理和分析忠诚度计划。 借助这些AI支持的技能，您可以快速设计引人入胜的忠诚度挑战、跟踪绩效指标并做出数据驱动型决策以优化成员参与和项目获利能力。 无论您是在提出新的挑战，还是在分析忠诚度计划趋势，忠诚度技能都可以简化整个忠诚度管理工作流。

### 忠诚度挑战管理 {#loyalty-challenge-management}

忠诚度挑战管理使Journey Optimizer用户能够使用自然语言提示在CX Co-worker中创建和管理忠诚度挑战。 有关创建、配置和管理忠诚度挑战的完整文档，包括详细的设置说明，请参阅[忠诚度挑战指南](../loyalty-challenges/get-started.md)。

#### 主要用例

1. **多步入门挑战**

   为新注册的客户构建一个名为“新帐户Kickstart”的挑战，要求他们按顺序完成以下步骤：打开支票帐户，至少使用500美元为其提供资金，并下载移动应用程序。 完成所有步骤后，给予5000分奖励。 9月1日至10月31日（东部时区）运行。”

1. **累积活动阈值质询**

   “为持卡人创建名为”Spent &amp; Earn Summer“的挑战，持卡人第三季度在信用卡上花费1500美元即可获得50美元的对帐单信用。 7月1日开始，东部时区。”

1. **频度连续挑战**

   对精英阶层会员发起一项名为“飞行常客冲刺”的挑战，要求会员连续两个月每月飞行3次。 以层级状态扩展和10,000英里奖励完成工作。 下个月第一个月，太平洋时区开始。”

1. **单个合格操作挑战**

   “设置一个名为”无纸化“的挑战，在后付费用户注册自动付款并在30天内切换到无纸化计费后，给予500个积分的奖励。 下个月的第一天，中部时区开始。”

1. **参与/消费目标挑战**

   创建名为“Explorer Badge”的挑战，要求成员在8月份至少完成3个不同类别的5项活动。 奖励他们1,000点和“浏览”完成时的徽章。 从8月1日开始，山区时区。”

1. **每日操作挑战**

   “帮我给抹茶爱好者带来一个挑战，要求他们本周每天到店里买一杯抹茶饮料。 如果他们能完成挑战，应该会得到额外200分的奖励。 可将其称为“Macha about Matcha”，使用SKU matcha-001，在下周一和东部时区启动。

#### 范围技能

忠诚度挑战管理支持以下功能：

* **挑战创建**：从自然语言（受众、操作标准、时间、奖励、命名）创建挑战配置。
* **质询更新**：通过迭代提示修改质询详细信息。
* **挑战发布**：直接从对话中发布支持的挑战配置。
* **质询上下文可见性**：迭代时检索和查看质询信息。

#### 超出范围技能

目前不支持以下功能：

* 挑战删除
* 忠诚度洞察和推荐技能
* 在所有情况下实现挑战消息传递的完全内容创作自动化

#### 提示最佳实践

1. **将其命名为**：用引号为挑战提供一个清晰易记的标题。
1. **指定受众**：符合条件的受众（例如，所有成员、层、区段、新注册者、持卡人、订阅者）。
1. **定义操作和数量**：成员必须执行的操作，以及计为完成的频率、阈值或序列。
1. **设置时间范围**：开始日期（如果持续时间固定，则为结束日期）加上时区。
1. **说明奖励**：积分、英里、结算积分、状态延期、优惠券或完成时授予的津贴。
1. **引用符合条件的事件**：指向挑战跟踪的特定SKU、产品、帐户操作或参与事件。

### 忠诚度代理 — 数据Insight {#loyalty-data-insight}

忠诚度代理 — Data Insight Skill允许Journey Optimizer用户使用自然语言分析和查询忠诚度计划绩效数据。 此技能可提供有关忠诚度积分、成员层、赎回和收入量度的洞察，从而让忠诚度管理员和分析师能够制定关于其忠诚度计划的数据驱动型决策。

主要用例：

1. **会员积分分析**

   * 分析在特定时段内授予、授予和兑换的忠诚度积分。
   * 比较不同忠诚度级别和计划之间的忠诚度点活动。
   * 按成员区段跟踪会员积分余额。

   示例提示：
   * “2026年8月期间，有多少忠诚度积分被授予？”
   * “2026年8月，会员在每个忠诚度级别上获得了多少忠诚度积分？”
   * “向我显示2026年8月期间会员忠诚度状态（而非忠诚度等级）兑换的总忠诚度积分。”
   * “显示2026年8月按忠诚度级别细分的忠诚度积分总余额。”

1. **收入和折扣分析**

   * 按层级和计划分析订单收入和忠诚度折扣趋势。
   * 比较忠诚度计划和时间段之间的收入生成。
   * 跟踪折扣对收入和成员参与的影响。

   示例提示：
   * “2026年8月每个忠诚度级别的总订单收入是多少？”
   * “2026年8月，每个忠诚度级别都打了多少忠诚度折扣？”
   * “显示2026年8月按忠诚度计划细分的忠诚度折扣总数。”
   * “2026年8月，每个忠诚度计划产生的订单收入总计是多少？”

1. **项目表现分析**

   * 分析每日、每周和每月的程序性能指标。
   * 比较不同产品类别和折扣策略的绩效。
   * 确定成员参与和赎回模式的趋势。

   示例提示：
   * “显示2026年8月按天划分的忠诚度计划总收入。”
   * “显示2026年8月按产品类别细分的总忠诚度折扣。”
   * “给我看2026年第三季度忠诚度计划绩效报告。”

### 内容管理 {#content-management}

>[!AVAILABILITY]
>
>内容管理适用于所有有权访问CX Co-worker的客户。

<!--However, you will need the following permissions in order to fully use the Content Management features:
**Manage Library Items**: This permission lets you list, retrieve, create, and update content templates and fragments directly in CX Coworker.

**Publish Fragment**: This permission lets you publish fragments directly in CX Coworker.-->

Journey Optimizer用户能够使用自然语言提示直接从CX Co-worker发现和管理内容资产 — 内容模板、片段、登陆页面和历程/营销活动内联消息内容。 它可让您从“告诉我我的内容”转到“构建、更新和发布内容”，而不离开对话。 此功能由适用于Journey Optimizer内容的15个可读写的MCP工具提供支持。

#### 主要用例

1. **浏览并检查内容**

   * 列出可用的内容模板、片段或登陆页，并检索其结构、元数据和状态。
   * 检索在历程或营销活动操作节点上配置的内联消息内容。

   示例提示：
   * “列出我的电子邮件内容模板。”
   * “给我看看我的夏季促销活动可用的片段。”
   * “获取登陆页面123的详细信息。”
   * “为营销活动camp-789中的操作节点的电子邮件变体配置什么内容？”

1. **创建内容模板**

   * 为任何渠道创建新的内容模板。

   示例提示：
   * “使用此HTML内容创建一个名为‘夏季促销’的电子邮件模板。”
   * “创建一个名为‘Flash Alert’的新短信模板。”

1. **更新内容模板**

   * 完全替换现有模板的内容。

   示例提示：
   * “使用此新HTML正文更新模板abc-123。”

1. **创建、更新、克隆和发布片段**

   * 创建新的HTML或表达式片段。
   * 更新现有片段的内容或元数据。
   * 使用新名称克隆现有片段。
   * 提交草稿片段以供发布。

   示例提示：
   * “使用此标记创建名为‘促销横幅’的HTML片段。”
   * “更新片段frag-456以将其名称更改为‘促销横幅V2’。”
   * “克隆片段abc-123作为促销横幅 — 夏天（变体B）。”
   * “发布片段frag-456。”

1. **更新内联消息内容**

   * 替换营销活动或历程操作节点的内联消息中的一个渠道变体。
   * 列出在历程或营销活动操作节点上定义的渠道变体。

   示例提示：
   * “使用此新内容更新营销活动camp-789中操作节点的电子邮件变体。”
   * “此操作节点上定义了哪些渠道变体？”

#### 范围

内容管理支持以下功能：

* **列出并获取内容模板**：浏览内容模板并检索其结构和元数据。
* **列出并获取片段**：浏览内容和表达式片段并检索其详细信息。
* **列出并获取登陆页面**：浏览登陆页面并检索其元数据和页面内容。
* **获取营销活动/历程内联内容**：检索在营销活动或历程操作节点上配置的内联消息内容，包括多语言变体。
* **创建内容模板**：为任何渠道创建新模板。
* **更新内容模板**：完全替换现有模板的内容。
* **创建、更新、克隆和发布片段**：创建新片段，更新现有片段，使用新名称克隆片段，并提交草稿片段以供发布。
* **更新内联消息内容**：替换促销活动/历程操作节点内联消息上的渠道变体（包括多语言变体），并列出操作节点上定义的渠道变体。

#### 超出范围

目前不支持以下功能：

* **跨模板或片段的全文搜索**
* **模板或片段验证**（孤立的引用、断开的链接、已弃用的组件）
* **创建或发布登陆页面**
* **正在删除内容模板、片段或登陆页面**

#### 提示最佳实践

1. **已知时引用ID**：在请求获取、更新、克隆或发布特定资产时，请提供模板、片段、登陆页面或营销活动/历程ID。
1. **明确了解渠道**：创建模板或片段时，请指定渠道或内容类型（电子邮件、HTML片段、表达式片段）。
1. **发布前确认**：在请求同事发布片段之前，请在创建或更新片段后查看片段的内容。
1. **提供完整的替换内容**：更新操作会完整替换内容，因此在提示中包含完整的HTML正文或变体内容。

<!--
Feedback from Ivan: Journey simulate is not ready as a skill

## Journey Simulate: Use Cases, Agentic Skills and User Guide

## Overview

>[!BEGINSHADEBOX]

Journey Simulation is available to all Journey Optimizer customers. Journey Simulate, the in-product agentic skill within Journey Simulation, is available to customers that are a part of the Agent Orchestrator Explorer program and requires at least one of the following permissions:

* **Simulate journeys**: Run simulation workflows from the journey canvas.

* **Publish journeys**: Publish journeys, including flows that use simulation before go-live.

* **Approve and Publish journeys**: Approve and publish journeys when your organization uses approval workflows.

To use AI in **[!UICONTROL Simulation]** (**[!UICONTROL Quick simulation]**, generating simulated users with AI, **[!UICONTROL Generate event values]**), users require **[!UICONTROL Generate Content]** permission from the **[!UICONTROL AI Assistant]** capability. 

[Learn more about permissions](https://experienceleague.adobe.com/en/docs/journey-optimizer/using/administration/permissions).

>[!ENDSHADEBOX]

Journey Simulation is a Journey Optimizer feature that enables Journey Optimizer users to safely test and validate marketing journeys before activation. Within Journey Simulation, Journey Simulate is an in-product agentic skill, not a conversational one, that automates and assists the testing process directly from the journey canvas.

Journey Simulate includes three capabilities:

* Generating simulated users
* Generating event values
* Quick simulation. 

Together, they bridge the gap between journey creation and activation, building confidence in journey logic and reducing the risk of post-launch errors.

## Use cases

### Key use cases for Journey Simulate

Journey Simulate offers three capabilities that can be leveraged to reduce testing time and improve journey quality before go-live:

**Generating simulated users**

* Generate simulated users automatically based on journey paths and required attributes.
* Create simulated users that cover all branches and conditions in a journey, including execution addresses (email, push, SMS).
* Update simulated user attributes on demand to refine test scenarios.
* Ensure all journey branches are covered by assigning the right simulated user to each path.

**Generating event values**

* Generate values for events used in a journey to drive test execution through specific paths.
* Define event attribute values that trigger the desired conditions and branches during simulation.

**Quick simulation**

* Start journey simulation and trigger test executions for all simulated users needed to test all paths of a journey, in a single interaction.
* Visualize how simulated users flow through a journey, step by step, including branching paths and conditional logic.
* Identify which simulated user flows through which path, and why, with detailed node-by-node traversal.
* Review simulation reporting at the end of a run in the Journey Optimizer UI to validate outcomes before activation.

## In scope skills and limitations

### **In scope**

The following capabilities are supported by the Journey Simulation feature:

* **Simulated user management**: View, edit, and update simulated user attributes, including execution addresses and personalization data.
* **Simulation control**: Start and stop journey simulation directly through the Journey Simulation in-product experience.
* **Test execution**: Trigger test executions for one or multiple simulated users.
* **Journey flow visualization**: View step-by-step traversal of simulated users through journey nodes, including branching, splits, and user status.
* **Simulation reporting**: View reporting at the end of a simulation run in the Journey Optimizer UI.
* **Multi-user testing**: Run and visualize tests for multiple simulated users simultaneously, covering all journey branches.

In addition to this, the following capabilities are supported by the Journey Simulate skill:

* **Simulated user generation**: Create simulated users based on journey paths, existing test profiles, or specified attributes.
* **Event value generation**: Generate and assign event attribute values to drive test execution through specific journey paths.
* **Quick simulation**: Run a full end-to-end simulation with minimal intervention. The skill automatically generates simulated users, event values, and pre-filled test settings, then executes the journey and surfaces results for review.

### **Limitations**

Simulation may not support every activity, channel, or integration that Test mode or a live journey supports, and behavior may change as the capability matures.

➡️ Learn more about [Simulation limitations](https://experienceleague.adobe.com/zh-hans/docs/journey-optimizer/using/orchestrate-journeys/create-journey/simulate-journey/simulate-journey-gs#limitations) in the Journey Optimizer documentation.

-->
