---
solution: Journey Optimizer
product: journey optimizer
title: 功能
description: 了解函数
feature: Journeys
role: Data Engineer, Architect
level: Experienced
keywords: 函数，表达式，编辑器，历程
exl-id: 5b978eef-7d3e-41fe-bb08-0cf37c3b125d
source-git-commit: d3f0adab52ed8e44a6097c5079396d1e9c06e0a7
workflow-type: tm+mt
source-wordcount: '185'
ht-degree: 68%

---

# 功能 {#functions}

一个函数可以有不同的特征码（一组不同的有序参数）。 函数签名可以有0-N个表达式作为有序参数。

`<function name>`(`<expression as param 1>`， `<expression as param 2>`， ... ，`<expression as param N>`)

每个函数都有一个特定的返回类型。

以下是支持的函数列表。

## 主要函数

| 类别 | 函数 |
|-------------|-----------------------|
| Adobe Experience Platform | [inAudience](../functions/functioninaudience.md) |
| 聚合 | [avg](../functions/functionavg.md) |
| 聚合 | [count](../functions/functioncount.md) |
| 聚合 | [countOnlyNull](../functions/functioncountonlynull.md) |
| 聚合 | [countWithNull](../functions/functioncountwithnull.md) |
| 聚合 | [distinctCount](../functions/functiondistinctcount.md) |
| 聚合 | [distinctCountWithNull](../functions/functiondistinctcountwithnull.md) |
| 聚合 | [max](../functions/functionmax.md) |
| 聚合 | [min](../functions/functionmin.md) |
| 聚合 | [sum](../functions/functionsum.md) |
| 转化 | [toBool](../functions/functiontobool.md) |
| 转化 | [toDateOnly](../functions/functiontodateonly.md) |
| 转化 | [toDateTime](../functions/functiontodatetime.md) |
| 转化 | [toDateTimeOnly](../functions/functiontodatetimeonly.md) |
| 转化 | [toDecimal](../functions/functiontodecimal.md) |
| 转化 | [toDuration](../functions/functiontoduration.md) |
| 转化 | [toInteger](../functions/functiontointeger.md) |
| 转化 | [toString](../functions/functiontostring.md) |
| 日期 | [currentTimeInMillis](../functions/functioncurrenttimeinmillis.md) |
| 日期 | [inLastDays](../functions/functioninlastdays.md) |
| 日期 | [inLastHours](../functions/functioninlasthours.md) |
| 日期 | [inLastMonths](../functions/functioninlastmonths.md) |
| 日期 | [inLastYears](../functions/functioninlastyears.md) |
| 日期 | [inNextDays](../functions/functioninnextdays.md) |
| 日期 | [inNextHours](../functions/functioninnexthours.md) |
| 日期 | [inNextMonths](../functions/functioninnextmonths.md) |
| 日期 | [inNextYears](../functions/functioninnextyears.md) |
| 日期 | [now](../functions/functionnow.md) |
| 日期 | [nowWithDelta](../functions/functionnowwithdelta.md) |
| 日期 | [setHours](../functions/functionsethours.md) |
| 日期 | [setDays](../functions/functionsetdays.md) |
| 日期 | [updateTimeZone](../functions/functionupdatetimezone.md) |
| 列表 | [distinct](../functions/functiondistinct.md) |
| 列表 | [distinctWithNull](../functions/functiondistinctwithnull.md) |
| 列表 | [筛选器](../functions/functionfilter.md) |
| 列表 | [getListItem](../functions/functiongetlistitem.md) |
| 列表 | [in](../functions/functionin.md) |
| 列表 | [相交](../functions/functionintersect.md) |
| 列表 | [限制](../functions/functionlimit.md) |
| 列表 | [listSize](../functions/functionlistsize.md) |
| 列表 | [serializeList](../functions/functionserializelist.md) |
| 列表 | [sort](../functions/functionsort.md) |
| 数学 | [random](../functions/functionrandom.md) |
| 数学 | [round](../functions/functionround.md) |
| 字符串 | [concat](../functions/functionconcat.md) |
| 字符串 | [contain](../functions/functioncontain.md) |
| 字符串 | [containIgnoreCase](../functions/functioncontainwithignorecase.md) |
| 字符串 | [endWith](../functions/functionendwith.md) |
| 字符串 | [endWithIgnoreCase](../functions/functionendwithignorecase.md) |
| 字符串 | [equalIgnoreCase](../functions/functionequalignorecase.md) |
| 字符串 | [indexOf](../functions/functionindexof.md) |
| 字符串 | [isEmpty](../functions/functionisempty.md) |
| 字符串 | [isNotEmpty](../functions/functionisnotempty.md) |
| 字符串 | [lastIndexOf](../functions/functionlastindexof.md) |
| 字符串 | [length](../functions/functionlength.md) |
| 字符串 | [lower](../functions/functionlower.md) |
| 字符串 | [matchRegExp](../functions/functionmatchregexp.md) |
| 字符串 | [notEqualIgnoreCase](../functions/functionnotequalignorecase.md) |
| 字符串 | [replace](../functions/functionreplace.md) |
| 字符串 | [replaceAll](../functions/functionreplaceall.md) |
| 字符串 | [split](../functions/functionsplit.md) |
| 字符串 | [startWith](../functions/functionstartwith.md) |
| 字符串 | [startWithIgnoreCase](../functions/functionstartwithignorecase.md) |
| 字符串 | [substr](../functions/functionsubstr.md) |
| 字符串 | [trim](../functions/functiontrim.md) |
| 字符串 | [upper](../functions/functionupper.md) |
| 字符串 | [uuid](../functions/functionuuid.md) |
