---
product: journey optimizer
title: updateTimeZone
description: 了解函数updateTimeZone
feature: Journeys
role: Data Engineer, Architect
level: Experienced
keywords: updateTimeZone，函数，表达式，历程
exl-id: 1bf4662e-55d0-4631-af93-1430ec7ed7e2
source-git-commit: 1d30c6ae49fd0cac0559eb42a629b59708157f7d
workflow-type: tm+mt
source-wordcount: '57'
ht-degree: 10%

---

# updateTimeZone {#updateTimeZone}

返回新的日期时间，并在同一时刻使用新时区。

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

`updateTimeZone(@{MyExpEvent.timestamp}, "Australia/Sydney")`

如果时间戳字段的值为 `2021-11-16T16:55:12.939318+01:00`，则函数会返回 `2021-11-17T02:55:12.942115+11:00`.
