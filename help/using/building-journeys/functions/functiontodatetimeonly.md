---
product: journey optimizer
title: toDateTimeOnly
description: 瞭解函式toDateTime
feature: Journeys
role: Data Engineer, Architect
level: Experienced
keywords: toDateTimeOnly，函式，運算式，歷程
exl-id: db54c119-5080-403a-b254-43645be6b4a8
source-git-commit: 1d30c6ae49fd0cac0559eb42a629b59708157f7d
workflow-type: tm+mt
source-wordcount: '59'
ht-degree: 15%

---

# toDateTimeOnly{#toDateTimeOnly}

將引數值轉換為僅日期時間值。

## 类别

转化

## 函式語法

`toDateTimeOnly(<parameters>)`

## 参数

| 参数 | 类型 |
|-----------|------------------|
| ISO-8601或&quot;YYYY-MM-DD&quot;格式的日期時間（XDM日期格式） | 字符串 |
| 日期時間 | dateTime |

## 簽章和傳回的型別

`toDateTimeOnly(<dateTime>)`

`toDateTimeOnly(<string>)`
<!--`toDateTimeOnly(<integer>,<integer>,<integer>)`
`toDateTimeOnly(<integer>,<integer>,<integer>,<integer>,<integer>,<integer>)`-->

傳回日期時間而不考慮時區。

## 示例

`toDateTimeOnly ("2016-08-18")`

傳回代表2016-08-18T00的dateTime:00:00.000

`toDateTimeOnly(now())`

<!--`toDateTimeOnly(2016,8,18,23,17,59)`

Returns 2016-08-18T23:17:59.000.

`toDateTimeOnly(2016,8,18)`

Returns 2016-08-18T00:00:00.000.-->
