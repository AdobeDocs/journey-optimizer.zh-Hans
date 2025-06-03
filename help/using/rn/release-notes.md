---
solution: Journey Optimizer
product: journey optimizer
title: 发行说明
feature: Release Notes
topic: Content Management
description: Adobe Journey Optimizer 发行说明
exl-id: 06fa956a-b500-416e-9d42-b683c328e837
source-git-commit: 6da1d9a3edb8a30b8f13fd0cb6a138f22459ad00
workflow-type: tm+mt
source-wordcount: '1394'
ht-degree: 88%

---

# 发行说明 {#release-notes}

>[!CONTEXTUALHELP]
>id="ajo_homepage_card1"
>title="新增功能"
>abstract="**Adobe Journey Optimizer** 不断地提供新功能、对现有功能的增强和错误修复。会在每月的最后一周将所有更改整合到发行说明中。"

[!DNL Adobe Journey Optimizer] 不断地提供新功能、对现有功能进行增强和修复错误。会在每月的最后一周将所有更改整合到发行说明中。[!DNL Adobe Journey Optimizer] 原生构建于 [!DNL Adobe Experience Platform] 之上并继承了其所具备的最新创新技术和改进。在 [Adobe Experience Platform 发行说明](https://experienceleague.adobe.com/docs/experience-platform/release-notes/latest.html?lang=zh-Hans){target="_blank"}中进一步了解这些更改。

## 2025年6月更新 {#25-6-rn}


<table>
<thead>
<tr>
<th><strong>扩展试验入选者的范围</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>通过缩放试验入选者，可自动或手动将试验的入选变体转出给全体受众。 通过此功能，确定最佳合适人选后，您就可以最大程度地扩大范围并提高效率，而无需持续进行人工监督。</p>
<p>有关更多信息，请参阅<a href="../content-management/content-experiment.md">详细文档</a>。</p>
<p>发布日期：2025年6月2日</p></td>
</tr>
</tbody>
</table>

&lt;<table>
<thead>
<tr>
<th><strong>冲突和优先级</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>在 Journey Optimizer 中，管理营销活动和历程的数量和时间至关重要，这样才能避免因过多的交互而让客户不堪重负。Journey Optimizer 现在提供多种冲突管理和优先级工具，这些工具之前仅向部分组织提供 (LA)，现在已正式发布 (GA)。</p>
<p>此功能之前为限量发布，现在可用于所有环境。在此正式发布版中，引入了以下增强功能：</p>
<ul>
<li>扩展支持：除了读取受众历程之外，冲突管理工具现在还支持单一历程和受众资格筛选历程。</li>
<li>改进了故障排除功能：查询服务中现在提供两个新的步骤事件字段，可以让您分析为何在历程或营销活动中拒绝某个轮廓。</li>
<li>增强了报告功能：报告现在可以显示哪个特定规则从历程或营销活动中排除了轮廓，从而提高透明度并提供切实可行的见解。</li></ul>
<img src="assets/do-not-localize/gif-conflict.gif">
<p>有关更多信息，请参阅<a href="../conflict-prioritization/gs-conflict-prioritization.md">详细文档</a>。</p>
<p>发布日期：2025年6月3日</p>
</td>
</tr>
</tbody>
</table>

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
<p>此更改当前仅适用于一组组织（限量发布）。 若要请求访问权限，请使用<a href="https://forms.cloud.microsoft/r/FC49afuJVi" target="_blank">此表单</a>。</p>
<img src="assets/do-not-localize/calendar.gif">
<p>有关更多信息，请参阅以下部分：<a href="../building-journeys/journey-ui.md">浏览和筛选您的历程</a>、<a href="../campaigns/modify-stop-campaign.md">访问营销活动</a>。</p>
<p>发布日期： 2025年5月28日</p>
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
<p>以前此功能可用于一组有限的组织(LA)，现在为GA，提供以下增强功能：您现在可以使用编辑器模式定义占位符并在片段签名中映射个性化值。</p>
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
<p>发布日期： 2025年5月20日</p>
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
<p>发布日期： 2025年5月20日</p>
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


* **沙盒副本支持新Campaign对象** — 发布日期： 2025年5月15日

  使用资源包导出和导入功能跨多个沙盒复制营销活动时，现在还会复制以下依赖项：渠道配置、试验变体和设置、决策策略和项目。[了解详情](../configuration/copy-objects-to-sandbox.md)

  <!--* **Decisioning** - Availability date: May 16, 2025

    Decisioning objects can now be copied between sandboxes, streamlining testing and deployment workflows. [Read more](../configuration/copy-objects-to-sandbox.md#decisioning)-->

* **登陆页的文件夹** - 发布日期：2025 年 5 月 9 日

  为轻松地管理登陆页，您现在可以使用文件夹将其更高效地组织为结构化层级。[了解详情](../landing-pages/manage-lp.md)

* **直邮：SFTP 连接支持 SSH 密钥** - 发布日期：2025 年 5 月 5 日

  在直邮文件路由配置中，除了使用密码身份验证类型的现有 SFTP 之外，您现在还可以将直邮文件导出到使用 SSH 密钥身份验证的 SFTP 服务器。[了解详情](../direct-mail/direct-mail-configuration.md)

* **激活“药丸”以用于个性化操作** - 发布日期：2025 年 5 月 5 日

  个性化编辑器中新增了一个“药丸”按钮。启用后，配置文件和上下文属性将显示为“药丸”，从而提高代码的可读性。[了解详情](../personalization/personalization-build-expressions.md#options)

  >[!AVAILABILITY]
  >
  >该功能将在接下来的 30 天内逐步推广到所有环境。

* Web渠道&#x200B;**中的**“重定向到URL”支持 — 可用日期： 2025年5月20日

  现在，您可通过 Journey Optimizer 的 Web 渠道将访客重定向到其他现有 URL，而无需在可视编辑器中创作新的变体。此功能适用于运行试验来比较两个完全不同的页面，而不是只更改页面中的几个元素。[了解详情](../web/create-web.md#web-redirect-to-url)

* **模板和片段的文件夹** — 可用日期： 2025年5月20日

  通过文件夹，您可以更轻松、更高效地将对象组织为结构化层级。文件夹以前面向一部分组织提供 (LA)，现在面向所有用户提供 (GA)，以便管理其内容模板和片段。要了解更多信息，请参阅[内容模板](../content-management/access-content-templates.md#folders)和[片段](../content-management/manage-fragments.md#folders)部分。

* **电子邮件模板中的点击跟踪** — 可用日期： 2025年5月20日

  现在，[!DNL Journey Optimizer] 原生支持电子邮件内容中图像映射的 `<area>` 元素点击跟踪。这是为了确保图像映射区域接收与标准超链接相同的跟踪包、跟踪数据和附加参数。[了解有关消息跟踪的更多信息](../email/message-tracking.md#manage-tracking)

<!--
* **Decisioning - Leverage Adobe Experience Platform datasets** 
  
  Journey Optimizer now allows you to leverage Adobe Experience Platform datasets in the following Decisioning objects: eligibility rules, ranking formulas, and capping rules.-->

* **营销活动列表中的右边栏** — 发布日期：2025年5月20日

  现在，在营销活动列表中，选择营销活动会打开显示其详细信息的窗格。

<!--* **Form fields in code-based experience content**

  In content templates, you can now define specific JSON or HTML fields which enable non-technical users to easily edit content in code-based experiences without the need to manipulate code.

* **Decision item attribute support for decisioning rules**
  
  You can now leverage decision item attributes to create decisioning rules.

* **Subdomains - 'Custom delegation' method**  
  In addition to the full delegation and the CNAME method, a new subdomain configuration method is now available: the Custom delegation method, which enables you to fully own controlling and maintaining all aspects of DNS that are required for delivering, rendering, and tracking messages.
  -->

