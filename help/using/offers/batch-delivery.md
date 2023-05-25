---
title: 批量决策
description: 了解如何将优惠决策投放给给定Adobe Experience Platform区段中的所有用户档案。
exl-id: 810c05b3-2bae-4368-bf12-3ea8c2f31c01
source-git-commit: 9657862f1c6bdb2399fcf3e6384bb9dec5b8f32b
workflow-type: tm+mt
source-wordcount: '833'
ht-degree: 2%

---

# 批量决策 {#deliver}

## 开始使用批量决策 {#start}

Journey Optimizer允许您向给定Adobe Experience Platform区段中的所有用户档案投放优惠决策。

为此，您需要在Journey Optimizer中创建一个作业请求，该请求将包含有关要定位的区段和要使用的优惠决策的信息。 然后，区段中每个配置文件的选件内容将放入Adobe Experience Platform数据集，该数据集可用于自定义批处理工作流。

也可以使用API执行批量交付。 有关详情，请参阅 [Batch Decisioning API文档](api-reference/offer-delivery-api/batch-decisioning-api.md).

## 先决条件 {#prerequisites}

在配置作业请求之前，请确保已创建：

* **数据集** 在Adobe Experience Platform中。 此数据集将用于使用“ODE DecisionEvents”架构存储决策结果。 了解详情，请参阅 [数据集文档](https://experienceleague.adobe.com/docs/experience-platform/catalog/datasets/overview.html?lang=zh-Hans).

* **区段** 在Adobe Experience Platform中。 应评估并更新区段。 了解如何更新中的区段会员资格评估 [分段服务文档](http://www.adobe.com/go/segmentation-overview-en)

   >[!NOTE]
   >
   >批处理作业以每天发生一次的配置文件快照运行。 批量决策会限制此频率，并始终从最新快照加载用户档案。 在您创建区段后，最长可能等待24小时，然后再尝试使用批量决策API。

* **决策** 在Adobe Journey Optimizer中。 [了解如何创建决策](offer-activities/create-offer-activities.md)

<!-- in API doc, remove these info and add ref here-->

## 创建作业请求

要创建新的作业请求，请执行以下步骤。

1. 在 **[!UICONTROL 选件]** 菜单，打开 **[!UICONTROL 批量决策]** 选项卡，然后单击 **[!UICONTROL 创建请求]**.

   ![](assets/batch-create.png)

1. 命名作业请求，然后选择作业数据应发送到的数据集。

1. 选择要定位的Adobe Experience Platform区段。

1. 选择您要用于向区段投放优惠的一个或多个优惠决策范围：
   1. 从列表中选择一个版面。
   1. 将显示可用于所选版面的决策。 选择您选择的决策并单击 **[!UICONTROL 添加]**.
   1. 重复该操作以添加所需数量的决策范围。

   ![](assets/batch-decision.png)

1. 默认情况下，将为每个用户档案返回一个决策范围选件。 您可以使用调整返回的优惠数量 **[!UICONTROL 每个配置文件的请求优惠]** 选项。 例如，如果选择2，则会为选定的决策范围显示最佳的2个优惠。

   >[!NOTE]
   >
   >您最多可以为每个决策范围请求30个优惠。

1. 如果要将选件内容包含在数据集中，请切换 **[!UICONTROL 包含内容]** 选项启用。 此选项默认处于禁用状态。

1. 单击 **[!UICONTROL 创建]** 执行作业请求。

## 监测批处理作业

所有请求的批处理作业都可以从 **[!UICONTROL 批量决策]** 选项卡。 此外，搜索和筛选工具也可用于帮助您优化列表。

![](assets/batch-list.png)

### 作业请求状态

创建作业请求后，批处理作业将经历多种状态：

>[!NOTE]
>
>要确保您获得有关作业请求状态的最新信息，请使用作业旁边的省略号按钮进行刷新。

1. **[!UICONTROL 已排队]**：作业请求已创建并已进入处理队列。 每个数据集一次最多可以运行5个批处理作业。 具有相同输出数据集的任何其他批处理请求都将添加到队列中。 一旦前一个作业运行完成，系统会选取已排队作业进行处理。
1. **[!UICONTROL 正在处理]**：正在处理作业请求
1. **[!UICONTROL 正在引入]**：已执行作业请求，正在选定数据集中摄取结果数据，
1. **[!UICONTROL 已完成]**：已执行作业请求，并且结果数据现在存储在所选数据集中。

   >[!NOTE]
   >
   >通过单击作业列表中的作业名称，您可以访问存储作业结果的数据集。

如果在执行作业请求时出错，它将获得 **[!UICONTROL 错误]** 状态。 尝试复制批处理作业以创建新请求。 [了解如何复制批处理作业](#duplicate)

### 批处理作业处理时间

每个批处理作业的端到端时间是从工作负载创建时到决策结果在输出数据集中可用的时长。

区段大小是影响端到端批量决策时间的主要因素。 如果符合条件的优惠启用了全局频率限制，则批量决策需要额外的时间才能完成。 下面是其各自区段大小端到端处理时间的一些近似值，包括有和无符合条件的优惠的频率上限：

为符合条件的优惠启用了频率上限：

| 区段大小 | 端到端处理时间 |
|--------------|----------------------------|
| 1万个或更少配置文件 | 7 分钟 |
| 100万个或更少配置文件 | 30 分钟 |
| 1500万个或更少的用户档案 | 50 分钟 |

符合条件的优惠没有频率上限：

| 区段大小 | 端到端处理时间 |
|--------------|----------------------------|
| 1万个或更少配置文件 | 6 分钟 |
| 100万个或更少配置文件 | 8 分钟 |
| 1500万个或更少的用户档案 | 16 分钟 |

## 复制作业请求 {#duplicate}

您可以重用现有作业的信息来创建新请求。

要执行此操作，请单击复制图标，根据需要编辑作业信息，然后单击 **[!UICONTROL 创建]** 以创建新请求。

![](assets/batch-duplicate.png)
