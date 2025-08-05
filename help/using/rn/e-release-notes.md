---
solution: Journey Optimizer
product: journey optimizer
title: Journey Optimizer的预发行说明
description: Adobe Journey Optimizer预发行说明
feature: Release Notes
hide: true
hidefromtoc: true
exl-id: 6e7d1300-8efd-4fdc-90e3-3ccdc3babd2f
source-git-commit: 3a44111345c1627610a6b026d7b19b281c4538d3
workflow-type: tm+mt
source-wordcount: '591'
ht-degree: 37%

---

# 预发行说明 {#e-release-notes}

[!DNL Adobe Journey Optimizer] 不断地提供新功能、对现有功能进行增强和修复错误。所有更改会在每月末整合到[发行说明](release-notes.md)中。

**在发行日期**&#x200B;之前，下面的预发行说明可能会有所更改，恕不另行通知。 在发行当日，会在[发行说明](release-notes.md)中发布链接、屏幕和更新文档。


## 2025年8月预发行说明 {#25-7-rn}

**在发行日期**&#x200B;之前，下面的预发行说明可能会有所更改，恕不另行通知。 链接、屏幕和更新文档在发布日期发布。

另请参阅[Adobe Experience Platform预发行说明](https://experienceleague.adobe.com/zh-hans/docs/experience-platform/release-notes/pre-release-notes){target="_blank"}。

**发行日期**：2025年8月19日


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
<p>以前，此功能仅面向有限的一组客户（有限可用性），而现在则面向所有环境提供（一般可用性）。</p>
<p>有关更多信息，请参阅<a href="../building-journeys/journey-pause.md">详细文档</a>。</p>
</td>
</tr>
</tbody>
</table>



<table>
<thead>
<tr>
<th><strong>日历视图</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>现在，历程和营销活动列表中提供日程表视图。该视图可让您在相应列表中查看所有历程和营销活动激活情况。</p>
<p>以前此功能在有限可用中可用，但现在此功能可用于所有环境。 在此正式发布版本中，该功能包括：</p>
<ul>
<li>日期中导航的设计改进</li>
<li>在设置了开始和结束日期的情况下查看草稿营销活动的功能</li>
<li>用于隐藏和显示长时间运行的日历项目的新设置</li>
</ul>
<img src="assets/do-not-localize/calendar.gif">
<p>有关详细信息，请参阅<a href="../building-journeys/journey-ui.md#journeys-calendar">详细文档</a></p>
</td>
</tr>
</tbody>
</table>


<table>
<thead>
<tr>
<th><strong>电子邮件Designer中的深色模式</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Journey Optimizer Email Designer现在提供切换到深色模式视图的功能，您还可以在该视图中定义特定的自定义设置，该设置将仅显示在深色模式下读取其电子邮件的收件人。</p>
<p>请注意以下事项：</p>
<ul>
<li>深色模式的最终呈现可能会有所不同，具体取决于收件人的电子邮件客户端。</li>
<li>并非所有电子邮件客户端都支持自定义深色模式。 此外，某些电子邮件客户端只对收到的所有电子邮件应用自己的默认深色模式。 在这两种情况下，无法呈现您在Email Designer中定义的自定义设置。</li>
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
<th><strong>活动中的优化</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Journey Optimizer现在可为您提供一些工具，用于向营销活动的受众提供个性化和优化的内容，让您能够运行内容实验、创建基于规则的定位以及使用两者的高级组合，从而最大限度地提高营销活动的有效性。</p>
<p>通过优化，您可以：</p>
<ul>
<li>测试多个内容变体以确定最有效的消息传送。</li>
<li>根据用户属性和上下文数据提供个性化内容。</li>
<li>将定位和试验与高级活动策略相结合。</li>
<li>筛选出不符合变体条件的用户。</li>
<li>确保后备机制以保持用户参与。</li>
</ul>
<P>活动上线后，将根据定义的标准并根据匹配标准评估用户档案，并随活动中的相应体验或内容一起提供。</p>
<p><img src="assets/do-not-localize/campaign-optimization.gif"/></p>
<!--p>For more information, refer to the <a href="../FILE.md">detailed documentation</a></p-->
</td>
</tr>
</tbody>
</table>

### 改进 {#Aug-25-8-improv}

此版本包含的改进如下所述。