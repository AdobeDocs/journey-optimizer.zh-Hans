---
solution: Journey Optimizer
product: journey optimizer
title: 发行说明
description: Journey Optimizer 早期发行说明
feature: Release Notes
topic: Content Management
hide: true
hidefromtoc: true
exl-id: 6e7d1300-8efd-4fdc-90e3-3ccdc3babd2f
source-git-commit: 428e08ca712724cb0b3453681bee1c7e86ce49dc
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---

# 早期发行说明 {#e-release-notes}

[!DNL Adobe Journey Optimizer] 不断地提供新功能、对现有功能进行增强和修复错误。所有更改会在每月末整合到[发行说明](release-notes.md)中。

**以下早期发行说明可能会在正式发行日期之前有所更改，恕不另行通知。**&#x200B;在发行当日，会在[发行说明](release-notes.md)中发布链接、屏幕和更新文档。

## 2024 年 8 月早期发行说明 {#e-2024}

**发布日期**：2024 年 8 月 20 日 - 21 日

### 新功能 {#e-features}

此版本引入了下方详述的新功能。

<table>
<thead>
<tr>
<th><strong>内容片段中的变量</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>片段现在可以在<a href="../personalization/use-expression-fragments.md">表达式片段</a>和<a href="../email/use-visual-fragments.md">可视化片段</a>中使用输入变量。您可以使用这些变量在营销活动和历程中个性化消息内容和参数。</p>
</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>IP 预热工作流</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>发布日期：8 月 13 日</p>
<p>如果使用全新的 IP 地址发送电子邮件，现在可以直接从用户界面轻松执行 IP 预热工作流。Adobe Journey Optimizer 提供了一种标准化的高效方法来预热 IP 地址，该方法遵循最佳实践以期实现最佳可投放性。</p>
<p>有关更多信息，请参阅<a href="../configuration/ip-warmup-gs.md">详细文档</a>。</p>
</td>
</tr>
</tbody>
</table>

<!--table>
<thead>
<tr>
<th><strong>Extended personalization data - Beta</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>You can now lookup and fetch data values within Adobe Experience Platform datasets, and use these values to build conditions in Adobe Journey Optimizer. You can leverage data from a lookup dataset when a relationship has been defined using an attribute inside of an array of objects. You can specify non-profile enabled datasets for lookup. Once enabled, you can use a profile attribute as a join key to the specified dataset to retrive further data for personalization.</p>
<p>This capability is currently available as a public beta.</p>
</td>
</tr>
</tbody>
</table-->

### 改进 {#e-improvements}

此版本包含下方列出的改进。

**历程**

* 现在，在&#x200B;**条件**&#x200B;活动中，时间条件默认按小时设置，从 00:00 到 12:00。[了解详情](../building-journeys/condition-activity.md#time_condition)
* 在构建历程时，警报现在会显示在下拉列表中，以与活动警报保持一致并带来一致的用户体验。[了解详情](../building-journeys/troubleshooting.md#checking-for-errors-before-testing)
* 历程工具栏中的缩放选项已得到改进：缩放百分比现在可见，并且可以轻松地将缩放值重置为 100%。

**受众**

* 现在，可以将自定义上传内容（CSV 文件）中的受众用于 Privacy and Security Shield。
* 在定位自定义上传（CSV 文件）受众时，您现在可以在营销活动和历程中使用文件中的属性。这些属性在个性化编辑器中可用，用于个性化您的消息和旅程高级表达式编辑器。


<!--
**Push channel**

* You can now add your mobile application push credentials inside Adobe Journey Optimizer channel configuration settings. Creating an App surface in Adobe Experience Platform Data Collection is no longer required.-->

<!--* The `event-id` condition is now automatically filled during test mode. -->

<!--**SMS channel**

* You can now modify existing SMS configurations.-->

<!--
**In-app channel**

* Expression fragments are now available for the In-app channel.-->
