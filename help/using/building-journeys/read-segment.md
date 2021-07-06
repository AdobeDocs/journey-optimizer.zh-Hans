---
title: 在历程中使用区段
description: 了解如何在历程中使用区段
feature: 历程
topic: 内容管理
role: User
level: Intermediate
source-git-commit: b07970ff11f1ba7c4e6db30dc2eca1252a579ca4
workflow-type: tm+mt
source-wordcount: '923'
ht-degree: 6%

---

# 在历程中使用区段 {#segment-trigger-activity}

## 关于读取区段活动 {#about-segment-trigger-actvitiy}

利用读取区段活动，可让属于Adobe Experience Platform区段的所有个人进入历程。 进入历程的操作可以执行一次，也可以定期执行。

让我们以[生成区段](../segment/about-segments.md)用例中创建的“Luma应用程序打开和结帐”区段为例。 通过读取区段活动，您可以让属于此区段的所有个人进入历程，并让他们进入将利用所有历程功能的个性化历程：条件、计时器、事件、操作。

>[!NOTE]
>
>Burst付费附加组件允许以大量量发送非常快速的推送消息，用于包括读取区段和简单推送消息的简单历程。 有关更多信息，请参见[此部分](../building-journeys/journey-gs.md#burst)

### 配置活动 {#configuring-segment-trigger-activity}

配置读取区段活动的步骤如下所示：

1. 展开&#x200B;**[!UICONTROL Orchestration]**&#x200B;类别并将&#x200B;**[!UICONTROL Read Segment]**&#x200B;活动放入画布中。

   活动必须定位为历程的第一步。

1. 向活动添加&#x200B;**[!UICONTROL Label]**（可选）。

1. 在&#x200B;**[!UICONTROL Segment]**&#x200B;字段中，选择将进入历程的Adobe Experience Platform区段，然后单击&#x200B;**[!UICONTROL Save]**。

   请注意，您可以自定义列表中显示的列，并对其进行排序。

   >[!NOTE]
   >
   >只有具有&#x200B;**Remailed**&#x200B;和&#x200B;**Existing**&#x200B;区段参与状态的个人才会进入历程。 有关如何评估区段的更多信息，请参阅[分段服务文档](https://experienceleague.adobe.com/docs/experience-platform/segmentation/tutorials/evaluate-a-segment.html?lang=en#interpret-segment-results){target=&quot;_blank&quot;}。

   ![](../assets/read-segment-selection.png)

   添加客户细分后，即可通过&#x200B;**[!UICONTROL Copy]**&#x200B;按钮复制其名称和 ID：

   `{"name":"Luma app opening and checkout",”id":"8597c5dc-70e3-4b05-8fb9-7e938f5c07a3"}`

   ![](../assets/read-segment-copy.png)

1. 在&#x200B;**[!UICONTROL Namespace]**&#x200B;字段中，选择要用于标识个人的命名空间。 [了解有关命名空间的更多信息](../event/about-creating.md#select-the-namespace)。

   >[!NOTE]
   >
   >属于某个区段、且其不同身份之间没有选定身份（命名空间）的个人无法进入历程。

1. 利用&#x200B;**[!UICONTROL Read Segment]**&#x200B;活动，可指定区段进入历程的时间。 为此，请单击&#x200B;**[!UICONTROL Edit journey schedule]**&#x200B;链接以访问历程的属性，然后配置&#x200B;**[!UICONTROL Scheduler type]**&#x200B;字段。

   ![](../assets/read-segment-schedule.png)

   默认情况下，区段会进入历程&#x200B;**[!UICONTROL As soon as possible]**。 如果要使区段在特定日期/时间或定期进入历程，请从列表中选择所需的值。

   >[!NOTE]
   >
   >请注意，**[!UICONTROL Schedule]**&#x200B;部分仅在&#x200B;**[!UICONTROL Read Segment]**&#x200B;活动被放入画布中时才可用。

   ![](../assets/read-segment-schedule-list.png)

### 测试并发布历程 {#testing-publishing}

利用&#x200B;**[!UICONTROL Read Segment]**&#x200B;活动，可在单一用户档案上或在100个随机测试用户档案（从符合区段资格条件的用户档案中选择）上测试历程。

为此，请激活测试模式，然后从左窗格中选择所需的选项。

![](../assets/read-segment-test-mode.png)

然后，您可以照常配置和运行测试模式。 [了解如何测试历程](testing-the-journey.md)。

运行测试后，**[!UICONTROL Show logs]**&#x200B;按钮允许您根据选定的测试选项查看测试结果：

* **[!UICONTROL Single profile at a time]**:测试日志显示与使用统一测试模式时相同的信息。有关更多信息，请参见[此部分](testing-the-journey.md#viewing_logs)

* **[!UICONTROL Up to 100 profiles at once]**:利用测试日志，可跟踪从Adobe Experience Platform导出区段的进度，以及所有进入历程的人员的个人进度。

   请注意，一次使用最多100个用户档案测试历程不允许使用可视化流程跟踪历程中个人的进度。

   ![](../assets/read-segment-log.png)

测试成功后，您可以发布历程（请参阅[发布历程](publishing-the-journey.md)）。 属于该区段的个人将在历程的属性&#x200B;**[!UICONTROL Scheduler]**&#x200B;部分中指定的日期/时间进入历程。

>[!NOTE]
>
>对于基于区段的定期历程，一旦执行最后一次事件，历程将自动关闭。 如果未指定结束日期/时间，则必须手动关闭通往新入口的历程才能结束。


## 基于客户细分的历程中的受众定位

基于区段的历程始终以&#x200B;**读取区段**&#x200B;活动开始，以检索属于Adobe Experience Platform区段的个人。

属于该区段的受众将定期检索一次。

进入历程后，您可以创建受众编排用例，使个人从初始区段流入历程的不同分支。

**区段**

您可以使用条件来使用&#x200B;**Condition**&#x200B;活动执行分段。 例如，您可以使VIP人员采用特定路径，而非VIP流量进入其他路径。

分段可以基于：

* 数据源数据
* 历程数据中事件部分的上下文，例如：有人点击了她一小时前收到的消息吗？
* 例如，日期：我们是在六月，当一个人走过旅程？
* 例如，某个时间：是在人的时区吗？
* 根据百分比拆分历程中流动的受众的算法，例如：90% - 10% — 排除控制组

![](../assets/read-segment-audience1.png)

**排除**

使用相同的&#x200B;**Condition**&#x200B;活动进行分段（请参阅上文），也可以排除部分群体。 例如，您可以排除VIP人员，方法是：使其流入紧接其后有结束步骤的分支。

出于群体计数目的或多步历程，可能会在检索区段后立即发生此排除。

![](../assets/read-segment-audience2.png)

**Union**

历程允许您在分段后创建N个分支并将它们连接在一起。

因此，您可以让两个受众返回到相同的体验。

例如，在历程中的十天内跟踪不同体验后，VIP和非VIP客户可以返回到同一路径。

合并后，您可以通过执行分段或排除来再次拆分受众。

![](../assets/read-segment-audience3.png)
