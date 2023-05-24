---
product: journey optimizer
title: distinctCount
description: 瞭解函式distinctCount
feature: Journeys
role: Data Engineer, Architect
level: Experienced
keywords: distinctCount，函式，運算式，歷程
exl-id: 8796ba91-5c64-43c2-a444-27ac8b719c86
source-git-commit: 1d30c6ae49fd0cac0559eb42a629b59708157f7d
workflow-type: tm+mt
source-wordcount: '53'
ht-degree: 30%

---

# distinctCount{#distinctCount}

計算忽略空值的不同值數目。

## 类别

聚合

## 函式語法

`distinctCount(<listAny>)`

## 参数

| 参数 | 类型 |
|-----------|------------------|
| 列表 | listString |
| 列表 | listBoolean |
| 列表 | listInteger |
| 列表 | listDecimal |
| 列表 | listDuration |
| 列表 | listDateTime |
| 列表 | listDateTimeOnly |
| 列表 | listDateOnly |

## 簽章和傳回的型別

`distinctCount(<listAny>)`

傳回整數。

## 示例

`distinctCount([10,2,10,null])`

傳回2。
