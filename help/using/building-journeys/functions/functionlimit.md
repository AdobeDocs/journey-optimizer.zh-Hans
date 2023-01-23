---
product: journey optimizer
title: limit
description: 了解函数限制
feature: Journeys
role: Data Engineer, Architect
level: Experienced
keywords: 限制，函数，表达式，历程
exl-id: 7fa1e393-2912-4392-b759-e54d08d5635a
source-git-commit: 1d30c6ae49fd0cac0559eb42a629b59708157f7d
workflow-type: tm+mt
source-wordcount: '156'
ht-degree: 8%

---

# limit {#limit}

返回列表的第一个或最后一个N个元素。

>[!NOTE]
>
>如果目标列表是listObject，则此函数只能在自定义操作表达式中使用。

## 类别

列表

## 函数语法

`limit(<parameters>)`

## 参数

| 参数 | 类型 | 描述 |
|-----------|------------------|------------------|
| listToProcess | listString、listBoolean、listInteger、listDecimal、listDuration、listDateTime、listDateTimeOnly、listDateOnly或listObject | 列表进行整理。 对于listObject，它必须是字段引用。 |
| numberOfItems | 整数 | 要从给定列表返回的项目数。 |
| firstOrLastItems | 布尔 | 此参数是可选的（默认为true）。 true会返回前一个项目。 false会返回最后的项目。 |

## 签名和返回的类型

`limit(<listString>,<integer>)`
`limit(<listString>,<integer>,<boolean>)`

返回字符串列表。

`limit(<listInteger>,<integer>)`
`limit(<listInteger>,<integer>,<boolean>)`

返回整数列表。

`limit(<listDecimal>,<integer>)`
`limit(<listDecimal>,<integer>,<boolean>)`

返回小数列表。

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

返回datetimes列表。

`limit(<listDuration>,<integer>)`
`limit(<listDuration>,<integer>,<boolean>)`

返回持续时间列表。

`limit(<listObject>,<integer>)`
`limit(<listObject>,<integer>,<boolean>)`

返回对象列表。

## 示例

`limit(["A", "B", "C", "D", "E"], 3)`

返回结果 `["A","B","C"]`.

`limit(["A", "B", "C", "D", "E"], 3, false)`

返回结果 `["C","D","E"]`.
