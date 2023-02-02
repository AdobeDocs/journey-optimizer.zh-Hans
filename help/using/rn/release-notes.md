---
solution: Journey Optimizer
product: journey optimizer
title: 发行说明
description: Journey Optimizer 发行说明
exl-id: 06fa956a-b500-416e-9d42-b683c328e837
source-git-commit: ad0ca954d2ba15293bdde2715a7aaed62b040cce
workflow-type: tm+mt
source-wordcount: '509'
ht-degree: 92%

---

# 发行说明 {#release-notes}

[!DNL Adobe Journey Optimizer] 不断地提供新功能、对现有功能进行增强和修复错误。会在每月的最后一周将所有更改整合到发行说明中。

要查看以前的发行说明，请访问[此页面](release-notes-2022.md)。您还可以查阅[最新文档更新](documentation-updates.md)页面以了解更多更改。

[!DNL Adobe Journey Optimizer] 原生构建于 [!DNL Adobe Experience Platform] 之上并继承了其所具备的最新创新技术和改进。在 [Adobe Experience Platform 发行说明](https://experienceleague.adobe.com/docs/experience-platform/release-notes/latest.html?lang=zh-Hans){target="_blank"}中，进一步了解这些更改。

![新闻稿](../assets/do-not-localize/nl-icon.png) 立即注册订阅 [Adobe Journey Optimizer 季度新闻稿](https://www.adobe.com/subscription/Adobe_Journey_Optimizer_NL.html){target="_blank"}，每个季度都能在收件箱中直接接收最新产品更新、精彩故事、用例、提示及更多内容。


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
<p>您现在可以创建独立的内容模板，这些模板可以跨历程和促销活动使用，以便快速重复使用。</p> 
</p>
<img src="assets/do-not-localize/content-template.gif"/>
<p>了解如何在 <a href="https://experienceleague.adobe.com/docs/journey-optimizer-learn/tutorials/email-channel/content-templates.html">此视频</a>. 有关更多信息，请参阅<a href="../email/content-templates.md">详细文档</a>。
</p>
</td>
</tr>
</tbody>
</table>

### 改进 {#jan-2023-improvements}

**历程**

<!--
* The **Re-entrance wait period** field has been added to the journey properties. This field allows you to define the time to wait before allowing a profile to enter the journey again in unitary journeys (starting with an event or a segment qualification). This prevents journeys from being erroneously triggered multiple times for the same event. By default the field is set to 5 minutes. [Learn more](../building-journeys/journey-gs.md#entrance)

* Improvements have been made for **journey start and end dates**. If you have not specified a start date, it is now automatically added at publication time. For **Read segment** journeys, you can now add an end date. This allows profiles to exit automatically when the date is reached. [Learn more](../building-journeys/journey-gs.md#dates)
-->

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

<!--
**Decision management**

* Additional parameters have been added in placements creation screen. They allow you to control whether an offer can be duplicated across multiple placements, and to specify if the offer's content and metadata should be included in the API response. [Learn more](../offers/offer-library/creating-placements.md)-->

<!--* It is now possible to reset the offer capping counter on a daily, weekly or monthly basis. [Learn more](../offers/offer-library/add-constraints.md#capping)-->

**个性化**

* 提供了新的辅助函数：formatCurrency、charCodeAt、stringToDate、toString、formatNumber 和 toHexString。此外，toDateTimeOnly 函数现在可接受字符串、日期、长字段和整数字段类型。[了解详情](../personalization/functions/functions.md)
