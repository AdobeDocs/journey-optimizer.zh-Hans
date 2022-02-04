---
title: 运算符函数库
description: 运算符函数库
feature: Personalization
topic: Personalization
role: Data Engineer
level: Experienced
exl-id: 75b0b380-d9a6-418e-b9f6-e64de385ba8d
source-git-commit: baa98afcc8e5e9be3062c8c16adc7f4ae17b15b7
workflow-type: tm+mt
source-wordcount: '302'
ht-degree: 11%

---

# 操作员 {#operators}

## 布尔函数 {#boolean-functions}

布尔函数用于对不同元素执行布尔逻辑。

### 和{#and}

的 `and` 函数创建逻辑连接。

**格式**

```sql
{%= query1 and query2 %}
```

**示例**

以下行动将返回所有以法国为祖国的人，并将于1985年出生。

```sql
{%= profile.homeAddress.country = "France" and profile.person.birthYear = 1985 %}
```

### 或{#or}

的 `or` 函数创建逻辑分离。

**格式**

```sql
{%= query1 or query2 %}
```

**示例**

以下行动将返回所有以法国为母国或出生年的人。

```sql
{%= profile.homeAddress.country = "France" or profile.person.birthYear = 1985 %}
```

<!--
## Not{#not}

The `not` (or `!`) function is used to create a logical negation.

**Format**

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

比较函数用于比较不同表达式和值，并相应地返回true或false。

### 等于{#equals}

的 `=` （等于）函数检查一个值或表达式是否等于另一个值或表达式。

**格式**

```sql
{%= expression = value %}
```

**示例**

以下操作会检查母地国是否为法国。

```sql
{%= profile.homeAddress.country = "France" %}
```

### 不等于{#notequal}

的 `!=` （不等于）函数检查一个值或表达式是否为 **not** 等于其他值或表达式。

**格式**

```sql
{%= expression != value %}
```

**示例**

以下操作会检查母地国是否不是法国。

```sql
{%= profile.homeAddress.country != "France" %}
```

### 大于{#greaterthan}

的 `>` （大于）函数用于检查第一个值是否大于第二个值。

**格式**

```sql
{%= expression1 > expression2 %}
```

**示例**

以下操作严格界定了1970年以后出生的人。

```sql
{%= profile.person.birthYear > 1970 %}
```

### 大于或等于{#greaterthanorequal}

的 `>=` （大于或等于）函数用于检查第一个值是否大于或等于第二个值。

**格式**

```sql
{%= expression1 >= expression2 %}
```

**示例**

以下操作定义了1970年或之后出生的人。

```sql
{%= profile.person.birthYear >= 1970 %}
```

### 小于{#lessthan}

的 `<` （小于）比较函数用于检查第一值是否小于第二值。

**格式**

```sql
{%= expression1 < expression2 %}
```

**示例**

以下操作定义了2000年之前出生的人。

```sql
{%= profile.person.birthYear < 2000 %}
```

### 小于或等于{#lessthanorequal}

的 `<=` （小于或等于）比较函数用于检查第一值是否小于或等于第二值。

**格式**

```sql
{%= expression1 <= expression2 %}
```

**示例**

以下操作定义2000年或之前出生的人。

```sql
{%= profile.person.birthYear <= 2000 %}
```

**带数字的运算**
