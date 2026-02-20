---
solution: Journey Optimizer
product: journey optimizer
title: 发行说明2026
description: Journey Optimizer 2026 年发行说明
feature: Release Notes
topic: Content Management
role: User
level: Beginner, Intermediate
exl-id: 65ca94cf-8e17-4a25-90f3-238083f81477
source-git-commit: eb1056b57e72ab1cff5e32bff31b9cba5604f695
workflow-type: tm+mt
source-wordcount: '1371'
ht-degree: 86%

---

# 2026 年版发行说明 {#release-notes-2026}

本页列出了于 2026 年发布的 [!DNL Journey Optimizer] 功能和改进。

## 2026 年 1 月发行说明 {#jan-26-rn}

<!--**Release date**: January 27-28, 2026-->

### 新功能 {#jan-26-01-features}


<table>
<thead>
<tr>
<th><strong>推送渠道中的决策支持</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>您现在可以使用<strong>决策</strong>个性化和优化<strong>推送通知</strong>的内容。 使用优先级评分、公式或 AI 模型向客户显示最佳内容。</p>
<p>包含推送通知的Experience Decisioning需要特定版本的Mobile SDK。 在实施此功能之前，请查看<a href="https://developer.adobe.com/client-sdks/home/release-notes/" target="_blank">发行说明</a>以确定所需的版本，并确保您已相应地升级。 您还可以在<a href="https://developer.adobe.com/client-sdks/home/current-sdk-versions/" target="_blank">此部分</a>中查看您的平台的所有可用SDK版本。</p>
<p>有关更多信息，请参阅<a href="../experience-decisioning/create-decision.md">详细文档</a>。</p>
<p>发布日期：2026 年 1 月 30 日</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>历程中的直邮渠道</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p><strong>直邮</strong>渠道此前仅在 Campaign 中可用，现已在历程画布上推出，使您能够将直邮合并入历程。 现在，可以在<strong>批处理和 1:1 历程场景</strong>中使用直邮，并支持文件提取配置和基于时间的频率设置。</p>
<p>此功能此前为有限发布版，现已可供所有环境使用（正式发布版）。</p>
<p><img src="assets/do-not-localize/dm-journey.gif"/></p>
<p>有关更多信息，请参阅<a href="../direct-mail/get-started-direct-mail.md">详细文档</a>。</p>
<p>发布日期： 2026年1月29日</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>免打扰时间（基于时间的排除项）</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>利用<strong>免打扰时间</strong>，您可以针对电子邮件、短信、推送和 WhatsApp 渠道定义基于时间的排除项。这可确保在特定时间段内不发送任何消息，从而帮助您尊重客户偏好并满足合规性要求。您可以通过<strong>规则集</strong>应用免打扰时间并分配给营销活动或历程中的单个操作，以实现精确控制。</p>
<p>此功能之前为限量发布版，现在可供所有环境使用。随着该正式发布版的发布，该功能现在能够让客户对营销活动操作进行排队，直到免打扰时间结束，以及能够预览已激活的免打扰时间规则。</p>
<p><img src="assets/do-not-localize/quiet-hour-ga.gif"/></p>
<p>有关更多信息，请参阅<a href="../conflict-prioritization/quiet-hours.md">详细文档</a>。</p>
<p>发布日期： 2026年1月29日</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>消息导出</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>现已针对电子邮件和短信渠道推出新的<strong>消息导出</strong>功能。 此功能允许您自动将已发送的消息内容导出到专用的 Experience Platform 数据集，从而使您能够：</p>
<ul>
<li>满足合规性要求（如 HIPAA ）</li>
<li>存档用于法律索赔和客户关怀查询的消息</li>
<li>保留发送给个人的个性化内容的副本</li>
</ul>
<p>记录在 AJO 消息导出数据集中保留 7 个日历日（自引入之日起）。 在此保留期内，您可以通过Experience Platform目标将它们导出到您自己的存储中。 该功能在渠道配置级别启用，使您能够<strong>精细控制</strong>要导出的消息。</p>
<p>此功能适用于已购买消息导出附加组件产品的组织，且仅限于电子邮件和短信渠道。有关更多信息，请与您的 Adobe 代表联系。</p>
<p><img src="assets/do-not-localize/message-export.gif"/></p>
<p>有关更多信息，请参阅<a href="../configuration/message-export.md#message-export">详细文档</a>。</p>
<p>发布日期：2026 年 1 月 28 日</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>编排的营销活动中的直邮渠道</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>编排的营销活动中现已推出直邮渠道。<strong>直邮活动</strong>有助于在编排的营销活动中以直邮方式发送消息，支持一次性发送和定期发送。它用于自动生成直邮服务提供商所需的<strong>提取文件</strong>，从而实现直邮流程的自动化。您可以在编排的营销活动画布中组合各类渠道活动，构建跨渠道营销活动，以根据客户行为和数据触发相应操作。</p>
<p><img src="assets/do-not-localize/dm-oc.gif"/></p>
<p>有关更多信息，请参阅<a href="../orchestrated/activities/channels.md#channel">详细文档</a>。</p>
<p>发布日期：2026 年 1 月 28 日</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Journey Agent - 创建历程</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Journey 代理现在提供创建功能，可让 Journey Optimizer 用户通过<strong>自然语言界面</strong>生成和配置营销历程。 凭借这些新技能，从业人员只需在<strong>对话提示</strong>中描述其要求即可快速创建历程。 这一创新简化了历程创建过程，使营销人员能够专注于战略而不是技术配置。</p>
<p>有关更多信息，请参阅<a href="../start/ai-features.md#journey-agent">详细文档</a>。</p>
<p>发布日期：2026 年 1 月 12 日</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>操作营销活动检索 API</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>新的 Journey Optimizer API 现已推出，可让您以编程方式检索和检查<strong>与营销活动相关的数据</strong>，如详细信息、版本和配置。</p>
<p>有关更多信息，请参阅<a href="https://developer.adobe.com/journey-optimizer-apis/references/campaigns-retrieve/" target="_blank">详细文档</a>。</p>
<p>发布日期：2025 年 11 月 24 日</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>电子邮件设计器主题</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>您现在可以快速应用<strong>预批准的主题</strong>，以确保在所有电子邮件中实现<strong>品牌一致性</strong>、加快营销活动创建流程，并独立生成高品质电子邮件，同时减少对设计团队的依赖。</p>
<p><img src="assets/do-not-localize/themes.gif"/></p>
<p>此功能之前以 Beta 发布，现在可供一部分组织使用（有限发布）。要获得访问权限，请与 Adobe 代表联系。</p>
<p>有关更多信息，请参阅<a href="../email/apply-email-themes.md">详细文档</a>。</p>
<p>发布日期：2025 年 11 月 5 日</p>
</td>
</tr>
</tbody>
</table>

### 改进 {#jan-26-01-improv}

#### AI

* **AI 助手内容质量检查** - 除品牌一致性之外，您现在还可以评估整体<strong>内容质量</strong>，独立于品牌准则识别其在<strong>可读性</strong>、连贯性和有效性方面的潜在问题。 这些自动化检查有助于识别消息表述不清、语调不一致或结构性差距问题。 [了解详情](../content-management/brands-score.md#validate-quality)。

  [观看视频了解此功能](https://video.tv.adobe.com/v/3470544/?learn=on)。

#### 历程

* **将原生和 Adobe Campaign 消息操作结合使用** – Journey Optimizer 现在允许您在同一历程中将 <strong>Adobe Campaign v7/v8</strong> 消息操作与<strong>原生渠道操作</strong>结合使用。[了解详情](../building-journeys/using-adobe-campaign-v7-v8.md)

  可用日期：2026年1月27日。

* **自定义操作错误响应有效负载** - 您现在可以为自定义操作定义可选的<strong>错误响应有效负载</strong>。 如果调用失败，错误有效负载会在历程上下文中显示（在操作的 errorResponse 节点下），同时显示在<strong>超时/错误分支</strong>以及`jo_status_code`中，以支持更丰富的回退逻辑和调试。 [了解详情](../action/about-custom-action-configuration.md#define-the-message-parameters)

  可用日期：2026年1月27日。

* **历程中的历程有效负载大小验证** - Journey Optimizer 现在可验证<strong>有效负载大小</strong>，以确保实现最佳性能和系统稳定性。 生成或发布历程时，如果有效负载的大小接近或超过建议的限制，您会收到明确的<strong>警告和错误</strong>，并获得可操作的指导以优化历程配置。 这种主动验证可帮助您尽早识别潜在问题并保持历程性能。 [了解详情](../start/guardrails.md#journey-payload-size)

  可用日期：2026年1月27日。


* **历程警报** - 现已推出面向历程的新<strong>预配置警报</strong>。
   * <strong>用户档案丢弃率超限</strong> - 过去 5 分钟内，用户档案丢弃数与进入历程的档案数的比率超过阈值
   * <strong>自定义操作错误率超限</strong>：过去 5 分钟内，自定义操作错误与成功 HTTP 调用的比率超过阈值
   * <strong>用户档案错误率超限</strong>：过去 5 分钟内，错误用户档案数与进入历程的用户档案数的比率超过阈值

  有关更多信息，请参阅[详细文档](../reports/alerts.md)。

  发布日期：2025 年 10 月 14 日。

#### 编排的营销活动

* **受众的数据使用标签继承** - 在编排的营销活动中保存<strong>受众</strong>时，Adobe Experience Platform 中应用的标签现在会自动延续，从而减少手动进行 <strong>DULE 标记</strong>。 [了解详情](../orchestrated/activities/save-audience.md)

* **带参数的预定义过滤器** - 您现在可以在编排的营销活动中为可重用、可编辑的规则创建带<strong>参数</strong>的<strong>预定义过滤器</strong>。 [了解详情](../orchestrated/predefined-filters.md)

* **选择属性和复制分发值** - 您现在可以直接从编排营销活动的<strong>值的分发</strong>视图<strong>中选择或复制值</strong>。 [了解详情](../orchestrated/build-query.md)

* **发送前的消息确认** - 发送编排的营销活动之前默认将启用<strong>确认步骤</strong>，以减少意外发送。 [了解详情](../orchestrated/activities/channels.md#confirm-message-sending)

* **预定义的重定位过滤器** - 此版本引入了新的<strong>营销活动反馈过滤器</strong>，用以更轻松地针对编排的营销活动用例进行重定位。 这些过滤器允许您根据<strong>消息参与度</strong>（例如已发送、仅打开、已打开或已单击，或已打开并已单击）直接定位受众，并选择要重新定位的特定营销活动或过渡中营销活动。 [了解详情](../orchestrated/retarget.md)

* **速率控制支持** - 编排的营销活动现在支持<strong>速率控制</strong>，以帮助您加快投放速度并适配<strong>容量限制</strong>。 [了解详情](../orchestrated/activities/channels.md#rate-control)

* **重新启动按钮** - 编排的营销活动现在包含<strong>重新启动按钮</strong>，因此您可以在发布营销活动之前根据需要快速<strong>重新启动运行</strong>。 [了解详情](../orchestrated/start-monitor-campaigns.md)

* **用户生成的元数据支持** - 编排的营销活动的个性化编辑器中现已推出 <strong>executionMetadata 帮助程序函数</strong>，使您能够将上下文信息附加到任何本机操作并将其存储在数据集中，以导出到外部系统。 [了解详情](../personalization/functions/helpers.md#execution-metadata)

  可用日期：2026年1月27日。

* **将实时营销活动还原为草稿状态** — 现在，当实时编排的营销活动遇到执行错误时，或者在开始执行之前需要修改计划的营销活动时，您可以将实时编排的营销活动还原为草稿状态。 在发送第一条消息之前，此选项可用。 [了解详情](../orchestrated/start-monitor-campaigns.md#back-to-draft)

#### 营销活动

* **使用用户档案时区安排营销活动** — 营销活动安排现在可以使用每个用户档案的<strong>时区</strong>在预期的本地时间投放消息。 [了解详情](../campaigns/campaign-schedule.md)

  **注意**：此改进仅适用于一组组织（限量发布）。

  可用日期：2026年1月27日。

#### 权限

* **阻止自行审批历程和营销活动** - 创建或设置<strong>审批策略</strong>时添加了一个选项，用于阻止历程或营销活动创建者<strong>审批他们自己的对象</strong>。 [了解详情](../test-approve/approval-policies.md)

  可用日期：2026年1月27日。
