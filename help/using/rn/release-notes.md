---
title: 发行说明
description: Journey Optimizer 发行说明
exl-id: 06fa956a-b500-416e-9d42-b683c328e837
source-git-commit: 0e978d0eab570a28c187f3e7779c450437f16cfb
workflow-type: tm+mt
source-wordcount: '552'
ht-degree: 88%

---

# 发行说明 {#release-notes}

此页面列出了 [!DNL Journey Optimizer] 的所有新增功能和改进。您还可以查阅[最新文档更新](documentation-updates.md)页面以了解更多更改。

[!DNL Adobe Journey Optimizer] 原生构建于 [!DNL Adobe Experience Platform] 之上并继承了其所具备的最新创新技术和改进。在 [Adobe Experience Platform 发行说明](https://experienceleague.adobe.com/docs/experience-platform/release-notes/latest.html?lang=zh-Hans){target=&quot;_blank&quot;} 中，进一步了解这些变更。

![新闻稿](../assets/do-not-localize/nl-icon.png) 立即注册 [Adobe Journey Optimizer 季度新闻稿](https://www.adobe.com/subscription/Adobe_Journey_Optimizer_NL.html){target=&quot;_blank&quot;}邮件，每个季度就能在收件箱中直接接收最新产品更新、精彩故事、用例、提示及更多内容。

>[!CAUTION]
>
>7月25日，Adobe Journey Optimizer将发布 [新功能](../rn/inline-messages.md) 这可改进您为Journey Optimizer渠道（电子邮件、推送、短信）创作内容的方式。 作为Journey Optimizer的从业者，你现在 [创建和创作](../messages/get-started-content.md) 您的邮件直接从历程发送。 将为您执行历程的自动转换。 话虽如此，我们需要你的帮助。 了解 [必需步骤](../rn/inline-messages-steps.md).

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
<img src="assets/do-not-localize/SMS.gif"/>
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
<img src="assets/do-not-localize/stock-rn.gif"/>
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
<img src="assets/do-not-localize/bcc-rn.gif"/>
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

<!--table>
<thead>
<tr>
<th><strong>Dynamic Expression Builder</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>You can now create conditional content blocks across different authoring services to personalize your content. In addition to the Personalization Expression Library, the Expression editor provides a new Conditional Rule Builder to help you design and save your content blocks.</p>
<p>For more information, refer to the <a href="../building-journeys/read-segment.md#configuring-segment-trigger-activity">detailed documentation</a>.
</td>
</tr>
</tbody>
</table-->


### 改进

**决策管理**

* **HTML 和 JSON 文件支持** – 现在，您可将外部 HTML 和 JSON 文件从 Adobe Experience Cloud 资产库拖放到优惠呈现内容中。[了解详情](../offers/offer-library/add-representations.md#html-json)


**电子邮件**

* **另存为模板** – 现在，您可将电子邮件内容另存为模板，并在创建其他消息时重复使用。[了解详情](../design/email-templates.md)

<!--
**Journeys**

* **Ending a journey** - In the journey canvas, the **End** activity has been removed from the palette. End tags are now added by default at the end of each path and cannot be removed. This improvement allows better reporting of where a customer dropped out of the journey, without any action from the user.

-->

**管理**

<!--* **Allowed list in the UI** - You can now use the Journey Optimizer user interface to add new email addresses or domains to the allowed list.-->

* **预览跟踪 URL 参数** – 现在，配置消息预设时，如果定义了 URL 跟踪参数，则会显示所产生的跟踪 URL 的动态预览。[了解详情](../configuration/email-settings.md#url-tracking)

* **消息预设版本** - 现在，更新消息预设时，处理时间最长可能只需 3 小时。[了解详情](../configuration/message-presets.md#edit-message-preset)

* **IP 池版本** - 现在，更新 IP 池时，处理时间最长可能只需 3 小时。[了解详情](../configuration/ip-pools.md#edit-ip-pool)

<!--* **Personalize tracking URL parameters** - You can now use the Expression editor to configure URL tracking parameters in your message presets. [Learn more](../configuration/email-settings.md#url-tracking)-->

<!--
**Reporting**

* **Performance measurement** - A new **Reporting** tab is now available in the Administration > Configurations menu to set up reporting data sources.
-->
