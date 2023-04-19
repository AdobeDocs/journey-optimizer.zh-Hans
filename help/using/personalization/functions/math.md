---
title: 数学函数库
description: 数学函数库
feature: Personalization
topic: Personalization
role: Data Engineer
level: Experienced
exl-id: b9149ad6-2be7-4bdf-82eb-7ab52780cb4e
source-git-commit: c823d1a02ca9d24fc13eaeaba2b688249e61f767
workflow-type: tm+mt
source-wordcount: '215'
ht-degree: 6%

---

# 数学函数 {#math}

了解如何在表达式编辑器中使用Math函数。

## 绝对 {#absolute}

的 `absolute` 函数来转换数字的绝对值。

**语法**

```sql
{%= absolute(int) %}: int
```

## formatNumber {#format-number}

的 `formatNumber` 函数将任何数字格式化为其语言敏感表示形式。

它接受表示区域设置的数字和字符串，并返回所需区域设置中该数字的格式化字符串。

**语法**

```sql
{%= formatNumber(number/double,string) %}: string
```

您可以使用格式和有效区域设置，如 [Oracle文档](https://docs.oracle.com/javase/8/docs/api/java/util/Locale.html) 和 [支持的区域设置](https://www.oracle.com/java/technologies/javase/jdk11-suported-locales.html){_blank}

**示例**

此查询返回一个阿拉伯文格式的字符串，其对应123456.789作为输入编号。

```sql
{%= formatNumber(123456.789, "ar_EG") %}
```

## Random {#random}

的 `random` 函数返回介于0和1之间的随机值。

**语法**

```sql
{%= random() %}: double
```

## 向下舍入 {#round-down}

的 `roundDown` 函数对数字进行四舍五入。

**语法**

```sql
{%= roundDown(double) %}: double
```

## 向上舍入 {#round-up}

的 `Count only null` 函数对数字进行四舍五入。

**语法**

```sql
{%= roundUp(double) %}: double
```

## 十六进制字符串 {#to-hex-string}

的 `toHexString` 函数会将任何数字转换为其十六进制字符串。

**语法**

```sql
{%= toHexString(number) %}: string
```

**示例**

此查询返回十六进制值158（即9e）。

```sql
{%= toHexString(158) %}
```

## 至百分比 {#to-percentage}

的 `toPercentage` 函数将数字转换为百分比。

**语法**

```sql
{%= toPercentage(double) %}: string
```

## 精度 {#to-precision}

的 `toPrecision` 函数将数字转换为所需的精度。

**语法**

```sql
{%= toPrecision(double,int) %}: string
```

## 至字符串 {#to-string}

的 **toString** 函数会将任何数字转换为其字符串表示形式。

**语法**

```sql
{%= toString(string) %}: string
```

**示例**

此查询返回“12”。

```sql
{%= toString(12) %} 
```
