---
title: 发行说明
description: Journey Optimizer 发行说明
exl-id: 06fa956a-b500-416e-9d42-b683c328e837
source-git-commit: 53a625c0e62fbfae703b40bb1d47105c168730ea
workflow-type: tm+mt
source-wordcount: '387'
ht-degree: 34%

---

# 发行说明 {#release-notes}

此页面列出了 [!DNL Journey Optimizer] 的所有新增功能和改进。您还可以查阅[最新文档更新](documentation-updates.md)页面以了解更多更改。

[!DNL Adobe Journey Optimizer] 原生构建于 [!DNL Adobe Experience Platform] 之上并继承了其所具备的最新创新技术和改进。在 [Adobe Experience Platform 发行说明](https://experienceleague.adobe.com/docs/experience-platform/release-notes/latest.html?lang=zh-Hans){target=&quot;_blank&quot;} 中，进一步了解这些变更。

![新闻稿](../assets/do-not-localize/nl-icon.png) 立即注册 [Adobe Journey Optimizer 季度新闻稿](https://www.adobe.com/subscription/Adobe_Journey_Optimizer_NL.html){target=&quot;_blank&quot;}邮件，每个季度就能在收件箱中直接接收最新产品更新、精彩故事、用例、提示及更多内容。

## 2022 年 5 月版 {#may-2022-release}

### 新功能

<!--table>
<thead>
<tr>
<th><strong>Message Frequency Rules</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>You can now set cross-channel business rules that will automatically exclude over-solicited profiles from messages and actions.</p>
<img src="assets/frequency-rn.gif"/>
<p>For more information, refer to the <a href="../configuration/frequency-rules.md">detailed documentation</a>.</p>
</td>
</tr>
</tbody>
</table-->


<table>
<thead>
<tr>
<th><strong>电子邮件密送</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>发布日期： <strong>5月31日</strong></p>
<p>您现在可以使用电子邮件密送（盲碳拷贝）功能存储由Adobe Journey Optimizer发送的电子邮件。 在电子邮件预设中启用此选项，以便发送的每封电子邮件都会被盲目复制到密件抄送地址。</p>
<img src="assets/bcc-rn.gif"/>
<p>有关更多信息，请参阅<a href="../configuration/email-settings.md#bcc-email">详细文档</a>。</p>
</td>
</tr>
</tbody>
</table>


<!--table>
<thead>
<tr>
<th><strong>Decision Management - AI Ranking auto-optimization model</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>You can now use trained model systems in Decision Management. This new capability ranks offers to display for a given profile.</p>
<img src="assets/optimization.gif"/>
<p>For more information, refer to the <a href="../offers/offer-activities/configure-offer-selection.md#use-ranking-strategy">detailed documentation</a>.</p>
</td>
</tr>
</tbody>
</table-->

<!--table>
<thead>
<tr>
<th><strong>Attribute-based Access Control (ABAC)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Permission management in Journey Optimizer has been extended to data access. You can now manage data access for specific teams or groups of users (i.e. internal, external, 3rd parties) ​and manage access to specific types of data (i.e. Sensitive Personal Data/SPD).</p>
<p>This capability is available for a limited set of customers.</p>
<p>For more information, refer to the <a href="../landing-pages/create-lp.md">detailed documentation</a>.</p>
</td>
</tr>
</tbody>
</table-->

<table>
<thead>
<tr>
<th><strong>Journey Optimizer审核日志</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>您现在可以监控用户对Adobe Journey Optimizer资源执行的操作。</p>
<img src="assets/audit-rn.gif"/>
<p>有关更多信息，请参阅<a href="../reports/audit-logs.md">详细文档</a>。</p>
</td>
</tr>
</tbody>
</table>

### 改进

**个性化**

* **用于字符隐藏的新帮助程序函数** - `mask` 帮助程序函数允许您将字符串的一部分替换为“X”字符。 [了解详情](../personalization/functions/string.md#mask)

**登陆页面**

* **没有表单的登陆页面**  — 您现在可以创建并发布不包含表单且无需访客执行任何操作的登陆页面。
* **登陆页面模板**  — 现在，您可以将登陆页面另存为模板，并在创建其他登陆页面时重复使用。 [了解详情](../landing-pages/lp-templates.md)
* **返回主页面**  — 您现在可以从同一登陆页面中的任何子页面添加指向主页面的链接。
* **自定义JavaScript支持**  — 您现在可以向登陆页面内容添加自定义JavaScript以执行高级样式或向登陆页面添加自定义行为。	[了解详情](../landing-pages/lp-custom-js.md)

<!--**Decision management**

* **HTML and JSON files support** - You can now drag and drop external HTML and JSON files from the AEM repository into the offer representation content.-->

**历程**

* **读取区段**  — 一次性读取区段历程现在在历程执行30天后变为“已完成”状态。 对于计划读取区段，则为上次执行该事件后的30天。 [了解更多信息](../building-journeys/read-segment.md)
* **表达式编辑器** - [限制](../building-journeys/functions/functionlimit.md) 函数，以限制列表的项目数。 的 [排序](../building-journeys/functions/functionsort.md) 函数现在允许您对列表对象进行排序。 还向 [disct](../building-journeys/functions/functiondistinct.md) 和 [distinctWithNull](../building-journeys/functions/functiondistinctwithnull.md) 函数。
