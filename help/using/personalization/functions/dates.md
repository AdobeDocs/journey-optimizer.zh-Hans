---
title: 日期时间函数库
description: 日期时间函数库
feature: Personalization
topic: Personalization
role: Data Engineer
level: Experienced
exl-id: edc040de-dfb3-4ebc-91b4-239e10c2260b
source-git-commit: 882b99d9b49e1ae6d0f97872a74dc5a8a4639050
workflow-type: tm+mt
source-wordcount: '262'
ht-degree: 6%

---

# 日期时间函数{#date-time}

日期和时间函数用于对Journey Optimizer中的值执行日期和时间操作。

## 年龄{#age}

的 `age` 函数来检索给定日期的页面。

**格式**

```sql
 {%= age(date) %}
```

<!--
**Example**

The following operation gets the value of the identity map for the key `example@example.com`.

```sql
 {%= age(date) %}
```
-->

## 当前时间（以毫秒为单位）{#current-time}

的 `currentTimeInMillis` 函数用于以新纪元毫秒为单位检索当前时间。

**格式**

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

## 日期差异{#date-diff}

的 `dateDiff` 函数用于以天为单位检索两个日期之间的差异。

**格式**

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


## 每周的某一日{#day-week}

的 `dayOfWeek` 函数用于检索星期。

**格式**

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

## 年中哪天{#day-year}

的 `dayOfYear` 函数用于检索每年的某一天。

**格式**

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

## 格式日期{#format-date}

的 `formatDate` 函数来设置日期时间值的格式。 格式应为有效的Java DateTimeFormat模式。

**格式**

```sql
{%= formatDate(date, format) %}
```

其中，第一个字符串是日期属性，第二个值是您希望转换和显示日期的方式。

>[!NOTE]
>
> 如果日期模式无效，日期将回退到ISO标准格式。
>
> 您可以使用摘要的Java日期格式功能 [oracle文档](https://docs.oracle.com/javase/8/docs/api/java/time/format/DateTimeFormatter.html){_blank}

**示例**

以下操作将以下列格式返回日期：MM/DD/YY。

```sql
{%= formatDate(profile.timeSeriesEvents._mobile.hotelBookingDetails.bookingDate, "MM/DD/YY") %}
```

## 设置天数{#set-days}

的 `setDays` 函数来设置给定日期时间在月中的某天。

**格式**

```sql
{%= setDays(date, day) %}
```

<!--
**Example**

The following operation gets all the values for the map `identityMap`.

```sql
{%= values(identityMap) %}
```
-->

## 设置小时数{#set-hours}

的 `setHours` 函数来设置日期时间的小时数。

**格式**

```sql
{%= setHours(date, hour) %}
```

<!--
**Example**

The following operation gets all the values for the map `identityMap`.

```sql
{%= values(identityMap) %}
```
-->


## 到UTC{#to-utc}

的 `toUTC` 函数将日期时间转换为UTC。


**格式**

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


## 每年的某一周(UTC){#week-of-year}

的 `weekOfYear` 函数用于检索一年中的某周。

**格式**

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
