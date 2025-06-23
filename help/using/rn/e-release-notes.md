---
solution: Journey Optimizer
product: journey optimizer
title: 早期发行说明
description: Journey Optimizer 早期发行说明
feature: Release Notes
hide: true
hidefromtoc: true
exl-id: 6e7d1300-8efd-4fdc-90e3-3ccdc3babd2f
source-git-commit: 20f5dc6eab5695b485f4569ad098922a130d4b56
workflow-type: ht
source-wordcount: '1022'
ht-degree: 100%

---

# 早期发行说明 {#e-release-notes}

[!DNL Adobe Journey Optimizer] 不断地提供新功能、对现有功能进行增强和修复错误。所有更改会在每月末整合到[发行说明](release-notes.md)中。

**以下早期发行说明可能会在正式发行日期之前有所更改，恕不另行通知。**&#x200B;在发行当日，会在[发行说明](release-notes.md)中发布链接、屏幕和更新文档。


## 2025 年 6 月早期发行说明 {#25-6-rn}


**以下早期发行说明可能会在正式发行日期之前有所更改，恕不另行通知。**&#x200B;链接、屏幕和更新文档在发布日期发布。

**发布日期**：2025 年 6 月 18 日


### 新功能 {#25-06-features}

此版本包含的新功能详述如下。




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
<!--p>For more information, refer to the <a href="../sms/sms-configuration.md">detailed documentation</a>.</p-->
</td>
</tr>
</tbody>
</table>

<!--table>
<thead>
<tr>
<th><strong>True Multi-Tenant Unitary Delivery</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>No description provided.</p>
</td>
</tr>
</tbody>
</table-->

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
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>子域的自定义委派方法</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>除了完全委派和 CNAME 方法之外，现在还提供新的子域配置方法：自定义委派方法。它使您能够完全控制和维护 DNS 的各个方面，以进行消息投放、呈现和跟踪。</p>
</td>
</tr>
</tbody>
</table>


<table>
<thead>
<tr>
<th><strong>历程中的内容决策活动</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>您现在可以通过历程画布中专门的内容决策活动在历程中纳入个性化产品建议，并在历程活动（包括条件和自定义操作）中使用它们。</p>
<p>此功能仅面向一部分组织提供（限量发布），将会通过未来的版本在全球范围内推出。</p>
</td>
</tr>
</tbody>
</table>


<!--table>
<thead>
<tr>
<th><strong>Experience Decisioning in email channel</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>No description provided.</p>
</td>
</tr>
</tbody>
</table-->



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
<p>此功能仅面向一部分组织提供（限量发布），将会通过未来的版本在全球范围内推出。</p>
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
<p>此功能仅面向一部分组织提供（限量发布），将会通过未来的版本在全球范围内推出。</p>
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

   * **上限的自定义持续时间窗口** - 渠道规则集配置屏幕中现在提供新的&#x200B;**重复计数**&#x200B;字段，您可以根据指定的持续时间，在几天、几周或几个月的时段内应用频率上限规则。

   * **按小时的持续时间** - 您现在可以针对渠道规则集按小时应用上限。

* **基于代码的体验**

   * 现在，可在基于代码的体验内容模板中添加决策策略。

   * 在基于代码的体验的历程或营销活动编辑屏幕中，您现在可以直接添加决策策略，而无需打开个性化编辑器。

* **电子邮件设计器中支持使用自定义 CSS**

  Journey Optimizer 现在允许您直接在电子邮件设计器中将自定义 CSS 添加到电子邮件内容。

* **适用于营销活动的新的选项卡式导航**

  通过新的导航模式，可以更快地访问内容创作功能，并支持在营销活动之间进一步扩展设置。

* **决策** - 发布日期：2025 年 6 月 3 日

  现在可以在不同沙盒中复制决策对象，从而简化测试和部署工作流程。[了解详情](../configuration/copy-objects-to-sandbox.md#decisioning)

* **支持使用决策项属性来创建决策规则** - 发布日期：2025 年 6 月 4 日

  您现在可以利用决策项属性来创建决策规则。[了解详情](../experience-decisioning/rules.md#create)

* **交互式消息执行 API 更新** - 发布日期：2025 年 6 月 6 日

  通过交互式消息执行 API，您现在可以删除即将执行的营销活动计划。[了解详情](https://developer.adobe.com/journey-optimizer-apis/references/messaging/){target="_blank"}