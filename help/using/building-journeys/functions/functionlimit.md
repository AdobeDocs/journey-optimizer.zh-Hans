---
product: journey optimizer
title: limit
description: 了解函数限制
feature: Journeys
role: Data Engineer, Architect
level: Experienced
keywords: 限制，函数，表达式，历程
exl-id: 7fa1e393-2912-4392-b759-e54d08d5635a
source-git-commit: f8d62a702824bcfca4221c857acf1d1294427543
workflow-type: tm+mt
source-wordcount: '138'
ht-degree: 7%

---

# limit {#limit}

返回列表的第一个或最后的N个元素。

## 类别

列表

## 函数语法

`limit(<parameters>)`

## 参数

| 参数 | 类型 | 描述 |
|-----------|------------------|------------------|
| listToProcess | listString、listBoolean、listInteger、listDecimal、listDuration、listDateTime、listDateTimeOnly、listDateOnly或listObject | 要考虑的列表。 对于listObject，它必须是字段引用。 |
| 项目数 | 整数 | 要从给定列表中返回的项目数。 |
| firstOrLastItems | 布尔 | 此参数是可选的（默认为true）。 true返回第一项。 false返回最后一个项目。 |

## 签名和返回的类型

`limit(<listString>,<integer>)`
`limit(<listString>,<integer>,<boolean>)`

返回字符串列表。

`limit(<listInteger>,<integer>)`
`limit(<listInteger>,<integer>,<boolean>)`

返回整数列表。

`limit(<listDecimal>,<integer>)`
`limit(<listDecimal>,<integer>,<boolean>)`

返回小数位数列表。

`limit(<listBoolean>,<integer>)`
`limit(<listBoolean>,<integer>,<boolean>)`

返回布尔值列表。

`limit(<listDateOnly>,<integer>)`
`limit(<listDateOnly>,<integer>,<boolean>)`

返回日期列表。

`limit(<listDateTimeOnly>,<integer>)`
`limit(<listDateTimeOnly>,<integer>,<boolean>)`

返回不考虑时区的日期时间列表。

`limit(<listDateTime>,integer>)`
`limit(<listDateTime>,<integer>,<boolean>)`

返回日期时间列表。

`limit(<listDuration>,<integer>)`
`limit(<listDuration>,<integer>,<boolean>)`

返回持续时间列表。

`limit(<listObject>,<integer>)`
`limit(<listObject>,<integer>,<boolean>)`

返回对象列表。

## 示例

`limit(["A", "B", "C", "D", "E"], 3)`

返回 `["A","B","C"]`.

`limit(["A", "B", "C", "D", "E"], 3, false)`

返回 `["C","D","E"]`.
