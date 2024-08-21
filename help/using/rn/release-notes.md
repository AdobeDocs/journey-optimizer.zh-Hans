---
solution: Journey Optimizer
product: journey optimizer
title: 发行说明
feature: Release Notes
topic: Content Management
description: Adobe Journey Optimizer 发行说明
exl-id: 06fa956a-b500-416e-9d42-b683c328e837
source-git-commit: 068714fc2cae501fcc13a7f3112e5c1f3a3470bb
workflow-type: tm+mt
source-wordcount: '450'
ht-degree: 57%

---

# 发行说明 {#release-notes}

>[!CONTEXTUALHELP]
>id="ajo_homepage_card1"
>title="新增功能？"
>abstract="**Adobe Journey Optimizer** 不断地提供新功能、对现有功能的增强和错误修复。会在每月的最后一周将所有更改整合到发行说明中。"

[!DNL Adobe Journey Optimizer] 不断地提供新功能、对现有功能进行增强和修复错误。会在每月的最后一周将所有更改整合到发行说明中。

[!DNL Adobe Journey Optimizer] 原生构建于 [!DNL Adobe Experience Platform] 之上并继承了其所具备的最新创新技术和改进。在 [Adobe Experience Platform 发行说明](https://experienceleague.adobe.com/docs/experience-platform/release-notes/latest.html?lang=zh-Hans){target="_blank"}中，进一步了解这些更改。

![新闻稿](../assets/do-not-localize/nl-icon.png) 立即注册订阅 [Adobe Journey Optimizer 季度新闻稿](https://www.adobe.com/subscription/Adobe_Journey_Optimizer_NL.html){target="_blank"}，每个季度都能在收件箱中直接接收最新产品更新、精彩故事、用例、提示及更多内容。

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

<!--table>
<thead>
<tr>
<th><strong>Guided Channel Setup</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Guided Channel Setup enables you to automate and validate channel setup in a unified experience, speeding up the process of getting started with Journey Optimizer. This new guided setup streamlines rapid channel configuration, ensuring all necessary resources are readily installed and working within Experience Platform, Journey Optimizer, and Data Collection. This enables marketing, product and data engineering teams to quickly begin with campaign and journey creation.</p>
</td>
</tr>
</tbody>
</table-->

<!--table>
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

<!--table>
<thead>
<tr>
<th><strong>Improved Channel Configurations</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>The current channel surface capabilities have been enhanced for a consistent approach across all channels. You can now define, manage, and reuse these configurations for any of your channels, including Web, In-app messaging, or Code-based experience.</p>
<p><ul>
<li>Channel surfaces are now renamed to <strong>Channel configurations</strong></li>
<li>You can attach one or multiple marketing actions to enforce consent and data governance policies</li>
<li>Object level access control (OLAC) is now available for each channel configuration, allowing you to decide which of your users are allowed to create or use specific configurations</li>
<li>For some channels, you can create channel configurations that target multiple platforms. An example here would be an In-app messaging channel configuration that can target a web page, an iOS app and an Android app.</li>
</ul></p>
<p>For more information, refer to the <a href="../configuration/ip-warmup-gs.md">detailed documentation</a>.</p>
</td>
</tr>
</tbody>
</table-->

<table>
<thead>
<tr>
<th><strong>Marketo Engage自定义操作</strong><br/></th>
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
<p>片段全局变量可增强现有片段功能，以提高内容重用和脚本用例的效率。 片段现在可以使用输入变量并创建可在营销活动和历程内容中使用的输出变量。 片段可以在<a href="../personalization/use-expression-fragments.md">表达式片段</a>和<a href="../email/use-visual-fragments.md">可视化片段</a>中使用输入变量。 您可以使用这些变量在营销活动和历程中个性化消息内容和参数。</p>
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

此版本具有下面列出的改进。

**历程**

* 在&#x200B;**条件**&#x200B;活动中，默认情况下，**[!UICONTROL 时间条件]**&#x200B;现在按小时设置，从00:00到12:00。 [了解详情](../building-journeys/condition-activity.md#time_condition)
* 现在，在构建历程时，将显示来自&#x200B;**警报**&#x200B;按钮的警报，以便与其他警报保持一致，并提供一致的用户体验。 [了解详情](../building-journeys/troubleshooting.md#checking-for-errors-before-testing)
* 历程工具栏中的缩放选项已得到改进：缩放百分比现在可见，您现在可以更轻松地重置缩放值。

<!--**Audiences and Profiles**-->

<!--* The use of audiences from custom upload (CSV file) is now available for use with Privacy and Security Shield add-on.-->
<!--* When targeting a custom upload (CSV file) audience, you can now use attributes from the file in your campaigns and journeys. These attributes are available in the personalization editor, to personalize your messages, and the journey advanced expression editor.-->
<!--* The License usage dashboard now shows the count of Engageable Profiles. [Read more](../audience/license-usage.md)

**Push channel**

* You can now add your mobile application push credentials inside Adobe Journey Optimizer channel configuration settings. Creating an App surface in Adobe Experience Platform Data Collection is no longer required.
-->

### 其他更改 {#changes}

**报告**

* 当前的报告体验将从10月版起停用。 在此日期之后，新的报告体验将成为标准。 我们建议您熟悉新特性和功能，以确保顺利过渡。

[开始使用Journey Optimizer新的报表界面](../reports/report-gs-cja.md)
