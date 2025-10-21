---
product: journey optimizer
title: setHours
description: 了解函数setHours
feature: Journeys
role: Engineer
level: Experienced
keywords: setHours，函数，表达式，历程
exl-id: ed78c2a9-d83a-4fac-a2e9-7383da131a1f
version: Journey Orchestration
source-git-commit: 6f7b9bfb65617ee1ace3a2faaebdb24fa068d74f
workflow-type: tm+mt
source-wordcount: '109'
ht-degree: 9%

---

# setHours {#setHours}

仅设置日期时间或日期时间的小时。 例如，如果您要等到明天的某个小时，则可以强制执行该小时。

## 类别

日期

## 函数语法

`setHours(<parameter>)`

## 参数

| 参数 | 类型 |
|--- |--- |
| 日期时间 | dateTime |
| 不考虑时区的日期时间 | dateTimeOnly |
| 小时 | 整数 |

## 签名和返回的类型

`setHours(<dateTime>,<hours>)`

返回日期时间。

`setHours(<dateTimeOnly>,<hours>)`

返回不考虑时区的日期时间。

## 示例

`setHours(toDateTime('2023-12-12T01:11:00Z'), 4)`

返回2023-12-12T04:11:00Z。

`setHours(nowWithDelta(1, "days"), 20)`

返回明天晚上8:XY，XY是当前时间评估时刻的分钟数。 如果评估发生在凌晨2:45，则返回的时间将为晚上8:45。
