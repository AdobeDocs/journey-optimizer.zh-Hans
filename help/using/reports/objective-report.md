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
exl-id: ec1af88c-7b0a-4eaf-97e1-0d9676268fed
badge: label="Beta 版" type="Informative"
source-git-commit: 59ecb9a5376e697061ddac4cc68f09dee68570c0
workflow-type: tm+mt
source-wordcount: '480'
ht-degree: 4%

---

# 营销活动全局报告 {#objective-report}

使用&#x200B;**[!UICONTROL 查看报告]**&#x200B;按钮，可以直接从营销活动访问营销活动全局报告。

营销活动&#x200B;**[!UICONTROL 全局报告]**&#x200B;被分为多个小部件，其中详细说明了营销活动的成功和错误。 如果需要，可以调整每个小部件的大小并将其删除。 有关此内容的更多信息，请参阅此[部分](../reports/global-report.md#modify-dashboard)。

有关Adobe Journey Optimizer中可用的每个量度的详细列表，请参阅[此页面](global-report.md#list-of-components-global.md)

## “营销活动”选项卡 {#campaign-global-objectives}

### 投放 {#delivery-global-objectives}

![](assets/campaign_report_global_1.png)

**[!UICONTROL 促销活动的统计数据]**&#x200B;小组件详细介绍了与您的促销活动相关的主要信息：

* **[!UICONTROL 输入的配置文件]**：启动历程的配置文件的数量。

* **[!UICONTROL 已交付操作]**：历程中某个操作已交付的不重复总次数。

* **[!UICONTROL 操作在%]**&#x200B;中失败：与操作已交付的独特次数总数相比，历程中操作失败的不重复次数。

### 目标报表 {#objective-global}

>[!AVAILABILITY]
>
>**目标报表**&#x200B;功能当前仅适用于一组组织（限量发布）。 有关更多信息，请与您的 Adobe 代表联系。

![](assets/performance_report.gif)

**[!UICONTROL 目标]**&#x200B;选项卡允许您通过定位一个特定量度来更好地优化投放的报告。

列出的&#x200B;**[!UICONTROL 目标]**&#x200B;链接到&#x200B;**[!UICONTROL 数据集]**，这些数据集定义了到系统的连接，以便检索其他信息。 内置&#x200B;**[!UICONTROL 目标]**&#x200B;的列表可用，但您可以通过添加新的&#x200B;**[!UICONTROL 数据集]**&#x200B;来添加您自己的目标。 有关详细过程，请参阅此[部分](../content-management/reporting-configuration.md)。

选择目标后，两个&#x200B;**[!UICONTROL 性能概述]**&#x200B;和&#x200B;**[!UICONTROL 营销活动目标]**&#x200B;构件将提供传递性能的详细摘要。

使用&#x200B;**[!UICONTROL 促销活动目标]**&#x200B;小组件，您还可以选择将您的主要目标与另一个量度进行比较。

### 试验报告 {#experimentation-global-objectives}

![](assets/experimentation_report_3.png)

**[!UICONTROL 试验]**&#x200B;选项卡提供了有关每个变体性能的关键见解，并标识了最成功的变体。

请注意，定义最佳业绩者可能需要一些时间，它将由此图标![](assets/experimentation_report_1.png)表示。

+++了解有关试验报告中可用的不同量度和小组件的更多信息。

**[!UICONTROL 实验结果]**&#x200B;构件详细说明了每个变体的性能。 您可以更改基线，方法是从&#x200B;**[!UICONTROL 基线]**&#x200B;下拉列表中选择一种处理。 最佳处理方式将以星形图标表示。

下表显示了以下量度：

* **[!UICONTROL 超过基线的提升]**：测量给定处理的转化率超过基线的改进百分比。

* **[!UICONTROL 置信度]**：表明给定处理与基线处理相同的证据。 [了解详情](../content-management/experiment-calculations.md#understand-confidence)

* **[!UICONTROL 独特出站点击次数]**：跨出站渠道的点击总数。

* **[!UICONTROL 配置文件]**：针对此处理的配置文件数。

* **[!UICONTROL 独特出站点击次数/配置文件]**：在创建实验时先前选择的成功量度的总值除以配置文件数。

**[!UICONTROL 置信区间]**&#x200B;图可测量关于改进的不确定性。 它详细说明了基线和最佳业绩处理之间的业绩差异百分比。 [了解详情](../content-management/experiment-calculations.md#confidence-intervals)。
+++

有关这些结果的深入了解及其解释方法，请参阅[此页面](../content-management/get-started-experiment.md#interpret-results)。
