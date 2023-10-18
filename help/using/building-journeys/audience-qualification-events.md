---
solution: Journey Optimizer
product: journey optimizer
title: 受众资格事件
description: 了解受众资格事件
feature: Journeys, Activities, Audiences
topic: Content Management
role: User
level: Intermediate
keywords: 资格，事件，受众，历程，平台
exl-id: 7e70b8a9-7fac-4450-ad9c-597fe0496df9
source-git-commit: 07b1f9b885574bb6418310a71c3060fa67f6cac3
workflow-type: tm+mt
source-wordcount: '970'
ht-degree: 29%

---

# 受众资格事件 {#segment-qualification}

## 关于受众资格事件{#about-segment-qualification}

>[!CONTEXTUALHELP]
>id="ajo_journey_event_segment_qualification"
>title="受众资格事件"
>abstract="此活动允许您的历程侦听 Adobe Experience Platform 受众中配置文件的进出口，以便使个人进入历程或在历程中前进。"

此活动允许您的历程侦听 Adobe Experience Platform 受众中配置文件的进出口，以便使个人进入历程或在历程中前进。有关创建受众的详细信息，请参阅此 [部分](../audience/about-audiences.md).

假设您拥有“白银客户”受众。通过此活动，您可以使所有新的白银客户进入历程，并向其发送一系列个性化消息。

此类事件可定位为历程的第一步或后续步骤。

### 重要说明{#important-notes-segment-qualification}

* 请记住，Adobe Experience Platform受众每天计算一次(**批次** 受众)或实时(**流式传输** 受众(使用Adobe Experience Platform的“高频受众”选项)。

* 如果对所选受众进行流式处理，则属于此受众的个人可能会实时进入历程。 如果受众是批量受众，则新近符合此受众条件的人员可能会在Adobe Experience Platform上执行受众计算时进入历程。

* 以读取受众、受众鉴别或业务事件活动开始的历程中，无法使用体验事件字段组。

* 在历程中使用受众资格时，该受众资格活动可能最多需要 10 分钟才能生效，并侦听进入或退出受众的用户档案。

### 配置活动{#cnfigure-segment-qualification}

1. 展开 **[!UICONTROL 活动]** 类别并放置 **[!UICONTROL 受众资格]** 活动移入画布。

   ![](assets/segment5.png)

1. 添加 **[!UICONTROL 标签]** 到活动。 此步骤是可选的。

1. 单击 **[!UICONTROL 受众]** 字段并选择要利用的受众。

   >[!NOTE]
   >
   >请注意，您可以自定义列表中显示的列，并对其进行排序。

   ![](assets/segment6.png)

   添加受众后， **[!UICONTROL 复制]** 按钮允许您复制其名称和ID：

   `{"name":"Loyalty membership“,”id":"8597c5dc-70e3-4b05-8fb9-7e938f5c07a3"}`

   ![](assets/segment-copy.png)

1. 在 **[!UICONTROL 行为]** 字段中，选择要侦听受众入口、出口还是两者。

   >[!NOTE]
   >
   >请注意 **[!UICONTROL 输入]** 和 **[!UICONTROL 退出]** 对应于 **已实现** 和 **已退出** Adobe Experience Platform的受众参与状态。 有关如何评估受众的更多信息，请参阅 [Segmentation Service文档](https://experienceleague.adobe.com/docs/experience-platform/segmentation/tutorials/evaluate-a-segment.html#interpret-segment-results){target="_blank"}.

1. 选择命名空间。仅当将事件定位为历程的第一步时，才需要此操作。 默认情况下，该字段会使用最后使用的命名空间预填充。

   >[!NOTE]
   >
   >您只能选择基于人员的身份命名空间。 如果您为查找表定义了命名空间（例如：产品查找的ProductID命名空间），则它将在 **命名空间** 下拉列表。

   ![](assets/segment7.png)

有效负荷包含以下可以在条件和操作中使用的上下文信息：

* 行为（入口、出口）
* 资格时间戳
* 受众id

在后跟的条件或操作中使用表达式编辑器时 **[!UICONTROL 受众资格]** 活动，则您有权访问 **[!UICONTROL AudienceQualification]** 节点。 您可以选择 **[!UICONTROL 上次资格取得时间]** 和 **[!UICONTROL 状态]** （进入或退出）。

请参阅[条件活动](../building-journeys/condition-activity.md#about_condition)。

![](assets/segment8.png)

包括受众资格活动的新历程将在您发布十分钟后开始运行。 此时间间隔对应于专用服务的缓存刷新时间间隔。 因此，您必须等待10分钟才能使用此历程。

## 最佳实践 {#best-practices-segments}

此 **[!UICONTROL 受众资格]** 活动允许在Adobe Experience Platform受众中获得资格或被取消资格的个人在历程中立即进入。

该信息的接收速度很快。所做的测量显示速度为每秒接收 10,000 个事件。因此，您应该确保了解入口峰值可能如何出现、如何避开，以及如何使历程针对此类情况做好准备。

### 批量受众{#batch-speed-segment-qualification}

在对批量受众使用受众资格时，请注意，在每日计算时将出现入口峰值。 峰值的大小将取决于每天进入（或退出）受众的个人数量。

此外，如果在历程中新建并立即使用批量受众，则第一批计算可能会使大量个人进入历程。

### 流式处理受众{#streamed-speed-segment-qualification}

在对流式传输的受众使用受众资格时，由于持续评估受众，入口/出口出现大量峰值的风险较小。 但是，如果受众定义导致大量客户同时获得资格，则也可能会出现峰值。

有关流式客户细分的更多信息，请参阅 [Adobe Experience Platform文档](https://experienceleague.adobe.com/docs/experience-platform/segmentation/api/streaming-segmentation.html#api)

### 如何避免过载{#overloads-speed-segment-qualification}

以下是将有助于避免使历程中利用的系统（数据源、自定义操作、渠道操作活动）过载的一些最佳实践。

请勿在中使用 **[!UICONTROL 受众资格]** 活动，即创建后的立即批量受众。 它将避免第一个计算峰值。请注意，如果您要使用从未计算的受众，则历程画布中将出现黄色警告。

![](assets/segment-error.png)

为历程中使用的数据源和操作设置上限规则，以避免其过载。 了解详情，请参阅 [Journey Orchestration文档](https://experienceleague.adobe.com/docs/journeys/using/working-with-apis/capping.html){target="_blank"}. 请注意，上限规则不带重试。如果需要重试，则必须通过选中框在历程中使用替代路径 **[!UICONTROL 在超时或错误的情况下添加替代路径]** 在条件或操作中。

在生产历程中使用受众之前，请始终首先评估每天符合此受众条件的个人数量。 为此，您可以检查 **[!UICONTROL 受众]** 菜单，打开受众，然后查看 **[!UICONTROL 随时间变化的配置文件]** 图形。

![](assets/segment-overload.png)
