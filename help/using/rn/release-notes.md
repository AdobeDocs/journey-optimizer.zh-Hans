---
solution: Journey Optimizer
product: journey optimizer
title: 发行说明
feature: Release Notes
topic: Content Management
description: Adobe Journey Optimizer 发行说明
exl-id: 06fa956a-b500-416e-9d42-b683c328e837
source-git-commit: b3e683e503f1784d61f6de4f0d866fc965515c1c
workflow-type: tm+mt
source-wordcount: '924'
ht-degree: 83%

---

# 发行说明 {#release-notes}

>[!CONTEXTUALHELP]
>id="ajo_homepage_card1"
>title="新增功能？"
>abstract="**Adobe Journey Optimizer** 不断地提供新功能、对现有功能的增强和错误修复。会在每月的最后一周将所有更改整合到发行说明中。"

[!DNL Adobe Journey Optimizer] 不断地提供新功能、对现有功能进行增强和修复错误。会在每月的最后一周将所有更改整合到发行说明中。

[!DNL Adobe Journey Optimizer] 原生构建于 [!DNL Adobe Experience Platform] 之上并继承了其所具备的最新创新技术和改进。在 [Adobe Experience Platform 发行说明](https://experienceleague.adobe.com/docs/experience-platform/release-notes/latest.html?lang=zh-Hans){target="_blank"}中，进一步了解这些更改。

![新闻稿](../assets/do-not-localize/nl-icon.png) 立即注册订阅 [Adobe Journey Optimizer 季度新闻稿](https://www.adobe.com/subscription/Adobe_Journey_Optimizer_NL.html){target="_blank"}，每个季度都能在收件箱中直接接收最新产品更新、精彩故事、用例、提示及更多内容。

## 9 月更新 {#9-2024}

<table>
<thead>
<tr>
<th><strong>AI助手 — 内容加速器 </strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>创建消息并对其进行个性化后，在Journey Optimizer中使用AI助手进行内容加速以将内容提升到新的水平。 您现在可以使用AI助手通过尝试不同的主标题和图像来优化消息的影响。 每个变体都是作为独特的处理方式进行管理，以衡量和比较哪个标题可以有效生成更多点击次数。</p>
<p>使用<a href="https://experienceleague.adobe.com/en/apps/journey-optimizer/ai-assistant-content-accelerator">我们的实时功能预览</a>，亲身体验亲身体验并充分了解其功能。</a></p>
<p>有关更多信息，请参阅<a href="../content-management/gs-generative.md">详细文档</a>。</p>
<img src="assets/do-not-localize/ai-content.gif"/>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>引导式渠道设置</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>“引导式渠道设置”让您能够在一个统一的体验中自动化并验证渠道设置，从而加快开始使用 Journey Optimizer 的过程。这一新的引导式设置简化了快速渠道配置，确保能够在 Experience Platform、Journey Optimizer 和数据收集中随时安装并使用所有必要的资源。这使营销、产品和数据工程团队能够快速开始创建营销活动和历程。</p>
<p>有关更多信息，请参阅<a href="../configuration/set-mobile-config.md">详细文档</a>。</p>
<img src="assets/do-not-localize/guided-setup.gif"/>
<p>发布日期： 9月3日</p>
</br>
</td>
</tr>
</tbody>
</table>

**历程**

（可用性日期： 9月10日）**重试功能** — 现在，在检索导出作业时，默认情况下对受众触发的历程（从&#x200B;**读取受众**&#x200B;或&#x200B;**业务事件**&#x200B;开始）应用重试。 如果在创建导出作业期间发生错误，将每10mn重试一次，最长为1小时。 之后，我们将它视为失败。 因此，这些类型的历程可以在计划时间后最多1小时执行。 [了解详情](../building-journeys/read-audience.md#retries)

## 2024 年 8 月发行说明 {#8-2024}

**发布日期**：2024 年 8 月 20 日 - 21 日

<!--
>[!CAUTION]
>
>**Early release notes below are subject to change without prior notice until the release date**. Links, screens and updated documentation are published at the release date.
>
-->

### 新功能 {#8-features}

此版本引入了下方详述的新功能。

<!--
<table>
<thead>
<tr>
<th><strong>Content Cards (Limited Availability)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Content cards are a new digital messaging feature in Adobe Journey Optimizer that delivers personalized and engaging content directly within mobile apps and websites. Unlike traditional push notifications, Content Cards integrate seamlessly into the user interface, offering persistent, non-intrusive updates that enhance user interaction and experience.</p>
<p>This feature enables marketers to present relevant, rich media content to users, driving higher engagement and ensuring important messages are seen without disrupting the user journey.</p>
</br>
<p>Content card are currently only available for a set of organizations (Limited Availability). To gain access, contact your Adobe representative.</p>
</td>
</tr>
</tbody>
</table-->

<table>
<thead>
<tr>
<th><strong>改进了渠道配置</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>增强了当前渠道表面功能，从而跨所有渠道采用一致的方式。您现在可以为任何渠道定义、管理和重用这些配置，包括 Web、应用程序内消息或基于代码的体验。</p>
<p><ul>
<li>渠道表面现在重命名为<strong>渠道配置</strong></li>
<li>您可以附加一个或多个营销操作以强制执行同意和数据治理策略</li>
<li>对象级访问控制 (OLAC) 现在可用于每个渠道配置，允许您决定允许哪些用户创建或使用特定配置</li>
<li>对于某些渠道，您可以创建针对多个平台的渠道配置。以下示例是应用程序内消息传递渠道配置，可针对网页、iOS 应用程序和 Android 应用程序。</li>
</ul></p>
<p>有关更多信息，请参阅<a href="../configuration/channel-surfaces.md">详细文档</a>。</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Marketo Engage 自定义操作</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>您现在可以将 Adobe Journey Optimizer 与 Adobe Marketo Engage 集成以构建您的 B2B 用例。在历程中，新的自定义操作允许您将数据摄取到 Marketo。</p>
<p>有关更多信息，请参阅<a href="../action/marketo-engage.md">详细文档</a>。</p>
</td>
</tr>
</tbody>
</table>


<table>
<thead>
<tr>
<th><strong>内容片段中的变量</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>片段全局变量增强了现有的片段功能，以提高内容可重用性和脚本用例的效率。片段现在可以使用输入变量并创建可用于营销活动和历程内容的输出变量。片段可以在<a href="../personalization/use-expression-fragments.md">表达式片段</a>和<a href="../email/use-visual-fragments.md">可视化片段</a>中使用输入变量。您可以使用这些变量在营销活动和历程中个性化消息内容和参数。</p>
<p>有关更多信息，请参阅<a href="../personalization/use-expression-fragments.md">详细文档</a>。</p>
</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>IP 预热工作流</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>发布日期：8 月 13 日</p>
<p>如果使用全新的 IP 地址发送电子邮件，现在可以直接从用户界面轻松执行 IP 预热工作流。Adobe Journey Optimizer 提供了一种标准化的高效方法来预热 IP 地址，该方法遵循最佳实践以期实现最佳可投放性。</p>
<p>有关更多信息，请参阅<a href="../configuration/ip-warmup-gs.md">详细文档</a>。</p>
</td>
</tr>
</tbody>
</table>

### 改进 {#8-improvements}

此版本包含下方列出的改进。

**历程**

* 在&#x200B;**条件**&#x200B;活动中，**[!UICONTROL 时间条件]**&#x200B;默认按小时设置，从 00:00 到 12:00。[了解详情](../building-journeys/condition-activity.md#time_condition)
* 在构建您的历程时，警报现在从&#x200B;**警报**&#x200B;按钮显示，以与其他警报保持一致并带来一致的用户体验。[了解详情](../building-journeys/troubleshooting.md#checking-for-errors-before-testing)
* 历程工具栏中的缩放选项已得到改进：缩放百分比现在可见，并且可以轻松地重置缩放值。

<!--**Audiences and Profiles**-->

<!--* The use of audiences from custom upload (CSV file) is now available for use with Privacy and Security Shield add-on.-->
<!--* When targeting a custom upload (CSV file) audience, you can now use attributes from the file in your campaigns and journeys. These attributes are available in the personalization editor, to personalize your messages, and the journey advanced expression editor.-->
<!--* The License usage dashboard now shows the count of Engageable Profiles. [Read more](../audience/license-usage.md)-->

**推送渠道**

* 您现在可以在 Adobe Journey Optimizer 渠道配置设置中添加您的移动应用程序推送凭据。不再需要在 Adobe Experience Platform 数据收集中创建应用程序表面。

### 其他更改 {#changes}

**报告**

* 当前的报告体验将从 10 月版起停用。在此日期之后，新的报告体验将成为标准。我们建议您熟悉新特性和功能，以确保顺利过渡。

[Journey Optimizer 的新报告界面入门](../reports/report-gs-cja.md)

* 新报告体验中添加了新用例：

   * 直接在报告中创建自定义计算指标。
   * 从报告数据创建受众。
   * 使用探索性分析工具，根据您选择的&#x200B;**[!UICONTROL 维度]**&#x200B;和&#x200B;**[!UICONTROL 指标]**&#x200B;轻松创建表和可视化内容。

  有关更多信息，请参阅[详细文档](../reports/report-cja-manage.md)。
