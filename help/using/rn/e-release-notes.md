---
solution: Journey Optimizer
product: journey optimizer
title: Journey Optimizer 的预发行说明
description: Adobe Journey Optimizer 预发行说明
feature: Release Notes
hide: true
hidefromtoc: true
exl-id: 6e7d1300-8efd-4fdc-90e3-3ccdc3babd2f
source-git-commit: 86bd616a9331c5225c78ccf52c5d26a063fa8654
workflow-type: tm+mt
source-wordcount: '2080'
ht-degree: 29%

---

# 预发行说明 {#e-release-notes}

[!DNL Adobe Journey Optimizer] 不断地提供新功能、对现有功能进行增强和修复错误。所有更改会在每月末整合到[发行说明](release-notes.md)中。


## 2026年1月发布前说明 {#jan-26-01-rn}

**以下预发行说明可能会在正式发行日期之前有所更改，恕不另行通知**。链接、屏幕和更新的文档会于发布日期在发行说明中发布。

另请参阅 [Adobe Experience Platform 预发行说明](https://experienceleague.adobe.com/zh-hans/docs/experience-platform/release-notes/pre-release-notes){target="_blank"}。

**上映日期**：2026年1月26日

### 新功能 {#jan-26-01-features}

<table>
<thead>
<tr>
<th><strong>历程中的操作活动</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Journey Optimizer支持新的通用<strong>操作活动</strong>，该活动允许您配置单个操作和<strong>多操作入站操作组</strong>，从而简化历程画布中的操作配置。 特别需要指出，通过这项新功能可以：</p>
<ul>
<li>简化历程画布中的原生操作配置。</li>
<li>创建多操作入站操作组的功能。</li>
<li>将优化设置添加到任何内置渠道操作。</li>
<li>向任何操作添加试验选项和多语言选项。</li>
</ul>
<p>此功能之前为限量发布版，现在可供在所有环境中使用（正式发布）。</p>
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
<th><strong>免打扰时间 / 基于时间进行排除</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>安静时间允许你为电子邮件、短信、推送和WhatsApp渠道定义 <strong>基于时间的排除</strong> 。 他们确保在特定时间段内不发送任何消息，帮助您尊重客户偏好和合规要求。 你可以通过规则<strong>套装应用安静时间</strong>，这些规则可以分配给战役或旅程中的单个行动，从而实现精确控制。</p>
<p>此功能此前仅限量发布，现在已适用于所有环境。 随着本次全面可用性发布，该功能现在包括客户可以排队执行活动作直到安静时段完成，以及预览激活后的安静时段规则。</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>直邮渠道在旅程中的应用</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>此前仅限于活动的直邮渠道<strong>，</strong>现在已在<strong>旅程画布</strong>上开放，使你能够将直邮融入你的行程中。直邮现可用于批量和1：1的行程场景，支持文件提取配置和基于时间的频率设置。</p>
<p>此功能之前为限量发布版，现在可供在所有环境中使用（正式发布）。</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>网页推送通知频道</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Adobe Journey Optimizer 现在支持 <strong>网页推送通知</strong>，将推送渠道扩展到移动端之外。 你可以无缝地向移动端和桌面端浏览器发送通知，使你无需应用程序即可直接在客户设备上联系他们。 通过此增强功能，您可以利用与移动设备推送相同的创作工作流和目标选择功能，实时使用个性化消息及时与客户联系。</p>
<p>此功能之前为限量发布版，现在可供在所有环境中使用（正式发布）。</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>RCS基础消息</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>借助新的 <strong>RCS Basic附加组件</strong> ，您现在可以在旅程优化器中提供基础的丰富通信服务（RCS）消息，从而在提供商和运营商支持下实现以下增强的消息传递功能：</p>
<ul>
<li>支持使用品牌和经验证的发件人：使用带有品牌化元素（徽标、发件人名称等）的经验证的业务轮廓发送消息。</li>
<li>消息投放洞察：接收详细的投放报告，包括消息状态更新（例如，已发送、已投放、已读取）。</li>
<li>链接跟踪：在 RCS 消息中嵌入和跟踪 URL，以进行参与度分析。</li>
<li>回退到短信：当用户的设备不支持 RCS 或暂时无法通过 RCS 投放时，自动回退到短信。</li>
<li>基本消息构成：发送基于文本的基本的RCS消息。</li>
</ul>
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
<p>您现在可以将<strong>决策策略</strong>添加到推送和短信历程及营销活动中。 决策策略是产品建议的容器，利用决策引擎动态返回将会为每个受众成员提供的最佳内容。</p>
<p>此功能仅面向一部分组织（限量发布）。要获得访问权限，请与 Adobe 代表联系。</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>编排广告活动中的直邮渠道</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>直邮渠道现已在协调活动中提供。 <strong>直邮活动</strong>促进了在你的有序活动中发送直邮，无论是一次性还是定期邮件。它用于自动化生成 <strong>直邮服务商所需的提取文件</strong> 过程。 您可以在编排营销活动画布中组合各类渠道活动，构建跨渠道营销活动，以根据客户行为和数据触发相应操作。</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>登陆页面自定义表单</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>借助Journey Optimizer，您现在可以通过登陆页面捕获<strong>配置文件属性</strong>。 根据特定数据集创建、设计和管理针对您的需求定制的<strong>自定义表单</strong>。 然后，您可以在登陆页面中利用这些表单，将您选择的轮廓属性添加到为每个表单定义的数据集中。</p>
<p>此功能之前为限量发布版，现在可供在所有环境中使用（正式发布）。</p>
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
<p><strong>Adobe Experience Platform 现已提供 Talon.One、Capillary 和 Kobie 忠诚度应用的新源连接器</strong>。这些连接器让您可以无缝地将忠诚度数据流式传输到 Adobe Experience Platform 中，并在 Journey Optimizer 中利用这些数据。</p>
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
<p>现在可以<strong>将已发送的投放</strong>导出到特定数据集，以便进行存档和遵循相关说明。 该容量不仅适用于电子邮件，还包括短信等其他渠道。 消息导出数据集的数据保留现在为<strong>7天</strong>。</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>用于检索操作营销活动的新 API</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>现已提供新的<strong>Journey Optimizer API</strong>，可让您以编程方式检索和检查与活动相关的数据，如详细信息、版本和配置。</p>
<p>有关更多信息，请参阅<a href="https://developer.adobe.com/journey-optimizer-apis/references/campaigns-retrieve/">详细文档</a>。</p>
<p>发布日期：2025 年 11 月 24 日</p>
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
<p>现已推出三款新的 <strong>行程提醒</strong> ，帮助您监控和跟踪行程生命周期事件及自定义作表现：</p>
<ul>
<li><strong>已发布历程</strong>：从业者在历程画布中发布历程时获得通知。</li>
<li><strong>已完成历程</strong>：当历程结束时获得通知，根据基于历程类型（读取受众或事件触发）的特定定义。</li>
<li><strong>已触发自定义操作上限</strong>：自定义操作端点的上限被激活时获得通知。</li>
</ul>
<p>这些警报可以在组织级别订阅，或者针对特定历程进行订阅。</p>
<p>有关更多信息，请参阅<a href="../reports/alerts.md#journey-alerts">详细文档</a>。</p>
<p>发布日期：2025 年 11 月 5 日</p>
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
<p>您现在可以快速应用<strong>预批准的主题</strong>以确保所有电子邮件中的品牌一致性、加快营销活动创建过程并独立生成高质量电子邮件，同时减少对设计团队的依赖。</p>
<p>此功能之前以 Beta 发布，现在可供一部分组织使用（有限发布）。要获得访问权限，请与 Adobe 代表联系。</p>
<img src="assets/do-not-localize/themes.gif">
<p>有关更多信息，请参阅<a href="../email/apply-email-themes.md">详细文档</a>。</p>
<p>发布日期：2025 年 11 月 5 日</p>
</td>
</tr>
</tbody>
</table>

### 改进 {#jan-26-01-improv}

此版本包含的改进如下所述。

#### 人工智能

* **AI助理内容质量检查** — 除了品牌协调之外，您现在还可以评估总体<strong>内容质量</strong>，以发现可读性、一致性和有效性方面的潜在问题，这与您的品牌准则无关。 这些自动检查有助于识别不明确的消息传送、不一致的语调或结构性缺口。
* **使用新的颜色选项卡更新品牌** — 品牌指南有助于确保在所有接触点上始终如一地展示您的品牌。 新的 <strong>“颜色”部分</strong> 定义了品牌色彩系统的标准，概述了颜色的选择、组织和应用方式。 它确保统一使用主色、次色、点缀色和中性色，以支持统一、易于接近且易于识别的品牌形象。

#### 营销活动

* **使用配置文件时区** 安排活动——活动调度现在可以利用每个配置文件的 <strong>时区</strong> 在预定的本地时间发送消息。

  **注意**：此改进仅对部分组织开放（有限可用性）。

#### 渠道

* **短信Webhooks：第二** 阶段——描述待提供。

* **WhatsApp 转售优惠** ——描述待提供。

#### 电子邮件设计工具

* **邮件设计** 器中的原地更正—— <strong>当内容验证过程中检测到违规时，AI驱动的自动内容建议</strong> 现在可在邮件设计器中提供。 如果内容被标记为与品牌指南不符或质量标准不符，系统会主动生成修正后的替代方案，可在线审核并应用，从而提升合规性并加快生产速度。

#### 体验决策

* **历程仲裁** — 您现在可以使用<strong>公式和AI模型</strong>根据客户配置文件属性和上下文因素自动提升历程优先级分数，确保客户进入最相关的历程。

  **注意**：此改进仅适用于一组组织（限量发布）。

* **exd 沙盒工具文档 - 更新** - 描述待提供。

* **自助迁移工具API** ——一套新的 <strong>迁移工具API</strong> ，用于将优惠管理实体迁移到体验决策。 该工具支持沙箱间无缝迁移，具备依赖解决和回滚功能。

* **将片段附加到决策项目**——Journey Optimizer 现在支持将片段<strong>附加</strong>到决策项目，这可以通过决策策略在基于代码的体验活动中加以利用。

  **注意**：此改进此前为有限可用性发布，现已适用于所有环境（正式发布）。

#### 历程

* **在旅程自定义动作** 中利用失败响应负载——你现在可以为自定义动作定义可选 <strong>的错误响应负载</strong> 。 当调用失败时，错误有效载荷会暴露在旅程上下文中，并以超时/错误分支提供，以支持更丰富的备选逻辑和调试。

* **将原生和 Adobe Campaign 消息作** 合并——Journey Optimizer 现在允许你在同一旅程中将 Adobe Campaign v7/v8 消息动作与原生渠道动作合并。

* **旅程有效载荷大小验证** ——Journey Optimizer 现在提供 <strong>有效载荷大小验证</strong> ，帮助确保最佳性能和系统稳定性。 在构建或发布行程时，如果有效载荷大小接近或超过推荐限值，您将获得明确的警告和错误，并会有可作的指导以优化行程配置。 这种主动验证帮助你及早发现潜在问题并保持旅程表现。

* **旅程中的** 多个入站动作——为了简化行程编排，你现在可以在单一旅程中定义 <strong>多个入站动作</strong> 。 此前在活动中提供的功能，允许你同时向不同地点发送基于代码的体验、应用内消息、内容卡或网页作，每个作包含特定内容。

  **注意**：此改进此前为有限可用性发布，现已适用于所有环境（正式发布）。

#### 编排的营销活动

* **选择属性并复制分配值** ——你现在可以直接从编排活动中的值分配视图中选择或复制值。

* **受众的数据使用标签继承** - <strong>现在，在协调的营销活动中保存受众时，Adobe Experience Platform中应用的数据使用标签</strong>会自动延续，从而减少手动DULE标记。

* **预定义的重定位过滤器** — 为了支持更轻松地针对编排的营销活动用例进行重定位，此版本引入了新的<strong>重定位过滤器</strong>。 通过这些过滤器，您可以根据消息参与度（例如，已发送、已打开、已打开或已单击，或已打开或已单击或已单击）直接定位受众，并选择要重新定位的特定营销活动或过渡中营销活动。

* **带参数的预定义过滤器** — 您现在可以在编排的营销活动中为可重用、可编辑的规则创建带参数的<strong>过滤器</strong>。

* **发送前的消息确认** — 默认情况下，在发送协调的活动之前，将启用<strong>确认步骤</strong>，以减少意外发送。

* **用户生成的元数据支持** - <strong>executionMetadata帮助程序函数</strong>现在可在编排的营销活动的个性化编辑器中使用，使您能够将上下文信息附加到任何本机操作并将其存储在数据集中以导出到外部系统。

* **重启按钮** ——编排战役现在包含 <strong>重启按钮</strong> ，方便你在发布战役前快速重新启动运行。

* **速率控制支持** ——协调式活动现在支持 <strong>速率控制</strong> ，帮助您控制配送节奏并符合数量限制。

#### 权限

* **阻止自我审批历程和营销活动** — 您现在可以要求创建者无法审批其自己的历程或营销活动，从而改进了审批工作流中的<strong>职责分离</strong>。

## 即将推出 {#jan-26-01-coming-soon}

在接下来的几天内，将计划发布以下功能和增强功能。**信息可能会有所更改**。这些更新在生产环境中启用后，将会共享更新的链接、屏幕和文档。

<table>
<thead>
<tr>
<th><strong>Journey Agent 内的内容生成</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Journey Agent<strong> 由 Adobe Experience Platform Agent Orchestrator 驱动，</strong>可在 Journey Optimizer 中使用，使您能够通过自然语言界面分析旅程。你现在还可以直接在Journey Agent中生成和管理渠道特定内容，为邮件和推送等渠道创建内容，应用和预览模板，通过提示细化语气和风格，并在内容设计师中打开内容进行上下文编辑。</p>
<p>可得日期：2026年2月2日</p>
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
<p>你现在可以通过旅程画布中的专门内容决策活动，在旅程中加入 <strong>个性化优惠</strong> ，并在旅程活动中使用，包括条件和自定义动作。</p>
<p>可得日期：2026年2月2日</p>
</td>
</tr>
</tbody>
</table>
