---
solution: Journey Optimizer
product: journey optimizer
title: 发行说明
feature: Release Notes
topic: Content Management
description: Journey Optimizer 发行说明
exl-id: 06fa956a-b500-416e-9d42-b683c328e837
source-git-commit: 354c05746b6aa45356969fab9af6ffdcee6b9e66
workflow-type: tm+mt
source-wordcount: '1152'
ht-degree: 71%

---

# 发行说明 {#release-notes}

>[!CONTEXTUALHELP]
>id="ajo_homepage_card1"
>title="新增功能？"
>abstract="**Adobe Journey Optimizer** 不断地提供新功能、对现有功能的增强和错误修复。会在每月的最后一周将所有更改整合到发行说明中。"

[!DNL Adobe Journey Optimizer] 不断地提供新功能、对现有功能进行增强和修复错误。会在每月的最后一周将所有更改整合到发行说明中。

[!DNL Adobe Journey Optimizer] 原生构建于 [!DNL Adobe Experience Platform] 之上并继承了其所具备的最新创新技术和改进。在 [Adobe Experience Platform 发行说明](https://experienceleague.adobe.com/docs/experience-platform/release-notes/latest.html?lang=zh-Hans){target="_blank"}中，进一步了解这些更改。

![新闻稿](../assets/do-not-localize/nl-icon.png) 立即注册订阅 [Adobe Journey Optimizer 季度新闻稿](https://www.adobe.com/subscription/Adobe_Journey_Optimizer_NL.html){target="_blank"}，每个季度都能在收件箱中直接接收最新产品更新、精彩故事、用例、提示及更多内容。


## 2024年6月早期发行说明 {#24-6-2024}

**在发行日期之前，以下早期发行说明可能会有所变更，恕不另行通知**.

**发行日期**：2024年6月18日至19日

### 新功能 {#june-24-features}

此版本引入了下方详述的新功能。

<table>
<thead>
<tr>
<th><strong>IP预热工作流</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>如果您使用全新的IP地址发送电子邮件，现在可以直接从用户界面轻松执行IP预热工作流。 Adobe Journey Optimizer提供了一种标准化的高效方法来预热您的IP地址，该方法遵循最佳实践以实现最佳可投放性。</p>
<!--p>For more information, refer to the <a href="../configuration/ip-warmup-gs.md">detailed documentation</a>.</p-->
</td>
</tr>
</tbody>
</table>


<!--<table>
<thead>
<tr>
<th><strong>Content Fragments customization</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>You can now define specific fields in a fragment that can be edited when the fragment is added to a campaign or journey. This allows for the adjustment of content portions at the time of use, providing flexibility to override default values with context-specific details.</p>
<p>For more information, refer to the <a href="../configuration/ip-warmup-gs.md">detailed documentation</a>.</p>
</td>
</tr>
</tbody>
</table>-->


<table>
<thead>
<tr>
<th><strong>Adobe Journey Optimizer的人工智能助手</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>AI Assistant是一项用户界面功能，可用于导航和了解Adobe概念，并获取对您特定环境的操作见解。 它在Adobe Experience Cloud的多个产品中可用，包括Adobe Journey Optimizer。</p>
<p>有关更多信息，请参阅<a href="../start/ai-assistant.md">详细文档</a>。</p>
</td>
</tr>
</tbody>
</table>


<!--table>
<thead>
<tr>
<th><strong>Reporting with Customer Journey Analytics (Beta)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Journey Optimizer reporting is now fully integrated with Customer Journey Analytics capabilities, standardizing reporting across both platforms and improving data consistency and reliability. This seamless integration between Journey Optimizer and Customer Journey Analytics provides a clearer view of performance metrics, enabling users to make more informed decisions.</p>
</td>
</tr>
</tbody>
</table-->


<!--table>
<thead>
<tr>
<th><strong>Multilingual messages in journeys and campaigns  (Limited Availability)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>You can now effortlessly create content in multiple languages within a single campaign or journey. With this feature, you can switch between languages when editing your campaign or your journey, streamlining the entire editing process and improving your capability to efficiently manage multilingual content.</p>
<p>Multilingual content is currently only available for a set of organizations (Limited Availability). To gain access, contact your Adobe representative.</p>
</td>
</tr>
</tbody>
</table-->


<!--table>
<thead>
<tr>
<th><strong>Experimentation in journeys (Limited Availability)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Already available in campaigns, Adobe Journey Optimizer now supports experiments in journeys. Experiments are randomized trials, which in the context of online testing, means that you expose some randomly selected users to a given variation of a message, and another randomly selected set of users to some other variation or treatment. After exposure, you can then measure the outcome metrics you are interested in, such as opens of emails, subscriptions, or purchases.</p>
<p>Experimentation in journeys is currently only available for a set of organizations (Limited Availability). To gain access, contact your Adobe representative.</p>
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

### 改进 {#june24-improvements}

此版本包含下方列出的改进。


**决策管理**

* **决策管理中的多规则支持**  — 现在，您可以在决策管理中为给定优惠添加最多10个上限规则。 这样，您就可以增强对优惠发送方式的控制级别。[了解详情](../offers/offer-library/add-constraints.md#capping)

<!--* **Audits** - The **Change log** tab allowing you to see all the changes that have been made to an offer or a decision has been removed. Changes related to offers and decisions can now be seen in the **Audits** menu. -->

<!--**Content fragments**

* Fragments can now be edited, and changes can be propagated across all live journeys and campaigns where they are used.
* New statuses for content fragments have been introduced: **Draft**, **Live**, **Publishing**, and **Archived**. 
* To use a fragment in a journey or campaign, it must now be in the **Live** status. A new step has been added to the fragment creation process, allowing the fragment to be published and made available for use in journeys and campaigns. Note that fragment publishing requires a new permission.
   
   **CAUTION** - Since **Draft** and **Live** statuses have been introduced with Journey Optimizer June release, all fragments created before this release have the **Draft** status, even if they are used in a journey or campaign. Learn how to update your existing fragments in this section.-->

**历程**

* 历程全局超时已从30天增加到90天。
* Adobe Journey Optimizer现在支持隐私删除/访问请求以及数据生命周期管理请求。
* 您现在可以调整历程清单中的列的大小。
* **事件配置中的高级表达式编辑器** 现在为GA — 现在，您可以在配置事件时利用高级表达式编辑器，从而定义更复杂的表达式或在事件ID条件中使用函数。 此功能以“有限可用”的状态向选定客户发布。 <!--[Read more](../event/about-creating.md)-->
* **合并策略** 现在为GA -历程使用的合并策略现在在整个历程中可见且一致。 此功能以“有限可用”的状态向选定客户发布。 <!--[Read more](../building-journeys/journey-gs.md#merge-policies)-->



**营销活动**

* 在Adobe Journey Optimizer中创建营销活动时，您现在可以在新模式中选择营销活动类型（已计划或触发）。

<!--**Email channel**

* **List-unsubscribe** - Following on the recent Gmail and Yahoo announcements for bulk senders, Journey Optimizer supports the "post/1-click" List-Unsubscribe option. Refer to the following pages: [Email opt-out management](../email/email-opt-out.md#unsubscribe-header) and [Configure email settings](../email/email-settings.md#list-unsubscribe)-->


**短信渠道**

* 您现在可以使用单个API配置为每个沙盒添加唯一的短代码，从而使过程更高效、更简单。
  <!--* You can now modify existing SMS configurations.-->

**应用程序内渠道**

* **表达片段**  — 表达式片段现在可用于 **应用程序内渠道**. <!--[Read more](../personalization/use-expression-fragments.md)-->


* 您现在可以使用Edge Delivery插件获取理解入站实施并对其进行故障诊断所需的信息。

<!--
**Direct mail channel**

* Direct mail channel is now available for organizations that have purchased the Adobe **Healthcare Shield** and **Privacy and Security Shield** add-on offerings.
-->

## 2024 年 5 月发行说明 {#may-2024}

**发布日期**：2024 年 5 月 21 日至 22 日

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
<th><strong>电子邮件表面个性化 - 限量发布</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>现在，您可以在创建电子邮件渠道表面时定义动态子域和个性化的标题参数，以提高灵活性和对电子邮件设置的控制。</p>
<p>目前，电子邮件表面个性化仅面向一部分组织提供（限量发布）。要获得访问权限，请与 Adobe 代表联系。</p>
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

**体验决策**（限量发布）

从 Beta 版到此版本，做出了以下改进：

* **体验决策 + 基于代码的体验** - 您现在可以利用体验决策功能在基于代码的营销活动中使用决策项。注释：基于代码的体验渠道和体验决策不适用于已购买 Adobe Health Shield 和 Privacy and Security Shield 附加产品的组织。[了解详情](../code-based/get-started-code-based.md)
* **上下文数据** - 现在，您可以在决策规则中利用 Adobe Experience Platform 的上下文数据并对公式排序。[了解详情](../experience-decisioning/context-data.md)
* **新权限** - 现在，决策管理资源具有新的“管理体验决策”权限。这允许您管理与体验决策相关的权限。[了解详情](../experience-decisioning/gs-experience-decisioning.md)
* **上限规则** - 您现在可以在体验决策中对特定决策项添加多个上限规则。这样，您就可以增强对优惠发送方式的控制级别。[了解详情](../experience-decisioning/items.md#capping)
* **报告** - 您现在可以使用 [!DNL Customer Journey Analytics] 创建体验决策营销活动的自定义报告仪表板。[了解详情](../experience-decisioning/cja-reporting.md)


<!--**Decision Management**

* **Multi-rule support** - You can now add up to 10 capping rules for a given offer in Decision Management. This allows you to increase the level of control over the way offers are sent.
* **Audits** - The **Change log** tab allowing you to see all the changes that have been made to an offer or a decision has been removed. Changes related to offers and decisions can now be seen in the **Audits** menu. -->


**电子邮件渠道**

<!--
* **List-unsubscribe** - Following on the recent Gmail and Yahoo announcements for bulk senders, Journey Optimizer supports the "post/1-click" List-Unsubscribe option. Refer to the following pages: [Email opt-out management](../email/email-opt-out.md#unsubscribe-header) and [Configure email settings](../email/email-settings.md#list-unsubscribe)
-->

* **垃圾邮件评分**（Beta 版）- 您现在可以在专用的垃圾邮件报告中检查您的垃圾邮件内容评分。通过 SpamAssassin，Adobe Journey Optimizer 现在可以测试您的电子邮件内容并为其评分，以检测 ISP 或邮箱提供商是否将其视为垃圾邮件。[了解详情](../content-management/spam-report.md)

  >[!AVAILABILITY]
  >
  >此功能目前为 Beta 版，仅供 Beta 版客户使用。要加入 Beta 版计划，请联系 Adobe 代表。

<!--
**Audiences**

* The use of audiences and attributes from audience composition and custom upload (CSV file) is now available for use with Healthcare Shield or Privacy and Security Shield.-->

<!--**Personalization**

* **Expression fragment** - Expression fragments are now available for the **In-app channel**. [Read more](../personalization/use-expression-fragments.md)-->

**历程**

<!--* **Merge policies** (Limited Availability)- Merge policies used by a journey are now visible and consistent throughout the journey.-->
* **mTLS 支持** - 自定义操作现在支持 mTLS 身份验证。无需在自定义操作或历程中执行额外配置即可激活 mTLS；当检测到启用了 mTLS 的端点时，会自动执行配置。[了解详情](../action/about-custom-action-configuration.md#mtls-protocol-support)
* **事件中的查找表** - 现在，当使用对象数组中的属性定义了关系时，您可以利用查找数据集中的数据。可以在历程（条件、自定义操作等）和消息个性化中使用查找值。[了解详情](../event/experience-event-schema.md#relationships_limitations)
* **事件配置中的高级表达式编辑器**（限量发布版）- 现在，您可以在配置事件时利用高级表达式编辑器，从而定义更复杂的表达式或在事件 ID 条件中使用函数。“限量发布版”的部分客户可使用此功能。[了解详情](../event/about-creating.md)
* **合并策略**（限量发布版）- 现在，历程使用的合并策略在整个历程中均可见且一致。“限量发布版”的部分客户可使用此功能。[了解详情](../building-journeys/journey-gs.md#merge-policies)

**全球化**

为持续努力提供统一的用户体验，我们整合了 Adobe Experience Cloud 产品和应用程序中使用的术语。在与对象名称相关时，德语术语“Titel”更改为“Label”。这些更改将在 UI 和文档中逐步体现。



