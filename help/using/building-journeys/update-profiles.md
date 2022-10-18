---
solution: Journey Optimizer
product: journey optimizer
title: 更新用户档案
description: 了解如何在历程中使用更新用户档案活动
feature: Journeys
topic: Content Management
role: User
level: Intermediate
exl-id: 8b2b2d1e-9bd1-439d-a15e-acdbab387c4b
source-git-commit: 021cf48ab4b5ea8975135a20d5cef8846faa5991
workflow-type: tm+mt
source-wordcount: '470'
ht-degree: 0%

---

# 更新用户档案 {#update-profile}

>[!CONTEXTUALHELP]
>id="ajo_journey_update_profiles"
>title="更新用户档案活动"
>abstract="利用更新配置文件操作活动，可使用来自事件、数据源或使用特定值的信息来更新现有Adobe Experience Platform配置文件。"

使用 **[!UICONTROL 更新用户档案]** 操作活动，使用来自事件、数据源或具有特定值的信息更新现有Adobe Experience Platform配置文件。

## Recommendations

* 的 **更新用户档案** 操作只能在以具有命名空间的事件开始的历程中使用。
* 该操作仅更新现有字段，而不会创建新的用户档案字段。
* 您不能使用 **更新用户档案** 操作以生成体验事件，例如购买。
* 与任何其他操作一样，在出现错误或超时时，您可以定义替代路径，并且不能并行放置两个操作。
* 发送到Adobe Experience Platform的更新请求会立即/在一秒内发送。 通常需要几秒钟，但有时候需要更多时间，而且无法保证。 因此，例如，如果某个操作使用的“字段1”是由 **更新用户档案** 操作位于之前，您不应期望在操作中更新“字段1”。
* 的 **更新用户档案** 活动不支持定义为枚举的XDM字段。

## 使用用户档案更新

1. 通过以事件开始来设计您的历程。 请参阅 [部分](../building-journeys/journey.md).

1. 在 **操作** ，请将 **更新用户档案** 活动。

   ![](assets/profileupdate0.png)

1. 从列表中选择架构。

1. 单击 **字段** ，以选择要更新的字段。 只能选择一个字段。

   ![](assets/profileupdate2.png)

1. 从列表中选择数据集。

   >[!NOTE]
   >
   >的 **更新用户档案** 操作会实时更新配置文件数据，但不会更新数据集。 由于配置文件是与数据集相关的记录，因此需要选择数据集。

1. 单击 **值** 字段来定义要使用的值：

   * 使用简单表达式编辑器，您可以从数据源或传入事件中选择字段。

      ![](assets/profileupdate4.png)

   * 如果要定义特定值或利用高级函数，请单击 **高级模式**.

      ![](assets/profileupdate3.png)

的 **更新用户档案** 现已配置。

![](assets/profileupdate1.png)


## 使用测试模式 {#using-the-test-mode}

在测试模式下，将不模拟用户档案更新。 将对测试用户档案执行更新。

只有测试用户档案才能在测试模式下进入历程。 您可以创建新的测试用户档案，或将现有用户档案转换为测试用户档案。 在Adobe Experience Platform中，您可以通过csv文件导入或API调用来更新用户档案属性。 更简单的方法是使用 **更新用户档案** 操作活动，并将测试用户档案布尔字段从false更改为true。

有关如何将现有用户档案转换为测试用户档案的更多信息，请参阅此 [部分](../segment/creating-test-profiles.md#create-test-profiles-csv).
