---
solution: Journey Optimizer
product: journey optimizer
title: 配置文件条目管理
description: 了解如何管理用户档案条目
feature: Journeys
role: User
level: Intermediate
keywords: 重新进入、历程、个人资料、定期
exl-id: 8874377c-6594-4a5a-9197-ba5b28258c02
source-git-commit: 1cf62f949c1309b864ccd352059a444fd7bd07f0
workflow-type: tm+mt
source-wordcount: '350'
ht-degree: 22%

---


# 配置文件条目管理 {#entry-management}

默认情况下，新历程允许重新进入。 您可以取消选中“一次性”旅程的选项，例如，如果您希望在人员进入商店时提供一次性礼品。 在这种情况下，您不希望客户能够重新进入历程并再次收到选件。

![](assets/journey-re-entrance.png)

历程结束时，其状态为 **[!UICONTROL 已关闭]**. 新个人再也无法进入旅程。 已在旅程中的人员正常完成旅程。

默认全局超时30天后，历程将切换到 **已完成** 状态。  [了解详情](journey-gs.md#global_timeout)。


## 单一历程{#entry-unitary}

单一历程（以事件或区段资格开始）包含护栏，可防止同一事件多次错误触发历程。默认情况下，重新访问用户档案会被暂时阻止 5 分钟。例如，如果某个事件在 12:01 触发某个特定用户档案的历程，而另一个事件在 12:03 到达（无论是同一事件还是其他事件触发同一历程），则对于此用户档案，该历程将不会重新开始。

此外：

* 如果启用了重新进入，则用户档案可以多次进入历程，但在完全退出该历程的上一个实例之前无法执行此操作。

* 如果禁用了重新进入，则用户档案无法多次进入同一历程

## 读取区段历程{#entry-read-segment}

在读取区段历程中：

* 对于非循环历程：用户档案只进入历程一次。

* 对于周期性历程：如果个人资料处于区段/预期状态，则个人资料会在每次周期性时进入历程。 如果他们仍然处于上一个重复事件的历程中，则将从头开始重新开始该历程。

在商业事件历程中，从 **读取区段** 活动：了解此历程基于对业务事件的接收，如果配置文件在预期区段中符合条件，他们将进入收到的每个业务事件的历程，这意味着此配置文件可以在同一历程中同时进行多次，但是在不同的业务事件背景下进行。

<!--
# Profile entry management {#entry-management}

There are two main types of journeys:

* event-based journeys: starting with an event, these journeys are unitary, they are associated to one individual. When the event is received, the individual enters the journey. [Read more](#entry-unitary)
* read segment journeys: starting with a read segment, these are batch journeys. Individuals belonging to the segment all enter the same journey. These journeys can be recurring or one-shot. [Read more](#entry-read-segment)

In both journey types, a profile cannot be present multiple times in the same journey, at the same time.


## Unitary journeys{#entry-unitary}

In unitary journeys, you can enable or disable re-entrance:

* If re-entrance is enabled, a profile can enter a journey several times, but cannot do it until he fully exited that previous instance of the journey.

* If re-entrance is disabled, a profile cannot enter multiple times the same journey

By default, new journeys allow re-entrance. You can uncheck the option for “one shot” journeys, for example if you want to offer a one-time gift when a person enters a shop. In that case, you don't want the customer to be able to re-enter the journey and receive the offer again. When a journey ends, its status is **[!UICONTROL Closed]**. New individuals can no longer enter the journey. Persons already in the journey finish the journey normally. [Learn more](journey-gs.md#entrance)

![](assets/journey-re-entrance.png)

After the default global timeout of 30 days, the journey switches to the **Finished** status. New individuals can no longer enter the journey. Persons already in the journey finish the journey normally.Due to the 30-day journey timeout, when journey re-entrance is not allowed, we cannot make sure the re-entrance blocking will work more than 30 days. Indeed, as we remove all information about persons who entered the journey 30 days after they enter, we cannot know the person entered previously, more than 30 days ago. [Learn more](journey-gs.md#global_timeout).

Unitary journeys (starting with an event or a segment qualification) include a guardrail that prevents journeys from being erroneously triggered multiple times for the same event. Profile re-entrance is temporally blocked by default for 5 minutes. For instance, if an event triggers a journey at 12:01 for a specific profile and another one arrives at 12:03 (whether it is the same event or a different one triggering the same journey) that journey will not start again for this profile.

The key is also used to check that a person is in a journey. Indeed, a person cannot be at two different places in the same journey. As a result, the system does not allow the same key, for example the key CRMID=3224, to be at different places in the same journey.

## Read segment journeys{#entry-read-segment}

In a read segment journey:

* For non-recurring journeys: the profile enters once and only once the journey.

* For recurring journeys: by default, all the profiles belonging to the segment enters the journey on each recurrence. They must finish the journey before they can reenter in another occurrence. 

>[!NOTE]
>
>Two options are available for recurring read segment journeys. The **Force reentrance on recurrence** option makes all the profiles still present in the journey automatically exit it on the next execution. The **Incremental read** option only targets the individuals who entered the segment since the last execution of the journey. Refer to this [section](../building-journeys/read-segment.md#configuring-segment-trigger-activity)

In business event journeys starting with a **Read segment** activity: knowing that this journey is based on the reception of a business event, if the profile is qualified in the expected segment, they will enter the journey for each business event received, meaning that this profile can be multiple times in the same journey, at the same time, but in the context of different business events.
-->