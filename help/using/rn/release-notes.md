---
title: 发行说明
description: Journey Optimizer 发行说明
exl-id: 06fa956a-b500-416e-9d42-b683c328e837
source-git-commit: 85686ace0b7a8255c795f821caac481bbee1e6d6
workflow-type: tm+mt
source-wordcount: '625'
ht-degree: 24%

---

# 发行说明 {#release-notes}

此页面列出了 [!DNL Journey Optimizer] 的所有新增功能和改进。您还可以查阅[最新文档更新](documentation-updates.md)页面以了解更多更改。

[!DNL Adobe Journey Optimizer] 原生构建于 [!DNL Adobe Experience Platform] 之上并继承了其所具备的最新创新技术和改进。在 [Adobe Experience Platform 发行说明](https://experienceleague.adobe.com/docs/experience-platform/release-notes/latest.html?lang=zh-Hans){target=&quot;_blank&quot;} 中，进一步了解这些变更。

![新闻稿](../assets/do-not-localize/nl-icon.png) 立即注册 [Adobe Journey Optimizer 季度新闻稿](https://www.adobe.com/subscription/Adobe_Journey_Optimizer_NL.html){target=&quot;_blank&quot;}邮件，每个季度就能在收件箱中直接接收最新产品更新、精彩故事、用例、提示及更多内容。

## 2022 年 7 月版 {#july-2022-release}

### 新功能

<table>
<thead>
<tr>
<th><strong>新的在线消息传递流程</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Journey Optimizer为在历程中创作消息提供了新流程。 在Journey Optimizer中，串联式消息传送将为用户节省大量时间并简化创建和发送电子邮件、推送通知或短信的工作流程。 通过将消息作为单独的步骤删除，而改为在历程画布上的操作中使其可内嵌编辑，用户将需要单击较少的按钮并导航较少的屏幕来设计和编辑其内容。</p>
<img src="assets/do-not-localize/inline.gif"/>
<p>有关更多信息，请参阅<a href="../messages/get-started-content.md">详细文档</a>。</p>
</td>
</tr>
</tbody>
</table>


<table>
<thead>
<tr>
<th><strong>基于属性的访问控制（有限可用性）</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>您现在可以使用标签来识别架构字段，这些标签可定义组织或数据使用范围。 管理员可以使用权限界面定义涵盖XDM架构字段的访问策略，并更好地管理给用户或用户组（内部、外部或第三方用户）的访问权限，以及管理对特定类型数据（即敏感个人数据/SPD）的访问权限。</p>
<p>基于属性的访问控制目前仅对选定用户使用，并将在未来版本中部署到所有环境。</p>
<p>有关更多信息，请参阅<a href="../administration/attribute-based-access.md">详细文档</a>。</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>批量决策作业</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>您现在可以从用户界面运行批量决策作业，这样我就不需要开发人员来运行批处理api作业，而且我可以缩短营销所需的时间。 此新界面允许您创建作业并管理当前/过去的作业。</p>
<img src="assets/do-not-localize/batch.gif"/>
<p>有关更多信息，请参阅<a href="../offers/batch-delivery.md">详细文档。</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>在您的决策中自动使用性能最佳的选件（可用性有限）</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>您现在可以在决策管理中使用个性化优化模型系统。 这种新型模型允许您根据区段和选件性能优化和个性化选件。</p>
<p>个性化优化AI模型的使用当前仅限于选定用户，并将在未来版本中部署到所有环境。</p>
<img src="assets/do-not-localize/ai-ranking.gif"/>
<p>有关更多信息，请参阅<a href="../offers/ranking/personalized-optimization-model.md">详细文档</a>。</p>
</td>
</tr>
</tbody>
</table>

### 改进

**历程**

* **结束旅程**  — 在历程画布中， **结束** 活动已从面板中删除。 现在，结束标记默认会添加到每个路径的末尾，且无法删除。 这项改进可更好地报告客户从历程中的退出位置，而无需用户采取任何操作。 [了解详情](../building-journeys/journey-end.md)

**消息**

* 现在提供了消息预设 **通道曲面**. [了解详情](../configuration/channel-surfaces.md)

**管理**

* **PTR记录版**  — 现在，更新PTR记录时，处理时间最多只需3小时。 [了解详情](../configuration/ptr-records.md#processing)

* **允许列表UI**  — 您现在可以使用Journey Optimizer用户界面向允许列表添加新的电子邮件地址或域。 [了解详情](../configuration/allow-list.md)

* **允许列表逻辑更新**  — 现在，一旦启用了该功能，即使列表为空，允许列表逻辑也会应用。 [了解详情](../configuration/allow-list.md#logic)

* **URL跟踪参数**  — 您现在可以使用表达式编辑器在电子邮件界面中配置URL跟踪参数（即消息预设）。 [了解详情](../configuration/email-settings.md#url-tracking)

**优惠决策**

* **受众大小**  — 现在，在创建决策规则、选择区段或规则以设置选件资格或将区段或规则添加到决策范围时，用户界面中会显示新的受众规模估算组件。