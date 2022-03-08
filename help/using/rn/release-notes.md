---
title: 发行说明
description: Journey Optimizer 发行说明
exl-id: 06fa956a-b500-416e-9d42-b683c328e837
source-git-commit: 68407db81224e9c2b6930c800e57b65e081781fe
workflow-type: tm+mt
source-wordcount: '2416'
ht-degree: 100%

---

# 发行说明 {#release-notes}

此页面列出了 [!DNL Journey Optimizer] 的所有新增功能和改进。您还可以查阅[最新文档更新](documentation-updates.md)页面以了解更多更改。


## 2022 年 1 月版 {#january-2022-release}

### 新功能

<table>
<thead>
<tr>
<th><strong>历程 - 使用用户档案上限条件优化 IP 增加</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>配置历程中的<strong>条件</strong>活动时，您现在可以定义用户档案上限。此新条件类型允许您为历程路径设置最大用户档案数。达到此限制后，输入的用户档案会采用替代路径。 这样，您就可以增加投放的数量（IP 增加）。例如，您可能希望通过拆分执行来提升域上的投放数量：第 1 天发送 1000 条消息，第 2 天发送 2000 条等。</p>
<p>有关更多信息，请参阅<a href="../building-journeys/condition-activity.md#profile_cap">详细文档</a>和相关的<a href="../building-journeys/ramp-up-deliveries-uc.md">示例用例</a>。</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>历程 - 读取区段改进</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p><strong>增量读取</strong>选项已添加到周期性<strong>读取区段</strong>活动。此选项允许您仅将自上次执行历程后进入区段的个人作为目标。第一次执行始终以所有区段成员为目标。</p>
<p>有关更多信息，请参阅<a href="../building-journeys/read-segment.md#configuring-segment-trigger-activity">详细文档</a>。
</td>
</tr>
</tbody>
</table>

### 改进

**历程**

* Journey Optimizer 步骤事件现在可以链接到 [Adobe Customer Journey Analytics](https://experienceleague.adobe.com/docs/analytics-platform/using/cja-overview/cja-overview.html?lang=zh-Hans)。**profileID** 字段，在内置的历程步骤事件架构中，现在定义为标识字段。[了解详情](../reports/sharing-overview.md#integration-cja)

**优惠决策**

* 现在，当您更新已发布的消息中直接或间接引用的优惠、后备优惠、优惠收藏集或优惠决策时，更新会自动反映在相应的消息中，而无需重新发布。[了解详情](../offers/offers-e2e.md#insert-decision-in-email)

* 在模拟将针对给定测试用户档案提供哪些优惠时，您现在可以修改默认的模拟设置，并查看与模拟对应的代码，这些代码可用于进行故障诊断。[了解详情](../offers/offer-activities/simulation.md#define-simulation-settings)

**管理**

* 管理员现在可以通过 CNAME 设置子域来编辑 PTR 记录。[了解详情](../configuration/ptr-records.md#edit-ptr-subdomains-cname)

**个性化**

* **添加到收藏夹** - 为帮助在进行个性化设置时提高效率，我们引入了“保存收藏内容”的概念。通过向收藏夹菜单添加不同属性，可以快速访问最常使用的项目。[了解详情](../personalization/personalize.md#fav)

## 2021 年 11 月版 {#november-2021-release}

<table>
<thead>
<tr>
<th><strong>CNAME 子域委派</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Adobe Journey Optimizer 现在支持 CNAME。CNAME（或称规范名称记录）是指向其他域地址而非 IP 地址的记录。CNAME 子域委派允许您创建子域，并使用 CNAME 指向特定于 Adobe 的记录。使用此配置，您和 Adobe 共同负责维护 DNS，以设置用于发送、渲染和跟踪电子邮件的环境。</p>
<p>如果您所在组织的策略对完全子域委派方法有限制，则建议使用此方法。</p>
<p>在<a href="../configuration/delegate-subdomain.md#cname-subdomain-delegation">详细文档</a>中了解有关 CNAME 子域委派的更多信息。</p>
</td>
</tr>
</tbody>
</table>


## 2021 年 10 月版 {#oct-2021-release}

### 新功能

<table>
<thead>
<tr>
<th><strong>决策管理 - 优惠模拟</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>现在，您可以在 Journey Optimizer UI 中针对给定的投放位置模拟将哪些优惠投放到测试用户档案。这允许您在将决策逻辑（包括资格限制和排名算法）投入生产之前轻松验证这些逻辑。此功能允许非技术和技术用户快速测试优惠决策并排除潜在问题。</p>
<p>有关更多信息，请参阅<a href="../offers/offer-activities/simulation.md">详细文档</a>。</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>决策管理 - 对优惠进行个性化设置</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>您现在可以使用 Adobe Experience Platform 用户档案属性和区段，使用在整个 Journey Optimizer UI 中都相同的表达式编辑器组件来对您的优惠内容进行个性化设置。 </p>
<p>有关更多信息，请参阅<a href="../offers/offer-library/creating-personalized-offers.md#custom-text">详细文档</a>。</p>
</td>
</tr>
</tbody>
</table>


有关更多更改信息，另请参阅 [Adobe Experience Platform 10 月发行说明](https://experienceleague.adobe.com/docs/experience-platform/release-notes/2021/october-2021.html?lang=zh-Hans){target=&quot;_blank&quot;}。

### 改进

**历程**

* **表达式编辑器** - 作为高级用户，您现在可以使用函数处理映射。此功能可与订阅列表一起使用。例如，您现在可以从区段中获取订阅列表中的电子邮件地址。[在此示例中了解更多信息](../building-journeys/message-to-subscribers-uc.md)

* **监控** - 改进了实时历程和测试模式的步骤事件。已添加与用户档案导出作业相关的[新字段](../reports/sharing-field-list.md#serviceevents)。为了实现更好的用户体验，现在按不同的类别组织步骤事件字段。所有先前的步骤事件字段在 [stepEvents](../reports/sharing-legacy-fields.md) 类别中仍然可用。
* **辅助功能** - 在历程中实施了辅助功能改进。
* **集合** - 现在支持包含子对象的对象数组。[了解更多信息](../building-journeys/collections.md)
* **列表** - 历程、事件、操作、数据源的列表屏幕已得到改进。

**报告**

* **全局视图中的数据格式** - 您现在可以在 **Execution** 选项卡的 **Global view** 中在数字和百分比之间切换。[了解详情](../messages/message-monitoring.md)


**管理**

* **编辑消息预设** - 您现在可以编辑消息预设并监控其更新状态。[了解详情](../configuration/message-presets.md#edit-message-preset)
* **编辑 PTR 记录** - 您现在可以编辑 PTR 记录并监控其更新状态。[了解详情](../configuration/ptr-records.md#edit-ptr-record)

**个性化**

* **用于日期格式的新辅助函数** - 您现在可以指定日期字符串的显示方式。[了解详情](../personalization/functions/dates.md#format-date)


**决策管理**

* **评估排序** - 通过新的、经改进的决策创建流程，您不仅可以更顺畅地在决策对象之间导航，而且还可以完全控制决策引擎评估优惠集合的方式。这包括对哪些集进行合并或单独评估，以及应按什么顺序评估集合。[了解详情](../offers/offer-activities/create-offer-activities.md#add-decision-scopes)

### 修复

* 修复了浏览器语言不是英语时无法显示历程列表、消息列表和电子邮件设计器的问题。
* 修复了在电子邮件设计器中使用表达式来添加个性化设置时发生的语法错误：字符被错误转义。
* 修复了导致在 **Administration** 菜单中导航时出现 404 错误的问题。
* 修复了使用商业事件测试历程时触发其他实时历程的问题。


## 2021 年 9 月版 {#september-2021-release}

### 新功能

<table>
<thead>
<tr>

<th><strong>报告 - 更好地了解目标受众</strong><br/></th>
</thead>
<tbody>
<tr>
<td>
<p>报告中提供了新量度：电子邮件和推送消息的“目标受众”和“排除受众”在实时报告和全局报告中均可见。</br> 如需访问最新量度，请注意，您必须为每个渠道和报告类型重置不同的报告仪表板。有关仪表板自定义的更多信息，请参阅<a href="../reports/live-report.md">详细文档。</a></p>
<p>消息执行列表中的新列会显示每个消息执行的目标用户档案数。 </p>
<p>有关更多信息，请参阅<a href="../messages/message-monitoring.md">详细文档</a>。</p>
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
<p>您现在可以在自定义操作参数中传递集合或数据列表，这些参数将在运行时动态填充。支持两种集合：简单集合和对象集合。之前创建的自定义操作将继续运行。 </p>
<p>有关详细信息，请参阅<a href="../building-journeys/collections.md">详细文档</a>。 </p>
<p>筛选条件和交集函数已添加到高级表达式编辑器的可用函数列表中。这为集合筛选和比较提供了更多可能性。</p>
<p>请查阅有关<a href="../building-journeys/functions/functionfilter.md">筛选条件</a>和<a href="../building-journeys/functions/functionintersect.md">交集</a>函数的文档。</p>
</td>
</tr>
</tbody>
</table>

### 改进

**历程**

* 系统生成的架构以及在为步骤事件进行配置期间创建的数据集现在处于只读模式，以防止对关键架构进行任何意外修改。[了解详情](../reports/sharing-overview.md)
* 用一个会显示在画布中的标签清晰地标示 **Wait** 活动。在报告和测试模式日志中也会使用这个标签，以清楚地标识您正在执行的操作。[了解详情](../building-journeys/about-journey-activities.md#best-practices)
* 通过使用搜索功能过滤 **Events** 和 **Action** 类别中的元素，更快地找到您的事件和操作。不再对编排活动进行过滤。[了解详情](../building-journeys/using-the-journey-designer.md)
* 在基于规则的事件或商业事件中定义事件 ID 条件时，“contains”运算符现在可用于字符串类型的字段。[了解详情](../event/about-creating.md)

**电子邮件配置**

* 当 IP 池与消息预设相关联时，您现在可以编辑它，该更新是异步的。您还可以检查每个 IP 池的更新状态。[了解详情](../configuration/ip-pools.md#edit-ip-pool)


## 2021 年 8 月版 {#august-2021-release}

### 新功能

<table>
<thead>
<tr>

<th><strong>在最佳时间发送消息 - 优化发送时间</strong><br/></th>
</thead>
<tbody>
<tr>
<td>
<p>使用 Adobe Journey Optimizer，在适合的时间自动向您接洽的每个客户发送推送或电子邮件。由 Adobe 的 AI 服务提供支持的发送时间优化功能可根据现成可用的历史打开率和点击率，预测发送电子邮件或推送消息的最佳时间，以最大化参与度。</p>
<p>此功能目前为 Beta 版，仅供 Beta 版客户使用。要加入 Beta 版计划，请联系 Adobe 客户关怀团队。</p>
<p>有关更多信息，请参阅<a href="../building-journeys/journeys-message.md#send-time-optimization">详细文档</a>。</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>

<th><strong>在商业事件中利用架构关系 - 查找表管理</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>在配置商业活动时，您现在可以利用架构之间的关系。此外，在配置单一事件时，在历程、消息个性化以及自定义操作个性化中使用条件时，还能够利用链接表中的字段。</p>
<p>有关更多信息，请参阅<a href="../event/experience-event-schema.md#leverage_schema_relationships">详细文档</a>。</p>
</td>
</tr>
</tbody>
</table>


<table>
<thead>
<tr>
<th><strong>个性化 URL</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>个性化 URL 可将收件人引导至网站的特定页面，或引导至个性化的微型网站，具体取决于用户档案属性。在 Adobe Journey Optimizer 中，您现在可以向消息内容中的 URL 添加个性化设置。URL 个性化可应用于文本和图像，并使用用户档案数据或上下文数据。</p>
<p>有关更多信息，请参阅<a href="../personalization/personalization-syntax.md#perso-urls">详细文档</a>。</p>
</td>
</tr>
</tbody>
</table>


<table>
<thead>
<tr>
<th><strong>确保您的电子邮件发送到用户 - 电子邮件重试</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>您现在可以按预设来定义重试时段，确保当不再需要时不会执行重试尝试。例如，对于包含仅在一天内有效的链接的密码重置事务性消息，您可以将重试期限设置为 24 小时。请注意，重试设置仅适用于电子邮件渠道。</p>
<p>有关更多信息，请参阅<a href="../configuration/retries.md#retry-duration">详细文档</a>。</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>定义要从发送中排除的地址 - 禁止列表</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>现在可以通过用户界面将电子邮件地址和域逐个添加到禁止列表，也可以通过 CSV 文件上传以批量方式添加。</p>
<p>有关更多信息，请参阅<a href="../configuration/manage-suppression-list.md#add-addresses-and-domains">详细文档</a>。</p>
</td>
</tr>
</tbody>
</table>


### 改进

**历程**

* **动态标头** - 您现在可以在 HTTP 标头参数中传递动态数据。集成系统可以使用这些参数接收历程操作 HTTP 调用，例如时间戳或跟踪 ID。[了解详情](../action/about-custom-action-configuration.md#url-configuration)
* **动态 URL 路径** - 您现在可为自定义操作设置动态 URL 路径。[了解详情](../action/about-custom-action-configuration.md#url-configuration)
* 读取区段的总限制速率已从每秒 17,000 条消息更改为每秒 20,000 条消息。[了解详情](../building-journeys/read-segment.md#configuring-segment-trigger-activity)

**用户界面**

* **搜索** - 现在，您可以在每个页面上直接从 Experience Cloud 统一搜索字段搜索业务对象和帮助文章。[了解详情](../start/user-interface.md#unified-search)
* **收件人** - Adobe Journey Optimizer 主页中最近访问过的元素的显示现已扩展到其他业务对象。通过此更新，您最近访问过的元素的快捷方式包括消息、历程、区段、架构、数据集、数据源、事件、操作、源和目标。[了解详情](../action/about-custom-action-configuration.md#passing-collection)

**内容设计**

* **背景** - 现在，实时预览支持背景图像。[了解详情](../messages/preview.md)
* **一键式选择退出链接** - 您可以在电子邮件内容中插入新类型的链接：**选择退出**&#x200B;链接让用户只需单击一下即可取消订阅以停止接收您的通信，而不会被重定向到登陆页面以确认选择退出。[了解详情](../messages/consent.md#one-click-opt-out-link)

**个性化**

* **表达式编辑器** - 现在，您可以在定义个性化设置时轻松添加回退值：当用户档案的个性化字段为空时，将显示回退值。[了解详情](../personalization/functions/helpers.md)

**电子邮件配置**

* **允许列表** - 现在，可以通过 API 调用在非生产沙盒上启用和禁用允许列表。[了解详情](../messages/allow-list.md#enable-allow-list)
* **导航** - 禁止列表，之前可在&#x200B;**管理 > 渠道 > 电子邮件配置 > 常规**&#x200B;菜单下访问，已移至新的&#x200B;**禁止列表**&#x200B;子菜单，该菜单集合了所有相关功能，访问起来更加轻松。[了解详情](../configuration/manage-suppression-list.md#access-suppression-list)

**决策管理**

* 已更新在创建优惠时添加和配置呈现的方法，以改善用户体验。特别是，现在仅当您为呈现定义图像类型的内容时，才会显示资源库。[了解详情](../offers/offer-library/creating-personalized-offers.md#representations)

### 修复

* 修复了消息选项卡导航中的辅助功能问题。
* 修复了电子邮件设计器标签中的本地化问题。
* 修复了选择历程中的多个节点并单击属性面板上的“Delete”时存在的问题。
* 修复了无法向历程中使用的操作添加新标头的问题。
* 现在，您可以通过用户界面中的内容更明确的警告，了解消息预设创建失败的原因。


## 2021 年 7 月版 {#july-2021-release}

### 新功能

<table>
<thead>
<tr>
<th><strong>在消息中使用元数据 - 查找表管理</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>利用您加载到 Journey Optimizer 中的参考数据丰富您的体验。示例包括：在体验事件中查找关于预订 ID 的元数据，或从体验事件中的 SKU 查找用在画布中的产品信息。 </p>
<p>现在，您可以利用架构之间的关系，将一个数据集用作另一个数据集的查询表。在配置单一事件时，在历程、消息个性化以及自定义操作个性化中使用条件时，您可以利用链接表格中的所有字段。</p>
<p>有关更多信息，请参阅<a href="../event/experience-event-schema.md#leverage_schema_relationships">详细文档</a>。</p>
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
<p>您现在可以在沙盒级别定义特定的安全发送列表，以便具有用于测试的安全环境。在可能出现错误的非生产实例上，允许列表可确保不会出现向客户发送不必要消息的风险。此功能通过利用禁止 API 来启用。</p>
<p>有关更多信息，请参阅<a href="../messages/allow-list.md">详细文档</a>。</p>
</td>
</tr>
</tbody>
</table>

### 改进

**历程**

* 在同一沙盒中同时运行的所有读取区段的总限制速率限制为每秒 17,000 条消息。[了解更多信息](../building-journeys/read-segment.md#configuring-segment-trigger-activity)
* **缓存时长**&#x200B;字段已从数据源配置面板中移除。[了解更多信息](../datasource/about-data-sources.md)
* 对于外部数据源，现在会自动定义每秒 15 次调用的上限规则。[了解更多信息](../configuration/external-systems.md#capping)
* 对于实时历程，历程属性屏幕现在显示发布日期和发布历程的用户名称。[了解更多信息](../building-journeys/journey-gs.md#change-properties)
* 在历程列表屏幕中，添加了历程类型筛选器。[了解更多信息](../start/user-interface.md#filter-lists)
* **[!UICONTROL Throttling rate]** 参数已添加到读取区段活动中。[了解更多信息](../building-journeys/read-segment.md#configuring-segment-trigger-activity)

**预览和测试消息**

* 标识和命名空间现在显示于 **[!UICONTROL Preview]** 屏幕中。[了解更多信息](../messages/preview.md#preview-your-messages)
* 验证的测试电子邮件数量现在限制为 10 封。
* 允许用作验证中的&#x200B;**主题行前缀**&#x200B;的字符现在有限。[了解更多信息](../messages/preview.md#send-proofs)

**个性化表达式编辑器**

* 辅助函数下拉列表已重命名并重新排序。

### 修复

* 修复了导致批量电子邮件投放出现重复消息投放的问题。
* 现在，当重试期限结束后未执行电子邮件发送时，将相应地生成事件。
* 修复了 PTR 记录屏幕中缺少 IP 信息的问题。
* 现在，在表达式编辑器中实现了选件边栏的本地化。
* 修复了信息弹出窗口中间距不正确的问题。
* 修复了在上传包含不支持的 `background-image` 属性的 HTML 文件时，电子邮件设计器内部样式表中出现的问题。
