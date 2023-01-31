---
solution: Journey Optimizer
product: journey optimizer
title: 发行说明
description: Journey Optimizer 发行说明
exl-id: 06fa956a-b500-416e-9d42-b683c328e837
source-git-commit: 4df89a36705fb53984ba04ba1ae2f45554e47f77
workflow-type: tm+mt
source-wordcount: '509'
ht-degree: 17%

---

# 发行说明 {#release-notes}

[!DNL Adobe Journey Optimizer] 不断提供新功能、现有功能增强和错误修复。 所有更改都将在每月最后一周合并到这些发行说明中。

以前的发行说明可在 [本页](release-notes-2022.md). 您还可以查阅[最新文档更新](documentation-updates.md)页面以了解更多更改。

[!DNL Adobe Journey Optimizer] 原生构建于 [!DNL Adobe Experience Platform] 之上并继承了其所具备的最新创新技术和改进。在 [Adobe Experience Platform发行说明](https://experienceleague.adobe.com/docs/experience-platform/release-notes/latest.html?lang=zh-Hans){target="_blank"}.

![新闻稿](../assets/do-not-localize/nl-icon.png) 注册 [Adobe Journey Optimizer季刊](https://www.adobe.com/subscription/Adobe_Journey_Optimizer_NL.html){target="_blank"} 今天，我们会每季度接收直接发送到收件箱的最新产品更新、精彩故事、用例、提示等。


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
<p>Adobe Experience Platform提供了一套数据卫生功能，允许您通过程序化删除消费者记录和数据集来管理存储的数据。 此功能现已可用于Adobe Journey Optimizer。 </p>
<p>您可以管理数据存储，以确保按预期使用信息，在需要修复错误数据时更新信息，并在组织策略认为有必要时删除信息。</p>
<p><strong>注意</strong>  — 目前，数据卫生功能仅适用于已购买 <strong>医疗盾</strong> 和 <strong>隐私和安全防护</strong> 附加产品。</p><p>有关更多信息，请参阅<a href="../privacy/data-hygiene.md">详细文档</a>。

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
<!--img src="assets/do-not-localize/"/-->
<p>了解如何在 <a href="https://experienceleague.adobe.com/docs/journey-optimizer-learn/tutorials/email-channel/content-templates.html">此视频</a>.
<p>有关更多信息，请参阅<a href="../email/content-templates.md">详细文档</a>。
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

* 添加 **区段鉴别** 或 **读取区段** 在历程中，命名空间现在默认使用上次使用的命名空间预填充。 请参阅 [区段鉴别](../building-journeys/segment-qualification-events.md#about-segment-qualification) 和 [读取区段](../building-journeys/read-segment.md#configuring-segment-trigger-activity) 中。

* 在历程画布中，工具栏中提供了一个新按钮，用于下载历程的屏幕截图。

**电子邮件设计工具**

* 您现在可以从 **导出HTML** 菜单。 导出的文件可在存档(.ZIP)文件中使用。

**管理**

* 新小节提供了关于在 **回复（电子邮件）** 地址和确保正确的回复管理。 [了解详情](../email/email-settings.md#reply-to-email)

* 创建或编辑时 **IP池**，关联的PTR记录现在显示在IP列表中，并将鼠标悬停在选定的IP地址上时。 [了解详情](../configuration/ip-pools.md#create-ip-pool)

* 现在，在通道表面中选择了IP池后，当将鼠标悬停在IP地址上时，可以看到PTR记录信息。 [了解详情](../email/email-settings.md#subdomains-and-ip-pools)

* 用于编辑的用户界面 [PTR记录](../configuration/ptr-records.md#edit-ptr-record) 和 [执行字段](../configuration/primary-email-addresses.md) 已更新。

* 用于创建和编辑子域的用户界面已得到改进。 [了解详情](../configuration/delegate-subdomain.md)

* 抑制列表 **最近上传** 屏幕已更新。 [了解详情](../configuration/manage-suppression-list.md#recent-uploads)

**营销活动**

* 现在，会自动生成允许执行API触发的营销活动的cURL示例请求，并在营销活动屏幕中提供该示例。 [了解详情](../campaigns/api-triggered-campaigns.md)

<!--
**Decision management**

* Additional parameters have been added in placements creation screen. They allow you to control whether an offer can be duplicated across multiple placements, and to specify if the offer's content and metadata should be included in the API response. [Learn more](../offers/offer-library/creating-placements.md)-->

<!--* It is now possible to reset the offer capping counter on a daily, weekly or monthly basis. [Learn more](../offers/offer-library/add-constraints.md#capping)-->

**个性化**

* 提供了新的帮助程序函数：formatCurrency、charCodeAt、stringToDate、toString、formatNumber和toHexString。 此外，toDateTimeOnly函数现在接受字符串、日期、长字段和整数字段类型。 [了解详情](../personalization/functions/functions.md)
