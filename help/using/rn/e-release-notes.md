---
solution: Journey Optimizer
product: journey optimizer
title: Journey Optimizer 的预发行说明
description: Adobe Journey Optimizer 预发行说明
feature: Release Notes
hide: true
hidefromtoc: true
exl-id: 6e7d1300-8efd-4fdc-90e3-3ccdc3babd2f
source-git-commit: 7f9828c1781468155702d9f8fd475736a7656188
workflow-type: tm+mt
source-wordcount: '1046'
ht-degree: 47%

---

# 预发行说明 {#e-release-notes}

[!DNL Adobe Journey Optimizer] 不断地提供新功能、对现有功能进行增强和修复错误。所有更改会在每月末整合到[发行说明](release-notes.md)中。


## 2025年8月预发行说明 {#25-8-rn}

**在发行日期**&#x200B;之前，下面的预发行说明可能会有所更改，恕不另行通知。 链接、屏幕和更新文档在发布日期的发行说明中发布。

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

<table>
<thead>
<tr>
<th><strong>电子邮件设计器中的深色模式</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Journey Optimizer 电子邮件设计器现在提供切换到深色模式视图的功能，您可以在其中定义额外的特定自定义设置，这些设置将仅显示给在深色模式下阅读电子邮件的收件人。</p>
<p>请注意以下事项：</p>
<ul>
<li>深色模式的最终呈现可能会有所不同，具体取决于收件人的电子邮件客户端。</li>
<li>并非所有电子邮件客户端都支持自定义深色模式。此外，某些电子邮件客户端只对收到的所有电子邮件应用自己的默认深色模式。在这两种情况下，无法呈现您在电子邮件设计器中定义的自定义设置。</li>
</ul>
<P>此功能目前为 Beta 版，仅供 Beta 版客户使用。要加入 Beta 版计划，请联系 Adobe 代表。</p>
<p><!--img src="assets/do-not-localize/dark-mode.gif"/>--></p>
<p><!--For more information, refer to the <a href="../email/dark-mode.md">detailed documentation</a>--></p>
</td>
</tr>
</tbody>
</table>

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
<li>支持入站渠道，</li>
<li>“datasetLookup”帮助程序函数现在可用于表达式和可视化片段中，以使用来自Adobe Experience Platform数据集的数据对内容进行个性化设置，</li>
<li>现在，通过数据集中的一个选项，您可以启用数据集以进行查找个性化，而无需执行API调用。</li>
</ul>
<p><!--img src="assets/do-not-localize/FILE.gif"/>--></p>
<p><!--For more information, refer to the <a href="../FILE.md">detailed documentation</a>--></p>
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
<p>此功能之前为限量发布版，现在可供在所有环境中使用（正式发布）。</p>
<p><!--img src="assets/do-not-localize/FILE.gif"/>--></p>
<p><!--For more information, refer to the <a href="../FILE.md">detailed documentation</a>--></p>
</td>
</tr>
</tbody>
</table>

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
<p>Journey Optimizer支持新的通用操作活动，通过该活动可配置单操作和多渠道出站操作，从而简化历程画布中的操作配置。 利用此新活动，您还可以将定位优化、实验和多语言变体添加到任何内置渠道操作中。</p>
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
<p>Journey Optimizer现在允许您创建自定义表单，并在登陆页面中利用这些表单，将配置文件属性捕获到为每个表单定义的数据集中。</p>
<p>此功能目前为 Beta 版，仅供 Beta 版客户使用。要加入 Beta 版计划，请联系 Adobe 代表。</p>
<p><!--img src="assets/do-not-localize/FILE.gif"/>--></p>
<p><!--For more information, refer to the <a href="../FILE.md">detailed documentation</a>--></p>
</td>
</tr>
</tbody>
</table>


### 改进 {#Aug-25-8-improv}

此版本包含的改进如下所述。

- **管理**
   - **通道配置监视警报** — 现在，您可以订阅接收系统警报，通过电子邮件或Journey Optimizer通知中心接收系统警报，以防发生通道配置失败或缺少DNS记录。

- **营销活动**
   - **出站营销活动中的速率控制** — 您现在可以为出站营销活动（电子邮件、短信、推送通知）启用限制速率控制，从而防止下游系统（如登陆页面或客户关怀平台）发生过载。
   - **操作营销活动计划** — 已更新营销活动每日、每周和每月计划程序，以提高粒度。 例如，您现在可以设置计划之间的周数/月数，定义执行的日期，并决定在特定发生次数后或特定日期停止。

- **渠道 — 推送**
   - **推送通知过期日期** — 您现在可以为每个推送通知指定过期日期，这样可防止在特定日期后发送时效性较差的消息（如黑色星期五特价促销），从而避免给客户带来不佳的体验。

- **渠道 — 电子邮件**
   - **电子邮件的PDF附件** — 您现在可以将静态PDF文件附加到使用Journey Optimizer发送的电子邮件。

- **配置**
   - **动态域支持** - Journey Optimizer现在支持在渠道配置级别列出的预定义域的跟踪URL中进行个性化。
   - **一键取消订阅URL支持的自定义属性** — 使用Journey Optimizer，如果您在Adobe之外管理同意，则可以通过在电子邮件配置中定义您自己的一键取消订阅链接来设置外部自定义端点。 当您的收件人单击取消订阅链接时，Journey Optimizer会向同意更新事件附加一些特定于用户档案的默认参数。

     为进一步个性化一键式取消订阅链接，您现在可以定义将附加到同意事件的自定义属性。

- **历程**
   - **历程批量操作** — 您现在可以从历程列表中选择多个项目。 选择后，您一次最多可以暂停或恢复10个历程。

