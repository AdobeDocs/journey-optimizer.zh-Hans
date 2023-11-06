---
solution: Journey Optimizer
product: journey optimizer
title: 发行说明
description: Journey Optimizer 早期发行说明
feature: Release Notes
topic: Content Management
role: User
level: Beginner, Intermediate
hide: true
hidefromtoc: true
exl-id: 6e7d1300-8efd-4fdc-90e3-3ccdc3babd2f
source-git-commit: 004eb41b084f32993ec437f589e4e3d2cf7500d3
workflow-type: ht
source-wordcount: '350'
ht-degree: 100%

---

# 早期发行说明 {#e-release-notes}

[!DNL Adobe Journey Optimizer] 不断地提供新功能、对现有功能进行增强和修复错误。所有更改会在每月的最后一周整合到[发行说明](release-notes.md)中。

以下早期发行说明可能会在正式发行日期之前发生更改，恕不另行通知。链接、屏幕和更新文档，会在发行之日发布于[发行说明](release-notes.md)中。

## 2023 年 10 月早期发行说明 {#oct-rn-2023}

**发行日期**：2023 年 10 月 25 日至 26 日

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
<!--p>For more information, refer to the <a href="../audience/get-started-audience-orchestration.md">detailed documentation</a>.</p-->
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
<th><strong>短信中的多媒体消息服务 (MMS) 内容（Beta 版） </strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>使用短信渠道时，您现在可以通过发送多媒体消息服务 (MMS) 消息（支持与客户共享图像、GIF 文件或视频）来增强沟通效果。请注意，此功能目前仅在支持 Sinch 的 Beta 版中可用。</p>
<!--img src="assets/channel-reports.png"/-->
<!--p>For more information, refer to the <a href="../in-app/get-started-in-app.md">detailed documentation</a>.</p-->
</tr>
</tbody>
</table>

### 改进 {#oct-2023-improvements}

此版本包含下方列出的改进。

**受众**

* 您现在可以将从 CSV 文件上传的受众定位到历程和营销活动中。
* 您现在可以定位通过受众组合创建的受众，并利用历程中的扩充属性。

>[!AVAILABILITY]
>
>这些功能目前作为 Private Beta 版提供。

<!--
**Spam scoring for emails**

* When simulating an email content, a new option enables you to check how your content performs against inboxes spam filtering. This feature is currently proposed to a set of customers only (Limited Availability), and available for the Email channel.-->

**营销活动**

<!--* You can now stop a live one-time campaign, make modifications and resume it again. This improvement is available in Beta.-->
* 当您的某个营销活动出现错误时，警告图标现在会与该营销活动的状态一起显示在营销活动列表中。

**历程**

* 现在，您可以定义的最长等待持续时间为 29 天，而不是 30 天。这适用于：

   * [等待活动](../building-journeys/wait-activity.md)中的&#x200B;**时间量**&#x200B;字段
   * [历程属性](../building-journeys/journey-gs.md#entrance)中的&#x200B;**重入等待期**
   * [常规](../building-journeys/general-events.md#events-specific-time)和[反应](../building-journeys/reaction-events.md)事件超时定义中的&#x200B;**等待**&#x200B;字段。

**渠道配置中的同意**

* 现在，您可以在渠道表面级别选择营销操作。在表面中使用时，将利用与该营销操作关联的所有同意策略，以尊重客户的偏好。

**决策管理**

* 更新了与决策管理界面中优惠上限相关的多个标签。
