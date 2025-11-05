---
product: journey optimizer
title: 日期函数
description: 了解日期函数
feature: Journeys
role: Developer
level: Experienced
keywords: 日期，函数，表达式，历程，时间
version: Journey Orchestration
source-git-commit: bb47ca4957129a4d05aa3d7286409eef0cb62143
workflow-type: tm+mt
source-wordcount: '791'
ht-degree: 12%

---

# 日期函数 {#date-functions}

通过日期函数，您可以在历程表达式中处理并使用日期和时间值。 这些函数对于客户历程中基于时间的条件、计划和时间计算至关重要。

当您需要以下任务时，请使用日期函数：

* 获取具有特定时区处理的当前时间或日期([now](#now)，[nowWithDelta](#nowWithDelta)，[currentTimeInMillis](#currentTimeInMillis))
* 检查日期是否在特定时间范围内([inLastDays](#inLastDays)，[inLastHours](#inLastHours)，[inLastMonths](#inLastMonths)，[inLastYears](#inLastYears)，[inNextDays](#inNextDays)，[inNextHours](#inNextHours)，[inNextMonths](#inNextMonths)，[inNextYears](#inNextYears))
* 修改日期和时间组件([setHours](#setHours)，[setDays](#setDays)，[updateTimeZone](#updateTimeZone))
* 执行基于时间的计算和比较
* 在不同时间格式和表示法之间转换

日期函数提供了对时间逻辑的精确控制，允许您创建对时间敏感的历程路径和条件，以响应特定时间范围和计划。

## currentTimeInMillis {#currentTimeInMillis}

返回当前时间（以纪元毫秒为单位）。

+++句法

`currentTimeInMillis()`

+++

+++参数

此函数不使用参数。

+++

+++签名和返回的类型

`currentTimeInMillis()`

返回整数。

+++

+++示例

`currentTimeInMillis()`

返回“1544712617131”。

+++

## inLastDays {#inLastDays}

如果给定的dateTime介于现在和现在之间 — 增量天，则返回true。

+++句法

`inLastDays(<dateTime>,<delta>)`

+++

+++参数

| 参数 | 类型 |
|-----------|------------------|
| 日期时间 | dateTime |
| 增量 | 整数 |

+++

+++签名和返回的类型

`inLastDays(<dateTime>,<integer>)`

返回布尔值。

+++

+++示例

`inLastDays(toDateTime('2023-12-12T01:11:00Z'), 4)`

返回真。

+++

## inLastHours {#inLastHours}

如果给定的日期时间介于现在和现在之间 — 增量小时，则返回true。

+++句法

`inLastHours(<dateTime>,<delta>)`

+++

+++参数

| 参数 | 类型 |
|-----------|------------------|
| 日期时间 | dateTime |
| 增量 | 整数 |

+++

+++签名和返回的类型

`inLastHours(<dateTime>,<integer>)`

返回布尔值。

+++

+++示例

`inLastHours(toDateTime('2023-12-12T01:11:00Z'), 4)`

返回真。

`inLastHours(@event{MyEvent.timestamp}, 4)`

返回真。

+++

## inLastMonths {#inLastMonths}

如果给定的日期或日期时间介于现在和现在之间 — 增量月份，则返回true。

+++句法

`inLastMonths(<dateTime>,<delta>)`

+++

+++参数

| 参数 | 类型 |
|-----------|------------------|
| 日期时间 | dateTime |
| 增量 | 整数 |

+++

+++签名和返回的类型

`inLastMonths(<dateTime>,<integer>)`

返回布尔值。

+++

+++示例

`inLastMonths(toDateTime('2023-12-12T01:11:00Z'), 4)`

返回真。

+++

## inLastYears {#inLastYears}

如果给定的日期或日期时间介于现在和现在之间 — 增量年，则返回true。

+++句法

`inLastYears(<dateTime>,<delta>)`

+++

+++参数

| 参数 | 类型 |
|-----------|------------------|
| 日期时间 | dateTime |
| 增量 | 整数 |

+++

+++签名和返回的类型

`inLastYears(<dateTime>,<integer>)`

返回布尔值。

+++

+++示例

`inLastYears(toDateTime('2023-12-12T01:11:00Z'), 4)`

返回真。

+++

## inNextDays {#inNextDays}

如果给定的日期或日期时间介于现在和现在+增量天之间，则返回true。

+++句法

`inNextDays(<dateTime>,<delta>)`

+++

+++参数

| 参数 | 类型 |
|-----------|------------------|
| 日期时间 | dateTime |
| 增量 | 整数 |

+++

+++签名和返回的类型

`inNextDays(<dateTime>,<integer>)`

返回布尔值。

+++

+++示例

`inNextDays(toDateTime('2023-12-12T01:11:00Z'), 4)`

返回真。

+++

## inNextHours {#inNextHours}

如果给定的日期或日期时间介于现在和现在+增量小时数之间，则返回true。

+++句法

`inNextHours(<dateTime>,<delta>)`

+++

+++参数

| 参数 | 类型 |
|-----------|------------------|
| 日期时间 | dateTime |
| 增量 | 整数 |

+++

+++签名和返回的类型

`inNextHours(<dateTime>,<integer>)`

返回布尔值。

+++

+++示例

`inNextHours(toDateTime('2023-12-12T01:11:00Z'), 4)`

返回真。

+++

## inNextMonths {#inNextMonths}

如果给定的日期或日期时间介于现在和现在+增量月份之间，则返回true。

+++句法

`inNextMonths(<dateTime>,<delta>)`

+++

+++参数

| 参数 | 类型 |
|-----------|------------------|
| 日期时间 | dateTime |
| 增量 | 整数 |

+++

+++签名和返回的类型

`inNextMonths(<dateTime>,<integer>)`

返回布尔值。

+++

+++示例

`inNextMonths(toDateTime('2023-01-12T01:11:00Z'), 4)`

返回真。

+++

## inNextYears {#inNextYears}

如果给定的日期或日期时间介于现在和现在+增量年之间，则返回true。

+++句法

`inNextYears(<dateTime>,<delta>)`

+++

+++参数

| 参数 | 类型 |
|-----------|------------------|
| 日期时间 | dateTime |
| 增量 | 整数 |

+++

+++签名和返回的类型

`inNextYears(<dateTime>,<integer>)`

返回布尔值。

+++

+++示例

`inNextYears(toDateTime('2021-12-12T01:11:00Z'), 4)`

返回真。

+++

## now {#now}

以日期时间格式返回当前日期。 有关数据类型的详细信息，请参阅[此页面](../expression/data-types.md)。

+++句法

`now(<parameter>)`

+++

+++参数

| 参数 | 描述 |
|--- |--- |
| 字符串 | 时区标识符（可选） |

+++

+++签名和返回的类型

`now()`

`now("<timeZone id>")`

返回日期时间。

+++

+++示例

`now()`

返回2023-06-03T06:30Z。

`toString(now())`

返回“2023-06-03T06:30Z”

`now("Europe/Paris")`

返回2023-06-03T08:30+02:00。

+++

## nowWithDelta {#nowWithDelta}

返回包含偏移量的当前日期时间。 如果指定了时区ID，将应用时区偏移。 有关数据类型的详细信息，请参阅[此页面](../expression/data-types.md)。

+++句法

`nowWithDelta(<parameters>)`

+++

+++参数

| 参数 | 描述 |
|--- |--- |
| 增量 | 正或负整数值 |
| 日期部分 | 年、月、日、小时、分钟或秒 |
| 时区id | 时区值的字符串表示形式。 有关详细信息，请参阅[数据类型](../expression/data-types.md)。 时区ID必须是字符串常量。 它不能是字段引用，也不能是表达式。 |

+++

+++签名和返回的类型

`nowWithDelta(<delta>,<date part>`

`nowWithDelta(<delta>,<date part>,"<timeZone id>")`

返回日期时间。

+++

+++示例

`nowWithDelta(-2, "hours")`

`nowWithDelta(-2, "hours", "Europe/Paris")`

返回2小时前的dateTime。

+++

## setHours {#setHours}

仅设置日期时间或日期时间的小时。 例如，如果您要等到明天的某个小时，则可以强制执行该小时。

+++句法

`setHours(<parameter>)`

+++

+++参数

| 参数 | 类型 |
|--- |--- |
| 日期时间 | dateTime |
| 不考虑时区的日期时间 | dateTimeOnly |
| 小时 | 整数 |

+++

+++签名和返回的类型

`setHours(<dateTime>,<hours>)`

返回日期时间。

`setHours(<dateTimeOnly>,<hours>)`

返回不考虑时区的日期时间。

+++

+++示例

`setHours(toDateTime('2023-12-12T01:11:00Z'), 4)`

返回2023-12-12T04:11:00Z。

`setHours(nowWithDelta(1, "days"), 20)`

返回明天晚上8:XY，XY是当前时间评估时刻的分钟数。 如果评估发生在凌晨2:45，则返回的时间将为晚上8:45。

+++

## setDays {#setDays}

仅设置日期时间或日期时间的日期。 例如，如果您要等到月份的某一天，则可以强制该天。

+++句法

`setDays(<parameter>)`

+++

+++参数

| 参数 | 类型 |
|--- |--- |
| 日期时间 | dateTime |
| 不考虑时区的日期时间 | dateTimeOnly |
| 天数 | 整数 |

+++

+++签名和返回的类型

`setDays(<dateTime>,<days>)`

返回日期时间。

`setDays(<dateTimeOnly>,<days>)`

返回不考虑时区的日期时间。

+++

+++示例

`setDays(toDateTime('2023-12-12T01:11:00Z'), 25)`

返回2023-12-25T01:11:00Z。

`setDays(toDateTimeOnly(@event{MyEvent.registrationDate}), 1)`

+++

## updateTimeZone {#updateTimeZone}

返回新的日期时间，同一时刻具有新的时区。

+++句法

`updateTimeZone(<parameters>)`

+++

+++参数

* 时区id：字符串
* dateTime

+++

+++签名和返回的类型

`updateTimeZone(<dateTime>,<timeZone id>)`

返回日期时间。

+++

+++示例

`updateTimeZone( toDateTime("2023-08-28T08:15:30.123-07:00"), "Europe/Paris"))`

返回2023-08-28T17:15:30.123+02:00。

`updateTimeZone(@event{MyExpEvent.timestamp}, "Australia/Sydney")`

如果时间戳字段的值为`2021-11-16T16:55:12.939318+01:00`，则函数返回`2021-11-17T02:55:12.942115+11:00`。

+++

