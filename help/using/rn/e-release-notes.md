---
solution: Journey Optimizer
product: journey optimizer
title: Journey Optimizer 的预发行说明
description: Adobe Journey Optimizer 预发行说明
feature: Release Notes
hide: true
exl-id: 6e7d1300-8efd-4fdc-90e3-3ccdc3babd2f
source-git-commit: fe8e38287939e289e04e07dfe5a2ca51172825e6
workflow-type: tm+mt
source-wordcount: '1698'
ht-degree: 15%

---

# 预发行说明 {#e-release-notes}

Adobe Journey Optimizer不断提供新功能、现有功能的增强以及错误修复。 所有更改会在每月末整合到[发行说明](release-notes.md)中。

## 2026年4月预发行说明 {#april-26-rn}

**以下预发行说明可能会在正式发行日期之前有所更改，恕不另行通知**。链接、屏幕和更新的文档会于发布日期在发行说明中发布。

另请参阅 [Adobe Experience Platform 预发行说明](https://experienceleague.adobe.com/zh-hans/docs/experience-platform/release-notes/pre-release-notes){target="_blank"}。

**发布日期**：2026 年 4 月 28-29 日

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
<p>文档JIRA任务：<a href="https://jira.corp.adobe.com/browse/DOCAC-14050">DOCAC-14050</a></p>
</td>
</tr>
</tbody>
</table>


<table>
<thead>
<tr>
<th><strong>电子邮件动态发件人</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>借助<strong>动态发件人</strong>功能，您现在可以发送发送实体（发件人）与创作实体（发件人）不同的电子邮件。 支持此功能的电子邮件客户端通常将其呈现为“代表发件人的发件人”或显示“通过”指示符。</p>
<p>此功能仅面向一部分组织（限量发布）。要获得访问权限，请与 Adobe 代表联系。</p>
<p>文档JIRA任务：<a href="https://jira.corp.adobe.com/browse/DOCAC-14458">DOCAC-14458</a></p>
</td>
</tr>
</tbody>
</table>


<table>
<thead>
<tr>
<th><strong>历程和营销活动文件夹</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>您现在可以将历程和营销活动组织到<strong>文件夹</strong>中，以改进界面中的导航和管理。</p>
<p>此功能仅面向一部分组织（限量发布）。要获得访问权限，请与 Adobe 代表联系。</p>
<p>文档JIRA任务：<a href="https://jira.corp.adobe.com/browse/DOCAC-14038">DOCAC-14038</a></p>
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
<p>Adobe Journey Optimizer现在提供了一个<strong>MCP（模型上下文协议）服务器</strong>，该服务器直接在任何MCP兼容的应用程序中呈现营销活动、忠诚度和沙盒操作。 通过这种集成，不同的角色可以围绕相同的编排数据进行协作。 您可以用对话方式描述您的意图，让LLM调用相应的MCP工具，而不是针对AJO REST API编写查询或导航多个UI屏幕。 此功能当前在Claude Web和Desktop中可用。</p>
<p>此功能适用于公共Beta中的所有客户。</p>
<p>文档JIRA任务：<a href="https://jira.corp.adobe.com/browse/DOCAC-14509">DOCAC-14509</a></p>
</td>
</tr>
</tbody>
</table>


<table>
<thead>
<tr>
<th><strong>编排的活动的沙盒副本</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p><strong>沙盒工具</strong>现在支持通过包在沙盒之间导出和导入<strong>协调的营销活动</strong>。</p>
<p>文档JIRA任务：<a href="https://jira.corp.adobe.com/browse/DOCAC-13760">DOCAC-13760</a></p>
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
<p><strong>增量查询</strong>活动现在可在<strong>协调的营销活动</strong>中使用。 每次运行营销活动时，此定位活动都会运行您的查询，并且只返回上次运行中未返回的记录。 您可以只发送消息或导出新注册、新金会员或其他“自上次运行以来新增的”区段，而无需重新定向相同的配置文件。</p>
<p>文档JIRA任务：<a href="https://jira.corp.adobe.com/browse/DOCAC-14262">DOCAC-14262</a></p>
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
<p>您现在可以在<strong>排名公式</strong>中使用<strong>AI模型</strong>根据客户个人资料属性和上下文因素自动提升<strong>历程优先级分数</strong>，确保客户进入最相关的历程。</p>
<p>此功能仅面向一部分组织（限量发布）。要获得访问权限，请与 Adobe 代表联系。</p>
<p>文档JIRA任务：<a href="https://jira.corp.adobe.com/browse/DOCAC-14295">DOCAC-14295</a></p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>针对AI收件箱优化电子邮件：更新后的工作流</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Adobe Journey Optimizer现在包含一项新功能，可确保您的电子邮件针对<strong>AI支持的收件箱</strong>（如Gmail中的<strong>Apple Intelligence</strong>和<strong>Google Gemini</strong>）进行最佳结构化。 随着AI助理越来越多地控制收件人如何阅读电子邮件并在电子邮件中执行操作，此功能可帮助您创作在下游AI任务中表现良好的内容，这些任务包括摘要、分类、优先级划分和意图提取。</p>
<p>文档JIRA任务：<a href="https://jira.corp.adobe.com/browse/DOCAC-14520">DOCAC-14520</a></p>
</td>
</tr>
</tbody>
</table>

<!--
<table>
<thead>
<tr>
<th><strong>Journey fragments</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p><strong>Journey fragments</strong> are reusable sets of journey nodes that you can build once and drop into any journey across your sandbox. Whether it's an eligibility check, a preferred channel routing logic, or a welcome sequence, fragments help teams move faster and stay consistent — without rebuilding the same logic from scratch every time. Once created, fragments are stored in a dedicated <strong>Fragment inventory</strong> and can be inserted into any journey using the <strong>Journey fragments</strong> activity.</p>
<p>This capability is only available for a set of organizations (Limited Availability). To gain access, contact your Adobe representative.</p>
<p>Documentation JIRA task: <a href="https://jira.corp.adobe.com/browse/DOCAC-11529">DOCAC-11529</a></p>
<p>Availability date: May 4, 2026</p>
</td>
</tr>
</tbody>
</table>
-->

<table>
<thead>
<tr>
<th><strong>适用于Personalization表达式的AI助手</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Adobe Journey Optimizer现在包含一个用于个性化表达式的AI助手。 在设计电子邮件内容时，您可以从Personalization编辑器和电子邮件Designer工具栏中打开它。 用简单的语言描述要个性化的内容，然后助手会生成个性化表达式，您可以按原样使用，也可以在后续的简短对话中对其进行优化。
您还可以选择现有的个性化代码，并请求助理对其进行解释、修复或提出改进建议。 生成表达式后，“显示样本配置文件预览”会针对一组有限的合成样本配置文件运行快速检查。</p>
<p>有关详细信息，请参阅<a href="../content-management/generative-personalization-expressions.md">Personalization表达式的AI助手</a>。</p>
<p>发布日期： 2026年4月13日</p>
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
<p><strong>收件箱</strong>是一项移动功能，随<strong>内容卡</strong>提供，它允许客户在其应用程序或网站中创建一个集中的位置，以显示发送给用户的消息。 这延长了营销通信的生命周期，确保消息在关闭后仍可访问。</p>
<p>有关更多信息，请参阅<a href="../inbox/inbox-gs.md">详细文档</a>。</p>
<p>发布日期： 2026年4月7日</p>
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
<p>使用新的<strong>优化</strong>节点运行<strong>A/B测试</strong>或<strong>多臂老虎机</strong>实验，以确定满足以业务为中心的KPI的最佳途径。 此工具允许您测试并更改通信、顺序和时间，以便最好地触及客户。 此功能此前为有限发布版，现已可供所有环境使用（正式发布版）。</p>
<p>有关更多信息，请参阅<a href="../building-journeys/path-experimentation.md">详细文档</a>。</p>
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
<p>您现在可以使用<strong>Decisioning</strong>来个性化和优化电子邮件的内容。 利用<strong>优先级分数</strong>、<strong>公式</strong>或<strong>AI模型</strong>向每个收件人显示最相关的优惠和内容。 此功能以前以“有限可用性”发布，现在可用于所有环境（一般可用性）。 在此General Availability版本中，现在支持<strong>镜像页面</strong>。</p>
<p>有关更多信息，请参阅<a href="../experience-decisioning/create-decision-policy.md">详细文档</a>。</p>
<p>发布日期： 2026年4月6日</p>
</td>
</tr>
</tbody>
</table>

### 改进 {#april-26-improv}

此版本包含的改进如下所述。

#### AI

* **Campaign仪表板中的品牌一致性分数** — 您现在可以直接在Campaign仪表板中评估您的品牌一致性分数，以确保内容保持品牌化。 这使您无需打开内容设计器即可一目了然地验证准则。

  文档JIRA任务：[DOCAC-14516](https://jira.corp.adobe.com/browse/DOCAC-14516)

#### 决策

* **将片段附加到决策项** — 现在，Journey Optimizer提供将片段附加到决策项的功能，可在基于代码的体验和电子邮件营销活动中通过决策策略利用这些功能。 此功能此前为有限发布版，现已可供所有环境使用（正式发布版）。

  文档JIRA任务：[DOCAC-14452](https://jira.corp.adobe.com/browse/DOCAC-14452)

* **跳过暂时不可用的片段** — 在决策项中使用片段时，如果Edge上暂时无法使用片段，则会跳过该片段，并且旅程或营销活动将继续渲染而不是失败。 [了解详情](../experience-decisioning/fragments-decision-policies.md#temporary-unavailable-fragments)

  发布日期： 2026年4月14日

#### 电子邮件设计

* **电子邮件内容的高级HTML编辑器** — 高级HTML模式允许您在Email Designer中编辑内容的HTML源，在源中添加高级表达式（如条件），并在HTML视图和桌面视图之间切换而不会丢失更改。 以前此功能仅可用于电子邮件内容模板，但现在此功能已部署到Email Designer中的&#x200B;**电子邮件**&#x200B;内容。 它当前处于“有限可用”状态 — 请联系您的Adobe代表以获取访问权限。 [了解详情](../email/email-expert-mode.md)

  发布日期： 2026年4月9日

#### 历程路径优化

* **试验类型** — 在配置路径试验时，您现在可以在A/B试验（开始时固定拆分）或多臂赌博机（自动拆分并每周更新权重）之间进行选择。 [了解详情](../building-journeys/path-experimentation.md)

  发布日期： 2026年4月7日

* **路径实验：缩放入选者** — 您现在可以自动或手动将实验的入选路径转给完整受众。 确定入选者后，您可以扩大其影响范围和增强其有效性，而无需持续监控试验。 此功能仅在单一历程（事件触发和受众资格）中可用。 [了解详情](../building-journeys/path-experimentation.md#scale-winner)

  发布日期： 2026年4月7日

* **条件** - [优化](../building-journeys/optimize.md)活动是在历程中创建条件路径的新工具。 它取代了以前的&#x200B;**条件**&#x200B;活动。 所有条件逻辑都将保留，并且现在通过&#x200B;**优化**&#x200B;活动的条件进行处理。 此功能以前以“有限可用性”发布，现在可用于所有环境（一般可用性）。 [了解详情](../building-journeys/conditions.md)

  发布日期： 2026年4月7日

#### Adobe Experience Manager集成

* **内容顾问选择器** -AEM Assets和内容片段选择器现在已被&#x200B;**内容顾问选择器**&#x200B;替换，这是一个统一的模式窗口，允许您浏览、搜索、筛选和访问所有AEM Assets和AEM内容片段。 还包括Dynamic Media演绎版支持，允许您在选择Dynamic Media资产时从UI添加图像演绎版。 此功能此前为有限发布版，现已可供所有环境使用（正式发布版）。

  文档JIRA任务：[DOCAC-13802](https://jira.corp.adobe.com/browse/DOCAC-13802)

* **使用Dynamic Media的带倒计时器的开放时间个性化** - Journey Optimizer和Adobe Experience Manager Dynamic Media集成允许对Dynamic Media模板进行开放时间个性化，解锁超个性化用例。 客户可以在Adobe Experience Manager中创建和发布个性化模板，并在Journey Optimizer中使用这些模板，并在打开时呈现数据。

  文档JIRA任务：[DOCAC-13801](https://jira.corp.adobe.com/browse/DOCAC-13801)

* **Adobe Experience Manager内容片段变体支持** — 在插入Adobe Experience Manager内容片段时，您可以选择&#x200B;**内容片段变体**（例如语言或渠道变体），从而改进区域设置和多语言方案的处理。 此功能仅面向一部分组织（限量发布）。要获得访问权限，请与 Adobe 代表联系。[了解详情](../integrations/aem-fragments.md#aem-variations)

  发布日期：2026年4月3日

* **创作时Adobe Experience Manager内容片段上下文** — 在文本字段和内容块之间移动时，您的内容片段选择将保持活动状态，以便您可以添加更多片段字段而无需每次重新打开&#x200B;**打开AEM内容顾问**。 此功能仅面向一部分组织（限量发布）。要获得访问权限，请与 Adobe 代表联系。[了解详情](../integrations/aem-fragments.md)

  发布日期：2026年4月1日

#### WhatsApp

* **WhatsApp渠道：嵌入式注册** - Adobe Journey Optimizer现在支持Meta的<strong>嵌入式注册</strong>流程进行WhatsApp渠道配置。 这种简化的入门体验允许您直接在AJO界面中连接<strong>WhatsApp商业帐户</strong>和电话号码，而无需导航到<strong>Meta Business Manager</strong>，从而显着缩短设置时间。 它还可用作迁移工具，将现有电话号码和<strong>WhatsApp商业帐户(WABA)</strong>转移到Adobe。

  文档JIRA任务：[DOCAC-13386](https://jira.corp.adobe.com/browse/DOCAC-13386)

#### 配置

* **URL参数加密密钥的特定权限** — 为了访问和管理URL参数加密的密钥，已创建了新权限。 现在必须授予&#x200B;**查看密钥注册表**&#x200B;和&#x200B;**管理密钥注册表**&#x200B;权限。

  文档JIRA任务：[DOCAC-14490](https://jira.corp.adobe.com/browse/DOCAC-14490)

#### 编排的营销活动

<!--* **Data Modeler enhancements** - The Data Modeler in Orchestrated Campaigns now supports enhanced <strong>composite relationship management</strong>. You can create and manage composite relationships directly in the UI, including linking a field to multiple tables of the same type. These enhancements build on the <strong>composite key</strong> and <strong>enumeration management</strong> capabilities introduced in the previous release.Documentation JIRA task: [DOCAC-14334](https://jira.corp.adobe.com/browse/DOCAC-14334)-->

* **协调的营销活动中的全局变量** — 协调的营销活动现在支持全局变量，这些变量可以定义一次，并在工作流内的所有活动中重复使用，从而简化配置并确保动态值、表达式和内容个性化的一致性。

  文档JIRA任务：[DOCAC-14113](https://jira.corp.adobe.com/browse/DOCAC-14113)

<!--
## March '26 pre-release notes {#march-26-rn}

**The pre-release notes below are subject to change without prior notice until the release availability date**. Links, screens and updated documentation are published in the release notes, at the release date.

See also [Adobe Experience Platform Pre-release notes](https://experienceleague.adobe.com/zh-hans/docs/experience-platform/release-notes/pre-release-notes){target="_blank"}.

**Release date**: March 24-25, 2026

### New capabilities {#march-26-features}

<table>
<thead>
<tr>
<th><strong>LLM email optimizer</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>You can now optimize your email content for deliverability using large language model (LLM) technology. The LLM email optimizer analyzes your email content and provides actionable recommendations to improve sender reputation, avoid spam filters, and enhance overall deliverability performance.</p>
<p>Documentation JIRA task: <a href="https://jira.corp.adobe.com/browse/DOCAC-14340">DOCAC-14340</a></p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Convert images to email content templates</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>You can now convert images into email content templates directly in Journey Optimizer. Use AI-powered analysis to automatically generate structured HTML templates from visual references, significantly reducing email design time.</p>
<p>Previously released in Limited Availability, this capability is now available to all environments (General Availability).</p>
<p>Documentation JIRA task: <a href="https://jira.corp.adobe.com/browse/DOCAC-14324">DOCAC-14324</a></p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Incremental query activity in Orchestrated Campaigns</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>A new <strong>Incremental query</strong> activity is now available in Orchestrated Campaigns. This activity queries only new or updated records since the last workflow execution, significantly reducing processing time and improving efficiency for recurring campaigns targeting large datasets.</p>
<p>Documentation JIRA task: <a href="https://jira.corp.adobe.com/browse/DOCAC-14262">DOCAC-14262</a></p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Transactional category in Orchestrated campaigns</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>In Orchestrated campaigns, you can now set a channel activity to the <strong>Transactional</strong> category using the <strong>Category</strong> field. This applies transactional channel configurations to that activity and bypasses business rules for it.</p>
<p>Documentation JIRA task: <a href="https://jira.corp.adobe.com/browse/DOCAC-14233">DOCAC-14233</a></p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Test activity in Orchestrated Campaigns</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>A new <strong>Test</strong> activity is now available in Orchestrated Campaigns. This activity routes workflow execution to different branches based on defined conditions, enabling you to validate campaign logic and configurations before activating live deliveries.</p>
<p>Documentation JIRA task: <a href="https://jira.corp.adobe.com/browse/DOCAC-14115">DOCAC-14115</a></p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Custom forms in landing pages</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>You can now create <strong>custom forms</strong> in landing pages to collect specific subscriber data beyond standard opt-in fields. Define your own form fields, validation rules, and submission behaviors to support a wider range of subscription and profile enrichment use cases.</p>
<p>Previously released in Limited Availability, this capability is now available to all environments (General Availability).</p>
<p>Documentation JIRA task: <a href="https://jira.corp.adobe.com/browse/DOCAC-13963">DOCAC-13963</a></p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Journey Agent: Create Orchestrated Campaign use case</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p><strong>Journey Agent</strong>, powered by Adobe Experience Platform Agent Orchestrator, can now create complete <strong>Orchestrated Campaign</strong> use cases through a natural language interface. Describe your campaign goal and requirements in plain language, and Journey Agent configures the campaign structure, activities, and targeting for you.</p>
<p>Documentation JIRA task: <a href="https://jira.corp.adobe.com/browse/DOCAC-13768">DOCAC-13768</a></p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>New profile acquisition in landing pages</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Landing pages now support <strong>new profile acquisition</strong> workflows, enabling you to capture and onboard new audience members directly from your landing page experiences. Configure acquisition forms to collect profile data and automatically provision new profiles in Adobe Experience Platform.</p>
<p>Documentation JIRA task: <a href="https://jira.corp.adobe.com/browse/DOCAC-13757">DOCAC-13757</a></p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Journey path optimization</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p><strong>Journey path optimization</strong> uses AI to analyze historical journey performance and automatically select the best path for each customer, maximizing conversion and engagement outcomes.</p>
<p>Previously released in Limited Availability, this capability is now available to all environments (General Availability).</p>
<p>Documentation JIRA task: <a href="https://jira.corp.adobe.com/browse/DOCAC-13492">DOCAC-13492</a></p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Decisioning support in email channel</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>You can now use <strong>Decisioning</strong> to personalize and optimize the content of your email messages. Leverage Priority Scores, Formulas, or AI Models to display the most relevant offers and content to each recipient.</p>
<p>Previously released in Limited Availability, this capability is now available to all environments (General Availability). With this General Availability release, mirror pages are now supported.</p>
<p>Documentation JIRA task: <a href="https://jira.corp.adobe.com/browse/DOCAC-13182">DOCAC-13182</a></p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Message inbox</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>A new <strong>Message Inbox</strong> is now available in Adobe Journey Optimizer, providing a centralized view of received in-app, push, and SMS messages. Recipients can access and interact with all their messages in one place, enabling richer engagement and re-engagement scenarios.</p>
<p>Documentation JIRA task: <a href="https://jira.corp.adobe.com/browse/DOCAC-11382">DOCAC-11382</a></p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Native channel action activities deprecated</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Following the General Availability of the <strong>Action activity</strong> in February 2026, legacy native channel action activities (Email, SMS, Push, In-App, etc.) in the journey canvas are now deprecated. Existing journeys using legacy channel activities continue to function without any changes or migration required.</p>
<p>Documentation JIRA task: <a href="https://jira.corp.adobe.com/browse/DOCAC-14144">DOCAC-14144</a></p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Dataset lookup support in journeys</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>A new activity in journeys, Dataset lookup, allows you to to dynamically retrieve data from Adobe Experience Platform record datasets during runtime. By leveraging this capability, you can access data that may not reside in the profile or event payload, ensuring your customer interactions are both relevant and timely. Previously released in Limited Availability, this capability is now available to all environments (General Availability).</p>
<p>Documentation JIRA task: <a href="https://jira.corp.adobe.com/browse/DOCAC-14351">DOCAC-14351</a></p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Trigger orchestrated campaigns using API</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>You can now trigger an orchestrated campaign via API. Configure the target campaign as "Triggered by a signal" and publish it. Then use an API call to fire the campaign. The API call can include parameters that will be available as variables in the triggered campaign.</p>
<p>Documentation JIRA task: <a href="https://jira.corp.adobe.com/browse/DOCAC-14030">DOCAC-14030</a></p>
</td>
</tr>
</tbody>
</table>

### Improvements {#march-26-improv}

Improvements coming with this release are listed below.

#### Journeys

* **Journey Arbitration - AI Models** - In addition to ranking formulas, AI models can now be used with Journey Arbitration to automatically rank and prioritize journey entry for customers, using machine learning to determine the most relevant journey for each profile based on historical behavior and contextual signals. This capability is only available for a set of organizations (Limited Availability). To gain access, contact your Adobe representative.

  Documentation JIRA task: [DOCAC-14295](https://jira.corp.adobe.com/browse/DOCAC-14295)

#### Reporting

* **Exclude bot clicks for email and SMS reporting** - Email and SMS reporting now automatically filters out bot clicks from click metrics, providing more accurate engagement data and preventing automated traffic from inflating your performance figures.
  Documentation JIRA task: [DOCAC-14354](https://jira.corp.adobe.com/browse/DOCAC-14354)

* **Send-Time Optimization: updated controls location and new lift report** - Send-Time Optimization (STO) controls have been relocated to the Action configuration menu. Additionally, a new lift report is now available in Journeys reports to measure the impact of STO on your campaign performance metrics.

  Documentation JIRA task: [DOCAC-14335](https://jira.corp.adobe.com/browse/DOCAC-14335)

#### Email Designer

* **Open-time personalization using Dynamic Media (Beta)** - You can now personalize email content at open time using Adobe Dynamic Media assets, enabling real-time, recipient-specific images and visuals that are generated dynamically based on each recipient's attributes at the moment of email opening. This capability is currently in Beta.
  Documentation JIRA task: [DOCAC-14353](https://jira.corp.adobe.com/browse/DOCAC-14353)

* **Email Designer displayed in Unified Shell** - The Email Designer is now displayed within the Unified Shell experience, providing a consistent navigation and header experience that aligns with other Adobe applications.
  Documentation JIRA task: [DOCAC-14254](https://jira.corp.adobe.com/browse/DOCAC-14254)

* **Text mode support in fragments** - Fragments now support text mode editing, allowing you to create and manage plain text versions of your content fragments for use in text-based email workflows and multi-channel scenarios.
  Documentation JIRA task: [DOCAC-14204](https://jira.corp.adobe.com/browse/DOCAC-14204)

#### Decisioning

* **Expression Fragment Reference change feed support in Edge Decisioning** - This enhancement allows changes in fragment references to automatically be reflected in all items that reference fragments, without needing to refresh anything manually (republishing the campaign or decision policy).
  Documentation JIRA task: [DOCAC-14350](https://jira.corp.adobe.com/browse/DOCAC-14350)

* **Optional fragments in decision items** - Fragments attached to decision items can now be configured as optional, providing greater flexibility in content composition when not all decision item renderings require a specific fragment.
  Documentation JIRA task: [DOCAC-14309](https://jira.corp.adobe.com/browse/DOCAC-14309)

#### Configuration

* **URL parameters encryption** - URL parameters in tracking links and landing pages can now be encrypted, providing an additional layer of security for sensitive parameter data. This capability is only available for a set of organizations (Limited Availability). To gain access, contact your Adobe representative.
  Documentation JIRA task: [DOCAC-14349](https://jira.corp.adobe.com/browse/DOCAC-14349)

* **Folders for journeys and campaigns** - You can now organize your journeys and campaigns into folders, enabling structured navigation and easier management for teams working with large volumes of content. This capability is only available for a set of organizations (Limited Availability). To gain access, contact your Adobe representative.
  Documentation JIRA task: [DOCAC-14038](https://jira.corp.adobe.com/browse/DOCAC-14038)

#### Orchestrated campaigns

* **Target dimension simplification in Orchestrated Campaigns** - You can now easily select or automatically deduce the right targeting and secondary dimensions in Orchestrated campaigns for accurate, efficient audience activation.
  Documentation JIRA task: [DOCAC-13554](https://jira.corp.adobe.com/browse/DOCAC-13554)
-->

<!--
## February '26 pre-release notes {#feb-26-01-rn}

**The pre-release notes below are subject to change without prior notice until the release availability date**. Links, screens and updated documentation are published in the release notes, at the release date.

See also [Adobe Experience Platform Pre-release notes](https://experienceleague.adobe.com/zh-hans/docs/experience-platform/release-notes/pre-release-notes){target="_blank"}.

**Release date**: February 17, 2026

### New capabilities {#feb-26-01-features}

<table>
<thead>
<tr>
<th><strong>Wave sending of outbound messages</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>You can schedule outbound messages from <strong>campaigns</strong> or <strong>journeys</strong> to be delivered in controlled <strong>batches</strong> over time.</p>
<p>Wave sending offers the following benefits:</p>
<ul>
<li>Better <strong>deliverability</strong> – Spread sends over time to help maintain a strong <strong>sender reputation</strong> and reduce the risk of being flagged as spam.</li>
<li><strong>Load control</strong> – Avoid overwhelming downstream systems (e.g. call centers, landing pages) by limiting how many messages go out at once.</li>
<li>High-volume and time-sensitive use cases – Suited to large audiences or when you need to control timing (e.g. call center capacity, ramp-up, or time-bound offers).</li>
</ul>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Journey arbitration</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>You can now use <strong>formulas</strong> and <strong>AI models</strong> to automatically boost <strong>journey priority scores</strong> based on customer profile attributes and contextual factors, ensuring customers enter the most relevant journeys.</p>
<p>This capability is only available for a set of organizations (<strong>Limited Availability</strong>). To gain access, contact your Adobe representative.</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Journey Agent: Channel Content Create</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Powered by <strong>Adobe Experience Platform Agent Orchestrator</strong>, <strong>Journey Agent</strong> is available in Journey Optimizer and enables you to analyze journeys through a <strong>natural language interface</strong>. You can now also generate and manage channel-specific content directly in Journey Agent, creating content for channels such as email and push, applying and previewing templates, refining tone and style through prompts, and opening content in <strong>Content Designer</strong> for in-context editing.</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Mobile Live Activities</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p><strong>Live Activities</strong> provide <strong>real-time updates</strong> and interactive experiences within mobile apps, allowing users to stay informed about ongoing events or tasks directly on their device's screen. This feature enhances engagement by delivering live information, such as progress tracking, event updates, or interactive content, without requiring users to open the app.</p>
<p>Previously released in beta, this capability is now available to all environments (<strong>General Availability</strong>).</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Action activity in journeys</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Journey Optimizer supports a new generic <strong>Action activity</strong> that enables you to configure both single actions and <strong>multi-action inbound action groups</strong>, allowing for streamlined action configuration within the <strong>journey canvas</strong>. In particular, this new feature allows for:</p>
<ul>
<li>A simplified native action configuration within the journey canvas.</li>
<li>The capacity to create multi-action inbound action groups.</li>
<li>The ability to add <strong>optimization</strong> to any built-in channel action.</li>
<li>The ability to add both <strong>experimentation</strong> and <strong>multilingual</strong> options to any action.</li>
</ul>
<p>Previously released in Limited Availability, this capability is now available to all environments (General Availability).</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Web Push notifications channel</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Adobe Journey Optimizer now supports <strong>Web Push notifications</strong>, expanding the push channel beyond mobile. You can seamlessly deliver notifications to both mobile and desktop browsers, enabling you to reach customers directly on their devices without requiring an app. This enhancement allows you to engage users with timely, personalized messages in real time, leveraging the same <strong>authoring workflows</strong> and <strong>targeting capabilities</strong> already available for mobile push.</p>
<p>Previously released in beta, this capability is now available to all environments (<strong>General Availability</strong>).</p>
<p>Availability date: February 13, 2026</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Content decision activity</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>A new <strong>Content decision activity</strong> is now available in the <strong>journey canvas</strong> for integrating <strong>personalized offers</strong> directly into your customer journeys. This activity enables you to deliver decision-based content and reference those offers throughout your journey—in conditions for creating eligibility-based branching, in custom actions for passing offer data to external systems, and in other activities for building fully personalized customer experiences.</p>
<p>Previously released in Limited Availability, this capability is now available to all environments (<strong>General Availability</strong>).</p>
<p><img src="assets/do-not-localize/content-decision.gif"/></p>
<p>For more information, refer to the <a href="../building-journeys/content-decision.md">detailed documentation</a>.</p>
<p>Availability date: February 11, 2026</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Self-service migration tooling APIs</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p><strong>Migration tooling APIs</strong> are now available to programmatically migrate <strong>Decision management</strong> entities to <strong>Decisioning</strong>, featuring:</p>
<ul>
<li>Flexible migration scopes (<strong>sandbox</strong>, <strong>offer</strong>, or <strong>decision</strong> level)</li>
<li>Automated <strong>dependency analysis</strong> and validation</li>
<li><strong>Rollback support</strong> for completed migrations</li>
<li>Detailed migration reports with object mappings</li>
</ul>
<p>For more information, refer to the <a href="../experience-decisioning/decisioning-migration-api.md">detailed documentation</a>.</p>
<p>Availability date: February 3, 2026</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Custom action monitoring</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Gain deeper insight into the health and performance of your <strong>custom action endpoints</strong> with a new <strong>monitoring dashboard</strong> and enriched <strong>journey step event data</strong>. Track successful calls, errors, throughput, response times, and queue wait times to quickly understand when, where, and why anomalies occur.</p>
<p>Previously released in Limited Availability, this capability is now available to all environments (<strong>General Availability</strong>).</p>
<p>For more information, refer to the <a href="../action/reporting.md">detailed documentation</a>.</p>
<p>Availability date: February 3, 2026</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Decisioning support in SMS channel</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>You can now personalize and optimize the content of your <strong>SMS messages</strong> with <strong>Decisioning</strong>. Use <strong>Priority Scores</strong>, <strong>Formulas</strong>, or <strong>AI Models</strong> to display the best content to your customers.</p>
<p>For more information, refer to the <a href="../experience-decisioning/create-decision.md">detailed documentation</a>.</p>
<p>Availability date: February 2, 2026</p>
</td>
</tr>
</tbody>
</table>

### Improvements {#feb-26-01-improv}

Improvements coming with this release are listed below.

#### Configuration

* **Experience event usage in journey expressions** - Starting April 1, 2026, the use of experience event attributes in journey expressions will no longer be supported for organizations that have not used this capability in the last 90 days. This capability has already been unavailable for new customer organizations since July 8, 2025. For alternatives, see [Experience event lookup in journeys](../building-journeys/exp-event-lookup.md).


* **Subdomain delegation method switching** - You can now switch from one <strong>subdomain delegation</strong> method to another. This enables you to migrate domains using the <strong>CNAME delegation</strong> mode to the <strong>custom delegation</strong> method to adhere to your company's security policies.

  **Note**: This capability is only available for a set of organizations (<strong>Limited Availability</strong>). To gain access, contact your Adobe representative.


#### Email Designer

* **Use a brand theme to convert an image to an email template** - When converting an image to an email template in Journey Optimizer, you can now use a <strong>theme</strong> as input so the generated HTML follows your <strong>brand parameters</strong>. Styling such as background color, button color, fonts, line spacing, margins, and padding is applied automatically, reducing manual design work and delivering a template that is ready to use with minimal edits.


* **Update brands with new color tab** - <strong>Brand guidelines</strong> help ensure your brand is presented consistently across all touchpoints. The new <strong>Colors section</strong> defines the standards for your brand's color system, outlining how colors are selected, organized, and applied across experiences. It ensures consistent use of primary, secondary, accent, and neutral colors to support a cohesive, accessible, and recognizable brand identity.


#### AI

* **Integration of custom Firefly models and third-party image generation models** - Enable seamless integration of standard and custom <strong>Firefly models</strong>, along with approved <strong>third-party image models</strong> (e.g., NanoBanana), to provide greater flexibility, control, and brand alignment when generating images. This allows you to select the best model for each use case: standard Firefly for general needs, custom Firefly for on-brand generation, or approved third-party models for specialized or experimental scenarios.


#### Experience Decisioning

* **Edge inbound support for using Adobe Experience Platform data in Decisioning** - Decisioning support of <strong>Experience Platform data lookup</strong> now includes <strong>edge inbound</strong> channel use cases. The capability remains in Limited Availability; General Availability of the underlying data lookup feature is not yet announced (AEP/product dependency).

  **Note**: This capability is only available for a set of organizations (<strong>Limited Availability</strong>). To gain access, contact your Adobe representative.


* **Experience Decisioning preview in Code-based Experience channel** - You can now preview <strong>decision items</strong> when configuring <strong>Experience Decisioning</strong> with the <strong>Code-based Experience</strong> channel. Preview is available directly in the authoring interface before going live.


* **Offer Ranking AI Model Observability** - Journey Optimizer now allows you to monitor the <strong>health</strong>, <strong>training status</strong>, and <strong>performance</strong> of your <strong>AI models</strong> in Decisioning—so you can verify training success, troubleshoot failures, and understand impact on your outcomes. This capability is available for personalized optimization models only (not auto-optimization).


* **Attach fragments to decision items** - Journey Optimizer now provides the ability to attach <strong>fragments</strong> to <strong>decision items</strong> which can be leveraged in code-based experience campaigns through <strong>decision policies</strong>.

  **Note**: Previously released in Limited Availability, this capability is now available to all environments (General Availability).

  Availability date: February 12, 2026.


#### Journeys

* **Multiple inbound actions in journeys** - To simplify your journey orchestration, you can now define several <strong>inbound actions</strong> in a single journey. Previously available in campaigns, this capability enables you to deliver multiple <strong>code-based experiences</strong>, <strong>in-app messages</strong>, <strong>content cards</strong>, or <strong>web actions</strong> to different locations at the same time, each action containing specific content.

  **Note**: Previously released in Limited Availability, this capability is now available to all environments (General Availability).


* **SMS Webhooks** - <strong>Webhooks</strong> are now supported across all SMS providers. You can configure each webhook based on its intended purpose: <strong>Inbound webhooks</strong> to capture incoming messages and <strong>Feedback webhooks</strong> to receive delivery receipts, status updates, and other message-related events. [Read more](../sms/sms-webhook.md)

  Availability date: February 2, 2026.
-->
<!--
## January '26 pre-release notes {#jan-26-01-rn}

**The pre-release notes below are subject to change without prior notice until the release availability date**. Links, screens and updated documentation are published in the release notes, at the release date.

See also [Adobe Experience Platform Pre-release notes](https://experienceleague.adobe.com/zh-hans/docs/experience-platform/release-notes/pre-release-notes){target="_blank"}.

**Release date**: January 27, 2026

### New capabilities {#jan-26-01-features}

<table>
<thead>
<tr>
<th><strong>Action activity in journeys</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Journey Optimizer supports a new generic <strong>Action activity</strong> that enables you to configure both single actions and <strong>multi-action inbound action groups</strong>, allowing for streamlined action configuration within the journey canvas. In particular, this new feature allows for:</p>
<ul>
<li>A simplified native action configuration within the journey canvas.</li>
<li>The capacity to create multi-action inbound action groups.</li>
<li>The ability to add optimization to any built-in channel action.</li>
<li>The ability to add both experimentation and multi-lingual options to any action.</li>
</ul>
<p>Previously released in Limited Availability, this capability is now available to all environments (General Availability).</p>
<p><a href="https://jira.corp.adobe.com/browse/CJM-111916">Link to PRODUCT JIRA task</a></p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Custom action monitoring</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Gain deeper insight into the health and performance of your custom action endpoints with a new <strong>monitoring dashboard</strong> and enriched journey step event data. Track successful calls, errors, throughput, response times, and queue wait times to quickly understand when, where, and why anomalies occur.</p>
<p>Previously released in Limited Availability, this capability is now available to all environments (General Availability).</p>
<p><a href="https://jira.corp.adobe.com/browse/CJM-126869">Link to PRODUCT JIRA task</a></p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Quiet Hours / Time Based Exclusions</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Quiet hours let you define <strong>time-based exclusions</strong> for Email, SMS, Push, and WhatsApp channels. They ensure that no messages are sent during specific periods of time, helping you respect customer preferences and compliance requirements. You can apply quiet hours through <strong>rule sets</strong>, which can be assigned to individual actions in campaigns or journeys for precise control.</p>
<p>Previously released in Limited Availability, this feature is now available to all environments. With this General Availability release, the feature now includes the ability for customer to queue a campaign action until the completion of Quiet Hours, and the ability to preview the activated Quiet Hours rule.</p>
<p><a href="https://jira.corp.adobe.com/browse/CJM-63912">Link to PRODUCT JIRA task</a></p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Direct Mail channel in journeys</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Previously limited to Campaigns, the <strong>Direct Mail channel</strong> is now available on the <strong>journey canvas</strong>, enabling you to incorporate Direct Mail into your journeys. Direct Mail can now be used in both batch and 1:1 journey scenarios, with support for file extraction configuration and time-based frequency settings.</p>
<p>Previously released in Limited Availability, this capability is now available to all environments (General Availability).</p>
<p><a href="https://jira.corp.adobe.com/browse/CJM-38399">Link to PRODUCT JIRA task</a></p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Web Push notifications channel</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Adobe Journey Optimizer now supports <strong>Web Push notifications</strong>, expanding the push channel beyond mobile. You can seamlessly deliver notifications to both mobile and desktop browsers, enabling you to reach customers directly on their devices without requiring an app. This enhancement allows you to engage users with timely, personalized messages in real time, leveraging the same authoring workflows and targeting capabilities already available for mobile push.</p>
<p>Previously released in Limited Availability, this capability is now available to all environments (General Availability).</p>
<p><a href="https://jira.corp.adobe.com/browse/CJM-37866">Link to PRODUCT JIRA task</a></p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Decisioning support in Push and SMS channels</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>You can now add <strong>Decision policies</strong> into push and SMS journeys and campaigns. Decision policies are containers for your offers that leverage the Decisioning engine to dynamically return the best content to deliver for each audience member.</p>
<p>This capability is only available for a set of organizations (Limited Availability). To gain access, contact your Adobe representative.</p>
<p><a href="https://jira.corp.adobe.com/browse/CJM-55817">Link to PRODUCT JIRA task</a> | <a href="https://jira.corp.adobe.com/browse/CJM-55818">Link to PRODUCT JIRA task</a></p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Direct mail channel in Orchestrated campaigns</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Direct mail channel is now available in orchestrated campaigns. The <strong>Direct mail activity</strong> facilitates direct mail sending within your Orchestrated campaign, for both one-time and recurring messages. It serves to automate the process of generating the <strong>extraction file</strong> required by direct mail providers. You can combine channel activities into the Orchestrated campaign canvas to create cross-channel campaigns that can trigger actions based on customer behavior and data.</p>
<p><a href="https://jira.corp.adobe.com/browse/CJM-82584">Link to PRODUCT JIRA task</a></p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>New source connectors for loyalty apps</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>New <strong>source connectors</strong> are now available in Adobe Experience Platform for the Talon.One, Capillary and Kobie loyalty Apps. These connectors let you seamlessly stream loyalty data into Adobe Experience Platform and leverage these data in Journey Optimizer.</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Message Export</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>A new <strong>Message Export</strong> capability is now available for email and SMS channels. This feature allows you to automatically export sent message content to a dedicated Experience Platform dataset, enabling you to:</p>
<ul>
<li>Meet regulatory compliance requirements (such as HIPAA)</li>
<li>Archive messages for legal claims and customer care inquiries</li>
<li>Retain copies of personalized content sent to individuals</li>
</ul>
<p>Records are retained in the AJO Message Export Dataset for <strong>7 calendar days from ingestion</strong>. During this retention period, you can export the data to your own storage via Experience Platform destinations. The feature is enabled at the channel configuration level, giving you granular control over which messages are exported.</p>
<p><a href="https://jira.corp.adobe.com/browse/CJM-105313">Link to PRODUCT JIRA task</a></p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Journey Agent - Create a Journey</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Journey Create Agent enables Journey Optimizer users to build and configure marketing journeys using a natural language interface. With Journey Create Agent, practitioners can quickly create journeys by describing their requirements in conversational prompts. The agent streamlines journey creation, allowing marketers to focus on strategy rather than technical configuration.</p>
<p><a href="https://experienceleague.adobe.com/zh-hans/docs/experience-cloud-ai/experience-cloud-ai/agents/ajo-agent#journey-create-agent-skill-overview-and-user-guide" target="_blank">Learn more</a></p>
<p><a href="https://jira.corp.adobe.com/browse/CJM-95142">Link to PRODUCT JIRA task</a></p>
<p>Availability date: January 12, 2026</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>New API to retrieve Action Campaigns</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>A new <strong>Journey Optimizer API</strong> is now available, enabling you to programmatically retrieve and inspect campaign-related data such as details, versions, and configurations.</p>
<p>For more information, refer to the <a href="https://developer.adobe.com/journey-optimizer-apis/references/campaigns-retrieve/">detailed documentation</a>.</p>
<p><a href="https://jira.corp.adobe.com/browse/CJM-96195">Link to PRODUCT JIRA task</a></p>
<p>Availability date: November 24, 2025</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>New journey alerts</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Three new <strong>journey alerts</strong> are now available to help you monitor and track journey lifecycle events and custom action performance:</p>
<ul>
<li><strong>Journey Published</strong>: Receive notifications when a journey is published by a practitioner in the journey canvas.</li>
<li><strong>Journey Finished</strong>: Get alerts when a journey has finished, with specific definitions based on journey type (Read Audience or Event-triggered).</li>
<li><strong>Custom Action Capping Triggered</strong>: Be notified when capping is activated on a custom action endpoint.</li>
</ul>
<p>These alerts can be subscribed to at the organization level or for specific journeys.</p>
<p>For more information, refer to the <a href="../reports/alerts.md#journey-alerts">detailed documentation</a>.</p>
<p>Availability date: November 5, 2025</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Themes in the Email Designer</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>You can now quickly apply <strong>pre-approved themes</strong> to ensure brand consistency across all emails, speed up your campaign creation process, and independently produce high-quality emails while reducing dependency on design teams.</p>
<p>Previously released in beta version, this capability is now available for a set of organizations (Limited Availability). To gain access, contact your Adobe representative.</p>
<img src="assets/do-not-localize/themes.gif">
<p>For more information, refer to the <a href="../email/apply-email-themes.md">detailed documentation</a>.</p>
<p><a href="https://jira.corp.adobe.com/browse/NEO-88838">Link to PRODUCT JIRA task</a></p>
<p>Availability date: November 5, 2025</p>
</td>
</tr>
</tbody>
</table>

### Improvements {#jan-26-01-improv}

Improvements coming with this release are listed below.

#### AI

* **AI Assistant Content Quality Checks** - In addition to brand alignment, you can now evaluate overall <strong>content quality</strong> to uncover potential issues with readability, cohesiveness, and effectiveness, independent of your brand guidelines. These automated checks help identify unclear messaging, inconsistent tone, or structural gaps.
  <a href="https://jira.corp.adobe.com/browse/CJM-103238">Link to PRODUCT JIRA task</a>
* **Update brands with new color tab** - Brand guidelines help ensure your brand is presented consistently across all touchpoints. The new <strong>Colors section</strong> defines the standards for your brand's color system, outlining how colors are selected, organized, and applied across experiences. It ensures consistent use of primary, secondary, accent, and neutral colors to support a cohesive, accessible, and recognizable brand identity.
  <a href="https://jira.corp.adobe.com/browse/CJM-121183">Link to PRODUCT JIRA task</a>

#### Campaigns

* **Schedule Campaign using Profile Time Zone** - Campaign scheduling can now use each profile's <strong>time zone</strong> to deliver messages at the intended local time.

  **Note**: This improvement is only available for a set of organizations (Limited Availability).
  <a href="https://jira.corp.adobe.com/browse/CJM-43782">Link to PRODUCT JIRA task</a>

#### Channels

* **SMS Webhooks: Phase II** - Description to be provided.
  <a href="https://jira.corp.adobe.com/browse/CJM-93914">Link to PRODUCT JIRA task</a>

#### Email Designer

* **In-place corrections in the Email designer** - <strong>AI-powered automatic content suggestions</strong> are now available in the Email Designer when violations are detected during content validation. If content is flagged as misaligned with brand guidelines or fails quality criteria, the system proactively generates corrected alternatives that can be reviewed and applied inline, improving compliance and accelerating production.
  <a href="https://jira.corp.adobe.com/browse/CJM-95365">Link to PRODUCT JIRA task</a>

#### Experience Decisioning

* **Self-service migration tooling APIs** - A new set of <strong>migration tooling APIs</strong> is available to migrate Offer management entities to Experience Decisioning. The tooling enables seamless migration between sandboxes with dependency resolution and rollback capabilities.
  <a href="https://jira.corp.adobe.com/browse/CJM-109695">Link to PRODUCT JIRA task</a>

* **Attach fragments to decision items** - Journey Optimizer now provides the ability to attach <strong>fragments</strong> to decision items which can be leveraged in code-based experience campaigns through decision policies.

  **Note**: Previously released in Limited Availability, this improvement is now available to all environments (General Availability).
  <a href="https://jira.corp.adobe.com/browse/CJM-110282">Link to PRODUCT JIRA task</a>

#### Journeys

* **Leverage a failure response payload in journey Custom Actions** - You can now define an optional <strong>error response payload</strong> for custom actions. When a call fails, the error payload is exposed in the journey context and is available in the timeout/error branch to support richer fallback logic and debugging.
  <a href="https://jira.corp.adobe.com/browse/CJM-113125">Link to PRODUCT JIRA task</a>

* **Combine native and Adobe Campaign message actions** - Journey Optimizer now lets you combine Adobe Campaign v7/v8 message actions with native channel actions in the same journey.
  <a href="https://jira.corp.adobe.com/browse/CJM-113103">Link to PRODUCT JIRA task</a>

* **Journey payload size validation in journeys** - Journey Optimizer now provides <strong>payload size validation</strong> to help ensure optimal performance and system stability. When building or publishing journeys, you receive clear warnings and errors if payload sizes approach or exceed recommended limits, along with actionable guidance to optimize your journey configuration. This proactive validation helps you identify potential issues early and maintain journey performance.
  <a href="https://jira.corp.adobe.com/browse/CJM-122236">Link to PRODUCT JIRA task</a>

* **Multiple inbound actions in journeys** - To simplify your journey orchestration, you can now define <strong>multiple inbound actions</strong> in a single journey. Previously available in campaigns, this capability enables you to deliver multiple code-based experiences, In-app messages, Content Cards or web actions to different locations at the same time, each action containing a specific content.

  **Note**: Previously released in Limited Availability, this improvement is now available to all environments (General Availability).
  <a href="https://jira.corp.adobe.com/browse/CJM-111916">Link to PRODUCT JIRA task</a>

#### Orchestrated campaigns

* **Select attributes and copy distribution values** - You can now select or copy values directly from the distribution of values view in orchestrated campaigns.
  <a href="https://jira.corp.adobe.com/browse/CJM-105244">Link to PRODUCT JIRA task</a>

* **Data usage label inheritance for audiences** - <strong>Data usage labels</strong> applied in Adobe Experience Platform now automatically carry over when saving audiences in orchestrated campaigns, reducing manual DULE tagging.
  <a href="https://jira.corp.adobe.com/browse/CJM-120769">Link to PRODUCT JIRA task</a>

* **Predefined retargeting filters** - To support easier retargeting for orchestrated campaign use cases, this release introduces new <strong>retargeting filters</strong>. These filters let you directly target audiences based on message engagement, such as sent, opened only, opened or clicked, or opened and clicked, and select the specific campaign or in-transition campaign you want to retarget.
  <a href="https://jira.corp.adobe.com/browse/CJM-116701">Link to PRODUCT JIRA task</a>

* **Predefined filters with parameters** - You can now create <strong>filters with parameters</strong> in orchestrated campaigns for reusable, editable rules.
  <a href="https://jira.corp.adobe.com/browse/CJM-115431">Link to PRODUCT JIRA task</a>

* **Message confirmation before send** - A <strong>confirmation step</strong> is now enabled by default before sending orchestrated campaigns to reduce accidental sends.
  <a href="https://jira.corp.adobe.com/browse/CJM-87219">Link to PRODUCT JIRA task</a>

* **User-generated metadata support** - The <strong>executionMetadata helper function</strong> is now available in the personalization editor for Orchestrated Campaigns, enabling you to attach contextual information to any native action and store it in a dataset for export to external systems.
  <a href="https://jira.corp.adobe.com/browse/CJM-112697">Link to PRODUCT JIRA task</a>

* **Restart button** - Orchestrated campaigns now include a <strong>restart button</strong> so you can quickly re-launch runs when needed before publishing the campaign.
  <a href="https://jira.corp.adobe.com/browse/CJM-106020">Link to PRODUCT JIRA task</a>

* **Rate control support** - Orchestrated campaigns now support <strong>rate control</strong> to help you pace deliveries and align with volume constraints.
  <a href="https://jira.corp.adobe.com/browse/CJM-113254">Link to PRODUCT JIRA task</a>

#### Permissions

* **Prevent self-approval for journeys and campaigns** - You can now require that creators cannot approve their own journeys or campaigns, improving <strong>separation of duties</strong> in approval workflows.
  <a href="https://jira.corp.adobe.com/browse/CJM-99957">Link to PRODUCT JIRA task</a> | <a href="https://jira.corp.adobe.com/browse/CJM-95676">Link to PRODUCT JIRA task</a>

## Coming soon {#jan-26-01-coming-soon}

In the next few days, the following capabilities and enhancements are scheduled for release. **Information is subject to change**. Updated links, screens, and documentation will be shared once these updates are live in production.

<table>
<thead>
<tr>
<th><strong>Content generation within Journey Agent</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Powered by Adobe Experience Platform Agent Orchestrator, <strong>Journey Agent</strong> is available in Journey Optimizer and enables you to analyze journeys through a natural language interface. You can now also generate and manage channel-specific content directly in Journey Agent, creating content for channels such as email and push, applying and previewing templates, refining tone and style through prompts, and opening content in Content Designer for in-context editing.</p>
<p><a href="https://jira.corp.adobe.com/browse/CJM-111882">Link to PRODUCT JIRA task</a></p>
<p>Availability date: February 2, 2026</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Content decision activity</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>You can now include <strong>personalized offers</strong> in your journeys through a dedicated Content decision activity in the journey canvas, and use them in journey activities, including conditions and custom actions.</p>
<p><a href="https://jira.corp.adobe.com/browse/CJM-99223">Link to PRODUCT JIRA task</a></p>
<p>Availability date: February 3, 2026</p>
</td>
</tr>
</tbody>
</table>
-->
