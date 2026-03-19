---
solution: Journey Optimizer
product: journey optimizer
title: 发行说明
feature: Release Notes
role: User
level: Beginner, Intermediate
description: Adobe Journey Optimizer 发行说明
exl-id: 06fa956a-b500-416e-9d42-b683c328e837
source-git-commit: fb267a12601f728e9c70ec0fd9dbcc7d6190f878
workflow-type: tm+mt
source-wordcount: '3237'
ht-degree: 25%

---

# 发行说明 {#release-notes}

>[!CONTEXTUALHELP]
>id="ajo_homepage_card1"
>title="新增功能"
>abstract="**Adobe Journey Optimizer** 不断地提供新功能、对现有功能的增强和错误修复。会在每月的最后一周将所有更改整合到发行说明中。"

[!DNL Adobe Journey Optimizer] 遵循持续交付模型，允许 Adobe 持续交付新功能、增强功能和修复。此方法支持以可扩展的方式分阶段推出各种功能，以确保所有环境的性能和稳定性。

由于此模型，在每月发行版本之间会更新发行说明。有关发行周期和可用性阶段的完整详细信息，请参阅 [Journey Optimizer 发行周期](releases.md)。

[!DNL Adobe Journey Optimizer] 原生构建于 [!DNL Adobe Experience Platform] 之上并继承了其所具备的最新创新技术和改进。在 [Adobe Experience Platform 发行说明](https://experienceleague.adobe.com/docs/experience-platform/release-notes/latest.html?lang=zh-Hans){target="_blank"}中进一步了解这些更改。

## 2026年3月预发行说明 {#march-26-rn}

**以下预发行说明可能会在正式发行日期之前有所更改，恕不另行通知**。链接、屏幕和更新的文档会于发布日期在发行说明中发布。

另请参阅 [Adobe Experience Platform 预发行说明](https://experienceleague.adobe.com/zh-hans/docs/experience-platform/release-notes/pre-release-notes){target="_blank"}。

**发布日期**：2026 年 3 月 24-25 日

### 新功能 {#march-26-features}

<!--
<table>
<thead>
<tr>
<th><strong>LLM email optimizer</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>You can now optimize your email content for deliverability using large language model (LLM) technology. The LLM email optimizer analyzes your email content and provides actionable recommendations to improve sender reputation, avoid spam filters, and enhance overall deliverability performance.</p>
</td>
</tr>
</tbody>
</table>
-->

<table>
<thead>
<tr>
<th><strong>Journey Agent：创建编排的活动用例</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>由Adobe Experience Platform Agent Orchestrator提供支持的<strong>Journey Agent</strong>现在可以通过自然语言界面创建完整的<strong>协调营销活动</strong>用例。 用纯语言描述您的促销活动目标和要求，Journey Agent将为您配置促销活动结构、活动和定位。</p>
</td>
</tr>
</tbody>
</table>

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
<p>此功能仅面向一部分组织（限量发布）。要获得访问权限，请与 Adobe 代表联系。</p>
<p>有关更多信息，请参阅<a href="https://experienceleague.adobe.com/docs/experience-cloud-ai/experience-cloud-ai/agents/ajo-agent.html?lang=zh-Hans">详细文档</a>。</p>
<p>发布日期：2026年3月4日</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>历程仲裁 — AI模型</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>您现在可以在排名公式中使用AI模型，根据客户用户档案属性和上下文因素自动提升历程优先级分数，确保客户进入最相关的历程。</p>
<p>此功能仅面向一部分组织（限量发布）。要获得访问权限，请与 Adobe 代表联系。</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>编排的活动中的事务型消息</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>编排的营销活动现在支持<strong>事务性消息传递</strong>，使您能够直接在营销活动工作流中触发实时事件驱动型消息，如订单确认、预订通知和帐户更新。</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>使用API触发编排的营销活动</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>您现在可以通过API触发编排的营销活动。 将Target营销活动配置为“由信号触发”并发布。 然后，使用API调用来触发营销活动。 API调用可以包含将在触发的营销活动中作为变量使用的参数。</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>编排的活动中的增量查询活动</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>新的<strong>增量查询</strong>活动现已在“编排的营销活动”中提供。 此活动仅查询自上次工作流执行以来的新记录或更新记录，这显着缩短了处理时间，提高了针对大型数据集的重复营销活动的效率。</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>在编排的营销活动中测试活动</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>新的<strong>Test</strong>活动现在可在编排的营销活动中使用。 此活动根据定义的条件将工作流执行路由到不同的分支，让您能够在激活实时投放之前验证活动逻辑和配置。</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>URL参数加密</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>现在，可对跟踪链接和登陆页面中的URL参数进行加密，从而为敏感参数数据提供额外的安全层。</p>
<ul>
<li>在专用<strong>管理</strong>注册表中注册和管理加密密钥。</li>
<li>在表达式中使用新的加密帮助程序来加密跟踪链接和登陆页URL中的敏感数据，以便您在渲染时保护查询参数。</li>
</ul>
<p>此功能仅面向一部分组织（限量发布）。要获得访问权限，请与 Adobe 代表联系。</p>
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
<p>使用新的优化节点以特定受众为目标或运行A/B测试，以确定满足以业务为中心的KPI的最佳途径。
通过此工具，您可以测试、更改并自定义通信、顺序和时间，以便更好地联系客户。
</p>
<p>此功能以前以“有限可用性”发布，现在可用于所有环境（一般可用性）。 <a href="../building-journeys/optimize.md">了解详情</a></p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>历程中的数据集查找支持</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>历程中的新活动“数据集查找”允许您在运行时从Adobe Experience Platform记录数据集动态检索数据。 通过利用此功能，您可以访问可能不存在于轮廓或事件负载中的数据，从而确保客户交互既相关又及时。此功能以前以“有限可用性”发布，现在可用于所有环境（一般可用性）。 有关更多信息，请参阅<a href="../building-journeys/dataset-lookup.md">详细文档</a>。</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>已弃用本机渠道操作活动</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>在2026年2月<strong>操作活动</strong>正式发布后，历程画布中的旧版本机渠道活动（电子邮件、推送、短信、应用程序内、Web、基于代码的体验和内容卡）现已弃用。</p>
<p>您现在使用单个<strong>操作活动</strong>来配置所有渠道操作，而不需要单独的特定于渠道的节点。</p>
使用旧版渠道活动的现有历程将继续正常运行，无需进行任何更改或迁移。
<p>有关更多信息，请参阅<a href="../building-journeys/journey-action.md">详细文档</a>。</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>电子邮件渠道中的决策支持</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>您现在可以使用<strong>Decisioning</strong>来个性化和优化电子邮件的内容。 利用优先级得分、公式或AI模型，向每位收件人显示最相关的选件和内容。</p>
<p>此功能以前以“有限可用性”发布，现在可用于所有环境（一般可用性）。 在此General Availability版本中，现在支持镜像页面。</p>
<p>有关更多信息，请参阅<a href="../experience-decisioning/create-decision-policy.md">详细文档</a>。</p>
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
<p><img src="assets/do-not-localize/ai-model-observability.gif"/></p>
<p>有关更多信息，请参阅<a href="../experience-decisioning/ranking/ai-model-observability.md">详细文档</a>。</p>
<p>发布日期： 2026年3月9日</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>登陆页面中的自定义表单</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>您现在可以在登陆页面中创建<strong>自定义表单</strong>，以收集标准选择加入字段之外的特定订阅者数据。 定义您自己的表单字段、验证规则和提交行为，以支持更广泛的订阅和配置文件扩充用例。</p>
<p>此功能以前以“有限可用性”发布，现在可用于所有环境（一般可用性）。 <a href="../landing-pages/lp-forms.md">了解详情</a></p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>消息收件箱</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Adobe Journey Optimizer现在提供新的<strong>消息收件箱</strong>，可集中查看已接收的应用程序内消息、推送消息和短信消息。 收件人可以在一个位置访问其所有消息并与之交互，从而实现更丰富的参与和重新参与情景。</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>将图像转换为电子邮件内容模板</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>您现在可以直接在Journey Optimizer中将图像转换为电子邮件内容模板。 使用AI支持的分析，从可视化引用自动生成结构化HTML模板，显着缩短电子邮件设计时间。</p>
<p>此功能以前以“有限可用性”发布，现在可用于所有环境（一般可用性）。 <a href="../content-management/image-to-html.md">了解详情</a></p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>电子邮件模板的高级HTML编辑器</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>电子邮件内容模板的高级HTML模式允许您在Email Designer中编辑内容的HTML源，在源中添加高级表达式（如条件），并在HTML视图和桌面视图之间切换，而不会丢失所做的更改。</p>
<p>此功能仅在电子邮件渠道的内容模板中可用。 它当前处于“有限可用”状态 — 请联系您的Adobe代表以获取访问权限。</p>
<p><img src="assets/do-not-localize/expert-mode.gif"/></p>
<p>有关更多信息，请参阅<a href="../content-management/email-template-expert-mode.md">详细文档</a>。</p>
<p>发布日期： 2026年3月10日</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>自定义Firefly模型与第三方图像生成模型的集成</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>实现标准和自定义Firefly模型与经批准的第三方图像模型的无缝集成，以在生成图像时提供更大的灵活性、控制力以及品牌一致性。</p>
<p>根据您的需求选择合适的模型：</p>
<ul><li> <strong>Adobe模型</strong>（由Firefly Image Model 4提供支持），无需其他设置即可立即生成图像</li><li> <strong>合作伙伴型号</strong> （由Gemini 2.5 Flash提供支持）提供专业功能</li><li><strong>自定义模型</strong>（基于您自己的资产进行培训的品牌特定模型），用于生成与您的品牌标识、风格和视觉准则完全一致的品牌。</li></ul>
<p>有关更多信息，请参阅<a href="../content-management/generative-models.md">详细文档</a>。</p>
<p>发布日期：2026年3月2日</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>iOS的实时活动</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>利用Adobe Journey Optimizer中的iOS实时活动，直接将实时体验引入客户的“锁定Screens”和“动态岛”中。 交付实时更新，从订单跟踪和航班状态到事件倒计时、实时得分和交付进度，而不要求用户打开您的应用程序。 让您的受众了解情况，并在正确的时间参与活动，即他们所在的位置。</p>
<p>此功能以前以测试版的形式发布，但现在向所有环境提供（正式发布）。</p>
<p>有关更多信息，请参阅<a href="../mobile-live/get-started-mobile-live.md">详细文档</a>。</p>
<p>发布日期：2026年3月3日</p>
</td>
</tr>
</tbody>
</table>

### 改进 {#march-26-improv}

此版本包含的改进如下所述。

#### 历程

* **历程中的出站消息波动发送** — 您现在可以计划来自Journey Optimizer历程的消息，以受控批次形式随时间传递。 [了解详情](../building-journeys/send-using-waves.md)

  此功能以前以“有限可用性”发布，以供在历程中使用，但现在对所有环境可用（一般可用性）。

  发布日期： 2026年3月16日

* **历程技术详细信息中的暂停和恢复详细信息** — 历程&#x200B;**技术详细信息**&#x200B;现在包含其他暂停和恢复信息：上次暂停和恢复的日期和时间、执行每个操作的用户的显示名称和内部标识符以及暂停行为、最长暂停持续时间和自动恢复状态等整套暂停历程设置。 [了解详情](../building-journeys/journey-properties.md)

  发布日期：2026年3月2日

#### 报告

* **排除电子邮件和短信报告的机器人点击次数** — 电子邮件和短信报告现在会自动从点击量度中过滤掉机器人点击次数，从而提供更准确的参与数据，并防止自动流量夸大您的性能数据。

* **发送时间优化：更新了控件位置和新的提升报告** — 发送时间优化(STO)控件已重新定位到操作配置菜单。 此外，历程报表中现在提供了新的提升报表，以衡量STO对促销活动绩效指标的影响。

#### 电子邮件设计器

* **使用Dynamic Media (Beta)的打开时间个性化** — 您现在可以使用Adobe Dynamic Media资源在打开时间个性化电子邮件内容，支持根据每个收件人在打开电子邮件时的属性动态生成的实时、特定于收件人的图像和视觉效果。 此功能当前位于Beta中。

* **在Unified Shell中显示Email Designer** - Email Designer现在显示在Unified Shell Experience中，提供与其他Adobe应用程序一致的导航和标头体验。

* **片段中的文本模式支持** — 为了支持基于文本的电子邮件工作流，您现在可以创建和管理可视片段的文本版本，以便在包含该片段的纯文本版本的电子邮件中实现最佳使用。

  **警告：**&#x200B;使用在当前版本之前创建的片段时，片段文本版本可能会错误地呈现 — 在Designer电子邮件中和发送给收件人的最终电子邮件中均如此。 为了对较旧的片段获得最佳结果，请编辑、保存并重新发布每个片段。

#### 决策

* **Edge Decisioning中的表达式片段引用更改馈送** — 此增强功能允许片段引用中的更改自动反映在引用片段的所有项目中，而无需手动刷新任何内容（重新发布活动或决策策略）。

* **决策项中的可选片段** — 在决策项中使用片段时，您现在可以将片段设置为可选片段，这样如果某个片段在Edge上暂时不可用，则会跳过该片段，并且历程或营销活动将继续呈现而不是失败。

#### 配置

* **历程和营销活动文件夹** — 您现在可以将历程和营销活动组织到文件夹中，支持结构化导航，使处理大量内容的团队更易于管理。 此功能仅面向一部分组织（限量发布）。要获得访问权限，请与 Adobe 代表联系。

* **AJO次要收件人反馈事件数据集重命名** - `AJO Email BCC Feedback Event`数据集已重命名为`AJO Secondary Recipient Feedback Event`数据集。 具体影响取决于您的情况：

   * **现有用户**：只更新显示名称。 基础表名称保持不变。
   * **新用户和沙盒**：显示名称和表名称都反映新名称。
   * **具有新沙盒的现有用户**：显示名称和表名称都已更新为新名称。

  发布日期：2026年3月2日

#### 编排的营销活动

* **协调的营销活动中的全局变量** — 协调的营销活动现在支持全局变量，这些变量可以定义一次，并在工作流内的所有活动中重复使用，从而简化配置并确保动态值、表达式和内容个性化的一致性。

* **在编排的营销活动中实现目标维度简化** — 您现在可以轻松地选择或自动推导编排的营销活动中的正确定向和次要维度，以实现准确、高效的受众激活。

## 2026年2月发行说明 {#feb-26-01-rn}

[新功能](#feb-26-01-features)和[改进](#feb-26-01-improv)部分涵盖的功能已经可用。<!--The [Coming soon](#coming-soon) section lists features and improvements scheduled for release later in February.-->

<!--**The pre-release notes below are subject to change without prior notice until the release availability date**. Links, screens and updated documentation are published in the release notes, at the release date.

See also [Adobe Experience Platform Pre-release notes](https://experienceleague.adobe.com/zh-hans/docs/experience-platform/release-notes/pre-release-notes){target="_blank"}.-->

<!--**Release date**: February 17-18, 2026-->

### 新功能 {#feb-26-01-features}


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
<p><img src="assets/do-not-localize/journey-arbitration-formulas.gif"/></p>
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

#### 决策

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

<!--## Coming soon {#coming-soon}

The features and improvements below are planned for release later in February. Release dates and scope may change without prior notice.

### Improvements {#coming-soon-improv}

* **Decisioning preview in Code-based Experience channel** - You can now preview decision items when configuring Decisioning with the Code-based Experience channel. Preview is available directly in the authoring interface before going live.

  Availability date: February 18, 2026
-->

