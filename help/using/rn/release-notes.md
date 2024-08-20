---
solution: Journey Optimizer
product: journey optimizer
title: 发行说明
feature: Release Notes
topic: Content Management
description: Adobe Journey Optimizer 发行说明
exl-id: 06fa956a-b500-416e-9d42-b683c328e837
source-git-commit: d971d857a480868f5ef502f3a3f2c209afc93cca
workflow-type: tm+mt
source-wordcount: '604'
ht-degree: 70%

---

# 发行说明 {#release-notes}

>[!CONTEXTUALHELP]
>id="ajo_homepage_card1"
>title="新增功能？"
>abstract="**Adobe Journey Optimizer** 不断地提供新功能、对现有功能的增强和错误修复。会在每月的最后一周将所有更改整合到发行说明中。"

[!DNL Adobe Journey Optimizer] 不断地提供新功能、对现有功能进行增强和修复错误。会在每月的最后一周将所有更改整合到发行说明中。

[!DNL Adobe Journey Optimizer] 原生构建于 [!DNL Adobe Experience Platform] 之上并继承了其所具备的最新创新技术和改进。在 [Adobe Experience Platform 发行说明](https://experienceleague.adobe.com/docs/experience-platform/release-notes/latest.html?lang=zh-Hans){target="_blank"}中，进一步了解这些更改。

![新闻稿](../assets/do-not-localize/nl-icon.png) 立即注册订阅 [Adobe Journey Optimizer 季度新闻稿](https://www.adobe.com/subscription/Adobe_Journey_Optimizer_NL.html){target="_blank"}，每个季度都能在收件箱中直接接收最新产品更新、精彩故事、用例、提示及更多内容。

## 2024 年 8 月早期发行说明 {#e-2024}

**发布日期**：2024 年 8 月 20 日 - 21 日

>[!CAUTION]
>
>**在发行日期**&#x200B;之前，下面的早期发行说明可能会有所更改，恕不另行通知。 链接、屏幕和更新文档在发布日期发布。
>

### 新功能 {#e-features}

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
<th><strong>Content Cards</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Content card is a new digital messaging feature in Adobe Journey Optimizer that delivers personalized and engaging content directly within mobile apps and websites. Unlike traditional push notifications, Content Cards integrate seamlessly into the user interface, offering persistent, non-intrusive updates that enhance user interaction and experience.</p>
<p>This feature enables marketers to present relevant, rich media content to users, driving higher engagement and ensuring important messages are seen without disrupting the user journey.</p>
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
<p>片段现在可以在<a href="../personalization/use-expression-fragments.md">表达式片段</a>和<a href="../email/use-visual-fragments.md">可视化片段</a>中使用输入变量。 您可以使用这些变量在营销活动和历程中个性化消息内容和参数。</p>
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


### 改进 {#e-improvements}

此版本具有下面列出的改进。

**历程**

<!--* In the **Condition** activity, by default, the Time condition is now set by hour, from 00:00 to 12:00. [Read more](../building-journeys/condition-activity.md#time_condition)-->
* 现在，在构建历程时，警报将显示在下拉列表中，以便与活动警报保持一致，并提供一致的用户体验。 [了解详情](../building-journeys/troubleshooting.md#checking-for-errors-before-testing)
* 历程工具栏中的缩放选项已得到改进：缩放百分比现在可见，您现在可以轻松地将缩放值重置为100%。

**受众**

* 现在，可以将自定义上传的受众（CSV文件）用于Privacy and Security Shield加载项。
* 在定位自定义上传（CSV文件）受众时，您现在可以在营销活动和历程中使用文件中的属性。 这些属性在个性化编辑器和历程高级表达式编辑器中可用，用于个性化消息。

## 2024 年 7 月发行说明 {#24-7-2024}

**发布日期**：2024 年 7 月 30 日至 31 日

### 新功能 {#27-4-features}

此版本引入了下方列出的新功能。

<table>
<thead>
<tr>
<th><strong>任何提供商的短信渠道（Beta 版）</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>除了默认短信提供商 Sinch、Infobip 和 Twilio 之外，您现在还可以在 Journey Optimizer 中配置其他短信提供商。</p>
<img src="assets/do-not-localize/byo_sms.gif"/>
<p>有关更多信息，请参阅<a href="../sms/sms-configuration-custom.md">详细文档</a>。</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>联合受众构成（限量发布）</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>现在可在 Adobe Journey Optimizer 中使用联合受众构成。它允许企业组合数据，以便在各种用例中更好地利用数据。通过这种新方法，作为 Adobe Real-Time Customer Data Platform 和/或 Adobe Journey Optimizer 用户，您可以直接从现有数据仓库联合数据集，以便在一个系统中丰富 Adobe Experience Platform 受众和属性。</p>
<p>有关更多信息，请参阅<a href="https://experienceleague.adobe.com/zh-hans/docs/federated-audience-composition/using/home"  target="_blank">详细文档</a>。</p>
</td>
</tr>
</tbody>
</table>

### 改进 {#27-4-improvements}

此版本包含下方列出的改进。

**历程**

* （发布日期：7 月 8 日）**历程事件配置中的高级表达式编辑器** - 现在，您可以在配置事件时利用高级表达式编辑器，从而定义更复杂的表达式或在事件 ID 条件中使用函数。[了解详情](../event/about-creating.md#adv-exp-editor)

