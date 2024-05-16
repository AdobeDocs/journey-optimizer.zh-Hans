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
source-git-commit: b5e073ef1d0c579f430913d60442d7d4cfa620a3
workflow-type: tm+mt
source-wordcount: '836'
ht-degree: 26%

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
<p>您现在可以创建精细的频率上限规则，并通过规则集将它们应用于不同类型的营销通信。 这项新功能允许您通过设置跨渠道规则来控制受众接收消息的频率，这些规则会自动从消息和操作中排除过度请求的用户档案。</p>
<p>Business Rules功能目前仅作为公共测试版提供。</p>
<p>有关更多信息，请参阅<a href="../configuration/business-rules.md">详细文档</a>。</p>
</td>
</tr>
</tbody>
</table>


<table>
<thead>
<tr>
<th><strong>扩展的个性化数据 — 测试版</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>现在，您可以在Adobe Experience Platform数据集中查找和获取数据值，并使用这些值在Adobe Journey Optimizer中构建条件。 当使用对象数组中的属性定义了关系时，您可以利用查找数据集中的数据。 您可以为查找指定未启用配置文件的数据集。 启用后，您可以将配置文件属性用作指定数据集的联接键，以检索更多数据来进行个性化。</p>
</td>
</tr>
</tbody>
</table>

### 改进 {#e-improvements}

此版本包含下方列出的改进。

**Experience Decisioning**

从测试版到此版本，添加了以下改进：

* **Experience Decisioning +基于代码的体验(LA)**  — 您现在可以利用Experience Decisioning功能在基于代码的营销活动中使用决策项。 注意：基于代码的Experience Channel和Experience Decisioning不适用于已购买AdobeHealthcare Shield和Privacy and Security Shield附加产品的组织。 [了解详情](../code-based/get-started-code-based.md)
* **上下文数据**  — 您现在可以在决策规则和排名公式中利用Adobe Experience Platform的上下文数据。 [了解详情](../experience-decisioning/context-data.md)
* **新建权限**  — 新的“管理体验决策”权限现在可用于决策管理资源。 它允许您管理与体验决策相关的权限。 [了解详情](../experience-decisioning/gs-experience-decisioning.md)
* **上限规则**  — 您现在可以在Experience Decisioning中为给定决策项目添加多个上限规则。 这样，您就可以提高对优惠发送方式的控制级别。 [了解详情](../experience-decisioning/items.md#capping)
* **报表**  — 您现在可以使用以下项目创建Experience Decisioning营销活动的自定义报告仪表板 [!DNL Customer Journey Analytics]. [了解详情](../experience-decisioning/cja-reporting.md)


**决策管理**

* **多规则支持**  — 现在，您可以在决策管理中为给定优惠添加最多10个上限规则。 这样，您就可以增强对优惠发送方式的控制级别。
* **审核** - **更改日志** 选项卡允许您查看对优惠或决策所做的所有更改已被删除。 现在，可在&#x200B;**审核**&#x200B;菜单中查看与优惠和决策相关的更改。


**电子邮件渠道**

* **列表取消订阅**  — 继最近的Gmail和Yahoo公告之后，Journey Optimizer对批量发件人支持“post/1-click”List-Unsubscribe选项。
* **垃圾邮件评分** （测试版） — 您现在可以在专用的垃圾邮件报告中检查您的内容垃圾邮件评分。 使用SpamAssassin，Adobe Journey Optimizer现在可以测试您的电子邮件内容，并为它打分，以指示ISP提供商是否将其视为垃圾邮件。 [了解详情](../content-management/spam-report.md)


**受众**

* 现在，可以将来自受众构成和自定义上传（CSV文件）的受众和属性用于Healthcare Shield或Privacy and Security Shield。

**个性化**

* **表达片段**  — 表达式片段现在可用于 **应用程序内渠道**. [了解详情](../personalization/use-expression-fragments.md)

**历程**

* **合并策略** （有限可用性） — 历程使用的合并策略现在在整个历程中可见并保持一致。
* **mTLS支持** - Journey Optimizer API和自定义操作现在支持mTLS协议。
* **事件中的查找表**  — 现在，当使用对象数组中的属性定义了关系时，您可以利用查找数据集中的数据。 查找值将在历程（条件、自定义操作等）中可用 和消息个性化。
