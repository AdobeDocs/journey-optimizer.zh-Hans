---
product: journey optimizer
title: avg
description: 瞭解函式avg
feature: Journeys
role: Data Engineer, Architect
level: Experienced
keywords: 平均，函式，運算式，歷程
exl-id: cc70f90c-2d12-42a0-829f-5f28c3c29cad
source-git-commit: 1d30c6ae49fd0cac0559eb42a629b59708157f7d
workflow-type: tm+mt
source-wordcount: '53'
ht-degree: 13%

---

# avg {#avg}

傳回一組運算式中的平均值，以清單或兩個運算式形式給出。 Null值會被忽略。


## 类别

聚合

## 函式語法

`avg(<parameter>)`

## 参数

支援的型別：

* listInteger
* listDecimal
* 小數
* 整数

## 簽章和傳回型別

`avg(<listInteger>)`

`avg(<listDecimal>)`

`avg(<decimal>,<decimal>)`

`avg(<decimal>,<integer>)`

`avg(<integer>,<decimal>)`

`avg(<integer>,<integer>)`

傳回小數。

## 示例

`avg(@{BarBeacon.inventory},5)`

`avg([10,3,8])`

傳回7.0。

`avg(10.2, 3)`

傳回6.6。
