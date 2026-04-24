---
solution: Journey Optimizer
product: journey optimizer
title: 发行说明
feature: Release Notes
role: User
level: Beginner, Intermediate
description: Adobe Journey Optimizer 发行说明
exl-id: 06fa956a-b500-416e-9d42-b683c328e837
source-git-commit: 7284814029465a8806b78640b8ffe6c44ad030a7
workflow-type: tm+mt
source-wordcount: '3902'
ht-degree: 17%

---

# 发行说明 {#release-notes}

>[!CONTEXTUALHELP]
>id="ajo_homepage_card1"
>title="新增功能"
>abstract="**Adobe Journey Optimizer** 不断地提供新功能、增强现有功能，并修复错误。 所有更改会在每月的最后一周整合到发行说明中。"

[!DNL Adobe Journey Optimizer]遵循持续交付模型，允许Adobe持续交付新功能、增强功能和修复。 此方法支持以可扩展的方式分阶段推出各种功能，以确保所有环境的性能和稳定性。

由于此模型，在每月发行版本之间会更新发行说明。 有关发行周期和可用性阶段的完整详细信息，请参阅 [Journey Optimizer 发行周期](releases.md)。

[!DNL Adobe Journey Optimizer] 原生构建于 [!DNL Adobe Experience Platform] 之上并继承了其所具备的最新创新技术和改进。 在 [Adobe Experience Platform 发行说明](https://experienceleague.adobe.com/docs/experience-platform/release-notes/latest.html?lang=zh-Hans){target="_blank"}中进一步了解这些更改。

## 2026年4月预发行说明 {#april-26-rn}

**以下预发行说明可能会在正式发行日期之前有所更改，恕不另行通知**。 链接、屏幕和更新的文档会于发布日期在发行说明中发布。

另请参阅 [Adobe Experience Platform 预发行说明](https://experienceleague.adobe.com/zh-hans/docs/experience-platform/release-notes/pre-release-notes){target="_blank"}。

将在4月早些时候发布的新功能和改进中公布其发布日期。

**发行日期**： 2026年4月28日至29日

### 新功能 {#april-26-features}

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
<p>此功能仅面向一部分组织（限量发布）。 要获得访问权限，请与 Adobe 代表联系。</p>
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
<p>此功能仅面向一部分组织（限量发布）。 要获得访问权限，请与 Adobe 代表联系。</p>
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
<p>现在，可以通过电子邮件Designer中的专用选项向电子邮件内容添加深层链接。 这可确保用户直接访问正确的应用程序内内容，而不是重定向到浏览器或应用商店，从而保留上下文和参与度。</p>
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
<p>Adobe Journey Optimizer现在提供了一个<strong>MCP（模型上下文协议）服务器</strong>，该服务器直接在任何MCP兼容的应用程序中呈现营销活动、忠诚度、渠道配置和沙盒操作。 通过这种集成，不同的角色可以围绕相同的编排数据进行协作。 您可以用对话方式描述您的意图，让LLM调用相应的MCP工具，而不是针对Adobe Journey Optimizer REST API编写查询或导航多个UI屏幕。 此功能当前在Claude Web和Desktop中可用。</p>
<p>此功能适用于公共Beta中的所有客户。</p>
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
<p>[!DNL Adobe Journey Optimizer] 现在在个性化编辑器中直接包含<strong>AI助手</strong>，该编辑器可将自然语言提示转换为有效的个性化表达式和条件逻辑，无需语法专业知识。 描述您要实现的个性化，AI会生成现成的代码，您可以立即应用，或通过后续提示进行优化。</p>
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

<!--
<table>
<thead>
<tr>
<th><strong>Optimize email text for AI inboxes</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Adobe Journey Optimizer now includes a new capability that ensures your emails are optimally structured for AI-powered inboxes such as Apple Intelligence and Google Gemini in Gmail.</p>
<p>As AI assistants increasingly control how recipients read and act on email, this feature helps you author content that performs well across downstream AI tasks including summarization, triage, prioritization, and intent extraction.</p>
<p><img src="assets/do-not-localize/text-optimizer.gif"></p>
<p>For more information, refer to <a href="../email/llm-email-optimizer.md">Optimize email text for AI inboxes</a>.</p>
<p>Availability date: April 3, 2026</p>
</td>
</tr>
</tbody>
</table>
-->

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

#### AI

* **Campaign仪表板中的品牌一致性分数** — 您现在可以直接在Campaign仪表板中评估您的品牌一致性分数，以确保内容保持品牌化。 这使您无需打开内容设计器即可一目了然地验证准则。

* **提示助理增强功能** — 当提示不明确、不完整或混合了多个目标时，**提示助理**&#x200B;现在可以提出重点明确的澄清问题，或在生成请求之前提供更明确的重写建议，从而帮助您在助理做出响应之前确定所需的内容，从而提高一致性并减少重试。 [了解详情](../content-management/ai-assistant-prompting-guide.md)

#### 决策

* **将片段附加到决策项** — 现在，Journey Optimizer提供将片段附加到决策项的功能，可在基于代码的体验和电子邮件营销活动中通过决策策略利用这些功能。 此功能此前为有限发布版，现已可供所有环境使用（正式发布版）。

* **跳过暂时不可用的片段** — 在决策项中使用片段时，如果Edge上暂时无法使用片段，则会跳过该片段，并且旅程或营销活动将继续渲染而不是失败。 [了解详情](../experience-decisioning/fragments-decision-policies.md#temporary-unavailable-fragments)

  发布日期： 2026年4月14日

#### 推送

* **在渠道设置中个性化应用程序ID** — 在“推送”渠道配置设置中，您现在可以个性化&#x200B;**应用程序ID**&#x200B;字段，以便每个收件人都可以根据其个人资料信息接收来自相应品牌的推送通知。

#### 短信

* **字符数** — 在Adobe Journey Optimizer中，您现在可以使用字符数实时监控SMS消息的长度。 它有助于您了解何时将消息拆分为多个区段，以便更好地管理格式并避免发送成本意外增加。 [了解详情](../sms/create-sms.md)

* **在电话号码和发件人处选择退出和同意** — 对于短信，Journey Optimizer现在会在用户档案的电话号码和短代码级别记录营销同意和选择退出。

  此功能当前仅适用于Sinch SMS配置。 [了解详情](../sms/sms-configuration-sinch.md)

* **SMS入站到自定义数据集** — 在&#x200B;**SMS API凭据**&#x200B;中，将&#x200B;**入站SMS**&#x200B;路由到您选择的启用了&#x200B;**个人资料的自定义体验事件数据集**，而不是仅路由默认跟踪数据集。 [了解详情](../sms/sms-webhook.md)

* **Webhook界面增强** — 在配置SMS Webhook时，用户界面现在包含带有实际示例的内置设置指南，使得在不离开配置流的情况下更容易对齐提供商有效负载和解决问题。 [了解详情](../sms/sms-webhook.md)

#### WhatsApp

* **WhatsApp交互按钮和跟踪** - Journey Optimizer中的WhatsApp现在支持您的模板和用例所需的交互按钮以及内置的交互跟踪，以便您可以测量参与度并分析性能，以及您的其他渠道报表。

#### Adobe Experience Manager集成

* **Adobe Experience Manager内容片段变体支持** — 在插入Adobe Experience Manager内容片段时，您可以选择&#x200B;**内容片段变体**（例如语言或渠道变体），从而改进区域设置和多语言方案的处理。 [了解详情](../integrations/aem-fragments.md#aem-variations)

  此功能仅面向一部分组织（限量发布）。 要获得访问权限，请与 Adobe 代表联系。

  发布日期：2026年4月3日

* **创作时Adobe Experience Manager内容片段上下文** — 在文本字段和内容块之间移动时，您的内容片段选择将保持活动状态，以便您可以添加更多片段字段而无需每次重新打开&#x200B;**打开AEM内容顾问**。 [了解详情](../integrations/aem-fragments.md)

  此功能仅面向一部分组织（限量发布）。 要获得访问权限，请与 Adobe 代表联系。

  发布日期：2026年4月1日

#### 配置

* **URL参数加密密钥的特定权限** — 为了访问和管理URL参数加密的密钥，已创建了新权限。 现在必须授予&#x200B;**查看密钥注册表**&#x200B;和&#x200B;**管理密钥注册表**&#x200B;权限。

#### 编排的营销活动

* **数据Modeler增强功能** — 编排的关系架构现在支持跨多个字段的组合键。 从DDL文件加载架构时还会引入明细列表，从DDL或Excel文件加载时会自动创建表之间的组合关系。 在实体关系视图中，复合链接现在会在文件上传后显示表之间的完整字段配对集。

* **协调的营销活动中的全局变量** — 协调的营销活动现在支持全局变量，这些变量可以定义一次，并在工作流内的所有活动中重复使用，从而简化配置并确保动态值、表达式和内容个性化的一致性。

#### 电子邮件设计

* **电子邮件内容的高级HTML编辑器** — 高级HTML模式允许您在Email Designer中编辑内容的HTML源，在源中添加高级表达式（如条件），并在HTML视图和桌面视图之间切换而不会丢失更改。

  以前此功能仅可用于电子邮件内容模板，现在此功能已部署到Email Designer中的&#x200B;**电子邮件**&#x200B;内容（例如，在历程和营销活动中创作的电子邮件）以及电子邮件内容模板。 它当前处于“有限可用”状态 — 请联系您的Adobe代表以获取访问权限。 [了解详情](../email/email-expert-mode.md)

  发布日期： 2026年4月9日

* 电子邮件Designer中个性化表达式的&#x200B;**AI助手** — 在电子邮件Designer中，选择一个组件并在上下文工具栏中使用&#x200B;**添加表达式**&#x200B;以纯语言描述所需的个性化设置，查看生成的表达式，并在不离开设计器的情况下插入该表达式。 [了解详情](../content-management/generative-personalization-expressions.md#generate-email-designer)

  发布日期： 2026年4月15日

#### 历程路径优化

* **试验类型** — 在配置路径试验时，您现在可以在A/B试验（开始时固定拆分）或多臂赌博机（自动拆分并每周更新权重）之间进行选择。 [了解详情](../building-journeys/path-experimentation.md)

  发布日期： 2026年4月7日

* **路径实验：缩放入选者** — 您现在可以自动或手动将实验的入选路径转给完整受众。 确定入选者后，您可以扩大其影响范围和增强其有效性，而无需持续监控试验。 [了解详情](../building-journeys/path-experimentation.md#scale-winner)

  此功能仅在单一历程（事件触发和受众资格）中可用。 它不适用于读取受众历程。

  发布日期： 2026年4月7日

* **条件** - [优化](../building-journeys/optimize.md)活动是在历程中创建条件路径的新工具。 它取代了以前的&#x200B;**条件**&#x200B;活动，该活动已从UI中删除。 所有条件逻辑都将保留，并且现在通过&#x200B;**优化**&#x200B;活动的条件进行处理。 [了解详情](../building-journeys/conditions.md)

  此功能此前为有限发布版，现已可供所有环境使用（正式发布版）。

  发布日期： 2026年4月7日


## 2026年3月发行说明 {#march-26-rn}

[新功能](#march-26-features)和[改进](#march-26-improv)部分涵盖的功能已经可用。<!--The [Coming soon](#coming-soon) section lists features and improvements scheduled for release later in March.-->

<!--
**The pre-release notes below are subject to change without prior notice until the release availability date**. Links, screens and updated documentation are published in the release notes, at the release date.

See also [Adobe Experience Platform pre-release notes](https://experienceleague.adobe.com/zh-hans/docs/experience-platform/release-notes/pre-release-notes){target="_blank"}.
-->

**发行日期**： 2026年3月24日至25日

### 新功能 {#march-26-features}

<table>
<thead>
<tr>
<th><strong>URL参数加密</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>现在，可以加密添加到电子邮件中的跟踪和登陆页面链接中的URL参数，从而为敏感参数数据提供额外的安全层。</p>
<ul>
<li>在专用<strong>管理</strong>注册表中注册和管理加密密钥。</li>
<li>在表达式中使用新的“Encrypt”帮助程序函数加密URL中要在渲染时保护的查询参数的敏感数据。</li>
</ul>
<p>此功能仅面向一部分组织（限量发布）。 要获得访问权限，请与 Adobe 代表联系。</p>
<p><img src="assets/do-not-localize/encrypt-helper.gif"></p>
<p>有关更多信息，请参阅<a href="../personalization/url-parameter-encryption.md">详细文档</a>。</p>
<p>发布日期：2026年3月31日</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>将图像转换为电子邮件内容模板</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>您现在可以直接在Journey Optimizer中将图像转换为电子邮件内容模板。 使用AI支持的分析，从可视化引用自动生成结构化HTML模板，显着缩短电子邮件设计时间。</p>
<p>此功能此前为有限发布版，现已可供所有环境使用（正式发布版）。</p>
<p><img src="assets/do-not-localize/image-converter.gif"></p>
<p>有关更多信息，请参阅<a href="../content-management/image-to-html.md">详细文档</a>。</p>
<p>发布日期：2026年3月31日</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>登陆页面自定义表单</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>使用[!DNL Journey Optimizer]，您可以通过登陆页面捕获配置文件属性。</p>
<p>根据特定的数据集，创建、设计和管理适合您需求的自定义表单。 然后，您可以在登陆页面中利用这些表单，将您选择的轮廓属性添加到为每个表单定义的数据集中。</p>
<p>此功能以前以“有限可用”的形式面向美国和澳大利亚的客户发布，现在则对所有环境均可用（一般可用）。</p>
<p><img src="assets/do-not-localize/forms.gif"/></p>
<p>有关更多信息，请参阅<a href="../landing-pages/lp-forms.md">详细文档</a>。</p>
<p>发布日期：2026年3月26日。</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>在编排的营销活动中测试活动</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>新的<strong>Test</strong>活动现在可在编排的营销活动中使用。 此活动根据定义的条件将工作流执行路由到不同的分支，让您能够在激活实时投放之前验证活动逻辑和配置。</p>
<p><img src="../orchestrated/assets/test-1.png"></p>
<p>有关更多信息，请参阅<a href="../orchestrated/activities/test.md">详细文档</a>。</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>历程中的数据集查找支持</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>历程中新增的<strong>数据集查找</strong>活动允许您在运行时动态检索Adobe Experience Platform记录数据集中的数据 — 让您能够访问不属于配置文件或事件有效负载的信息，因此客户交互始终相关且及时。</p>
<p>以前以“有限可用性”发布给一组有限组织，现在历程中的数据集查找活动可供所有有权使用[数据集查找](../data/lookup-aep-data.md)的客户使用，同时仍保持有限可用性。</p>
<p><img src="../building-journeys/assets/aep-data-activity.png"></p>
<p>有关更多信息，请参阅<a href="../building-journeys/dataset-lookup.md">详细文档</a>。</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>操作活动取代了特定于渠道的历程活动</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>在2026年2月<strong>操作活动</strong>正式发布后，历程画布中的旧版本机渠道活动（电子邮件、推送、短信、应用程序内、Web、基于代码的体验和内容卡）现已弃用。</p>
<p>现在，您必须使用单个操作活动来配置所有渠道操作，而无需单独的特定于渠道的节点。</p>
<p>使用旧版渠道活动的现有历程可以继续正常运行，无需进行任何更改或迁移。</p>
<p><img src="assets/do-not-localize/action-activity.gif"></p>
<p>有关更多信息，请参阅<a href="../building-journeys/journey-action.md">详细文档</a>。</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>电子邮件模板的高级HTML编辑器</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>电子邮件内容模板的高级HTML模式允许您在Email Designer中编辑内容的HTML源，在源中添加高级表达式（如条件），并在HTML视图和桌面视图之间切换，而不会丢失所做的更改。</p>
<p>此功能仅在电子邮件渠道的内容模板中可用。 它当前处于“有限可用”状态 — 请联系您的Adobe代表以获取访问权限。</p>
<p><img src="assets/do-not-localize/expert-mode.gif"/></p>
<p>有关更多信息，请参阅<a href="../email/email-expert-mode.md">详细文档</a>。</p>
<p>发布日期： 2026年3月10日</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>自定义Firefly模型与第三方图像生成模型的集成</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>启用标准和自定义 Firefly 模型以及经过批准的第三方图像模型的无缝集成，从而在生成图像时提供更大的灵活性、控制力以及品牌一致性。</p>
<p>根据您的需求选择合适的模型：</p>
<ul><li> <strong>Adobe模型</strong>（由Firefly Image Model 4提供支持），无需其他设置即可立即生成图像</li><li> <strong>合作伙伴型号</strong> （由Gemini 2.5 Flash提供支持）提供专业功能</li><li><strong>自定义模型</strong>（基于您自己的资产进行培训的品牌特定模型），用于生成与您的品牌标识、风格和视觉准则完全一致的品牌。</li></ul>
<p>有关更多信息，请参阅<a href="../content-management/generative-models.md">详细文档</a>。</p>
<p>发布日期：2026年3月2日</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>iOS的实时活动</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>通过Adobe Journey Optimizer中的<strong>iOS Live Activity</strong>，将实时体验直接引入客户的Lock Screens和Dynamic Island。 交付实时更新，从订单跟踪和航班状态到事件倒计时、实时得分和交付进度，而不要求用户打开您的应用程序。 让您的受众了解情况，并在正确的时间参与活动，即他们所在的位置。</p>
<p>此功能以前以测试版的形式发布，但现在向所有环境提供（正式发布）。</p>
<p>有关更多信息，请参阅<a href="../mobile-live/get-started-mobile-live.md">详细文档</a>。</p>
<p>发布日期：2026年3月3日</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Journey Agent：渠道内容创建</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>由<strong>Adobe Experience Platform Agent Orchestrator</strong>提供支持的<strong>Journey Agent</strong>在Journey Optimizer中可用，并允许您通过自然语言界面分析旅程。 您现在还可以直接在Journey Agent中生成和管理特定于渠道的内容，为电子邮件和推送等渠道创建内容，应用和预览模板，通过提示优化音调和样式，以及在<strong>内容Designer</strong>中打开内容以进行上下文内编辑。</p>
<p>此功能仅面向一部分组织（限量发布）。 要获得访问权限，请与 Adobe 代表联系。</p>
<p>有关更多信息，请参阅<a href="https://experienceleague.adobe.com/docs/experience-cloud-ai/experience-cloud-ai/agents/ajo-agent.html?lang=zh-Hans" target="_blank">详细文档</a>。</p>
<p>发布日期：2026年3月4日</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>AI模型监测</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Journey Optimizer现在允许您监控Decisioning AI模型的运行状况、培训状态和性能。 这使您可以验证培训是否成功、排除故障以及了解对结果的影响，以便使用AI为每个客户选择最佳选件。 请注意，此功能仅适用于<strong>决策</strong>（不适用于旧版决策管理模型）。</p>
<p>此功能当前仅适用于<strong>个性化优化</strong>模型（非自动优化）。</p>
<p><img src="assets/do-not-localize/ai-model-observability.gif"/></p>
<p>有关更多信息，请参阅<a href="../experience-decisioning/ranking/ai-model-observability.md">详细文档</a>。</p>
<p>发布日期： 2026年3月9日</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>使用信号触发编排的营销活动</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>现在可以通过<strong>API信号</strong>触发编排的营销活动。 若要进行此设置，请将目标营销活动配置为<strong>由信号</strong>触发，发布该营销活动，然后使用API调用触发它。 API调用中包含的任何参数均可用作正在运行的营销活动中的变量。 请注意，信号触发的编排营销活动仍是<strong>批次</strong>营销活动，不同于API触发的营销活动。</p>
<p><img src="assets/do-not-localize/oc-triggered.gif"></p>
<p>有关更多信息，请参阅<a href="../orchestrated/trigger-orchestrated-campaign.md">详细文档</a>。</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>编排的活动中的事务性类别</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>在编排的营销活动中，您现在可以将渠道活动设置为<strong>事务性</strong>类别。 这会将事务性渠道配置应用于该活动，并在业务规则不应应用或不需要客户选择加入时非常有用。</p>
<p><img src="assets/do-not-localize/oc-transactional.gif"></p>
<p>有关更多信息，请参阅<a href="../orchestrated/activities/channels.md#add">详细文档</a>。</p>
<p>此功能将在未来几天内逐步推广到所有地区。</p>
</td>
</tr>
</tbody>
</table>

### 改进 {#march-26-improv}

此版本包含的改进如下所述。

#### 个性化

* **完整/基本URL个性化** — 您可以使用配置文件属性（例如，针对域或路径）个性化目标URL。 要启用此功能，请向Adobe提供您的接受域列表。 [了解详情](../personalization/personalization-build-expressions.md#where)

  此功能以前以“有限可用性”发布，以供在历程中使用，但现在对所有环境可用（一般可用性）。

  发布日期：2026年4月1日

#### 报告

* **发送时间优化：更新了控件位置和新的提升报告** — 发送时间优化(STO)控件已重新定位到操作配置菜单。 此外，历程报表中现在提供了新的提升报表，以衡量STO对促销活动绩效指标的影响。 [了解详情](../reports/channel-report-cja.md#optimization-models)

  发布日期： 2026年3月27日

<!--
* **Exclude bot clicks for email and SMS reporting** - Email and SMS reporting now automatically filters out bot clicks from click metrics, providing more accurate engagement data and preventing automated traffic from inflating your performance figures.

#### Email Designer

* **Email Designer displayed in Unified Shell** - The Email Designer is now displayed within the Unified Shell experience, providing a consistent navigation and header experience that aligns with other Adobe applications.

* **Text mode support in fragments** - To support text-based email workflows, you can now create and manage text versions of your visual fragments for optimal use in the plain text version of emails that include that fragment.

  **Caution:** When using a fragment that was created before the current release, the fragment text version may be incorrectly rendered—both in the Email Designer and in the final email delivered to your recipients. For best results with older fragments, edit, save and republish each fragment.
-->

#### 配置

<!--* **Folders for journeys and campaigns** - You can now organize your journeys and campaigns into folders, enabling structured navigation and easier management for teams working with large volumes of content. This capability is only available for a set of organizations (Limited Availability). To gain access, contact your Adobe representative.-->

* **AJO域证书续订失败** — 现在，当用于电子邮件传递的域证书即将到期或已过期时，您可以通过电子邮件或在Journey Optimizer通知中心订阅接收系统警报。 [了解详情](../reports/alerts.md#alert-certificates-renewal-unsuccessful)

  发布日期： 2026年3月26日

* **AJO次要收件人反馈事件数据集重命名** - `AJO Email BCC Feedback Event`数据集已重命名为`AJO Secondary Recipient Feedback Event`数据集。 具体影响取决于您的情况：

   * **现有用户**：只更新显示名称。 基础表名称保持不变。
   * **新用户和沙盒**：显示名称和表名称都反映新名称。
   * **具有新沙盒的现有用户**：显示名称和表名称都已更新为新名称。

  >[!NOTE]
  >
  >新数据集立即显示新名称。 对于较旧的数据集名称，回填和对帐会逐步进行，并且可能需要几周才能完成。

  发布日期：2026年3月2日


#### 历程

* **更新配置文件操作：支持多个配置文件属性** - **更新配置文件**&#x200B;操作活动现在支持在单个节点中更新最多五个配置文件属性。 以前，每个操作一次只能更新一个属性，需要多个节点更新多个属性。 使用新的&#x200B;**更新其他字段**&#x200B;按钮添加其他字段/值对，从而降低画布复杂性并提高性能。 [了解详情](../building-journeys/update-profiles.md)

* **历程中的出站消息波动发送** — 您现在可以计划来自Journey Optimizer历程的消息，以受控批次形式随时间传递。 [了解详情](../building-journeys/send-using-waves.md)

  此功能以前以“有限可用性”发布，以供在历程中使用，但现在对所有环境可用（一般可用性）。

  发布日期： 2026年3月16日

* **历程技术详细信息中的暂停和恢复详细信息** — 历程&#x200B;**技术详细信息**&#x200B;现在包含其他暂停和恢复信息：上次暂停和恢复的日期和时间、执行每个操作的用户的显示名称和内部标识符以及暂停行为、最长暂停持续时间和自动恢复状态等整套暂停历程设置。 [了解详情](../building-journeys/journey-properties.md)

  发布日期：2026年3月2日

#### 决策

* **决策迁移 — 选件和上下文属性** — 迁移API实体映射现在列出了&#x200B;**选件属性** （`migratedofferattributes`个性化选件项架构）和&#x200B;**上下文属性** （`migratedcontextattributes`迁移数据集架构）。 [了解详情](../experience-decisioning/decisioning-migration-api.md#entity-mapping)

  发布日期：2026年3月31日

<!--
## Coming soon {#coming-soon}

The features and improvements below are planned for release later in March/early April. Release dates and scope are **subject to change without prior notice**.


WAITING RELEASE DATE CONFIRMATION * **Target dimension simplification in Orchestrated Campaigns** - The active targeting dimension is now shown on the workflow canvas, so you can see which dimension is used by a channel activity. The multi-entity segmentation flow is simpler as you no longer need a separate "Change dimension" activity. Moreover, you can now choose explicitly whether messages are sent at the profile level or at a secondary dimension level.


WAITING RELEASE DATE CONFIRMATION
* **Target dimension simplification in Orchestrated Campaigns** - The active targeting dimension is now shown on the workflow canvas, so you can see which dimension is used by a channel activity. The multi-entity segmentation flow is simpler as you no longer need a separate "Change dimension" activity. Moreover, you can now choose explicitly whether messages are sent at the profile level or at a secondary dimension level.
-->
