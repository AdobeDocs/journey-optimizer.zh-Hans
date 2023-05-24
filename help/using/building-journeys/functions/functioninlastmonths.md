---
product: journey optimizer
title: inLastMonths
description: 瞭解函式inLastMonths
feature: Journeys
role: Data Engineer, Architect
level: Experienced
keywords: inLastMonths，函式，運算式，歷程
exl-id: 4933ef43-66b8-462d-867c-03edd4c34947
source-git-commit: 1d30c6ae49fd0cac0559eb42a629b59708157f7d
workflow-type: tm+mt
source-wordcount: '48'
ht-degree: 18%

---

# inLastMonths {#inLastMonths}

如果指定的日期或dateTime介於現在和現在 — 差異月份之間，則傳回true。

## 类别

日期

## 函式語法

`inLastMonths(<dateTime>,<delta>)`

## 参数

| 参数 | 类型 |
|-----------|------------------|
| 日期時間 | dateTime |
| delta | 整数 |

## 簽章和傳回型別

`inLastMonths(<dateTime>,<integer>)`

傳回布林值。

## 示例

`inLastMonths(toDateTime('2010-12-12T01:11:00Z'), 4)`

傳回true。
