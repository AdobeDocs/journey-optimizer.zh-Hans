---
title: 数组函数库
description: 数组函数库
feature: Personalization
topic: Personalization
role: Data Engineer
level: Experienced
exl-id: dfe611fb-9c50-473c-9eb7-b983e1e6f01e
source-git-commit: f4068450dde5f85652096c09e7f817dbab40a3d8
workflow-type: tm+mt
source-wordcount: '564'
ht-degree: 6%

---

# 数组和列表函数 {#arrays}

使用这些函数可以更轻松地与数组、列表和字符串进行交互。

## 仅计算null {#count-only-null}

此 `countOnlyNull` 函数用于计算列表中空值的数量。

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

此 `countWithNull` 函数用于计算列表中的所有元素，包括空值。

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

此 `distinct` 函数用于从删除了重复值的数组或列表中获取值。

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

此 `distinctCountWithNull` 函数用于计算列表中包含空值的不同值的数量。

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

此 `head` 函数用于返回数组或列表中的第一项。

**语法**

```sql
{%= head(array) %}
```

**示例**

以下操作将返回价格最高的前五个订单中的第一个。 欲知关于 `topN` 函数位于 [第一 `n` 在数组中](#first-n) 部分。

```sql
{%= head(topN(orders,price, 5)) %}
```

## 第一 `n` 在数组中 {#first-n}

此 `topN` 函数用于返回第一个 `N` 数组中的项（当根据给定的数值表达式按升序排序时）。

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

此 `in` 函数用于确定一个项是否是一个数组或列表的成员。

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

此 `includes` 函数用于确定一个数组或列表是否包含给定项。

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

此 `intersects` 函数用于确定两个数组或列表是否至少有一个公共成员。

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

## 最后一个 `n` 在数组中{#last-n}

此 `bottomN` 函数用于返回最后 `N` 数组中的项（当根据给定的数值表达式按升序排序时）。

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

此 `notIn` 函数用于确定一个项是否不是一个数组或列表的成员。

>[!NOTE]
>
>此 `notIn` 函数 *另外* 确保这两个值都不等于null。 因此，结果并不是完全否定 `in` 函数。

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

此 `subsetOf` 函数用于确定一个特定数组（数组A）是否是另一个数组（数组B）的子集。 换句话说，数组A中的所有元素都是数组B的元素。

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

此 `supersetOf` 函数用于确定一个特定数组（数组A）是否是另一个数组（数组B）的超集。 换句话说，该数组A包含数组B中的所有元素。

**语法**

```sql
{%= supersetOf(array1, array2) %}
```

**示例**

以下操作定义至少吃过一次寿司和比萨的人。

```sql
{%= supersetOf(person.eatenFoods,["sushi", "pizza"] %}
```
