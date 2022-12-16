---
product: journey optimizer
title: max
description: 了解函数max
feature: Journeys
role: Data Engineer
level: Experienced
exl-id: 5c792d33-32b9-4b1b-ab99-3ebfac391678
source-git-commit: d17e64e03d093a8a459caef2fb0197a5710dfb7d
workflow-type: tm+mt
source-wordcount: '92'
ht-degree: 6%

---

# max{#max}

返回一组表达式中的最大值（以列表或两个表达式的形式给定）。 将忽略空值。

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

返回日期时间，而不考虑时区。

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

返回日期时间，而不考虑时区。

`max(<integer>,<integer>)`

返回整数。

## 示例

`max(@{BarBeacon.inventory},5)`

`max([10,3,8])`

返回10。

`max([10,null,8])`

返回10。
