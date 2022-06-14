---
title: 2022 年发行说明
description: Journey Optimizer 2022 年发行说明
exl-id: 0997a640-3f89-4460-ba93-ea21a9d4efc5
source-git-commit: 0ca491315e214e3c12bec11a93da1a2b98b493b6
workflow-type: ht
source-wordcount: '0'
ht-degree: 100%

---

# 2022 年发行说明 {#release-notes-2022}

本页列出了 [!DNL Journey Optimizer] 于 2022 年发布的功能和改进。

可在[本页](release-notes.md)查看最新发行说明。

## 2022 年 4 月版 {#april-2022-release}

### 改进

**登陆页面**

* **选择启用/选择禁用复选框的新选项** - 您现在可以在订阅登陆页面中为选择启用/选择禁用插入一个复选框。用户需要选中复选框来表示同意（选择启用），取消选中该复选框以取消同意（选择禁用）。[了解详情](../landing-pages/design-lp.md#define-lp-specific-content)

* **预填登陆页面字段** - 现在，允许用户使用用户档案信息预填登陆页面字段。[了解详情](../landing-pages/create-lp.md#configure-primary-page)

**决策管理**

* **Edge 上的 Decisioning API** - Edge Decisioning API 可以投放和渲染在 Offer Decisioning 中管理的个性化优惠。您可以使用 Offer Decisioning 用户界面 (UI) 或 API 创建优惠和其他相关对象。[了解详情](../offers/api-reference/offer-delivery-api/edge-decisioning-api.md)

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
* 通过 Batch Decisioning API，组织可以在一次调用中对特定区段中的所有用户档案运用 Offer Decisioning 功能。区段中每个用户档案的优惠内容会放置在 AEP 数据集中，可用于自定义批量工作流。[了解详情](../offers/api-reference/offer-delivery-api/batch-decisioning-api.md)

**管理**

* 现在，您可以在邮件预设级别启用/禁用电子邮件标头中的取消订阅链接，并在邮件级别设置自定义取消订阅 URL。[了解详情](../configuration/message-presets.md#list-unsubscribe)
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
<p>有关更多信息，请参阅<a href="../configuration/message-presets.md#configure-email-settings">详细文档</a>。</p-->
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

<!--* Offer Decisioning reports are now available in Journey Optimizer. You can access the following metrics: Offers sent - Offers' impression rate - Offers' click rate - Breakdown report on Offers' sent.-->

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

**优惠决策**

* 现在，当您更新已发布的消息中直接或间接引用的优惠、后备优惠、优惠收藏集或优惠决策时，更新会自动反映在相应的消息中，而无需重新发布。[了解详情](../offers/offers-e2e.md#insert-decision-in-email)

* 在模拟将针对给定测试用户档案提供哪些优惠时，您现在可以修改默认的模拟设置，并查看与模拟对应的代码，这些代码可用于进行故障诊断。[了解详情](../offers/offer-activities/simulation.md#define-simulation-settings)

**管理**

* 管理员现在可以通过 CNAME 设置子域来编辑 PTR 记录。[了解详情](../configuration/ptr-records.md#edit-ptr-subdomains-cname)

**个性化**

* **添加到收藏夹** - 为帮助在进行个性化设置时提高效率，我们引入了“保存收藏内容”的概念。通过向收藏夹菜单添加不同属性，可以快速访问最常使用的项目。[了解详情](../personalization/personalize.md#fav)
