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
source-git-commit: 28a4f04ebcda27213d3bac763fb9bea8ea4a0146
workflow-type: tm+mt
source-wordcount: '634'
ht-degree: 100%

---

# 早期发行说明 {#e-release-notes}

[!DNL Adobe Journey Optimizer] 不断地提供新功能、对现有功能进行增强和修复错误。所有更改会在每月的最后一周整合到[发行说明](release-notes.md)中。

以下早期发行说明可能会在正式发行日期之前发生更改，恕不另行通知。链接、屏幕和更新文档，会在发行之日发布于[发行说明](release-notes.md)中。

## 2023 年 9 月早期发行说明 {#sept-rn-2023}

**发行日期**：2023 年 9 月 26 日至 27 日

### 新功能{#sept-2023-features}

此版本引入了下方列出的新功能。


<table>
<thead>
<tr>
<th><strong>整合的渠道报告</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>渠道报告功能为分析师和营销人员在渠道级别提供了流量和参与量度的全面概述。要访问“报告”菜单，您必须具有“查看渠道报告”权限。</p>
<img src="assets/channel-reports.png"/>
<!--p>For more information, refer to the <a href="../in-app/get-started-in-app.md">detailed documentation</a>.</p-->
</tr>
</tbody>
</table>


<table>
<thead>
<tr>
<th><strong>数据集导出目标 (GA)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>现在，一般可以将 Journey Optimizer 数据集导出到云存储目标。通过此功能，您可以与云存储位置建立实时连接，以导出数据集的内容。</p>
<img src="../data/assets/dataset-export-setup.png">
<!--p>For more information, refer to the <a href="../audience/get-started-audience-orchestration.md">detailed documentation</a>.</p-->
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>基于单个沙盒的移动应用程序凭据存储</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>这项新功能允许您轻松管理推送凭据，并将其与应用程序表面中的专用沙盒关联。</p>
<p>有关更多信息，请参阅<a href="../in-app/inapp-configuration.md">详细文档</a>。</p>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>计算属性</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>计算属性使您可以通过直观的用户界面轻松地将事件数据汇总到配置文件属性中，以增强基于行为的分段、个性化和激活。借助此功能，您可以以自助方式创建计算属性，管理这些属性，并在分段、实时客配置文件目标或 Journey Optimizer 中进行使用。<br/><br/>
此外，计算属性简化了分段和历程工作流，帮助您完美投放相关体验。有关更多信息，请参阅<a href="https://experienceleague.adobe.com/docs/experience-platform/profile/computed-attributes/overview.html?lang=zh-Hans">详细文档</a>。</p>
<img src="assets/do-not-localize/computed-attributes.gif">
</tr>
</tbody>
</table>


### 改进 {#sept-2023-improvements}

此版本包含下方列出的改进。

<!--**Audiences**

* You can now target audiences uploaded from a CSV file into journeys and campaigns.
* You can now target audiences resulting from composition workflows into journeys. -->

**个性化**

* 除了可视片段之外，现在还可以通过表达式编辑器从 Journey Optimizer 界面创建、保存和重用表达式片段。表达式片段替换以前保存的表达式。

**警报**

* 一种新型的系统警报现已推出。现在，您会在读取受众失败时收到通知。

**Web 渠道**

* 现在可以在 Web 设计器可视编辑器中创作单页应用程序 (SPA)，该编辑器允许您选择要应用网页修改的特定视图。视图可定义为整个网站或网站上的一组可视化元素，例如主页、整个产品网站或所有结账页面上的投放首选项框架。要在 SPA 上创建和运行 Adobe Journey Optimizer Web 营销活动，需要进行一次性开发人员设置，以定义 Adobe Experience Platform Web SDK 实施中的视图。

* 使用 Web 设计器编辑页面时，您现在可以直接从&#x200B;**修改**&#x200B;窗格向内容添加新更改，而无需从设计器界面中选择组件并进行编辑。
* 在设置 Web 子域时，除了使用已委派给 Adobe 的子域之外，您现在可以选择添加自己的子域。

**历程**

* 自定义操作响应功能现已普遍可用。 这允许您在自定义操作中对 API 调用响应加以利用，并根据这些响应编排历程。此外，还新增了限制，以将所有自定义操作限制为每个端点 5000 次调用/秒。
* 复制历程时，您现在可以定义历程副本的名称。

<!--
* The maximum duration that you can define in the Wait activity is now 29 days instead of 30.
-->

**电子邮件渠道**

利用电子邮件表面配置中的新选项，可选择向用户档案发送事务型消息，即使其电子邮件地址在 Adobe Journey Optimizer 禁止列表中。

**短信渠道**

**选择加入消息**&#x200B;和&#x200B;**帮助消息**&#x200B;这两个新字段已添加到 API 配置屏幕，允许用户自定义针对入站关键字的响应。请注意，这仅适用于Sinch 短信提供商。

**报告**

您现在可以将 Journey Optimizer 报告导出为 CSV 文件。[了解详情](../reports/global-report.md#export-reports)

<!--**Decision management**

Enhancements have been made to the audience picker in journeys or campaigns, with the addition of new columns displaying the origin and update frequency of audiences.    -->
