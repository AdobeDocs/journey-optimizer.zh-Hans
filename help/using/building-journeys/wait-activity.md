---
solution: Journey Optimizer
product: journey optimizer
title: 等待活动
description: 了解等待活动
feature: Journeys, Activities
topic: Content Management
role: User
level: Intermediate
keywords: 等待，活动，历程，下一个，画布
exl-id: 7268489a-38c1-44da-b043-f57aaa12d7d5
source-git-commit: cb1fed2460ddbf3b226fe191b9695008970937c1
workflow-type: tm+mt
source-wordcount: '489'
ht-degree: 17%

---

# 等待活动{#wait-activity}

>[!CONTEXTUALHELP]
>id="ajo_journey_wait"
>title="等待活动"
>abstract="如果您想在执行路径中的下一个活动之前等待，可以使用等待活动。这让您可以定义执行下一个活动的时刻。有两个选项可用：持续时间和自定义。"

如果您希望在执行路径中的下一个活动之前等待，则可以使用 **[!UICONTROL 等待]** 活动。 这让您可以定义执行下一个活动的时刻。可以使用以下选项：

* [持续时间](#duration)
* [自定义](#custom)

<!--
* [Email send time optimization](#email_send_time_optimization)
* [Fixed date](#fixed_date) 
-->

## 关于等待活动{#about_wait}

最长等待时间为29天。 在测试模式下， **[!UICONTROL 测试中的等待时间]** 参数允许您定义每个等待活动的持续时间。 默认时间为 10 秒。这将确保您快速获得测试结果。 请参阅[此页](../building-journeys/testing-the-journey.md)。

当在历程中使用多个等待活动时，请务必谨慎，因为全局历程超时为30天，这意味着用户档案在进入历程后，将始终退出历程的最长30天。 请参阅[此页](../building-journeys/journey-gs.md#global_timeout)。

仅当个人在历程中剩余的时间足以在30天历程超时前完成等待持续时间时，他或她才能进入等待活动。 例如，如果添加两个分别设置为20天的等待活动，则系统将检测到第二个等待将在30天超时后结束。 因此，第二次等待将被忽略，个人将在启动历程之前退出历程。 在该示例中，客户在历程中将总共保留20天。

最佳做法是不使用等待来阻止重新进入。 请改用 **允许重新进入** 历程属性级别的选项。 请参阅[此页](../building-journeys/journey-gs.md#entrance)。

## 持续时间等待{#duration}

选择下一个活动执行前等待的持续时间。 最长持续时间为29天。

![](assets/journey55.png)

<!--
## Fixed date wait{#fixed_date}

Select the date for the execution of the next activity.

![](assets/journey56.png)

-->

## 自定义等待{#custom}

此选项允许您使用基于来自事件或数据源的字段的高级表达式来定义自定义日期，例如2020年7月12日下午5点。 它不允许您定义自定义持续时间，例如7天。 表达式编辑器中的表达式应提供dateTimeOnly格式。 请参阅此 [页面](expression/expressionadvanced.md). 有关dateTimeOnly格式的详细信息，请参阅此 [页面](expression/data-types.md).

>[!NOTE]
>
>您可以利用dateTimeOnly表达式或使用函数转换为dateTimeOnly。 例如： toDateTimeOnly(@event{Event.offerOpened.activity.endTime})，事件中的字段格式为2016-08-12T09:46:06Z。
>
>此 **时区** 应在历程的属性中找到。 因此，目前不可能从界面直接指向完整的ISO-8601时间戳混合时间和时区偏移，如2016-08-12T09:46:06.982-05. 请参阅[此页](../building-journeys/timezone-management.md)。

![](assets/journey57.png)

要验证等待活动是否按预期运行，您可以使用步骤事件。 请参阅[此页](../reports/query-examples.md#common-queries)。

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
