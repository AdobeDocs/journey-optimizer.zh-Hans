---
product: journey optimizer
title: avg
description: 了解函数avg
feature: Journeys
role: Data Engineer, Architect
level: Experienced
keywords: 平均，函数，表达式，历程
exl-id: cc70f90c-2d12-42a0-829f-5f28c3c29cad
source-git-commit: cb1fed2460ddbf3b226fe191b9695008970937c1
workflow-type: tm+mt
source-wordcount: '55'
ht-degree: 12%

---

# avg {#avg}

返回一组表达式中的平均值，这些表达式以列表或两个表达式形式给定。 Null值将被忽略。


## 类别

聚合

## 函数语法

`avg(<parameter>)`

## 参数

支持的类型：

* listInteger
* listDecimal
* 小数
* 整数

## 签名和返回的类型

`avg(<listInteger>)`

`avg(<listDecimal>)`

`avg(<decimal>,<decimal>)`

`avg(<decimal>,<integer>)`

`avg(<integer>,<decimal>)`

`avg(<integer>,<integer>)`

返回小数。

## 示例

`avg(@event{BarBeacon.inventory},5)`

`avg([10,3,8])`

返回7.0。

`avg(10.2, 3)`

返回6.6。
