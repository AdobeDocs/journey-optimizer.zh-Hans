---
solution: Journey Optimizer
product: journey optimizer
title: 2025 年版发行说明
description: Journey Optimizer 2025 年发行说明
feature: Release Notes
topic: Content Management
role: User
level: Beginner, Intermediate
source-git-commit: e80554570d62d1ddb52516366be55711387c5d19
workflow-type: tm+mt
source-wordcount: '677'
ht-degree: 89%

---

# 2025 年版发行说明 {#release-notes-2025}

本页列出了于 2025 年发布的 [!DNL Journey Optimizer] 功能和改进。

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
<p>以前，业务规则可用于一组组织(LA)，现在则可用于所有用户(GA)。 历程域业务规则仍仅对有限的一组组织(LA)可用。</p>
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
<th><strong>使用 AI 助手的品牌（Beta 版）</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>您现在可以设置自己的品牌，来定义品牌的视觉效果和语言标识。 </p>
<p>此功能作为 Private Beta 版发布，面向部分客户提供。在未来版本中，将逐步向所有客户提供。</p>
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
<p>您现在可以通过直接从Adobe Journey Optimizer发出实际API调用来验证自定义操作配置。 此新功能可帮助您在历程中使用自定义操作之前或之后对其进行故障排除。 </p>
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

