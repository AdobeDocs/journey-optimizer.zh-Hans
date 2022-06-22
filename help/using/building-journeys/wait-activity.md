---
title: 等待活动
description: 了解等待活动
feature: Journeys
topic: Content Management
role: User
level: Intermediate
exl-id: 7268489a-38c1-44da-b043-f57aaa12d7d5
source-git-commit: 8a68d1e6d498ef3055c703d4e73471ab6d7bff40
workflow-type: tm+mt
source-wordcount: '339'
ht-degree: 4%

---

# 等待活动{#wait-activity}

>[!CONTEXTUALHELP]
>id="ajo_journey_wait"
>title="等待活动"
>abstract="如果要在执行路径中的下一个活动之前等待，可以使用等待活动。 利用该活动，可定义执行下一个活动的时间。 提供了以下三个选项：持续时间、固定日期和自定义。"

如果要在路径中执行下一个活动之前等待，可以使用 **[!UICONTROL Wait]** 活动。 利用该活动，可定义执行下一个活动的时间。 提供了以下三个选项：

* [持续时间](#duration)
* [固定日期](#fixed_date)
* [自定义](#custom)

<!--* [Email send time optimization](#email_send_time_optimization)-->

## 关于等待活动{#about_wait}

最长等待时长为30天。 在测试模式下， **[!UICONTROL Wait time in test]** 参数允许您定义每个等待活动的持续时间。 默认时间为 10 秒。这样可以确保快速获得测试结果。 请参阅 [本页](../building-journeys/testing-the-journey.md)

在历程中使用多个等待活动时要谨慎，因为全局历程超时为30天，这意味着用户档案将始终在其进入历程后30天内从历程中删除。

## 持续等待{#duration}

选择在执行下一个活动之前等待的持续时间。

![](assets/journey55.png)

## 修复了日期等待{#fixed_date}

选择执行下一个活动的日期。

![](assets/journey56.png)

## 自定义等待{#custom}

利用此选项，可使用基于来自事件或数据源的字段的高级表达式，定义自定义日期，例如2020年7月12日下午5点。 它不允许您定义自定义持续时间，例如7天。 表达式编辑器中的表达式应提供dateTimeOnly格式。 请参阅 [页面](expression/expressionadvanced.md). 有关dateTimeOnly格式的详细信息，请参阅此 [页面](expression/data-types.md).

>[!NOTE]
>
>您可以使用dateTimeOnly表达式或使用函数转换为dateTimeOnly。 例如：toDateTimeOnly(@{Event.offerOpened.activity.endTime})，事件中的字段为2016-08-12T09格式:46:06Z。
>
>的 **时区** 在历程的属性中是预期的。 因此，今天从界面无法直接指向完全ISO-8601时间戳混合时间和时区偏移，如2016-08-12T09:46:06.982-05。 请参阅[此页](../building-journeys/timezone-management.md)。

![](assets/journey57.png)

<!--## Email send time optimization{#email_send_time_optimization}

This type of wait uses a score calculated in Adobe Experience Platform. The score calculates the propensity to click or open an email in the future based on past behavior. Note that the algorithm calculating the score needs a certain amount of data to work. As a result, when it does not have enough data, the default wait time will apply. At publication time, you’ll be notified that the default time applies.

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
