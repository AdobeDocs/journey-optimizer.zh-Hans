---
solution: Journey Optimizer
product: journey optimizer
title: 发行说明
feature: Release Notes
topic: Content Management
description: Adobe Journey Optimizer 发行说明
exl-id: 06fa956a-b500-416e-9d42-b683c328e837
source-git-commit: 6f517ca209ae992f8daf3b285ccabebac100081b
workflow-type: tm+mt
source-wordcount: '1414'
ht-degree: 48%

---

# 发行说明 {#release-notes}

>[!CONTEXTUALHELP]
>id="ajo_homepage_card1"
>title="新增功能？"
>abstract="**Adobe Journey Optimizer** 不断地提供新功能、对现有功能的增强和错误修复。会在每月的最后一周将所有更改整合到发行说明中。"

[!DNL Adobe Journey Optimizer] 不断地提供新功能、对现有功能进行增强和修复错误。所有更改将在每个月的最后一周汇总在这些发行说明中。 [!DNL Adobe Journey Optimizer] 原生构建于 [!DNL Adobe Experience Platform] 之上并继承了其所具备的最新创新技术和改进。在 [Adobe Experience Platform 发行说明](https://experienceleague.adobe.com/docs/experience-platform/release-notes/latest.html?lang=zh-Hans){target="_blank"}中，进一步了解这些更改。

## 2024年10月版 {#24-10-rn}

**发行日期**：2024年10月29日至30日

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
<p>自2024年10月24日起提供</p>
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
<p>自2024年10月1日起提供</p>
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
<p>自2024年10月1日起提供</p>
</tr>
</tbody>
</table>


<!--<table>
<thead>
<tr>
<th><strong>Conflict and priority management (Limited Availability)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>In Journey Optimizer, managing the volume and timing of campaigns and journeys is essential to avoid overwhelming customers with too many interactions. Journey Optimizer now offers several tools for conflict management and prioritization.</p><p><ul><li><b>Journey frequency capping</b>: You can now create rule sets to apply to your journeys, allowing you to limit the number of journeys for a profile per day, week, or month, as well as control the number of concurrent journeys running simultaneously.</li>
<li><b>Priority score</b>: You can now assign a priority score to a campaign or a journey, ranging from 0 to 100. A higher number indicates a higher priority. When two campaigns or journey actions use the same channel configuration, Journey Optimizer will select the one with the highest priority score. If the campaigns have the same score, the campaign that was least recently modified will be chosen.</li>
<li><b>View potential conflicts</b>: A new "View potential conflicts" button in journeys and campaigns now allows you to identify overlap with other journeys or campaigns such as the start date, the targeted audience, or the selected channel configuration.</li>
<li><b>Journey Arbitration</b>: This new capability enables you to prioritize the most important journeys for your customers. You can create a rule to suppress entry into a lower priority journey when a customer qualifies for an upcoming journey of higher priority.</li>
<li><b>Frequency capping by communication type: </b>With rule sets, you can now set granular rules by communication type (e.g., Sales, Promotional) to prevent overloading customers with similar messages. You can control frequency across multiple channels, automatically excluding over-solicited profiles to ensure a better customer experience.</li></ul>
<p>For more information, refer to the <a href="../email/surface-personalization.md">detailed documentation</a>.</p>
<p>Conflict and priority management capabilities are available in Limited Availability to a select group of customers. Please note that these features will be gradually rolled out to more users in the future. Reach out to your account team if interested in being added to the waitlist for these features.</p>
</td>
</tr>
</tbody>
</table>-->


<table>
<thead>
<tr>
<th><strong>Mobile Ink与Adobe Journey Optimizer集成</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>您现在可以将Mobile Ink Da Vinci与Adobe Journey Optimizer集成在一起。 通过此新集成，您可以： </p>
<p><ul><li>利用Mobile Ink的Da Vinci产品中的强大功能，为批量营销活动汇编和个性化电子邮件变体</li>
<li>使用Da Vinci进行创作，使用Adobe Journey Optimizer进行优化和交付，加快Journey Optimizer客户的从业人员工作流程</li>
<li>使用Adobe数据优化Da Vinci模型。</li></ul></p>
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
<p>为了增强对电子邮件设置的灵活性和控制，您可以在创建电子邮件渠道配置时定义动态子域和个性化标头参数。
</p>
<p>有关更多信息，请参阅<a href="../email/surface-personalization.md">详细文档</a>。</p>
<img src="assets/do-not-localize/surface-perso.gif"/>
<p>自2024年10月23日起提供</p>
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
<p>自2024年10月22日起提供</p>
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

<!--table>
<thead>
<tr>
<th><strong>Multilingual messages in journeys and campaigns (General availability)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>You can now effortlessly create content in multiple languages within a single campaign or journey. With this feature, you can switch between languages when editing your campaign or your journey, streamlining the entire editing process and improving your capability to efficiently manage multilingual content.</p>
<p>For more information, refer to the <a href="../content-management/multilingual-gs.md">detailed documentation</a>.</p>
<img src="assets/do-not-localize/multilingual.gif">
</td>
</tr>
</tbody>
</table-->


<table>
<thead>
<tr>
<th><strong>更新的报告体验（正式发布）</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Journey Optimizer报告功能现已正式推出(GA)，并提高了与Customer Journey Analytics功能的互操作性，实现了两个平台的报告标准化，并提高了数据一致性和可靠性。 Journey Optimizer 与 Customer Journey Analytics 之间的这种无缝集成能够帮助更清晰地了解绩效指标，使用户能够做出更加明智的决策。</p>
<p>在正式发布版中引入了四个新功能：创建简单量度、创建和发布受众、使用Insight Builder提出临时问题以及安排报表自动通过电子邮件发送给关键收件人。</p>
<p>有关更多信息，请参阅<a href="../reports/report-cja-manage.md">详细文档</a>。</p>
<img src="assets/do-not-localize/ajo-cja.gif">
<p>重要：目前的报告经验将于2025年1月停用。 在此日期之后，新的报告体验将成为标准。我们建议您熟悉新特性和功能，以确保顺利过渡。 <a href="../reports/report-gs-cja.md">了解如何开始使用 Journey Optimizer 的新报告界面</a></p>
<p>自2024年10月16日起提供</p>
</tr>
</tbody>
</table>


<!--The following capabilities are available to all customers in public beta:

<table>
<thead>
<tr>
<th><strong>Test your content using sample input data (Beta)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Journey optimizer now allows you to test different variants of your email content by previewing it and sending proofs using sample input data uploaded from a file or added manually. All the profiles attributes used in your content for personalization are automatically detected by the system and can be used for your tests to create multiple variants.</p>
<p>This capability is currently available to all customers as a public beta.</p>
<p>For more information, refer to the <a href="../email/surface-personalization.md">detailed documentation</a>.</p>
</td>
</tr>
</tbody>
</table>-->

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

已引入短信增强功能来改进消息传送功能：

* 您可以为短信活动和历程定义和管理唯一的关键字，从而实现更加个性化和高效的通信。

* 当关键字无法识别时，您可以创建和投放默认短信消息。

* 您现在可以编辑或删除SMS API渠道配置。

<!--**Journeys**-->

<!--* **Path experiment in journeys** - With the journey path experiment, you can now define and track key metrics for your journey paths, allowing you to measure the impact of your activities and to provide clearer insights into your performance. -->

&lt;!—* **最大实时历程数** -Journey Optimizer现在在生产沙盒上具有500个实时历程的护栏，而不是100个。 实时历程的数量在历程画布中可见。<!-- DOCAC-10977-->

**Web 渠道**

* **Web设计器的非可视化编辑模式** — 作为Journey Optimizer Web设计器的替代方法，您现在可以使用非可视化编辑器向您的网站添加修改。 它允许您手动输入更改，而无需在可视编辑器中打开页面。 如果您无法安装浏览器扩展(如Adobe Experience Cloud可视化帮助程序)，这种非可视化编辑模式非常有用，在Web设计器中加载页面时需要使用该工具。 [了解详情](../web/web-non-visual-editor.md)


**数据集**

* **发送和打开事件** — 从2024年11月1日开始，流式分段将不再支持使用Journey Optimizer跟踪和反馈数据集的发送和打开事件。 此更改将应用于所有客户沙盒和组织。 [了解详情](../data/datasets-ttl.md#segmentation-update)

* **数据集生存时间(TTL)** — 从2025年2月开始，将在新沙盒和新组织中向Journey Optimizer系统生成的数据集推出生存时间(TTL)护栏，如下所示：

   * 配置文件存储中的数据为 90 天
   * 数据湖中的数据为 13 个月

  此更改将在后续阶段中推出到现有客户沙盒。 [了解详情](../data/datasets-ttl.md#ttl)

* **自定义操作中的参数**（可用日期：2024年10月3日） — 自定义操作现在支持NULL和可选参数。 [了解详情](../action/about-custom-action-configuration.md#define-the-message-parameters)

**报告**

* **Experience Decisioning报告**&#x200B;现已可用，可提供关于访客如何与您的体验进行交互的基本见解。 [了解详情](../reports/campaign-global-report-cja-code.md##decisioning-kpis)

**数据治理和同意策略** - 发布日期：2024 年 10 月 7 日

* 现在，Journey Optimizer 中的所有渠道都会实施&#x200B;**数据治理策略**。对于在Adobe Experience Platform中创建了策略的客户，这些策略将应用于营销操作，作为渠道配置设置的一部分。 使用配置创建内容时，系统会检查所有个性化字段是否存在任何数据治理违规。如果发现违规，将无法发布历程或营销活动。[了解详情](../action/action-privacy.md)

* **自定义同意政策**&#x200B;现在适用于所有 Journey Optimizer 渠道。在发送消息或投放入站体验之前执行时，系统会检查用户是否同意在接收的内容中使用个性化字段。如果未获得同意，则不会显示体验。[了解详情](../action/consent.md)

  >[!NOTE]
  >
  >目前，同意策略仅适用于已购买 Adobe **Healthcare Shield** 或 **Privacy and Security Shield** 附加产品的组织。

**受众** - 发布日期：2024 年 10 月 8 日

* 定位 CSV 文件受众时，您现在可以在个性化编辑器以及历程和营销活动规则构建器中使用来自文件的属性。[了解详情](../audience/about-audiences.md)

* 现在可以将自定义上传（CSV 文件）中的受众和属性与 Healthcare Shield 或 Privacy and Security Shield 一起使用。

**配置** — 可用日期：2024年10月23日

* 在营销活动或历程中使用个性化配置时，您现在可以预览电子邮件内容，以检查您定义的动态设置是否存在潜在错误。 [了解详情](../email/surface-personalization.md#check-configuration)

**基于代码的渠道**

* 内容模板现已可用。 您可以从开发人员构建的内容模板开始，加快基于代码的体验的创作速度。 通过使用内容模板，营销人员可以只修改某些值或字段，而不是构成整个HTML或JSON内容有效负载。 [了解详情](../content-management/content-templates.md)

**决策**

<!--* [Adobe Customer Journey Analytics](https://experienceleague.adobe.com/docs/analytics-platform/using/cja-overview/cja-overview.html) users can now choose custom models to optimize on when setting up an AI model in Decisioning (formerly known as Experience Decisioning). This allows you, for example, to optimize on a custom "purchases" table rather than defined constraints such as clickthrough rate."-->

* 在使用Experience Decisioning将决策策略添加到基于代码的营销活动时，除了选择策略之外，您现在还可以手动选择单个决策项目。 此外，您现在可以选择多个备用选件。 这可保证返回一定数量的决策项目。 [了解详情](../experience-decisioning/create-decision.md)
