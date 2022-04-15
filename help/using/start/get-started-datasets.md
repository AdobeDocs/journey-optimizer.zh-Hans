---
title: 数据集入门
description: 了解如何在Adobe Journey Optimizer中使用Adobe Experience Platform数据集
role: User
level: Beginner
exl-id: dcdd3c81-0f00-4259-a8a5-9062a4c40b6f
source-git-commit: 9ebcfd6c41c17fe3be0423822209443fc55244a7
workflow-type: tm+mt
source-wordcount: '430'
ht-degree: 11%

---

# 数据集入门 {#datasets-gs}

摄取到Adobe Experience Platform的所有数据都将作为数据集保留在数据湖中。 数据集是用于数据集合的存储和管理结构，通常是表格，其中包含架构（列）和字段（行）。

## 访问数据集{#access-datasets}

的 **数据集** 工作区 [!DNL Adobe Journey Optimizer] 用户界面允许您浏览数据并创建数据集。

选择 **数据集** 在左侧导航中打开数据集功能板。

![](assets/datasets-home.png)

将数据添加到Adobe Experience Platform是构建用户档案的基础。 然后，您便能够在 [!DNL Adobe Journey Optimizer]. 首先定义架构，使用ETL工具准备和标准化您的数据，然后根据您的架构创建数据集。

选择 **浏览** 选项卡，以显示贵组织所有可用数据集的列表。 系统会为每个列出的数据集显示详细信息，包括其名称、数据集所遵循的架构以及最近摄取运行的状态。

默认情况下，只会显示已摄取到的数据集。 如果要查看系统生成的数据集，请启用 **显示系统数据集** 切换。

![](assets/ajo-system-datasets.png)

选择数据集的名称以访问其“数据集”活动屏幕，并查看您选择的数据集的详细信息。 活动选项卡包含一个图表，其中可视化了消息使用率，以及成功批次和失败批次的列表。

## 创建数据集{#create-datasets}

要创建新数据集，请首先选择 **创建数据集** 在数据集功能板中。

您可以：

* 从架构创建数据集。 [在此文档中了解更多信息](https://experienceleague.adobe.com/docs/experience-platform/catalog/datasets/user-guide.html?lang=en#schema){target=&quot;_blank&quot;}
* 从CSV文件创建数据集。 [在此文档中了解更多信息](https://experienceleague.adobe.com/docs/experience-platform/ingestion/tutorials/map-a-csv-file.html?lang=zh-Hans){target=&quot;_blank&quot;}


请观看此视频，了解如何创建数据集、将其映射到架构、向其添加数据，以及确认已摄取数据。

>[!VIDEO](https://video.tv.adobe.com/v/334293?quality=12)


了解如何在Adobe Journey Optimizer中创建架构、数据集和摄取数据，以在 [此端到端示例](../segment/creating-test-profiles.md)

了解有关在中创建数据集的更多信息 [Adobe Experience Platform文档](https://experienceleague.adobe.com/docs/experience-platform/catalog/datasets/overview.html){target=&quot;_blank&quot;}。

了解如何在 [数据摄取概述文档](https://experienceleague.adobe.com/docs/experience-platform/ingestion/home.html?lang=zh-Hans){target=&quot;_blank&quot;}。


**另请参阅**

* [在Journey Optimizer中创建架构、数据集和摄取数据以添加测试用户档案](../segment/creating-test-profiles.md)
* [流摄取概述](https://experienceleague.adobe.com/docs/experience-platform/ingestion/streaming/overview.html?lang=zh-Hans){target=&quot;_blank&quot;}
* [将数据摄取到Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/ingestion/tutorials/ingest-batch-data.html){target=&quot;_blank&quot;}
