---
title: 聚合函数库
description: 聚合函数库
feature: 个性化
topic: 个性化
role: Data Engineer
level: Experienced
source-git-commit: b58c5b527e594c03f3b415549e6b7cd15b050139
workflow-type: tm+mt
source-wordcount: '159'
ht-degree: 8%

---

# 聚合函数 {#aggregation}

![](../../assets/do-not-localize/badge.png)

聚合函数用于将多个值组合在一起，以形成单个摘要值。

## 计数{#count}

`count`函数返回给定数组中的元素数。

**格式**

```sql
{%= count(array) %}
```

**示例**

以下操作返回数组中的订单数。

```sql
{%= count(orders) %}
```

## 总和{#sum}

`sum`函数返回数组中所有选定值的总和。

**格式**

```sql
{%= sum(array) %}
```

**示例**

以下操作将返回所有订单价格的总和。

```sql
{%=sum(orders.order.price)%}
```

## 平均{#average}

`average`函数返回数组中所有选定值的算术平均值。

**格式**

```sql
{%= average(array) %}
```

**示例**

以下操作会返回所有订单的平均价格。

```sql
{%=average(orders.order.price)%}
```

## 最小{#min}

`min`函数返回数组中所有选定值的最小值。

**格式**

```sql
{%= min(array) %}
```

**示例**

以下操作会返回所有订单的最低价格。

```sql
{%=min(orders.order.price)%}
```

## 最大值{#max}

`max`函数返回数组中所有选定值的最大值。

**格式**

```sql
{%= max(array) %}
```

**示例**

以下操作会返回所有订单的最高价格。

```sql
{%=max(orders.order.price)%}
```
