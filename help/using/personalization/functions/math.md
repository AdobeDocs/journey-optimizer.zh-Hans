---
title: 数学函数库
description: 数学函数库
feature: Personalization
topic: Personalization
role: Data Engineer
level: Experienced
exl-id: b9149ad6-2be7-4bdf-82eb-7ab52780cb4e
source-git-commit: 8a1ec5acef067e3e1d971deaa4b10cffa6294d75
workflow-type: tm+mt
source-wordcount: '243'
ht-degree: 11%

---

# 数学函数 {#math}

了解如何在个性化编辑器中使用数学函数。

## Absolute {#absolute}

`absolute`函数用于将数字转换为绝对值。

**语法**

```sql
{%= absolute(int) %}: int
```

## 格式数字 {#format-number}

`formatNumber`函数用于将任何数字格式化为其区分语言的表示形式。

它接受一个数字和一个表示区域设置的字符串，并返回所需区域设置中数字的格式化字符串。

**语法**

```sql
{%= formatNumber(number/double,string) %}: string
```

您可以使用[Oracle文档](https://docs.oracle.com/javase/8/docs/api/java/util/Locale.html)和[支持的区域设置](https://www.oracle.com/java/technologies/javase/jdk11-suported-locales.html){_blank}中概述的格式设置和有效区域设置

**示例**

此查询返回一个格式化的阿拉伯语字符串，作为输入数字，对应于123456.789。

```sql
{%= formatNumber(123456.789, "ar_EG") %}
```

## Random {#random}

`random`函数用于返回0到1之间的随机值。

**语法**

```sql
{%= random() %}: double
```

## Round down {#round-down}

`roundDown`函数用于对数字进行向下舍入。

**语法**

```sql
{%= roundDown(double) %}: double
```

## Round Up {#round-up}

`Count only null`函数用于对数字进行向上四舍五入。

**语法**

```sql
{%= roundUp(double) %}: double
```

## 到十六进制字符串 {#to-hex-string}

`toHexString`函数将任意数字转换为十六进制字符串。

**语法**

```sql
{%= toHexString(number) %}: string
```

**示例**

此查询返回158的十六进制值，即9e。

```sql
{%= toHexString(158) %}
```

## 到 Int {#to-int}

`toInt`函数用于将任意这些类型（数字、双精度、整数、长整数、浮点数、短整数、字节、布尔值、字符串）转换为整数。

**语法**

```sql
{%= toInt(<valueToConvert>) %}: integer
```

**示例**

此查询返回整数值42,6，即42。

```sql
{%= toInt(42.6) %}: integer
```

## To Percentage {#to-percentage}

`toPercentage`函数用于将数字转换为百分比。

**语法**

```sql
{%= toPercentage(double) %}: string
```

## To Precision {#to-precision}

`toPrecision`函数用于将数字转换为所需的精度。

**语法**

```sql
{%= toPrecision(double,int) %}: string
```

## 目标字符串 {#to-string}

**toString**&#x200B;函数将任意数字转换为字符串表示形式。

**语法**

```sql
{%= toString(string) %}: string
```

**示例**

此查询返回“12”。

```sql
{%= toString(12) %} 
```
