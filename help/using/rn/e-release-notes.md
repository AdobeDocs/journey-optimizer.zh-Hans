---
solution: Journey Optimizer
product: journey optimizer
title: Journey Optimizer 的预发行说明
description: Adobe Journey Optimizer 预发行说明
feature: Release Notes
hide: true
hidefromtoc: true
exl-id: 6e7d1300-8efd-4fdc-90e3-3ccdc3babd2f
source-git-commit: d09fc3ed670a50b6a99bcf660353ee37d31c7501
workflow-type: tm+mt
source-wordcount: '1089'
ht-degree: 100%

---

# 预发行说明 {#e-release-notes}

[!DNL Adobe Journey Optimizer] 不断地提供新功能、对现有功能进行增强和修复错误。所有更改会在每月末整合到[发行说明](release-notes.md)中。


## 2025 年 10 月预发行说明 {#oct-25-10-rn}

**以下预发行说明可能会在正式发行日期之前有所更改，恕不另行通知**。链接、屏幕和更新的文档会于发布日期在发行说明中发布。

另请参阅 [Adobe Experience Platform 预发行说明](https://experienceleague.adobe.com/zh-hans/docs/experience-platform/release-notes/pre-release-notes){target="_blank"}。

**发布日期**：2025 年 10 月 22 日

### 新功能 {#oct-25-10-features}



<table>
<thead>
<tr>
<th><strong>免打扰时间 / 基于时间进行排除</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>利用免打扰时间，您可以针对电子邮件、短信、推送和 WhatsApp 渠道定义基于时间的排除项。这可确保在特定时间段内不发送任何消息，从而帮助您尊重客户偏好并满足合规性要求。</p>
<p>您可以通过规则集应用免打扰时间并分配给营销活动或历程中的单个操作，以实现精确控制。通过简化这些流程。</p>
<p>此功能仅面向一部分组织（限量发布）。要获得访问权限，请与 Adobe 代表联系。</p>
<!--img src="assets/do-not-localize/FILE.gif"-->
<!-- p>For more information, refer to the <a href="../FILE.md">detailed documentation</a>.</p -->
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>自定义操作监控和报告</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>通过此功能，可以更好地了解历程运行状况和执行情况，包括生命周期状态和性能警报。您现在可以快速了解自定义操作中何时何处发生异常以及发生异常的原因。</p>
<!--img src="assets/do-not-localize/FILE.gif"-->
<!-- p>For more information, refer to the <a href="../FILE.md">detailed documentation</a>.</p -->
</td>
</tr>
</tbody>
</table>

<!--table>
<thead>
<tr>
<th><strong>RCS Basic Messaging</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>With the new RCS Basic add-on offering, you can now deliver basic Rich Communication Services (RCS) messaging in Journey Optimizer, enabling the following enhanced messaging capabilities subject to provider and geographical support:</p>
<ul>
<li><strong>Branded and verified sender support:</strong> Send messages using verified business profiles with branding elements (logo, sender name, etc.).</li>
<li><strong>Message delivery insights:</strong> Receive detailed delivery reports including message status updates (e.g., sent, delivered, read).</li>
<li><strong>Link tracking:</strong> Embed and track URLs within RCS messages for engagement analytics.</li>
<li><strong>Fallback to SMS:</strong> Automatic fallback to SMS when the recipient's device does not support RCS or is temporarily unreachable via RCS.</li>
<li><strong>Basic message composition:</strong> Send basic text-based RCS messages.</li>
</ul>
<!--img src="assets/do-not-localize/FILE.gif"-->
<!-- p>For more information, refer to the <a href="../FILE.md">detailed documentation</a>.</p -->
<!--/td>
</tr>
</tbody>
</table-->

<!--table>
<thead>
<tr>
<th><strong>Direct mail channel in Orchestrated campaigns</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Direct mail channel is now available in orchestrated campaigns. The Direct mail activity facilitates direct mail sending within your Orchestrated campaign, for both one-time and recurring messages. It serves to automate the process of generating the extraction file required by direct mail providers. You can combine channel activities into the Orchestrated campaign canvas to create cross-channel campaigns that can trigger actions based on customer behavior and data.</p>
<!--img src="assets/do-not-localize/FILE.gif"-->
<!-- p>For more information, refer to the <a href="../FILE.md">detailed documentation</a>.</p -->
<!--/td>
</tr>
</tbody>
</table-->

<!--table>
<thead>
<tr>
<th><strong>Direct Mail channel in journeys</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Previously limited to Campaigns, Direct Mail channel is now available on the journey canvas, enabling you to incorporate Direct Mail into your journeys. Direct Mail can now be used in both batch and 1:1 journey scenarios, with support for file extraction configuration and time-based frequency settings.</p>
<p> Previously released in Limited Availability, this capability is now available to all environments (General Availability).</p>
<!--img src="assets/do-not-localize/FILE.gif"-->
<!-- p>For more information, refer to the <a href="../FILE.md">detailed documentation</a>.</p -->
<!--/td>
</tr>
</tbody>
</table-->

<table>
<thead>
<tr>
<th><strong>用于检索操作营销活动的新 API</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>现已提供新的 Journey Optimizer API，可让您以编程方式检索和检查与活动相关的数据，如详细信息、版本和配置。</p>
<!--img src="assets/do-not-localize/FILE.gif"-->
<!-- p>For more information, refer to the <a href="../FILE.md">detailed documentation</a>.</p -->
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>新的忠诚度应用程序源连接器</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Adobe Experience Platform 现在为 Talon.One、Capillary 和 Kobie 忠诚度应用程序提供新的源连接器。这些连接器让您可以无缝地将忠诚度数据流式传输到 Adobe Experience Platform 中，并在 Journey Optimizer 中利用这些数据。</p>
<!--img src="assets/do-not-localize/FILE.gif"-->
<!-- p>For more information, refer to the <a href="../FILE.md">detailed documentation</a>.</p -->
</td>
</tr>
</tbody>
</table>

<!--table>
<thead>
<tr>
<th><strong>Decisioning support in email channel</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>You can now add Decision policies into email journeys and campaigns. Decision policies are containers for your offers that leverage the Decisioning engine to dynamically return the best content to deliver for each audience member.</p>
<p>Previously released in Limited Availability, this capability is now available to all environments (General Availability).</p>
<img src="assets/do-not-localize/FILE.gif">
<p>For more information, refer to the <a href="../FILE.md">detailed documentation</a></p>
</td>
</tr>
</tbody>
</table-->

<table>
<thead>
<tr>
<th><strong>适用于 API 触发电子邮件营销活动的高吞吐量模式</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>API 触发的营销活动现在提供新的高吞吐量模式。此模式专为大规模实时消息传送而设计（每秒最多 5000 个事务），能够在提高可用性的同时降低延迟。</p>
<p>此功能仅适用于电子邮件渠道，以及已购买 Adobe 高吞吐量事务性消息附加组件的组织。请联系 Adobe 客户代表以获取更多详情。</p>
<!--img src="assets/do-not-localize/FILE.gif"-->
<!-- p>For more information, refer to the <a href="../FILE.md">detailed documentation</a>.</p -->
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>可重复使用的目标选择规则</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Journey Optimizer 现在可以让您从专用 UI 菜单创建规则并在构建目标选择时利用这些规则，无论是在营销活动的内容优化还是在优化历程活动中。</p>
<p>目标选择规则当前处于有限发布状态。请联系 Adobe 代表以获取访问权限。</p>
<p>请注意，此功能仅适用于已购买决策附加组件的组织。将逐步向所有客户推广此功能。</p>
<!--img src="assets/do-not-localize/FILE.gif"-->
<!-- p>For more information, refer to the <a href="../FILE.md">detailed documentation</a>.</p -->
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>电子邮件设计器中的主题</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>您现在可以快速应用预批准的主题，以确保在所有电子邮件中实现品牌一致性、加快营销活动创建流程，并独立生成高质量电子邮件，同时减少对设计团队的依赖。</p>
<p>此功能之前以 Beta 发布，现在可供一部分组织使用（有限发布）。要获得访问权限，请与 Adobe 代表联系。</p>
<img src="assets/do-not-localize/themes.gif">
<p>有关更多信息，请参阅<a href="../email/apply-email-themes.md">详细文档</a></p>
<!--p>Availability date: October 22, 2025</p-->
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>新历程警报</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>可使用新的预配置警报监测历程执行：</p>
<ul><li><a href="../reports/alerts.md#alert-discard-rate">轮廓丢弃率超限</a>：过去 5 分钟内，丢弃的轮廓与进入历程的轮廓的比率超过阈值。</li>
<li><a href="../reports/alerts.md#alert-custom-action-error-rate">自定义操作错误率超限</a>：过去 5 分钟内，自定义操作错误与成功 HTTP 调用的比率超过阈值。</li>
<li><a href="../reports/alerts.md#alert-profile-error-rate">轮廓错误率超限</a>：过去 5 分钟内，出错轮廓与进入历程的轮廓的比率超过阈值。</li></ul> <p>您可以修改阈值并订阅单个历程级别警报和全局警报。</p>
<p>有关更多信息，请参阅<a href="../reports/alerts.md">详细文档</a></p>
<p>发布日期：2025 年 10 月 14 日</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>执行元数据帮助程序</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>在个性化编辑器中提供了新的“executionMetadata”辅助函数。利用该功能，可将上下文信息附加到任何本机操作，并将其捕获到数据集中以导出到外部系统。</p>
<p>此功能为限量发布版。请联系 Adobe 代表以获取访问权限。</p>
<p>有关更多信息，请参阅<a href="../personalization/functions/helpers.md#execution-metadata">详细文档</a></p>
<p>发布日期：2025 年 10 月 13 日</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Experimentation 代理上线！</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Experimentation 代理由 <a href="https://experienceleague.adobe.com/zh-hans/docs/experience-cloud-ai/experience-cloud-ai/agents/agent-orchestrator" target="_blank">Adobe Experience Platform Agent Orchestrator</a> 提供支持，可在 Journey Optimizer 中使用。 </p>
<p>Experimentation 代理是一款 AI 驱动的工具，可使在网站、电子邮件、推送消息和应用程序中运行和管理数字试验的方式更加现代化。它可帮助您更高效地运行试验、组织业务目标，并生成可操作洞察，突出显示有效项和无效项以及下一步的试验方向。</p>
<p>有关更多信息，请参阅<a href="https://experienceleague.adobe.com/docs/experience-cloud-ai/experience-cloud-ai/agents/agent-experiment.html?lang=zh-Hans" target="_blank">详细文档</a></p>
<p>发布日期：2025 年 10 月 10 日</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>电子邮件的 PDF 附件</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>您现在可以将静态 PDF 文件附加到使用 Journey Optimizer 发送的电子邮件中。</p>
<ul>
<li>对于每个轮廓，每年最多可以发送 6 条包含 PDF 附件的消息。</li>
<li>每个附件的最大文件大小为 5 MB。</li>
<li>如需额外大小或容量，您可以购买 PDF 附件功能的附加组件。有关更多信息，请与 Adobe 代表联系。</li>
</ul>
<p>此功能之前为限量发布版，现在可供在所有环境中使用（正式发布）。</p>
<p><img src="assets/do-not-localize/pdf-attachments.gif"/></p>
<p>有关更多信息，请参阅<a href="../email/pdf-attachments.md">详细文档</a></p>
<p>发布日期：2025 年 9 月 30 日</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>用于检索历程的公共 API</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>新 Journey Optimizer API 现在可用于检索历程及其关联的对象，例如营销活动和表面。</p>
<p>有关更多信息，请参阅<a href="https://developer.adobe.com/journey-optimizer-apis/references/journeys-retrieve/">详细文档</a></p>
<p>发布日期：2025 年 9 月 25 日</p>
</td>
</tr>
</tbody>
</table>


### 改进

**通过 AI 模型在电子邮件中决策**

您现在可以通过使用决策，使用 AI 模型优化电子邮件中的最佳内容。例如，此功能可以让您根据自定义事件（如购买、按钮点击、添加到购物车等）优化最佳内容。

**WhatsApp 渠道的执行字段**

除了电子邮件和短信之外，您还可以在沙盒级别更新 WhatsApp 投放的默认执行字段。也可以通过更改 WhatsApp 历程活动高级参数或 WhatsApp 渠道配置来覆盖全局设置的执行字段。<!-- [Read more](../FILE.md) -->

**自定义属性支持 Mailto（取消订阅）地址**

借助 Journey Optimizer，若您在 Adobe 平台外管理同意，可通过在电子邮件设定中定义一键取消订阅链接和自定义取消订阅电子邮件来设置外部自定义端点。当您的收件人点击取消订阅链接时，Journey Optimizer 会将一些默认的特定于轮廓的参数附加到同意更新事件。

为进一步对自定义端点进行个性化设置，您现在可以定义还将会附加到同意事件的自定义属性。[了解详情](../email/list-unsubscribe.md#custom-attributes)

>[!AVAILABILITY]
>
>此功能自 2025 年 8 月起已可用于自定义&#x200B;**[!UICONTROL 一键取消订阅 URL]**，现在，在有限发布版中可用于 **[!UICONTROL Mailto（取消订阅）]**&#x200B;选项。请联系 Adobe 代表以获取访问权限。

发布日期：2025 年 10 月 6 日