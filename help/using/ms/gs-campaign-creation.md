---
solution: Journey Optimizer
product: journey optimizer
title: 多步营销活动创建的关键原则
description: 了解使用Adobe Journey Optimizer执行多步营销活动的主要原则
hide: true
hidefromtoc: true
exl-id: b04aa15a-71bf-4683-bcbf-f611c189ffe1
source-git-commit: 3ecb1691cc8a1c429d9bd9919b06ddc5a316eff7
workflow-type: tm+mt
source-wordcount: '461'
ht-degree: 24%

---

# 关键原则 {#ms-campaign-creation}

>[!CONTEXTUALHELP]
>id="ajo_targeting_workflow_list"
>title="多步营销活动"
>abstract="在此屏幕中，您可以访问多步骤营销活动的完整列表，检查其当前状态、上次/下次执行日期，并创建新的多步骤营销活动。"

借助Adobe Journey Optimizer，您可以将多步营销活动构建到可视画布中，以设计跨渠道流程，例如分段、营销活动执行、文件处理。

## 多步营销活动包含哪些内容？ {#gs-ms-campaign-inside}

多步骤营销活动画布是所应发生情况的呈现。 它描述要执行的各种任务及其如何链接在一起。

![](assets/workflow-example.png){zoomable="yes"} {zoomable="yes"}

每个多步骤营销活动包含：

* **活动**：活动是要执行的任务。在图上用图标表示各种活动。每个活动都有特定属性和所有活动共有的其他属性。

  在多步骤营销活动图中，给定活动可以生成多个任务，尤其是当存在循环或重复操作时。

* **过渡**：过渡将源活动链接到目标活动并定义它们的顺序。

* **工作表**：工作表包含了过渡所携带的所有信息。每个多步骤活动都使用多个工作表。 这些表中传送的数据可在多步骤营销活动的整个生命周期中使用。

## 创建多步营销活动的关键步骤 {#gs-ms-campaign-steps}

创建多步骤营销活动的关键步骤如下：

![](assets/workflow-creation-process.png){zoomable="yes"}

## 访问多步骤活动

在&#x200B;**[!UICONTROL 营销活动]**&#x200B;菜单中，浏览到“多步”选项卡以访问多步营销活动的完整列表。

列表中的每个多步骤营销活动都显示有关其当前[状态](#status)、上次执行或修改该营销活动的时间，以及下一个计划执行日期和时间的信息。

可以通过单击列表右上角的&#x200B;**[!UICONTROL 为自定义版面配置列]**&#x200B;图标来自定义显示的列。这样，您就可以向列表中添加其他信息，例如每个多步骤营销活动出错的最后一个活动，或应用的定位维度。

此外，还可使用搜索栏和过滤器以便在列表中轻松搜索。例如，您可以筛选多步骤营销活动，以仅显示属于某个营销活动的营销活动，或显示在特定日期范围内处理的营销活动。

要复制或删除多步骤营销活动，请单击省略号按钮，然后选择&#x200B;**[!UICONTROL 复制]**&#x200B;或&#x200B;**[!UICONTROL 删除]**。

>[!NOTE]
>
>当多步营销活动正在进行时，您可以复制它，但无法删除它。

## 状态和生命周期 {#status}

营销活动可以具有多种状态：

* **[!UICONTROL 草稿]**：已创建并保存多步骤营销活动。
* **[!UICONTROL 进行中]**：多步骤营销活动当前正在运行。
* **[!UICONTROL 已完成]**：多步骤营销活动执行已完成。
* **[!UICONTROL 已暂停]**：多步骤营销活动已暂停。
* **[!UICONTROL 错误]**：多步骤营销活动遇到错误。 打开多步骤营销活动并访问日志和任务，以识别错误并加以解决。


## 构建查询

## Personalization准则
