---
product: journey optimizer
title: avg
description: 了解函数avg
feature: Journeys
role: Data Engineer
level: Experienced
exl-id: cc70f90c-2d12-42a0-829f-5f28c3c29cad
source-git-commit: d17e64e03d093a8a459caef2fb0197a5710dfb7d
workflow-type: tm+mt
source-wordcount: '51'
ht-degree: 0%

---

# avg {#avg}

返回一组表达式中的平均值（以列表或两个表达式的形式提供）。 将忽略空值。


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

## 签名和返回类型

`avg(<listInteger>)`

`avg(<listDecimal>)`

`avg(<decimal>,<decimal>)`

`avg(<decimal>,<integer>)`

`avg(<integer>,<decimal>)`

`avg(<integer>,<integer>)`

返回小数。

## 示例

`avg(@{BarBeacon.inventory},5)`

`avg([10,3,8])`

返回7.0。

`avg(10.2, 3)`

返回6.6。
