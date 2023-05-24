---
title: 日期時間函式庫
description: 日期時間函式庫
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

# 日期時間函式{#date-time}

日期和時間函式可用來對Journey Optimizer中的值執行日期和時間作業。

## 年龄{#age}

此 `age` 函式用於從指定日期擷取年齡。

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

## 目前時間（毫秒）{#current-time}

此 `currentTimeInMillis` 函式用於擷取目前時間（以epoch毫秒為單位）。

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

## 日期差異{#date-diff}

此 `dateDiff` 函式來擷取兩個日期之間的天數差異。

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

此 `dayOfWeek` 函式來擷取星期幾。

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

此 `dayOfYear` 函式來擷取一年中的第幾天。

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

## 格式化日期{#format-date}

此 `formatDate` 函式來格式化日期時間值。 格式應為有效的Java DateTimeFormat模式。

**语法**

```sql
{%= formatDate(datetime, format) %}
```

其中第一個字串是日期屬性，第二個值是您希望轉換和顯示日期的方式。

>[!NOTE]
>
> 如果日期模式無效，日期將退回至ISO標準格式。
>
> 您可以使用Java日期格式函式，如中所述 [oracle檔案](https://docs.oracle.com/javase/8/docs/api/java/time/format/DateTimeFormatter.html){_blank}

**示例**

下列作業會以下列格式傳回日期：MM/DD/YY。

```sql
{%= formatDate(profile.timeSeriesEvents._mobile.hotelBookingDetails.bookingDate, "MM/DD/YY") %}
```

## 支援地區設定的日期格式{#format-date-locale}

此 `formatDate` 函式可用來將日期時間值格式化為對應的語言敏感表示法，亦即所需的地區設定。 格式應為有效的Java DateTimeFormat模式。

**语法**

```sql
{%= formatDate(datetime, format, locale) %}
```

其中第一個字串是日期屬性，第二個值是您轉換和顯示日期的方式，第三個值代表字串格式的地區設定。

>[!NOTE]
>
> 如果日期模式無效，日期將退回至ISO標準格式。
>
> 您可以使用Java日期格式函式，如中所述 [oracle檔案](https://docs.oracle.com/javase/8/docs/api/java/time/format/DateTimeFormatter.html).
>
> 您可以使用格式設定和有效地區設定，如中所述 [oracle檔案](https://docs.oracle.com/javase/8/docs/api/java/util/Locale.html) 和 [支援的區域設定](https://www.oracle.com/java/technologies/javase/jdk11-suported-locales.html).


**示例**

下列作業會以下列格式傳回日期： MM/DD/YY和locale FRANCE。

```sql
{%= formatDate(profile.timeSeriesEvents._mobile.hotelBookingDetails.bookingDate, "MM/DD/YY", "fr_FR") %}
```

## 設定天數{#set-days}

此 `setDays` 函式用來設定指定日期時間的月份日期。

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

## 設定小時{#set-hours}

此 `setHours` 函式來設定日期時間的小時。

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

此 `toUTC` 函式用於將日期時間轉換為UTC。


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

此 `weekOfYear` 函式來擷取一年中的周數。

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