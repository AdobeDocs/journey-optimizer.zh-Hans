---
product: journey optimizer
title: min
description: 了解函数min
feature: Journeys
role: Data Engineer, Architect
level: Experienced
keywords: 最小值，函数，表达式，历程
exl-id: 1c425d1d-08b4-446b-83ce-db376b2bf39f
source-git-commit: 1d30c6ae49fd0cac0559eb42a629b59708157f7d
workflow-type: tm+mt
source-wordcount: '98'
ht-degree: 7%

---

# min {#min}

返回一组表达式中的最小值，这些表达式以列表或两个表达式形式给定。 Null值将被忽略。

## 类别

聚合

## 函数语法

`min(<parameters>)`

## 参数

* listDuration
* listInteger
* listDecimal
* listDateTime
* listDateTimeOnly
* listDateOnly
* 持续时间
* 整数
* 小数
* dateTime
* dateTimeOnly

## 签名和返回的类型

`min(<listDuration>)`

返回持续时间。

`min(<listInteger>)`

返回持续时间。

`min(<listDateTimeOnly>)`

返回不考虑时区的日期时间。

`min(<listDateTime>)`

返回日期时间。

`min(<listDateOnly>)`

返回日期。

`min(<listDecimal>)`

返回小数。

`min(<decimal>,<decimal>)`

返回小数。

`min(<duration>,<duration>)`

返回持续时间。

`min(<dateTime>,<dateTime>)`

返回日期时间。

`min(<dateTimeOnly>,<dateTimeOnly>)`

返回不考虑时区的日期时间。

`min(<integer>,<integer>)`

返回整数。

## 示例

`min(@{BarBeacon.inventory},5)`

`min([10,3,8])`

返回3。

`min([10,null,8])`

返回8。
