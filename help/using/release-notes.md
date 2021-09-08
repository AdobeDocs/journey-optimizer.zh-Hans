---
title: 发行说明
description: Journey Optimizer 发行说明
exl-id: 06fa956a-b500-416e-9d42-b683c328e837
source-git-commit: 5df4856c7be31a75116d906320ae50cd5dc6a2dc
workflow-type: tm+mt
source-wordcount: '1071'
ht-degree: 11%

---

# 发行说明 {#release-notes}

此页面列出 [!DNL Journey Optimizer] 的所有新增功能和改进。您还可以查阅最新的[文档更新](documentation-updates.md)。


## 2021 年 8 月版 {#august-2021-release}

### 新功能

<table>
<thead>
<tr>

<th><strong>在最佳时间发送消息 — 发送时间优化</strong><br/></th>
</thead>
<tbody>
<tr>
<td>
<p>在最佳时间为与Adobe Journey Optimizer互动的每个客户自动发送推送或电子邮件。 由Adobe的AI服务提供支持的发送时间优化可根据历史打开率和开箱即用的点击率，预测发送电子邮件或推送消息以最大化参与度的最佳时间。</p>
<p>此功能目前为测试版，仅供测试版客户使用。 要加入测试版计划，请联系Adobe客户关怀团队。</p>
<p>有关更多信息，请参阅<a href="building-journeys/journeys-message.md#send-time-optimization">详细的文档</a>。</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>

<th><strong>在业务事件中利用架构关系 — 查询表管理</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>现在，您可以在配置业务事件时利用架构之间的关系。 此外，在配置单一事件时、在历程中使用条件时、在消息个性化中以及在自定义操作个性化中时，还能够利用链接表中的字段。</p>
<p>有关更多信息，请参阅<a href="event/experience-event-schema.md#leverage_schema_relationships">详细的文档</a>。</p>
</td>
</tr>
</tbody>
</table>

<!--
<table>
<thead>
<tr>
<th><strong>Personalized URLs</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Personalized URLs take recipients to specific pages of a website, or to a personalized microsite, depending on the profile attributes. In Adobe Journey Optimizer, you can now add personalization to URLs in your message content. URL personalization can be applied to text and images, and use profile data or contextual data.</p>
<p>For more information, refer to the <a href="documentation-updates.md">detailed documentation</a>.</p>
</td>
</tr>
</tbody>
</table>
-->

<table>
<thead>
<tr>
<th><strong>确保向用户发送电子邮件 — 电子邮件重试</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>现在，您可以基于每个预设定义重试时间段，以确保不再需要时再次尝试。 例如，对于包含仅有效一天的链接的密码重置事务型消息，您可以将重试期限设置为24小时。 请注意，重试设置仅适用于电子邮件渠道。</p>
<p>有关更多信息，请参阅<a href="configuration/retries.md#retry-duration">详细的文档</a>。</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>定义要从发送中排除的地址 — 隐藏列表</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>现在，可以通过用户界面逐个地通过CSV文件上传批量模式，将电子邮件地址和域添加到禁止列表中。</p>
<p>有关更多信息，请参阅<a href="configuration/manage-suppression-list.md#add-addresses-and-domains">详细的文档</a>。</p>
</td>
</tr>
</tbody>
</table>

<!--
<table>
<thead>
<tr>
<th><strong>Customer Alerts</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>You can now subscribe to event-based alerts regarding Adobe Journey Optimizer activities. The user interface allows you to view a history of received alerts based on metrics revealed by Adobe Experience Platform Observability Insights. The UI also allows you to view, enable, and disable available alert rules.</p>
<p>This feature is currently in beta version and only available to beta customers. To join the beta program, contact Adobe Customer Care.
</p>
<p>For more information, refer to the <a href="https://experienceleague.adobe.com/docs/experience-platform/observability/alerts/overview.html">Adobe Experience Platform documentation</a>.</p>
</td>
</tr>
</tbody>
</table>
-->

### 改进

**历程**

* **动态标头**  — 您现在可以在HTTP标头参数中传递动态数据。这些参数可由接收历程操作HTTP调用（例如，时间戳或跟踪ID）的集成系统使用。 [了解详情](action/about-custom-action-configuration.md#url-configuration)
* **动态URL路径**  — 您现在可以为自定义操作设置动态URL路径。[了解详情](action/about-custom-action-configuration.md#url-configuration)
* 读取段的总限制速率已从每秒17,000条消息更改为每秒20,000条消息。 [了解详情](building-journeys/read-segment.md#configuring-segment-trigger-activity)

**用户界面**

* **搜索**  — 现在，您在每个页面上都可以直接从统一Experience Cloud搜索字段搜索业务对象和帮助文章。[了解详情](user-interface.md#unified-search)
* **Recents**  — 现在，Adobe Journey Optimizer主页中的Recents元素显示已扩展为其他业务对象。通过此更新，您最近访问的快捷方式包括消息、历程、区段、架构、数据集、数据源、事件、操作、源和目标。 [了解详情](action/about-custom-action-configuration.md#passing-collection)

**内容设计**

* **背景**  — 现在，实时预览支持背景图像。[了解详情](preview.md)
* **一键单击选择退出链接**  — 您可以在电子邮件内容中插入新类型的链接：通过 **选择退** 出链接，用户只需一次单击即可取消订阅接收您的通信，而无需重定向到登陆页面以确认选择退出。[了解详情](message-tracking.md#one-click-opt-out-link)

**个性化**

* **表达式编辑器**  — 现在，您可以在定义个性化时轻松添加回退值：当用户档案的个性化字段为空时，将显示回退值。[了解详情](personalization/functions/helper.md)

**电子邮件配置**

* **允许列表**  — 现在，可以通过API调用在非生产沙盒上启用和禁用允许列表。[了解详情](allow-list.md#enable-allow-list)
* **导航**  — 隐藏列表(可在“管理”>“渠道”>“电子邮件配置”>“常规”菜单 **下访问)已移至新的“隐藏列表”子菜单，该子菜单** 可 **** 收集所有相关功能以便于访问。[了解详情](configuration/manage-suppression-list.md#access-suppression-list)
<!--* **Suppression list** - Adding email addresses and domains into the suppression list is now available from the user interface, either one by one, either in bulk mode through a CSV file upload. [Learn more](configuration/manage-suppression-list.md#add-addresses-and-domains)-->

### 修复

* 修复了消息选项卡导航中的辅助功能问题。
* 修复了电子邮件设计器标签中的本地化问题。
* 修复了在历程中选择多个节点并单击属性面板上的“删除”时的问题。
* 修复了无法向历程中使用的操作添加新标头的问题。
* 现在，您可以通过用户界面中的更明确警告，了解消息预设创建失败的原因。


## 2021年7月版 {#july-2021-release}

### 新功能

<table>
<thead>
<tr>
<th><strong>在消息中使用元数据 — 查找表管理</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>使用您加载到Journey Optimizer中的参考数据丰富您的体验。 示例包括在体验事件中查找预订ID上的元数据，或从体验事件中的SKU查找产品信息以在画布中使用。 </p>
<p>现在，您可以利用架构之间的关系，以便将一个数据集用作另一个数据集的查询表。 然后，在配置单一事件时、在历程中使用条件时、在消息个性化中以及在自定义操作个性化中时，您可以利用链接表格中的所有字段。</p>
<p>有关更多信息，请参阅<a href="event/experience-event-schema.md#leverage_schema_relationships">详细的文档</a>。</p>
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
<p>有关更多信息，请参阅<a href="allow-list.md">详细的文档</a>。</p>
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
* 修复了上传HTML文件时Email designer中不支持具有`background-image`属性的内部样式表的问题。
