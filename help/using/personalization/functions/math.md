---
title: 數學函式館
description: 數學函式館
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

# 數學函式 {#math}

瞭解如何在運算式編輯器中使用數學函式。

## 绝对 {#absolute}

此 `absolute` 函式可用來將數字轉換為絕對值。

**语法**

```sql
{%= absolute(int) %}: int
```

## formatNumber {#format-number}

此 `formatNumber` 函式用於將任何數字格式化成其區分語言的表示法。

它會接受數字和代表地區設定的字串，並傳回所需地區設定中數字的格式化字串。

**语法**

```sql
{%= formatNumber(number/double,string) %}: string
```

您可以使用格式設定和有效地區設定，如中所述 [oracle檔案](https://docs.oracle.com/javase/8/docs/api/java/util/Locale.html) 和 [支援的區域設定](https://www.oracle.com/java/technologies/javase/jdk11-suported-locales.html){_blank}

**示例**

此查詢會傳回對應至123456.789的阿拉伯文格式化字串作為輸入數字。

```sql
{%= formatNumber(123456.789, "ar_EG") %}
```

## Random {#random}

此 `random` 函式用於傳回0到1之間的隨機值。

**语法**

```sql
{%= random() %}: double
```

## 向下四捨五入 {#round-down}

此 `roundDown` 函式用於對數字進行向下四捨五入。

**语法**

```sql
{%= roundDown(double) %}: double
```

## 向上四捨五入 {#round-up}

此 `Count only null` 函式用於對數字進行向上四捨五入。

**语法**

```sql
{%= roundUp(double) %}: double
```

## 至十六進位字串 {#to-hex-string}

此 `toHexString` 函式將任何數字轉換為十六進位字串。

**语法**

```sql
{%= toHexString(number) %}: string
```

**示例**

此查詢會傳回158的十六進位值，即9e。

```sql
{%= toHexString(158) %}
```

## 目標百分比 {#to-percentage}

此 `toPercentage` 函式用於將數字轉換為百分比。

**语法**

```sql
{%= toPercentage(double) %}: string
```

## 至精確度 {#to-precision}

此 `toPrecision` 函式用於將數字轉換為所需的精確度。

**语法**

```sql
{%= toPrecision(double,int) %}: string
```

## 至字串 {#to-string}

此 **toString** 函式將任何數字轉換為字串表示法。

**语法**

```sql
{%= toString(string) %}: string
```

**示例**

此查詢傳回「12」。

```sql
{%= toString(12) %} 
```
