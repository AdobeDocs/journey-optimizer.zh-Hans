---
solution: Journey Optimizer
product: journey optimizer
title: 发行说明
feature: Release Notes
topic: Content Management
description: Adobe Journey Optimizer 发行说明
exl-id: 06fa956a-b500-416e-9d42-b683c328e837
source-git-commit: ec2cccb651360ec796610781affcedca96d66af4
workflow-type: tm+mt
source-wordcount: '1278'
ht-degree: 66%

---

# 发行说明 {#release-notes}

>[!CONTEXTUALHELP]
>id="ajo_homepage_card1"
>title="新增功能"
>abstract="**Adobe Journey Optimizer** 不断地提供新功能、对现有功能的增强和错误修复。会在每月的最后一周将所有更改整合到发行说明中。"

[!DNL Adobe Journey Optimizer] 不断地提供新功能、对现有功能进行增强和修复错误。会在每月的最后一周将所有更改整合到发行说明中。[!DNL Adobe Journey Optimizer] 原生构建于 [!DNL Adobe Experience Platform] 之上并继承了其所具备的最新创新技术和改进。在 [Adobe Experience Platform 发行说明](https://experienceleague.adobe.com/docs/experience-platform/release-notes/latest.html?lang=zh-Hans){target="_blank"}中进一步了解这些更改。


## 最近更新 {#latest-updates}

### 历程条件的更改 {#ee-change@}

从7月8日开始，在新的客户组织中，历程条件中使用的表达式编辑器将不再支持使用体验事件创建表达式。 因此，[Experience Platform数据源](../datasource/adobe-experience-platform-data-source.md)中的体验事件不能用于创建表达式。 [此处](../building-journeys/exp-event-lookup.md)引用了使用体验事件创建表达式/逻辑的替代方法和最佳实践。

在单一历程中访问历程上下文事件数据的方式没有变化。 在表达式和个性化编辑器中，用户可继续访问通过初始历程事件传入的数据。

在本常见问题解答[&#128279;](../building-journeys/exp-event-lookup.md#faq-ee)中了解更多。


## 2025年6月发行说明 {#25-6-rn}

<!--
**Early release notes below are subject to change without prior notice until the release availability date**. Links, screens and updated documentation are published at the release date.-->

**发布日期**：2025 年 6 月 18 日

<!--See also [Adobe Experience Platform Pre Release Notes](https://experienceleague.adobe.com/zh-hans/docs/experience-platform/release-notes/pre-release-notes){target="_blank"}.-->

### 新功能 {#25-06-features}

此版本包含的新功能详述如下。

<table>
<thead>
<tr>
<th><strong>决策中的Adobe Experience Platform数据集（测试版）</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>以前可用于个性化，但现在可利用Adobe Experience Platform数据集进行决策。 这样，您可以将决策属性的定义扩展到数据集中的其他数据，以便进行定期更改的批量更新，而无需一次手动更新一个属性。 例如，可用性、等待时间等。</p>
<p>此功能目前为公开 Beta 版，可供所有客户使用。如果您希望获得访问权限，请联系您的客户代表。</p>
<p>有关更多信息，请参阅<a href="../experience-decisioning/aep-data-exd.md">详细文档</a>。</p>
<p>发布日期：2025年6月20日</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>RCS 消息</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Journey Optimizer 现在支持富通信服务 (RCS) 消息，可根据提供商和运营商的支持实现以下增强消息功能：</p>
<ul>
<li>支持使用品牌和经验证的发件人：使用带有品牌化元素（徽标、发件人名称等）的经验证的业务轮廓发送消息。</li>
<li>消息投放分析：接收详细的投放报告，包括消息状态更新（例如，已发送、已投放、已读取）。</li>
<li>链接跟踪：在 RCS 消息中嵌入和跟踪 URL，以进行参与度分析。</li>
<li>回退到短信：当用户的设备不支持 RCS 或暂时无法通过 RCS 投放时，自动回退到短信。</li>
<li>基本消息合成：发送基于文本的 RCS 消息，其中包含可选的媒体和富元素，具体取决于提供商的支持情况。</li>
</ul>
<p>有关更多信息，请参阅<a href="../sms/sms-configuration.md">详细文档</a>。</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>基于代码的体验内容中的表单字段</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>您现在可以在 JSON 或 HTML 内容模板中定义特定的可编辑字段。通过这些字段，非技术用户能够在基于代码的体验渠道创作中轻松编辑表单视图内容，而无需处理任何代码。<br />此外，在定义基于代码的体验内容模板时，您现在可以在模板中插入决策策略，从而提高可重复使用性和易用性。</p>
<img src="assets/do-not-localize/form-fields.gif">
<p>有关更多信息，请参阅<a href="../code-based/code-based-form-fields.md">详细文档</a>。</p>
</td>
</tr>
</tbody>
</table>

<!--
<table>
<thead>
<tr>
<th><strong>Custom delegation method for subdomains</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>In addition to the full delegation and the CNAME method, a new subdomain configuration method is now available: the Custom delegation method, which enables you to fully own controlling and maintaining all aspects of DNS that are required for delivering, rendering and tracking messages.</p>
</td>
</tr>
</tbody>
</table>
-->

<table>
<thead>
<tr>
<th><strong>历程中的内容决策活动</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>现在，您可以通过历程画布中的专用内容决策活动在历程中包含个性化优惠，并在历程活动（包括条件和自定义操作）中使用它们。</p>
<img src="assets/do-not-localize/content-decision.gif">
<p>此功能仅面向一部分组织提供（限量发布），将会通过未来的版本在全球范围内推出。</p>
<p>有关更多信息，请参阅<a href="../building-journeys/content-decision.md">详细文档</a>。</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>历程试运行</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>历程试运行是 Adobe Journey Optimizer 中的一种特殊历程发布模式，使历程设计人员能够在不接触真实客户或更新轮廓信息的前提下，使用真实生产数据对历程进行测试。此功能有助于历程设计人员在正式发布前验证历程设计和受众定位，从而增强信心。</p>
<img src="assets/do-not-localize/DryRun.gif">
<p>此功能仅面向一部分组织提供（限量发布），将会通过未来的版本在全球范围内推出。</p>
<p>有关更多信息，请参阅<a href="../building-journeys/journey-dry-run.md">详细文档</a>。</p>

</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>暂停和恢复历程</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>您现在可以暂停和恢复历程。通过此功能，可以在不中断客户体验的情况下临时暂停实时历程，从而为历程设计人员提供了更好的控制力和灵活性。暂停后，不会发送任何通信，并且轮廓将停留在暂停状态，直到历程恢复。</p>
<p>您只能暂停和恢复一个历程，或者对一组历程执行批量暂停和恢复操作。</p>
<p>此外，您可以向暂停的历程应用全局筛选条件，以根据轮廓的属性排除轮廓。</p>
<img src="assets/do-not-localize/PauseResume.gif">
<p>此功能仅面向一部分组织提供（限量发布），将会通过未来的版本在全球范围内推出。</p>
<p>有关更多信息，请参阅<a href="../building-journeys/journey-pause.md">详细文档</a>。</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>扩展试验入选者的范围</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>通过扩展试验入选者的范围，您可以自动或手动将试验的入选范围扩展到全体受众。通过此功能，确定最佳合适人选后，您就可以最大程度地扩大范围并提高效率，而无需持续进行人工监督。</p>
<p>有关更多信息，请参阅<a href="../content-management/content-experiment.md">详细文档</a>。</p>
<p>发布日期：2025 年 6 月 2 日</p></td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>冲突和优先级</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>在 Journey Optimizer 中，管理营销活动和历程的数量和时间至关重要，这样才能避免因过多的交互而让客户不堪重负。Journey Optimizer 现在提供多种冲突管理和优先级工具，这些工具之前仅向部分组织提供 (LA)，现在已正式发布 (GA)。</p>
<p>此功能之前为限量发布，现在可用于所有环境。在此正式发布版中，引入了以下增强功能：</p>
<ul>
<li>扩展支持：除了读取受众历程之外，冲突管理工具现在还支持单一历程和受众资格筛选历程。</li>
<li>改进了故障排除功能：查询服务中现在提供两个新的步骤事件字段，可以让您分析为何在历程或营销活动中拒绝某个轮廓。</li>
<li>增强了报告功能：报告现在可以显示哪个特定规则从历程或营销活动中排除了轮廓，从而提高透明度并提供切实可行的见解。</li></ul>
<img src="assets/do-not-localize/gif-conflict.gif">
<p>有关更多信息，请参阅<a href="../conflict-prioritization/gs-conflict-prioritization.md">详细文档</a>。</p>
<p>发布日期：2025 年 6 月 3 日</p>
</td>
</tr>
</tbody>
</table>

### 改进 {#25-06-improv}

此版本包含的改进如下所述。

* **渠道规则集**

   * **自定义持续时间窗口**&#x200B;上限 — 渠道规则集配置屏幕中现在提供新的&#x200B;**Every**&#x200B;字段，允许您根据指定的持续时间跨多天、几周或几个月应用频率上限规则。

   * **每小时重置上限频率** — 您现在可以每小时为渠道规则集应用上限。 此功能仅面向一部分组织（限量发布）。请联系您的客户关怀以启用它。

   * **每日持续时间** — 以前在有限可用性中提供，现在所有客户都可以使用渠道规则集中的“每日”频率上限。

  有关更多信息，请参阅[详细文档](../conflict-prioritization/channel-capping.md)。

* **基于代码的体验**

   * 现在，可在基于代码的体验内容模板中添加决策策略，在该模板中，可将其用于在可编辑表单字段中利用优惠。 [了解详情](../code-based/code-based-form-fields.md)

   * 从基于代码的体验历程或营销活动版本屏幕中，您现在可以直接添加决策策略，而无需打开个性化编辑器。 [了解详情](../code-based/create-code-based.md#edit-code)

* **电子邮件设计器中支持使用自定义 CSS**

  Journey Optimizer现在允许您直接在Email Designer中将自定义CSS添加到电子邮件内容。 [了解详情](../email/custom-css.md)

* **适用于营销活动的新的选项卡式导航**

  新的导航模式允许更快地访问内容创作，并支持在营销策划间进一步扩展设置。 [了解详情](../campaigns/create-campaign.md)

* **决策**

   * **沙盒复制和决策**（发布日期：2025年6月3日） — 现在可以在沙盒之间复制决策对象，从而简化测试和部署工作流。 [了解详情](../configuration/copy-objects-to-sandbox.md#decisioning)

   * **决策规则的决策项属性支持**（发布日期：2025年6月4日） — 您现在可以利用决策项属性创建决策规则。 [了解详情](../experience-decisioning/rules.md#create)

* **交互式消息执行 API 更新** - 发布日期：2025 年 6 月 6 日

  通过交互式消息执行 API，您现在可以删除即将执行的营销活动计划。[了解详情](https://developer.adobe.com/journey-optimizer-apis/references/messaging/){target="_blank"}
