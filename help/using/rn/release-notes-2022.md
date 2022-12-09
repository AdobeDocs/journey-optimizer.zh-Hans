---
solution: Journey Optimizer
product: journey optimizer
title: 发行说明2022
description: Journey Optimizer 2022发行说明
exl-id: 0997a640-3f89-4460-ba93-ea21a9d4efc5
source-git-commit: c6498633fdfdc9442203a3bf980f1b12bd1c6a6b
workflow-type: tm+mt
source-wordcount: '3479'
ht-degree: 0%

---

# 发行说明2022 {#release-notes-2022}

本页列出了 [!DNL Journey Optimizer] 于2022年发布。


## 2022年9月版{#sept-2022-release}

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
<p>您现在可以创建动态内容，以根据条件规则调整消息的内容。</p> 
<p>条件规则是使用表达式编辑器中的可视化规则生成器创建的，您可以在其中存储这些规则以供在历程和营销活动中进一步重复使用。</p>
<img src="assets/do-not-localize/dynamic-content.gif"/>
<p>有关更多信息，请参阅 <a href="../personalization/get-started-dynamic-content.md">详细文档</a>.
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>API触发的营销活动</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>除了现有的计划营销活动之外，您现在还可以在Journey Optimizer中创建API触发的营销活动，并使用API从外部系统调用它们。</p>
<p>这允许您满足各种操作和事务性消息传递需求，如密码重置、OTP令牌等。</p>
<img src="assets/do-not-localize/api-triggered.gif"/>
<p>有关更多信息，请参阅 <a href="../campaigns/api-triggered-campaigns.md">详细文档</a>.
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
<p>通过基于属性的访问控制，管理员可以根据特定属性控制对特定对象的访问。 这些属性可以是添加到对象的元数据，如标签。 从此版本开始，管理员还可以定义只能访问特定字段和/或对象以及与这些字段和/或对象对应的数据的用户角色。</p>
<p> 基于属性的访问控制目前仅限于选定的客户，将在未来版本中部署到所有环境。</p>
<img src="assets/do-not-localize/olac.gif"/>
<p>有关更多信息，请参阅 <a href="../administration/object-based-access.md">详细文档</a>.
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
<p>借助其数据使用标签和执行(DULE)管理框架，Journey Optimizer现在可以利用Adobe Experience Platform管理策略，防止敏感字段通过自定义操作导出到第三方系统。 如果系统在自定义操作参数中标识受限字段，则会显示一个错误，阻止您发布历程。</p>
<p>数据使用标签和执行(DULE)的使用当前仅限于选定的客户，并且将在将来的版本中部署到所有环境。</p>
<p>有关更多信息，请参阅 <a href="../action/action-privacy.md">详细文档</a>.
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
<p>通过Adobe Experience Platform，您可以轻松采用和实施营销策略，以尊重客户的同意偏好。 同意策略在Adobe Experience Platform中定义。 在Journey Optimizer中，您可以将这些同意策略应用于您的自定义操作。 例如，您可以定义同意策略以排除未同意接收电子邮件、推送或短信通信的客户。
<p>自动同意强制实施当前仅适用于已购买Healthcare Shield附加产品的组织。</p>
<p>有关更多信息，请参阅 <a href="../action/consent.md">详细文档</a>.
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
<p>Journey Optimizer支持定义用户角色和访问策略以管理功能和对象的权限。 到达 <strong>Adobe Experience Cloud权限</strong>，您可以创建和管理角色，并为这些角色分配所需的资源权限。 权限还允许您管理与特定角色关联的标签、沙箱和用户。</p>
<p> 权限的使用当前仅限于选定的客户，并且将在未来版本中部署到所有环境。</p>
<p>有关更多信息，请参阅 <a href="../administration/attribute-based-access.md">详细文档</a>.
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
<p>作为Journey Optimizer用户，您现在可以通过用户界面访问系统警报，以在历程未按预期工作时获得通知。 您可以查看可用的警报并订阅它们。 如果读取区段活动在定义的时间范围内未处理任何用户档案，则此版本中提供的第一个警报将警告您。 解锁此工作流后，将会有更多内容。</p>
<p>有关更多信息，请参阅 <a href="../reports/alerts.md">详细文档</a>.
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
<p>For more information, refer to the <a href="../building-journeys/read-segment.md#configuring-segment-trigger-activity">detailed documentation</a>.
</td>
</tr>
</tbody>
</table-->

### 改进{#sept-2022-improvements}

**历程**

* 的 **实体数据集** 现在可作为Adobe Journey Optimizer中现成的数据集使用。 此查询数据集包含元数据，以丰富跟踪和反馈数据集信息。 这将帮助您使用更易理解的数据来改进报表和查询。 [了解更多](../data/datasets-query-examples.md#entity-dataset)
* 向单一历程（从事件或区段鉴别开始）添加了新护栏，以防止历程针对同一事件被错误多次触发。 用户档案重新进入现在将默认被暂时阻止5分钟。 [了解更多](../start/guardrails.md#events-g)

**管理**

* 现在，激活或取消激活允许列表时，会显示一个新警告，以详细描述每个操作的影响。 [了解更多](../configuration/allow-list.md#enable-allow-list)
* 更新了用于创建渠道表面、创建IP池、管理禁止列表和允许列表以及配置短信渠道的用户界面。
* 现在，在为给定子域创建第一个通道曲面时，处理时间将需要10分钟到10天，而使用该子域的后续曲面的处理时间最多只需3小时。 [了解更多](../configuration/channel-surfaces.md#create-channel-surface)
* 更新了用于创建登陆页面预设和登陆页面子域的用户界面。 [了解更多](../landing-pages/lp-subdomains.md)

**审核控制**

* 通过Journey Optimizer，您可以识别系统中的用户对各种服务和功能（如促销活动、历程、消息、登陆页面等）执行的操作。 审核日志资源现在包括对各种其他操作所做的更改，并会在活动发生时自动进行记录。 了解更多 [本页](../privacy/audit-logs.md).

**存档支持**

* 新 **实体数据集** 包括“模板”字段，用于导出所有渠道上已发送消息的格式和结构，以便进行存档。 [了解更多](../configuration/archiving-support.md)

**登陆页面**

* 您现在可以使用来自同一登陆页面内其他页面的上下文数据。 例如，如果将复选框链接到主登录页上的订阅列表，则可以在“谢谢”子页面上使用该订阅列表。 [了解更多](../landing-pages/lp-content.md#use-primary-page-context)

<!--* When configuring the primary page, you can now create additional data to enable storing information when the landing page is being submitted. [Learn more](../landing-pages/lp-content.md#use-additional-data)-->

<!--* You can now use information that was submitted on a landing page to send communications to your customers. For example, if a user subscribes to a given subscription list, you can leverage that information to send an email recommending other subscription lists to that user.-->

### 其他更改{#sept-2022-other}

* 历程突发模式已被Campaign快速投放模式所取代。 [了解更多](../campaigns/create-campaign.md#rapid-delivery)
* 为了提高性能，从读取区段、区段鉴别或业务事件活动开始的历程中，无法再使用体验事件字段组。 此更改仅适用于新历程。 现有行为将保留当前行为。 [了解更多](../start/guardrails.md#expression-editor)
* 已删除计划读取区段历程的1小时限制。 这些历程现在可以立即执行。




## 2022年8月版 {#aug-2022-release}

### 新功能

<table>
<thead>
<tr>
<th><strong>在Journey Optimizer中创建和管理营销活动</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>使用Journey Optimizer促销活动，通过各种渠道将一次性内容交付到特定区段。 使用历程时，设计会按顺序执行操作。 对于营销活动，可同时执行（立即执行）或根据指定的计划执行（即）操作。 </p>
<img src="assets/do-not-localize/campaigns.gif"/>
<p>了解如何在 <a href="../campaigns/get-started-with-campaigns.md">详细文档</a> 和 <a href="https://video.tv.adobe.com/v/346680">功能视频</a>.
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>向用户发送短信（正式发布）</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>您现在可以通过与 <b>辛奇</b> 或 <b>Twilio</b>.</p>
<img src="assets/do-not-localize/SMS.gif"/>
<p>在此中了解如何创建和发送短信 <a href="../sms/create-sms.md">详细文档</a>.</p>
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
<p>For more information, refer to the <a href="../building-journeys/read-segment.md#configuring-segment-trigger-activity">detailed documentation</a>.
</td>
</tr>
</tbody>
</table-->


### 改进

**报表**

* 同意策略表和图表现在可在历程全局报表中使用。 利用这些小组件，可在自定义操作中跟踪来自策略中排除的用户档案。 [了解更多](../reports/journey-global-report.md#journey-global)

   要访问最新的小组件，请注意，您必须重置不同的报表功能板。 有关功能板自定义的更多信息，请参阅 [详细文档](../reports/global-report.md).

**管理**

* 现在，可以更新用于短信渠道的主电话号码。 [了解更多](../configuration/primary-email-addresses.md)


## 2022年7月版 {#july-2022-release}

### 新功能

<table>
<thead>
<tr>
<th><strong>新的在线消息传递流程</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Journey Optimizer为Journeys中的消息创作提供了新流程。 在Journey Optimizer中，串联消息可以节省用户大量时间并简化创建和发送电子邮件、推送通知或短信的工作流程。 通过将消息作为单独步骤删除，而改为在历程画布上的某个操作中使其串联可编辑，用户将需要单击较少的按钮并导航较少的屏幕来设计和编辑其内容。</p>
<img src="assets/do-not-localize/inline.gif"/>
</td>
</tr>
</tbody>
</table>


<table>
<thead>
<tr>
<th><strong>基于属性的访问控制（有限可用性）</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>您现在可以使用标签来识别架构字段，这些标签可定义组织或数据使用范围。 管理员可以使用权限界面定义涵盖XDM架构字段的访问策略，并更好地管理给用户或用户组（内部、外部或第三方用户）的访问权限，以及管理对特定类型数据（即敏感个人数据/SPD）的访问权限。</p>
<p>基于属性的访问控制目前仅对选定用户使用，并将在未来版本中部署到所有环境。</p>
<p>有关更多信息，请参阅 <a href="../administration/attribute-based-access.md">详细文档</a>.</p>
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
<p>您现在可以从用户界面运行批量决策作业，这样我就不需要开发人员来运行批处理api作业，而且我可以缩短营销所需的时间。 此新界面允许您创建作业并管理当前/过去的作业。</p>
<img src="assets/do-not-localize/batch.gif"/>
<p>有关更多信息，请参阅 <a href="../offers/batch-delivery.md">详细文档。</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>在您的决策中自动使用性能最佳的选件（可用性有限）</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>现在，您可以在决策管理中使用个性化的优化模型系统。 这种新型模型允许您根据区段和选件性能优化和个性化选件。</p>
<p>个性化优化AI模型的使用当前仅限于选定用户，并将在未来版本中部署到所有环境。</p>
<img src="assets/do-not-localize/ai-ranking.gif"/>
<p>有关更多信息，请参阅 <a href="../offers/ranking/personalized-optimization-model.md">详细文档</a>.</p>
</td>
</tr>
</tbody>
</table>

### 改进

**历程**

* **结束旅程**  — 在历程画布中， **结束** 活动已从面板中删除。 现在，结束标记默认会添加到每个路径的末尾，且无法删除。 这项改进可更好地报告客户从历程中退出的位置，而无需历程从业者执行任何操作。 请参阅 [文档](../building-journeys/end-journey.md) 和 [功能视频](https://video.tv.adobe.com/v/345376){target=&quot;_blank&quot;}。


* 的 **配置文件时区** 默认情况下，历程属性中的选项处于未选中状态。 [了解更多](../building-journeys/timezone-management.md#timezone-from-profiles)

**消息**

* 现在提供了消息预设 **通道曲面**. [了解更多](../configuration/channel-surfaces.md)

**管理**

* **PTR记录版**  — 现在，更新PTR记录时，处理时间最多只需3小时。 [了解更多](../configuration/ptr-records.md#processing)

* **允许的列表UI**  — 您现在可以使用Journey Optimizer用户界面向允许列表添加新的电子邮件地址或域。 [了解更多](../configuration/allow-list.md)

* **允许的列表逻辑更新**  — 现在，在启用该功能后，即使列表为空，也会立即应用允许的列表逻辑。 [了解更多](../configuration/allow-list.md#logic)

* **URL跟踪参数**  — 您现在可以使用表达式编辑器在电子邮件界面中配置URL跟踪参数（即预设）。 [了解更多](../email/email-settings.md#url-tracking)

**决策管理**

* **受众大小**  — 现在，在创建决策规则、选择区段或规则以设置选件资格或将区段或规则添加到决策范围时，用户界面中会显示新的受众规模估算组件。


## 2022年6月版 {#june-2022-release}

### 新功能

<table>
<thead>
<tr>
<th><strong>向用户发送短信（可用性有限）</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>您现在可以通过与 <b>辛奇</b> 或 <b>Twilio</b>.</p>
<!--img src="assets/do-not-localize/SMS.gif"/-->
<p>短信渠道当前仅适用于一组组织（有限可用性）。 有关更多信息，请联系您的Adobe代表。</p>
<p>在此中了解如何创建和发送短信 <a href="../sms/create-sms.md">详细文档</a>.</p>
</td>
</tr>
</tbody>
</table>


<table>
<thead>
<tr>
<th><strong>通过Adobe Stock集成，更快地查找更具影响力的图像</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Adobe Stock和Adobe Journey Optimizer Email Designer集成插件为客户提供了一种轻松的方式来导航、许可和保存图像，以用于消息创作。 </br> 新 <b>查找类似的Stock照片</b> 选项还允许您查找与图像的内容、颜色和构成匹配的照片库。 </p>
<!--img src="assets/do-not-localize/stock-rn.gif"/-->
<p>有关更多信息，请参阅 <a href="../email/stock.md">详细文档</a>.</p>
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
<p>您现在可以使用电子邮件密送（盲碳拷贝）功能存储由Adobe Journey Optimizer发送的电子邮件。 在电子邮件预设中启用此选项，以便发送的每封电子邮件都会被盲目复制到密件抄送地址。</p>
<!--img src="assets/do-not-localize/bcc-rn.gif"/-->
<p>有关更多信息，请参阅 <a href="../configuration/archiving-support.md#bcc-email">详细文档</a>.</p>
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
<p>You can now use personalized optimization model systems in Decision Management. This new type of model allows you to optimize and personalize offers based on segments and offer performance.</p>
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
<th><strong>在沙箱之间复制对象</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>您现在可以将体验从Journey Optimizer沙盒重新创建到另一个沙盒，例如从非生产沙盒到生产沙盒。 此新功能可将整个历程（包括历程依赖的任何对象）从一个环境复制到另一个环境中以正确运行。 除了历程之外，您还可以复制其他组件，例如选件、消息、架构、数据集、数据源、事件和操作。</p>
<p>有关更多信息，请参阅 <a href="../building-journeys/copy-to-sandbox.md">详细文档</a>.
</td>
</tr>
</tbody>
</table>




### 改进

**决策管理**

* **HTML和JSON文件支持**  — 您现在可以将外部HTML和JSON文件从Adobe Experience Cloud资产库拖放到选件表示内容中。 [了解更多](../offers/offer-library/add-representations.md#html-json)


**电子邮件**

* **另存为模板**  — 现在，您可以将电子邮件内容另存为模板，并在创建其他消息时重复使用。 [了解更多](../email/email-templates.md)


**管理**

* **预览跟踪URL参数**  — 在配置消息预设时，如果您定义URL跟踪参数，则现在会显示结果跟踪URL的动态预览。 [了解更多](../email/email-settings.md#url-tracking)

* **消息预设版**  — 现在，更新消息预设时，处理时间最长可能只需3小时。 [了解更多](../configuration/channel-surfaces.md#edit-channel-surface)

* **IP池版本**  — 现在，更新IP池时，处理时间最长可能只需3小时。 [了解更多](../configuration/ip-pools.md#edit-ip-pool)




## 2022年5月版 {#may-2022-release}

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
<p>您现在可以设置跨渠道业务规则，以自动从消息和操作中排除发送过量请求的用户档案。</p>
<!--img src="assets/do-not-localize/frequency-rn.gif"/-->
<p>有关更多信息，请参阅 <a href="../configuration/frequency-rules.md">详细文档</a>.</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>决策管理 — 人工智能排名自动优化模型</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>现在，您可以在决策管理中使用经过培训的模型系统。 此新功能对要为给定用户档案显示的选件进行排名。</p>
<!--img src="assets/do-not-localize/optimization.gif"/-->
<p>有关更多信息，请参阅 <a href="../offers/offer-activities/configure-offer-selection.md#use-ranking-strategy">详细文档</a>.</p>
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
<th><strong>Journey Optimizer审核日志</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>您现在可以监控用户在Adobe Journey Optimizer资源上执行的操作。</p>
<!--img src="assets/do-not-localize/audit-rn.gif"/-->
<p>有关更多信息，请参阅 <a href="../privacy/audit-logs.md">详细文档</a>.</p>
</td>
</tr>
</tbody>
</table>

### 改进

**个性化**

* **用于字符隐藏的新帮助程序函数** - `mask` 帮助程序函数允许您将字符串的一部分替换为“X”字符。 [了解更多](../personalization/functions/string.md#mask)

**登陆页面**

* **没有表单的登陆页面**  — 您现在可以创建并发布不包含表单且无需访客执行任何操作的登陆页面。
* **登陆页面模板**  — 现在，您可以将登陆页面另存为模板，并在创建其他登陆页面时重复使用。 [了解更多](../landing-pages/lp-templates.md)
* **返回主页面**  — 您现在可以从同一登陆页面中的任何子页面添加指向主页面的链接。
* **自定义JavaScript支持**  — 您现在可以向登陆页面内容添加自定义JavaScript以执行高级样式或向登陆页面添加自定义行为。    [了解更多](../landing-pages/lp-custom-js.md)

**历程**

* **读取区段**  — 一次性读取区段历程现在在历程执行30天后变为“已完成”状态。 对于计划读取区段，则为上次执行该事件后的30天。 [了解更多](../building-journeys/read-segment.md)
* **表达式编辑器** - [限制](../building-journeys/functions/functionlimit.md) 函数，以限制列表的项目数。 的 [排序](../building-journeys/functions/functionsort.md) 函数现在允许您对列表对象进行排序。 还向 [disct](../building-journeys/functions/functiondistinct.md) 和 [distinctWithNull](../building-journeys/functions/functiondistinctwithnull.md) 函数。

**管理**

* **许可证使用功能板更新**  — 许可证使用情况功能板(位于 [!DNL Adobe Journey Optimizer] 用户界面现在可以准确地反映 **许可** 平均用户档案丰富度。 此量度表示形式中将显示一个删除，这意味着许可证限制现在可以正确报告。 [了解更多](../segment/license-usage.md)


## 2022年4月版 {#april-2022-release}

### 改进

**登陆页面**

* **选择启用/选择禁用复选框的新选项**  — 您现在可以在订阅登陆页面中为选择启用/选择禁用插入一个复选框。 用户需要选中要同意的复选框（选择加入），然后取消选中该复选框以删除其同意（选择退出）。 [了解更多](../landing-pages/design-lp.md#define-lp-specific-content)

* **预填充登陆页面字段**  — 现在，允许用户使用用户档案信息预填登陆页面字段。 [了解更多](../landing-pages/create-lp.md#configure-primary-page)

**决策管理**

* **Edge上的决策API** - Edge Decisioning API可以交付和渲染在决策管理中管理的个性化选件。 您可以使用决策管理用户界面(UI)或API创建选件和其他相关对象。 [了解更多](../offers/api-reference/offer-delivery-api/edge-decisioning-api.md)

**管理**

* **PTR提交持续时间**  — 现在，PTR编辑生效的持续时间为数小时。 [了解更多](../configuration/ptr-records.md#processing)

**电子邮件设计**

* **20个新电子邮件模板** 现在可用于在Journey Optimizer中设计电子邮件内容。

**用户界面**

* **Journey Optimizer UI中的上下文帮助**  — 上下文帮助链接已添加到Journey Optimizer中的多个页面。 如果可用，请单击“i”图标以查看当前功能的快速说明并访问相关文章。

**与Adobe Campaign Standard集成**

作为Adobe Campaign Standard客户，您现在可以使用Journey Optimizer发送电子邮件、推送通知和短信。 使用新的内置操作将Campaign Standard事务性消息传递功能利用到Journey Optimizer中。  [了解更多](../action/acs-action.md)

<!--
### Fixes

* Fixed an issue which caused tracking reports not to be available as the `JourneyActionId` was not properly populated. PLATIR-19854, CJM-26006
* Fixed an error on business events which could block the journey publication. CJM-25931
* Fixed an issue which could prevent images in Email Designer templates from being displayed. PLATIR-18176, CJM-25008
-->

## 2022年3月版 {#march-2022-release}

### 改进

**历程**

* 为避免统一用户档案架构中包含不必要的字段，默认情况下将不再为用户档案启用历程步骤事件架构。 如果需要，您可以激活它。 [了解更多](../reports/sharing-overview.md)
* 与导出作业相关的新步骤事件现在由Journey Optimizer发送到Adobe Experience Platform。 向文档中添加了查询示例。 [了解更多](../reports/query-examples.md)

**决策管理**

* 现在，您可以指定是否对所有用户或某个特定用户档案以及所有版面或每个版面应用选件上限。 [了解更多](../offers/offer-library/add-constraints.md#capping)
* 批量决策API允许组织在一次调用中对给定区段中的所有用户档案都使用决策管理功能。 区段中每个配置文件的选件内容会放置在AEP数据集中，该数据集可用于自定义批量工作流。 [了解更多](../offers/api-reference/offer-delivery-api/batch-decisioning-api.md)

**管理**

* 现在，您可以在消息预设级别启用/禁用电子邮件标题中的取消订阅链接，并在消息级别设置自定义取消订阅URL。 [了解更多](../configuration/channel-surfaces.md#list-unsubscribe)
* 现在，可以通过 [!DNL Journey Optimizer] 生产沙箱和非生产沙箱的界面。 [了解更多](../configuration/allow-list.md#enable-allow-list)

**个性化**

* 现在，您可以在库中保存40多个个性化表达式。 [了解更多](../personalization/personalization-library.md)

## 2022年2月版 {#feb-2022-release}

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
<p>您现在可以在Journey Optimizer中创建和设计登陆页面，并将用户引导至在线表单，在该表单中，用户可以选择加入或选择退出接收您的通信，或订阅特定服务（如新闻稿）。</p>
<p>有关更多信息，请参阅 <a href="../landing-pages/create-lp.md">详细文档</a> 相关 <a href="../landing-pages/lp-use-cases.md">示例用例</a>.</p>
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
<p>Journey Optimizer现在提供了一个库，您可以在其中访问预定义的个性化表达式。 这些表达式由管理员用户配置。</p>
<p>有关更多信息，请参阅 <a href="../personalization/personalization-library.md">详细文档</a>.</p>
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
<th><strong>传递信息以使用UTM跟踪参数跟踪消息</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>在Journey Optimizer消息内容中，您现在可以将UTM参数添加到链接：他们可以提供有关该链接的其他数据，并帮助您确定用户点击您链接的位置和原因。</p>
<p>有关更多信息，请参阅 <a href="../configuration/channel-surfaces.md#configure-email-settings">详细文档</a>.</p>
</td>
</tr>
</tbody>
</table>

### 改进

**历程**

* 为了优化性能，所有处于测试模式且一周内未触发的历程现在都将切换回草稿状态。 [了解更多](../building-journeys/testing-the-journey.md#important_notes)
* Journey Optimizer与Adobe Campaign Classic之间的集成已进行优化以提高性能。 上限默认配置已更改为4000次调用/ 5分钟。    [了解更多](../action/acc-action.md#important-notes)

**报表**

* 现在，可以根据投放的状态对其进行筛选：
   * 现在，从消息执行列表中，可以从投放列表中排除校样。
   * 从实时/全局报表中，您可以选择排除测试事件。

* 您现在可以访问有关发送时间优化数据的报表：立即发送消息的人数，以及通过1小时优化、2小时优化等方式发送消息的人数。

<!--* decision management reports are now available in Journey Optimizer. You can access the following metrics: Offers sent - Offers' impression rate - Offers' click rate - Breakdown report on Offers' sent.-->

**决策管理**

* 排名和人工智能排名现在分为一个选项卡。

## 2022年1月版 {#january-2022-release}

### 新功能

<table>
<thead>
<tr>
<th><strong>历程 — 利用用户档案上限条件优化IP提升</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>配置 <strong>条件</strong> 活动时，您现在可以定义用户档案上限。 此新条件类型允许您为历程路径设置最大用户档案数。 达到此限制后，输入的用户档案会采用替代路径。 这样，您就可以增加投放的数量（IP数量）。 例如，您可能希望通过拆分执行来提升域上的投放数量：在2000年第1天发送1000条消息，在2天发送等。</p>
<p>有关更多信息，请参阅 <a href="../building-journeys/condition-activity.md#profile_cap">详细文档</a> 相关 <a href="../building-journeys/ramp-up-deliveries-uc.md">示例用例</a>.</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>历程 — 读取区段改进</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>的 <strong>增量读取</strong> 选项已添加到循环 <strong>读取区段</strong> 活动。 此选项允许您仅定位自上次执行历程后进入区段的个人。 第一次执行始终定向所有区段成员。</p>
<p>有关更多信息，请参阅 <a href="../building-journeys/read-segment.md#configuring-segment-trigger-activity">详细文档</a>.
</td>
</tr>
</tbody>
</table>

### 改进

**历程**

* Journey Optimizer步骤事件现在可以链接到 [Adobe Customer Journey Analytics](https://experienceleague.adobe.com/docs/analytics-platform/using/cja-overview/cja-overview.html). 的 **profileID** 在内置历程步骤事件架构中，字段现在定义为标识字段。 [了解更多](../reports/sharing-overview.md#integration-cja)

**决策管理**

* 现在，当您更新发布的消息中直接或间接引用的选件、备用选件、选件收藏集或选件决策时，更新会自动反映在相应的消息中，而无需重新发布。 [了解更多](../offers/offers-e2e.md#insert-decision-in-email)

* 在模拟将针对给定测试用户档案提供哪些选件时，您现在可以修改默认的模拟设置，并查看与模拟对应的代码，这些代码可用于进行故障诊断。 [了解更多](../offers/offer-activities/simulation.md#define-simulation-settings)

**管理**

* 管理员现在可以通过设置子域的CNAME来编辑PTR记录。 [了解更多](../configuration/ptr-records.md#edit-ptr-subdomains-cname)

**个性化**

* **添加到收藏夹**  — 为帮助在使用个性化时提高效率，我们引入了“保存收藏”的概念。 通过向收藏夹菜单添加不同属性，可以快速访问最常使用的项目。 [了解更多](../personalization/personalize.md#fav)
