---
title: 在历程中使用区段
description: 了解如何在历程中使用区段
feature: Journeys
topic: Content Management
role: User
level: Intermediate
exl-id: 7b27d42e-3bfe-45ab-8a37-c55b231052ee
source-git-commit: 1abea49a0dce8d5866662235b243a3b82fb50c7b
workflow-type: tm+mt
source-wordcount: '1036'
ht-degree: 7%

---

# 在历程中使用区段 {#segment-trigger-activity}

## 关于读取区段活动 {#about-segment-trigger-actvitiy}

利用读取区段活动，可让属于Adobe Experience Platform区段的所有个人进入历程。 进入历程的操作可以执行一次，也可以定期执行。

以在 [生成区段](../segment/about-segments.md) 用例。 通过读取区段活动，您可以让属于此区段的所有个人进入历程，并让他们进入将利用所有历程功能的个性化历程：条件、计时器、事件、操作。

>[!NOTE]
>
>Burst付费附加组件允许以大量量发送非常快速的推送消息，用于包括读取区段和简单推送消息的简单历程。 有关更多信息，请参阅 [此部分](../building-journeys/journey-gs.md#burst)

### 配置活动 {#configuring-segment-trigger-activity}

配置读取区段活动的步骤如下所示：

1. 展开&#x200B;**[!UICONTROL Orchestration]**&#x200B;类别并将&#x200B;**[!UICONTROL Read Segment]**&#x200B;活动放入画布中。

   活动必须定位为历程的第一步。

1. 添加 **[!UICONTROL Label]** （可选）。

1. 在 **[!UICONTROL Segment]** 字段中，选择将进入历程的Adobe Experience Platform区段，然后单击 **[!UICONTROL Save]**.

   请注意，您可以自定义列表中显示的列，并对其进行排序。

   >[!NOTE]
   >
   >只有 **已实现** 和 **现有** 区段参与状态将进入历程。 有关如何评估区段的更多信息，请参阅 [Segmentation Service文档](https://experienceleague.adobe.com/docs/experience-platform/segmentation/tutorials/evaluate-a-segment.html#interpret-segment-results){target=&quot;_blank&quot;}。

   ![](../assets/read-segment-selection.png)

   添加客户细分后，即可通过&#x200B;**[!UICONTROL Copy]**&#x200B;按钮复制其名称和 ID：

   `{"name":"Luma app opening and checkout",”id":"8597c5dc-70e3-4b05-8fb9-7e938f5c07a3"}`

   ![](../assets/read-segment-copy.png)

1. 在 **[!UICONTROL Namespace]** 字段中，选择要用于标识个人的命名空间。 [了解有关命名空间的更多信息](../event/about-creating.md#select-the-namespace).

   >[!NOTE]
   >
   >属于某个区段、且其不同身份之间没有选定身份（命名空间）的个人无法进入历程。

1. 设置 **[!UICONTROL Throttling rate]** 字段，以限制读取区段活动的吞吐量。

   此值存储在历程版本有效负载中。 默认值为每秒17,000条消息。 您可以将此值从每秒500条修改为17,000条消息。

   >[!NOTE]
   >
   >每个沙盒的总限制率设置为每秒20,000条消息。 因此，在同一沙盒中同时运行的所有读取区段的限制速率每秒最多可达20,000条消息。 您无法修改此上限。

1. 的 **[!UICONTROL Read Segment]** 活动允许您指定区段进入历程的时间。 为此，请单击 **[!UICONTROL Edit journey schedule]** 链接以访问历程的属性，然后配置 **[!UICONTROL Scheduler type]** 字段。

   ![](../assets/read-segment-schedule.png)

   默认情况下，区段会进入历程 **[!UICONTROL As soon as possible]**. 如果要使区段在特定日期/时间或定期进入历程，请从列表中选择所需的值。

   >[!NOTE]
   >
   >请注意， **[!UICONTROL Schedule]** 部分仅在 **[!UICONTROL Read Segment]** 活动已在画布中删除。

   ![](../assets/read-segment-schedule-list.png)

   的 **增量读取** 选项允许您仅定位自上次执行历程后进入区段的个人。 第一次执行始终定向所有区段成员。 此选项仅可重复使用 **读取区段** 活动。

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

### 测试并发布历程 {#testing-publishing}

的 **[!UICONTROL Read Segment]** 活动允许您在单一用户档案上或在100个随机测试从符合区段资格的用户档案中选择的用户档案上测试历程。

为此，请激活测试模式，然后从左窗格中选择所需的选项。

![](../assets/read-segment-test-mode.png)

然后，您可以照常配置和运行测试模式。 [了解如何测试历程](testing-the-journey.md).

测试运行后， **[!UICONTROL Show logs]** 按钮可根据选定的测试选项查看测试结果：

* **[!UICONTROL Single profile at a time]**:测试日志显示与使用统一测试模式时相同的信息。 有关更多信息，请参阅 [此部分](testing-the-journey.md#viewing_logs)

* **[!UICONTROL Up to 100 profiles at once]**:利用测试日志，可跟踪从Adobe Experience Platform导出区段的进度，以及所有进入历程的人员的个人进度。

   请注意，一次使用最多100个用户档案测试历程不允许使用可视化流程跟踪历程中个人的进度。

   ![](../assets/read-segment-log.png)

测试成功后，您可以发布历程(请参阅 [发布历程](publishing-the-journey.md))。 属于该区段的个人将在历程属性中指定的日期/时间进入历程 **[!UICONTROL Scheduler]** 中。

>[!NOTE]
>
>对于基于区段的定期历程，一旦执行最后一次事件，历程将自动关闭。 如果未指定结束日期/时间，则必须手动关闭通往新入口的历程才能结束。

## 基于客户细分的历程中的受众定位

基于区段的历程始终以 **读取区段** 活动来检索属于Adobe Experience Platform区段的个人。

属于该区段的受众将定期检索一次。

进入历程后，您可以创建受众编排用例，使个人从初始区段流入历程的不同分支。

**区段**

您可以使用条件通过 **条件** 活动。 例如，您可以使VIP人员采用特定路径，而非VIP流量进入其他路径。

分段可以基于：

* 数据源数据
* 历程数据中事件部分的上下文，例如：某人点击了一小时前收到的消息吗？
* 例如，日期：我们是在六月，当一个人走过旅程？
* 例如，某个时间：是在人的时区吗？
* 根据百分比拆分历程中流动的受众的算法，例如：90% - 10% — 排除控制组

![](../assets/read-segment-audience1.png)

**排除**

相同 **条件** 用于分段的活动（请参阅上文）还允许您排除部分群体。 例如，您可以排除VIP人员，方法是：使其流入紧接其后有结束步骤的分支。

出于群体计数目的或多步历程，可能会在检索区段后立即发生此排除。

![](../assets/read-segment-audience2.png)

**Union**

历程允许您在分段后创建N个分支并将它们连接在一起。

因此，您可以让两个受众返回到相同的体验。

例如，在历程中的十天内跟踪不同体验后，VIP和非VIP客户可以返回到同一路径。

合并后，您可以通过执行分段或排除来再次拆分受众。

![](../assets/read-segment-audience3.png)
