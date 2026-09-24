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
    internal-label: Journey Optimizer
feature_v2:
  - id: bb359667-ec7d-4d4b-8663-5850fc219d32
    internal-label: Administration
subfeature_v2:
  - id: a7b2bfc5-be71-4740-b371-76fa6be8df02
    internal-label: Journey Optimizer release notes
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
    internal-label: User
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
    internal-label: Intermediate
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
    internal-label: Beginner
topic_v2:
  - id: a004cc84-67b9-4a33-a3a7-8ec7273ef4dc
    internal-label: Metadata
  - id: bce87dde-a4ab-44c9-8a18-ad66e4ddb377
    internal-label: Customer experience
  - id: d00e9f03-e50b-4162-b143-0c0817c937c2
    internal-label: Customer journeys
  - id: e0eb8757-182f-49f3-94a4-1587d16f5094
    internal-label: Personalization
source-git-commit: d645b6528fa7a1ae5169f129613f9085672e2ebb
workflow-type: tm+mt
source-wordcount: '3954'
ht-degree: 13%
---
# 发行说明 {#release-notes}

>[!CONTEXTUALHELP]
>id="ajo_homepage_card1"
>title="新增功能"
>abstract="**Adobe Journey Optimizer** 不断地提供新功能、增强现有功能，并修复错误。 所有更改会在每月的最后一周整合到发行说明中。"

[!DNL Adobe Journey Optimizer] 遵循持续交付模式，使 Adobe 能够持续不断地提供新功能、增强功能和修复。 此方法支持以可扩展的方式分阶段推出各种功能，以确保所有环境的性能和稳定性。 由于此模型，发行说明会在每月版本之间更新。 有关发行周期和可用性阶段的完整详细信息，请参阅 [Journey Optimizer 发行周期](releases.md)。

[!DNL Adobe Journey Optimizer] 原生构建于 [!DNL Adobe Experience Platform] 之上并继承了其所具备的最新创新技术和改进。 在 [Adobe Experience Platform 发行说明](https://experienceleague.adobe.com/docs/experience-platform/release-notes/latest.html?lang=zh-Hans){target="_blank"}中进一步了解这些更改。

>[!NOTE]
>
>这些发行说明中列出的功能包括&#x200B;**可用日期**，该日期指明每项变更在您的环境中何时可供使用。 **即将推出**&#x200B;折叠面板中的条目预计将在未来几天或几周内列出。 这些部分中的信息可能随时更改。

## 2026年9月发行说明 {#sep-26-updates}

>[!BEGINSHADEBOX]

**本月CX Enterprise Coworker的新增功能**

此版本提供了几项新的和改进的[同事](../start/ai-features.md#cx-coworker)功能和技能，此处列出了这些功能和技能，以供大家了解。 每项资料也详见下文其相关章节。

* [CE渠道内容插件](#sep-26-content-management) — 一个新插件，可在同事中将HTML的营销活动副本、图像和电子邮件技能融为一体，从营销活动简报到生产就绪的副本和HTML。
* [内容管理MCP工具](#sep-26-content-management) — 通过同事中的自然语言提示发现和管理内容模板、片段、登陆页以及内嵌消息内容。
* [历程模拟](#sep-26-journeys) — 自动进行端到端历程验证并直接在协作程序中解释结果。
* [比较历程版本](#sep-26-journeys) — 通过同事聊天获取任意两个历程版本之间的完全保真、结构化差异。
* [分析历程异常技能](#sep-26-journeys) — 使用根本原因诊断检测历程的进入、退出或消息发送计数中意外的峰值、下降或平线。

+++ 即将推出 — **以下信息可能会随时更改。**

* [从同事边栏创建历程](#sep-26-journeys) — 使用AI直接从同事右边栏生成旅程，替换以前的AI助手体验。
* [忠诚度推荐技能](#sep-26-loyalty) — 直接在同事的对话界面中请求挑战机会，并在不离开聊天的情况下将其转换为实时挑战。
* [保健分析技能](#sep-26-journeys) — 通过推荐的修复，扫描活动和草稿历程中的配置损坏、静默失败、资产老化或未使用等。
* [业务绩效分析技能](#sep-26-journeys) — 分析历程绩效并从聊天中获取具体的优化建议。

+++

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
<p>Co-worker中现在提供新的<strong>渠道内容</strong>插件，可在从策略到部署的一个插件下将活动副本、图像和组合电子邮件HTML技能整合在一起。 <b>渠道内容</b>插件下提供了以下技能：</p>
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
<p>有关更多信息，请参阅<a href="../content-management/content-management-coworker-skills.md#content-management#ce-channel-content">详细文档</a>。</p>
<p>发布日期： 2026年9月24日</p>
</td>
</tr>
</tbody>
</table>


<table>
<thead>
<tr>
<th><strong>CX Coworker中的内容管理MCP工具</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>CX Coworker现在提供了一组新的<strong>内容管理MCP工具</strong>，允许您通过自然语言提示发现和管理Journey Optimizer内容资源。 要求它列出或检索内容模板、片段、登陆页面和历程/营销活动内联消息内容。 它还可以创建内容、更新模板以及创建、更新、克隆和发布片段，并直接在历程和营销活动中更新内联渠道操作内容。</p>
<p>有关更多信息，请参阅<a href="../content-management/content-management-coworker-skills.md#content-management">详细文档</a>。</p>
<p>发布日期：2026年9月3日</p>
</td>
</tr>
</tbody>
</table>

* **登陆页面的强制同意复选框** — 现在，您可以在登陆页面表单组件中强制使用该复选框，要求访客在提交表单之前先选择它（例如，提供同意）。 [了解详情](../landing-pages/lp-content.md#use-form-component)

  发布日期：2026年9月4日

* **个性化语法中的其他保留关键字** - Profile Query Language (PQL)中的保留关键字列表已展开，包括常规关键字、时间单位和布尔值/逻辑运算符。 如果XDM架构包含的字段名称与这些关键字之一匹配，请用反撇号将其包装以便在个性化表达式中引用它。 [了解详情](../personalization/personalization-syntax.md#reserved-keywords)

  发布日期：2026年9月1日

### 忠诚度 {#sep-26-loyalty}

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
<p>有关更多信息，请参阅<a href="../loyalty-challenges/loyalty-admin.md#event-mappings">详细文档</a>。</p>
<p>发布日期：2026年9月22日</p>
</td>
</tr>
</tbody>
</table>

* **“永远”忠诚度挑战** — 忠诚度挑战现在可以无限期地运行。 配置计划时，将&#x200B;**质询结束**&#x200B;设置为&#x200B;**无结束日期**，质询永不过期。 [了解详情](../loyalty-challenges/create-challenges.md#schedule)

  发布日期：2026年9月1日

* **忠诚度适用于Healthcare Shield和Privacy and Security Shield客户** - Journey Optimizer Loyalty现在适用于Healthcare Shield和Privacy and Security Shield客户。 [了解详情](../loyalty-challenges/get-started.md)

  发布日期：2026年9月15日

+++ 即将推出 — **以下信息可能会随时更改。**

<table>
<thead>
<tr>
<th><strong>质询建议</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>“忠诚度绩效”菜单现在包括&#x200B;**机会**&#x200B;和**趋势**&#x200B;选项卡，这些选项卡显示AI检测到的趋势和差距，例如层级进展摩擦或挑战任务流失，每个选项卡都具有预计的影响，并且一键单击“使用AI创建”操作可生成可解决该问题的挑战。</p><p>此外，营销人员可以直接在同事的对话界面中请求&#x200B;**挑战机会**，根据真正的忠诚度计划趋势获得扎实的挑战想法，并在不离开聊天的情况下将其转化为实时挑战。</p>
</td>
</tr>
</tbody>
</table>

* **每个成员忠诚度质询完成截止日期** — 忠诚度质询现在支持每个成员的完成截止日期：根据完成要求选择“选择加入后的几天内”，以便根据每个成员的选择加入日期而不是整个计划的固定结束日期计算每个成员的截止日期。 如果同时设置了质询结束日期和此选择加入窗口，则每个成员的截止日期为第一个成员。<!-- Documentation link: TBD -->

* **内容卡个性化编辑器中的挑战域** — 内容卡个性化编辑器现在支持&#x200B;**挑战**&#x200B;作为域，允许您在创作内容卡个性化时访问挑战元数据。 这样可以更轻松地为挑战的每个阶段（启动、进行中和结束）创建量身定制的内容，而无需自定义代码。

+++

### 历程 {#sep-26-journeys}

<table>
<thead>
<tr>
<th><strong>与同事比较历程版本</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>现在，查看历程的两个版本之间发生了什么变化时，需要在Journey Optimizer节点中逐节点手动比较它们。 没有结构化的差异，这会使更改审查、审核和发布前检查变得缓慢且容易出错，尤其是在历程越来越复杂的情况下。 此功能允许客户或AI代理通过Co-worker Chat比较历程的任意两个版本，并获取全保真、**结构化差异** — 添加/删除/修改/移动节点，其中包括字段级详细信息、更改的连接、历程级属性更改和汇总计数，而无需打开Journey Optimizer。 </p>
<p>有关更多信息，请参阅<a href="../building-journeys/journeys-coworker-skills.md#journey-analyze">详细文档</a>。</p>
<p>发布日期： 2026年9月24日</p>
</td>
</tr>
</tbody>
</table>

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
<p>有关更多信息，请参阅<a href="../building-journeys/journeys-coworker-skills.md#journey-simulation">详细文档</a>。</p>
<p>发布日期：2026年9月23日</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>历程级保留（有限发布版）</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>您现在可以直接从历程属性为历程配置保留组。 保留是目标受众中可配置的百分比，该受众不会进入历程且不会收到任何通信。 通过将保留轮廓与 Customer Journey Analytics 报告中的活跃轮廓进行比较，您可以衡量历程带来的增量提升（真实影响）。</p>
<p>此功能仅面向一部分组织（限量发布）。 要获得访问权限，请与 Adobe 代表联系。 有关发行周期和可用性阶段的完整详细信息，请参阅 <a href="releases.md">Journey Optimizer 发行周期</a>。</p>
<p>有关更多信息，请参阅<a href="../building-journeys/journey-properties.md#performance-management">详细文档</a>。</p>
<p>发布日期：2026年9月1日</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>在历程中使用人工智能生成表达式</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>历程高级表达式编辑器现在集成了AI支持的表达式生成：描述您要以自然语言构建的表达式，该编辑器生成现成的代码，您可以立即应用或通过后续提示进行优化。</p>
<p>此功能此前为有限发布版，现已可供所有环境使用（正式发布版）。</p>
<p>有关更多信息，请参阅<a href="../building-journeys/expression/generate-expression.md">详细文档</a>。</p>
<p>发布日期：2026年9月1日</p>
</td>
</tr>
</tbody>
</table>

* **支持受众资格历程中的跳转活动** — 您现在可以在以受众资格节点开始的历程中使用跳转活动以跳转到基于事件的历程。 此功能正在逐步向组织推出。 如果您在环境中没有看到此内容，可能是因为您仍在受众资格中使用批量受众。 [了解详情](../building-journeys/jump.md)

  发布日期：2026年9月22日。

* **批次受众评估后触发** — 对于以批次受众为目标的周期性历程，可在历程运行前为全新批次评估配置最多6小时的等待时段。 如果正在进行评估，则历程将等待它完成；如果上次运行使用了最新的快照，则历程将等待较新的批次。 如果等待时段结束时没有可用的新受众，则会跳过该事件。 [了解详情](../building-journeys/read-audience.md)

  发布日期：2026年9月18日

* 历程模拟中的&#x200B;**决策** — 模拟中现在支持&#x200B;**优化**&#x200B;活动中的路径试验。 路由由Decisioning处理，每个模拟用户都具有随机性和不确定性。

  [了解详情](../building-journeys/simulate-journey-gs.md)

  发布日期：2026年9月15日

* **检测到新历程异常警报** — 现在，当实时旅程的每日流量在事件条目、历程退出和事件发送之间偏离其历史基线或意外降至零时，新历程警报会警告您。 此警报当前仅在生产沙盒中可用。

  [了解详情](../reports/alerts.md)

  发布日期：2026年9月15日

* **历程模拟中的决策** — 您现在可以模拟依赖决策的历程，新支持以下功能：

  * 现在，模拟中支持内容决策节点。
  * 现在，模拟中支持优化活动的定位规则方法。
  * 现在，模拟中支持包含Adobe Journey Optimizer决策内容的操作（例如，使用决策策略的电子邮件）。
  * 完全支持使用优惠资格并按规则、受众、优先级或公式进行排名的决策策略。 按AI模型排名 — 还支持Personalization，尽管返回的优惠可能在运行之间有所不同。

  [了解详情](../building-journeys/simulate-journey-gs.md)

  发布日期：2026年9月8日

* **分析历程异常技能** - CX Coworker现在可以使用&#x200B;**分析历程异常**&#x200B;技能根据历史基线检测历程的进入、退出或消息发送计数中的意外峰值、下降或平线。 一旦真正的异常得到确认，该技能就会运行只读诊断来揭示可能的根本原因和推荐。 [了解详情](../building-journeys/journeys-coworker-skills.md#journey-analyze)

  发布日期：2026年9月2日

* **历程表达式编辑器中的新dateDiff函数** — 历程表达式编辑器现在包含`dateDiff`函数，该函数计算两个日期之间的天数差。 此函数对于基于时间的逻辑很有用，例如创建截止日期、计算客户生命周期持续时间或在历程条件中构建倒计时计时器。  [了解详情](../building-journeys/functions/date-functions.md#dateDiff)

  发布日期：2026年9月1日

+++ 即将推出 — **以下信息可能会随时更改。**

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
<p>今天查看渠道内容需要一次单独打开一个活动 — 在包含多个渠道活动的历程中，速度慢且容易出错，尤其是当个性化意味着检查每个活动的多个处理或变体时。 <strong>内容预览</strong>通过直接在画布中为每个渠道活动显示内容缩略图，并使用全屏模式检查并在处理方式和变体之间切换来消除该摩擦。</p>
<p>目标可用日期：2026年9月28日</p>
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

* **Heague Analysis技能** - CX Coworker现在可以扫描您的活动和草稿历程，以查找中断的配置、静默失败、损坏或未使用的资源（例如过时的草稿历程、孤立的数据源和持续的自定义操作错误），并直接在聊天中显示建议的修复。<!-- Documentation link: TBD -->

* 历程模拟中支持&#x200B;**补充ID** - **历程模拟中现在支持补充ID**，允许您测试读取受众历程和事件触发历程的复杂用户方案。

* **自定义报告的练习步骤事件抑制** — 作为步骤事件优化的一部分，Journey Optimizer现在在历程练习期间停止生成某些不可报告的步骤事件。 这仅会影响基于这些模拟运行步骤事件类型构建的自定义报表。 如果您受到影响，请重新触发模拟以重新生成数据。

* **历程属性中的自动事件恢复超时** -历程属性现在包括&#x200B;**设置事件恢复超时**&#x200B;设置：默认情况下，受影响的旅程事件在服务中断后最多72小时内自动重放，而无需执行任何操作。 您可以打开此设置来控制对时间敏感的历程的重播窗口（0-72小时）。 现有的&#x200B;**超时或错误**&#x200B;字段也已重命名为&#x200B;**自定义操作/数据源超时**，以避免这两个设置混淆。

+++

### 营销活动 {#sep-26-campaigns}

+++ 即将推出 — **以下信息可能会随时更改。**

* **操作营销活动文件夹** — 您现在可以将操作营销活动组织到文件夹中，以改进界面中的导航和管理。

* **覆盖操作营销活动中的默认执行字段** — 以前在历程级别可用，但现在您可以在操作营销活动参数中覆盖为电子邮件、短信和WhatsApp投放全局配置的默认执行字段。

+++


### 渠道 {#sep-26-channels}

此版本中的渠道即将提供以下功能和改进。

+++ 即将推出 — **以下信息可能会随时更改。**

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

+++

### 编排的营销活动 {#sep-26-orchestrated-campaigns}

<table>
<thead>
<tr>
<th><strong>针对编排的活动发出警报</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>现在，编排的营销活动通过跨历程和营销活动使用的同一警报框架支持<strong>自动警报</strong>。 当营销活动执行失败、超时时会触发警报，每个警报都包含所发生的情况、时间、位置和指向画布的直接链接，以便查看日志中的详细信息。</p>
<p>有关更多信息，请参阅<a href="../orchestrated/start-monitor-campaigns.md#alerting">详细文档</a>。</p>
<p>发布日期：2026年9月22日</p>
</td>
</tr>
</tbody>
</table>

* **在编排的营销活动中包含关系数据的条件内容** — 在Email Designer中为编排的营销活动构建条件内容时，您现在可以直接基于关系数据（例如与配置文件关联的相关记录）构建条件，而不仅仅是标准配置文件属性。 [了解详情](../orchestrated/activities/channels.md#add-personalization)

  发布日期：2026年9月22日

* **在编排的营销活动中直接联接收藏集** — 从相关收藏集中添加属性时，您现在可以选择三种联接模式（一种新默认模式，用于警告笛卡尔产品对性能的潜在影响）以及现有的“聚合”和“高级”模式，从而更容易在构建查询之前了解查询的权衡。 [了解详情](../orchestrated/build-query.md#links)

  发布日期：2026年9月22日

+++ 即将推出 — **以下信息可能会随时更改。**

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

* **营销活动编排监控** — 新的用户界面现在可用于跟踪编排的营销活动分段所使用的关系存储数据的摄取状态和新鲜度。 它让您能够直接查看提供给批处理受众的数据的运行状况。 Adobe Experience Platform的“监控”仪表板中新增的Campaign Orchestration选项卡可显示关系存储数据流（摄取/更新/删除/失败/跳过的记录）的运行状况，并带有向下钻取图形和每个数据流/数据集划分，包括族系。

* **新的协调营销活动监控API** — 新&#x200B;**API规范**&#x200B;现在可用于协调营销活动，允许您以编程方式创建、管理和触发协调营销活动，从而与外部系统和自动化管道进行更深度的集成。

+++

### 入门 {#sep-26-onboarding}

此版本即将载入以下改进。

<table>
<thead>
<tr>
<th><strong>引导式电子邮件和历程功能</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>引导式电子邮件和历程功能现在包括以下改进：</p>
<ul>
<li>在迁移电子邮件时，[!DNL Journey Optimizer]将标识该电子邮件引用的内容块，并将其显示为措施项，以便您可以随电子邮件迁移内容块。</li>
<li>界面已得到改进，使引导式入门更直观。</li></ul>
<p>有关更多信息，请参阅<a href="../start/onboarding-hub.md">详细文档</a>。</p>
<p>发布日期：2026年9月23日</p>
</td>
</tr>
</tbody>
</table>

### 报表 {#sep-26-reporting}

以下功能即将在此版本中报告。

+++ 即将推出 — **以下信息可能会随时更改。**

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

+++

### 集成 {#sep-26-integrations}

以下功能即将在此版本中集成。

+++ 即将推出 — **以下信息可能会随时更改。**


* **Experience Manager片段的动态令牌替换** - Experience Manager内容片段引用现在支持&#x200B;**tokenSubstitution**&#x200B;属性。 当设置为`false`时，片段的字段中的个性化设置将直接解析，而无需引用中的令牌映射。 默认值为`true`，这将保留现有行为。

  此功能仅面向一部分组织（限量发布）。 要获得访问权限，请与 Adobe 代表联系。

* **Decisioning中的AEM Managed Services内容片段支持** - Decisioning在管理决策项目时现在支持AEM Managed Services内容片段。


+++

### 个性化 {#sep-26-personalization}

* **使用AI修复语法** — 现在，在检测到PQL语法验证错误时，Personalization编辑器会提供“使用AI修复”选项，以帮助直接从编辑器解决问题。

  发布日期：2026年9月22日

### 决策 {#sep-26-decisioning}

此版本中的决策功能即将提供以下功能和改进。

<table>
<thead>
<tr>
<th><strong>Web渠道中的决策支持</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>决策现在可用于网页渠道。 您可以直接在 Web 可视编辑器中使用决策策略，向每位访客提供最相关的产品建议。</p>
<p>有关更多信息，请参阅<a href="../experience-decisioning/use-decision-policy.md">详细文档</a>。</p>
<p>发布日期：2026年9月22日</p>
</td>
</tr>
</tbody>
</table>

* **Decisioning中的AEM内容片段可供Managed Services客户使用** — 以前，Decisioning中的AEM内容片段仅可供&#x200B;**Adobe Experience Manager as a Cloud Service**&#x200B;集成的客户使用。 此功能现在也可供使用&#x200B;**Adobe Experience Manager Managed Services**&#x200B;的客户使用。 [了解详情](../experience-decisioning/items.md#attributes)

  发布日期：2026年9月23日

* **在规则和排名公式模拟中支持Adobe Experience Platform配置文件** — 在模拟规则或排名公式时，您现在可以选择Adobe Experience Platform配置文件以自动填充测试数据变体的属性，而不是手动输入属性。 [了解详情](../experience-decisioning/ranking/ranking-formulas.md#simulate-ranking-formula)

  发布日期：2026年9月22日

### 受众 {#sep-26-audiences}

以下提醒适用于此版本中的受众。

* **即将更改受众组合扩充受众** — 在10月版本（10月底）中，Journey Optimizer将停止使用或引用源数据集不具有&#x200B;**主身份描述符**&#x200B;的受众组合受众的历程和营销活动。 从那时起，历程和营销活动仅支持使用主身份描述符构建的受众组合受众。 如果您需要这些历程或营销活动保持活动状态，请联系您的Adobe代表 — 我们的产品团队可以帮助您进行迁移。<!-- Documentation link: TBD -->

### 管理 {#sep-26-administration}

以下提醒适用于此版本中的管理。

* **数据集的生存时间(TTL)护栏 — 现有沙盒** — 从2026年10月1日起，将在现有客户沙盒和组织上强制实施Journey Optimizer系统生成的数据集的生存时间(TTL)护栏（配置文件存储为90天，数据湖为13个月）。

### 可用性改进 {#sep-26-usability}

* **片段验证警报中的AI概述** — 片段验证警报对话框现在包含一个AI概述，其中汇总并说明了验证问题（例如表达式格式不正确、缺少配置文件字段和无效的JSON），以便用户能够更快地排除故障。

  发布日期：2026年9月22日

* **在新的历程画布中更轻松地分离和加入分支** — 现在，您可以通过直接在画布上选择符合条件的活动，或从断开连接或已使用分支的列表中选取活动，将分支从历程的其余部分分离而不删除它，并在稍后在不同点重新加入。 [了解详情](../building-journeys/using-the-journey-designer.md#join-and-detach-branches)

  发布日期：2026年9月1日

+++ 即将推出 — **以下信息可能会随时更改。**

* **内容模拟体验中的可用性改进** — 现在，通过新的内容模拟体验，您可以命名和组织变体以便轻松比较，直接从每个信息卡复制或删除变体详细信息，根据需要查看完整属性路径和每信息卡渠道配置，以及通过更突出的上传按钮上传您自己的CSV、JSON或JSONL配置文件。

+++
