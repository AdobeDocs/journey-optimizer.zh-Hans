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
source-git-commit: c52049383bf6a8b60fcb0ab1c2331724c8cdb771
workflow-type: tm+mt
source-wordcount: '2168'
ht-degree: 15%

---

# 在历程中使用受众 {#segment-trigger-activity}

## 关于读取受众活动 {#about-segment-trigger-actvitiy}

>[!CONTEXTUALHELP]
>id="ajo_journey_read_segment"
>title="读取受众活动"
>abstract="利用读取受众活动功能，您可以允许属于 Adobe Experience Platform 受众的所有个人进入历程。进入历程的操作可以执行一次，也可以定期执行。"

使用&#x200B;**读取受众**&#x200B;活动让受众的所有个人进入历程。 进入历程的操作可以执行一次，也可以定期执行。

我们以在[构建受众](../audience/about-audiences.md)用例中创建的“Luma应用程序打开和签出”受众为例。 通过读取受众活动，您可以让属于此受众的所有个人进入历程，并使他们流入将利用所有历程功能（条件、计时器、事件、操作）的个性化历程。

➡️ [通过观看视频了解此功能](#video)

## 护栏和最佳实践 {#must-read}

* 历程中只能使用一个&#x200B;**[!UICONTROL 读取受众]**&#x200B;活动，并且它必须是画布中的第一个活动。

* **[!UICONTROL 读取受众]**&#x200B;活动只能针对一个受众。 如果需要多个受众，请考虑将这些受众合并到单个受众中，然后再使用。 [了解如何使用组合工作流组合受众](../audience/get-started-audience-orchestration.md)

* 对于使用&#x200B;**读取受众**&#x200B;活动的历程，可以同时启动的历程数具有上限。系统将重试，但避免同时启动超过5个历程（具有&#x200B;**读取受众**，已计划或“尽快”开始）。 最佳实践是将其分散到不同的时间，例如相隔5到10分钟。

* 体验事件字段组不能用于以&#x200B;**读取受众**&#x200B;活动、**[受众资格](audience-qualification-events.md)**&#x200B;活动或业务事件活动开始的历程。

* 作为最佳实践，我们建议您仅在&#x200B;**读取受众**&#x200B;活动中使用批次受众。 这将为历程中使用的受众提供可靠且一致的计数。 读取受众专为批量用例而设计。 如果您的用例需要实时数据，请使用&#x200B;**[受众资格](audience-qualification-events.md)**&#x200B;活动。

* 可以在&#x200B;**读取受众**&#x200B;活动中选择从CSV文件[&#128279;](https://experienceleague.adobe.com/docs/experience-platform/segmentation/ui/overview.html?lang=zh-Hans#import-audience)导入或从[组合工作流](../audience/get-started-audience-orchestration.md)生成的受众。 这些受众在&#x200B;**受众资格**&#x200B;活动中不可用。

[此页面](../start/guardrails.md#read-segment-g)中列出了与&#x200B;**读取受众**&#x200B;活动相关的护栏。

## 配置活动 {#configuring-segment-trigger-activity}

配置读取受众活动的步骤如下。

### 添加读取受众活动并选择受众

1. 展开&#x200B;**[!UICONTROL 编排]**&#x200B;类别并将&#x200B;**[!UICONTROL 读取受众]**&#x200B;活动拖放到画布中。

   必须将活动定位为历程的第一步。

1. 向活动添加&#x200B;**[!UICONTROL 标签]**（可选）。

1. 在&#x200B;**[!UICONTROL 受众]**&#x200B;字段中，选择将进入历程的Adobe Experience Platform受众，然后单击&#x200B;**[!UICONTROL 保存]**。 您可以选择使用[区段定义](../audience/creating-a-segment-definition.md)生成的任何Adobe Experience Platform受众。

   >[!NOTE]
   >
   >此外，您还可以定位使用从CSV文件[&#128279;](https://experienceleague.adobe.com/docs/experience-platform/segmentation/ui/overview.html?lang=zh-Hans#import-audience){target="_blank"}上传的[受众合成](../audience/get-started-audience-orchestration.md)或创建的Adobe Experience Platform受众。

   请注意，您可以自定义列表中显示的列，并对其进行排序。

   ![](assets/read-segment-selection.png)

   添加受众后，**[!UICONTROL 复制]**&#x200B;按钮允许您复制其名称和ID：

   `{"name":"Luma app opening and checkout","id":"8597c5dc-70e3-4b05-8fb9-7e938f5c07a3"}`

   ![](assets/read-segment-copy.png)

   >[!NOTE]
   >
   >只有具有&#x200B;**已实现**&#x200B;受众参与状态的个人才能进入历程。 有关如何评估受众的更多信息，请参阅[分段服务文档](https://experienceleague.adobe.com/docs/experience-platform/segmentation/tutorials/evaluate-a-segment.html?lang=zh-Hans#interpret-segment-results){target="_blank"}。

1. 在&#x200B;**[!UICONTROL 命名空间]**&#x200B;字段中，选择要使用的命名空间以标识个人。 默认情况下，该字段会使用最后使用的命名空间预填充。 [了解有关命名空间的更多信息](../event/about-creating.md#select-the-namespace)。

   >[!NOTE]
   >
   >如果受众的不同身份中没有选定的身份（命名空间），则属于该受众的个人无法进入历程。 您只能选择基于人员的身份命名空间。 如果您为查找表定义了命名空间（例如：产品查找的ProductID命名空间），则该命名空间在&#x200B;**命名空间**&#x200B;下拉列表中不可用。

### 管理历程中的用户档案条目

设置&#x200B;**[!UICONTROL 读取率]**。 这是每秒可以进入历程的配置文件的最大数量。 此比率仅适用于此活动，不适用于历程中的其他活动。 例如，如果您想对自定义操作定义限制速率，则需要使用限制API。 请参阅此[页面](../configuration/throttling.md)。

此值存储在历程版本有效负载中。 默认值为每秒5,000个配置文件。 您可以将此值从每秒500个配置文件修改为20,000个配置文件。

>[!NOTE]
>
>每个沙盒的整体读取率设置为每秒20,000个配置文件。 因此，在同一沙盒中同时运行的所有读取受众的读取率每秒最多可添加20,000个配置文件。 您无法修改此上限。

### 计划历程 {#schedule}

>[!CONTEXTUALHELP]
>id="ajo_journey_read_segment_scheduler_start_date"
>title="开始日期/时间"
>abstract="定义您想要触发此历程的日期和时间。"

>[!CONTEXTUALHELP]
>id="ajo_journey_read_segment_scheduler_repeat_until"
>title="重复直到"
>abstract="定义定期事件的结束日期。"

>[!CONTEXTUALHELP]
>id="ajo_journey_read_segment_scheduler_repeat_every"
>title="重复每一次"
>abstract="定义定期调度程序的频率。"

>[!CONTEXTUALHELP]
>id="ajo_journey_read_segment_scheduler_incremental_read"
>title="增量读取"
>abstract="仅允许自上次读取后的新轮廓进入历程。"

>[!CONTEXTUALHELP]
>id="ajo_journey_read_segment_scheduler_force_reentrance"
>title="强制重入"
>abstract="在读取每个受众之前删除所有历程参与者。"

>[!CONTEXTUALHELP]
>id="ajo_journey_read_segment_scheduler_synchronize_audience"
>title="批次受众评估后触发"
>abstract="对批次受众进行新的评估后，请切换启用此选项以触发历程执行。"

>[!CONTEXTUALHELP]
>id="ajo_journey_read_segment_scheduler_synchronize_audience_wait_time"
>title="重新进行新的受众评估的等待时间"
>abstract="指定历程等待对批次受众进行新评估的持续时间。等待期限于整数值，可指定以分钟或小时为单位，并且必须介于 1 到 6 小时之间。"

默认情况下，历程配置为运行一次。 要定义历程应运行的特定日期/时间和频率，请执行以下步骤。

>[!NOTE]
>
>一次性读取受众历程在历程执行91天（[历程全局超时](journey-properties.md#global_timeout)）后移至&#x200B;**已完成**&#x200B;状态。 对于计划的读取受众，此期限为上次执行后的91天。

1. 在&#x200B;**[!UICONTROL 读取受众]**&#x200B;活动属性中，个人助理选择&#x200B;**[!UICONTROL 编辑历程计划]**。

   ![](assets/read-segment-schedule.png)

1. 旅程的属性随即显示。 在&#x200B;**[!UICONTROL 计划程序类型]**&#x200B;下拉列表中，选择您希望历程运行的频率。

   ![](assets/read-segment-schedule-list.png)

对于定期历程，提供特定选项以帮助您管理将用户档案输入历程。 展开以下部分，了解有关每个选项的更多信息。

![](assets/read-audience-options.png)

+++**[!UICONTROL 增量读取]**

当具有定期&#x200B;**读取受众**&#x200B;的历程首次执行时，受众中的所有用户档案都进入该历程。

利用此选项，可在第一次发生后仅定向自上次执行历程以来进入受众的个人。

>[!NOTE]
>
>如果您在历程中以[自定义上传受众](../audience/about-audiences.md#segments-in-journey-optimizer)为目标，则只有在循环历程中启用此选项时，才会在第一次循环时检索配置文件，因为这些受众已修复。

+++

+++**[!UICONTROL 在重复时强制重入]**

利用此选项，可让历程中仍存在的所有用户档案在下次执行时自动退出该历程。

例如，如果您在每日循环历程中等待2天，则通过激活此选项，将始终在下一个历程执行时移动用户档案（因此是在后一天），无论它们是否在下一个运行的受众中。

如果此历程中用户档案的生命周期可能长于重复频率，请勿激活此选项以确保用户档案可以完成其历程。

+++

+++在批量受众评估后触发&#x200B;**&#x200B;**

对于安排在每日和定向批处理受众的历程，您可以定义一个长达6小时的时间范围，以便该历程从批处理分段作业中等待新的受众数据。 如果分段作业在时间范围内完成，则历程将触发。 否则，它会跳过该旅程，直到下一次出现。 此选项确保历程使用准确且最新的受众数据运行。

例如，如果旅程安排在每日下午6点，则可以指定在旅程运行之前等待的分钟数或小时数。 当旅程在下午6点唤醒时，它会检查是否有新受众，这意味着受众比上一个旅程执行中使用的受众新。 在指定的时间范围内，将在检测到新受众后立即执行历程。 但是，如果未检测到新受众，则将跳过当天的历程执行。

增量读取历程的&#x200B;**回顾期**

当选择批量受众评估&#x200B;**后的**&#x200B;触发器时，[!DNL Journey Optimizer]将查找新的受众评估。 对于回顾期间的起点，系统使用上一次成功执行历程的时间，即使该时间发生在24小时之前。 这对于增量读取旅程（通常具有24小时的回溯时段）非常重要。

每日增量读取历程示例：

* 激活“批量受众评估后触发”：如果自增量用户档案进入历程以来已经过了三天，则在查找增量用户档案时，回顾期间将延长三天。
* 不激活“批量受众评估后触发”：如果自增量用户档案进入历程以来已经过了三天，则在查找增量用户档案时，回顾期间将仅返回24小时。

+++

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

## 测试并发布历程 {#testing-publishing}

**[!UICONTROL 读取受众]**&#x200B;活动允许您在单一配置文件上测试历程。

为此，请激活测试模式。

![](assets/read-segment-test-mode.png)

像往常一样配置和运行测试模式。 [了解如何测试历程](testing-the-journey.md)。

测试运行后，**[!UICONTROL 显示日志]**&#x200B;按钮允许您查看测试结果。 有关详细信息，请参阅[此部分](testing-the-journey.md#viewing_logs)

![](assets/read-segment-log.png)

测试成功后，即可发布历程（请参阅[发布历程](publishing-the-journey.md)）。 属于受众的个人将在历程的属性&#x200B;**[!UICONTROL 调度程序]**&#x200B;部分中指定的日期/时间进入历程。

>[!NOTE]
>
>对于基于受众的定期历程，一旦执行了其最后一次发生次数，该历程将自动关闭。 如果未指定结束日期/时间，则必须手动将历程关闭到新入口，才能结束历程。

## 基于受众的历程中的受众定位

基于受众的历程始终以&#x200B;**读取受众**&#x200B;活动开始，以检索属于Adobe Experience Platform受众的个人。

属于受众的受众会被检索一次或定期检索。

进入历程后，您可以创建受众编排用例，使来自初始受众的个人流入历程的不同分支。

**区段**

您可以使用&#x200B;**条件**&#x200B;活动使用条件执行分段。 例如，您可以让VIP人员采用特定的路径，而非VIP人员采用其他路径。

分段可以基于：

* 数据源数据
* 事件上下文是历程数据的一部分，例如：某人是否单击了一小时前收到的消息？
* 例如，日期：人员进入旅程时是否在6月？
* 时间，例如：上午是人员时区吗？
* 一种算法，根据百分比拆分历程中流动的受众，例如：90% - 10%以排除控制组

![](assets/read-segment-audience1.png)

>[!NOTE]
>
>在将“每日”调度程序类型与&#x200B;**[!UICONTROL 读取受众]**&#x200B;活动结合使用时，您可以为历程定义一个等待新受众数据的时间范围。 这可以确保准确定位，并防止批量分段作业延迟导致的问题。 [了解如何计划历程](#schedule)
>
>**[!UICONTROL 批量受众评估后触发]**&#x200B;选项仅适用于一组组织（限量发布）。 要获得访问权限，请与 Adobe 代表联系。

**排除**

用于分段的相同&#x200B;**条件**&#x200B;活动（请参阅上文）还允许您排除部分群体。 例如，您可以排除VIP人员，方法是：让这些人员流入分支中，并在其后执行结束步骤。

此排除可能紧随受众检索之后、出于群体计数目的或随着多步历程而发生。

![](assets/read-segment-audience2.png)

**并集**

历程允许您创建N个分支，并在分段后将它们连接在一起。 因此，您可以使两个受众返回同一个体验。

例如，在旅程中的十天中完成其他体验后，VIP和非VIP客户可以返回到同一路径。 合并后，您可以通过执行分段或排除来再次拆分受众。

![](assets/read-segment-audience3.png)

## 重试 {#read-audience-retry}

在检索导出作业时，重试操作会被默认应用于受众触发的历程（从&#x200B;**读取受众**&#x200B;或&#x200B;**业务事件**&#x200B;开始）。如果在创建导出作业期间发生错误，则每 10 分钟重试一次，最多 1 小时。之后，我们将它视为失败。因此，这些类型的历程可以在预定时间之后 1 小时内执行。

捕获了失败的&#x200B;**读取受众**&#x200B;触发器并将其显示在&#x200B;**警报**&#x200B;中。 如果&#x200B;**读取受众**&#x200B;活动在计划执行时间后的10分钟内未处理任何配置文件，则&#x200B;**读取受众警报**&#x200B;会警告您。 此故障可能是由技术问题或受众为空导致的。 如果这种失败是由技术问题引起的，请注意，根据问题的类型，重试仍然可能发生（例如：如果导出作业创建失败，我们将每10mn重试一次，最长为1h）。 [了解详情](../reports/alerts.md#alert-read-audiences)

## 操作方法视频 {#video}

了解由读取受众活动触发的历程的适用用例。了解如何构建基于批次的历程以及可以应用的最佳实践。

>[!VIDEO](https://video.tv.adobe.com/v/3430362?quality=12&captions=chi_hans)
