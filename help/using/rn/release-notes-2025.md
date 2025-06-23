---
solution: Journey Optimizer
product: journey optimizer
title: 2025 年版发行说明
description: Journey Optimizer 2025 年发行说明
feature: Release Notes
topic: Content Management
role: User
level: Beginner, Intermediate
exl-id: aa8c74de-748b-4947-a972-14703f6ab4a7
source-git-commit: 024356ca30728611d1d32ba72172711e4714b64c
workflow-type: tm+mt
source-wordcount: '3117'
ht-degree: 100%

---

# 2025 年版发行说明 {#release-notes-2025}

本页列出了于 2025 年发布的 [!DNL Journey Optimizer] 功能和改进。


## 2025 年 5 月发行说明 {#25-5-rn}

<!--**Release date**: May 20-21, 2025-->

### 新功能 {#25-05-features}

此版本包含的新功能详述如下。

<table>
<thead>
<tr>
<th><strong>营销活动和历程库的日程表视图</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>现在，历程和营销活动列表中提供日程表视图。该视图可让您在相应列表中查看所有历程和营销活动激活情况。</p>
<p>目前，此更改仅面向一部分组织提供（限量发布版）。要申请访问权限，请使用<a href="https://forms.cloud.microsoft/r/FC49afuJVi" target="_blank">此表单</a>。</p>
<img src="assets/do-not-localize/calendar.gif">
<p>有关更多信息，请参阅以下部分：<a href="../building-journeys/journey-ui.md">浏览和筛选历程</a>、<a href="../campaigns/modify-stop-campaign.md">访问营销活动</a>。</p>
<p>发布日期：2025 年 5 月 28 日</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Adobe Experience Manager 内容片段集成</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>通过将 Adobe Experience Manager 与 Adobe Journey Optimizer 集成，您现在可以轻松地在 Journey Optimizer 内容中使用 Adobe Experience Manager 内容片段。通过这种无缝连接，可以更加轻松地直接在 Journey Optimizer 中访问和使用 AEM 内容。</p>
<p>此功能之前仅供部分组织使用 (LA)，现在已正式发布并提供以下增强功能：您现在可以使用编辑器模式定义占位符并在片段签名中映射个性化值。</p>
<ul>
<!--li>Create offers by directly selecting an AEM Content Fragment.</li>
<li>Define placeholders and map personalization values within the fragment signature using the Editor mode.</li-->
</ul>
</br>
<img src="assets/do-not-localize/content-fragment.gif">
<p>有关更多信息，请参阅<a href="../integrations/aem-fragments.md">详细文档</a>。</p>
<p>发布日期：2025 年 5 月 23 日</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Adobe Experience Manager Dynamic Media 集成</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Dynamic Media 资源现可直接在 Journey Optimizer 中使用和访问。通过此集成，您可以：</p>
<ul>
<li>通过实时更新集中管理资源。</li>
<li>即时修改宽度和高度等资源设置。</li>
<li>通过更新内容和添加个性化字段自定义 Dynamic Media 模板。</li>
</ul>
</br>
<img src="assets/do-not-localize/dynamic_media_template_html.gif">
<p>此功能之前为限量发布，现在可用于所有环境（正式发布）。</p>
<p>有关更多信息，请参阅<a href="../integrations/aem-dynamic.md">详细文档</a>。</p>
<p>发布日期：2025 年 5 月 23 日</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>触发事件的历程的补充 ID</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>您现在可以通过用户档案 ID 以及其他标识符（如订单 ID、订阅 ID 或计划 ID）触发历程，使同一轮廓同时多次出现在同一历程中。这支持同时管理多个订单或订阅等场景，每个实例在整个历程中都遵循各自的路径。</p>
<p>有关更多信息，请参阅<a href="../building-journeys/supplemental-identifier.md">详细文档</a>。</p>
<p>此功能仅面向一部分组织（限量发布）。要获得访问权限，请与 Adobe 代表联系。</p>
<p>发布日期：2025 年 5 月 23 日</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>模拟内容变体</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<!--p>Previously available in beta, content variations simulation is now generally available (GA). It allows you to preview different variations of your content using sample input data uploaded from a CSV or JSON file or added manually. All the attributes used in your content for personalization are automatically detected by the system and can be used for your tests to create multiple variants.</p-->
<p>此功能之前为限量发布，现在可用于所有环境。在此正式发布版中，该功能现在支持多语言内容和内容试验，使您能够测试不同语言和处理方法的变体。此外，它现在支持上下文属性（以及轮廓属性），从而允许进行更加动态和情境化的内容测试。</p>
<img src="assets/do-not-localize/variants.gif">
<p>有关更多信息，请参阅<a href="../test-approve/simulate-sample-input.md">详细文档</a>。</p>
<p>发布日期：2025 年 5 月 23 日</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>将读取受众计划与批量分段作业同步</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>您现在可以在批量分段完成后触发每日历程运行。现在，所有客户都可以在每日计划的历程中使用此选项。该选项可让您定义最长 6 小时的时间范围，以等待批量分段作业中的受众数据，确保使用最新数据运行历程或者在未准备就绪时跳过历程。</p>
<p>此功能之前为限量发布，现在可用于所有环境（正式发布）。</p>
<img src="assets/do-not-localize/trigger-journeys.gif">
<p>有关更多信息，请参阅<a href="../building-journeys/read-audience.md#schedule">详细文档</a>。</p>
<p>发布日期：2025 年 5 月 20 日</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>自定义短信提供商</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Journey Optimizer 现在允许您配置其他短信服务提供商，而不限于 Sinch、Infobip 和 Twilio 等默认选项。通过自定义短信服务提供商配置，您可以直接集成第三方提供商，利用高级负载自定义进行动态消息传递，并管理同意首选项（选择加入/选择退出）以确保合规性。</p>
<p>有关更多信息，请参阅<a href="../sms/sms-configuration-custom.md">详细文档</a>。</p>
<p>此功能之前为限量发布，现在可用于所有环境（正式发布）。</p>
<p>发布日期：2025 年 5 月 20 日</p>
</td>
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
<p>您现在可以快速应用预批准的主题，以确保在所有电子邮件中实现品牌一致性、加快营销活动创建流程，并独立生成高质量电子邮件，同时减少对设计团队的依赖。</p>
<p>此功能目前为 Beta 版，仅供 Beta 版客户使用。要加入 Beta 版计划，请联系 Adobe 代表。</p>
<img src="assets/do-not-localize/themes.gif">
<p>有关更多信息，请参阅<a href="../email/apply-email-themes.md">详细文档</a>。</p>
<p>发布日期：2025 年 5 月 14 日</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>决策 - 新的 AI 公式生成器</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>您现在可以在新改进的界面中定义和组合标准，从而创建特定的决策排名公式。您可以通过引导式界面自定义排名公式，将 AI 模型分数、产品建议优先级、轮廓属性、产品建议属性和上下文信号组合起来，而不是仅依赖静态产品建议优先级。</p>
<img src="assets/do-not-localize/formula-builder.gif">
<p>有关更多信息，请参阅<a href="../experience-decisioning/exd-ranking-formulas.md">详细文档</a>。</p>
<p>发布日期：2025 年 5 月 14 日</p>
</td>
</tr>
</tbody>
</table>

### 改进 {#25-05-improv}

此版本包含的改进如下所述。


* **沙盒副本支持新 Campaign 对象** - 发布日期：2025 年 5 月 15 日

  使用资源包导出和导入功能跨多个沙盒复制营销活动时，现在还会复制以下依赖项：渠道配置、试验变体和设置、决策策略和项目。[了解详情](../configuration/copy-objects-to-sandbox.md)

* **登陆页的文件夹** - 发布日期：2025 年 5 月 9 日

  为轻松地管理登陆页，您现在可以使用文件夹将其更高效地组织为结构化层级。[了解详情](../landing-pages/manage-lp.md)

* **直邮：SFTP 连接支持 SSH 密钥** - 发布日期：2025 年 5 月 5 日

  在直邮文件路由配置中，除了使用密码身份验证类型的现有 SFTP 之外，您现在还可以将直邮文件导出到使用 SSH 密钥身份验证的 SFTP 服务器。[了解详情](../direct-mail/direct-mail-configuration.md)

* **激活“药丸”以用于个性化操作** - 发布日期：2025 年 5 月 5 日

  个性化编辑器中新增了一个“药丸”按钮。启用后，配置文件和上下文属性将显示为“药丸”，从而提高代码的可读性。[了解详情](../personalization/personalization-build-expressions.md#options)

  >[!AVAILABILITY]
  >
  >该功能将在接下来的 30 天内逐步推广到所有环境。

* **Web 渠道中支持“重定向到 URL”**- 发布日期：2025 年 5 月 20 日

  现在，您可通过 Journey Optimizer 的 Web 渠道将访客重定向到其他现有 URL，而无需在可视编辑器中创作新的变体。此功能适用于运行试验来比较两个完全不同的页面，而不是只更改页面中的几个元素。[了解详情](../web/create-web.md#web-redirect-to-url)

* **模板和片段的文件夹** - 发布日期：2025 年 5 月 20 日

  通过文件夹，您可以更轻松、更高效地将对象组织为结构化层级。文件夹以前面向一部分组织提供 (LA)，现在面向所有用户提供 (GA)，以便管理其内容模板和片段。要了解更多信息，请参阅[内容模板](../content-management/access-content-templates.md#folders)和[片段](../content-management/manage-fragments.md#folders)部分。

* **电子邮件模板中的点击跟踪** - 发布日期：2025 年 5 月 20 日

  现在，[!DNL Journey Optimizer] 原生支持电子邮件内容中图像映射的 `<area>` 元素点击跟踪。这是为了确保图像映射区域接收与标准超链接相同的跟踪包、跟踪数据和附加参数。[了解有关消息跟踪的更多信息](../email/message-tracking.md#manage-tracking)

<!--
* **Decisioning - Leverage Adobe Experience Platform datasets** 
  
  Journey Optimizer now allows you to leverage Adobe Experience Platform datasets in the following Decisioning objects: eligibility rules, ranking formulas, and capping rules.-->

* **营销活动列表中的右边栏** - 发布日期：2025 年 5 月 20 日

  现在，在营销活动列表中，选择营销活动会打开显示其详细信息的窗格。

<!--* **Form fields in code-based experience content**

  In content templates, you can now define specific JSON or HTML fields which enable non-technical users to easily edit content in code-based experiences without the need to manipulate code.-->

<!--* **Subdomains - 'Custom delegation' method**  
  In addition to the full delegation and the CNAME method, a new subdomain configuration method is now available: the Custom delegation method, which enables you to fully own controlling and maintaining all aspects of DNS that are required for delivering, rendering, and tracking messages.
  -->



## 2025 年 4 月发行说明 {#25-4-rn}

**发布日期**：2025 年 4 月 29-30 日

### 新功能 {#25-04-features}

此版本包含的新功能如下所列。

<table>
<thead>
<tr>
<th><strong>个性化编辑器 - 通过实践学习</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>个性化游乐场现已可用，您可以在其中试验个性化表达式。它提供了可供选择的示例模板和负载，有助于上手和尝试自己的个性化表达式。</p>
<p>有关更多信息，请参阅<a href="../personalization/personalize.md#playground">详细文档</a>。</p>
<p>发布日期：2025 年 4 月 24 日</p>
<img src="assets/do-not-localize/templating-playground.gif"/>
</td>
</tr>
</tbody>
</table>

<!--table>
<thead>
<tr>
<th><strong>Adobe Experience Manager as a Cloud Service integration</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>The integration between Adobe Journey Optimizer and Adobe Experience Manager as a Cloud Service is now released in General Availability (GA). This integration enables seamless content sourcing and management for personalized customer journeys.</p>
<p>For more information, refer to the <a href="../integrations/aem-templates.md">detailed documentation</a>.</p>
</td>
</tr>
</tbody>
</table-->

<!--<table>
<thead>
<tr>
<th><strong>Simulate content variations (General Availability)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Previously available in beta, content variations simulation is now generally available (GA). It allows you to preview different variations of your content using sample input data uploaded from a CSV or JSON file or added manually. All the attributes used in your content for personalization are automatically detected by the system and can be used for your tests to create multiple variants.</p>
<p>With the General Availability release, the feature now includes support for multilingual content and content experiments, enabling you to test variations across different languages and treatments. Additionally, it now supports contextual attributes (in addition to profile attributes), allowing for even more dynamic and situational content testing.</p>
<img src="assets/do-not-localize/variants.gif">
</td>
</tr>
</tbody>
</table>-->

<table>
<thead>
<tr>
<th><strong>LINE 渠道</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Adobe Journey Optimizer 已扩展其跨渠道功能，包括对 LINE 渠道的支持。通过此增强功能，您可以创建、编辑和预览 LINE 体验，从而实现更加个性化且富有吸引力的交互。借助 LINE，您可以与更多客户建立联系，发送相关内容并提高参与度。</p>
<p>应请求，已为 Adobe Journey Optimizer 客户启用 LINE 渠道。请联系 Adobe 客户关怀部门或 Adobe 代表，为您的组织激活该功能。</p>
<p>有关更多信息，请参阅<a href="../line/get-started-line.md">详细文档</a>。</p></td>
</tr>
</tbody>
</table>


<!--table>
<thead>
<tr>
<th><strong>Custom SMS provider (General Availability)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Adobe Journey Optimizer now supports custom SMS providers, allowing you to integrate your preferred SMS services for enhanced communication flexibility.</p>
<p>For more information, refer to the <a href="../sms/sms-configuration-custom.md">detailed documentation</a>.</p></td>
</tr>
</tbody>
</table-->


<table>
<thead>
<tr>
<th><strong>历程指标</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>通过历程指标，您可以根据业务的各项关键量度衡量活动的影响，更清楚地掌握绩效表现。</p>
</br>
<img src="assets/do-not-localize/success-metric.gif"/>
<p>有关更多信息，请参阅<a href="../building-journeys/success-metrics.md">详细文档</a>。</p>
<p>发布日期：2025 年 4 月 9 日</p>
</td>
</tr>
</tbody>
</table>



<!--<table>
<thead>
<tr>
<th><strong>Calendar view for campaign and journey inventory (Limited Availability)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>A new calendar view is now available for campaigns and journey activations. This feature provides a visual representation of scheduled activities, allowing you to view and manage your campaigns and journeys more effectively. Selecting a calendar item opens a right rail with detailed information. This feature is currently in Limited Availability.</p>
<img src="assets/do-not-localize/calendar.gif">
</td>
</tr>
</tbody>
</table>-->

<table>
<thead>
<tr>
<th><strong>Adobe Express 集成（限量发布版）</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Adobe Journey Optimizer 现在与 Adobe Express 集成在一起，使您能够将创意资产与 Journey Orchestration 无缝连接。此集成简化了跨营销活动设计和部署个性化内容的过程。 </p>
<p>此集成当前不适用于 Healthcare Shield 或 Privacy and Security Shield。</p>
<img src="assets/do-not-localize/express_resize.gif">
<p>有关更多信息，请参阅<a href="../integrations/express.md">详细文档</a>。</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>在批量分段完成后触发每日历程运行（限量发布版）</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>对于每日计划的历程，新增选项可让您定义长达 6 小时的时间范围，以便等待获取批量分段作业中的受众数据，从而确保使用最新数据运行历程或者在未准备就绪时跳过历程。“在批量受众评估后触发”选项仅面向一部分组织提供（限量发布版）。要获得访问权限，请与 Adobe 代表联系。</p>
<p>有关更多信息，请参阅<a href="../building-journeys/read-audience.md#schedule">详细文档</a>。</p>
<img src="assets/do-not-localize/trigger-journeys.gif">
</td>
</tr>
</tbody>
</table>

<!--table>
<thead>
<tr>
<th><strong>Themes in the Email Designer (Beta)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>You can now quickly apply pre-approved styling themes to your email content to ensure brand consistency across all emails, speed up your campaign creation process and independently produce hight-quality emails while reducing dependency on design teams.</p>
<p>This capability is currently in beta version and only available to beta customers. To join the beta program, contact your Adobe representative.</p>
<p>For more information, refer to the <a href="../content-management/brands-score.md">detailed documentation</a>.</p>
<img src="assets/do-not-localize/themes.gif">
<p>Availability date: May 5, 2025</p>
</td>
</tr>
</tbody>
</table-->

<table>
<thead>
<tr>
<th><strong>品牌一致性分数（Beta 版）</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>品牌一致性分数功能可以直接在电子邮件设计器中提供清晰的反馈，帮助您了解内容是否与品牌的基调、风格和准则保持一致。此功能目前作为 Beta 版提供。</p>
<p>有关更多信息，请参阅<a href="../content-management/brands-score.md">详细文档</a>。</p>
<img src="assets/do-not-localize/brand-score.gif">
</td>
</tr>
</tbody>
</table>

<!--
<table>
<thead>
<tr>
<th><strong>Decisioning - New AI formula builder</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>You can now create specific Decisioning ranking formulas by defining and combining criteria from a new improved interface. Ranking formulas allow you to define rules that will determine which decision items should be presented first, rather than taking into account the priority scores.</p>
<p>For more information, refer to the <a href="../content-management/brands-score.md">detailed documentation</a>.</p>
<img src="assets/do-not-localize/formula-builder.gif">
<p>Availability date: May 5, 2025</p>
</td>
</tr>
</tbody>
</table>
-->

### 改进 {#25-04-improv}

**营销活动预览 API**

除了现有的验证发送功能外，还可通过新的 API 预览营销活动。[了解详情](https://developer.adobe.com/journey-optimizer-apis/references/simulations/#operation/createCampaignPreview){target="_blank"}。

**沙盒工具**

* **用于自定义操作的沙盒工具**

  现在，可以使用沙盒工具功能复制的 Adobe Journey Optimizer 对象列表中包含自定义操作，这样有助于简化测试和部署。[了解详情](../configuration/copy-objects-to-sandbox.md)

* **用于营销活动的沙盒工具** - 发布日期：2025 年 4 月 3 日

  您现在可以使用资源包导出和导入功能跨多个沙盒复制营销活动。在复制营销活动时，与轮廓、受众、架构、内联消息和依赖对象相关的所有项目会一并复制。某些项目不会被复制，例如决策项目、数据使用标签和语言设置。[了解详情](../configuration/copy-objects-to-sandbox.md#custom-actions)

**个性化**

* **新的上下文属性**

  现在可以从个性化编辑器中选择新的上下文属性（**消息轮廓 ID）**。这是一种消息导向属性，用于唯一标识发送给投放中每个目标轮廓的每条消息。例如，此唯一标识符可用作 URL 跟踪参数，以区分收件人打开或单击的每个链接。

* **属性窗格中的已填充属性** - 发布日期：2025 年 4 月 2 日

  默认情况下，个性化编辑器中的属性窗格现在仅显示填充的属性。要查看所有属性，请使用“设置”按钮关闭&#x200B;**[!UICONTROL 仅显示填充属性]**&#x200B;选项。[了解详情](../personalization/personalization-build-expressions.md)

**电子邮件渠道**

* **个性化 URL 跟踪** - 发布日期：2025 年 4 月 30 日

  为了提高灵活性和对电子邮件设置的控制，您现在可以在电子邮件渠道配置级别一次性对所有 URL 跟踪参数进行个性化设置，而不是在电子邮件设计器中为内容中的每个链接进行个性化设置。[了解详情](../email/surface-personalization.md#personalize-url-tracking)

* **电子邮件设计器** - 发布日期：2025 年 4 月 1 日

  为了增强 Journey Optimizer 中的辅助功能，电子邮件设计器中现在提供两个新的字段：它们对应电子邮件内容的 `<html>` 元素中的 `<title>` 元素和 `lang` 属性。除了在&#x200B;**[!UICONTROL 邮件引文]**&#x200B;字段中，您还可以在电子邮件&#x200B;**[!UICONTROL 正文]**&#x200B;部分中定义这些设置。[了解详情](../email/email-metadata.md)

**用例战术手册**

* **战术手册的编写和共享 (Private Beta)** - 您现在可以创建、管理和共享自己的用例战术手册。目前，此功能仅作为 Private Beta 版面向一部分组织提供。要获得访问权限，请与 Adobe 代表联系。[了解详情](../start/playbooks.md)

**导航**

* **内容管理** - 发布日期：2025 年 4 月 2 日

  为了轻松地管理内容模板和片段，您现在可以使用文件夹将它们更高效地组织为结构化层级结构。要了解更多信息，请参阅[内容模板](../content-management/access-content-templates.md#folders)和[片段](../content-management/manage-fragments.md#folders)部分。

  >[!AVAILABILITY]
  >
  >此改进仅面向一部分组织（有限发布版）。

<!--- **Folders for content templates and fragments** - Availability date: May 5, 2025

  Previously available for a set of organizations (LA), folders are now available to all users (GA) to manage their content templates and fragments. Folders let you organize your content templates and fragments more easily and effectively into a structured hierarchy.



<!--- **Right rail in campaigns list**  

  A right rail has been added to the campaigns list, providing detailed information when a campaign is selected.-->

<!--**Playbooks**

- **Create your own playbooks (Beta)**
  
  You can now create your own playbooks in Adobe Journey Optimizer, enabling greater customization and flexibility in journey planning.-->



## 2025 年 3 月发行说明 {#25-3-rn}

### 新功能 {#25-03-features}

此版本包含的新功能详述如下。

<!--table>
<thead>
<tr>
<th><strong>Integration with Adobe Express (Limited Availability)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>The Adobe Express integration in Adobe Journey Optimizer lets you use Adobe Express's editing tools directly during content creation, enabling you to resize, remove backgrounds, crop, and convert assets to JPEG or PNG.<p>
<p>Adobe Express integration in Adobe Journey Optimizer is currently only available for a set of organizations (Limited Availability). It cannot be deployed for use with Healthcare Shield or Privacy and Security Shield.</p>
<p>For more information, refer to the <a href="../integrations/express.md">detailed documentation</a>.</p>
</br>
<img src="assets/do-not-localize/express_resize.gif"/>
</td>
</tr>
</tbody>
</table-->


<!--table>
<thead>
<tr>
<th><strong>Journey metrics</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Journey metrics are now available, allowing you to measure the impact of your activities across the key metrics of your business and to provide clearer insights into your performance.</p>
<p>For more information, refer to the <a href="../building-journeys/success-metrics.md">detailed documentation</a>.</p>
<img src="assets/do-not-localize/success-metric.gif"/>
</td>
</tr>
</tbody>
</table-->

<!-- table>
<thead>
<tr>
<th><strong>Calendar view for journeys (Limited Availability)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>A calendar view is now available in Journey Optimizer to visualize all journeys activations. From this view, you can browse your journeys and check details and properties.<p>
<p>This change is only available for a set of organizations (Limited Availability). To gain access, contact your Adobe representative.</p>
<p>For more information, refer to the <a href="../conflict-prioritization/rule-sets.md">detailed documentation</a>.</p>
</td>
</tr>
</tbody>
</table-->

<table>
<thead>
<tr>
<th><strong>与 Dynamic Media 集成（有限发布版）</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Dynamic Media 资源现可直接在 Journey Optimizer 中使用和访问。通过此集成，您可以：
<ul>
<li>通过实时更新集中管理资源</li>
<li>即时修改宽度和高度等资源设置</li>
<li>通过更新内容和添加个性化字段自定义 Dynamic Media 模板</li>
</ul>
<p>
<p>此集成仅面向一部分组织（有限发布版）。要获得访问权限，请与 Adobe 代表联系。</p>
<p>有关更多信息，请参阅<a href="../integrations/aem-dynamic.md">详细文档</a>。</p>
</td>
</tr>
</tbody>
</table>



<table>
<thead>
<tr>
<th><strong>与 Adobe GenStudio 集成（有限发布版）</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>为了提高营销效率并保持品牌一致性，您现在可以将 GenStudio for Performance Marketing 体验与 Journey Optimizer 无缝集成。这使您能够利用 GenStudio 的 AI 驱动的内容创建以及 Journey Optimizer 的高级编排功能。<p>
<p>目前，Journey Optimizer 中的 GenStudio 集成不可用于 Healthcare Shield 或 Privacy and Security Shield（有限发布版）。</p>
<p>有关更多信息，请参阅<a href="../integrations/genstudio.md">详细文档</a>。</p>
<img src="assets/do-not-localize/genstudio.gif"/>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>灵活的受众评估 (GA)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>以前，灵活的受众评估面向一部分组织提供 (LA)，现在面向所有用户提供 (GA)。通过该功能，您可以按需为选定的受众运行分段作业，确保始终掌握最新的受众数据，然后再将受众作为 Journey Optimizer 历程和营销活动目标。</p>
<img src="assets/do-not-localize/flexible-audience.gif">
<p>有关更多信息，请参阅<a href="../audience/creating-a-segment-definition.md#flexible">详细文档</a>。</p>
</tr>
</tbody>
</table>
</table>

<!--table>
<thead>
<tr>
<th><strong>LINE channel (Limited Availability)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Adobe Journey Optimizer has expanded its cross-channel capabilities to include support for the LINE channel. This enhancement allows you to create, edit, and preview LINE experiences enabling more personalized and engaging interactions. With LINE, you can connect with more customers, send relevant content, and improve your engagement.<p>
<p>This capability is only available for a set of organizations (Limited Availability). To gain access, contact your Adobe representative.</p>
<p>For more information, refer to the <a href="../conflict-prioritization/rule-sets.md">detailed documentation</a>.</p>
</td>
</tr>
</tbody>
</table-->


### 改进 {#25-03-improv}

**个性化编辑器**（发布日期：3 月 12 日）

Journey Optimizer 个性化编辑器已更新，新增了以下功能：
* **更新的代码编辑器设计** – 更简洁的现代界面，改善了可用性和重点内容的显示。
* **搜索和替换** – 添加了在编辑器中快速查找和替换内容的功能。
* **支持撤销和重做** – 允许您轻松还原或重新应用更改。
* **可自定义字体大小** – 允许调整编辑器的字体大小，以提高可读性。
* **内联 JSON 验证** – 为 JSON 内容提供实时客户端验证以加快错误检测。
* **自动填写用户档案和上下文属性** – 提供智能建议以简化内容创建。
* **增强的语法突出显示** – 使代码结构在视觉上更加明显，从而提高可读性。

![展示个性化编辑器中的新增功能的视频](assets/do-not-localize/personalization-editor.gif)

有关更多信息，请参阅[详细文档](../personalization/personalization-build-expressions.md)。

**审批**

现在，在定义审批策略的条件时，您可以选择按标记和/或对象类别进行筛选。

有关更多信息，请参阅[详细文档](../test-approve/approval-policies.md)。

**配置**

* 您现在可以为渠道配置分配 Adobe Experience Platform 统一标记。这让您能够轻松对其进行分类，并改进所有列表中的搜索和导航。[了解详情](../configuration/channel-surfaces.md#channel-config-tags)

* 在 Journey Optimizer 中设置或编辑电子邮件子域时，如果在父域中拥有相关记录，那么您现在可以选择自己管理相关的 DMARC 记录。[了解详情](../configuration/dmarc-record.md#set-up-dmarc)

**业务规则**

现在，您可以在使用批量分段的历程和营销活动中设置每日频率上限。要保证每日频率上限规则的准确性，请确保在创作营销活动或历程时选择优先级最高的命名空间。在 [Platform 身份标识服务指南](https://experienceleague.adobe.com/zh-hans/docs/experience-platform/identity/features/identity-graph-linking-rules/namespace-priority){target="_blank"}中详细了解命名空间优先级

请注意，规则集中的每日频率上限仅适用于一部分组织（有限发布版）。要获得访问权限，请与 Adobe 代表联系。

有关业务规则的更多信息，请参阅[详细文档](../conflict-prioritization/rule-sets.md)。

**内容模板**

现已弃用 HTML 类型内容模板。请注意，您仍然可以使用之前在 [!DNL Journey Optimizer] 中创建的现有 HTML 内容模板。[了解有关内容模板的更多信息](../content-management/content-templates.md)


<!--**Deliverability**

You can now choose to have your emails relayed to your SMTP servers instead of being sent directly from Journey Optimizer to ISPs. This allows you to route final email deliveries through your own Mail Transfer Agents and IPs, or to perform final validations on the emails before sending them to your recipients. The SMTP relay capacity is available on demand - contact your Adobe representative.-->




## 2025 年 2 月发行说明 {#25-02-rn}

**发布日期**：2025 年 2 月 18-19 日


### 新功能 {#25-02-features}

此版本包含的新功能详述如下。

<table>
<thead>
<tr>
<th><strong>创建和管理业务规则</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>您现在可以使用规则集创建业务规则。规则集是一组规则，可帮助您限制在营销活动和跨渠道历程操作中发送的消息，并控制进入历程的用户档案。<p>
<p><ul><li>创建渠道规则集，以限制跨一个或多个渠道发送的消息数。将它们应用于营销活动或历程操作，以实施规则集中定义的规则。通过渠道规则集，您可以根据通信类型应用上限规则。例如，设置规则集以限制“促销消息”，并为“新闻稿”设置另一个规则。根据发送的通信类型，在营销活动或历程操作中应用相应的规则集。</li>
<li> 创建历程规则集以控制用户档案进入历程的情况。限制用户档案在给定时间段内进入历程的频率或同一用户档案可同时参与的历程数。在历程级别应用这些限制，以确保进行正确的进入管理。</li></ul></p>
<p>业务规则以前面向一部分组织提供 (LA)，现在面向所有用户提供 (GA)。历程域业务规则仍然是仅面向一部分组织 (LA) 提供。</p>
<p>有关更多信息，请参阅<a href="../conflict-prioritization/rule-sets.md">详细文档</a>。</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>使用 AI 助手生成登陆页</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>您现在可以借助 AI 助手为登陆页面制作具有吸引力的内容，包括全页设计、个性化文本和自定义视觉效果。</p>
<img src="assets/do-not-localize/ai-lp.gif">
<p>有关更多信息，请参阅<a href="../content-management/generative-lp.md">详细文档</a>。</p>
</td>
</tr>
</tbody>
</table>


<table>
<thead>
<tr>
<th><strong>使用 AI 助手设置品牌（Beta 版）</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>您现在可以设置自己的品牌，来定义品牌的视觉效果和语言标识。 </p>
<p>此功能作为 Private Beta 版发布，面向部分客户提供。在未来版本中，其将逐步向所有客户提供。</p>
<p>有关更多信息，请参阅<a href="../content-management/brands.md">详细文档</a>。</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>自定义操作故障排除</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>您现在可以直接从 Adobe Journey Optimizer 进行实际 API 调用，以验证自定义操作配置。此项新增功能可帮助您在历程中使用自定义操作之前或之后对其进行故障排除。 </p>
<p>有关更多信息，请参阅<a href="../action/troubleshoot-custom-action.md">详细文档</a>。</p>
<!--p> This capability is only available for a set of organizations (Limited Availability). To gain access, contact your Adobe representative.</p-->
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>灵活的受众评估（限量发布）</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>通过灵活的受众评估，您可以按需为选定的受众运行分段作业，确保始终掌握最新的受众数据，然后再将受众作为 Journey Optimizer 历程和营销活动目标。</p>
<img src="assets/do-not-localize/flexible-audience.gif">
<p>有关更多信息，请参阅<a href="../audience/creating-a-segment-definition.md#flexible">详细文档</a>。</p>
<p>此功能仅面向一部分组织（限量发布）。要获得访问权限，请与 Adobe 代表联系。</p>
<p>发布日期：2025 年 1 月 28 日</p>
</tr>
</tbody>
</table>
</table>


### 改进 {#25-02-improvements}

2 月的更新提供了以下改进。

* **数据集生存时间 (TTL)** - 从本月起，将在新沙盒和新组织中推出用于 Journey Optimizer 系统生成的数据集的生存时间 (TTL) 护栏，如下所示：

   * 配置文件存储中的数据为 90 天
   * 数据湖中的数据为 13 个月

  此更改将在后续阶段推广到现有的客户沙盒。

  在[专门的常见问题解答](../data/datasets-ttl.md#frequently-asked-questions)中了解有关此更新的更多信息。

<!--* **Playbooks** - You can now create and publish your own Use Case Playbooks in Journey Optimizer.-->

* **直邮** - 直邮渠道配置中的文件路由现在支持新的服务器类型“数据登陆区”。[了解详情](../direct-mail/direct-mail-configuration.md#file-routing-configuration)

* **短信** - 您现在可以通过覆盖投放、反馈、入站和回调 URL 来管理来自多区域端点的短信消息投放。为支持此功能，已在 API 凭据配置中添加了新的字段“覆盖 URL”。此更改仅适用于 Sinch 提供程序。[了解详情](../sms/sms-configuration-sinch.md)

* **个性化**（发布日期：2025 年 1 月 29 日）- 可在个性化编辑器中使用新的日期/时间帮助程序功能。[了解详情](../personalization/functions/dates.md)


<!--
* The personalization editor has been enhanced with new capabilities such as Auto-complete, Search, and filtering options. You can also show or hide deprecated attributes.-->


* **电子邮件配置** - 如果您在 Adobe 之外管理同意，在进行电子邮件渠道配置设置时，现在可以设置自定义取消订阅电子邮件地址和自定义一键式取消订阅 URL。[了解详情](../email/list-unsubscribe.md#custom-managed)

  ![](../email/assets/surface-list-unsubscribe-custom.png){width="80%"}

* **Decisioning**（发布日期：2025 年 1 月 28 日）- 在编辑项目目录的架构时，Decisioning 现在支持“对象”数据类型。[了解详情](../experience-decisioning/catalogs.md)
