---
product: adobe campaign
title: distinctCount
description: 了解distinctCount函数
feature: Journeys
role: Data Engineer
level: Experienced
source-git-commit: d786f3d42515d65a6574f51b6cff4b85063a0126
workflow-type: tm+mt
source-wordcount: '49'
ht-degree: 32%

---

# distinctCount{#distinctCount}

计算忽略空值的不同值的数量。

## 类别

聚合

## 函数语法

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

## 签名和返回的类型

`distinctCount(<listAny>)`

返回整数。

## 示例

`distinctCount([10,2,10,null])`

返回2。
