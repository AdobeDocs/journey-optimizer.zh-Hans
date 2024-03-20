---
solution: Journey Optimizer
product: journey optimizer
title: 发行说明
description: Journey Optimizer 早期发行说明
feature: Release Notes
topic: Content Management
exl-id: 6e7d1300-8efd-4fdc-90e3-3ccdc3babd2f
hide: true
hidefromtoc: true
source-git-commit: f957737aa741cc8b854912414d15154489d1b0b0
workflow-type: tm+mt
source-wordcount: '311'
ht-degree: 29%

---

# 早期发行说明 {#e-release-notes}

[!DNL Adobe Journey Optimizer] 不断地提供新功能、对现有功能进行增强和修复错误。所有变更于每月月底在 [发行说明](release-notes.md).

以下早期发行说明可能会在正式发行日期之前发生更改，恕不另行通知。在发行当日，会在[发行说明](release-notes.md)中发布链接、屏幕和更新文档。

## 2024年3月早期发行说明 {#e-2024}

**发行日期**：2024年3月19日至20日

### 新功能 {#e-features}

此版本引入了以下详细介绍的新功能。

<table>
<thead>
<tr>
<th><strong>基于代码的体验</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>借助新的基于代码的体验渠道，Adobe Journey Optimizer允许您对任何入站资产进行高级个性化和测试，从而无缝交付跨不同接触点的定制体验，如Web应用程序、移动应用程序、桌面应用程序、视频控制台、电视连接设备、智能电视、网亭、ATM、物联网设备等。</p>
<P>主要功能包括：</p>
<ul><li> 通用个性化：在所有接触点之间扩展个性化体验，确保有凝聚力且量身定制的用户历程</li>
<li>粒度编辑精度：在应用程序或网页内的各个位置编辑特定内容</li>
<li>通用实施：支持服务器端、基于API或基于SDK的实施方法，以便与开发环境无缝集成。</li></ul></p>
<p>有关更多信息，请参阅<a href="../code-based/get-started-code-based.md">详细文档</a>。</p>
<img src="assets/do-not-localize/code-based.gif">
</tr>
</tbody>
</table>

### 改进 {#e-improvements}

此版本包含下方列出的改进。

**内容模板**

* **缩略图** - A **网格视图** 模式现在可用于内容模板，显示缩略图可改善可视访问。 当前仅支持电子邮件HTML模板。 [了解详情](../content-management/content-templates.md#template-thumbnails)

  >[!AVAILABILITY]
  >
  >此功能面向一小部分客户限量发布 (LA)。

**历程**

历程创作生命周期中添加了新的中间状态：

* **发布** 介于两者之间的状态 **草稿** 状态和 **实时** 状态
* **正在停止** 介于两者之间的状态 **实时** 状态和 **已停止** 状态
* **激活测试模式** 或 **停用测试模式** 介于以下各项之间的状态： **草稿** 状态和 **草稿（测试）** 状态

当历程处于中间状态时，它是只读的。