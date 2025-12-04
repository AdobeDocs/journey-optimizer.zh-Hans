---
product: journey optimizer
title: 转换函数
description: 了解转换函数
feature: Journeys
role: Developer
level: Experienced
keywords: 转化，函数，表达式，历程，类型，转换
version: Journey Orchestration
source-git-commit: 451a9e1e5d5e6e1408849e8d1c5c9644a95359da
workflow-type: tm+mt
source-wordcount: '1054'
ht-degree: 6%

---

# 转换函数 {#conversion-functions}

利用转换函数，您可以在历程表达式中将数据从一种类型转换为另一种类型。 在使用不同的数据源和操作时，这些函数对于确保数据兼容性和正确类型处理至关重要。

当您需要执行以下操作时，请使用转换函数：

* 将字符串值转换为数字、布尔或日期类型([toInteger](#toInteger)，[toDecimal](#toDecimal)，[toBool](#toBool))
* 在不同格式和呈现方式之间转换日期和时间([toDateTime](#toDateTime)，[toDateTimeOnly](#toDateTimeOnly)，[toDateOnly](#toDateOnly))
* 转换介于整数和小数类型([toInteger](#toInteger)，[toDecimal](#toDecimal))之间的数值
* 将值转换为字符串格式([toString](#toString))或持续时间([toDuration](#toDuration))
* 确保比较和操作的类型兼容性
* 处理来自可能具有不同类型格式的外部源的数据

每个转换函数都会自动处理特定于类型的规则和边缘案例，从而使数据转换在历程表达式中更加可靠和可预测。

## toBool {#toBool}

根据类型将参数值转换为布尔值。

* 从字符串：尝试将字符串值转换为布尔值；如果字符串值为“true”，则从“true”；否则从“false”
* 从数值：如果数值不等于0，则为true；否则为false

+++句法

`toBool(<parameter>)`

+++

+++参数

* 小数
* 布尔
* 字符串
* 整数

+++

+++签名和返回的类型

`toBool(<decimal>)`

`toBool(<boolean>)`

`toBool(<string>)`

`toBool(<integer>)`

返回布尔值。

+++

+++示例

`toBool("true")`

`toBool(1)`

返回真。

`toBool("this is not a boolean")`

返回假。

+++

## toDateOnly {#toDateOnly}

将参数转换为dateOnly类型值。 要了解有关数据类型的更多信息，请参阅此[部分](../expression/data-types.md)。

+++句法

`toDateOnly(<parameters>)`

+++

+++参数

| 参数 | 类型 |
|-----------|------------------|
| 以“YYYY-MM-DD”形式表示的日期的字符串（XDM格式）。 还支持ISO-8601格式：仅考虑&#x200B;**完整日期**&#x200B;部分（请参阅[RFC 3339，第5.6](https://www.rfc-editor.org/rfc/rfc3339#section-5.6)节） | 字符串 |
| 日期时间 | dateTime |
| 不带时区的日期时间 | dateTimeOnly |
| 纪元的整数值（以毫秒为单位） | 整数 |

+++

+++签名和返回的类型

`toDateOnly(<dateTime>)`

`toDateOnly(<dateTimeOnly>)`

`toDateOnly(<string>)`

`toDateOnly(<integer>, <integer>, <integer>)`

返回dateOnly类型值。

+++

+++示例

`toDateOnly("2023-08-18")`

`toDateOnly("2023-08-18T00:00:00.000Z")`

`toDateOnly("2023-08-18T00:00:00")`

所有参数都返回表示2023-08-18的dateOnly对象。

`toDateOnly(#{ExperiencePlatform.ProfileFieldGroup.person.birthDate})`

返回dateOnly。

+++

## toDateTime {#toDateTime}

根据参数类型将参数转换为日期时间值。

+++句法

`toDateTime(<parameters>)`

+++

+++参数

| 参数 | 描述 |
|--- |--- |
| 字符串 | ISO-8601格式的日期时间。 包含时区信息的日期时间的字符串表示形式 |
| 字符串 | 时区id。 时区标识符（例如“UTC”、“欧洲/巴黎”） |
| dateOnly | 表示不带时区的日期，以年 — 月 — 日形式查看 |
| dateTimeOnly | 表示不带时区的日期时间，格式为year-month-day-hour-minute-second-millicond |
| 整数 | 纪元的整数值（以毫秒为单位） |

+++

+++签名和返回的类型

`toDateTime(<string>)`

`toDateTime(<string>, <dateOnly>)`

`toDateTime(<string>, <dateTimeOnly>)`

`toDateTime(<integer>)`

返回&#x200B;**日期时间**。

+++

+++示例

`toDateTime("2023-08-18T23:17:59.123Z")`

返回2023-08-18T23:17:59.123Z

ISO-8601字符串已包含时区信息。

`toDateTime("Europe/Paris", toDateOnly("2023-08-18"))`

返回2023-08-18T00:00:00.000+02:00

这通过将时区与仅用于日期的值组合来创建日期时间。 在指定的时区内，时间设置为午夜(00:00:00)。

`toDateTime("UTC", toDateTimeOnly("2023-08-18T23:17:59.123"))`

返回2023-08-18T23:17:59.123Z

这通过将时区应用于dateTimeOnly值（没有时区信息）来创建dateTime。

`toDateTime(1560762190189)`

返回2019-06-17T09:03:10.189Z

将Unix时间戳（以毫秒为单位）转换为dateTime值。

+++

>[!NOTE]
>
>时区ID必须是字符串常量。 它不能是字段引用，也不能是表达式。 有关数据类型的详细信息，请参阅[此页面](../expression/data-types.md)。

## toDateTimeOnly {#toDateTimeOnly}

将参数值转换为仅日期时间值。

+++句法

`toDateTimeOnly(<parameters>)`

+++

+++参数

| 参数 | 类型 |
|-----------|------------------|
| ISO-8601或“YYYY-MM-DD”格式的日期时间（XDM日期格式） | 字符串 |
| 日期时间 | dateTime |

+++

+++签名和返回的类型

`toDateTimeOnly(<dateTime>)`

`toDateTimeOnly(<string>)`

返回不考虑时区的日期时间。

+++

+++示例

`toDateTimeOnly ("2023-08-18")`

返回表示2023-08-18T00:00:00.000的日期时间

`toDateTimeOnly(now())`

+++

## toDecimal {#toDecimal}

根据类型将参数值转换为十进制值。

+++句法

`toDecimal(<parameter>)`

+++

+++参数

| 参数 | 描述 |
|--- |--- |
| 字符串 | 将字符串值转换为小数 |
| dateTime | 将日期转换为毫秒数（纪元毫秒） |
| 布尔 | 如果为true，则将布尔值转换为1；如果为false，则将布尔值转换为0 |
| 整数 | 转换为小数（示例）。：1变为1.0) |

+++

+++签名和返回的类型

`toDecimal(<integer>)`

`toDecimal(<decimal>)`

`toDecimal(<string>)`

`toDecimal(<boolean>)`

返回小数。

+++

+++示例

`toDecimal("4.0")`

返回4.0。

+++

## toDuration {#toDuration}

将参数值转换为持续时间。 有关数据类型的详细信息，请参阅[此页面](../expression/data-types.md)。

+++句法

`toDuration(<parameter>)`

+++

+++参数

| 参数 | 描述 |
|--- |--- |
| 字符串 | 基于ISO-8601持续时间格式PnDTnHnMn.nS的格式，天数被视为刚好24小时 |
| 整数 | 毫秒数 |

如果字符串表达式：接受的格式基于ISO-8601持续时间格式PnDTnHnMn.nS，天数被认为刚好是24小时。

字符串以可选符号开头，由ASCII负号或正号表示。 如果为负值，则整个期间将被否定。 ASCII字母“P”是下一个大写或小写。 然后有四个部分，每个部分包含一个数字和一个后缀。 各节的ASCII后缀为“D”、“H”、“M”和“S”，表示日、小时、分钟和秒，可使用大写或小写。 后缀必须按顺序出现。 ASCII字母“T”必须出现在小时、分钟或秒部分的第一次（如果有）之前。 四个部分中的至少一个必须存在，如果存在“T”，则“T”后面必须至少有一个部分。 每个部分的数字部分必须包含一个或多个ASCII数字。 数字可以用ASCII负号或正号作为前缀。 必须将天数、小时数和分钟数解析为。 必须解析到的秒数以及可选的分数。 小数点可以是点或逗号。 小数部分可以有0到9位数字。

+++

+++签名和返回的类型

`toDuration(<string>)`

`toDuration(<integer>)`

返回持续时间。

+++

+++示例

`toDuration("PT10H")`

返回10小时的持续时间。

`toDuration("PT4S")`

返回4秒的持续时间。

`toDuration(4000)`

返回4秒的持续时间。

+++

## toInteger {#toInteger}

将参数值转换为整数。

+++句法

`toInteger(<parameter>)`

+++

+++参数

| 参数 | 描述 |
|--- |--- |
| 字符串 | 将字符串值转换为整数 |
| dateTime | 将日期转换为毫秒数（纪元毫秒） |
| 小数 | 通过删除小数部分转换为整数（示例：1.5变为1） |
| 布尔 | 如果为true，则将布尔值转换为1；如果为false，则将布尔值转换为0 |

+++

+++签名和返回的类型

`toInteger(<dateTime>)`

`toInteger(<decimal>)`

`toInteger(<integer>)`

`toInteger(<string>)`

`toInteger(<boolean>)`

返回整数。

+++

+++示例

`toInteger("4")`

返回4。

+++

## toString {#toString}

根据类型将参数值转换为字符串值。 有关数据类型的详细信息，请参阅[此页面](../expression/data-types.md)。

+++句法

`toString(<parameter>)`

+++

+++参数

| 参数 | 描述 |
|--- |--- |
| dateTime | 将日期转换为UTC日期格式 |
| dateTimeOnly | 将日期转换为UTC日期格式 |
| 持续时间 | 转换为字符串形式的相应毫秒数 |
| 整数 | 转换为值的字符串表示形式（1变为“1”） |
| 小数 | 转换为值的字符串表示形式（1.5变为“1.5”） |
| 布尔 | 将布尔值转换为“true”（如果为true），“false”（如果为false） |

+++

+++签名和返回的类型

`toString(<dateTimeOnly>)`

`toString(<dateTime>)`

`toString(<duration>)`

`toString(<boolean>)`

`toString(<integer>)`

`toString(<decimal>)`

返回字符串。

+++

+++示例

`toString(4)`

返回“4”。

`toString(#{ExperiencePlatform.test_date.person.birthDate}))`

返回给定dateOnly字段（XDM日期字段）的字符串表示形式，例如“2023-08-18”。

`toString(toDuration(1520))`

返回“PT1.52S”。

+++

