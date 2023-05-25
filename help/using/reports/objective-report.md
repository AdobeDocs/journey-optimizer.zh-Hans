---
solution: Journey Optimizer
product: journey optimizer
title: 营销活动全局报告
description: 了解如何使用Campaign全局报告中的数据
feature: Reporting
topic: Content Management
role: User
level: Intermediate
hide: true
hidefromtoc: true
source-git-commit: 6b8983d3f3fa989bd7190fc6a8b51fa8989b2293
workflow-type: tm+mt
source-wordcount: '479'
ht-degree: 3%

---

# 营销活动全局报告 {#objective-report}

Campaign全局报告可通过以下方式直接从您的Campaign访问： **[!UICONTROL 查看报告]** 按钮。

营销活动 **[!UICONTROL 全局报告]** 将被划分为多个构件，这些构件详细描述营销活动的成功和错误。 如果需要，可以调整每个小部件的大小并将其删除。 有关此内容的更多信息，请参阅此 [部分](../reports/global-report.md#modify-dashboard).

有关Adobe Journey Optimizer中可用的每个量度的详细列表，请参阅 [此页面](global-report.md#list-of-components-global.md)

## “营销活动”选项卡 {#campaign-global-objectives}

### 交付 {#delivery-global-objectives}

![](assets/campaign_report_global_1.png)

此 **[!UICONTROL 营销活动的统计数据]** 构件详细列出了与您的营销活动相关的主要信息：

* **[!UICONTROL 输入的配置文件]**：启动历程的用户档案数。

* **[!UICONTROL 已交付操作]**：历程中交付操作的唯一总次数。

* **[!UICONTROL 操作失败百分比]**：与已交付操作的独特次数总数相比，历程中操作的独特失败总次数。

### 目标报表 {#objective-global}

>[!AVAILABILITY]
>
>此 **目标报表** 功能目前仅适用于一组组织（限量发布）。 有关更多信息，请与您的 Adobe 代表联系。

![](assets/performance_report.gif)

此 **[!UICONTROL 目标]** 选项卡允许您通过定位一个特定量度来更好地优化投放的报告。

此 **[!UICONTROL 目标]** 列表已链接到 **[!UICONTROL 数据集]** 来定义与系统的连接以检索附加信息。 内置列表 **[!UICONTROL 目标]** 可用，但您可以通过添加新的来添加您自己的 **[!UICONTROL 数据集]**. 有关详细过程，请参阅此 [部分](../campaigns/reporting-configuration.md).

选择完要定位的目标后，两项 **[!UICONTROL 性能概述]** 和 **[!UICONTROL 营销活动目标]** 构件将提供投放性能的详细摘要。

使用 **[!UICONTROL 营销活动目标]** 构件，您还可以选择将您的主要目标与其他指标进行比较。

### 试验报告 {#experimentation-global-objectives}

![](assets/experimentation_report_3.png)

此 **[!UICONTROL 试验]** 选项卡提供了有关每个变体的性能的关键分析，并标识了最成功的变体。

请注意，定义最佳业绩者可能需要一些时间，它将由此图标表示 ![](assets/experimentation_report_1.png).

+++了解有关试验报表可用的不同量度和小部件的更多信息。

此 **[!UICONTROL 实验结果]** 构件详细说明每个变体的性能。 通过从中选择处理方法之一，可以更改基线 **[!UICONTROL 基线]** 下拉列表。 最佳处理方式将以星形图标表示。

下表显示了以下量度：

* **[!UICONTROL 提升度超过基线]**：衡量给定疗法的转化率相对于基线的提高百分比。

* **[!UICONTROL 置信度]**：表明给定治疗与基线治疗相同的证据。 [了解详情](../campaigns/experiment-calculations.md#understand-confidence)

* **[!UICONTROL 独特出站点击次数]**：跨出站渠道的点击总数。

* **[!UICONTROL 配置文件]**：针对此处理的用户档案数。

* **[!UICONTROL 独特出站点击次数/个人资料]**：成功量度的总值（之前创建实验时选择）除以用户档案数。

此 **[!UICONTROL 置信区间]** 图表衡量改进的不确定性。 它详细说明了基线和最佳业绩处理之间的业绩差异百分比。 [了解详情](../campaigns/experiment-calculations.md#confidence-intervals)。
+++

要深入了解这些结果以及如何解释这些结果，请参阅 [此页面](../campaigns/get-started-experiment.md#interpret-results).

