---
title: 发行说明
description: Journey Optimizer 发行说明
exl-id: 06fa956a-b500-416e-9d42-b683c328e837
source-git-commit: d3895b0d6a73c1618f417d28e971c5b3c9b89b4e
workflow-type: tm+mt
source-wordcount: '961'
ht-degree: 19%

---

# 发行说明 {#release-notes}

此页面列出了 [!DNL Journey Optimizer] 的所有新增功能和改进。您还可以查阅[最新文档更新](documentation-updates.md)页面以了解更多更改。

[!DNL Adobe Journey Optimizer] 原生构建于 [!DNL Adobe Experience Platform] 之上并继承了其所具备的最新创新技术和改进。在 [Adobe Experience Platform 发行说明](https://experienceleague.adobe.com/docs/experience-platform/release-notes/latest.html?lang=zh-Hans){target=&quot;_blank&quot;} 中，进一步了解这些变更。

![新闻稿](../assets/do-not-localize/nl-icon.png) 立即注册 [Adobe Journey Optimizer 季度新闻稿](https://www.adobe.com/subscription/Adobe_Journey_Optimizer_NL.html){target=&quot;_blank&quot;}邮件，每个季度就能在收件箱中直接接收最新产品更新、精彩故事、用例、提示及更多内容。

## 2022 年 9 月版{#sept-2022-release}

### 新功能{#sept-2022-features}


<!--
<table>
<thead>
<tr>
<th><strong>Dynamic content & new conditional rule builder</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>You can now create dynamic content to adapt the content of your messages based on conditional rules.</p> 
<p>Conditional rules are created using a visual rule builder within the Expression Editor, where you can store them for further reuse across your journeys and campaigns.</p>
<img src="assets/do-not-localize/dynamic-content.gif"/>
<p>For more information, refer to the <a href="../personalization/get-started-dynamic-content.md">detailed documentation</a>.
</td>
</tr>
</tbody>
</table>
-->

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
<p>通过基于属性的访问控制，管理员可以根据特定属性控制对特定对象的访问。 这些属性可以是添加到对象的元数据，如标签。 从此版本开始，管理员还可以定义只能访问特定字段和/或对象以及与这些字段和/或对象对应的数据的用户角色。</p>
<p> 基于属性的访问控制目前仅限于选定的客户，将在未来版本中部署到所有环境。</p>
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
<p>凭借其数据使用标签和执行(DULE)管理框架，Journey Optimizer现在可以利用Adobe Experience Platform管理策略来防止敏感字段通过自定义操作导出到第三方系统。 如果系统在自定义操作参数中标识受限字段，则会显示一个错误，阻止您发布历程。</p>
<p>数据使用标签和执行(DULE)的使用当前仅限于选定的客户，并且将在将来的版本中部署到所有环境。</p>
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
<p>Adobe Experience Platform允许您轻松地采用和实施营销策略，以尊重客户的同意偏好。 同意策略在Adobe Experience Platform中定义。 在Journey Optimizer中，您可以将这些同意策略应用于自定义操作。 例如，您可以定义同意策略以排除未同意接收电子邮件、推送或短信通信的客户。
<p>自动同意强制实施当前仅适用于已购买Healthcare Shield附加产品的组织。</p>
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
<p>Journey Optimizer支持定义用户角色和访问策略以管理功能和对象的权限。 到达 <strong>Adobe Experience Cloud权限</strong>，您可以创建和管理角色，并为这些角色分配所需的资源权限。 权限还允许您管理与特定角色关联的标签、沙箱和用户。</p>
<p> 权限的使用当前仅限于选定的客户，并且将在未来版本中部署到所有环境。</p>
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
<p>作为Journey Optimizer用户，您现在可以通过用户界面访问系统警报，以在历程未按预期工作时获得通知。 您可以查看可用的警报并订阅它们。 如果读取区段活动在定义的时间范围内未处理任何用户档案，则此版本中提供的第一个警报将警告您。 解锁此工作流后，将会有更多内容。</p>
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

* 的 **实体数据集** 现在可用作Adobe Journey Optimizer中现成的数据集。 此查询数据集包含元数据，以丰富跟踪和反馈数据集信息。 这将帮助您使用更易理解的数据来改进报表和查询。 [了解详情](../start/datasets-query-examples.md#entity-dataset)
* 向单一历程（从事件或区段鉴别开始）添加了新护栏，以防止历程针对同一事件被错误多次触发。 用户档案重新进入现在将默认被暂时阻止5分钟。 [了解详情](../start/guardrails.md#events-g)

**管理**

* 现在，在启用或禁用允许列表时，会显示一个新警告，以详细描述每个操作的影响。 [了解详情](../configuration/allow-list.md#enable-allow-list)
* 更新了用于创建渠道表面、创建IP池、管理禁止列表和允许列表以及配置短信渠道的用户界面。
<!--* Now when creating the first channel surface for a given subdomain, the processing time will take 10 minutes to 10 days, and only up to 3 hours for subsequent surfaces using that subdomain. Learn more
* Now when downloading the suppression list as a CSV file, you can choose the file that was previously generated, or generate a new file.
* The user interface for creating landing page presets and landing page subdomains has been improved. Learn more -->

**审核控制**

* 通过Journey Optimizer，您可以识别系统中的用户对各种服务和功能（如促销活动、历程、消息、登陆页面等）执行的操作。 审核日志资源现在包括对各种其他操作所做的更改，并会在活动发生时自动进行记录。 请参阅[此页面](../privacy/audit-logs.md)以了解详情。

**存档支持**

* 新 **实体数据集** 包括“模板”字段，用于导出所有渠道上已发送消息的格式和结构，以便进行存档。 [了解详情](../configuration/archiving-support.md)

**登陆页面**

* 您现在可以使用来自同一登陆页面内其他页面的上下文数据。 例如，如果将复选框链接到主登录页上的订阅列表，则可以在“谢谢”子页面上使用该订阅列表。 [了解详情](../landing-pages/lp-content.md#use-primary-page-context)

* 现在，在配置主页面时，您可以创建其他数据，以便在提交登陆页面时能够存储信息。 [了解详情](../landing-pages/lp-content.md#use-additional-data)

<!--* You can now use information that was submitted on a landing page to send communications to your customers. For example, if a user subscribes to a given subscription list, you can leverage that information to send an email recommending other subscription lists to that user.-->

### 其他更改{#sept-2022-other}

* 历程突发模式已被Campaign快速投放模式所取代。 [了解详情](../campaigns/create-campaign.md#rapid-delivery})
* 为了提高性能，从读取区段、区段鉴别或业务事件活动开始的历程中，无法再使用体验事件字段组。 此更改仅适用于新历程。 现有行为将保留当前行为。 [了解详情](../start/guardrails.md#expression-editor)
* 已删除计划读取区段历程的1小时限制。 这些历程现在可以立即执行。

