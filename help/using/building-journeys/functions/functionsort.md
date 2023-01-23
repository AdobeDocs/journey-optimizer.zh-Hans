---
product: journey optimizer
title: sort
description: 了解函数排序
feature: Journeys
role: Data Engineer, Architect
level: Experienced
keywords: 排序，函数，表达式，历程
exl-id: 607e1424-4165-48ae-b896-cce2d18f7dcc
source-git-commit: 1d30c6ae49fd0cac0559eb42a629b59708157f7d
workflow-type: tm+mt
source-wordcount: '152'
ht-degree: 8%

---

# sort {#sort}

按自然顺序对值或对象列表进行排序。

>[!NOTE]
>
>如果目标列表是listObject，则此函数只能在自定义操作表达式中使用。

## 类别

列表

## 函数语法

`sort(<parameters>)`

## 参数

| 参数 | 类型 | 描述 |
|-----------|------------------|------------------|
| listToSort | listString、listBoolean、listInteger、listDecimal、listDuration、listDateTime、listDateTimeOnly、listDateOnly或listObject | 列表进行整理。 对于listObject，它必须是字段引用。 |
| keyAttributeName | 字符串 | 此参数仅用于listObject。 给定列表对象中的属性名称用作排序键。 |
| sortingOrder | 布尔 | 升序(true)或降序(false) |

## 签名和返回的类型

`sort(<listInteger>,<boolean>)`

返回整数列表。

`sort(<listDecimal>,<boolean>)`

返回小数列表。

`sort(<listString>,<boolean>)`

返回字符串列表。

`sort(<listDateTimeOnly>,<boolean>)`

返回不考虑时区的日期时间列表。

`sort(<listDateTime>,<boolean>)`

返回datetimes列表。

`sort(<listDateOnly>,<boolean>)`

返回日期列表。

`sort(<listBoolean>,<boolean>)`

返回布尔值列表。

`sort(<listObject>,<string>,<boolean>)`

返回对象列表。

## 示例

`sort(["A", "C", "B"], true)`

返回结果 `["A","B","C"]`.

`sort([1, 3, 2], false)`

返回结果 `[3, 2, 1]`.

