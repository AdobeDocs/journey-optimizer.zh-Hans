---
product: journey optimizer
title: min
description: 瞭解函式最小值
feature: Journeys
role: Data Engineer, Architect
level: Experienced
keywords: min，函式，運算式，歷程
exl-id: 1c425d1d-08b4-446b-83ce-db376b2bf39f
source-git-commit: 1d30c6ae49fd0cac0559eb42a629b59708157f7d
workflow-type: tm+mt
source-wordcount: '96'
ht-degree: 7%

---

# min {#min}

傳回一組運算式中的最小值，以清單或兩個運算式形式給出。 Null值會被忽略。

## 类别

聚合

## 函式語法

`min(<parameters>)`

## 参数

* listDuration
* listInteger
* listDecimal
* listDateTime
* listDateTimeOnly
* listDateOnly
* 持續時間
* 整数
* 小數
* dateTime
* dateTimeOnly

## 簽章和傳回的型別

`min(<listDuration>)`

傳回持續時間。

`min(<listInteger>)`

傳回持續時間。

`min(<listDateTimeOnly>)`

傳回不考慮時區的日期時間。

`min(<listDateTime>)`

傳回日期時間。

`min(<listDateOnly>)`

傳回日期。

`min(<listDecimal>)`

傳回小數。

`min(<decimal>,<decimal>)`

傳回小數。

`min(<duration>,<duration>)`

傳回持續時間。

`min(<dateTime>,<dateTime>)`

傳回日期時間。

`min(<dateTimeOnly>,<dateTimeOnly>)`

傳回不考慮時區的日期時間。

`min(<integer>,<integer>)`

傳回整數。

## 示例

`min(@{BarBeacon.inventory},5)`

`min([10,3,8])`

傳回3。

`min([10,null,8])`

傳回8。
