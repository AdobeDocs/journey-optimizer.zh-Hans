---
solution: Journey Optimizer
product: journey optimizer
title: 发行说明
feature: Release Notes
role: User
level: Beginner, Intermediate
description: Adobe Journey Optimizer 发行说明
exl-id: 06fa956a-b500-416e-9d42-b683c328e837
TQID: https://experienceleague.adobe.com/YJKQFYUi8Kw7yZZKm8blcM-1G9uYsqcsEsopH0hOMhA
product_v2:
  - id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2:
  - id: b3538224-471e-4c63-a444-9b19d89ae29c
  - id: d556b755-390a-43f0-be32-a08cf6236126
  - id: d998adac-2f81-400b-a669-d07bb196e4eb
  - id: df64005d-8f9a-422e-ba4d-c6f6dc3454b4
  - id: fe338112-e2ce-4876-8989-fc4d497613f1
subfeature_v2:
  - id: c2beecbb-b93e-4ae3-baa9-72adcdc06781
  - id: cfba2953-2ce9-4b00-a00c-71cd338ae63f
  - id: ee5bb250-0884-4d71-86eb-d8489e8bcadd
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2:
  - id: a004cc84-67b9-4a33-a3a7-8ec7273ef4dc
  - id: bce87dde-a4ab-44c9-8a18-ad66e4ddb377
  - id: d00e9f03-e50b-4162-b143-0c0817c937c2
  - id: e0eb8757-182f-49f3-94a4-1587d16f5094
source-git-commit: f00bb7373065f199346326b3b3e85c542dcd56d8
workflow-type: tm+mt
source-wordcount: 2609
ht-degree: 81%

---

# 发行说明 {#release-notes}

>[!CONTEXTUALHELP]
>id="ajo_homepage_card1"
>title="新增功能"
>abstract="**Adobe Journey Optimizer** 不断地提供新功能、增强现有功能，并修复错误。 所有更改会在每月的最后一周整合到发行说明中。"

[!DNL Adobe Journey Optimizer] 遵循持续交付模式，使 Adobe 能够持续不断地提供新功能、增强功能和修复。 此方法支持以可扩展的方式分阶段推出各种功能，以确保所有环境的性能和稳定性。

由于此模型，在每月发行版本之间会更新发行说明。 有关发行周期和可用性阶段的完整详细信息，请参阅 [Journey Optimizer 发行周期](releases.md)。

[!DNL Adobe Journey Optimizer] 原生构建于 [!DNL Adobe Experience Platform] 之上并继承了其所具备的最新创新技术和改进。 在 [Adobe Experience Platform 发行说明](https://experienceleague.adobe.com/docs/experience-platform/release-notes/latest.html?lang=zh-Hans){target="_blank"}中进一步了解这些更改。

## 2026年5月更新 {#may-26-rn}

<table>
<thead>
<tr>
<th><strong>电子邮件设计器中的深度链接</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>现在，可以通过电子邮件设计器中的专用选项向电子邮件内容添加深度链接。</p><p>这可确保用户直接被带到正确的应用程序内内容，而不是重定向到浏览器或应用商店，从而保持上下文和参与度。</p>
<p><img src="assets/do-not-localize/deeplinks.gif"></p>
<p>有关更多信息，请参阅<a href="../email/deeplinks.md">详细文档</a>。</p>
<p>发布日期： 2026年5月12日</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>历程模拟</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>您现在可以将历程设置为<strong>模拟</strong>模式。 此模式允许您使用<strong>模拟用户</strong>验证逻辑。 这些是为了模拟而专门创建的临时轮廓，让您可以自由测试，而无需在 Adobe Experience Platform 中管理长期保留的测试轮廓。</p>
<p>此功能以限量发布版的形式提供给所有客户，仅具备基础能力。</p>
<p><img src="assets/do-not-localize/simulate-user.gif"></p>
<p>有关更多信息，请参阅<a href="../building-journeys/simulate-journey.md">详细文档</a>。</p>
<p>发布日期： 2026年5月5日</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>决策规则和排名公式AI优化</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>[!DNL Adobe Journey Optimizer] 现在使用AI检测可简化的决策规则和排名公式。 在库存中，AI已为其标识优化机会的任何规则上均会显示一个红色指示符。 单击该指示器会显示原始表达式和AI建议的版本。 从此处，您可以下载一个文件以查看每个版本评估模拟配置文件的方式，并确认它们行为相同，然后将表达式替换为优化表达式。</p>
<p>有关更多信息，请参阅<a href="../start/ai-features.md#decisioning-optimization">详细文档</a>。</p>
<p>发布日期： 2026年5月5日</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>集成</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p><b>集成</b>功能允许您直接将第三方数据源连接到 Adobe Journey Optimizer。 该功能简化了拉取外部数据和<b>可组合内容</b>的方式，使您能够更轻松地在所有渠道中提供个性化、动态的消息。</p>
<p>此功能之前作为 Beta 版发布，现在可供在所有环境中使用（正式发布）。</p>
<p>有关更多信息，请参阅<a href="../integrations/integrations.md">详细文档</a>。</p>
<p>发布日期： 2026年5月4日</p>
</td>
</tr>
</tbody>
</table>

### 改进 {#may-26-improv}

#### 决策

* **决策迁移工作流API** — 用于创建依赖项分析和迁移工作流的API协定已更新：在请求URL （`sandbox`、`offer`或`decision`）上传递&#x200B;**`request-level`**&#x200B;作为&#x200B;**查询参数**。 不能再在JSON正文中发送请求级别。 [了解详情](../experience-decisioning/decisioning-migration-api.md)

  发布日期： 2026年5月6日

#### 短信

<!--
* **Opt-out and consent at phone number and sender** - For SMS, Journey Optimizer now records marketing consent and opt-out at the level of both the profile's phone number and short code. 

  This capability is currently only available for Sinch SMS configurations. [Read more](../sms/sms-configuration-sinch.md)
-->

* **字符数** – 在 Adobe Journey Optimizer 中，您现在可以使用字符数实时监控短信消息的长度。 它有助于您了解消息何时会被拆分为多个片段，以便更好地管理格式并避免发送成本意外增加。 [了解详情](../sms/create-sms.md)

* **使短信进入自定义数据集** – 在&#x200B;**短信 API 凭据**&#x200B;中，将&#x200B;**入站短信**&#x200B;路由到您选择的&#x200B;**启用了轮廓的自定义体验事件数据集**，而不仅仅路由到默认的跟踪数据集。 [了解详情](../sms/sms-webhook.md)

* **Webhook 界面增强功能** – 在配置短信 Webhook 时，用户界面现在包含带有实用示例的内置设置指南，让您无需离开配置流程，即可更轻松地对齐提供商负载和解决问题。 [了解详情](../sms/sms-webhook.md)

#### WhatsApp

* **WhatsApp按钮支持和跟踪** - WhatsApp模板现在支持&#x200B;**快速回复**、**Call to action - URL**&#x200B;和&#x200B;**Call to action — 不支持电话**、**复制代码**。 Journey Optimizer会发送支持的按钮并跟踪与其他渠道报表的交互。

## 即将推出 {#coming-soon}

以下功能和增强功能计划在未来几天发布。 **信息可能会有所更改**。 这些更新在生产环境中启用后，将会共享更新的链接、屏幕和文档。

### 新功能 {#comming-soon-features}

<table>
<thead>
<tr>
<th><strong>历程片段</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>您现在可以在Adobe Journey Optimizer中创建<strong>历程片段</strong>。 历程片段是可重用的旅程节点集，您可以只构建一次这些节点，然后将其放到沙盒中的任意旅程中。 无论是资格检查、首选渠道路由逻辑还是欢迎序列，片段都可以帮助团队更快地移动并保持一致，而无需每次从头开始重建相同的逻辑。</p>
<p>创建后，片段将存储在专用的<strong>片段清单</strong>中，并可使用<strong>历程片段</strong>活动插入任何历程。</p>
<!--<p><img src="assets/do-not-localize/journey-fragments.gif"></p>-->
<p>此功能仅适用于一组组织（限量发布）。 要获得访问权限，请与 Adobe 代表联系。</p>
<!--p>For more information, refer to the <a href="../building-journeys/journey-fragments.md">detailed documentation</a>.</p-->
<p>发布日期： 2026年5月12日</p>
</td>
</tr>
</tbody>
</table>

## 2026年4月发行说明 {#april-26-rn}

<!--
**The pre-release notes below are subject to change without prior notice until the release availability date**. Links, screens and updated documentation are published in the release notes, at the release date.

See also [Adobe Experience Platform Pre-release notes](https://experienceleague.adobe.com/zh-hans/docs/experience-platform/release-notes/pre-release-notes){target="_blank"}.
-->

四月初发布的新功能和改进内容随其可用日期一同公布。

**发布日期**：2026 年 4 月 28-29 日

### 新功能 {#april-26-features}

<table>
<thead>
<tr>
<th><strong>编排的营销活动中的增量查询活动</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p><strong>编排的营销活动</strong>现在支持<strong>增量查询</strong>活动，该活动仅定向到自上次执行以来新符合条件的轮廓或事件。

这使得重复性营销活动始终专注于全新受众（新注册、新符合条件的忠诚度会员和类似区段），同时减少查询工作负载，并避免随时间推移而出现的冗余发送。</p>
<p>有关更多信息，请参阅<a href="../orchestrated/activities/incremental-query.md#incremental-query-configuration">详细文档</a>。</p>
<p>发布日期： 2026年4月30日</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>电子邮件标头中的发件人参数</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>凭借 Journey Optimizer，您现在可以在发送实体（发件人）与撰写实体（来自）不同的情况下发送电子邮件。 支持此功能的电子邮件客户端通常将其呈现为“发件人 代表 来自”或显示一个“经由”指示标记。 填写电子邮件渠道设置中可选的<strong>发件人标头</strong>字段以配置此功能。</p>
<p><img src="assets/do-not-localize/sender-headers.gif"></p>
<p>有关更多信息，请参阅<a href="../email/header-parameters.md#sender-header">详细文档</a>。</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>电子邮件渠道设置中的“抄送”字段</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>您现在可以在电子邮件渠道设置中配置可选的“抄送”字段。 与密件抄送不同，抄送收件人对主要收件人可见，从而实现透明的通信和更清晰的责任归属。</p>
<p>这样，您就可以自动将正确的利益相关者（如客户关系经理或客户负责人）添加到每封邮件的抄送列表，同时确保客户知道应联系谁进行跟进。</p>
<p>抄送字段支持个性化，因此单个配置可以根据用户轮廓数据动态路由邮件副本，无需额外设置即可扩展至多种用例。</p>
<p><img src="../configuration/assets/email-config-cc.png"></p>
<p>有关更多信息，请参阅<a href="../configuration/cc-email-field.md">详细文档</a>。</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>跨沙盒复制编排的营销活动</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>沙盒工具现在支持将编排的营销活动从一个沙盒打包并复制到另一个沙盒。 这样便无需在每个环境中手动重建营销活动。 打包营销活动时，其核心依赖对象（如合并策略、消息）会自动包含在内，因此营销活动在导入后即可直接进行配置和验证。 为了保护生产环境，所有导入的营销活动都会在目标沙盒中进入草稿状态，从而使团队可以在任何营销活动上线之前执行审查和审批步骤。</p>
<p><img src="assets/do-not-localize/oc-sandbox.gif"></p>
<p>有关更多信息，请参阅<a href="../configuration/copy-objects-to-sandbox.md">详细文档</a>。</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>通过 MCP 集成 Journey Optimizer AI 代理</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Adobe Journey Optimizer现在提供了一个<strong>MCP（模型上下文协议）服务器</strong>，该服务器直接在任何MCP兼容的应用程序中呈现营销活动、渠道配置和沙盒操作。 通过这种集成，不同的角色可以围绕相同的编排数据进行协作。 您可以用对话方式描述您的意图，让 LLM 调用相应的 MCP 工具，无需编写针对 Adobe Journey Optimizer REST API 的查询，也无需在多个 UI 界面之间来回导航。 此功能当前在 Claude Web 端和桌面端中可用。</p>
<p>此功能已向使用公开 Beta 版的所有客户开放。</p>
<p>有关更多信息，请参阅<a href="../integrations/ajo-mcp.md">详细文档</a>。</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>历程仲裁 – AI 模型</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>您现在可以在排名公式中使用 <strong>AI 模型</strong>，以根据客户轮廓属性和上下文因素自动提升历程优先级分数，确保客户进入最相关的历程。</p>
<p>此功能仅面向一部分组织（限量发布）。 要获得访问权限，请与 Adobe 代表联系。</p>
<p><img src="assets/do-not-localize/journey-arbitration-ai-models.gif"></p>
<p>有关更多信息，请参阅<a href="../conflict-prioritization/journey-ai-models.md">详细文档</a>。</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Adobe Express 集成</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Adobe Journey Optimizer 中的 <b>Adobe Express 集成</b>允许您在内容创建过程中直接使用 Adobe Express 的编辑工具，从而能够调整大小、删除背景、进行裁切以及将资产转换为 JPEG 或 PNG 格式。
</p>
<p>此功能此前为有限发布版，现已可供所有环境使用（正式发布版）。</p>
<p><img src="assets/do-not-localize/express_resize.gif"></p>
<p>有关更多信息，请参阅<a href="../integrations/express.md">详细文档</a>。</p>
<p>发布日期：2026 年 4 月 23 日</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>针对 AI 收件箱优化电子邮件</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Adobe Journey Optimizer 现新增了一项功能，可确保您的电子邮件拥有优化的结构，能够很好地适应采用 AI 技术的收件箱，例如 Apple Intelligence 以及 Gmail 中的 Google Gemini。</p>
<p>随着 AI 助手越来越多地左右收件人阅读和处理电子邮件的方式，此功能可帮助您生成和创作出在各类下游 AI 任务（包括摘要生成、分类、优先级排序和意图提取）中表现良好的内容。</p>
<p><img src="assets/do-not-localize/optimize-for-ai.gif"></p>
<p>有关更多信息，请参见<a href="../email/llm-email-optimizer.md">为 AI 收件箱优化电子邮件</a>。</p>
<p>发布日期：2026 年 4 月 17 日</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>用于个性化表达式的 AI 助手</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>[!DNL Adobe Journey Optimizer] 现在在个性化编辑器中直接包含<strong>AI助手</strong>，以及可将自然语言提示转换为有效的个性化表达式和条件逻辑的Email Designer，无需语法专业知识。 描述您想要实现的个性化效果，AI 便会生成可直接使用的代码。您可以立即应用这些代码，或通过后续的提示对其进行优化完善。</p>
<p>AI 助手也能反向工作。 选择任何现有的表达式，要求它解释逻辑、识别问题或提出改进建议。 这不仅使其可用于编写新的表达式，还可用于跨团队审查和调试现有的表达式。</p>
<p><img src="assets/do-not-localize/assistant-perso.gif"></p>
<p>有关详细信息，请参阅<a href="../content-management/generative-personalization-expressions.md">用于个性化表达式的 AI 助手</a>。</p>
<p>发布日期：2026 年 4 月 13 日</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>历程路径试验</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>使用新的<strong>优化</strong>节点，运行 A/B 测试或多臂老虎机实验，确定达成以业务为中心的 KPI 的最佳路径。 通过此工具，您可以测试、更改并自定义通信、顺序和时间，以便更好地联系客户。
</p>
<p>此功能此前为有限发布版，现已可供所有环境使用（正式发布版）。</p>
<p>作为正式发布的一部分，此版本引入了针对单一历程的<strong>试验类型</strong>选择（A/B 或多臂老虎机）和<strong>入选者扩展</strong>功能。</p>
<p><img src="assets/do-not-localize/optimize-experiment.gif"></p>
<p>有关更多信息，请参阅<a href="../building-journeys/path-experimentation.md">详细文档</a>。</p>
<p>发布日期：2026 年 4 月 7 日</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>收件箱</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p><strong>收件箱</strong>是随内容卡一起提供的移动功能，它使客户能够在其应用程序或网站中创建一个集中的位置，用于显示发送给其用户的消息。 这确保了消息在被关闭后仍然可访问，从而延长了营销通信的存留期。</p>
<p><img src="assets/do-not-localize/inbox.gif"/></p>
<p>有关更多信息，请参阅<a href="../inbox/inbox-gs.md">详细文档</a>。</p>
<p>发布日期：2026 年 4 月 7 日</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>电子邮件渠道中的决策支持</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>您现在可以使用<strong>决策</strong>功能对电子邮件信息的内容进行个性化设置和优化。 利用优先级分数、公式或 AI 模型，向每位收件人显示最相关的产品建议和内容。</p>
<p>此功能此前为有限发布版，现已可供所有环境使用（正式发布版）。 在此限量发布版中，现在支持镜像页面。</p>
<p><img src="assets/do-not-localize/exd-email.gif"></p>
<p>有关更多信息，请参阅<a href="../experience-decisioning/create-decision-policy.md">详细文档</a>。</p>
<p>发布日期：2026 年 4 月 6 日</p>
</td>
</tr>
</tbody>
</table>

### 改进 {#april-26-improv}

#### AI

<!--
* **Brand alignment score in Campaign dashboard** - You can now assess your brand alignment score directly within your Campaign dashboard to ensure content stays on-brand. This allows you to verify guidelines at a glance without having to open the content designer.
-->

* **提示助手增强功能** – 提示助手可实时分析用户提示并识别清晰度、完整度和上下文方面的不足，从而增强 AI 内容的生成。 它会提出优化的改写建议，并提供可操作的指导，帮助您在提示中补充受众、语气、意图等关键细节。 此功能还会提出有针对性的澄清问题，以帮助用户在生成之前优化其输入。 这样可以生成更准确、高质量的输出，迭代次数更少。 [了解详情](../content-management/ai-assistant-prompting-guide.md#prompt-assistant)

  发布日期： 2026年5月5日

#### 推送

* **在渠道设置中个性化应用程序 ID** – 在“推送”渠道配置设置中，您现在可以对&#x200B;**应用程序 ID** 字段进行个性化设置，从而基于每个收件人的轮廓信息，向他们发送相应品牌的推送通知。 [了解详情](../push/push-configuration.md#app-id-personalization)

#### 决策

* **决策迁移工作流API** — 用于创建依赖项分析和迁移工作流的API协定已更新：在请求URL （`sandbox`、`offer`或`decision`）上传递&#x200B;**`request-level`**&#x200B;作为&#x200B;**查询参数**。 不能再在JSON正文中发送请求级别。 [了解详情](../experience-decisioning/decisioning-migration-api.md)

  发布日期： 2026年5月6日

* **将片段附加到决策项** – Journey Optimizer 现在提供将片段附加到决策项的功能，可通过决策策略，在基于代码的体验和电子邮件营销活动中利用这些片段。 [了解详情](../experience-decisioning/fragments-decision-policies.md)

  此功能此前为有限发布版，现已可供所有环境使用（正式发布版）。

* **跳过暂时不可用的片段** – 在决策项中使用片段时，如果某个片段在 Edge 上暂时不可用，则会跳过该片段，并且历程或营销活动将继续渲染而不会失败。 [了解详情](../experience-decisioning/fragments-decision-policies.md#temporary-unavailable-fragments)

  发布日期：2026 年 4 月 14 日

#### Adobe Experience Manager 集成

* **Adobe Experience Manager 内容片段变体支持** – 在插入 Adobe Experience Manager 内容片段时，您可以选择&#x200B;**内容片段变体**（例如语言或渠道变体），并且改进了区域设置和多语言场景的处理。 [了解详情](../integrations/aem-fragments.md#aem-variations)

  此功能此前为有限发布版，现已可供所有环境使用（正式发布版）。

* **创作时的 Adobe Experience Manager 内容片段上下文** – 在文本字段和内容块之间移动时，您的内容片段选择将保持活跃状态，以便您可以添加更多片段字段，而无需每次都重新调出&#x200B;**打开 AEM 内容顾问**。 [了解详情](../integrations/aem-fragments.md)

  此功能此前为有限发布版，现已可供所有环境使用（正式发布版）。

#### 电子邮件设计

* **电子邮件内容的高级 HTML 编辑器** – 借助高级 HTML 模式，您可以在电子邮件设计器中编辑内容的 HTML 源，在源中添加高级表达式（如条件），还能在 HTML 视图和桌面视图之间切换，而不会丢失所做的更改。

  此功能之前仅可用于电子邮件内容模板，现已部署到电子邮件设计器中的&#x200B;**电子邮件**&#x200B;内容（例如，在历程和营销活动中创作的电子邮件）以及电子邮件内容模板。 它目前处于限量发布状态，请联系您的 Adobe 代表以获取访问权限。 [了解详情](../email/email-expert-mode.md)

  发布日期：2026 年 4 月 9 日

#### 历程

* **在历程属性中可见的当前历程有效负载大小** — 历程属性面板现在显示与配置的限制相比的历程有效负载的当前大小 — 例如，*1.5 MB （共2 MB）*。 此只读指示器可帮助您在发布之前监控历程复杂性，并避免因超出有效负载大小限制而导致的错误。 [了解详情](../building-journeys/journey-properties.md#journey-payload-size)

  发布日期： 2026年4月30日

#### 历程路径优化

* **试验类型** – 在配置路径试验时，您现在可以在 A/B 试验（开始时固定比例分配）或多臂老虎机（自动分配比例并每周更新权重）之间进行选择。 [了解详情](../building-journeys/path-experimentation.md)

  发布日期：2026 年 4 月 7 日

* **路径试验：扩展入选者** – 您现在可以自动或手动将试验的入选路径扩展到全体受众。 确定入选者后，即可扩大其覆盖范围并增强其效果，而无需持续监控试验。 [了解详情](../building-journeys/path-experimentation.md#scale-winner)

  此功能仅在单一历程（事件触发和受众资格认定）中可用。 它不适用于读取受众历程。

  发布日期：2026 年 4 月 7 日

* **条件** – [优化](../building-journeys/optimize.md)活动是用于在历程中创建条件路径的新工具。 它取代了以前的&#x200B;**条件**&#x200B;活动，该活动已从 UI 中移除。 所有条件逻辑都得以保留，现在通过&#x200B;**优化**&#x200B;活动的条件进行处理。 [了解详情](../building-journeys/conditions.md)

  此功能此前为有限发布版，现已可供所有环境使用（正式发布版）。

  发布日期：2026 年 4 月 7 日

#### 编排的营销活动

* **编排的营销活动中的全局变量** – 编排的营销活动现在支持全局变量，这些变量只需定义一次，就能在工作流内的所有活动中重复使用，从而简化配置并确保动态值、表达式和内容个性化的一致性。 [了解详情](../orchestrated/global-variables.md)
* **数据建模器增强功能** – 编排的关系架构现在支持跨多个字段的组合键。 从 DDL 文件加载架构时还会引入明细列表，从 DDL 或 Excel 文件加载时会自动创建表之间的组合关系。 在实体关系视图中，复合链接现在会在上传文件后显示表之间的完整字段配对集。 [了解详情](../orchestrated/gs-schemas.md)

