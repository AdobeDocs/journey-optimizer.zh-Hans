---
product: journey optimizer
title: inLastHours
description: 瞭解函式inLastHours
feature: Journeys
role: Data Engineer, Architect
level: Experienced
keywords: inLastHours，函式，運算式，歷程
exl-id: c648d711-c81b-403b-9adb-792c7e79e4e2
source-git-commit: 1d30c6ae49fd0cac0559eb42a629b59708157f7d
workflow-type: tm+mt
source-wordcount: '49'
ht-degree: 18%

---

# inLastHours {#inLastHours}

如果指定的日期時間介於現在和現在之間 — 差異小時，則傳回true。

## 类别

日期

## 函式語法

`inLastHours(<dateTime>,<delta>)`

## 参数

| 参数 | 类型 |
|-----------|------------------|
| 日期時間 | dateTime |
| delta | 整数 |

## 簽章和傳回型別

`inLastHours(<dateTime>,<integer>)`

傳回布林值。

## 示例

`inLastHours(toDateTime('2019-12-12T01:11:00Z'), 4)`

傳回true。

`inLastHours(@{MyEvent.timestamp}, 4)`

傳回true。
