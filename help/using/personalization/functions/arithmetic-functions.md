---
title: 算术函数库
description: 算术函数库
feature: 个性化
topic: 个性化
role: Data Engineer
level: Experienced
source-git-commit: 4be1d6f4034a0bb0a24fe5e4f634253dc1ca798e
workflow-type: tm+mt
source-wordcount: '182'
ht-degree: 7%

---

# 算术函数 {#maths}

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
