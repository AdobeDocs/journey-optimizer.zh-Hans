---
solution: Journey Optimizer
product: journey optimizer
title: 发行说明
description: Journey Optimizer 早期发行说明
feature: Release Notes
topic: Content Management
hide: true
hidefromtoc: true
exl-id: 6e7d1300-8efd-4fdc-90e3-3ccdc3babd2f
source-git-commit: 61447b6400b65e29a9187790e74be47b09764c4a
workflow-type: tm+mt
source-wordcount: '1967'
ht-degree: 98%

---

# 早期发行说明 {#e-release-notes}

[!DNL Adobe Journey Optimizer] 不断地提供新功能、对现有功能进行增强和修复错误。所有更改会在每月末整合到[发行说明](release-notes.md)中。

**以下早期发行说明可能会在正式发行日期之前有所更改，恕不另行通知。**&#x200B;在发行当日，会在[发行说明](release-notes.md)中发布链接、屏幕和更新文档。

## 2024 年 10 月早期发行说明 {#e-2024}

**发布日期**：2024 年 10 月 29-30 日

### 新功能 {#e-features}

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
<!--p>For more information, refer to the <a href="../content-management/gs-generative.md">detailed documentation</a>.</p>
<img src="assets/do-not-localize/ai-content.gif"/-->
</td>
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
<p>审批策略以前面向一部分组织提供 (LA)，现在面向所有用户提供 (GA)。</p>
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
<p>以前，电子邮件配置个性化功能面向一部分组织提供 (LA)，现在面向所有用户提供 (GA)。</p>
<p>有关更多信息，请参阅<a href="../email/surface-personalization.md">详细文档</a>。</p>
</td>
</tr>
</tbody>
</table>


<table>
<thead>
<tr>
<th><strong>使用示例输入数据测试您的内容（Beta 版）</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Journey Optimizer 现在允许您测试电子邮件内容的各种变体，方法是预览该内容并使用从 CSV 文件上传或手动添加的示例输入数据发送验证。系统会自动检测内容中用于个性化的所有用户档案属性，可使用这些属性进行测试以创建多个变体。</p>
<p>此功能目前作为 Beta 版提供。</p>
<!--<p>For more information, refer to the <a href="../email/surface-personalization.md">detailed documentation</a>.</p>-->
</td>
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
<p>在 Journey Optimizer 中，管理营销活动和历程的数量和时间至关重要，这样才能避免因过多的交互而让客户不堪重负。Journey Optimizer 现在提供多种冲突管理和优先级设置工具。</p><p><ul><li><b>历程频率上限</b>：您现在可以创建要应用于历程的规则集，从而限制每日、每周或每月可以向用户档案发送历程的次数，并控制同时运行的并行历程数量。</li>
<li><b>优先级分数</b>：您现在可以为营销活动或历程分配优先级分数，范围在 0 到 100 之间。数字越大，表示优先级越高。当两个营销活动或历程操作使用同一渠道配置时，Journey Optimizer 将选择具有最高优先级分数的一个。如果营销活动优先级分数相同，则将选择在最早时间修改的营销活动。</li>
<li><b>查看潜在冲突</b>：现在，通过历程和营销活动中新的“查看潜在冲突”按钮，可识别与其他历程或营销活动的重叠部分，例如开始日期、目标受众或所选渠道配置。</li>
<li><b>历程仲裁</b>：此新功能使您能够优先考虑对客户最重要的历程。当客户有资格参加即将到来的更高优先级的历程时，您可以创建一个规则来阻止客户访问较低优先级的历程。</li></ul></p>
<!--<p>For more information, refer to the <a href="../email/surface-personalization.md">detailed documentation</a>.</p>-->
<p>冲突和优先级管理功能面向部分客户限量发布。请注意，未来将会逐步面向更多用户推出这些功能。如果有兴趣加入这些功能的试用候选名单，请联系您的客户团队。</p>

</td>
</tr>
</tbody>
</table>


<table>
<thead>
<tr>
<th><strong>Web 设计器的非可视化编辑模式</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>作为 Journey Optimizer Web 设计器的替代工具，您现在可以使用非可视化编辑器向网站添加修改内容。这允许您手动进行更改，而无需在可视化编辑器中打开页面。
在 Web 设计器中加载页面时，如果您无法安装所需的 Adobe Experience Cloud 可视化帮助程序等浏览器扩展，这种非可视化编辑模式将很有帮助。</p>
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
<p>历程中的试验功能以前面向一部分组织提供 (LA)，现在面向所有用户提供 (GA)。</p>
</td>
</tr>
</tbody>
</table>


<table>
<thead>
<tr>
<th><strong>决策（正式发布）</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>决策在之前被称为体验决策且仅面向一部分组织提供 (LA)，现在面向所有用户提供 (GA)。通过提供称为“决策项”的集中式营销优惠目录和复杂的决策引擎，它简化了个性化操作。此引擎利用规则和排名标准来选择最相关的决策项并将其呈现给每个人。这些决策项通过基于代码的体验渠道无缝集成到广泛的入站表面中。</p>

<p>目前，不向已购买 Adobe Health Shield 和 Privacy and Security Shield 附加产品的客户提供决策功能。</p>

<!--p>For more information, refer to the <a href="../configuration/business-rules.md">detailed documentation</a>.</p-->
</td>
</tr>
</tbody>
</table>


<table>
<thead>
<tr>
<th><strong>规则集（限量发布）</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>您现在可以创建粒度频率上限规则，并通过规则集将它们应用于消息或历程。这项新功能允许您通过设置跨渠道规则来控制受众接收消息的频率，从而自动从消息和操作中排除过度联系的用户档案。</p><p>它还允许您限制每日、每周或每月的历程数量，并控制同时运行的并行历程数量。</p>
<p>规则集功能面向部分客户限量发布。请注意，未来将会逐步面向更多用户推出这些功能。如果有兴趣加入此功能的试用候选名单，请联系您的客户团队。</p>
<!--p>For more information, refer to the <a href="../configuration/business-rules.md">detailed documentation</a>.</p-->
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
<p>在正式发布后，现在可以跨所有渠道访问多语言内容。 </p>
<!--p>For more information, refer to the <a href="../configuration/business-rules.md">detailed documentation</a>.</p-->
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
<li>使用 Da Vinci 进行创作，使用 AJO 进行优化和投放，加快 Journey Optimizer 客户的从业人员工作流程</li>
<li>使用 Adobe 数据优化 Da Vinci 模型。</li></ul></p>
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
<p>自 2024 年 10 月 16 日起发布</p>
<p>Journey Optimizer 报告功能现已正式发布 (GA)，改善了与客户历程分析的互操作性，可在两个平台之间实现报告标准化，并提高了数据一致性和可靠性。Journey Optimizer 与 Customer Journey Analytics 之间的这种无缝集成能够帮助更清晰地了解绩效指标，使用户能够做出更加明智的决策。</p>
<p>在正式发布后，引入了四个新功能：创建简单量度、创建和发布受众、使用洞察生成器提出临时问题以及将报告通过电子邮件自动发送给关键收件人。</p>
<p>有关更多信息，请参阅<a href="../reports/report-cja-manage.md">详细文档</a>。</p>
<img src="assets/do-not-localize/ajo-cja.gif">
<p>重要：当前的报告体验将从 2025 年 1 月起停用。在此日期之后，新的报告体验将成为标准。我们建议您熟悉新特性和功能，以确保顺利过渡。<a href="../reports/report-gs-cja.md">了解如何开始使用 Journey Optimizer 的新报告界面</a></p>
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
<p>自 2024 年 10 月 1 日起发布</p>
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
<p>自 2024 年 10 月 1 日起发布</p>
<p>借助 Web 渠道，Adobe Journey Optimizer 允许您通过入站 Web 历程为客户提供个性化 Web 体验。现在，可在历程画布中使用 Web 渠道。</p>
<p>有关更多信息，请参阅<a href="../web/create-web.md">详细文档</a>。</p>
<img src="../assets/do-not-localize/web-journey.gif"/>
</tr>
</tbody>
</table>

### 改进 {#e-improvements}

此版本包含下方列出的改进。

**短信渠道**

>[!AVAILABILITY]
>
>以下增强功能仅适用于Sinch和Infobip提供程序。

增强了短信功能来改进消息传送功能：

* 您可以为短信营销活动和历程定义和管理唯一的关键字，从而实现更加个性化和高效的通信。

* 当关键字无法识别时，您可以创建和投放默认短信消息。

* 您现在可以编辑或删除短信 API 渠道配置。

<!--**Journeys**-->

<!--* **Path experiment in journeys** - With the journey path experiment, you can now define and track key metrics for your journey paths, allowing you to measure the impact of your activities and to provide clearer insights into your performance. -->

<!--* **Max number of Live journeys** - Journey Optimizer now has a guardrail of 500 live journeys on production sandboxes, instead of 100. The number of live journeys is visible in the journey canvas. (DOCAC-10977) -->

**数据集**

* **生存时间护栏** - 从 2024 年 11 月 1 日起，将在新沙盒和新组织中推出用于 Journey Optimizer 系统生成的数据集的生存时间护栏 (TTL)，如下所示：

   * 配置文件存储中的数据为 90 天
   * 数据湖中的数据为 13 个月

  随后，此更改将在第二阶段推广到现有的客户沙盒。

  此外，自 2024 年 11 月 1 日起，流式分段将不再支持在跟踪和反馈数据集中使用发送和打开事件。此更改将适用于当时的所有客户沙盒和组织。[了解详情](../data/datasets-ttl.md)

* **自定义操作中的参数**（发布日期：2024 年 10 月 3 日）- 自定义操作现在支持 NULL 和可选参数。[了解详情](../action/about-custom-action-configuration.md#define-the-message-parameters)

**报告**

* **决策报告**&#x200B;现已可用，可提供关于访客如何与您的体验进行交互的基本见解。

**数据治理和同意策略** - 发布日期：2024 年 10 月 7 日

* 现在，Journey Optimizer 中的所有渠道都会实施&#x200B;**数据治理策略**。对于在 Adobe Experience Platform 中创建了策略的客户，这些策略将作为渠道配置设置的一部分应用于营销操作。使用配置创建内容时，系统会检查所有个性化字段是否存在任何数据治理违规。如果发现违规，将无法发布历程或营销活动。[了解详情](../action/action-privacy.md)

* **自定义同意政策**&#x200B;现在适用于所有 Journey Optimizer 渠道。在发送消息或投放入站体验之前执行时，系统会检查用户是否同意在接收的内容中使用个性化字段。如果未获得同意，则不会显示体验。[了解详情](../action/consent.md)

  >[!NOTE]
  >
  >目前，同意策略仅适用于已购买 Adobe **Healthcare Shield** 或 **Privacy and Security Shield** 附加产品的组织。

**受众** - 发布日期：2024 年 10 月 8 日

* 定位 CSV 文件受众时，您现在可以在个性化编辑器以及历程和营销活动规则构建器中使用来自文件的属性。[了解详情](../audience/about-audiences.md)

* 现在可以将自定义上传（CSV 文件）中的受众和属性与 Healthcare Shield 或 Privacy and Security Shield 一起使用。

**基于代码的渠道**

* 内容模板现已可用。您可以从开发人员构建的内容模板开始，加快基于代码的体验的创作速度。通过使用内容模板，营销人员可以只修改某些值或字段，而不是构建整个 HTML 或 JSON 内容负载。

**决策**

[Adobe Customer Journey Analytics](https://experienceleague.adobe.com/docs/analytics-platform/using/cja-overview/cja-overview.html?lang=zh-Hans) 用户现在可以在决策（以前称为体验决策）中设置 AI 模型时选择用于进行优化的自定义模型。例如，这允许您在自定义“购买”表格上进行优化，而不是使用定义的约束（如点击率）。
