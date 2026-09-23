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
source-git-commit: 8519e5f342809046780427f225c7ce6473363710
workflow-type: tm+mt
source-wordcount: '1991'
ht-degree: 21%
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

### 内容管理 {#sep-26-content-management}

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
<p>创建或编辑事件映射现在使用新的**可视化映射生成器**：选择架构，从可搜索的字段选择器中选择字段，将每个字段映射到具有每行连接状态的忠诚度事件字段，并预览自动生成的JSONata表达式，同时提供随时切换到手动JSONata编辑的选项。</p><p>此外，忠诚度管理员中的“事件定义”已重命名为“事件映射”，更新的列表视图可显示人类可读的体验事件架构名称。</p>
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

* **每个成员忠诚度质询完成截止日期** — 忠诚度质询现在支持每个成员的完成截止日期：根据完成要求选择“选择加入后的几天内”，以便根据每个成员的选择加入日期而不是整个计划的固定结束日期计算每个成员的截止日期。 如果同时设置了质询结束日期和此选择加入窗口，则每个成员的截止日期为第一个成员。<!-- Documentation link: TBD -->

+++

### 历程 {#sep-26-journeys}

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

* **Heague Analysis技能** - CX Coworker现在可以扫描您的活动和草稿历程，以查找中断的配置、静默失败、损坏或未使用的资源（例如过时的草稿历程、孤立的数据源和持续的自定义操作错误），并直接在聊天中显示建议的修复。<!-- Documentation link: TBD -->

+++

### 营销活动 {#sep-26-campaigns}

+++ 即将推出 — **以下信息可能会随时更改。**

* **操作营销活动文件夹** — 您现在可以将操作营销活动组织到文件夹中，以改进界面中的导航和管理。

* **覆盖操作营销活动中的默认执行字段** — 以前在历程级别可用，但现在您可以在操作营销活动参数中覆盖为电子邮件、短信和WhatsApp投放全局配置的默认执行字段。

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

### 个性化 {#sep-26-personalization}

* **使用AI修复语法** — 现在，在检测到PQL语法验证错误时，Personalization编辑器会提供“使用AI修复”选项，以帮助直接从编辑器解决问题。

  发布日期：2026年9月22日

### 决策 {#sep-26-decisioning}

* **在规则和排名公式模拟中支持Adobe Experience Platform配置文件** — 在模拟规则或排名公式时，您现在可以选择Adobe Experience Platform配置文件以自动填充测试数据变体的属性，而不是手动输入属性。 [了解详情](../experience-decisioning/ranking/ranking-formulas.md#simulate-ranking-formula)

  发布日期：2026年9月22日

+++ 即将推出 — **以下信息可能会随时更改。**

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
</td>
</tr>
</tbody>
</table>

+++

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

