---
solution: Journey Optimizer
product: journey optimizer
title: 发行说明
feature: Release Notes
topic: Content Management
description: Adobe Journey Optimizer 发行说明
exl-id: 06fa956a-b500-416e-9d42-b683c328e837
source-git-commit: 2afc9c4eb2a0433a22f1b369824086db2f5618ec
workflow-type: tm+mt
source-wordcount: '1776'
ht-degree: 44%

---

# 发行说明 {#release-notes}

>[!CONTEXTUALHELP]
>id="ajo_homepage_card1"
>title="新增功能"
>abstract="**Adobe Journey Optimizer** 不断地提供新功能、对现有功能的增强和错误修复。会在每月的最后一周将所有更改整合到发行说明中。"

[!DNL Adobe Journey Optimizer] 不断地提供新功能、对现有功能进行增强和修复错误。会在每月的最后一周将所有更改整合到发行说明中。[!DNL Adobe Journey Optimizer] 原生构建于 [!DNL Adobe Experience Platform] 之上并继承了其所具备的最新创新技术和改进。在 [Adobe Experience Platform 发行说明](https://experienceleague.adobe.com/docs/experience-platform/release-notes/latest.html?lang=zh-Hans){target="_blank"}中进一步了解这些更改。


## 2025 年 8 月预发行说明 {#25-8-rn}

**以下预发行说明可能会在正式发行日期之前有所更改，恕不另行通知**。链接、屏幕和更新文档在发布日期发布。

另请参阅 [Adobe Experience Platform 预发行说明](https://experienceleague.adobe.com/zh-hans/docs/experience-platform/release-notes/pre-release-notes){target="_blank"}。

**发布日期**：2025 年 8 月 19 日


### 新功能 {#Aug-25-8-features}

此版本包含的新功能详述如下。

<table>
<thead>
<tr>
<th><strong>暂停和恢复历程</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>您现在可以暂停和恢复历程。通过此功能，可以在不中断客户体验的情况下临时暂停实时历程，从而为历程设计人员提供了更好的控制力和灵活性。暂停后，不会发送任何通信，并且轮廓将停留在暂停状态，直到历程恢复。</p>
<p>您只能暂停和恢复一个历程，或者对一组历程执行批量暂停和恢复操作。</p>
<p>此外，您可以向暂停的历程应用全局筛选条件，以根据轮廓的属性排除轮廓。</p>
<p><!--img src="assets/do-not-localize/PauseResume.gif"/>--></p>
<p>此功能之前为限量发布版，现在可供在所有环境中使用（正式发布）。</p>
<p><!--For more information, refer to the <a href="../building-journeys/journey-pause.md">detailed documentation</a>--></p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>日程表视图</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>现在，历程和营销活动列表中提供日程表视图。该视图可让您在相应列表中查看所有历程和营销活动激活情况。</p>
<p>此功能之前为限量发布版，现在可供在所有环境中使用。在此正式发布版本中，该功能包括：</p>
<ul>
<li>日期中导航的设计改进，</li>
<li>能够查看草稿营销活动（如果已设置开始和结束日期），</li>
<li>用于隐藏和显示长时间运行的日历项目的新设置。</li>
</ul>
<p><!--img src="assets/do-not-localize/calendar.gif"/>--></p>
<p><!--For more information, refer to the <a href="../building-journeys/journey-ui.md#journeys-calendar">detailed documentation</a>--></p>
</td>
</tr>
</tbody>
</table>

<!--table>
<thead>
<tr>
<th><strong>Dark mode in the Email Designer</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>The Journey Optimizer Email Designer now offers the ability to switch to dark mode view, where you can additionally define specific custom settings that will display only for recipients reading their emails in dark mode.</p>
<p>Note the following:</p>
<ul>
<li>The dark mode final rendering may vary and depends on the recipient's email client.</li>
<li>Not all email clients support custom dark mode. Moreover, some email clients only apply their own default dark mode for all emails that are received. In both cases, the custom settings that you defined in the Email Designer cannot be rendered.</li>
</ul>
<P>This capability is currently in beta version and only available to beta customers. To join the beta program, contact your Adobe representative.</p>
<p><img src="assets/do-not-localize/dark-mode.gif"/></p>
<p>For more information, refer to the <a href="../email/dark-mode.md">detailed documentation</a></p>
</td>
</tr>
</tbody>
</table-->

<table>
<thead>
<tr>
<th><strong>使用 Adobe Experience Platform 数据进行个性化设置</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>在个性化编辑器中利用来自[!DNL Adobe Experience Platform]的数据来个性化您的内容和决策属性。 特别是，这允许您将属性的定义扩展到数据集中的其他数据，以便进行定期更改的批量更新，而无需一次手动更新一个属性。</p>
<p>在此版本中，引入了以下增强功能：</p>
<ul>
<li>支持入站渠道，</li>
<li>“datasetLookup”帮助程序函数现在可用于表达式和可视化片段中，以使用来自Adobe Experience Platform数据集的数据对内容进行个性化设置，</li>
<li>现在，通过数据集中的一个选项，您可以启用数据集以进行查找个性化，而无需执行API调用。</li>
</ul>
<p>此功能为限量发布版。请联系 Adobe 代表以获取访问权限。</p>
<p><!--img src="assets/do-not-localize/FILE.gif"/>--></p>
<p><!--For more information, refer to the <a href="../FILE.md">detailed documentation</a>--></p>
</td>
</tr>
</tbody>
</table>

<!--table>
<thead>
<tr>
<th><strong>Use Decisioning in email channel</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>You can now add Decision policies into email journeys and campaigns. Decision policies are containers for your offers that leverage the Decisioning engine to dynamically return the best content to deliver for each audience member.</p>
<p>Previously released in Limited Availability, this capability is now available to all environments (General Availability).</p>
<p><img src="assets/do-not-localize/FILE.gif"/></p>
<p><For more information, refer to the <a href="../FILE.md">detailed documentation</a></p>
</td>
</tr>
</tbody>
</table-->

<table>
<thead>
<tr>
<th><strong>历程路径优化</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Journey Optimizer现在为您提供各种工具，让您通过利用AI和实验框架来优化历程，同时确保条件和优化功能之间的无缝可用性和区分。</p>
<p>使用路径优化来定位、试验或使用人工智能来确定通信顺序、通信间隔时间、渠道组合以及您在旅程画布上梦见的任何内容。</p>
<p>此功能为限量发布版。请联系 Adobe 代表以获取访问权限。</p>
<p><!--img src="assets/do-not-localize/FILE.gif"/>--></p>
<p><!--For more information, refer to the <a href="../FILE.md">detailed documentation</a>--></p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>历程中的操作活动</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Journey Optimizer支持新的通用操作活动，通过该活动可配置单操作和多操作入站操作组，从而简化历程画布中的操作配置。 特别是，这项新功能允许：</p>
<ul>
<li>历程画布中简化的本机操作配置。</li>
<li>创建多操作入站节点的能力。</li>
<li>能够将优化添加到任何内置渠道操作中。</li>
<li>能够向任何操作同时添加试验选项和多语言选项。</li>
</ul>
<p>此功能为限量发布版。请联系 Adobe 代表以获取访问权限。</p>
<p><!--img src="assets/do-not-localize/pdf-attachments.gif"/>--></p>
<p><!--For more information, refer to the <a href="../FILE.md">detailed documentation</a>--></p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>电子邮件的PDF附件</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>您现在可以将静态PDF文件附加到使用Journey Optimizer发送的电子邮件中。</p>
<ul>
<li>每个用户档案每年最多可以发送6条包含PDF附件的消息。</li>
<li>每个附件允许的最大文件大小为5 MB。</li>
<li>对于任何其他大小或卷，您可以购买附件包附加组件。 有关更多详细信息，请联系您的Adobe代表。</li>
</ul>
<p>此功能为限量发布版。请联系 Adobe 代表以获取访问权限。</p>
<p><!--img src="assets/do-not-localize/FILE.gif"/>--></p>
<p><!--For more information, refer to the <a href="../FILE.md">detailed documentation</a>--></p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>登陆页面自定义表单</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>使用[!DNL Journey Optimizer]，您现在可以通过登陆页面捕获配置文件属性。</p>
<p>根据特定数据集创建、设计和管理根据您的需求定制的自定义表单。 然后，您可以在登陆页面中利用这些表单，将您选择的配置文件属性添加到为每个表单定义的数据集中。</p>
<p>此功能为限量发布版。请联系 Adobe 代表以获取访问权限。</p>
<p><!--This capability is currently in beta version and only available to beta customers. To join the beta program, contact your Adobe representative.--></p>
<p><!--img src="assets/do-not-localize/FILE.gif"/>--></p>
<p><!--For more information, refer to the <a href="../FILE.md">detailed documentation</a>--></p>
</td>
</tr>
</tbody>
</table>

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

### 改进 {#Aug-25-8-improv}

此版本包含的改进如下所述。

* **管理**

   * **渠道配置监视警报** — 您现在可以通过电子邮件或在Journey Optimizer通知中心订阅以接收系统警报，以防缺少<!--a channel configuration failure happens or if -->DNS记录。

* **营销活动**

   * **出站营销活动中的速率控制** — 您现在可以为出站营销活动（电子邮件、短信、推送通知）启用速率控制，从而防止下游系统（如登陆页面或客户关怀平台）过载。

   * **操作营销活动计划** — 营销活动每日、每周和每月计划程序已更新，以提供对定期计划的更详细控制：

      * **每周重复**：您现在可以选择每周或每两周重复一次营销活动，并选择在一周中运行该营销活动的日期。

      * **每月重复**：您现在可以选择每月或每两个月重复一次此营销活动，并选择每月运行一次的日期。

      * **每日、每周或每月计划**：您可以指定定期计划应在特定日期停止，还是应在特定次数的发生后停止。

   * **计划的事务性操作营销活动** — 计划的事务性操作营销活动现在可用于通过电子邮件、短信和推送渠道发送批处理、基于受众的事务性通信。

* **渠道 — 推送**

   * **推送通知过期日期** — 您现在可以为每个推送通知指定过期日期，这样可防止在特定日期后发送时效性较差的消息（如黑色星期五特价促销），从而避免给客户带来不佳的体验。

* **渠道 — 短信**

   * **模糊选择退出** — 启用时，**模糊选择退出**&#x200B;选项将检测与定义的选择退出关键字（如“CANCIL”）非常相似的入站消息，并自动发送确认回复以验证用户的取消订阅意图。 如果用户通过定义的提示进行确认，则取消订阅它们。

     请注意，**Fuzzy Opt-out**&#x200B;仅适用于Sinch和Infobip。

   * **验证SMS连接** — 现在，您可以通过向指定设备发送示例消息，在Adobe Journey Optimizer中轻松测试和验证SMS API凭据。

* **配置**

   * **动态域支持** - Journey Optimizer现在支持在渠道配置级别列出的预定义域的跟踪URL中进行个性化。

   * **一键取消订阅URL支持的自定义属性** — 使用Journey Optimizer，如果您在Adobe之外管理同意，则可以通过在电子邮件配置中定义您自己的一键取消订阅链接来设置外部自定义端点。 当您的收件人单击取消订阅链接时，Journey Optimizer会向同意更新事件附加一些特定于用户档案的默认参数。

     为进一步个性化一键式取消订阅链接，您现在可以定义还将附加到同意事件的自定义属性。

* **决策**

   * **将片段附加到决策项** - Journey Optimizer现在提供将片段附加到决策项的功能，可在基于代码的体验营销活动中通过决策策略利用这些决策项。

* **历程**

   * **历程批量操作** — 您现在可以从历程列表中选择多个项目。 选择后，您一次最多可以暂停或恢复10个历程。

   * 自定义操作中的&#x200B;**重定向(302)支持** — 自定义操作现在可以基于每个请求处理HTTP 302重定向。 这允许历程与将请求重定向到本地化或特定于区域的URL的API集成。 系统会自动执行重定向，以确保提供正确的内容而无需额外配置。

* **数据集**

   * **Experience Decisioning对象存储库 — 个性化优惠项目** — 内置导出数据集现在捕获所有优惠属性和生命周期状态，实现完整的个性化和报告。

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


