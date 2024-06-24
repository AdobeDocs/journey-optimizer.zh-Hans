---
solution: Journey Optimizer
product: journey optimizer
title: 发行说明
feature: Release Notes
topic: Content Management
description: Journey Optimizer 发行说明
exl-id: 06fa956a-b500-416e-9d42-b683c328e837
source-git-commit: 6c4e0418776622467e7f5b7bb3d9332d965becf1
workflow-type: tm+mt
source-wordcount: '965'
ht-degree: 58%

---

# 发行说明 {#release-notes}

>[!CONTEXTUALHELP]
>id="ajo_homepage_card1"
>title="新增功能？"
>abstract="**Adobe Journey Optimizer** 不断地提供新功能、对现有功能的增强和错误修复。会在每月的最后一周将所有更改整合到发行说明中。"

[!DNL Adobe Journey Optimizer] 不断地提供新功能、对现有功能进行增强和修复错误。会在每月的最后一周将所有更改整合到发行说明中。

[!DNL Adobe Journey Optimizer] 原生构建于 [!DNL Adobe Experience Platform] 之上并继承了其所具备的最新创新技术和改进。在 [Adobe Experience Platform 发行说明](https://experienceleague.adobe.com/docs/experience-platform/release-notes/latest.html?lang=zh-Hans){target="_blank"}中，进一步了解这些更改。

![新闻稿](../assets/do-not-localize/nl-icon.png) 立即注册订阅 [Adobe Journey Optimizer 季度新闻稿](https://www.adobe.com/subscription/Adobe_Journey_Optimizer_NL.html){target="_blank"}，每个季度都能在收件箱中直接接收最新产品更新、精彩故事、用例、提示及更多内容。


## 2024 年 6 月发行说明 {#24-6-2024}

**在发行日期之前，以下早期发行说明可能会有所变更，恕不另行通知**.

**发行日期**：2024 年 6 月 18 日至 19 日

### 新功能 {#june-24-features}

此版本引入了下方详述的新功能。

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


<table>
<thead>
<tr>
<th><strong>内容片段自定义</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>您现在可以在片段中定义特定字段，并在将片段添加到营销活动或历程时进行编辑。这允许您在使用时调整内容部分，并且可以灵活地使用特定于上下文的信息覆盖默认值。</p>
<img src="../content-management/assets/do-not-localize/gif-fragments.gif"/>
<p>有关更多信息，请参阅<a href="../content-management/customizable-fragments.md">详细文档</a>。</p>
</td>
</tr>
</tbody>
</table>




<table>
<thead>
<tr>
<th><strong>使用Customer Journey Analytics进行报告（测试版）</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Journey Optimizer报告功能提高了与Customer Journey Analytics功能的互操作性，实现了两个平台的报告标准化，并提高了数据一致性和可靠性。 Journey Optimizer与Customer Journey Analytics之间的这种无缝集成提供了对绩效指标的更清晰查看，使用户能够做出更明智的决策。</p>
<p>有关更多信息，请参阅<a href="../reports/report-gs-cja.md">详细文档</a>。</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Adobe Journey Optimizer 中的 AI 助手</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>AI 助手是一项用户界面功能，可用于浏览和了解 Adobe 概念，并获取针对特定环境的操作见解。在 Adobe Experience Cloud 的多个产品中均可使用该功能，包括 Adobe Journey Optimizer。</p>
<p>有关更多信息，请参阅<a href="../start/ai-assistant.md">详细文档</a>。</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>历程和营销活动中的多语言消息（限量发布）</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>现在，您可以在单个活动或历程中轻松创建多种语言的内容。 利用此功能，您可以在编辑活动或历程时切换语言，简化整个编辑过程，并提高有效管理多语言内容的能力。</p>
<p>目前，多语言内容仅适用于一组组织（限量发布）。 要获得访问权限，请与 Adobe 代表联系。</p>
</td>
</tr>
</tbody>
</table>


<table>
<thead>
<tr>
<th><strong>历程中的试验（限量发布）</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Adobe Journey Optimizer已在营销活动中提供，现在支持历程中的试验。 试验是开展在线测试时进行的随机试用，这意味着您将为给定的消息试验接触部分随机选择的用户，并为其他试验或试验组接触另外一组随机选择的用户。公开后，您可以衡量感兴趣的结果指标，如电子邮件打开次数、订阅次数或购买次数。</p>
<p>历程中的试验当前仅适用于一组组织（限量发布）。 要获得访问权限，请与 Adobe 代表联系。</p>
</td>
</tr>
</tbody>
</table>

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

* **决策管理中的多规则支持** - 现在，您可以在决策管理中为给定优惠添加最多 10 个上限规则。这样，您就可以增强对优惠发送方式的控制级别。[了解详情](../offers/offer-library/add-constraints.md#capping)

<!--* **Audits** - The **Change log** tab allowing you to see all the changes that have been made to an offer or a decision has been removed. Changes related to offers and decisions can now be seen in the **Audits** menu. -->

**内容片段**

>[!AVAILABILITY]
>
>请注意，这些增强功能将在首次发布后的几天内逐步推出。 虽然某些用户将可以立即访问，但其他用户在环境中使用它之前可能会遇到延迟。

* 现在您可以编辑片段，并且可以将更改同步到使用这些片段的所有实时历程和营销活动中。
* 为内容片段引入了多个新状态：**草稿**、**实时**、**发布中**&#x200B;和&#x200B;**已存档**。
* 要在历程或营销活动中使用某个片段，片段必须处于&#x200B;**实时**&#x200B;状态。片段创建流程中新增了一个步骤，通过该步骤可以发布片段并将其用于历程和营销活动。请注意，发布片段需要新权限。

  **注意** - Journey Optimizer 六月版中引入了&#x200B;**草稿**&#x200B;和&#x200B;**实时**&#x200B;状态，在此版本之前创建的所有片段均为&#x200B;**草稿**&#x200B;状态，无论片段是否已用于历程或营销活动。要了解如何更新现有片段，请参阅此部分。

有关更多信息，请参阅 [内容片段](../content-management/fragments.md) 文档。

**历程**

* 历程的全局超时已延长到91天。 [了解详情](../building-journeys/journey-properties.md#global_timeout)

  创建的任何新历程都将反映此新超时。 请参阅此 [常见问题解答部分](../building-journeys/journey-properties.md#timeout-faq) 了解更多信息。 请注意，这些更改将在6月份逐步推出。


* Adobe Journey Optimizer现在支持隐私删除/访问请求以及数据生命周期管理请求。 [了解详情](../privacy/requests.md)
* 您现在可以调整历程清单中的列大小。
  <!--* **Advanced expression editor in Event configuration** is now GA - You can now leverage the advanced expression editor while configuring an event, allowing you to define more complex expressions or use functions in the event id condition. This capability is released in Limited Availability for selected customers. [Read more](../event/about-creating.md)-->
* **合并策略**&#x200B;已正式推出 - 现在，历程使用的合并策略在整个历程中均可见且一致。[了解详情](../building-journeys/journey-properties.md#merge-policies)



**营销活动**

* 在Adobe Journey Optimizer中创建营销活动时，您现在可以在新模式中选择营销活动类型（已计划或触发）。 [了解详情](../campaigns/create-campaign.md)

**电子邮件渠道**

* **列表取消订阅**  — 继最近的Gmail和Yahoo公告之后，Journey Optimizer对批量发件人支持“post/1-click”List-Unsubscribe选项。 请参阅以下页面： [电子邮件选择退出管理](../email/email-opt-out.md#unsubscribe-header) 和 [配置电子邮件设置](../email/email-settings.md#list-unsubscribe).


**短信渠道**

* 您现在可以使用单个API配置为每个沙盒添加唯一的短代码，从而使过程更高效、更简单。 [了解详情](../sms/sms-configuration.md)

* 创建后， **api令牌** 上的字段 **API凭据详细信息** 页面现在已屏蔽。

<!--* You can now modify existing SMS configurations.-->

**应用程序内渠道**

<!--* **Expression fragment** - Expression fragments are now available for the **In-app channel**. [Read more](../personalization/use-expression-fragments.md)-->

* 您现在可以使用Edge Delivery插件获取理解入站实施并对其进行故障诊断所需的信息。 [了解有关Edge Delivery视图的更多信息](https://experienceleague.adobe.com/en/docs/experience-platform/assurance/view/edge-delivery){target="_blank"}.


**直邮渠道**

* 直邮渠道现在可供所有客户使用。 [了解详情](../direct-mail/get-started-direct-mail.md)
