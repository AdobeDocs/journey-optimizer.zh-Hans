---
solution: Journey Optimizer
product: journey optimizer
title: 发行说明
feature: Release Notes
role: User
level: Beginner, Intermediate
description: Adobe Journey Optimizer 发行说明
exl-id: 06fa956a-b500-416e-9d42-b683c328e837
source-git-commit: 868debfda4791dde687a8db5edd04af79e8f4081
workflow-type: tm+mt
source-wordcount: '1734'
ht-degree: 15%

---

# 发行说明 {#release-notes}

>[!CONTEXTUALHELP]
>id="ajo_homepage_card1"
>title="新增功能"
>abstract="**Adobe Journey Optimizer** 不断地提供新功能、对现有功能的增强和错误修复。会在每月的最后一周将所有更改整合到发行说明中。"

[!DNL Adobe Journey Optimizer] 遵循持续交付模型，允许 Adobe 持续交付新功能、增强功能和修复。此方法支持以可扩展的方式分阶段推出各种功能，以确保所有环境的性能和稳定性。

由于此模型，每月发行版本之间会更新发行说明。 有关发行周期和可用性阶段的完整详细信息，请参阅 [Journey Optimizer 发行周期](releases.md)。

[!DNL Adobe Journey Optimizer] 原生构建于 [!DNL Adobe Experience Platform] 之上并继承了其所具备的最新创新技术和改进。在 [Adobe Experience Platform 发行说明](https://experienceleague.adobe.com/docs/experience-platform/release-notes/latest.html?lang=zh-Hans){target="_blank"}中进一步了解这些更改。

## 2026年1月预发行说明 {#latest-rn}

**发行日期**： 2026年1月27日至28日

**以下预发行说明可能会在正式发行日期之前有所更改，恕不另行通知**。链接、屏幕和更新的文档会于发布日期在发行说明中发布。

另请参阅 [Adobe Experience Platform 预发行说明](https://experienceleague.adobe.com/zh-hans/docs/experience-platform/release-notes/pre-release-notes){target="_blank"}。

### 新功能 {#jan-26-01-features}

<table>
<thead>
<tr>
<th><strong>无讯息小时数（基于时间的排除）</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>无讯息小时允许您为电子邮件、短信、推送和WhatsApp渠道定义<strong>基于时间的排除</strong>。 它们可确保在特定时间段内不发送任何消息，从而帮助您尊重客户偏好和合规性要求。 您可以通过<strong>规则集</strong>应用无提示小时数，该规则集可以分配给营销活动或历程中的单个操作，以实现精确控制。</p>
<p>此功能以前以“有限可用”的形式发布，但现在对所有环境可用（一般可用）。 在此General Availability版本中，该功能现在包括允许客户将促销活动操作排队到免打扰时间完成的功能，以及预览激活的免打扰时间规则的功能。</p>
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
<p>以前仅限于营销活动，现在历程画布上提供<strong>直邮渠道</strong>，可让您将直邮合并到历程中。 现在，可以在批处理和1:1历程场景中使用直邮，并且支持文件提取配置和基于时间的频率设置。</p>
<p>此功能之前为限量发布版，现在可供在所有环境中使用（正式发布）。</p>
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
<p>直邮渠道现在可用于编排的营销活动。 <strong>直邮活动</strong>有助于在协调的活动中发送一次性消息和定期消息的直邮。 它会自动生成直邮提供商所需的<strong>提取文件</strong>。 您可以将渠道活动合并到编排的活动画布中，以创建跨渠道活动，从而根据客户行为和数据触发操作。</p>
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
<p>您现在可以将<strong>决策策略</strong>添加到短信历程和营销活动中。 决策策略是产品建议的容器，利用决策引擎动态返回将会为每个受众成员提供的最佳内容。</p>
<p>此功能在有限可用性中适用于一系列组织。 联系您的 Adobe 代表。</p>
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
<p>通过新的<strong>监控仪表板</strong>和丰富的历程步骤事件数据，更深入地了解insight的运行状况以及自定义操作端点的性能。 跟踪成功的调用、错误、吞吐量、响应时间和队列等待时间，以快速了解发生异常的时间、位置和原因。</p>
<p>此功能之前为限量发布版，现在可供在所有环境中使用（正式发布）。</p>
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
<p>Journey Agent现在提供创建功能，可让Journey Optimizer用户通过<strong>自然语言界面</strong>构建和配置营销历程。 从业者可以通过在对话提示中描述其要求来快速创建历程。 这简化了历程创建过程，允许营销人员专注于策略而不是技术配置。</p>
</td>
</tr>
</tbody>
</table>

### 改进 {#jan-26-01-improv}

此版本包含的改进如下所述。

#### 人工智能

* **AI助理内容质量检查** — 除了品牌协调之外，您现在还可以评估总体<strong>内容质量</strong>，以发现可读性、一致性和有效性方面的潜在问题，这与您的品牌准则无关。 这些自动检查有助于识别不明确的消息传送、不一致的语调或结构性缺口。

* **使用新的颜色选项卡更新品牌** — 品牌指南有助于确保在所有接触点上始终如一地展示您的品牌。 新的<strong>颜色部分</strong>定义了您品牌颜色系统的标准，概述了如何在体验间选择、组织和应用颜色。 它确保了一致地使用主要、次要、个性色和中性色，以支持有凝聚力、可访问和可识别的品牌标识。

#### 渠道

#### 营销活动

#### Experience Decisioning

* **将片段附加到决策项** — 现在，Journey Optimizer提供将<strong>片段</strong>附加到决策项的功能，可在基于代码的体验营销活动中通过决策策略利用此功能。

  **注意**：以前以有限可用性发布，现在此改进对所有环境都可用（正式发布）。

#### 历程

* **在历程自定义操作中利用失败响应有效负载** — 您现在可以为自定义操作定义可选的<strong>错误响应有效负载</strong>。 当调用失败时，错误有效负载会在历程上下文中公开，并与`jo_status_code`一起在超时/错误分支中可用，以支持更丰富的回退逻辑和调试。

* **将本机和Adobe Campaign消息操作结合使用** — 现在，通过Journey Optimizer，可将Adobe Campaign v7/v8消息操作与同一历程中的本机渠道操作结合使用。

* **历程中的有效负载大小验证**&#x200B;历程- Journey Optimizer现在验证历程有效负载的大小以帮助确保最佳性能和系统稳定性。 在构建或发布历程时，如果有效负载大小接近或超过建议的限制，您将收到明确的警告和错误，并获得可操作的指导以优化历程配置。 此主动验证可帮助您尽早识别潜在问题并保持历程性能。

#### 编排的营销活动

* **选择属性和复制分配值** — 您现在可以直接从编排的营销活动中的值分配视图中选择或复制值。

* **受众的数据使用标签继承** — 现在，在编排的营销活动中保存受众时，Adobe Experience Platform中应用的标签会自动延续，从而减少手动DULE标记。

* **预定义的重定位过滤器** — 为了支持更轻松地针对编排的营销活动用例进行重定位，此版本引入了新的<strong>营销活动反馈过滤器</strong>。 通过这些过滤器，您可以根据消息参与度（例如，已发送、已打开、已打开或已单击，或已打开或已单击或已单击）直接定位受众，并选择要重新定位的特定营销活动或过渡中营销活动。

* **带参数的预定义过滤器** — 您现在可以在编排的营销活动中创建带<strong>个参数的预定义过滤器</strong>，以便形成可重用、可编辑的规则。

* **发送前的消息确认** — 默认情况下，在发送协调的活动之前，将启用<strong>确认步骤</strong>，以减少意外发送。

* **用户生成的元数据支持** - <strong>executionMetadata帮助程序函数</strong>现在可用于编排的营销活动的个性化编辑器，使您能够将上下文信息附加到任何本机操作并将其存储在数据集中，以导出到外部系统。

* **重新启动按钮** — 编排的营销活动现在包含<strong>重新启动按钮</strong>，因此，您可以在发布营销活动之前根据需要快速重新启动运行。

* **速率控制支持** — 编排的营销活动现在支持<strong>速率控制</strong>，以帮助您加快投放速度并与数量限制保持一致。

#### 权限

* **阻止历程和营销活动自行审批** — 在创建或设置审批策略时添加了一个选项，以防止历程或营销活动创建者审批自己的对象。

## 即将推出 {#jan-26-01-coming-soon}

在接下来的几天内，将计划发布以下功能和增强功能。**信息可能会有所更改**。这些更新在生产环境中启用后，将会共享更新的链接、屏幕和文档。

### 改进

* 所有短信提供商都将支持&#x200B;**短信Webhook** - <strong>Webhook</strong>。 您将能够根据预期目的配置每个webhook：用于捕获传入消息的入站webhook和用于接收投放接收、状态更新和其他消息相关事件的反馈webhook。 可用日期：2026年1月28日。

* **使用用户档案时区安排营销活动** — 营销活动安排将能够使用每个用户档案的<strong>时区</strong>在预期的本地时间投放消息。 **注意**：此改进仅适用于一组组织（限量发布）。 可用日期：2026年1月28日。

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
<p>新的<strong>消息导出</strong>功能将可用于电子邮件和短信渠道。 此功能允许您自动将已发送的消息内容导出到专用的Experience Platform数据集，从而使您能够：</p>
<ul>
<li>满足法规遵从性要求（如HIPAA ）</li>
<li>存档法律索赔和客户关怀查询的消息</li>
<li>保留发送给个人的个性化内容的副本</li>
</ul>
<p>记录会保留在AJO消息导出数据集中，从引入后保留7天。 在此保留期内，您可以通过Experience Platform目标将数据导出到您自己的存储中。 该功能在渠道配置级别启用，使您可精细地控制要导出哪些消息。</p>
<p>此功能仅适用于电子邮件和短信渠道，以及购买了Message Export附加产品的组织。 有关更多信息，请与您的 Adobe 代表联系。</p>
<p>发布日期： 2026年1月28日</p>
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
<p>Adobe Journey Optimizer将支持<strong>Web推送通知</strong>，从而将推送渠道扩展到移动以外。 您将能够向移动浏览器和桌面浏览器发送通知，从而能够直接在其设备上联系客户，而无需应用程序。 此增强功能将帮助您利用与移动推送相同的创作工作流和定位功能，实时向用户发送个性化的即时消息。</p>
<p>此功能以前在Beta中发布，现在将对所有环境可用（正式发布）。</p>
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
<p><strong>迁移工具API</strong>可用于以编程方式将决策管理实体迁移到Decisioning，其功能：</p>
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
<th><strong>Journey Agent中的内容生成</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p><strong>Journey Agent</strong>由Adobe Experience Platform Agent Orchestrator提供支持，将在Journey Optimizer中提供，并且允许您通过自然语言界面分析旅程。 您将能够直接在Journey Agent中生成和管理特定于渠道的内容，为电子邮件和推送等渠道创建内容，应用和预览模板，通过提示优化音调和样式，以及在<strong>Content Designer</strong>中打开内容以进行上下文内编辑。</p>
<p>发布日期：2026年2月2日</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>推送渠道中的决策支持</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>您将能够使用<strong>决策</strong>对推送消息的内容进行个性化和优化。 使用<strong>优先级得分</strong>、公式或AI模型向客户显示最佳内容。</p>
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
<p>历程画布中将提供新的<strong>内容决策活动</strong>，用于将个性化优惠直接集成到客户历程中。 此活动让您能够在整个历程中提供基于决策的内容并引用这些选件，在条件中用于创建基于资格的分支，在自定义操作中用于将选件数据传递到外部系统，以及在其他活动中用于构建完全个性化的客户体验。</p>
<p>此功能将对所有环境可用（正式发布）。</p>
<p>发布日期：2026年2月3日</p>
</td>
</tr>
</tbody>
</table>
