---
solution: Journey Optimizer
product: journey optimizer
title: 发行说明
description: Journey Optimizer 早期发行说明
feature: Release Notes
hide: true
hidefromtoc: true
topic: Content Management
exl-id: 6e7d1300-8efd-4fdc-90e3-3ccdc3babd2f
source-git-commit: 1cbc5512fe23db22eca4fe1a2cb512a154b01844
workflow-type: tm+mt
source-wordcount: '447'
ht-degree: 32%

---

# 早期发行说明 {#e-release-notes}

[!DNL Adobe Journey Optimizer] 不断地提供新功能、对现有功能进行增强和修复错误。所有更改会在每月末整合到[发行说明](release-notes.md)中。

**以下早期发行说明可能会在正式发行日期之前有所更改，恕不另行通知。**&#x200B;在发行当日，会在[发行说明](release-notes.md)中发布链接、屏幕和更新文档。

## 2024 年 7 月早期发行说明 {#e-2024}

**发行日期**： 2024年7月30日至31日

### 新功能 {#e-features}

此版本引入了下方详述的新功能。

<table>
<thead>
<tr>
<th><strong>IP预热工作流(GA)</strong><br/></th>
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
<th><strong>与任何提供商的短信渠道(Beta)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>除了默认短信提供商Sinch、Infobip和Twilio之外，您现在还可以在Journey Optimizer中配置其他短信提供商。</p>
<!--p>For more information, refer to the <a href="../configuration/ip-warmup-gs.md">detailed documentation</a>.</p-->
</td>
</tr>
</tbody>
</table>



<table>
<thead>
<tr>
<th><strong>Marketo Engage自定义操作</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>您现在可以将Adobe Journey Optimizer与Adobe Marketo Engage集成以构建您的B2B用例。 在历程中，新的自定义操作允许您将数据摄取到Marketo。</p>
<!--p>For more information, refer to the <a href="../configuration/ip-warmup-gs.md">detailed documentation</a>.</p-->
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
<!--p>For more information, refer to the <a href="../configuration/ip-warmup-gs.md">detailed documentation</a>.</p-->
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

* （可用性： 7月8日）现在，您可以在配置事件时利用高级表达式编辑器，从而定义更复杂的表达式或在事件ID条件中使用函数。 [了解详情](../event/about-creating.md#adv-exp-editor)

<!--* The `event-id` condition is now automatically filled during test mode. -->

**短信渠道**

* 您现在可以修改现有SMS配置。

**应用程序内渠道**

* 表达式片段现在可用于应用程序内渠道。

**推送渠道**

* 您现在可以在Adobe Journey Optimizer渠道配置设置中添加移动应用程序推送凭据。 不再需要在Adobe Experience Platform数据收集中创建应用程序表面。

**受众**

* 现在，可以将来自受众构成和自定义上传（CSV文件）的受众和属性用于Healthcare Shield或Privacy and Security Shield。