---
product: journey optimizer
title: 聚合函数
description: 了解聚合函数
feature: Journeys
role: Developer
level: Experienced
keywords: 聚合，函数，表达式，历程，平均，计数，最大值，最小值，总和
version: Journey Orchestration
source-git-commit: af1babe501a5b2c6a67730396a8f5e2c5d85e60a
workflow-type: tm+mt
source-wordcount: '635'
ht-degree: 8%

---

# 聚合函数 {#aggregation-functions}

聚合函数用于对一组值执行计算并返回单个值。 在历程表达式中使用列表和数组时，这些函数特别有用。

## avg {#avg}

返回一组表达式中的平均值，这些表达式以列表或两个表达式形式给定。 Null值将被忽略。

+++句法

`avg(<parameter>)`

+++

+++参数

支持的类型：

* listInteger
* listDecimal
* 小数
* 整数

+++

+++签名和返回的类型

`avg(<listInteger>)`

`avg(<listDecimal>)`

`avg(<decimal>,<decimal>)`

`avg(<decimal>,<integer>)`

`avg(<integer>,<decimal>)`

`avg(<integer>,<integer>)`

返回小数。

+++

+++示例

`avg(@event{BarBeacon.inventory},5)`

`avg([10,3,8])`

返回7.0。

`avg(10.2, 3)`

返回6.6。

+++

## count {#count}

计算列表的元素，而不考虑null值。

+++句法

`count(<listAny>)`

`count(<listObject>)`

+++

+++参数

| 参数 | 类型 | 描述 |
|-----------|------------------|------------------|
| listToProcess | listString、listBoolean、listInteger、listDecimal、listDuration、listDateTime、listDateTimeOnly、listDateOnly或listObject | 要处理的列表。 对于listObject，它必须是字段引用。 listObject不能包含null对象。 |

+++

+++签名和返回的类型

`count(<listAny>)`

返回整数。

+++

+++示例

`count([10,2,10,null])`

返回3。

`count(@event{my_event.productListItems})`

返回给定对象数组（listObject类型）中的对象数。 备注： listObject不能包含null对象

+++

## countOnlyNull {#countOnlyNull}

计算列表中的空值的数量。

**注意：**&#x200B;此函数不支持参数`<listObject>`。

+++句法

`countOnlyNull(<listAny>)`

+++

+++参数

| 参数 | 类型 |
|-----------|------------------|
| listToProcess | listString、listBoolean、listInteger、listDecimal、listDuration、listDateTime、listDateTimeOnly、listDateOnly |

+++

+++签名和返回的类型

`countOnlyNull(<listAny>)`

返回整数。

+++

+++示例

`countOnlyNull([10,2,10,null])`

返回1。

+++

## countWithNull {#countWithNull}

计算列表的所有元素，包括null值。

**注意：**&#x200B;此函数不支持参数`<listObject>`。

+++句法

`countWithNull(<listAny>)`

+++

+++参数

| 参数 | 类型 |
|-----------|------------------|
| listToProcess | listString、listBoolean、listInteger、listDecimal、listDuration、listDateTime、listDateTimeOnly、listDateOnly |

+++

+++签名和返回的类型

`countWithNull(<listAny>)`

返回整数。

+++

+++示例

`countWithNull([10,2,10,null])`

返回4。

+++

## distinctCount {#distinctCount}

计算不同值的数量，忽略空值。

+++句法

`distinctCount(<listAny>)`

+++

+++参数

| 参数 | 类型 | 描述 |
|-----------|------------------|------------------|
| listToProcess | listString、listBoolean、listInteger、listDecimal、listDuration、listDateTime、listDateTimeOnly、listDateOnly或listObject | 要处理的列表。 对于listObject，它必须是字段引用。 |
| keyAttributeName | 字符串 | 此参数是可选的，并且仅适用于listObject。 如果未提供参数，则当所有属性都具有相同的值时，会将对象视为重复。 否则，如果给定的属性具有相同的值，则将对象视为重复。 |

+++

+++签名和返回的类型

`distinctCount(<listAny>)`

返回整数。

`distinctCount(<listObject>)`

`distinctCount(<listObject>,<string>)`

返回对象列表。

+++

+++示例

`distinctCount([10,2,10,null])`

返回2。

`distinctCount(@event{my_event.productListItems})`

返回给定对象数组（listObject类型）中完全不同的对象数。

`distinctCount(@event{my_event.productListItems}, "SKU")`

返回具有不同“SKU”属性值{}的对象数。

+++

## distinctCountWithNull {#distinctCountWithNull}

计算不同值（包括空值）的数量。

**注意：**&#x200B;此函数不支持参数`<listObject>`。

+++句法

`distinctCountWithNull(<listAny>)`

+++

+++参数

| 参数 | 类型 |
|-----------|------------------|
| listToProcess | listString、listBoolean、listInteger、listDecimal、listDuration、listDateTime、listDateTimeOnly、listDateOnly |

+++

+++签名和返回的类型

`distinctCountWithNull(<listAny>)`

返回整数。

+++

+++示例

`distinctCountWithNull([10,2,10,null])`

返回3。

+++

## max {#max}

返回一组表达式中的最大值，这些表达式以列表或两个表达式形式给定。 Null值将被忽略。

+++句法

`max(<parameter>)`

+++

+++参数

* listDuration
* listInteger
* listDecimal
* listDateTime
* listDateTimeOnly
* listDateOnly
* 持续时间
* 整数
* 小数
* dateTime
* dateTimeOnly

+++

+++签名和返回的类型

`max(<listDuration>)`

返回持续时间。

`max(<listInteger>)`

返回持续时间。

`max(<listDateTimeOnly>)`

返回不考虑时区的日期时间。

`max(<listDateTime>)`

返回日期时间。

`max(<listDateOnly>)`

返回日期。

`max(<listDecimal>)`

返回小数。

`max(<decimal>,<decimal>)`

返回小数。

`max(<duration>,<duration>)`

返回持续时间。

`max(<dateTime>,<dateTime>)`

返回日期时间。

`max(<dateTimeOnly>,<dateTimeOnly>)`

返回不考虑时区的日期时间。

`max(<integer>,<integer>)`

返回整数。

+++

+++示例

`max(@event{BarBeacon.inventory},5)`

`max([10,3,8])`

返回10。

`max([10,null,8])`

返回10。

+++

## min {#min}

返回一组表达式中的最小值，这些表达式以列表或两个表达式形式给定。 Null值将被忽略。

+++句法

`min(<parameters>)`

+++

+++参数

* listDuration
* listInteger
* listDecimal
* listDateTime
* listDateTimeOnly
* listDateOnly
* 持续时间
* 整数
* 小数
* dateTime
* dateTimeOnly

+++

+++签名和返回的类型

`min(<listDuration>)`

返回持续时间。

`min(<listInteger>)`

返回持续时间。

`min(<listDateTimeOnly>)`

返回不考虑时区的日期时间。

`min(<listDateTime>)`

返回日期时间。

`min(<listDateOnly>)`

返回日期。

`min(<listDecimal>)`

返回小数。

`min(<decimal>,<decimal>)`

返回小数。

`min(<duration>,<duration>)`

返回持续时间。

`min(<dateTime>,<dateTime>)`

返回日期时间。

`min(<dateTimeOnly>,<dateTimeOnly>)`

返回不考虑时区的日期时间。

`min(<integer>,<integer>)`

返回整数。

+++

+++示例

`min(@event{BarBeacon.inventory},5)`

`min([10,3,8])`

返回3。

`min([10,null,8])`

返回8。

+++

## sum {#sum}

返回一组表达式的值的总和。 Null值将被忽略。

+++句法

`sum(<parameters>)`

+++

+++参数

* listInteger
* listDecimal
* 持续时间
* 整数
* 小数

+++

+++签名和返回的类型

`sum(<listDecimal>)`

返回小数。

`sum(<listInteger>)`

返回整数。

`sum(<integer>,<integer>)`

返回整数。

`sum(<decimal>,<decimal>)`

返回小数。

+++

+++示例

`sum(@event{BarBeacon.inventory},5)`

`sum([10,3,8])`

返回21。

`sum([10.5,null,8.1])`

返回18.6。

+++
