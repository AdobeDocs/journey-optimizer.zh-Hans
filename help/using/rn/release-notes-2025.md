---
solution: Journey Optimizer
product: journey optimizer
title: 2025 年发行说明
description: Journey Optimizer 2025 年发行说明
feature: Release Notes
topic: Content Management
role: User
level: Beginner, Intermediate
exl-id: aa8c74de-748b-4947-a972-14703f6ab4a7
source-git-commit: 0f3191a3d7c5c78e1d8fac2e587e26522f02f8f5
workflow-type: tm+mt
source-wordcount: '1237'
ht-degree: 100%

---

# 2025 年发行说明 {#release-notes-2025}

本页列出了于 2025 年发布的 [!DNL Journey Optimizer] 功能和改进。

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
<th><strong>灵活的受众评估 (GA)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>以前，灵活的受众评估面向一部分组织提供 (LA)，现在面向所有用户提供 (GA)。通过该功能，您可以按需为选定的受众运行分段作业，确保始终掌握最新的受众数据，然后再将受众作为 Journey Optimizer 历程和营销活动目标。</p>
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

现在，您可以在使用批量分段的历程和营销活动中设置每日频次上限。要保证每日频次上限规则的准确性，请确保在创作营销活动或历程时选择优先级最高的命名空间。在 [Platform 身份标识服务指南](https://experienceleague.adobe.com/zh-hans/docs/experience-platform/identity/features/identity-graph-linking-rules/namespace-priority){target="_blank"}中详细了解命名空间优先级

请注意，规则集中的每日频次上限仅适用于一部分组织（有限发布版）。要获得访问权限，请与 Adobe 代表联系。

有关业务规则的更多信息，请参阅[详细文档](../configuration/rule-sets.md)。

**内容模板**

HTML 类型内容模板现已弃用。请注意，您仍然可以使用之前在 [!DNL Journey Optimizer] 中创建的现有 HTML 内容模板。[了解有关内容模板的更多信息](../content-management/content-templates.md)


<!--**Deliverability**

You can now choose to have your emails relayed to your SMTP servers instead of being sent directly from Journey Optimizer to ISPs. This allows you to route final email deliveries through your own Mail Transfer Agents and IPs, or to perform final validations on the emails before sending them to your recipients. The SMTP relay capacity is available on demand - contact your Adobe representative.-->




## 2025 年 2 月发行说明 {#25-02-rn}

**发布日期**：2025 年 2 月 18-19 日


### 新功能 {#25-02-features}

此版本包含的新功能详述如下。

<table>
<thead>
<tr>
<th><strong>创建和管理业务规则</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>您现在可以使用规则集创建业务规则。规则集是一组规则，可帮助您限制在营销活动和跨渠道历程操作中发送的消息，并控制进入历程的用户档案。<p>
<p><ul><li>创建渠道规则集，以限制跨一个或多个渠道发送的消息数。将它们应用于营销活动或历程操作，以实施规则集中定义的规则。通过渠道规则集，您可以根据通信类型应用上限规则。例如，设置规则集以限制“促销消息”，并为“新闻稿”设置另一个规则。根据发送的通信类型，在营销活动或历程操作中应用相应的规则集。</li>
<li> 创建历程规则集以控制用户档案进入历程的情况。限制用户档案在给定时间段内进入历程的频率或同一用户档案可同时参与的历程数。在历程级别应用这些限制，以确保进行正确的进入管理。</li></ul></p>
<p>业务规则以前面向一部分组织提供 (LA)，现在面向所有用户提供 (GA)。历程域业务规则仍然是仅面向一部分组织 (LA) 提供。</p>
<p>有关更多信息，请参阅<a href="../configuration/rule-sets.md">详细文档</a>。</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>使用 AI 助手生成登陆页</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>您现在可以借助 AI 助手为登陆页面制作具有吸引力的内容，包括全页设计、个性化文本和自定义视觉效果。</p>
<img src="assets/do-not-localize/ai-lp.gif">
<p>有关更多信息，请参阅<a href="../content-management/generative-lp.md">详细文档</a>。</p>
</td>
</tr>
</tbody>
</table>


<table>
<thead>
<tr>
<th><strong>使用 AI 助手的品牌 (Beta)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>您现在可以设置自己的品牌，来定义品牌的视觉效果和语言标识。 </p>
<p>此功能作为 Private Beta 版发布，面向部分客户提供。在未来版本中，其将逐步向所有客户提供。</p>
<p>有关更多信息，请参阅<a href="../content-management/brands.md">详细文档</a>。</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>自定义操作故障排除</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>您现在可以直接从 Adobe Journey Optimizer 进行实际 API 调用，以验证自定义操作配置。此项新增功能可帮助您在历程中使用自定义操作之前或之后对其进行故障排除。 </p>
<p>有关更多信息，请参阅<a href="../action/troubleshoot-custom-action.md">详细文档</a>。</p>
<!--p> This capability is only available for a set of organizations (Limited Availability). To gain access, contact your Adobe representative.</p-->
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>灵活的受众评估（限量发布）</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>通过灵活的受众评估，您可以按需为选定的受众运行分段作业，确保始终掌握最新的受众数据，然后再将受众作为 Journey Optimizer 历程和营销活动目标。</p>
<img src="assets/do-not-localize/flexible-audience.gif">
<p>有关更多信息，请参阅<a href="../audience/creating-a-segment-definition.md#flexible">详细文档</a>。</p>
<p>此功能仅面向一部分组织（限量发布）。要获得访问权限，请与 Adobe 代表联系。</p>
<p>发布日期：2025 年 1 月 28 日</p>
</tr>
</tbody>
</table>
</table>


### 改进 {#25-02-improvements}

2 月的更新提供了以下改进。

* **数据集生存时间 (TTL)** - 从本月起，将在新沙盒和新组织中推出用于 Journey Optimizer 系统生成的数据集的生存时间 (TTL) 护栏，如下所示：

   * 配置文件存储中的数据为 90 天
   * 数据湖中的数据为 13 个月

  此更改将在后续阶段推广到现有的客户沙盒。

  在[专门的常见问题解答](../data/datasets-ttl.md#frequently-asked-questions)中了解有关此更新的更多信息。

<!--* **Playbooks** - You can now create and publish your own Use Case Playbooks in Journey Optimizer.-->

* **直邮** - 直邮渠道配置中的文件路由现在支持新的服务器类型“数据登陆区”。[了解详情](../direct-mail/direct-mail-configuration.md#file-routing-configuration)

* **短信** - 您现在可以通过覆盖投放、反馈、入站和回调 URL 来管理来自多区域端点的短信消息投放。为支持此功能，已在 API 凭据配置中添加了新的字段“覆盖 URL”。此更改仅适用于 Sinch 提供程序。[了解详情](../sms/sms-configuration-sinch.md)

* **个性化**（发布日期：2025 年 1 月 29 日）- 可在个性化编辑器中使用新的日期/时间帮助程序功能。[了解详情](../personalization/functions/dates.md)


<!--
* The personalization editor has been enhanced with new capabilities such as Auto-complete, Search, and filtering options. You can also show or hide deprecated attributes.-->


* **电子邮件配置** - 如果您在 Adobe 之外管理同意，在进行电子邮件渠道配置设置时，现在可以设置自定义取消订阅电子邮件地址和自定义一键式取消订阅 URL。[了解详情](../email/list-unsubscribe.md#custom-managed)

  ![](../email/assets/surface-list-unsubscribe-custom.png){width="80%"}

* **Decisioning**（发布日期：2025 年 1 月 28 日）- 在编辑项目目录的架构时，Decisioning 现在支持“对象”数据类型。[了解详情](../experience-decisioning/catalogs.md)
