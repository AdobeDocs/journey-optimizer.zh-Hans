---
title: 发行说明
description: Journey Optimizer 发行说明
exl-id: 06fa956a-b500-416e-9d42-b683c328e837
source-git-commit: 6cfd56d22cc18c044818dc73fc265ce5e882d36c
workflow-type: tm+mt
source-wordcount: '1996'
ht-degree: 16%

---

# 发行说明 {#release-notes}

此页面列出 [!DNL Journey Optimizer] 的所有新增功能和改进。您还可以查阅 [最新文档更新](documentation-updates.md).

## 2021 年 10 月版 {#oct-2021-release}

<!--table>
<thead>
<tr>
<th><strong>Journeys - Target users in a subscription list</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>You can now trigger a journey targeting a subscription list. To perform this: add a Read segment activity followed by a message, and in the message email settings, define an expression that will fetch the subscriber email address from the profile, for the targeted subscription list. The expression editor has been enhanced to allow you to to select the first entry key of a map.</p>
<p>Learn more in the <a href="https://experienceleague.adobe.com/docs/journeys/using/building-advanced-conditions-journeys/main-functions-journey/list/functionfilter.html">detailed documentation</a>.</p>>
</td>
</tr>
</tbody>
</table-->



<!--table>
<thead>
<tr>
<th><strong>Journeys - Profile cap condition</strong><br/></th>
</thead>
<tbody>
<tr>
<td>
<p>When using a <strong>Condition</strong> activity in a journey, you can now define a <strong>Profile cap</strong> condition. This new condition type allows you set a maximum number of profiles for a journey path. When this limit is reached, the selected profiles take a second path. This allows you to optimize your IP ramp up. For example, you may want to ramp up your deliveries on a domain to 50 millions by splitting the execution: send 1000 messages on day 1, 2000 on day 2, etc.</p>
<p>For more information, refer to the <a href="building-journeys/condition-activity.md#profile_cap">detailed documentation</a> and related <a href="building-journeys/ramp-up-deliveries-uc.md">sample use case</a>.</p>
</td>
</tr>
</tbody>
</table-->

<table>
<thead>
<tr>
<th><strong>决策管理 — 优惠模拟</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>现在，您可以在Journey Optimizer UI中模拟将哪些选件交付到给定版面的测试用户档案。 这允许您在将决策逻辑（包括资格限制和排名算法）投入生产之前轻松验证这些逻辑。 此功能允许非技术和技术用户快速测试offer decisioning并排除潜在问题。</p>
<p>有关更多信息，请参阅<a href="offers/offer-activities/simulation.md">详细文档</a>。</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>决策管理 — 个性化您的选件</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>现在，您可以使用Adobe Experience Platform配置文件属性和区段将选件的内容个性化，该组件与Journey Optimizer UI中的表达式编辑器组件相同。 </p>
<p>有关更多信息，请参阅<a href="offers/offer-library/creating-personalized-offers.md#content">详细文档</a>。</p>
</td>
</tr>
</tbody>
</table>


另请参阅 [Adobe Experience Platform 10月发行说明](https://experienceleague.adobe.com/docs/experience-platform/release-notes/latest.html){target=&quot;_blank&quot;}以了解更多更改。

### 改进

**历程**

* **表达式编辑器**  — 作为高级用户，您现在可以使用函数处理映射。 此功能可与订阅列表一起使用。 例如，从区段，您现在可以从订阅列表中获取电子邮件地址。 [在此示例中了解更多信息](building-journeys/message-to-subscribers-uc.md)

   <!-- * **Delta on segments** - When using a **Read segment** activity, you can now target the individuals who entered or exited a specific segment since the last execution.  -->
* **监控**  — 实时历程和测试模式的步骤事件已得到增强。 [新字段](reports/sharing-field-list.md#serviceevents) 已添加与配置文件导出作业相关的内容。 为了获得更好的用户体验，步骤事件字段现在按不同的类别进行组织。 上一步的所有事件字段仍可在 [stepEvents](reports/sharing-legacy-fields.md) 类别。
* **辅助功能**  — 在历程中实施了辅助功能增强。
* **收藏集**  — 现在支持包含子对象的对象数组。 [了解更多信息](building-journeys/collections.md)
* **列表**  — 历程、事件、操作、数据源的列表屏幕已得到改进。

**报告**

* **全局视图中的数据格式**  — 您现在可以在 **全局视图** 的 **执行** 选项卡。 [了解详情](message-monitoring.md)

<!--* **New metrics** - New metrics and widgets are now available in **Live** and **Global** reports to measure your offers' impact on recipients. [Learn more](reports/journey-global-report.md)-->

**管理**

* **编辑消息预设**  — 您现在可以编辑消息预设并监视其更新状态。 [了解详情](configuration/message-presets.md#edit-message-preset)
* **编辑PTR记录**  — 您现在可以编辑PTR记录并监视其更新状态。 [了解详情](configuration/ptr-records.md#edit-ptr-record)

**个性化**

* **用于日期格式的新帮助程序函数**  — 您现在可以指定日期字符串的显示方式。 [了解详情](personalization/functions/dates.md#format-date)

**决策管理**

* **评估排序**  — 通过新的和改进的决策创建流程，您不仅可以更顺畅地在决策对象之间导航，而且还可以完全控制决策引擎如何评估选件集。 这包括将哪些收藏集一起与单独评估，以及应按什么顺序评估收藏集。 [了解详情](offers/offer-activities/create-offer-activities.md#add-decision-scopes)

### 修复

* 修复了浏览器语言不是英语时无法显示历程列表、消息列表和电子邮件设计器的问题。
* 修复了使用Email designer中的表达式添加个性化时发生的语法错误：字符被错误转义。
* 修复了在 **管理** 菜单。
* 修复了在使用业务事件测试历程时触发其他实时历程的问题。

## 2021 年 9 月版 {#september-2021-release}

### 新功能

<table>
<thead>
<tr>

<th><strong>报表 — 更好地洞察目标受众</strong><br/></th>
</thead>
<tbody>
<tr>
<td>
<p>报表中提供了新量度：电子邮件和推送消息的“目标”和“排除”在实时报表和全局报表中均可见。 </br> 要访问最新量度，请注意，您必须为每个渠道和报表类型重置不同的报表功能板。 有关功能板自定义的更多信息，请参阅 <a href="reports/live-report.md">详细文档。</a></p>
<p>消息执行列表中的新列显示每个消息执行的目标用户档案数。 </p>
<p>有关更多信息，请参阅<a href="message-monitoring.md">详细文档</a>。</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>

<th><strong>使用自定义操作动态传递数据列表</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>您现在可以在自定义操作参数中传递将在运行时动态填充的集合或数据列表。 支持两种收藏集：简单集合和对象集合。 之前创建的自定义操作将继续工作。 </p>
<p>有关收藏集的更多信息，请参阅 <a href="building-journeys/collections.md">详细文档</a>. </p>
<p>过滤器和交集函数已添加到高级表达式编辑器中可用函数的列表。 这为收藏集筛选和比较提供了更多可能性。</p>
<p>请查阅有关 <a href="https://experienceleague.adobe.com/docs/journeys/using/building-advanced-conditions-journeys/main-functions-journey/list/functionfilter.html">过滤器</a> 和 <a href="https://experienceleague.adobe.com/docs/journeys/using/building-advanced-conditions-journeys/main-functions-journey/list/functionintersect.html">相交</a> 函数。</p>
</td>
</tr>
</tbody>
</table>



### 改进

**历程**

* 系统生成的架构和在为步骤事件配置期间创建的数据集现在处于只读模式，可防止对关键架构进行任何意外修改。 [了解详情](reports/sharing-overview.md)
* 将 **等待** 活动，该活动的标签将显示在画布中。 在报告和测试模式日志中也会使用标签，以明确标识您正在执行的操作。 [了解详情](building-journeys/about-journey-activities.md#best-practices)
* 通过过滤 **事件** 和 **操作** 类别。 编排活动不再过滤。 [了解详情](building-journeys/using-the-journey-designer.md)
* 现在，在基于规则的事件或业务事件中定义事件ID条件时，“包含”运算符可用于字符串类型的字段。 [了解详情](event/about-creating.md)

**电子邮件配置**

* 当IP池与消息预设关联时，您现在可以编辑它，该更新是异步的。 您还可以检查每个IP池更新状态。 [了解详情](configuration/ip-pools.md#edit-ip-pool)

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
<p>使用 Adobe Journey Optimizer，在适合的时间自动向您接洽的每个客户发送推送或电子邮件。由Adobe的AI服务提供支持的发送时间优化可根据历史打开率和开箱即用的点击率，预测发送电子邮件或推送消息以最大化参与度的最佳时间。</p>
<p>此功能目前为测试版，仅供测试版客户使用。 要加入测试版计划，请联系Adobe客户关怀团队。</p>
<p>有关更多信息，请参阅<a href="building-journeys/journeys-message.md#send-time-optimization">详细文档</a>。</p>
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
<p>有关更多信息，请参阅<a href="event/experience-event-schema.md#leverage_schema_relationships">详细文档</a>。</p>
</td>
</tr>
</tbody>
</table>


<table>
<thead>
<tr>
<th><strong>个性化URL</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>个性化URL可将收件人引导至网站的特定页面，或引导至个性化的微型网站，具体取决于用户档案属性。 在Adobe Journey Optimizer中，您现在可以向消息内容中的URL添加个性化。 URL个性化可应用于文本和图像，并使用用户档案数据或上下文数据。</p>
<p>有关更多信息，请参阅<a href="personalization/personalization-syntax.md#perso-urls">详细文档</a>。</p>
</td>
</tr>
</tbody>
</table>


<table>
<thead>
<tr>
<th><strong>确保向用户发送电子邮件 — 电子邮件重试</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>您现在可以按预设来定义重试时段，确保当不再需要时不会执行重试尝试。例如，对于包含仅有效一天的链接的密码重置事务型消息，您可以将重试期限设置为24小时。 请注意，重试设置仅适用于电子邮件渠道。</p>
<p>有关更多信息，请参阅<a href="configuration/retries.md#retry-duration">详细文档</a>。</p>
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
<p>现在可以通过用户界面将电子邮件地址和域逐个添加到禁止列表，也可以通过 CSV 文件上传以批量方式添加。</p>
<p>有关更多信息，请参阅<a href="configuration/manage-suppression-list.md#add-addresses-and-domains">详细文档</a>。</p>
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

* **动态标题**  — 您现在可以在HTTP标头参数中传递动态数据。 集成系统可以使用这些参数接收历程操作 HTTP 调用，例如时间戳或跟踪 ID。[了解详情](action/about-custom-action-configuration.md#url-configuration)
* **动态URL路径**  — 您现在可以为自定义操作设置动态URL路径。 [了解详情](action/about-custom-action-configuration.md#url-configuration)
* 读取段的总限制速率已从每秒17,000条消息更改为每秒20,000条消息。 [了解详情](building-journeys/read-segment.md#configuring-segment-trigger-activity)

**用户界面**

* **搜索**  — 现在，您可以在每个页面上直接从统一Experience Cloud搜索字段搜索业务对象和帮助文章。 [了解详情](user-interface.md#unified-search)
* **收件人**  — 显示Adobe Journey Optimizer主页中的收件人元素现已扩展到其他业务对象。 通过此更新，您最近访问的快捷方式包括消息、历程、区段、架构、数据集、数据源、事件、操作、源和目标。 [了解详情](action/about-custom-action-configuration.md#passing-collection)

**内容设计**

* **背景**  — 现在，实时预览支持背景图像。 [了解详情](preview.md)
* **一键单击选择退出链接**  — 您可以在电子邮件内容中插入新类型的链接：the **选择退出** 链接允许用户一键单击即可取消订阅接收您的通信，而不会被重定向到登陆页面以确认选择退出。 [了解详情](message-tracking.md#one-click-opt-out-link)

**个性化**

* **表达式编辑器**  — 现在，您可以在定义个性化时轻松添加回退值：当用户档案的个性化字段为空时，将显示回退值。 [了解详情](personalization/functions/helpers.md)

**电子邮件配置**

* **允许列表**  — 现在，可以通过API调用在非生产沙盒上启用和禁用允许列表。 [了解详情](allow-list.md#enable-allow-list)
* **导航**  — 禁止列表，可在 **管理>渠道>电子邮件配置>常规** ，已移至新 **禁止列表** 子菜单，可收集所有相关功能以便更轻松地访问。 [了解详情](configuration/manage-suppression-list.md#access-suppression-list)

**决策管理**

* 已更新在创建优惠时添加和配置呈现的方法，以改善用户体验。特别是，现在仅当您为呈现定义图像类型的内容时，才会显示资源库。[了解详情](offers/offer-library/creating-personalized-offers.md#representations)

### 修复

* 修复了消息选项卡导航中的辅助功能问题。
* 修复了电子邮件设计器标签中的本地化问题。
* 修复了在历程中选择多个节点并单击属性面板上的“删除”时的问题。
* 修复了无法向历程中使用的操作添加新标头的问题。
* 现在，您可以通过用户界面中的更明确警告，了解消息预设创建失败的原因。


## 2021 年 7 月版 {#july-2021-release}

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
<p>有关更多信息，请参阅<a href="event/experience-event-schema.md#leverage_schema_relationships">详细文档</a>。</p>
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
<p>有关更多信息，请参阅<a href="allow-list.md">详细文档</a>。</p>
</td>
</tr>
</tbody>
</table>

### 改进

**历程**

* 在同一沙盒中同时运行的所有读取区段的总限制速率限制为每秒17,000条消息。 [了解更多信息](building-journeys/read-segment.md#configuring-segment-trigger-activity)
* 的 **缓存时长** 字段，已从数据源配置窗格中删除。 [了解更多信息](datasource/about-data-sources.md)
* 对于外部数据源，现在会自动定义每秒15次调用的上限规则。 [了解更多信息](configuration/external-systems.md#capping)
* 对于实时历程，历程属性屏幕现在显示发布日期和发布历程的用户名称。 [了解更多信息](building-journeys/journey-gs.md#change-properties)
* 在历程列表屏幕中，添加了历程类型过滤器。 [了解更多信息](user-interface.md#section_lgm_hpz_pgb)
* 的 **[!UICONTROL Throttling rate]** 参数已添加到读取区段活动中。 [了解更多信息](building-journeys/read-segment.md#configuring-segment-trigger-activity)

**预览和测试消息**

* 标识和命名空间现在在 **[!UICONTROL Preview]** 屏幕。 [了解更多信息](preview.md#preview-your-messages)
* 校样的测试电子邮件数量现在限制为10个。
* 允许使用的字符 **主题行前缀** 校样现在有限。 [了解更多信息](preview.md#send-proofs)

**个性化表达式编辑器**

* 帮助程序下拉列表已重命名并重新排序。

### 修复

* 修复了导致批量电子邮件投放重复邮件的问题。
* 现在，当重试期限结束后未执行电子邮件发送时，将相应地生成事件。
* 修复了PTR记录屏幕中缺少IP信息的问题。
* 现在，在表达式编辑器中实现了选件边栏的本地化。
* 修复了信息弹出窗口中的间距不正确的问题。
* 修复了在上传HTML文件时，在Email Designer中内部样式表包含 `background-image` 不支持属性。
