---
solution: Journey Optimizer
product: journey optimizer
title: Journey Optimizer 的预发行说明
description: Adobe Journey Optimizer 预发行说明
hide: true
feature: Release Notes
exl-id: 6e7d1300-8efd-4fdc-90e3-3ccdc3babd2f
TQID: https://experienceleague.adobe.com/951PJzmmITN1nSUapVomlYnPws9pS0TosI1Gl3R9yL4
product_v2:
  - id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2:
  - id: bb359667-ec7d-4d4b-8663-5850fc219d32
subfeature_v2:
  - id: a7b2bfc5-be71-4740-b371-76fa6be8df02
source-git-commit: 18306a37e360f359712c51b3755d2f5739bfc6f8
workflow-type: tm+mt
source-wordcount: 2943
ht-degree: 11%

---


# 预发行说明 {#e-release-notes}

Adobe Journey Optimizer 不断地提供新功能、对现有功能的增强和错误修复。 所有更改会在每月末整合到[发行说明](release-notes.md)中。

## 2026年9月预发行说明 {#sep-26-rn}

**以下预发行说明可能会在正式发行日期之前有所更改，恕不另行通知**。 一旦更改发布到生产环境，链接、屏幕和更新的文档就会发布。 虽然大多数更改将在发布日期交付，但其中一些更改可能会稍后推出 — 有关详细信息，请参阅为每个条目列出的发布日期。

另请参阅 [Adobe Experience Platform 预发行说明](https://experienceleague.adobe.com/zh-hans/docs/experience-platform/release-notes/pre-release-notes){target="_blank"}。

**发行日期**： 2026年9月22日至23日

### 内容管理 {#sep-26-content-management}

此版本中的内容管理即将提供以下功能。

<table>
<thead>
<tr>
<th><strong>CX Co-worker中的邮件复制和电子邮件设计插件</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>CX Co-worker中现在提供了两个新的插件，以简化从策略到部署的<strong>消息传递和电子邮件工作流</strong>：</p>
<p><strong>邮件复制插件</strong>：</p>
<ul>
<li>捕获营销活动简报并定义消息传送图、叙述弧和渠道角色。</li>
<li>构建一个跨渠道、接触点、区域设置、受众和变体定制的多维度内容矩阵。</li>
<li>生成全新副本，并利用Adobe Firefly生成、裁切和调整营销活动可视化图表。</li>
<li>允许就地进行内容评估，并将批准的资产直接同步回Journey Optimizer、Adobe Campaign V8和Marketo。</li>
</ul>
<p><strong>电子邮件设计插件</strong>：</p>
<ul>
<li>将营销目标、参考屏幕截图或图形设计链接转换为自定义布局计划和生产就绪型电子邮件HTML。</li>
<li>管理可重用的品牌资产、设计令牌和结构化电子邮件模板。</li>
<li>审核针对公司法规遵从性、可视设计质量和WCAG 2.1 AA辅助功能标准而汇编的电子邮件代码。</li>
<li>将批准的HTML直接导出到Adobe Journey Optimizer和Adobe Campaign。</li>
</ul>
<p><a href="https://jira.corp.adobe.com/browse/DOCAC-15642" target="_blank">DOCAC-15642</a></p>
<!-- GIF placeholder: to be added -->
<!-- Documentation link: TBD -->
</td>
</tr>
</tbody>
</table>

### 忠诚度 {#sep-26-loyalty}

在此版本中，“忠诚度”将实现以下功能和改进。

<table>
<thead>
<tr>
<th><strong>挑战机会</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>忠诚度绩效菜单现在包括<strong>机会选项卡</strong>，该选项卡显示人工智能检测到的趋势和差距，例如层级进展摩擦或挑战任务流失，每个都具有预计的影响，并且一键单击“使用AI创建”操作可生成可解决该问题的挑战。</p>
<p><a href="https://jira.corp.adobe.com/browse/DOCAC-15563" target="_blank">DOCAC-15563</a></p>
<!-- GIF placeholder: to be added -->
<!-- Documentation link: TBD -->
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>忠诚度事件映射更新</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>创建或编辑事件映射现在使用新的&#x200B;**可视化映射生成器**：选择架构，从可搜索的字段选择器中选择字段，将每个字段映射到具有每行连接状态的忠诚度事件字段，并预览自动生成的JSONata表达式，同时提供随时切换到手动JSONata编辑的选项。</p><p>此外，忠诚度管理员中的“事件定义”已重命名为“事件映射”，更新的列表视图可显示人类可读的体验事件架构名称。</p>
<p><a href="https://jira.corp.adobe.com/browse/DOCAC-15661" target="_blank">DOCAC-15661</a></p>
<!-- GIF placeholder: to be added -->
<!-- Documentation link: TBD -->
</td>
</tr>
</tbody>
</table>

* **CX Coworker忠诚度推荐技能** — 营销人员现在可以在CX Coworker的对话界面中直接请求&#x200B;**挑战机会**，根据真正的忠诚度计划趋势获得扎实的挑战想法，并在不离开聊天的情况下将其转化为实时挑战。 <a href="https://jira.corp.adobe.com/browse/DOCAC-15565" target="_blank">DOCAC-15565</a> <!-- Documentation link: TBD -->

### 入门 {#sep-26-onboarding}

此版本即将载入以下功能。

<table>
<thead>
<tr>
<th><strong>引导式电子邮件和历程功能（正式发布）</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>通过引导式功能，可帮助您将现有电子邮件内容和历程移入 Journey Optimizer，更轻松地从另一个营销平台过渡到 Adobe Journey Optimizer。 通过<strong>专用工作区</strong>，您可以重复使用现有的工作区，而不是从头开始重建。</p>
<p>此功能此前为有限发布版，现已可供所有环境使用（正式发布版）。</p>
<p><a href="https://jira.corp.adobe.com/browse/DOCAC-15330" target="_blank">DOCAC-15330</a></p>
<!-- GIF placeholder: to be added -->
<!-- Documentation link: TBD -->
</td>
</tr>
</tbody>
</table>

### 历程 {#sep-26-journeys}

在此版本中，历程中即将提供以下功能和改进。

<table>
<thead>
<tr>
<th><strong>CX Co-worker中的历程模拟（MCP和聊天）</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>CX Co-worker中的<strong>历程模拟技能</strong>可自动进行端到端历程验证，并让您轻松解释结果。 请注意，此功能当前仅支持快速模拟流程，不会完全取代Journey Optimizer手动模拟体验。</p>
<p><a href="https://jira.corp.adobe.com/browse/DOCAC-15374" target="_blank">DOCAC-15374</a></p>
<!-- GIF placeholder: to be added -->
<!-- Documentation link: TBD -->
</td>
</tr>
</tbody>
</table>

* 历程模拟中支持&#x200B;**历程模拟中的决策路径试验** - **路径试验**，它是决策中优化活动的一部分。 <a href="https://jira.corp.adobe.com/browse/DOCAC-15641" target="_blank">DOCAC-15641</a> <!-- Documentation link: TBD -->

* 历程模拟中支持&#x200B;**补充ID** - **历程模拟中现在支持补充ID**，允许您测试读取受众历程和事件触发历程的复杂用户方案。 <a href="https://jira.corp.adobe.com/browse/DOCAC-15448" target="_blank">DOCAC-15448</a> <!-- Documentation link: TBD -->

<table>
<thead>
<tr>
<th><strong>从CX Co-worker边栏创建历程</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>现在可直接从CX Co-worker右边栏使用AI</strong>创建<strong>历程，将以前的AI Assistant体验替换为用于生成历程的品牌再造集成入口点。</p>
<p><a href="https://jira.corp.adobe.com/browse/DOCAC-14898" target="_blank">DOCAC-14898</a></p>
<!-- GIF placeholder: to be added -->
<!-- Documentation link: TBD -->
</td>
</tr>
</tbody>
</table>

* **优化批处理受众评估等待逻辑** — 在&#x200B;**读取受众活动**&#x200B;中，历程中的“在批处理受众评估之后触发”选项现在等待已完成的任何批处理分段，确保历程使用运行的数据，而不是回退到旧快照。 如果未进行任何批量分段，则历程会使用最新的可用受众数据立即触发。 <a href="https://jira.corp.adobe.com/browse/DOCAC-15465" target="_blank">DOCAC-15465</a> <!-- Documentation link: TBD -->

* **将历程版本与CX Coworker进行比较** — 今天，查看两个历程版本之间的更改内容需要在Journey Optimizer节点中逐个手动比较它们 — 没有结构化的差异，这会使更改查看、审核和预发布检查变得缓慢且容易出错，尤其是当历程越来越复杂时。 此功能允许客户或AI代理通过CX Coworker Chat比较历程的任意两个版本，在不打开Journey Optimizer的情况下重新获得完全保真的&#x200B;**结构化差异** — 添加/删除/修改/移动了具有字段级详细信息、更改了连接、历程级属性更改和汇总计数的节点。 <a href="https://jira.corp.adobe.com/browse/DOCAC-15297" target="_blank">DOCAC-15297</a> <!-- Documentation link: TBD -->

* **历程画布中的内容预览** — 今天查看渠道内容需要一次单独打开一个节点 — 在具有多个渠道节点的历程中缓慢且容易出错，尤其是当个性化意味着检查每个节点的多个处理或变体时。 **内容预览**&#x200B;通过直接在画布中为每个渠道节点显示内容缩略图，并使用全屏模式检查并在处理方式和变体之间切换来消除该摩擦。 <a href="https://jira.corp.adobe.com/browse/DOCAC-15456" target="_blank">DOCAC-15456</a> <!-- Documentation link: TBD -->

* **检测到新历程异常警报** — 现在，当实时旅程的每日流量在事件条目、历程退出和事件发送之间偏离其历史基线或意外降至零时，新历程警报会警告您。 此警报当前仅在生产沙盒中可用。 <a href="https://jira.corp.adobe.com/browse/DOCAC-15545" target="_blank">DOCAC-15545</a> <!-- Documentation link: TBD -->

### 渠道 {#sep-26-channels}

此版本中的渠道即将提供以下功能和改进。

<table>
<thead>
<tr>
<th><strong>Android Live Updates的实时活动</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Journey Optimizer现在通过将<strong>实时活动支持扩展到Android</strong>来扩展其实时移动个性化功能。 您可以直接向用户交付实时进度更新，例如订单跟踪、航班状态、实时活动更新和实时体育赛事得分。</p>
<p>除了支持iOS Live活动之外，Journey Optimizer现在还跨其平台配置管理Android Live更新的临时推送令牌。 它使用API触发的营销活动和Headless API支持广播和事务性更新流。</p>
<p><a href="https://jira.corp.adobe.com/browse/DOCAC-15510" target="_blank">DOCAC-15510</a></p>
<!-- GIF placeholder: to be added -->
<!-- Documentation link: TBD -->
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>自定义出站渠道（正式发布）</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p><strong>自定义出站渠道</strong>允许管理员通过无代码渠道生成器将任何基于HTTP的出站消息渠道（如WeChat、Kakao Talk、Messenger或专有提供商）直接引入Journey Optimizer。 配置后，自定义渠道可在营销活动、历程和编排的营销活动中使用，并具有与原生渠道相同的完整功能集：使用表达式编辑器进行个性化、内容实验、预览和校样、开箱即用的报告以及同意和治理实施。</p>
<p>在此版本中，自定义出站渠道还获得了几项新功能：</p>
<ul>
<li>通过Journey Optimizer编辑器在自定义渠道有效载荷中使用Personalization Decisioning，与在基于代码的体验中一样。</li>
<li>将业务规则应用于自定义渠道，就像在本机渠道上一样。</li>
<li>在渠道列表中，为API触发的营销活动选择自定义渠道（这在以前是不可能的）。</li>
<li>为自定义渠道定义报表webhook并将其附加到渠道配置，以便您可以通过交互事件丰富Journey Optimizer报表。</li>
</ul>
<p><a href="https://jira.corp.adobe.com/browse/DOCAC-14037" target="_blank">DOCAC-14037</a></p>
<!-- GIF placeholder: to be added -->
<!-- Documentation link: TBD -->
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>覆盖电子邮件渠道配置设置</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>在构建历程和营销策划时，您现在可以直接在历程或营销策划操作级别覆盖从所选渠道配置派生的电子邮件参数。</p>
<p>这样，您就可以使用配置文件属性或上下文数据对电子邮件标头字段（<strong>来自名称</strong>、<strong>来自电子邮件前缀</strong>、<strong>回复名称</strong>和<strong>回复电子邮件</strong>）、执行地址和列表取消订阅值进行个性化设置，以便更精确地控制。 特别是，这允许发件人详细信息反映每个收件人的相关顾问、位置或分支，而不是通过单个公司地址路由所有发送。</p>
<p><a href="https://jira.corp.adobe.com/browse/DOCAC-14718" target="_blank">DOCAC-14718</a></p>
<!-- GIF placeholder: to be added -->
<!-- Documentation link: TBD -->
</td>
</tr>
</tbody>
</table>

* **自定义SMS BYOP身份验证灵活性** — 现在，在连接SMS提供商的OAuth设置时，您可以配置&#x200B;**自定义身份验证标头**，包括令牌在传出消息中的放置位置以及令牌请求本身的格式。 <a href="https://jira.corp.adobe.com/browse/DOCAC-15638" target="_blank">DOCAC-15638</a> <!-- Documentation link: TBD -->

### 编排的营销活动 {#sep-26-oc}

在此版本中，编排的营销活动中即将提供以下功能和改进。

<table>
<thead>
<tr>
<th><strong>或加入编排的营销活动的活动</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>现在，编排的营销活动中的<strong>加入活动</strong>支持AND和OR加入条件。 使用OR逻辑时，完成任意一个上游分支（而非所有上游分支）的用户档案会沿着单个共享下游路径继续。 这使得在画布上直接建模“如果A、B或C，则执行此操作”模式成为可能，而无需跨独立分支重复下游步骤。</p>
<p><a href="https://jira.corp.adobe.com/browse/DOCAC-15020" target="_blank">DOCAC-15020</a></p>
<!-- GIF placeholder: to be added -->
<!-- Documentation link: TBD -->
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>针对编排的活动发出警报</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>现在，编排的营销活动通过跨历程和营销活动使用的同一警报框架支持<strong>自动警报</strong>。 当活动执行失败、超时或需要确认时，将触发警报，每个警报都包括发生的情况、时间、位置和指向监控视图的直接链接，并按严重性分类，以便团队无需手动UI检查即可优先处理。</p>
<p><a href="https://jira.corp.adobe.com/browse/DOCAC-14886" target="_blank">DOCAC-14886</a></p>
<!-- GIF placeholder: to be added -->
<!-- Documentation link: TBD -->
</td>
</tr>
</tbody>
</table>

* 用于编排营销活动的&#x200B;**LINE渠道** - LINE现在作为编排营销活动中的本机出站渠道以及电子邮件、短信和推送一起提供。 您可以直接从营销活动画布构建和投放LINE消息，包括文本、贴图、图像、视频、位置数据和Flex消息，在日本和APAC等LINE市场占主导地位的市场支持促销、交易和持续参与用例。 此功能以前以“有限可用”的形式发布，现在已正式发布。 <a href="https://jira.corp.adobe.com/browse/DOCAC-15102" target="_blank">DOCAC-15102</a> <!-- Documentation link: TBD -->

* **新的协调营销活动监控API** — 新&#x200B;**API规范**&#x200B;现在可用于协调营销活动，允许您以编程方式创建、管理和触发协调营销活动，从而与外部系统和自动化管道进行更深度的集成。 <a href="https://jira.corp.adobe.com/browse/DOCAC-14308" target="_blank">DOCAC-14308</a> <!-- Documentation link: TBD -->

* **直接联接UX改进** — 从相关收藏集添加属性时，您现在可以在三种联接模式（一种新默认模式，用于警告笛卡尔产品对性能的潜在影响）以及现有的“聚合”和“高级”模式之间进行选择，从而更容易在构建查询之前了解查询的权衡。 <a href="https://jira.corp.adobe.com/browse/DOCAC-15675" target="_blank">DOCAC-15675</a> <!-- Documentation link: TBD -->

* **在编排的营销活动中包含关系数据的条件内容** — 在Email Designer中为编排的营销活动构建条件内容时，您现在可以直接基于&#x200B;**关系数据**&#x200B;构建条件，而不只是标准配置文件属性，例如与配置文件关联记录。 这弥补了原始版本的一个空白，因此营销人员可以直观地构建这些条件，而无需工程方面的帮助。 <a href="https://jira.corp.adobe.com/browse/DOCAC-15679" target="_blank">DOCAC-15679</a> <!-- Documentation link: TBD -->

### 营销活动 {#sep-26-campaigns}

此版本中的营销活动即将推出以下功能和改进。

<table>
<thead>
<tr>
<th><strong>Action Campaigns (Beta)中的入站体验模拟</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>您现在可以在上线之前在“操作营销活动”中模拟入站渠道操作。 使用模拟模式通过模拟用户测试您的配置并预览渲染的体验，包括生成的 URL 和 QR 代码，因此您可以端到端地验证规则、决策和内容渲染。</p>
<p>此功能当前为 Private Beta 版，仅向有限的组织提供。 请联系 Adobe 代表以获取更多信息。</p>
<p><a href="https://jira.corp.adobe.com/browse/DOCAC-15166" target="_blank">DOCAC-15166</a></p>
</td>
</tr>
</tbody>
</table>

* **营销活动文件夹** — 您现在可以将营销活动组织到&#x200B;**文件夹**&#x200B;中，以改进界面中的导航和管理。 <a href="https://jira.corp.adobe.com/browse/DOCAC-15098" target="_blank">DOCAC-15098</a> <!-- Documentation link: TBD -->

### 决策 {#sep-26-decisioning}

在此版本中，决策中即将提供以下功能和改进。

<table>
<thead>
<tr>
<th><strong>Web渠道中的决策支持</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>决策现在可用于网页渠道。 您可以直接在 Web 可视编辑器中使用决策策略，向每位访客提供最相关的产品建议。</p>
<p><a href="https://jira.corp.adobe.com/browse/DOCAC-11548" target="_blank">DOCAC-11548</a></p>
<!-- GIF placeholder: to be added -->
<!-- Documentation link: TBD -->
</td>
</tr>
</tbody>
</table>

* 从CX Coworker生成&#x200B;**决策规则** — 以前通过右边栏提供的&#x200B;**AI辅助决策规则生成**&#x200B;体验现在可通过CX Coworker访问，该功能取代了右边栏，作为使用AI生成规则的方式。 <a href="https://jira.corp.adobe.com/browse/DOCAC-15290" target="_blank">DOCAC-15290</a> <!-- Documentation link: TBD -->

### 直邮 {#sep-26-direct-mail}

此版本中的直邮即将提供以下功能和改进。

* **自动拆分大文件** — 现在，当直邮文件大约超过20 GB时，可以自动将其拆分为多个部分，或者通过在文件路由配置中选择目标文件大小来手动拆分。 可选的JSON清单文件描述了所有生成的部分。 <a href="https://jira.corp.adobe.com/browse/DOCAC-15677" target="_blank">DOCAC-15677</a> <!-- Documentation link: TBD -->

* **受众限制提高** — 直邮渠道受众限制已从300万个配置文件提高至1亿个配置文件，使您可定位更多受众，而不会出现文件创建错误。 <a href="https://jira.corp.adobe.com/browse/DOCAC-15676" target="_blank">DOCAC-15676</a> <!-- Documentation link: TBD -->

### 电子邮件设计器 {#sep-26-email-designer}

此版本中的Email Designer即将提供以下功能和改进。

<table>
<thead>
<tr>
<th><strong>电子邮件主题变体的独立深色模式样式</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>电子邮件主题现在支持深色模式的独立样式。 在主题生成器中，可以为给定变量打开深色模式以生成专用深色模式样式表，该样式表与浅色模式样式分开进行编辑 — 在一个模式中所做的更改不再覆盖另一个模式。 在电子邮件和模板编辑器中，通过桌面和移动设备视图选项旁边的新预览切换，可在深色模式下预览内容。</p>
<p><a href="https://jira.corp.adobe.com/browse/DOCAC-15663" target="_blank">DOCAC-15663</a></p>
<!-- GIF placeholder: to be added -->
<!-- Documentation link: TBD -->
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>直接从Email Designer中的PSD文件导入Dynamic Media模板</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>电子邮件Designer的Dynamic Media组件现在可让您在浏览现有Dynamic Media模板之外，直接导入Photoshop (PSD)文件作为新模板。 将PSD文件拖放到组件中，Adobe Journey Optimizer会自动将其转换为存储在Dynamic Media中的Dynamic Media模板 — 无需手动转换或穿过Adobe Experience Manager来回转换。 导入模板后，您可以使用内置的Dynamic Media编辑器编辑该模板，这与电子邮件Designer中的Adobe Express内容具有相同的体验。</p>
<p><a href="https://jira.corp.adobe.com/browse/DOCAC-15664" target="_blank">DOCAC-15664</a></p>
<!-- GIF placeholder: to be added -->
<!-- Documentation link: TBD -->
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>电子邮件Designer中的新表组件</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Email Designer现在包含内置<strong>表组件</strong>，允许您直接在电子邮件中构建行和列中的内容。 将组件拖放到画布上，自定义行和列的数量，并单独设置每个单元格的样式，以创建清晰、有序的布局，而无需依赖自定义HTML。</p>
<p><a href="https://jira.corp.adobe.com/browse/DOCAC-15093" target="_blank">DOCAC-15093</a></p>
<!-- GIF placeholder: to be added -->
<!-- Documentation link: TBD -->
</td>
</tr>
</tbody>
</table>

* **电子邮件主题中自定义字体的回退字体** — 您现在可以为通过电子邮件主题应用的任何自定义(Web)字体定义回退字体。 如果订阅者的电子邮件客户端不支持该自定义字体，Adobe Journey Optimizer会自动显示指定的后备字体，而不是将选项保留给电子邮件客户端的默认字体。 这样可使电子邮件排版更接近于您的品牌准则，并减少电子邮件客户端中字体渲染不一致的情况。 <a href="https://jira.corp.adobe.com/browse/DOCAC-15662" target="_blank">DOCAC-15662</a> <!-- Documentation link: TBD -->

### 报表 {#sep-26-reporting}

以下功能即将在此版本中报告。

<table>
<thead>
<tr>
<th><strong>Data Management中的新入站监控图</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>您现在可以直接从<strong>数据管理&gt;监控&gt; Edge</strong>监控入站数据运行状况，新增了6个图表，分别涵盖吞吐量、延迟和建议事件：</p>
<ul>
<li><strong>AJO入站吞吐量</strong> — 一段时间的总体入站吞吐量（每秒记录数）。</li>
<li><strong>AJO入站吞吐量细分</strong> — 按位置细分的入站吞吐量。</li>
<li><strong>AJO入站延迟</strong> — 入站请求延迟（以毫秒为单位），按值分布（P50、P90等）划分。</li>
<li><strong>AJO入站建议事件吞吐量</strong> — 建议事件的吞吐量（当用户与、查看或触发个性化优惠时生成的跟踪信号）。</li>
<li><strong>按渠道列出的AJO入站建议事件吞吐量</strong> — 按入站渠道（CBE、应用程序内、内容卡）划分的建议事件吞吐量。</li>
<li><strong>按事件类型</strong>列出的AJO入站建议事件吞吐量 — 按事件类型（已取消、已禁止、已显示、已触发、已交互、已发送）划分的建议事件吞吐量。</li>
</ul>
<p><a href="https://jira.corp.adobe.com/browse/DOCAC-15680" target="_blank">DOCAC-15680</a></p>
<!-- GIF placeholder: to be added -->
<!-- Documentation link: TBD -->
</td>
</tr>
</tbody>
</table>

### 管理 {#sep-26-administration}

以下提醒适用于此版本中的管理。

* **数据集的生存时间(TTL)护栏 — 现有沙盒** — 从2026年10月1日起，将在现有客户沙盒和组织上强制实施Journey Optimizer系统生成的数据集的生存时间(TTL)护栏（配置文件存储为90天，数据湖为13个月）。 <a href="https://jira.corp.adobe.com/browse/DOCAC-15239" target="_blank">DOCAC-15239</a> <!-- Documentation link: TBD -->

* **即将更改受众组合扩充受众** — 在10月版本（10月底）期间，Journey Optimizer将停止使用或引用源数据集不具有&#x200B;**主标识描述符**&#x200B;的受众组合受众的历程。 从那时起，历程中仅支持使用主标识描述符构建的受众组合受众。 如果您需要这些历程保持活动状态，请联系您的Adobe代表 — 我们的产品团队可以帮助您进行迁移。 <a href="https://jira.corp.adobe.com/browse/DOCAC-15690" target="_blank">DOCAC-15690</a> <!-- Documentation link: TBD -->

### 可用性改进 {#sep-26-usability}

* **内容模拟体验中的可用性改进** — 现在，通过新的内容模拟体验，您可以命名和组织变体以便轻松比较，直接从每个信息卡复制或删除变体详细信息，根据需要查看完整属性路径和每信息卡渠道配置，以及通过更突出的上传按钮上传您自己的CSV、JSON或JSONL配置文件。 <a href="https://jira.corp.adobe.com/browse/DOCAC-15570" target="_blank">DOCAC-15570</a>


