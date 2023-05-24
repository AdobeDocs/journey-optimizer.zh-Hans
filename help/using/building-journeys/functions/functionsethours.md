---
product: journey optimizer
title: setHours
description: 瞭解函式setHours
feature: Journeys
role: Data Engineer, Architect
level: Experienced
keywords: setHours，函式，運算式，歷程
exl-id: ed78c2a9-d83a-4fac-a2e9-7383da131a1f
source-git-commit: 1d30c6ae49fd0cac0559eb42a629b59708157f7d
workflow-type: tm+mt
source-wordcount: '105'
ht-degree: 9%

---

# setHours {#setHours}

僅設定日期時間或日期時間的小時。 例如，如果您要等到明天的某個小時，您可以強制該小時。

## 类别

日期

## 函式語法

`setHours(<parameter>)`

## 参数

| 参数 | 类型 |
|--- |--- |
| 日期時間 | dateTime |
| 不考慮時區的日期時間 | dateTimeOnly |
| 小时 | 整数 |

## 簽章和傳回型別

`setHours(<dateTime>,<hours>)`

傳回日期時間。

`setHours(<dateTimeOnly>,<hours>)`

傳回不考慮時區的日期時間。

## 示例

`setHours(toDateTime('2010-12-12T01:11:00Z'), 4)`

傳回2010-12-12T04:11:00Z。

`setHours(nowWithDelta(1, "days"), 20)`

明天晚上8：XY，XY會傳回目前時間評估的分鐘數。 如果評估在凌晨2:45進行，則傳回的時間將會是晚上8:45。
