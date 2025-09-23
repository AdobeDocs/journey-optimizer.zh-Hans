---
solution: Journey Optimizer
product: journey optimizer
title: 编排的营销活动快速入门
description: 了解如何开始使用精心编排的营销活动
short-description: 了解精心编排的营销活动的主要功能和用例。
exl-id: 611dd06d-aa18-4fa3-a477-8a910cec21d8
version: Campaign Orchestration
source-git-commit: 4d5505cbb46bdff846218bfc3657c6a6e5447af3
workflow-type: tm+mt
source-wordcount: '654'
ht-degree: 98%

---


# 编排的营销活动快速入门 {#orchestrated-camp}

>[!CONTEXTUALHELP]
>id="campaigns_overview_orchestrated"
>title="营销活动_概述_精心策划"
>abstract="<b>精心策划营销活动</b><br/>拆分、合并、扩充并操作关系型数据集以定义您的受众<br/><br/> <b>利用多实体数据</b><br/>了解精心编排的营销活动如何利用关系数据集来扩充数据，从而进行分段和个性化<br/><br/><b>临时分段和准确计数</b><br/>通过准确计数逐步构建您的区段<br/><br/><b>可用渠道</b><br/>电子邮件、短信、推送通知、直邮"

[!DNL Adobe Journey Optimizer] 中的营销活动编排功能旨在为品牌发起的跨渠道复杂营销活动提供支持，从而帮助您大规模提高参与度、收入和客户忠诚度。

>[!IMPORTANT]
>
>要访问营销活动编排，您的许可证必须包括 **Journey Optimizer – 营销活动和历程**&#x200B;或 **Journey Optimizer – 营销活动**&#x200B;包。请联系 Adobe 代表，确认您的许可证并在需要时进行更新。

跨渠道营销至关重要，而精心设计的营销活动可以让这项工作变得流畅一体。借助可视化的拖放界面，您可以设计和自动化跨多个渠道的复杂营销工作流程，从分段到消息投放。您可以在直观的环境中进行一切操作，从而提升速度、控制力和效率。

![](assets/canvas-example-diagram.png){zoomable="yes"}

➡️ [观看视频以了解编排的营销活动](#video-oc)

## 核心功能

营销活动编排围绕四大要点构建：

<table style="table-layout:auto">
<tr style="border: 0;">
<td><img alt="按需受众" src="assets/do-not-localize/icon-audience.svg" width="150px"></a></td><td><b>按需受众</b><br/>即时进行跨数据集查询，以便使用数据类型和维度的任意组合创建受众区段。</td></tr>
<tr style="border: 0;">
<td><img alt="多实体分段和发送" src="assets/do-not-localize/icon-entity.svg" width="150px"></a></td><td><b>多实体分段和发送</b><br/>超越基于人员的营销活动 - 使用产品目录、店铺位置或服务数据等实体来精确选择目标。<br/><br/>
支持多级发送，将向每个轮廓和关联的次级实体发送一条消息。这些次级实体可能包括：联系地址、预订、订阅、合同或其他关联的数据。例如，这允许将营销活动发送到轮廓的所有已知地址或与该轮廓关联的每个预订。</td></tr>
<tr style="border: 0;">
<td><img alt="发送前的可见性和精确性" src="assets/do-not-localize/icon-visibility.svg" width="150px"></a></td><td><b>发送前的可见性和精确性</b><br/>在发布前获取准确的分段计数和完整的营销活动范围，确保准确性和信心。</td></tr>
<tr style="border: 0;">
<td><img alt="多步骤营销活动工作流" src="assets/do-not-localize/icon-multistep.svg" width="150px"></a></td><td><b>多步骤营销活动工作流</b><br/>设计多步骤营销活动，从每日消息到复杂的营销活动，如季节性促销活动或主要产品发布。</td></tr>
</table>


>[!NOTE]
>
>支持的渠道包括：[电子邮件](../email/get-started-email.md)、[短信/彩信/RCS](../sms/get-started-sms.md)、[推送通知](../push/get-started-push.md)。
>
>可用渠道因您的许可模式和附加组件而异。

## 编排的营销活动和历程

尽管编排的营销活动的可视化图表与历程具有相似之处，但它适用于不同的目的和用例：

* **历程** - 1 比 1 画布，每个轮廓可以按照自己的节奏完成各个步骤。每个客户的状态都会被保留在其上下文中，以便触发实时操作。

* **编排的营销活动** - 与历程不同，精心策划的营销活动通过计算区段的批次画布运行。这会同时处理所有轮廓。

针对其各自的用例，这两个画布得到了优化：历程画布用于发布生命周期往往更长的历程，而营销活动画布专为批量营销活动的迭代和增量运行而设计。

## 编排的营销活动包含哪些内容？ {#gs-ms-campaign-inside}

编排的营销活动画布是对预期流程的呈现。它描述要执行的各种任务及其如何关联在一起。

![显示编排的营销活动画布的图像](assets/canvas-example.png)

每个编排的营销活动都包含：

* **活动**：活动是要执行的任务。[各种活动](activities/about-activities.md)在画布上用图标表示。 每个活动都有特定属性和所有活动共有的其他属性。

  在编排的营销活动画布中，一个给定活动可以产生多个任务，特别是当存在循环或定期操作时。

* **过渡**：过渡将源活动链接到目标活动并定义它们的顺序。

* **工作表**：工作表包含了过渡所携带的所有信息。每个编排的营销活动均使用多个工作表。在编排的营销活动的整个生命周期内均可使用在这些表中传递的数据。


## 介绍视频 {#video-oc}

了解编排的营销活动的关键概念和功能。


>[!VIDEO](https://video.tv.adobe.com/v/3471538/?learn=on&enablevpops)


## 让我们深入探究

您现在已经了解什么是编排的营销活动，是时候详细参阅这些文档章节，以便开始使用该功能。

<table><tr style="border: 0; text-align: center;">
<td>
<a href="gs-campaign-creation.md">
<img alt="访问和管理营销活动" src="assets/do-not-localize/workflow-access.jpeg">
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
