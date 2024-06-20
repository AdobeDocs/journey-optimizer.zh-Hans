---
solution: Journey Optimizer
product: journey optimizer
title: 配置文件条目管理
description: 了解如何管理配置文件输入
feature: Journeys, Profiles
role: User
level: Intermediate
keywords: 重新进入、历程、个人资料、定期
exl-id: 8874377c-6594-4a5a-9197-ba5b28258c02
source-git-commit: fec6b15db9f8e6b2a07b55bc9e8fc4d9cb0d73d7
workflow-type: tm+mt
source-wordcount: '682'
ht-degree: 5%

---


# 用户档案入口管理 {#entry-management}

历程分为四种类型：

* **单一事件** 历程：这些历程从单一事件开始。 收到事件后，关联的配置文件将进入旅程。 [了解详情](#entry-unitary)

* **业务事件** 历程：这些历程以业务事件开始，随后是读取受众。 收到事件后，属于目标受众的用户档案将进入历程。 将为每个用户档案创建一个此历程的实例。 [了解详情](#entry-business)

* **读取受众** 历程：这些历程以读取受众开始。 执行历程时，属于目标受众的用户档案进入历程。 将为每个用户档案创建一个此历程的实例。 这些历程可以是循环或一次性历程。 [了解详情](#entry-read-audience)

* **受众资格** 历程：这些历程以受众资格事件开始。 这些历程侦听受众中用户档案的进出口。 发生此情况时，关联的配置文件将进入旅程。 [了解详情](#entry-unitary)

在所有历程类型中，同一历程中无法同时存在多个用户档案。 要检查人员是否在历程中，会将用户档案身份用作密钥。 系统不允许将相同的键（例如键CRMID=3224）放置在同一历程的不同位置。

## 单一事件和受众资格历程{#entry-unitary}

在单一事件和受众资格历程中，您可以启用或禁用重新进入：

* 如果启用了重新进入，则用户档案可以多次进入历程，但只有在完全退出历程的上一个实例后才能进入历程。

* 如果禁用重新进入，则用户档案无法在全局历程超时时间内多次进入同一历程。 请参阅此[部分](../building-journeys/journey-properties.md#global_timeout)。

默认情况下，历程允许重新进入。 当 **允许重新进入** 选项已激活， **重新进入等待期** 字段。 它允许您定义允许用户档案再次进入历程之前的等待时间。 这可防止同一事件多次错误触发历程。默认情况下，字段设置为 5 分钟。最长持续时间为91天([全局超时](journey-properties.md#global_timeout))。

<!--
When a journey ends, its status is **[!UICONTROL Closed]**. New individuals can no longer enter the journey. Persons already in the journey automatically exit the journey. 
-->

![](assets/journey-re-entrance.png)

在重新进入期后，用户档案可以重新进入历程。 要避免此情况，并完全禁止这些用户档案的重新进入，您可以使用用户档案或受众数据，添加条件以测试是否已经输入用户档案。

<!--
Due to the 30-day journey timeout, when journey re-entrance is not allowed, we cannot make sure the re-entrance blocking will work more than 91 days. Indeed, as we remove all information about persons who entered the journey 91 days after they enter, we cannot know the person entered previously, more than 91 days ago. -->

## 业务历程{#entry-business}

<!--
Business events follow re-entrance rules in the same way as for unitary events. If a journey allows re-entrance, the next business event will be processed.
-->

要允许多个业务事件执行，请在 **[!UICONTROL 执行]** 旅程属性的部分。

![](assets/business-entry.png)

对于业务事件，对于给定历程，在1小时时间范围内重用首次执行时检索到的受众数据。

同一历程中可以同时存在多个用户档案，但不同业务事件的上下文中可能出现多个用户档案。

有关更多信息，请参阅此 [部分](../event/about-creating-business.md)

## 读取受众历程{#entry-read-audience}

读取受众历程可以是循环或一次性历程：

* 对于非循环历程：用户档案在历程中只输入一次。

* 对于定期历程：默认情况下，属于受众的所有用户档案都会在每次定期时进入历程。 必须先完成历程，然后才能在另一个事件中再次进入。

有两个选项可用于定期读取受众历程：

* **增量读取** 选项：当具有循环的历程时 **读取受众** 首次执行时，受众中的所有用户档案都会进入历程。 利用此选项，可在首次发生后仅定向自上次执行历程以来进入受众的个人。

  >[!NOTE]
  >
  >如果您要定位 [自定义上传受众](../audience/about-audiences.md#segments-in-journey-optimizer) 在您的历程中，仅当在定期历程中启用此选项时，才会在第一次重复时检索用户档案，因为这些受众是固定的。

* **在重复时强制重入**：利用此选项可让历程中仍存在的所有用户档案在下次执行时自动退出历程。 如果配置文件在此历程中的生命周期可能长于重复频率（例如，如果您使用等待活动），请勿激活此选项以确保配置文件可以完成其历程。

![](assets/read-audience-options.png)

有关更多信息，请参阅此 [部分](../building-journeys/read-audience.md#configuring-segment-trigger-activity)

<!--
After 91 days, a Read audience journey switches to the **Finished** status. This behavior is set for 91 days only (i.e. journey timeout default value) as all information about profiles who entered the journey is removed 91 days after they entered. Persons still in the journey automatically are impacted. They exit the journey after the 30 day timeout. 
-->
