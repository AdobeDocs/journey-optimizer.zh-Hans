---
solution: Journey Optimizer
product: journey optimizer
title: 数据类型
description: 了解高级表达式中的数据类型
feature: Journeys
role: Developer
level: Experienced
keywords: 表达式，数据，数据类型，历程
exl-id: fdfc3287-d733-45fb-ad11-b4238398820a
version: Journey Orchestration
TQID: https://experienceleague.adobe.com/0UKY3G4hyMnSkzh8wlMx-yQ1yymKjs6FuIBdGo1SJqc
product_v2:
  - id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2:
  - id: d998adac-2f81-400b-a669-d07bb196e4eb
role_v2:
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
subfeature_v2: []
source-git-commit: bf5866b0e7437f93936f573fd83ada8526fe004d
workflow-type: tm+mt
source-wordcount: 1124
ht-degree: 3%

---

# 数据类型 {#data-types}

从技术上讲，常量始终包含数据类型。 在文本表达式中，我们仅指定值。 可以从值推断数据类型（例如字符串、整数、小数等）。 对于日期时间等具体情况，我们使用专门的函数进行表示。

以下各部分提供了有关不同数据类型表达式及其表示方式的信息。

## 字符串 {#string}

**描述**

常用字符序列。 除来自环境的隐式大小（例如可用内存量）外，它没有任何特定大小。

JSON格式：字符串

序列化格式：UTF-8

**文本呈现**

```json
"<value>"
```

```json
'<value>'
```

**示例**

```json
"hello world"
```

```json
'hello world'
```

## 整数 {#integer}

**描述**

从–2^63到2^63-1的整数值。

JSON格式：数字

**文本呈现**

```json
<integer value>
```

**示例**

```json
42
```

## 小数 {#decimal}

**描述**

十进制数。 它表示一个浮动值：

* 双精度型的最大正有限值，(2-2^-52)x2^1023
* double类型的最小正正规值，2-1022
* double类型的最小正非零值，2 p-1074

JSON格式：数字

序列化格式：使用“。”作为小数分隔符。

**文本呈现**

```json
<integer value>.<integer value>
```

**示例**

```json
3.14
```

## 布尔 {#boolean}

**描述**

布尔值写入小写： true或false

JSON格式：布尔型

**文本呈现**

```json
true
```

```json
false
```

**示例**

```json
true
```

## dateOnly {#date-only}

**描述**

表示不带时区的日期，以年 — 月 — 日形式查看。

它是日期的描述，用于生日。

json格式：字符串。

格式为：YYYY-MM-DD (ISO-8601)，例如：“2021-03-11”。

它可以封装在toDateOnly函数中。

它使用DateTimeFormatter ISO_LOCAL_DATE_TIME反序列化和序列化该值。 [了解详情](https://datatracker.ietf.org/doc/html/rfc3339#section-5.6)

**文本呈现**

```json
date("<dateOnly in ISO-8601 format>")  
```

**示例**

```json
date("2021-02-19")
```

## dateTimeOnly {#date-time-only}

**描述**

表示不带时区的日期时间，它以年 — 月 — 日 — 小时 — 分钟 — 秒 — 毫秒形式查看。

json格式：字符串。

它不存储或表示时区。 相反，它是对日期的描述（用于生日），与墙上时钟上显示的当地时间相结合。

如果没有偏移或时区等附加信息，它不能表示时间线上的瞬间。

它可以封装在toDateTimeOnly函数中。

序列化格式：ISO-8601扩展偏移日期时间格式。

它使用DateTimeFormatter ISO_LOCAL_DATE_TIME反序列化和序列化该值。 [了解详情](https://docs.oracle.com/javase/8/docs/api/java/time/format/DateTimeFormatter.html#ISO_LOCAL_DATE_TIME”){_blank}。

**文本呈现**

```json
date("<dateTimeOnly in ISO-8601 format>")  
```

**示例**

```json
date("2024-02-19T00.00.000")
date("2024-02-19T00.00")
```

## dateTime {#date-time}

**描述**

日期时间常量，也会考虑时区。 它表示一个日期时间，带有与UTC的偏移。

它可以被视为带有偏移量附加信息的即时时刻。 这是一种在世界特定地点表示特定“时刻”的方式。

json格式：字符串。

它可以封装在toDateTime函数中。

序列化格式：ISO-8601扩展偏移日期时间格式。

它使用DateTimeFormatter ISO_OFFSET_DATE_TIME反序列化和序列化值。 [了解详情](https://docs.oracle.com/javase/8/docs/api/java/time/format/DateTimeFormatter.html#ISO_OFFSET_DATE_TIME){_blank}。

您还可以传递一个传递epoch值的整数。 [了解详情](https://www.epochconverter.com){_blank}。

时区可以通过偏移或时区代码指定（例如：欧洲/巴黎，Z — 表示UTC）。

**文本呈现**

```json
toDateTime("<dateTime in ISO-8601 format>")
```

```json
date("<dateTime in ISO-8601 format>")
```

```json
toDateTime(<integer value of an epoch in milliseconds>)
```

**示例**

```json
date("2024-02-19T00.00.000Z")
```

```json
toDateTime("1977-04-22T06:00:00Z")
```

```json
toDateTime("2023-12-03T15:15:30Z")
```

```json
toDateTime("2023-12-03T15:15:30.123Z")
```

```json
toDateTime("2023-12-03T15:15:30.123+02:00")
```

```json
toDateTime("2023-12-03T15:15:30.123-00:20")
```

```json
toDateTime(1560762190189)
```

## 持续时间 {#duration}

**描述**

它表示基于时间的时间量，如“34.5秒”。 它以毫秒为单位对时间量或时间量建模。

支持的临时单位为：毫秒、秒、分钟、小时、天，其中天等于24小时。 不支持年份和月份，因为它们不是固定时间。

json格式：字符串。

必须将其封装在toDuration函数中。

序列化格式：要反序列化时区ID，它使用java函数java.time。

Duration.parse：可接受的格式基于ISO-8601持续时间格式PnDTnHnMn.nS，天数被认为刚好是24小时。 [了解详情](https://docs.oracle.com/javase/8/docs/api/java/time/Duration.html#parse-java.lang.CharSequence-){_blank}。

**文本呈现**

```json
toDuration("<duration in ISO-8601 format>")
```

```json
toDuration(<duration in milliseconds>)
```

**示例**

```json
toDuration("PT5S") -- parses as 5 seconds
```

```json
toDuration(500) -- parses as 500ms
```

```json
toDuration("PT20.345S") -- parses as "20.345 seconds"
```

```json
toDuration("PT15M") -- parses as "15 minutes" (where a minute is 60 seconds)
```

```json
toDuration("PT10H")  -- parses as "10 hours" (where an hour is 3600 seconds)
```

```json
toDuration("P2D") -- parses as "2 days" (where a day is 24 hours or 86400 seconds)
```

```json
toDuration("P2DT3H4M") -- parses as "2 days, 3 hours and 4 minutes"
```

```json
toDuration("P-6H3M") -- parses as "-6 hours and +3 minutes"
```

```json
toDuration("-P6H3M") -- parses as "-6 hours and -3 minutes"
```

```json
toDuration("-P-6H+3M") -- parses as "+6 hours and -3 minutes"
```

## list {#list}

**描述**

使用方括号作为分隔符的表达式逗号分隔列表。

不支持多态性，因此列表中包含的所有表达式都应具有相同的类型。

**文本呈现**

```json
[<expression>, <expression>, ... ]
```

**示例**

```json
["value1","value2"]
```

```json
[3,5]
```

```json
[toDuration(500),toDuration(800)]
```

+++ AI知识参考

本节包含结构化知识，用于支持与本主题相关的解释、检索和问答。

要全面了解相关信息，应将此信息与本页上的文档相结合。 这两个源都不是独立的；页面描述了功能，而本节提供了其他上下文来帮助消除术语、意图、适用性和约束条件的歧义。

* **TL；DR：**&#x200B;本页介绍了历程高级表达式编辑器支持的每种数据类型（字符串、整数、小数、布尔值、dateOnly、dateTimeOnly、dateTime、持续时间和list）及其JSON格式、序列化规则和文本表示语法。

**意图：**

* 在编写历程表达式时，识别每种数据类型的正确文本语法
* 了解`dateOnly`、`dateTimeOnly`和`dateTime`类型之间的区别以及何时使用每种类型
* 使用ISO-8601格式或毫秒与`toDuration()`函数一起表示持续时间值
* 使用方括号语法构造列表表达式以用于集合操作
* 使用转换函数(`toDateTime`、`toDateTimeOnly`、`toDuration`、`toDateOnly`)创建类型化的常量

**术语表：**

* **dateOnly**：不带时间或时区的日期，格式为YYYY-MM-DD；适用于生日或日历日期&#x200B;*（产品特定）*
* **dateTimeOnly**：没有时区信息的日期和时间；无法表示没有偏移量的特定时刻&#x200B;*（产品特定）*
* **dateTime**：包含UTC偏移量的日期时间常量，表示特定时刻；也可以从纪元整数&#x200B;*（产品特定）*&#x200B;创建
* **持续时间**：基于时间的数量，以毫秒为单位建模；使用ISO-8601 `PnDTnHnMn.nS`格式；不支持年和月&#x200B;*（产品特定）*
* **list**：以逗号分隔的相同类型表达式集合，用方括号&#x200B;*（产品特定）*&#x200B;分隔

**护栏：**

* 持续时间仅支持毫秒、秒、分钟、小时和天 — 不支持年和月，因为它们不是固定的时间量
* `duration`值必须封装在`toDuration()`中 — 它不能表示为空文本
* `list`中的所有表达式必须具有相同的类型 — 不支持多态性
* `dateTimeOnly`无法表示没有额外偏移或时区的即时信息

**术语：**

* 规范名称：数据类型 — 首字母缩略词：none — 变体：表达式数据类型、历程数据类型
* 同义词： &quot;dateTime&quot; = &quot;date-time with timezone&quot;；&quot;dateTimeOnly&quot; = &quot;local date-time&quot;
* 请勿混淆： `dateOnly` （无时间） ≠ `dateTimeOnly` （日期+时间，无时区） ≠ `dateTime` （日期+时间+时区/偏移）

**常见问题解答：**

* **问：`dateTimeOnly`与`dateTime`之间有何区别？** — `dateTimeOnly`没有时区或偏移，无法表示精确的瞬间；`dateTime`包含UTC偏移量并表示特定的时间点。
* **问：我如何表示2天3小时的持续时间？**  — 使用`toDuration("P2DT3H")`。
* **问：可以在列表表达式中混合整数和字符串吗？**  — 否；列表中的所有表达式都必须是同一类型。
* **问：如何从纪元时间戳创建`dateTime`（以毫秒为单位）？**  — 使用`toDateTime(<epoch in milliseconds>)`，例如`toDateTime(1560762190189)`。
* **问：`true`或`True`是否为正确的布尔型？**  — 使用小写`true`或`false`；大写变量无效。

+++
