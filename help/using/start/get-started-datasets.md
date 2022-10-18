---
solution: Journey Optimizer
product: journey optimizer
title: 数据集入门
description: 了解如何在Adobe Journey Optimizer中使用Adobe Experience Platform数据集
role: User
level: Beginner
exl-id: dcdd3c81-0f00-4259-a8a5-9062a4c40b6f
source-git-commit: 63c52f04da9fd1a5fafc36ffb5079380229f885e
workflow-type: tm+mt
source-wordcount: '820'
ht-degree: 7%

---

# 数据集入门 {#datasets-gs}

摄取到Adobe Experience Platform的所有数据都将作为数据集保留在数据湖中。 数据集是用于数据集合的存储和管理结构，通常是表格，其中包含架构（列）和字段（行）。

## 访问数据集{#access-datasets}

的 **数据集** 工作区 [!DNL Adobe Journey Optimizer] 用户界面允许您浏览数据并创建数据集。

选择 **数据集** 在左侧导航中打开数据集功能板。

![](assets/datasets-home.png)

将数据添加到 [!DNL Adobe Experience Platform] 是构建用户档案的基础。 然后，您便能够在 [!DNL Adobe Journey Optimizer]. 首先定义架构，使用ETL工具准备和标准化您的数据，然后根据您的架构创建数据集。

选择 **浏览** 选项卡，以显示贵组织所有可用数据集的列表。 系统会为每个列出的数据集显示详细信息，包括其名称、数据集所遵循的架构以及最近摄取运行的状态。

默认情况下，只会显示已摄取到的数据集。 如果要查看系统生成的数据集，请启用 **显示系统数据集** 切换。

![](assets/ajo-system-datasets.png)

选择数据集的名称以访问其“数据集”活动屏幕，并查看您选择的数据集的详细信息。 活动选项卡包含一个图表，其中可视化了消息使用率，以及成功批次和失败批次的列表。

以下是可用的不同数据集：

**报告**

* _报表 — 消息反馈事件数据集_:消息投放日志。 有关从Journey Optimizer投放所有消息以用于报告和创建区段的信息。 此数据集中还记录了来自电子邮件ISP关于退回的反馈。
* _报表 — 电子邮件跟踪体验事件数据集_:电子邮件渠道的交互日志，用于报告和创建区段。 存储的信息会告知最终用户在电子邮件中执行的操作（打开数、点击数等）。
* _报表 — 推送跟踪体验事件数据集_:推送渠道的交互日志，用于报告和创建区段。 存储的信息会通知最终用户在推送通知上执行的操作。
* _报表 — 历程步骤事件_:捕获从Journey Optimizer生成的所有历程步骤体验事件，以供报表等服务使用。 对于在Customer Journey Analytics中生成报表以便进行YoY分析，这一点也至关重要。 绑定到历程元数据。
* _报表 — 历程_:包含历程中每个步骤信息的元数据数据集。
* _报表 — 密送_:用于存储密送电子邮件投放日志的反馈事件数据集。 用于报告。

**同意**

* _同意服务数据集_:存储用户档案的同意信息。

**Intelligent Services**

* _发送时间优化得分/参与度得分_:历程AI的输出分数。

## 预览数据集{#preview-datasets}

从数据集活动屏幕中，选择 **预览数据集** 在屏幕的右上角附近，预览此数据集中最新成功的批处理。 当数据集为空时，将停用预览链接。

![](assets/dataset-preview.png)

## 创建数据集{#create-datasets}

要创建新数据集，请首先选择 **创建数据集** 在数据集功能板中。

您可以：

* 从架构创建数据集。 [在此文档中了解更多信息](https://experienceleague.adobe.com/docs/experience-platform/catalog/datasets/user-guide.html?lang=en#schema){target=&quot;_blank&quot;}
* 从CSV文件创建数据集。 [在此文档中了解更多信息](https://experienceleague.adobe.com/docs/experience-platform/ingestion/tutorials/map-a-csv-file.html?lang=zh-Hans){target=&quot;_blank&quot;}

请观看此视频，了解如何创建数据集、将其映射到架构、向其添加数据，以及确认已摄取数据。

>[!VIDEO](https://video.tv.adobe.com/v/334293?quality=12)

## 数据管理

在数据集中，浏览 **数据管理** 选项卡来检查数据集和字段级别的标签。 “数据管理”根据适用的策略类型对数据进行分类。

的核心功能之一 [!DNL Adobe Experience Platform] 是将多个企业系统中的数据整合在一起，以便营销人员能够更好地识别、了解和吸引客户。 此数据可能受贵组织或法律法规定义的使用限制的约束。 因此，务必确保您的数据操作符合数据使用策略。

[!DNL Adobe Experience Platform Data Governance] 允许您管理客户数据，并确保符合适用于数据使用的法规、限制和策略。 它在Experience Platform的各个级别中发挥着关键作用，包括编目、数据谱系、数据使用标签、数据使用策略以及控制营销操作数据的使用。

在 [数据管理文档](https://experienceleague.adobe.com/docs/experience-platform/data-governance/labels/user-guide.html){target=&quot;_blank&quot;}

## 示例和用例{#uc-datasets}

了解如何在Adobe Journey Optimizer中创建架构、数据集和摄取数据，以在 [此端到端示例](../segment/creating-test-profiles.md)

了解有关在中创建数据集的更多信息 [Adobe Experience Platform文档](https://experienceleague.adobe.com/docs/experience-platform/catalog/datasets/overview.html?lang=zh_Hans){target=&quot;_blank&quot;}。

了解如何在 [数据摄取概述文档](https://experienceleague.adobe.com/docs/experience-platform/ingestion/home.html?lang=zh-Hans){target=&quot;_blank&quot;}。

提供了包含查询示例的用例列表 [此处](../start/datasets-query-examples.md).

**另请参阅**

* [流摄取概述](https://experienceleague.adobe.com/docs/experience-platform/ingestion/streaming/overview.html?lang=zh-Hans){target=&quot;_blank&quot;}
* [将数据摄取到Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/ingestion/tutorials/ingest-batch-data.html){target=&quot;_blank&quot;}
