---
solution: Journey Optimizer
product: journey optimizer
title: 发行说明
feature: Release Notes
role: User
level: Beginner, Intermediate
description: Adobe Journey Optimizer 发行说明
exl-id: 06fa956a-b500-416e-9d42-b683c328e837
source-git-commit: b53c28405e453be3767f05e2c7a7a1b2e69d0416
workflow-type: tm+mt
source-wordcount: '1537'
ht-degree: 29%

---

# 发行说明 {#release-notes}

>[!CONTEXTUALHELP]
>id="ajo_homepage_card1"
>title="新增功能"
>abstract="**Adobe Journey Optimizer** 不断地提供新功能、对现有功能的增强和错误修复。会在每月的最后一周将所有更改整合到发行说明中。"

[!DNL Adobe Journey Optimizer] 遵循持续交付模型，允许 Adobe 持续交付新功能、增强功能和修复。此方法支持以可扩展的方式分阶段推出各种功能，以确保所有环境的性能和稳定性。

由于此模型，在每月发行版本之间会更新发行说明。有关发行周期和可用性阶段的完整详细信息，请参阅 [Journey Optimizer 发行周期](releases.md)。

[!DNL Adobe Journey Optimizer] 原生构建于 [!DNL Adobe Experience Platform] 之上并继承了其所具备的最新创新技术和改进。在 [Adobe Experience Platform 发行说明](https://experienceleague.adobe.com/docs/experience-platform/release-notes/latest.html?lang=zh-Hans){target="_blank"}中进一步了解这些更改。

## 2026年2月发行说明 {#feb-26-01-rn}

**以下预发行说明可能会在正式发行日期之前有所更改，恕不另行通知**。链接、屏幕和更新的文档会于发布日期在发行说明中发布。

另请参阅 [Adobe Experience Platform 预发行说明](https://experienceleague.adobe.com/zh-hans/docs/experience-platform/release-notes/pre-release-notes){target="_blank"}。

**发布日期**：2026 年 2 月 17-18 日

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
<p>此功能此前为有限发布版，现已可供所有环境使用（正式发布版）。</p>
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
<p>发布日期： 2026年2月13日</p>
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
</td>
</tr>
</tbody>
</table>

### 改进 {#feb-26-01-improv}

此版本包含的改进如下所述。

#### 配置

* **历程表达式中的体验事件用法** — 从2026年4月1日开始，过去90天内未使用此功能的组织将不再支持在历程表达式中使用体验事件属性。 自2025年7月8日以来，此功能已不适用于新客户组织。 有关替代项，请参阅历程中的[体验事件查找](../building-journeys/exp-event-lookup.md)。


* **子域委派方法切换** — 您现在可以从一个<strong>子域委派</strong>方法切换到另一个。 这使您能够使用<strong>CNAME委派</strong>模式将域迁移到<strong>自定义委派</strong>方法，以遵守您公司的安全策略。

  **注意**：此功能仅适用于一组组织（<strong>有限可用性</strong>）。 要获得访问权限，请与 Adobe 代表联系。


#### 电子邮件设计器

* **使用品牌主题将图像转换为电子邮件模板** — 在Journey Optimizer中将图像转换为电子邮件模板时，现在可以使用<strong>主题</strong>作为输入，以便生成的HTML遵循<strong>品牌参数</strong>。 样式（如背景颜色、按钮颜色、字体、行距、边距和填充）会自动应用，从而减少手动设计工作，并提供只需少量编辑即可使用的模板。


* **使用新颜色标签更新品牌** - <strong>品牌指南</strong>有助于确保在所有接触点上始终如一地呈现您的品牌。 新的<strong>颜色板块</strong>定义了您品牌颜色体系的标准，介绍了如何在不同体验中选择、组织和应用颜色。 它确保对主色、辅色、个性色和中性色使用的一致性，以打造一个有粘性、可访问和有辨识度的品牌标识。


#### AI

* **自定义Firefly模型与第三方图像生成模型的集成** — 实现标准和自定义<strong>Firefly模型</strong>以及批准的<strong>第三方图像模型</strong>（例如，NanoBanana）的无缝集成，以便在生成图像时提供更大的灵活性、控制力以及品牌一致性。 这允许您为每个用例选择最佳模型：可满足一般需求的标准Firefly、用于品牌内生成的自定义Firefly，或针对专用或实验场景的批准的第三方模型。


#### 体验决策

* 在Decisioning中使用Adobe Experience Platform数据的&#x200B;**Edge入站支持** - <strong>Experience Platform数据查找</strong>的Decisioning支持现在包括<strong>边缘入站</strong>渠道用例。 该功能仍保持有限可用性；尚未宣布底层数据查找功能的正式可用性(依赖于AEP/产品)。

  **注意**：此功能仅适用于一组组织（<strong>有限可用性</strong>）。 要获得访问权限，请与 Adobe 代表联系。


* **基于代码的体验渠道中的Experience Decisioning预览** — 在使用<strong>基于代码的体验</strong>渠道配置<strong>Experience Decisioning</strong>时，您现在可以预览<strong>决策项</strong>。 上线之前，可以直接在创作界面中预览。


* **优惠排名AI模型可观察性** — 现在，通过Journey Optimizer可在Decisioning中监视<strong>AI模型</strong>的<strong>运行状况</strong>、<strong>培训状态</strong>和<strong>性能</strong>，以便验证培训是否成功、排除故障并了解对结果的影响。 此功能仅适用于个性化优化模型（不适用于自动优化）。


* **将片段附加到决策项** - Journey Optimizer现在提供将<strong>片段</strong>附加到<strong>决策项</strong>的功能，这些功能可通过<strong>决策策略</strong>在基于代码的体验营销活动中使用。

  **注意**：以前以有限可用性发布，此功能现在可用于所有环境（正式发布）。

  发布日期：2026年2月12日。


#### 历程

* **历程中的多个入站操作** — 为简化历程编排，您现在可以在单个历程中定义多个<strong>入站操作</strong>。 此功能以前在营销活动中提供，它使您能够同时将多个<strong>基于代码的体验</strong>、<strong>应用程序内消息</strong>、<strong>内容卡</strong>或<strong>Web操作</strong>传送到不同的位置，每个操作都包含特定内容。

  **注意**：以前以有限可用性发布，此功能现在可用于所有环境（正式发布）。


* **SMS Webhook** - 现在，所有短信服务提供商都支持 <strong>Webhook</strong>。 您可以根据预期目的配置每个webhook：<strong>入站webhook</strong>以捕获传入邮件，以及<strong>反馈webhook</strong>以接收送达回执、状态更新和其他与邮件相关的事件。 [了解详情](../sms/sms-webhook.md)

  发布日期：2026年2月2日。