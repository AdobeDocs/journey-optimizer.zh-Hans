---
solution: Journey Optimizer
product: journey optimizer
title: 发行说明
feature: Release Notes
topic: Content Management
description: Adobe Journey Optimizer 发行说明
exl-id: 06fa956a-b500-416e-9d42-b683c328e837
source-git-commit: e80554570d62d1ddb52516366be55711387c5d19
workflow-type: tm+mt
source-wordcount: '682'
ht-degree: 40%

---

# 发行说明 {#release-notes}

>[!CONTEXTUALHELP]
>id="ajo_homepage_card1"
>title="新增功能？"
>abstract="**Adobe Journey Optimizer** 不断地提供新功能、对现有功能的增强和错误修复。会在每月的最后一周将所有更改整合到发行说明中。"

[!DNL Adobe Journey Optimizer] 不断地提供新功能、对现有功能进行增强和修复错误。会在每月的最后一周将所有更改整合到发行说明中。[!DNL Adobe Journey Optimizer] 原生构建于 [!DNL Adobe Experience Platform] 之上并继承了其所具备的最新创新技术和改进。在 [Adobe Experience Platform 发行说明](https://experienceleague.adobe.com/docs/experience-platform/release-notes/latest.html?lang=zh-Hans){target="_blank"}中，进一步了解这些更改。


## 2025年3月发行说明 {#25-3-rn}


### 新功能 {#25-03-features}

此版本包含的新功能详述如下。

<table>
<thead>
<tr>
<th><strong>与Adobe Express集成（限量发布）</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Adobe Journey Optimizer中的Adobe Express集成允许您在内容创建期间直接使用Adobe Express的编辑工具，使您能够调整大小、删除背景、裁剪以及将资源转换为JPEG或PNG。<p>
<p>Adobe Journey Optimizer中的Adobe Express集成当前仅适用于一批组织（限量发布）。 它不能部署为用于Healthcare Shield或Privacy and Security Shield。</p>
<p>有关更多信息，请参阅<a href="../integrations/express.md">详细文档</a>。</p>
</br>
<img src="assets/do-not-localize/express_resize.gif"/>
</td>
</tr>
</tbody>
</table>


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
<img src="assets/do-not-localize/success-metric.gif"/>
</td>
</tr>
</tbody>
</table>

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
<th><strong>与Dynamic Media集成（限量发布）</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Dynamic Media资源现在可直接在Journey Optimizer中访问和使用。 通过此集成，您可以：
<ul>
<li>通过实时更新集中管理资源</li>
<li>立即修改资源设置，如宽度和高度</li>
<li>通过更新内容和添加个性化字段自定义Dynamic Media模板</li>
</ul>
<p>
<p>此集成仅适用于一组组织（限量发布）。 要获得访问权限，请与 Adobe 代表联系。</p>
<p>有关更多信息，请参阅<a href="../integrations/aem-dynamic.md">详细文档</a>。</p>
</td>
</tr>
</tbody>
</table>



<table>
<thead>
<tr>
<th><strong>与Adobe GenStudio集成（限量发布）</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>为了提高营销效率并维护品牌一致性，您现在可以将GenStudio for Performance Marketing体验与Journey Optimizer无缝集成。 这使您能够利用GenStudio的AI功能内容创建以及Journey Optimizer的高级编排功能。<p>
<p>目前，Journey Optimizer中的GenStudio集成不可用于Healthcare Shield或Privacy and Security Shield （限量发布）。</p>
<p>有关更多信息，请参阅<a href="../integrations/genstudio.md">详细文档</a>。</p>
<img src="assets/do-not-localize/genstudio.gif"/>
</td>
</tr>
</tbody>
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

**Personalization编辑器**（可用日期： 3月12日）

Journey Optimizer 个性化编辑器已更新，新增了以下功能：
* **更新的代码编辑器设计** – 更简洁的现代界面，改善了可用性和重点内容的显示。
* **搜索和替换** – 添加了在编辑器中快速查找和替换内容的功能。
* **支持撤销和重做** – 允许您轻松还原或重新应用更改。
* **可自定义字体大小** – 允许调整编辑器的字体大小，以提高可读性。
* **内联 JSON 验证** – 为 JSON 内容提供实时客户端验证以加快错误检测。
* **自动填写用户档案和上下文属性** – 提供智能建议以简化内容创建。
* **增强的语法突出显示** – 使代码结构在视觉上更加明显，从而提高可读性。

![视频显示Personalization编辑器中的新功能](assets/do-not-localize/personalization-editor.gif)

有关更多信息，请参阅[详细文档](../personalization/personalization-build-expressions.md)。

**审批**

现在，在定义审批策略的条件时，您可以选择按标记和/或对象类别进行过滤。

有关更多信息，请参阅[详细文档](../test-approve/approval-policies.md)。

**配置**

* 您现在可以将Adobe Experience Platform统一标记分配给渠道配置。 这使您能够轻松地对它们进行分类，并改进所有列表中的搜索和导航。 [了解详情](../configuration/channel-surfaces.md#channel-config-tags)

* 在Journey Optimizer中设置或编辑电子邮件子域时，如果您在父域中拥有相关记录，那么您现在可以选择自己管理相关的DMARC记录。 [了解详情](../configuration/dmarc-record.md#set-up-dmarc)

**业务规则**

现在，您可以在历程和营销活动中通过批量分段使用每日频率上限。 要确保每日频率上限规则的准确性，请确保在创作活动或历程时选择最高优先级的命名空间。 在[Platform Identity Service指南](https://experienceleague.adobe.com/en/docs/experience-platform/identity/features/identity-graph-linking-rules/namespace-priority){target="_blank"}中了解有关命名空间优先级的更多信息

请注意，规则集中的每日频率上限仅适用于一组组织（限量发布）。 要获得访问权限，请与 Adobe 代表联系。

有关业务规则的更多信息，请参阅[详细文档](../configuration/rule-sets.md)。

<!--**Content management**

To easily manage your fragments and your content templates, you can now use folders to organize them more effectively into a structured hierarchy. This improvement is only available for a set of organizations (Limited Availability). <!--To gain access, contact your Adobe representative.

**Deliverability**

You can now choose to have your emails relayed to your SMTP servers instead of being sent directly from Journey Optimizer to ISPs. This allows you to route final email deliveries through your own Mail Transfer Agents and IPs, or to perform final validations on the emails before sending them to your recipients. The SMTP relay capacity is available on demand - contact your Adobe representative.-->


