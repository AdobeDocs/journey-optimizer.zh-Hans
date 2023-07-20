---
solution: Journey Optimizer
product: journey optimizer
title: 发行说明
description: Journey Optimizer早期发行说明
hide: true
hidefromtoc: true
source-git-commit: 1cfa4484329355310205421072af65f5dec32b5b
workflow-type: tm+mt
source-wordcount: '626'
ht-degree: 25%

---

# 早期发行说明 {#e-release-notes}

[!DNL Adobe Journey Optimizer] 不断地提供新功能、对现有功能进行增强和修复错误。所有更改都将在每月的最后一周合并到中 [发行说明](release-notes.md).

在发行日期之前，以下早期发行说明可能会发生更改，恕不另行通知。 链接、屏幕和更新的文档发布在 [发行说明](release-notes.md)，在发行日期。


## 2023年7月早期发行说明 {#july-rn-2023}

**发行日期**： 7月26日至27日

### 新功能{#july-2023-features}

此版本引入了下面列出的新功能。

<table>
<thead>
<tr>
<th><strong>受众构成</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>您现在可以创建组合工作流，将现有Adobe Experience Platform受众组合到可视画布中，并利用各种活动（拆分、扩充……）来创建新受众。 新创建的受众与现有受众一起保存回Adobe Experience Platform中，并可在Journey Optimizer营销活动中利用来定位客户。</p>
<img src="../audience/assets/audiences-publish.png"/>
<p>有关更多信息，请参阅<a href="../audience/get-started-audience-orchestration.md">详细文档</a>。</p>
<p>受众构成与新的Adobe Experience Platform“受众”菜单完全集成，该菜单用作受众的集中门户。 您现在可以使用包含新仪表板（带有区段趋势和重叠）的浏览页面来查找新见解并探索用于折叠和标记的组织工具。 此体验中嵌入了用于标准化受众标签的管理控制以及用于管理激活工作流的受众生命周期管理功能。 凭借这种新的管理体验，您现在可以从一个位置轻松安全地管理受众。 有关更多信息，请参阅 <a href="https://experienceleague.adobe.com/docs/experience-platform/segmentation/ui/overview.html" target="_blank">Adobe Experience Platform文档</a>.</p></p>
</td>
</tr>
</tbody>
</table>


<table>
<thead>
<tr>
<th><strong>直邮渠道</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>您现在可以在营销活动和历程中添加直邮消息。 直邮是一种离线渠道，允许您对直邮提供商向客户发送邮件所需的文件进行个性化和生成。</p>
<p>在准备直邮投放时，Journey Optimizer会生成一个文件，其中包含所有定向的用户档案和选定的联系信息（例如邮政地址）。 然后，您可以将此文件发送给直邮提供商，由其负责发送纸质信函。</p>
<img src="../direct-mail/assets/direct-mail-properties.png">
<p>有关更多信息，请参阅<a href="../direct-mail/create-direct-mail.md">详细文档</a>。</p>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>为Email Designer转换HTML内容</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>您现在可以在Journey Optimizer的电子邮件编辑器中导入和转换任何HTML内容。 内容块是自动标识的，并且可在Email Designer中使用：利用其强大的设计功能对其进行更新和个性化！</p>
<!--img src="../audience/assets/audiences-publish.png"/-->
<!--p>For more information, refer to the <a href="../audience/get-started-audience-orchestration.md">detailed documentation</a>.</p-->
</td>
</tr>
</tbody>
</table>


<table>
<thead>
<tr>
<th><strong>使用Journey Optimizer中的标记</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>除了营销活动和历程之外，您现在还可以将Adobe Experience Platform统一标记分配给登陆页面、模板、内容片段和订阅列表。 这使您能够轻松对它们进行分类，并改进所有列表中的搜索和导航。 此功能目前处于GA阶段（一般可用）。</p>
<img src="assets/do-not-localize/campaigns-tag.gif"/>
<p>有关更多信息，请参阅<a href="../start/search-filter-categorize.md#tags">详细文档</a>。</p>
</td>
</tr>
</tbody>
</table>


### 改进 {#july-2023-improvements}

此版本附带了下面列出的改进。

**受众**

历程或营销活动中的受众选择器已得到增强，新增了显示受众来源和更新频率的新列。

随着受众构成门户的发布，Adobe Experience Platform和Adobe Journey Optimizer更新了系统和文档中“受众”和“区段”的使用。

* 受众：一组具有共同特征和行为的人员、帐户、家庭或其他实体。
* 区段定义：在 Adobe Experience Platform 中，用于描述目标受众关键特征或行为的规则。此术语以前称为“区段”。

因此，在 Adobe Journey Optimizer 和 Adobe Experience Platform UI 中，“受众”将取代“区段”，这体现出了这种创建和管理受众的新方式。


**历程**

* 您现在可以在自定义操作中利用 API 调用响应，并根据这些响应编排历程。


**营销活动**

* 现在，与营销活动相关的上下文事件可在个性化编辑器“上下文属性”菜单中使用。

