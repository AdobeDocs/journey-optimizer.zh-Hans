---
solution: Journey Optimizer
product: journey optimizer
title: Journey Optimizer 的预发行说明
description: Adobe Journey Optimizer 预发行说明
feature: Release Notes
hide: true
hidefromtoc: true
exl-id: 6e7d1300-8efd-4fdc-90e3-3ccdc3babd2f
source-git-commit: 75c3db704853b8d2d8920ddd0086681d1fb02a93
workflow-type: tm+mt
source-wordcount: '1033'
ht-degree: 86%

---

# 预发行说明 {#e-release-notes}

[!DNL Adobe Journey Optimizer] 不断地提供新功能、对现有功能进行增强和修复错误。所有更改会在每月末整合到[发行说明](release-notes.md)中。


## 2025 年 8 月预发行说明 {#25-8-rn}

**以下预发行说明可能会在正式发行日期之前有所更改，恕不另行通知**。链接、屏幕和更新的文档会于发布日期在发行说明中发布。

另请参阅 [Adobe Experience Platform 预发行说明](https://experienceleague.adobe.com/zh-hans/docs/experience-platform/release-notes/pre-release-notes){target="_blank"}。

**发布日期**：2025 年 8 月 19 日


### 新功能 {#Aug-25-8-features}

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
<li>对在日期中导航做出的设计改进；</li>
<li>如果设置了开始和结束日期，可以查看营销活动草稿；</li>
<li>对于长时间运行的日程表项，提供了用于隐藏和显示它们的新设置。</li>
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
<p>在个性化编辑器中利用 Adobe Experience Platform 中的数据来对内容进行个性化。为此，必须首先通过 API 调用启用查找个性化所需的数据集。完成后，可以使用其数据对您的内容进行个性化并将它们引入到 [!DNL Journey Optimizer] 中。</p>
<p>此功能之前为限量发布，现在可用于所有环境。在此正式发布版中，引入了以下增强功能：</p>
<ul>
<li>支持入站渠道；</li>
<li>“datasetLookup”辅助函数现在可用于表达式和可视化片段中，以使用来自 Adobe Experience Platform 数据集的数据对内容进行个性化设置；</li>
<li>在数据集中提供了一个选项，让您可以启用数据集以实现查找个性化，而无需执行 API 调用。</li>
</ul>
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
<p>Journey Optimizer 现在提供多种工具，帮助您利用 AI 和试验框架来优化历程，同时确保实现顺畅的可用性，以及条件和优化功能之间的差异化。</p>
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
<p>借助 Journey Optimizer，您现在可以创建自定义表单并在登陆页面中加以利用，以便将轮廓属性捕获到为每个表单定义的数据集中。</p>
<p>此功能为限量发布版。请联系 Adobe 代表以获取访问权限。</p>
<p><!--This capability is currently in beta version and only available to beta customers. To join the beta program, contact your Adobe representative.--></p>
<p><!--img src="assets/do-not-localize/FILE.gif"/>--></p>
<p><!--For more information, refer to the <a href="../FILE.md">detailed documentation</a>--></p>
</td>
</tr>
</tbody>
</table>


### 改进 {#Aug-25-8-improv}

此版本包含的改进如下所述。

* **管理**

   * **渠道配置监控警报** - 现在，您可以订阅接收系统警报（通过电子邮件或 Journey Optimizer 通知中心接收），以便在发生渠道配置故障或缺失 DNS 记录时及时获知。

* **营销活动**

   * **出站营销活动中的速率控制** - 您现在可以为出站营销活动（电子邮件、短信、推送通知）启用节流速率控制功能，避免下游系统（如登陆页面或客户关怀平台）过载。

   * **操作营销活动计划** - 已更新营销活动的每日、每周和每月调度程序，以改善计划粒度。例如，您现在可以设置计划间隔的周数/月数，指定执行日期，并设定为在达到特定次数后或在特定日期停止执行。

   * **计划的事务性操作营销活动** - 计划的事务性操作营销活动现支持通过电子邮件、短信和推送渠道批量发送基于受众的事务性通信。

* **渠道 - 推送**

   * **推送通知过期日期** - 您现在可以为每条推送通知指定过期日期，避免时效性信息（如黑色星期五促销）在特定日期过后继续发送，从而避免给客户带来糟糕的体验。

* **渠道 - 电子邮件**

   * **电子邮件 PDF 附件** - 您现在可以在通过 Journey Optimizer 发送的邮件中添加静态 PDF 附件。

* **渠道 - 短信**

   * **模糊退出** - 启用后，**模糊退出**&#x200B;选项可检测与定义的退出关键词（如“CANCIL”）非常相似的入站消息，并自动发送确认回复以验证用户取消订阅的意向。如果用户通过定义的提示进行确认，系统将执行取消订阅操作。

     请注意，**Fuzzy Opt-out**&#x200B;仅适用于Sinch和Infobip。

   * **验证SMS连接** — 现在，您可以通过向指定设备发送示例消息，在Adobe Journey Optimizer中轻松测试和验证SMS API凭据。

* **配置**

   * **动态域支持** - 对于在渠道配置层面列出的预定义域，Journey Optimizer 现支持在跟踪 URL 中进行个性化设置。

   * **自定义属性支持一键取消订阅 URL** - 借助 Journey Optimizer，若您在 Adobe 平台外管理同意，可通过在电子邮件设定中定义一键取消订阅链接来设置外部自定义端点。当您的收件人点击取消订阅链接时，Journey Optimizer 会将一些默认的特定于轮廓的参数附加到同意更新事件。

     为进一步对一键取消订阅链接进行个性化设置，您现在可以定义将会附加到同意事件的自定义属性。

* **决策**

   * **将片段附加到决策项** - Journey Optimizer现在提供将片段附加到决策项的功能，可在基于代码的体验营销活动中通过决策策略利用这些决策项。

* **历程**

   * **历程批量操作** - 您现在可以从历程列表中选择多个项目。选择后，您可一次性暂停或恢复最多 10 个历程。
