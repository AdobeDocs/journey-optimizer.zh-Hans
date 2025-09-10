---
solution: Journey Optimizer
product: journey optimizer
title: 营销活动报告
description: 了解如何使用历程报表中的试验数据
feature: Reporting
topic: Content Management
role: User
level: Intermediate
source-git-commit: 158d9d9a1070e1d842183e5bd6cb5ce8e38834c5
workflow-type: tm+mt
source-wordcount: '386'
ht-degree: 2%

---

# 试验历程报告 {#campaign-global-report-cja-experimentation}

您的历程报表可以让您全面了解试验的执行情况，以及了解其影响所需的关键指标。

在Journey Optimizer中，旅程试验分为两种类型：

* [内容试验](../content-management/content-experiment.md)
* [路径实验](../building-journeys/optimize.md)

## 路径试验 {#experimentation}

>[!NOTE]
>
> 内容试验的详细表和KPI与路径试验的详细表和KPI相同。 如果您已设置内容试验，请参阅下面的文档。

### 试验KPI {#experimentation-kpis}

![](assets/journey-report-experiment-1.png)

**试验摘要**&#x200B;提供了有关试验性能的关键见解，并确定了最成功的见解。 请注意，定义最佳业绩者可能需要一些时间。 如果试验不成功，它将设置为&#x200B;**无结论**。

**试验关键绩效指标(KPI)**&#x200B;用作一个包含所有内容的仪表板，提供与您的试验关联的基本量度的分析。

+++ 了解有关试验KPI量度的更多信息

* **[!UICONTROL 提升]**：测量给定处理的转化率相对于基线的提升百分比。

* **[!UICONTROL 置信度]**：表明给定处理与基线处理相同的证据。 [了解详情](../content-management/experiment-calculations.md#understand-confidence)

+++



### 按成功量度显示的变量 {#variant-inbound}

![](assets/cja-experimentation-variants.png)

根据成功量度&#x200B;**列出的**变量表根据设置试验时选择的成功量度显示每个变量的执行情况。
有关这些结果的深入了解及其解释方法，请参阅[此页面](../content-management/get-started-experiment.md#interpret-results)。

+++ 详细了解“按成功列出的变量”量度

* **[!UICONTROL 人员]**：符合消息目标用户档案资格的用户档案数。

* **[!UICONTROL 入站点击数]**：创建实验时先前选择的成功量度的总值。

* **[!UICONTROL 转化率]**：之前在创建试验时选择的成功量度的总值除以配置文件数。

* **[!UICONTROL 提升]**：测量给定处理的转化率相对于基线的提升百分比。

* **[!UICONTROL 置信下限]**：在所选置信区间内，处理和基线之间转化率差异的最低估计值。

* **[!UICONTROL 置信度]**：表明给定处理与基线处理相同的证据。 [了解详情](../content-management/experiment-calculations.md#understand-confidence)

* **[!UICONTROL 置信上限]**：在所选置信区间内，处理和基线之间转换率差异的最大估计值。

+++

### 成功量度的转化率 {#conversion-rate}

![](assets/cja-experimentation-conversion.png)

**[!UICONTROL 置信区间]**&#x200B;图形显示可能的改善范围，并将基线与所选成功量度的最佳表现处理进行比较。 [了解详情](../content-management/experiment-calculations.md#confidence-intervals)。
