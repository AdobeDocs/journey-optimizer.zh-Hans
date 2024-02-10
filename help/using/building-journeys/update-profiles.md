---
solution: Journey Optimizer
product: journey optimizer
title: 更新配置文件
description: 了解如何在历程中使用更新用户档案活动
feature: Journeys, Profiles, Activities
topic: Content Management
role: User
level: Intermediate
keywords: 个人资料，更新，历程，活动
exl-id: 8b2b2d1e-9bd1-439d-a15e-acdbab387c4b
source-git-commit: 9010b173eb5126fff72d71aa582b265cc05fddf0
workflow-type: tm+mt
source-wordcount: '614'
ht-degree: 6%

---

# 更新配置文件 {#update-profile}

>[!CONTEXTUALHELP]
>id="ajo_journey_update_profiles"
>title="更新配置文件活动"
>abstract="更新配置文件操作活动让您可以使用来自事件、数据源的信息或使用特定值，更新现有 Adobe Experience Platform 配置文件。"

使用 **[!UICONTROL 更新配置文件]** 操作活动，使用来自事件、数据源的信息或使用特定值更新现有Adobe Experience Platform用户档案。

## 建议

* 此 **更新配置文件** 操作只能在以具有命名空间的事件开始的历程中使用。
* 该操作仅更新现有字段，不创建新配置文件字段。
* 您不能使用 **更新配置文件** 用于生成体验事件的操作，例如购买。
* 与任何其他操作一样，您可以定义在发生错误或超时时的替代路径，并且不能将两个操作并行放置。
* 发送到Adobe Experience Platform的更新请求是立即的/在一秒内。 通常需要几秒钟的时间，但有时需要更长时间，无法保证。 因此，例如，如果某个操作正在使用由更新的“字段1”， **更新配置文件** 位于之前的操作，您不应预期操作中将更新“字段1”。
* 此 **更新配置文件** 活动不支持定义为枚举的XDM字段。
* 此 **[!UICONTROL 更新配置文件]** 仅活动会更新 [配置文件存储](https://experienceleague.adobe.com/docs/experience-platform/profile/home.html#profile-data-store){target="_blank"}而不是数据湖。
* 在中选择数据集时 **[!UICONTROL 更新配置文件]** 活动，建议使用未被数据摄取流定位的流量。 因为 **更新配置文件** 更新仅存储在 [配置文件存储](https://experienceleague.adobe.com/docs/experience-platform/profile/home.html#profile-data-store){target="_blank"}，则存在使用数据摄取流覆盖此类更改的风险。

  此外， **更新配置文件** 活动配置不需要标识命名空间。 因此，请确保所选数据集使用的身份命名空间与启动历程的操作所使用的命名空间相同，因为这些更新将使用此命名空间。 所选数据集也可以使用身份映射。 如果未能选择具有正确命名空间或使用标识映射的数据集，则会导致 **更新配置文件** 活动失败。



## 使用用户档案更新

1. 从事件开始设计您的旅程。 请参阅此[部分](../building-journeys/journey.md)。

1. 在 **操作** 部分，拖放 **更新配置文件** 活动移入画布。

   ![](assets/profileupdate0.png)

1. 从列表中选择架构。

1. 单击 **字段** 以选择要更新的字段。 只能选择一个字段。

   ![](assets/profileupdate2.png)

1. 从列表中选择数据集。

   >[!NOTE]
   >
   >此 **更新配置文件** 操作可实时更新用户档案数据，但不会更新数据集。 需要选择数据集，因为用户档案是与数据集相关的记录。

1. 单击 **值** 字段以定义要使用的值：

   * 使用简单表达式编辑器，您可以从数据源或传入事件中选择字段。

     ![](assets/profileupdate4.png)

   * 如果要定义特定值或利用高级函数，请单击 **高级模式**.

     ![](assets/profileupdate3.png)

此 **更新配置文件** 现已配置。

![](assets/profileupdate1.png)


## 使用测试模式 {#using-the-test-mode}

在测试模式下，将不会模拟用户档案更新。 将对测试用户档案执行更新。

只有测试配置文件才能进入处于测试模式的历程。 您可以创建新的测试配置文件，或将现有配置文件转换为测试配置文件。 在Adobe Experience Platform中，您可以通过csv文件导入或API调用更新用户档案属性。 更简单的方法是使用 **更新配置文件** 操作活动，并将测试用户档案布尔字段从false更改为true。

有关如何将现有配置文件转换为测试配置文件的更多信息，请参阅此 [部分](../audience/creating-test-profiles.md#create-test-profiles-csv).
