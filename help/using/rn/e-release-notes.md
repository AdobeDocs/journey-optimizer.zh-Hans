---
solution: Journey Optimizer
product: journey optimizer
title: 早期发行说明
description: Journey Optimizer 早期发行说明
feature: Release Notes
hide: true
hidefromtoc: true
exl-id: 6e7d1300-8efd-4fdc-90e3-3ccdc3babd2f
source-git-commit: eff3f2fb4d1c369e77a22013ae1576b57449a8b7
workflow-type: tm+mt
source-wordcount: '1000'
ht-degree: 35%

---

# 早期发行说明 {#e-release-notes}

[!DNL Adobe Journey Optimizer] 不断地提供新功能、对现有功能进行增强和修复错误。所有更改会在每月末整合到[发行说明](release-notes.md)中。

**以下早期发行说明可能会在正式发行日期之前有所更改，恕不另行通知。**&#x200B;在发行当日，会在[发行说明](release-notes.md)中发布链接、屏幕和更新文档。


## 2025年6月早期发行说明 {#25-6-rn}


**以下早期发行说明可能会在正式发行日期之前有所更改，恕不另行通知。**&#x200B;链接、屏幕和更新文档在发布日期发布。

**发行日期**： 2025年6月18日


### 新功能 {#25-06-features}

此版本包含的新功能详述如下。




<table>
<thead>
<tr>
<th><strong>RCS消息传送</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Journey Optimizer现在支持RCS（富通信服务）消息传送，可根据提供商和运营商支持实现以下增强消息传送功能：</p>
<ul>
<li>品牌和经验证的发件人支持：使用带有品牌元素（徽标、发件人姓名等）的经验证的业务配置文件发送消息。</li>
<li>消息投放分析：接收详细的投放报告，包括消息状态更新（例如，已发送、已投放、已读取）。</li>
<li>链接跟踪：在RCS消息中嵌入和跟踪URL，以进行参与分析。</li>
<li>回退到短信：当配置文件设备不支持RCS或暂时无法通过RCS访问时，自动回退到短信。</li>
<li>基本消息合成：发送基于文本的RCS消息，其中带有可选的媒体和富元素，具体取决于提供商的支持。</li>
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
<p>您现在可以在JSON或HTML内容模板中定义特定的可编辑字段，这些字段使非技术用户能够轻松编辑基于代码的体验中的内容，而无需处理代码。</p>
<p>此功能之前为限量发布，现在可用于所有环境（正式发布）。</p>
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
<p>除了完全委派和CNAME方法之外，现在还提供新的子域配置方法：自定义委派方法，它使您能够完全拥有控制和维护投放、渲染和跟踪消息所需的DNS的所有方面。</p>
<p>此功能之前为限量发布，现在可用于所有环境（正式发布）。</p>
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
<p>您现在可以通过历程画布中的专用内容决策活动在历程中包含个性化优惠，并在历程活动（包括条件和自定义操作）中使用它们。</p>
<p>此功能仅适用于一组组织（限量发布），并将在未来版本中在全球范围内推出。</p>
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
<p>历程练习是Adobe Journey Optimizer中的一种特殊旅程发布模式，允许旅程从业人员使用真实生产数据测试旅程，而无需联系真实客户或更新用户档案信息。 此功能有助于历程从业者在将其发布到实时状态之前获得对其历程设计和受众定位的信心。</p>
<p>此功能仅适用于一组组织（限量发布），并将在未来版本中在全球范围内推出。</p>
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
<p>您现在可以暂停并继续您的历程。 此功能允许在不中断客户体验的情况下临时暂停实时历程，从而为历程参与者提供了更好的控制和灵活性。 暂停后，不会发送任何通信，并且用户档案将保持暂停状态，直到历程恢复。</p>
<p>您只能暂停和恢复一个历程，或者对一组历程执行批量暂停和恢复操作。</p>
<p>此外，您可以将全局过滤器应用于暂停的历程，以根据用户档案的属性排除用户档案。</p>
<p>此功能仅适用于一组组织（限量发布），并将在未来版本中在全球范围内推出。</p>
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
<p>通过缩放试验入选者，可自动或手动将试验的入选变体转出给全体受众。 通过此功能，确定最佳合适人选后，您就可以最大程度地扩大范围并提高效率，而无需持续进行人工监督。</p>
<p>有关更多信息，请参阅<a href="../content-management/content-experiment.md">详细文档</a>。</p>
<p>发布日期：2025年6月2日</p></td>
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
<p>发布日期：2025年6月3日</p>
</td>
</tr>
</tbody>
</table>


### 改进 {#25-06-improv}

此版本包含的改进如下所述。

* **渠道规则集**

   * **自定义持续时间窗口**&#x200B;上限 — 渠道规则集配置屏幕中现在提供了新的&#x200B;**重复计数**&#x200B;字段，允许您根据指定的持续时间跨几天、几周或几个月应用频率上限规则。

   * **每小时持续时间** — 您现在可以每小时为渠道规则集应用上限。

* **基于代码的体验**

  现在，基于代码的体验内容模板和代码编辑器右边栏中提供了决策策略。

* **电子邮件设计工具**

   * **自定义CSS支持** — 现在，通过Journey Optimizer，您可以在电子邮件设计器中直接将自定义CSS添加到电子邮件内容。
   * **深色模式支持** - Journey Optimizer Email designer现在提供切换到深色模式的功能，您可以在其中定义特定设置。


* **决策** — 发布日期：2025年6月3日

  现在可以在不同沙盒中复制决策对象，从而简化测试和部署工作流程。[了解详情](../configuration/copy-objects-to-sandbox.md#decisioning)

* **决策规则的决策项属性支持** — 发布日期： 2025年6月4日

  您现在可以利用决策项目属性来创建决策规则。 [了解详情](../experience-decisioning/rules.md#create)

* **交互式消息执行API更新** — 可用日期： 2025年6月6日

  交互式消息执行API现在允许您删除即将执行的营销活动计划。 [了解详情](https://developer.adobe.com/journey-optimizer-apis/references/messaging/){target="_blank"}