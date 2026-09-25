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
source-git-commit: c49af406dc410b4f508835207fc7d1e016a8c38b
workflow-type: tm+mt
source-wordcount: '5024'
ht-degree: 67%
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

**CX Enterprise Coworker 本月新增功能**

此版本提供了多项新增和改进的 [Coworker](../start/ai-features.md#cx-coworker) 功能和技能，现列出如下，方便用户查阅。 每一项将在下文相应章节中详细介绍。

* [CE渠道内容插件](#sep-26-content-management) — 一个新插件，可在同事中将HTML的营销活动副本、图像和电子邮件技能融为一体，从营销活动简报到生产就绪的副本和HTML。
* [内容管理MCP工具](#sep-26-content-management) — 通过同事中的自然语言提示发现和管理内容模板、片段、登陆页以及内嵌消息内容。
* [历程模拟](#sep-26-journeys) – 自动执行端到端历程验证，并直接在 Coworker 中解读结果。
* [比较历程版本](#sep-26-journeys) – 通过 Coworker 聊天，获取任意两个历程版本之间的完整保真的结构化差异对比。
* [分析历程异常技能](#sep-26-journeys) — 使用根本原因诊断检测历程的进入、退出或消息发送计数中意外的峰值、下降或平线。
* [决策解释者技能](#sep-26-decisioning) — 询问同事为什么特定优惠显示或未显示给用户档案或区段，并获取资格、排名和规则排除的完整跟踪。
* [规则和排名技能](#sep-26-decisioning) — 创建、解释、模拟和优化决策资格规则和自然语言排名公式，而无需手动编写或验证PQL语法。

+++ 即将推出 — **以下信息可能会随时更改。**

* [从 Coworker 边栏创建历程](#sep-26-journeys) – 可直接在 Coworker 右边栏中借助 AI 生成历程，取代此前的 AI 助手体验。
* [忠诚度推荐技能](#sep-26-loyalty) – 直接在 Coworker 的对话界面中请求挑战机会，无需离开聊天即可将其转化为正式上线的挑战活动。
* [健康度分析技能](#sep-26-journeys) – 扫描处于活跃和草稿状态的历程，查找损坏的配置、静默故障以及逐渐失效或闲置的资产，并提供建议的修复方案。
* [业务绩效分析技能](#sep-26-journeys) – 直接在聊天中分析历程绩效，并获取具体的优化建议。

+++

>[!ENDSHADEBOX]

### 内容管理 {#sep-26-content-management}

此版本将在内容管理方面新增以下功能。

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
<th><strong>CX Coworker 中的内容管理 MCP 工具</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>CX Coworker 现在提供了一组新的<strong>内容管理 MCP 工具</strong>，可让您通过自然语言提示来发现和管理 Journey Optimizer 内容资产。 要求它列出或检索内容模板、片段、登陆页面和历程/营销活动内联消息内容。 它还可以创建内容、更新模板，以及创建、更新、克隆和发布片段，并直接在历程和营销活动中更新内联渠道操作内容。</p>
<p>有关更多信息，请参阅<a href="../content-management/content-management-coworker-skills.md#content-management">详细文档</a>。</p>
<p>发布日期：2026 年 9 月 3 日</p>
</td>
</tr>
</tbody>
</table>

* **登陆页面的强制同意复选框** – 现在，您可以在登陆页面表单组件中将复选框设为必选项，要求访客在提交表单前先勾选该复选框（例如，表示同意）。 [了解详情](../landing-pages/lp-content.md#use-form-component)

  发布日期：2026 年 9 月 4 日

* **个性化语法中的额外保留关键字** – Profile Query Language (PQL) 中的保留关键字列表已扩充，新增了通用关键字、时间单位和布尔/逻辑运算符。 如果您的 XDM 架构中包含与上述关键字之一同名的字段名，请用反引号将其括起，以便在个性化表达式中引用它。 [了解详情](../personalization/personalization-syntax.md#reserved-keywords)

  发布日期：2026 年 9 月 1 日

+++ 即将推出 — **以下信息可能会随时更改。**

* **模拟内容中的URL验证** — 现在，预览内容时，Journey Optimizer会自动检查它包含的Web链接，并在发送之前标记损坏、不安全或无法访问的URL。 该功能以有限发布形式向部分客户提供。

+++

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
<p>现在，您可通过全新的&#x200B;**可视化映射构建器**&#x200B;创建或编辑事件映射：选择架构，从可搜索的字段选择器中选择字段，将每个字段映射到忠诚度事件字段（会显示每一行的连接状态），预览自动生成的 JSONata 表达式，还可随时选择切换为手动编辑 JSONata。</p><p>此外，忠诚度管理界面中的“事件定义”已重命名为“事件映射”，并采用了全新的列表视图，可显示易读的体验事件架构名称。</p>
<p>有关更多信息，请参阅<a href="../loyalty-challenges/loyalty-admin.md#event-mappings">详细文档</a>。</p>
<p>发布日期：2026年9月22日</p>
</td>
</tr>
</tbody>
</table>

* **“永久”忠诚度挑战** – 忠诚度挑战现在可以无限期运行。 配置计划时，将&#x200B;**挑战结束**&#x200B;设置为&#x200B;**无结束日期**，挑战便永不过期。 [了解详情](../loyalty-challenges/create-challenges.md#schedule)

  发布日期：2026 年 9 月 1 日

* **Healthcare Shield 和 Privacy and Security Shield 客户现可使用 Loyalty** – Journey Optimizer Loyalty 现已面向 Healthcare Shield 和 Privacy and Security Shield 客户开放。 [了解详情](../loyalty-challenges/get-started.md)

  发布日期：2026 年 9 月 15 日

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

* **内容卡个性化编辑器中的挑战域** – 内容卡个性化编辑器现在支持将&#x200B;**挑战**&#x200B;作为一个域，让您在编写内容卡片个性化内容时，能够访问挑战元数据。 这样可以更轻松地为挑战的每个阶段（启动、进行中和结束）创建量身定制的内容，而无需自定义代码。

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
<th><strong>Coworker 中的历程模拟</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Coworker 中的<strong>历程模拟技能</strong>可自动执行端到端历程验证，并让您轻松解读结果。 请注意，此功能当前仅支持快速模拟流程，不能完全取代 Journey Optimizer 的手动模拟体验。</p>
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
<p>此功能仅面向部分组织开放（限量发布）。 要获得访问权限，请与 Adobe 代表联系。 有关发行周期和可用性阶段的完整详细信息，请参阅 <a href="releases.md">Journey Optimizer 发行周期</a>。</p>
<p>有关更多信息，请参阅<a href="../building-journeys/journey-properties.md#performance-management">详细文档</a>。</p>
<p>发布日期：2026 年 9 月 1 日</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>在历程中使用 AI 生成表达式</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>历程高级表达式编辑器现在集成了 AI 驱动的表达式生成功能：以自然语言描述您要构建的表达式，编辑器即会生成可立即应用或通过后续提示进一步优化的即用型代码。</p>
<p>此功能此前为限量发布，现已可供所有环境使用（正式发布版）。</p>
<p>有关更多信息，请参阅<a href="../building-journeys/expression/generate-expression.md">详细文档</a>。</p>
<p>发布日期：2026 年 9 月 1 日</p>
</td>
</tr>
</tbody>
</table>

* **支持受众资格历程中的跳转活动** — 您现在可以在以受众资格节点开始的历程中使用跳转活动以跳转到基于事件的历程。 此功能正在逐步向组织推出。 如果您在环境中没有看到此内容，可能是因为您仍在受众资格中使用批量受众。 [了解详情](../building-journeys/jump.md)

  发布日期：2026年9月22日。

* **批次受众评估后触发** — 对于以批次受众为目标的周期性历程，可在历程运行前为全新批次评估配置最多6小时的等待时段。 如果正在进行评估，则历程将等待它完成；如果上次运行使用了最新的快照，则历程将等待较新的批次。 如果等待时段结束时没有可用的新受众，则会跳过该事件。 [了解详情](../building-journeys/read-audience.md)

  发布日期：2026年9月18日

* **历程模拟中的决策** – 路径试验作为&#x200B;**优化**&#x200B;活动的一部分，现已在模拟中受支持。 路由是由决策功能处理的，且对每个模拟用户而言都是随机且不确定的。

  [了解详情](../building-journeys/simulate-journey-gs.md)

  发布日期：2026 年 9 月 15 日

* **新增的“检测到历程异常”警报** – 当实时历程的每日流量（涵盖历程进入、历程退出和事件发送）偏离其自身历史基线，或意外降至零时，新的系统警报会向您发出提醒。 此警报当前仅在生产沙盒中可用。

  [了解详情](../reports/alerts.md)

  发布日期：2026 年 9 月 15 日

* **历程模拟中的决策** – 您现在可以模拟依赖决策的历程，新增以下支持：

  * 现已支持在模拟中使用内容决策节点。
  * 现已支持在模拟中使用“优化”活动的“目标选择规则”方法。
  * 现已支持在模拟中使用带有 Adobe Journey Optimizer 决策内容（如使用决策策略的电子邮件）的操作。
  * 完全支持使用“产品建议资格”并按规则、受众、优先级或公式进行排名的决策策略。 同时还支持按“AI 模型 - 个性化”进行排名，不过每次运行返回的产品建议可能会有所不同。

  [了解详情](../building-journeys/simulate-journey-gs.md)

  发布日期：2026 年 9 月 8 日

* **分析历程异常技能** – CX Coworker 现在可以使用&#x200B;**分析历程异常**&#x200B;技能，对照历史基线来检测历程进入、退出或消息发送数量中的意外峰值、骤降或持平情况。 一旦确认存在真实异常，该技能便会运行只读诊断，以揭示可能的根本原因并给出建议。 [了解详情](../building-journeys/journeys-coworker-skills.md#journey-analyze)

  发布日期：2026 年 9 月 2 日

* **历程表达式编辑器中的新增 dateDiff 函数** – 历程表达式编辑器现在包含 `dateDiff` 函数，可计算两个日期之间的天数差。 此函数对于基于时间的逻辑很有用，例如创建截止日期、计算客户生命周期时长，或在历程条件中构建倒计时器。  [了解详情](../building-journeys/functions/date-functions.md#dateDiff)

  发布日期：2026 年 9 月 1 日

+++ 即将推出 — **以下信息可能会随时更改。**

<table>
<thead>
<tr>
<th><strong>历程警报的 AI 推荐卡</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>当历程警报触发时，Journey Optimizer 主页现在会显示 <strong>AI 推荐卡</strong>，涵盖<strong>历程自定义操作失败</strong>和<strong>检测到历程异常</strong>警报。 选择该卡片会打开相应历程，右边栏会预先填充已执行的分析结果。</p>
<!-- GIF placeholder: to be added -->
<!-- Documentation link: TBD -->
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>“入站活动停用”历程活动</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>历程画布中新增了一个<strong>入站活动停用</strong>活动，它允许您直接在历程中将某个轮廓从最多五个入站活动或体验中移除，从而使入站资格取消与历程退出分离，以实现更高级的跨渠道编排。</p>
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
<th><strong>从 Coworker 边栏创建历程</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p></strong>使用 AI 创建历程<strong>现可直接从 Coworker 右边栏访问，这一经过更名改版的集成式入口取代了此前的 AI 助手体验，用来生成历程。</p>
</td>
</tr>
</tbody>
</table>

* **Heague Analysis技能** - CX Coworker现在可以扫描您的活动和草稿历程，以查找中断的配置、静默失败、损坏或未使用的资源（例如过时的草稿历程、孤立的数据源和持续的自定义操作错误），并直接在聊天中显示建议的修复。<!-- Documentation link: TBD -->

* **支持在历程模拟中使用补充 ID** – 历程模拟现已支持&#x200B;**补充 ID**，使您可以为读取受众和事件触发的历程测试复杂的用户场景。

* **自定义报告的试运行步骤事件抑制** – 作为步骤事件优化的一部分，Journey Optimizer 现在会在“历程试运行”期间停止生成某些不可报告的步骤事件。 这仅会影响基于这些试运行步骤事件类型构建的自定义报告。 如果您受到影响，请重新触发试运行以重新生成数据。

* **历程属性中的自动事件恢复超时** – 历程属性现在包含&#x200B;**设置事件恢复超时**&#x200B;设置：默认情况下，受影响的历程事件会在服务中断后自动重放，最长可达 72 小时，无需任何操作。 您可以开启此设置，以控制时间敏感型历程的重放窗口（0–72 小时）。 现有的&#x200B;**超时或错误**&#x200B;字段也已重命名为&#x200B;**自定义操作/数据源超时**，以避免这两个设置混淆。

* **减少等待和事件活动的步骤事件** — 不再为&#x200B;**等待**&#x200B;活动和&#x200B;**事件**&#x200B;活动生成步骤事件，因为在该活动中实际未处理配置文件。

+++

### 营销活动 {#sep-26-campaigns}

+++ 即将推出 — **以下信息可能会随时更改。**

* **操作营销活动文件夹** – 您现在可以将操作营销活动整理到文件夹中，以改善界面中的导航和管理。

* **覆盖操作营销活动中的默认执行字段** – 此功能之前在历程级别可用，现在可覆盖在操作营销活动参数中为电子邮件、短信和 WhatsApp 投放全局设置的默认执行字段。

+++


### 渠道 {#sep-26-channels}

此版本将在渠道方面新增以下功能和改进。

* **子域委派限制提高** — 根据您的许可合同，您现在可以通过联系您的Adobe代表来请求最多3000个子域（以前限制为100个）。 该功能以有限发布形式向部分客户提供。 [了解详情](../configuration/delegate-subdomain.md#guardrails)

  发布日期： 2026年9月25日

+++ 即将推出 — **以下信息可能会随时更改。**

<table>
<thead>
<tr>
<th><strong>自定义出站渠道（正式发布）</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p><strong>自定义出站渠道</strong>让管理员能够通过无代码渠道生成器，将任何基于 HTTP 的出站消息渠道（例如微信、Kakao Talk、Messenger 或专有提供商）直接引入 Journey Optimizer。 配置后，自定义渠道可在营销活动、历程和编排的营销活动中使用，并具有与原生渠道相同的完整功能集：使用表达式编辑器进行个性化、内容实验、预览和校样、开箱即用的报告以及同意和治理要求的执行。</p>
<p>在此版本中，自定义出站渠道还新增了几项功能：</p>
<ul>
<li>在自定义渠道负载中，您可以像在基于代码的体验中一样，通过个性化编辑器使用 Journey Optimizer 决策功能。</li>
<li>您可以将业务规则应用于自定义渠道，方式与原生渠道相同。</li>
<li>现在可以在渠道列表中为 API 触发的营销活动选择自定义渠道，此前不支持此操作。</li>
<!--<li>Define a reporting webhook for a custom channel and attach it to a channel configuration, so you can enrich your Journey Optimizer reports with interaction events.</li>-->
</ul>
<p>以前此功能在“有限可用性”中提供，但现在向所有环境提供（一般可用性），并包含上述增强功能。</p>
<p><img src="assets/do-not-localize/custom-channel.gif"></p>
<p>有关更多信息，请参阅<a href="../custom-channel/get-started-custom-channel.md">详细文档</a>。</p>

</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Android Live Updates 的实时活动</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Journey Optimizer 现将<strong>实时活动支持延伸到 Android</strong>，从而进一步扩展了其实时移动端个性化功能。 您可以直接向用户传递实时进度更新，例如订单跟踪、航班状态、实时活动更新和实时体育赛事比分。</p>
<p>除了支持 iOS 实时活动之外，Journey Optimizer 现在还可跨平台配置管理 Android Live Updates 的临时推送令牌。 通过使用 API 触发的营销活动和 Headless API，它同时支持广播和事务性更新流程。</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Android 推送通知模板改进</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>此前，Android 推送通知通过单一固定布局进行渲染：图像始终被居中裁剪，较长的正文文本也会被截断。 此版本引入了可在编写时使用的模板选取器，让营销人员能够控制 Android 推送通知的布局。</p>
<p>提供了以下改进：</p>
<ul>
<li><b>布局选择</b>：新增了推送通知布局选取器（标准/展开），可在设置 Android 推送时使用。</li>
<li><b>带有“显示整个图像”的标准布局</b>：可在“裁剪填充”和“缩放适应”之间选择。</li>
<li><b>展开布局</b>：多行正文文本不会被截断，还可选择显示大图标缩略图。</li>
<li><b>折叠正文（展开布局）</b>：针对折叠状态设置单独的、较短的正文文本。</li>
</ul>
</td>
</tr>
</tbody>
</table>

* **自定义短信 BYOP 身份验证灵活性** – 现在，在连接短信服务提供商的 OAuth 设置时，您可以配置&#x200B;**自定义身份验证标头**，包括令牌在传出消息中的放置位置以及令牌请求本身的格式。

* **直邮 — 自动拆分大文件** — 现在，当直邮文件大约超过20 GB时，可以自动将其拆分为多个部分，或者通过在文件路由配置中选择目标文件大小来手动拆分。

* **直邮 — 增加了受众限制** — 直邮渠道受众限制已从300万个配置文件增加到1亿个配置文件，使您可定位更多受众，而不会出现文件创建错误。

+++

### 编排的营销活动 {#sep-26-orchestrated-campaigns}

<table>
<thead>
<tr>
<th><strong>编排的营销活动的警报</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>编排的营销活动现在支持<strong>自动警报</strong>，其所用的警报框架与历程和营销活动中的一致。 当营销活动执行失败、超时时会触发警报，每个警报都包含所发生的情况、时间、位置和指向画布的直接链接，以便查看日志中的详细信息。</p>
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
<th><strong>用于编排的营销活动的 OR 连接活动</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>现在，编排的营销活动中的<strong>连接活动</strong>支持 AND 和 OR 连接条件。 使用 OR 逻辑时，轮廓完成任意一个上游分支（而非全部），就会沿着共用的单一下游路径继续执行。 这样一来，就可以直接在画布上对“如果 A 或 B 或 C，则执行此操作”这类模式进行建模，而无需跨独立分支重复下游步骤。</p>
</td>
</tr>
</tbody>
</table>

* **用于编排的营销活动的 LINE 渠道** – LINE 现已作为编排的营销活动中的原生出站渠道提供，与电子邮件、短信和推送渠道并列。 您可以直接从营销活动画布构建和投放 LINE 消息，包括文本、贴图、图像、视频、位置数据和 Flex 消息，适合日本及亚太等以 LINE 为主流的市场中的促销、交易和持续互动用例。 此功能之前为限量发布，现已正式发布。

* **营销活动编排监控** – 新增了一个用户界面，可用于跟踪编排的营销活动分段所使用的关系存储数据的摄取状态和新鲜度。 它让您能够直接掌握提供给批量受众的数据的健康状况。 Adobe Experience Platform 的“监控”仪表板中新增了一个“营销活动编排”选项卡，可展示关系存储数据流的健康状况（已摄取/已更新/已删除/失败/已跳过的记录数），并提供深入分析图表，以及按数据流/数据集细分的信息，包括世系信息。

* **新的编排的营销活动监控 API** – 新的&#x200B;**API 规范**&#x200B;现已可用于编排的营销活动，允许您以编程方式创建、管理和触发编排的营销活动，从而实现与外部系统和自动化管道的更深度集成。

+++

### 电子邮件渠道 {#sep-26-email-channel}

此版本中的电子邮件渠道即将提供以下功能和改进。

+++ 即将推出 — **以下信息可能会随时更改。**

<table>
<thead>
<tr>
<th><strong>覆盖电子邮件渠道配置设置</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>在构建历程和营销活动时，您现在可以直接在历程或营销活动操作级别覆盖从所选渠道配置派生的电子邮件参数。</p>
<p>这样，您就可以使用轮廓属性或上下文数据对电子邮件标头字段（<strong>发件人名称</strong>、<strong>发件人电子邮件前缀</strong>、<strong>回复名称</strong>和<strong>回复电子邮件地址</strong>）、执行地址和列表取消订阅值进行个性化设置，以实现更精确的控制。 特别是，这允许发件人详细信息反映每个收件人的相关顾问、位置或分支机构，而不是通过单个公司地址路由所有发送。</p>
</td>
</tr>
</tbody>
</table>

* **在电子邮件操作级别覆盖禁止列表现在** -Journey Optimizer允许您在历程和营销活动中直接在电子邮件操作级别覆盖禁止列表行为。 这允许团队在需要专用发送配置的操作性或合规性关键通信方面有更大的灵活性，同时保留所有其他发送的现有全局禁止列表控制。 此增强功能可帮助组织准确处理异常场景，而无需更改其更广泛的抑制治理模型。

+++

### 电子邮件设计器 {#sep-26-email-designer}

此版本将在电子邮件设计器方面新增以下功能和改进。

<table>
<thead>
<tr>
<th><strong>对电子邮件内容进行协作</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>电子邮件Designer现在包含用于评论和解决的内置<strong>协作工具</strong>，因此营销团队可以直接在Journey Optimizer中查看、讨论和最终确定电子邮件内容，而不是通过聊天、电子邮件线程或电子表格等外部工具共享草稿。 邀请协作者和审阅人，添加常规或特定于组件的注释，以及回复、解决和管理注释线程 — 所有这些操作都无需离开电子邮件Designer。</p>
<p>有关更多信息，请参阅<a href="../email/email-collaboration.md">详细文档</a>。</p>
<p>发布日期：2024年9月25日。</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>新建表组件</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>电子邮件设计器现在包含内置的<strong>表格组件</strong>，允许您直接在电子邮件中以行和列的形式构建内容。 将组件拖放到画布上，自定义行和列的数量，并单独设置每个单元格的样式，以创建清晰、有序的布局，而无需依赖自定义 HTML。</p>
<p><img src="assets/do-not-localize/table-component.gif"></p>
<p>有关更多信息，请参阅<a href="../email/content-components.md#table">详细文档</a>。</p>
<p>发布日期：2024年9月24日。</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>支持对电子邮件主题变体使用深色模式</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>电子邮件主题现在支持深色模式，因此每个颜色变体都可以呈现一种量身定制的外观，适合在启用深色模式的客户端中查看电子邮件的收件人。</p>
<p>启用后，系统会自动为每个变体生成默认深色调色板，您还可以进一步使用其他调色板或自定义颜色对其进行自定义，该设置与浅色模式设计相互独立，因此在一个模式下所做的更改不会影响另一个模式。</p>
<p><img src="../email/assets/theme-dark-mode-support.gif"></p>
<p>有关更多信息，请参阅<a href="../email/apply-email-themes.md">详细文档</a>。</p>
<p>发布日期：2024年9月24日。</p>
</td>
</tr>
</tbody>
</table>

+++ 即将推出 — **以下信息可能会随时更改。**

<table>
<thead>
<tr>
<th><strong>在电子邮件设计器中直接从 PSD 文件导入 Dynamic Media 模板</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>电子邮件设计器的 Dynamic Media 组件现在除了可以浏览现有的 Dynamic Media 模板外，还允许您直接将 Photoshop (PSD) 文件导入为新模板。 将PSD文件拖放到组件中，Adobe Journey Optimizer会自动将其转换为Dynamic Media模板 — 无需手动转换或穿过Adobe Experience Manager来回转换。 导入模板后，使用内置的Dynamic Media编辑器编辑该模板。</p>
</td>
</tr>
</tbody>
</table>

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

+++ 即将推出 — **以下信息可能会随时更改。**

<table>
<thead>
<tr>
<th><strong>用于入门电子邮件和历程的引导式功能（正式发布）</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>借助引导式功能，您可以将现有电子邮件内容和历程移入 Journey Optimizer，更轻松地从另一个营销平台迁移到 Adobe Journey Optimizer。 <strong>专用工作区</strong>可让您重复利用现有资源，而不用从头开始重建。</p>
<p>此功能此前为限量发布，现已可供所有环境使用（正式发布版）。</p>
</td>
</tr>
</tbody>
</table>

+++

### 报表 {#sep-26-reporting}

此版本将在报告方面新增以下功能。

<table>
<thead>
<tr>
<th><strong>“数据管理”中的新入站监控图表</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>您现在可以直接从<strong>数据管理 &gt; 监控 &gt; Edge</strong> 监控入站数据健康状况，新增了 6 个图表，分别涵盖吞吐量、延迟和建议事件：</p>
<ul>
<li><strong>AJO 入站吞吐量</strong> – 一段时间内的整体入站吞吐量（每秒记录数）。</li>
<li><strong>AJO 入站吞吐量细分</strong> – 按位置细分的入站吞吐量。</li>
<li><strong>AJO 入站延迟</strong> – 入站请求延迟（以毫秒为单位），按值分布（P50、P90 等）细分。</li>
<li><strong>AJO 入站建议事件吞吐量</strong> – 随时间变化的建议事件吞吐量（建议事件是指用户与个性化产品建议交互、查看或触发个性化产品建议时生成的跟踪信号）。</li>
<li><strong>按渠道列出的 AJO 入站建议事件吞吐量</strong> – 按入站渠道（CBE、应用程序内、内容卡）细分的建议事件吞吐量。</li>
<li><strong>AJO 入站建议事件吞吐量（按事件类型）</strong> – 按事件类型（已关闭、已抑制、已展示、已触发、已互动、已发送）细分的建议事件吞吐量。</li>
</ul>
<p>有关更多信息，请参阅<a href="../data/monitoring.md">详细文档</a>。</p>
<p>发布日期： 2026年9月24日</p>
</td>
</tr>
</tbody>
</table>

### 集成 {#sep-26-integrations}

以下功能即将在此版本中集成。

+++ 即将推出 — **以下信息可能会随时更改。**


* **Experience Manager片段的动态令牌替换** - Experience Manager内容片段引用现在支持&#x200B;**tokenSubstitution**&#x200B;属性。 当设置为`false`时，片段的字段中的个性化设置将直接解析，而无需引用中的令牌映射。 默认值为`true`，这将保留现有行为。

  此功能仅面向一部分组织（限量发布）。 要获得访问权限，请与 Adobe 代表联系。

* **Decisioning中的AEM Managed Services内容片段支持** - Decisioning在管理决策项目时现在支持AEM Managed Services内容片段。


+++

### 个性化 {#sep-26-personalization}

* **使用AI修复语法** — 在验证表达式时，如果检测到PQL语法错误，则Personalization编辑器会提供“使用AI修复”选项，以帮助直接从编辑器解决问题。 [了解更多信息](../personalization/personalization-build-expressions.md#validation-mechanisms)。

  发布日期：2026年9月22日

### 决策 {#sep-26-decisioning}

此版本中的决策功能即将提供以下功能和改进。

<table>
<thead>
<tr>
<th><strong>支持在网页渠道中使用决策功能</strong><br/></th>
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

<table>
<thead>
<tr>
<th><strong>Co-worker中的决策解释器</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>CX Coworker中新增的<strong>决策解释器</strong>技能可让您以自然语言询问，为什么特定优惠已或未向配置文件或区段显示、跟踪资格、上限、排名以及决策中涉及的候选池。</p>
<p>有关更多信息，请参阅<a href="../experience-decisioning/experience-decisioning-coworker-skills.md#decisioning-explainer">详细文档</a>。</p>
<p>发布日期：2026年9月16日</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>同事的规则和排名</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>CX Coworker中新增的<strong>规则和排名</strong>技能允许您使用自然语言创建、解释、模拟和优化资格规则和排名公式，而无需手动编写或验证PQL语法。</p>
<p>有关更多信息，请参阅<a href="../experience-decisioning/experience-decisioning-coworker-skills.md#rules-ranking">详细文档</a>。</p>
<p>发布日期：2026年9月16日</p>
</td>
</tr>
</tbody>
</table>

* **Decisioning中的AEM内容片段可供Managed Services客户使用** — 以前，Decisioning中的AEM内容片段仅可供&#x200B;**Adobe Experience Manager as a Cloud Service**&#x200B;集成的客户使用。 此功能现在也可供使用&#x200B;**Adobe Experience Manager Managed Services**&#x200B;的客户使用。 [了解详情](../experience-decisioning/items.md#attributes)

  发布日期：2026年9月23日

* **支持在规则和排名公式模拟中使用 Adobe Experience Platform 轮廓** – 在模拟规则或排名公式时，您现在可以选择 Adobe Experience Platform 轮廓以自动填充测试数据变体的属性，而无需手动输入。 [了解详情](../experience-decisioning/ranking/ranking-formulas.md#simulate-ranking-formula)

  发布日期：2026年9月22日

### 受众 {#sep-26-audiences}

以下提醒适用于此版本中的受众。

* **受众组合扩充受众即将发生变更** – 在 10 月版本（10 月底发布）中，Journey Optimizer 将停止运行以下历程和营销活动：其使用或引用的“受众构成”受众的源数据集缺少&#x200B;**主身份标识描述符**。 从那时起，在历程和营销活动中，仅支持使用主身份标识描述符构建的“受众构成”受众。 如果您需要让这些历程或营销活动保持活跃状态，请联系您的 Adobe 代表 – 我们的产品团队可以帮助您进行迁移。<!-- Documentation link: TBD -->

### 管理 {#sep-26-administration}

以下提醒适用于此版本中的管理工作。

* **数据集生存时间 (TTL) 护栏 – 现有沙盒** – 从 2026 年 10 月 1 日开始，将在现有客户沙盒和组织上强制实施 Journey Optimizer 系统生成的数据集的生存时间 (TTL) 护栏（轮廓存储为 90 天，数据湖为 13 个月）。

### 易用性改进 {#sep-26-usability}

* **在新的历程画布中更轻松地分离和连接分支** – 现在，您可以将某个分支从历程的其余部分中分离出来，而无需将其删除，并在之后将其重新连接到不同的位置。具体操作方式有两种：直接在画布上选择符合条件的活动，或从已断开连接或已使用的分支列表中进行选取。 [了解详情](../building-journeys/using-the-journey-designer.md#join-and-detach-branches)

  发布日期：2026 年 9 月 1 日

+++ 即将推出 — **以下信息可能会随时更改。**

* **内容模拟体验的易用性改进** – 全新的内容模拟体验现在允许您为变体命名并进行整理，以便轻松比较；可以直接从每张卡片复制或删除变体详情；按需查看完整属性路径和每张卡片的渠道配置；还可以通过更醒目的上传按钮上传您自己的 CSV、JSON 或 JSONL 配置文件。

* **营销活动、历程和编排的营销活动的统一日历** – 历程和营销活动的日历视图现已从各自独立的清单中移出，整合到一个可通过左侧边栏访问的统一菜单中，并在一个合并视图中同时显示两者。

+++
