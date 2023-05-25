---
title: 运算符函数库
description: 运算符函数库
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

## 布尔函数 {#boolean-functions}

布尔函数用于对不同的元素执行布尔逻辑。

### 和{#and}

此 `and` 函数用于创建逻辑连接。

**语法**

```sql
{%= query1 and query2 %}
```

**示例**

这次行动将把所有以法国为原籍国和1985年为出生年份的人送回。

```sql
{%= profile.homeAddress.country = "France" and profile.person.birthYear = 1985 %}
```

### 或{#or}

此 `or` 函数用于创建逻辑分离。

**语法**

```sql
{%= query1 or query2 %}
```

**示例**

以法国或1985年出生年份为原籍国的全体人民将参加以下行动。

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

## 比较函数 {#comparison-functions}

比较函数用于比较不同表达式和值之间的差异，并相应地返回true或false。

### 等于{#equals}

此 `=` （等于）函数检查一个值或表达式是否等于另一个值或表达式。

**语法**

```sql
{%= expression = value %}
```

**示例**

以下操作检查家庭地址国家/地区是否为法国。

```sql
{%= profile.homeAddress.country = "France" %}
```

### 不等于{#notequal}

此 `!=` （不等于）函数检查一个值或表达式是否为 **非** 等于另一个值或表达式。

**语法**

```sql
{%= expression != value %}
```

**示例**

以下操作检查家庭地址国家/地区是否不是法国。

```sql
{%= profile.homeAddress.country != "France" %}
```

### 大于{#greaterthan}

此 `>` （大于）函数用于检查第一个值是否大于第二个值。

**语法**

```sql
{%= expression1 > expression2 %}
```

**示例**

以下操作严格定义了1970年后出生的人。

```sql
{%= profile.person.birthYear > 1970 %}
```

### 大于或等于{#greaterthanorequal}

此 `>=` （大于或等于）函数用于检查第一个值是否大于或等于第二个值。

**语法**

```sql
{%= expression1 >= expression2 %}
```

**示例**

以下操作定义了1970年或之后出生的人。

```sql
{%= profile.person.birthYear >= 1970 %}
```

### 小于{#lessthan}

此 `<` （小于）比较函数用于检查第一个值是否小于第二个值。

**语法**

```sql
{%= expression1 < expression2 %}
```

**示例**

以下操作定义了2000年以前出生的人。

```sql
{%= profile.person.birthYear < 2000 %}
```

### 小于或等于{#lessthanorequal}

此 `<=` （小于或等于）比较函数用于检查第一个值是否小于或等于第二个值。

**语法**

```sql
{%= expression1 <= expression2 %}
```

**示例**

以下操作定义了2000年或之前出生的人。

```sql
{%= profile.person.birthYear <= 2000 %}
```

**具有数字的操作**
