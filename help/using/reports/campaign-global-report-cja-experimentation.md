---
solution: Journey Optimizer
product: journey optimizer
title: 营销活动报告
description: 了解如何使用活动报告中的试验数据
feature: Reporting
topic: Content Management
role: User
level: Intermediate
exl-id: 69742163-7378-49ab-929e-86213d6e65e3
TQID: https://experienceleague.adobe.com/m11Vxa3bSvaOHe1kFs5tU9oQS08lzcL0DSPyrABbXBI
product_v2: id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2: id: a9f73820-6899-47c2-a597-3fec28ab756aid: b49ca41f-eb7a-4f4b-abeb-a97c06fd0c04
subfeature_v2: id: d145add9-d5b9-481b-aa8a-e15e6bb7f813id: a7289281-9ae4-47b1-b8cf-4028b98af776id: b5afe8bf-bda6-41b5-ba06-922638872d63
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554
level_v2: id: b5a62a22-46f7-4f0d-b151-3fc640bef588
topic_v2: id: aa2f3246-cb95-4b30-8899-fdf7d73550ccid: bcc5edb5-84c3-4940-9f84-ed88b6c16274id: e1e0219c-f879-479f-8427-888ed2a6e9c2
source-git-commit: 7f28f19b11ead867b0851943fdd997dcc3af170b
workflow-type: tm+mt
source-wordcount: 356
ht-degree: 9%

---

# 实验营销活动报告 {#campaign-global-report-cja-experimentation}

>[!BEGINSHADEBOX]

**在此页面上：**&#x200B;了解如何在Adobe Journey Optimizer中阅读试验性营销活动报告，以便使用提升度、置信度和转化率等指标比较变体性能。

>[!ENDSHADEBOX]

>[!CONTEXTUALHELP]
>id="ajo_campaigns_content_experiment_click"
>title="成功量度"
>abstract="您之前在创建试验时选择的成功量度的总值，除以轮廓数。"

## 试验 {#experimentation}

**[!UICONTROL 试验]**&#x200B;选项卡提供了有关每个变体性能的关键见解，并标识了最成功的变体。

请注意，定义最佳业绩者可能需要一些时间。 如果试验不成功，它将设置为&#x200B;**无结论**。

![](assets/cja-experimentation-1.png)

### 试验KPI {#experimentation-kpis}

![](assets/cja-experimentation-kpis.png)

**[!UICONTROL 试验]**&#x200B;关键绩效指标(KPI)作为功能全面的功能板，提供与试验关联的基本量度分析。

+++ 了解有关试验KPI量度的更多信息

* **[!UICONTROL 提升]**：测量给定处理的转化率相对于基线的提升百分比。

* **[!UICONTROL 置信度]**：表明给定处理与基线处理相同的证据。 [了解详情](../content-management/experiment-calculations.md#adobes-statistical-methodology-any-time-valid-confidence-sequences)

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

* **[!UICONTROL 置信度]**：表明给定处理与基线处理相同的证据。 [了解详情](../content-management/experiment-calculations.md#adobes-statistical-methodology-any-time-valid-confidence-sequences)

* **[!UICONTROL 置信上限]**：在所选置信区间内，处理和基线之间转换率差异的最大估计值。

+++

### 成功量度的转化率 {#conversion-rate}

![](assets/cja-experimentation-conversion.png)


**[!UICONTROL 置信区间]**&#x200B;图形显示可能的改善范围，并将基线与所选成功量度的最佳表现处理进行比较。 [了解详情](../content-management/experiment-calculations.md#adobes-statistical-methodology-any-time-valid-confidence-sequences)。