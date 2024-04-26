---
solution: Journey Optimizer
product: journey optimizer
title: 发行说明
description: Journey Optimizer 早期发行说明
feature: Release Notes
topic: Content Management
exl-id: 6e7d1300-8efd-4fdc-90e3-3ccdc3babd2f
source-git-commit: f133a33237fccacbf800de445c27684de4f42453
workflow-type: tm+mt
source-wordcount: '478'
ht-degree: 33%

---

# 早期发行说明 {#e-release-notes}

[!DNL Adobe Journey Optimizer] 不断地提供新功能、对现有功能进行增强和修复错误。所有更改会在每月末整合到[发行说明](release-notes.md)中。

以下早期发行说明可能会在正式发行日期之前发生更改，恕不另行通知。在发行当日，会在[发行说明](release-notes.md)中发布链接、屏幕和更新文档。

## 2024年4月早期发行说明 {#e-2024}

**发行日期**：2024年4月30日

### 新功能 {#e-features}

此版本新增了以下详细介绍的功能。

<!--table>
<thead>
<tr>
<th><strong>Business rules - Private Beta</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>It is now possible to create and apply rule sets to your marketing communications.  </p>
</td>
</tr>
</tbody>
</table-->

<table>
<thead>
<tr>
<th><strong>Experience Decisioning — 限量发布</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Experience Decisioning通过提供称为“决策项目”的集中营销优惠目录和复杂的决策引擎，简化了个性化操作。 此引擎利用规则和排名标准来选择最相关的决策项并将其呈现给每个人。</p>
<p>这些决策项目通过新的基于代码的体验渠道(现在可在Journey Optimizer促销活动中访问)无缝集成到广泛的集客界面中。 Experience Decisioning决策策略仅适用于基于代码的体验营销活动。</p>
<p>Experience Decisioning当前仅适用于一批组织（限量发布）。 要获得访问权限，请联系您的Adobe代表。</p>
</td>
</tr>
</tbody>
</table>

<!--table>
<thead>
<tr>
<th><strong>Personalization - Local Lookups - Multi-Entity Support - Beta</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>TBD</p>
</td>
</tr>
</tbody>
</table-->

<table>
<thead>
<tr>
<th><strong>多媒体消息服务(MMS) — 所有提供商</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>使用短信渠道时，您现在可以通过发送多媒体消息服务 (MMS) 消息（支持与客户共享图像、GIF 文件或视频）来增强沟通效果。最初仅适用于Sinch，现在也适用于Infobip和Twilio。</p>
<img src="assets/do-not-localize/mms.gif"/>
</td>
</tr>
</tbody>
</table>

<!-- table>
<thead>
<tr>
<th><strong>AI Assistant - Experience Variant Generation - Beta</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Once you have created and personalized your message, take your content to the next level with the AI assistant. You can now use the AI assistant to optimize your message's impact by experimenting with different main titles, and images. Each variant is managed as a unique Treatment, to measure and compare which title effectively generates more clicks.</p>
</td>
</tr>
</tbody>
</table-->

<!--table>
<thead>
<tr>
<th><strong>IP Warmup Workflow - LA</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>You can now easily perform IP warmup workflows directly from the Journey Optimizer interface in a standardized and efficient way that follows the best practices for optimal deliverability.</p>
</td>
</tr>
</tbody>
</table-->

<!--table>
<thead>
<tr>
<th><strong>Email Surface Personalization - Private beta </strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>You can now define dynamic subdomains and personalized header parameters when creating email channel surfaces, for increased flexibility and control over your email settings.</p>
</td>
</tr>
</tbody>
</table-->

### 改进 {#e-improvements}

此版本包含下方列出的改进。

<!--
* **Experience Decisioning + Code-based experiences (LA)**: You can now leverage the Experience decisioning feature to use decision items in your code-based campaigns. Note: The Code-based experience channel and Experience decisioning are not available for organizations that have purchased the Adobe Healthcare Shield and Privacy and Security Shield add-on offerings.
-->
<!--
* **Expression Fragments supported for Web and In-App**: Expression fragments are now available for the Web and In-app channels. 
-->


<!--
* **DULE for AJO Channel Surface**: It is now possible to apply a label on certain profile attributes to restrict their usage inside a channel surface through marketing actions.
-->


<!--
* **List-Unsubscribe updates**: Following on the recent Gmail and Yahoo announcements for bulk senders, Journey Optimizer supports the "post/1-click" List-Unsubscribe option. 
-->

**决策管理**

* 此 **更改日志** 选项卡允许您查看对优惠或决策所做的所有更改已被删除。 现在，可在中查看与优惠和决策相关的更改 **审核** 菜单。

**Experience decisioning**

从Beta版到洛杉矶版，已添加以下改进：

* 现在，您可以在决策规则中使用Adobe Experience Platform中的上下文数据 **上下文数据** 选项卡。
* 现在，决策管理资源具有新的“管理体验决策”权限。 它允许您管理与体验决策相关的权限。
* 您现在可以在Experience Decisioning中为给定决策项目添加多个上限规则。 这样，您就可以增强对优惠发送方式的控制级别。
* 您现在可以使用以下内容创建Experience Decisioning营销活动的自定义报告仪表板 [!DNL Customer Journey Analytics].

**历程**

* **改进了历程设计器**

   * 改进的画布UI提供了更直观和更高效的用户体验。
   * 活动更清晰，通过更少的单击即可显示更多有关历程画布的信息。

* **新建实时报告**：最近24小时的旅程报告现在可直接在历程画布中访问。

**配置**

* 现在，您可以在渠道表面级别选择营销操作。在表面中使用时，将利用与该营销操作关联的所有同意策略，以尊重客户的偏好。
* 现在，可以在渠道表面使用对象级访问控制。

