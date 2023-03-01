---
solution: Journey Optimizer
product: journey optimizer
title: 发行说明
description: Journey Optimizer 发行说明
exl-id: 06fa956a-b500-416e-9d42-b683c328e837
source-git-commit: 8de851b42b92ca4632000698fa78278671dd848b
workflow-type: tm+mt
source-wordcount: '919'
ht-degree: 60%

---

# 发行说明 {#release-notes}

[!DNL Adobe Journey Optimizer] 不断地提供新功能、对现有功能进行增强和修复错误。会在每月的最后一周将所有更改整合到发行说明中。

要查看以前的发行说明，请访问[此页面](release-notes-2022.md)。您还可以查阅[最新文档更新](documentation-updates.md)页面以了解更多更改。

[!DNL Adobe Journey Optimizer] 原生构建于 [!DNL Adobe Experience Platform] 之上并继承了其所具备的最新创新技术和改进。在 [Adobe Experience Platform 发行说明](https://experienceleague.adobe.com/docs/experience-platform/release-notes/latest.html?lang=zh-Hans){target="_blank"}中，进一步了解这些更改。

![新闻稿](../assets/do-not-localize/nl-icon.png) 立即注册订阅 [Adobe Journey Optimizer 季度新闻稿](https://www.adobe.com/subscription/Adobe_Journey_Optimizer_NL.html){target="_blank"}，每个季度都能在收件箱中直接接收最新产品更新、精彩故事、用例、提示及更多内容。

## 2023年2月发行说明 {#feb-2023}

### 新功能{#feb-2023-features}

<table>
<thead>
<tr>
<th><strong>应用程序内渠道（测试版）</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>现在，您可以在促销活动中向应用程序用户发送个性化的应用程序内消息。 使用Journey Optimizer设计通知并自定义消息布局、显示、文本和按钮以创建无缝体验。</p>
<p><strong>注意</strong>  — 此功能目前为测试版，仅供测试版客户使用。 要加入 Beta 版计划，请联系 Adobe 客户关怀团队。</p>
<img src="assets/do-not-localize/in-app.gif"/>
<p>有关更多信息，请参阅<a href="../in-app/get-started-in-app.md">详细文档</a>。</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>将Journey Optimizer数据集导出到Cloud Storage Destinations (beta)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>您现在可以与云存储位置建立实时连接，以导出数据集的内容。 可用的目标包括：Amazon S3 Cloud Storage、Azure Blob、Azure Data Lake Gen 2、Data Landing Zone、Google Cloud Storage、SFTP。</p>
<p><strong>注意</strong>  — 此功能目前为测试版，可供所有Adobe Journey Optimizer用户使用。 如果您还没有访问权限，请与您的Adobe代表合作以获取对目标的访问权限。</p>
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

* 此 **重新进入等待期** 字段已添加到历程属性。 此字段允许您定义允许用户档案在单一历程中再次进入历程之前的等待时间（从事件或区段资格开始）。 这样可防止同一事件多次错误地触发历程。 默认情况下，该字段设置为5分钟。 [了解详情](../building-journeys/journey-gs.md#entrance)

* 在以下方面做出了改进： **历程开始和结束日期**. 如果尚未指定开始日期，则会在发布时自动添加该日期。 对象 **读取区段** 历程，您现在可以添加结束日期。 这允许用户档案在到达日期时自动退出。 [了解详情](../building-journeys/journey-gs.md#dates)

<!--

* The Journey canvas has been enhanced for a simpler and improved user experience. At the end of each path in the canvas, the empty placeholders have been removed. You can now simply add your activities by dragging them anywhere between nodes. [Learn more](../building-journeys/using-the-journey-designer.md)

* Timeout and error management has been improved in journeys. Timeout and error paths are now always added on the canvas. A new toolbar button is available to show/hide these paths. [Learn more](../building-journeys/journey-gs.md#timeout_and_error)

* A new type of system alert has been introduced. You can now get notified when a custom action fails. [Learn more](../reports/alerts.md)

* The Journey dashboard is now split in two tabs:
    * Use the **Overview** tab to access a new dashboard which displays key metrics related to your journeys.
    * Use the **Browse** tab to access list of all journeys.
-->


**管理**

* **允许列表**  — 您现在可以将允许列表下载为.csv文件。 [了解详情](../configuration/allow-list.md#download-allowed-list)

* **电子邮件表面**  — 已对电子邮件表面设置添加了其他检查：如果子域的MX记录用于 **回复（电子邮件）地址** 或在 **密件抄送电子邮件地址** 配置不正确，无法再创建电子邮件表面。 您必须配置它或使用其他服务器。 [了解详情](../email/email-settings.md#reply-to-email)

* **电子邮件表面**  — 在 **URL跟踪参数** 电子邮件表面设置部分，每个部分的 **值** 为了与Adobe Analytics跟踪兼容，字段已从255个字符更新为5 KB。 [了解详情](../email/email-settings.md#url-tracking)

**决策管理**

<!--
* **Placements** - Additional parameters have been added in placements creation screen. They allow you to control whether an offer can be duplicated across multiple placements, and to specify if the offer's content and metadata should be included in the API response. [Learn more](../offers/offer-library/creating-placements.md)
-->

* **URL个性化**  — 将URL作为内容添加到优惠的表示法时，您现在可以使用表达式编辑器对这些URL进行个性化设置。 [了解详情](../offers/offer-library/add-representations.md)

<!--
* **Capping** - You can now reset the offer capping counter on a daily, weekly or monthly basis. [Learn more](../offers/offer-library/add-constraints.md#capping)

* **Capping** - You can now choose which Adobe Experience Platform event should be looked at for offer decisioning capping. [Learn more](../offers/offer-library/add-constraints.md#capping)
-->

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
