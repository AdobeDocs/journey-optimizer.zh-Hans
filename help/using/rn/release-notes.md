---
solution: Journey Optimizer
product: journey optimizer
title: 发行说明
feature: Release Notes
topic: Content Management
description: Adobe Journey Optimizer 发行说明
exl-id: 06fa956a-b500-416e-9d42-b683c328e837
source-git-commit: b08f996d9871f59665c2d329b493fd6e61030fac
workflow-type: tm+mt
source-wordcount: '1774'
ht-degree: 75%

---

# 发行说明 {#release-notes}

>[!CONTEXTUALHELP]
>id="ajo_homepage_card1"
>title="新增功能"
>abstract="**Adobe Journey Optimizer** 不断地提供新功能、对现有功能的增强和错误修复。会在每月的最后一周将所有更改整合到发行说明中。"

[!DNL Adobe Journey Optimizer]遵循持续交付模型，允许Adobe持续交付新功能、增强功能和修复。 此方法支持可扩展、分阶段地推出各种功能，以确保所有环境的性能和稳定性。

由于此模型，每月发行版本之间会更新发行说明。  专用[最新更新](#updates-rn)部分重点介绍部署到生产环境的新功能和改进，因此您始终可以实时获知所有更改。<!--For full details about the release cycle and availability phases, see [Journey Optimizer release cycle](#releases.md).-->

[!DNL Adobe Journey Optimizer] 原生构建于 [!DNL Adobe Experience Platform] 之上并继承了其所具备的最新创新技术和改进。在 [Adobe Experience Platform 发行说明](https://experienceleague.adobe.com/docs/experience-platform/release-notes/latest.html?lang=zh-Hans){target="_blank"}中进一步了解这些更改。

## 最近更新 {#updates-rn}

下面列出了过去几周发布的新功能和改进及其发布日期。 它们将在月底与下一个发行说明内容一起分组。 另请参阅以下[的最新](#latest-rn)发行说明。

### 新功能 {#updates-features}

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
<p>有关更多信息，请参阅<a href="https://developer.adobe.com/journey-optimizer-apis/references/journeys-retrieve/">详细文档</a></p>
<p>发布日期： 2025年10月13日</p>
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
<th><strong>用于检索历程的公共API</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>新的Journey Optimizer API现在可用于检索历程及其关联的对象，例如营销活动和表面。</p>
<p>有关更多信息，请参阅<a href="https://developer.adobe.com/journey-optimizer-apis/references/journeys-retrieve/">详细文档</a></p>
<p>发布日期：2025 年 9 月 25 日</p>
</td>
</tr>
</tbody>
</table>

### 改进 {#updates-improvements}

对Mailto（取消订阅）地址的&#x200B;**自定义属性支持**

借助Journey Optimizer，如果您在Adobe之外管理同意，则可以通过在电子邮件配置中定义您自己的一键式取消订阅链接和自定义取消订阅电子邮件地址，来设置外部自定义端点。 当您的收件人点击取消订阅链接时，Journey Optimizer 会将一些默认的特定于轮廓的参数附加到同意更新事件。

为进一步个性化您的自定义端点，您现在可以定义也将附加到同意事件的自定义属性。 [了解详情](../email/list-unsubscribe.md#custom-attributes)

>[!AVAILABILITY]
>
>此功能自2025年8月起已可用于自定义&#x200B;**[!UICONTROL 一键取消订阅URL]**，现在已针对&#x200B;**[!UICONTROL Mailto（取消订阅）]**&#x200B;选项在有限可用性中发布。 请联系 Adobe 代表以获取访问权限。

发布日期：2025年10月6日

## 2025 年 9 月发行说明 {#latest-rn}

**发行日期**：2025 年 9 月 23-24 日

### 新功能 {#sept-25-9-features}

<table>
<thead>
<tr>
<th><strong>Journey Optimizer Experimentation Accelerator</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Journey Optimizer Experimentation Accelerator 是以 AI 为基础的产品，旨在将试验提升到新水平。它专为 Adobe Journey Optimizer 和 Adobe Target 用户构建，可统一试验管理，提供 AI 驱动的见解和机会，并引入新的试验代理。</p>
<p>您可以获得：</p>
<ul>
<li><strong>统一试验资源库：</strong>在一个中心工作区中快速查看、筛选和管理 Adobe Journey Optimizer 和 Adobe Target 的所有实验。</li>
<li><strong>AI 试验见解和机会：</strong>生成式 AI 驱动的洞察和建议，带来的价值超越单纯的统计数据。每个试验现在都会呈现切实可行的机会并附上支撑理由，以便团队可以更自信地决定下一步要测试的内容。</li>
<li><strong>Journey Optimizer 对多臂老虎机 (MAB) 试验的支持</strong>：通过多臂老虎机试验，最大限度提高影响力，同时减少流量浪费。MAB 不会平均拆分受众，而是自动将更多访客实时分配到效果最佳的变体，使您能够在检验效果的同时，为更多客户提供更好的体验。</li></ul>
<p><img src="assets/do-not-localize/experimentation-accelerator.gif"/></p>
<p>有关更多信息，请参阅<a href="../content-management/experiment-accelerator.md">详细文档</a></p>
<p>发布日期：2025 年 10 月 3 日</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Journey 代理上线！</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Journey 代理由 <a href="https://experienceleague.adobe.com/zh-hans/docs/experience-cloud-ai/experience-cloud-ai/agents/agent-orchestrator" target="_blank">Adobe Experience Platform Agent Orchestrator</a> 提供支持，可在 Journey Optimizer 中使用。它使您能够通过自然语言界面分析历程。代理能够检测历程中的受众或计划冲突和轮廓流失情况，帮助您采取措施解决这些问题。很快，您便可以创建具有代理式辅助的历程。</p>
<p>有关更多信息，请参阅<a href="https://experienceleague.adobe.com/zh-hans/docs/experience-cloud-ai/experience-cloud-ai/agents/ajo-agent-analyze" target="_blank">详细文档</a></p>
<p>发布日期：2025 年 9 月 24 日</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>电子邮件设计器中的深色模式</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Journey Optimizer 电子邮件设计器现在提供切换到深色模式视图的功能，您可以在其中定义额外的特定自定义设置，这些设置将仅显示给在深色模式下阅读电子邮件的收件人。</p>
<p>请注意以下事项：</p>
<ul>
<li>深色模式的最终呈现可能会有所不同，具体取决于收件人的电子邮件客户端。</li>
<li>并非所有电子邮件客户端都支持自定义深色模式。此外，某些电子邮件客户端只对收到的所有电子邮件应用自己的默认深色模式。在这两种情况下，无法呈现您在电子邮件设计器中定义的自定义设置。</li>
</ul>
<p><img src="assets/do-not-localize/dark-mode.gif"/></p>
<p>有关更多信息，请参阅<a href="../email/dark-mode.md">详细文档</a></p>
 <p>发布日期：2025 年 9 月 16 日</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>历程路径优化</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>使用新的“优化”节点，选择特定的目标受众或运行 A/B 测试，确定满足以业务为中心的 KPI 的最佳路径。</p>
<p>通过此工具，您可以测试、更改并自定义通信、顺序和时间，以便更好地联系客户。</p>
<p>此功能为限量发布版。请联系 Adobe 代表以获取访问权限。</p>
<p><img src="assets/do-not-localize/optimize.gif"/></p>
<p>有关更多信息，请参阅<a href="../building-journeys/optimize.md">详细文档</a></p>
<p>发布日期：2025 年 9 月 4 日</p>
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
<p>此功能为限量发布版。请联系 Adobe 代表以获取访问权限。</p>
<p><img src="assets/do-not-localize/custom-delegation.gif"/></p>
<p>有关更多信息，请参阅<a href="../configuration/delegate-custom-subdomain.md">详细文档</a></p>
<p>发布日期：2025 年 9 月 4 日</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>使用 Adobe Experience Platform 数据进行个性化和决策制定</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>此功能之前为公开 Beta 版，现在可用于所有环境。在此版本中，引入了以下增强功能：</p>
<ul><li>支持在入站渠道中进行个性化数据集查找。</li>
<li>“datasetLookup”辅助函数现在可用于表达式片段中。目前，此功能仅面向部分客户提供。要获得访问权限，请与 Adobe 代表联系。</li>
<li>在数据集管理界面中提供了一个选项，让您可以启用基于记录的数据集以实现查找个性化，而无需执行 API 调用。</li>
<li>增强的监控功能，可跟踪数据摄取状态并了解数据集何时可用于查找。</li>
<li>更新了使用指南和护栏，以确保最佳性能和可靠性。</li>
<li>现在可以在决策上限规则中使用 Adobe Experience Platform 数据集。</li></ul></p>
<p>有关更多信息，请参阅<a href="../data/lookup-aep-data.md">详细文档</a></p>
<p>发布日期：2025 年 9 月 1 日</p>
</td>
</tr>
</tbody>
</table>


### 改进 {#sept-25-9-improvements}

* **API 触发营销活动支持 Webhook**\
  API 触发营销活动现在支持 Webhook。 配置webhook URL以接收每条消息的实时状态更新，从而提高可观察性并实现无缝监控和自动化。 [了解详情](../configuration/feedback-webhooks.md)

  发布日期：2025 年 9 月 29 日

* **短信渠道的 mTLS 支持**
设置自定义短信服务提供商时，您现在可以选择启用双向 TLS (mTLS) 身份验证，这需要客户端和服务器在建立安全连接之前确认彼此的身份。[了解详情](../sms/sms-configuration-custom.md) – 发布日期：2025 年 9 月 23 日

* **基于模型的架构**\
  现在，可以使用基于模型的架构在编排的营销活动中进行关系建模。[了解详情](../orchestrated/gs-schemas.md) – 发布日期：2025 年 9 月 23 日

* **支持在历程中查找数据集**\
  通过历程中新的&#x200B;**数据集查找**&#x200B;活动，您可以在运行时期间从 Adobe Experience Platform 的记录数据集动态检索数据。通过利用此功能，您可以访问可能不存在于轮廓或事件负载中的数据，从而确保客户交互既相关又及时。[了解详情](../building-journeys/dataset-lookup.md) – 发布日期：2025 年 9 月 23 日

  此活动仅面向一部分组织提供（有限发布版）。要获得访问权限，请与 Adobe 代表联系。

* **支持在历程自定义操作中重定向**\
  历程自定义操作现在支持重定向 (302)。– 发布日期：2025 年 9 月 23 日

* **渠道配置监控警报** – 现在，您可以通过电子邮件或 Journey Optimizer 通知中心订阅接收系统警报，以防使用自定义子域委派类型时发生电子邮件渠道配置错误。[了解详情](../reports/alerts.md#alert-channel-config-failure) – 发布日期：2025 年 9 月 23 日

* **一键取消订阅请求** – 我们进行了多项改进，进一步加强了对 Adobe 托管下配置的一键取消订阅请求的处理能力，确保进行可靠一致的处理。– 发布日期：2025 年 9 月 23 日

* **自定义身份验证现在支持嵌套 JSON 正文参数**\
  为自定义操作配置自定义身份验证时，现在支持嵌套 JSON 对象（例如 `bodyParams` 中的子对象）。[了解详情](../datasource/external-data-sources.md#custom-authentication-mode) – 发布日期：2025 年 9 月 18 日

* **按小时重置上限频率** – 您现在可以针对渠道规则集按小时应用上限。此功能之前为有限发布版，现在可在所有环境中使用，并且允许您选择 1 小时（之前为 3 小时）。[了解详情](../conflict-prioritization/channel-capping.md) – 发布日期：2025 年 9 月 17 日

* **模拟所有入站渠道的内容变体**\
  之前，模拟内容变体仅可用于电子邮件、短信和推送通知渠道，现在可用于所有入站渠道。[了解详情](../test-approve/simulate-sample-input.md) – 发布日期：2025 年 9 月 17 日

* **决策上限规则的表达式** – 您现在可以构建自己的表达式来定义决策项的上限规则阈值。[了解详情](../experience-decisioning/items.md#capping) – 发布日期：2025 年 9 月 16 日

* **动态域支持** – Journey Optimizer 现支持对 Adobe 接受的预定义域进行完整/基础 URL 个性化设置。[了解详情](../personalization/personalization-build-expressions.md#where) – 发布日期：2025 年 9 月 12 日

  该功能以有限发布形式向部分客户提供。

* **Webhooks** — 此版本在配置自定义SMS提供程序时引入了Webhook的以下增强功能：

   * 您现在可以定义webhook的目的，即入站或反馈，具体取决于要捕获的数据类型。 [了解详情](../sms/sms-configuration-custom.md#webhook) – 发布日期：2025 年 9 月 23 日

   * 改进了用于配置关键字的界面，以便更轻松地设置。 [了解详情](../sms/sms-configuration-custom.md#webhook) – 发布日期：2025 年 9 月 23 日

* **短信**

   * 设置自定义短信提供商时，您现在可以定义在传入短信包含无法识别的关键字时使用的&#x200B;**Default**&#x200B;关键字。 您还可以为特定操作创建&#x200B;**自定义**&#x200B;关键字。 [了解详情](../sms/sms-configuration-custom.md) – 发布日期：2025 年 9 月 23 日

   * 现在，您可以访问通过短信发送的未定义入站关键词响应，包括配置中未明确定义的拼写错误、单词或句子。 它们存储在&#x200B;**AJO电子邮件跟踪体验事件**&#x200B;数据集的&#x200B;**InboundMessage**&#x200B;下，为期13个月。 仅适用于Sinch、Infobip和自定义SMS提供商。  — 发布日期：2025年9月23日

<!--
* **Approval policy permissions**
  Added an option when creating or setting Approval Policy to prevent Journey/Campaign creators from approving their own objects. [Read more](../test-approve/approval-policies.md) - Availability date: Sept 23, 2025-->

<!--
### Coming soon {#sept-25-9-soon}

In the next few days, the following capabilities and enhancements are scheduled for release. **Information is subject to change**. Updated links, screens, and documentation will be shared once these updates are live in production.

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


* **New Journey Alerts**  
  New pre-configured alerts are available for journeys:

  * Profile Discard Rate Exceeded: Ratio of profile discards to entered profiles over the last 5 mins exceeded threshold.  
  * Custom Action Error Rate Exceeded: Ratio of custom action errors to successful HTTP calls over the last 5 mins exceeded threshold.  
  * Profile Error Rate Exceeded: Ratio of profiles-in-error to entered profiles over the last 5 mins exceeded threshold.


  * [Profile Discard Rate Exceeded](../reports/alerts.md#profile-discard-rate-exceeded): Ratio of profile discards to entered profiles over the last 5 mins exceeded threshold.  
  * [Custom Action Error Rate Exceeded](../reports/alerts.md#custom-action-error-rate-exceeded): Ratio of custom action errors to successful HTTP calls over the last 5 mins exceeded threshold.  
  * [Profile Error Rate Exceeded](../reports/alerts.md#profile-error-rate-exceeded): Ratio of profiles-in-error to entered profiles over the last 5 mins exceeded threshold.

  You can modify threshold values and subscribe to individual journey-level alerts vs globally.

  Availability date: Sept XX, 2025

-->
