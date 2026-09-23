---
solution: Journey Optimizer
product: journey optimizer
title: Journey Optimizer 的预发行说明
description: Adobe Journey Optimizer 预发行说明
feature: Release Notes
exl-id: 6e7d1300-8efd-4fdc-90e3-3ccdc3babd2f
TQID: https://experienceleague.adobe.com/951PJzmmITN1nSUapVomlYnPws9pS0TosI1Gl3R9yL4
product_v2:
  - id: cb954087-f4fc-4456-afb9-e939cabcdc79
    internal-label: Journey Optimizer
feature_v2:
  - id: bb359667-ec7d-4d4b-8663-5850fc219d32
    internal-label: Administration
subfeature_v2:
  - id: a7b2bfc5-be71-4740-b371-76fa6be8df02
    internal-label: Journey Optimizer release notes
source-git-commit: 7e153a072cacd37ec3837c7607ce28fbd565cc4a
workflow-type: tm+mt
source-wordcount: '3111'
ht-degree: 8%
---

# 预发行说明 {#e-release-notes}

Adobe Journey Optimizer 不断地提供新功能、对现有功能的增强和错误修复。 所有更改会在每月末整合到[发行说明](release-notes.md)中。

## 2026年9月预发行说明 {#sep-26-rn}

**以下预发行说明可能会在正式发行日期之前有所更改，恕不另行通知**。 一旦更改发布到生产环境，链接、屏幕和更新的文档就会发布。 虽然大多数更改将在发布日期交付，但其中一些更改可能会稍后推出 — 有关详细信息，请参阅为每个条目列出的发布日期。

另请参阅 [Adobe Experience Platform 预发行说明](https://experienceleague.adobe.com/zh-hans/docs/experience-platform/release-notes/pre-release-notes){target="_blank"}。

**发行日期**： 2026年9月22日至23日

>[!BEGINSHADEBOX]

**本月CX Enterprise Coworker的新增功能**

此版本提供了几项新的和改进的[同事](../start/ai-features.md#cx-coworker)功能和技能，此处列出了这些功能和技能，以供大家了解。 每项资料也详见下文其相关章节。

* [CE渠道内容插件](#sep-26-content-management) — 一个新插件，可在同事中将HTML的营销活动副本、图像和电子邮件技能融为一体，从营销活动简报到生产就绪的副本和HTML。
* [忠诚度推荐技能](#sep-26-loyalty) — 直接在同事的对话界面中请求挑战机会，并在不离开聊天的情况下将其转换为实时挑战。
* [历程模拟](#sep-26-journeys) — 自动进行端到端历程验证并直接在协作程序中解释结果。
* [从同事边栏创建历程](#sep-26-journeys) — 使用AI直接从同事右边栏生成旅程，替换以前的AI助手体验。
* [比较历程版本](#sep-26-journeys) — 通过同事聊天获取任意两个历程版本之间的完全保真、结构化差异。
* [保健分析技能](#sep-26-journeys) — 通过推荐的修复，扫描活动和草稿历程中的配置损坏、静默失败、资产老化或未使用等。
* [业务绩效分析技能](#sep-26-journeys) — 分析历程绩效并从聊天中获取具体的优化建议。

>[!ENDSHADEBOX]

### 内容管理 {#sep-26-content-management}

此版本中的内容管理即将提供以下功能。

<table>
<thead>
<tr>
<th><strong>Co-worker中的“渠道内容”插件</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Co-worker中现在提供新的<strong>渠道内容</strong>插件，可在从策略到部署的一个插件下将活动副本、图像和组合电子邮件HTML技能整合在一起。 **Channel Content**&#x200B;插件下提供了以下技能：</p>
<ul>
<li><strong>编排内容创作</strong>。</li>
<li><strong>浏览内容策略</strong></li>
<li><strong>内容摘要</strong></li>
<li><strong>生成内容</strong></li>
<li><strong>检查内容准备情况</strong></li>
<li><strong>修订和重新生成内容</strong></li>
<li><strong>生成图像</strong></li>
<li><strong>评估内容设计</strong></li>
<li><strong>保存渠道内容</strong></li>
<li><strong>从Figma构建电子邮件</strong></li>
<li><strong>品牌查找</strong> </li>
</ul>
<!-- GIF placeholder: to be added -->
<!-- Documentation link: TBD -->
</td>
</tr>
</tbody>
</table>

### 集成 {#sep-26-integrations}

此版本中的集成提供了以下功能。

* **Experience Manager片段的动态令牌替换** - Experience Manager内容片段引用现在支持&#x200B;**tokenSubstitution**&#x200B;属性。 当设置为`false`时，片段的字段中的个性化设置将直接解析，而无需引用中的令牌映射。 默认值为`true`，这将保留现有行为。

  此功能仅面向一部分组织（限量发布）。 要获得访问权限，请与 Adobe 代表联系。

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
<!-- GIF placeholder: to be added -->
<!-- Documentation link: TBD -->
</td>
</tr>
</tbody>
</table>

* **同事忠诚度推荐技能** — 营销人员现在可以在同事的对话界面中直接请求&#x200B;**挑战机会**，根据真正的忠诚度计划趋势获得扎实的挑战想法，并在不离开聊天的情况下将其转化为实时挑战。

* **内容卡个性化编辑器中的挑战域** — 内容卡个性化编辑器现在支持&#x200B;**挑战**&#x200B;作为域，允许您在创作内容卡个性化时访问挑战元数据。 这样可以更轻松地为挑战的每个阶段（启动、进行中和结束）创建量身定制的内容，而无需自定义代码。



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
</td>
</tr>
</tbody>
</table>

### 受众 {#sep-26-audiences}

以下提醒适用于此版本中的受众。

* **即将更改受众组合扩充受众** — 在10月版本（10月底）中，Journey Optimizer将停止使用或引用源数据集不具有&#x200B;**主身份描述符**&#x200B;的受众组合受众的历程和营销活动。 从那时起，历程和营销活动仅支持使用主身份描述符构建的受众组合受众。 如果您需要这些历程或营销活动保持活动状态，请联系您的Adobe代表 — 我们的产品团队可以帮助您进行迁移。<!-- Documentation link: TBD -->

### 历程 {#sep-26-journeys}

在此版本中，历程中即将提供以下功能和改进。

<table>
<thead>
<tr>
<th><strong>Co-worker中的历程模拟</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Co-worker中的<strong>历程模拟技能</strong>可自动进行端到端历程验证，并可让您轻松解释结果。 请注意，此功能当前仅支持快速模拟流程，不会完全取代Journey Optimizer手动模拟体验。</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>从同事边栏创建历程</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>现在可直接从同事的右边栏使用AI</strong>创建<strong>历程，将以前的AI Assistant体验替换为用于生成旅程的品牌再造集成入口点。</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>历程警报的AI推荐卡</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>当历程警报触发时，Journey Optimizer主页现在会显示<strong>AI推荐卡</strong>，其中涵盖<strong>历程自定义操作失败</strong>和<strong>检测到历程异常</strong>警报。 选择卡片会打开历程，其中右边栏预先填充了已执行的分析。</p>
<!-- GIF placeholder: to be added -->
<!-- Documentation link: TBD -->
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>入站活动停用历程活动</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>历程画布中新增的<strong>入站活动停用</strong>活动允许您直接从历程中删除最多五个入站活动或体验的个人资料，从而将入站取消资格从历程退出中分离，以实现更高级的跨渠道编排。</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>历程画布中的内容预览</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>现在查看渠道内容需要一次单独打开一个节点 — 在具有许多渠道节点的历程中，速度慢且容易出错，尤其是个性化意味着检查每个节点的多个处理或变体时。 <strong>内容预览</strong>通过直接在画布中为每个渠道节点显示内容缩略图，并使用全屏模式检查并在处理方式和变体之间切换来消除该摩擦。</p>
</td>
</tr>
</tbody>
</table>

* 历程模拟中支持&#x200B;**补充ID** - **历程模拟中现在支持补充ID**，允许您测试读取受众历程和事件触发历程的复杂用户方案。

* **对Audience Qualification历程的跳转支持** — 以&#x200B;**Audience Qualification**&#x200B;开始的历程现在可以使用&#x200B;**跳转**&#x200B;活动进入基于事件的开始历程；跳转到基于Audience Qualification的历程仍然不受支持。

* **与同事比较历程版本** — 今天，查看两个历程版本之间的更改内容需要在Journey Optimizer节点中逐个节点手动比较它们 — 没有结构化的差异，这会使更改查看、审核和发布前检查变得缓慢且容易出错，尤其是当历程越来越复杂时。 此功能允许客户或AI代理通过Co-worker Chat比较历程的任意两个版本，在不打开Journey Optimizer的情况下，重新获得全保真&#x200B;**结构化差异** — 添加/删除/修改/移动了具有字段级详细信息、更改了连接、历程级属性更改和汇总计数的节点。

* **减少等待和事件活动的步骤事件** — 不再为&#x200B;**等待**&#x200B;活动和&#x200B;**事件**&#x200B;活动生成步骤事件，因为在该活动中实际未处理配置文件。<!-- DRAFT: pending DOCAC sub-task under DOCAC-15691, see CJM-165835 -->
<!-- Documentation link: TBD -->

* **自定义报告的练习步骤事件抑制** — 作为步骤事件优化的一部分，Journey Optimizer现在在历程练习期间停止生成某些不可报告的步骤事件。 这仅会影响基于这些模拟运行步骤事件类型构建的自定义报表。 如果您受到影响，请重新触发模拟以重新生成数据。

* **卫生分析同事技能** — 同事中的新卫生分析技能将扫描您的活动和草稿历程，以查找中断的配置、静默失败、损坏或未使用的资产（例如过时的草稿历程、孤立的数据源和持续的自定义操作错误）并直接从聊天中呈现建议的修复。<!-- Documentation link: TBD -->

* **业务绩效分析同事技能** — 同事中的新&#x200B;**业务绩效分析**&#x200B;技能可分析您的历程执行情况、说明性能较低的方面，并建议具体的优化，例如重新参与等待、渠道升级和发送时间优化。 <!-- Documentation link: TBD -->

* **历程属性中的自动事件恢复超时** -历程属性现在包括&#x200B;**设置事件恢复超时**&#x200B;设置：默认情况下，受影响的旅程事件在服务中断后最多72小时内自动重放，而无需执行任何操作。 您可以打开此设置来控制对时间敏感的历程的重播窗口（0-72小时）。 现有的&#x200B;**Timeout或error**&#x200B;字段也已重命名为&#x200B;**自定义操作/IDS操作超时**，以避免这两个设置混淆。

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
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Android推送通知模板改进</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Android推送通知以前通过单个固定布局呈现：图像始终居中裁剪，长正文文本被截断。 此版本在创作时引入了模板选取器，允许营销人员控制Android推送通知的布局。</p>
<p>提供了以下改进：</p>
<ul>
<li><b>布局选择</b>：在创作Android推送时新增了推送通知布局选取器（标准/展开）。</li>
<li><b>带有“显示整个图像”的标准布局</b>：选择裁剪为填充与缩放为适合。</li>
<li><b>扩展的布局</b>：无截断的多行正文文本，加上可选的大图标缩略图。</li>
<li><b>折叠的正文（展开的布局）</b>：为折叠状态设置单独的、较短的正文文本。</li>
</ul>
</td>
</tr>
</tbody>
</table>


* **自定义SMS BYOP身份验证灵活性** — 现在，在连接SMS提供商的OAuth设置时，您可以配置&#x200B;**自定义身份验证标头**，包括令牌在传出消息中的放置位置以及令牌请求本身的格式。

* **直邮 — 自动拆分大文件** — 现在，当直邮文件大约超过20 GB时，可以自动将其拆分为多个部分，或者通过在文件路由配置中选择目标文件大小来手动拆分。

* **直邮 — 增加了受众限制** — 直邮渠道受众限制已从300万个配置文件增加到1亿个配置文件，使您可定位更多受众，而不会出现文件创建错误。

### 电子邮件渠道 {#sep-26-email-channel}

此版本中的电子邮件渠道即将提供以下功能和改进。

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
</td>
</tr>
</tbody>
</table>

* **在电子邮件操作级别覆盖禁止列表现在** -Journey Optimizer允许您在历程和营销活动中直接在电子邮件操作级别覆盖禁止列表行为。 这允许团队在需要专用发送配置的操作性或合规性关键通信方面有更大的灵活性，同时保留所有其他发送的现有全局禁止列表控制。 此增强功能可帮助组织准确处理异常场景，而无需更改其更广泛的抑制治理模型。

* **电子邮件创作中的URL语法验证** — 现在，Journey Optimizer会验证电子邮件创作流程中较早的URL，并在检测到语法格式错误时显示更清晰的指导。 这有助于作者在最终确定之前捕获问题、减少发布错误并提高投放可信度。

### 电子邮件设计器 {#sep-26-email-designer}

此版本中的Email Designer即将提供以下功能和改进。

<table>
<thead>
<tr>
<th><strong>对电子邮件主题变体的深色模式支持</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>电子邮件主题现在支持深色模式，因此每个颜色变体都可以呈现一种量身定制的外观，适合在启用深色模式的客户端中查看电子邮件的收件人。</p>
<p>启用后，将自动为每个变体生成一个默认的深色调色板，您可以使用不同的调色板或您自己的自定义颜色进一步对其进行自定义 — 这与浅色模式设计无关，因此在一个模式下所做的更改不会影响另一个模式。</p>
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
</td>
</tr>
</tbody>
</table>

* **电子邮件主题中自定义字体的回退字体** — 您现在可以为通过电子邮件主题应用的任何自定义(Web)字体定义回退字体。 如果订阅者的电子邮件客户端不支持该自定义字体，Adobe Journey Optimizer会自动显示指定的后备字体，而不是将选项保留给电子邮件客户端的默认字体。 这样可使电子邮件排版更接近于您的品牌准则，并减少电子邮件客户端中字体渲染不一致的情况。

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
</td>
</tr>
</tbody>
</table>

* 用于编排营销活动的&#x200B;**LINE渠道** - LINE现在作为编排营销活动中的本机出站渠道以及电子邮件、短信和推送一起提供。 您可以直接从营销活动画布构建和投放LINE消息，包括文本、贴图、图像、视频、位置数据和Flex消息，在日本和APAC等LINE市场占主导地位的市场支持促销、交易和持续参与用例。 此功能以前以“有限可用”的形式发布，现在已正式发布。

* **新的协调营销活动监控API** — 新&#x200B;**API规范**&#x200B;现在可用于协调营销活动，允许您以编程方式创建、管理和触发协调营销活动，从而与外部系统和自动化管道进行更深度的集成。

* **直接联接UX改进** — 从相关收藏集添加属性时，您现在可以在三种联接模式（一种新默认模式，用于警告笛卡尔产品对性能的潜在影响）以及现有的“聚合”和“高级”模式之间进行选择，从而更容易在构建查询之前了解查询的权衡。

* **营销活动编排监控** — 新的用户界面现在可用于跟踪编排的营销活动分段所使用的关系存储数据的摄取状态和新鲜度。 它让您能够直接查看提供给批处理受众的数据的运行状况。 Adobe Experience Platform的“监控”仪表板中新增的Campaign Orchestration选项卡可显示关系存储数据流（摄取/更新/删除/失败/跳过的记录）的运行状况，并带有向下钻取图形和每个数据流/数据集划分，包括族系。


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
</td>
</tr>
</tbody>
</table>

### 管理 {#sep-26-administration}

以下提醒适用于此版本中的管理。

* **数据集的生存时间(TTL)护栏 — 现有沙盒** — 从2026年10月1日起，将在现有客户沙盒和组织上强制实施Journey Optimizer系统生成的数据集的生存时间(TTL)护栏（配置文件存储为90天，数据湖为13个月）。

### 可用性改进 {#sep-26-usability}

* **内容模拟体验中的可用性改进** — 现在，通过新的内容模拟体验，您可以命名和组织变体以便轻松比较，直接从每个信息卡复制或删除变体详细信息，根据需要查看完整属性路径和每信息卡渠道配置，以及通过更突出的上传按钮上传您自己的CSV、JSON或JSONL配置文件。

* **片段验证警报中的AI概述** — 片段验证警报对话框现在包含一个AI概述，其中汇总并说明了验证问题（例如，格式错误的表达式、缺少配置文件字段和无效的JSON），以便用户更快地进行故障排除。

* **促销活动、历程和编排的促销活动的统一日历** — 历程和促销活动的日历视图现在从单独的清单中移到一个统一的左边栏可访问菜单中，两者都显示在一个组合视图中。

