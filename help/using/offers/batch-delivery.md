---
title: 批量决策
description: 了解如何向给定Adobe Experience Platform受众中的所有用户档案投放优惠决策。
badge: label="旧版" type="Informative"
feature: Decision Management
role: User
level: Intermediate
exl-id: 810c05b3-2bae-4368-bf12-3ea8c2f31c01
source-git-commit: 87f3da0a1d73f9aa26c7420d260778286bacdf0c
workflow-type: tm+mt
source-wordcount: '842'
ht-degree: 5%

---

# 批量决策 {#deliver}

## 开始使用批量决策 {#start}

利用Journey Optimizer，可将优惠决策投放给给给定Adobe Experience Platform受众中的所有用户档案。

为此，您需要在Journey Optimizer中创建一个作业请求，该请求将包含有关要定位的受众和要使用的优惠决策的信息。 然后，受众中每个用户档案的选件内容会放置在Adobe Experience Platform数据集中，可用于自定义批处理工作流。

也可以使用API执行批量交付。 有关详细信息，请参阅[批量决策API文档](api-reference/offer-delivery-api/batch-decisioning-api.md)。

## 先决条件 {#prerequisites}

在配置作业请求之前，请确保已创建：

* Adobe Experience Platform中的&#x200B;**数据集**。 此数据集将用于使用“ODE DecisionEvents”架构存储决策结果。 请参阅[数据集文档](https://experienceleague.adobe.com/docs/experience-platform/catalog/datasets/overview.html?lang=zh-Hans)以了解详情。

* Adobe Experience Platform中的&#x200B;**受众**。 应评估并更新受众。 请参阅[分段服务文档](https://www.adobe.com/go/segmentation-overview-en_cn)以了解如何更新受众成员资格评估

  >[!NOTE]
  >
  >批处理作业将使用每天发生一次的配置文件快照运行。 批量决策可限制频率并始终从最新快照加载用户档案。 预计在创建受众后最多等待24小时，然后再尝试批量决策API。

* Adobe Journey Optimizer中的&#x200B;**决策**。 [了解如何创建决策](offer-activities/create-offer-activities.md)

<!-- in API doc, remove these info and add ref here-->

## 创建作业请求

要创建新的作业请求，请执行以下步骤。

1. 在&#x200B;**[!UICONTROL 选件]**&#x200B;菜单中，打开&#x200B;**[!UICONTROL 批量决策]**&#x200B;选项卡，然后单击&#x200B;**[!UICONTROL 创建请求]**。

   ![](assets/batch-create.png)

1. 命名您的作业请求，然后选择应将作业数据发送到的数据集。

1. 选择要定位的Adobe Experience Platform受众。

1. 选择您要用于向受众提供优惠的一个或多个优惠决策范围：
   1. 从列表中选择版面。
   1. 将显示可用于选定版面的决策。 选择您选择的决策并单击&#x200B;**[!UICONTROL 添加]**。
   1. 重复该操作以添加所需数量的决策范围。

   ![](assets/batch-decision.png)

1. 默认情况下，将为每个用户档案返回一个决策范围选件。 您可以使用&#x200B;**[!UICONTROL 每个配置文件的请求选件]**&#x200B;选项调整返回的选件数。 例如，如果您选择 2，则在所选决策范围内将显示最佳的 2 个产品建议。

   >[!NOTE]
   >
   >您最多可以为每个决策范围请求30个优惠。

1. 如果要在数据集中包含选件内容，请启用&#x200B;**[!UICONTROL 包含内容]**&#x200B;选项。 默认禁用此选项。

1. 单击&#x200B;**[!UICONTROL 创建]**&#x200B;以执行作业请求。

## 监测批处理作业

所有请求的批处理作业都可以从&#x200B;**[!UICONTROL 批量决策]**&#x200B;选项卡访问。 此外，搜索和筛选工具也可用于帮助您优化列表。

![](assets/batch-list.png)

### 作业请求状态

创建作业请求后，批处理作业将经历多种状态：

>[!NOTE]
>
>要确保您获得有关作业请求状态的最新信息，请使用作业旁边的省略号按钮进行刷新。

1. **[!UICONTROL 已排队]**：作业请求已创建并已进入处理队列。 每个数据集一次最多可以运行5个批处理作业。 具有相同输出数据集的任何其他批处理请求都将添加到队列中。 一旦前一个作业运行完成，系统会选取已排队作业进行处理。
1. **[!UICONTROL 正在处理]**：正在处理作业请求
1. **[!UICONTROL 正在摄取]**：已执行作业请求，正在选定数据集中摄取结果数据，
1. **[!UICONTROL 已完成]**：作业请求已执行，结果数据现在已存储到所选的数据集中。

   >[!NOTE]
   >
   >您可以通过单击作业列表中的作业名称来访问存储作业结果的数据集。

如果执行作业请求时出错，它将获得&#x200B;**[!UICONTROL 错误]**&#x200B;状态。 尝试复制批处理作业以创建新请求。 [了解如何复制批处理作业](#duplicate)

### 批处理作业处理时间

每个批处理作业的端到端时间是从工作负载创建到决策结果在输出数据集中可用的时间之间的持续时间。

受众规模是影响端到端批量决策时间的主要因素。 如果符合条件的优惠启用了全局频率限制，则批量决策需要更多时间才能完成。 下面是其各自受众规模的端到端处理时间的一些近似值，包含和不包含合格优惠的频率上限：

为符合条件的优惠启用了频率上限：

| 受众规模 | 端到端处理时间 |
|--------------|----------------------------|
| 1万个或更少配置文件 | 7 分钟 |
| 100万个或更少配置文件 | 30 分钟 |
| 1500万个或更少配置文件 | 50 分钟 |

符合条件的优惠没有频率上限：

| 受众规模 | 端到端处理时间 |
|--------------|----------------------------|
| 1万个或更少配置文件 | 6 分钟 |
| 100万个或更少配置文件 | 8 分钟 |
| 1500万个或更少配置文件 | 16 分钟 |

## 复制作业请求 {#duplicate}

您可以重用现有作业的信息来创建新请求。

为此，请单击“复制”图标，根据需要编辑作业信息，然后单击&#x200B;**[!UICONTROL 创建]**&#x200B;以创建新请求。

![](assets/batch-duplicate.png)
