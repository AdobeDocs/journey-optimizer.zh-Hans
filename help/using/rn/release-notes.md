---
solution: Journey Optimizer
product: journey optimizer
title: 发行说明
feature: Release Notes
role: User
level: Beginner, Intermediate
description: Adobe Journey Optimizer 发行说明
exl-id: 06fa956a-b500-416e-9d42-b683c328e837
source-git-commit: 2dd468a97b8cb696d4ad7f1d0de2aceb15da29df
workflow-type: tm+mt
source-wordcount: '1839'
ht-degree: 19%

---

# 发行说明 {#release-notes}

>[!CONTEXTUALHELP]
>id="ajo_homepage_card1"
>title="新增功能"
>abstract="**Adobe Journey Optimizer** 不断地提供新功能、对现有功能的增强和错误修复。会在每月的最后一周将所有更改整合到发行说明中。"

[!DNL Adobe Journey Optimizer] 遵循持续交付模型，允许 Adobe 持续交付新功能、增强功能和修复。此方法支持以可扩展的方式分阶段推出各种功能，以确保所有环境的性能和稳定性。

由于此模型，每月发行版本之间会更新发行说明。 有关发行周期和可用性阶段的完整详细信息，请参阅 [Journey Optimizer 发行周期](releases.md)。

[!DNL Adobe Journey Optimizer] 原生构建于 [!DNL Adobe Experience Platform] 之上并继承了其所具备的最新创新技术和改进。在 [Adobe Experience Platform 发行说明](https://experienceleague.adobe.com/docs/experience-platform/release-notes/latest.html?lang=zh-Hans){target="_blank"}中进一步了解这些更改。

## 2026年1月发行说明 {#latest-rn}

**发行日期**： 2026年1月27日至28日

[功能](#jan-26-01-features)和[改进](#jan-26-01-improv)部分包含已提供的功能，而[即将推出](#jan-26-01-coming-soon)列出了计划在以后可用日期推出的项目。

<!-- **The pre-release notes below are subject to change without prior notice until the release availability date**. Links, screens and updated documentation are published in the release notes, at the release date. 

See also [Adobe Experience Platform Pre-release notes](https://experienceleague.adobe.com/zh-hans/docs/experience-platform/release-notes/pre-release-notes){target="_blank"}.-->

### 新功能 {#jan-26-01-features}

<table>
<thead>
<tr>
<th><strong>Web推送通知渠道</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Adobe Journey Optimizer现在支持<strong>Web推送通知</strong>，从而将推送渠道扩展到移动以外。 您可以无缝地向<strong>移动浏览器和桌面浏览器</strong>发送通知，这样您就可以在他们的设备上直接联系客户，而无需使用应用程序。 通过此增强功能，您可以利用与移动设备推送相同的创作工作流和目标选择功能，实时使用个性化消息及时与客户联系。</p>
<p><img src="assets/do-not-localize/web-push.gif"/></p>
<p>此功能之前作为 Beta 版发布，现在可供在所有环境中使用（正式发布）。</p>
<p>有关更多信息，请参阅<a href="../push/push-configuration-web.md">详细文档</a>。</p>
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
<p>直邮渠道现在可用于编排的营销活动。 <strong>直邮活动</strong>有助于在协调的活动中发送一次性消息和定期消息的直邮。 它用于自动执行生成直邮提供商所需的<strong>提取文件</strong>的过程。 您可以在编排营销活动画布中组合各类渠道活动，构建跨渠道营销活动，以根据客户行为和数据触发相应操作。</p>
<p><img src="assets/do-not-localize/dm-oc.gif"/></p>
<p>有关更多信息，请参阅<a href="../orchestrated/activities/channels.md#channel">详细文档</a>。</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Journey Agent — 创建历程</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Journey Agent现在提供创建功能，可让Journey Optimizer用户通过<strong>自然语言界面</strong>构建和配置营销历程。 凭借这些新技能，从业人员只需在<strong>对话提示</strong>中描述其要求即可快速创建历程。 这一创新简化了历程创建过程，使营销人员能够专注于战略而不是技术配置。</p>
<p>有关更多信息，请参阅<a href="../start/ai-features.md#journey-agent">详细文档</a>。</p>
<p>发布日期： 2026年1月12日</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>操作营销活动检索API</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>现已提供新的Journey Optimizer API，可让您以编程方式检索和检查<strong>促销活动相关数据</strong>，如详细信息、版本和配置。</p>
<p>有关更多信息，请参阅<a href="https://developer.adobe.com/journey-optimizer-apis/references/campaigns-retrieve/" target="_blank">详细文档</a>。</p>
<p>发布日期：2025 年 11 月 24 日</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>向Designer主题发送电子邮件</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>您现在可以快速应用<strong>预批准主题</strong>以确保所有电子邮件中的<strong>品牌一致性</strong>、加快营销活动创建过程并独立生成高质量电子邮件，同时减少对设计团队的依赖。</p>
<p><img src="assets/do-not-localize/themes.gif"/></p>
<p>此功能之前以 Beta 发布，现在可供一部分组织使用（有限发布）。要获得访问权限，请与 Adobe 代表联系。</p>
<p>有关更多信息，请参阅<a href="../email/apply-email-themes.md">详细文档</a>。</p>
<p>发布日期：2025 年 11 月 5 日</p>
</td>
</tr>
</tbody>
</table>

### 改进 {#jan-26-01-improv}

#### 人工智能

* **AI助理内容质量检查** — 除了品牌协调之外，您现在还可以评估整体<strong>内容质量</strong>以发现<strong>可读性</strong>、一致性和有效性方面的潜在问题，这与您的品牌准则无关。 这些自动检查有助于识别不明确的消息传送、不一致的语调或结构性缺口。 [阅读更多](../content-management/brands-score.md#validate-quality)。 [在视频中发现此功能](https://video.tv.adobe.com/v/3470556/?captions=chi_hans&learn=on)。

#### Experience Decisioning

* **将片段附加到决策项** — 现在，Journey Optimizer提供将<strong>片段</strong>附加到<strong>决策项</strong>的功能，可在基于代码的体验营销活动中通过决策策略利用这些功能。 [了解详情](../experience-decisioning/items.md)

  **注意**：以前以有限可用性发布，现在此改进对所有环境都可用（正式发布）。

#### 历程

* **合并本机和Adobe Campaign消息操作** — 现在，通过Journey Optimizer，可在同一历程中将<strong>Adobe Campaign v7/v8</strong>消息操作与<strong>本机渠道操作</strong>合并。 [了解详情](../building-journeys/using-adobe-campaign-v7-v8.md)

* **自定义操作错误响应负载** — 您现在可以为自定义操作定义可选的<strong>错误响应负载</strong>。 当调用失败时，错误有效负载会公开在历程上下文中（在操作的errorResponse节点下），并在<strong>timeout/error分支</strong>以及`jo_status_code`中可用，以支持更丰富的回退逻辑和调试。 [了解详情](../action/action-response.md)

* **历程中的有效负载大小验证**&#x200B;历程- Journey Optimizer现在验证<strong>有效负载大小</strong>，以帮助确保最佳性能和系统稳定性。 在构建或发布历程时，如果有效负载的大小接近或超过建议的限制，您会收到明确的<strong>警告和错误</strong>，并获得可操作的指导以优化历程配置。 此主动验证可帮助您尽早识别潜在问题并保持历程性能。 [了解详情](../start/guardrails.md#journey-payload-size)

* **历程警报** — 有新的<strong>预配置的警报</strong>可用于历程。
   * <strong>超过配置文件丢弃率</strong> — 过去5分钟输入的配置文件与配置文件丢弃的比率超过阈值
   * <strong>自定义操作错误率超过</strong> — 自定义操作错误与过去5分钟成功HTTP调用的比率超过阈值
   * <strong>超过配置文件错误率</strong> — 在过去5分钟内输入的配置文件与错误的配置文件之比超过阈值

  有关更多信息，请参阅[详细文档](../reports/alerts.md)。

  发布日期：2025年10月14日。

#### 编排的营销活动

* **受众的数据使用标签继承** — 现在，在协调的营销活动中保存<strong>受众</strong>时，Adobe Experience Platform中应用的标签会自动延续，从而减少手动<strong>DULE标记</strong>。 [了解详情](../orchestrated/activities/save-audience.md)

* **带参数的预定义过滤器** — 您现在可以在编排的营销活动中创建带<strong>参数</strong>的<strong>预定义过滤器</strong>，用于可重用、可编辑的规则。 [了解详情](../orchestrated/predefined-filters.md)

* **选择属性和复制分发值** — 您现在可以在编排的营销活动中直接从值的<strong>分发</strong>视图<strong>选择或复制值</strong>。 [了解详情](../orchestrated/build-query.md)

* **发送前的消息确认** — 默认情况下，在发送协调的活动之前，将启用<strong>确认步骤</strong>，以减少意外发送。 [了解详情](../orchestrated/activities/channels.md#confirm-message-sending)

* **预定义的重定位过滤器** — 为了支持更轻松地针对编排的营销活动用例进行重定位，此版本引入了新的<strong>营销活动反馈过滤器</strong>。 这些过滤器允许您根据<strong>消息参与</strong>（例如已发送、仅打开、已打开或已单击，或已打开或已单击或已单击）直接定位受众，并选择要重新定位的特定营销活动或过渡中营销活动。 [了解详情](../orchestrated/retarget.md)

* **速率控制支持** — 编排的营销活动现在支持<strong>速率控制</strong>，以帮助您加快投放速度并符合<strong>数量约束</strong>。 [了解详情](../orchestrated/activities/channels.md#rate-control)

* **重新启动按钮** — 编排的营销活动现在包含<strong>重新启动按钮</strong>，因此您可以在发布营销活动之前根据需要快速<strong>重新启动运行</strong>。 [了解详情](../orchestrated/start-monitor-campaigns.md)

* **用户生成的元数据支持** - <strong>executionMetadata帮助程序函数</strong>现在可用于编排的营销活动的个性化编辑器，使您能够将上下文信息附加到任何本机操作并将其存储在数据集中，以导出到外部系统。 [了解详情](../personalization/functions/helpers.md#execution-metadata)

#### 权限

* **阻止历程和营销活动自行审批** — 在创建或设置<strong>审批策略</strong>时添加了一个选项，用于阻止历程或营销活动创建者<strong>审批他们自己的对象</strong>。 [了解详情](../test-approve/approval-policies.md)

## 即将推出 {#jan-26-01-coming-soon}

在接下来的几天内，将计划发布以下功能和增强功能。**信息可能会有所更改**。这些更新在生产环境中启用后，将会共享更新的链接、屏幕和文档。

### 功能

<table>
<thead>
<tr>
<th><strong>消息导出</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>新的<strong>消息导出</strong>功能现在可用于电子邮件和短信渠道。 此功能允许您自动将已发送的消息内容导出到专用的Experience Platform数据集，从而使您能够：</p>
<ul>
<li>满足法规遵从性要求（如HIPAA ）</li>
<li>存档法律索赔和客户关怀查询的消息</li>
<li>保留发送给个人的个性化内容的副本</li>
</ul>
<p>记录会保留在AJO消息导出数据集中，从引入后保留7天。 在此保留期内，您可以通过Experience Platform目标将数据导出到您自己的存储中。 该功能在通道配置级别启用，为您提供<strong>粒度控制</strong>导出消息的权限。</p>
<p>此功能仅适用于电子邮件和短信渠道，以及购买了Message Export附加产品的组织。 有关更多信息，请与您的 Adobe 代表联系。</p>
<p>发布日期： 2026年1月28日</p>
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
<p>以前只有营销活动，现在历程画布上提供<strong>直邮</strong>渠道，可让您将直邮合并到历程中。 直邮现在可在<strong>批处理和1:1历程方案</strong>中使用，支持文件提取配置和基于时间的频率设置。</p>
<p>此功能以前以“有限可用性”发布，它将对所有环境可用（一般可用性）。</p>
<p>发布日期： 2026年1月28日</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>无讯息小时数（基于时间的排除）</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p><strong>安静时间</strong>允许您定义电子邮件、短信、推送和WhatsApp渠道的基于时间的排除项。 它们可确保在特定时间段内不发送任何消息，从而帮助您尊重客户偏好和合规性要求。 您可以通过<strong>规则集</strong>应用无提示小时数，该规则集可以分配给营销活动或历程中的单个操作，以实现精确控制。</p>
<p>此功能以前以“有限可用”的形式发布，但现在向所有环境提供。 在此General Availability版本中，该功能现在包括让客户将促销活动操作排队到免打扰时间完成的功能，以及预览激活的免打扰时间规则的功能。</p>
<p>发布日期： 2026年1月28日</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>自助迁移工具API</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p><strong>迁移工具API</strong>现在可用于以编程方式将决策管理实体迁移到Decisioning，其功能：</p>
<ul>
<li>灵活的迁移范围（沙盒、选件或决策级别）</li>
<li>自动化依赖关系分析和验证</li>
<li>对已完成的迁移提供回滚支持</li>
<li>具有对象映射的详细迁移报告</li>
</ul>
<p>发布日期： 2026年1月28日</p>
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
<p>通过新的监视仪表板和丰富的历程步骤事件数据，更深入地了解<strong>自定义操作端点</strong>的运行状况和性能insight。 跟踪成功的调用、错误、吞吐量、响应时间和队列等待时间，以快速了解发生异常的时间、位置和原因。</p>
<p>此功能之前为限量发布版，现在可供在所有环境中使用（正式发布）。</p>
<p>发布日期： 2026年1月28日</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>推送和短信渠道中的决策支持</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>您现在可以通过<strong>决策</strong>个性化并优化<strong>推送和短信</strong>消息的内容。 使用优先级得分、公式或AI模型向客户显示最佳内容。</p>
<p>发布日期：2026年2月3日</p>
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
<p>历程画布中现在提供了新的<strong>内容决策活动</strong>，用于将<strong>个性化优惠</strong>直接集成到您的客户历程中。 此活动可让您提供基于决策的内容并在整个历程中引用这些选件 — 在创建基于资格的分支的条件中，在用于将选件数据传递到外部系统的自定义操作中，以及在构建完全个性化的客户体验的其他活动中。</p>
<p>此功能将对所有环境可用（正式发布）。</p>
<p>发布日期：2026年2月3日</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Journey Agent中的内容生成</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p><strong>Journey Agent</strong>由Adobe Experience Platform Agent Orchestrator提供支持，可在Journey Optimizer中使用，并允许您通过自然语言界面分析旅程。 您现在还可以在Journey Agent中直接<strong>生成和管理内容</strong>，为电子邮件和推送等渠道创建内容，应用和预览模板，通过提示优化音调和样式，以及在内容Designer中打开内容以进行上下文内编辑。</p>
<p>发布日期：2026年2月2日</p>
</td>
</tr>
</tbody>
</table>

### 改进

* **使用用户档案时区安排营销活动** — 营销活动安排现在可以使用每个用户档案的<strong>时区</strong>在预期的本地时间投放消息。

  **注意**：此改进仅适用于一组组织（限量发布）。

  可用日期：2026年1月28日。

* 现在，所有SMS提供商都支持&#x200B;**SMS Webhook** - <strong>Webhook</strong>。 您可以根据预期目的、用于捕获传入消息的入站Webhook和用于接收投放接收、状态更新和其他消息相关事件的反馈Webhook来配置每个Webhook。

  可用日期：2026年1月28日。
