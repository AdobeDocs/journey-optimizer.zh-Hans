---
title: 日期时间函数库
description: 日期时间函数库
feature: Personalization
topic: Personalization
role: Data Engineer
level: Experienced
exl-id: edc040de-dfb3-4ebc-91b4-239e10c2260b
source-git-commit: 3a4a58f8601c67e8e9a2b606a47c6b4bcc2dab05
workflow-type: tm+mt
source-wordcount: '384'
ht-degree: 7%

---

# 日期时间函数{#date-time}

日期和时间函数用于对Journey Optimizer中的值执行日期和时间操作。

## Age{#age}

`age`函数用于从给定日期检索年龄。

**语法**

```sql
 {%= age(datetime) %}
```

<!--
**Example**

The following operation gets the value of the identity map for the key `example@example.com`.

```sql
 {%= age(datetime) %}
```
-->

## Current time in milliseconds{#current-time}

`currentTimeInMillis`函数用于检索当前时间（以纪元毫秒为单位）。

**语法**

```sql
{%= currentTimeInMillis() %}
```

<!--
**Example**

The following operation gets all the keys for the map `identityMap`.

```sql
{%= keys(identityMap) %}
```
-->

## Date difference{#date-diff}

`dateDiff`函数用于检索两个日期之间的天数差。

**语法**

```sql
{%= dateDiff(datetime,datetime) %}
```

<!--
**Example**

The following operation gets all the values for the map `identityMap`.

```sql
{%= values(identityMap) %}
```
-->


## Day of week{#day-week}

`dayOfWeek`函数用于检索星期几。

**语法**

```sql
{%= dayOfWeek(datetime) %}
```

<!--
**Example**

The following operation gets all the values for the map `identityMap`.

```sql
{%= values(identityMap) %}
```
-->

## Day of year{#day-year}

`dayOfYear`函数用于检索一年中的第几天。

**语法**

```sql
{%= dayOfYear(datetime) %}
```

<!--
**Example**

The following operation gets all the values for the map `identityMap`.

```sql
{%= values(identityMap) %}
```
-->

## 设置日期格式{#format-date}

`formatDate`函数用于设置日期时间值的格式。 格式应为有效的Java DateTimeFormat模式。

**语法**

```sql
{%= formatDate(datetime, format) %}
```

其中第一个字符串是日期属性，第二个值是您希望如何转换和显示日期。

>[!NOTE]
>
> 如果日期模式无效，日期将回退到ISO标准格式。
>
> 您可以使用[Oracle文档](https://docs.oracle.com/javase/8/docs/api/java/time/format/DateTimeFormatter.html){_blank}中概述的Java日期格式函数

**示例**

以下操作将返回以下格式的日期：MM/DD/YY。

```sql
{%= formatDate(profile.timeSeriesEvents._mobile.hotelBookingDetails.bookingDate, "MM/dd/YY") %}
```

## 支持区域设置的日期格式{#format-date-locale}

`formatDate`函数用于将日期时间值格式化为相应的语言敏感表示形式，即所需的区域设置。 格式应为有效的Java DateTimeFormat模式。

**语法**

```sql
{%= formatDate(datetime, format, locale) %}
```

其中第一个字符串是日期属性，第二个值是您希望如何转换和显示日期，第三个值以字符串格式表示区域设置。

>[!NOTE]
>
> 如果日期模式无效，日期将回退到ISO标准格式。
>
> 您可以使用[Oracle文档](https://docs.oracle.com/javase/8/docs/api/java/time/format/DateTimeFormatter.html)中概述的Java日期格式函数。
>
> 您可以使用[Oracle文档](https://docs.oracle.com/javase/8/docs/api/java/util/Locale.html)和[支持的区域设置](https://www.oracle.com/java/technologies/javase/jdk11-suported-locales.html)中概述的格式设置和有效区域设置。


**示例**

以下操作将返回以下格式的日期： MM/DD/YY和locale FRANCE。

```sql
{%= formatDate(profile.timeSeriesEvents._mobile.hotelBookingDetails.bookingDate, "MM/DD/YY", "fr_FR") %}
```

## 设置天数{#set-days}

`setDays`函数用于在给定的日期时间设置月中某日。

**语法**

```sql
{%= setDays(datetime, day) %}
```

<!--
**Example**

The following operation gets all the values for the map `identityMap`.

```sql
{%= values(identityMap) %}
```
-->

## 设置小时数{#set-hours}

`setHours`函数用于设置日期时间的小时。

**语法**

```sql
{%= setHours(datetime, hour) %}
```

<!--
**Example**

The following operation gets all the values for the map `identityMap`.

```sql
{%= values(identityMap) %}
```
-->


## To UTC{#to-utc}

`toUTC`函数用于将日期时间转换为UTC。


**语法**

```sql
{%= toUTC(datetime) %}
```

<!--
**Example**

The following operation gets all the values for the map `identityMap`.

```sql
{%= values(identityMap) %}
```
-->


## UTC年周{#week-of-year}

`weekOfYear`函数用于检索年中周。

**语法**

```sql
{%= weekOfYear(datetime) %}
```

<!--
**Example**

The following operation gets all the values for the map `identityMap`.

```sql
{%= values(identityMap) %}
```
-->