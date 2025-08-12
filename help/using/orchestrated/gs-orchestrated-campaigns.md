---
solution: Journey Optimizer
product: journey optimizer
title: 精心编排的营销活动快速入门
description: 了解如何开始使用编排的营销活动
short-description: 了解协调的活动主要功能和用例。
exl-id: 611dd06d-aa18-4fa3-a477-8a910cec21d8
source-git-commit: 4510cfde1579fbabe7deb1289f70f13ee21a3d4a
workflow-type: tm+mt
source-wordcount: '619'
ht-degree: 30%

---


# 精心编排的营销活动快速入门 {#orchestrated-camp}

>[!CONTEXTUALHELP]
>id="campaigns_overview_orchestrated"
>title="营销活动_概述_精心策划"
>abstract="<b>精心策划营销活动</b><br/>拆分、合并、扩充并操作关系型数据集以定义您的受众<br/><br/> <b>利用多实体数据</b><br/>了解精心编排的营销活动如何利用关系数据集来扩充数据，从而进行分段和个性化<br/><br/><b>临时分段和准确计数</b><br/>通过准确计数逐步构建您的区段<br/><br/><b>可用渠道</b><br/>电子邮件、短信、推送通知、直邮"

[!DNL Adobe Journey Optimizer]中的营销活动编排可跨渠道支持由品牌发起的复杂营销活动，从而帮助您大规模提高参与度、收入和客户忠诚度。

>[!IMPORTANT]
>
>要访问Campaign Orchestration，您的许可证必须包括&#x200B;**Journey Optimizer — 营销活动和历程**&#x200B;或&#x200B;**Journey Optimizer — 营销活动**&#x200B;包。 请联系您的Adobe代表以确认您的许可证并在需要时进行更新。

跨渠道营销至关重要，而精心设计的营销活动可以让这项工作变得流畅一体。借助可视化的拖放界面，您可以设计和自动化跨多个渠道的复杂营销工作流程，从分段到消息投放。您可以在直观的环境中进行一切操作，从而提升速度、控制力和效率。

![](assets/canvas-example-diagram.png){zoomable="yes"}

## 核心功能

Campaign Orchestration围绕四个关键支柱构建：

<table style="table-layout:auto">
<tr style="border: 0;">
<td><img alt="按需受众" src="assets/do-not-localize/icon-audience.svg" width="150px"></a></td><td><b>按需受众</b><br/>即时跨数据集查询以使用数据类型和维度的任意组合创建受众区段。</td></tr>
<tr style="border: 0;">
<td><img alt="多实体分段和发送" src="assets/do-not-localize/icon-entity.svg" width="150px"></a></td><td><b>多实体分段和发送</b><br/>超越基于人员的营销活动 — 使用产品目录、商店位置或服务数据等实体来精确定位。<br/><br/>
支持多级发送，其中每个用户档案和关联的辅助实体发送一条消息。 这些次要实体可包括联系地址、预订、订阅、合同或其他链接数据。 例如，这允许将营销活动发送到用户档案的所有已知地址或与该用户档案关联的每个预订。</td></tr>
<tr style="border: 0;">
<td><img alt="预发送可见性和精确性" src="assets/do-not-localize/icon-visibility.svg" width="150px"></a></td><td><b>发送前可见性和精确度</b><br/>在启动前获取准确的分段计数和完整的促销活动范围，确保准确性和可信度。</td></tr>
<tr style="border: 0;">
<td><img alt="多步骤活动工作流" src="assets/do-not-localize/icon-multistep.svg" width="150px"></a></td><td><b>多步骤营销活动工作流</b><br/>设计多步骤营销活动，从每日消息到复杂的营销活动，如季节性促销活动或主要产品发布。</td></tr>
</table>

## 编排的营销活动和历程

尽管编排的营销活动可视化图表与历程具有相似之处，但它解决了不同的目的和用例：

* **历程** - 1到1个画布，每个个人资料将按照自己的速度在各个步骤中传递。 每个客户的状态都保留在其上下文中，以触发实时操作。

* **协调的营销活动** — 与历程不同，协调的营销活动使用计算区段的批次画布运行。 所有配置文件都会同时处理。

这两个画布均针对其各自的用例进行了优化：历程画布发布了其生命周期往往更长的历程，而Campaign画布专为批营销活动的迭代和增量运行而设计。

## 精心策划的营销活动包含哪些内容？ {#gs-ms-campaign-inside}

精心策划的竞选活动画布代表了将要发生的事情。 它描述要执行的各种任务及其如何关联在一起。

![图像显示编排的活动画布](assets/canvas-example.png)

每个编排的活动都包含：

* **活动**：活动是要执行的任务。在图上用图标表示各种活动。每个活动都有特定属性和所有活动共有的其他属性。

  在编排的活动图中，给定活动可以生成多个任务，尤其是存在循环或重复操作时。

* **过渡**：过渡将源活动链接到目标活动并定义它们的顺序。

* **工作表**：工作表包含了过渡所携带的所有信息。每个编排的活动都使用几个工作表。 这些表中传送的数据可在整个编排营销活动的生命周期中使用。

## 让我们深入探究

现在，您已了解哪些是精心策划的营销活动，接下来该深入挖掘这些文档部分，以开始使用此功能。

<table><tr style="border: 0; text-align: center;">
<td>
<a href="gs-campaign-creation.md">
<img alt="访问和管理活动" src="assets/do-not-localize/workflow-access.jpeg">
</a>
<div>
<a href="gs-campaign-creation.md"><strong>配置步骤</strong></a>
</div>
<p>
</td>
<td>
<a href="create-orchestrated-campaign.md">
<img alt="潜在客户" src="assets/do-not-localize/workflow-create.jpeg">
</a>
<div><a href="create-orchestrated-campaign.md"><strong>创建编排的营销活动</strong>
</div>
<p>
</td>
<td>
<a href="activities/about-activities.md">
<img alt="不频繁" src="assets/do-not-localize/workflow-activities.jpeg">
</a>
<div>
<a href="activities/about-activities.md"><strong>使用活动</strong></a>
</div>
<p></td>
</tr></table>
