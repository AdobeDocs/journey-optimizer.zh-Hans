---
solution: Journey Optimizer
product: journey optimizer
title: 在历程中使用受众
description: 了解如何配置和使用读取受众活动，以使 [!DNL Adobe Experience Platform] 受众中的个人进入历程。
feature: Journeys, Activities, Audiences
topic: Content Management
role: User
level: Intermediate
keywords: 活动，历程，读取受众，受众，区段，批处理，入口点，触发器，计划，受众资格
exl-id: 7b27d42e-3bfe-45ab-8a37-c55b231052ee
version: Journey Orchestration
source-git-commit: fc64ca7ef0935ce72ec5bb1cf88546a22d5ca0a4
workflow-type: tm+mt
source-wordcount: '3605'
ht-degree: 5%

---

# 在历程中使用受众 {#segment-trigger-activity}

使用读取受众活动，开始具有已定义受众的历程。 您可以选择受众及其运行时间；然后使用条件、计时器和操作将每个用户档案的路径个性化。

## 关于读取受众活动 {#about-segment-trigger-activity}

>[!CONTEXTUALHELP]
>id="ajo_journey_read_segment"
>title="读取受众活动"
>abstract="将来自选定[!DNL Adobe Experience Platform]受众的所有符合条件的配置文件添加到此历程。 运行一次或按计划运行。"

**读取受众**&#x200B;活动是历程入口点活动，可将选定[!DNL Adobe Experience Platform]受众的所有配置文件添加到历程。 您可以按一次或定期计划运行入口。 在API和技术参考中，此活动也称为区段触发器或基于受众的历程条目。

**何时使用“读取受众”与“受众资格”**

| 使用&#x200B;**读取受众**&#x200B;时间 | 在以下情况下使用&#x200B;**[受众资格](audience-qualification-events.md)**： |
|----------------------------|-----------------------------------------------------------------------|
| 您希望按计划（批处理）运行一次历程。 | 您需要用户档案在符合条件时实时进入历程。 |
| 您的受众将进行批量评估（例如，每日快照）。 | 您的受众是流式传输或基于事件的。 |
| 您可以容忍受众评估和历程输入之间的延迟。 | 当配置文件符合条件时，您需要立即输入。 |

**键限制：**&#x200B;每个历程一个读取受众（必须是第一个活动）；每个活动一个受众；每个组织最多并发运行五个读取受众；每个沙盒每秒有20,000个配置文件；12小时作业超时。 [护栏和建议](#must-read)中的完整详细信息。

**先决条件：**&#x200B;已生成并评估的[!DNL Adobe Experience Platform]受众（已实现状态）、为历程选择的基于人员的身份命名空间，以及对于定期运行，了解[计划和吞吐量限制](#must-read)。

例如，在`Luma app opening and checkout`生成受众[用例中创建的](../audience/about-audiences.md)受众可以用作入口点。 所有符合条件的用户档案都会使用条件、计时器、事件和操作进入旅程并经过个性化路径。

➡️ [通过观看视频了解此功能](#video)


>[!CAUTION]
>
>* 在使用读取受众活动之前，[请阅读护栏和限制](#must-read)。

## 配置活动 {#configuring-segment-trigger-activity}

您将设置：**受众**（必需）、**命名空间**（必需）、**读取率**（必需，默认5,000/s）和&#x200B;**计划**（历程运行时）。 可以选择添加&#x200B;**标签**&#x200B;和&#x200B;**补充标识符**。 以下步骤将指导您完成每个设置。

### 添加活动并选择受众 {#add-activity-and-select-audience}

>[!CONTEXTUALHELP]
>id="ajo_journey_read_segment_label"
>title="标签"
>abstract="在报告和测试模式日志中标识此活动的可选标签。"

>[!CONTEXTUALHELP]
>id="ajo_journey_read_segment_audience"
>title="受众"
>abstract="选择其配置文件将进入此历程的[!DNL Adobe Experience Platform]受众。"

>[!CONTEXTUALHELP]
>id="ajo_journey_read_segment_namespace"
>title="命名空间"
>abstract="选择用于识别进入历程的个人的身份（例如电子邮件、ECID）。 选择列表中的顶部选项，以获得与Business Rules和上限的最佳兼容性。"

1. 展开&#x200B;**[!UICONTROL 编排]**&#x200B;类别并将&#x200B;**[!UICONTROL 读取受众]**&#x200B;活动拖放到画布中。

   必须将活动定位为历程的第一步。

1. 向活动添加&#x200B;**[!UICONTROL 标签]**（可选）。 可选标签可帮助您在报告和测试模式日志中识别活动。

1. 在&#x200B;**[!UICONTROL 受众]**&#x200B;字段中，选择将进入历程的[!DNL Adobe Experience Platform]受众，然后单击&#x200B;**[!UICONTROL 保存]**。 您可以选择使用[!DNL Adobe Experience Platform]区段定义[生成的任何](../audience/creating-a-segment-definition.md)受众。

   >[!NOTE]
   >
   >此外，您还可以定位使用[!DNL Adobe Experience Platform]受众合成[创建的](../audience/get-started-audience-orchestration.md)受众。
   >您还可以定位从CSV文件[上传的受众](https://experienceleague.adobe.com/docs/experience-platform/segmentation/ui/overview.html?lang=zh-Hans#import-audience){target="_blank"}。
   >[了解有关如何在Journey Optimizer中生成和定位受众的更多信息](../audience/about-audiences.md)。

   请注意，您可以自定义列表中显示的列，并对其进行排序。

   ![受众选择界面显示可用的[!DNL Adobe Experience Platform]受众](assets/read-segment-selection.png)

   添加受众后，**[!UICONTROL 复制]**&#x200B;按钮允许您复制其名称和ID：

   `{"name":"Luma app opening and checkout","id":"8597c5dc-70e3-4b05-8fb9-7e938f5c07a3"}`

   ![复制按钮以复制JSON格式的受众名称和ID](assets/read-segment-copy.png)

   >[!NOTE]
   >
   >只有具有&#x200B;**已实现**&#x200B;受众参与状态的个人才能进入历程。 有关如何评估受众的更多信息，请参阅[分段服务文档](https://experienceleague.adobe.com/docs/experience-platform/segmentation/tutorials/evaluate-a-segment.html?lang=zh-Hans#interpret-segment-results){target="_blank"}。

1. 在&#x200B;**[!UICONTROL 命名空间]**&#x200B;字段中，选择要使用的命名空间以标识个人。 默认情况下，该字段会使用最后使用的命名空间预填充。 [了解有关命名空间的更多信息](../event/about-creating.md#select-the-namespace)。

   >[!NOTE]
   >
   >如果受众的不同身份中没有选定的身份（命名空间），则属于该受众的个人无法进入历程。 您只能选择基于人员的身份命名空间。 如果您为查找表定义了命名空间（例如：产品查找的ProductID命名空间），则该命名空间在&#x200B;**命名空间**&#x200B;下拉列表中不可用。

### 补充标识符 {#read-audience-supplemental-id}

>[!CONTEXTUALHELP]
>id="ajo_journey_parameters_supplemental_identifier"
>title="使用补充标识符"
>abstract="历程上下文的可选辅助标识符（例如订单ID）。 选择字段及其命名空间。"

您可以选择启用&#x200B;**使用补充标识符**&#x200B;在配置文件标识符之外的辅助标识符（例如，订单ID或预订ID）的上下文中运行历程。 当补充标识符不同时，这允许同一配置文件的多个入口。

[了解如何在历程中使用补充标识符](supplemental-identifier.md)。 对于读取受众历程，补充标识符必须是配置文件属性；使用补充ID时，读取率限制为每秒500个配置文件。

### 护栏和建议 {#must-read}

* 历程中只能使用一个&#x200B;**[!UICONTROL 读取受众]**&#x200B;活动，并且它必须是画布中的第一个活动。

* **[!UICONTROL 读取受众]**&#x200B;活动只能针对一个受众。 如果需要多个受众，请考虑将这些受众合并到单个受众中，然后再使用。 [了解如何使用组合工作流组合受众](../audience/get-started-audience-orchestration.md)

* 对于使用&#x200B;**读取受众**&#x200B;活动的历程，可以同时启动的历程数具有上限。系统将执行重试。 但是，请避免同时启动超过5个历程（具有&#x200B;**读取受众**、已计划或“尽快”开始）。 最佳实践是将其分散到不同的时间，例如相隔5到10分钟。

* 体验事件字段组不能用于以&#x200B;**读取受众**&#x200B;活动、**[受众资格](audience-qualification-events.md)**&#x200B;活动或业务事件活动开始的历程。

* 作为最佳实践，我们建议您仅在&#x200B;**读取受众**&#x200B;活动中使用批次受众。 这将为历程中使用的受众提供可靠且一致的计数。 读取受众专为批量用例而设计。 如果您的用例需要实时数据，请使用&#x200B;**[受众资格](audience-qualification-events.md)**&#x200B;活动。

* 可以在[读取受众](https://experienceleague.adobe.com/docs/experience-platform/segmentation/ui/overview.html?lang=zh-Hans#import-audience)活动中选择从CSV文件[导入或从](../audience/get-started-audience-orchestration.md)组合工作流&#x200B;**生成的受众**。 这些受众在&#x200B;**受众资格**&#x200B;活动中不可用。

* 每个组织的并行读取受众限制：每个组织最多可同时运行五个读取受众实例。 这包括计划的运行以及业务事件触发的运行。 此限制适用于所有沙盒和历程。 强制实施此限制以确保在所有组织间公平和平衡的资源分配。

* 沙盒吞吐量管理：系统动态管理每个沙盒的处理吞吐量，最大限制为每秒20,000个配置文件，在所有读取受众活动中共享。 单个读取受众活动可以配置为最低速率为每秒500个配置文件。 如果达到沙盒级别的吞吐量限制，作业可能会排队以确保公平的资源分配。

* 作业处理超时：读取由于护栏限制在12小时内无法处理的受众作业，将自动清理这些作业，永不执行。 这样可以防止作业累积并确保系统稳定性。

* 使用批处理区段时，请确保在历程开始之前完成摄取和每日快照更新。 如果区段必须反映同一天摄取的数据，请考虑额外的等待期。 如果即时用户档案刷新率至关重要，请使用基于事件的方法或流式方法，而不是每日批量方法。 或者，插入等待机制以允许更新的数据在旅程评估之前传播。

**此页面**&#x200B;中列出了与[读取受众](../start/guardrails.md#read-segment-g)活动相关的护栏。

>[!CAUTION]
>
>实时客户配置文件数据和分段的[护栏](https://experienceleague.adobe.com/docs/experience-platform/profile/guardrails.html?lang=zh-Hans){target="_blank"}也适用于[!DNL Adobe Journey Optimizer]。

**下一步：**&#x200B;设置[读取率](#profile-entry-and-reading-rate)和[计划](#schedule)，然后[测试和发布](#testing-publishing)。

### 配置文件输入和读取率 {#profile-entry-and-reading-rate}

>[!CONTEXTUALHELP]
>id="ajo_journey_read_segment_reading_rate"
>title="读取率"
>abstract="每秒进入历程的最大用户档案(500-20,000)。 默认值为5,000。"

设置&#x200B;**[!UICONTROL 读取率]**（必需）。 这是每秒可以进入历程的配置文件的最大数量。 此比率仅适用于此活动，不适用于历程中的其他活动。 例如，如果您想对自定义操作定义限制速率，则需要使用限制API。 请参见[此页面](../configuration/throttling.md)。

此值存储在历程版本有效负载中。 默认值为每秒5,000个配置文件。 您可以将此值从每秒500个配置文件修改为20,000个配置文件。

>[!NOTE]
>
>每个沙盒的整体读取率设置为每秒20,000个配置文件。 因此，在同一沙盒中同时运行的所有读取受众的读取率每秒最多可添加20,000个配置文件。 您无法修改此上限。 在[本节](entry-management.md#journey-processing-rate)中了解有关历程处理率和吞吐量的更多信息。

### 计划历程 {#schedule}

>[!CONTEXTUALHELP]
>id="ajo_journey_read_segment_scheduler_start_date"
>title="开始日期/时间"
>abstract="何时开始此历程。"

>[!CONTEXTUALHELP]
>id="ajo_journey_read_segment_scheduler_repeat_until"
>title="重复直到"
>abstract="定期运行的结束日期。"

>[!CONTEXTUALHELP]
>id="ajo_journey_read_segment_scheduler_repeat_every"
>title="重复每一次"
>abstract="历程运行的频率（例如，每天、每周）。"

>[!CONTEXTUALHELP]
>id="ajo_journey_read_segment_scheduler_incremental_read"
>title="增量读取"
>abstract="首次运行后，只有添加到受众的新配置文件进入历程。"

>[!CONTEXTUALHELP]
>id="ajo_journey_read_segment_scheduler_force_reentrance"
>title="强制重入"
>abstract="在读取每个新受众之前，清除历程中的所有参与者。"

>[!CONTEXTUALHELP]
>id="ajo_journey_read_segment_scheduler_synchronize_audience"
>title="批次受众评估后触发"
>abstract="仅在最新评估批次受众后运行历程。"

>[!CONTEXTUALHELP]
>id="ajo_journey_read_segment_scheduler_synchronize_audience_wait_time"
>title="重新进行新的受众评估的等待时间"
>abstract="历程等待新受众数据的时长（1-6个小时，以分钟或小时为单位）。"

默认情况下，历程配置为运行一次。 要定义历程应运行的特定日期/时间和频率，请执行以下步骤。

>[!NOTE]
>
>一次性读取受众历程在历程执行91天（**历程全局超时**）后移至[已完成](journey-properties.md#global_timeout)状态。 对于计划的读取受众，此期限为上次执行后的91天。

1. 在&#x200B;**[!UICONTROL 读取受众]**&#x200B;活动属性中，选择&#x200B;**[!UICONTROL 编辑历程计划]**。

   读取受众活动属性中的![编辑历程计划按钮](assets/read-segment-schedule.png)

1. 旅程的属性随即显示。 在&#x200B;**[!UICONTROL 计划程序类型]**&#x200B;下拉列表中，选择您希望历程运行的频率。

   ![包含频率选项的调度程序类型下拉列表：一次、每天、每周、每月](assets/read-segment-schedule-list.png)

对于定期历程，提供特定选项以帮助您管理将用户档案输入历程。 展开以下部分，了解有关每个选项的更多信息。

![读取受众循环选项：增量读取、强制重入、批处理后触发](assets/read-audience-options.png)

+++**[!UICONTROL 增量读取]**

当具有定期&#x200B;**读取受众**&#x200B;的历程首次执行时，受众中的所有用户档案都进入该历程。 利用此选项，可在首次发生后仅定向自上次执行历程以来进入受众的个人。

使用此选项时，系统会从&#x200B;**的分段服务执行的上次受众评估作业的时间开始，回顾** 24小时[!DNL Adobe Experience Platform]。

分段完成后，将开始配置文件快照导出作业，该作业允许Journey Optimizer检测和处理新配置文件。 如果在这两个作业之间计划了历程，则增量读取将不会选取自上次执行历程以来成为受众成员的用户档案。

要最大限度地降低丢失用户档案的风险，请执行以下操作：
* 启用&#x200B;**[!UICONTROL 在批量受众评估后触发]**&#x200B;选项，将回顾时间扩展到上一次成功执行历程的时间，而不管它是在多长时间之前发生的
* 安排在每日批处理分段作业完成后运行良好的历程（通常为2-3小时的缓冲）
* 对于需要立即包含用户档案的时间关键用例，请考虑改用具有流式受众的[受众资格](audience-qualification-events.md)活动

>[!CAUTION]
>
>如果您在历程中以[自定义上传受众](../audience/about-audiences.md#about-segments)为目标，则仅当在循环历程中启用此选项时，才会在第一次循环时检索配置文件。 这些受众是固定的。

+++

+++**[!UICONTROL 在重复时强制重入]**

利用此选项，可让历程中仍存在的所有用户档案在下次执行时自动退出该历程。

例如，如果您在每日循环历程中等待2天，则激活此选项会将用户档案移动到下一个历程执行。 此事件发生在第二天，无论它们是否处于下次运行的受众中。

如果此历程中用户档案的生命周期可能长于重复频率，请勿激活此选项以确保用户档案可以完成其历程。

+++

+++在批量受众评估后触发&#x200B;**&#x200B;**

对于安排在每日和定向批处理受众的历程，您可以定义一个长达6小时的时间范围，以便该历程从批处理分段作业中等待新的受众数据。 如果分段作业在时间范围内完成，则历程将触发。 否则，它会跳过旅程，直到下一次出现。 此选项确保历程使用准确且最新的受众数据运行。

例如，如果旅程安排在每日下午6点，则可以指定在旅程运行之前等待的分钟数或小时数。 当旅程在下午6点唤醒时，它会检查是否有新受众，这意味着受众比上一个旅程执行中使用的受众新。 在指定的时间范围内，将在检测到新受众后立即执行历程。 如果未检测到新受众，则将跳过当天的历程执行。

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

![具有测试配置文件选择的读取受众活动的测试模式界面](assets/read-segment-test-mode.png)

像往常一样配置和运行测试模式。 [了解如何测试历程](testing-the-journey.md)。

测试运行后，**[!UICONTROL 显示日志]**&#x200B;按钮允许您查看测试结果。 有关详细信息，请参阅[此部分](testing-the-journey.md#viewing_logs)

![显示受众执行结果和配置文件流的测试日志](assets/read-segment-log.png)

测试成功后，即可发布历程（请参阅[发布历程](../building-journeys/publish-journey.md)）。 属于受众的个人将在历程的属性&#x200B;**[!UICONTROL 调度程序]**&#x200B;部分中指定的日期/时间进入历程。

>[!NOTE]
>
>对于基于受众的定期历程，一旦执行了其最后一次发生次数，该历程将自动关闭。 如果未指定结束日期/时间，则必须手动将历程关闭到新入口，才能结束历程。

## 历程中的受众定位

基于受众的历程始终以&#x200B;**读取受众**&#x200B;活动开始，以检索属于[!DNL Adobe Experience Platform]受众的个人。 这些用户档案读取一次或按定期计划读取。

进入历程后，您可以使用&#x200B;**条件**&#x200B;活动对其进行编排：按属性或行为分段、排除部分群体或将分支合并在一起（合并）。 以下各部分描述了每种模式。

**区段**

您可以使用&#x200B;**条件**&#x200B;活动使用条件执行分段。 例如，您可以让VIP人员采用特定的路径，而非VIP人员采用其他路径。

分段可以基于：

* 数据源数据
* 事件上下文是历程数据的一部分，例如：某人是否单击了一小时前收到的消息？
* 例如，日期：人员完成旅程时是否为六月？
* 时间，例如：上午是人员时区吗？
* 一种算法，根据百分比拆分历程中流动的受众，例如：90% - 10%以排除控制组

![将受众分段到VIP和非VIP路径的条件活动](assets/read-segment-audience1.png)

>[!NOTE]
>
>在将“每日”调度程序类型与&#x200B;**[!UICONTROL 读取受众]**&#x200B;活动结合使用时，您可以为历程定义一个等待新受众数据的时间范围。 这可以确保准确定位，并防止批量分段作业延迟导致的问题。 [了解如何计划历程](#schedule)

**排除**

用于分段的相同&#x200B;**条件**&#x200B;活动（请参阅上文）还允许您排除部分群体。 例如，您可以排除VIP人员，方法是：让这些人员流入分支中，并在其后执行结束步骤。

此排除可能紧随受众检索之后、出于群体计数目的或随着多步历程而发生。

使用结束历程![的](assets/read-segment-audience2.png)分支排除分支的路径

**并集**

历程允许您创建N个分支，并在分段后将它们连接在一起。 因此，您可以使两个受众返回同一个体验。

例如，在旅程中的十天中完成其他体验后，VIP和非VIP客户可以返回到同一路径。 合并后，您可以通过执行分段或排除来再次拆分受众。

使用并集进行分段后，![历程路径合并在一起](assets/read-segment-audience3.png)

## 故障排除 {#audience-count-mismatch}

此部分可帮助您解决&#x200B;**受众规模不匹配**（输入的配置文件少于或超过预期数）、已处理&#x200B;**个配置文件**（读取受众警报或没有条目）以及&#x200B;**延迟或缺少条目**（时间和数据传播）。

>[!NOTE]
>
>执行读取受众活动时，系统会生成内部事件（称为`segmentExportJob`事件）以跟踪受众导出操作的生命周期。 这些事件在活动级别进行记录，而不是按个人资料进行记录，并且可供查询以用于监控和故障排除目的。 了解有关[查询读取受众事件](../reports/query-examples.md#read-segment-queries)的详细信息。

**查找您的问题：**

| 症状 | 转到 |
|---------|--------|
| 输入的配置文件少于受众规模（或更多） | [计时和数据传播](#timing-and-data-propagation)，[数据验证和监视](#data-validation-and-monitoring) |
| 读取受众处理了零个配置文件；触发了警报 | [零个配置文件已处理](#zero-profiles-processed) |
| 批次受众的条目延迟或缺失 | [计时和数据传播](#timing-and-data-propagation) |
| 需要验证区段作业状态或命名空间 | [数据验证和监视](#data-validation-and-monitoring) |

### 零个配置文件已处理 {#zero-profiles-processed}

如果&#x200B;**读取受众**&#x200B;活动尚未处理任何配置文件（例如，您看到了[读取受众警报](../reports/alerts.md#alert-read-audiences)）：

1. **检查受众是否为空** — 在[!DNL Adobe Experience Platform]中，验证受众大小以及配置文件是否处于&#x200B;**已实现**&#x200B;状态。 如果受众为空或未评估，则不会生成任何条目。
2. **检查命名空间** — 在读取受众活动中选择的命名空间必须存在于受众的用户档案中。 没有该身份的用户档案无法进入历程。 [了解有关命名空间的更多信息](../event/about-creating.md#select-the-namespace)。
3. **查看警报和重试** - **警报**&#x200B;中报告失败。 系统每10分钟重试一次导出作业创建，最长可为1小时。 [了解有关重试和警报的详细信息](#read-audience-retry)。

如果在这些检查后问题仍然存在，请参阅[计时和数据传播](#timing-and-data-propagation)和[数据验证和监视](#data-validation-and-monitoring)以了解批处理原因和配置原因。

### 定时和数据传播 {#timing-and-data-propagation}

* **批处理分段作业完成**：对于批处理受众，请确保在历程运行之前已完成每日批处理分段作业并更新快照。 分段作业完成后约&#x200B;**2小时**&#x200B;批次受众即可使用。 了解有关[受众评估方法](https://experienceleague.adobe.com/docs/experience-platform/segmentation/home.html?lang=zh-Hans#evaluate-segments){target="_blank"}的更多信息。

* **数据摄取时间**：验证在历程执行之前配置文件数据摄取是否已完全完成。 如果在历程开始前不久摄取了用户档案，则这些用户档案可能尚未反映在受众中。 了解有关[&#x200B; [!DNL Adobe Experience Platform]中](https://experienceleague.adobe.com/docs/experience-platform/ingestion/home.html?lang=zh-Hans){target="_blank"}数据摄取的更多信息。

* **使用“批次受众评估后触发”选项**：对于使用批次受众的每日计划历程，请考虑启用&#x200B;**[!UICONTROL 批次受众评估后触发]**&#x200B;选项。 这可确保历程在执行之前等待新的受众数据（最多6个小时）。 [了解有关计划的更多信息](#schedule)

* **添加等待活动**：对于包含最近摄取的数据的流受众，请考虑在历程开始时添加&#x200B;**等待**&#x200B;活动，以便有时间进行数据传播和配置文件鉴别。 [了解有关等待活动的更多信息](wait-activity.md)

### 数据验证 {#data-validation-and-monitoring}

* **检查分段作业状态**：在[!DNL Adobe Experience Platform] [监视仪表板](https://experienceleague.adobe.com/docs/experience-platform/dataflows/ui/monitor-segments.html?lang=zh-Hans){target="_blank"}中监视批处理分段作业完成时间。 使用它来验证受众数据何时准备就绪。

* **验证合并策略**：确保为受众配置的合并策略与组合来自不同源的配置文件数据的预期行为相匹配。 了解有关[&#x200B; [!DNL Adobe Experience Platform]中](https://experienceleague.adobe.com/docs/experience-platform/profile/merge-policies/overview.html?lang=zh-Hans){target="_blank"}合并策略的更多信息。

* **查看区段定义**：确认区段定义配置正确并包括所有预期的资格条件。 了解有关[构建受众](../audience/creating-a-segment-definition.md)的更多信息。 请特别注意：
   * 可能根据事件时间戳排除用户档案的基于时间的条件
   * 取决于最近更新数据的属性资格
   * 流式评估方法与批量评估方法

* **验证命名空间配置**：确保&#x200B;**读取受众**&#x200B;活动中选择的命名空间与受众中配置文件使用的主要标识匹配。 没有选定命名空间的配置文件将不会进入历程。 了解有关[身份命名空间](../event/about-creating.md#select-the-namespace)的更多信息。

### 最佳实践

* **在分段后安排历程**：对于批处理受众，安排历程在典型的批处理分段作业完成时间后至少2-3小时执行。 [了解有关历程计划的更多信息](#schedule)

* **将流式受众用于实时用例**：如果您需要即时配置文件资格和历程条目，请使用具有流式受众的[受众资格](audience-qualification-events.md)活动，而不是&#x200B;**具有批处理受众的“读取受众”**。

* **首先使用较小的受众进行测试**：在启动大规模历程之前，请使用较小的子集进行测试，以验证计数是否与预期相符。 [了解如何测试历程](testing-the-journey.md)

* **定期监控**：设置定期监控受众大小和历程进入量度，以尽早检测到差异。 了解有关[历程处理率和条目管理](entry-management.md)的更多信息。

### 何时联系支持人员

如果在执行上述步骤后，计数不匹配或零配置文件运行仍然存在，请与Adobe支持部门联系。 准备就绪：受众名称/ID、历程名称/ID、计划运行时间、沙盒和差异的简短描述（例如“受众展示已实现10,000项，只有2,000项在[日期]进入历程”）。

## 重试 {#read-audience-retry}

在检索导出作业时，重试操作会被默认应用于受众触发的历程（从&#x200B;**读取受众**&#x200B;或&#x200B;**业务事件**&#x200B;开始）。如果在创建导出作业期间发生错误，则每 10 分钟重试一次，最多 1 小时。之后，我们将它视为失败。因此，这些类型的历程可以在预定时间之后 1 小时内执行。

捕获了失败的&#x200B;**读取受众**&#x200B;触发器并显示在&#x200B;**警报**&#x200B;中。 如果&#x200B;**读取受众**&#x200B;活动在计划执行时间10分钟后未处理任何配置文件，则&#x200B;**读取受众警报**&#x200B;会警告您。 此故障可能由技术问题或空受众导致。 如果失败是由技术问题引起的，则根据问题类型，重试仍可能发生。 例如，如果导出作业创建失败，我们每10分钟重试一次，最长为1小时。 [了解详情](../reports/alerts.md#alert-read-audiences)

## 相关主题

* [生成受众](../audience/about-audiences.md)
* [受众资格筛选活动](audience-qualification-events.md)
* [在历程中使用补充标识符](supplemental-identifier.md)
* [历程属性和护栏](../start/guardrails.md#read-segment-g)
* [历程处理率和登入管理](entry-management.md)
* [测试历程](testing-the-journey.md)
* [发布历程](../building-journeys/publish-journey.md)

## 操作方法视频 {#video}

了解由读取受众活动触发的历程的适用用例。了解如何构建基于批次的历程以及可以应用的最佳实践。

>[!VIDEO](https://video.tv.adobe.com/v/3430362?captions=chi_hans&quality=12)
