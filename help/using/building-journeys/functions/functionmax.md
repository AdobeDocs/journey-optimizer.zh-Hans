---
product: journey optimizer
title: max
description: 了解函数max
feature: Journeys
role: Developer
level: Experienced
keywords: max，函数，表达式，历程
exl-id: 5c792d33-32b9-4b1b-ab99-3ebfac391678
version: Journey Orchestration
source-git-commit: bdf857c010854b7f0f6ce4817012398e74a068d5
workflow-type: tm+mt
source-wordcount: '98'
ht-degree: 7%

---

# max{#max}

返回一组表达式中的最大值，这些表达式以列表或两个表达式形式给定。 Null值将被忽略。

## 类别

聚合

## 函数语法

`max(<parameter>)`

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

`max(<listDuration>)`

返回持续时间。

`max(<listInteger>)`

返回持续时间。

`max(<listDateTimeOnly>)`

返回不考虑时区的日期时间。

`max(<listDateTime>)`

返回日期时间。

`max(<listDateOnly>)`

返回日期。

`max(<listDecimal>)`

返回小数。

`max(<decimal>,<decimal>)`

返回小数。

`max(<duration>,<duration>)`

返回持续时间。

`max(<dateTime>,<dateTime>)`

返回日期时间。

`max(<dateTimeOnly>,<dateTimeOnly>)`

返回不考虑时区的日期时间。

`max(<integer>,<integer>)`

返回整数。

## 示例

`max(@event{BarBeacon.inventory},5)`

`max([10,3,8])`

返回10。

`max([10,null,8])`

返回10。
