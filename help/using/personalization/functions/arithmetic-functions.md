---
title: 算术函数库
description: 算术函数库
feature: Personalization
topic: Personalization
role: Data Engineer
level: Experienced
exl-id: 21ef8f50-8389-4675-a8e5-0438a3eee592
source-git-commit: f4068450dde5f85652096c09e7f817dbab40a3d8
workflow-type: tm+mt
source-wordcount: '180'
ht-degree: 7%

---

# 算术函数 {#maths}

算术函数用于对值进行基本计算。

## Add{#add}

`+` （相加）函数用于求两个参数表达式的总和。

**语法**

```sql
{%= double + double %}
```

**示例**

以下操作对两个不同产品的价格求和。

```sql
{%= product1.price + product2.price %}
```

## 乘{#multiply}

`*` （乘法）函数用于查找两个参数表达式的乘积。

**语法**

```sql
{%= double * double %}
```

**示例**

以下操作将查找库存的产品和产品价格，以查找产品的总值。

```sql
{%= product.inventory * product.price %}
```

## 减{#substract}

`-` （减法）函数用于找出两个参数表达式的差异。

**语法**

```sql
{%= double - double %}
```

**示例**

以下操作找出两个不同产品之间的价格差异。

```sql
{%= product1.price - product2.price %}
```

## 除{#divide}

`/` （除）函数用于查找两个参数表达式的商。

**语法**

```sql
{%= double / double %}
```

**示例**

以下操作将查找已售产品总数与已挣金额总数之间的商数，以查看每个项目的平均成本。

```sql
{%= totalProduct.price / totalProduct.sold %}
```

## 余数{#remainder}

`%` （模/余数）函数用于求两个参数表达式相除后的余数。

**语法**

```sql
{%= double % double %}
```

**示例**

以下操作检查人员的年龄是否可被5岁整除。

```sql
{%= person.age % 5 = 0 %}
```
