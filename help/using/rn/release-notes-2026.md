---
solution: Journey Optimizer
product: journey optimizer
title: 发行说明2026
description: Journey Optimizer 2026版发行说明
feature: Release Notes
topic: Content Management
role: User
level: Beginner, Intermediate
exl-id: 65ca94cf-8e17-4a25-90f3-238083f81477
source-git-commit: 70a9be0c253bbed319510058f7f249f5919bf7b8
workflow-type: tm+mt
source-wordcount: '4254'
ht-degree: 45%

---

# 2026年版发行说明 {#release-notes-2026}

本页列出了于2026年发布的[!DNL Journey Optimizer]的所有功能和改进。

## 2026年3月发行说明 {#march-26-rn}

[新功能](#march-26-features)和[改进](#march-26-improv)部分涵盖的功能已经可用。<!--The [Coming soon](#coming-soon) section lists features and improvements scheduled for release later in March.-->

<!--
**The pre-release notes below are subject to change without prior notice until the release availability date**. Links, screens and updated documentation are published in the release notes, at the release date.

See also [Adobe Experience Platform pre-release notes](https://experienceleague.adobe.com/en/docs/experience-platform/release-notes/pre-release-notes){target="_blank"}.
-->

**发行日期**： 2026年3月24日至25日

### 新功能 {#march-26-features}

<table>
<thead>
<tr>
<th><strong>URL参数加密</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>现在，可以加密添加到电子邮件中的跟踪和登陆页面链接中的URL参数，从而为敏感参数数据提供额外的安全层。</p>
<ul>
<li>在专用<strong>管理</strong>注册表中注册和管理加密密钥。</li>
<li>在表达式中使用新的“Encrypt”帮助程序函数加密URL中要在渲染时保护的查询参数的敏感数据。</li>
</ul>
<p>此功能仅面向一部分组织（限量发布）。 要获得访问权限，请与 Adobe 代表联系。</p>
<p><img src="assets/do-not-localize/encrypt-helper.gif"></p>
<p>有关更多信息，请参阅<a href="../personalization/url-parameter-encryption.md">详细文档</a>。</p>
<p>发布日期：2026年3月31日</p>
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
<p>此功能此前为有限发布版，现已可供所有环境使用（正式发布版）。</p>
<p><img src="assets/do-not-localize/image-converter.gif"></p>
<p>有关更多信息，请参阅<a href="../content-management/image-to-html.md">详细文档</a>。</p>
<p>发布日期：2026年3月31日</p>
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
<p>使用[!DNL Journey Optimizer]，您可以通过登陆页面捕获配置文件属性。</p>
<p>根据特定的数据集，创建、设计和管理适合您需求的自定义表单。 然后，您可以在登陆页面中利用这些表单，将您选择的轮廓属性添加到为每个表单定义的数据集中。</p>
<p>此功能以前以“有限可用”的形式面向美国和澳大利亚的客户发布，现在则对所有环境均可用（一般可用）。</p>
<p><img src="assets/do-not-localize/forms.gif"/></p>
<p>有关更多信息，请参阅<a href="../landing-pages/lp-forms.md">详细文档</a>。</p>
<p>发布日期：2026年3月26日。</p>
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
<p><img src="../orchestrated/assets/test-1.png"></p>
<p>有关更多信息，请参阅<a href="../orchestrated/activities/test.md">详细文档</a>。</p>
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
<p>历程中新增的<strong>数据集查找</strong>活动允许您在运行时动态检索Adobe Experience Platform记录数据集中的数据 — 让您能够访问不属于配置文件或事件有效负载的信息，因此客户交互始终相关且及时。</p>
<p>以前以“有限可用性”发布给一组有限组织，现在历程中的数据集查找活动可供所有有权使用[数据集查找](../data/lookup-aep-data.md)的客户使用，同时仍保持有限可用性。</p>
<p><img src="../building-journeys/assets/aep-data-activity.png"></p>
<p>有关更多信息，请参阅<a href="../building-journeys/dataset-lookup.md">详细文档</a>。</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>操作活动取代了特定于渠道的历程活动</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>在2026年2月<strong>操作活动</strong>正式发布后，历程画布中的旧版本机渠道活动（电子邮件、推送、短信、应用程序内、Web、基于代码的体验和内容卡）现已弃用。</p>
<p>现在，您必须使用单个操作活动来配置所有渠道操作，而无需单独的特定于渠道的节点。</p>
<p>使用旧版渠道活动的现有历程可以继续正常运行，无需进行任何更改或迁移。</p>
<p><img src="assets/do-not-localize/action-activity.gif"></p>
<p>有关更多信息，请参阅<a href="../building-journeys/journey-action.md">详细文档</a>。</p>
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
<p>有关更多信息，请参阅<a href="../email/email-expert-mode.md">详细文档</a>。</p>
<p>发布日期： 2026年3月10日</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>自定义 Firefly 模型与第三方图像生成模型的集成</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>启用标准和自定义 Firefly 模型以及经过批准的第三方图像模型的无缝集成，从而在生成图像时提供更大的灵活性、控制力以及品牌一致性。</p>
<p>根据您的需求选择合适的模型：</p>
<ul><li> <strong>Adobe 模型</strong>（基于 Firefly Image Model 4），无需额外设置即可即时生成图像</li><li> <strong>合作伙伴模型</strong>（基于 Gemini 2.5 Flash），专为特定功能而设计</li><li><strong>自定义模型</strong>（基于您自有资产训练的特定品牌模型），可生成完全符合您的品牌形象、风格和视觉指南的内容。</li></ul>
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
<p>通过Adobe Journey Optimizer中的<strong>iOS Live Activity</strong>，将实时体验直接引入客户的Lock Screens和Dynamic Island。 交付实时更新，从订单跟踪和航班状态到事件倒计时、实时得分和交付进度，而不要求用户打开您的应用程序。 让您的受众了解情况，并在正确的时间参与活动，即他们所在的位置。</p>
<p>此功能以前以测试版的形式发布，但现在向所有环境提供（正式发布）。</p>
<p>有关更多信息，请参阅<a href="../mobile-live/get-started-mobile-live.md">详细文档</a>。</p>
<p>发布日期：2026年3月3日</p>
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
<p>此功能仅面向一部分组织（限量发布）。 要获得访问权限，请与 Adobe 代表联系。</p>
<p>有关更多信息，请参阅<a href="https://experienceleague.adobe.com/docs/experience-cloud-ai/experience-cloud-ai/agents/ajo-agent.html" target="_blank">详细文档</a>。</p>
<p>发布日期：2026年3月4日</p>
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
<th><strong>使用信号触发编排的营销活动</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>现在可以通过<strong>API信号</strong>触发编排的营销活动。 若要进行此设置，请将目标营销活动配置为<strong>由信号</strong>触发，发布该营销活动，然后使用API调用触发它。 API调用中包含的任何参数均可用作正在运行的营销活动中的变量。 请注意，信号触发的编排营销活动仍是<strong>批次</strong>营销活动，不同于API触发的营销活动。</p>
<p><img src="assets/do-not-localize/oc-triggered.gif"></p>
<p>有关更多信息，请参阅<a href="../orchestrated/trigger-orchestrated-campaign.md">详细文档</a>。</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>编排的活动中的事务性类别</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>在编排的营销活动中，您现在可以将渠道活动设置为<strong>事务性</strong>类别。 这会将事务性渠道配置应用于该活动，并在业务规则不应应用或不需要客户选择加入时非常有用。</p>
<p><img src="assets/do-not-localize/oc-transactional.gif"></p>
<p>有关更多信息，请参阅<a href="../orchestrated/activities/channels.md#add">详细文档</a>。</p>
<p>此功能将在未来几天内逐步推广到所有地区。</p>
</td>
</tr>
</tbody>
</table>

### 改进 {#march-26-improv}

此版本包含的改进如下所述。

#### 个性化

* **完整/基本URL个性化** — 您可以使用配置文件属性（例如，针对域或路径）个性化目标URL。 要启用此功能，请向Adobe提供您的接受域列表。 [了解详情](../personalization/personalization-build-expressions.md#where)

  此功能以前以“有限可用性”发布，以供在历程中使用，但现在对所有环境可用（一般可用性）。

  发布日期：2026年4月1日

#### 报告

* **发送时间优化：更新了控件位置和新的提升报告** — 发送时间优化(STO)控件已重新定位到操作配置菜单。 此外，历程报表中现在提供了新的提升报表，以衡量STO对促销活动绩效指标的影响。 [了解详情](../reports/channel-report-cja.md#optimization-models)

  发布日期： 2026年3月27日

<!--
* **Exclude bot clicks for email and SMS reporting** - Email and SMS reporting now automatically filters out bot clicks from click metrics, providing more accurate engagement data and preventing automated traffic from inflating your performance figures.

#### Email Designer

* **Email Designer displayed in Unified Shell** - The Email Designer is now displayed within the Unified Shell experience, providing a consistent navigation and header experience that aligns with other Adobe applications.

* **Text mode support in fragments** - To support text-based email workflows, you can now create and manage text versions of your visual fragments for optimal use in the plain text version of emails that include that fragment.

  **Caution:** When using a fragment that was created before the current release, the fragment text version may be incorrectly rendered—both in the Email Designer and in the final email delivered to your recipients. For best results with older fragments, edit, save and republish each fragment.
-->

#### 配置

<!--* **Folders for journeys and campaigns** - You can now organize your journeys and campaigns into folders, enabling structured navigation and easier management for teams working with large volumes of content. This capability is only available for a set of organizations (Limited Availability). To gain access, contact your Adobe representative.-->

* **AJO域证书续订失败** — 现在，当用于电子邮件传递的域证书即将到期或已过期时，您可以通过电子邮件或在Journey Optimizer通知中心订阅接收系统警报。 [了解详情](../reports/alerts.md#alert-certificates-renewal-unsuccessful)

  发布日期： 2026年3月26日

* **AJO次要收件人反馈事件数据集重命名** - `AJO Email BCC Feedback Event`数据集已重命名为`AJO Secondary Recipient Feedback Event`数据集。 具体影响取决于您的情况：

   * **现有用户**：只更新显示名称。 基础表名称保持不变。
   * **新用户和沙盒**：显示名称和表名称都反映新名称。
   * **具有新沙盒的现有用户**：显示名称和表名称都已更新为新名称。

  >[!NOTE]
  >
  >新数据集立即显示新名称。 对于较旧的数据集名称，回填和对帐会逐步进行，并且可能需要几周才能完成。

  发布日期：2026年3月2日


#### 历程

* **更新配置文件操作：支持多个配置文件属性** - **更新配置文件**&#x200B;操作活动现在支持在单个节点中更新最多五个配置文件属性。 以前，每个操作一次只能更新一个属性，需要多个节点更新多个属性。 使用新的&#x200B;**更新其他字段**&#x200B;按钮添加其他字段/值对，从而降低画布复杂性并提高性能。 [了解详情](../building-journeys/update-profiles.md)

* **历程中的出站消息波动发送** — 您现在可以计划来自Journey Optimizer历程的消息，以受控批次形式随时间传递。 [了解详情](../building-journeys/send-using-waves.md)

  此功能以前以“有限可用性”发布，以供在历程中使用，但现在对所有环境可用（一般可用性）。

  发布日期： 2026年3月16日

* **历程技术详细信息中的暂停和恢复详细信息** — 历程&#x200B;**技术详细信息**&#x200B;现在包含其他暂停和恢复信息：上次暂停和恢复的日期和时间、执行每个操作的用户的显示名称和内部标识符以及暂停行为、最长暂停持续时间和自动恢复状态等整套暂停历程设置。 [了解详情](../building-journeys/journey-properties.md)

  发布日期：2026年3月2日

#### 决策

* **决策迁移 — 选件和上下文属性** — 迁移API实体映射现在列出了&#x200B;**选件属性** （`migratedofferattributes`个性化选件项架构）和&#x200B;**上下文属性** （`migratedcontextattributes`迁移数据集架构）。 [了解详情](../experience-decisioning/decisioning-migration-api.md#entity-mapping)

  发布日期：2026年3月31日

<!--
## Coming soon {#coming-soon}

The features and improvements below are planned for release later in March/early April. Release dates and scope are **subject to change without prior notice**.


WAITING RELEASE DATE CONFIRMATION * **Target dimension simplification in Orchestrated Campaigns** - The active targeting dimension is now shown on the workflow canvas, so you can see which dimension is used by a channel activity. The multi-entity segmentation flow is simpler as you no longer need a separate "Change dimension" activity. Moreover, you can now choose explicitly whether messages are sent at the profile level or at a secondary dimension level.


WAITING RELEASE DATE CONFIRMATION
* **Target dimension simplification in Orchestrated Campaigns** - The active targeting dimension is now shown on the workflow canvas, so you can see which dimension is used by a channel activity. The multi-entity segmentation flow is simpler as you no longer need a separate "Change dimension" activity. Moreover, you can now choose explicitly whether messages are sent at the profile level or at a secondary dimension level.
-->


## 2026年2月发行说明 {#feb-26-01-rn}

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
<p>此功能仅面向一部分组织（限量发布）。 要获得访问权限，请与 Adobe 代表联系。</p>
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
<p>此功能仅面向一部分组织（限量发布）。 要获得访问权限，请与 Adobe 代表联系。</p>
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
<p>Adobe Journey Optimizer现在支持<strong>Web推送通知</strong>，从而将推送渠道扩展到移动以外。 您可以无缝地向<strong>移动设备浏览器和桌面设备浏览器</strong>发送通知，使您无需依赖应用程序即可通过客户的设备直接与其联系。 通过此增强功能，您可以利用与移动设备推送相同的创作工作流和定位功能，实时向用户发送及时的个性化消息与其互动。</p>
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

  此功能仅面向一部分组织（限量发布）。 要获得访问权限，请与 Adobe 代表联系。

* **基于代码的体验渠道中的决策预览** — 现在，在使用基于代码的体验渠道配置决策时，您可以预览决策项目。 上线之前，可以直接在创作界面中预览。 [了解详情](../code-based/test-code-based.md#preview-code-based)

  发布日期： 2026年2月18日

<!--
THIS WAS FINALLY NOT RELEASED IN FEBRUARY

* **Attach fragments to decision items** - Journey Optimizer now provides the ability to attach fragments to decision items which can be leveraged in code-based experience campaigns through decision policies. [Read more](../experience-decisioning/fragments-decision-policies.md)

  Previously released in Limited Availability, this capability is now available to all environments (General Availability).

  Availability date: February 12, 2026.
-->

#### 个性化

* **执行元数据帮助程序** - `executionMetadata`帮助程序函数现在可供所有Journey Optimizer客户使用。 使用它可以动态地将上下文信息附加到任何本机操作，并将其捕获到数据集中以导出到外部系统。 [了解详情](../personalization/functions/helpers.md#execution-metadata)

  此功能此前为有限发布版，现已可供所有环境使用（正式发布版）。

  发布日期：2026年2月20日。

#### 短信

* **短信Webhook** — 现在，所有短信提供商都支持Webhook。 您可以基于其预期目的配置每个webhook：入站webhook ，以捕获传入消息；反馈webhook，以接收投放接收、状态更新和其他消息相关事件。 [了解详情](../sms/sms-webhook.md)

  发布日期：2026年2月2日。



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
<p>包含推送通知的Experience Decisioning需要特定版本的Mobile SDK。 在实施此功能之前，请查看<a href="https://developer.adobe.com/client-sdks/home/release-notes" target="_blank">发行说明</a>以确定所需的版本，并确保您已相应地升级。 您还可以在<a href="https://developer.adobe.com/client-sdks/home/current-sdk-versions" target="_blank">此部分</a>中查看您的平台的所有可用SDK版本。</p>
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
<p>利用<strong>免打扰时间</strong>，您可以针对电子邮件、短信、推送和 WhatsApp 渠道定义基于时间的排除项。 这可确保在特定时间段内不发送任何消息，从而帮助您尊重客户偏好并满足合规性要求。 您可以通过<strong>规则集</strong>应用免打扰时间并分配给营销活动或历程中的单个操作，以实现精确控制。</p>
<p>此功能之前为限量发布版，现在可供所有环境使用。 随着该正式发布版的发布，该功能现在能够让客户对营销活动操作进行排队，直到免打扰时间结束，以及能够预览已激活的免打扰时间规则。</p>
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
<p>此功能适用于已购买消息导出附加组件产品的组织，且仅限于电子邮件和短信渠道。 有关更多信息，请与您的 Adobe 代表联系。</p>
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
<p>编排的营销活动中现已推出直邮渠道。 <strong>直邮活动</strong>有助于在编排的营销活动中以直邮方式发送消息，支持一次性发送和定期发送。 它用于自动生成直邮服务提供商所需的<strong>提取文件</strong>，从而实现直邮流程的自动化。 您可以在编排的营销活动画布中组合各类渠道活动，构建跨渠道营销活动，以根据客户行为和数据触发相应操作。</p>
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
<p>有关更多信息，请参阅<a href="https://developer.adobe.com/journey-optimizer-apis/references/campaigns-retrieve" target="_blank">详细文档</a>。</p>
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
<p>此功能之前以 Beta 发布，现在可供一部分组织使用（有限发布）。 要获得访问权限，请与 Adobe 代表联系。</p>
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

* **将原生和 Adobe Campaign 消息操作结合使用** – Journey Optimizer 现在允许您在同一历程中将 <strong>Adobe Campaign v7/v8</strong> 消息操作与<strong>原生渠道操作</strong>结合使用。 [了解详情](../building-journeys/using-adobe-campaign-v7-v8.md)

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

* **使用轮廓时区安排营销活动** – 营销活动安排现在可根据每个轮廓的<strong>时区</strong>进行，从而在预定的当地时间投放消息。 [了解详情](../campaigns/campaign-schedule.md)

  **注意**：此改进仅适用于一组组织（限量发布）。

  可用日期：2026年1月27日。

#### 权限

* **阻止自行审批历程和营销活动** - 创建或设置<strong>审批策略</strong>时添加了一个选项，用于阻止历程或营销活动创建者<strong>审批他们自己的对象</strong>。 [了解详情](../test-approve/approval-policies.md)

  可用日期：2026年1月27日。
