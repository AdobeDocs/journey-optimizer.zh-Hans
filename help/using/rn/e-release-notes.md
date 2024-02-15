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
source-git-commit: 27ef6f591fdf5d8175b79bbbf3f59fe65e44106f
workflow-type: tm+mt
source-wordcount: '491'
ht-degree: 20%

---

# 早期发行说明 {#e-release-notes}

[!DNL Adobe Journey Optimizer] 不断地提供新功能、对现有功能进行增强和修复错误。所有更改会在每月的最后一周整合到[发行说明](release-notes.md)中。

以下早期发行说明可能会在正式发行日期之前发生更改，恕不另行通知。在发行当日，会在[发行说明](release-notes.md)中发布链接、屏幕和更新文档。

## 2024年2月早期发行说明 {#e-2024}

**发行日期**：2024年2月20日至21日

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
<p>您现在可以使用新的Web应用程序内消息传送功能，通过模式叠加消息直接在网站上显示个性化内容。 此功能使您能够有效地与Web访客互动，提高用户交互、维系率和转化率。<br/><!--br/>
Learn more in the <a href="../audience/computed-attributes.md">detailed documentation</a>.</p-->
<!--img src="assets/do-not-localize/computed-attributes.gif"-->
</tr>
</tbody>
</table>


<table>
<thead>
<tr>
<th><strong>Business Rules（测试版）</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>您现在可以创建适用于短信和直邮渠道的频率上限规则。 此外，您还可以按通信类型设置频率上限规则。<br/><!--br/>
Learn more in the <a href="../audience/computed-attributes.md">detailed documentation</a>.</p-->
<!--img src="assets/do-not-localize/computed-attributes.gif"-->
</tr>
</tbody>
</table>



### 改进 {#e-improvements}

此版本包含下方列出的改进。

**受众**

* 使用时，现在支持变体 **种子列表**. 与来自目标受众的每个用户档案一样，种子地址也会收到同一消息的所有变体的副本（例如内容实验的不同处理）。

以前作为测试版提供，但现在，所有用户都可以使用以下改进：

* 您现在可以定位 **从CSV文件上传的受众** 历程和营销活动。 [了解详情](../audience/about-audiences.md#segments-in-journey-optimizer)
* 您现在可以定位 **通过受众组合创建的受众** 并利用历程中的扩充属性。 [了解详情](../building-journeys/read-audience.md)

**历程**

* 历程屏幕中的顶部栏已重新组织，以改善体验。 在不同的更新中，请注意允许您访问历程属性的“铅笔”图标现在显示在顶部栏的左侧，位于历程名称的旁边。
* 您现在可以使用 **用于筛选历程的自定义日期** 库存，以及现有的预定义日期过滤器。 这允许您通过显示特定日期、特定月内、全年或指定时间范围内发布的旅程来优化列表。
* 您现在可以更新中的“content-type”标头 **自定义操作**.
* stepEvents中的identityMap属性现在已预填充。 主标识被定义为“primary = true”。

**短信渠道**

* 配置短信渠道时，您现在可以自定义 **选择启用和选择禁用关键词** 根据您的喜好选择。 Journey Optimizer会根据这些指定的关键词触发响应。

**营销活动**

* 的“cURL请求”部分中添加了信息 **API触发的营销活动** 处于“草稿”状态的示例cURL请求，用于指定仅在发布并执行活动后才能看到示例cURL请求。

**决策管理**

* 您现在可以添加 **多个上限规则** 一个报价。 这样，您就可以提高对优惠发送方式的控制级别。

**内容模板**

* A **缩略图视图** 现在可用于内容模板和片段，以改进可视访问。
* 内容模板现在可用于 **所有渠道**，Web除外。