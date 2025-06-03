---
solution: Journey Optimizer
product: journey optimizer
title: 受众鉴定事件
description: 了解如何使用及配置受众资格事件
feature: Journeys, Activities, Audiences
topic: Content Management
role: User
level: Intermediate
keywords: 资格，事件，受众，历程，平台
exl-id: 7e70b8a9-7fac-4450-ad9c-597fe0496df9
source-git-commit: 84beb9ba9646cb1b40bcfd8a180fc98963a8ff0b
workflow-type: tm+mt
source-wordcount: '1191'
ht-degree: 12%

---

# 受众鉴定事件 {#segment-qualification}

>[!CONTEXTUALHELP]
>id="ajo_journey_event_segment_qualification"
>title="受众鉴定事件"
>abstract="此活动允许您的历程侦听轮廓是否符合 Adobe Experience Platform 受众资格，以便使个人进入历程或在历程中前进。"

## 关于受众资格筛选事件{#about-segment-qualification}

此活动允许您的旅程侦听Adobe Experience Platform受众中用户档案的进出口，以便使个人进入旅程或在旅程中前进。 有关创建受众的详细信息，请参阅此[部分](../audience/about-audiences.md)。

假设您拥有“白银客户”受众。通过此活动，您可以使所有新的白银客户进入历程，并向其发送一系列个性化消息。

此类事件可定位为历程的第一步或后续步骤。

➡️ [通过观看视频了解此功能](#video)

### 护栏和建议 {#important-notes-segment-qualification}

遵循以下护栏和建议以构建Audience Qualification历程。 另请参阅[受众资格最佳实践](#best-practices-segments)。


* 受众资格历程主要设计用于流受众。 这种结合保证了更好的实时体验。 强烈建议在受众资格活动中使用&#x200B;**流式受众**。

  但是，如果要在流式受众或批量受众中使用基于批量摄取的属性进行受众资格历程，请考虑用于受众评估/激活的时间范围。 使用批量摄取属性的批量受众或流式受众在分段作业完成后约&#x200B;**2小时**&#x200B;即可在&#x200B;**受众资格**&#x200B;活动中使用。 此作业每天在Adobe组织管理员定义的时间运行一次。

* Adobe Experience Platform受众每天计算一次（**批次**&#x200B;受众），或使用Adobe Experience Platform的“高频受众”选项实时计算（针对&#x200B;**流式传输**&#x200B;受众）。

   * 如果对所选受众进行流式处理，则属于此受众的个人可能会实时进入历程。
   * 如果受众是批量受众，则新近符合此受众条件的人员可能会在Adobe Experience Platform上执行受众计算时进入历程。

  作为最佳实践，请在&#x200B;**受众资格**&#x200B;活动中使用流式受众。 对于批量用例，请使用&#x200B;**[读取受众](read-audience.md)**&#x200B;活动。

  >[!NOTE]
  >
  >由于使用组合工作流和自定义上传创建的受众具有批次性质，因此无法在“受众资格”活动中定位这些受众。 此活动中只能利用使用区段定义创建的受众。


* 以&#x200B;**读取受众**、**受众资格**&#x200B;或&#x200B;**业务事件**&#x200B;活动开始的历程中，无法使用体验事件字段组。

* 在历程中使用&#x200B;**受众资格**&#x200B;活动时，该活动可能最多需要10分钟才能激活，并侦听进入或退出受众的用户档案。


>[!CAUTION]
>
>实时客户配置文件数据和分段的[护栏](https://experienceleague.adobe.com/docs/experience-platform/profile/guardrails.html?lang=zh-Hans){target="_blank"}也适用于Adobe Journey Optimizer。



### 配置活动 {#configure-segment-qualification}

要配置&#x200B;**[!UICONTROL 受众资格]**&#x200B;活动，请执行以下步骤：

1. 展开&#x200B;**[!UICONTROL 事件]**&#x200B;类别并将&#x200B;**[!UICONTROL 受众资格]**&#x200B;活动放入画布中。

   ![](assets/segment5.png)

1. 向活动添加&#x200B;**[!UICONTROL 标签]**。 此步骤是可选的。

1. 单击&#x200B;**[!UICONTROL 受众]**&#x200B;字段并选择要利用的受众。

   >[!NOTE]
   >
   >您可以自定义列表中显示的列并对其进行排序。

   ![](assets/segment6.png)

   添加受众后，**[!UICONTROL 复制]**&#x200B;按钮允许您复制其名称和ID：

   `{"name":"Loyalty membership","id":"8597c5dc-70e3-4b05-8fb9-7e938f5c07a3"}`

   ![](assets/segment-copy.png)

1. 在&#x200B;**[!UICONTROL Behavior]**&#x200B;字段中，选择要侦听受众入口、出口还是两者。

   >[!NOTE]
   >
   >**[!UICONTROL Enter]**&#x200B;和&#x200B;**[!UICONTROL Exit]**&#x200B;对应于Adobe Experience Platform中的&#x200B;**Realized**&#x200B;和&#x200B;**Exited**&#x200B;受众参与状态。 有关如何评估受众的更多信息，请参阅[分段服务文档](https://experienceleague.adobe.com/docs/experience-platform/segmentation/tutorials/evaluate-a-segment.html?lang=zh-Hans#interpret-segment-results){target="_blank"}。

1. 选择命名空间。仅当将事件定位为历程的第一步时，才需要此操作。 默认情况下，该字段会使用最后使用的命名空间预填充。

   >[!NOTE]
   >
   >您只能选择基于人员的身份命名空间。 如果您为查找表定义了命名空间（例如：产品查找的ProductID命名空间），则该命名空间在&#x200B;**命名空间**&#x200B;下拉列表中不可用。

   ![](assets/segment7.png)

有效负荷包含以下可以在条件和操作中使用的上下文信息：

* 行为（入口、出口）
* 资格筛选时间戳
* 受众id

在遵循&#x200B;**[!UICONTROL 受众资格]**&#x200B;活动的条件或操作中使用表达式编辑器时，您有权访问&#x200B;**[!UICONTROL AudienceQualification]**&#x200B;节点。 您可以选择&#x200B;**[!UICONTROL 上次资格取得时间]**&#x200B;和&#x200B;**[!UICONTROL 状态]**（进入或退出）。

请参阅[条件活动](../building-journeys/condition-activity.md#about_condition)。

![](assets/segment8.png)

包含&#x200B;**受众资格**&#x200B;事件的新历程在发布十分钟后即可开始运行。 此时间间隔对应于专用服务的缓存刷新时间间隔。 因此，您必须等待10分钟才能使用此历程。

## 最佳实践 {#best-practices-segments}

**[!UICONTROL 受众资格]**&#x200B;活动允许在Adobe Experience Platform受众中获得资格或被取消资格的个人立即进入历程。

该信息的接收速度很快。测量显示每秒接收10,000个事件的速度。 因此，请确保您了解入口峰值可能如何出现、如何避开，以及如何使历程针对这些情况做好准备。

### 批量受众 {#batch-speed-segment-qualification}

在对批量受众使用“受众资格”时，请注意，在每日计算时会出现入口峰值。 峰值的大小取决于每天进入（或退出）受众的个人数量。

此外，如果在历程中新创建并立即使用批量受众，则第一批计算可能会导致大量个人进入历程。

### 流式处理受众 {#streamed-speed-segment-qualification}

在对流式传输的受众使用受众资格时，由于持续评估受众，入口/出口出现大量峰值的风险较小。 但是，如果受众定义导致大量客户同时符合条件，则仍可能会出现峰值。

避免使用具有流式分段的“打开”和“发送”事件。 相反，应使用真正的用户活动信号，如点击次数、购买次数或信标数据。 对于频率或抑制逻辑，请使用业务规则而不是发送事件。 [了解详情](../audience/about-audiences.md#open-and-send-event-guardrails)

有关流式客户细分的更多信息，请参阅[Adobe Experience Platform文档](https://experienceleague.adobe.com/zh-hans/docs/experience-platform/segmentation/methods/streaming-segmentation){target="_blank"}。

### 如何避免过载 {#overloads-speed-segment-qualification}

以下是避免使历程中利用的系统（数据源、自定义操作、渠道操作活动）过载的一些最佳实践：

* 在&#x200B;**[!UICONTROL 受众资格]**&#x200B;活动中创建批次受众后，请勿立即使用批次受众。 这样可以避免第一个计算峰值。 如果您要使用从未计算的受众，则历程画布中会显示黄色警告。

  ![](assets/segment-error.png)

* 为历程中使用的数据源和操作设置上限规则，以避免其过载。 请参阅[Journey Orchestration文档](https://experienceleague.adobe.com/docs/journeys/using/working-with-apis/capping.html?lang=zh-Hans){target="_blank"}以了解详情。 请注意，上限规则不带重试。如果需要重试，请通过选中框&#x200B;**[!UICONTROL 在条件或操作中出现超时或错误]**&#x200B;时添加替代路径来在历程中使用替代路径。

* 在生产历程中使用受众之前，请每天评估符合此受众条件的个人数量。 为此，请检查&#x200B;**[!UICONTROL 受众]**&#x200B;菜单，打开受众，然后查看&#x200B;**[!UICONTROL 随时间变化的配置文件]**&#x200B;图形。

  ![](assets/segment-overload.png)

## 操作说明视频 {#video}

通过此视频了解受众资格历程的适用用例。 了解如何使用Audience Qualification构建历程以及可以应用的最佳实践。

>[!VIDEO](https://video.tv.adobe.com/v/3446214?quality=12&captions=chi_hans)
