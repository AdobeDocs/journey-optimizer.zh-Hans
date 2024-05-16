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
source-git-commit: 8dacf28f4c3217a57e648b3c80e1724d9794c9ea
workflow-type: tm+mt
source-wordcount: '699'
ht-degree: 34%

---

# 早期发行说明 {#e-release-notes}

[!DNL Adobe Journey Optimizer] 不断地提供新功能、对现有功能进行增强和修复错误。所有更改会在每月末整合到[发行说明](release-notes.md)中。

以下早期发行说明可能会在正式发行日期之前发生更改，恕不另行通知。在发行当日，会在[发行说明](release-notes.md)中发布链接、屏幕和更新文档。

## 2024年5月早期发行说明 {#e-2024}

**发行日期**： 2024年5月21日至22日

### 新功能 {#e-features}

此版本引入了下方详述的新功能。


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
<p>这些决策项目通过新的基于代码的体验渠道(现在可在Journey Optimizer促销活动中访问)无缝集成到广泛的集客界面中。 Experience Decisioning决策策略仅适用于基于代码的体验营销活动。</p>
<p>目前，体验决策功能仅面向一部分组织提供（限量发布版）。要获得访问权限，请与 Adobe 代表联系。</p>
<img src="assets/do-not-localize/gif-exd.gif"/>
<p>有关更多信息，请参阅<a href="../experience-decisioning/gs-experience-decisioning.md">详细文档</a>。</p>
</td>
</tr>
</tbody>
</table>


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
<th><strong>业务规则 — 测试版</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>您现在可以创建精细的频率上限规则，并通过规则集将它们应用于不同类型的营销通信。 </p>
</td>
</tr>
</tbody>
</table>


<table>
<thead>
<tr>
<th><strong>本地查找的多实体支持 — Beta版</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>待定</p>
</td>
</tr>
</tbody>
</table>


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

### 改进 {#e-improvements}

此版本包含下方列出的改进。

**Experience Decisioning**

从Beta版到洛杉矶版，已添加以下改进：

* **Experience Decisioning +基于代码的体验(LA)**：您现在可以利用Experience Decisioning功能在基于代码的营销活动中使用决策项。 注意：基于代码的Experience Channel和Experience Decisioning不适用于已购买AdobeHealthcare Shield和Privacy and Security Shield附加产品的组织。 [了解详情](../code-based/get-started-code-based.md)
* 您现在可以在决策规则和排名公式中利用Adobe Experience Platform中的上下文数据。 [了解详情](../experience-decisioning/context-data.md)
* 现在，决策管理资源具有新的“管理体验决策”权限。它允许您管理与体验决策相关的权限。 [了解详情](../experience-decisioning/gs-experience-decisioning.md)
* 您现在可以在体验决策中对特定决策项添加多个上限规则。这样，您就可以提高对优惠发送方式的控制级别。 [了解详情](../experience-decisioning/items.md#capping)
* 您现在可以使用以下内容创建Experience Decisioning营销活动的自定义报告仪表板 [!DNL Customer Journey Analytics]. [了解详情](../experience-decisioning/cja-reporting.md)


**Offer Decisioning**

* **多规则支持**  — 现在，您可以在决策管理中为给定优惠添加最多10个上限规则。 这样，您就可以增强对优惠发送方式的控制级别。
* **审核** - **更改日志** 选项卡允许您查看对优惠或决策所做的所有更改已被删除。 现在，可在&#x200B;**审核**&#x200B;菜单中查看与优惠和决策相关的更改。


**电子邮件渠道**

* **列表取消订阅**  — 继最近的Gmail和Yahoo公告之后，Journey Optimizer对批量发件人支持“post/1-click”List-Unsubscribe选项。
* **垃圾邮件评分**  — 您现在可以在专用的垃圾邮件报告中检查您的内容垃圾邮件评分。 使用SpamAssassin，Adobe Journey Optimizer现在可以测试您的电子邮件内容，并为它打分，以指示ISP提供商是否将其视为垃圾邮件。 [了解详情](../content-management/spam-report.md)


**受众**

* 现在，可以将来自受众构成和自定义上传（CSV文件）的受众和属性用于Healthcare Shield或Privacy and Security Shield。

**个性化**

* **查找表**  — 现在，当使用对象数组中的属性定义了关系时，您可以利用查找数据集中的数据。 查找值将在历程（条件、自定义操作等）中可用 和消息个性化。
* **表达片段**  — 表达式片段现在可用于应用程序内渠道。

**历程**

* **合并策略**  — 现在可以配置合并策略并在历程中使用。
* **mTLS支持** - Journey Optimizer API和自定义操作现在支持mTLS协议。
