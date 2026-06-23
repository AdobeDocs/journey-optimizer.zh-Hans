---
product: journey optimizer
title: 聚合函数
description: 了解聚合函数
feature: Journeys
role: Developer
level: Experienced
keywords: 聚合，函数，表达式，历程，平均，计数，最大值，最小值，总和
version: Journey Orchestration
exl-id: 871a5212-5b94-4a54-bf1d-276022be3c95
feature_v2: []
subfeature_v2: []
source-git-commit: bf5866b0e7437f93936f573fd83ada8526fe004d
workflow-type: tm+mt
source-wordcount: 1105
ht-degree: 5%

---

# 聚合函数 {#aggregation-functions}

聚合函数对一组值执行计算并返回单个汇总结果。 利用这些函数，您可以通过计算平均值、查找最小值和最大值、计数元素以及汇总数值来分析历程表达式中的数据。

当您需要执行以下操作时，请使用聚合函数：

* 从列表或数组中计算统计值([avg](#avg)，[sum](#sum)，[min](#min)，[max](#max))
* 对集合([count](#count)， [countOnlyNull](#countOnlyNull)， [countWithNull](#countWithNull))中的元素进行计数，选项包括或排除null值
* 确定数据集中的唯一值([distinctCount](#distinctCount)，[distinctCountWithNull](#distinctCountWithNull))
* 根据计算指标做出数据驱动型决策

聚合函数会根据其特定行为自动处理空值，从而使处理可能包含缺失或未定义值的真实数据变得更轻松。


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

**注意：**&#x200B;此函数不支持参数`<listObject>`。

## countWithNull {#countWithNull}

计算列表的所有元素，包括null值。

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

**注意：**&#x200B;此函数不支持参数`<listObject>`。

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

**注意：**&#x200B;此函数不支持参数`<listObject>`。

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

+++ AI知识参考

本节包含结构化知识，用于支持与本主题相关的解释、检索和问答。

要全面了解相关信息，应将此信息与本页上的文档相结合。 这两个源都不是独立的；页面描述了功能，而本节提供了其他上下文来帮助消除术语、意图、适用性和约束条件的歧义。

* **TL；DR：**&#x200B;本页记录了AJO历程表达式中可用的所有聚合函数，其中包括如何计算列表和数组的平均值、总和、最小值/最大值、计数和非重复计数。

**意图：**
* 使用`avg`计算数值列表的平均值
* 使用`sum`对列表或事件字段中的数值求和
* 使用`min`或`max`查找列表中的最小值或最大值
* 使用`count`、`countOnlyNull`或`countWithNull`对列表中非null、仅null或所有元素进行计数
* 使用`distinctCount`或`distinctCountWithNull`对列表中的不同值进行计数，无论是否为null
* 使用带有键参数的`distinctCount`按特定键属性筛选listObject中的唯一对象

**术语表：**
* **listObject**：复杂对象的列表（字段引用）；不能包含null对象&#x200B;*（产品特定）*
* **listAny**：任何支持的标量类型（字符串、布尔值、整数、小数、持续时间、日期时间、日期时间仅、日期唯一）的列表&#x200B;*（产品特定）*
* **Null值**：列表中不存在或未定义的元素；大多数聚合函数忽略空值，除非该函数显式处理它们（例如，`countOnlyNull`、`countWithNull`、`distinctCountWithNull`）

**护栏：**
* `countOnlyNull`、`countWithNull`和`distinctCountWithNull`不支持`<listObject>`参数类型
* `listObject`上的`distinctCount`要求列表是字段引用，而不是内联文本
* `listObject`上的`count`要求列表是字段引用；listObject不能包含null对象

**术语：**
* 规范名称：聚合函数 — 首字母缩略词：none — 变体：聚合函数，集合函数
* 同义词： &quot;count&quot; = &quot;count non-null elements&quot;； &quot;countWithNull&quot; = &quot;count all elements include null&quot;
* 请勿混淆：“distinctCount”（忽略null）≠“distinctCountWithNull”（包括null作为非重复值）

**常见问题解答：**
* **问：`avg`的计算中是否包含null值？**  — 否，`avg`会自动忽略null值。
* **问：`count`与`countWithNull`之间有何区别？** — `count`从总计中排除null值，而`countWithNull`计算每个元素（包括null）。
* **问：我能否在listObject上使用`countOnlyNull`？**  — 否，`countOnlyNull`、`countWithNull`或`distinctCountWithNull`不支持`<listObject>`。
* **问：如何根据特定属性计算数组中的不同对象？**  — 使用`distinctCount(@event{...}, "attributeName")`提供键属性名称作为第二个参数。
* **问：当列表包含null时，`max`返回什么？** — `max`忽略null值并返回非null元素中的最大值。

+++
