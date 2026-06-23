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
version: Journey Orchestration
TQID: https://experienceleague.adobe.com/iHr0CFVSDz-4tOxNKyCyPZdwva3nfDyuU0Y5XHZEdjk
product_v2:
  - id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2:
  - id: b3538224-471e-4c63-a444-9b19d89ae29c
  - id: d998adac-2f81-400b-a669-d07bb196e4eb
subfeature_v2:
  - id: fa683eda-48de-4558-af32-2673edcd44fe
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
topic_v2:
  - id: aa2f3246-cb95-4b30-8899-fdf7d73550cc
  - id: b5520579-b31f-4df7-9281-f0d9f91e2edc
  - id: cdd65e7e-8839-44a2-bc21-0e03623b5dd1
  - id: d00e9f03-e50b-4162-b143-0c0817c937c2
  - id: e1e0219c-f879-479f-8427-888ed2a6e9c2
source-git-commit: bf5866b0e7437f93936f573fd83ada8526fe004d
workflow-type: tm+mt
source-wordcount: 1153
ht-degree: 3%

---

# 配置和跟踪历程指标 {#success-metrics}

>[!BEGINSHADEBOX]

**在此页面上：**&#x200B;了解如何配置和分配历程量度，以根据KPI跟踪性能并实时衡量客户历程的有效性。

>[!ENDSHADEBOX]

通过历程量度清楚地了解客户历程的有效性。 利用此功能，您可以根据定义的KPI跟踪性能、揭示对有效内容的洞察以及确定优化区域。 通过实时衡量影响，您可以推动持续改进并做出有数据根据的决策，从而提高客户参与度。

## 先决条件 {#prerequisites}

在使用历程量度之前，您必须在[!DNL Adobe Experience Platform]中的配置>报表下添加包含`Commerce Details`、`Web`和`Mobile` [字段组](https://experienceleague.adobe.com/docs/experience-platform/xdm/tutorials/create-schema-ui.html?lang=zh_Hans#field-group){target="_blank"}的数据集。

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
| 购买 | Commerce详细信息字段组 |
| 结账次数 | Commerce详细信息字段组 |
| 购物车添加次数 | Commerce详细信息字段组 |
| 购物车打开次数 | Commerce详细信息字段组 |
| 购物车查看 | Commerce详细信息字段组 |
| 购物车减货次数 | Commerce详细信息字段组 |
| 产品查看次数 | Commerce详细信息字段组 |
| 保存留待后用 | Commerce详细信息字段组 |

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

   历程属性中的![成功量度配置面板](assets/success_metric.png)

1. 单击&#x200B;**[!UICONTROL 保存]**。

1. 使用必要的&#x200B;**[!UICONTROL 活动]**&#x200B;设计您的历程。

1. 测试并发布您的历程。

1. 打开您的历程报告，以跟踪您分配的成功量度的性能。

   您选择的指标将显示在报表的KPI和历程统计信息表中。

   ![成功量度下拉列表显示目标跟踪的可用事件](assets/success_metric_2.png)

+++ AI知识参考

本节包含结构化知识，用于支持与本主题相关的解释、检索和问答。

要全面了解相关信息，应将此信息与本页上的文档相结合。 这两个源都不是独立的；页面描述了功能，而本节提供了其他上下文来帮助消除术语、意图、适用性和约束条件的歧义。

* **TL；DR：**&#x200B;本页介绍如何通过将KPI分配给历程并在历程报表中查看其性能，在Adobe Journey Optimizer中配置和跟踪历程成功量度。

**意图：**
* 添加所需的AEP数据集字段组（Commerce详细信息、Web、移动设备）作为历程量度的先决条件
* 在历程创建或配置期间向历程分配历程量度(KPI)
* 根据配置的数据集字段组，了解哪些量度可用
* 解释Journey Optimizer和Customer Journey Analytics许可证下历程量度的归因模型
* 使用Customer Journey Analytics许可证创建自定义成功量度
* 根据历程报表中分配的KPI跟踪历程表现

**术语表：**
* **历程量度**：分配给历程以衡量其效果的KPI，在历程报告&#x200B;*（产品特定）中可见*
* **最近联系归因**：将转化前最近交互归因的默认归因模型
* **Commerce详细信息字段组**： XDM字段组正在启用与商业相关的量度，例如购买、结账和购物车事件
* **回顾时间范围**：评估归因的时间范围；仅使用Journey Optimizer许可证时，最多可设置7天

**护栏：**
* 每个历程只允许一个历程量度
* 必须从内置选项而不是自定义组中选择数据集字段组（Commerce详细信息、Web、移动设备），并在Adobe Experience Platform中的配置>报表下添加
* 如果没有配置的数据集，则只有点击次数、唯一点击次数、点进率和打开率可用
* 仅使用Journey Optimizer许可证的最长回看窗口为7天
* 自定义量度和自定义归因设置需要Customer Journey Analytics许可证

**术语：**
* 规范名称：历程量度 — 缩写：none — 变体：成功量度、历程成功量度
* 规范名称：点进率 — 缩写：CTR — 变体：无
* 规范名称：点进打开率 — 缩写：CTOR — 变体：无
* 同义词：“历程量度”=“成功量度”（在UI和文档中可互换使用）
* 请勿混淆：“Journey Optimizer许可证归因”≠“Customer Journey Analytics归因” — CJA许可证支持自定义归因模型和更长的回顾窗口

**常见问题解答：**
* **问：我可以为单个历程分配多少历程量度？**  — 每个历程只允许一个历程量度。
* **问：如果我没有配置包含字段组的数据集，有哪些量度可用？**  — 只有点击次数、唯一点击次数、点进率和打开率可用，而无需额外的字段组配置。
* **问：启用购买和商务量度需要哪些字段组？**  — 您需要将Commerce详细信息字段组添加到Adobe Experience Platform中的报表数据集。
* **问：历程量度的默认归因模型是什么？**  — 最近联系，用于记录转化前的最新交互，根据Journey Optimizer许可，回顾时间范围最长为7天。
* **问：能否创建自定义成功量度？**  — 是，但必须具有Customer Journey Analytics许可证。
* **问：发布后可在何处查看历程量度结果？**  — 在历程报告的KPI和历程统计信息表中。

+++
