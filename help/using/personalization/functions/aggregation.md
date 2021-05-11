---
title: 函数库
description: 函数库
translation-type: tm+mt
source-git-commit: 55b9e5d8ed259ec6ed7746e835691d7d6261a8a4
workflow-type: tm+mt
source-wordcount: '163'
ht-degree: 6%

---

# 聚合函数{#aggregation}

![](../../assets/do-not-localize/badge.png)

聚合函数用于将[!DNL Profile Query Language](PQL)数组中的多个值组合在一起，以形成单个摘要值。

## 计数

`count`函数返回给定数组中的元素数。

**格式**

```sql
count({ARRAY})
```

**示例**

以下PQL查询返回数组中的订单数。

```sql
count(orders)
```

## Sum

`sum`函数返回数组中所有选定值的和。

**格式**

```sql
sum({ARRAY})
```

**示例**

以下PQL查询返回所有订单价格的总和。

```sql
sum(orders.order.price)
```

## 平均

`average`函数返回数组中所有选定值的算术平均值。

**格式**

```sql
average({ARRAY})
```

**示例**

以下PQL查询返回所有订单的平均价格。

```sql
average(orders.order.price)
```

## 最低

`min`函数返回数组中所有选定值中最小值。

**格式**

```sql
min({ARRAY})
```

**示例**

以下PQL查询返回所有订单的最低价格。

```sql
min(orders.order.price)
```

## 最大值

`max`函数返回数组中所有选定值中最大值。

**格式**

```sql
max({ARRAY})
```

**示例**

以下PQL查询返回所有订单的最高价格。

```sql
max(orders.order.price)
```
