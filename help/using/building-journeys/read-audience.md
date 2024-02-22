---
solution: Journey Optimizer
product: journey optimizer
title: 在历程中使用受众
description: 了解如何在历程中使用受众
feature: Journeys, Activities, Audiences
topic: Content Management
role: User
level: Intermediate
keywords: 活动，历程，读取，受众，平台
exl-id: 7b27d42e-3bfe-45ab-8a37-c55b231052ee
source-git-commit: d3f0adab52ed8e44a6097c5079396d1e9c06e0a7
workflow-type: tm+mt
source-wordcount: '1427'
ht-degree: 7%

---

# 在历程中使用受众 {#segment-trigger-activity}

## 添加“读取受众”活动 {#about-segment-trigger-actvitiy}

>[!CONTEXTUALHELP]
>id="ajo_journey_read_segment"
>title="读取受众活动"
>abstract="利用读取受众活动功能，您可以允许属于 Adobe Experience Platform 受众的所有个人进入历程。进入历程的操作可以执行一次，也可以定期执行。"

使用 **读取受众** 活动使受众的所有个人进入历程。 进入历程的操作可以执行一次，也可以定期执行。

以中创建的“Luma应用程序打开和签出”受众为例 [构建受众](../audience/about-audiences.md) 用例。 通过读取受众活动，您可以让属于此受众的所有个人进入历程，并使他们流入将利用所有历程功能（条件、计时器、事件、操作）的个性化历程。

➡️ [在视频中发现此功能](#video)

## 必读 {#must-read}

* 对于使用 **读取受众** 活动时，可以同时开始的历程数已达到上限。 系统将执行重试，但避免具有超过五个历程(使用 **读取受众**，已计划或“尽快”开始)。 最佳实践是将其分散到不同的时间，例如相隔5到10分钟。

* 以开始的历程中无法使用体验事件字段组 **读取受众** 活动，和 **[受众资格](audience-qualification-events.md)** 活动或业务事件活动。

* 作为最佳实践，我们建议您仅在中使用批量受众 **读取受众** 活动。 这将为历程中使用的受众提供可靠且一致的计数。 读取受众专为批量用例而设计。 如果您的用例需要实时数据，请使用 **[受众资格](audience-qualification-events.md)** 活动。

* 受众 [从CSV文件导入](https://experienceleague.adobe.com/docs/experience-platform/segmentation/ui/overview.html#import-audience) 或源自 [组合工作流](../audience/get-started-audience-orchestration.md) 可以在以下位置选择 **读取受众** 活动。 这些受众在中不可用 **受众资格** 活动。

## 配置活动 {#configuring-segment-trigger-activity}

配置读取受众活动的步骤如下：

1. 展开 **[!UICONTROL 编排]** 类别并放置 **[!UICONTROL 读取受众]** 活动移入画布。

   必须将活动定位为历程的第一步。

1. 添加 **[!UICONTROL 标签]** 到活动（可选）。

1. 在 **[!UICONTROL 受众]** 字段中，选择将进入历程的Adobe Experience Platform受众，然后单击 **[!UICONTROL 保存]**. 您可以选择使用以下方式生成的任何Adobe Experience Platform受众 [区段定义](../audience/creating-a-segment-definition.md).

   >[!NOTE]
   >
   >此外，您还可以定位通过创建的Adobe Experience Platform受众 [受众合成](../audience/get-started-audience-orchestration.md) 或 [从CSV文件上传](https://experienceleague.adobe.com/docs/experience-platform/segmentation/ui/overview.html#import-audience){target="_blank"}.

   请注意，您可以自定义列表中显示的列，并对其进行排序。

   ![](assets/read-segment-selection.png)

   添加受众后， **[!UICONTROL 复制]** 按钮允许您复制其名称和ID：

   `{"name":"Luma app opening and checkout","id":"8597c5dc-70e3-4b05-8fb9-7e938f5c07a3"}`

   ![](assets/read-segment-copy.png)

   >[!NOTE]
   >
   >仅具有 **已实现** 和 **现有** 受众参与状态将进入历程。 有关如何评估受众的更多信息，请参阅 [Segmentation Service文档](https://experienceleague.adobe.com/docs/experience-platform/segmentation/tutorials/evaluate-a-segment.html#interpret-segment-results){target="_blank"}.

1. 在 **[!UICONTROL 命名空间]** 字段中，选择要使用的命名空间以标识个人。 默认情况下，该字段会使用最后使用的命名空间预填充。 [了解有关命名空间的更多信息](../event/about-creating.md#select-the-namespace).

   >[!NOTE]
   >
   >如果受众的不同身份中没有选定的身份（命名空间），则属于该受众的个人无法进入历程。 您只能选择基于人员的身份命名空间。 如果您为查找表定义了命名空间（例如：产品查找的ProductID命名空间），则它将在 **命名空间** 下拉列表。

1. 设置 **[!UICONTROL 读取率]**. 这是每秒可以进入历程的配置文件的最大数量。 此比率仅适用于此活动，不适用于历程中的其他活动。 例如，如果您想对自定义操作定义限制速率，则需要使用限制API。 请参阅此 [页面](../configuration/throttling.md).

   此值存储在历程版本有效负载中。 默认值为每秒5,000个配置文件。 您可以将此值从每秒500个配置文件修改为20,000个配置文件。

   >[!NOTE]
   >
   >每个沙盒的整体读取率设置为每秒20,000个配置文件。 因此，在同一沙盒中同时运行的所有读取受众的读取率每秒最多可添加20,000个配置文件。 您无法修改此上限。

1. 此 **[!UICONTROL 读取受众]** 利用活动，可指定受众进入历程的时间。 要执行此操作，请单击 **[!UICONTROL 编辑历程计划]** 链接以访问历程的属性，然后配置 **[!UICONTROL 计划程序类型]** 字段。

   ![](assets/read-segment-schedule.png)

   默认情况下，受众会进入历程 **[!UICONTROL 尽快]**. 如果要让受众在特定日期/时间或定期进入历程，请从列表中选择所需的值。

   >[!NOTE]
   >
   >请注意 **[!UICONTROL 计划]** 部分仅在 **[!UICONTROL 读取受众]** 活动已放入画布中。

   ![](assets/read-segment-schedule-list.png)

   **增量读取** 选项：当具有循环的历程时 **读取受众** 首次执行时，受众中的所有用户档案都会进入历程。 利用此选项，可在第一次发生后仅定向自上次执行历程以来进入受众的个人。

   **在重复时强制重入**：利用此选项可让历程中仍存在的所有用户档案在下次执行时自动退出历程。 例如，如果您在每日循环历程中等待2天，则通过激活此选项，将始终在下一个历程执行时移动用户档案（因此是在后一天），无论它们是否在下一个运行的受众中。 如果此历程中用户档案的生命周期可能长于重复频率，请勿激活此选项以确保用户档案可以完成其历程。

<!--

### Segment filters {#segment-filters}

[!CONTEXTUALHELP]
>id="jo_segment_filters"
>title="About segment filters"
>abstract="You can choose to target only the individuals who entered or exited a specific segment during a specific time window. For example, you can decide to only retrieve all the customers who entered the VIP segment since last week."

You can choose to target only the individuals who entered or exited a specific segment during a specific time window. For example, you can decide to only retrieve all the customers who entered the VIP segment since last week. Only the new VIP customers will be targeted. All the customers who were already part of the VIP segment before will be excluded.

To activate this mode, click the **Segment Filters** toggle. Two fields are displayed:

**Segment membership**: choose whether you want to listen to segment entrances or exits. 

**Lookback window**: define when you want to start to listen to entrances or exits. This lookback window is expressed in hours, starting from the moment the journey is triggered.  If you set this duration to 0, the journey will target all members of the segment. For recurring journeys, it will take into account all entrances/exits since the last time the journey was triggered.

-->

>[!NOTE]
>
>一次性读取受众历程在历程执行30天后会变为“已完成”状态。 对于计划的读取受众，此期限为上次执行后的30天。

## 测试并发布历程 {#testing-publishing}

此 **[!UICONTROL 读取受众]** 利用活动，可在单一用户档案上测试历程。

为此，请激活测试模式。

![](assets/read-segment-test-mode.png)

像往常一样配置和运行测试模式。 [了解如何测试历程](testing-the-journey.md).

测试运行后， **[!UICONTROL 显示日志]** 按钮以查看测试结果。 有关详细信息，请参见 [本节](testing-the-journey.md#viewing_logs)

![](assets/read-segment-log.png)

测试成功后，即可发布历程(请参阅 [发布旅程](publishing-the-journey.md))。 属于受众的个人将在历程属性中指定的日期/时间进入历程 **[!UICONTROL 计划程序]** 部分。

>[!NOTE]
>
>对于基于受众的定期历程，一旦执行了其最后一次发生次数，该历程将自动关闭。 如果未指定结束日期/时间，则必须手动将历程关闭到新入口，才能结束历程。

## 基于受众的历程中的受众定位

基于受众的历程始终以 **读取受众** 活动，用于检索属于Adobe Experience Platform受众的个人。

属于受众的受众会被检索一次或定期检索。

进入历程后，您可以创建受众编排用例，使来自初始受众的个人流入历程的不同分支。

**区段**

您可以使用条件来执行分段，方法是 **条件** 活动。 例如，您可以让VIP人员采用特定路径，而非VIP人员采用其他路径。

分段可以基于：

* 数据源数据
* 事件上下文是历程数据的一部分，例如：某人是否单击了一小时前收到的消息？
* 例如，日期：人员进入旅程时是否在6月？
* 时间，例如：上午是人员时区吗？
* 一种算法，根据百分比拆分历程中流动的受众，例如：90% - 10%以排除控制组

![](assets/read-segment-audience1.png)

**排除**

相同 **条件** 用于分段的活动（请参阅上文）还允许您排除部分群体。 例如，您可以排除VIP人员，方法是：让这些人员流入分支中，并在其后执行结束步骤。

此排除可能紧随受众检索之后、出于群体计数目的或随着多步历程而发生。

![](assets/read-segment-audience2.png)

**Union**

历程允许您创建N个分支，并在分段后将它们连接在一起。

因此，您可以使两个受众返回同一个体验。

例如，在旅程中完成十天的其他体验后，VIP和非VIP客户可以返回同一路径。

合并后，您可以通过执行分段或排除来再次拆分受众。

![](assets/read-segment-audience3.png)

## 操作方法视频 {#video}

了解由读取受众活动触发的历程的适用用例。了解如何构建基于批次的历程以及可以应用的最佳实践。

>[!VIDEO](https://video.tv.adobe.com/v/3424997?quality=12)
