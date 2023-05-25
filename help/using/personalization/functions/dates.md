---
title: 日期时间函数库
description: 日期时间函数库
feature: Personalization
topic: Personalization
role: Data Engineer
level: Experienced
exl-id: edc040de-dfb3-4ebc-91b4-239e10c2260b
source-git-commit: 2444d8fbe3a86feb0497d754b4f57f234fa29e49
workflow-type: tm+mt
source-wordcount: '413'
ht-degree: 4%

---

# 日期时间函数{#date-time}

日期和时间函数用于对Journey Optimizer中的值执行日期和时间操作。

## 年龄{#age}

此 `age` 函数用于从给定日期检索年龄。

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

## 当前时间（以毫秒为单位）{#current-time}

此 `currentTimeInMillis` 函数用于检索当前时间，以纪元毫秒为单位。

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

## 日期差异{#date-diff}

此 `dateDiff` 函数用于检索两个日期之间的天数差。

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


## 每周的某一日{#day-week}

此 `dayOfWeek` 函数用于检索星期几。

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

## 年中哪天{#day-year}

此 `dayOfYear` 函数用于检索每年的某一日。

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

此 `formatDate` 函数用于设置日期时间值的格式。 格式应为有效的Java DateTimeFormat模式。

**语法**

```sql
{%= formatDate(datetime, format) %}
```

其中第一个字符串是日期属性，第二个值是您希望如何转换和显示日期。

>[!NOTE]
>
> 如果日期模式无效，日期将回退到ISO标准格式。
>
> 您可以使用Java日期格式函数，如中所述 [oracle文档](https://docs.oracle.com/javase/8/docs/api/java/time/format/DateTimeFormatter.html){_blank}

**示例**

以下操作将返回以下格式的日期：MM/DD/YY。

```sql
{%= formatDate(profile.timeSeriesEvents._mobile.hotelBookingDetails.bookingDate, "MM/DD/YY") %}
```

## 支持区域设置的日期格式{#format-date-locale}

此 `formatDate` 函数用于将日期时间值格式化为其相应的语言敏感表示形式，即在所需的区域设置中。 格式应为有效的Java DateTimeFormat模式。

**语法**

```sql
{%= formatDate(datetime, format, locale) %}
```

其中第一个字符串是日期属性，第二个值是您希望如何转换和显示日期，第三个值表示字符串格式的区域设置。

>[!NOTE]
>
> 如果日期模式无效，日期将回退到ISO标准格式。
>
> 您可以使用Java日期格式函数，如中所述 [oracle文档](https://docs.oracle.com/javase/8/docs/api/java/time/format/DateTimeFormatter.html).
>
> 您可以使用格式设置和有效区域设置，如中所述 [oracle文档](https://docs.oracle.com/javase/8/docs/api/java/util/Locale.html) 和 [支持的区域设置](https://www.oracle.com/java/technologies/javase/jdk11-suported-locales.html).


**示例**

以下操作将返回以下格式的日期： MM/DD/YY和locale FRANCE。

```sql
{%= formatDate(profile.timeSeriesEvents._mobile.hotelBookingDetails.bookingDate, "MM/DD/YY", "fr_FR") %}
```

## 设置天数{#set-days}

此 `setDays` 函数用于为给定的日期时间设置月中日（该月中的第几天）。

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

## 设置小时{#set-hours}

此 `setHours` 函数用于设置日期时间的小时。

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


## 到UTC{#to-utc}

此 `toUTC` 函数用于将日期时间转换为UTC。


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


## UTC年中的周{#week-of-year}

此 `weekOfYear` 函数用于检索年中周。

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