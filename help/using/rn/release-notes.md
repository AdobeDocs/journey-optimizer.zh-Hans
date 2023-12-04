---
solution: Journey Optimizer
product: journey optimizer
title: 发行说明
feature: Release Notes
topic: Content Management
role: User
level: Beginner, Intermediate
description: Journey Optimizer 发行说明
exl-id: 06fa956a-b500-416e-9d42-b683c328e837
source-git-commit: 299b34dec2e864fff5eb874b3fd491da80bc0c16
workflow-type: ht
source-wordcount: '418'
ht-degree: 100%

---

# 发行说明 {#release-notes}


>[!CONTEXTUALHELP]
>id="ajo_homepage_card1"
>title="新增功能？"
>abstract="**Adobe Journey Optimizer** 不断地提供新功能、对现有功能进行增强和修复错误。会在每月的最后一周将所有更改整合到发行说明中。"

[!DNL Adobe Journey Optimizer] 不断地提供新功能、对现有功能进行增强和修复错误。会在每月的最后一周将所有更改整合到发行说明中。

要查看以前的发行说明，请访问[此页面](release-notes-2023.md)。您还可以查阅[最新文档更新](documentation-updates.md)页面以了解更多更改。

[!DNL Adobe Journey Optimizer] 原生构建于 [!DNL Adobe Experience Platform] 之上并继承了其所具备的最新创新技术和改进。在 [Adobe Experience Platform 发行说明](https://experienceleague.adobe.com/docs/experience-platform/release-notes/latest.html?lang=zh-Hans){target="_blank"}中，进一步了解这些更改。

![新闻稿](../assets/do-not-localize/nl-icon.png) 立即注册订阅 [Adobe Journey Optimizer 季度新闻稿](https://www.adobe.com/subscription/Adobe_Journey_Optimizer_NL.html){target="_blank"}，每个季度都能在收件箱中直接接收最新产品更新、精彩故事、用例、提示及更多内容。

## 2023 年 10 月发行说明 {#oct-rn-2023}

### 新功能{#oct-2023-features}

此版本引入了下方列出的新功能。

<table>
<thead>
<tr>
<th><strong>沙盒工具</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>沙盒工具允许您利用包导出和导入跨多个沙盒复制对象。包可以包含单个对象或多个对象。包中包含的任何对象必须来自同一沙盒。</p>
<!--img src="../data/assets/dataset-export-setup.png"-->
<p>有关更多信息，请参阅<a href="../building-journeys/copy-to-sandbox.md">详细文档</a>。</p>
</td>
</tr>
</tbody>
</table>

<!-- table>
<thead>
<tr>
<th><strong>Composed audiences in journeys</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>You can now use audiences created in composition workflows in your journeys to target customers. Once an audience composition is published, and the audience saved, use a Read Audience activity to select this new audience in your journey canvas.</p>
<img src="assets/channel-reports.png"/>
<p>For more information, refer to the <a href="../audience/get-started-audience-orchestration.md">detailed documentation</a>.</p>
</tr>
</tbody>
</table -->

<table>
<thead>
<tr>
<th><strong>短信中的多媒体消息服务 (MMS) 内容</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>使用短信渠道时，您现在可以通过发送多媒体消息服务 (MMS) 消息（支持与客户共享图像、GIF 文件或视频）来增强沟通效果。请注意，此功能当前仅适用于 Sinch。</p>
<img src="assets/do-not-localize/mms.gif"/>
<p>有关更多信息，请参阅<a href="../sms/create-sms.md#mms-content">详细文档</a>。</p>
</tr>
</tbody>
</table>

### 改进 {#oct-2023-improvements}

此版本包含下方列出的改进。

**受众**

* 您现在可以将从 CSV 文件上传的受众定位到历程和营销活动中。[了解详情](../audience/about-audiences.md#segments-in-journey-optimizer)
* 您现在可以定位通过受众组合创建的受众，并利用历程中的扩充属性。[了解详情](../building-journeys/read-audience.md)

>[!AVAILABILITY]
>
>这些功能目前作为 Private Beta 版提供。

<!--
**Spam scoring for emails**

* When simulating an email content, a new option enables you to check how your content performs against inboxes spam filtering. This feature is currently proposed to a set of customers only (Limited Availability), and available for the Email channel.-->

**营销活动**

<!--* You can now stop a live one-time campaign, make modifications and resume it again. This improvement is available in Beta.-->
* 当您的某个营销活动发生错误时，警告图标现在会与该营销活动的状态一起显示在营销活动列表中。[了解详情](../campaigns/modify-stop-campaign.md#statuses)

**历程**

* 现在，您可以定义的最长等待持续时间为 29 天，而不是 30 天。引入此改进是为了防止等待持续时间超过 30 天的历程生命周期。这适用于：

   * [等待活动](../building-journeys/wait-activity.md)中的&#x200B;**时间量**&#x200B;字段
   * [历程属性](../building-journeys/journey-gs.md#entrance)中的&#x200B;**重入等待期**
   * [事件活动](../building-journeys/general-events.md#events-specific-time)的超时定义中的&#x200B;**等待**&#x200B;字段

<!--
**Consent in channel configuration**

* You can now select a marketing action at the channel surface level. When used in a surface, all consent policies associated with that marketing action are leveraged in order to respect the preferences of your customers.-->

**决策管理**

* 更新了与决策管理界面中的优惠上限相关的多个标签。[了解详情](../offers/offer-library/add-constraints.md#capping)

