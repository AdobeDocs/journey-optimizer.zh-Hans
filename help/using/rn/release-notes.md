---
solution: Journey Optimizer
product: journey optimizer
title: 发行说明
feature: Release Notes
topic: Content Management
description: Adobe Journey Optimizer 发行说明
exl-id: 06fa956a-b500-416e-9d42-b683c328e837
source-git-commit: a64cfe6a474864df02e18fdb772974d73ec58cc5
workflow-type: tm+mt
source-wordcount: '1602'
ht-degree: 92%

---

# 发行说明 {#release-notes}

>[!CONTEXTUALHELP]
>id="ajo_homepage_card1"
>title="新增功能？"
>abstract="**Adobe Journey Optimizer** 不断地提供新功能、对现有功能的增强和错误修复。会在每月的最后一周将所有更改整合到发行说明中。"

[!DNL Adobe Journey Optimizer] 不断地提供新功能、对现有功能进行增强和修复错误。所有更改将在每个月的最后一周汇总在这些发行说明中。 [!DNL Adobe Journey Optimizer] 原生构建于 [!DNL Adobe Experience Platform] 之上并继承了其所具备的最新创新技术和改进。在 [Adobe Experience Platform 发行说明](https://experienceleague.adobe.com/docs/experience-platform/release-notes/latest.html?lang=zh-Hans){target="_blank"}中，进一步了解这些更改。

## 2024 年 10 月更新 {#24-10-rn}

即将发行的&#x200B;**发行日期**： 2024年10月28日至30日

下面列出的[功能](#24-10-features)和[改进](#24-10-improvements)已于本月发布。

### 新功能 {#24-10-features}

<table>
<thead>
<tr>
<th><strong>更新的报告体验（正式发布）</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Journey Optimizer报告功能现已正式推出(GA)，并提高了与Customer Journey Analytics功能的互操作性，实现了两个平台的报告标准化，并提高了数据一致性和可靠性。 Journey Optimizer 与 Customer Journey Analytics 之间的这种无缝集成能够帮助更清晰地了解绩效指标，使用户能够做出更加明智的决策。</p>
<p>在正式发布后，引入了四个新功能：创建简单量度、创建和发布受众、使用Insight Builder提出临时问题以及安排报表自动通过电子邮件发送给关键收件人。</p>
<p>有关更多信息，请参阅<a href="../reports/report-cja-manage.md">详细文档</a>。</p>
<img src="assets/do-not-localize/ajo-cja.gif">
<p>发布日期：2024 年 10 月 16 日</p>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>历程中基于代码的体验</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>借助基于代码的体验渠道，Adobe Journey Optimizer 允许您对任何入站属性进行高级个性化和测试，从而向不同的接触点无缝投放定制化体验，如 Web 应用程序、移动应用程序、桌面应用程序、视频游戏机、电视连接设备、智能电视、网亭、ATM、物联网设备等。现在，历程画布中提供了基于代码的体验渠道。</p>
<p>有关更多信息，请参阅<a href="../code-based/create-code-based.md">详细文档</a>。</p>
<img src="../assets/do-not-localize/code-based-journey.gif"/>
<p>发布日期：2024 年 10 月 1 日</p>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>历程中的 Web 体验</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>借助 Web 渠道，Adobe Journey Optimizer 允许您通过入站 Web 历程为客户提供个性化 Web 体验。现在，可在历程画布中使用 Web 渠道。</p>
<p>有关更多信息，请参阅<a href="../web/create-web.md">详细文档</a>。</p>
<img src="../assets/do-not-localize/web-journey.gif"/>
<p>发布日期：2024 年 10 月 1 日</p>
</tr>
</tbody>
</table>

>[!IMPORTANT]
>
>目前的报告经验将于2025年1月停用。 在此日期之后，新的报告体验将成为标准。我们建议您熟悉新特性和功能，以确保顺利过渡。
>
> [了解如何开始使用 Journey Optimizer 的新报告界面](../reports/report-gs-cja.md)

### 改进 {#24-10-improvements}

**历程** - 发布日期：2024 年 10 月 3 日

* **自定义操作中的参数** - 自定义操作现在支持 NULL 和可选参数。[了解详情](../action/about-custom-action-configuration.md#define-the-message-parameters)

**数据治理和同意策略** - 发布日期：2024 年 10 月 7 日

* 现在，Journey Optimizer 中的所有渠道都会实施&#x200B;**数据治理策略**。对于在 Adobe Experience Platform 中创建了策略的客户，这些策略将作为渠道配置设置的一部分应用于营销操作。使用配置创建内容时，系统会检查所有个性化字段是否存在任何数据治理违规。如果发现违规，将无法发布历程或营销活动。[了解详情](../action/action-privacy.md)

* **自定义同意政策**&#x200B;现在适用于所有 Journey Optimizer 渠道。在发送消息或投放入站体验之前执行时，系统会检查用户是否同意在接收的内容中使用个性化字段。如果未获得同意，则不会显示体验。[了解详情](../action/consent.md)

  >[!NOTE]
  >
  >目前，同意策略仅适用于已购买 Adobe **Healthcare Shield** 或 **Privacy and Security Shield** 附加产品的组织。

**受众** - 发布日期：2024 年 10 月 8 日

* 定位 CSV 文件受众时，您现在可以在个性化编辑器以及历程和营销活动规则构建器中使用来自文件的属性。[了解详情](../audience/about-audiences.md)

* 现在可以将自定义上传（CSV 文件）中的受众和属性与 Healthcare Shield 或 Privacy and Security Shield 一起使用。

## 2024 年 9 月版 {#24-9-rn}

<!--
>[!CAUTION]
>
>**Early release notes below are subject to change without prior notice until the release date**. Links, screens and updated documentation are published at the release date.
>
-->

**发行日期**：2024 年 9 月 24-26 日

### 新功能 {#24-9-features}

此版本引入了下方详述的新功能。

<table>
<thead>
<tr>
<th><strong>适用于移动设备应用程序和网站的内容卡</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>内容卡是 Adobe Journey Optimizer 中新增的数字消息传送功能，可直接在移动应用和网站内提供个性化且引人入胜的内容。与传统推送通知不同，内容卡无缝集成到用户界面中，提供持续性的非侵入式更新，以增强用户交互和体验。</p>
<p>此功能允许营销人员向用户展示相关的富媒体内容，从而提高参与度，并确保会看到重要消息而不会中断用户历程。</p>
<p>有关更多信息，请参阅<a href="../content-card/get-started-content-card.md">详细文档</a>。</p>
<img src="assets/do-not-localize/content-card.gif"/>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>历程和营销活动中的审批 (LA)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>现在，通过审批策略，您可以在 Journey Optimizer 中设置审批流程，从而使营销团队可以确保营销活动及历程在投入使用之前由相应的负责人审查和签署。</p>
<p>目前，审批策略仅面向一部分组织提供（限量发布版）。要获得访问权限，请与 Adobe 代表联系。</p>
<p>有关更多信息，请参阅<a href="../test-approve/gs-approval.md">详细文档</a>。</p>
<img src="assets/do-not-localize/approval.gif"/>
</td>
</tr>
</tbody>
</table>

<!--<table>
<thead>
<tr>
<th><strong>Email Content Locking</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Journey Optimizer now allows you to lock content in email templates, either by locking the entire template or specific structures and component. This allows you to prevent unintentional edits or deletions, giving you greater control over template customization, and improving the efficiency and reliability of your email campaigns.</p>
<p>For more information, refer to the <a href="../content-management/gs-generative.md">detailed documentation</a>.</p>
<img src="assets/do-not-localize/gif-content-locking.gif">
</td>
</tr>
</tbody>
</table>-->

<table>
<thead>
<tr>
<th><strong>历程中的全局退出标准</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>现在，您可以在历程级别定义退出标准。通过添加退出条件，您可以在事件发生后（例如：购买）或符合受众的条件时，让用户档案立即退出历程。这将阻止用户从历程收到任何进一步的通信。</p>
<p>有关更多信息，请参阅<a href="../building-journeys/journey-properties.md#exit-criteria">详细文档</a>。</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>AI 助手内容加速器 </strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>创建邮件并对其进行个性化设置后，您可以使用 Journey Optimizer for Content Acceleration 中的 AI 助手将您的内容提升到新的水平。您现在可以使用 AI 助手，通过尝试不同的主标题和图像来优化邮件的影响。每个变体都是作为独特的处理方式进行管理，以衡量和比较哪个标题可以有效生成更多点击次数。</p>
<p>通过<a href="https://experienceleague.adobe.com/zh-hans/apps/journey-optimizer/ai-assistant-content-accelerator">我们的实时功能预览</a>获得亲身体验，该预览旨在让您亲自探索其功能并充分了解其能力。</a>。</p>
<p>有关更多信息，请参阅<a href="../content-management/gs-generative.md">详细文档</a>。</p>
<img src="assets/do-not-localize/ai-content.gif"/>
<p>发布日期：2024 年 9 月 12 日</p>
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
<p>发布日期：2024 年 9 月 3 日</p>
</br>
</td>
</tr>
</tbody>
</table>


### 改进 {#24-9-improvements}

此版本包含下方列出的改进。

**受众** - 发布日期：2024 年 9 月 17 日

<!--* The use of audiences from custom upload (CSV file) is now available for use with Privacy and Security Shield add-on.-->
* **许可证使用情况** - 许可证使用情况仪表板现在显示“符合资格的用户档案”，而不是“符合资格的受众”。[了解详情](../audience/license-usage.md)

**内容管理**

* 您现在可以在沙盒中导出内容模板和片段。[了解详情](../configuration/copy-objects-to-sandbox.md)

<!--**Data Governance**

* You can now apply data governance policies to Journey Optimizer channels, in addition to custom actions within journeys. This enhancement helps prevent the use of sensitive fields in communications by applying marketing actions directly within your channel configurations.    -->

<!--
**Conflict and priority management**

* **Priority score** - You can now assign a priority score to a campaign or a journey, ranging from 0 to 100. A higher number indicates a higher priority. When two campaigns or journeys use the same surface, Journey Optimizer will select the one with the highest priority score. If the campaigns have the same score, the campaign that was most recently modified will be chosen. Priority score is available for all inbound channels in campaigns, and for the in-app channel in journeys.    

* **View conflicts** - A new **View conflicts** button in journeys and campaigns now allows you to check whenever there's a possibility of overlap with other journeys or campaigns such as the start date, the targeted audience, or the selected channel configuration.
-->

**历程**

<!-- DOCAC-10977 * **Max number of Live journeys** - Journey Optimizer now has a guardrail of 500 live journeys on production sandboxes, instead of 100. The number of live journeys is visible in the journey canvas.-->

* **实时报告增强功能** - 实时报告可提供有关过去 24 小时内的历程绩效的深入见解。我们添加了新量度（已进入、已退出、已丢弃的用户档案和出错的用户档案）以增强此功能，以便您能直接从历程画布更深入地了解用户行为和表现。[了解详情](../building-journeys/report-journey.md)


* （发布日期：9 月 10 日）**自动重试读取受众** - 现在，在检索导出作业时，重试操作会被默认应用于受众触发的历程（从&#x200B;**读取受众**&#x200B;或&#x200B;**业务事件**&#x200B;开始）。如果在创建导出作业期间发生错误，则每 10 分钟重试一次，最多 1 小时。之后，我们将它视为失败。因此，这些类型的历程可以在预定时间之后 1 小时内执行。[了解详情](../building-journeys/read-audience.md#retries)

**电子邮件渠道**

* **已发送的电子邮件和密件抄送中的邮件标头** - 已为所有电子邮件添加了新邮件标头。对于已发送的每封电子邮件及其对应的密件抄送电子邮件副本来说，此标头值都是唯一的。此外，此标头存储在消息和密件抄送反馈数据集中，允许协调密件抄送副本和相应的已发送电子邮件信息。[了解详情](../configuration/archiving-support.md#bcc-header)

* **垃圾邮件评分** (GA) - 您现在可以在专用的&#x200B;**垃圾邮件报告**&#x200B;中检查您的垃圾邮件内容评分。通过 SpamAssassin，Adobe Journey Optimizer 现在可以测试您的电子邮件内容并为其评分，以检测 ISP 或邮箱提供商是否将其视为垃圾邮件。[了解详情](../content-management/spam-report.md)

**短信渠道**

* **编辑 API 凭据** - 您现在可以编辑短信 API 凭据中的设置，包括更新选择启用/禁用关键字和回复。

**API**

* **营销活动模拟 API** - 使用此 API 触发营销活动的校对作业。发送营销活动验证是一个异步过程，该 API 将返回一个 proofJobId，可用于检查验证的状态。[了解详情](https://developer.adobe.com/journey-optimizer-apis/references/simulations/){target="_blank"}

* （发布日期：9 月 10 日）[Adobe Journey Optimizer API 文档](https://developer.adobe.com/journey-optimizer-apis/references/simulations/){target="_blank"}现在具备交互功能。直接从文档页面探索 API 端点，以获得即时反馈并加快您的技术实施。


  所有 API 参考页面现在都有 **Try it（试试看）**&#x200B;功能，您可以使用它直接在文档网站页面上测试 API 调用。[获取所需的身份验证凭据](https://developer.adobe.com/journey-optimizer-apis/references/authentication/){target="_blank"}并开始使用该功能探索 API 端点。

  使用此新功能来探索 API 端点的请求和响应，以获得即时反馈并加快您的技术实施。

  >[!CAUTION]
  >
  >请注意，通过使用文档页面上的交互式 API 功能，您正在对端点进行真正的 API 调用。在试验生产沙盒时请记住这一点。

**配置**

* **IP 预热计划** - 此功能现在可供所有客户使用，包括已购买 Adobe **Healthcare Shield** 或 **Privacy and Security Shield** 附加产品的组织。[了解详情](../configuration/ip-warmup-gs.md)


![新闻稿](../assets/do-not-localize/nl-icon.png) 立即注册订阅 [Adobe Journey Optimizer 季度新闻稿](https://www.adobe.com/subscription/Adobe_Journey_Optimizer_NL.html){target="_blank"}，每个季度都能在收件箱中直接接收最新产品更新、精彩故事、用例、提示及更多内容。