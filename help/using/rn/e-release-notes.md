---
solution: Journey Optimizer
product: journey optimizer
title: 发行说明
description: Journey Optimizer 早期发行说明
hide: true
hidefromtoc: true
source-git-commit: ca22edacfdad9b09abd742229471d23d23d2059b
workflow-type: tm+mt
source-wordcount: '362'
ht-degree: 43%

---

# 早期发行说明 {#e-release-notes}

[!DNL Adobe Journey Optimizer] 不断地提供新功能、对现有功能进行增强和修复错误。所有更改会在每月的最后一周整合到[发行说明](release-notes.md)中。

以下早期发行说明可能会在正式发行日期之前发生更改，恕不另行通知。链接、屏幕和更新文档，会在发行之日发布于[发行说明](release-notes.md)中。

## 2023年8月早期发行说明 {#aug-rn-2023}

**发行日期**： 2023年8月23日至24日

### 新功能{#aug-2023-features}

此版本引入了下方列出的新功能。

<table>
<thead>
<tr>
<th><strong>在您的历程中发送应用程序内消息</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>现在，您可以在历程中向应用程序用户发送个性化的应用程序内消息。 使用 Journey Optimizer 设计通知并自定义消息布局、显示、文本和按钮，以创造无缝体验。</p>
<img src="assets/in_app_journey_1.png"/>
<p>有关更多信息，请参阅<a href="../in-app/get-started-in-app.md">详细文档</a>。</p>
</tr>
</tbody>
</table>


<table>
<thead>
<tr>
<th><strong>使用种子列表验证电子邮件</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>您现在可以在Journey Optimizer中创建和管理种子列表。 种子列表包含内部地址，这些地址可以添加到实际受众，并在投放执行时收到与目标用户档案完全相同的消息。 使用此功能可监控已发送的通信，并确保所有显示格式、URL、图像和链接均正确。</p>
<img src="../configuration/assets/seed-list-details.png">
<!--p>For more information, refer to the <a href="../audience/get-started-audience-orchestration.md">detailed documentation</a>.</p-->
</td>
</tr>
</tbody>
</table>


<!--table>
<thead>
<tr>
<th><strong>Generate text and images with the Content assistant</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Once you have created and personalized your message, take your content to the next level with the Content assistant. You can now use the Content assistant to optimize your message's impact by experimenting with different main titles, and images. Each variant is managed as a unique Treatment, to measure and compare which title effectively generates more clicks.</p>
<p>This capability is currently available as a private beta.</p>
<img src="assets/gen-ai-image-2.png"/>
<p>For more information, refer to the <a href="../start/search-filter-categorize.md#tags">detailed documentation</a>.</p>
</td>
</tr>
</tbody>
</table-->



### 改进 {#aug-2023-improvements}

此版本包含下方列出的改进。

**API**

现在提供了用于创建和管理内容片段的新API。 [了解详情](https://developer.adobe.com/journey-optimizer-apis/references/content-templates/#tag/Content-fragment-API){target="_blank"}.

**电子邮件渠道**

电子邮件界面设置中提供了一个新选项，用于包含由于事务型消息受众中投诉垃圾邮件而被禁止使用的电子邮件地址。 即使他们将营销消息标记为垃圾邮件，这些用户档案随后仍可以接收事务型消息，例如密码重置或帐户报表。 此选项默认处于禁用状态。

**历程**

* 您现在可以在自定义操作中利用 API 调用响应，并根据这些响应编排历程。此功能目前作为私有测试版提供。
* 推出了一种新型的系统警报。现在，您会在自定义操作失败时收到通知。
  <!--* When duplicating a journey, you can now define the name of the journey copy.-->


**直邮**

* 现在可以在文件路由配置中选择Azure作为服务器类型。
* &amp;现在可用作直邮表面设置中的列分隔符字段。