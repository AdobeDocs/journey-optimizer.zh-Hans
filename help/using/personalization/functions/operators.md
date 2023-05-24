---
title: 運運算元函式庫
description: 運運算元函式庫
feature: Personalization
topic: Personalization
role: Data Engineer
level: Experienced
exl-id: 75b0b380-d9a6-418e-b9f6-e64de385ba8d
source-git-commit: f4068450dde5f85652096c09e7f817dbab40a3d8
workflow-type: tm+mt
source-wordcount: '302'
ht-degree: 11%

---

# 操作员 {#operators}

## 布林函式 {#boolean-functions}

布林值函式可用來在不同的元素上執行布林值邏輯。

### 和{#and}

此 `and` 函式用來建立邏輯結合。

**语法**

```sql
{%= query1 and query2 %}
```

**示例**

下列作業將傳回原籍國為France及1985年出生年份的所有人。

```sql
{%= profile.homeAddress.country = "France" and profile.person.birthYear = 1985 %}
```

### 或{#or}

此 `or` 函式用來建立邏輯分離。

**语法**

```sql
{%= query1 or query2 %}
```

**示例**

下列作業將傳回原籍國為法國或1985年出生年份的所有人。

```sql
{%= profile.homeAddress.country = "France" or profile.person.birthYear = 1985 %}
```

<!--
## Not{#not}

The `not` (or `!`) function is used to create a logical negation.

**Syntax**

```sql
not ({QUERY})
!({QUERY})
```

**Example**

The following operation will return all people who do not have their home country as Canada.

```sql
not (homeAddress.countryISO = "CA")
```
-->

## 比較函式 {#comparison-functions}

比較函式可用來比較不同運算式和值之間的差異，並相應地傳回true或false。

### 等于{#equals}

此 `=` （等於）函式檢查一個值或運算式是否等於另一個值或運算式。

**语法**

```sql
{%= expression = value %}
```

**示例**

下列作業會檢查住家地址（國家）是否為法國。

```sql
{%= profile.homeAddress.country = "France" %}
```

### 不等于{#notequal}

此 `!=` （不等於）函式檢查一個值或運算式是否為 **not** 等於另一個值或運算式。

**语法**

```sql
{%= expression != value %}
```

**示例**

下列作業會檢查住家地址國家/地區是否不是法國。

```sql
{%= profile.homeAddress.country != "France" %}
```

### 大于{#greaterthan}

此 `>` （大於）函式來檢查第一個值是否大於第二個值。

**语法**

```sql
{%= expression1 > expression2 %}
```

**示例**

下列作業會嚴格定義1970年後出生的人。

```sql
{%= profile.person.birthYear > 1970 %}
```

### 大于或等于{#greaterthanorequal}

此 `>=` （大於或等於）函式來檢查第一個值是否大於或等於第二個值。

**语法**

```sql
{%= expression1 >= expression2 %}
```

**示例**

下列作業定義1970年或之後出生的人。

```sql
{%= profile.person.birthYear >= 1970 %}
```

### 小于{#lessthan}

此 `<` （小於）比較函式用於檢查第一個值是否小於第二個值。

**语法**

```sql
{%= expression1 < expression2 %}
```

**示例**

下列作業定義2000年以前出生的人。

```sql
{%= profile.person.birthYear < 2000 %}
```

### 小于或等于{#lessthanorequal}

此 `<=` （小於或等於）比較函式用於檢查第一個值是否小於或等於第二個值。

**语法**

```sql
{%= expression1 <= expression2 %}
```

**示例**

下列作業會定義2000年或之前出生的人。

```sql
{%= profile.person.birthYear <= 2000 %}
```

**含數字的作業**
