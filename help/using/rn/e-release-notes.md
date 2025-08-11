---
solution: Journey Optimizer
product: journey optimizer
title: Journey Optimizer 的预发行说明
description: Adobe Journey Optimizer 预发行说明
feature: Release Notes
hide: true
hidefromtoc: true
exl-id: 6e7d1300-8efd-4fdc-90e3-3ccdc3babd2f
source-git-commit: 3a44111345c1627610a6b026d7b19b281c4538d3
workflow-type: ht
source-wordcount: '591'
ht-degree: 100%

---

# 预发行说明 {#e-release-notes}

[!DNL Adobe Journey Optimizer] 不断地提供新功能、对现有功能进行增强和修复错误。所有更改会在每月末整合到[发行说明](release-notes.md)中。

**以下预发行说明可能会在正式发行日期之前有所更改，恕不另行通知**。在发行当日，会在[发行说明](release-notes.md)中发布链接、屏幕和更新文档。


## 2025 年 8 月预发行说明 {#25-7-rn}

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
<img src="assets/do-not-localize/PauseResume.gif">
<p>此功能之前仅面向部分客户提供（限量发布），现在可供在所有环境中使用（正式发布）。</p>
<p>有关更多信息，请参阅<a href="../building-journeys/journey-pause.md">详细文档</a>。</p>
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
<li>对在日期中导航做出的设计改进</li>
<li>如果设置了开始和结束日期，可以查看营销活动草稿</li>
<li>对于长时间运行的日程表项，提供了用于隐藏和显示它们的新设置</li>
</ul>
<img src="assets/do-not-localize/calendar.gif">
<p>有关更多信息，请参阅<a href="../building-journeys/journey-ui.md#journeys-calendar">详细文档</a></p>
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
<p><img src="assets/do-not-localize/dark-mode.gif"/></p>
<p>有关更多信息，请参阅<a href="../email/dark-mode.md">详细文档</a>。 </p>
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
<!--p>For more information, refer to the <a href="../FILE.md">detailed documentation</a></p-->
</td>
</tr>
</tbody>
</table>

### 改进 {#Aug-25-8-improv}

此版本包含的改进如下所述。