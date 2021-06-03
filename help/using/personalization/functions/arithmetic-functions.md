---
title: 函数库
description: 函数库
source-git-commit: cd1b07bbb4b247d1d8c0cc87be9e4bdad22377ed
workflow-type: tm+mt
source-wordcount: '178'
ht-degree: 6%

---

# 算术函数 {#maths}

![](../../assets/do-not-localize/badge.png)

算术函数用于对值执行基本计算。

## Add{#add}

`+`（加法）函数用于查找两个参数表达式的和。

**格式**

```sql
{%= double + double %}
```

**示例**

下面的操作汇总了两种不同产品的价格。

```sql
{%= product1.price + product2.price %}
```

## 乘{#multiply}

`*`（乘法）函数用于查找两个参数表达式的乘积。

**格式**

```sql
{%= double * double %}
```

**示例**

以下工序将查找库存产品和产品价格，以查找产品的总价值。

```sql
{%= product.inventory * product.price %}
```

## 减{#substract}

`-`（减法）函数用于查找两个参数表达式的差。

**格式**

```sql
{%= double - double %}
```

**示例**

以下操作会查找两个不同产品之间的价格差异。

```sql
{%= product1.price - product2.price %}
```

## 除数{#divide}

`/`（除）函数用于查找两个参数表达式的商。

**格式**

```sql
{%= double / double %}
```

**示例**

下面的运算会查找销售产品总数与收入总和之间的商，以查看每项的平均成本。

```sql
{%= totalProduct.price / totalProduct.sold %}
```

## 余数{#remainder}

`%`（模/余数）函数用于在将两个参数表达式除以后找到余数。

**格式**

```sql
{%= double % double %}
```

**示例**

以下操作会检查人员的年龄是否可被5整除。

```sql
{%= person.age % 5 = 0 %}
```
