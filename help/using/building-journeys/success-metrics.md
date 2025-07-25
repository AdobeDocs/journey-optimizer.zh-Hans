---
solution: Journey Optimizer
product: journey optimizer
title: 发布历程
description: 了解如何报告历程量度
feature: Journeys
topic: Content Management
role: User
level: Intermediate
keywords: 发布，历程，实时，有效性，检查
exl-id: 95d0267e-fab4-4057-8ab5-6f7c9c866b0f
source-git-commit: f26083c222efa71176ce5c78f5f35f2c208240e6
workflow-type: tm+mt
source-wordcount: '530'
ht-degree: 6%

---

# 配置和跟踪历程指标 {#success-metrics}

通过历程量度清楚地了解客户历程的有效性。 利用此功能，您可以根据定义的KPI跟踪性能、揭示对有效内容的洞察以及确定优化区域。 通过实时衡量影响，您可以推动持续改进并做出有数据根据的决策，从而提高客户参与度。

## 先决条件 {#prerequisites}

在使用历程量度之前，您必须在Adobe Experience Platform中的配置>报表下添加包含`Commerce Details`、`Web`和`Mobile` [字段组](https://experienceleague.adobe.com/docs/experience-platform/xdm/tutorials/create-schema-ui.html?lang=zh_Hans#field-group){target="_blank"}的数据集。

这些字段组必须从内置选项中选择，而不是从自定义组中选择。 请参阅[添加数据集](../reports/reporting-configuration.md#add-datasets)部分。

## 可用量度 {#metrics}

量度列表因数据集中包含的[字段组](https://experienceleague.adobe.com/docs/experience-platform/xdm/tutorials/create-schema-ui.html?lang=zh_Hans#field-group){target="_blank"}而异。

如果未配置数据集，则只有以下量度可用： **[!UICONTROL 点击]**、**[!UICONTROL 唯一点击]**、**[!UICONTROL 点进率]**&#x200B;和&#x200B;**[!UICONTROL 打开率]**。

请注意，使用Customer Journey Analytics许可证，您可以创建自定义成功量度。 [了解详情](https://experienceleague.adobe.com/zh-hans/docs/analytics-platform/using/cja-components/cja-calcmetrics/cm-workflow/participation-metric)


| 量度 | 相关字段组 |
|-|-|
| 点击次数 | 不需要字段组 |
| 独特点击 | 不需要字段组 |
| 点进率(CTR) | 不需要字段组 |
| 点进打开率(CTOR) | 不需要字段组 |
| Page Views | Web字段组 |
| 应用程序启动次数 | 移动字段组 |
| 应用程序首次启动次数 | 移动字段组 |
| 应用程序安装次数 | 移动字段组 |
| 应用程序升级 | 移动字段组 |
| 购买次数 | Commerce详细信息字段组 |
| 结账次数 | Commerce详细信息字段组 |
| 购物车添加次数 | Commerce详细信息字段组 |
| 购物车打开次数 | Commerce详细信息字段组 |
| 购物车查看 | Commerce详细信息字段组 |
| 购物车减货次数 | Commerce详细信息字段组 |
| 产品查看次数 | Commerce详细信息字段组 |
| 保存以供日后使用次数 | Commerce详细信息字段组 |

## 归因 {#attribution}

每个量度都带有一组归因，该归因确定哪些接触点或交互对特定结果做出了贡献。

* 具有Journey Optimizer许可证的&#x200B;**量度归因**：

  仅使用Journey Optimizer许可证，任何选定指标的最大可用回溯时段均设置为7天。 对于这些量度，归因模型默认设置为&#x200B;**最近联系**，即转化前的最近交互。

  例如，您可以跟踪客户在过去7天内与您的历程交互后是否进行了购买。

* 具有Customer Journey Analytics许可证的&#x200B;**量度归因**：

  借助Journey Optimizer和Customer Journey Analytics许可证，您可以创建具有特定归因设置的自定义量度，或更改内置量度的归因。

  了解有关[归因模型](https://experienceleague.adobe.com/zh-hans/docs/analytics-platform/using/cja-dataviews/component-settings/attribution#attribution-models)的更多信息

## 分配您的历程量度 {#assign}

>[!IMPORTANT]
>
>每个历程只允许一个历程量度。

要开始跟踪历程量度，请执行以下步骤：

1. 从您的&#x200B;**[!UICONTROL 历程]**&#x200B;菜单中，单击&#x200B;**[!UICONTROL 创建历程]**。

1. 编辑历程的配置窗格以定义历程的名称并设置其属性。 了解如何在[此页面](../building-journeys/journey-properties.md)上设置历程的属性。

1. 选择您的&#x200B;**[!UICONTROL 历程指标]**，用于衡量历程的有效性。

   请注意，这些量度适用于历程本身，并适用于历程的所有元素。

   ![](assets/success_metric.png)

1. 单击&#x200B;**[!UICONTROL 保存]**。

1. 使用必要的&#x200B;**[!UICONTROL 活动]**&#x200B;设计您的历程。

1. 测试并发布您的历程。

1. 打开您的历程报告，以跟踪您分配的成功量度的性能。

   您选择的指标将显示在报表的KPI和历程统计信息表中。

   ![](assets/success_metric_2.png)

