---
solution: Journey Optimizer
product: journey optimizer
title: 2022 年发行说明
description: Journey Optimizer 2022 年发行说明
feature: Release Notes
topic: Content Management
role: User
level: Beginner, Intermediate
hidefromtoc: true
exl-id: 0997a640-3f89-4460-ba93-ea21a9d4efc5
source-git-commit: 528e1a54dd64503e5de716e63013c4fc41fd98db
workflow-type: tm+mt
source-wordcount: '3598'
ht-degree: 100%

---

# 2022 年发行说明 {#release-notes-2022}

本页列出了 [!DNL Journey Optimizer] 于 2022 年发布的功能和改进。



## 2022 年 10 月版 {#oct-2022-release}

<!--

### New capability{#oct-2022-features}

<table>
<thead>
<tr>
<th><strong>Direct Mail Channel (Limited Availability)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>You can now add direct mail messages in your campaigns and journeys. Direct mail is an offline channel that allows you to personalize and generate the files required by direct mail providers to send mail to your customers.</p>
<p>When you prepare a direct mail delivery, Journey Optimizer generates a file including all the targeted profiles and the chosen contact information (postal address for example). You will then be able to send this file to your direct mail provider who will take care of the actual sending.</p>
</td>
</tr>
</tbody>
</table>

-->

### 改进 {#oct-2022-improvements}

**历程**

* **强制定期重入**&#x200B;选项已添加到定期读取受众计划参数中。利用此选项，可让历程中仍存在的所有轮廓在下次执行时自动退出该历程。停用此选项后，轮廓必须先完成历程，然后才能在另一个事件中再次进入。[了解详情](../building-journeys/read-audience.md#configuring-segment-trigger-activity)

**管理**

* 在用户界面中添加了一条消息，警告称子域、登陆页子域、PTR 记录和 IP 池配置对所有沙盒都是通用的，因此对这些配置中的任何修改也会影响生产沙盒。
* 修改了从用户界面以 CSV 文件格式上传禁止列表的步骤。[了解详情](../configuration/manage-suppression-list.md#download-suppression-list)

**营销活动**

* 您现在可以存档已完成和已停止的营销活动。[了解详情](../campaigns/modify-stop-campaign.md#archive)


## 2022 年 9 月版{#sept-2022-release}

### 新功能{#sept-2022-features}

<table>
<thead>
<tr>
<th><strong>动态内容和新的条件规则生成器</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>你现在可以创建动态内容，以根据条件规则调整消息的内容。</p> 
<p>条件规则是使用表达式编辑器中的可视化规则生成器创建的，你可以在其中存储这些规则以供在历程和营销活动中进一步重复使用。</p>
<img src="assets/do-not-localize/dynamic-content.gif"/>
<p>有关更多信息，请参阅<a href="../personalization/get-started-dynamic-content.md">详细文档</a>。
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>API 触发的营销活动</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>除了现有的计划营销活动之外，您现在还可以在 Journey Optimizer 中创建 API 触发的营销活动，并使用 API 从外部系统调用它们。</p>
<p>这允许您满足各种操作和事务性消息传递需求，如密码重置、OTP 令牌等。</p>
<img src="assets/do-not-localize/api-triggered.gif"/>
<p>有关更多信息，请参阅<a href="../campaigns/api-triggered-campaigns.md">详细文档</a>。
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>数据访问控制</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>通过基于属性的访问控制，管理员可以根据特定属性控制对特定对象的访问。这些属性可以是添加到对象的元数据，如标签。从此版本开始，管理员还可以定义只能访问特定字段和/或对象的用户角色以及与这些字段和/或对象对应的数据。</p>
<p> 目前，基于属性的访问控制的使用仅限于选定用户，但将在未来版本中部署到所有环境。</p>
<img src="assets/do-not-localize/olac.gif"/>
<p>有关更多信息，请参阅<a href="../administration/object-based-access.md">详细文档</a>。
</td>
</tr>
</tbody>
</table>


<table>
<thead>
<tr>
<th><strong>数据管理和隐私</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>凭借其数据使用标签和执行 (DULE) 管理框架，Journey Optimizer 现在可以利用 Adobe Experience Platform 管理策略来防止通过自定义操作将敏感字段导出到第三方系统。如果系统在自定义操作参数中识别出受限字段，则会显示一条错误消息，阻止您发布历程。</p>
<p>数据使用标签和执行 (DULE) 的使用当前仅限于选定客户，并且将在未来版本中部署到所有环境。</p>
<p>有关更多信息，请参阅<a href="../action/action-privacy.md">详细文档</a>。
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>自动同意执行（同意策略）</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Adobe Experience Platform 允许您轻松地采用和执行营销策略，尊重客户的同意偏好。同意策略是在 Adobe Experience Platform 中定义的。在 Journey Optimizer 中，您可以将这些同意策略应用于自定义操作。例如，您可以定义同意策略以排除未同意接收电子邮件、推送或短信通信的客户。
<p>自动同意执行当前仅适用于已购买 Healthcare Shield 加载项的组织。</p>
<p>有关更多信息，请参阅<a href="../action/consent.md">详细文档</a>。
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>权限管理</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Journey Optimizer 支持定义用户角色和访问策略，以用来管理有关功能和对象的权限。通过 <strong>Adobe Experience Cloud 权限</strong>，您可以创建和管理角色，并为这些角色分配所需的资源权限。权限还允许您管理与特定角色关联的标签、沙盒和用户。</p>
<p> 目前，权限的使用仅限于选定用户，但将在未来版本中部署到所有环境。</p>
<p>有关更多信息，请参阅<a href="../administration/attribute-based-access.md">详细文档</a>。
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>警报和监控</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>作为 Journey Optimizer 用户，您现在可以通过用户界面访问系统警报，在历程工作异常时获得通知。您可以查看可用的警报并订阅它们。如果读取受众活动在定义的时间范围内未处理任何轮廓，则此版本中提供的第一个警报将会警告您。解锁此工作流后，将会有更多内容。</p>
<!--p>For more information, refer to the <a href="../reports/alerts.md">detailed documentation</a>.</p-->
</td>
</tr>
</tbody>
</table>


<!--table>
<thead>
<tr>
<th><strong>Data Hygiene</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Adobe Experience Platform provides a suite of data hygiene capabilities that allow you manage your stored data through programmatic deletions of consumer records and datasets. This capability is now available for Adobe Journey Optimizer. </p>
<p>You can manage your data stores to ensure that information is used as expected, is updated when incorrect data needs fixing, and is deleted when organizational policies deem it necessary.</p>
<p><strong>Caution</strong> - Data Hygiene capabilities are currently only available for organizations that have purchased the Healthcare Shield add-on offering.</p>
<p>For more information, refer to the <a href="../building-journeys/read-audience.md#configuring-segment-trigger-activity">detailed documentation</a>.
</td>
</tr>
</tbody>
</table-->

### 改进{#sept-2022-improvements}

**历程**

* 现在，**实体数据集**&#x200B;是 Adobe Journey Optimizer 中包含的现成可用的数据集。此查询数据集包含元数据，可用于丰富跟踪和反馈数据集信息。这有助于您使用更易理解的数据来改进报表和查询。[了解详情](../data/datasets-query-examples.md#entity-dataset)
* 向单一历程（以事件或受众资格筛选开始）添加了新护栏，以防止历程因同一事件被错误地触发多次。默认情况下，会暂时阻止用户档案重新进入 5 分钟。[了解详情](../start/guardrails.md#events-g)

**管理**

* 激活或停用允许列表时，现在会显示新的警告，详细说明每个操作的影响。[了解详情](../configuration/allow-list.md#enable-allow-list)
* 更新了用于创建渠道配置、创建 IP 池、管理禁止列表和允许列表以及配置短信渠道的用户界面。
* 现在，为给定子域创建第一个渠道配置时，处理时间需要 10 分钟到 10 天，而使用该子域的后续界面的处理时间最多只需 3 小时。[了解详情](../configuration/channel-surfaces.md#create-channel-surface)
* 更新了用于创建登陆页面预设和登陆页面子域的用户界面。[了解详情](../landing-pages/lp-subdomains.md)

**审核控制**

* 借助 Journey Optimizer，您可以识别用户在系统中对各种服务和功能（如营销活动、历程、消息、登陆页面等）执行的操作。审核日志资源现在包括对各种其他操作所做的更改，并会在活动发生时自动进行记录。请参阅[此页面](../privacy/audit-logs.md)以了解详情。

**存档支持**

* 新的&#x200B;**实体数据集**&#x200B;包括“模板”字段，用于导出所有渠道上已发送消息的格式和结构，以便进行存档。[了解详情](../configuration/archiving-support.md)

**登陆页面**

* 您现在可以在同一登陆页面内使用来自其他页面的上下文数据。例如，如果将复选框链接到主登录页上的订阅列表，则可以在“感谢”子页面上使用该订阅列表。[了解详情](../landing-pages/lp-content.md#use-primary-page-context)

<!--* When configuring the primary page, you can now create additional data to enable storing information when the landing page is being submitted. [Learn more](../landing-pages/lp-content.md#use-additional-data)-->

<!--* You can now use information that was submitted on a landing page to send communications to your customers. For example, if a user subscribes to a given subscription list, you can leverage that information to send an email recommending other subscription lists to that user.-->

### 其他更改{#sept-2022-other}

* 历程突发模式已被 Campaign 快速投放模式取代。[了解详情](../push/create-push.md#rapid-delivery)
* 为了提高性能，从读取受众、受众资格筛选或业务事件活动开始的历程中，无法再使用体验事件字段组。此更改仅适用于新历程。现有历程将保留当前行为。[了解详情](../start/guardrails.md#expression-editor)
* 已移除计划读取受众历程的 1 小时限制。这些历程现在可以毫不延迟地执行。




## 2022 年 8 月版 {#aug-2022-release}

### 新功能

<table>
<thead>
<tr>
<th><strong>在 Journey Optimizer 中创建和管理营销活动</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>使用 Journey Optimizer 营销活动通过各种渠道向特定受众投放一次性内容。使用历程时，操作被设计为按顺序执行。 借助营销活动，可同时执行诸多操作：立即执行或根据指定计划执行。 </p>
<img src="assets/do-not-localize/campaigns.gif"/>
<p>在<a href="../campaigns/get-started-with-campaigns.md">详细文档</a>和<a href="https://video.tv.adobe.com/v/346680">功能介绍视频</a>中了解如何创建营销活动。
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>向用户发送短信（一般情况可用）</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>现在，通过与 <b>Sinch</b> 或 <b>Twilio</b> 集成，您可以在 Journey Optimizer 中创建、个性化和发送短信。</p>
<img src="assets/do-not-localize/SMS.gif"/>
<p>在此<a href="../sms/create-sms.md">详细文档</a>中了解如何创建和发送短信。</p>
</td>
</tr>
</tbody>
</table>

<!--table>
<thead>
<tr>
<th><strong>New Dynamic Expression Builder</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>You can now create conditional content blocks across different authoring services to personalize your content.</p>
<p>In addition to the Personalization Expression Library, the Expression Editor provides a new Conditional Rule Builder to help you design and save your content blocks.</p>
<p>For more information, refer to the <a href="../building-journeys/read-audience.md#configuring-segment-trigger-activity">detailed documentation</a>.
</td>
</tr>
</tbody>
</table-->


### 改进

**报告**

* 历程全局报告中现在提供同意策略表和图表。利用这些小组件，可跟踪在自定义操作中从策略排除的轮廓。[了解详情](../reports/journey-global-report-cja.md#journey-global)

  要访问最新的小组件，请注意，您必须重置不同的报告仪表板。有关仪表板自定义的更多信息，请参阅[详细文档](../reports/report-gs-cja.md)。

**管理**

* 现在，可以更新用于短信渠道的主电话号码。[了解详情](../configuration/primary-email-addresses.md)


## 2022 年 7 月版 {#july-2022-release}

### 新功能

<table>
<thead>
<tr>
<th><strong>新增内联消息传送流程</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Journey Optimizer 为历程中的消息创作提供了一个新流程。在 Journey Optimizer 中，内联消息传送可简化创建和发送电子邮件、推送通知或短信的工作流程，为用户节省大量时间。通过将消息作为单独的步骤删除，而改为在历程画布上的操作中使其可内联编辑，用户只需单击较少的按钮并导航较少的屏幕即可设计和编辑内容。</p>
<img src="assets/do-not-localize/inline.gif"/>
</td>
</tr>
</tbody>
</table>


<table>
<thead>
<tr>
<th><strong>基于属性的访问控制（限量发布）</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>现可使用标签来识别架构字段，这些标签可定义组织或数据使用范围。管理员可使用权限界面定义涵盖 XDM 架构字段的访问策略，更好地管理授予用户或用户组（内部、外部或第三方用户）的访问权限，以及管理特定类型数据（即敏感个人数据/SPD）的访问权限。</p>
<p>目前，基于属性的访问控制的使用仅限于选定的用户，但将在未来版本中部署到所有环境。</p>
<p>有关更多信息，请参阅<a href="../administration/attribute-based-access.md">详细文档</a>。</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>批量决策作业</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>现可从用户界面运行批量决策作业，这样就不需要开发人员来运行批处理 API 作业，还可以缩短营销所需的时间。使用新界面可创建作业并管理当前/过去的作业。</p>
<img src="assets/do-not-localize/batch.gif"/>
<p>有关更多信息，请参阅<a href="../offers/batch-delivery.md">详细文档。</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>在决策中自动使用表现最好的产品建议（限量发布）</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>现可在决策管理中使用个性化优化模型系统。利用这种新型模型可根据受众和产品建议表现对产品建议进行优化和个性化设置。</p>
<p>目前，个性化优化 AI 模型的使用仅限于选定的用户，但将在未来的版本中部署到所有环境。</p>
<img src="assets/do-not-localize/ai-ranking.gif"/>
<p>有关更多信息，请参阅<a href="../offers/ranking/personalized-optimization-model.md">详细文档</a>。</p>
</td>
</tr>
</tbody>
</table>

### 改进

**历程**

* **结束历程** - 在历程画布中，已从面板中移除&#x200B;**结束**&#x200B;活动。现在，会默认将结束标记添加到每个路径的末尾，且无法移除。这项改进可更好地报告客户从历程中退出的位置，而无需历程参与者执行任何操作。请参阅[文档](../building-journeys/end-journey.md)和[功能视频](https://video.tv.adobe.com/v/345376){target="_blank"}。


*  默认情况下，历程属性中的&#x200B;**轮廓时区**&#x200B;选项现在处于未选中状态。[了解详情](../building-journeys/timezone-management.md#timezone-from-profiles)

**消息**

* 消息预设现已改为&#x200B;**渠道配置**。[了解详情](../configuration/channel-surfaces.md)

**管理**

* **PTR 记录版本** - 现在，更新 PTR 记录时，处理时间最多只需 3 小时。[了解详情](../configuration/ptr-records.md#processing)

* **允许列表 UI** - 现可使用 Journey Optimizer 用户界面向允许列表添加新的电子邮件地址或域。[了解详情](../configuration/allow-list.md)

* **允许列表逻辑更新** - 现在，允许列表这一功能会在启用后立即应用允许列表逻辑，即使该列表为空也是如此。[了解详情](../configuration/allow-list.md#logic)

* **URL 跟踪参数** - 现可使用表达式编辑器在电子邮件界面中配置 URL 跟踪参数（即消息预设）。[了解详情](../email/email-settings.md#url-tracking)

**决策管理**

* **受众规模** - 现在，在创建决策规则、选择受众或规则以设置产品建议资格，或将受众或规则添加到决策范围时，用户界面中会显示新的受众规模估算组件。


## 2022 年 6 月版 {#june-2022-release}

### 新功能

<table>
<thead>
<tr>
<th><strong>向用户发送短信（限量发布）</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>现在，通过与 <b>Sinch</b> 或 <b>Twilio</b> 集成，您可以在 Journey Optimizer 中创建、个性化和发送短信。</p>
<!--img src="assets/do-not-localize/SMS.gif"/-->
<p>目前，短信渠道仅适用于一批组织（限量发布）。有关更多信息，请与您的 Adobe 代表联系。</p>
<p>在此<a href="../sms/create-sms.md">详细文档</a>中了解如何创建和发送短信。</p>
</td>
</tr>
</tbody>
</table>


<table>
<thead>
<tr>
<th><strong>利用 Adobe Stock 集成，更快地找到更具影响力的图像</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Adobe Stock 和 Adobe Journey Optimizer 电子邮件设计器集成插件为客户提供一种简单的方式来导航、许可和保存图像，用于消息创作。使用</br>全新的<b>查找类似 Stock 照片</b>选项，您可查找与图像的内容、颜色以及合成匹配的照片库。 </p>
<p>有关更多信息，请参阅<a href="../integrations/stock.md">详细文档</a>。</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>对所有电子邮件使用电子邮件密送</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>现在，您可以使用电子邮件密送功能存储由 Adobe Journey Optimizer 发送的电子邮件。在电子邮件预设中启用此选项，以便发送的每封电子邮件都会密送至您的密送电子邮件地址。</p>
<p>有关更多信息，请参阅<a href="../configuration/archiving-support.md#bcc-email">详细文档</a>。</p>
</td>
</tr>
</tbody>
</table>

<!--<table>
<thead>
<tr>
<th><strong>Automatically use the best performing offer in your decisions</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>You can now use personalized optimization model systems in Decision Management. This new type of model allows you to optimize and personalize offers based on audiences and offer performance.</p>
<p>The use of personalized optimization AI models is currently restricted to selected users, and will be deployed to all environments in a future release.</p>
<img src="assets/do-not-localize/ai-ranking.gif"/>
<p>For more information, refer to the <a href="../offers/ranking/personalized-optimization-model.md">detailed documentation</a>.</p>
</td>
</tr>
</tbody>
</table>-->

<table>
<thead>
<tr>
<th><strong>在沙盒之间复制对象</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>现在，您可以重新创建从 Journey Optimizer 沙盒到另一个沙盒的体验，例如从非生产沙盒到生产沙盒。此新功能可将整个历程（包括历程赖以正常运行的任何对象）从一个环境复制到另一个环境。除了历程之外，您还可以复制其他组件，如产品建议、消息、架构、数据集、数据源、事件和操作。</p>
<p>有关更多信息，请参阅<a href="../building-journeys/copy-to-sandbox.md">详细文档</a>。
</td>
</tr>
</tbody>
</table>




### 改进

**决策管理**

* **HTML 和 JSON 文件支持** – 现在，您可将外部 HTML 和 JSON 文件从 Adobe Experience Cloud 资产库拖放到产品建议展现方案内容中。[了解详情](../offers/offer-library/add-representations.md#html-json)


**电子邮件**

* **另存为模板** – 现在，您可将电子邮件内容另存为模板，并在创建其他消息时重复使用。[了解详情](../content-management/content-templates.md#save-as-template)


**管理**

* **预览跟踪 URL 参数** – 现在，配置消息预设时，如果定义了 URL 跟踪参数，则会显示所产生的跟踪 URL 的动态预览。[了解详情](../email/email-settings.md#url-tracking)

* **消息预设版本** - 现在，更新消息预设时，处理时间最长可能只需 3 小时。[了解详情](../configuration/channel-surfaces.md#edit-channel-surface)

* **IP 池版本** - 现在，更新 IP 池时，处理时间最长可能只需 3 小时。[了解详情](../configuration/ip-pools.md#edit-ip-pool)




## 2022 年 5 月版 {#may-2022-release}

### 新功能

<table>
<thead>
<tr>
<th><strong>消息频度规则</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>您现在可以设置跨渠道业务规则，以自动从消息和操作中排除遭到过量请求的轮廓。</p>
<p>有关更多信息，请参阅<a href="../conflict-prioritization/rule-sets.md">详细文档</a>。</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>决策管理 - 人工智能排名自动优化模型</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>现在，您可以在决策管理中使用经过培训的模型系统。 此新功能可为给定轮廓显示产品建议排名。</p>
<p>有关更多信息，请参阅<a href="../offers/offer-activities/configure-offer-selection.md#use-ranking-strategy">详细文档</a>。</p>
</td>
</tr>
</tbody>
</table>

<!--table>
<thead>
<tr>
<th><strong>Attribute-based Access Control (ABAC)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Permission management in Journey Optimizer has been extended to data access. You can now manage data access for specific teams or groups of users (i.e. internal, external, 3rd parties) ​and manage access to specific types of data (i.e. Sensitive Personal Data/SPD).</p>
<p>This capability is available for a limited set of customers.</p>
<p>For more information, refer to the <a href="../landing-pages/create-lp.md">detailed documentation</a>.</p>
</td>
</tr>
</tbody>
</table-->

<table>
<thead>
<tr>
<th><strong>Journey Optimizer 审核日志</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>您现在可以监测用户对 Adobe Journey Optimizer 资源执行的操作。</p>
<p>有关更多信息，请参阅<a href="../privacy/audit-logs.md">详细文档</a>。</p>
</td>
</tr>
</tbody>
</table>

### 改进

**个性化**

* **用于字符隐藏的新辅助函数** - 使用 `mask` 辅助函数，可将字符串的一部分替换为“X”字符。 [了解详情](../personalization/functions/string.md#mask)

**登陆页面**

* **不包含表单的登陆页面** - 您现在可以创建并发布不包含表单且无需访客执行任何操作的登陆页面。
* **登陆页面模板** - 现在，您可以将登陆页面另存为模板，并在创建其他登陆页面时重复使用。 [了解详情](../landing-pages/lp-templates.md)
* **返回主页面** - 您现在可以从同一登陆页面中的任何子页面添加指向主页面的链接。
* **自定义 JavaScript 支持** - 您现在可以向登陆页面内容添加自定义 JavaScript 以执行高级样式调整或向登陆页面添加自定义行为。[了解详情](../landing-pages/lp-custom-js.md)

**历程**

* **读取受众** - 现在，一次性读取受众历程在历程执行 30 天后会变为“已完成”状态。对于计划的读取受众，此期限为上次执行后的 30 天。[了解详情](../building-journeys/read-audience.md)
* **表达式编辑器** - 添加了 [limit](../building-journeys/functions/functionlimit.md) 函数，以限制列表的项目数。 现在，使用 [sort](../building-journeys/functions/functionsort.md) 函数可对列表对象进行排序。 此外，还向 [disctinct](../building-journeys/functions/functiondistinct.md) 和 [distinctWithNull](../building-journeys/functions/functiondistinctwithnull.md) 函数添加了 listObject 支持。

**管理**

* **许可证使用情况仪表板更新** – 现在，[!DNL Adobe Journey Optimizer] 用户界面中提供的“许可证使用情况”仪表板可反映&#x200B;**已授予许可**&#x200B;平均用户轮廓丰富度。您可在此量度呈现中看到一个下拉信息，这意味着现在可以正确报告许可证限制。[了解详情](../audience/license-usage.md)


## 2022 年 4 月版 {#april-2022-release}

### 改进

**登陆页面**

* **选择启用/选择禁用复选框的新选项** - 您现在可以在订阅登陆页面中为选择启用/选择禁用插入一个复选框。用户需要选中复选框来表示同意（选择启用），取消选中该复选框以取消同意（选择禁用）。[了解详情](../landing-pages/design-lp.md#define-lp-specific-content)

* **预填登陆页面字段** - 现在，允许用户使用轮廓信息预填登陆页面字段。[了解详情](../landing-pages/create-lp.md#configure-primary-page)

**决策管理**

* **Edge 上的 Decisioning API** - Edge Decisioning API 可以投放和呈现在决策管理中管理的个性化产品建议。您可以使用决策管理用户界面 (UI) 或 API 创建产品建议和其他相关对象。[了解详情](../offers/api-reference/offer-delivery-api/edge-decisioning-api.md)

**管理**

* **PTR 提交持续时间** - 现在，PTR 编辑生效的持续时间为数小时。[了解详情](../configuration/ptr-records.md#processing)

**电子邮件设计**

* **20 个新电子邮件模板**&#x200B;现在可用于在 Journey Optimizer 中设计电子邮件内容。

**用户界面**

* **Journey Optimizer UI 中的上下文帮助** - 为 Journey Optimizer 中的多个页面添加了上下文帮助链接。如果可用，请单击“i”图标以查看当前功能的快速说明并访问相关文章。

**与 Adobe Campaign Standard 的集成**

作为 Adobe Campaign Standard 客户，您现在可以使用 Journey Optimizer 发送电子邮件、推送通知和短信。借助新的内置操作在 Journey Optimizer 中利用 Campaign Standard 事务型消息传递功能。[了解详情](../action/acs-action.md)

<!--
### Fixes

* Fixed an issue which caused tracking reports not to be available as the `JourneyActionId` was not properly populated. PLATIR-19854, CJM-26006
* Fixed an error on business events which could block the journey publication. CJM-25931
* Fixed an issue which could prevent images in Email Designer templates from being displayed. PLATIR-18176, CJM-25008
-->

## 2022 年 3 月版 {#march-2022-release}

### 改进

**历程**

* 为了避免统一轮廓架构中出现不必要的字段，默认情况下将不再为轮廓启用历程步骤事件架构。如有需要，您可以启用它。[了解详情](../reports/sharing-overview.md)
* 与导出作业相关的新步骤事件现在由 Journey Optimizer 发送至 Adobe Experience Platform。文档中添加了查询示例。[了解详情](../reports/query-examples.md)

**决策管理**

* 现在，您可以指定是将产品建议上限应用到所有用户还是某个特定轮廓，是应用到所有放置环境还是具体的放置环境。[了解详情](../offers/offer-library/add-constraints.md#capping)
* 通过“批量决策 API”，各类组织可以在一次调用中对特定受众中的所有轮廓使用决策管理功能。受众中每个轮廓的产品建议内容会放置在 AEP 数据集中，可用于自定义批量工作流。[了解详情](../offers/api-reference/offer-delivery-api/batch-decisioning-api.md)

**管理**

* 现在，您可以在邮件预设级别启用/禁用电子邮件标头中的取消订阅链接，并在邮件级别设置自定义取消订阅 URL。[了解详情](../configuration/channel-surfaces.md#list-unsubscribe)
* 现在可以通过 [!DNL Journey Optimizer] 界面在生产沙盒和非生产沙盒上启用和禁用允许列表。[了解详情](../configuration/allow-list.md#enable-allow-list)

**个性化**

* 现在可以在库中保存 40 多个个性化表达式。[了解详情](../personalization/use-expression-fragments.md)

## 2022 年 2 月版 {#feb-2022-release}

### 新功能

<table>
<thead>
<tr>
<th><strong>订阅登陆页面</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>您现在可以在 Journey Optimizer 中创建和设计登陆页面，并将用户定向到在线表单，在表单中，用户可以选择加入或选择退出接收您的通信，或订阅特定服务（如新闻稿）。</p>
<p>有关更多信息，请参阅<a href="../landing-pages/create-lp.md">详细文档</a>和相关的<a href="../landing-pages/lp-use-cases.md">示例用例</a>。</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>新的个性化表达式库</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Journey Optimizer 现提供一个可供您访问预定义的个性化表达式的库。这些表达式由管理员用户配置。</p>
<p>有关更多信息，请参阅<a href="../personalization/use-expression-fragments.md">详细文档</a>。</p>
</td>
</tr>
</tbody>
</table>


<!--table>
<thead>
<tr>
<th><strong>API Developer Site and Suppression API</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Journey Optimizer provide RESTful APIs that allow you to programmatically perform key operations in your applications.
Developer SDK for Journey Optimizer is now available with the Suppression API (beta).</p>
<p>With this API, you can control your outgoing messages using suppression and allow lists.
The suppression list helps you with honoring the ISPs' feedback to preserve sending IP reputation. The allow list helps you ensure that you send only to those email addresses which are in the allowed list, and typically to ensure that you don't send mails to customers from your development sandbox.</p>
<p>See <a href="https://developer.adobe.com/journey-optimizer-apis/">Adobe Journey Optimizer APIs</a>.</p>
</td>
</tr>
</tbody>
</table-->

<table>
<thead>
<tr>
<th><strong>使用 UTM 跟踪参数传递信息以跟踪您的消息</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>在 Journey Optimizer 消息内容中，您现在可以将 UTM 参数添加到链接：这些参数可以提供有关该链接的其他数据，并帮助您确定用户点击您链接的位置和原因。</p>
<p>有关更多信息，请参阅<a href="../configuration/channel-surfaces.md#configure-email-settings">详细文档</a>。</p>
</td>
</tr>
</tbody>
</table>

### 改进

**历程**

* 为优化性能，现在，所有处于测试模式且一周内未触发的历程都将切换回草稿状态。[了解更多信息](../building-journeys/testing-the-journey.md#important_notes)
* Journey Optimizer 和 Adobe Campaign v7/v8 之间的集成已经过优化以提高性能。默认配置上限已更改为 4000 次调用/5 分钟。[了解更多信息](../action/acc-action.md#important-notes)

**报告**

* 现在，可以根据投放的状态对其进行筛选：
   * 在消息执行列表中，您现在可以从投放列表中排除校样。
   * 在实时/全局报告中，您可以选择排除测试事件。

* 您现在可以访问有关发送时间优化数据的报告：立即向其发送消息的人数，以及通过 1 小时优化、2 小时优化向其发送消息的人数，等等。

<!--* decision management reports are now available in Journey Optimizer. You can access the following metrics: Offers sent - Offers' impression rate - Offers' click rate - Breakdown report on Offers' sent.-->

**决策管理**

* 排名和 AI 排名现在位于同一选项卡中。

## 2022 年 1 月版 {#january-2022-release}

### 新功能

<table>
<thead>
<tr>
<th><strong>历程 - 使用轮廓上限条件优化 IP 增加</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>配置历程中的<strong>条件</strong>活动时，您现在可以定义轮廓上限。此新条件类型允许您为历程路径设置最大轮廓数。达到此限制后，输入的轮廓会采用替代路径。 这样，您就可以增加投放的数量（IP 增加）。例如，您可能希望通过拆分执行来提升域上的投放数量：第 1 天发送 1000 条消息，第 2 天发送 2000 条等。</p>
<p>有关更多信息，请参阅<a href="../building-journeys/condition-activity.md#profile_cap">详细文档</a>。</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>历程 - 读取受众改进</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p><strong>增量读取</strong>选项已添加到定期<strong>读取受众</strong>活动。此选项允许您仅将自上次执行历程后进入受众的个人作为目标。第一次执行始终以所有受众成员为目标。</p>
<p>有关更多信息，请参阅<a href="../building-journeys/read-audience.md#configuring-segment-trigger-activity">详细文档</a>。
</td>
</tr>
</tbody>
</table>

### 改进

**历程**

* Journey Optimizer 步骤事件现在可以链接到 [Adobe Customer Journey Analytics](https://experienceleague.adobe.com/docs/analytics-platform/using/cja-overview/cja-overview.html?lang=zh-Hans)。**profileID** 字段，在内置的历程步骤事件架构中，现在定义为身份标识字段。[了解详情](../reports/sharing-overview.md#integration-cja)

**决策管理**

* 现在，当您更新已发布的消息中直接或间接引用的产品建议、后备产品建议、产品建议集合或产品建议决策时，更新会自动反映在相应的消息中，而无需重新发布。[了解详情](../offers/offers-e2e.md#insert-decision-in-email)

* 在模拟将针对给定测试轮廓提供哪些产品建议时，您现在可以修改默认的模拟设置，并查看与模拟对应的代码，这些代码可用于进行故障诊断。[了解详情](../offers/offer-activities/simulation.md#define-simulation-settings)

**管理**

* 管理员现在可以通过 CNAME 设置子域来编辑 PTR 记录。[了解详情](../configuration/ptr-records.md#edit-ptr-subdomains-cname)

**个性化**

* **添加到收藏夹** - 为帮助在进行个性化设置时提高效率，我们引入了“保存收藏内容”的概念。通过向收藏夹菜单添加不同属性，可以快速访问最常使用的项目。[了解详情](../personalization/personalize.md#fav)
