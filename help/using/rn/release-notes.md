---
solution: Journey Optimizer
product: journey optimizer
title: 发行说明
feature: Release Notes
topic: Content Management
description: Journey Optimizer 发行说明
exl-id: 06fa956a-b500-416e-9d42-b683c328e837
source-git-commit: 40e4aaa93400daf52c96aa5ac2de17151cdbb07f
workflow-type: tm+mt
source-wordcount: '768'
ht-degree: 42%

---

# 发行说明 {#release-notes}

>[!CONTEXTUALHELP]
>id="ajo_homepage_card1"
>title="新增功能？"
>abstract="**Adobe Journey Optimizer** 不断提供新功能、现有功能的增强以及错误修复。 会在每月的最后一周将所有更改整合到发行说明中。"

[!DNL Adobe Journey Optimizer] 不断地提供新功能、对现有功能进行增强和修复错误。会在每月的最后一周将所有更改整合到发行说明中。

[!DNL Adobe Journey Optimizer] 原生构建于 [!DNL Adobe Experience Platform] 之上并继承了其所具备的最新创新技术和改进。在 [Adobe Experience Platform 发行说明](https://experienceleague.adobe.com/docs/experience-platform/release-notes/latest.html?lang=zh-Hans){target="_blank"}中，进一步了解这些更改。

![新闻稿](../assets/do-not-localize/nl-icon.png) 立即注册订阅 [Adobe Journey Optimizer 季度新闻稿](https://www.adobe.com/subscription/Adobe_Journey_Optimizer_NL.html){target="_blank"}，每个季度都能在收件箱中直接接收最新产品更新、精彩故事、用例、提示及更多内容。


## 2024 年 5 月发行说明 {#may-2024}

**发行日期**： 2024年5月21日至22日

### 新功能 {#e-features}

此版本引入了下方详述的新功能。


<table>
<thead>
<tr>
<th><strong>体验决策 - 限量发布版</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>通过提供称为“决策项”的集中式营销优惠目录和复杂的决策引擎，体验决策简化了个性化操作。此引擎利用规则和排名标准来选择最相关的决策项并将其呈现给每个人。</p>
<p>这些决策项通过新的基于代码的体验渠道无缝集成到广泛的入站表面中，现在可以在 Journey Optimizer 营销活动中访问。体验决策的决策策略仅适用于基于代码的体验营销活动。</p>
<p>目前，体验决策功能仅面向一部分组织提供（限量发布版）。要获得访问权限，请与 Adobe 代表联系。</p>
<img src="assets/do-not-localize/gif-exd.gif"/>
<p>有关更多信息，请参阅<a href="../experience-decisioning/gs-experience-decisioning.md">详细文档</a>。</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>电子邮件表面个性化 — 限量发布</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>现在，您可以在创建电子邮件渠道界面时定义动态子域和个性化的标题参数，以提高灵活性和对电子邮件设置的控制。</p>
<p>电子邮件表面个性化目前仅适用于一组组织（限量发布）。 要获得访问权限，请与 Adobe 代表联系。</p>
<p>有关更多信息，请参阅<a href="../email/surface-personalization.md">详细文档</a>。</p>
</td>
</tr>
</tbody>
</table>

<!--table>
<thead>
<tr>
<th><strong>IP Warmup Workflow</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>If you are sending email on a brand new IP address, you can now easily perform IP warmup workflows directly from the user interface. Adobe Journey Optimizer offers a standardized and efficient way to warm up your IP adresses that follows the best practices for optimal deliverability.</p>
<p>For more information, refer to the <a href="../configuration/ip-warmup-gs.md">detailed documentation</a>.</p>
</td>
</tr>
</tbody>
</table-->

<!--table>
<thead>
<tr>
<th><strong>Business rules - Beta</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>You can now create granular frequency capping rules, and apply them to different types of marketing communications through rule sets. This new capability lets you control how often your audiences receive a message by setting cross-channel rules, that automatically exclude over-solicited profiles from messages and actions.</p>
<p>Business rules capability is currently available as a beta. To join the beta program, contact your Adobe representative.</p>
<p>For more information, refer to the <a href="../configuration/business-rules.md">detailed documentation</a>.</p>
</td>
</tr>
</tbody>
</table-->


<!--table>
<thead>
<tr>
<th><strong>Extended personalization data - Beta</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>You can now lookup and fetch data values within Adobe Experience Platform datasets, and use these values to build conditions in Adobe Journey Optimizer. You can leverage data from a lookup dataset when a relationship has been defined using an attribute inside of an array of objects. You can specify non-profile enabled datasets for lookup. Once enabled, you can use a profile attribute as a join key to the specified dataset to retrive further data for personalization.</p>
<p>This capability is currently available as a public beta.</p>
</td>
</tr>
</tbody>
</table-->

### 改进 {#e-improvements}

此版本包含下方列出的改进。

**Experience Decisioning** （限量发布）

从测试版到此版本，添加了以下改进：

* **Experience Decisioning +基于代码的体验**  — 您现在可以利用Experience Decisioning功能在基于代码的营销活动中使用决策项。 注释：基于代码的体验渠道和体验决策不适用于已购买 Adobe Health Shield 和 Privacy and Security Shield 附加产品的组织。[了解详情](../code-based/get-started-code-based.md)
* **上下文数据**  — 您现在可以在决策规则和排名公式中利用Adobe Experience Platform的上下文数据。 [了解详情](../experience-decisioning/context-data.md)
* **新建权限**  — 新的“管理体验决策”权限现在可用于决策管理资源。 这允许您管理与体验决策相关的权限。[了解详情](../experience-decisioning/gs-experience-decisioning.md)
* **上限规则**  — 您现在可以在Experience Decisioning中为给定决策项目添加多个上限规则。 这样，您就可以增强对优惠发送方式的控制级别。[了解详情](../experience-decisioning/items.md#capping)
* **报表**  — 您现在可以使用以下项目创建Experience Decisioning营销活动的自定义报告仪表板 [!DNL Customer Journey Analytics]. [了解详情](../experience-decisioning/cja-reporting.md)


<!--**Decision Management**

* **Multi-rule support** - You can now add up to 10 capping rules for a given offer in Decision Management. This allows you to increase the level of control over the way offers are sent.
* **Audits** - The **Change log** tab allowing you to see all the changes that have been made to an offer or a decision has been removed. Changes related to offers and decisions can now be seen in the **Audits** menu. -->


**电子邮件渠道**

<!--
* **List-unsubscribe** - Following on the recent Gmail and Yahoo announcements for bulk senders, Journey Optimizer supports the "post/1-click" List-Unsubscribe option. Refer to the following pages: [Email opt-out management](../email/email-opt-out.md#unsubscribe-header) and [Configure email settings](../email/email-settings.md#list-unsubscribe)
-->

* **垃圾邮件评分** （测试版） — 您现在可以在专用的垃圾邮件报告中检查您的内容垃圾邮件评分。 使用SpamAssassin，Adobe Journey Optimizer现在可以测试您的电子邮件内容，并为它打分，以指示ISP或邮箱提供商是否将其视为垃圾邮件。 [了解详情](../content-management/spam-report.md)

  >[!AVAILABILITY]
  >
  >此功能目前为测试版本，仅供测试版客户使用。 要加入测试版计划，请联系您的Adobe代表。

<!--
**Audiences**

* The use of audiences and attributes from audience composition and custom upload (CSV file) is now available for use with Healthcare Shield or Privacy and Security Shield.-->

<!--**Personalization**

* **Expression fragment** - Expression fragments are now available for the **In-app channel**. [Read more](../personalization/use-expression-fragments.md)-->

**历程**

<!--* **Merge policies** (Limited Availability)- Merge policies used by a journey are now visible and consistent throughout the journey.-->
* **mTLS支持**  — 自定义操作现在支持mTLS身份验证。 自定义操作或历程中无需额外配置即可激活mTLS；当检测到启用了mTLS的端点时，会自动进行此配置。 [了解详情](../action/about-custom-action-configuration.md#mtls-protocol-support)
* **事件中的查找表**  — 现在，当使用对象数组中的属性定义了关系时，您可以利用查找数据集中的数据。 查找值将在历程（条件、自定义操作等）中可用 和消息个性化。 [了解详情](../event/experience-event-schema.md#relationships_limitations)
* **事件配置中的高级表达式编辑器** (LA) — 现在，您可以在配置事件时利用高级表达式编辑器，从而定义更复杂的表达式或在事件ID条件中使用函数。 此功能以“有限可用”的状态向选定客户发布。 [了解详情](../event/about-creating.md)
* **合并策略** (LA) -历程使用的合并策略现在在整个历程中可见且一致。 此功能以“有限可用”的状态向选定客户发布。 [了解详情](../building-journeys/journey-gs.md#merge-policies)

**全球化**

作为我们持续努力提供统一用户体验的一部分，我们统一了Adobe Experience Cloud产品和应用程序中使用的术语。 这会影响德语术语“Titel”，在与对象名称相关时，该术语会更改为“Label”。 这些更改将在UI和文档中逐步推出。



