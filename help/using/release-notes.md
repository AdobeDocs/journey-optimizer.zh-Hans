---
title: 发行说明
description: Journey Optimizer 发行说明
source-git-commit: c9fa07efd03e84bf38fb1d67fabba4b6066c4179
workflow-type: tm+mt
source-wordcount: '373'
ht-degree: 16%

---


# 发行说明 {#release-notes}

此页面列出 [!DNL Journey Optimizer] 的所有新增功能和改进。您还可以查阅最新的[文档更新](documentation-updates.md)。

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
<p>Adobe Experience Platform允许您定义架构之间的关系，以便将一个数据集用作另一个数据集的查询表。 [!DNL Journey Optimizer]现在可以利用来自链接架构的数据。</p>
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
<p>您现在可以在沙盒级别定义特定的发送安全列表，以便具有用于测试的安全环境。 在可能出现错误的非生产实例上，允许列表可确保您没有向客户发送不需要的消息的风险。 此功能通过利用抑制API来启用。</p>
<p>有关更多信息，请参阅<a href="allow-list.md">有详细说明的文档</a>。</p>
</td>
</tr>
</tbody>
</table>

### 改进

**历程**

* 在同一沙盒中同时运行的所有读取区段的总限制速率限制为每秒17,000条消息。 [了解更多信息](building-journeys/read-segment.md#configuring-segment-trigger-activity)
* **缓存持续时间**&#x200B;字段已从数据源配置窗格中删除。 [了解更多信息](datasource/about-data-sources.md)
* 对于外部数据源，现在会自动定义每秒15次调用的上限规则。 [了解更多信息](configuration/external-systems.md#capping)
* 对于实时历程，历程属性屏幕现在显示发布日期和发布历程的用户名称。 [了解更多信息](building-journeys/journey-gs.md#change-properties)
* 在历程列表屏幕中，添加了历程类型过滤器。 [了解更多信息](user-interface.md#section_lgm_hpz_pgb)
* **[!UICONTROL Throttling rate]**&#x200B;参数已添加到读取区段活动中。 [了解更多信息](building-journeys/read-segment.md#configuring-segment-trigger-activity)

**预览和测试消息**
* 标识和命名空间现在在&#x200B;**[!UICONTROL Preview]**&#x200B;屏幕中可见。 [了解更多信息](preview.md#preview-your-messages)
* 校样的测试电子邮件数量现在限制为10个。
* 校样中&#x200B;**主题行前缀**&#x200B;允许使用的字符现在受到限制。 [了解更多信息](preview.md#send-proofs)

**个性化表达式编辑器**
* 帮助程序下拉列表已重命名并重新排序。

### 修复

* 修复了导致批量电子邮件投放重复邮件的问题。
* 现在，当重试期限结束后未执行电子邮件发送时，将相应地生成事件。
* 修复了PTR记录屏幕中缺少IP信息的问题。
* 现在，在表达式编辑器中实现了选件边栏的本地化。
* 修复了信息弹出窗口中的间距不正确的问题。
