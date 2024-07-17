---
product: journey optimizer
title: sort
description: 了解函数排序
feature: Journeys
role: Data Engineer, Architect
level: Experienced
keywords: 排序，函数，表达式，历程
exl-id: 607e1424-4165-48ae-b896-cce2d18f7dcc
source-git-commit: 2f47209ad2a5e5b5d26f01949f5e9ade63c2581f
workflow-type: tm+mt
source-wordcount: '144'
ht-degree: 7%

---

# sort {#sort}

以自然顺序对值列表或对象进行排序。

## 类别

列表

## 函数语法

`sort(<parameters>)`

## 参数

| 参数 | 类型 | 描述 |
|-----------|------------------|------------------|
| listToSort | listString、listBoolean、listInteger、listDecimal、listDuration、listDateTime、listDateTimeOnly、listDateOnly或listObject | 要排序的列表。 对于listObject，它必须是字段引用。 |
| keyAttributeName | 字符串 | 此参数仅适用于listObject。 给定列表中的对象中的属性名称用作排序的键。 |
| sortingOrder | 布尔 | 升序(true)或降序(false) |

## 签名和返回的类型

`sort(<listInteger>,<boolean>)`

返回整数列表。

`sort(<listDecimal>,<boolean>)`

返回小数位数列表。

`sort(<listString>,<boolean>)`

返回字符串列表。

`sort(<listDateTimeOnly>,<boolean>)`

返回不考虑时区的日期时间列表。

`sort(<listDateTime>,<boolean>)`

返回日期时间列表。

`sort(<listDateOnly>,<boolean>)`

返回日期列表。

`sort(<listBoolean>,<boolean>)`

返回布尔值列表。

`sort(<listObject>,<string>,<boolean>)`

返回对象列表。

## 示例

`sort(["A", "C", "B"], true)`

返回`["A","B","C"]`。

`sort([1, 3, 2], false)`

返回`[3, 2, 1]`。

`sort(@event{my_event.productListItems}, "SKU", true)`

返回按SKU属性排序的listObject（升序）

