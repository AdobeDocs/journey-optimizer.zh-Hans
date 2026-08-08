---
solution: Journey Optimizer
product: journey optimizer
title: Journey Optimizer 的预发行说明
description: Adobe Journey Optimizer 预发行说明
feature: Release Notes
exl-id: 6e7d1300-8efd-4fdc-90e3-3ccdc3babd2f
TQID: https://experienceleague.adobe.com/951PJzmmITN1nSUapVomlYnPws9pS0TosI1Gl3R9yL4
hide: true
product_v2:
  - id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2:
  - id: a7b2bfc5-be71-4740-b371-76fa6be8df02
subfeature_v2:
  - id: eac3bd2c-b027-4dfa-80d2-0bd752ae4794
  - id: e437f8db-d1f7-44c0-bdc0-b0a361adc4c0
  - id: c4e1378f-bb85-43a2-8b7c-1623ad3b14b5
source-git-commit: 1b68a987121407a6fa95f21fb328ad2d349108c0
workflow-type: tm+mt
source-wordcount: 1839
ht-degree: 20%

---


# 预发行说明 {#e-release-notes}

Adobe Journey Optimizer 不断地提供新功能、对现有功能的增强和错误修复。 所有更改会在每月末整合到[发行说明](release-notes.md)中。

## 2026年8月预发行说明 {#august-26-rn}

**以下预发行说明可能会在正式发行日期之前有所更改，恕不另行通知**。 一旦更改发布到生产环境，链接、屏幕和更新的文档就会发布。 虽然大多数更改都在发布日期交付，但其中一些更改可能会稍后推出。

另请参阅 [Adobe Experience Platform 预发行说明](https://experienceleague.adobe.com/zh-hans/docs/experience-platform/release-notes/pre-release-notes){target="_blank"}。

**发行日期**：2026年8月18日至19日

### 入门 {#august-26-onboarding}

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
<p>通过引导式功能，可帮助您将现有电子邮件内容和历程移入Journey Optimizer，更轻松地从另一个营销平台转换到Adobe Journey Optimizer。 专用工作区可让您重复利用现有资源，而不是从头开始重建。</p>
<p>此功能此前为有限发布版，现已可供所有环境使用（正式发布版）。</p>
<p><a href="https://jira.corp.adobe.com/browse/DOCAC-15330">DOCAC-15330</a></p>
<!-- GIF placeholder: to be added -->
<!-- Documentation link: TBD -->
</td>
</tr>
</tbody>
</table>

### 历程 {#august-26-journeys}

在此版本中，历程中即将提供以下功能和改进。

<table>
<thead>
<tr>
<th><strong>历程级维持</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>您现在可以直接从历程属性为历程配置维持组。 维持是目标受众中可配置的百分比，该受众不会进入历程且不会收到任何通信。 通过将保留用户档案与Customer Journey Analytics报表中的活动用户档案进行比较，您可以衡量旅程带来的增量提升（真实影响）。</p>
<p><a href="https://jira.corp.adobe.com/browse/DOCAC-15162">DOCAC-15162</a></p>
<!-- GIF placeholder: to be added -->
<!-- Documentation link: TBD -->
</td>
</tr>
</tbody>
</table>

* **在历程表达式编辑器中添加新的dateDiff函数** — 历程表达式编辑器现在包含`dateDiff`函数，该函数计算两个日期之间的天数差。 此函数对于基于时间的逻辑很有用，例如创建截止日期、计算客户生命周期持续时间或在历程条件中构建倒计时计时器。 <a href="https://jira.corp.adobe.com/browse/DOCAC-15293">DOCAC-15293</a> <!-- Documentation link: TBD -->

* **历程标题中的开始和结束日期** — 在历程中配置开始和/或结束日期后，它们现在会显示在历程标题中的状态标记旁边。 显示的标签会根据每个日期即将到来还是已经过去进行调整。 <a href="https://jira.corp.adobe.com/browse/DOCAC-14702">DOCAC-14702</a> <!-- Documentation link: TBD -->

### 营销活动 {#august-26-camp}

此版本中的营销活动即将推出以下功能和改进。

<table>
<thead>
<tr>
<th><strong>活动中的入站体验模拟</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>您现在可以在上线之前在“操作”营销活动中模拟入站渠道操作。 使用模拟模式通过模拟用户测试您的配置并预览呈现的体验，包括生成的URL和二维码，因此您可以端到端地验证规则、决策和内容呈现。</p>
<p>此功能当前为私有测试版，仅向有限的组织提供。 请联系 Adobe 代表以获取更多信息。</p>
<p><a href="https://jira.corp.adobe.com/browse/DOCAC-15166">DOCAC-15166</a></p>
<!-- GIF placeholder: to be added -->
<!-- Documentation link: TBD -->
</td>
</tr>
</tbody>
</table>

* **营销活动文件夹** — 您现在可以将营销活动组织到文件夹中，以改进界面中的导航和管理。 <a href="https://jira.corp.adobe.com/browse/DOCAC-15098">DOCAC-15098</a> <!-- Documentation link: TBD -->

* **营销活动仪表板中的品牌一致性分数** – 您现在可以直接在营销活动仪表板中评估品牌一致性分数，以确保内容符合品牌形象。 这使您无需打开内容设计器即可一目了然地验证各项准则。 <a href="https://jira.corp.adobe.com/browse/DOCAC-14516">DOCAC-14516</a> <!-- Documentation link: TBD -->

* **覆盖营销活动中的默认执行字段** — 该功能此前仅在历程级别可用，现在可覆盖在营销活动参数中为电子邮件、短信和 WhatsApp 投放全局设置的默认执行字段。 <a href="https://jira.corp.adobe.com/browse/DOCAC-14718">DOCAC-14718</a> <!-- Documentation link: TBD -->

### 编排的营销活动 {#august-26-oc}

在此版本中，编排的营销活动中即将提供以下功能和改进。

<table>
<thead>
<tr>
<th><strong>免打扰时间支持</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>您现在可以应用免打扰时间。 无讯息小时允许您定义基于时间的排除来防止在特定时段发送消息，从而帮助您跨活动编排用例尊重客户偏好和合规性要求。</p>
<p><a href="https://jira.corp.adobe.com/browse/DOCAC-14054">DOCAC-14054</a></p>
<!-- GIF placeholder: to be added -->
<!-- Documentation link: TBD -->
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
<p>您现在可以直接将LINE操作添加到营销策划。 这项新活动允许您构建并提供高度个性化的内容，包括文本、标签、图像、视频、位置数据和丰富的Flex消息，从而在LINE平台上无缝吸引客户。 此功能仅面向一部分组织（限量发布）。 要获得访问权限，请与 Adobe 代表联系。</p>
<p><a href="https://jira.corp.adobe.com/browse/DOCAC-14905">DOCAC-14905</a></p>
<!-- GIF placeholder: to be added -->
<!-- Documentation link: TBD -->
</td>
</tr>
</tbody>
</table>

* **能够管理配置文件目标维度** — 您现在可以删除配置文件目标Dimension，或者编辑和交换其配置的身份命名空间，从而更好地控制数据设置，提高灵活性。 <a href="https://jira.corp.adobe.com/browse/DOCAC-15018">DOCAC-15018</a> <!-- Documentation link: TBD -->

* **新的公共API** — 现已提供新的API规范。 这些API允许您以编程方式创建、管理和触发编排的营销活动，实现与外部系统和自动化管道的更深集成。 <a href="https://jira.corp.adobe.com/browse/DOCAC-14308">DOCAC-14308</a> <!-- Documentation link: TBD -->

* **为每个收件人和营销活动个性化电子邮件发件人详细信息** — 现在，编排的营销活动可使用用户档案属性或关系数据对电子邮件标题字段（包括发件人姓名、发件人地址和回复地址）进行个性化。 这允许发件人详细信息反映每个收件人的相关顾问、位置或分支，而不是通过单个公司地址路由所有发送。 可以在渠道级别设置标题值，并使用上下文数据覆盖每个营销活动的标题值，以实现更精确的控制。 <a href="https://jira.corp.adobe.com/browse/DOCAC-13761">DOCAC-13761</a> <!-- Documentation link: TBD -->

* **目标维度简化** — 活动定向维度现在显示在工作流画布上，以便您查看渠道活动使用了哪个维度。 多实体分段流程更简单，因为您不再需要单独的“更改维度”活动。 此外，您现在可以明确选择是在用户档案级别还是在辅助维度级别发送消息。 <a href="https://jira.corp.adobe.com/browse/DOCAC-13554">DOCAC-13554</a> <!-- Documentation link: TBD -->

* **使用批次发送** — 您现在可以计划出站消息以受控批次形式随时间传递。 波次发送非常适合大流量或对时间敏感的活动，还支持更好的可投放性，并通过降低标记为垃圾邮件的风险来帮助保持发件人的良好声誉。 <a href="https://jira.corp.adobe.com/browse/DOCAC-13990">DOCAC-13990</a> <!-- Documentation link: TBD -->

### 渠道 {#august-26-channels}

此版本中的渠道即将提供以下功能和改进。

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
<p><a href="https://jira.corp.adobe.com/browse/DOCAC-11548">DOCAC-11548</a></p>
<!-- GIF placeholder: to be added -->
<!-- Documentation link: TBD -->
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>API触发的电子邮件中的个性化PDF附件</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Journey Optimizer现在支持在API触发的营销活动中，每封电子邮件最多附加5个特定于收件人的PDF。 PDF文件将从数据登陆区安全获取，并在发送时附加，每个文件的位置直接传递到API有效负载中。 这允许保留现有的上游文档生成系统，由Journey Optimizer处理投放。</p>
<p>受支持的用例包括发票、对帐单、票证、合同、运输标签和类似的文档，这些文档因收件人而异。 个性化PDF附件仅在API触发的营销活动中可用，在历程或编排的营销活动中不受支持。</p>
<p>PDF附件加载项支持更大的附件卷和大小；有关更多信息，请与Adobe代表联系。</p>
<p><a href="https://jira.corp.adobe.com/browse/DOCAC-15186">DOCAC-15186</a></p>
<!-- GIF placeholder: to be added -->
<!-- Documentation link: TBD -->
</td>
</tr>
</tbody>
</table>

* **LINE 频道：创作功能更改**：LINE 频道 UI 已升级，具有高级消息创作功能。 此发行版本引入了对多种消息格式的支持，包括文本、图像、图像映射、轮播和Flex （JSON编辑器），以及实时设备预览。 用户现在可以管理由最多五条有序消息组成的分组消息（提供添加、删除和重新排序控件），并使用集成的个性化编辑器实现经过验证的动态消息传送。 <a href="https://jira.corp.adobe.com/browse/DOCAC-14869">DOCAC-14869</a> <!-- Documentation link: TBD -->

* **吞吐量的性能加载项 — 推送** — 在API触发的营销活动中提供新的高吞吐量事务性消息传递模式。 此模式专为大规模实时事务型消息传递而设计，支持每秒最多 5,000 个事务并具有较高的可用性。 以前仅适用于电子邮件渠道，而现在此功能也可用于推送渠道，适用于已购买Adobe高吞吐量事务性消息传递附加产品的组织。 请联系 Adobe 客户代表以获取更多详情。 <a href="https://jira.corp.adobe.com/browse/DOCAC-14717">DOCAC-14717</a> <!-- Documentation link: TBD -->

### 决策 {#august-26-decisioning}

此版本中的Decisioning即将进行以下改进。

* **决策中的投放位置级别频率上限** — 决策中的频率上限规则现在可以将范围限定到单个投放位置，从而让您能够更好地控制优惠在给定界面中的显示频率。 有两种模式可用：特定于投放位置的上限，定义仅在选件显示在选定投放位置时应用的上限；以及按投放位置的上限，用于在出现选件的每个投放位置中独立应用上限，因此每个投放位置都会维护其自己的上限计数器。 请注意，与投放相关的最高限额不适用于使用基于Adobe Experience Platform数据的规则设置的最高限额。 <a href="https://jira.corp.adobe.com/browse/DOCAC-14980">DOCAC-14980</a> <!-- Documentation link: TBD -->

### 电子邮件设计器 {#august-26-email}

此版本中的Email Designer即将进行以下改进。

* **电子邮件Designer中的新表组件** - Email Designer现在包含一个内置的表组件，允许您直接在电子邮件中构建行和列中的内容。 将组件拖放到画布上，自定义行和列的数量，并单独设置每个单元格的样式，以创建清晰、有序的布局，而无需依赖自定义HTML。 <a href="https://jira.corp.adobe.com/browse/DOCAC-15093">DOCAC-15093</a> <!-- Documentation link: TBD -->

### 管理 {#august-26-administration}

此版本中的管理即将进行以下改进。

* **自定义子域的反馈循环OTP流程** — 反馈循环(FBL)自定义子域配置流程已得到改进，直接在产品UI中显示Yahoo发件人中心一次性密码(OTP)。 用户现在可以自动检索和显示Yahoo发件人中心域所有权验证期间生成的OTP。 <a href="https://jira.corp.adobe.com/browse/DOCAC-14815">DOCAC-14815</a> <!-- Documentation link: TBD -->

### 可用性改进 {#august-26-usability}

此版本中提供了以下可用性改进。

* **内容变体的新内容模拟体验** - **模拟内容**&#x200B;工作流引入了重新设计的体验：所有变体现在都在单个可滚动网格（并排、栈叠或包装布局）中一起呈现，并替换一次一个变体的视图。 单个底部操作栏可整合测试变体之间的导航、缩放、视区切换（桌面/移动设备）、区域设置切换、添加示例输入、使用AI生成变体、选取和保存模拟用户，以及导入或导出变体。 移除左边栏并折叠额外的页眉层可大幅增加预览的空间。 通过底部操作栏中的&#x200B;**切换到经典体验**&#x200B;选项，您可以随时还原到之前的体验。 <a href="https://jira.corp.adobe.com/browse/DOCAC-15285">DOCAC-15285</a> <!-- Documentation link: TBD -->

* **历程清单中的批量操作** — 您现在可以直接从历程清单列表中执行新的批量操作，从而更快地同时管理多个历程。 选择多个历程并在单步中应用以下任何新操作：**添加到包**、**删除**、**移动到文件夹**、**编辑标记**&#x200B;或&#x200B;**管理访问权限**。 这降低了逐个历程重复相同操作的需要，并简化了处理大量历程的团队的历程管理。 <a href="https://jira.corp.adobe.com/browse/DOCAC-15358">DOCAC-15358</a> <!-- Documentation link: TBD -->

<!--

## June '26 pre-release notes {#june-26-rn}

**The pre-release notes below are subject to change without prior notice until the release availability date**. Links, screens and updated documentation are published once changes are live in production. While most changes are delivered on the release date, a few may roll out later — refer to the Availability Date listed for each entry for details.

See also [Adobe Experience Platform Pre-release notes](https://experienceleague.adobe.com/zh-hans/docs/experience-platform/release-notes/pre-release-notes){target="_blank"}.

**Release date**: June 16-17, 2026

### Journeys {#june-26-journeys}

The following capabilities and improvements are coming to journeys in this release.

* **Increased live journey limit and new guardrails** - You can now have up to **200 active journeys**, increased from the previous limit of 100.



### Orchestrated campaigns {#june-26-oc}

The following capabilities and improvements are coming to orchestrated campaigns in this release.

-->


