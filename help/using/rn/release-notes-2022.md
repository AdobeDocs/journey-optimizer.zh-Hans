---
title: 2022 年发行说明
description: Journey Optimizer 2022 年发行说明
exl-id: 0997a640-3f89-4460-ba93-ea21a9d4efc5
source-git-commit: c530905eacbdf6161f6449d7a0b39c8afaf3a321
workflow-type: tm+mt
source-wordcount: '2337'
ht-degree: 97%

---

# 2022 年发行说明 {#release-notes-2022}

本页列出了 [!DNL Journey Optimizer] 于 2022 年发布的功能和改进。


## 2022 年 7 月版 {#july-2022-release}

### 新功能

<table>
<thead>
<tr>
<th><strong>新增内联消息传送流程</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Journey Optimizer 为历程中的消息创作提供了一个新流程。在 Journey Optimizer 中，内联消息传送可简化创建和发送电子邮件、推送通知或短信的工作流程，为用户节省大量时间。通过将消息作为单独的步骤删除，而改为在历程画布上的操作中使其可内联编辑，用户只需单击较少的按钮并导航较少的屏幕即可设计和编辑内容。</p>
<img src="assets/do-not-localize/inline.gif"/>
<p>有关更多信息，请参阅<a href="../messages/get-started-content.md">详细文档</a>。</p>
</td>
</tr>
</tbody>
</table>


<table>
<thead>
<tr>
<th><strong>基于属性的访问控制（限量发布）</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>现可使用标签来识别架构字段，这些标签可定义组织或数据使用范围。管理员可使用权限界面定义涵盖 XDM 架构字段的访问策略，更好地管理授予用户或用户组（内部、外部或第三方用户）的访问权限，以及管理特定类型数据（即敏感个人数据/SPD）的访问权限。</p>
<p>目前，基于属性的访问控制的使用仅限于选定的用户，但将在未来版本中部署到所有环境。</p>
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
<p>现可从用户界面运行批量决策作业，这样就不需要开发人员来运行批处理 API 作业，还可以缩短营销所需的时间。使用新界面可创建作业并管理当前/过去的作业。</p>
<img src="assets/do-not-localize/batch.gif"/>
<p>有关更多信息，请参阅<a href="../offers/batch-delivery.md">详细文档。</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>在决策中自动使用表现最好的优惠（限量发布）</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>现可在决策管理中使用个性化优化模型系统。利用这种新型模型可根据区段和优惠表现对优惠进行优化和个性化设置。</p>
<p>目前，个性化优化 AI 模型的使用仅限于选定的用户，但将在未来的版本中部署到所有环境。</p>
<img src="assets/do-not-localize/ai-ranking.gif"/>
<p>有关更多信息，请参阅<a href="../offers/ranking/personalized-optimization-model.md">详细文档</a>。</p>
</td>
</tr>
</tbody>
</table>

### 改进

**历程**

* **结束历程** - 在历程画布中，已从面板中移除&#x200B;**结束**&#x200B;活动。现在，会默认将结束标记添加到每个路径的末尾，且无法移除。这项改进可更好地报告客户从历程中退出的位置，而无需历程参与者执行任何操作。请参阅[文档](../building-journeys/journey-end.md)和[功能视频](https://video.tv.adobe.com/v/345376){target=&quot;_blank&quot;}。


*  默认情况下，历程属性中的&#x200B;**配置文件时区**&#x200B;选项现在处于未选中状态。[了解详情](../building-journeys/timezone-management.md#timezone-from-profiles)

**消息**

* 消息预设现已改为&#x200B;**渠道平面**。[了解详情](../configuration/channel-surfaces.md)

**管理**

* **PTR 记录版本** - 现在，更新 PTR 记录时，处理时间最多只需 3 小时。[了解详情](../configuration/ptr-records.md#processing)

* **允许列表 UI** - 现可使用 Journey Optimizer 用户界面向允许列表添加新的电子邮件地址或域。[了解详情](../configuration/allow-list.md)

* **允许列表逻辑更新** - 现在，允许列表这一功能会在启用后立即应用允许列表逻辑，即使该列表为空也是如此。[了解详情](../configuration/allow-list.md#logic)

* **URL 跟踪参数** - 现可使用表达式编辑器在电子邮件界面中配置 URL 跟踪参数（即消息预设）。[了解详情](../configuration/email-settings.md#url-tracking)

**决策管理**

* **受众规模** - 现在，在创建决策规则、选择区段或规则以设置优惠资格，或将区段或规则添加到决策范围时，用户界面中会显示新的受众规模估算组件。


## 2022 年 6 月版 {#june-2022-release}

### 新功能

<table>
<thead>
<tr>
<th><strong>向用户发送短信（限量发布）</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>现在，通过与 <b>Sinch</b> 或 <b>Twilio</b> 集成，您可以在 Journey Optimizer 中创建、个性化和发送短信。</p>
<!--img src="assets/do-not-localize/SMS.gif"/-->
<p>目前，短信渠道仅适用于一批组织（限量发布）。有关更多信息，请与您的 Adobe 代表联系。</p>
<p>在此<a href="../messages/create-sms.md">详细文档</a>中了解如何创建和发送短信。</p>
</td>
</tr>
</tbody>
</table>


<table>
<thead>
<tr>
<th><strong>利用 Adobe Stock 集成，更快地找到更具影响力的图像</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Adobe Stock 和 Adobe Journey Optimizer 电子邮件设计器集成插件为客户提供一种简单的方式来导航、许可和保存图像，用于消息创作。使用</br>全新的<b>查找类似 Stock 照片</b>选项，您可查找与图像的内容、颜色以及合成匹配的照片库。 </p>
<!--img src="assets/do-not-localize/stock-rn.gif"/-->
<p>有关更多信息，请参阅<a href="../design/stock.md">详细文档</a>。</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>对所有电子邮件使用电子邮件密送</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>现在，您可以使用电子邮件密送功能存储由 Adobe Journey Optimizer 发送的电子邮件。在电子邮件预设中启用此选项，以便发送的每封电子邮件都会密送至您的密送电子邮件地址。</p>
<!--img src="assets/do-not-localize/bcc-rn.gif"/-->
<p>有关更多信息，请参阅<a href="../configuration/bcc-email.md">详细文档</a>。</p>
</td>
</tr>
</tbody>
</table>

<!--<table>
<thead>
<tr>
<th><strong>Automatically use the best performing offer in your decisions</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>You can now use personalized optimization model systems in Decision Management. This new type of model allows you to optimize and personalize offers based on segments and offer performance.</p>
<p>The use of personalized optimization AI models is currently restricted to selected users, and will be deployed to all environments in a future release.</p>
<img src="assets/do-not-localize/ai-ranking.gif"/>
<p>For more information, refer to the <a href="../offers/ranking/personalized-optimization-model.md">detailed documentation</a>.</p>
</td>
</tr>
</tbody>
</table>-->

<table>
<thead>
<tr>
<th><strong>在沙箱之间复制对象</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>现在，您可以重新创建从 Journey Optimizer 沙箱到另一个沙箱的体验，例如从非生产沙箱到生产沙箱。此新功能可将整个历程（包括历程赖以正常运行的任何对象）从一个环境复制到另一个环境。除了历程之外，您还可以复制其他组件，如优惠、消息、模式、数据集、数据源、事件和操作。</p>
<p>有关更多信息，请参阅<a href="../building-journeys/copy-to-sandbox.md">详细文档</a>。
</td>
</tr>
</tbody>
</table>




### 改进

**决策管理**

* **HTML 和 JSON 文件支持** – 现在，您可将外部 HTML 和 JSON 文件从 Adobe Experience Cloud 资产库拖放到优惠呈现内容中。[了解详情](../offers/offer-library/add-representations.md#html-json)


**电子邮件**

* **另存为模板** – 现在，您可将电子邮件内容另存为模板，并在创建其他消息时重复使用。[了解详情](../design/email-templates.md)


**管理**

* **预览跟踪 URL 参数** – 现在，配置消息预设时，如果定义了 URL 跟踪参数，则会显示所产生的跟踪 URL 的动态预览。[了解详情](../configuration/email-settings.md#url-tracking)

* **消息预设版本** - 现在，更新消息预设时，处理时间最长可能只需 3 小时。[了解详情](../configuration/channel-surfaces.md#edit-channel-surface)

* **IP 池版本** - 现在，更新 IP 池时，处理时间最长可能只需 3 小时。[了解详情](../configuration/ip-pools.md#edit-ip-pool)




## 2022 年 5 月版 {#may-2022-release}

### 新功能

<table>
<thead>
<tr>
<th><strong>消息频度规则</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>您现在可以设置跨渠道业务规则，以自动从消息和操作中排除遭到过量请求的用户档案。</p>
<!--img src="assets/do-not-localize/frequency-rn.gif"/-->
<p>有关更多信息，请参阅<a href="../configuration/frequency-rules.md">详细文档</a>。</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>决策管理 - 人工智能排名自动优化模型</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>现在，您可以在决策管理中使用经过培训的模型系统。 此新功能可为给定用户档案显示优惠排名。</p>
<!--img src="assets/do-not-localize/optimization.gif"/-->
<p>有关更多信息，请参阅<a href="../offers/offer-activities/configure-offer-selection.md#use-ranking-strategy">详细文档</a>。</p>
</td>
</tr>
</tbody>
</table>

<!--table>
<thead>
<tr>
<th><strong>Attribute-based Access Control (ABAC)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Permission management in Journey Optimizer has been extended to data access. You can now manage data access for specific teams or groups of users (i.e. internal, external, 3rd parties) ​and manage access to specific types of data (i.e. Sensitive Personal Data/SPD).</p>
<p>This capability is available for a limited set of customers.</p>
<p>For more information, refer to the <a href="../landing-pages/create-lp.md">detailed documentation</a>.</p>
</td>
</tr>
</tbody>
</table-->

<table>
<thead>
<tr>
<th><strong>Journey Optimizer 审核日志</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>您现在可以监测用户对 Adobe Journey Optimizer 资源执行的操作。</p>
<!--img src="assets/do-not-localize/audit-rn.gif"/-->
<p>有关更多信息，请参阅<a href="../privacy/audit-logs.md">详细文档</a>。</p>
</td>
</tr>
</tbody>
</table>

### 改进

**个性化**

* **用于字符隐藏的新辅助函数** - 使用 `mask` 辅助函数，可将字符串的一部分替换为“X”字符。 [了解详情](../personalization/functions/string.md#mask)

**登陆页面**

* **不包含表单的登陆页面** - 您现在可以创建并发布不包含表单且无需访客执行任何操作的登陆页面。
* **登陆页面模板** - 现在，您可以将登陆页面另存为模板，并在创建其他登陆页面时重复使用。 [了解详情](../landing-pages/lp-templates.md)
* **返回主页面** - 您现在可以从同一登陆页面中的任何子页面添加指向主页面的链接。
* **自定义 JavaScript 支持** - 您现在可以向登陆页面内容添加自定义 JavaScript 以执行高级样式或向登陆页面添加自定义行为。	[了解详情](../landing-pages/lp-custom-js.md)

**历程**

* **读取区段** - 现在，一次性读取区段历程在历程执行 30 天后会变为“已完成”状态。 对于计划的读取区段，此期限为上次执行后的 30 天。 [了解详情](../building-journeys/read-segment.md)
* **表达式编辑器** - 添加了 [limit](../building-journeys/functions/functionlimit.md) 函数，以限制列表的项目数。 现在，使用 [sort](../building-journeys/functions/functionsort.md) 函数可对列表对象进行排序。 此外，还向 [disctinct](../building-journeys/functions/functiondistinct.md) 和 [distinctWithNull](../building-journeys/functions/functiondistinctwithnull.md) 函数添加了 listObject 支持。

**管理**

* **许可证使用情况仪表板更新** – 现在，[!DNL Adobe Journey Optimizer] 用户界面中提供的“许可证使用情况”仪表板可反映&#x200B;**已授予许可**&#x200B;平均用户档案丰富度的准确值。您可在此量度呈现中看到一个下拉信息，这意味着现在可以正确报告许可证限制。[了解详情](../segment/license-usage.md)


## 2022 年 4 月版 {#april-2022-release}

### 改进

**登陆页面**

* **选择启用/选择禁用复选框的新选项** - 您现在可以在订阅登陆页面中为选择启用/选择禁用插入一个复选框。用户需要选中复选框来表示同意（选择启用），取消选中该复选框以取消同意（选择禁用）。[了解详情](../landing-pages/design-lp.md#define-lp-specific-content)

* **预填登陆页面字段** - 现在，允许用户使用用户档案信息预填登陆页面字段。[了解详情](../landing-pages/create-lp.md#configure-primary-page)

**决策管理**

* **Edge上的决策API** - Edge Decisioning API可以交付和渲染在决策管理中管理的个性化选件。 您可以使用决策管理用户界面(UI)或API创建选件和其他相关对象。 [了解详情](../offers/api-reference/offer-delivery-api/edge-decisioning-api.md)

**管理**

* **PTR 提交持续时间** - 现在，PTR 编辑生效的持续时间为数小时。[了解详情](../configuration/ptr-records.md#processing)

**电子邮件设计**

* **20 个新电子邮件模板**&#x200B;现在可用于在 Journey Optimizer 中设计电子邮件内容。

**用户界面**

* **Journey Optimizer UI 中的上下文帮助** - 为 Journey Optimizer 中的多个页面添加了上下文帮助链接。如果可用，请单击“i”图标以查看当前功能的快速说明并访问相关文章。

**与 Adobe Campaign Standard 的集成**

作为 Adobe Campaign Standard 客户，您现在可以使用 Journey Optimizer 发送电子邮件、推送通知和短信。借助新的内置操作在 Journey Optimizer 中利用 Campaign Standard 事务型消息传递功能。[了解详情](../action/acs-action.md)

<!--
### Fixes

* Fixed an issue which caused tracking reports not to be available as the `JourneyActionId` was not properly populated. PLATIR-19854, CJM-26006
* Fixed an error on business events which could block the journey publication. CJM-25931
* Fixed an issue which could prevent images in Email Designer templates from being displayed. PLATIR-18176, CJM-25008
-->

## 2022 年 3 月版 {#march-2022-release}

### 改进

**历程**

* 为了避免统一用户档案架构中出现不必要的字段，默认情况下将不再为用户档案启用历程步骤事件架构。如有需要，您可以启用它。[了解详情](../reports/sharing-overview.md)
* 与导出作业相关的新步骤事件现在由 Journey Optimizer 发送至 Adobe Experience Platform。文档中添加了查询示例。[了解详情](../reports/query-examples.md)

**决策管理**

* 现在，您可以指定是将优惠上限应用到所有用户还是某个特定用户档案，是应用到所有投放位置还是具体的投放位置。[了解详情](../offers/offer-library/add-constraints.md#capping)
* 批量决策API允许组织在一次调用中对给定区段中的所有用户档案都使用决策管理功能。 区段中每个用户档案的优惠内容会放置在 AEP 数据集中，可用于自定义批量工作流。[了解详情](../offers/api-reference/offer-delivery-api/batch-decisioning-api.md)

**管理**

* 现在，您可以在邮件预设级别启用/禁用电子邮件标头中的取消订阅链接，并在邮件级别设置自定义取消订阅 URL。[了解详情](../configuration/channel-surfaces.md#list-unsubscribe)
* 现在可以通过 [!DNL Journey Optimizer] 界面在生产沙盒和非生产沙盒上启用和禁用允许列表。[了解详情](../configuration/allow-list.md#enable-allow-list)

**个性化**

* 现在可以在库中保存 40 多个个性化表达式。[了解详情](../personalization/personalization-library.md)

## 2022 年 2 月版 {#feb-2022-release}

### 新功能

<table>
<thead>
<tr>
<th><strong>订阅登陆页面</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>您现在可以在 Journey Optimizer 中创建和设计登陆页面，并将用户定向到在线表单，在表单中，用户可以选择加入或选择退出接收您的通信，或订阅特定服务（如新闻稿）。</p>
<p>有关更多信息，请参阅<a href="../landing-pages/create-lp.md">详细文档</a>和相关的<a href="../landing-pages/lp-use-cases.md">示例用例</a>。</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>新的个性化表达式库</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Journey Optimizer 现提供一个可供您访问预定义的个性化表达式的库。这些表达式由管理员用户配置。</p>
<p>有关更多信息，请参阅<a href="../personalization/personalization-library.md">详细文档</a>。</p>
</td>
</tr>
</tbody>
</table>


<!--table>
<thead>
<tr>
<th><strong>API Developer Site and Suppression API</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Journey Optimizer provide RESTful APIs that allow you to programmatically perform key operations in your applications.
Developer SDK for Journey Optimizer is now available with the Suppression API (beta).</p>
<p>With this API, you can control your outgoing messages using suppression and allow lists.
The suppression list helps you with honoring the ISPs’ feedback to preserve sending IP reputation. The allow list helps you ensure that you send only to those email addresses which are in the allowed list, and typically to ensure that you don't send mails to customers from your development sandbox.</p>
<p>See <a href="https://developer.adobe.com/journey-optimizer-apis/">Adobe Journey Optimizer APIs</a>.</p>
</td>
</tr>
</tbody>
</table-->

<table>
<thead>
<tr>
<th><strong>使用 UTM 跟踪参数传递信息以跟踪您的消息</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>在 Journey Optimizer 消息内容中，您现在可以将 UTM 参数添加到链接：这些参数可以提供有关该链接的其他数据，并帮助您确定用户点击您链接的位置和原因。</p>
<p>有关更多信息，请参阅<a href="../configuration/channel-surfaces.md#configure-email-settings">详细文档</a>。</p-->
</td>
</tr>
</tbody>
</table>

### 改进

**历程**

* 为优化性能，现在，所有处于测试模式且一周内未触发的历程都将切换回草稿状态。[了解更多信息](../building-journeys/testing-the-journey.md#important_notes)
* Journey Optimizer 和 Adobe Campaign Classic 之间的集成已经过优化以提高性能。默认配置上限已更改为 4000 次调用/5 分钟。[了解更多信息](../action/acc-action.md#important-notes)

**报告**

* 现在，可以根据投放的状态对其进行筛选：
   * 在消息执行列表中，您现在可以从投放列表中排除验证。
   * 在实时/全局报告中，您可以选择排除测试事件。

* 您现在可以访问有关发送时间优化数据的报告：立即向其发送消息的人数，以及通过 1 小时优化、2 小时优化向其发送消息的人数，等等。

<!--* decision management reports are now available in Journey Optimizer. You can access the following metrics: Offers sent - Offers' impression rate - Offers' click rate - Breakdown report on Offers' sent.-->

**决策管理**

* 排名和 AI 排名现在位于同一选项卡中。

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

**决策管理**

* 现在，当您更新已发布的消息中直接或间接引用的优惠、后备优惠、优惠收藏集或优惠决策时，更新会自动反映在相应的消息中，而无需重新发布。[了解详情](../offers/offers-e2e.md#insert-decision-in-email)

* 在模拟将针对给定测试用户档案提供哪些优惠时，您现在可以修改默认的模拟设置，并查看与模拟对应的代码，这些代码可用于进行故障诊断。[了解详情](../offers/offer-activities/simulation.md#define-simulation-settings)

**管理**

* 管理员现在可以通过 CNAME 设置子域来编辑 PTR 记录。[了解详情](../configuration/ptr-records.md#edit-ptr-subdomains-cname)

**个性化**

* **添加到收藏夹** - 为帮助在进行个性化设置时提高效率，我们引入了“保存收藏内容”的概念。通过向收藏夹菜单添加不同属性，可以快速访问最常使用的项目。[了解详情](../personalization/personalize.md#fav)
