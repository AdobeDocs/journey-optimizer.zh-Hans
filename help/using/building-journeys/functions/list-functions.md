---
product: journey optimizer
title: 列表函数
description: 了解列表函数
feature: Journeys
role: Developer
level: Experienced
keywords: 列表，函数，表达式，历程，数组，集合
version: Journey Orchestration
source-git-commit: bb47ca4957129a4d05aa3d7286409eef0cb62143
workflow-type: tm+mt
source-wordcount: '1158'
ht-degree: 9%

---

# 列表函数 {#list-functions}

列表函数允许您处理和处理历程表达式中的值集合。 这些功能对于过滤、排序、转换和分析客户历程中的阵列和列表至关重要。

当您需要执行以下操作时，请使用列表函数：

* 根据条件（[筛选器](#filter)，[getListItem](#getListItem)）从收藏集中筛选和提取特定项
* 按升序或降序对列表元素进行排序和组织（[排序](#sort)）
* 删除重复项，并从列表([distinct](#distinct)， [distinctWithNull](#distinctWithNull))中获取唯一值
* 检查集合([in](#in))中是否存在值
* 限制从列表返回的项目数([limit](#limit))
* 获取列表的大小([listSize](#listSize))或将列表转换为不同的格式([serializeList](#serializeList))
* 执行集合操作，如查找列表之间的公共元素（[相交](#intersect)）

列表函数提供了用于处理复杂数据结构的强大工具，支持基于收集内容的复杂数据操作和条件逻辑。

## distinct {#distinct}

返回给定列表的不同值或对象。 Null条目将被忽略。

+++句法

`distinct(<parameters>)`

+++

+++参数

| 参数 | 类型 | 描述 |
|-----------|------------------|------------------|
| listToProcess | listString、listBoolean、listInteger、listDecimal、listDuration、listDateTime、listDateTimeOnly、listDateOnly或listObject | 要处理的列表。 对于listObject，它必须是字段引用。 |
| keyAttributeName | 字符串 | 此参数是可选的，并且仅适用于listObject。 如果未提供参数，则当所有属性都具有相同的值时，会将对象视为重复。 否则，如果给定的属性具有相同的值，则将对象视为重复。 |

+++

+++签名和返回的类型

`distinct(<listInteger>)`

返回整数列表。

`distinct(<listDecimal>)`

返回小数位数列表。

`distinct(<listString>)`

返回字符串列表。

`distinct(<listDateTimeOnly>)`

返回不考虑时区的日期时间列表。

`distinct(<listDateTime>)`

返回日期时间列表。

`distinct(<listDateOnly>)`

返回日期列表。

`distinct(<listBoolean>)`

返回布尔值列表。

`distinct(<listDuration>)`

返回持续时间列表。

`distinct(<listObject>)`

`distinct(<listObject>,<string>)`

返回对象列表。

+++

+++示例

`distinct([10,2,10,null])`

返回`[10, 2]`。

+++

## distinctWithNull {#distinctWithNull}

返回给定列表的不同值或对象。 如果列表至少有一个null条目，则返回的列表中将显示一个null条目。

+++句法

`distinctWithNull(<parameters>)`

+++

+++参数

| 参数 | 类型 | 描述 |
|-----------|------------------|------------------|
| listToProcess | listString、listBoolean、listInteger、listDecimal、listDuration、listDateTime、listDateTimeOnly、listDateOnly | 要处理的列表。 |

+++

+++签名和返回的类型

`distinctWithNull(<listInteger>)`

返回整数列表。

`distinctWithNull(<listDecimal>)`

返回小数位数列表。

`distinctWithNull(<listString>)`

返回字符串列表。

`distinctWithNull(<listDateTimeOnly>)`

返回不考虑时区的日期时间列表。

`distinctWithNull(<listDateTime>)`

返回日期时间列表。

`distinctWithNull(<listDateOnly>)`

返回日期列表。

`distinctWithNull(<listBoolean>)`

返回布尔值列表。

`distinctWithNull(<listDuration>)`

返回持续时间列表。

+++

+++示例

`distinctWithNull([10,2,10,null])`

返回[10， 2， null]

+++

**注意：**&#x200B;此函数不支持参数`<listObject>`。

## filter {#filter}

返回一个listObject，其中的对象具有匹配给定键值之一的键属性。

+++句法

`filter(<parameters>)`

+++

+++参数

| 参数 | 类型 | 描述 |
|-----------|------------------|------------------|
| listToFilter | listObject | 要过滤的对象列表。 它必须是字段引用。 |
| keyAttributeName | 字符串 | 给定列表对象中的属性名称，用作筛选键 |
| keyValueList | list | 用于过滤的键值数组 |

+++

+++签名和返回的类型

`filter(listObject, string, listString)`

`filter(listObject, string, listInteger)`

`filter(listObject, string, listDecimal)`

`filter(listObject, string, listDateTime)`

`filter(listObject, string, listDateTimeOnly)`

`filter(listObject, string, listDateOnly)`

`filter(listObject, string, listDuration)`

`filter(listObject, string, listBoolean)`

返回listObject。

+++

+++示例

以下是在传入事件“myevent”中传递的有效负载示例：

```json
"productListItems": [{
   "id": "product1",
   "name": "the product 1",
   "price": 20
},{
   "id": "product2",
   "name": "the product 2",
   "price": 30
},{
   "id": "product3",
   "name": "the product 3",
   "price": 50
}]
```

您可以使用以下表达式：

```json
filter(
 @event{myevent.productListItems},
 "id", 
 ["product2", "product3", "product4"]
)
```

返回包含两个对象的listObject，其中“product2”和“product3”作为ID。

+++

## getListItem {#getListItem}

返回给定索引处的列表项。

+++句法

`getListItem(<parameters>)`

+++

+++参数

| 参数 | 类型 |
|-----------|------------------|
| list | listString |
| list | listBoolean |
| list | listInteger |
| list | listDecimal |
| list | listDuration |
| list | listDateTime |
| list | listDateTimeOnly |
| list | listDateOnly |
| index | 整数 |

+++

+++签名和返回的类型

`getListItem(<listInteger>,<index>)`

返回整数。

`getListItem(<listDecimal>,<index>)`

返回小数。

`getListItem(<listString>,<index>)`

返回字符串。

`getListItem(<listDateTimeOnly>,<index>)`

返回不考虑时区的日期时间。

`getListItem(<listDateTime>,<index>)`

返回日期时间。

`getListItem(<listDateOnly>,<index>)`

返回日期列表。

`getListItem(<listBoolean>,<index>)`

返回布尔值。

`getListItem(<listDuration>,<index>)`

返回持续时间。

+++

+++示例

`getListItem([10, 2, 3], 1)`

返回“2”

`getListItem(["A", "B", "C"], 2)`

返回“C”

具有事件字段&quot;event.appVersion&quot;且值为&quot;20.45.2.3434&quot;的示例

`split(@event{event.appVersion}, "\\.")`

返回`["20", "45", "2", "3434"]`

`getListItem(split(@event{event.appVersion}, "\\."), 0)`

返回“20”

+++

## in {#in}

检查第一个参数值是否在列表中。 检查通过对每个参数值执行Equal。 如果找到参数值，则返回true；否则，返回false。

`<expression>`的类型必须与列表项匹配。 作为提醒，列表的项目类型必须匹配。

+++句法

`in(<parameters>)`

+++

+++参数

| 参数 | 类型 |
|-----------|------------------|
| 字符串 | 字符串 |
| 布尔值 | 布尔值 |
| 整数 | 整数 |
| 小数 | 小数 |
| 持续时间 | 持续时间 |
| 日期时间 | 日期时间 |
| DateTimeOnly | DateTimeOnly |
| 列表 | listString |
| 列表 | listBoolean |
| 列表 | listInteger |
| 列表 | listDecimal |
| 列表 | listDuration |
| 列表 | listDateTime |
| 列表 | listDateTimeOnly |
| 列表 | listDateOnly |

+++

+++签名和返回的类型

`in(<integer>,<listInteger>)`

`in(<decimal>,<listDecimal>)`

`in(<string>,<listString>)`

`in(<boolean>,<listBoolean>)`

`in(<dateTimeOnly>,<listDateTimeOnly>)`

`in(<dateTime>,<listDateTime>)`

`in(<dateOnly>,<listDateOnly>)`

`in(<duration>,<listDuration>)`

返回布尔值。

+++

+++示例

`in(4,[4,5,3,4])`

返回真。

`in(8,[4,5,3,4])`

返回假。

`in(#{ExperiencePlatform.ProfileFieldGroup.profile.person.gender}, ["male"])`

+++

## intersect {#intersect}

返回两个输入列表中的公用值。 如果两个列表之一为null，则返回空列表。

+++句法

`intersect(<parameters>)`

+++

+++参数

| 参数 | 类型 |
|-----------|------------------|
| 列表1 | list |
| 列表2 | list |

+++

+++签名和返回的类型

`intersect(listString,listString)`：列表字符串

`intersect(listDecimal,listDecimal)`： listDecimal

`intersect(listInteger,listInteger)`： listInteger

`intersect(listDateTime,listDateTime)`： listDateTime

`intersect(listDateTimeOnly,listDateTimeOnly)`： listDateTimeOnly

`intersect(listDateOnly,listDateOnly)`： listDateOnly

`intersect(listDuration,listDuration)`： listDuration

`intersect(listBoolean,listBoolean)`：列表布尔值

返回列表。

+++

+++示例

```json
intersect(
    ["sports", "news", "documentary"],
    ["sports", "movies", "documentary"]
)
```

返回[&quot;sports&quot;，&quot;news&quot;]

```json
intersect(
    #{ExperienceDataPlatform.profile.interests},
    ["sports", "documentary"]
)
```

返回配置文件属性和给定类别列表之间的通用项目。

```json
intersect(
    #{ExperienceDataPlatform.profile.interests},
        @event{myEvent.sport_interests}
)
```

返回用户档案属性和给定事件字段之间的公用项。

+++

## limit {#limit}

返回列表的第一个或最后的N个元素。

+++句法

`limit(<parameters>)`

+++

+++参数

| 参数 | 类型 | 描述 |
|-----------|------------------|------------------|
| listToProcess | listString、listBoolean、listInteger、listDecimal、listDuration、listDateTime、listDateTimeOnly、listDateOnly或listObject | 要考虑的列表。 对于listObject，它必须是字段引用。 |
| 项目数 | 整数 | 要从给定列表中返回的项目数。 |
| firstOrLastItems | 布尔 | 此参数是可选的（默认为true）。 true返回第一项。 false返回最后一个项目。 |

+++

+++签名和返回的类型

`limit(<listString>,<integer>)`

`limit(<listString>,<integer>,<boolean>)`

返回字符串列表。

`limit(<listInteger>,<integer>)`

`limit(<listInteger>,<integer>,<boolean>)`

返回整数列表。

`limit(<listDecimal>,<integer>)`

`limit(<listDecimal>,<integer>,<boolean>)`

返回小数位数列表。

`limit(<listBoolean>,<integer>)`

`limit(<listBoolean>,<integer>,<boolean>)`

返回布尔值列表。

`limit(<listDateOnly>,<integer>)`

`limit(<listDateOnly>,<integer>,<boolean>)`

返回日期列表。

`limit(<listDateTimeOnly>,<integer>)`

`limit(<listDateTimeOnly>,<integer>,<boolean>)`

返回不考虑时区的日期时间列表。

`limit(<listDateTime>,integer>)`

`limit(<listDateTime>,<integer>,<boolean>)`

返回日期时间列表。

`limit(<listDuration>,<integer>)`

`limit(<listDuration>,<integer>,<boolean>)`

返回持续时间列表。

`limit(<listObject>,<integer>)`

`limit(<listObject>,<integer>,<boolean>)`

返回对象列表。

+++

+++示例

`limit(["A", "B", "C", "D", "E"], 3)`

返回`["A","B","C"]`。

`limit(["A", "B", "C", "D", "E"], 3, false)`

返回`["C","D","E"]`。

+++

## listSize {#listSize}

计算列表中的元素数。

+++句法

`listSize(<parameters>)`

+++

+++参数

| 参数 | 类型 | 描述 |
|-----------|------------------|------------------|
| listToProcess | listString、listBoolean、listInteger、listDecimal、listDuration、listDateTime、listDateTimeOnly、listDateOnly或listObject | 要处理的列表。 对于listObject，它必须是字段引用。 listObject不能包含null对象。 |

+++

+++签名和返回的类型

`listSize(<listInteger>)`

`listSize(<listDecimal>)`

`listSize(<listString>)`

`listSize(<listBoolean>)`

`listSize(<listDateTimeOnly>)`

`listSize(<listDateTime>)`

`listSize(<listDateOnly>)`

`listSize(<listDuration>)`

返回整数。

`listSize(<listObject>)`

+++

+++示例

`listSize([10,2,3])`

返回3。

`listSize(@event{my_event.productListItems})`

返回给定对象数组（listObject类型）中的对象数。

+++

## serializeList {#serializeList}

将给定列表（除listObject之外的任何类型）转换为字符串。

+++句法

`serializeList(<parameters>)`

+++

+++参数

| 参数 | 类型 | 描述 |
|-----------|------------------|------------------|
| listToProcess | listString、listBoolean、listInteger、listDecimal、listDuration、listDateTime、listDateTimeOnly、listDateOnly | 要转换为字符串的列表。 |
| 分隔符 | 字符串 | 输出字符串中每个列表元素之间的分隔符。 |
| addQuotes | 布尔 | 此参数指示输出字符串中的每个元素是否应包含引号(true)或(false)。 |

+++

+++签名和返回的类型

`serializeList(<listInteger>,<string>,<boolean>)`

`serializeList(<listDecimal>,<string>,<boolean>)`

`serializeList(<listString>,<string>,<boolean>)`

`serializeList(<listBoolean>,<string>,<boolean>)`

`serializeList(<listDateTimeOnly>,<string>,<boolean>)`

`serializeList(<listDateTime>,<string>,<boolean>)`

`serializeList(<listDateOnly>,<string>,<boolean>)`

`serializeList(<listDuration>,<string>,<boolean>)`

返回字符串。

+++

+++示例

`serializeList(["Hello","World"], " ", false)`

返回“Hello World”。

`serializeList(["Hello", "World"], ",", true)`

返回“Hello”、“World”。

+++

## sort {#sort}

以自然顺序对值列表或对象进行排序。

+++句法

`sort(<parameters>)`

+++

+++参数

| 参数 | 类型 | 描述 |
|-----------|------------------|------------------|
| listToSort | listString、listBoolean、listInteger、listDecimal、listDuration、listDateTime、listDateTimeOnly、listDateOnly或listObject | 要排序的列表。 对于listObject，它必须是字段引用。 |
| keyAttributeName | 字符串 | 此参数仅适用于listObject。 给定列表中的对象中的属性名称用作排序的键。 |
| sortingOrder | 布尔 | 升序(true)或降序(false) |

+++

+++签名和返回的类型

`sort(<listInteger>,<boolean>)`

返回整数列表。

`sort(<listDecimal>,<boolean>)`

返回小数位数列表。

`sort(<listString>,<boolean>)`

返回字符串列表。

`sort(<listDateTimeOnly>,<boolean>)`

返回不考虑时区的日期时间列表。

`sort(<listDateTime>,<boolean>)`

返回日期时间列表。

`sort(<listDateOnly>,<boolean>)`

返回日期列表。

`sort(<listBoolean>,<boolean>)`

返回布尔值列表。

`sort(<listObject>,<string>,<boolean>)`

返回对象列表。

+++

+++示例

`sort(["A", "C", "B"], true)`

返回`["A","B","C"]`。

`sort([1, 3, 2], false)`

返回`[3, 2, 1]`。

`sort(@event{my_event.productListItems}, "SKU", true)`

返回按SKU属性排序的listObject（升序）

+++

