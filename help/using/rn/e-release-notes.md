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
source-git-commit: 2a4d4511cd3ba2986b8356edd734f85f84037e02
workflow-type: tm+mt
source-wordcount: '571'
ht-degree: 26%

---

# 早期发行说明 {#e-release-notes}

[!DNL Adobe Journey Optimizer] 不断地提供新功能、对现有功能进行增强和修复错误。所有更改会在每月末整合到[发行说明](release-notes.md)中。

**以下早期发行说明可能会在正式发行日期之前有所更改，恕不另行通知。**&#x200B;在发行当日，会在[发行说明](release-notes.md)中发布链接、屏幕和更新文档。

## 2024 年 8 月早期发行说明 {#e-2024}

**发行日期**： 2024年8月20日至21日

### 新功能 {#e-features}

此版本引入了下方详述的新功能。

<table>
<thead>
<tr>
<th><strong>Marketo Engage自定义操作</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>您现在可以将 Adobe Journey Optimizer 与 Adobe Marketo Engage 集成以构建您的 B2B 用例。在历程中，新的自定义操作允许您将数据摄取到 Marketo。</p>
</td>
</tr>
</tbody>
</table>


<table>
<thead>
<tr>
<th><strong>引导式渠道设置</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>通过引导式渠道设置，您可以在统一体验中自动设置移动渠道的步骤，从而更快地开始使用Journey Optimizer。 这种设置便于快速配置营销渠道，确保所有所需资源在Experience Platform、Journey Optimizer和数据收集中随时可用。 这使您的营销团队能够立即开始创建营销活动和历程。</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>内容卡片</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>内容卡是Adobe Journey Optimizer中新增的数字消息传送功能，可直接在移动应用程序和网站上提供个性化且引人入胜的内容。 与传统推送通知不同，内容卡无缝集成到用户界面中，提供持久的非侵入式更新，以增强用户交互和体验。</p>
<p>此功能允许营销人员向用户展示相关的富媒体内容，从而提高参与度并确保查看重要消息而不会中断用户历程。</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>改进了渠道配置</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>已增强当前渠道表面功能，以实现跨所有渠道的一致方法。 您现在可以为任何渠道定义、管理和重用这些配置。</p>
<p><ul>
<li>渠道表面现在重命名为<strong>渠道配置</strong></li>
<li>从渠道配置清单中，您现在可以为所有渠道创建可重复使用的渠道配置，包括现在的Web、应用程序内消息传送或基于代码的体验</li>
<li>对象级访问控制(OLAC)现在可用于每个渠道配置，允许您决定允许哪些用户创建或使用特定配置</li>
<li>对于某些渠道，您可以创建针对多个平台的渠道配置。 以下示例是应用程序内消息传递渠道配置，可定位网页、iOS应用程序和Android应用程序。</li>
</ul></p>
<p>有关更多信息，请参阅<a href="../configuration/ip-warmup-gs.md">详细文档</a>。</p>
</td>
</tr>
</tbody>
</table>


<table>
<thead>
<tr>
<th><strong>内容片段中的变量</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>片段现在可以在<a href="../personalization/use-expression-fragments.md">表达式片段</a>和<a href="../email/use-visual-fragments.md">可视化片段</a>中使用输入变量。 您可以使用这些变量在营销活动和历程中个性化消息内容和参数。</p>
</p>
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

* 在&#x200B;**Condition**&#x200B;活动中，默认情况下，时间条件现在按小时设置，从00:00到12:00。 [了解详情](../building-journeys/condition-activity.md#time_condition)
* 现在，在构建历程时，警报将显示在下拉列表中，以便与活动警报保持一致，并提供一致的用户体验。 [了解详情](../building-journeys/troubleshooting.md#checking-for-errors-before-testing)
* 历程工具栏中的缩放选项已得到改进：缩放百分比现在可见，您现在可以轻松地将缩放值重置为100%。

**受众**

* 现在，可以将自定义上传内容（CSV 文件）中的受众用于 Privacy and Security Shield。
* 在定位自定义上传（CSV文件）受众时，您现在可以在营销活动和历程中使用文件中的属性。 这些属性在个性化编辑器和历程高级表达式编辑器中可用，用于个性化消息。

<!--
**Push channel**

* You can now add your mobile application push credentials inside Adobe Journey Optimizer channel configuration settings. Creating an App surface in Adobe Experience Platform Data Collection is no longer required.-->

<!--* The `event-id` condition is now automatically filled during test mode. -->

<!--**SMS channel**

* You can now modify existing SMS configurations.-->

<!--
**In-app channel**

* Expression fragments are now available for the In-app channel.-->
