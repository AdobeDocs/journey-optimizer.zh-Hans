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
product_v2: id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2: id: a7b2bfc5-be71-4740-b371-76fa6be8df02
subfeature_v2: id: eac3bd2c-b027-4dfa-80d2-0bd752ae4794id: e437f8db-d1f7-44c0-bdc0-b0a361adc4c0id: c4e1378f-bb85-43a2-8b7c-1623ad3b14b5
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554
level_v2: id: b5a62a22-46f7-4f0d-b151-3fc640bef588id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2: id: a004cc84-67b9-4a33-a3a7-8ec7273ef4dcid: bce87dde-a4ab-44c9-8a18-ad66e4ddb377id: d00e9f03-e50b-4162-b143-0c0817c937c2id: e0eb8757-182f-49f3-94a4-1587d16f5094
source-git-commit: 5592f564456edf86e04dc9849c947402126cf161
workflow-type: tm+mt
source-wordcount: 2234
ht-degree: 85%

---

# 发行说明 {#release-notes}

>[!CONTEXTUALHELP]
>id="ajo_homepage_card1"
>title="新增功能"
>abstract="**Adobe Journey Optimizer** 不断地提供新功能、增强现有功能，并修复错误。 所有更改会在每月的最后一周整合到发行说明中。"

[!DNL Adobe Journey Optimizer] 遵循持续交付模式，使 Adobe 能够持续不断地提供新功能、增强功能和修复。 此方法支持以可扩展的方式分阶段推出各种功能，以确保所有环境的性能和稳定性。 由于此模型，在每月发行版本之间会更新发行说明。 有关发行周期和可用性阶段的完整详细信息，请参阅 [Journey Optimizer 发行周期](releases.md)。

[!DNL Adobe Journey Optimizer] 原生构建于 [!DNL Adobe Experience Platform] 之上并继承了其所具备的最新创新技术和改进。 在 [Adobe Experience Platform 发行说明](https://experienceleague.adobe.com/docs/experience-platform/release-notes/latest.html?lang=zh-Hans){target="_blank"}中进一步了解这些更改。

>[!NOTE]
>
>这些发行说明中列出的功能包括&#x200B;**可用日期**，该日期指明每项变更在您的环境中何时可供使用。 **即将推出**&#x200B;折叠面板中的条目预计将在未来几天或几周内列出。 这些部分中的信息可能随时更改。

## 2026年9月更新 {#sep-26-updates}

### 历程 {#sep-26-journeys}

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

* **历程表达式编辑器中的新dateDiff函数** — 历程表达式编辑器现在包含`dateDiff`函数，该函数计算两个日期之间的天数差。 此函数对于基于时间的逻辑很有用，例如创建截止日期、计算客户生命周期持续时间或在历程条件中构建倒计时计时器。  [了解详情](../building-journeys/functions/date-functions.md#dateDiff)

  发布日期：2026年9月1日

### 营销活动 {#sep-26-campaigns}

+++ 即将推出 — **以下信息可能会随时更改。**

<table>
<thead>
<tr>
<th><strong>操作营销活动中的入站体验模拟</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>您现在可以在上线之前在“操作营销活动”中模拟入站渠道操作。 使用模拟模式通过模拟用户测试您的配置并预览渲染的体验，包括生成的 URL 和 QR 代码，因此您可以端到端地验证规则、决策和内容渲染。</p>
<p>此功能当前为 Private Beta 版，仅向有限的组织提供。 请联系 Adobe 代表以获取更多信息。</p>
<p>发布日期：2026年9月4日</p>
</td>
</tr>
</tbody>
</table>

* **操作营销活动文件夹** — 您现在可以将操作营销活动组织到文件夹中，以改进界面中的导航和管理。

* **操作营销活动创作流程重新设计** - Adobe Journey Optimizer 操作营销活动创作流程已重新设计，可提供更加直观、高效且无缝的用户体验。

* **覆盖操作营销活动中的默认执行字段** — 以前在历程级别可用，但现在您可以在操作营销活动参数中覆盖为电子邮件、短信和WhatsApp投放全局配置的默认执行字段。

+++

## 2026 年 8 月发行说明 {#aug-26-updates}

### 内容管理

在此版本中，Content Management 中添加了以下功能和改进。

<table>
<thead>
<tr>
<th><strong>用于 AI 内容生成的灵活图像源</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>现在，在 Journey Optimizer 中生成内容时，直接从 Adobe Experience Manager Assets Essentials 及更高版本中获取品牌批准的图像。 控制平衡的模式有三种：平衡（以数字资产管理为主，AI 填补空缺，默认）、资产（以数字资产管理为来源）和创意 (AI)。</p>
<p><img src="../content-management/assets/image-mode-3.png"></p>
<p>有关更多信息，请参阅<a href="../content-management/generative-uc.md#image-mode">详细文档</a>。</p>
<p> 发布日期：2026 年 8 月 5 日</p>
</td>
</tr>
</tbody>
</table>

* **内容变体大小警告** - 现在，当内容变体超过其建议的大小阈值时，Journey Optimizer 会显示软限制警告 — 模板和消息为 1200 KB，片段为 700 KB，登陆页为 1000 KB。 不会阻止保存和发布。 [了解详情](../start/guardrails.md#content-authoring)

  发布日期： 2026年8月25日

* **内容片段计数限制** - Journey Optimizer 现在验证一段内容中使用的唯一片段数量：每个变体最多 60 个，单个消息的所有变体最多 120 个。 当达到每个限制的 75% 时会出现警告；一旦达到硬限制，发布将被阻止。 [了解详情](../start/guardrails.md#fragments-guardrails)

  发布日期： 2026年8月25日

### 历程 {#aug-26-journeys}


* **历程标题中的开始和结束日期** — 在历程中配置开始和/或结束日期时，它们现在显示在状态徽章旁边的历程标题中。 显示的标签会根据每个日期即将到来还是已经过去进行调整。 [了解更多](../building-journeys/journey-properties.md#dates)

  发布日期： 2026年8月20日

* **高级表达式编辑器中的新列表函数** — 高级表达式编辑器中提供了两个新函数： `mergeLists`将两个带有或不带有重复数据删除的列表组合在一起，`differenceLists`返回一个列表中不存在其他列表的项目。 [了解详情](../building-journeys/functions/list-functions.md)

  发布日期：2026 年 8 月 13 日

* **等待活动中的发送时间优化** — 等待活动中现在提供发送时间优化，可让 Adobe 的 AI 确定继续任何下游活动的最佳时间。 [了解详情](../building-journeys/wait-activity.md#sto-wait)

  发布日期：2026 年 8 月 13 日

### 营销活动 {#aug-26-campaigns}

在此版本中，Campaigns 中添加了以下功能和改进。

<table>
<thead>
<tr>
<th><strong>API 触发的电子邮件中的个性化 PDF 附件</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>现在，Journey Optimizer 在 API 触发的营销活动中支持向每封电子邮件添加最多 <b>5 个 PDF 附件</b>，包括静态和收件人特定的 PDF。 收件人特定的 PDF 文件将从数据登陆区安全获取，并在发送时附加，每个文件的位置直接传递到 API 有效负载中。 这允许保留现有的上游文档生成系统，由 Journey Optimizer 处理投放。</p>
<p>受支持的用例包括发票、对帐单、票证、合同、运输标签和类似的文档，这些文档因收件人而异。 个性化 PDF 附件仅适用于事务性 API 触发的电子邮件营销活动，在历程或编排的营销活动中不受支持。</p>
<p>PDF 附件加载项支持更大的附件卷和大小；有关更多信息，请与 Adobe 代表联系。</p>
<p>有关更多信息，请参阅<a href="../email/pdf-attachments.md#personalized-attachments">详细文档</a>。</p>
<p>发布日期：2026 年 8 月 12 日</p>
</td>
</tr>
</tbody>
</table>

* **每个营销活动生命周期警报订阅** — 除了现有的沙盒级别订阅之外，您现在可以为单个营销活动订阅支持的营销活动生命周期警报。 这样，您就可以监控各个高优先级的营销活动，而不会收到沙盒中每个营销活动的相同警报。 [了解详情](../reports/alerts.md#subscribe-alerts)

  发布日期：2026 年 8 月 13 日

### 编排的营销活动 {#august-26-oc}

在此版本中，Orchestrated Campaigns 中添加了以下功能和改进。

<table>
<thead>
<tr>
<th><strong>免打扰时间</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>您现在可以应用免打扰时间。 “免打扰时间”允许您定义基于时间的排除以防止在特定期间发送消息，从而帮助您跨活动编排用例尊重客户偏好和合规性要求。</p>
<p>有关更多信息，请参阅<a href="../conflict-prioritization/quiet-hours.md">详细文档</a>。</p>
<p>发布日期：2026 年 8 月 18 日</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>按波次发送</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>您现在可以对消息进行计划安排，以受控的分批形式随时间推移进行投放。 波次发送非常适合大流量或对时间敏感的活动，还支持更好的可投放性，并通过降低标记为垃圾邮件的风险来帮助保持发件人的良好声誉。 </p>
<p>有关更多信息，请参阅<a href="../delivery/send-using-waves.md">详细文档</a>。</p>
<p>发布日期：2026 年 8 月 18 日</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>LINE 渠道支持（限量发布）</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>您现在可以将LINE操作添加到编排的营销活动中。 这项新活动允许您构建并提供高度个性化的内容，包括文本、标签、图像、视频、位置数据和丰富的 Flex 消息，从而在 LINE 平台上无缝吸引客户。 此功能仅面向一部分组织（限量发布）。 要获得访问权限，请与 Adobe 代表联系。</p>
<p>有关更多信息，请参阅<a href="../orchestrated/activities/channels.md">详细文档</a>。</p>
<p>发布日期：2026 年 8 月 12 日</p>
</td>
</tr>
</tbody>
</table>

* **管理轮廓目标维度的功能** – 您现在可以删除轮廓目标维度，或者编辑和交换其配置的身份标识命名空间，从而更好地控制数据设置，提高灵活性。 [了解详情](../orchestrated/target-dimension.md)

  发布日期：2026 年 8 月 18 日

<!-- * **New public APIs** - New API specifications are now available. These APIs allow you to programmatically create, manage, and trigger orchestrated campaigns, enabling deeper integration with external systems and automation pipelines. Documentation link: TBD -->

* **按收件人和营销活动个性化电子邮件发件人详细信息（有限发布版）**– 现在，编排的营销活动支持使用轮廓属性或关系数据对电子邮件标头字段进行个性化，包括发件人姓名、发件人电子邮件前缀、回复姓名、回复邮箱以及执行地址。 这允许发件人详细信息反映每个收件人的相关顾问、位置或分支机构，而不是通过单个公司地址路由所有发送。 可以在渠道级别设置标题值，并使用上下文数据覆盖每个营销活动的标题值，以实现更精确的控制。 [了解详情](../orchestrated/activities/channels.md#configuration)

  此功能仅对部分组织开放（有限发布版）。

  发布日期：2026 年 8 月 18 日

* **目标维度简化** — 活动定向维度现在显示在工作流画布上，以便您查看渠道活动使用了哪个维度。 多实体分段流程更简单，因为您不再需要单独的“更改维度”活动。 此外，您现在可以明确选择是在用户档案级别还是在辅助维度级别发送消息。 [了解详情](../orchestrated/activities/channels.md#add)

  发布日期：2026 年 8 月 18 日

### 忠诚度 {#aug-26-loyalty}

<table>
<thead>
<tr>
<th><strong>忠诚度分析技能</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Journey Optimizer引入了<strong>忠诚度洞察</strong>，这是一种新的CX同事技能，可用于询问有关挑战表现的问题以及引入Adobe Experience Platform中的忠诚度字段组中的其他忠诚度计划数据。</p>
<p>有关更多信息，请参阅<a href="../start/ajo-coworker-skills.md#loyalty-skills">详细文档</a>。</p>
<p>发布日期：2026年8月31日</p>
</td>
</tr>
</tbody>
</table>

### 渠道 {#august-26-channels}

* **实时活动执行元数据(executionMetadata)** - API触发的实时活动营销活动（交易和营销）现在支持每个收件人上使用可选的executionMetadata字段。 这样，您可以将自定义键/值数据（如订单ID、忠诚度级别或区域代码）附加到执行。 [了解详情](../mobile-live/create-mobile-live.md#metadata)

  发布日期：2026 年 8 月 19 日

* **用于吞吐量的性能附加组件 - Push** — API 触发营销活动现在提供新的高吞吐量事务型消息传送模式。 此模式专为大规模实时事务型消息传递而设计，支持每秒最多 5,000 个事务并具有较高的可用性。 此功能此前仅适用于电子邮件渠道，现在对于已购买 Adobe 高吞吐量事务型消息传送附加组件的组织，也适用于推送渠道。 请联系 Adobe 客户代表以获取更多详情。 [了解详情](../campaigns/api-triggered-high-throughput.md)

  发布日期：2026 年 8 月 11 日

### 配置 {#august-26-configuration}

* **在自定义子域设置的CSR生成中支持多SAN** — 使用自定义委派方法设置或迁移自定义子域时，证书签名请求(CSR)现在将自动生成，`data.{subdomain}`和`cdn.{subdomain}`都用作使用者备用名称(SAN)。 以前，生成的CSR仅包含`data.{subdomain}`，在提交到证书颁发机构之前需要手动添加`cdn.{subdomain}`。 [了解详情](../configuration/custom-subdomain-migration.md#send-csr-to-ca)

  发布日期： 2026年8月20日

### 决策 {#decisioning-august}

* **决策中的投放位置级别频率上限** - 决策中的频率上限规则现在可以将范围限定到单个投放位置，从而让您能够更好地控制产品建议在给定界面中的显示频率。 有两种模式可用：**特定投放位置的上限**，它定义了一个上限，该上限仅在产品建议显示在选定投放位置时适用；以及&#x200B;**每个投放位置的上限**，该模式将上限独立应用于产品建议出现的每个投放位置，因此每个投放位置都会维护自己的上限计数器。 请注意，与投放相关的最高限额不适用于使用基于Adobe Experience Platform数据的规则设置的最高限额。 [了解详情](../experience-decisioning/items.md#capping)

  发布日期： 2026年8月24日

* **可视化片段中的镜像页面** — 您现在可以将镜像页面插入到可视化片段中。 决策属性在镜像页面链接上正确呈现，即使片段用于利用Decisioning的电子邮件营销活动也是如此。 必须在发布片段之前将镜像页面添加到可视片段，以便显示决策属性。 [了解详情](../email/message-tracking.md#decisioning-mirror-page)

  发布日期：2026 年 8 月 11 日

### 可用性改进 {#august-26-usability}

* **新历程画布中的多选** — 新历程画布体验引入了简化的多节点选择：按住 Shift 键并拖动以同时选择多个节点，而不是分别选择它们。 这使批量操作（如复制、删除或另存为历程片段）能够在多个节点之间高效执行。 [了解详情](../building-journeys/using-the-journey-designer.md#canvas-capabilities)

  发布日期：2026 年 8 月 17 日

* **历程清单中的批量操作** — 您现在可以直接从历程清单列表中执行新的批量操作，从而更快地同时管理多个历程。 选择多个历程并在单步中应用以下任何新操作：**添加到包**、**删除**、**移动到文件夹**、**编辑标记**&#x200B;或&#x200B;**管理访问权限**。 这降低了逐个历程重复相同操作的需要，并简化了处理大量历程的团队的历程管理。 [了解详情](../building-journeys/journey-ui.md)

  发布日期：2026 年 8 月 12 日

* **用于内容测试的新内容模拟体验** - **模拟内容**&#x200B;工作流引入了重新设计的体验：所有变体现在都在单个可滚动网格（并排、栈叠或包装布局）中一起呈现，并替换了一次一个变体的视图。 单个底部操作栏可整合测试变体之间的导航、缩放、视区切换（桌面/移动设备）、区域设置切换、添加示例输入、使用AI生成变体、选取和保存模拟用户，以及导入或导出变体。 移除左边栏并折叠额外的页眉层可大幅增加预览的空间。 通过底部操作栏中的&#x200B;**切换到经典体验**&#x200B;选项，您可以随时还原到之前的体验。 [了解详情](../test-approve/simulate-content-variations.md)

  发布日期：2026 年 8 月 11 日


