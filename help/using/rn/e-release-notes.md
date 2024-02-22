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
source-git-commit: d3f0adab52ed8e44a6097c5079396d1e9c06e0a7
workflow-type: tm+mt
source-wordcount: '609'
ht-degree: 16%

---

# 早期发行说明 {#e-release-notes}

[!DNL Adobe Journey Optimizer] 不断地提供新功能、对现有功能进行增强和修复错误。所有更改会在每月的最后一周整合到[发行说明](release-notes.md)中。

以下早期发行说明可能会在正式发行日期之前发生更改，恕不另行通知。在发行当日，会在[发行说明](release-notes.md)中发布链接、屏幕和更新文档。

## 2024年2月早期发行说明 {#e-2024}

**发行日期**：2024年2月21日至22日

### 新功能{#e-features}

此版本引入了下方列出的新功能。


<table>
<thead>
<tr>
<th><strong>Web应用程序内消息传递</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>您现在可以使用新的Web应用程序内消息传送功能，通过模式叠加消息直接在网站上显示个性化内容。 此功能使您能够有效地与Web访客互动，提高用户交互、维系率和转化率。<br/><br/></p>
<img src="assets/do-not-localize/web_inapp.gif">
</tr>
</tbody>
</table>


<table>
<thead>
<tr>
<th><strong>短信和直邮的频率规则</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>您现在可以为短信和直邮渠道创建频率规则。 当达到频率上限时，频率规则会自动从消息和操作中排除过度请求的用户档案。 <br/><br/></p>
<img src="assets/do-not-localize/sms-dm-rules.gif">
</tr>
</tbody>
</table>

### 改进 {#e-improvements}

此版本包含下方列出的改进。

**受众**

* **种子列表**  — 使用时，现在支持变体 **种子列表**. 与来自目标受众的每个用户档案一样，种子地址也会收到同一消息的所有变体的副本（例如内容实验的不同处理）。

以前作为测试版提供，但现在，所有用户都可以使用以下改进：

* 您现在可以定位 **通过受众组合创建的受众** 并利用历程中的扩充属性。 [了解详情](../building-journeys/read-audience.md)

* 您现在可以定位 **从CSV文件上传的受众** 历程和营销活动。 [了解详情](../audience/about-audiences.md#segments-in-journey-optimizer)

  >[!AVAILABILITY]
  >
  >* 受众构成和自定义上传（CSV文件）中的受众和属性的使用当前不适用于Healthcare Shield或Privacy and Security Shield。
  >* 请注意，从CSV文件改进的受众上传功能将在初始发布后的几天内逐步推出。 虽然某些用户将可以立即访问，但其他用户在帐户中可以使用之前可能会遇到延迟。

**历程**

* **筛选您的历程**  — 您现在可以使用 **用于筛选历程的自定义日期** 库存，以及现有的预定义日期过滤器。 这允许您细化列表，显示在特定日期、特定月份、整个年份或指定时间范围内创建或发布的历程。
* **自定义操作**  — 您现在可以更新 **content-type** 标题。 此新 **content-type** 应引用JSON内容。
* **配置** - stepEvents中的identityMap属性现在已预填充。 主标识被定义为“primary = true”。
* **用户界面**  — 历程屏幕中的顶部栏已重新组织，以改善体验。 在不同的更新中，请注意允许您访问历程属性的“铅笔”图标现在显示在顶部栏的左侧，位于历程名称的旁边。

**短信渠道**

* **选择启用/选择禁用关键词**  — 配置短信渠道时，您现在可以自定义 **选择启用和选择禁用关键词** 根据您的喜好选择。 Journey Optimizer会根据这些指定的关键词触发响应。

**营销活动**

* **API触发的营销活动**  — 对激活API触发的营销活动后生成的cURL代码进行了增强。 它现在包含消息中使用的所有个性化（用户档案和上下文）变量。

**决策管理**

* **上限规则**  — 您现在可以添加 **多个上限规则** 一个报价。 这样，您就可以提高对优惠发送方式的控制级别。

**内容模板**

* **缩略图** - A **缩略图视图** 现在可用于内容模板和片段，以改进可视访问。

  >[!AVAILABILITY]
  >
  >此功能在有限可用性(LA)中面向一小部分客户发布。

* **多渠道模板**  — 内容模板现在可用于 **所有渠道**，Web除外。 对于电子邮件，您现在可以选择类型(HTML或内容)。
