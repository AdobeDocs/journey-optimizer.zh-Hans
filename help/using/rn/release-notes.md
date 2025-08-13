---
solution: Journey Optimizer
product: journey optimizer
title: 发行说明
feature: Release Notes
topic: Content Management
description: Adobe Journey Optimizer 发行说明
exl-id: 06fa956a-b500-416e-9d42-b683c328e837
source-git-commit: 667f1a2bd03c958d7d1a95c4f9fb3378417276c0
workflow-type: tm+mt
source-wordcount: '1460'
ht-degree: 96%

---

# 发行说明 {#release-notes}

>[!CONTEXTUALHELP]
>id="ajo_homepage_card1"
>title="新增功能"
>abstract="**Adobe Journey Optimizer** 不断地提供新功能、对现有功能的增强和错误修复。会在每月的最后一周将所有更改整合到发行说明中。"

[!DNL Adobe Journey Optimizer] 不断地提供新功能、对现有功能进行增强和修复错误。会在每月的最后一周将所有更改整合到发行说明中。[!DNL Adobe Journey Optimizer] 原生构建于 [!DNL Adobe Experience Platform] 之上并继承了其所具备的最新创新技术和改进。在 [Adobe Experience Platform 发行说明](https://experienceleague.adobe.com/docs/experience-platform/release-notes/latest.html?lang=zh-Hans){target="_blank"}中进一步了解这些更改。


## 营销活动编排

**发布日期**：2025 年 8 月 4 日

Journey Optimizer 现在包括&#x200B;**营销活动编排**，这是一项专门为品牌发起的批量营销活动而设计的新功能。此版本引入了营销活动编排画布和增强的数据建模。同时利用这两项功能，营销人员可以规划、定向和提供个性化的跨渠道营销活动。

>[!IMPORTANT]
>
>要访问Campaign Orchestration，您的许可证必须包括&#x200B;**Journey Optimizer — 营销活动和历程**&#x200B;或&#x200B;**Journey Optimizer — 营销活动**&#x200B;包。 请联系您的Adobe代表以确认您的许可证并在需要时进行更新。

![营销活动编排 GIF](assets/do-not-localize/release.gif)

它包括[关系架构和数据集](#oc-relational)与[营销活动画布](#oc-canvas)。这两项创新共同为 Journey Optimizer 中的批量营销活动编排建立了新标准。下面列出了关键功能。

### 关键功能 {#oc-capabilities}

* **多步骤工作流**

  使用专门构建的全新营销活动编排画布，推动复杂的多渠道批量营销活动。

* **按需受众**

  按需细分受众以便立即激活。

* **多实体分段**

  使用业务上下文（非人员维度，例如产品、店铺、续订、预订等）构建受众。

* **预发送可见性**

  在营销活动启动前和运行时，审查、改善和优化受众及营销活动

### 营销活动画布 {#oc-canvas}

专为批量营销活动构建的全新可视化编排界面。此画布支持：

* 针对多步骤、多渠道营销活动流进行可视化规划

* 支持通过关系查询构建的按需受众

* 高级受众拆分、等待和条件逻辑

* 应用业务规则和筛选条件后获得精确的预发送计数

### 关系架构和数据集 {#oc-relational}

Adobe Journey Optimizer现在支持链接到基于人员的配置文件的关系实体（例如，产品、商店、预订、合同）。 这允许跨多维数据结构进行分段和个性化，支持如下用例：

* 每项预订、订阅或合同对应一条消息

* 基于相关实体属性（例如，产品类别或店铺位置）进行分段

* 增强可寻址性（例如，发送到与实体绑定的所有已知联系人）

### 为什么这很重要

此版本使营销人员能够完全控制品牌发起的、基于受众的批量营销，并将灵活的数据建模与专门构建的编排体验相结合。它专为实时历程中的批量营销活动编排而设计，同时提供高级个性化和可扩展性。

### 了解详情

请参阅[营销活动编排文档](../orchestrated/gs-orchestrated-campaigns.md)以了解详情。

<!--
## August '25 pre release notes {#25-7-rn}

**Pre release notes below are subject to change without prior notice until the release availability date**. Links, screens and updated documentation are published at the release date.

See also [Adobe Experience Platform Pre-release notes](https://experienceleague.adobe.com/zh-hans/docs/experience-platform/release-notes/pre-release-notes){target="_blank"}.

**Release date**: August 19, 2025


### New capabilities {#Aug-25-8-features}

New capabilities coming with this release are detailed below.

### Improvements {#Aug-25-8-improv}

Improvements coming with this release are listed below.
-->

## ’25年8月更新 {#25.8-rn}

<table>
<thead>
<tr>
<th><strong>营销活动中的优化</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Journey Optimizer 现在提供了一些工具，可帮助您向营销活动的受众提供个性化的优化内容，让您能够运行内容试验、创建基于规则的目标选择以及使用两者的高级组合，从而最大限度提高营销活动的有效性。</p>
<p>通过优化，您可以：</p>
<ul>
<li>测试多个内容变体，确定最有效的消息内容。</li>
<li>根据用户属性和上下文数据提供个性化内容。</li>
<li>将目标选择和试验相结合，制定高级的营销活动策略。</li>
<li>筛选出不符合变体条件的用户。</li>
<li>确保后备机制到位，保持用户参与。</li>
</ul>
<P>营销活动上线后，将根据定义的标准评估轮廓。根据匹配的标准，向这些用户提供营销活动中相应的体验或内容。</p>
<p><img src="assets/do-not-localize/campaign-optimization.gif"/></p>
<p>发行日期： 2025年8月8日</p>
<p>有关更多信息，请参阅<a href="../campaigns/campaigns-message-optimization.md">详细文档</a></p>
</td>
</tr>
</tbody>
</table>



## 2025 年 7 月发行说明 {#25-7-rn}

**发布日期**：2025 年 7 月 29 日

### 新功能 {#features-25-7}

此版本包含的新功能详述如下。

#### 功能

<table>
<thead>
<tr>
<th><strong>品牌</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>您现在可以创建并自定义您的品牌，在所有宣传中清晰传达您的视觉风格与语言特征。通过品牌一致性评分，您可以实时获得内容是否符合品牌语调、风格和规范的反馈，帮助您在每一次沟通中始终保持品牌一致性。</p>
<p>此功能之前作为 Beta 版发布，现在可供在所有环境中使用（正式发布）。</p>
<p><img src="assets/do-not-localize/brand-score.gif"/></p>
<p>有关更多信息，请参阅<a href="../content-management/brands.md">详细文档</a>。</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>在电子邮件渠道中使用决策功能</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>您现在可以将决策策略添加到电子邮件历程和营销活动中。决策策略是产品建议的容器，利用决策引擎动态返回将会为每个受众成员提供的最佳内容。</p>
<p>此功能为限量发布版。请联系 Adobe 代表以获取访问权限。</p>
有关更多信息，请参阅<a href="../experience-decisioning/create-decision.md">详细文档</a></p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>LINE 渠道</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Adobe Journey Optimizer 已扩展其跨渠道功能，包括对 LINE 渠道的支持。通过此增强功能，您可以创建、编辑和预览 LINE 体验，从而实现更加个性化且富有吸引力的交互。借助 LINE，您可以与更多客户建立联系，发送相关内容并提高参与度。</p>
<p>LINE 渠道之前仅在申请时提供，现在所有用户均可使用（正式发布）。</p>
<p>有关更多信息，请参阅<a href="../../rp_landing_pages/line-landing-page.md">详细文档</a>。</p></td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>历程试运行</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>历程试运行是 Adobe Journey Optimizer 中的一种特殊历程发布模式，使历程设计人员能够在不接触真实客户或更新轮廓信息的前提下，使用真实生产数据对历程进行测试。此功能有助于历程设计人员在正式发布前验证历程设计和受众定位，从而增强信心。</p>
<img src="assets/do-not-localize/DryRun.gif">
<p>此功能之前为限量发布版，现在可供在所有环境中使用（正式发布）。</p>
<p>有关更多信息，请参阅<a href="../building-journeys/journey-dry-run.md">详细文档</a></p>
</td>
</tr>
</tbody>
</table>


<table>
<thead>
<tr>
<th><strong>历程的补充 ID</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>您现在可以通过用户档案 ID 以及其他标识符（如订单 ID、订阅 ID 或计划 ID）触发历程，使同一轮廓同时多次出现在同一历程中。这支持同时管理多个订单或订阅等场景，每个实例在整个历程中都遵循各自的路径。</p>
<p>在历程中使用补充 ID 的功能之前为限量发布版，现在可供在所有环境中使用。在此正式发布版本中，该功能现在支持读取受众历程。</p>
<p><img src="assets/do-not-localize/gif-supplemental.gif"/></p>
<p>有关更多信息，请参阅<a href="../building-journeys/supplemental-identifier.md">详细文档</a></p>
</td>
</tr>
</tbody>
</table>

### 产品内警报

现在可以订阅有关 Journey Optimizer 产品版本的&#x200B;**电子邮件和产品内警报**。

要进行订阅：

* 请导航到 **Adobe Experience Cloud 首选项**。
* 在&#x200B;**通知**&#x200B;下，找到 **Journey Optimizer 新版本**
* 启用应用程序内通知和电子邮件通知

![](assets/do-not-localize/pulse-notif.png){width="70%" align="left"}


### 历程条件的更改 {#ee-change@}

从 7 月 8 日起，在新的客户组织中，历程条件中使用的表达式编辑器将不再支持使用体验事件创建表达式。因此，[Experience Platform 数据源](../datasource/adobe-experience-platform-data-source.md)中的体验事件不能用于创建表达式。[此处](../building-journeys/exp-event-lookup.md)引述了使用体验事件创建表达式/逻辑的替代方法和最佳实践。

在单一历程中访问历程上下文事件数据的方式没有变化。在表达式和个性化编辑器中，用户可继续访问通过初始历程事件传入的数据。

请参阅[此常见问题解答](../building-journeys/exp-event-lookup.md#faq-ee)以了解详情。

### 改进 {#25-7-improv}

此版本包含的改进如下所述。

* **营销活动**

   * **营销活动中的多个入站操作** - 为简化营销活动编排，您现在可以在单个营销活动中定义多个入站操作。利用此功能，您可以同时向不同位置投放多个基于代码的体验、应用程序内消息、内容卡或 Web 操作，每个操作都包含特定内容。
     [了解详情](../campaigns/campaign-action.md#multi-action)

   * **营销活动清单重组** - 计划的营销活动和 API 触发的营销活动现在拆分到营销活动清单中的单独选项卡，以便更轻松地导航和管理。

[了解更多信息](../campaigns/modify-stop-campaign.md)

* **数据管理**
   * **决策管理系统数据集更新** - 现在，已删除的个性化和后备产品建议在“decision_object_repository_personalized_offers”和“decision_object_repository_fallback_offers”数据集中标记为已存档。数据集中的现有记录不会更改。

[了解更多信息](../offers/export-catalog/access-dataset.md)

* **历程**
   * **历程沙盒工具增强** - 在使用包导出和导入功能跨多个沙盒复制历程时，现在还可使用以下功能：
      * 选择目标上的现有事件
      * 独立于历程复制事件
      * 检测字段组/数据源关系，如果存在，则将其链接到目标；如果不存在，则创建关系。

[了解更多信息](../configuration/copy-objects-to-sandbox.md)

* **渠道 - 应用程序内**
   * **应用程序内键/值对** - 对于应用程序内消息，您可以定义键值对，以在消息负载中包含自定义变量。利用这些键值对，可基于特定配置和用例传递其他数据。[了解详情](../in-app/design-in-app.md)

* **渠道 - 内容卡**

   * **基于规则的营销活动淘汰** - 在编辑其他投放规则时，之前的投放规则选项已替换为三种不同的规则类型，以便更好地控制消息的时点和可见性：
      * 如果满足确定何时显示内容卡的条件，则显示消息。
      * 如果满足临时隐藏内容卡的条件，则不显示消息。如果再次满足显示条件，则可能会重新出现。
      * 如果满足永久阻止内容卡再次显示的条件，则淘汰消息。

[了解更多信息](../content-card/design-content-card.md)

* **决策**
   * **迁移工具 API** - Journey Optimizer 团队目前正在开发迁移工具 API，以便将决策管理实体迁移到决策。此工具支持在沙盒之间进行无缝迁移，并具有依赖项解析和回滚功能。如有兴趣，请联系 Adobe 代表。

* **个性化**
   * 个性化编辑器中新增了一个辅助函数“SHA256”。此函数用于计算并返回字符串的 sha256 哈希值。

[了解更多信息](../personalization/functions/string.md#sha256)
