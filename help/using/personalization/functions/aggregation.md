---
title: 彙總函式庫
description: 彙總函式庫
feature: Personalization
topic: Personalization
role: Data Engineer
level: Experienced
exl-id: a029f716-ea1e-4d79-82b7-59770f05161b
source-git-commit: f4068450dde5f85652096c09e7f817dbab40a3d8
workflow-type: tm+mt
source-wordcount: '157'
ht-degree: 7%

---

# 彙總函式 {#aggregation}

彙總函式用於將多個值群組在一起，以形成單一摘要值。

## 平均{#average}

此 `average` 函式傳回陣列中所有選取值的算術平均值。

**语法**

```sql
{%= average(array) %}
```

**示例**

下列作業會傳回所有訂單的平均價格。

```sql
{%=average(orders.order.price)%}
```

## 計數{#count}

此 `count` 函式傳回給定陣列中的元素數。

**语法**

```sql
{%= count(array) %}
```

**示例**

下列作業會傳回陣列中的訂單數。

```sql
{%= count(orders) %}
```

## 最大值{#max}

此 `max` 函式會傳回陣列中所有選取值的最大值。

**语法**

```sql
{%= max(array) %}
```

**示例**

下列作業會傳回所有訂單的最高價格。

```sql
{%=max(orders.order.price)%}
```

## 最小值{#min}

此 `min` 函式傳回陣列中所有選取值的最小值。

**语法**

```sql
{%= min(array) %}
```

**示例**

下列作業會傳回所有訂單的最低價格。

```sql
{%=min(orders.order.price) %}
```

## 總和{#sum}

此 `sum` 函式會傳回陣列中所有選取值的總和。

**语法**

```sql
{%= sum(array) %}
```

**示例**

下列作業會傳回所有訂單價格的總和。

```sql
{%=sum(orders.order.price)%}
```
