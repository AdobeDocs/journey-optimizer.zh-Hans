---
title: 聚合函数库
description: 聚合函数库
feature: Personalization
topic: Personalization
role: Developer
level: Experienced
exl-id: a029f716-ea1e-4d79-82b7-59770f05161b
TQID: https://experienceleague.adobe.com/y1ivXVJe-Y5aIkMu--Tz22U0j-cuGcTUYrdkCkl1xyE
product_v2:
  - id: cb954087-f4fc-4456-afb9-e939cabcdc79
role_v2:
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2:
  - id: e0eb8757-182f-49f3-94a4-1587d16f5094
feature_v2:
  - id: fda7be7c-b81e-42c0-95a9-616e5b893c03
subfeature_v2: []
source-git-commit: 0ee10a0689d38c22b1180b197796b08a10c286cf
workflow-type: tm+mt
source-wordcount: 157
ht-degree: 9%

---

# 聚合函数 {#aggregation}

聚合函数用于将多个值组合在一起，以形成单个摘要值。

## 平均{#average}

`average`函数返回数组中所有选定值的算术平均值。

**语法**

```sql
{%= average(array) %}
```

**示例**

以下操作将返回所有订单的平均价格。

```sql
{%=average(orders.order.price)%}
```

## Count{#count}

`count`函数返回给定数组中的元素数。

**语法**

```sql
{%= count(array) %}
```

**示例**

以下操作返回数组中的订单数。

```sql
{%= count(orders) %}
```

## 最大值{#max}

`max`函数返回数组中所有选定值中的最大值。

**语法**

```sql
{%= max(array) %}
```

**示例**

以下操作将返回所有订单的最高价格。

```sql
{%=max(orders.order.price)%}
```

## 最小值{#min}

`min`函数返回数组中所有选定值中的最小值。

**语法**

```sql
{%= min(array) %}
```

**示例**

以下工序返回所有订单的最低价格。

```sql
{%=min(orders.order.price) %}
```

## Sum{#sum}

`sum`函数返回数组中所有选定值的总和。

**语法**

```sql
{%= sum(array) %}
```

**示例**

以下操作返回所有订单价格的总和。

```sql
{%=sum(orders.order.price)%}
```
