---
solution: Journey Optimizer
product: journey optimizer
title: 配置文件条目管理
description: 了解如何管理配置文件输入
feature: Journeys
role: User
level: Intermediate
keywords: 重新进入、历程、个人资料、定期
exl-id: 8874377c-6594-4a5a-9197-ba5b28258c02
source-git-commit: 35f52afe61bf3eda897cc96f5484778522e38d45
workflow-type: tm+mt
source-wordcount: '620'
ht-degree: 13%

---


# 配置文件条目管理 {#entry-management}

历程有两种主要类型：

* 基于事件的历程：从事件开始，这些历程是单一的，它们与一个个人相关联。 收到事件后，个人进入旅程。 [了解详情](#entry-unitary)
* 读取受众历程：从读取受众开始，这些是批量历程。 属于受众的个人都会进入同一历程。 这些历程可以是循环或一次性历程。 [了解详情](#entry-read-segment)

在这两种历程类型中，无法在同一历程中同时存在多个用户档案。

## 单一历程{#entry-unitary}

在单一历程中，您可以启用或禁用重新进入：

* 如果启用了重新进入，则用户档案可以多次进入历程，但只有在完全退出该历程的上一个实例后才能进入历程。

* 如果禁用重新进入，则用户档案无法多次进入同一历程。

默认情况下，新历程允许重新进入。 您可以取消选中“一次性”旅程选项，例如，当您想要在某人访问商店时提供一次性礼品时。 在这种情况下，客户必须无法重新进入历程并再次收到选件。 历程结束时，其状态为 **[!UICONTROL 已关闭]**. 新个人无法再进入历程。 已在历程中的人员正常完成历程。 [了解详情](journey-gs.md#entrance)

![](assets/journey-re-entrance.png)

默认设置之后 [全局超时](journey-gs.md#global_timeout) 在30天内，历程将切换到 **已完成** 状态。 历程中已有的用户档案通常会完成历程。 新配置文件无法再进入历程。 此行为仅设置为30天（即历程超时默认值），因为有关进入历程的用户档案的所有信息在进入30天后会被删除。 在该时段后，用户档案可以重新进入历程。 要避免此情况，并完全禁止这些用户档案的重新进入，您可以使用用户档案或受众数据，添加条件以测试是否已经输入用户档案。

<!--
Due to the 30-day journey timeout, when journey re-entrance is not allowed, we cannot make sure the re-entrance blocking will work more than 30 days. Indeed, as we remove all information about persons who entered the journey 30 days after they enter, we cannot know the person entered previously, more than 30 days ago. -->

单一历程（以事件或受众鉴别开始）包含护栏，可防止同一事件多次错误触发历程。默认情况下，重新访问用户档案会被暂时阻止 5 分钟。例如，如果某个事件在 12:01 触发某个特定用户档案的历程，而另一个事件在 12:03 到达（无论是同一事件还是其他事件触发同一历程），则对于此用户档案，该历程将不会重新开始。

密钥还用于检查人员是否正在旅程中。 事实上，一个人在同一历程中不能位于两个不同的位置。 因此，系统不允许相同的键（例如键CRMID=3224）位于同一历程的不同位置。

## 读取受众历程{#entry-read-segment}

在读取受众历程中：

* 对于非循环历程：用户档案在历程中只输入一次。

* 对于定期历程：默认情况下，属于受众的所有用户档案在每次定期时进入历程。 必须先完成历程，然后才能在另一个事件中再次进入。

>[!NOTE]
>
>有两个选项可用于定期读取受众历程。 此 **在重复时强制重入** 选项允许历程中仍存在的所有用户档案在下次执行时自动退出该历程。 此 **增量读取** 选项仅定向自上次执行历程以来进入受众的个人。 请参阅此 [部分](../building-journeys/read-audience.md#configuring-segment-trigger-activity)

在商业事件历程中，以 **读取受众** 活动：了解此历程基于业务事件接收情况，如果配置文件符合预期受众中的条件，他们将进入收到的每个业务事件的历程，这意味着此配置文件可以在同一历程中同时多次出现，但位于不同的业务事件上下文中。