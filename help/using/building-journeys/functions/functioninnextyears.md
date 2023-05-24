---
product: journey optimizer
title: inNextYears
description: 瞭解函式inNextYears
feature: Journeys
role: Data Engineer, Architect
level: Experienced
keywords: inNextYears，函式，運算式，歷程
exl-id: e4597772-d53c-4e15-8237-b2460ce31170
source-git-commit: 1d30c6ae49fd0cac0559eb42a629b59708157f7d
workflow-type: tm+mt
source-wordcount: '48'
ht-degree: 18%

---

# inNextYears {#inNextYears}

如果指定的日期或dateTime介於現在和現在+差異年度之間，則傳回true。

## 类别

日期

## 函式語法

`inNextYears(<dateTime>,<delta>)`

## 参数

| 参数 | 类型 |
|-----------|------------------|
| 日期時間 | dateTime |
| delta | 整数 |

## 簽章和傳回型別

`inNextYears(<dateTime>,<integer>)`

傳回布林值。

## 示例

`inNextYears(toDateTime('2021-12-12T01:11:00Z'), 4)`

傳回true。
