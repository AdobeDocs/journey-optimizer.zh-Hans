---
title: 日期时间函数库
description: 日期时间函数库
feature: Personalization
topic: Personalization
role: Data Engineer
level: Experienced
exl-id: edc040de-dfb3-4ebc-91b4-239e10c2260b
source-git-commit: 3eab04f28b1daab556c4b4395d67f28d292fc52b
workflow-type: tm+mt
source-wordcount: '1034'
ht-degree: 11%

---

# 日期时间函数{#date-time}

日期和时间函数用于对Journey Optimizer中的值执行日期和时间操作。

## 添加天数 {#add-days}

`addDays`函数按指定的天数调整给定日期，使用正值递增和负值递减。

**语法**

```sql
{%= addDays(date, number) %}
```

+++示例

* 输入： `{%= addDays(stringToDate("2024-11-01T17:19:51Z"),10) %}`
* 输出： `2024-11-11T17:19:51Z`

+++

## 添加小时数 {#add-hours}

`addHours`函数按指定的小时数调整给定日期，使用正值递增，使用负值递减。

**语法**

```sql
{%= addHours(date, number) %}
```

+++示例

* 输入： `{%= addHours(stringToDate("2024-11-01T17:19:51Z"),1) %}`
* 输出： `2024-11-01T18:19:51Z`

+++

## 添加分钟 {#add-minutes}

`addMinutes`函数按指定的分钟数调整给定日期，使用正值递增，使用负值递减

**语法**

```sql
{%= addMinutes(date, number) %}
```

+++示例

* 输入： `{%= addMinutes(stringToDate("2024-11-01T17:59:51Z"),10) %}`
* 输出： `2024-11-01T18:09:51Z`

+++

## 添加月份 {#add-months}

`addMonths`函数按指定的月数调整给定日期，使用正值递增，使用负值递减。

**语法**

```sql
{%= addMonths(date, number) %}
```

+++示例

* 输入： `{%= addMonths(stringToDate("2024-11-01T17:19:51Z"),2) %}`
* 输出： `2025-01-01T17:19:51Z`

+++

## 添加秒数 {#add-seconds}

`addSeconds`使用正值递增和负值递减将给定日期调整指定的秒数。

**语法**

```sql
{%= addSeconds(date, number) %}
```

+++示例

* 输入： `{%= addSeconds(stringToDate("2024-11-01T17:19:51Z"),10) %}`
* 输出： `2024-11-01T17:20:01Z`

+++

## 添加年份 {#add-years}

`addYears`按指定的年数调整给定日期，使用正值递增和负值递减。

**语法**

```sql
{%= addYears(date, number) %}
```

+++示例

* 输入： `{%= addYears(stringToDate("2024-11-01T17:19:51Z"),2) %}`
* 输出： `2026-11-01T17:19:51Z`

+++

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

## 年龄（以天为单位） {#age-days}

`ageInDays`函数计算给定日期的年龄（以天为单位），即给定日期与当前日期之间经过的天数，对于未来日期为负数，对于过去日期为正数。

**语法**

```sql
{%= ageInDays(date) %}
```

+++示例

currentDate = 2025-01-07T12:17:10.720122+05:30 （亚洲/加尔各答）

* 输入： `{%= ageInDays(stringToDate("2025-01-01T17:19:51Z"))%}`
* 输出： `5`

+++

## 年龄（以月为单位） {#age-months}

`ageInMonths`函数计算给定日期的年龄（以月为单位），即给定日期与当前日期之间经过的月数；对于未来日期为负，对于过去日期为正。

**语法**

```sql
{%= ageInMonths(date) %}
```

+++示例

currentDate = 2025-01-07T12:22:46.993748+05:30（亚洲/加尔各答）

* 输入： `{%=ageInMonths(stringToDate("2024-01-01T00:00:00Z"))%}`
* 输出： `12`

+++

## 比较日期 {#compare-dates}

`compareDates`函数将第一个输入日期与另一个输入日期进行比较。 如果date1等于date2，则返回0；如果date1早于date2，则返回–1；如果date1晚于date2，则返回1。

**语法**

```sql
{%= compareDates(date1, date2) %}
```

+++示例

* 输入： `{%=compareDates(stringToDate("2024-12-02T00:00:00Z"), stringToDate("2024-12-03T00:00:00Z"))%}`
* 输出： `-1`

+++

## 转换分区日期时间 {#convert-zoned-date-time}

`convertZonedDateTime`函数将日期时间转换为给定时区。

**语法**

```sql
{%= convertZonedDateTime(dateTime, timezone) %}
```

+++示例

* 输入： `{%=convertZonedDateTime(stringToDate("2019-02-19T08:09:00Z"), "Asia/Tehran")%}`
* 输出： `2019-02-19T11:39+03:30[Asia/Tehran]`

+++

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

## 每月的第几日 {#day-month}

`dayOfWeek`返回表示月份日期的数字。

**语法**

```sql
{%= dayOfMonth(datetime) %}
```

+++示例

* 输入： `{%= dayOfMonth(stringToDate("2024-11-05T17:19:51Z")) %}`
* 输出： `5`

+++


## Day of week {#day-week}

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

## 秒数差 {#diff-seconds}

`diffInSeconds`函数返回两个日期之间的差值（以秒为单位）。

**语法**

```sql
{%= diffInSeconds(endDate, startDate) %}
```

+++示例

* 输入： `{%=diffInSeconds(stringToDate("2024-11-01T17:19:51Z"), stringToDate("2024-11-01T17:19:01Z"))%}`
* 输出： `50`

+++

## 提取小时数 {#extract-hours}

`extractHours`函数从给定时间戳中提取小时组件。

**语法**

```sql
{%= extractHours(date) %}
```

+++示例

* 输入： `{%= extractHours(stringToDate("2024-11-01T17:19:51Z"))%}`
* 输出： `17`

+++

## 提取分钟数 {#extract-minutes}

`extractMinutes`函数从给定时间戳中提取分钟组件。

**语法**

```sql
{%= extractMinutes(date) %}
```

+++示例

* 输入： `{%= extractMinute(stringToDate("2024-11-01T17:19:51Z"))%}`
* 输出： `19`

+++

## 提取月数 {#extract-months}

`extractMonth`函数从给定时间戳中提取月份组件。

**语法**

```sql
{%= extractMonths(date) %}
```

+++示例

* 输入： `{%=extractMonth(stringToDate("2024-11-01T17:19:51Z"))%}`
* 输出： `11`

+++

## 提取秒数 {#extract-seconds}

`extractSeconds`函数从给定时间戳中提取第二个组件。

**语法**

```sql
{%= extractSeconds(date) %}
```

+++示例

* 输入： `{%=extractSeconds(stringToDate("2024-11-01T17:19:51Z"))%}`
* 输出： `51`

+++

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

## 获取 CurrentZonedDateTime {#get-current-zoned-date-time}

`getCurrentZonedDateTime`函数返回包含时区信息的当前日期和时间。

**语法**

```sql
{%= getCurrentZonedDateTime() %}
```

+++示例

* 输入： `{%= getCurrentZonedDateTime() %}`
* 输出： `2024-12-06T17:22:02.281067+05:30[Asia/Kolkata]`

+++

## 小时数差 {#hours-difference}

`diffInHours`函数返回两个日期之间的小时数差。

**语法**

```sql
{%= diffInHours(endDate, startDate) %}
```

+++示例

* 输入： `{%= diffInHours(stringToDate("2024-11-01T17:19:51Z"), stringToDate("2024-11-01T07:19:51Z"))%}`
* 输出： `10`

+++

## 分钟数差{#diff-minutes}

`diffInMinutes`函数用于返回两个日期之间的分钟数差。

**语法**

```sql
{%= diffInMinutes(endDate, startDate) %}
```

+++示例

* 输入： `{%= diffInMinutes(stringToDate("2024-11-01T17:19:51Z"), stringToDate("2024-11-01T16:19:51Z"))%}`
* 输出： `60`

+++

## 月数差 {#months-difference}

`diffInMonths`函数返回两个日期之间的月数差。

**语法**

```sql
{%= diffInMonths(endDate, startDate) %}
```

+++示例

* 输入： `{%=diffInMonths(stringToDate("2024-11-01T17:19:51Z"), stringToDate("2024-08-01T17:19:51Z"))%}`
* 输出： `3`

+++

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

## To Date Time {#to-date-time}

`ToDateTime`函数将字符串转换为日期。 对于无效的输入，它返回纪元日期作为输出。

**语法**

```sql
{%= toDateTime(string, string) %}
```

+++示例

* 输入： `{%=toDateTime("2024-11-01T17:19:51Z")%}`
* 输出： `2024-11-01T17:19:51Z`

+++

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

## 截断到一天的开始 {#truncate-day}

`truncateToStartOfDay`函数用于将给定日期时间设置为00:00的某天的开始时间，从而修改该日期时间。

**语法**

```sql
{%= truncateToStartOfDay(date) %}
```

+++示例

* 输入： `{%= truncateToStartOfDay(stringToDate("2024-11-01T17:19:51Z")) %}`
* 输出： `2024-11-01T00:00Z`

+++

## 截断到一季度的开始 {#truncate-quarter}

`truncateToStartOfQuarter`函数用于将日期时间截断为其季度的第一天（例如，1月1日、4月1日、7月1日、10月1日），截断时间为00:00。

**语法**

```sql
{%= truncateToStartOfQuarter(dateTime) %}
```

+++示例

* 输入： `{%=truncateToStartOfQuarter(stringToDate("2024-11-01T17:19:51Z"))%}`
* 输出： `2024-10-01T00:00Z`

+++

## 截断到一周的开始 {#truncate-week}

`truncateToStartOfWeek`函数通过将给定日期时间设置为一周的开始（星期一的00:00）来修改该日期。

**语法**

```sql
{%= truncateToStartOfWeek(dateTime) %}
```

+++示例

* 输入： `truncateToStartOfWeek(stringToDate("2024-11-19T17:19:51Z"))%} // tuesday`
* 输出： `2024-11-18T00:00Z // monday`

+++

## 截断到一年的开始 {#truncate-year}

`truncateToStartOfYear`函数用于修改给定的日期时间，方法是在00:00将给定日期时间截断为一年的第一天（1月1日）。

**语法**

```sql
{%= truncateToStartOfYear(dateTime) %}
```

+++示例

* 输入： `{%=truncateToStartOfYear(stringToDate("2024-11-01T17:19:51Z"))%}`
* 输出： `2024-01-01T00:00Z`

+++

## Week of year {#week-of-year}

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

## 年数差异 {#diff-years}

`diffInYears`函数用于返回两个日期之间的年数差。

**语法**

```sql
{%= diffInYears(endDate, startDate) %}: int
```

+++示例

* 输入： `{%=diffInYears(stringToDate("2024-11-01T17:19:51Z"), stringToDate("2019-10-01T17:19:51Z"))%}`
* 输出： `5`

+++
