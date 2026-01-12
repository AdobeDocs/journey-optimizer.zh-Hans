---
solution: Journey Optimizer
product: journey optimizer
title: 将集合传递到自定义操作参数
description: 了解如何使用自定义操作在Journey Optimizer中动态传递收藏集
feature: Journeys, Use Cases, Custom Actions, Collections
topic: Content Management
role: Developer
level: Experienced
exl-id: 8832d306-5842-4be5-9fb9-509050fcbb01
version: Journey Orchestration
source-git-commit: 6976f2b1b8b95f7dc9bffe65b7a7ddcc5dab5474
workflow-type: tm+mt
source-wordcount: '794'
ht-degree: 3%

---


# 将集合传递到自定义操作参数 {#passing-collection}

您可以在自定义操作参数中传递集合，这些参数在运行时动态填充。

支持两种类型的收藏集：

* **简单收藏集**

  将简单集合用于基本值列表，例如字符串、数字或布尔值。 当您只需传递项目列表而无需附加属性时，这些功能非常有用。

  例如，设备类型列表：

  ```json
  {
   "deviceTypes": [
       "android",
       "ios"
   ]
  }
  ```

* **对象集合**

  当每个项包含多个字段或属性时，使用对象集合。 它们通常用于传递结构化数据，例如产品详细信息、事件记录或项目属性。

  例如：

  ```json
  {
  "products":[
     {
        "id":"productA",
        "name":"A",
        "price":20.1
     },
     {
        "id":"productB",
        "name":"B",
        "price":10.0
     },
     {
        "id":"productC",
        "name":"C",
        "price":5.99
     }
   ]
  }
  ```

>[!NOTE]
>
>在自定义操作请求负载中，仅部分支持集合中的嵌套数组。 有关详细信息，请参阅[限制](#limitations)。

## 一般程序 {#general-procedure}

在此部分中，我们使用以下JSON有效负载示例。 这是一个对象数组，其中的字段是一个简单的集合。

```json
{
  "ctxt": {
    "products": [
      {
        "id": "productA",
        "name": "A",
        "price": 20.1,
        "color":"blue",
        "locations": [
          "Paris",
          "London"
        ]
      },
      {
        "id": "productB",
        "name": "B",
        "price": 10.99
      }
    ]
  }
}
```

您可以看到`products`是两个对象的数组。 您需要至少具有一个对象。

1. 创建自定义操作。 请参阅[此页面](../action/about-custom-action-configuration.md)以了解详情。

1. 在&#x200B;**[!UICONTROL 操作参数]**&#x200B;部分中，粘贴JSON示例。 显示的结构是静态的：粘贴有效负载时，所有字段都定义为常量。

   显示集合函数和操作的![表达式编辑器](assets/uc-collection-1.png)

1. 如果需要，请调整字段类型。 集合支持以下字段类型：listString、listInteger、listDecimal、listBoolean、listDateTime、listDateTimeOnly、listDateOnly、listObject

   >[!NOTE]
   >
   >根据有效负载示例自动推断字段类型。

1. 如果要动态传递对象，则需要将它们设置为变量。 在此示例中，我们将`products`设置为变量。 对象中包含的所有对象字段都会自动设置为变量。

   >[!NOTE]
   >
   >有效负载示例的第一个对象用于定义字段。

1. 对于每个字段，定义将在历程画布中显示的标签。

   ![筛选集合函数与条件生成器接口](assets/uc-collection-2.png){width="70%" align="left"}

1. 创建历程并添加您创建的自定义操作。 请参阅[此页面](../building-journeys/using-custom-actions.md)以了解详情。

1. 在&#x200B;**[!UICONTROL 操作参数]**&#x200B;部分中，使用高级表达式编辑器定义数组参数（在本例中为`products`）。

   ![包含字段选择的集合筛选表达式](assets/uc-collection-3.png)

1. 对于以下每个对象字段，键入源XDM架构中的相应字段名称。 如果名称相同，则不需要此操作。 在我们的示例中，我们只需要定义`product id`和“颜色”。

   ![具有排序配置的集合排序函数](assets/uc-collection-4.png){width="50%" align="left"}

对于数组字段，您还可以使用高级表达式编辑器执行数据操作。 在以下示例中，我们使用[filter](functions/list-functions.md#filter)和[intersect](functions/list-functions.md#intersect)函数：

![包含筛选、排序和限制操作的完整集合表达式](assets/uc-collection-5.png)

## 限制 {#limitations}

虽然自定义操作中的集合为传递动态数据提供了灵活性，但需要注意一些结构性约束：

* **在自定义操作中支持嵌套数组**

  Adobe Journey Optimizer支持自定义操作&#x200B;**响应负载**&#x200B;中的嵌套对象数组，但此支持在&#x200B;**请求负载**&#x200B;中受限。

  在请求有效负载中，仅当嵌套数组包含固定数量的项目时（如自定义操作配置中所定义），才支持嵌套数组。 例如，如果嵌套数组始终只包含三个项目，则可以将其配置为常量。 当项目的数量需要为动态时，只能将非嵌套数组（位于底层的数组）定义为变量。

  示例：

   1. 以下示例说明了&#x200B;**不支持的用例**。

      在此示例中，products数组包含一个嵌套数组(`locations`)，该数组具有动态数量的项，这在请求负载中不受支持。

      ```json
      {
      "products": [
         {
            "id": "productA",
            "name": "A",
            "price": 20,
            "locations": [
            { "name": "Paris" },
            { "name": "London" }
            ]
         }
      ]
      }
      ```

   2. 支持的示例，其中包含定义为常量的固定项目。

      在这种情况下，嵌套位置将由固定字段(`location1`， `location2`)替换，从而允许有效负载在支持的配置中保持有效。

      ```json
      {
      "products": [
         {
            "id": "productA",
            "name": "A",
            "price": 20,
            "location1": { "name": "Paris" },
            "location2": { "name": "London" }
         }
      ]
      }
      ```


* **测试集合**：要使用测试模式测试集合，必须使用代码视图模式。 请注意，业务事件不支持代码视图模式，因此在这种情况下，您只能发送包含单个元素的集合。


## 特定案例{#examples}

对于异构类型和阵列阵列，使用listAny类型定义阵列。 只能映射单个项，但不能将数组更改为变量。

![具有混合数据类型和字段选择的异构集合](assets/uc-collection-heterogeneous.png){width="70%" align="left"}

异质类型示例：

```json
{
    "data_mixed-types": [
        "test",
        "test2",
        null,
        0
    ]
}
```

阵列示例：

```json
{
    "data_multiple-arrays": [
        [
            "test",
            "test1",
            "test2"
        ]
    ]
}
```

## 其他资源

浏览以下部分，了解有关配置、使用和排除自定义操作的更多信息：

* [自定义操作入门](../action/action.md) — 了解什么是自定义操作以及它们如何帮助您连接到第三方系统
* [配置自定义操作](../action/about-custom-action-configuration.md) — 了解如何创建和配置自定义操作
* [使用自定义操作](../building-journeys/using-custom-actions.md) — 了解如何在历程中使用自定义操作
* [自定义操作疑难解答](../action/troubleshoot-custom-action.md) — 了解自定义操作疑难解答
* [对上下文数据进行迭代](../personalization/iterate-contextual-data.md#arrays-in-journeys) — 了解如何在历程表达式中使用数组，并在消息个性化中迭代自定义操作响应、事件数据和数据集查找

