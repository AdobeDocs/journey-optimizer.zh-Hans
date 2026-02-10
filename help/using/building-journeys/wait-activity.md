---
solution: Journey Optimizer
product: journey optimizer
title: 等待活动
description: 了解如何配置等待活动
feature: Journeys, Activities
topic: Content Management
role: User
level: Intermediate
keywords: 等待，活动，历程，下一个，画布
exl-id: 7268489a-38c1-44da-b043-f57aaa12d7d5
version: Journey Orchestration
source-git-commit: 70653bafbbe8f1ece409e3005256d9dff035b518
workflow-type: tm+mt
source-wordcount: '906'
ht-degree: 12%

---

# 等待活动 {#wait-activity}

>[!CONTEXTUALHELP]
>id="ajo_journey_wait"
>title="等待活动"
>abstract="如果您想在执行路径中的下一个活动之前等待，可以使用等待活动。这让您可以定义执行下一个活动的时刻。有两个选项可用：持续时间和自定义。"

您可以使用&#x200B;**[!UICONTROL 等待]**&#x200B;活动定义持续时间，然后再执行下一个活动。  最长等待时间为&#x200B;**90天**。

您可以设置两种类型的&#x200B;**等待**&#x200B;活动：

* 基于相对持续时间的等待。 [了解详情](#duration)
* 自定义日期，使用函数进行计算。 [了解详情](#custom)

<!--
* [Email send time optimization](#email_send_time_optimization)
* [Fixed date](#fixed_date) 
-->

## 推荐做法 {#wait-recommendations}

使用这些建议可保持等待的可预测性和安全性。

### 多个等待活动 {#multiple-wait-activities}

在历程中使用多个&#x200B;**等待**&#x200B;活动时，请注意，历程的[全局超时](journey-properties.md#global_timeout)为91天，这意味着用户档案始终在进入历程后91天内退出该历程。 请参阅[此页面](journey-properties.md#global_timeout)以了解详情。

仅当个人在历程中剩余的时间足以在91天历程超时之前完成等待持续时间时，个人才能进入&#x200B;**等待**&#x200B;活动。

### 等待并重新进入 {#wait-reentrance}

不使用&#x200B;**等待**&#x200B;活动阻止重新进入的最佳实践。 请改用历程属性级别的&#x200B;**允许重入**&#x200B;选项。 请参阅[此页面](../building-journeys/journey-properties.md#entrance)以了解详情。

### 等待和测试模式 {#wait-test-mode}

在测试模式下，**[!UICONTROL 测试中的等待时间]**&#x200B;参数允许您定义每个&#x200B;**等待**&#x200B;活动的持续时间。 默认时间为 10 秒。这将确保您快速获得测试结果。 请参阅[此页面](../building-journeys/testing-the-journey.md)以了解详情。

### 等待和移动渠道 {#wait-mobile-channels}

如果要在发送[推送通知](../in-app/create-in-app.md)后不久显示[应用程序内消息](../../rp_landing_pages/push-landing-page.md)，请使用&#x200B;**等待**&#x200B;活动以允许传播应用程序内消息有效负荷时间。 通常建议等待5-15分钟，但具体时间会因有效负载复杂性和个性化需求而异。

## 配置 {#wait-configuration}

在此处配置等待时长和计时。

### 持续时间等待 {#duration}

选择&#x200B;**持续时间**&#x200B;类型以设置下一个活动执行前等待的相对持续时间。 最长持续时间为&#x200B;**90天**。

![定义等待持续时间](assets/journey55.png)

<!--
## Fixed date wait{#fixed_date}

Select the date for the execution of the next activity.

![Wait activity configuration panel with duration and fixed date options](assets/journey56.png)

-->

### 自定义等待 {#custom}

选择&#x200B;**自定义**&#x200B;类型以使用基于来自事件或自定义操作响应的字段的高级表达式来定义自定义日期。 您不能直接定义相对持续时间，例如7天，但您可以根据需要使用函数计算相对持续时间（例如：购买后2天）。

![使用表达式定义自定义等待](assets/journey57.png)

编辑器中的表达式应提供`dateTimeOnly`格式。 请参见[此页面](expression/expressionadvanced.md)。有关dateTimeOnly格式的详细信息，请参阅[此页面](expression/data-types.md)。

最佳实践是使用特定于您用户档案的自定义日期，并避免对所有用户使用相同的日期。 例如，不要定义`toDateTimeOnly('2024-01-01T01:11:00Z')`，而是要定义特定于每个配置文件的`toDateTimeOnly(@event{Event.productDeliveryDate})`。 请注意，使用固定日期可能会导致历程执行出现问题。 在[本节](entry-management.md#wait-activities-impact)中进一步了解等待活动对历程处理率的影响。


>[!NOTE]
>
>您可以利用`dateTimeOnly`表达式或使用函数转换为`dateTimeOnly`。 例如： `toDateTimeOnly(@event{Event.offerOpened.activity.endTime})`，事件中的字段格式为2023-08-12T09:46:06Z。
>
>历程的属性中应为&#x200B;**时区**。 因此，从用户界面中，无法直接指向混合时间和时区偏移的完整ISO-8601时间戳点，如2023-08-12T09:46:06.982-05。 [了解详情](../building-journeys/timezone-management.md)。

>[!CAUTION]
>
>创建具有`toDateTimeOnly()`的自定义等待表达式时，请避免在表达式结果中附加“Z”或任何时区偏移（例如，“–05:00”）。 表达式必须使用引用历程配置的时区的有效ISO日期/时间语法，且不含明确的时区指示符。
>
>**正确的示例：** `toDateTimeOnly(concat(toString(toDateOnly(nowWithDelta(2, "days"))),"T10:00:00"))`
>
>**不正确的示例：** `toDateTimeOnly(concat(toString(toDateOnly(nowWithDelta(2, "days"))),"T10:00:00Z"))` ❌ （包含“Z”）
>
>使用不受支持的时区指示符可能会导致配置文件在等待活动中持续卡住，而不是按预期前进。

要验证等待活动是否按预期运行，您可以使用步骤事件。 [了解详情](../reports/query-examples.md#common-queries)。

## 等待后配置文件刷新 {#profile-refresh}

当配置文件驻留在以&#x200B;**读取受众**&#x200B;活动开始的历程中的&#x200B;**等待**&#x200B;活动时，该历程会自动从统一配置文件服务(UPS)中刷新配置文件的属性，以获取最新可用数据。

* **在历程条目**：配置文件使用历程启动时计算的受众快照中的属性值。
* **在等待节点之后**：历程执行查找以从UPS检索最新的配置文件数据，而不是旧的快照数据。 这意味着自历程开始以来，配置文件属性可能已更改。

此行为可确保下游活动在等待时段后使用当前配置文件信息。 但是，如果您希望历程在整个执行过程中仅使用原始快照数据，则可能会产生意外结果。

示例：如果配置文件在历程开始时符合“银级客户”受众的条件，但在3天等待期间升级到“金级客户”，则等待后的活动将看到更新的“金级客户”状态。

## 自动等待节点  {#auto-wait-node}

>[!CONTEXTUALHELP]
>id="ajo_journey_auto_wait_node "
>title="关于自动等待节点"
>abstract="此活动后会自动添加一个&#x200B;**等待**&#x200B;活动。其设置为 3 天。您可以根据需要移除它或者对其进行配置。"

每个入站体验活动（应用程序内消息、基于代码的体验或卡片）都包含3天&#x200B;**等待**&#x200B;活动。 当用户档案到达历程终点时，入站消息会自动结束，因此我们假定您希望用户至少在3天内看到该消息。 您可以删除此&#x200B;**等待**&#x200B;活动，或者根据需要更改其配置。
