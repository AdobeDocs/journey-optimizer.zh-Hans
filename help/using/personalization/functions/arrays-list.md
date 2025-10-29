---
title: 数组函数库
description: 数组函数库
feature: Personalization
topic: Personalization
role: Developer
level: Experienced
exl-id: dfe611fb-9c50-473c-9eb7-b983e1e6f01e
source-git-commit: 07a582db495ecbfae97b6d299b65b06c0cdf8c14
workflow-type: tm+mt
source-wordcount: '592'
ht-degree: 5%

---

# 数组和列表函数 {#arrays}

使用这些函数可以更轻松地与数组、列表和字符串进行交互。

## 仅计算null {#count-only-null}

`countOnlyNull`函数用于计算列表中空值的数量。

**语法**

```sql
{%= countOnlyNull(array) %}
```

**示例**

```sql
{%= countOnlyNull([4,0,1,6,0,0]) %}
```

返回3。

## 空计数 {#count-with-null}

`countWithNull`函数用于对包含null值的列表的所有元素进行计数。

**语法**

```sql
{%= countWithNull(array) %}
```

**示例**

```sql
{%= countOnlyNull([4,0,1,6,0,0]) %}
```

返回6。

## Distinct{#distinct}

`distinct`函数用于从已删除重复值的数组或列表中获取值。

**语法**

```sql
{%= distinct(array) %}
```

**示例**

以下操作指定在多个商店下订单的人员。

```sql
{%= distinct(person.orders.storeId).count() > 1 %}
```

## Null非重复计数 {#distinct-count-with-null}

`distinctCountWithNull`函数用于计算列表中包括null值的不同值的数量。

**语法**

```sql
{%= distinctCountWithNull(array) %}
```

**示例**

```sql
{%= distinctCountWithNull([10,2,10,null]) %}
```

返回3。

## 第一个项目{#head}

`head`函数用于返回数组或列表中的第一个项。

**语法**

```sql
{%= head(array) %}
```

**示例**

以下操作将返回价格最高的前五个订单中的第一个。 有关`topN`函数的更多信息，请参见[数组`n`中的第一个](#first-n)。

```sql
{%= head(topN(orders,price, 5)) %}
```

## 排序并获取数组中的前N个 {#first-n}

`topN`函数根据给定的数值表达式以降序排序数组，并返回前`N`项。 如果数组大小小于`N`，则返回整个排序的数组。

此函数
**语法**

```sql
{%= topN(array, value, amount) %}
```

| 参数 | 描述 |
| --------- | ----------- |
| `{ARRAY}` | 要排序的数组或列表。 |
| `{VALUE}` | 要对数组或列表进行排序的属性。 |
| `{AMOUNT}` | 要返回的项目数。 |

**示例**

以下操作将返回价格最低的前五个订单。

```sql
{%= topN(orders,price, 5) %}
```

## 在{#in}

`in`函数用于确定一个项是数组还是列表的成员。

**语法**

```sql
{%= in(value, array) %}
```

**示例**

以下操作定义3月、6月或9月拥有生日的人员。

```sql
{%= in (person.birthMonth, [3, 6, 9]) %}
```

## 包括{#includes}

`includes`函数用于确定一个数组或列表是否包含给定项。

**语法**

```sql
{%= includes(array,item) %}
```

**示例**

以下操作定义其最喜爱的颜色包括红色的人员。

```sql
{%= includes(person.favoriteColors,"red") %}
```

## 相交{#intersects}

`intersects`函数用于确定两个数组或列表是否至少有一个公共成员。

**语法**

```sql
{%= intersects(array1, array2) %}
```

**示例**

以下操作定义其最喜爱的颜色至少包括红色、蓝色或绿色中的一种的人员。

```sql
{%= intersects(person.favoriteColors,["red", "blue", "green"]) %}
```


<!-- ## Intersection{#intersection}

The `intersection` function is used to determine the common members of two arrays or lists.

**Syntax**

```sql
intersection({ARRAY},{ARRAY})
```

**Example**

The following operation defines if person 1 and person 2 both have favorite colors of red, blue, and green.

```sql
intersection(person1.favoriteColors,person2.favoriteColors) = ["red", "blue", "green"]
```
-->

## 排序并获取数组中的最后N个 {#last-n}

`bottomN`函数根据给定的数值表达式对数组进行升序排序，并返回前`N`项。 如果数组大小小于`N`，则返回整个排序的数组。

**语法**

```sql
{%= bottomN(array, value, amount) %}
```

| 参数 | 描述 |
| --------- | ----------- | 
| `{ARRAY}` | 要排序的数组或列表。 |
| `{VALUE}` | 要对数组或列表进行排序的属性。 |
| `{AMOUNT}` | 要返回的项目数。 |

**示例**

以下操作将返回具有最高价格的最后5个订单。

```sql
{%= bottomN(orders,price, 5) %}
```

## 不在{#notin}

`notIn`函数用于确定一个项是否不是一个数组或列表的成员。

>[!NOTE]
>
>`notIn`函数&#x200B;*还*&#x200B;确保这两个值都不等于null。 因此，结果不是`in`函数的完全否定。

**语法**

```sql
{%= notIn(value, array) %}
```

**示例**

以下操作定义非三月、六月或九月的生日人员。

```sql
{%= notIn(person.birthMonth ,[3, 6, 9]) %}
```


## 子集{#subset}

`subsetOf`函数用于确定一个特定数组（数组A）是否是另一个数组（数组B）的子集。 换句话说，数组A中的所有元素都是数组B的元素。

**语法**

```sql
{%= subsetOf(array1, array2) %}
```

**示例**

以下操作定义访问过他们喜欢的所有城市的人。

```sql
{%= subsetOf(person.favoriteCities,person.visitedCities) %}
```

## 超集{#superset}

`supersetOf`函数用于确定一个特定数组（数组A）是否是另一个数组（数组B）的超集。 换句话说，该数组A包含数组B中的所有元素。

**语法**

```sql
{%= supersetOf(array1, array2) %}
```

**示例**

以下操作定义至少吃过一次寿司和比萨的人。

```sql
{%= supersetOf(person.eatenFoods,["sushi", "pizza"]) %}
```
