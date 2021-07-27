---
title: 发行说明
description: Journey Optimizer 发行说明
source-git-commit: 4d3352184aac7fe19096c21650982e29506f2bff
workflow-type: tm+mt
source-wordcount: '233'
ht-degree: 24%

---


# 发行说明 {#release-notes}

此页面列出了 Journey Optimizer 的所有新增功能和改进之处。
您还可以查阅最新的[文档更新](documentation-updates.md)。

## 2021年7月版 {#july-2021-release}

<table>
<thead>
<tr>
<th><strong>利用架构关系</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Adobe Experience Platform允许您定义架构之间的关系，以便将一个数据集用作另一个数据集的查询表。 Journey Optimizer现在可以利用来自链接架构的数据。</p>
<p>这些字段在统一的事件配置、历程条件、消息个性化和自定义操作个性化中可用。</p>
<p>有关更多信息，请参阅<a href="event/experience-event-schema.md#leverage_schema_relationships">有详细说明的文档</a>。</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>允许列表</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>现在，您可以在沙盒级别定义特定的发送安全列表，以避免例如在测试环境中向收件人发送不需要的电子邮件。
</p>
<p>有关更多信息，请参阅<a href="allow-list.md">有详细说明的文档</a>。</p>
</td>
</tr>
</tbody>
</table>

### 改进

* 在同一沙盒中同时运行的所有读取区段的总限制速率限制为每秒17,000条消息。 [了解更多信息](building-journeys/read-segment.md#configuring-segment-trigger-activity)
* **缓存持续时间**&#x200B;字段已从数据源配置窗格中删除。 [了解更多信息](datasource/about-data-sources.md)
* 对于外部数据源，现在会自动定义每秒15次调用的上限规则。 [了解更多信息](configuration/external-systems.md#capping)
* 对于实时历程，历程属性屏幕现在显示发布日期和发布历程的用户名称。 [了解更多信息](building-journeys/journey-gs.md#change-properties)
* 在历程列表屏幕中，添加了历程类型过滤器。 [了解更多信息](user-interface.md#section_lgm_hpz_pgb)
* [!UICONTROL Throttling rate]参数已添加到读取区段活动中。 [了解更多信息](building-journeys/read-segment.md#configuring-segment-trigger-activity)
