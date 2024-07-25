---
solution: Journey Optimizer
product: journey optimizer
title: 发行说明
description: Journey Optimizer 早期发行说明
feature: Release Notes
topic: Content Management
exl-id: 6e7d1300-8efd-4fdc-90e3-3ccdc3babd2f
source-git-commit: 5ccf9e08a24f840de7adbf04dc545904eaa32b8c
workflow-type: tm+mt
source-wordcount: '305'
ht-degree: 77%

---

# 早期发行说明 {#e-release-notes}

[!DNL Adobe Journey Optimizer] 不断地提供新功能、对现有功能进行增强和修复错误。所有更改会在每月末整合到[发行说明](release-notes.md)中。

**以下早期发行说明可能会在正式发行日期之前有所更改，恕不另行通知。**&#x200B;在发行当日，会在[发行说明](release-notes.md)中发布链接、屏幕和更新文档。

## 2024 年 7 月早期发行说明 {#e-2024}

**发布日期**：2024 年 7 月 30 日至 31 日

### 新功能 {#e-features}

此版本引入了下方详述的新功能。

<table>
<thead>
<tr>
<th><strong>IP 预热工作流</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>如果使用全新的 IP 地址发送电子邮件，现在可以直接从用户界面轻松执行 IP 预热工作流。Adobe Journey Optimizer 提供了一种标准化的高效方法来预热 IP 地址，该方法遵循最佳实践以期实现最佳可投放性。</p>
<!--p>For more information, refer to the <a href="../configuration/ip-warmup-gs.md">detailed documentation</a>.</p-->
</td>
</tr>
</tbody>
</table>


<table>
<thead>
<tr>
<th><strong>任何提供商的短信渠道（Beta 版）</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>除了默认短信提供商 Sinch、Infobip 和 Twilio 之外，您现在还可以在 Journey Optimizer 中配置其他短信提供商。</p>
<!--p>For more information, refer to the <a href="../configuration/ip-warmup-gs.md">detailed documentation</a>.</p-->
</td>
</tr>
</tbody>
</table>


<table>
<thead>
<tr>
<th><strong>联合受众构成（限量发布）</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>联合受众组合现在可在Adobe Journey Optimizer中使用。 它使企业能够组合数据，以便更好地在各种用例中使用。 通过这种新方法，作为Adobe Real-time Customer Data Platform和/或Adobe Journey Optimizer用户，您可以直接从现有数据仓库联合数据集，以在一个系统中构建和扩充Adobe Experience Platform受众和属性。</p>
<!--p>For more information, refer to the <a href="https://experienceleague.adobe.com/en/docs/federated-audience-composition/using/home"  target="_blank">detailed documentation</a>.</p-->
</td>
</tr>
</tbody>
</table>

<!--table>
<thead>
<tr>
<th><strong>Marketo Engage custom action</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>You can now integrate Adobe Journey Optimizer with Adobe Marketo Engage to build your B2B use cases. From a journey, a new custom action allows you to ingest data into Marketo.</p>
</td>
</tr>
</tbody>
</table-->

<!--table>
<thead>
<tr>
<th><strong>Improved channel configurations</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>The current channel surface capabilities have been enhanced for a consistent approach across all channels. You can now define, manage, and reuse these configurations for any of your channels.</p>
<p><ul>
<li>Channel surfaces are now renamed to <strong>Channel configurations</strong></li>
<li>From the Channel configurations inventory you can now create reusable channel configurations for all channels, including now Web, In-app messaging, or Code-based experience</li>
<li>Object level access control (OLAC) is now available for each channel configuration, allowing you to decide which of your users are allowed to create or use specific configurations</li>
<li>For some channels, you can create channel configurations that target multiple platforms. An example here would be an In-app messaging channel configuration that can target a web page, an iOS app and an Android app.</li>
</ul></p>
<p>For more information, refer to the <a href="../configuration/ip-warmup-gs.md">detailed documentation</a>.</p>
</td>
</tr>
</tbody>
</table-->


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

* （上市时间：7 月 8 日）您现在可以在配置事件时利用高级表达式编辑器，从而定义更复杂的表达式或在事件 ID 条件中使用函数。[了解详情](../event/about-creating.md#adv-exp-editor)

<!--* The `event-id` condition is now automatically filled during test mode. -->

<!--**SMS channel**

* You can now modify existing SMS configurations.-->

**应用程序内渠道**

* 表达式片段不适用于应用程序内渠道。

**受众**

* 现在，可以将自定义上传内容（CSV 文件）中的受众用于 Privacy and Security Shield。
<!--
**Push channel**

* You can now add your mobile application push credentials inside Adobe Journey Optimizer channel configuration settings. Creating an App surface in Adobe Experience Platform Data Collection is no longer required.-->

