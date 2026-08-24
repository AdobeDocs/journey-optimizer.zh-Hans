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
source-git-commit: 92d0c79a5773c2d7fd7b3f3c2c4c142df7e39466
workflow-type: tm+mt
source-wordcount: 2112
ht-degree: 20%

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

## 2026年8月发行说明 {#aug-26-updates}

<!--
### Loyalty {#aug-26-loyalty}

<table>
<thead>
<tr>
<th><strong>Loyalty Insights skill</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Journey Optimizer introduces <strong>Loyalty Insights</strong>, a new CX Coworker skill for asking questions about challenge performance and other loyalty program data ingested into the Loyalty field groups in Adobe Experience Platform.</p>
<p>For more information, refer to the <a href="../start/ajo-coworker-skills.md">detailed documentation</a>.</p>
<p>Availability date: August 12, 2026</p>
</td>
</tr>
</tbody>
</table>
-->

### 内容管理

此版本中为内容管理引入了以下功能和改进。

<table>
<thead>
<tr>
<th><strong>用于AI内容生成的灵活图像源</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>现在，在Journey Optimizer中生成内容时，直接从Adobe Experience Manager Assets Essentials及更高版本中获取品牌批准的图像。 控制平衡的模式有三种：平衡（数字资产管理优先，AI填补空白，默认）、Assets（数字资产管理源）和Creative (AI)。</p>
<p><img src="../content-management/assets/image-mode-3.png"></p>
<p>有关更多信息，请参阅<a href="../content-management/generative-uc.md#image-mode">详细文档</a>。</p>
<p> 发布日期：2026年8月5日</p>
</td>
</tr>
</tbody>
</table>


+++ 即将推出 — **以下信息可能会随时更改。**

* **内容变体大小警告** — 现在，当内容变体超过其建议的大小阈值时，Journey Optimizer会显示软限制警告 — 模板和消息为1200 KB，片段为700 KB，登陆页为1000 KB。 不会阻止保存和发布。

* 内容&#x200B;**片段计数限制** - Journey Optimizer现在验证一段内容中使用的唯一片段数：每个变体最多60个，单个消息的所有变体最多120个。 警告显示在每个限制的75%；一旦达到硬限制，将阻止发布。

+++

### 历程 {#aug-26-journeys}


* **历程标题中的开始和结束日期** — 在历程中配置开始和/或结束日期后，它们现在会显示在历程标题中的状态标记旁边。 显示的标签会根据每个日期即将到来还是已经过去进行调整。 [了解更多](../building-journeys/journey-properties.md#dates)


发布日期： 2026年8月20日

* **高级表达式编辑器中的新列表函数** — 高级表达式编辑器中提供了两个新函数： `mergeLists`将两个带有或不带有重复数据删除的列表组合在一起，`differenceLists`返回一个列表中不存在其他列表的项目。 [了解详情](../building-journeys/functions/list-functions.md)

  发布日期： 2026年8月13日

* **等待活动中的发送时间优化** — 等待活动中现在提供发送时间优化，可让Adobe的AI确定继续任何下游活动的最佳时间。 [了解详情](../building-journeys/wait-activity.md#sto-wait)

  发布日期： 2026年8月13日

+++ 即将推出 — **以下信息可能会随时更改。**

<table>
<thead>
<tr>
<th><strong>历程级维持（限量提供）</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>您现在可以直接从历程属性为历程配置维持组。 维持是目标受众中可配置的百分比，该受众不会进入历程且不会收到任何通信。 通过将保留用户档案与Customer Journey Analytics报表中的活动用户档案进行比较，您可以衡量旅程带来的增量提升（真实影响）。</p>
<p>此功能仅面向一部分组织（限量发布）。 要获得访问权限，请与 Adobe 代表联系。</p>
</td>
</tr>
</tbody>
</table>

* **在历程表达式编辑器中添加新的dateDiff函数** — 历程表达式编辑器现在包含`dateDiff`函数，该函数计算两个日期之间的天数差。 此函数对于基于时间的逻辑很有用，例如创建截止日期、计算客户生命周期持续时间或在历程条件中构建倒计时计时器。

+++

### 营销活动 {#aug-26-campaigns}

此版本中的营销活动引入了以下功能和改进。

<table>
<thead>
<tr>
<th><strong>API触发的电子邮件中的个性化PDF附件</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Journey Optimizer现在在API触发的营销活动中，每封电子邮件最多支持<b>5个PDF附件</b>，包括静态和收件人特定的PDF。 收件人特定的PDF文件将从数据登陆区安全获取，并在发送时附加，每个文件的位置直接传递到API有效负载中。 这允许保留现有的上游文档生成系统，由Journey Optimizer处理投放。</p>
<p>受支持的用例包括发票、对帐单、票证、合同、运输标签和类似的文档，这些文档因收件人而异。 个性化PDF附件仅适用于事务性API触发的电子邮件营销活动，在历程或编排的活动中不受支持。</p>
<p>PDF附件加载项支持更大的附件卷和大小；有关更多信息，请与Adobe代表联系。</p>
<p>有关更多信息，请参阅<a href="../email/pdf-attachments.md#personalized-attachments">详细文档</a>。</p>
<p>发布日期： 2026年8月12日</p>
</td>
</tr>
</tbody>
</table>

* **每个营销活动生命周期警报订阅** — 除了现有的沙盒级别订阅之外，您现在可以为单个营销活动订阅支持的营销活动生命周期警报。 这样，您就可以监控各个高优先级的营销活动，而不会收到沙盒中每个营销活动的相同警报。 [了解更多](../reports/alerts.md#subscribe-alerts)
发布日期： 2026年8月13日

+++ 即将推出 — **以下信息可能会随时更改。**

<table>
<thead>
<tr>
<th><strong>Action Campaigns中的入站体验模拟</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>您现在可以在上线之前在“操作营销活动”中模拟入站渠道操作。 使用模拟模式通过模拟用户测试您的配置并预览呈现的体验，包括生成的URL和二维码，因此您可以端到端地验证规则、决策和内容呈现。</p>
<p>此功能当前为私有测试版，仅向有限的组织提供。 请联系 Adobe 代表以获取更多信息。</p>
</td>
</tr>
</tbody>
</table>

* **Action Campaign创作流程重新设计** - Adobe Journey Optimizer Action Campaign创作流程已重新设计，可提供更加直观、高效且无缝的用户体验。

* **操作营销活动文件夹** — 您现在可以将操作营销活动组织到文件夹中，以改进界面中的导航和管理。

* **覆盖操作营销活动中的默认执行字段** — 以前在历程级别可用，但现在您可以在操作营销活动参数中覆盖为电子邮件、短信和WhatsApp投放全局配置的默认执行字段。

+++

### 编排的营销活动 {#august-26-oc}

此版本中的编排活动引入了以下功能和改进。

<table>
<thead>
<tr>
<th><strong>免打扰时间支持</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>您现在可以应用免打扰时间。 “免打扰时间”允许您定义基于时间的排除以防止在特定期间发送消息，从而帮助您跨活动编排用例尊重客户偏好和合规性要求。</p>
<p>有关更多信息，请参阅<a href="../conflict-prioritization/quiet-hours.md">详细文档</a>。</p>
<p>发布日期： 2026年8月18日</p>
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
<p>您现在可以安排出站消息在一段时间内以受控批量投放。 波次发送非常适合大流量或对时间敏感的活动，还支持更好的可投放性，并通过降低标记为垃圾邮件的风险来帮助保持发件人的良好声誉。 </p>
<p>有关更多信息，请参阅<a href="../delivery/send-using-waves.md">详细文档</a>。</p>
<p>发布日期： 2026年8月18日</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>LINE渠道支持（限量发布）</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>您现在可以将LINE操作添加到编排的营销活动中。 这项新活动允许您构建并提供高度个性化的内容，包括文本、标签、图像、视频、位置数据和丰富的Flex消息，从而在LINE平台上无缝吸引客户。 此功能仅面向一部分组织（限量发布）。 要获得访问权限，请与 Adobe 代表联系。</p>
<p>有关更多信息，请参阅<a href="../orchestrated/activities/channels.md">详细文档</a>。</p>
<p>发布日期： 2026年8月12日</p>
</td>
</tr>
</tbody>
</table>

* **能够管理配置文件目标维度** — 您现在可以删除配置文件目标Dimension，或者编辑和交换其配置的身份命名空间，从而更好地控制数据设置，提高灵活性。 [了解详情](../orchestrated/target-dimension.md)

  发布日期： 2026年8月18日

<!-- * **New public APIs** - New API specifications are now available. These APIs allow you to programmatically create, manage, and trigger orchestrated campaigns, enabling deeper integration with external systems and automation pipelines. Documentation link: TBD -->

* **按收件人和营销活动个性化电子邮件发件人详细信息（限量发布）** — 现在，编排的营销活动支持使用用户档案属性或关系数据对电子邮件标题字段（包括发件人姓名、发件人电子邮件前缀、回复姓名和回复电子邮件）以及执行地址进行个性化。 这允许发件人详细信息反映每个收件人的相关顾问、位置或分支，而不是通过单个公司地址路由所有发送。 可以在渠道级别设置标题值，并使用上下文数据覆盖每个营销活动的标题值，以实现更精确的控制。 [了解详情](../orchestrated/activities/channels.md#configuration)

  此功能仅面向一部分组织（限量发布）。

  发布日期： 2026年8月18日

* **目标维度简化** — 活动定向维度现在显示在工作流画布上，以便您查看渠道活动使用了哪个维度。 多实体分段流程更简单，因为您不再需要单独的“更改维度”活动。 此外，您现在可以明确选择是在用户档案级别还是在辅助维度级别发送消息。 [了解详情](../orchestrated/activities/channels.md#add)

  发布日期： 2026年8月18日

### 渠道 {#august-26-channels}

* **实时活动执行元数据(executionMetadata)** - API触发的实时活动营销活动（交易和营销）现在支持每个收件人上使用可选的executionMetadata字段。 这样，您可以将自定义键/值数据（如订单ID、忠诚度级别或区域代码）附加到执行。 [了解详情](../mobile-live/create-mobile-live.md#metadata)

  发布日期： 2026年8月19日

* **吞吐量的性能加载项 — 推送** — 在API触发的营销活动中提供新的高吞吐量事务性消息传递模式。 此模式专为大规模实时事务型消息传递而设计，支持每秒最多 5,000 个事务并具有较高的可用性。 以前仅适用于电子邮件渠道，而现在此功能也可用于推送渠道，适用于已购买Adobe高吞吐量事务性消息传递附加产品的组织。 请联系 Adobe 客户代表以获取更多详情。 [了解详情](../campaigns/api-triggered-high-throughput.md)

  发布日期： 2026年8月11日

### 配置 {#august-26-configuration}

* **在自定义子域设置的CSR生成中支持多SAN** — 使用自定义委派方法设置或迁移自定义子域时，证书签名请求(CSR)现在将自动生成，`data.{subdomain}`和`cdn.{subdomain}`都用作使用者备用名称(SAN)。 以前，生成的CSR仅包含`data.{subdomain}`，在提交到证书颁发机构之前需要手动添加`cdn.{subdomain}`。 [了解详情](../configuration/custom-subdomain-migration.md#send-csr-to-ca)

  发布日期： 2026年8月20日

### 决策 {#decisioning-august}

* **决策中的投放位置级别频率上限** — 决策中的频率上限规则现在可以将范围限定到单个投放位置，从而让您能够更好地控制优惠在给定界面中的显示频率。 有两种模式可用：**特定于投放位置的上限**，它定义了一个上限，该上限仅在选件显示在选定投放位置时适用；以及&#x200B;**每个投放位置的上限**，该模式将上限独立应用于选件出现的每个投放位置，因此每个投放位置都会维护自己的上限计数器。 请注意，与投放相关的最高限额不适用于使用基于Adobe Experience Platform数据的规则设置的最高限额。 [了解详情](../experience-decisioning/items.md#capping)

  发布日期： 2026年8月24日

* **可视化片段中的镜像页面** — 您现在可以将镜像页面插入到可视化片段中。 决策属性在镜像页面链接上正确呈现，即使片段用于利用Decisioning的电子邮件营销活动也是如此。 必须在发布片段之前将镜像页面添加到可视片段，以便显示决策属性。 [了解详情](../email/message-tracking.md#decisioning-mirror-page)

  发布日期： 2026年8月11日

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
<p>Decisioning现在可用于Web渠道。 您可以直接在Web可视编辑器中使用决策策略，向每位访客提供最相关的选件。</p>
</td>
</tr>
</tbody>
</table>

+++

### 可用性改进 {#august-26-usability}

* **历程清单中的批量操作** — 您现在可以直接从历程清单列表中执行新的批量操作，从而更快地同时管理多个历程。 选择多个历程并在单步中应用以下任何新操作：**添加到包**、**删除**、**移动到文件夹**、**编辑标记**&#x200B;或&#x200B;**管理访问权限**。 这降低了逐个历程重复相同操作的需要，并简化了处理大量历程的团队的历程管理。 [了解详情](../building-journeys/journey-ui.md)

  发布日期： 2026年8月12日

* **用于内容测试的新内容模拟体验** - **模拟内容**&#x200B;工作流引入了重新设计的体验：所有变体现在都在单个可滚动网格（并排、栈叠或包装布局）中一起呈现，并替换了一次一个变体的视图。 单个底部操作栏可整合测试变体之间的导航、缩放、视区切换（桌面/移动设备）、区域设置切换、添加示例输入、使用AI生成变体、选取和保存模拟用户，以及导入或导出变体。 移除左边栏并折叠额外的页眉层可大幅增加预览的空间。 通过底部操作栏中的&#x200B;**切换到经典体验**&#x200B;选项，您可以随时还原到之前的体验。 [了解详情](../test-approve/simulate-content-variations.md)

  发布日期： 2026年8月11日

* **新历程画布中的多选** — 新历程画布体验引入了简化的多节点选择：按住Shift键并拖动以同时选择多个节点，而不是分别选择它们。 这使批量操作（如复制、删除或另存为历程片段）能够在多个节点之间高效执行。 [了解详情](../building-journeys/using-the-journey-designer.md#canvas-capabilities)

  发布日期： 2026年8月17日
