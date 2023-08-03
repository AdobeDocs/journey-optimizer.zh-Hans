---
solution: Journey Optimizer
product: journey optimizer
title: 发行说明
description: Journey Optimizer 早期发行说明
hide: true
hidefromtoc: true
source-git-commit: 4112ac79a1f21fb369119ccd801dcbceac3c1e58
workflow-type: ht
source-wordcount: '638'
ht-degree: 100%

---

# 早期发行说明 {#e-release-notes}

[!DNL Adobe Journey Optimizer] 不断地提供新功能、对现有功能进行增强和修复错误。所有更改会在每月的最后一周整合到[发行说明](release-notes.md)中。

以下早期发行说明可能会在正式发行日期之前发生更改，恕不另行通知。链接、屏幕和更新文档，会在发行之日发布于[发行说明](release-notes.md)中。

## 2023 年 7 月早期发行说明 {#july-rn-2023}

**发行日期**：7 月 26-27 日

### 新功能{#july-2023-features}

此版本引入了下方列出的新功能。

<table>
<thead>
<tr>
<th><strong>受众组合</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>您现在可以创建组合工作流，将现有 Adobe Experience Platform 受众组合到可视画布中，并利用各种活动（拆分、扩充等）来创建新受众。新创建的受众与现有受众会被一起保存回 Adobe Experience Platform 中，并可在 Journey Optimizer 营销活动中利用它们来定位客户。</p>
<p>有关更多信息，请参阅<a href="../audience/get-started-audience-orchestration.md">详细文档</a>。</p>
<p>受众组合与新的 Adobe Experience Platform“受众”菜单完全集成，该菜单可作为受众的集中式门户。您现在可以使用包含新仪表板（带有区段趋势和区段重叠功能）的浏览页面来寻获新见解并探索用于折叠和标记的组织工具。此体验中嵌入了用于标准化受众标签的管理控制以及受众生命周期管理功能，可管理激活工作流程。凭借这种新的管理体验，您现在可以从一个位置轻松安全地管理受众。有关更多信息，请参阅 <a href="https://experienceleague.adobe.com/docs/experience-platform/segmentation/ui/overview.html?lang=zh-Hans" target="_blank">Adobe Experience Platform 文档</a>。</p></p>
</td>
</tr>
</tbody>
</table>

<!--table>
<thead>
<tr>
<th><strong>Direct mail channel</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>You can now add direct mail messages in your campaigns. Direct mail is an offline channel that allows you to personalize and generate the files required by direct mail providers to send mail to your customers.</p>
<p>When you prepare a direct mail delivery, Journey Optimizer generates a file including all the targeted profiles and the chosen contact information (postal address for example). You will then be able to send this file to your direct mail provider who will take care of the actual sending.</p>
<img src="assets/do-not-localize/gif-dm.gif"/>
<p>For more information, refer to the <a href="../direct-mail/create-direct-mail.md">detailed documentation</a>.</p>
</tr>
</tbody>
</table-->

<table>
<thead>
<tr>
<th><strong>转换 HTML 内容以在电子邮件设计器中使用</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>您现在可以在 Journey Optimizer 的电子邮件编辑器中导入和转换任何 HTML 内容。内容块会被自动标识，并且可在电子邮件设计器中使用：利用其强大的设计功能对其进行更新和个性化！</p>
<img src="../email/assets/html-imported_2.png">
<!--p>For more information, refer to the <a href="../audience/get-started-audience-orchestration.md">detailed documentation</a>.</p-->
</td>
</tr>
</tbody>
</table>


<table>
<thead>
<tr>
<th><strong>使用 Journey Optimizer 中的标记</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>除了营销活动和历程之外，您现在还可以将 Adobe Experience Platform 统一标记分配给登陆页面、内容模板、片段和订阅列表。这让您能够轻松对其进行分类，并改进所有列表中的搜索和导航。 </p>
<img src="assets/do-not-localize/campaigns-tag.gif"/>
<p>有关更多信息，请参阅<a href="../start/search-filter-categorize.md#tags">详细文档</a>。</p>
</td>
</tr>
</tbody>
</table>


<table>
<thead>
<tr>
<th><strong>内容模板 API</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>您现在可以使用专用 API 创建和管理 Adobe Journey Optimizer 内容模板，体验与现有内容系统的无缝集成。</p>
<!--<p>For more information, refer to the <a href="../start/search-filter-categorize.md#tags">detailed documentation</a>.</p>-->
</td>
</tr>
</tbody>
</table>


### 改进 {#july-2023-improvements}

此版本包含下方列出的改进。

<!--
**Journeys**

* You can now leverage API call responses in custom actions and orchestrate your journey based on these responses.-->
* 推出了一种新型的系统警报。现在，您会在自定义操作失败时收到通知。
-->

**营销活动**

* 现在，可在个性化编辑器“上下文属性”菜单中使用与营销活动相关的上下文事件。


**受众**

已对历程或营销活动中的受众选择器进行增强，新增了显示受众来源和更新频率的新列。

随着受众组合门户的发布，更新了 Adobe Experience Platform 和 Adobe Journey Optimizer 的系统和文档中“受众”和“区段”的使用说明。

* 受众：一组具有共同特征和行为的人员、帐户、家庭或其他实体。
* 区段定义：在 Adobe Experience Platform 中，用于描述目标受众关键特征或行为的规则。此术语以前称为“区段”。

因此，在 Adobe Journey Optimizer 和 Adobe Experience Platform UI 中，“受众”将取代“区段”，这体现出了这种创建和管理受众的新方式。

**API**

Adobe Journey Optimizer API 身份验证 - 已弃用用于生成访问令牌的 JWT 方法。必须使用 OAuth 服务器到服务器身份验证方法创建所有新集成。Adobe 还建议您将现有集成迁移到 OAuth 方法。[了解详情](https://developer.adobe.com/journey-optimizer-apis/references/authentication/)


**其他更改**

现在作为公开 Beta 功能，所有客户都可以将 Journey Optimizer 数据集导出到云存储目标。通过此功能，您可以与云存储位置建立实时连接，以导出数据集的内容。[了解详情](../data/export-datasets.md)




