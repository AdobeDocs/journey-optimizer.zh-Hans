---
solution: Journey Optimizer
product: journey optimizer
title: 发行说明
feature: Release Notes
topic: Content Management
description: Adobe Journey Optimizer 发行说明
exl-id: 06fa956a-b500-416e-9d42-b683c328e837
source-git-commit: d6905059dbf1504407c49f76415e4c6eb819bed7
workflow-type: tm+mt
source-wordcount: '1014'
ht-degree: 47%

---

# 发行说明 {#release-notes}

>[!CONTEXTUALHELP]
>id="ajo_homepage_card1"
>title="新增功能"
>abstract="**Adobe Journey Optimizer** 不断地提供新功能、对现有功能的增强和错误修复。会在每月的最后一周将所有更改整合到发行说明中。"

[!DNL Adobe Journey Optimizer]遵循持续交付模型，允许Adobe持续交付新功能、增强功能和修复。 此方法支持可扩展、分阶段地推出各种功能，以确保所有环境的性能和稳定性。

由于此模型，每月发行版本之间会更新发行说明。  专用[最新更新](#updates-rn)部分重点介绍部署到生产环境的新功能和改进，因此您始终可以实时获知所有更改。<!--For full details about the release cycle and availability phases, see [Journey Optimizer release cycle](#releases.md).-->

[!DNL Adobe Journey Optimizer] 原生构建于 [!DNL Adobe Experience Platform] 之上并继承了其所具备的最新创新技术和改进。在 [Adobe Experience Platform 发行说明](https://experienceleague.adobe.com/docs/experience-platform/release-notes/latest.html?lang=zh-Hans){target="_blank"}中进一步了解这些更改。

## 2025年10月发行说明 {#oct-25-10-rn}

**发行日期**：2025年10月22日

### 新功能 {#oct-25-10-features}

<table>
<thead>
<tr>
<th><strong>无讯息小时数/基于时间的排除</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>利用免打扰时间，您可以定义电子邮件、短信、推送和WhatsApp渠道的基于时间的排除项。 它们可确保在特定时间段内不发送任何消息，从而帮助您尊重客户偏好和合规性要求。</p>
<p>您可以通过规则集应用无提示小时数，这些规则集可以分配给营销活动或历程中的单个操作，以实现精确控制。</p>
<p>免打扰时间规则目前仅适用于一组组织（限量发布）。 要添加到轮候表，请联系您的Adobe代表。</p>
<img src="assets/do-not-localize/quiet-hour.gif">
<p>有关更多信息，请参阅<a href="../conflict-prioritization/quiet-hours.md">详细文档</a>。</p>
<p>发布日期： 2025年10月22日</p>
</td>
</tr>
</tbody>
</table>

<!--table>
<thead>
<tr>
<th><strong>Custom action monitoring and reporting</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>This capability provides better visibility into journey health and execution, including lifecycle status and performance alerts. You can now quickly understand when, where, and why an anomalous situation is occurring in a custom action.</p>
<img src="assets/do-not-localize/FILE.gif">
<p>For more information, refer to the <a href="../FILE.md">detailed documentation</a>.</p>
<p>Availability date: October 22, 2025</p>
</td>
</tr>
</tbody>
</table-->

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

<!--table>
<thead>
<tr>
<th><strong>New API to retrieve Action Campaigns</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>A new Journey Optimizer API is now available, enabling you to programmatically retrieve and inspect campaign-related data such as details, versions, and configurations.</p>
<p>For more information, refer to the <a href="https://developer.adobe.com/journey-optimizer-apis/references/campaigns-retrieve/">detailed documentation</a>.</p>
<p>Availability date: October 22, 2025</p>
</td>
</tr>
</tbody>
</table-->

<!--<table>
<thead>
<tr>
<th><strong>New source connectors for loyalty apps</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>New source connectors are now available in Adobe Experience Platform for the Talon.One, Capillary and Kobie loyalty Apps. These connectors let you seamlessly stream loyalty data into Adobe Experience Platform and leverage these data in Journey Optimizer.</p>
<p>For more information, refer to the <a href="../start/get-started-sources.md">detailed documentation</a>.</p>
<p>Availability date: October 22, 2025</p>
</td>
</tr>
</tbody>
</table>-->

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
<p>For more information, refer to the <a href="../FILE.md">detailed documentation</a>.</p>
<p>Availability date: October 22, 2025</p>
</td>
</tr>
</tbody>
</table-->

<!--<table>
<thead>
<tr>
<th><strong>High throughput messaging for API triggered email campaigns</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>A new high throughput transactional messaging mode is available in API triggered campaigns. This mode is designed for large-scale, real-time transactional messaging and supports up to 5,000 transactions per second with higher availability. This mode also supports transactional messages without referencing or creating customer profiles, such as guest checkout, order confirmation, password resets, security notifications, and one-time passwords for two-factor authentication.</p>
<p>This capability is only available for the email channel, for organizations that have purchased the Adobe High Throughput Transactional Messaging add-on offering. Contact your Adobe representative for more details.</p>
<p>For more information, refer to the <a href="../campaigns/api-triggered-campaign-action.md">detailed documentation</a>.</p>
<p>Availability date: October 22, 2025</p>
</td>
</tr>
</tbody>
</table>-->

<table>
<thead>
<tr>
<th><strong>可重复使用的定位规则</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>为了节省您所花的时间和精力，Journey Optimizer现在允许您从专用UI菜单创建可重用的规则，并在构建定位时利用这些规则，无论是在营销活动中的内容优化还是在优化历程活动中。</p>
<p>定位规则当前处于“有限可用”状态。 请联系 Adobe 代表以获取访问权限。请注意，此功能仅适用于已购买Decisioning附加产品的组织。 它将逐步推广到所有客户。</p>
<img src="assets/do-not-localize/targeting-rules.gif">
<p>有关更多信息，请参阅<a href="../experience-decisioning/rules.md">详细文档</a>。</p>
<p>发布日期： 2025年10月22日</p>
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
<p>有新的预配置警报可用于监视历程执行：</p>
<ul><li><a href="../reports/alerts.md#alert-discard-rate">超过配置文件丢弃率</a>：过去5分钟输入的配置文件与配置文件丢弃的比率超过阈值</li>
<li><a href="../reports/alerts.md#alert-custom-action-error-rate">自定义操作错误率已超出</a>：自定义操作错误与过去5分钟成功HTTP调用的比率已超过阈值</li>
<li><a href="../reports/alerts.md#alert-profile-error-rate">超过配置文件错误率</a>：在过去5分钟内输入的配置文件与错误的配置文件之比超过阈值。</li></ul> <p>您可以修改阈值并订阅单个历程级别警报和全局警报。</p>
<p>有关更多信息，请参阅<a href="../reports/alerts.md">详细文档</a>。</p>
<p>发布日期： 2025年10月14日</p>
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
<p>个性化编辑器中提供了新的“executionMetadata”辅助函数。 利用该功能，可将上下文信息附加到任何本机操作，并将其捕获到数据集中以导出到外部系统。</p>
<p>此功能为限量发布版。请联系 Adobe 代表以获取访问权限。</p>
<img src="assets/do-not-localize/execution-metadata.gif">
<p>有关更多信息，请参阅<a href="../personalization/functions/helpers.md#execution-metadata">详细文档</a>。</p>
<p>发布日期： 2025年10月13日</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>带有试验代理的Experimentation Accelerator</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Journey Optimizer Experimentation Accelerator现在包括Experimentation Agent，它是一个AI支持的对话工具，可让您与实验、见解和机会进行交互。 它增强了Journey Optimizer Experimentation Accelerator体验，帮助您更高效地运行实验，揭示有效的工作方式，并探索下一步优化的位置。</p>
<p>有关更多信息，请参阅<a href="https://experienceleague.adobe.com/docs/experience-cloud-ai/experience-cloud-ai/agents/agent-experiment.html?lang=zh-Hans" target="_blank">详细文档</a>。</p>
<p>发布日期： 2025年10月10日</p>
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
<p>有关更多信息，请参阅<a href="../email/pdf-attachments.md">详细文档</a>。</p>
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

<!--
## Latest updates {#updates-rn}

New capabilities and improvements released in the past weeks are listed below, with their availability date. They will be grouped with the next release notes content at the end of the month. See also the latest [release notes below](#latest-rn).
-->

### 改进 {#updates-improvements}

<!--Availability date: October 22, 2025-->

WhatsApp渠道的&#x200B;**执行字段**

除了电子邮件和短信之外，您还可以在沙盒级别更新WhatsApp投放的默认执行字段。 也可以通过在WhatsApp历程活动高级参数或WhatsApp渠道配置中更改执行字段来覆盖全局设置的执行字段。 [了解详情](../configuration/primary-email-addresses.md)

发布日期： 2025年10月22日

**自定义属性支持 Mailto（取消订阅）地址**

借助 Journey Optimizer，若您在 Adobe 平台外管理同意，可通过在电子邮件设定中定义一键取消订阅链接和自定义取消订阅电子邮件来设置外部自定义端点。当您的收件人点击取消订阅链接时，Journey Optimizer 会将一些默认的特定于轮廓的参数附加到同意更新事件。

为进一步对自定义端点进行个性化设置，您现在可以定义还将会附加到同意事件的自定义属性。[了解详情](../email/list-unsubscribe.md#custom-attributes)

>[!AVAILABILITY]
>
>此功能自 2025 年 8 月起已可用于自定义&#x200B;**[!UICONTROL 一键取消订阅 URL]**，现在，在有限发布版中可用于 **[!UICONTROL Mailto（取消订阅）]**&#x200B;选项。请联系 Adobe 代表以获取访问权限。

发布日期：2025 年 10 月 6 日

### 即将推出 {#oct-25-10-soon}

在接下来的几天内，将计划发布以下功能和增强功能。**信息可能会有所更改**。这些更新在生产环境中启用后，将会共享更新的链接、屏幕和文档。

#### 新功能 {#oct-25-10-soon-features}

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
<p>此功能以前以测试版发布，现在可供一组组织使用（限量发布）。 要获得访问权限，请与 Adobe 代表联系。</p>
<!--img src="assets/do-not-localize/themes.gif">
<p>For more information, refer to the <a href="../email/apply-email-themes.md">detailed documentation</a>.</p>
<p>Availability date: November 4, 2025</p-->
</td>
</tr>
</tbody>
</table>

#### 改进 {#oct-25-10-soon-improvements}

通过AI模型&#x200B;**在电子邮件中决策**

您现在可以通过使用Decisioning，使用AI模型优化电子邮件中的最佳内容。 例如，此功能允许您根据自定义事件（如购买、按钮点击、添加到购物车等）提供最佳内容。

<!--
<table>
<thead>
<tr>
<th><strong>New Web Push notifications channel</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Adobe Journey Optimizer now supports Web Push notifications, expanding the push channel beyond mobile. You can seamlessly deliver notifications to both mobile and desktop browsers, enabling you to reach customers directly on their devices without requiring an app.</p>
<p>This enhancement allows you to engage users with timely, personalized messages in real time, leveraging the same authoring workflows and targeting capabilities already available for mobile push.</p>
<p>For more information, refer to the <a href="../FILE.md">detailed documentation</a></p>
<p>Availability date: Sept XX, 2025</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Custom action monitoring and reporting</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Custom action monitoring and reporting is now available. This capability provides better visibility into journey health and execution, including lifecycle status and performance alerts. You can now quickly understand when, where, and why an anomalous situation is occurring in a custom action.</p>
<p>For more information, refer to the <a href="../FILE.md">detailed documentation</a></p>
<p>Availability date: Sept XX, 2025</p>
</td>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>New source connectors for loyalty apps</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>New source connectors are now available in Adobe Experience Platform for the Talon.One, Capillary, and Kobie loyalty apps. These connectors let you seamlessly stream loyalty data into Adobe Experience Platform and leverage these data in Journey Optimizer.</p>
</td>
</tr>
</tbody>
</table>


<table>
<thead>
<tr>
<th><strong>Landing page custom forms</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>With [!DNL Journey Optimizer], you can now capture profile attributes though your landing pages.</p>
<p>Create, design and manage custom forms tailored to your needs based on a specific dataset. You can then leverage these forms in landing pages to add the profile attributes of your choice into the dataset defined for each form.</p>
<p>This capability is available in Limited Availability. Contact your Adobe representative to gain access.</p>
<p><img src="assets/do-not-localize/forms.gif"/></p>
<p>For more information, refer to the <a href="../landing-pages/lp-forms.md">detailed documentation</a></p>
<p>Availability date: Sept XX, 2025</p>
</td>
</tr>
</tbody>
</table>
-->
