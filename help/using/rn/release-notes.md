---
solution: Journey Optimizer
product: journey optimizer
title: 发行说明
feature: Release Notes
topic: Content Management
description: Adobe Journey Optimizer 发行说明
exl-id: 06fa956a-b500-416e-9d42-b683c328e837
source-git-commit: f9fdb738210c5450376bdbf86b44d385cd740fd0
workflow-type: tm+mt
source-wordcount: '3101'
ht-degree: 56%

---

# 发行说明 {#release-notes}

>[!CONTEXTUALHELP]
>id="ajo_homepage_card1"
>title="新增功能？"
>abstract="**Adobe Journey Optimizer** 不断地提供新功能、对现有功能的增强和错误修复。会在每月的最后一周将所有更改整合到发行说明中。"

[!DNL Adobe Journey Optimizer] 不断地提供新功能、对现有功能进行增强和修复错误。所有更改将在每个月的最后一周汇总在这些发行说明中。 [!DNL Adobe Journey Optimizer] 原生构建于 [!DNL Adobe Experience Platform] 之上并继承了其所具备的最新创新技术和改进。在 [Adobe Experience Platform 发行说明](https://experienceleague.adobe.com/docs/experience-platform/release-notes/latest.html?lang=zh-Hans){target="_blank"}中，进一步了解这些更改。

## 2024年10月早期发行说明 {#24-10-rn}

>[!CAUTION]
>
>**以下早期发行说明可能会在正式发行日期之前有所更改，恕不另行通知。**&#x200B;链接、屏幕和更新文档在发布日期发布。

**发行日期**：2024年10月29日至30日

### 新功能 {#24-10-features}

此版本引入了下方详述的新功能。

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
</td>
</tr>
</tbody>
</table>


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
<p>以前，电子邮件配置个性化可用于一组组织(LA)，现在所有用户均可使用(GA)。</p>
<p>有关更多信息，请参阅<a href="../email/surface-personalization.md">详细文档</a>。</p>
<img src="assets/do-not-localize/surface-perso.gif"/>
<p>发布日期：2024 年 10 月 23 日</p>
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
<p>以前对一组组织(LA)可用，但现在所有用户(GA)都可以使用审批策略。</p>
<p>有关更多信息，请参阅<a href="../test-approve/gs-approval.md">详细文档</a>。</p>
<img src="assets/do-not-localize/approval.gif"/>
</td>
</tr>
</tbody>
</table>


<table>
<thead>
<tr>
<th><strong>电子邮件配置个性化（正式发布）</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>现在，您可以在创建电子邮件渠道配置时定义动态子域和个性化的标题参数，以提高灵活性和对电子邮件设置的控制。</p><p>通过在营销活动或历程中使用个性化配置，您可以预览电子邮件内容，以检查您定义的动态设置是否存在潜在错误。</p>
<p>以前，电子邮件配置个性化可用于一组组织(LA)，现在所有用户均可使用(GA)。</p>
<p>有关更多信息，请参阅<a href="../email/surface-personalization.md">详细文档</a>。</p>
</td>
</tr>
</tbody>
</table>


<table>
<thead>
<tr>
<th><strong>使用示例输入数据测试您的内容(Beta)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>历程优化器现在允许您测试电子邮件内容的各种变体，方法是预览该内容并使用从CSV文件上传或手动添加的示例输入数据发送校样。 系统会自动检测您的内容中用于个性化的所有配置文件属性，这些属性可用于您的测试以创建多个变体。</p>
<p>此功能当前以Beta版提供。</p>
<!--<p>For more information, refer to the <a href="../email/surface-personalization.md">detailed documentation</a>.</p>-->
</td>
</tr>
</tbody>
</table>


<table>
<thead>
<tr>
<th><strong>冲突和优先级管理（有限可用性）</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>在Journey Optimizer中，管理营销活动和历程的数量和时间至关重要，这样才能避免因过多的交互而让客户不知所措。 Journey Optimizer现在提供了多种用于冲突管理和优先排序的工具。</p><p><ul><li><b>历程频率上限</b>：您现在可以创建要应用于历程的规则集，从而允许您限制个人资料每日、每周或每月的历程次数，并控制同时运行的并行历程次数。</li>
<li><b>优先级得分</b>：您现在可以为营销活动或历程分配从0到100的优先级得分。 数字越大，表示优先级越高。当两个营销活动或历程操作使用相同的渠道配置时，Journey Optimizer将选择具有最高优先级分数的营销活动或历程操作。 如果促销活动具有相同的得分，则将选择最近修改得最低的促销活动。</li>
<li><b>查看潜在冲突</b>：现在，通过历程和营销活动中的新“查看潜在冲突”按钮，可识别与其他历程或营销活动的重叠，例如开始日期、目标受众或所选渠道配置。</li>
<li><b>历程仲裁</b>：此新功能使您能够优先考虑客户最重要的历程。 您可以创建一个规则，以阻止客户进入具有较低优先级的即将到来的历程。</li>
<li><b>按通信类型设置频率上限： </b>通过规则集，您现在可以按通信类型（例如，销售、促销）设置粒度规则，以防止对类似消息的客户造成过载。 您可以跨多个渠道控制频率，自动排除过度请求的用户档案，以确保获得更好的客户体验。</li></ul>
<!--<p>For more information, refer to the <a href="../email/surface-personalization.md">detailed documentation</a>.</p>-->
<p>冲突和优先级管理功能以“有限可用性”提供给选定的客户组。 请注意，这些功能将在未来逐步向更多用户推出。 如果您有兴趣被添加到这些功能的轮候表中，请与您的客户团队联系。</p>
</td>
</tr>
</tbody>
</table>


<table>
<thead>
<tr>
<th><strong>Web设计器的非可视化编辑模式</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>作为Journey Optimizer Web设计器的替代方法，您现在可以使用非可视编辑器向网站添加修改。 它允许您手动输入更改，而无需在可视编辑器中打开页面。
如果您无法安装浏览器扩展(如Adobe Experience Cloud可视化帮助程序)，这种非可视化编辑模式非常有用，在Web设计器中加载页面时需要使用该工具。</p>
<!--p>For more information, refer to the <a href="../email/surface-personalization.md">detailed documentation</a>.</p-->
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
<p>以前可供一组组织(LA)使用，现在所有用户(GA)都可以使用历程中的试验。</p>
</td>
</tr>
</tbody>
</table>


<table>
<thead>
<tr>
<th><strong>Decisioning（正式发布）</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Decisioning以前只适用于一组组织(LA)，现在称为Experience Decisioning，可供所有用户(GA)使用，包括已购买AdobeHealthcare Shield或Privacy and Security Shield附加产品的组织。</p><p>Decisioning通过提供称为“决策项目”的集中营销优惠目录和复杂的决策引擎，简化了个性化。 此引擎利用规则和排名标准来选择最相关的决策项并将其呈现给每个人。 这些决策项目通过基于代码的体验渠道无缝集成到广泛的集客界面中。</p>

<p>有关更多信息，请参阅<a href="../experience-decisioning/gs-experience-decisioning.md">详细文档</a>。</p>
</td>
</tr>
</tbody>
</table>

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
<p>以前，多语言消息仅提供给一组组织(LA)，但现在所有用户均可使用多语言消息(GA)。</p>
<!--p>For more information, refer to the <a href="../configuration/business-rules.md">detailed documentation</a>.</p-->
</td>
</tr>
</tbody>
</table>

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
<li>使用Da Vinci进行创作，使用AJO进行优化和交付，加快Journey Optimizer客户的从业人员工作流程</li>
<li>使用Adobe数据优化Da Vinci模型。</li></ul></p>
<!--p>For more information, refer to the <a href="../code-based/get-started-code-based.md">detailed documentation</a>.</p-->
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
<p>自2024年10月16日起提供</p>
<p>Journey Optimizer报告功能现已正式推出(GA)，并提高了与Customer Journey Analytics功能的互操作性，实现了两个平台的报告标准化，并提高了数据一致性和可靠性。 Journey Optimizer 与 Customer Journey Analytics 之间的这种无缝集成能够帮助更清晰地了解绩效指标，使用户能够做出更加明智的决策。</p>
<p>在正式发布后，引入了四个新功能：创建简单量度、创建和发布受众、使用Insight Builder提出临时问题以及安排报表自动通过电子邮件发送给关键收件人。</p>
<p>有关更多信息，请参阅<a href="../reports/report-cja-manage.md">详细文档</a>。</p>
<img src="assets/do-not-localize/ajo-cja.gif">
<p>重要信息：当前报告体验将于2025年1月停用。 在此日期之后，新的报告体验将成为标准。我们建议您熟悉新特性和功能，以确保顺利过渡。 <a href="../reports/report-gs-cja.md">了解如何开始使用 Journey Optimizer 的新报告界面</a></p>
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
<p>自2024年10月1日起提供</p>
<p>借助基于代码的体验渠道，Adobe Journey Optimizer 允许您对任何入站属性进行高级个性化和测试，从而向不同的接触点无缝投放定制化体验，如 Web 应用程序、移动应用程序、桌面应用程序、视频游戏机、电视连接设备、智能电视、网亭、ATM、物联网设备等。现在，历程画布中提供了基于代码的体验渠道。</p>
<p>有关更多信息，请参阅<a href="../code-based/create-code-based.md">详细文档</a>。</p>
<img src="../assets/do-not-localize/code-based-journey.gif"/>
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
<p>自2024年10月1日起提供</p>
<p>借助 Web 渠道，Adobe Journey Optimizer 允许您通过入站 Web 历程为客户提供个性化 Web 体验。现在，可在历程画布中使用 Web 渠道。</p>
<p>有关更多信息，请参阅<a href="../web/create-web.md">详细文档</a>。</p>
<img src="../assets/do-not-localize/web-journey.gif"/>
</tr>
</tbody>
</table>

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

**数据集**

* **发送和打开事件** — 从2024年11月1日开始，流式分段将不再支持使用Journey Optimizer跟踪和反馈数据集的发送和打开事件。 此更改将应用于所有客户沙盒和组织。 [了解详情](../data/datasets-ttl.md#segmentation-update)

* **数据集生存时间(TTL)** — 从2025年2月开始，将在新沙盒和新组织中向Journey Optimizer系统生成的数据集推出生存时间(TTL)护栏，如下所示：

   * 配置文件存储中的数据为 90 天
   * 数据湖中的数据为 13 个月

  此更改将在后续阶段中推出到现有客户沙盒。 [了解详情](../data/datasets-ttl.md#ttl)

* **自定义操作中的参数**（可用日期：2024年10月3日） — 自定义操作现在支持NULL和可选参数。 [了解详情](../action/about-custom-action-configuration.md#define-the-message-parameters)

**报告**

* **Experience Decisioning报告**&#x200B;现已可用，可提供关于访客如何与您的体验进行交互的基本见解。

**数据治理和同意策略** - 发布日期：2024 年 10 月 7 日

* 现在，Journey Optimizer 中的所有渠道都会实施&#x200B;**数据治理策略**。对于在 Adobe Experience Platform 中创建了策略的客户，这些策略将作为渠道配置设置的一部分应用于营销操作。使用配置创建内容时，系统会检查所有个性化字段是否存在任何数据治理违规。如果发现违规，将无法发布历程或营销活动。[了解详情](../action/action-privacy.md)

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

* 内容模板现已可用。 您可以从开发人员构建的内容模板开始，加快基于代码的体验的创作速度。 通过使用内容模板，营销人员可以只修改某些值或字段，而不是构成整个HTML或JSON内容有效负载。

**决策**

* 在Decisioning（以前称为Experience Decisioning）中设置AI模型时，[Adobe Customer Journey Analytics](https://experienceleague.adobe.com/docs/analytics-platform/using/cja-overview/cja-overview.html?lang=zh-Hans)用户现在可以选择优化自定义模型。 例如，这允许您在自定义“购买”表上进行优化，而不是使用定义的约束（如点击率）。

* 当使用决策（以前称为Experience Decisioning）将决策策略添加到基于代码的营销活动时，除了选择策略之外，您现在还可以手动选择单个决策项目。 此外，您现在可以选择多个备用选件。 这可保证返回一定数量的决策项目。 [了解详情](../experience-decisioning/create-decision.md)

## 2024 年 9 月版 {#24-9-rn}

<!--
>[!CAUTION]
>
>**Early release notes below are subject to change without prior notice until the release date**. Links, screens and updated documentation are published at the release date.
>
-->

**发行日期**：2024 年 9 月 24-26 日

### 新功能 {#24-9-features}

此版本引入了下方详述的新功能。

<table>
<thead>
<tr>
<th><strong>适用于移动设备应用程序和网站的内容卡</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>内容卡是 Adobe Journey Optimizer 中新增的数字消息传送功能，可直接在移动应用和网站内提供个性化且引人入胜的内容。与传统推送通知不同，内容卡无缝集成到用户界面中，提供持续性的非侵入式更新，以增强用户交互和体验。</p>
<p>此功能允许营销人员向用户展示相关的富媒体内容，从而提高参与度，并确保会看到重要消息而不会中断用户历程。</p>
<p>有关更多信息，请参阅<a href="../content-card/get-started-content-card.md">详细文档</a>。</p>
<img src="assets/do-not-localize/content-card.gif"/>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>历程和营销活动中的审批 (LA)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>现在，通过审批策略，您可以在 Journey Optimizer 中设置审批流程，从而使营销团队可以确保营销活动及历程在投入使用之前由相应的负责人审查和签署。</p>
<p>目前，审批策略仅面向一部分组织提供（限量发布版）。要获得访问权限，请与 Adobe 代表联系。</p>
<p>有关更多信息，请参阅<a href="../test-approve/gs-approval.md">详细文档</a>。</p>
<img src="assets/do-not-localize/approval.gif"/>
</td>
</tr>
</tbody>
</table>

<!--<table>
<thead>
<tr>
<th><strong>Email Content Locking</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Journey Optimizer now allows you to lock content in email templates, either by locking the entire template or specific structures and component. This allows you to prevent unintentional edits or deletions, giving you greater control over template customization, and improving the efficiency and reliability of your email campaigns.</p>
<p>For more information, refer to the <a href="../content-management/gs-generative.md">detailed documentation</a>.</p>
<img src="assets/do-not-localize/gif-content-locking.gif">
</td>
</tr>
</tbody>
</table>-->

<table>
<thead>
<tr>
<th><strong>历程中的全局退出标准</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>现在，您可以在历程级别定义退出标准。通过添加退出条件，您可以在事件发生后（例如：购买）或符合受众的条件时，让用户档案立即退出历程。这将阻止用户从历程收到任何进一步的通信。</p>
<p>有关更多信息，请参阅<a href="../building-journeys/journey-properties.md#exit-criteria">详细文档</a>。</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>AI 助手内容加速器 </strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>创建消息并个性化消息后，使用Journey Optimizer中的AI助手内容加速器将您的内容提升到新的级别。 您现在可以使用AI Assistant通过尝试不同的主标题和图像来优化消息的影响。 每个变体都是作为独特的处理方式进行管理，以衡量和比较哪个标题可以有效生成更多点击次数。</p>
<p>通过<a href="https://experienceleague.adobe.com/zh-hans/apps/journey-optimizer/ai-assistant-content-accelerator">我们的实时功能预览</a>获得亲身体验，该预览旨在让您亲自探索其功能并充分了解其能力。</a>。</p>
<p>有关更多信息，请参阅<a href="../content-management/gs-generative.md">详细文档</a>。</p>
<img src="assets/do-not-localize/ai-content.gif"/>
<p>发布日期：2024 年 9 月 12 日</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>引导式渠道设置</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>“引导式渠道设置”让您能够在一个统一的体验中自动化并验证渠道设置，从而加快开始使用 Journey Optimizer 的过程。这一新的引导式设置简化了快速渠道配置，确保能够在 Experience Platform、Journey Optimizer 和数据收集中随时安装并使用所有必要的资源。这使营销、产品和数据工程团队能够快速开始创建营销活动和历程。</p>
<p>有关更多信息，请参阅<a href="../configuration/set-mobile-config.md">详细文档</a>。</p>
<img src="assets/do-not-localize/guided-setup.gif"/>
<p>发布日期：2024 年 9 月 3 日</p>
</br>
</td>
</tr>
</tbody>
</table>


### 改进 {#24-9-improvements}

此版本包含下方列出的改进。

**受众** - 发布日期：2024 年 9 月 17 日

**许可证使用情况** - 许可证使用情况仪表板现在显示“符合资格的用户档案”，而不是“符合资格的受众”。[了解详情](../audience/license-usage.md)

**内容管理**

您现在可以在沙盒中导出内容模板和片段。[了解详情](../configuration/copy-objects-to-sandbox.md)

**历程**

* **实时报告增强功能** - 实时报告可提供有关过去 24 小时内的历程绩效的深入见解。我们添加了新量度（已进入、已退出、已丢弃的用户档案和出错的用户档案）以增强此功能，以便您能直接从历程画布更深入地了解用户行为和表现。[了解详情](../building-journeys/report-journey.md)


* （发布日期：9 月 10 日）**自动重试读取受众** - 现在，在检索导出作业时，重试操作会被默认应用于受众触发的历程（从&#x200B;**读取受众**&#x200B;或&#x200B;**业务事件**&#x200B;开始）。如果在创建导出作业期间发生错误，则每 10 分钟重试一次，最多 1 小时。之后，我们将它视为失败。因此，这些类型的历程可以在预定时间之后 1 小时内执行。[了解详情](../building-journeys/read-audience.md#retries)

**电子邮件渠道**

* **已发送的电子邮件和密件抄送中的邮件标头** - 已为所有电子邮件添加了新邮件标头。对于已发送的每封电子邮件及其对应的密件抄送电子邮件副本来说，此标头值都是唯一的。此外，此标头存储在消息和密件抄送反馈数据集中，允许协调密件抄送副本和相应的已发送电子邮件信息。[了解详情](../configuration/archiving-support.md#bcc-header)

* **垃圾邮件评分** (GA) - 您现在可以在专用的&#x200B;**垃圾邮件报告**&#x200B;中检查您的垃圾邮件内容评分。通过 SpamAssassin，Adobe Journey Optimizer 现在可以测试您的电子邮件内容并为其评分，以检测 ISP 或邮箱提供商是否将其视为垃圾邮件。[了解详情](../content-management/spam-report.md)

**短信渠道**

* **编辑 API 凭据** - 您现在可以编辑短信 API 凭据中的设置，包括更新选择启用/禁用关键字和回复。

**API**

* **营销活动模拟 API** - 使用此 API 触发营销活动的校对作业。发送营销活动验证是一个异步过程，该 API 将返回一个 proofJobId，可用于检查验证的状态。[了解详情](https://developer.adobe.com/journey-optimizer-apis/references/simulations/){target="_blank"}

* （发布日期：9 月 10 日）[Adobe Journey Optimizer API 文档](https://developer.adobe.com/journey-optimizer-apis/references/simulations/){target="_blank"}现在具备交互功能。直接从文档页面探索 API 端点，以获得即时反馈并加快您的技术实施。


  所有 API 参考页面现在都有 **Try it（试试看）**&#x200B;功能，您可以使用它直接在文档网站页面上测试 API 调用。[获取所需的身份验证凭据](https://developer.adobe.com/journey-optimizer-apis/references/authentication/){target="_blank"}并开始使用该功能探索 API 端点。

  使用此新功能来探索 API 端点的请求和响应，以获得即时反馈并加快您的技术实施。

  >[!CAUTION]
  >
  >请注意，通过使用文档页面上的交互式 API 功能，您正在对端点进行真正的 API 调用。在试验生产沙盒时请记住这一点。

**配置**

* **IP 预热计划** - 此功能现在可供所有客户使用，包括已购买 Adobe **Healthcare Shield** 或 **Privacy and Security Shield** 附加产品的组织。[了解详情](../configuration/ip-warmup-gs.md)


![新闻稿](../assets/do-not-localize/nl-icon.png) 立即注册订阅 [Adobe Journey Optimizer 季度新闻稿](https://www.adobe.com/subscription/Adobe_Journey_Optimizer_NL.html){target="_blank"}，每个季度都能在收件箱中直接接收最新产品更新、精彩故事、用例、提示及更多内容。