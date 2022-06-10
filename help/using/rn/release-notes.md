---
title: 发行说明
description: Journey Optimizer 发行说明
exl-id: 06fa956a-b500-416e-9d42-b683c328e837
source-git-commit: 06eb2ebec284f807de7ddca5d26e13fc08194642
workflow-type: tm+mt
source-wordcount: '445'
ht-degree: 90%

---

# 发行说明 {#release-notes}

此页面列出了 [!DNL Journey Optimizer] 的所有新增功能和改进。您还可以查阅[最新文档更新](documentation-updates.md)页面以了解更多更改。

[!DNL Adobe Journey Optimizer] 原生构建于 [!DNL Adobe Experience Platform] 之上并继承了其所具备的最新创新技术和改进。在 [Adobe Experience Platform 发行说明](https://experienceleague.adobe.com/docs/experience-platform/release-notes/latest.html?lang=zh-Hans){target=&quot;_blank&quot;} 中，进一步了解这些变更。

![新闻稿](../assets/do-not-localize/nl-icon.png) 立即注册 [Adobe Journey Optimizer 季度新闻稿](https://www.adobe.com/subscription/Adobe_Journey_Optimizer_NL.html){target=&quot;_blank&quot;}邮件，每个季度就能在收件箱中直接接收最新产品更新、精彩故事、用例、提示及更多内容。

## 2022 年 5 月版 {#may-2022-release}

### 新功能

<table>
<thead>
<tr>
<th><strong>消息频度规则</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>您现在可以设置跨渠道业务规则，以自动从消息和操作中排除遭到过量请求的用户档案。</p>
<img src="assets/frequency-rn.gif"/>
<p>有关更多信息，请参阅<a href="../configuration/frequency-rules.md">详细文档</a>。</p>
</td>
</tr>
</tbody>
</table>


<!--table>
<thead>
<tr>
<th><strong>Email BCC</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Availability date: <strong>May, 31</strong></p>
<p>You can now use the Email BCC (blind carbon copy) capability to store emails sent by Adobe Journey Optimizer. Enable this option in your email presets so that every email sent is blind-copied to your BCC address.</p>
<img src="assets/bcc-rn.gif"/>
<p>For more information, refer to the <a href="../configuration/email-settings.md#bcc-email">detailed documentation</a>.</p>
</td>
</tr>
</tbody>
</table-->


<table>
<thead>
<tr>
<th><strong>决策管理 - 人工智能排名自动优化模型</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>现在，您可以在决策管理中使用经过培训的模型系统。 此新功能可为给定用户档案显示优惠排名。</p>
<img src="assets/optimization.gif"/>
<p>有关更多信息，请参阅<a href="../offers/offer-activities/configure-offer-selection.md#use-ranking-strategy">详细文档</a>。</p>
</td>
</tr>
</tbody>
</table>

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
<th><strong>Journey Optimizer 审核日志</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>您现在可以监测用户对 Adobe Journey Optimizer 资源执行的操作。</p>
<img src="assets/audit-rn.gif"/>
<p>有关更多信息，请参阅<a href="../reports/audit-logs.md">详细文档</a>。</p>
</td>
</tr>
</tbody>
</table>

### 改进

**个性化**

* **用于字符隐藏的新辅助函数** - 使用 `mask` 辅助函数，可将字符串的一部分替换为“X”字符。 [了解详情](../personalization/functions/string.md#mask)

**登陆页面**

* **不包含表单的登陆页面** - 您现在可以创建并发布不包含表单且无需访客执行任何操作的登陆页面。
* **登陆页面模板** - 现在，您可以将登陆页面另存为模板，并在创建其他登陆页面时重复使用。 [了解详情](../landing-pages/lp-templates.md)
* **返回主页面** - 您现在可以从同一登陆页面中的任何子页面添加指向主页面的链接。
* **自定义 JavaScript 支持** - 您现在可以向登陆页面内容添加自定义 JavaScript 以执行高级样式或向登陆页面添加自定义行为。	[了解详情](../landing-pages/lp-custom-js.md)

**历程**

* **读取区段** - 现在，一次性读取区段历程在历程执行 30 天后会变为“已完成”状态。 对于计划的读取区段，此期限为上次执行后的 30 天。 [了解详情](../building-journeys/read-segment.md)
* **表达式编辑器** - 添加了 [limit](../building-journeys/functions/functionlimit.md) 函数，以限制列表的项目数。 现在，使用 [sort](../building-journeys/functions/functionsort.md) 函数可对列表对象进行排序。 此外，还向 [disctinct](../building-journeys/functions/functiondistinct.md) 和 [distinctWithNull](../building-journeys/functions/functiondistinctwithnull.md) 函数添加了 listObject 支持。

**管理**

* **许可证使用功能板更新**  — 许可证使用情况功能板(位于 [!DNL Adobe Journey Optimizer] 用户界面现在可以准确地反映 **许可** 平均用户档案丰富度。 此量度表示形式中将显示一个删除，这意味着许可证限制现在可以正确报告。 [了解详情](../segment/licence-usage.md)
