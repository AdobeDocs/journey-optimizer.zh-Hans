---
solution: Journey Optimizer
product: journey optimizer
title: 使用Adobe Experience Platform数据进行个性化（测试版）
description: 了解如何使用Adobe Experience Platform数据进行个性化。
feature: Personalization, Rules
topic: Personalization
role: Data Engineer
level: Intermediate
keywords: 表达式，编辑器
hidefromtoc: true
hide: true
source-git-commit: 4d4ce1e892d51393972973950e8e03259e16c204
workflow-type: tm+mt
source-wordcount: '566'
ht-degree: 0%

---

# 使用Adobe Experience Platform数据进行个性化（测试版） {#aep-data}

>[!AVAILABILITY]
>
>此功能目前仅作为专用测试版提供。
>
>目前，它仅适用于在您提供给Adobe的非生产沙盒中测试以及为Beta测试请求的数据集。

Journey Optimizer允许您在表达式编辑器中利用Adobe Experience Platform中的数据，以 [使内容个性化](../personalization/personalize.md). 步骤如下：

1. 打开表达式编辑器，您可以在每个上下文中定义个性化设置（如消息），该编辑器将可用。 [了解如何使用表达式编辑器](../personalization/personalization-build-expressions.md)

1. 导航到辅助函数列表，然后添加 **datasetLookup** 辅助函数到代码窗格。

   ![](assets/aep-data-helper.png)

1. 此函数提供了一个预定义语法，允许您从Adobe Experience Platform数据集调用字段。 语法如下：

   ```
   {{entity.datasetId="datasetId" id="key" result="store"}}
   ```

   * **entity.datasetId** 是您正在处理的数据集的ID，
   * **id** 是用作数据集中的主要标识的字段，

     >[!NOTE]
     >
     >为此字段输入的值可以是字段ID (*profile.couponValue*)，在历程事件中传递的字段(*context.journey.events.event_ID.couponValue*)或静态值(*couponAbcd*)。 在任何情况下，系统都将使用值，并在数据集中查找以检查它是否与键匹配)。

   * **结果** 是一个任意名称，您需要提供它以引用要从数据集中检索的所有字段值。 此值将在您的代码中用于调用每个字段。

   +++在哪里检索数据集ID？

   可在Adobe Experience Platform用户界面中检索数据集ID。 了解如何使用中的数据集 [Adobe Experience Platform文档](https://experienceleague.adobe.com/en/docs/experience-platform/catalog/datasets/user-guide#view-datasets){target="_blank"}.

   ![](assets/aep-data-dataset.png)

+++

   +++如何识别数据集中的主标识字段？

   可以在链接到数据集的架构中找到已定义为给定数据集的主标识的字段。 了解如何使用中的标识字段 [Adobe Experience Platform文档](https://experienceleague.adobe.com/en/docs/experience-platform/xdm/ui/fields/identity){target="_blank"}.

   ![](assets/aep-data-identity.png)

+++

1. 调整语法以符合您的需求。 在本例中，我们要检索与乘客航班相关的数据。 语法如下：

   ```
   {{entity.datasetId="1234567890abcdtId" id="profile.personalEmail.address" result="flight"}}
   ```

   * 我们正在处理ID为“1234567890abcdtId”的数据集，
   * 此数据集中用作主键的字段是电子邮件地址，
   * 我们希望在“flight”引用下包含所有字段值。

1. 配置要在Adobe Experience Platform数据集中调用的语法后，您可以指定要检索的字段。 语法如下：

   ```
   {{result.fieldId}}
   ```

   * **结果** 是您已分配到的值 **结果** 中的参数 **多实体** 辅助函数。 在本例中，为“flight”。
   * **字段标识** 是要检索的字段的ID。 在浏览数据集时，此ID显示在Adobe Experience Platform用户界面中。 展开以下部分以显示示例：

     +++从何处检索字段ID？

     在Adobe Experience Platform用户界面中预览数据集时，可以检索字段ID。 了解如何在中预览数据集 [Adobe Experience Platform文档](https://experienceleague.adobe.com/en/docs/experience-platform/catalog/datasets/user-guide#preview){target="_blank"}.

     ![](assets/aep-data-field.png)

+++

   在本例中，我们希望使用与乘客登机时间和登机口相关的信息。 因此，我们添加了这两行：

   * `{{flight._myorg.booking.boardingTime}}`
   * `{{flight._myorg.booking.gate}}`

1. 现在，您的代码已准备就绪，您可以像往常一样完成内容，然后使用进行测试 **模拟内容** 按钮以检查个性化。 [了解如何预览和测试内容](../content-management/preview-test.md)


   ![](assets/aep-data-sample.png)
