---
product: journey optimizer
title: distinctWithNull
description: 了解distinctWithNull函数
feature: Journeys
role: Developer
level: Experienced
keywords: distinctWithNull，函数，表达式，历程
exl-id: 73fa9837-d2e1-4f0a-a423-cf7728882eba
version: Journey Orchestration
source-git-commit: bdf857c010854b7f0f6ce4817012398e74a068d5
workflow-type: tm+mt
source-wordcount: '123'
ht-degree: 7%

---

# distinctWithNull {#distinctWithNull}

返回给定列表的不同值或对象。 如果列表至少有一个null条目，则返回的列表中将显示一个null条目。

请注意，此函数不支持参数`<listObject>`。

## 类别

列表

## 函数语法

`distinctWithNull(<parameters>)`

## 参数

| 参数 | 类型 | 描述 |
|-----------|------------------|------------------|
| listToProcess | listString、listBoolean、listInteger、listDecimal、listDuration、listDateTime、listDateTimeOnly、listDateOnly | 要处理的列表。 |

## 签名和返回的类型

`distinctWithNull(<listInteger>)`

返回整数列表。

`distinctWithNull(<listDecimal>)`

返回小数位数列表。

`distinctWithNull(<listString>)`

返回字符串列表。

`distinctWithNull(<listDateTimeOnly>)`

返回不考虑时区的日期时间列表。

`distinctWithNull(<listDateTime>)`

返回日期时间列表。

`distinctWithNull(<listDateOnly>)`

返回日期列表。

`distinctWithNull(<listBoolean>)`

返回布尔值列表。

`distinctWithNull(<listDuration>)`

返回持续时间列表。

## 示例

`distinctWithNull([10,2,10,null])`

返回[10， 2， null]
