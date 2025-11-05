---
solution: Journey Optimizer
product: journey optimizer
title: 函数
description: 了解函数
feature: Journeys
role: Developer
level: Experienced
keywords: 函数，表达式，编辑器，历程
exl-id: 5b978eef-7d3e-41fe-bb08-0cf37c3b125d
version: Journey Orchestration
source-git-commit: d58319d687d113ce680c415524fdea0400cb38f0
workflow-type: tm+mt
source-wordcount: '185'
ht-degree: 69%

---

# 函数 {#functions}

一个函数可以有不同的特征码（一组不同的有序参数）。 函数签名可以有0-N个表达式作为有序参数。

`<function name>`(`<expression as param 1>`， `<expression as param 2>`， ... ，`<expression as param N>`)

每个函数都有一个特定的返回类型。

以下是支持的函数列表。

## 主要函数

| 类别 | 函数 |
|-------------|-----------------------|
| Adobe Experience Platform | [inAudience](../functions/functioninaudience.md) |
| 聚合 | [avg](../functions/aggregation-functions.md#avg) |
| 聚合 | [count](../functions/aggregation-functions.md#count) |
| 聚合 | [countOnlyNull](../functions/aggregation-functions.md#countOnlyNull) |
| 聚合 | [countWithNull](../functions/aggregation-functions.md#countWithNull) |
| 聚合 | [distinctCount](../functions/aggregation-functions.md#distinctCount) |
| 聚合 | [distinctCountWithNull](../functions/aggregation-functions.md#distinctCountWithNull) |
| 聚合 | [max](../functions/aggregation-functions.md#max) |
| 聚合 | [min](../functions/aggregation-functions.md#min) |
| 聚合 | [sum](../functions/aggregation-functions.md#sum) |
| 转化 | [toBool](../functions/conversion-functions.md#toBool) |
| 转化 | [toDateOnly](../functions/conversion-functions.md#toDateOnly) |
| 转化 | [toDateTime](../functions/conversion-functions.md#toDateTime) |
| 转化 | [toDateTimeOnly](../functions/conversion-functions.md#toDateTimeOnly) |
| 转化 | [toDecimal](../functions/conversion-functions.md#toDecimal) |
| 转化 | [toDuration](../functions/conversion-functions.md#toDuration) |
| 转化 | [toInteger](../functions/conversion-functions.md#toInteger) |
| 转化 | [toString](../functions/conversion-functions.md#toString) |
| 日期 | [currentTimeInMillis](../functions/date-functions.md#currentTimeInMillis) |
| 日期 | [inLastDays](../functions/date-functions.md#inLastDays) |
| 日期 | [inLastHours](../functions/date-functions.md#inLastHours) |
| 日期 | [inLastMonths](../functions/date-functions.md#inLastMonths) |
| 日期 | [inLastYears](../functions/date-functions.md#inLastYears) |
| 日期 | [inNextDays](../functions/date-functions.md#inNextDays) |
| 日期 | [inNextHours](../functions/date-functions.md#inNextHours) |
| 日期 | [inNextMonths](../functions/date-functions.md#inNextMonths) |
| 日期 | [inNextYears](../functions/date-functions.md#inNextYears) |
| 日期 | [now](../functions/date-functions.md#now) |
| 日期 | [nowWithDelta](../functions/date-functions.md#nowWithDelta) |
| 日期 | [setHours](../functions/date-functions.md#setHours) |
| 日期 | [setDays](../functions/date-functions.md#setDays) |
| 日期 | [updateTimeZone](../functions/date-functions.md#updateTimeZone) |
| 列表 | [distinct](../functions/list-functions.md#distinct) |
| 列表 | [distinctWithNull](../functions/list-functions.md#distinctWithNull) |
| 列表 | [筛选器](../functions/list-functions.md#filter) |
| 列表 | [getListItem](../functions/list-functions.md#getListItem) |
| 列表 | [in](../functions/list-functions.md#in) |
| 列表 | [相交](../functions/list-functions.md#intersect) |
| 列表 | [限制](../functions/list-functions.md#limit) |
| 列表 | [listSize](../functions/list-functions.md#listSize) |
| 列表 | [serializeList](../functions/list-functions.md#serializeList) |
| 列表 | [sort](../functions/list-functions.md#sort) |
| 数学 | [random](../functions/functionrandom.md) |
| 数学 | [round](../functions/functionround.md) |
| 字符串 | [concat](../functions/string-functions.md#concat) |
| 字符串 | [contain](../functions/string-functions.md#contain) |
| 字符串 | [containIgnoreCase](../functions/string-functions.md#containIgnoreCase) |
| 字符串 | [endWith](../functions/string-functions.md#endWith) |
| 字符串 | [endWithIgnoreCase](../functions/string-functions.md#endWithIgnoreCase) |
| 字符串 | [equalIgnoreCase](../functions/string-functions.md#equalIgnoreCase) |
| 字符串 | [indexOf](../functions/string-functions.md#indexOf) |
| 字符串 | [isEmpty](../functions/string-functions.md#isEmpty) |
| 字符串 | [isNotEmpty](../functions/string-functions.md#isNotEmpty) |
| 字符串 | [lastIndexOf](../functions/string-functions.md#lastIndexOf) |
| 字符串 | [length](../functions/string-functions.md#length) |
| 字符串 | [lower](../functions/string-functions.md#lower) |
| 字符串 | [matchRegExp](../functions/string-functions.md#matchRegExp) |
| 字符串 | [notEqualIgnoreCase](../functions/string-functions.md#notEqualIgnoreCase) |
| 字符串 | [replace](../functions/string-functions.md#replace) |
| 字符串 | [replaceAll](../functions/string-functions.md#replaceAll) |
| 字符串 | [split](../functions/string-functions.md#split) |
| 字符串 | [startWith](../functions/string-functions.md#startWith) |
| 字符串 | [startWithIgnoreCase](../functions/string-functions.md#startWithIgnoreCase) |
| 字符串 | [substr](../functions/string-functions.md#substr) |
| 字符串 | [trim](../functions/string-functions.md#trim) |
| 字符串 | [upper](../functions/string-functions.md#upper) |
| 字符串 | [uuid](../functions/string-functions.md#uuid) |
