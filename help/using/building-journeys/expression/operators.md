---
solution: Journey Optimizer
product: journey optimizer
title: 操作员
description: 了解高级表达式中的运算符
feature: Journeys
role: Developer
level: Experienced
keywords: 表达式、语法、运算符、编辑器、历程
exl-id: 706e2e02-9bd9-46e7-a73d-dda3c9ae4ba8
version: Journey Orchestration
TQID: https://experienceleague.adobe.com/sK2GNHkkiJ4M5V99Uucc-b68iESNW7kCNBjHVNT-dMs
product_v2:
  - id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2:
  - id: d998adac-2f81-400b-a669-d07bb196e4eb
role_v2:
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
subfeature_v2: []
source-git-commit: bf5866b0e7437f93936f573fd83ada8526fe004d
workflow-type: tm+mt
source-wordcount: 1001
ht-degree: 3%

---

# 操作员 {#operators}

运算符分为二类：一元运算符和二元运算符。 有左一元运算符和右一元运算符。

```json
// left-hand unary operators
// <operator> <operand> 
// operand is an expression
not (@event{LobbyBeacon.endUserIDs._experience.emailid.id}=="example@adobe.com")

// right-hand unary operators
// <operator> <operand> 
// operand is an expression
@event{LobbyBeacon.endUserIDs._experience.emailid.id} is not null

// binary operators
// <operand1> <operator> <operand2>
// operand is an expression
(@event{LobbyBeacon.endUserIDs._experience.emailid.id}=="example1@adobe.com") or (@event{LobbyBeacon.endUserIDs._experience.emailid.id}=="example2@adobe.com") 
```

## 重要说明{#important-notes}

* 使用乘法(`*`)时，两个操作字段必须具有相同的类型，可以是整数或小数。 示例：
   * 以下示例是正确的： `3.0 * 4.0`
   * `3 * 4.0`将导致错误

* 使用`+`运算符时，表达式需要封装在括号中。 示例：
   * `toDateTimeOnly(toDateTime((currentTimeInMillis()) + 1))`正确
   * `toDateTimeOnly(toDateTime(currentTimeInMillis() + 1))`将导致错误

## 逻辑  {#logical}

### 和

```json
<expression1> and <expression2>
```

&lt;expression1>和&lt;expression2>都必须是布尔值。 结果是布尔值。

示例：

```json
3.14 > 2 and 3.15 < 1
```

### 或

```json
<expression1> or <expression2>
```

&lt;expression1>和&lt;expression2>都必须是布尔值。 结果是布尔值。

示例：

```json
3.14 > 2 or 3.15 < 1
```

### 非

```json
not <expression>
```

&lt;expression>必须为布尔值。 结果是布尔值。

示例：

```json
not 3.15 < 1
```

## 比较 {#comparison}

### 为空

```json
<expression> is null
```

结果是布尔值。

请注意，null表示表达式没有计算值。

示例：

```json
@event{BarBeacon.location} is null
```

### 不为null

```json
<expression> is not null
```

结果是布尔值。

请注意，null表示表达式没有计算值。

示例：

```json
@event{BarBeacon.location} is not null
```

### 为空

```json
<expression> has null
```

&lt;expression>必须为列表。 结果是布尔值。

用于标识列表是否包含至少一个null值。

示例：

```json
["foo", "bar", null] has null
```

返回true

```json
["foo", "bar", ""] has null
```

返回false，因为“”不视为null。

### ==

```json
<expression1> == <expression2>
```

>[!NOTE]
>
>对于&lt;expression1>和&lt;expression2>，没有数据类型控件。

示例：

```json
3.14 == 42
```

```json
"foo" == "bar"
```

### !=

```json
<expression1> != <expression2>
```

>[!NOTE]
>
>对于&lt;expression1>和&lt;expression2>，没有数据类型控件。

结果是布尔值。

示例：

```json
3.14 != 42
```

```json
"foo" != "bar"
```

### >

```json
<expression1> > <expression2>
```

日期时间可以与日期时间进行比较。

只能将Datetimeonly与Datetimeonly进行比较。

整数或小数都可与整数或小数进行比较。

禁止任何其他组合。

结果是布尔值。

示例：

```json
3.14 > 42
```

### >=

```json
<expression1> >= <expression2>
```

日期时间可以与日期时间进行比较。

只能将Datetimeonly与Datetimeonly进行比较。

整数或小数都可与整数或小数进行比较。

禁止任何其他组合。

结果是布尔值。

示例：

```json
42 >= 3.14
```

### &lt;

```json
<expression1> < <expression2>
```

日期时间可以与日期时间进行比较。

只能将Datetimeonly与Datetimeonly进行比较。

整数或小数都可与整数或小数进行比较。

禁止任何其他组合。

结果是布尔值。

示例：

```json
42 < 3.14
```

### &lt;=

```json
<expression1> <= <expression2>
```

日期时间可以与日期时间进行比较。

只能将Datetimeonly与Datetimeonly进行比较。

整数或小数都可与整数或小数进行比较。

禁止任何其他组合。

结果是布尔值。

示例：

```json
42 <= 3.14
```

## 算术 {#arithmetic}

### +

```json
<expression1> + <expression2>
```

两个表达式都必须是数字（整数或小数）。

结果也是数字。

示例：

```json
1 + 2
```

返回3

### -

```json
<expression1> - <expression2>
```

两个表达式都必须是数字（整数或小数）。

结果也是数字。

示例：

```json
2 - 1 
```

返回1

### /

```json
<expression1> / <expression2>
```

两个表达式都必须是数字（整数或小数）。

结果也是数字。

&lt;expression2>不能等于0（返回0）。

示例：

```json
4 / 2
```

返回2

### *

```json
<expression1> * <expression2>
```

两个表达式都必须是数字（整数或小数）。

结果也是数字。

示例：

```json
3 * 4
```

返回12

### %

```json
<expression1> % <expression2>
```

两个表达式都必须是数字（整数或小数）。

结果也是数字。

示例：

```json
3 % 2
```

返回1。

## 数学 {#math}

### 是数字

```json
<expression> is numeric
```

表达式的类型为整数或小数。

示例：

```json
@ is numeric
```

### 为整数

```json
<expression> is integer
```

表达式的类型为integer。

示例：

```json
@ is integer
```

### 为小数

```json
<expression> is decimal
```

表达式的类型为小数。

示例：

```json
@ is decimal
```

## 字符串 {#string}

### +

```json
<string> + <expression>
```

```json
<expression> + <string>
```

它连接两个表达式。

一个表达式必须是链接字符串。

示例：

```json
"the current time is " + (now())
```

返回“当前时间为2023-09-23T09:30:06.693Z”

```json
(now()) + " is the current time"
```

返回“2023-09-23T09:30:06.693Z是当前时间”

```json
"a" + "b" + "c" + 1234
```

返回“abc1234”。

## 日期 {#date}

### +

```json
<expression> + <duration>
```

将持续时间附加到dateTime、dateTimeOnly或duration。

示例：

```json
(toDateTime("2023-12-03T15:15:30Z")) + (toDuration("PT15M"))  
```

返回&#x200B;_dateTime_ 2023-12-03T15:30:30Z

```json
(toDateTimeOnly("2023-12-03T15:15:30")) + (toDuration("PT15M"))
```

返回&#x200B;_dateTimeOnly_ 2023-12-03T15:30:30

```json
(now()) + (toDuration("PT1H"))
```

从当前时间后一小时返回&#x200B;_dateTime_（具有UTC时区）

```json
(toDuration("PT1H")) + (toDuration("PT1H"))
```

返回&#x200B;_持续时间_ PT2H

+++ AI知识参考

本节包含结构化知识，用于支持与本主题相关的解释、检索和问答。

要全面了解相关信息，应将此信息与本页上的文档相结合。 这两个源都不是独立的；页面描述了功能，而本节提供了其他上下文来帮助消除术语、意图、适用性和约束条件的歧义。

* **TL；DR：**&#x200B;此页是历程高级表达式编辑器中可用运算符的完整引用，涵盖逻辑(`and`、`or`、`not`)、比较(`==`、`!=`、`>`、`>=`、`<`、`<=`、`is null`、`is not null`、`has null`)、算术(`+`、`-`、`/`、`*`、`%`)、数学类型检查(`is numeric`、`is integer`、`is decimal`)、字符串连接和日期算术运算符。

**意图：**

* 使用逻辑运算符`and`、`or`和`not`组合布尔条件
* 使用`is null` / `is not null`检查字段或表达式值是否为null或不为null
* 使用`has null`运算符检测列表中的null值
* 使用`>`、`>=`、`<`、`<=`、`==`和`!=`比较数值、日期时间和仅日期时间值
* 使用`+`、`-`、`/`、`*`和`%`对数值执行算术
* 使用`+`运算符将持续时间添加到dateTime、dateTimeOnly或duration值

**术语表：**

* **一元运算符**：应用于单个操作数的运算符；可以为左侧（例如`not`）或右侧（例如`is null`） *（产品特定）*
* **二进制运算符**：在两个操作数（例如`and`，`==`，`+`） *（产品特定）*&#x200B;之间应用的运算符
* **具有null**：如果列表至少包含一个null元素&#x200B;*（产品特定）*，则右边一元运算符会返回true
* **是数字/是整数/是十进制**：类型检查运算符根据表达式&#x200B;*（特定于产品）的数值子类型返回布尔值*

**护栏：**

* 使用乘法(`*`)时，两个操作数必须是相同的数字类型（整数或小数两者） — 混合类型会导致错误
* 在日期算术中使用`+`运算符时，表达式必须用括号括起来，以避免出现分析错误
* 比较运算符(`>`、`>=`、`<`、`<=`)仅在兼容类型之间有效：带有Datetime的Datetime、带有DatetimeOnly的DatetimeOnly或带有数值的numeric — 禁止任何其他组合
* 空字符串`""`不视为null — `has null`对包含`""`的列表返回false
* `==`和`!=`运算符在操作数之间不执行数据类型控制

**术语：**

* 规范名称：运算符 — 首字母缩写：none — 变体：表达式运算符、历程运算符
* 同义词： `and` = &quot;logical AND&quot;；`or` = &quot;logical OR&quot;；`not` = &quot;logical NOT&quot;；`%` = &quot;modulo&quot;
* 请勿混淆： `is null` （表达式没有计算值）≠ `== null` （不是有效的语法）； `has null` （列表包含null）≠ `is null` （表达式本身为null）

**常见问题解答：**

* **问：能否将整数直接乘以小数？**  — 否；`*`的两个操作数都必须是同一类型。 使用`3.0 * 4.0`（小数）或`3 * 4`（整数）。
* **问：如何向dateTime添加15分钟？**  — 使用`(toDateTime("...")) + (toDuration("PT15M"))`。
* **问：`is null`与`has null`之间有何区别？** — `is null`检查单个表达式是否没有计算值；`has null`检查列表是否包含至少一个null元素。
* **问：`"" has null`是否返回true？**  — 否；不将空字符串视为null，因此结果为false。
* **问：为什么`3 * 4.0`会导致错误？** — `*`运算符要求两个操作数必须是相同的数字类型；不允许混合使用整数和小数。

+++
