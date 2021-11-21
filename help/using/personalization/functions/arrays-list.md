---
title: 数组函数库
description: 数组函数库
feature: Personalization
topic: Personalization
role: Data Engineer
level: Experienced
exl-id: dfe611fb-9c50-473c-9eb7-b983e1e6f01e
source-git-commit: 7138e1f031bd26caf9379c3ff19d79ac29442bc6
workflow-type: tm+mt
source-wordcount: '495'
ht-degree: 5%

---

# 数组和列表函数 {#arrays}

使用这些函数可更轻松地与数组、列表和字符串进行交互。

## 非重复{#distinct}

的 `distinct` 函数，用于从删除了重复值的数组或列表中获取值。

**格式**

```sql
{%= distinct(array) %}
```

**示例**

以下操作可指定在多个商店中下订单的人员。

```sql
{%= distinct(person.orders.storeId).count() > 1 %}
```

## 第一项{#head}

的 `head` 函数返回数组或列表中的第一个项目。

**格式**

```sql
{%= head({array}) %}
```

**示例**

以下操作将返回价格最高的前五个订单中的第一个订单。 有关 `topN` 函数 [第 `n` 在阵列中](#first-n) 中。

```sql
{%= head(topN(orders,price, 5)) %}
```

## 第一个 `n` 在阵列中 {#first-n}

的 `topN` 函数返回 `N` 数组中的项目，当根据给定的数值表达式以升序排序时。

**格式**

```sql
{%= topN(array, value, amount) %}
```

| 参数 | 描述 |
| --------- | ----------- |
| `{ARRAY}` | 要排序的数组或列表。 |
| `{VALUE}` | 对数组或列表进行排序的属性。 |
| `{AMOUNT}` | 要返回的项目数。 |

**示例**

以下操作将返回价格最高的前五个订单。

```sql
{%= topN(orders,price, 5) %}
```

## 在{#in}

的 `in` 函数来确定项目是否是数组或列表的成员。

**格式**

```sql
{%= in(value, array) %}
```

**示例**

以下操作可定义3月、6月或9月的生日用户。

```sql
{%= in (person.birthMonth, [3, 6, 9]) %}
```

## 包括{#includes}

的 `includes` 函数来确定数组或列表是否包含给定项。

**格式**

```sql
{%= includes(array,item) %}
```

**示例**

以下操作定义其最喜爱的颜色包括红色的人员。

```sql
{%= includes(person.favoriteColors,"red") %}
```

## Intersects{#intersects}

的 `intersects` 函数用于确定两个阵列或列表是否具有至少一个公共成员。

**格式**

```sql
{%= intersects(array1, array2) %}
```

**示例**

以下操作定义其喜爱颜色至少包括红色、蓝色或绿色之一的人员。

```sql
{%= intersects(person.favoriteColors,["red", "blue", "green"]) %}
```


<!-- ## Intersection{#intersection}

The `intersection` function is used to determine the common members of two arrays or lists.

**Format**

```sql
intersection({ARRAY},{ARRAY})
```

**Example**

The following operation defines if person 1 and person 2 both have favorite colors of red, blue, and green.

```sql
intersection(person1.favoriteColors,person2.favoriteColors) = ["red", "blue", "green"]
```
-->

## 最后 `n` 在阵列中{#last-n}

的 `bottomN` 函数返回 `N` 数组中的项目，当根据给定的数值表达式以升序排序时。

**格式**

```sql
{%= bottomN(array, value, amount) %}
```

| 参数 | 描述 |
| --------- | ----------- | 
| `{ARRAY}` | 要排序的数组或列表。 |
| `{VALUE}` | 对数组或列表进行排序的属性。 |
| `{AMOUNT}` | 要返回的项目数。 |

**示例**

以下操作将以最低的价格返回前五个订单。

```sql
{%= bottomN(orders,price, 5) %}
```


## 不在{#notin}

的 `notIn` 函数来确定项目是否不是数组或列表的成员。

>[!NOTE]
>
>的 `notIn` 函数 *也* 确保两个值均不等于null。 因此，结果不是 `in` 函数。

**格式**

```sql
{%= notIn(value, array) %}
```

**示例**

以下操作可定义不在3月、6月或9月的生日用户。

```sql
{%= notIn(person.birthMonth ,[3, 6, 9]) %}
```


## 子集{#subset}

的 `subsetOf` 函数用于确定特定阵列（阵列A）是否是另一阵列（阵列B）的子集。 换句话说，数组A中的所有元素都是数组B的元素。

**格式**

```sql
{%= subsetOf(array1, array2) %}
```

**示例**

以下操作定义访问过其所有喜爱城市的人员。

```sql
{%= subsetOf(person.favoriteCities,person.visitedCities) %}
```

## 超集{#superset}

的 `supersetOf` 函数用于确定特定阵列（阵列A）是否是另一阵列（阵列B）的超集。 换言之，数组A包含数组B中的所有元素。

**格式**

```sql
{%= supersetOf(array1, array2) %}
```

**示例**

以下操作定义了至少吃过一次寿司和比萨的人。

```sql
{%= supersetOf(person.eatenFoods,["sushi", "pizza"] %}
```
