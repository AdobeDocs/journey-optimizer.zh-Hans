---
solution: Journey Optimizer
product: journey optimizer
title: Journey Optimizer 的预发行说明
description: Adobe Journey Optimizer 预发行说明
feature: Release Notes
exl-id: 6e7d1300-8efd-4fdc-90e3-3ccdc3babd2f
TQID: https://experienceleague.adobe.com/951PJzmmITN1nSUapVomlYnPws9pS0TosI1Gl3R9yL4
product_v2:
  - id: cb954087-f4fc-4456-afb9-e939cabcdc79
    internal-label: Journey Optimizer
feature_v2:
  - id: bb359667-ec7d-4d4b-8663-5850fc219d32
    internal-label: Administration
subfeature_v2:
  - id: a7b2bfc5-be71-4740-b371-76fa6be8df02
    internal-label: Journey Optimizer release notes
source-git-commit: d645b6528fa7a1ae5169f129613f9085672e2ebb
workflow-type: tm+mt
source-wordcount: '901'
ht-degree: 19%
---

# 预发行说明 {#e-release-notes}

Adobe Journey Optimizer 不断地提供新功能、对现有功能的增强和错误修复。 所有更改会在每月末整合到[发行说明](release-notes.md)中。

## 2026年9月预发行说明 {#sep-26-rn}

**以下预发行说明可能会在正式发行日期之前有所更改，恕不另行通知**。 一旦更改发布到生产环境，链接、屏幕和更新的文档就会发布。 虽然大多数更改将在发布日期交付，但其中一些更改可能会稍后推出 — 有关详细信息，请参阅为每个条目列出的发布日期。

另请参阅 [Adobe Experience Platform 预发行说明](https://experienceleague.adobe.com/zh-hans/docs/experience-platform/release-notes/pre-release-notes){target="_blank"}。

**发行日期**： 2026年9月22日至23日


<!--
### Onboarding {#sep-26-onboarding}

The following capability is coming to onboarding in this release.

<table>
<thead>
<tr>
<th><strong>Guided capabilities for onboarding emails and journeys (General Availability)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Transitioning to Adobe Journey Optimizer from another marketing platform is easier with guided capabilities that help you move existing email content and journeys into Journey Optimizer. A <strong>dedicated workspace</strong> lets you reuse what you have instead of rebuilding from scratch.</p>
<p>Previously released in Limited Availability, this capability is now available to all environments (General Availability).</p>
</td>
</tr>
</tbody>
</table>

-->

### 历程 {#sep-26-journeys}

在此版本中，历程中即将提供以下功能和改进。

* **减少等待和事件活动的步骤事件** — 不再为&#x200B;**等待**&#x200B;活动和&#x200B;**事件**&#x200B;活动生成步骤事件，因为在该活动中实际未处理配置文件。<!-- DRAFT: pending DOCAC sub-task under DOCAC-15691, see CJM-165835 -->
<!-- Documentation link: TBD -->

### 渠道 {#sep-26-channels}

此版本中的渠道即将提供以下功能和改进。

<table>
<thead>
<tr>
<th><strong>自定义出站渠道（正式发布）</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p><strong>自定义出站渠道</strong>允许管理员通过无代码渠道生成器将任何基于HTTP的出站消息渠道（如WeChat、Kakao Talk、Messenger或专有提供商）直接引入Journey Optimizer。 配置后，自定义渠道可在营销活动、历程和编排的营销活动中使用，并具有与原生渠道相同的完整功能集：使用表达式编辑器进行个性化、内容实验、预览和校样、开箱即用的报告以及同意和治理实施。</p>
<p>在此版本中，自定义出站渠道还获得了几项新功能：</p>
<ul>
<li>通过Journey Optimizer编辑器在自定义渠道有效载荷中使用Personalization Decisioning，与在基于代码的体验中一样。</li>
<li>将业务规则应用于自定义渠道，就像在本机渠道上一样。</li>
<li>在渠道列表中，为API触发的营销活动选择自定义渠道（这在以前是不可能的）。</li>
<li>为自定义渠道定义报表webhook并将其附加到渠道配置，以便您可以通过交互事件丰富Journey Optimizer报表。</li>
</ul>
</td>
</tr>
</tbody>
</table>

### 电子邮件渠道 {#sep-26-email-channel}

此版本中的电子邮件渠道即将提供以下功能和改进。

<table>
<thead>
<tr>
<th><strong>覆盖电子邮件渠道配置设置</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>在构建历程和营销策划时，您现在可以直接在历程或营销策划操作级别覆盖从所选渠道配置派生的电子邮件参数。</p>
<p>这样，您就可以使用配置文件属性或上下文数据对电子邮件标头字段（<strong>来自名称</strong>、<strong>来自电子邮件前缀</strong>、<strong>回复名称</strong>和<strong>回复电子邮件</strong>）、执行地址和列表取消订阅值进行个性化设置，以便更精确地控制。 特别是，这允许发件人详细信息反映每个收件人的相关顾问、位置或分支，而不是通过单个公司地址路由所有发送。</p>
</td>
</tr>
</tbody>
</table>

* **在电子邮件操作级别覆盖禁止列表现在** -Journey Optimizer允许您在历程和营销活动中直接在电子邮件操作级别覆盖禁止列表行为。 这允许团队在需要专用发送配置的操作性或合规性关键通信方面有更大的灵活性，同时保留所有其他发送的现有全局禁止列表控制。 此增强功能可帮助组织准确处理异常场景，而无需更改其更广泛的抑制治理模型。

* **电子邮件创作中的URL语法验证** — 现在，Journey Optimizer会验证电子邮件创作流程中较早的URL，并在检测到语法格式错误时显示更清晰的指导。 这有助于作者在最终确定之前捕获问题、减少发布错误并提高投放可信度。

### 电子邮件设计器 {#sep-26-email-designer}

此版本中的Email Designer即将提供以下功能和改进。

<table>
<thead>
<tr>
<th><strong>对电子邮件主题变体的深色模式支持</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>电子邮件主题现在支持深色模式，因此每个颜色变体都可以呈现一种量身定制的外观，适合在启用深色模式的客户端中查看电子邮件的收件人。</p>
<p>启用后，将自动为每个变体生成一个默认的深色调色板，您可以使用不同的调色板或您自己的自定义颜色进一步对其进行自定义 — 这与浅色模式设计无关，因此在一个模式下所做的更改不会影响另一个模式。</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>直接从Email Designer中的PSD文件导入Dynamic Media模板</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>电子邮件Designer的Dynamic Media组件现在可让您在浏览现有Dynamic Media模板之外，直接导入Photoshop (PSD)文件作为新模板。 将PSD文件拖放到组件中，Adobe Journey Optimizer会自动将其转换为存储在Dynamic Media中的Dynamic Media模板 — 无需手动转换或穿过Adobe Experience Manager来回转换。 导入模板后，您可以使用内置的Dynamic Media编辑器编辑该模板，这与电子邮件Designer中的Adobe Express内容具有相同的体验。</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>电子邮件Designer中的新表组件</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Email Designer现在包含内置<strong>表组件</strong>，允许您直接在电子邮件中构建行和列中的内容。 将组件拖放到画布上，自定义行和列的数量，并单独设置每个单元格的样式，以创建清晰、有序的布局，而无需依赖自定义HTML。</p>
</td>
</tr>
</tbody>
</table>

* **电子邮件主题中自定义字体的回退字体** — 您现在可以为通过电子邮件主题应用的任何自定义(Web)字体定义回退字体。 如果订阅者的电子邮件客户端不支持该自定义字体，Adobe Journey Optimizer会自动显示指定的后备字体，而不是将选项保留给电子邮件客户端的默认字体。 这样可使电子邮件排版更接近于您的品牌准则，并减少电子邮件客户端中字体渲染不一致的情况。
