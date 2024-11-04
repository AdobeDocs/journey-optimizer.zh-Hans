---
solution: Journey Optimizer
product: journey optimizer
title: 发行说明
feature: Release Notes
topic: Content Management
description: Adobe Journey Optimizer 发行说明
exl-id: 06fa956a-b500-416e-9d42-b683c328e837
source-git-commit: 018ff365780c5064afd94c8f842ca0498fe06065
workflow-type: tm+mt
source-wordcount: '1960'
ht-degree: 79%

---

# 发行说明 {#release-notes}

>[!CONTEXTUALHELP]
>id="ajo_homepage_card1"
>title="新增功能？"
>abstract="**Adobe Journey Optimizer** 不断地提供新功能、对现有功能的增强和错误修复。会在每月的最后一周将所有更改整合到发行说明中。"

[!DNL Adobe Journey Optimizer] 不断地提供新功能、对现有功能进行增强和修复错误。会在每月的最后一周将所有更改整合到发行说明中。[!DNL Adobe Journey Optimizer] 原生构建于 [!DNL Adobe Experience Platform] 之上并继承了其所具备的最新创新技术和改进。在 [Adobe Experience Platform 发行说明](https://experienceleague.adobe.com/docs/experience-platform/release-notes/latest.html?lang=zh-Hans){target="_blank"}中，进一步了解这些更改。

## 2024年10月版 {#24-10-rn}

**发布日期**：2024 年 10 月 29-30 日

### 新功能 {#24-10-features}

此版本新增了以下详细介绍的功能：

<table>
<thead>
<tr>
<th><strong>电子邮件内容锁定</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Journey Optimizer 现在允许您通过锁定整个模板或特定结构和组件来锁定电子邮件模板中的内容。这样可防止无意中编辑或删除内容，让您更好地控制模板自定义，并提高电子邮件营销活动的效率和可靠性。</p>
<p>有关更多信息，请参阅<a href="../content-management/content-locking.md">详细文档</a>。</p>
<img src="assets/do-not-localize/gif-content-locking.gif">
<p>自 2024 年 10 月 24 日起发布</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>历程中基于代码的体验</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>借助基于代码的体验渠道，Adobe Journey Optimizer 允许您对任何入站属性进行高级个性化和测试，从而向不同的接触点无缝投放定制化体验，如 Web 应用程序、移动应用程序、桌面应用程序、视频游戏机、电视连接设备、智能电视、网亭、ATM、物联网设备等。现在，历程画布中提供了基于代码的体验渠道。</p>
<p>有关更多信息，请参阅<a href="../code-based/create-code-based.md">详细文档</a>。</p>
<img src="../assets/do-not-localize/code-based-journey.gif"/>
<p>自 2024 年 10 月 1 日起发布</p>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>历程中的 Web 体验</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>借助 Web 渠道，Adobe Journey Optimizer 允许您通过入站 Web 历程为客户提供个性化 Web 体验。现在，可在历程画布中使用 Web 渠道。</p>
<p>有关更多信息，请参阅<a href="../web/create-web.md">详细文档</a>。</p>
<img src="../assets/do-not-localize/web-journey.gif"/>
<p>自 2024 年 10 月 1 日起发布</p>
</tr>
</tbody>
</table>


<table>
<thead>
<tr>
<th><strong>冲突和优先级管理（限量发布）</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>在 Journey Optimizer 中，管理营销活动和历程的数量和时间至关重要，这样才能避免因过多的交互而让客户不堪重负。Journey Optimizer 现在提供多种冲突管理和优先级设置工具。 <p>有关更多信息，请参阅<a href="../conflict-prioritization/gs-conflict-prioritization.md">详细文档</a>。</p></p><p><ul><li><b>历程频率上限</b>：您现在可以创建要应用于历程的规则集，从而限制每日、每周或每月可以向用户档案发送历程的次数，并控制同时运行的并行历程数量。</li>
<li><b>优先级分数</b>：您现在可以为营销活动或历程分配优先级分数，范围在 0 到 100 之间。数字越大，表示优先级越高。当两个营销活动或历程操作使用同一渠道配置时，Journey Optimizer 将选择具有最高优先级分数的一个。如果营销活动优先级分数相同，则将选择在最早时间修改的营销活动。</li>
<li><b>查看潜在冲突</b>：现在，通过历程和营销活动中新的“查看潜在冲突”按钮，可识别与其他历程或营销活动的重叠部分，例如开始日期、目标受众或所选渠道配置。</li>
<li><b>历程仲裁</b>：此新功能使您能够优先考虑对客户最重要的历程。当客户有资格参加即将到来的更高优先级的历程时，您可以创建一个规则来阻止客户访问较低优先级的历程。</li>
<li><b>按通信类型设置频率上限：</b>通过规则集，您现在可以按通信类型（如销售、促销）设置粒度规则，防止向客户发送过多的内容相似的消息。您可以跨多个渠道控制频率，自动排除过度联系的用户档案，以确保获得更好的客户体验。</li></ul>

<img src="assets/do-not-localize/gif-conflict.gif">

<p>冲突和优先级管理功能面向部分客户限量发布。请注意，未来将会逐步面向更多用户推出这些功能。如果有兴趣加入这些功能的试用候选名单，请联系您的客户团队。</p>

</td>
</tr>
</tbody>
</table>


<table>
<thead>
<tr>
<th><strong>Mobile Ink 与 Adobe Journey Optimizer 集成</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>您现在可以将 Mobile Ink Da Vinci 与 Adobe Journey Optimizer 集成。通过此新集成，您可以： </p>
<p><ul><li>利用 Mobile Ink Da Vinci 产品中的强大功能，为批量营销活动编写并个性化电子邮件变体</li>
<li>使用Da Vinci进行创作，使用Adobe Journey Optimizer进行优化和交付，加快Journey Optimizer客户的从业人员工作流程</li>
<li>使用 Adobe 数据优化 Da Vinci 模型。</li></ul></p>
<p>有关详细信息，请参阅<a href="https://movableink.com/adobe-and-movable-ink">可移动墨迹达芬奇文档</a>。</p>
</tr>
</tbody>
</table>

以前对一组组织(LA)可用，现在所有用户(GA)都可以使用以下功能：

<table>
<thead>
<tr>
<th><strong>电子邮件配置个性化（正式发布） </strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>为增强电子邮件设置的灵活性和控制，您可以在创建电子邮件渠道配置时定义动态子域和个性化标头参数。
</p>
<p>有关更多信息，请参阅<a href="../email/surface-personalization.md">详细文档</a>。</p>
<img src="assets/do-not-localize/surface-perso.gif"/>
<p>自 2024 年 10 月 23 日起发布</p>
</tr>
</tbody>
</table>


<table>
<thead>
<tr>
<th><strong>历程和营销活动中的审批（正式发布）</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>现在，通过审批策略，您可以在 Journey Optimizer 中设置审批流程，从而使营销团队可以确保营销活动及历程在投入使用之前由相应的负责人审查和签署。</p>
<p>有关更多信息，请参阅<a href="../test-approve/gs-approval.md">详细文档</a>。</p>
<img src="assets/do-not-localize/approval.gif"/>
<p>自 2024 年 10 月 22 日起发布</p>
</td>
</tr>
</tbody>
</table>


<table>
<thead>
<tr>
<th><strong>历程中的内容试验（正式发布）</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>已经可用于营销活动，Adobe Journey Optimizer 现在支持历程中的试验。试验是开展在线测试时进行的随机试用，这意味着您将为给定的消息试验接触部分随机选择的用户，并为其他试验或试验组接触另外一组随机选择的用户。公开后，您可以衡量感兴趣的结果指标，如电子邮件打开次数、订阅次数或购买次数。</p>
<p>有关更多信息，请参阅<a href="../content-management/content-experiment.md">详细文档</a>。</p>
</td>
</tr>
</tbody>
</table>


<!--<table>
<thead>
<tr>
<th><strong>Decisioning (General Availability)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Decisioning, previously available for a set of organizations (LA) and known as Experience Decisioning, is now available to all users (GA), including organizations that have purchased the Adobe Healthcare Shield or Privacy and Security Shield add-on offerings.</p><p>Decisioning simplifies personalization by offering a centralized catalog of marketing offers known as 'decision items' and a sophisticated decision engine. This engine leverages rules and ranking criteria to select and present the most relevant decision items to each individual. These decision items are seamlessly integrated into a wide range of inbound surfaces through the code-based experience channel.</p>
<p>For more information, refer to the <a href="../experience-decisioning/gs-experience-decisioning.md">detailed documentation</a>.</p>
</td>
</tr>
</tbody>
</table>-->

<table>
<thead>
<tr>
<th><strong>历程和营销活动中的多语言消息（正式发布）</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>现在，您可以在单个营销活动或历程中轻松创建多种语言的内容。利用此功能，您可以在编辑营销活动或历程时切换语言，简化整个编辑过程，并提高有效管理多语言内容的能力。</p>
<p>有关更多信息，请参阅<a href="../content-management/multilingual-gs.md">详细文档</a>。</p>
<img src="assets/do-not-localize/multilingual.gif">
</td>
</tr>
</tbody>
</table>


<table>
<thead>
<tr>
<th><strong>更新的报告体验（正式发布）</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Journey Optimizer 报告功能现已正式发布 (GA)，改善了与客户历程分析的互操作性，可在两个平台之间实现报告标准化，并提高了数据一致性和可靠性。Journey Optimizer 与 Customer Journey Analytics 之间的这种无缝集成能够帮助更清晰地了解绩效指标，使用户能够做出更加明智的决策。</p>
<p>在正式发布版中引入了四个新功能：创建简单量度、创建和发布受众、使用Insight Builder提出临时问题以及安排报表自动通过电子邮件发送给关键收件人。</p>
<p>有关更多信息，请参阅<a href="../reports/report-cja-manage.md">详细文档</a>。</p>
<img src="assets/do-not-localize/ajo-cja.gif">
<p>重要：目前的报告经验将于2025年1月停用。 在此日期之后，新的报告体验将成为标准。我们建议您熟悉新特性和功能，以确保顺利过渡。<a href="../reports/report-gs-cja.md">了解如何开始使用 Journey Optimizer 的新报告界面</a></p>
<p>自 2024 年 10 月 16 日起发布</p>
</tr>
</tbody>
</table>

<!--The following capabilities are available to all customers in public beta:-->

<table>
<thead>
<tr>
<th><strong>使用示例输入数据测试您的内容（Beta 版）</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>历程优化器现在允许您测试内容的各种变体，方法是：预览内容并使用从文件上传或手动添加的示例输入数据发送电子邮件校样。 系统会自动检测内容中用于个性化的所有用户档案属性，可使用这些属性进行测试以创建多个变体。</p>
<p>此功能目前以公开测试版的形式向所有客户提供，可用于电子邮件、短信和推送通知渠道。</p>
<p>有关更多信息，请参阅<a href="../test-approve/simulate-sample-input.md">详细文档</a>。</p>
<img src="assets/do-not-localize/gif-simulate.gif">
</td>
</tr>
</tbody>
</table>


<!--<table>
<thead>
<tr>
<th><strong>Use Adobe Experience Platform data for personalization (Beta)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Leverage data from Adobe Experience Platform in the personalization editor to personalize your content. To do this, datasets needed for lookup personalization must first be enabled through an API call. Once done, you can use their data to personalize your content into [!DNL Journey Optimizer].</p>
<p>This capability is currently available to all customers as a public beta.</p>
<p>For more information, refer to the <a href="../personalization/lookup-aep-data.md"</a>.</p>
</td>
</tr>
</tbody>
</table>-->

### 改进 {#24-10-improvements}

此版本包含下方列出的改进。

**短信渠道**

* 您现在可以编辑或删除SMS API渠道配置。 [了解详情](../sms/sms-configuration.md)

* 已引入以下增强功能，以通过Infobip和Sinch改善您的短信消息传送功能：

   * 您可以为短信营销活动和历程定义和管理唯一的关键字，从而实现更加个性化和高效的通信。

   * 当关键字无法识别时，您可以创建和投放默认短信消息。

  在[Infobip](../sms/sms-configuration-infobip.md)和[Sinch](../sms/sms-configuration-sinch.md)的SMS配置文档中了解有关这些改进的更多信息。


<!--**Journeys**-->

<!--* **Path experiment in journeys** - With the journey path experiment, you can now define and track key metrics for your journey paths, allowing you to measure the impact of your activities and to provide clearer insights into your performance. -->

&lt;!--* **实时历程的最大数量** - 现在，Journey Optimizer 在生产沙盒上具有 500 个实时历程的护栏，而不是 100 个。实时历程的数量显示在历程画布中。<!-- DOCAC-10977-->

**Web 渠道**

* **Web设计器的非可视化编辑模式** — 作为Journey Optimizer Web设计器的替代方法，您现在可以使用非可视化编辑器向您的网站添加修改。 它允许您手动输入更改，而无需在可视编辑器中打开页面。 如果您无法安装浏览器扩展(如Adobe Experience Cloud可视化帮助程序)，这种非可视化编辑模式非常有用，在Web设计器中加载页面时需要使用该工具。 [了解详情](../web/web-non-visual-editor.md)


**数据集**

* **发送和打开事件** - 从 2024 年 11 月 1 日起，流式分段将不再支持在 Journey Optimizer 跟踪和反馈数据集中使用发送和打开事件。此更改将适用于所有客户沙盒和组织。[了解详情](../data/datasets-ttl.md#segmentation-update)

* **数据集生存时间 (TTL)** - 从 2025 年 2 月起，将在新沙盒和新组织中推出用于 Journey Optimizer 系统生成的数据集的生存时间 (TTL) 护栏，如下所示：

   * 配置文件存储中的数据为 90 天
   * 数据湖中的数据为 13 个月

  此更改将在后续阶段推广到现有的客户沙盒。[了解详情](../data/datasets-ttl.md#ttl)

* 自定义操作中的&#x200B;**参数** — 可用日期：2024年10月3日 — 自定义操作现在支持NULL和可选参数。 [了解详情](../action/about-custom-action-configuration.md#define-the-message-parameters)

**报告**

* **决策报告**&#x200B;现已可用，可提供关于访客如何与您的体验进行交互的基本见解。 [了解详情](../reports/campaign-global-report-cja-code.md#decisioning-kpis)

**数据治理和同意策略** - 发布日期：2024 年 10 月 7 日

* 现在，Journey Optimizer 中的所有渠道都会实施&#x200B;**数据治理策略**。对于在Adobe Experience Platform中创建了策略的客户，这些策略将应用于营销操作，作为渠道配置设置的一部分。 使用配置创建内容时，系统会检查所有个性化字段是否存在任何数据治理违规。如果发现违规，将无法发布历程或营销活动。[了解详情](../action/action-privacy.md)

* **自定义同意政策**&#x200B;现在适用于所有 Journey Optimizer 渠道。在发送消息或投放入站体验之前执行时，系统会检查用户是否同意在接收的内容中使用个性化字段。如果未获得同意，则不会显示体验。[了解详情](../action/consent.md)

  >[!NOTE]
  >
  >目前，同意策略仅适用于已购买 Adobe **Healthcare Shield** 或 **Privacy and Security Shield** 附加产品的组织。

**受众** - 发布日期：2024 年 10 月 8 日

* 定位 CSV 文件受众时，您现在可以在个性化编辑器以及历程和营销活动规则构建器中使用来自文件的属性。[了解详情](../audience/about-audiences.md)

* 现在可以将自定义上传（CSV 文件）中的受众和属性与 Healthcare Shield 或 Privacy and Security Shield 一起使用。

**配置** - 发布日期：2024 年 10 月 23 日

* 在营销活动或历程中使用个性化配置时，您现在可以预览电子邮件内容，以检查您定义的动态设置是否存在潜在错误。[了解详情](../email/surface-personalization.md#check-configuration)

**基于代码的渠道**

* 内容模板现已可用。您可以从开发人员构建的内容模板开始，加快基于代码的体验的创作速度。通过使用内容模板，营销人员可以只修改某些值或字段，而不是构成整个HTML或JSON内容有效负载。 [了解详情](../content-management/content-templates.md)

**决策**

* [Adobe Customer Journey Analytics](https://experienceleague.adobe.com/docs/analytics-platform/using/cja-overview/cja-overview.html?lang=zh-Hans) 用户现在可以在决策（以前称为体验决策）中设置 AI 模型时选择用于进行优化的自定义模型。例如，这允许您在自定义“购买”表上进行优化，而不是使用定义的约束（如点击率）。 [了解详情](../experience-decisioning/ranking.md)

* 将决策策略添加到具有决策功能的基于代码的营销活动时，除了选择策略之外，您现在还可以手动选择单个决策项目。 此外，您现在可以选择多个后备优惠。这可保证返回一定数量的决策项。[了解详情](../experience-decisioning/create-decision.md)
