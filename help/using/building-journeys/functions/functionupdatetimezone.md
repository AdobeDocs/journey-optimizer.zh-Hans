---
product: journey optimizer
title: updateTimeZone
description: 了解函数updateTimeZone
feature: Journeys
role: Data Engineer, Architect
level: Experienced
keywords: updateTimeZone，函数，表达式，历程
exl-id: 1bf4662e-55d0-4631-af93-1430ec7ed7e2
source-git-commit: cb1fed2460ddbf3b226fe191b9695008970937c1
workflow-type: tm+mt
source-wordcount: '62'
ht-degree: 9%

---

# updateTimeZone {#updateTimeZone}

返回新的日期时间，同一时刻具有新的时区。

## 类别

日期

## 函数语法

`updateTimeZone(<parameters>)`

## 参数

* 时区id：字符串
* dateTime

## 签名和返回的类型

`updateTimeZone(<dateTime>,<timeZone id>)`

返回日期时间。

## 示例

`updateTimeZone( toDateTime("2019-08-28T08:15:30.123-07:00"), "Europe/Paris"))`

返回2019-08-28T17:15:30.123+02:00。

<!--`updateTimeZone( toDateTime("2019-08-28T08:15:30.123-07:00"), toTimeZone("Europe/Paris")))`
Returns "2019-08-28T17:15:30.123+02:00".-->

`updateTimeZone(@event{MyExpEvent.timestamp}, "Australia/Sydney")`

如果时间戳字段的值为 `2021-11-16T16:55:12.939318+01:00`，则函数会返回 `2021-11-17T02:55:12.942115+11:00`.
