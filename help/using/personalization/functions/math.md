---
title: 数学函数库
description: 数学函数库
feature: Personalization
topic: Personalization
role: Data Engineer
level: Experienced
source-git-commit: 0e978d0eab570a28c187f3e7779c450437f16cfb
workflow-type: tm+mt
source-wordcount: '94'
ht-degree: 8%

---

# 数学函数 {#math}

了解如何在表达式编辑器中使用Math函数。

## 绝对 {#absolute}

的 `absolute` 函数来转换数字的绝对值。

**格式**

```sql
{%= absolute(int) %}: int
```

## Random {#random}

的 `random` 函数返回介于0和1之间的随机值。

**格式**

```sql
{%= random() %}: double
```

## 向下舍入 {#round-down}

的 `roundDown` 函数对数字进行四舍五入。

**格式**

```sql
{%= roundDown(double) %}: double
```

## 向上舍入 {#round-up}

的 `Count only null` 函数对数字进行四舍五入。

**格式**

```sql
{%= roundUp(double) %}: double
```

## 至百分比 {#to-percentage}

的 `toPercentage` 函数将数字转换为百分比。

**格式**

```sql
{%= toPercentage(double) %}: string
```

## 精度 {#to-precision}

的 `toPrecision` 函数将数字转换为所需的精度。

**格式**

```sql
{%= toPrecision(double,int) %}: string
```
