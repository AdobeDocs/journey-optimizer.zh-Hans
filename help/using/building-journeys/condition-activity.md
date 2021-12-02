---
title: 条件活动
description: 了解条件活动
feature: Journeys
topic: Content Management
role: User
level: Intermediate
exl-id: 496c7666-a133-4aeb-be8e-c37b3b9bf5f9
source-git-commit: 43e4e089025721180a6b8ce9ea9104a2f73d3e47
workflow-type: tm+mt
source-wordcount: '982'
ht-degree: 10%

---

# 条件活动{#section_e2n_pft_dgb}

可以使用以下类型的条件：

* [数据源条件](#data_source_condition)
* [时间条件](#time_condition)
* [百分比拆分](#percentage_split)
* [日期条件](#date_condition)
<!--
* [Profile cap](#profile_cap)
-->

![](../assets/journey49.png)

## 关于条件活动 {#about_condition}

在历程中使用多个条件时，您可以为其中每个条件定义标签，以便更轻松地识别它们。

单击 **[!UICONTROL Add a path]** 要定义多个条件时，请执行以下操作： 对于每个条件，都会在活动后的画布中添加新路径。

![](../assets/journey47.png)

请注意，历程的设计会对功能产生影响。 在条件后定义多个路径时，将只执行第一个符合条件的路径。 这意味着您可以通过将路径置于彼此之上或之下来改变路径的优先级。

例如，让我们以第一个路径的条件“人员是VIP”和第二个路径的条件“人员是男性”为例。 如果符合这两个条件的人员(男性，VIP)通过此步骤，则将选择第一个路径，即使此人也有资格使用第二个路径，因为第一个路径“高于”。 要更改此优先级，请按其他垂直顺序移动活动。

![](../assets/journey48.png)

您可以通过选中 **[!UICONTROL Show path for other cases than the one(s) above]**. 请注意，此选项在拆分条件中不可用。 请参阅 [百分比拆分](#percentage_split).

利用简单模式，可根据字段组合执行简单查询。 所有可用字段都显示在屏幕的左侧。 将字段拖放到主区域中。 要组合不同的元素，请将它们互相联锁，以创建不同的组和/或组级别。 然后，您可以选择逻辑运算符来组合同一级别上的元素：

* 和：两个条件的交集。 只考虑与所有条件匹配的元素。
* 或：两个标准的并集。 考虑至少符合一个条件的元素。

![](../assets/journey64.png)

如果您使用 [Adobe Experience Platform Segmentation Service](https://experienceleague.adobe.com/docs/experience-platform/segmentation/home.html){target=&quot;_blank&quot;}要创建区段，您可以在历程条件中利用这些区段。 请参阅 [在条件中使用区段](../building-journeys/condition-activity.md#using-a-segment).


>[!NOTE]
>
>无法使用简单的编辑器对时间序列（例如购买列表、消息的过去点击）执行查询。 为此，您将需要使用高级编辑器。 请参阅 [AdobeJourney Orchestration文档](expression/expressionadvanced.md).

当操作或条件中发生错误时，个人历程将停止。使其继续的唯一方法是选中 **[!UICONTROL Add an alternative path in case of a timeout or an error]** 框。请参阅[此章节](../building-journeys/using-the-journey-designer.md#paths)。

在简单编辑器中，您还可以在事件和数据源类别下方找到历程属性类别。 此类别包含与给定用户档案的历程相关的技术字段。 这是系统从实时历程中检索到的信息，如历程 ID 或遇到的特定错误。有关更多信息，请参阅 [AdobeJourney Orchestration文档](expression/journey-properties.md)

## 数据源条件 {#data_source_condition}

这允许您根据数据源中的字段或先前位于历程中的事件定义条件。 要了解如何使用表达式编辑器，请参阅 [AdobeJourney Orchestration文档](expression/expressionadvanced.md). 使用高级表达式编辑器，您可以设置更高级的条件来处理集合或使用需要传递参数的数据源。 请参阅[此页](../datasource/external-data-sources.md)。

![](../assets/journey50.png)

## 时间条件{#time_condition}

这样，您就可以根据一天中的某个小时和/或一周中的某天执行不同的操作。 例如，您可以决定在白天发送短信消息，在工作日发送夜间电子邮件。

>[!NOTE]
>
>时区不再特定于条件，现在在历程属性的历程级别定义。 请参见[此页面](../building-journeys/timezone-management.md)。

![](../assets/journey51.png)

## 百分比拆分 {#percentage_split}

利用此选项，可随机拆分受众以为每个群组定义不同的操作。 为每个路径定义拆分数和重新分区。 拆分计算是统计的，因为系统无法预测此历程活动中将会有多少人流。 因此，分割具有非常低的误差范围。 此函数基于Java随机机制(请参阅 [页面](https://docs.oracle.com/javase/7/docs/api/java/util/Random.html))。

在测试模式下，达到拆分时，将始终选择顶部分支。 如果希望测试选择其他路径，则可以重新组织拆分分支的位置。 请参见[此页面](../building-journeys/testing-the-journey.md)。

>[!NOTE]
>
>请注意，没有按钮可在百分比拆分条件中添加路径。 路径的数量将取决于拆分的数量。 在拆分条件中，您无法为其他情况添加路径，因为该路径不可能发生。 人们将始终进入一条分割的路径。

![](../assets/journey52.png)

## 日期条件 {#date_condition}

这允许您根据日期定义不同的流量。 例如，如果人员在“销售”期间进入该步骤，您将向他们发送特定消息。 你今年剩下的时间，你会再发一条信息。

>[!NOTE]
>
>时区不再特定于条件，现在在历程属性的历程级别定义。 请参阅[此页](../building-journeys/timezone-management.md)。

![](../assets/journey53.png)

<!--
## Profile cap {#profile_cap}

Use this condition type to set a maximum number of profiles for a journey path. When this limit is reached, the entering profiles take an alternate path.

You can use this condition type to ramp up the volume of your deliveries. See this [use case](ramp-up-deliveries-uc.md).

The default cap is 1000. You can set an integer value from 1 to 20,000.

The counter applies only to the selected journey version. The counter is reset to zero after 180 days. After a reset, the entering profiles take the nominal path again until the counter limit is reached.

The nominal path always has priority over the alternate path, even if you move the alternate path above the nominal path on the journey canvas.

![](../assets/profile-cap-condition.png)
-->

## 在条件中使用区段 {#using-a-segment}

本节介绍如何在历程条件中使用区段。 有关区段以及如何构建区段的更多信息，请参阅 [此部分](../segment/about-segments.md).

要在历程条件中使用区段，请执行以下步骤：

1. 打开旅程，删除 **[!UICONTROL Condition]** 活动，然后选择 **数据源条件**.
   ![](../assets/journey47.png)

1. 单击 **[!UICONTROL Add a path]** 每个需要的额外路径。 对于每个路径，单击 **[!UICONTROL Expression]** 字段。

   ![](../assets/segment3.png)

1. 在左侧，展开 **[!UICONTROL Segments]** 节点。 拖放要用于条件的区段。 默认情况下，区段上的条件为true。

   ![](../assets/segment4.png)

   >[!NOTE]
   >
   >请注意，只有 **已实现** 和 **现有** 区段参与状态将被视为区段的成员。 有关如何评估区段的更多信息，请参阅 [Segmentation Service文档](https://experienceleague.adobe.com/docs/experience-platform/segmentation/tutorials/evaluate-a-segment.html#interpret-segment-results){target=&quot;_blank&quot;}。
