---
solution: Journey Optimizer
product: journey optimizer
title: 在历程中使用区段
description: 了解如何在历程中使用区段
feature: Journeys
topic: Content Management
role: User
level: Intermediate
keywords: 活动，历程，读取，区段，平台
exl-id: 7b27d42e-3bfe-45ab-8a37-c55b231052ee
source-git-commit: c235e7cd77e50a15a12f6ed14e51ca4185ecb7c2
workflow-type: tm+mt
source-wordcount: '1337'
ht-degree: 12%

---

# 在历程中使用区段 {#segment-trigger-activity}

## 添加读取区段活动 {#about-segment-trigger-actvitiy}

>[!CONTEXTUALHELP]
>id="ajo_journey_read_segment"
>title="读取区段活动"
>abstract="利用读取区段活动，您可以允许属于 Adobe Experience Platform 区段的所有个人进入历程。进入历程的操作可以执行一次，也可以定期执行。"

使用 **读取区段** 活动使区段的所有个人进入旅程。 进入历程的操作可以执行一次，也可以定期执行。

让我们以中创建的“Luma应用程序打开和结账”区段为例 [构建区段用例](../segment/about-segments.md). 使用 **[!UICONTROL 读取区段]** 活动时，您可以使属于某个区段的所有个人进入旅程，并使他们流入将利用所有旅程功能（条件、计时器、事件、操作）的个性化旅程。

>[!NOTE]
>
>对于使用“读取区段”活动的历程，可以同时启动的历程数具有上限。系统将重试，但请不要同时启动超过 5 个历程（读取区段、预定或“尽快”开始），可以将它们分散到不同的时间，例如间隔 5 到 10 分钟。
>
>以读取区段、区段鉴别或业务事件活动开始的历程中，无法使用体验事件字段组。

### 配置活动 {#configuring-segment-trigger-activity}

配置“读取区段”活动的步骤如下：

1. 展开 **[!UICONTROL 编排]** 类别并放置 **[!UICONTROL 读取区段]** 活动放入画布。

   必须将活动定位为历程的第一步。

1. 添加 **[!UICONTROL 标签]** 到活动（可选）。

1. 在 **[!UICONTROL 区段]** 字段中，选择将进入历程的Adobe Experience Platform区段，然后单击 **[!UICONTROL 保存]**.

   请注意，您可以自定义列表中显示的列，并对其进行排序。

   >[!NOTE]
   >
   >仅具有 **已实现** 和 **现有** 区段参与状态将进入历程。 有关如何评估区段的更多信息，请参阅 [分段服务文档](https://experienceleague.adobe.com/docs/experience-platform/segmentation/tutorials/evaluate-a-segment.html#interpret-segment-results){target="_blank"}.

   ![](assets/read-segment-selection.png)

   添加区段后， **[!UICONTROL 复制]** 按钮允许您复制其名称和ID：

   `{"name":"Luma app opening and checkout",”id":"8597c5dc-70e3-4b05-8fb9-7e938f5c07a3"}`

   ![](assets/read-segment-copy.png)

1. 在 **[!UICONTROL 命名空间]** 字段，选择要使用的命名空间以标识个人。 默认情况下，该字段会使用最后使用的命名空间预填充。 [了解有关命名空间的更多信息](../event/about-creating.md#select-the-namespace).

   >[!NOTE]
   >
   >如果属于区段的个人在不同的身份中没有选定的身份（命名空间），则个人无法进入历程。 您只能选择基于人员的身份命名空间。 如果您为查找表定义了命名空间（例如：产品查找的ProductID命名空间），则该命名空间将无法在 **命名空间** 下拉列表。

1. 设置 **[!UICONTROL 限制率]** 字段到读取区段活动的吞吐量限制。

   此值存储在历程版本有效负载中。 默认值为每秒5,000条消息。 您可以将此值从每秒500条消息修改为每秒20,000条消息。

   >[!NOTE]
   >
   >每个沙盒的总限制速率设置为每秒20,000条消息。 因此，在同一沙盒中同时运行的所有读取区段的限制速率每秒最多可添加20,000条消息。 您无法修改此上限。

1. 此 **[!UICONTROL 读取区段]** 利用活动，可指定区段进入历程的时间。 要执行此操作，请单击 **[!UICONTROL 编辑历程计划]** 用于访问历程属性的链接。然后，配置 **[!UICONTROL 计划程序类型]** 字段。

   ![](assets/read-segment-schedule.png)

   默认情况下，区段进入历程 **[!UICONTROL 尽快]**. 如果要使区段在特定日期/时间或定期进入历程，请从列表中选择所需的值。

   >[!NOTE]
   >
   >请注意 **[!UICONTROL 计划]** 部分仅在 **[!UICONTROL 读取区段]** 活动已放入画布中。

   ![](assets/read-segment-schedule-list.png)

   当具有循环的历程时 **读取区段** 首次执行时，区段中的所有用户档案都进入历程。 使用 **增量读取** 选项，用于在第一次发生后，仅定向自上次执行历程以来进入区段的个人。

   启用 **在重复时强制重入** 选项允许您在下次执行期间自动删除历程中当前所有用户档案。 例如，如果每日循环历程中存在2天等待，则激活此选项会始终将用户档案移动到后续历程执行（第二天），而不管它们是否属于下次运行的受众。 但是，如果此历程中用户档案的持续时间可能超过重复频率，则建议不要启用此选项，以确保用户档案可以完成其历程。

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
>一次性 **读取区段** 历程移至 **已完成** 历程执行30天后的状态。 对于已计划 **读取区段**，则为上次执行后的30天。

### 测试并发布历程 {#testing-publishing}

此 **[!UICONTROL 读取区段]** 活动允许您在单一用户档案上测试历程，或者在符合区段条件的用户档案中随机选择100个测试用户档案上测试历程。

为此，请激活 **测试模式**. 然后，从左窗格中选择所需的选项。

![](assets/read-segment-test-mode.png)

然后，您可以配置并运行 **测试模式** 和往常一样。 [了解如何测试历程](testing-the-journey.md).

测试运行后， **[!UICONTROL 显示日志]** 按钮允许您根据选定的测试选项查看测试结果：

* **[!UICONTROL 一次单个配置文件]**：测试日志显示的信息与使用单一测试模式时相同。 有关更多信息，请参阅 [本节](testing-the-journey.md#viewing_logs)

* **[!UICONTROL 一次最多100个配置文件]**：利用测试日志，可跟踪从Adobe Experience Platform导出区段的进度，以及所有进入旅程的人员的个人进度。

  请注意，一次最多使用100个配置文件测试历程不允许您使用视觉流跟踪历程中个人的进度。

  ![](assets/read-segment-log.png)

测试成功后，即可发布历程(请参阅 [发布历程](publishing-the-journey.md))。 属于区段的个人将在历程的属性中指定的日期/时间进入历程 **[!UICONTROL 调度程序]** 部分。

>[!NOTE]
>
>对于基于区段的定期历程，一旦执行了其最后一次发生次数，该历程将自动关闭。 如果未指定结束日期/时间，则必须手动将历程关闭到新入口，才能结束历程。

## 基于区段的历程中的受众定位

基于区段的历程始终以 **读取区段** 活动以检索属于Adobe Experience Platform区段的个人。

属于区段的受众会被检索一次或定期检索。

进入历程后，您可以创建受众编排用例，使个人从初始区段流入历程的不同分支。

**区段**

您可以使用条件来执行分段，方法是 **条件** 活动。 例如，您可以让VIP人员采用特定路径，而非VIP人员采用其他路径。

分段可以基于：

* 数据源数据
* 历程数据中的事件上下文部分，例如：某人是否单击了一小时前收到的消息？
* 日期，例如：人员是否在六月完成历程？
* 时间，例如：上午是人员时区吗？
* 一种算法，根据百分比拆分历程中流动的受众，例如：90% - 10%以排除控制组

![](assets/read-segment-audience1.png)

**排除**

相同 **条件** 用于分段的活动（见上文）还允许您排除部分群体。 例如，您可以排除VIP人员，方法是使其流入分支中，并在后面紧跟一个结束步骤。

此排除可能紧随区段检索之后、出于群体计数目的或随着多步旅程发生。

![](assets/read-segment-audience2.png)

**Union**

历程允许您创建N个分支，并在分段后将它们联接在一起。

因此，您可以使两个受众返回同一个体验。

例如，在旅程中的十天中完成不同体验后，VIP和非VIP客户可以返回到同一路径。

合并后，您可以通过执行分段或排除来再次拆分受众。

![](assets/read-segment-audience3.png)
