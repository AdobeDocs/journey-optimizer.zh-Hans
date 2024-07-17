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
source-git-commit: cae6d394ad1c2356e55bd5f1cb4ad7494c9623dd
workflow-type: tm+mt
source-wordcount: '508'
ht-degree: 15%

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

### 多个等待活动 {#multiple-wait-activities}

在历程中使用多个&#x200B;**等待**&#x200B;活动时，请注意，历程的[全局超时](journey-properties.md#global_timeout)为91天，这意味着用户档案始终在进入历程后91天内退出该历程。 请参阅[此页面](journey-properties.md#global_timeout)以了解详情。

仅当个人在历程中剩余的时间足以在91天历程超时之前完成等待持续时间时，个人才能进入&#x200B;**等待**&#x200B;活动。

### 等待并重新进入 {#wait-re-entrance}

不使用&#x200B;**等待**&#x200B;活动阻止重新进入的最佳实践。 请改用历程属性级别的&#x200B;**允许重新进入**&#x200B;选项。 请参阅[此页面](../building-journeys/journey-properties.md#entrance)以了解详情。

### 等待和测试模式 {#wait-test-modd}

在测试模式下，**[!UICONTROL 测试中的等待时间]**&#x200B;参数允许您定义每个&#x200B;**等待**&#x200B;活动的持续时间。 默认时间为 10 秒。这将确保您快速获得测试结果。 请参阅[此页面](../building-journeys/testing-the-journey.md)以了解详情。

## 配置 {#wait-configuration}

### 持续时间等待 {#duration}

选择&#x200B;**持续时间**&#x200B;类型以设置下一个活动执行前等待的相对持续时间。 最长持续时间为&#x200B;**90天**。

![定义等待持续时间](assets/journey55.png)

<!--
## Fixed date wait{#fixed_date}

Select the date for the execution of the next activity.

![](assets/journey56.png)

-->

### 自定义等待 {#custom}

选择&#x200B;**自定义**&#x200B;类型以使用基于来自事件或自定义操作响应的字段的高级表达式来定义自定义日期。 您不能直接定义相对持续时间，例如7天，但您可以根据需要使用函数计算相对持续时间（例如：购买后2天）。

![使用表达式定义自定义等待](assets/journey57.png)

编辑器中的表达式应提供`dateTimeOnly`格式。 请参见[此页面](expression/expressionadvanced.md)。有关dateTimeOnly格式的详细信息，请参阅[此页面](expression/data-types.md)。

最佳实践是使用特定于您用户档案的自定义日期，并避免对所有用户使用相同的日期。 例如，不要定义`toDateTimeOnly('2024-01-01T01:11:00Z')`，而是要定义特定于每个配置文件的`toDateTimeOnly(@event{Event.productDeliveryDate})`。 请注意，使用固定日期可能会导致历程执行出现问题。


>[!NOTE]
>
>您可以利用`dateTimeOnly`表达式或使用函数转换为`dateTimeOnly`。 例如： `toDateTimeOnly(@event{Event.offerOpened.activity.endTime})`，事件中的字段格式为2023-08-12T09:46:06Z。
>
>历程的属性中应为&#x200B;**时区**。 因此，从用户界面中，无法直接指向混合时间和时区偏移的完整ISO-8601时间戳点，如2023-08-12T09:46:06.982-05。 [了解详情](../building-journeys/timezone-management.md)。


要验证等待活动是否按预期运行，您可以使用步骤事件。 [了解详情](../reports/query-examples.md#common-queries)。

<!--## Email send time optimization{#email_send_time_optimization}

This type of wait uses a score calculated in Adobe Experience Platform. The score calculates the propensity to click or open an email in the future based on past behavior. Note that the algorithm calculating the score needs a certain amount of data to work. As a result, when it does not have enough data, the default wait time will apply. At publication time, you'll be notified that the default time applies.

>[!NOTE]
>
>The first event of your journey must have a namespace.
>
>This capability is only available after an **[!UICONTROL Email]** activity. You need to have Adobe Campaign Standard.

1. In the **[!UICONTROL Amount of time]** field, define the number of hours to consider to optimize email sending.
1. In the **[!UICONTROL Optimization type]** field, choose if the optimization should increase clicks or opens.
1. In the **[!UICONTROL Default time]** field, define the default time to wait if the predictive send time score is not available.

    >[!NOTE]
    >
    >Note that the send time score can be unavailable because there is not enough data to perform the calculation. In this case, you will be informed, at publication time, that the default time applies.

![](assets/journey57bis.png)-->
