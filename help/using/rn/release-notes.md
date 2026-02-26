---
solution: Journey Optimizer
product: journey optimizer
title: 发行说明
feature: Release Notes
role: User
level: Beginner, Intermediate
description: Adobe Journey Optimizer 发行说明
exl-id: 06fa956a-b500-416e-9d42-b683c328e837
source-git-commit: 82972e593628b44406b0a545225d65f6ed645274
workflow-type: tm+mt
source-wordcount: '1606'
ht-degree: 35%

---

# 发行说明 {#release-notes}

>[!CONTEXTUALHELP]
>id="ajo_homepage_card1"
>title="新增功能"
>abstract="**Adobe Journey Optimizer** 不断地提供新功能、对现有功能的增强和错误修复。会在每月的最后一周将所有更改整合到发行说明中。"

[!DNL Adobe Journey Optimizer] 遵循持续交付模型，允许 Adobe 持续交付新功能、增强功能和修复。此方法支持以可扩展的方式分阶段推出各种功能，以确保所有环境的性能和稳定性。

由于此模型，在每月发行版本之间会更新发行说明。有关发行周期和可用性阶段的完整详细信息，请参阅 [Journey Optimizer 发行周期](releases.md)。

[!DNL Adobe Journey Optimizer] 原生构建于 [!DNL Adobe Experience Platform] 之上并继承了其所具备的最新创新技术和改进。在 [Adobe Experience Platform 发行说明](https://experienceleague.adobe.com/docs/experience-platform/release-notes/latest.html?lang=zh-Hans){target="_blank"}中进一步了解这些更改。

## 2026年2月发行说明 {#feb-26-01-rn}

[新功能](#feb-26-01-features)和[改进](#feb-26-01-improv)部分涵盖的功能已经可用。 [即将推出](#coming-soon)部分列出了计划于2月晚些时候发布的功能和改进。

<!--**The pre-release notes below are subject to change without prior notice until the release availability date**. Links, screens and updated documentation are published in the release notes, at the release date.

See also [Adobe Experience Platform Pre-release notes](https://experienceleague.adobe.com/en/docs/experience-platform/release-notes/pre-release-notes){target="_blank"}.-->

<!--**Release date**: February 17-18, 2026-->

### 新功能 {#feb-26-01-features}


<!--
<table>
<thead>
<tr>
<th><strong>Mobile Live Activities</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p><strong>Live Activities</strong> provide real-time updates and interactive experiences within mobile apps, allowing users to stay informed about ongoing events or tasks directly on their device's screen. This feature enhances engagement by delivering live information, such as progress tracking, event updates, or interactive content, without requiring users to open the app.</p>
<p>Previously released in beta, this capability is now available to all environments (General Availability).</p>
</td>
</tr>
</tbody>
</table>
-->

<table>
<thead>
<tr>
<th><strong>历程仲裁</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>您现在可以使用<strong>排名公式</strong>根据客户个人资料属性和上下文因素自动提升历程优先级分数，确保客户进入最相关的历程。</p>
<!--p><img src="assets/do-not-localize/journey-arbitration-formulas.gif"/></p-->
<p>此功能仅面向一部分组织（限量发布）。要获得访问权限，请与 Adobe 代表联系。</p>
<p>有关更多信息，请参阅<a href="../conflict-prioritization/journey-ranking-formulas.md">详细文档</a>。</p>
<p>发布日期： 2026年2月24日</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>历程中的操作活动</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Journey Optimizer支持新的通用<strong>操作活动</strong>，该活动允许您配置单操作和多操作入站操作组，从而简化历程画布中的操作配置。 特别需要指出，通过这项新功能可以：</p>
<ul>
<li>简化历程画布中的原生操作配置。</li>
<li>创建多操作入站操作组的功能。</li>
<li>将优化设置添加到任何内置渠道操作。</li>
<li>能够向任何操作同时添加试验选项和多语言选项。</li>
</ul>
<p><img src="assets/do-not-localize/action-activity.gif"/></p>
<p>此功能此前为有限发布版，现已可供所有环境使用（正式发布版）。</p>
<p>有关更多信息，请参阅<a href="../building-journeys/journey-action.md">详细文档</a>。</p>
<p>发布日期： 2026年2月20日</p>
<p><strong>注意：</strong>现在可以通过“操作”历程活动访问所有本机渠道。 3月版将弃用旧版本机渠道活动。 包含旧版操作的现有历程将继续按原样运行，无需迁移。</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>出站消息的波动发送</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>您现在可以计划来自Journey Optimizer营销活动或历程的消息，以可控批量方式随时间推移投放。</p>
<p>波次发送具备以下优势：</p>
<ul>
<li>更好的可交付性 — 随着时间的推移，分布发送有助于保持发件人的良好信誉并降低被标记为垃圾邮件的风险。</li>
<li>负载控制 — 通过限制同时传出多少条消息，避免使下游系统（例如呼叫中心、登陆页面）不堪重负。</li>
<li>大容量、时效性强的用例 — 适用于较大的受众或您需要控制计时时（例如，呼叫中心容量、加电或有时限的选件）。</li>
</ul>
<p><img src="assets/do-not-localize/waves.gif"/></p>
<p>在<strong>营销活动</strong>中，此功能对所有环境都可用（一般可用性）。 有关更多信息，请参阅<a href="../campaigns/send-using-waves.md">详细文档</a>。</p>

<p>在<strong>历程</strong>中，此功能仅对一组组织可用（限量发布） — 要获得访问权限，请联系您的Adobe代表。 有关更多信息，请参阅<a href="../building-journeys/send-using-waves.md">详细文档</a>。</p>
<p>发布日期： 2026年2月19日</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>将子域迁移至自定义委派</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>您现在可以使用CNAME委派模式将子域直接从界面迁移到自定义委派，这样您就可以根据公司的准则满足更严格的安全策略，而无需重新创建渠道配置。</p>
<p><img src="assets/do-not-localize/subdomain-migration.gif"/></p>
<p>此功能仅面向一部分组织（限量发布）。要获得访问权限，请与 Adobe 代表联系。</p>
<p>有关更多信息，请参阅<a href="../configuration/custom-subdomain-migration.md">详细文档</a>。</p>
<p>发布日期： 2026年2月19日</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Web推送通知渠道</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Adobe Journey Optimizer现在支持<strong>Web推送通知</strong>，从而将推送渠道扩展到移动以外。 您可以无缝地向<strong>移动设备浏览器和桌面设备浏览器</strong>发送通知，使您无需依赖应用程序即可通过客户的设备直接与其联系。通过此增强功能，您可以利用与移动设备推送相同的创作工作流和定位功能，实时向用户发送及时的个性化消息与其互动。</p>
<p><img src="assets/do-not-localize/web-push.gif"/></p>
<p>此功能以前在Beta中发布，现在将对所有环境可用（正式发布）。</p>
<p>有关更多信息，请参阅<a href="../push/push-configuration-web.md">详细文档</a>。</p>
<p>发布日期： 2026年2月13日</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>内容决策活动</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>历程画布中现在提供新的<strong>内容决策活动</strong>，用于将个性化优惠直接集成到客户历程中。 此活动可让您提供基于决策的内容并在整个历程中引用这些优惠 — 在创建基于资格的分支的条件、在用于将优惠数据传递到外部系统的自定义操作以及在其他构建完全个性化客户体验的活动中。</p>
<p>此功能此前为有限发布版，现已可供所有环境使用（正式发布版）。</p>
<p><img src="assets/do-not-localize/content-decision.gif"/></p>
<p>有关更多信息，请参阅<a href="../building-journeys/content-decision.md">详细文档</a>。</p>
<p>发布日期： 2026年2月10日</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>自助迁移工具 API</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>迁移工具API现在可用于以编程方式将<strong>决策管理</strong>实体迁移到<strong>决策</strong>，其功能：</p>
<ul>
<li>灵活的迁移范围（沙盒、产品建议或决策级别）</li>
<li>自动执行依赖关系分析和验证</li>
<li>对已完成的迁移提供回滚支持</li>
<li>具有对象映射的详细迁移报告</li>
</ul>
<p>有关更多信息，请参阅<a href="../experience-decisioning/decisioning-migration-api.md">详细文档</a>。</p>
<p>发布日期：2026 年 2 月 3 日</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>自定义操作监控</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>通过新的监视仪表板和丰富的历程步骤事件数据，更深入地了解insight的运行状况以及自定义操作端点的性能。 跟踪成功的调用、错误、吞吐量、响应时间和队列等待时间，以快速了解发生异常的时间、位置和原因。</p>
<p>此功能此前为有限发布版，现已可供所有环境使用（正式发布版）。</p>
<p>有关更多信息，请参阅<a href="../action/reporting.md">详细文档</a>。</p>
<p>发布日期：2026 年 2 月 3 日</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>短信渠道中的决策支持</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>您现在可以使用Decisioning个性化和优化短信消息的内容。 使用优先级评分、公式或 AI 模型向客户显示最佳内容。</p>
<p>有关更多信息，请参阅<a href="../experience-decisioning/create-decision.md">详细文档</a>。</p>
<p>发布日期：2026 年 2 月 2 日</p>
</td>
</tr>
</tbody>
</table>

### 改进 {#feb-26-01-improv}

此版本包含的改进如下所述。

#### 配置

* **历程表达式中的体验事件用法** — 从2026年4月1日开始，过去90天内未使用此功能的组织将不再支持在历程表达式中使用体验事件属性。 自2025年7月8日以来，此功能已不适用于新客户组织。 有关替代项，请参阅历程中的[体验事件查找](../building-journeys/exp-event-lookup.md)。

#### 内容管理

<!--
* **Update brands with new color tab** - Brand guidelines help ensure your brand is presented consistently across all touchpoints. The new <strong>Colors</strong> section defines the standards for your brand's color system, outlining how colors are selected, organized, and applied across experiences. It ensures consistent use of primary, secondary, accent, and neutral colors to support a cohesive, accessible, and recognizable brand identity. [Read more](../content-management/brands.md)
-->

* **使用主题将图像转换为电子邮件模板** — 在Journey Optimizer中将图像转换为电子邮件模板时，您现在可以使用主题作为输入，以便生成的HTML遵循您的品牌参数。 样式（如背景颜色、按钮颜色、字体、行距、边距和填充）会自动应用，从而减少手动设计工作，并提供只需少量编辑即可使用的模板。 [了解详情](../content-management/image-to-html.md)

  发布日期：2026年2月17日。

<!--* **Text mode for fragments** - You can now create and manage text versions of your fragments, supporting workflows that rely on plain text content and providing the same flexibility as in email content. [Read more](../content-management/create-fragments.md)-->

#### 电子邮件设计器

* **文本缩进** — 您现在可以直接从属性面板将可自定义的左缩进应用到文本组件中段落的第一行。 <!--The new **Indentation** control lets you define indentation in pixels or percentage via a numeric input or slider, with live preview on the canvas. -->这提高了长格式内容（如编辑和文章）的可读性。 [了解详情](../email/get-started-email-style.md)

  发布日期：2026年2月18日。

#### 体验决策

* **在Decisioning中使用Adobe Experience Platform数据的Edge入站支持** — 现在，在Decisioning中使用Adobe Experience Platform数据除了支持历程中的电子邮件和自定义操作之外，还支持边缘入站用例。 [了解详情](../experience-decisioning/aep-data-exd.md)

  此功能仅面向一部分组织（限量发布）。要获得访问权限，请与 Adobe 代表联系。


* **将片段附加到决策项** - Journey Optimizer 现在提供将片段附加到决策项的功能，可在基于代码的体验营销活动中通过决策策略利用这些决策项。[了解详情](../experience-decisioning/fragments-decision-policies.md)

  此功能此前为有限发布版，现已可供所有环境使用（正式发布版）。

  发布日期：2026年2月12日。

#### 个性化

* **执行元数据帮助程序** - `executionMetadata`帮助程序函数现在可供所有Journey Optimizer客户使用。 使用它可以动态地将上下文信息附加到任何本机操作，并将其捕获到数据集中以导出到外部系统。 [了解详情](../personalization/functions/helpers.md#execution-metadata)

  此功能此前为有限发布版，现已可供所有环境使用（正式发布版）。

  发布日期：2026年2月20日。

#### 短信

* **短信Webhook** — 现在，所有短信提供商都支持Webhook。 您可以基于其预期目的配置每个webhook：入站webhook ，以捕获传入消息；反馈webhook，以接收投放接收、状态更新和其他消息相关事件。 [了解详情](../sms/sms-webhook.md)

  发布日期：2026年2月2日。

## 即将推出 {#coming-soon}

以下的功能和改进计划于2月晚些时候发布。 发行日期和范围可能会发生变化，恕不另行通知。

<table>
<thead>
<tr>
<th><strong>Journey Agent：渠道内容创建</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>由<strong>Adobe Experience Platform Agent Orchestrator</strong>提供支持的<strong>Journey Agent</strong>在Journey Optimizer中可用，并允许您通过自然语言界面分析旅程。 您现在还可以直接在Journey Agent中生成和管理特定于渠道的内容，为电子邮件和推送等渠道创建内容，应用和预览模板，通过提示优化音调和样式，以及在<strong>内容Designer</strong>中打开内容以进行上下文内编辑。</p>
<p>发布日期：2026年3月初</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>AI模型监测</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Journey Optimizer现在允许您监控Decisioning AI模型的运行状况、培训状态和性能。 这使您可以验证培训是否成功、排除故障以及了解对结果的影响，以便使用AI为每个客户选择最佳选件。 请注意，此功能仅适用于<strong>决策</strong>（不适用于旧版决策管理模型）。</p>
<p>此功能当前仅适用于<strong>个性化优化</strong>模型（非自动优化）。</p>
<p>发布日期：2026年3月初</p>
</td>
</tr>
</tbody>
</table>

### 改进 {#coming-soon-improv}

* **基于代码的体验渠道中的Experience Decisioning预览** — 现在，在使用基于代码的体验渠道配置Experience Decisioning时，您可以预览决策项。 上线之前，可以直接在创作界面中预览。

  发布日期： 2026年2月18日

* **自定义Firefly模型与第三方图像生成模型的集成** — 实现标准和自定义Firefly模型与批准的第三方图像模型（如NanoBanana）的无缝集成，以便在生成图像时提供更大的灵活性、控制力以及品牌一致性。 这允许您为每个用例选择最佳模型：可满足一般需求的标准Firefly、用于品牌内生成的自定义Firefly，或针对专用或实验场景的批准的第三方模型。

  发布日期：2026年3月初。
