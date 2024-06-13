---
solution: Journey Optimizer
product: journey optimizer
title: 发行说明
description: Journey Optimizer 早期发行说明
feature: Release Notes
hide: true
hidefromtoc: true
topic: Content Management
exl-id: 6e7d1300-8efd-4fdc-90e3-3ccdc3babd2f
source-git-commit: c6daa2aef557943374a3eff005eda34dad214a5d
workflow-type: tm+mt
source-wordcount: '568'
ht-degree: 23%

---

# 早期发行说明 {#e-release-notes}

[!DNL Adobe Journey Optimizer] 不断地提供新功能、对现有功能进行增强和修复错误。所有更改会在每月末整合到[发行说明](release-notes.md)中。

**以下早期发行说明可能会在正式发行日期之前有所更改，恕不另行通知。**&#x200B;在发行当日，会在[发行说明](release-notes.md)中发布链接、屏幕和更新文档。

## 2024年6月早期发行说明 {#e-2024}

**发行日期**：2024年6月18日至19日

### 新功能 {#e-features}

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
<p>有关更多信息，请参阅<a href="../configuration/ip-warmup-gs.md">详细文档</a>。</p>
</td>
</tr>
</tbody>
</table>


<table>
<thead>
<tr>
<th><strong>内容片段自定义</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>您现在可以在片段中定义特定字段，在将片段添加到营销活动或历程时，可以编辑这些字段。 这允许在使用时调整内容部分，从而提供了用特定于上下文的详细信息覆盖默认值的灵活性。</p>
<!--p>For more information, refer to the <a href="../configuration/ip-warmup-gs.md">detailed documentation</a>.</p-->
</td>
</tr>
</tbody>
</table>


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


**决策管理**

* **决策管理中的多规则支持**  — 现在，您可以在决策管理中为给定优惠添加最多10个上限规则。 这样，您就可以增强对优惠发送方式的控制级别。[了解详情](../offers/offer-library/add-constraints.md#capping)

<!--* **Audits** - The **Change log** tab allowing you to see all the changes that have been made to an offer or a decision has been removed. Changes related to offers and decisions can now be seen in the **Audits** menu. -->

**内容片段**

* 现在可以编辑片段，并且可以将更改传播到使用它们的所有实时历程和营销活动中。
* 为内容片段引入了新状态： **草稿**， **实时**， **发布**、和 **已存档**.
* 要在历程或营销策划中使用片段，它现在必须位于 **实时** 状态。 片段创建流程中新增了一个步骤，允许发布片段并可用于历程和营销活动。 请注意，片段发布需要新权限。

  **注意**  — 从 **草稿** 和 **实时** Journey Optimizer 6月版本中引入了状态，在此版本之前创建的所有片段都具有 **草稿** 状态，即使它们用在历程或营销策划中也是如此。 在本节中了解如何更新现有片段。

**历程**

* 历程全局超时已从30天增加到91天。
* Adobe Journey Optimizer现在支持隐私删除/访问请求。
* 您现在可以调整历程清单中的列的大小。


**营销活动**

* 在Adobe Journey Optimizer中创建营销活动时，您现在可以在新模式中选择营销活动类型（已计划或触发）。

**电子邮件渠道**

* **列表取消订阅**  — 继最近的Gmail和Yahoo公告之后，Journey Optimizer对批量发件人支持“post/1-click”List-Unsubscribe选项。 <!--Refer to the following pages: [Email opt-out management](../email/email-opt-out.md#unsubscribe-header) and [Configure email settings](../email/email-settings.md#list-unsubscribe)-->


**短信渠道**

* 您现在可以使用单个API配置为每个沙盒添加唯一的短代码，从而使过程更高效、更简单。
* 您现在可以修改现有SMS配置。

**应用程序内渠道**

* **表达片段**  — 表达式片段现在可用于 **应用程序内渠道**. [了解详情](../personalization/use-expression-fragments.md)


* 您现在可以使用Edge Delivery插件获取理解入站实施并对其进行故障诊断所需的信息。


