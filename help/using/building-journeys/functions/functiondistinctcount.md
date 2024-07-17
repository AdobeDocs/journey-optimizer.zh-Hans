---
product: journey optimizer
title: distinctCount
description: 了解distinctCount函数
feature: Journeys
role: Data Engineer, Architect
level: Experienced
keywords: distinctCount，函数，表达式，历程
exl-id: 8796ba91-5c64-43c2-a444-27ac8b719c86
source-git-commit: 2f47209ad2a5e5b5d26f01949f5e9ade63c2581f
workflow-type: tm+mt
source-wordcount: '138'
ht-degree: 7%

---

# distinctCount{#distinctCount}

计算不同值的数量，忽略空值。

## 类别

聚合

## 函数语法

`distinctCount(<listAny>)`

## 参数

| 参数 | 类型 | 描述 |
|-----------|------------------|------------------|
| listToProcess | listString、listBoolean、listInteger、listDecimal、listDuration、listDateTime、listDateTimeOnly、listDateOnly或listObject | 要处理的列表。 对于listObject，它必须是字段引用。 |
| keyAttributeName | 字符串 | 此参数是可选的，并且仅适用于listObject。 如果未提供参数，则当所有属性都具有相同的值时，会将对象视为重复。 否则，如果给定的属性具有相同的值，则将对象视为重复。 |

## 签名和返回的类型

`distinctCount(<listAny>)`

返回整数。

`distinctCount(<listObject>)`

`distinctCount(<listObject>,<string>)`

返回对象列表。


## 示例

`distinctCount([10,2,10,null])`

返回2。

`distinctCount(@event{my_event.productListItems})`

返回给定对象数组（listObject类型）中完全不同的对象数。

`distinctCount(@event{my_event.productListItems}, "SKU")`

返回具有不同“SKU”属性值{}的对象数。
