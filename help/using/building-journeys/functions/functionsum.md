---
product: adobe campaign
title: sum
description: 了解函数和
feature: Journeys
role: Data Engineer
level: Experienced
exl-id: a9085f4d-6434-4bc5-8e5d-3f2b6033defc
source-git-commit: 2022b2c81738ae6d3e66280265948c5b88a117c8
workflow-type: tm+mt
source-wordcount: '51'
ht-degree: 11%

---

# sum {#sum}

返回一组表达式值的和。 将忽略空值。

## 类别

聚合

## 函数语法

`sum(<parameters>)`

## 参数

* listInteger
* listDecimal
* 持续时间
* 整数
* 小数

## 签名和返回的类型

`sum(<listDecimal>)`

返回小数。

`sum(<listInteger>)`

返回整数。

`sum(<integer>,<integer>)`

返回整数。

`sum(<decimal>,<decimal>)`

返回小数。

## 示例

`sum(@{BarBeacon.inventory},5)`

`sum([10,3,8])`

返回21。

`sum([10.5,null,8.1])`

返回18.6。
