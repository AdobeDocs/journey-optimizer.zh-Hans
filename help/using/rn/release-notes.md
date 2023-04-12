---
solution: Journey Optimizer
product: journey optimizer
title: 发行说明
description: Journey Optimizer 发行说明
exl-id: 06fa956a-b500-416e-9d42-b683c328e837
source-git-commit: 3dffd032edb3ffda4a1bcd460d554f7ecc253a8e
workflow-type: tm+mt
source-wordcount: '1540'
ht-degree: 100%

---

# 发行说明 {#release-notes}

[!DNL Adobe Journey Optimizer] 不断地提供新功能、对现有功能进行增强和修复错误。会在每月的最后一周将所有更改整合到发行说明中。

要查看以前的发行说明，请访问[此页面](release-notes-2022.md)。您还可以查阅[最新文档更新](documentation-updates.md)页面以了解更多更改。

[!DNL Adobe Journey Optimizer] 原生构建于 [!DNL Adobe Experience Platform] 之上并继承了其所具备的最新创新技术和改进。在 [Adobe Experience Platform 发行说明](https://experienceleague.adobe.com/docs/experience-platform/release-notes/latest.html?lang=zh-Hans){target="_blank"}中，进一步了解这些更改。

![新闻稿](../assets/do-not-localize/nl-icon.png) 立即注册订阅 [Adobe Journey Optimizer 季度新闻稿](https://www.adobe.com/subscription/Adobe_Journey_Optimizer_NL.html){target="_blank"}，每个季度都能在收件箱中直接接收最新产品更新、精彩故事、用例、提示及更多内容。


## 2023 年 3 月发行说明 {#mar-2023}

以下信息可能会在发行日期之前发生更改，恕不另行通知。更新文档将在发行之日发布，其直接链接将添加到此页面。


### 新功能{#mar-2023-features}

<table>
<thead>
<tr>
<th><strong>应用程序内渠道（正式发布）</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>现在，您可以在营销活动中向应用程序用户发送个性化的应用程序内消息。使用 Journey Optimizer 设计通知并自定义消息布局、显示、文本和按钮，以创造无缝体验。</p>
<img src="assets/do-not-localize/in-app.gif"/>
<p>有关更多信息，请参阅<a href="../in-app/get-started-in-app.md">详细文档</a>。</p>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>短信点击跟踪</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>借助短信点击跟踪功能，您可以监控缩短 URL 的效果，识别点击者，并利用此数据在后续营销活动中重新定位这些客户。</p>
<img src="assets/do-not-localize/sms-tracking.gif"/>
<p>有关更多信息，请参阅<a href="../sms/create-sms.md#sms-content">详细文档</a>。</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>在您的历程中使用标记（Beta 版）</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>作为使用 Journey Optimizer 的专业人员，您现在可以使用标记组织业务对象。标记是用于进行对象分类的一种快速而简单的方法，能够改进搜索。此功能目前为 Beta 版，仅适用于历程。</p>
<p>有关更多信息，请参阅<a href="../building-journeys/tags.md">详细文档</a>。</p>
</td>
</tr>
</tbody>
</table>


### 改进 {#mar-2023-improvements}

**历程**

* 借助全新的&#x200B;**限制 API** 功能，您可以对每秒发送的事件数量设置限制，以防止外部系统或 API 出现流量激增。达到设置限制后，所有后续 API 调用将按接收到的顺序尽快排入队列并进行处理。请注意，此功能仅支持在所有沙箱中配置一个限制。[了解详情](../configuration/external-systems.md)
* 历程画布已得到改进，可提供更简单、更优质的用户体验。移除了在画布中每个路径的末尾的空占位符。现在，您只需将活动拖动到路径末尾即可添加活动。
* 在历程画布中，**结束**&#x200B;标记的标签不再使用之前的活动名称自动设置。用户可以根据需要手动添加自定义标签。
* 历程属性中的默认超时和错误持续时间已从 5 秒更改为 30 秒。[了解详情](../configuration/external-systems.md#timeout)
* 读取区段活动中的默认限制速率已从每秒 20000 条消息更改为每秒 5000 条消息。[了解详情](../building-journeys/read-segment.md#configuring-segment-trigger-activity)

<!-- 
* When adding an Email, SMS or Push action in a journey, the surface is now pre-filled, by default, with the last used surface for that channel.
* A new type of system alert has been introduced. You can now get notified when a custom action fails. [Learn more](../reports/alerts.md)
* Timeout and error management has been improved in journeys. Timeout and error paths are now always added on the canvas. A new toolbar button is available to show/hide these paths. [Learn more](../building-journeys/journey-gs.md#timeout_and_error)
* The Journey dashboard is now split in two tabs:
    * Use the **Overview** tab to access a new dashboard which displays key metrics related to your journeys.
    * Use the **Browse** tab to access list of all journeys.
-->

**决策管理**

* 为了防止与最近发布的 Adobe Experience Platform 中的标记功能混淆，决策管理标记已重命名为“收藏集限定符”。

   请注意，尽管术语“标记”不再用于“决策管理”用户界面中，但仍然在后端服务中使用，例如 API 和数据集。

* 您现在可以每日、每周或每月重置优惠上限计数器。[了解详情](../offers/offer-library/add-constraints.md#capping)

* 您还可以选择应查看哪个 Adobe Experience Platform 事件来设置 Offer Decisioning 上限。[了解详情](../offers/offer-library/add-constraints.md#capping)

* 投放位置创建屏幕中添加了更多参数。通过这些参数，您可以控制是否能在多个投放位置中复制某个优惠，并指定是否应将该优惠的内容和元数据包含在 API 响应中。[了解详情](../offers/offer-library/creating-placements.md)

**个性化**

* 现在，您可以在“表达式编辑器”中包含基于字符串的个人资料属性的默认回退文本。如果选定的属性未返回任何结果，则将显示这些值。[了解详情](../personalization/personalization-build-expressions.md#add)

**报告**

* 报表小组件功能已得到改进，允许自定义用户查看其数据的方式。通过这项改进，用户现在可以在多个可视化选项（包括图形、表格和圆环图）之间进行选择。

   要访问最新的小组件，请注意，您必须重置不同的报告仪表板。有关仪表板自定义的更多信息，请参阅[详细文档](../reports/global-report.md#modify-dashboard)。

## 2023 年 2 月发行说明 {#feb-2023}

### 新功能{#feb-2023-features}

<table>
<thead>
<tr>
<th><strong>应用程序内渠道（Beta 版）</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>现在，您可以在营销活动中向应用程序用户发送个性化的应用程序内消息。使用 Journey Optimizer 设计通知并自定义消息布局、显示、文本和按钮，以创造无缝体验。</p>
<p><strong>注意</strong> - 此功能目前为 Beta 版，仅供 Beta 版客户使用。要加入 Beta 版计划，请联系 Adobe 客户关怀团队。</p>
<img src="assets/do-not-localize/in-app.gif"/>
<p>有关更多信息，请参阅<a href="../in-app/get-started-in-app.md">详细文档</a>。</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>将 Journey Optimizer 数据集导出到云存储目标（Beta 版）</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>您现在可以与云存储位置建立实时连接，以导出数据集的内容。可用目标包括：Amazon S3 云存储、Azure Blob、Azure Data Lake 第 2 代、数据登陆区、Google 云存储、SFTP。</p>
<p><strong>注意</strong> - 此功能目前为 Beta 版，可供所有 Adobe Journey Optimizer 用户使用。如果您尚未拥有访问权限，请与 Adobe 代表联系，获取目标的访问权限。</p>
<img src="assets/do-not-localize/gif-destinations.gif"/>
<p>有关更多信息，请参阅<a href="../data/export-datasets.md">详细文档</a>。</p>
</td>
</tr>
</tbody>
</table>

<!--

<table>
<thead>
<tr>
<th><strong>Performance Measurement in campaigns</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>You can now measure the performance of your campaigns across inbound and outbound through dedicated reports. Adobe Journey Optimizer reports can retrieve additional metrics to use in the <strong>Objective</strong> tab of your campaign reports. </p>
<img src="assets/do-not-localize/performance_report.gif"/>
<p>For more information, refer to the <a href="../privacy/data-hygiene.md">detailed documentation</a>.</p>
</td>
</tr>
</tbody>
</table>

+++ Learn more about Performance Measurement

The **[!UICONTROL Objective]** tab of your Campaign report allows you to better fine-tune your deliveries' reports by targeting one specific metric. With this feature, you can effectively track and analyze your campaign's performance and make informed decisions to improve your results.

The **[!UICONTROL Objectives]** listed are linked to **[!UICONTROL Datasets]** that define a connection to a system in order to retrieve additional information. A list of pre-configured **[!UICONTROL Objectives]** is available, but you can also customize your report by adding new **[!UICONTROL Datasets]** and defining your own objectives. 

By selecting the desired Objectives, the **[!UICONTROL Performance overview]** and **[!UICONTROL Campaign objective]** widgets provide a comprehensive and insightful summary of your delivery performance, allowing you to closely monitor and evaluate the success of your campaign.

With the **[!UICONTROL Campaign objective]** widget, you can also choose to compare your primary objective against another performance metric.

Note that each widget can be resized and deleted as needed.
+++




<table>
<thead>
<tr>
<th><strong>Use Tags in your Journeys</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>As a Journey Optimizer practitioner, you can now organize your business objects using tags. Tags are a quick and easy way of classifying objects to improve search. Tags are currently only available for Journeys.</p>
</td>
</tr>
</tbody>
</table>

-->

### 改进 {#feb-2023-improvements}

**历程**

* **重新进入等待期**&#x200B;字段已添加到历程属性。使用该字段，您可以定义允许用户档案再次进入单一历程（以事件或区段鉴别开始）之前等待的时间。这可防止同一事件多次错误触发历程。默认情况下，字段设置为 5 分钟。[了解详情](../building-journeys/journey-gs.md#entrance)

* 对&#x200B;**历程开始和结束日期**&#x200B;做出了一些改进。如果您未指定开始日期，现在会在发布时自动添加。对于&#x200B;**读取区段**&#x200B;历程，您现在可以添加结束日期。这允许用户档案在到期时自动退出。[了解详情](../building-journeys/journey-gs.md#dates)

<!--

* The Journey canvas has been enhanced for a simpler and improved user experience. At the end of each path in the canvas, the empty placeholders have been removed. You can now simply add your activities by dragging them anywhere between nodes. [Learn more](../building-journeys/using-the-journey-designer.md)

* Timeout and error management has been improved in journeys. Timeout and error paths are now always added on the canvas. A new toolbar button is available to show/hide these paths. [Learn more](../building-journeys/journey-gs.md#timeout_and_error)

* A new type of system alert has been introduced. You can now get notified when a custom action fails. [Learn more](../reports/alerts.md)

* The Journey dashboard is now split in two tabs:
    * Use the **Overview** tab to access a new dashboard which displays key metrics related to your journeys.
    * Use the **Browse** tab to access list of all journeys.
-->


**管理**

* **允许列表** - 您现在可以将允许列表下载为 .csv 文件。[了解详情](../configuration/allow-list.md#download-allowed-list)

* **电子邮件平面** - 向电子邮件平面设置添加了额外的检查：如果&#x200B;**回复（电子邮件）地址**&#x200B;或&#x200B;**密送电子邮件地址**&#x200B;中使用的子域 MX 记录未正确配置，则无法再创建电子邮件平面。您必须对其进行配置或使用其他记录。[了解详情](../email/email-settings.md#reply-to-email)

* **电子邮件平面** - 在电子邮件平面设置的 **URL 跟踪参数**&#x200B;部分，每个&#x200B;**值**&#x200B;字段的限制已从 255 个字符更新为 5 KB，以便与 Adobe Analytics 跟踪兼容。[了解详情](../email/email-settings.md#url-tracking)

**决策管理**

* **投放位置** - 投放位置创建屏幕中添加了更多参数。通过这些参数，您可以控制是否能在多个投放位置中复制某个优惠，并指定是否应将该优惠的内容和元数据包含在 API 响应中。[了解详情](../offers/offer-library/creating-placements.md)

* **URL 个性化** - 现在，在将 URL 作为内容添加到优惠呈现中时，您可以使用表达式编辑器对这些 URL 进行个性化设置。[了解详情](../offers/offer-library/add-representations.md)

## 2023 年 1 月版 {#jan-2023-release}

### 新功能{#jan-2023-features}

<table>
<thead>
<tr>
<th><strong>数据安全机制</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Adobe Experience Platform 提供了一整套数据安全功能，允许您通过程序化删除客户记录和数据集来管理存储的数据。Adobe Journey Optimizer 现已提供此功能。 </p>
<p>您可以管理数据存储，以确保按预期使用信息，在需要修复错误数据时更新信息，并在组织策略认为有必要时删除信息。</p>
<p><strong>注意</strong> - 目前，数据安全功能仅适用于已购买 <strong>Healthcare Shield</strong> 和 <strong>Privacy and Security Shield</strong> 附加产品的组织。</p><p>有关更多信息，请参阅<a href="../privacy/data-hygiene.md">详细文档</a>。
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>电子邮件内容模板</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>您现在可以创建独立的内容模板，这些模板可供跨历程和营销活动使用，方便快速重复利用。</p> 
</p>
<img src="assets/do-not-localize/content-template.gif"/>
<p>通过<a href="https://experienceleague.adobe.com/docs/journey-optimizer-learn/tutorials/email-channel/content-templates.html?lang=zh-Hans">此视频</a>了解如何创建、编辑和使用内容模板。有关更多信息，请参阅<a href="../email/content-templates.md">详细文档</a>。
</p>
</td>
</tr>
</tbody>
</table>

### 改进 {#jan-2023-improvements}

**历程**

* 在历程中添加&#x200B;**区段鉴别**&#x200B;或&#x200B;**读取区段**&#x200B;时，现在会默认使用上次用过的命名空间预填充命名空间。请参阅[区段鉴别](../building-journeys/segment-qualification-events.md#about-segment-qualification)和[读取区段](../building-journeys/read-segment.md#configuring-segment-trigger-activity)部分。

* 在历程画布中，工具栏中新增了一个按钮，用于下载历程的屏幕截图。

**电子邮件设计工具**

* 您现在可以从&#x200B;**导出 HTML** 菜单导出电子邮件内容。导出的文件可使用存档 (.ZIP) 格式。

**管理**

* 在新增添的小节中，针对&#x200B;**回复（电子邮件）**&#x200B;地址和确保正确回复管理提供了建议。[了解详情](../email/email-settings.md#reply-to-email)

* 现在，创建或编辑 **IP 池**&#x200B;时，将鼠标悬停在选定的 IP 地址上，关联的 PTR 记录会显示在 IP 列表中。[了解详情](../configuration/ip-pools.md#create-ip-pool)

* 现在，在渠道界面中选择了 IP 池后，将鼠标悬停在 IP 地址上时，可以看到 PTR 记录信息。[了解详情](../email/email-settings.md#subdomains-and-ip-pools)

* 用于编辑 [PTR 记录](../configuration/ptr-records.md#edit-ptr-record)和[执行字段](../configuration/primary-email-addresses.md)的用户界面已更新。

* 用于创建和编辑子域的用户界面已得到改进。[了解详情](../configuration/delegate-subdomain.md)

* 黑名单&#x200B;**最近上传**&#x200B;屏幕已更新。[了解详情](../configuration/manage-suppression-list.md#recent-uploads)

**营销活动**

* 现在会自动生成一个示例 cURL 请求，允许执行 API 触发的营销活动，并可在营销活动屏幕中获得。[了解详情](../campaigns/api-triggered-campaigns.md)


**个性化**

* 提供了新的辅助函数：formatCurrency、charCodeAt、stringToDate、toString、formatNumber 和 toHexString。此外，toDateTimeOnly 函数现在可接受字符串、日期、长字段和整数字段类型。[了解详情](../personalization/functions/functions.md)
