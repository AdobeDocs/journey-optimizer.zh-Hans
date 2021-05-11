---
title: 函数库
description: 函数库
translation-type: tm+mt
source-git-commit: 55b9e5d8ed259ec6ed7746e835691d7d6261a8a4
workflow-type: tm+mt
source-wordcount: '535'
ht-degree: 5%

---

# 数组和列表函数{#arrays}

![](../../assets/do-not-localize/badge.png)

[!DNL Profile Query Language] (PQL)优惠函数可使与数组、列表和字符串的交互更简单。

## 入

`in`函数用于确定项目是否是数组或列表的成员。

**格式**

```sql
in ({VALUE},{ARRAY})
```

**示例**

以下PQL查询定义三月、六月或九月的生日。

```sql
in (person.birthMonth, [3, 6, 9])
```

## 不在

`notIn`函数用于确定项目是否不是数组或列表的成员。

>[!NOTE]
>
>`notIn`函数&#x200B;*还*&#x200B;确保这两个值均不等于null。 因此，结果不是对`in`函数的精确取反。

**格式**

```sql
notIn ({VALUE},{ARRAY})
```

**示例**

以下PQL查询定义生日不在3月、6月或9月的人。

```sql
notIn (person.birthMonth ,[3, 6, 9])
```

## Intersects

`intersects`函数用于确定两个阵列或列表是否具有至少一个公共成员。

**格式**

```sql
intersects({ARRAY},{ARRAY})
```

**示例**

以下PQL查询定义其最喜爱的颜色至少包括红色、蓝色或绿色之一的人。

```sql
intersects(person.favoriteColors,["red", "blue", "green"])
```

## 交集

`intersection`函数用于确定两个阵列或列表的公用成员。

**格式**

```sql
intersection({ARRAY},{ARRAY})
```

**示例**

以下PQL查询定义人物1和人物2是否都具有最喜爱的红色、蓝色和绿色。

```sql
intersection(person1.favoriteColors,person2.favoriteColors) = ["red", "blue", "green"]
```

## 子集

`subsetOf`函数用于确定特定阵列（阵列A）是否是另一阵列（阵列B）的子集。 换句话说，数组A中的所有元素都是数组B的元素。

**格式**

```sql
subsetOf({ARRAY},{ARRAY})
```

**示例**

以下PQL查询定义访问过其所有喜爱城市的人员。

```sql
subsetOf(person.favoriteCities,person.visitedCities)
```

## 超集

`supersetOf`函数用于确定特定阵列（阵列A）是否是另一阵列（阵列B）的超集。 换句话说，数组A包含数组B中的所有元素。

**格式**

```sql
supersetOf({ARRAY},{ARRAY})
```

**示例**

以下PQL查询定义了至少吃过一次寿司和比萨的人。

```sql
supersetOf(person.eatenFoods,["sushi", "pizza"])
```

## 包括

`includes`函数用于确定数组或列表是否包含给定项。

**格式**

```sql
includes({ARRAY},{ITEM})
```

**示例**

以下PQL查询定义其喜爱颜色包含红色的人。

```sql
includes(person.favoriteColors,"red")
```

## Distinct

`distinct`函数用于从数组或列表中删除重复值。

**格式**

```sql
distinct({ARRAY})
```

**示例**

以下PQL查询指定在多个商店中下订单的人员。

```sql
distinct(person.orders.storeId).count() > 1
```

## 数组{#first-n}中的第一个`n`

`topN`函数用于返回数组中的前一个`N`项，当这些项基于给定的数字表达式按升序排序时。

**格式**

```sql
topN({ARRAY},{VALUE}, {AMOUNT})
```

| 参数 | 描述 |
| --------- | ----------- |
| `{ARRAY}` | 要排序的数组或列表。 |
| `{VALUE}` | 对数组或列表排序的属性。 |
| `{AMOUNT}` | 要返回的项目数。 |

**示例**

以下PQL查询返回价格最高的前5个订单。

```sql
topN(orders,price, 5)
```

## 数组中最后一个`n`

`bottomN`函数用于返回数组中最后的`N`项，当这些项根据给定的数字表达式按升序排序时。

**格式**

```sql
bottomN({ARRAY},{VALUE}, {AMOUNT})
```

| 参数 | 描述 |
| --------- | ----------- | 
| `{ARRAY}` | 要排序的数组或列表。 |
| `{VALUE}` | 对数组或列表排序的属性。 |
| `{AMOUNT}` | 要返回的项目数。 |

**示例**

以下PQL查询返回价格最低的前5个订单。

```sql
bottomN(orders,price, 5)
```

## 第一项

`head`函数用于返回数组或列表中的第一个项。

**格式**

```sql
head({ARRAY})
```

**示例**

以下PQL查询返回价格最高的前五个订单中的第一个。 有关`topN`函数的详细信息，请参阅数组](#first-n)部分的[第一个`n`。

```sql
head(topN(orders,price, 5))
```
