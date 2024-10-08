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
exl-id: 2fc10fdd-ca9e-46f0-94ed-2d7ea4de5baf
source-git-commit: a03541b5f1d9c799c30bf1d38b6f187d94c21dff
workflow-type: tm+mt
source-wordcount: '537'
ht-degree: 0%

---

# 使用Adobe Experience Platform数据进行个性化（测试版） {#aep-data}

>[!AVAILABILITY]
>
>此功能目前仅作为专用测试版提供。
>
>目前，该工具仅可用于&#x200B;**电子邮件渠道**，以及在您提供给Adobe的非生产沙盒中测试以及测试版所请求的数据集。

Journey Optimizer允许您在个性化编辑器中利用Adobe Experience Platform中的数据来[个性化您的内容](../personalization/personalize.md)。 步骤如下：

1. 打开个性化编辑器，您可以在每个上下文中定义个性化设置（如消息）时使用该编辑器。 [了解如何使用个性化编辑器](../personalization/personalization-build-expressions.md)

1. 导航到帮助程序函数列表，并将&#x200B;**datasetLookup**&#x200B;帮助程序函数添加到代码窗格。

   ![](assets/aep-data-helper.png)

1. 此函数提供了一个预定义语法，允许您从Adobe Experience Platform数据集调用字段。 语法如下：

   ```
   {{entity.datasetId="datasetId" id="key" result="store"}}
   ```

   * **entity.datasetId**&#x200B;是您正在处理的数据集的ID。
   * **id**&#x200B;是源列的ID，它应该与查找数据集的主标识联接。

     >[!NOTE]
     >
     >为此字段输入的值可以是字段ID (*profile.couponValue*)、在历程事件中传递的字段(*context.journey.events.event_ID.couponValue*)，也可以是静态值(*couponAbcd*)。 无论如何，系统都将使用值，并在数据集中查找，以检查它是否与键匹配。

   * **结果**&#x200B;是一个任意名称，您需要提供它以引用要从数据集中检索的所有字段值。 此值将在您的代码中用于调用每个字段。

   +++在哪里检索数据集ID？

   可在Adobe Experience Platform用户界面中检索数据集ID。 在[Adobe Experience Platform文档](https://experienceleague.adobe.com/en/docs/experience-platform/catalog/datasets/user-guide#view-datasets){target="_blank"}中了解如何使用数据集。

   ![](assets/aep-data-dataset.png)

+++

1. 调整语法以符合您的需求。 在本例中，我们要检索与乘客航班相关的数据。 语法如下：

   ```
   {{entity.datasetId="1234567890abcdtId" id=profile.upcomingFlightId result="flight"}}
   ```

   * 我们正在处理ID为“1234567890abcdtId”的数据集，
   * 我们要用于与查找数据集进行联结的字段是&#x200B;*profile.exputingFlightId*，
   * 我们希望在“flight”引用下包含所有字段值。

1. 配置要在Adobe Experience Platform数据集中调用的语法后，您可以指定要检索的字段。 语法如下：

   ```
   {{result.fieldId}}
   ```

   * **result**&#x200B;是您分配给&#x200B;**MultiEntity**&#x200B;帮助程序函数中的&#x200B;**result**&#x200B;参数的值。 在本例中，为“flight”。
   * **fieldID**&#x200B;是要检索的字段的ID。 在浏览数据集时，此ID显示在Adobe Experience Platform用户界面中。 展开以下部分以显示示例：

     +++从何处检索字段ID？

     在Adobe Experience Platform用户界面中预览数据集时，可以检索字段ID。 在[Adobe Experience Platform文档](https://experienceleague.adobe.com/en/docs/experience-platform/catalog/datasets/user-guide#preview){target="_blank"}中了解如何预览数据集。

     ![](assets/aep-data-field.png)

+++

   在本例中，我们希望使用与乘客登机时间和登机口相关的信息。 因此，我们添加了这两行：

   * `{{flight._myorg.booking.boardingTime}}`
   * `{{flight._myorg.booking.gate}}`

1. 现在，您的代码已准备就绪，您可以照常完成内容，并使用&#x200B;**模拟内容**&#x200B;按钮进行测试以检查个性化。 [了解如何预览和测试内容](../content-management/preview-test.md)


   ![](assets/aep-data-sample.png)
