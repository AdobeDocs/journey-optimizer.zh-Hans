---
solution: Journey Optimizer
product: journey optimizer
title: 发行说明
feature: Release Notes
role: User
level: Beginner, Intermediate
description: Adobe Journey Optimizer 发行说明
exl-id: 06fa956a-b500-416e-9d42-b683c328e837
source-git-commit: d975d9cd95d33ea8972cf9388e7f868009c4fb95
workflow-type: tm+mt
source-wordcount: '1990'
ht-degree: 21%

---

# 发行说明 {#release-notes}

>[!CONTEXTUALHELP]
>id="ajo_homepage_card1"
>title="新增功能"
>abstract="**Adobe Journey Optimizer** 不断地提供新功能、增强现有功能，并修复错误。 所有更改会在每月的最后一周整合到发行说明中。"

[!DNL Adobe Journey Optimizer]遵循持续交付模型，允许Adobe持续交付新功能、增强功能和修复。 此方法支持以可扩展的方式分阶段推出各种功能，以确保所有环境的性能和稳定性。

由于此模型，在每月发行版本之间会更新发行说明。 有关发行周期和可用性阶段的完整详细信息，请参阅 [Journey Optimizer 发行周期](releases.md)。

[!DNL Adobe Journey Optimizer] 原生构建于 [!DNL Adobe Experience Platform] 之上并继承了其所具备的最新创新技术和改进。 在 [Adobe Experience Platform 发行说明](https://experienceleague.adobe.com/docs/experience-platform/release-notes/latest.html?lang=zh-Hans){target="_blank"}中进一步了解这些更改。

## 2026年4月发行说明 {#april-26-rn}

<!--
**The pre-release notes below are subject to change without prior notice until the release availability date**. Links, screens and updated documentation are published in the release notes, at the release date.

See also [Adobe Experience Platform Pre-release notes](https://experienceleague.adobe.com/en/docs/experience-platform/release-notes/pre-release-notes){target="_blank"}.
-->

将在4月早些时候发布的新功能和改进中公布其发布日期。

**发行日期**： 2026年4月28日至29日

### 新功能 {#april-26-features}

<table>
<thead>
<tr>
<th><strong>集成</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p><b>集成</b>功能允许您直接将第三方数据源连接到Adobe Journey Optimizer。 通过简化您拉入外部数据和<b>可组合内容</b>的方式，此功能让您更容易在所有渠道中提供个性化、动态的消息传递。</p>
<p>此功能之前作为 Beta 版发布，现在可供在所有环境中使用（正式发布）。</p>
<p>有关更多信息，请参阅<a href="../integrations/integrations.md">详细文档</a>。</p>
<p>发布日期： 2026年5月4日</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>编排的活动中的增量查询活动</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p><strong>编排的营销活动</strong>现在支持<strong>增量查询</strong>活动，该活动仅定向自上次执行以来新符合条件的用户档案或事件。

这使得重复营销活动始终专注于全新受众（新注册、新合格的忠诚度会员和类似区段），同时减少查询工作负载并避免随时间推移而出现的冗余发送。</p>
<p>有关更多信息，请参阅<a href="../orchestrated/activities/incremental-query.md#incremental-query-configuration">详细文档</a>。</p>
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
<p>使用Journey Optimizer，您现在可以在发送实体(Sender)与创作实体(From)不同的情况下发送电子邮件。 支持此功能的电子邮件客户端通常将其呈现为“代表发件人的发件人”或显示“通过”指示符。 填写电子邮件渠道设置中的可选<strong>发件人标头</strong>字段以配置此功能。</p>
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
<p>您现在可以在电子邮件渠道设置中配置可选的“抄送”字段。 与密件抄送不同，抄送收件人对主要收件人可见，从而实现透明通信和更清晰的所有权。</p>
<p>这样，您就可以自动复制每封邮件中适当的利益相关者（如关系经理或客户所有者），同时确保客户知道联系谁进行跟进。</p>
<p>CC字段支持个性化，因此单个配置可以根据用户档案数据动态路由副本，使其可在多个用例中扩展而无需其他设置。</p>
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
<p>沙盒工具现在支持将编排的活动从一个沙盒打包并复制到另一个沙盒。 这样便无需在每个环境中手动重建营销活动。 打包营销活动后，其核心依赖对象（如合并策略、消息）会自动包含在内，因此导入的营销活动便可到达此处进行配置和验证。 为了保护生产环境，所有导入的营销活动都会在目标沙盒中进入草稿状态，从而为团队在任何营销活动上线之前提供审查和审批步骤。</p>
<p><img src="assets/do-not-localize/oc-sandbox.gif"></p>
<p>有关更多信息，请参阅<a href="../configuration/copy-objects-to-sandbox.md">详细文档</a>。</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>通过MCP集成Journey Optimizer AI代理</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Adobe Journey Optimizer现在提供了一个<strong>MCP（模型上下文协议）服务器</strong>，该服务器直接在任何MCP兼容的应用程序中呈现营销活动、渠道配置和沙盒操作。 通过这种集成，不同的角色可以围绕相同的编排数据进行协作。 您可以用对话方式描述您的意图，让LLM调用相应的MCP工具，而不是针对Adobe Journey Optimizer REST API编写查询或导航多个UI屏幕。 此功能当前在Claude Web和Desktop中可用。</p>
<p>此功能适用于公共Beta中的所有客户。</p>
<p>有关更多信息，请参阅<a href="../integrations/ajo-mcp.md">详细文档</a>。</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>历程仲裁 — AI模型</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>您现在可以在排名公式中使用<strong>AI模型</strong>，以根据客户个人资料属性和上下文因素自动提升历程优先级分数，确保客户进入最相关的历程。</p>
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
<p>Adobe Journey Optimizer中的<b>Adobe Express集成</b>允许您在内容创建过程中直接使用Adobe Express的编辑工具，从而能够调整大小、删除背景、裁剪并将资源转换为JPEG或PNG。
</p>
<p>此功能此前为有限发布版，现已可供所有环境使用（正式发布版）。</p>
<p><img src="assets/do-not-localize/express_resize.gif"></p>
<p>有关更多信息，请参阅<a href="../integrations/express.md">详细文档</a>。</p>
<p>发布日期： 2026年4月23日</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>针对AI收件箱优化电子邮件</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Adobe Journey Optimizer现在包含一项新功能，可确保将您的电子邮件结构优化为采用AI的收件箱，例如Gmail中的Apple Intelligence和Google Gemini。</p>
<p>随着AI助理越来越多地控制收件人如何阅读电子邮件和执行操作，此功能可帮助您生成和创作在下游AI任务中表现良好的内容，包括摘要、分类、优先级划分和意图提取。</p>
<p><img src="assets/do-not-localize/optimize-for-ai.gif"></p>
<p>有关详细信息，请参阅<a href="../email/llm-email-optimizer.md">为AI收件箱优化电子邮件</a>。</p>
<p>发布日期： 2026年4月17日</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>适用于Personalization表达式的AI助手</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>[!DNL Adobe Journey Optimizer] 现在在个性化编辑器中直接包含<strong>AI助手</strong>，以及可将自然语言提示转换为有效的个性化表达式和条件逻辑的Email Designer，无需语法专业知识。 描述您要实现的个性化，AI会生成现成的代码，您可以立即应用，或通过后续提示进行优化。</p>
<p>助理的工作方式也相反。 选择任何现有的表达式，要求它解释逻辑、识别问题或提出改进建议。 这使其不仅可用于创作新表达式，而且可用于查看和调试团队中的现有表达式。</p>
<p><img src="assets/do-not-localize/assistant-perso.gif"></p>
<p>有关详细信息，请参阅<a href="../content-management/generative-personalization-expressions.md">Personalization表达式的AI助手</a>。</p>
<p>发布日期： 2026年4月13日</p>
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
<p>使用新的<strong>Optimize</strong>节点运行A/B测试或多臂老虎机实验，以确定满足以业务为中心的KPI的最佳途径。 通过此工具，您可以测试、更改并自定义通信、顺序和时间，以便更好地联系客户。
</p>
<p>此功能此前为有限发布版，现已可供所有环境使用（正式发布版）。</p>
<p>作为正式发布的一部分，此版本引入了<strong>试验类型</strong>选择（A/B或多臂老虎机）和<strong>缩放单一历程的入选者</strong>。</p>
<p><img src="assets/do-not-localize/optimize-experiment.gif"></p>
<p>有关更多信息，请参阅<a href="../building-journeys/path-experimentation.md">详细文档</a>。</p>
<p>发布日期： 2026年4月7日</p>
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
<p><strong>收件箱</strong>是随内容卡一起提供的移动功能，它使客户能够在其应用程序或网站中创建一个集中的位置，以显示发送给其用户的消息。 这延长了营销通信的生命周期，确保消息在关闭后仍可访问。</p>
<p><img src="assets/do-not-localize/inbox.gif"/></p>
<p>有关更多信息，请参阅<a href="../inbox/inbox-gs.md">详细文档</a>。</p>
<p>发布日期： 2026年4月7日</p>
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
<p>您现在可以使用<strong>Decisioning</strong>来个性化和优化电子邮件的内容。 利用优先级得分、公式或AI模型，向每位收件人显示最相关的选件和内容。</p>
<p>此功能此前为有限发布版，现已可供所有环境使用（正式发布版）。 在此General Availability版本中，现在支持镜像页面。</p>
<p><img src="assets/do-not-localize/exd-email.gif"></p>
<p>有关更多信息，请参阅<a href="../experience-decisioning/create-decision-policy.md">详细文档</a>。</p>
<p>发布日期： 2026年4月6日</p>
</td>
</tr>
</tbody>
</table>

### 改进 {#april-26-improv}

<!--
#### AI

* **Brand alignment score in Campaign dashboard** - You can now assess your brand alignment score directly within your Campaign dashboard to ensure content stays on-brand. This allows you to verify guidelines at a glance without having to open the content designer.

* **Prompt Assistant enhancement** - Prompt Assistant enhances AI content generation by analyzing user prompts in real time and identifying gaps in clarity, completeness, and context. It suggests improved rewrites and provides actionable guidance to enrich prompts with key details like audience, tone, and intent. The feature also asks targeted clarifying questions to help users refine their inputs before generation. This results in more accurate, high-quality outputs with fewer iterations. [Learn more](../content-management/ai-assistant-prompting-guide.md)
-->

#### 推送

* **在渠道设置中个性化应用程序ID** — 在“推送”渠道配置设置中，您现在可以个性化&#x200B;**应用程序ID**&#x200B;字段，以便每个收件人都可以根据其个人资料信息接收来自相应品牌的推送通知。 [了解详情](../push/push-configuration.md#app-id-personalization)

#### 决策

* **将片段附加到决策项** — 现在，Journey Optimizer提供将片段附加到决策项的功能，可在基于代码的体验和电子邮件营销活动中通过决策策略利用这些功能。 [了解详情](../experience-decisioning/fragments-decision-policies.md)

  此功能此前为有限发布版，现已可供所有环境使用（正式发布版）。

* **跳过暂时不可用的片段** — 在决策项中使用片段时，如果Edge上暂时无法使用片段，则会跳过该片段，并且旅程或营销活动将继续渲染而不是失败。 [了解详情](../experience-decisioning/fragments-decision-policies.md#temporary-unavailable-fragments)

  发布日期： 2026年4月14日

<!--
#### SMS

* **Character Count** - In Adobe Journey Optimizer, you can now use the Character Count to monitor the length of your SMS messages in real time. It helps you see when a message will be split into multiple segments to better manage formatting and avoid unexpected increases in sending costs. [Read more](../sms/create-sms.md)

* **Opt-out and consent at phone number and sender** - For SMS, Journey Optimizer now records marketing consent and opt-out at the level of both the profile's phone number and short code. 

  This capability is currently only available for Sinch SMS configurations. [Read more](../sms/sms-configuration-sinch.md)

* **SMS inbounds to a custom dataset** - In **SMS API credentials**, route **inbound SMS** to a **custom, profile-enabled Experience Event dataset** you select instead of only the default tracking dataset. [Read more](../sms/sms-webhook.md)

* **Webhook interface enhancement** - When configuring SMS webhooks, the user interface now includes a built-in setup guide with practical examples, making it easier to align provider payloads and troubleshoot issues without leaving the configuration flow. [Read more](../sms/sms-webhook.md)

#### WhatsApp

* **WhatsApp interactive buttons and tracking** - WhatsApp in Journey Optimizer now supports interactive buttons required by your templates and use cases, along with built-in interaction tracking so you can measure engagement and analyze performance alongside your other channel reporting.
-->

#### Adobe Experience Manager集成

* **Adobe Experience Manager内容片段变体支持** — 在插入Adobe Experience Manager内容片段时，您可以选择&#x200B;**内容片段变体**（例如语言或渠道变体），从而改进区域设置和多语言方案的处理。 [了解详情](../integrations/aem-fragments.md#aem-variations)

  此功能此前为有限发布版，现已可供所有环境使用（正式发布版）。

* **创作时Adobe Experience Manager内容片段上下文** — 在文本字段和内容块之间移动时，您的内容片段选择将保持活动状态，以便您可以添加更多片段字段而无需每次重新打开&#x200B;**打开AEM内容顾问**。 [了解详情](../integrations/aem-fragments.md)

  此功能此前为有限发布版，现已可供所有环境使用（正式发布版）。

#### 电子邮件设计

* **电子邮件内容的高级HTML编辑器** — 高级HTML模式允许您在Email Designer中编辑内容的HTML源，在源中添加高级表达式（如条件），并在HTML视图和桌面视图之间切换而不会丢失更改。

  以前此功能仅可用于电子邮件内容模板，现在此功能已部署到Email Designer中的&#x200B;**电子邮件**&#x200B;内容（例如，在历程和营销活动中创作的电子邮件）以及电子邮件内容模板。 它当前处于“有限可用”状态 — 请联系您的Adobe代表以获取访问权限。 [了解详情](../email/email-expert-mode.md)

  发布日期： 2026年4月9日

#### 历程路径优化

* **试验类型** — 在配置路径试验时，您现在可以在A/B试验（开始时固定拆分）或多臂赌博机（自动拆分并每周更新权重）之间进行选择。 [了解详情](../building-journeys/path-experimentation.md)

  发布日期： 2026年4月7日

* **路径实验：缩放入选者** — 您现在可以自动或手动将实验的入选路径转给完整受众。 确定入选者后，您可以扩大其影响范围和增强其有效性，而无需持续监控试验。 [了解详情](../building-journeys/path-experimentation.md#scale-winner)

  此功能仅在单一历程（事件触发和受众资格）中可用。 它不适用于读取受众历程。

  发布日期： 2026年4月7日

* **条件** - [优化](../building-journeys/optimize.md)活动是在历程中创建条件路径的新工具。 它取代了以前的&#x200B;**条件**&#x200B;活动，该活动已从UI中删除。 所有条件逻辑都将保留，并且现在通过&#x200B;**优化**&#x200B;活动的条件进行处理。 [了解详情](../building-journeys/conditions.md)

  此功能此前为有限发布版，现已可供所有环境使用（正式发布版）。

  发布日期： 2026年4月7日

#### 编排的营销活动

* **协调的营销活动中的全局变量** — 协调的营销活动现在支持全局变量，这些变量可以定义一次，并在工作流内的所有活动中重复使用，从而简化配置并确保动态值、表达式和内容个性化的一致性。 [了解详情](../orchestrated/global-variables.md)
* **数据Modeler增强功能** — 编排的关系架构现在支持跨多个字段的组合键。 从DDL文件加载架构时还会引入明细列表，从DDL或Excel文件加载时会自动创建表之间的组合关系。 在实体关系视图中，复合链接现在会在文件上传后显示表之间的完整字段配对集。 [了解详情](../orchestrated/gs-schemas.md)

## 即将推出 {#coming-soon}

以下功能和增强功能计划在未来几天发布。 **信息可能会有所更改**。 这些更新在生产环境中启用后，将会共享更新的链接、屏幕和文档。

### 新功能 {#comming-soon-features}

<table>
<thead>
<tr>
<th><strong>历程模拟</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>您现在可以将历程设置为<strong>模拟</strong>。 此模式允许您使用<strong>模拟用户</strong>验证逻辑。 这些是专门为模拟创建的临时配置文件，允许您自由测试，而无需在Adobe Experience Platform中管理持续的测试配置文件。</p>
<p>此功能以有限可用性的形式提供给所有客户，并具有基本功能。</p>
<!--p><img src="assets/do-not-localize/simulate-user.gif"></p-->
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>电子邮件Designer中的深层链接</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>现在，可以通过电子邮件Designer中的专用选项向电子邮件内容添加深层链接。</p><p>这可确保用户直接访问正确的应用程序内内容，而不是重定向到浏览器或应用商店，从而保留上下文和参与度。</p>
<!--<p><img src="assets/do-not-localize/forms.gif"></p>-->
<p>有关更多信息，请参阅<a href="../email/message-tracking.md">详细文档</a>。</p>
<p>发布日期： 2026年5月7日</p>
</td>
</tr>
</tbody>
</table>

