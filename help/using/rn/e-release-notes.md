---
solution: Journey Optimizer
product: journey optimizer
title: 发行说明
description: Journey Optimizer 早期发行说明
feature: Release Notes
topic: Content Management
hide: true
hidefromtoc: true
exl-id: 6e7d1300-8efd-4fdc-90e3-3ccdc3babd2f
source-git-commit: ac8ccb52bd16a26c14dea148f989256e28170765
workflow-type: tm+mt
source-wordcount: '1999'
ht-degree: 37%

---

# 早期发行说明 {#e-release-notes}

[!DNL Adobe Journey Optimizer] 不断地提供新功能、对现有功能进行增强和修复错误。所有更改会在每月末整合到[发行说明](release-notes.md)中。

**以下早期发行说明可能会在正式发行日期之前有所更改，恕不另行通知。**&#x200B;在发行当日，会在[发行说明](release-notes.md)中发布链接、屏幕和更新文档。

## 2024 年 10 月早期发行说明 {#e-2024}

**发行日期**：2024年10月29日至30日

### 新功能 {#e-features}

此版本引入了下方详述的新功能。

<table>
<thead>
<tr>
<th><strong>电子邮件内容锁定</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Journey Optimizer 现在允许您通过锁定整个模板或特定结构和组件来锁定电子邮件模板中的内容。这样可防止无意中编辑或删除内容，让您更好地控制模板自定义，并提高电子邮件营销活动的效率和可靠性。</p>
<!--p>For more information, refer to the <a href="../content-management/gs-generative.md">detailed documentation</a>.</p>
<img src="assets/do-not-localize/ai-content.gif"/-->
</td>
</tr>
</tbody>
</table>


<table>
<thead>
<tr>
<th><strong>Approvals in journeys and campaigns (General availability)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>现在，通过审批策略，您可以在 Journey Optimizer 中设置审批流程，从而使营销团队可以确保营销活动及历程在投入使用之前由相应的负责人审查和签署。</p>
<p>Previously available for a set of organizations (LA), approval policies are now available to all users (GA).</p>
<p>有关更多信息，请参阅<a href="../test-approve/gs-approval.md">详细文档</a>。</p>
<img src="assets/do-not-localize/approval.gif"/>
</td>
</tr>
</tbody>
</table>


<table>
<thead>
<tr>
<th><strong>Email configuration personalization (General availability)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>现在，您可以在创建电子邮件渠道配置时定义动态子域和个性化的标题参数，以提高灵活性和对电子邮件设置的控制。</p><p>Using a personalized configuration in a campaign or a journey allows you to preview your email content to check for potential errors with the dynamic settings you defined.</p>
<p>Previously available for a set of organizations (LA), email configuration personalization is now available to all users (GA).</p>
<p>有关更多信息，请参阅<a href="../email/surface-personalization.md">详细文档</a>。</p>
</td>
</tr>
</tbody>
</table>


<table>
<thead>
<tr>
<th><strong>使用示例输入数据测试您的内容(Beta)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>历程优化器现在允许您测试电子邮件内容的各种变体，方法是预览该内容并使用从CSV文件上传或手动添加的示例输入数据发送校样。 All the profiles attributes used in your content for personalization are automatically detected by the system and can be used for your tests to create multiple variants.</p>
<p>This capability is currently available as a beta.</p>
<!--<p>For more information, refer to the <a href="../email/surface-personalization.md">detailed documentation</a>.</p>-->
</td>
</tr>
</tbody>
</table>


<table>
<thead>
<tr>
<th><strong>Conflict and priority management (Limited Availability)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>在Journey Optimizer中，管理营销活动和历程的数量和时间至关重要，这样才能避免因过多的交互而让客户不知所措。 Journey Optimizer现在提供了多种用于冲突管理和优先排序的工具。</p><p><ul><li><b>历程频率上限</b>：您现在可以创建要应用于历程的规则集，从而允许您限制个人资料每日、每周或每月的历程次数，并控制同时运行的并行历程次数。</li>
<li><b>优先级得分</b>：您现在可以为营销活动或历程分配从0到100的优先级得分。 数字越大，表示优先级越高。当两个营销活动或历程操作使用相同的渠道配置时，Journey Optimizer将选择具有最高优先级分数的营销活动或历程操作。 如果促销活动具有相同的得分，则将选择最近修改得最低的促销活动。</li>
<li><b></b></li>
<li><b></b>You can create a rule to suppress entry into a lower priority journey when a customer qualifies for an upcoming journey of higher priority.</li></ul></p>
<!--<p>For more information, refer to the <a href="../email/surface-personalization.md">detailed documentation</a>.</p>-->
<p>Conflict and priority management capabilities are available in Limited Availability to a select group of customers. Please note that these features will be gradually rolled out to more users in the future. 如果您有兴趣被添加到这些功能的轮候表中，请与您的客户团队联系。</p>

</td>
</tr>
</tbody>
</table>


<table>
<thead>
<tr>
<th><strong>Web设计器的非可视化编辑模式</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>As an alternative to the Journey Optimizer web designer, you can now add modifications to your website using a non-visual editor. It allows you to enter your changes manually without opening the pages in the visual editor.
This non-visual editing mode is useful if you cannot install browser extensions such as the Adobe Experience Cloud Visual Helper, which is required to load your pages in the web designer.</p>
<!--p>For more information, refer to the <a href="../email/surface-personalization.md">detailed documentation</a>.</p-->
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Content experimentation in journeys (General Availability)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>已经可用于营销活动，Adobe Journey Optimizer 现在支持历程中的试验。试验是开展在线测试时进行的随机试用，这意味着您将为给定的消息试验接触部分随机选择的用户，并为其他试验或试验组接触另外一组随机选择的用户。公开后，您可以衡量感兴趣的结果指标，如电子邮件打开次数、订阅次数或购买次数。</p>
<p>Previously available for a set of organizations (LA), experiments in journeys are now available to all users (GA).</p>
</td>
</tr>
</tbody>
</table>


<table>
<thead>
<tr>
<th><strong>Decisioning（正式发布）</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Decisioning, previously available for a set of organizations (LA) and known as Experience Decisioning, is now available to all users (GA). 它通过提供称为“决策项目”的集中营销优惠目录和复杂的决策引擎，简化了个性化。 This engine leverages rules and ranking criteria to select and present the most relevant decision items to each individual. These decision items are seamlessly integrated into a wide range of inbound surfaces through the code-based experience channel.</p>

<p>For now, Decisioning is unavailable for customers who have purchased the Adobe Healthcare Shield and Privacy and Security Shield add-on offerings.</p>

<!--p>For more information, refer to the <a href="../configuration/business-rules.md">detailed documentation</a>.</p-->
</td>
</tr>
</tbody>
</table>


<table>
<thead>
<tr>
<th><strong>Rule sets (Limited Availability)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>You can now create granular frequency capping rules, and apply them to your messages or journeys through rule sets. This new capability lets you control how often your audiences receive a message by setting cross-channel rules, that automatically exclude over-solicited profiles from messages and actions.</p><p>It also allows you to limit the number of journeys per day, week, or month, as well as control the number of concurrent journeys running simultaneously.</p>
<p>Rule sets are available in Limited Availability to a select group of customers. Please note that these features will be gradually rolled out to more users in the future. Reach out to your account team if interested in being added to the waitlist for this feature.</p>
<!--p>For more information, refer to the <a href="../configuration/business-rules.md">detailed documentation</a>.</p-->
</td>
</tr>
</tbody>
</table>


<table>
<thead>
<tr>
<th><strong>Multilingual messages in journeys and campaigns (General availability)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>现在，您可以在单个营销活动或历程中轻松创建多种语言的内容。利用此功能，您可以在编辑营销活动或历程时切换语言，简化整个编辑过程，并提高有效管理多语言内容的能力。</p>
<p>With general availability, multilingual content is now accessible across all channels. </p>
<!--p>For more information, refer to the <a href="../configuration/business-rules.md">detailed documentation</a>.</p-->
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Movable Ink and Adobe Journey Optimizer integration</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>You can now integrate Movable Ink Da Vinci and Adobe Journey Optimizer. With this new integration you can: </p>
<p><ul><li>利用Mobile Ink的Da Vinci产品中的强大功能，为批量营销活动汇编和个性化电子邮件变体</li>
<li>使用Da Vinci进行创作，使用AJO进行优化和交付，加快Journey Optimizer客户的从业人员工作流程</li>
<li>使用Adobe数据优化Da Vinci模型。</li></ul></p>
<!--p>For more information, refer to the <a href="../code-based/get-started-code-based.md">detailed documentation</a>.</p-->
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>更新的报告体验（正式发布）</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>自2024年10月16日起提供</p>
<p>Journey Optimizer reporting is now generally available (GA) and comes with an improved interoperability with Customer Journey Analytics capabilities, standardizing reporting across both platforms and improving data consistency and reliability. Journey Optimizer 与 Customer Journey Analytics 之间的这种无缝集成能够帮助更清晰地了解绩效指标，使用户能够做出更加明智的决策。</p>
<p>在正式发布后，引入了四个新功能：创建简单量度、创建和发布受众、使用Insight Builder提出临时问题以及安排报表自动通过电子邮件发送给关键收件人。</p>
<p>有关更多信息，请参阅<a href="../reports/report-cja-manage.md">详细文档</a>。</p>
<img src="assets/do-not-localize/ajo-cja.gif">
<p>重要信息：当前报告体验将于2025年1月停用。 在此日期之后，新的报告体验将成为标准。我们建议您熟悉新特性和功能，以确保顺利过渡。 <a href="../reports/report-gs-cja.md">了解如何开始使用 Journey Optimizer 的新报告界面</a></p>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>历程中基于代码的体验</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Available since Oct 1, 2024</p>
<p>借助基于代码的体验渠道，Adobe Journey Optimizer 允许您对任何入站属性进行高级个性化和测试，从而向不同的接触点无缝投放定制化体验，如 Web 应用程序、移动应用程序、桌面应用程序、视频游戏机、电视连接设备、智能电视、网亭、ATM、物联网设备等。现在，历程画布中提供了基于代码的体验渠道。</p>
<p>有关更多信息，请参阅<a href="../code-based/create-code-based.md">详细文档</a>。</p>
<img src="../assets/do-not-localize/code-based-journey.gif"/>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>历程中的 Web 体验</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Available since Oct 1, 2024</p>
<p>借助 Web 渠道，Adobe Journey Optimizer 允许您通过入站 Web 历程为客户提供个性化 Web 体验。现在，可在历程画布中使用 Web 渠道。</p>
<p>有关更多信息，请参阅<a href="../web/create-web.md">详细文档</a>。</p>
<img src="../assets/do-not-localize/web-journey.gif"/>
</tr>
</tbody>
</table>

### 改进 {#e-improvements}

此版本包含下方列出的改进。

**短信渠道**

>[!AVAILABILITY]
>
>以下增强功能仅适用于Sinch和Infobip提供程序。

已引入短信增强功能来改进消息传送功能：

* You can define and manage unique keywords for your SMS campaigns and journeys, enabling more personalized and efficient communication.

* You can create and deliver a default SMS message when a keyword is not recognized.

* You can now edit or delete an SMS API Channel Configuration.

<!--**Journeys**-->

<!--* **Path experiment in journeys** - With the journey path experiment, you can now define and track key metrics for your journey paths, allowing you to measure the impact of your activities and to provide clearer insights into your performance. -->

&lt;!—* **最大实时历程数** -Journey Optimizer现在在生产沙盒上具有500个实时历程的护栏，而不是100个。 实时历程的数量在历程画布中可见。<!-- DOCAC-10977-->

**数据集**

* **生存时间护栏** — 从2024年11月1日开始，将在新沙盒和新组织中向Journey Optimizer系统生成的数据集推出生存时间(TTL)护栏，如下所示：

   * 配置文件存储中的数据为 90 天
   * 数据湖中的数据为 13 个月

  This change will be rolled out to existing customer sandboxes subsequently in a second phase.

  Additionally, starting November 1st, streaming segmentation will no longer support the use of send and open events from tracking and feedback datasets. This change will apply to all customer sandboxes and orgs at that time. [了解详情](../data/datasets-ttl.md)

* ****[了解详情](../action/about-custom-action-configuration.md#define-the-message-parameters)

**报告**

* **决策报告**&#x200B;现已可用，可提供关于访客如何与您的体验进行交互的基本见解。

**数据治理和同意策略** - 发布日期：2024 年 10 月 7 日

* 现在，Journey Optimizer 中的所有渠道都会实施&#x200B;**数据治理策略**。对于在 Adobe Experience Platform 中创建了策略的客户，这些策略将作为渠道配置设置的一部分应用于营销操作。使用配置创建内容时，系统会检查所有个性化字段是否存在任何数据治理违规。如果发现违规，将无法发布历程或营销活动。[了解详情](../action/action-privacy.md)

* **自定义同意政策**&#x200B;现在适用于所有 Journey Optimizer 渠道。在发送消息或投放入站体验之前执行时，系统会检查用户是否同意在接收的内容中使用个性化字段。如果未获得同意，则不会显示体验。[了解详情](../action/consent.md)

  >[!NOTE]
  >
  >目前，同意策略仅适用于已购买 Adobe **Healthcare Shield** 或 **Privacy and Security Shield** 附加产品的组织。

**受众** - 发布日期：2024 年 10 月 8 日

* 定位 CSV 文件受众时，您现在可以在个性化编辑器以及历程和营销活动规则构建器中使用来自文件的属性。[了解详情](../audience/about-audiences.md)

* 现在可以将自定义上传（CSV 文件）中的受众和属性与 Healthcare Shield 或 Privacy and Security Shield 一起使用。

****

* Content templates are now available. You can speed up authoring your code-based experiences starting from a content template built by your developers. Using a content template will allow the marketer to just modify some values or fields, instead of composing the whole HTML or JSON content payload.

**决策**

[](https://experienceleague.adobe.com/docs/analytics-platform/using/cja-overview/cja-overview.html?lang=zh-Hans)This allows you, for example, to optimize on a custom &quot;purchases&quot; table rather than defined constraints such as clickthrough rate.&quot;
