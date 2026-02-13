---
solution: Journey Optimizer
product: journey optimizer
title: Journey Optimizer 的预发行说明
description: Adobe Journey Optimizer 预发行说明
feature: Release Notes
hide: true
hidefromtoc: true
exl-id: 6e7d1300-8efd-4fdc-90e3-3ccdc3babd2f
source-git-commit: 9c30e6ce9c2d1074834c98e428755734b6bb585c
workflow-type: tm+mt
source-wordcount: '1497'
ht-degree: 26%

---

# 预发行说明 {#e-release-notes}

[!DNL Adobe Journey Optimizer] 不断地提供新功能、对现有功能进行增强和修复错误。所有更改会在每月末整合到[发行说明](release-notes.md)中。

## 2026年2月预发行说明 {#feb-26-01-rn}

**以下预发行说明可能会在正式发行日期之前有所更改，恕不另行通知**。链接、屏幕和更新的文档会于发布日期在发行说明中发布。

另请参阅 [Adobe Experience Platform 预发行说明](https://experienceleague.adobe.com/zh-hans/docs/experience-platform/release-notes/pre-release-notes){target="_blank"}。

**发行日期**：2026年2月17日

### 新功能 {#feb-26-01-features}

<table>
<thead>
<tr>
<th><strong>出站消息的波动发送</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>您可以安排来自<strong>营销活动</strong>或<strong>历程</strong>的出站消息在一段时间内以受控制的<strong>批次</strong>投放。</p>
<p>波次发送具备以下优势：</p>
<ul>
<li>更好的<strong>可投放性</strong> — 随着时间推移，分散发送有助于保持强大的<strong>发件人信誉</strong>，并降低标记为垃圾邮件的风险。</li>
<li><strong>加载控制</strong> — 通过限制一次传出多少条消息，避免使下游系统（如呼叫中心、登陆页面）不堪重负。</li>
<li>大容量、时效性强的用例 — 适用于较大的受众或您需要控制计时时（例如，呼叫中心容量、加电或有时限的选件）。</li>
</ul>
<p><a href="https://jira.corp.adobe.com/browse/DOCAC-11533">链接到 DOCAC JIRA 任务</a></p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>历程仲裁</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>您现在可以使用<strong>公式</strong>和<strong>AI模型</strong>根据客户个人资料属性和上下文因素自动提升<strong>历程优先级分数</strong>，确保客户进入最相关的历程。</p>
<p>此功能仅适用于一组组织（<strong>有限可用性</strong>）。 要获得访问权限，请与 Adobe 代表联系。</p>
<p><a href="https://jira.corp.adobe.com/browse/DOCAC-13976">链接到 DOCAC JIRA 任务</a></p>
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
<p>由<strong>Adobe Experience Platform Agent Orchestrator</strong>提供支持的<strong>Journey Agent</strong>在Journey Optimizer中可用，使您能够通过<strong>自然语言界面</strong>分析旅程。 您现在还可以直接在Journey Agent中生成和管理特定于渠道的内容，为电子邮件和推送等渠道创建内容，应用和预览模板，通过提示优化音调和样式，以及在<strong>内容Designer</strong>中打开内容以进行上下文内编辑。</p>
<p><a href="https://jira.corp.adobe.com/browse/DOCAC-13980">链接到 DOCAC JIRA 任务</a></p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>移动实时活动</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p><strong>实时活动</strong>在移动应用内提供<strong>实时更新</strong>和交互式体验，使用户能够直接在设备屏幕上随时了解正在进行的事件或任务。 此功能通过提供实时信息（例如进度跟踪、活动更新或交互式内容）来增强参与度，而无需用户打开应用程序。</p>
<p>以前以Beta版发布，此功能现在可用于所有环境（<strong>一般可用性</strong>）。</p>
<p><a href="https://jira.corp.adobe.com/browse/DOCAC-13588">链接到 DOCAC JIRA 任务</a></p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>历程中的操作活动</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Journey Optimizer支持新的通用<strong>操作活动</strong>，该活动允许您配置单个操作和<strong>多操作入站操作组</strong>，从而简化<strong>历程画布</strong>中的操作配置。 特别需要指出，通过这项新功能可以：</p>
<ul>
<li>简化历程画布中的原生操作配置。</li>
<li>创建多操作入站操作组的功能。</li>
<li>能够将<strong>优化</strong>添加到任何内置渠道操作。</li>
<li>能够将<strong>experimentation</strong>和<strong>multilingual</strong>选项添加到任何操作。</li>
</ul>
<p>此功能现在可用于所有环境（<strong>一般可用性</strong>）。</p>
<p><a href="https://jira.corp.adobe.com/browse/DOCAC-13290">链接到 DOCAC JIRA 任务</a></p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Web 推送通知渠道</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Adobe Journey Optimizer 现在支持 <strong>Web 推送通知</strong>，将推送渠道从移动设备扩展到更多平台。您可以无缝地向移动设备浏览器和桌面设备浏览器发送通知，无需依赖应用程序即可通过客户的设备直接与其联系。此增强功能允许您利用移动推送中已有的相同<strong>创作工作流</strong>和<strong>定位功能</strong>，实时向用户发送及时、个性化的消息。</p>
<p>以前以Beta版发布，此功能现在可用于所有环境（<strong>一般可用性</strong>）。</p>
<p>发布日期： 2026年2月12日</p>
<p><a href="https://jira.corp.adobe.com/browse/DOCAC-13581">链接到 DOCAC JIRA 任务</a></p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>内容决策活动</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p><strong>历程画布</strong>中现在提供了新的<strong>内容决策活动</strong>，用于将<strong>个性化优惠</strong>直接集成到您的客户历程中。 此活动可让您提供基于决策的内容并在整个历程中引用这些优惠 — 在创建基于资格的分支的条件、在用于将优惠数据传递到外部系统的自定义操作以及在其他构建完全个性化客户体验的活动中。</p>
<p>以前以“有限可用性”形式发布，现在此功能可用于所有环境（<strong>一般可用性</strong>）。</p>
<p><img src="assets/do-not-localize/content-decision.gif"/></p>
<p>有关更多信息，请参阅<a href="../building-journeys/content-decision.md">详细文档</a>。</p>
<p>发布日期： 2026年2月11日</p>
<p><a href="https://jira.corp.adobe.com/browse/DOCAC-12902">链接到 DOCAC JIRA 任务</a></p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>自助迁移工具 API</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p><strong>迁移工具API</strong>现在可用于以编程方式将<strong>决策管理</strong>实体迁移到<strong>决策</strong>，功能：</p>
<ul>
<li>灵活的迁移范围（<strong>沙盒</strong>、<strong>选件</strong>或<strong>决策</strong>级别）</li>
<li>自动的<strong>依赖关系分析</strong>和验证</li>
<li>已完成迁移的<strong>回滚支持</strong></li>
<li>具有对象映射的详细迁移报告</li>
</ul>
<p>有关更多信息，请参阅<a href="../experience-decisioning/decisioning-migration-api.md">详细文档</a>。</p>
<p>发布日期：2026 年 2 月 3 日</p>
<p><a href="https://jira.corp.adobe.com/browse/DOCAC-13837">链接到 DOCAC JIRA 任务</a></p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>自定义操作监控</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>通过新的<strong>监视仪表板</strong>和扩充的<strong>历程步骤事件数据</strong>，更深入地了解<strong>自定义操作端点</strong>的运行状况和性能insight。 跟踪成功的调用、错误、吞吐量、响应时间和队列等待时间，以快速了解发生异常的时间、位置和原因。</p>
<p>以前以“有限可用性”形式发布，现在此功能可用于所有环境（<strong>一般可用性</strong>）。</p>
<p>有关更多信息，请参阅<a href="../action/reporting.md">详细文档</a>。</p>
<p>发布日期：2026 年 2 月 3 日</p>
<p><a href="https://jira.corp.adobe.com/browse/DOCAC-13981">链接到 DOCAC JIRA 任务</a></p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>短信渠道中的决策支持</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>您现在可以使用<strong>Decisioning</strong>个性化并优化<strong>短信消息</strong>的内容。 使用<strong>优先级分数</strong>、<strong>公式</strong>或<strong>AI模型</strong>向客户显示最佳内容。</p>
<p>有关更多信息，请参阅<a href="../experience-decisioning/create-decision.md">详细文档</a>。</p>
<p>发布日期：2026 年 2 月 2 日</p>
<p><a href="https://jira.corp.adobe.com/browse/DOCAC-13426">链接到 DOCAC JIRA 任务</a></p>
</td>
</tr>
</tbody>
</table>

### 改进 {#feb-26-01-improv}

此版本包含的改进如下所述。

#### 配置

* **历程表达式中的体验事件用法** — 从2026年4月1日开始，过去90天内未使用此功能的组织将不再支持在历程表达式中使用体验事件属性。 自2025年7月8日以来，此功能已不适用于新客户组织。 有关替代项，请参阅历程中的[体验事件查找](../building-journeys/exp-event-lookup.md)。

  <a href="https://jira.corp.adobe.com/browse/DOCAC-14136">链接到DOCAC JIRA任务</a>

* **子域委派方法切换** — 您现在可以从一个<strong>子域委派</strong>方法切换到另一个。 这使您能够使用<strong>CNAME委派</strong>模式将域迁移到<strong>自定义委派</strong>方法，以遵守您公司的安全策略。

  <a href="https://jira.corp.adobe.com/browse/DOCAC-13610">链接到DOCAC JIRA任务</a>

#### 电子邮件设计器

* **使用品牌主题将图像转换为电子邮件模板** — 在Journey Optimizer中将图像转换为电子邮件模板时，现在可以使用<strong>主题</strong>作为输入，以便生成的HTML遵循<strong>品牌参数</strong>。 样式（如背景颜色、按钮颜色、字体、行距、边距和填充）会自动应用，从而减少手动设计工作，并提供只需少量编辑即可使用的模板。

  <a href="https://jira.corp.adobe.com/browse/DOCAC-14105">链接到DOCAC JIRA任务</a>

* **使用新颜色标签更新品牌** - <strong>品牌指南</strong>有助于确保在所有接触点上始终如一地呈现您的品牌。 新的<strong>颜色板块</strong>定义了您品牌颜色体系的标准，介绍了如何在不同体验中选择、组织和应用颜色。 它确保对主色、辅色、个性色和中性色使用的一致性，以打造一个有粘性、可访问和有辨识度的品牌标识。

  <a href="https://jira.corp.adobe.com/browse/DOCAC-13811">链接到DOCAC JIRA任务</a>

#### AI

* **自定义Firefly模型与第三方图像生成模型的集成** — 实现标准和自定义<strong>Firefly模型</strong>以及批准的<strong>第三方图像模型</strong>（例如，NanoBanana）的无缝集成，以便在生成图像时提供更大的灵活性、控制力以及品牌一致性。 这允许您为每个用例选择最佳模型：可满足一般需求的标准Firefly、用于品牌内生成的自定义Firefly，或针对专用或实验场景的批准的第三方模型。

  <a href="https://jira.corp.adobe.com/browse/DOCAC-13918">链接到DOCAC JIRA任务</a>

#### 营销活动

* **历程和营销活动文件夹** — 您现在可以将您的<strong>历程</strong>和<strong>营销活动</strong>组织到<strong>文件夹</strong>中，以改进界面中的导航和管理。

  <a href="https://jira.corp.adobe.com/browse/DOCAC-14038">链接到DOCAC JIRA任务</a>

#### 体验决策

* **基于代码的体验渠道中的Experience Decisioning预览** — 在使用<strong>基于代码的体验</strong>渠道配置<strong>Experience Decisioning</strong>时，您现在可以预览<strong>决策项</strong>。 上线之前，可以直接在创作界面中预览。

  <a href="https://jira.corp.adobe.com/browse/DOCAC-14082">链接到DOCAC JIRA任务</a>

* **优惠排名AI模型可观察性** — 现在，通过Journey Optimizer可在Decisioning中监视<strong>AI模型</strong>的<strong>运行状况</strong>、<strong>培训状态</strong>和<strong>性能</strong>，以便验证培训是否成功、排除故障并了解对结果的影响。 此功能仅适用于个性化优化模型（不适用于自动优化）。

  <a href="https://jira.corp.adobe.com/browse/DOCAC-14040">链接到DOCAC JIRA任务</a>

* **将片段附加到决策项** - Journey Optimizer现在提供将<strong>片段</strong>附加到<strong>决策项</strong>的功能，这些功能可通过<strong>决策策略</strong>在基于代码的体验营销活动中使用。

  **注意**：此改进现在对所有环境都可用（<strong>一般可用性</strong>）。

  发布日期：2026年2月12日。

  <a href="https://jira.corp.adobe.com/browse/DOCAC-13418">链接到DOCAC JIRA任务</a>

#### 历程

* **历程中的多个入站操作** — 为简化历程编排，您现在可以在单个历程中定义多个<strong>入站操作</strong>。 此功能以前在营销活动中提供，它使您能够同时将多个<strong>基于代码的体验</strong>、<strong>应用程序内消息</strong>、<strong>内容卡</strong>或<strong>Web操作</strong>传送到不同的位置，每个操作都包含特定内容。

  **注意**：此改进现在对所有环境都可用（<strong>一般可用性</strong>）。

  <a href="https://jira.corp.adobe.com/browse/DOCAC-13453">链接到DOCAC JIRA任务</a>

* **SMS Webhook** - 现在，所有短信服务提供商都支持 <strong>Webhook</strong>。 您可以根据预期目的配置每个webhook：<strong>入站webhook</strong>以捕获传入邮件，以及<strong>反馈webhook</strong>以接收送达回执、状态更新和其他与邮件相关的事件。 [了解详情](../sms/sms-webhook.md)

  发布日期：2026年2月2日。

  <a href="https://jira.corp.adobe.com/browse/DOCAC-13978">链接到DOCAC JIRA任务</a>

<!--
## January '26 pre-release notes {#jan-26-01-rn}

**The pre-release notes below are subject to change without prior notice until the release availability date**. Links, screens and updated documentation are published in the release notes, at the release date.

See also [Adobe Experience Platform Pre-release notes](https://experienceleague.adobe.com/en/docs/experience-platform/release-notes/pre-release-notes){target="_blank"}.

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
<p><a href="https://jira.corp.adobe.com/browse/DOCAC-13290">Link to DOCAC JIRA task</a> | <a href="https://jira.corp.adobe.com/browse/CJM-111916">Link to PRODUCT JIRA task</a></p>
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
<p><a href="https://jira.corp.adobe.com/browse/DOCAC-13981">Link to DOCAC JIRA task</a> | <a href="https://jira.corp.adobe.com/browse/CJM-126869">Link to PRODUCT JIRA task</a></p>
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
<p><a href="https://jira.corp.adobe.com/browse/DOCAC-13986">Link to DOCAC JIRA task</a> | <a href="https://jira.corp.adobe.com/browse/CJM-63912">Link to PRODUCT JIRA task</a></p>
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
<p><a href="https://jira.corp.adobe.com/browse/DOCAC-13543">Link to DOCAC JIRA task</a> | <a href="https://jira.corp.adobe.com/browse/CJM-38399">Link to PRODUCT JIRA task</a></p>
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
<p><a href="https://jira.corp.adobe.com/browse/DOCAC-13581">Link to DOCAC JIRA task</a> | <a href="https://jira.corp.adobe.com/browse/CJM-37866">Link to PRODUCT JIRA task</a></p>
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
<p><a href="https://jira.corp.adobe.com/browse/DOCAC-13426">Link to DOCAC JIRA task</a> | <a href="https://jira.corp.adobe.com/browse/DOCAC-13425">Link to DOCAC JIRA task</a> | <a href="https://jira.corp.adobe.com/browse/CJM-55817">Link to PRODUCT JIRA task</a> | <a href="https://jira.corp.adobe.com/browse/CJM-55818">Link to PRODUCT JIRA task</a></p>
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
<p><a href="https://jira.corp.adobe.com/browse/DOCAC-13379">Link to DOCAC JIRA task</a> | <a href="https://jira.corp.adobe.com/browse/CJM-82584">Link to PRODUCT JIRA task</a></p>
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
<p><a href="https://jira.corp.adobe.com/browse/DOCAC-13372">Link to DOCAC JIRA task</a></p>
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
<p><a href="https://jira.corp.adobe.com/browse/DOCAC-12915">Link to DOCAC JIRA task</a> | <a href="https://jira.corp.adobe.com/browse/CJM-105313">Link to PRODUCT JIRA task</a></p>
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
<p><a href="https://experienceleague.adobe.com/en/docs/experience-cloud-ai/experience-cloud-ai/agents/ajo-agent#journey-create-agent-skill-overview-and-user-guide" target="_blank">Learn more</a></p>
<p><a href="https://jira.corp.adobe.com/browse/DOCAC-13747">Link to DOCAC JIRA task</a> | <a href="https://jira.corp.adobe.com/browse/CJM-95142">Link to PRODUCT JIRA task</a></p>
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
<p><a href="https://jira.corp.adobe.com/browse/DOCAC-13506">Link to DOCAC JIRA task</a> | <a href="https://jira.corp.adobe.com/browse/CJM-96195">Link to PRODUCT JIRA task</a></p>
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
<p><a href="https://jira.corp.adobe.com/browse/DOCAC-13465">Link to DOCAC JIRA task</a></p>
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
<p><a href="https://jira.corp.adobe.com/browse/DOCAC-12941">Link to DOCAC JIRA task</a> | <a href="https://jira.corp.adobe.com/browse/NEO-88838">Link to PRODUCT JIRA task</a></p>
<p>Availability date: November 5, 2025</p>
</td>
</tr>
</tbody>
</table>

### Improvements {#jan-26-01-improv}

Improvements coming with this release are listed below.

#### AI

* **AI Assistant Content Quality Checks** - In addition to brand alignment, you can now evaluate overall <strong>content quality</strong> to uncover potential issues with readability, cohesiveness, and effectiveness, independent of your brand guidelines. These automated checks help identify unclear messaging, inconsistent tone, or structural gaps.
  <a href="https://jira.corp.adobe.com/browse/DOCAC-13917">Link to DOCAC JIRA task</a> | <a href="https://jira.corp.adobe.com/browse/CJM-103238">Link to PRODUCT JIRA task</a>
* **Update brands with new color tab** - Brand guidelines help ensure your brand is presented consistently across all touchpoints. The new <strong>Colors section</strong> defines the standards for your brand's color system, outlining how colors are selected, organized, and applied across experiences. It ensures consistent use of primary, secondary, accent, and neutral colors to support a cohesive, accessible, and recognizable brand identity.
  <a href="https://jira.corp.adobe.com/browse/DOCAC-13811">Link to DOCAC JIRA task</a> | <a href="https://jira.corp.adobe.com/browse/CJM-121183">Link to PRODUCT JIRA task</a>

#### Campaigns

* **Schedule Campaign using Profile Time Zone** - Campaign scheduling can now use each profile's <strong>time zone</strong> to deliver messages at the intended local time.

  **Note**: This improvement is only available for a set of organizations (Limited Availability).
  <a href="https://jira.corp.adobe.com/browse/DOCAC-11534">Link to DOCAC JIRA task</a> | <a href="https://jira.corp.adobe.com/browse/CJM-43782">Link to PRODUCT JIRA task</a>

#### Channels

* **SMS Webhooks: Phase II** - Description to be provided.
  <a href="https://jira.corp.adobe.com/browse/DOCAC-13978">Link to DOCAC JIRA task</a> | <a href="https://jira.corp.adobe.com/browse/CJM-93914">Link to PRODUCT JIRA task</a>

#### Email Designer

* **In-place corrections in the Email designer** - <strong>AI-powered automatic content suggestions</strong> are now available in the Email Designer when violations are detected during content validation. If content is flagged as misaligned with brand guidelines or fails quality criteria, the system proactively generates corrected alternatives that can be reviewed and applied inline, improving compliance and accelerating production.
  <a href="https://jira.corp.adobe.com/browse/DOCAC-13979">Link to DOCAC JIRA task</a> | <a href="https://jira.corp.adobe.com/browse/CJM-95365">Link to PRODUCT JIRA task</a>

#### Experience Decisioning

* **Self-service migration tooling APIs** - A new set of <strong>migration tooling APIs</strong> is available to migrate Offer management entities to Experience Decisioning. The tooling enables seamless migration between sandboxes with dependency resolution and rollback capabilities.
  <a href="https://jira.corp.adobe.com/browse/DOCAC-13837">Link to DOCAC JIRA task</a> | <a href="https://jira.corp.adobe.com/browse/CJM-109695">Link to PRODUCT JIRA task</a>

* **Attach fragments to decision items** - Journey Optimizer now provides the ability to attach <strong>fragments</strong> to decision items which can be leveraged in code-based experience campaigns through decision policies.

  **Note**: Previously released in Limited Availability, this improvement is now available to all environments (General Availability).
  <a href="https://jira.corp.adobe.com/browse/DOCAC-13418">Link to DOCAC JIRA task</a> | <a href="https://jira.corp.adobe.com/browse/CJM-110282">Link to PRODUCT JIRA task</a>

#### Journeys

* **Leverage a failure response payload in journey Custom Actions** - You can now define an optional <strong>error response payload</strong> for custom actions. When a call fails, the error payload is exposed in the journey context and is available in the timeout/error branch to support richer fallback logic and debugging.
  <a href="https://jira.corp.adobe.com/browse/DOCAC-13977">Link to DOCAC JIRA task</a> | <a href="https://jira.corp.adobe.com/browse/CJM-113125">Link to PRODUCT JIRA task</a>

* **Combine native and Adobe Campaign message actions** - Journey Optimizer now lets you combine Adobe Campaign v7/v8 message actions with native channel actions in the same journey.
  <a href="https://jira.corp.adobe.com/browse/DOCAC-13974">Link to DOCAC JIRA task</a> | <a href="https://jira.corp.adobe.com/browse/CJM-113103">Link to PRODUCT JIRA task</a>

* **Journey payload size validation in journeys** - Journey Optimizer now provides <strong>payload size validation</strong> to help ensure optimal performance and system stability. When building or publishing journeys, you receive clear warnings and errors if payload sizes approach or exceed recommended limits, along with actionable guidance to optimize your journey configuration. This proactive validation helps you identify potential issues early and maintain journey performance.
  <a href="https://jira.corp.adobe.com/browse/DOCAC-13840">Link to DOCAC JIRA task</a> | <a href="https://jira.corp.adobe.com/browse/CJM-122236">Link to PRODUCT JIRA task</a>

* **Multiple inbound actions in journeys** - To simplify your journey orchestration, you can now define <strong>multiple inbound actions</strong> in a single journey. Previously available in campaigns, this capability enables you to deliver multiple code-based experiences, In-app messages, Content Cards or web actions to different locations at the same time, each action containing a specific content.

  **Note**: Previously released in Limited Availability, this improvement is now available to all environments (General Availability).
  <a href="https://jira.corp.adobe.com/browse/DOCAC-13453">Link to DOCAC JIRA task</a> | <a href="https://jira.corp.adobe.com/browse/CJM-111916">Link to PRODUCT JIRA task</a>

#### Orchestrated campaigns

* **Select attributes and copy distribution values** - You can now select or copy values directly from the distribution of values view in orchestrated campaigns.
  <a href="https://jira.corp.adobe.com/browse/DOCAC-13973">Link to DOCAC JIRA task</a> | <a href="https://jira.corp.adobe.com/browse/CJM-105244">Link to PRODUCT JIRA task</a>

* **Data usage label inheritance for audiences** - <strong>Data usage labels</strong> applied in Adobe Experience Platform now automatically carry over when saving audiences in orchestrated campaigns, reducing manual DULE tagging.
  <a href="https://jira.corp.adobe.com/browse/DOCAC-13972">Link to DOCAC JIRA task</a> | <a href="https://jira.corp.adobe.com/browse/CJM-120769">Link to PRODUCT JIRA task</a>

* **Predefined retargeting filters** - To support easier retargeting for orchestrated campaign use cases, this release introduces new <strong>retargeting filters</strong>. These filters let you directly target audiences based on message engagement, such as sent, opened only, opened or clicked, or opened and clicked, and select the specific campaign or in-transition campaign you want to retarget.
  <a href="https://jira.corp.adobe.com/browse/DOCAC-13971">Link to DOCAC JIRA task</a> | <a href="https://jira.corp.adobe.com/browse/CJM-116701">Link to PRODUCT JIRA task</a>

* **Predefined filters with parameters** - You can now create <strong>filters with parameters</strong> in orchestrated campaigns for reusable, editable rules.
  <a href="https://jira.corp.adobe.com/browse/DOCAC-13970">Link to DOCAC JIRA task</a> | <a href="https://jira.corp.adobe.com/browse/CJM-115431">Link to PRODUCT JIRA task</a>

* **Message confirmation before send** - A <strong>confirmation step</strong> is now enabled by default before sending orchestrated campaigns to reduce accidental sends.
  <a href="https://jira.corp.adobe.com/browse/DOCAC-13927">Link to DOCAC JIRA task</a> | <a href="https://jira.corp.adobe.com/browse/CJM-87219">Link to PRODUCT JIRA task</a>

* **User-generated metadata support** - The <strong>executionMetadata helper function</strong> is now available in the personalization editor for Orchestrated Campaigns, enabling you to attach contextual information to any native action and store it in a dataset for export to external systems.
  <a href="https://jira.corp.adobe.com/browse/DOCAC-13923">Link to DOCAC JIRA task</a> | <a href="https://jira.corp.adobe.com/browse/CJM-112697">Link to PRODUCT JIRA task</a>

* **Restart button** - Orchestrated campaigns now include a <strong>restart button</strong> so you can quickly re-launch runs when needed before publishing the campaign.
  <a href="https://jira.corp.adobe.com/browse/DOCAC-13920">Link to DOCAC JIRA task</a> | <a href="https://jira.corp.adobe.com/browse/CJM-106020">Link to PRODUCT JIRA task</a>

* **Rate control support** - Orchestrated campaigns now support <strong>rate control</strong> to help you pace deliveries and align with volume constraints.
  <a href="https://jira.corp.adobe.com/browse/DOCAC-13764">Link to DOCAC JIRA task</a> | <a href="https://jira.corp.adobe.com/browse/CJM-113254">Link to PRODUCT JIRA task</a>

#### Permissions

* **Prevent self-approval for journeys and campaigns** - You can now require that creators cannot approve their own journeys or campaigns, improving <strong>separation of duties</strong> in approval workflows.
  <a href="https://jira.corp.adobe.com/browse/DOCAC-13472">Link to DOCAC JIRA task</a> | <a href="https://jira.corp.adobe.com/browse/CJM-99957">Link to PRODUCT JIRA task</a> | <a href="https://jira.corp.adobe.com/browse/CJM-95676">Link to PRODUCT JIRA task</a>

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
<p><a href="https://jira.corp.adobe.com/browse/DOCAC-13980">Link to DOCAC JIRA task</a> | <a href="https://jira.corp.adobe.com/browse/CJM-111882">Link to PRODUCT JIRA task</a></p>
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
<p><a href="https://jira.corp.adobe.com/browse/DOCAC-12902">Link to DOCAC JIRA task</a> | <a href="https://jira.corp.adobe.com/browse/CJM-99223">Link to PRODUCT JIRA task</a></p>
<p>Availability date: February 3, 2026</p>
</td>
</tr>
</tbody>
</table>
-->
