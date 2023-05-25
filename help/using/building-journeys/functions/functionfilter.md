---
product: journey optimizer
title: filter
description: 了解函数筛选器
feature: Journeys
role: Data Engineer, Architect
level: Experienced
keywords: 过滤器，函数，表达式，历程
exl-id: 05e3d2ba-1a27-4f27-88cc-3d83eb3b14af
source-git-commit: 1d30c6ae49fd0cac0559eb42a629b59708157f7d
workflow-type: tm+mt
source-wordcount: '130'
ht-degree: 8%

---

# filter{#filter}

返回一个listObject，其对象具有匹配给定键值之一的键属性。

>[!NOTE]
>
>如果目标列表是listObject，则此函数只能在自定义操作表达式中使用。

## 类别

列表

## 函数语法

`filter(<parameters>)`

## 参数

| 参数 | 类型 | 描述 |
|-----------|------------------|------------------|
| listToFilter | listObject | 要筛选的对象列表。 它必须是字段引用。 |
| keyAttributeName | 字符串 | 给定列表对象中的属性名称，用作筛选键 |
| keyValueList | list | 用于筛选的键值数组 |

## 签名和返回的类型

`filter(listObject, string, listString)`

`filter(listObject, string, listInteger)`

`filter(listObject, string, listDecimal)`

`filter(listObject, string, listDateTime)`

`filter(listObject, string, listDateTimeOnly)`

`filter(listObject, string, listDateOnly)`

`filter(listObject, string, listDuration)`

`filter(listObject, string, listBoolean)`

返回listObject。

## 示例

以下是在传入事件“myevent”中传递的有效负载示例：

```json
"productListItems": [{
   "id": "product1",
   "name": "the product 1",
   "price": 20
},{
   "id": "product2",
   "name": "the product 2",
   "price": 30
},{
   "id": "product3",
   "name": "the product 3",
   "price": 50
}]
```

您可以使用以下表达式：

```json
filter(
 @{myevent.productListItems},
 "id", 
 ["product2", "product3", "product4"]
)
```

返回包含两个对象的listObject，其中“product2”和“product3”作为ID。
