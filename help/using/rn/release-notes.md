---
solution: Journey Optimizer
product: journey optimizer
title: 发行说明
feature: Release Notes
topic: Content Management
description: Journey Optimizer 发行说明
exl-id: 06fa956a-b500-416e-9d42-b683c328e837
source-git-commit: 5ce388e5d86950e5cc6b173aab48225825f1c648
workflow-type: ht
source-wordcount: '675'
ht-degree: 100%

---

# 发行说明 {#release-notes}

>[!CONTEXTUALHELP]
>id="ajo_homepage_card1"
>title="新增功能？"
>abstract="**Adobe Journey Optimizer** 不断地提供新功能、对现有功能进行增强和修复错误。会在每月的最后一周将所有更改整合到发行说明中。"

[!DNL Adobe Journey Optimizer] 不断地提供新功能、对现有功能进行增强和修复错误。会在每月的最后一周将所有更改整合到发行说明中。

[!DNL Adobe Journey Optimizer] 原生构建于 [!DNL Adobe Experience Platform] 之上并继承了其所具备的最新创新技术和改进。在 [Adobe Experience Platform 发行说明](https://experienceleague.adobe.com/docs/experience-platform/release-notes/latest.html?lang=zh-Hans){target="_blank"}中，进一步了解这些更改。

![新闻稿](../assets/do-not-localize/nl-icon.png) 立即注册订阅 [Adobe Journey Optimizer 季度新闻稿](https://www.adobe.com/subscription/Adobe_Journey_Optimizer_NL.html){target="_blank"}，每个季度都能在收件箱中直接接收最新产品更新、精彩故事、用例、提示及更多内容。

## 5 月份更新 {#may-updates}

**发布日期**：2024 年 5 月 7 日

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

从 Beta 版到限量发布版，已添加以下改进：

* **体验决策 + 基于代码的体验 (LA)**：您现在可以利用体验决策功能在基于代码的营销活动中使用决策项。注释：基于代码的体验渠道和体验决策不适用于已购买 Adobe Health Shield 和 Privacy and Security Shield 附加产品的组织。[了解详情](../code-based/get-started-code-based.md)
* 现在，您可以在决策规则中利用 Adobe Experience Platform 的上下文数据并对公式排序。[了解详情](../experience-decisioning/context-data.md)
* 现在，决策管理资源具有新的“管理体验决策”权限。这允许您管理与体验决策相关的权限。[了解详情](../experience-decisioning/gs-experience-decisioning.md)
* 您现在可以在体验决策中对特定决策项添加多个上限规则。这样，您就可以增强对优惠发送方式的控制级别。[了解详情](../experience-decisioning/items.md#capping)
* 您现在可以使用 [!DNL Customer Journey Analytics] 创建体验决策营销活动的自定义报告仪表板。[了解详情](../experience-decisioning/cja-reporting.md)

## 2024 年 4 月发行说明 {#apr-2024}

**发布日期**：2024 年 5 月 2 日

### 新功能 {#apr-features}

<!--table>
<thead>
<tr>
<th><strong>Business rules - Private Beta</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>It is now possible to create and apply rule sets to your marketing communications.  </p>
</td>
</tr>
</tbody>
</table-->

<!--table>
<thead>
<tr>
<th><strong>Personalization - Local Lookups - Multi-Entity Support - Beta</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>TBD</p>
</td>
</tr>
</tbody>
</table-->

此版本引入了下方详述的新功能。

<table>
<thead>
<tr>
<th><strong>多媒体消息服务 (MMS) - 所有提供商</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>使用短信渠道时，您现在可以通过发送多媒体消息服务 (MMS) 消息（支持与客户共享图像、GIF 文件或视频）来增强沟通效果。最初仅适用于 Sinch，现在也适用于 Infobip 和 Twilio。</p>
<img src="assets/do-not-localize/mms.gif"/>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>改进了历程设计器和实时报告</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>此版本具有改进的用于历程的画布用户界面，并提供更直观、高效的用户体验。活动情况更清晰，通过更少的单击操作即可显示更多有关历程画布的信息。</p>
<img src="assets/new-canvas3.gif"/>
<p>除了改进的历程画布设计之外，我们还引入了在历程画布中直接查看过去 24 小时的报告指标的功能。 </p>
<img src="assets/new-canvas6bis.png"/>
<p><strong>注意</strong>：从 4 月版本开始，这些更改将逐步在所有环境中推出。</p>
<p>有关更多信息，请参阅<a href="new-canvas.md">详细文档</a>。</p>
</td>
</tr>
</tbody>
</table>

<!-- table>
<thead>
<tr>
<th><strong>AI Assistant - Experience Variant Generation - Beta</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Once you have created and personalized your message, take your content to the next level with the AI assistant. You can now use the AI assistant to optimize your message's impact by experimenting with different main titles, and images. Each variant is managed as a unique Treatment, to measure and compare which title effectively generates more clicks.</p>
</td>
</tr>
</tbody>
</table-->

<!--table>
<thead>
<tr>
<th><strong>IP Warmup Workflow - LA</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>You can now easily perform IP warmup workflows directly from the Journey Optimizer interface in a standardized and efficient way that follows the best practices for optimal deliverability.</p>
</td>
</tr>
</tbody>
</table-->

<!--table>
<thead>
<tr>
<th><strong>Email Surface Personalization - Private beta </strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>You can now define dynamic subdomains and personalized header parameters when creating email channel surfaces, for increased flexibility and control over your email settings.</p>
</td>
</tr>
</tbody>
</table-->

### 改进 {#apr-improvements}

此版本包含下方列出的改进。

<!--
* **Expression Fragments supported for Web and In-App**: Expression fragments are now available for the Web and In-app channels. 
-->


<!--
* **DULE for AJO Channel Surface**: It is now possible to apply a label on certain profile attributes to restrict their usage inside a channel surface through marketing actions.
-->


<!--
* **List-Unsubscribe updates**: Following on the recent Gmail and Yahoo announcements for bulk senders, Journey Optimizer supports the "post/1-click" List-Unsubscribe option. 
-->

**配置**

* 现在，您可以在渠道表面级别选择营销操作。在表面中使用时，将利用与该营销操作关联的所有同意策略，以尊重客户的偏好。[了解详情](../action/consent.md#surface-marketing-actions)
* 现在，渠道表面可以使用对象级访问控制。[了解详情](../configuration/channel-surfaces.md#create-channel-surface)
* 在渠道表面中启用列表取消订阅时，您现在可以定义同意级别，以符合您管理来自所有其他来源的同意的方式。[了解详情](../email/email-settings.md#list-unsubscribe)

**内容管理**

* 您现在可以模拟所有渠道的内容模板。[了解详情](../content-management/content-templates.md#test-templates)

**个性化**

* 在表达式编辑器中提供了新的 **toInt** 辅助函数。它允许您将任意这些类型（数值、双精度、整数、长整数、浮点数、短整数、字节、布尔值、字符串）转换为整数。[了解详情](../personalization/functions/math.md#to-int)
