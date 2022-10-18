---
solution: Journey Optimizer
product: journey optimizer
title: 发行说明
description: Journey Optimizer 发行说明
exl-id: 06fa956a-b500-416e-9d42-b683c328e837
source-git-commit: 63c52f04da9fd1a5fafc36ffb5079380229f885e
workflow-type: tm+mt
source-wordcount: '1101'
ht-degree: 90%

---

# 发行说明 {#release-notes}

此页面列出了 [!DNL Journey Optimizer] 的所有新增功能和改进。您还可以查阅[最新文档更新](documentation-updates.md)页面以了解更多更改。

[!DNL Adobe Journey Optimizer] 原生构建于 [!DNL Adobe Experience Platform] 之上并继承了其所具备的最新创新技术和改进。在 [Adobe Experience Platform 发行说明](https://experienceleague.adobe.com/docs/experience-platform/release-notes/latest.html?lang=zh-Hans){target=&quot;_blank&quot;} 中，进一步了解这些变更。

![新闻稿](../assets/do-not-localize/nl-icon.png) 立即注册 [Adobe Journey Optimizer 季度新闻稿](https://www.adobe.com/subscription/Adobe_Journey_Optimizer_NL.html){target=&quot;_blank&quot;}邮件，每个季度就能在收件箱中直接接收最新产品更新、精彩故事、用例、提示及更多内容。


## 2022 年 10 月 {#oct-2022-release}

### 改进{#oct-2022-improvements}

**历程**

* 的 **重复时强制重入** 选项已添加到定期读取区段计划参数中。 利用此选项，可让历程中仍存在的所有用户档案在下次执行时自动退出该历程。 停用选项后，用户档案必须先完成历程，然后才能再次进入另一个实例。 [了解详情](../building-journeys/read-segment.md#configuring-segment-trigger-activity)

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
<p>您现在可以创建动态内容，以根据条件规则调整消息的内容。</p> 
<p>条件规则是使用表达式编辑器中的可视化规则生成器创建的，您可以在其中存储这些规则以供在历程和营销活动中进一步重复使用。</p>
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
<p>作为 Journey Optimizer 用户，您现在可以通过用户界面访问系统警报，在历程工作异常时获得通知。您可以查看可用的警报并订阅它们。如果读取区段活动在定义的时间范围内未处理任何用户档案，则此版本中提供的第一个警报将会警告您。解锁此工作流程后，将会有更多内容。</p>
<p>有关更多信息，请参阅<a href="../reports/alerts.md">详细文档</a>。
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

* 现在，**实体数据集**&#x200B;是 Adobe Journey Optimizer 中包含的现成可用的数据集。此查询数据集包含元数据，可用于丰富跟踪和反馈数据集信息。这有助于您使用更易理解的数据来改进报表和查询。[了解详情](../start/datasets-query-examples.md#entity-dataset)
* 向单一历程（从事件或区段鉴别开始）添加了新护栏，以防止历程因同一事件被错误地触发多次。默认情况下，重新进入用户档案会被暂时阻止 5 分钟。[了解详情](../start/guardrails.md#events-g)

**管理**

* 激活或停用允许列表时，现在会显示新的警告，详细说明每个操作的影响。[了解详情](../configuration/allow-list.md#enable-allow-list)
* 更新了用于创建渠道界面、创建 IP 池、管理禁止列表和允许列表以及配置短信渠道的用户界面。
* 现在，为给定子域创建第一个渠道界面时，处理时间需要 10 分钟到 10 天，而使用该子域的后续界面的处理时间最多只需 3 小时。[了解详情](../configuration/channel-surfaces.md#create-channel-surface)

<!--* Now when downloading the suppression list as a CSV file, you can choose the file that was previously generated, or generate a new file.-->
* 更新了用于创建登陆页面预设和登陆页面子域的用户界面。[了解详情](../configuration/lp-subdomains.md)

**审核控制**

* 借助 Journey Optimizer，您可以识别用户在系统中对各种服务和功能（如营销活动、历程、消息、登陆页面等）执行的操作。审核日志资源现在包括对各种其他操作所做的更改，并会在活动发生时自动进行记录。请参阅[此页面](../privacy/audit-logs.md)以了解详情。

**存档支持**

* 新的&#x200B;**实体数据集**&#x200B;包括“模板”字段，用于导出所有渠道上已发送消息的格式和结构，以便进行存档。[了解详情](../configuration/archiving-support.md)

**登陆页面**

* 您现在可以在同一登陆页面内使用来自其他页面的上下文数据。例如，如果将复选框链接到主登录页上的订阅列表，则可以在“感谢”子页面上使用该订阅列表。[了解详情](../landing-pages/lp-content.md#use-primary-page-context)

<!--* When configuring the primary page, you can now create additional data to enable storing information when the landing page is being submitted. [Learn more](../landing-pages/lp-content.md#use-additional-data)-->

<!--* You can now use information that was submitted on a landing page to send communications to your customers. For example, if a user subscribes to a given subscription list, you can leverage that information to send an email recommending other subscription lists to that user.-->

### 其他更改{#sept-2022-other}

* 历程突发模式已被 Campaign 快速投放模式取代。[了解详情](../campaigns/create-campaign.md#rapid-delivery)
* 为了提高性能，从读取区段、区段鉴别或业务事件活动开始的历程中，无法再使用体验事件字段组。此更改仅适用于新历程。现有历程将保留当前行为。[了解详情](../start/guardrails.md#expression-editor)
* 已移除计划读取区段历程的 1 小时限制。这些历程现在可以毫不延迟地执行。

