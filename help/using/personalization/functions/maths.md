---
title: 函数库
description: 函数库
translation-type: tm+mt
source-git-commit: 55b9e5d8ed259ec6ed7746e835691d7d6261a8a4
workflow-type: tm+mt
source-wordcount: '185'
ht-degree: 5%

---

# 数学函数{#math}

![](../../assets/do-not-localize/badge.png)

算术函数用于对[!DNL Profile Query Language](PQL)中的值执行基本计算。

## Add

`+`(addition)函数用于查找两个参数表达式的和。

**格式**

```sql
{NUMBER} + {NUMBER}
```

**示例**

以下PQL查询概括了两种不同产品的价格。

```sql
product1.price + product2.price
```

## 乘

`*`（乘法）函数用于查找两个参数表达式的乘积。

**格式**

```sql
{NUMBER} * {NUMBER}
```

**示例**

以下PQL查询查找库存产品和产品价格以查找产品的总价值。

```sql
product.inventory * product.price
```

## 减

`-`（减法）函数用于查找两个参数表达式的差值。

**格式**

```sql
{NUMBER} - {NUMBER}
```

**示例**

以下PQL查询会查找两种不同产品之间的价格差异。

```sql
product1.price - product2.price
```

## 除法

`/`(division)函数用于查找两个参数表达式的商。

**格式**

```sql
{NUMBER} / {NUMBER}
```

**示例**

以下PQL查询将查找销售产品总数与查看每个项目的平均成本所赚总金额之间的商。

```sql
totalProduct.price / totalProduct.sold
```

## 剩余

`%`(modulo/remainer)函数用于在将两个参数表达式除以后查找余数。

**格式**

```sql
{NUMBER} % {NUMBER}
```

**示例**

以下PQL查询检查人员的年龄是否可被五个人整除。

```sql
person.age % 5 = 0
```
