---
solution: Journey Optimizer
product: journey optimizer
title: 发行说明
feature: Release Notes
topic: Content Management
description: Adobe Journey Optimizer 发行说明
exl-id: 06fa956a-b500-416e-9d42-b683c328e837
source-git-commit: d28341dd39ec3ab838a5fbb3ae49539b8776c60b
workflow-type: tm+mt
source-wordcount: '867'
ht-degree: 69%

---

# 发行说明 {#release-notes}

>[!CONTEXTUALHELP]
>id="ajo_homepage_card1"
>title="新增功能？"
>abstract="**Adobe Journey Optimizer** 不断地提供新功能、对现有功能的增强和错误修复。会在每月的最后一周将所有更改整合到发行说明中。"

[!DNL Adobe Journey Optimizer] 不断地提供新功能、对现有功能进行增强和修复错误。会在每月的最后一周将所有更改整合到发行说明中。[!DNL Adobe Journey Optimizer] 原生构建于 [!DNL Adobe Experience Platform] 之上并继承了其所具备的最新创新技术和改进。在 [Adobe Experience Platform 发行说明](https://experienceleague.adobe.com/docs/experience-platform/release-notes/latest.html?lang=zh-Hans){target="_blank"}中，进一步了解这些更改。

## 2025 年 4 月更新

### 新功能 {#25-04-feature}

<table>
<thead>
<tr>
<th><strong>历程指标</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>历程指标现已可用，可让您在业务的各个关键指标上衡量活动的影响，并更清楚地了解您的绩效。</p>
<p>有关更多信息，请参阅<a href="../building-journeys/success-metrics.md">详细文档</a>。</p>
<p>发布日期： 2025年4月9日</p>
</br>
<img src="assets/do-not-localize/success-metric.gif"/>
</td>
</tr>
</tbody>
</table>

### 改进 {#25-04-improv}

* **沙盒工具** — 可用日期： 2025年4月3日

  您现在可以使用资源包导出和导入功能跨多个沙盒复制营销活动。 活动会与所有与用户档案、受众、模式、内联消息和依赖对象相关的项目一起复制。 某些项目不会被复制，例如决策项目、数据使用标签和语言设置。 [了解详情](../configuration/copy-objects-to-sandbox.md)

* **Personalization** — 发布日期：2025年4月2日

  默认情况下，个性化编辑器中的属性窗格现在仅显示填充的属性。 要查看所有属性，请使用“设置”按钮关闭&#x200B;**[!UICONTROL 仅显示填充的属性]**&#x200B;选项。 [了解详情](../personalization/personalization-build-expressions.md)

* **内容管理** — 发布日期：2025年4月2日

  为了轻松地管理内容模板和片段，您现在可以使用文件夹将它们更有效地组织到结构化层次结构中。 要了解更多信息，请参阅[内容模板](../content-management/access-content-templates.md#folders)和[片段](../content-management/manage-fragments.md#folders)部分。

  >[!AVAILABILITY]
  >
  >此改进仅面向一部分组织（有限发布版）。

* **向Designer发送电子邮件** — 发布日期：2025年4月1日

  为了增强Journey Optimizer中的辅助功能，Email Designer中现在提供了两个新字段：它们对应于电子邮件内容`<html>`元素中的`<title>`元素和`lang`属性。 除了电子邮件&#x200B;**[!UICONTROL 正文]**&#x200B;部分中的&#x200B;**[!UICONTROL Preheader]**&#x200B;字段外，您还可以定义这些设置。 [了解详情](../email/email-metadata.md)


## 2025 年 3 月发行说明 {#25-3-rn}


### 新功能 {#25-03-features}

此版本包含的新功能详述如下。

<!--table>
<thead>
<tr>
<th><strong>Integration with Adobe Express (Limited Availability)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>The Adobe Express integration in Adobe Journey Optimizer lets you use Adobe Express's editing tools directly during content creation, enabling you to resize, remove backgrounds, crop, and convert assets to JPEG or PNG.<p>
<p>Adobe Express integration in Adobe Journey Optimizer is currently only available for a set of organizations (Limited Availability). It cannot be deployed for use with Healthcare Shield or Privacy and Security Shield.</p>
<p>For more information, refer to the <a href="../integrations/express.md">detailed documentation</a>.</p>
</br>
<img src="assets/do-not-localize/express_resize.gif"/>
</td>
</tr>
</tbody>
</table-->


<!--table>
<thead>
<tr>
<th><strong>Journey metrics</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Journey metrics are now available, allowing you to measure the impact of your activities across the key metrics of your business and to provide clearer insights into your performance.</p>
<p>For more information, refer to the <a href="../building-journeys/success-metrics.md">detailed documentation</a>.</p>
<img src="assets/do-not-localize/success-metric.gif"/>
</td>
</tr>
</tbody>
</table-->

<!-- table>
<thead>
<tr>
<th><strong>Calendar view for journeys (Limited Availability)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>A calendar view is now available in Journey Optimizer to visualize all journeys activations. From this view, you can browse your journeys and check details and properties.<p>
<p>This change is only available for a set of organizations (Limited Availability). To gain access, contact your Adobe representative.</p>
<p>For more information, refer to the <a href="../configuration/rule-sets.md">detailed documentation</a>.</p>
</td>
</tr>
</tbody>
</table-->

<table>
<thead>
<tr>
<th><strong>与 Dynamic Media 集成（有限发布版）</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Dynamic Media 资源现可直接在 Journey Optimizer 中使用和访问。通过此集成，您可以：
<ul>
<li>通过实时更新集中管理资源</li>
<li>即时修改宽度和高度等资源设置</li>
<li>通过更新内容和添加个性化字段自定义 Dynamic Media 模板</li>
</ul>
<p>
<p>此集成仅面向一部分组织（有限发布版）。要获得访问权限，请与 Adobe 代表联系。</p>
<p>有关更多信息，请参阅<a href="../integrations/aem-dynamic.md">详细文档</a>。</p>
</td>
</tr>
</tbody>
</table>



<table>
<thead>
<tr>
<th><strong>与 Adobe GenStudio 集成（有限发布版）</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>为了提高营销效率并保持品牌一致性，您现在可以将 GenStudio for Performance Marketing 体验与 Journey Optimizer 无缝集成。这使您能够利用 GenStudio 的 AI 驱动的内容创建以及 Journey Optimizer 的高级编排功能。<p>
<p>目前，Journey Optimizer 中的 GenStudio 集成不可用于 Healthcare Shield 或 Privacy and Security Shield（有限发布版）。</p>
<p>有关更多信息，请参阅<a href="../integrations/genstudio.md">详细文档</a>。</p>
<img src="assets/do-not-localize/genstudio.gif"/>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>灵活的受众评估(GA)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>以前，灵活的受众评估可用于一组组织(LA)，现在所有用户均可使用(GA)。 利用此功能，可按需为选定受众运行分段作业，从而确保在将受众定位到Journey Optimizer历程和营销活动之前，您始终拥有最新的受众数据。</p>
<img src="assets/do-not-localize/flexible-audience.gif">
<p>有关更多信息，请参阅<a href="../audience/creating-a-segment-definition.md#flexible">详细文档</a>。</p>
</tr>
</tbody>
</table>
</table>

<!--table>
<thead>
<tr>
<th><strong>LINE channel (Limited Availability)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Adobe Journey Optimizer has expanded its cross-channel capabilities to include support for the LINE channel. This enhancement allows you to create, edit, and preview LINE experiences enabling more personalized and engaging interactions. With LINE, you can connect with more customers, send relevant content, and improve your engagement.<p>
<p>This capability is only available for a set of organizations (Limited Availability). To gain access, contact your Adobe representative.</p>
<p>For more information, refer to the <a href="../configuration/rule-sets.md">detailed documentation</a>.</p>
</td>
</tr>
</tbody>
</table-->


### 改进 {#25-03-improv}

**个性化编辑器**（发布日期：3 月 12 日）

Journey Optimizer 个性化编辑器已更新，新增了以下功能：
* **更新的代码编辑器设计** – 更简洁的现代界面，改善了可用性和重点内容的显示。
* **搜索和替换** – 添加了在编辑器中快速查找和替换内容的功能。
* **支持撤销和重做** – 允许您轻松还原或重新应用更改。
* **可自定义字体大小** – 允许调整编辑器的字体大小，以提高可读性。
* **内联 JSON 验证** – 为 JSON 内容提供实时客户端验证以加快错误检测。
* **自动填写用户档案和上下文属性** – 提供智能建议以简化内容创建。
* **增强的语法突出显示** – 使代码结构在视觉上更加明显，从而提高可读性。

![展示个性化编辑器中的新增功能的视频](assets/do-not-localize/personalization-editor.gif)

有关更多信息，请参阅[详细文档](../personalization/personalization-build-expressions.md)。

**审批**

现在，在定义审批策略的条件时，您可以选择按标记和/或对象类别进行筛选。

有关更多信息，请参阅[详细文档](../test-approve/approval-policies.md)。

**配置**

* 您现在可以为渠道配置分配 Adobe Experience Platform 统一标记。这让您能够轻松对其进行分类，并改进所有列表中的搜索和导航。[了解详情](../configuration/channel-surfaces.md#channel-config-tags)

* 在 Journey Optimizer 中设置或编辑电子邮件子域时，如果在父域中拥有相关记录，那么您现在可以选择自己管理相关的 DMARC 记录。[了解详情](../configuration/dmarc-record.md#set-up-dmarc)

**业务规则**

现在，您可以在使用批量分段的历程和营销活动中设置每日频次上限。要保证每日频次上限规则的准确性，请确保在创作营销活动或历程时选择优先级最高的命名空间。在[Platform Identity Service指南](https://experienceleague.adobe.com/zh-hans/docs/experience-platform/identity/features/identity-graph-linking-rules/namespace-priority){target="_blank"}中了解有关命名空间优先级的更多信息

请注意，规则集中的每日频次上限仅适用于一部分组织（有限发布版）。要获得访问权限，请与 Adobe 代表联系。

有关业务规则的更多信息，请参阅[详细文档](../configuration/rule-sets.md)。

<!--**Deliverability**

You can now choose to have your emails relayed to your SMTP servers instead of being sent directly from Journey Optimizer to ISPs. This allows you to route final email deliveries through your own Mail Transfer Agents and IPs, or to perform final validations on the emails before sending them to your recipients. The SMTP relay capacity is available on demand - contact your Adobe representative.-->


