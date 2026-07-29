---
solution: Journey Optimizer
product: journey optimizer
title: Journey Optimizer 的预发行说明
description: Adobe Journey Optimizer 预发行说明
feature: Release Notes
exl-id: 6e7d1300-8efd-4fdc-90e3-3ccdc3babd2f
TQID: https://experienceleague.adobe.com/951PJzmmITN1nSUapVomlYnPws9pS0TosI1Gl3R9yL4
hide: true
product_v2:
  - id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2:
  - id: a7b2bfc5-be71-4740-b371-76fa6be8df02
subfeature_v2:
  - id: eac3bd2c-b027-4dfa-80d2-0bd752ae4794
  - id: e437f8db-d1f7-44c0-bdc0-b0a361adc4c0
  - id: c4e1378f-bb85-43a2-8b7c-1623ad3b14b5
source-git-commit: c58b70fa5f792e2fa1448034559ad7210e3e10d4
workflow-type: tm+mt
source-wordcount: 967
ht-degree: 21%

---


# 预发行说明 {#e-release-notes}

Adobe Journey Optimizer 不断地提供新功能、对现有功能的增强和错误修复。 所有更改会在每月末整合到[发行说明](release-notes.md)中。

<!--
## June '26 pre-release notes {#june-26-rn}

**The pre-release notes below are subject to change without prior notice until the release availability date**. Links, screens and updated documentation are published once changes are live in production. While most changes are delivered on the release date, a few may roll out later — refer to the Availability Date listed for each entry for details.

See also [Adobe Experience Platform Pre-release notes](https://experienceleague.adobe.com/zh-hans/docs/experience-platform/release-notes/pre-release-notes){target="_blank"}.

**Release date**: June 16-17, 2026

### Journeys {#june-26-journeys}

The following capabilities and improvements are coming to journeys in this release.

<table>
<thead>
<tr>
<th><strong>Channel optimization (Limited Availability)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>You can now add multiple outbound channels (Email, Push, SMS) to a single journey action and let Journey Optimizer automatically deliver through the best channel for each customer. Three optimization modes are available: manual ranking, customer profile preference (XDM attribute), and AI model-based ranking using propensity scores. When the top-ranked channel is unavailable, the system falls back to the next available channel.</p>
<p>This capability is only available for a set of organizations (Limited Availability). To gain access, contact your Adobe representative.</p>
<p>For more information, refer to the <a href="../building-journeys/channel-optimization.md">detailed documentation</a>.</p>
</td>
</tr>
</tbody>
</table>

* **Increased live journey limit and new guardrails** - You can now have up to **200 active journeys**, increased from the previous limit of 100.



### Orchestrated campaigns {#june-26-oc}

The following capabilities and improvements are coming to orchestrated campaigns in this release.

-->

## 2026年7月预发行说明 {#july-26-rn}

**以下预发行说明可能会在正式发行日期之前有所更改，恕不另行通知**。 一旦更改发布到生产环境，链接、屏幕和更新的文档就会发布。 虽然大多数更改都在发布日期交付，但其中一些更改可能会稍后推出。

另请参阅 [Adobe Experience Platform 预发行说明](https://experienceleague.adobe.com/zh-hans/docs/experience-platform/release-notes/pre-release-notes){target="_blank"}。

**发行日期**： 2026年7月28日至29日

<!--

### Onboarding {#july-26-onboarding}

Journey Optimizer introduces the Onboarding Assistant, a new capability in this release.

<table>
<thead>
<tr>
<th><strong>Onboarding Assistant</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Transitioning to Adobe Journey Optimizer from another marketing platform is easier with guided capabilities that help you move existing email content and journeys into Journey Optimizer. A dedicated workspace lets you reuse what you have instead of rebuilding from scratch.</p>
<p>This capability is only available for a set of organizations (Limited Availability). To gain access, contact your Adobe representative.</p>
<GIF placeholder: to be added>
<Documentation link: TBD>
</td>
</tr>
</tbody>
</table>

-->

### 历程 {#july-26-journeys}

此版本中的历程添加了以下改进。

<!-- Documentation link: TBD -->

### 营销活动 {#july-26-campaigns}

此版本中的营销活动添加了以下功能和改进。

<table>
<thead>
<tr>
<th><strong>API触发的电子邮件中的个性化PDF附件</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Journey Optimizer现在支持在API触发的营销活动中，每封电子邮件最多附加5个特定于收件人的PDF。 PDF文件是从Azure或AWS存储中安全获取的，并在发送时附加，每个文件的位置直接传递到API有效负载中。 这允许保留现有的上游文档生成系统，由Journey Optimizer处理投放。</p>
<p>受支持的用例包括发票、对帐单、票证、合同、运输标签和类似的文档，这些文档因收件人而异。 个性化PDF附件仅在API触发的营销活动中可用，在历程或其他营销活动类型（操作、编排）中不受支持。</p>
<p>PDF附件加载项支持更大的附件卷和大小；有关更多信息，请与Adobe代表联系。</p>
<p></p>
<!-- Documentation link: TBD -->
</td>
</tr>
</tbody>
</table>

<!--
<table>
<thead>
<tr>
<th><strong>Inbound experience simulation in Action campaigns</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>You can now simulate inbound channel actions in Action campaigns before going live. Use simulation mode to test your configuration with simulated users and preview the rendered experience, including a generated URL and QR code, so you can validate rules, decisioning, and content rendering end-to-end.</p>
<p>This capability is only available for a set of organizations (Limited Availability). To gain access, contact your Adobe representative.</p>
[GIF placeholder: to be added]
[Documentation link: TBD]
</td>
</tr>
</tbody>
</table>

-->

### 编排的营销活动 {#july-26-oc}

此版本中的编排活动中添加了以下改进。


<!--
* **Send messages in waves** - You can now schedule outbound messages from orchestrated campaigns to be delivered in controlled batches over time. Ideal for high-volume or time-sensitive campaigns, wave sending also supports better deliverability and helps maintain a strong sender reputation by reducing the risk of being flagged as spam.
-->

<!--
### Optimization {#july-26-optimization}

<table>
<thead>
<tr>
<th><strong>Channel optimization</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>You can now configure a journey or campaign action to include multiple outbound channels (Email, Push, SMS) and let Journey Optimizer automatically deliver through the best channel for each customer. Three optimization modes are available:</p>
<ul>
<li>Manual ranking: specify your preferred channel order.</li>
<li>Customer preference: use the customer's preferred channel from their profile (Experience Data Model Consents & Preferences attribute).</li>
<li>AI model-based ranking: use machine learning propensity scores to infer the most effective channel per customer.</li>
</ul>
<p>When the top-ranked channel is unavailable (not opted-in, frequency-capped, or not configured), the system falls back to the next available channel.</p>
<p>This capability is only available for a set of organizations (Limited Availability). To gain access, contact your Adobe representative.</p>
</td>
</tr>
</tbody>
</table>
-->

<!--
<table>
<thead>
<tr>
<th><strong>Quiet Hours support for orchestrated campaigns</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>You can now apply quiet hours to Orchestrated campaigns. Quiet hours let you define time-based exclusions to prevent messages from being sent during specific periods, helping you respect customer preferences and compliance requirements across campaign orchestration use cases.</p>
<Documentation link: TBD>
</td>
</tr>
</tbody>
</table>

* **Ability to Manage Profile Target Dimensions** - You can now delete a Profile Target Dimension or edit and swap its configured identity namespace, providing greater control and flexibility over your data setups.

* **Support for Line** - You can now add LINE actions directly into your Orchestrated campaigns. This new activity allows you to build and deliver highly personalized content, including text, stickers, images, videos, location data, and rich Flex Messages, to engage your customers seamlessly on the LINE platform. This capability is only available for a set of organizations (Limited Availability). To gain access, contact your Adobe representative.

* **New Orchestrated campaigns public APIs** - New API specifications are now available for Orchestrated campaigns. These APIs allow you to programmatically create, manage, and trigger orchestrated campaigns, enabling deeper integration with external systems and automation pipelines.

* **Personalize email sender details per recipient and campaign** - Orchestrated campaigns now support personalization of email header fields, including From name, From address, and Reply-To, using profile attributes or relational data. This allows sender details to reflect the relevant advisor, location, or branch for each recipient, rather than routing all sends through a single corporate address. Header values can be set at the channel level and overridden per campaign using contextual data for more precise control. Documentation link: TBD

* **Target dimension simplification in Orchestrated campaigns** - The active targeting dimension is now shown on the workflow canvas, so you can see which dimension is used by a channel activity. The multi-entity segmentation flow is simpler as you no longer need a separate "Change dimension" activity. Moreover, you can now choose explicitly whether messages are sent at the profile level or at a secondary dimension level.

-->

### 渠道 {#july-26-channels}

此版本中的渠道添加了以下功能和改进。

<table>
<thead>
<tr>
<th><strong>自定义出站频道</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Journey Optimizer现在引入了“自定义渠道”这一新功能，管理员可以通过无代码渠道生成器，将任何基于HTTP的出站消息渠道（如WeChat、Kakao Talk、Messenger或专有提供商）直接引入Journey Optimizer。</p >
<p>配置后，自定义渠道可在营销活动、历程和编排的营销活动中使用，并具有与本机渠道相同的完整功能集：使用表达式编辑器进行个性化、内容实验、预览和验证、现成的报告以及同意和治理实施。</p>
<p>这填补了以前由自定义操作填补的空白，这些操作仅适用于历程，并且缺乏专用渠道功能。</p>
<p>自定义出站渠道当前以“有限可用”的形式提供。 要获得访问权限，请与 Adobe 代表联系。</p>
<!-- GIF placeholder: to be added -->
<!-- Documentation link: TBD -->
</td>
</tr>
</tbody>
</table>

* **吞吐量的性能加载项 — 推送** — 在API触发的营销活动中提供新的高吞吐量事务性消息传递模式。 此模式专为大规模实时事务型消息传递而设计，支持每秒最多 5,000 个事务并具有较高的可用性。 以前仅适用于电子邮件渠道，而现在此功能也可用于推送渠道，适用于已购买Adobe高吞吐量事务性消息传递附加产品的组织。 有关更多详细信息，请与Adobe代表联系。<!-- Documentation link: TBD -->



### 决策 {#july-26-decisioning}

在此版本中，已向Decisioning添加了以下改进。

* **优惠级别的Personalization** — 决策项自定义属性现在可以在交付时使用配置文件、上下文和受众数据进行个性化。 这消除了维护次要内容变体的重复选件的需要，允许营销人员管理更少、更灵活的决策项目。<!-- Documentation link: TBD -->

<!--
* **Placement-level frequency capping in Decisioning** - Frequency capping rules in Decisioning can now be scoped to individual placements, giving you finer control over how often an offer is shown in a given surface. Two modes are available: placement-specific capping (define a cap that applies only when the offer is displayed in a selected placement) and per-placement capping (apply a cap independently across every placement where the offer appears, so each placement maintains its own capping counter). Documentation link: TBD
-->

### 内容管理 {#july-26-content}

此版本中的内容管理添加了以下改进。

* **电子邮件模板**&#x200B;的`<head>`中支持表达式片段 — 现在可以在电子邮件模板的`<head>`中使用表达式片段。 这允许您在一个片段中集中设置样式或任何自定义代码，并在多个模板中重复使用。 更新并重新发布片段后，所有基于引用该片段的模板构建的电子邮件都会自动继承最新代码，而无需分别手动更新每封电子邮件。<!-- Documentation link: TBD -->
<!-- Documentation link: TBD -->



<!--
### Integrations {#july-26-integrations}

The following improvements have been added to integrations in this release.

* **Real-time countdown timers for Adobe Experience Manager Dynamic Media integration** - Marketers can now build countdown timers as Dynamic Media templates in Adobe Experience Manager and pull them directly into Journey Optimizer. Timers render live at the moment of open, so every recipient sees an accurate countdown, not a static image. Configure dates, styling, and fallback values right within the Journey Optimizer editor to power flash sales and limited-time offers. [Documentation link: TBD]
-->

### 个性化 {#july-26-personalization}

此版本中的个性化设置添加了以下改进。

* **管理用于完整/基本URL个性化的域** — 您现在可以直接从Adobe Journey Optimizer中的“管理”设置创建和管理用于完整/基本URL个性化的已批准域，而无需联系Adobe支持部门。<!-- Documentation link: TBD -->

<!-- Documentation link: TBD -->

### 电子邮件设计器 {#july-26-email}

以下功能已添加到此版本的电子邮件渠道中。

<table>
<thead>
<tr>
<th><strong>电子邮件设计器中的模块</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Email Designer 现在内置了一个现成的布局模块库——包括页眉、产品卡片、信息块和页脚等——您可以将这些模块直接拖放到电子邮件画布中。</p>
<p>每个模块都预先配置了可编辑的属性（图像、标题、文本、按钮、链接），并且可以通过 WYSIWYG 界面完全自定义，从而加快电子邮件创建速度，而无需您从头开始构建结构。</p>
<!-- GIF placeholder: to be added -->
<!-- Documentation link: TBD -->
</td>
</tr>
</tbody>
</table>


### 管理 {#july-26-administration}

此版本中的管理中添加了以下功能。

<table>
<thead>
<tr>
<th><strong>Web应用程序防火墙IP白名单</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Adobe Journey Optimizer现在支持将登陆页列入Web应用程序防火墙IP白名单，从而使组织能够强制要求所有传入请求仅通过其配置的Web应用程序防火墙基础架构进行路由。 借助这项增强功能，客户可以将Journey Optimizer配置为拒绝任何绕过Web应用程序防火墙层的直接请求，从而确保始终如一地应用在Imperva等工具中定义的安全策略。</p>
<p>此功能增强了具有严格网络访问要求的企业的安全状况，使它们能够完全控制流向Journey Optimizer托管的登陆页面的流量。</p>
<!-- Documentation link: TBD -->
</td>
</tr>
</tbody>
</table>

### 可用性改进 {#july-26-usability}

此版本中提供了以下可用性改进。

* **内容模板中短信、推送、应用程序内和代码库渠道的快速启动快捷方式** — “内容模板”列表中的&#x200B;**更多操作**&#x200B;按钮现在提供了其他特定于渠道的快捷方式。 对于短信模板，请快速编辑消息或检查字符计数/区段。 对于推送模板，请编辑标题、正文或媒体。 对于应用程序内模板，编辑消息标头、消息正文或媒体URL。 对于代码库渠道模板，请直接编辑代码。 这些快捷方式可扩展已有的电子邮件渠道快速启动快捷方式。<!-- Documentation link: TBD -->
