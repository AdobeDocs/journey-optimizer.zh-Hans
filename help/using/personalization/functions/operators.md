---
title: 运算符函数库
description: 运算符函数库
feature: Personalization
topic: Personalization
role: Developer
level: Experienced
exl-id: 75b0b380-d9a6-418e-b9f6-e64de385ba8d
TQID: https://experienceleague.adobe.com/b4Tz4auDyWb-iaUYAie31DL5hlHh97n3rYm7EP-JjIw
product_v2:
  - id: cb954087-f4fc-4456-afb9-e939cabcdc79
role_v2:
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2:
  - id: e0eb8757-182f-49f3-94a4-1587d16f5094
feature_v2:
  - id: fda7be7c-b81e-42c0-95a9-616e5b893c03
subfeature_v2: []
source-git-commit: b08de542c4f952f82a503103c783e54196c6d5b6
workflow-type: tm+mt
source-wordcount: 461
ht-degree: 9%

---

# 操作员 {#operators}

## 布尔函数 {#boolean-functions}

布尔函数用于对不同元素执行布尔逻辑。

### 与{#and}

`and`函数用于创建逻辑连接。

**语法**

```sql
{%= query1 and query2 %}
```

**示例**

这次行动将把所有以法国为母国和1985年出生年份的人送回国内。

```sql
{%= profile.homeAddress.country = "France" and profile.person.birthYear = 1985 %}
```

### 或{#or}

`or`函数用于创建逻辑分离。

**语法**

```sql
{%= query1 or query2 %}
```

**示例**

这次行动将把所有原籍国为法国或1985年出生年份的人送回。

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

比较函数用于比较不同表达式和值之间的差异，从而相应地返回true或false。

### 等于{#equals}

`=` （等于）函数检查一个值或表达式是否等于另一个值或表达式。

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

`!=` （不等于）函数检查一个值或表达式是&#x200B;**不是**&#x200B;等于另一个值或表达式。

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

`>` （大于）函数用于检查第一个值是否大于第二个值。

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

`>=` （大于或等于）函数用于检查第一个值是否大于或等于第二个值。

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

`<` （小于）比较函数用于检查第一个值是否小于第二个值。

**语法**

```sql
{%= expression1 < expression2 %}
```

**示例**

以下操作定义了2000年之前出生的人。

```sql
{%= profile.person.birthYear < 2000 %}
```

### 小于或等于{#lessthanorequal}

`<=` （小于或等于）比较函数用于检查第一个值是否小于或等于第二个值。

**语法**

```sql
{%= expression1 <= expression2 %}
```

**示例**

以下操作定义了2000年或之前出生的人。

```sql
{%= profile.person.birthYear <= 2000 %}
```

**具有编号的操作**

## 模板迁移函数 {#template-migration-functions}

个性化编辑器中提供了模板迁移函数，可帮助将现有模板迁移到Journey Optimizer。

### 通过运算符比较{#amp-compare}

`ampCompare`函数使用指定的比较运算符比较两个值。

**语法**

```sql
{%= ampCompare(value1, value2, operator) %}
```

| 参数 | 描述 |
| --------- | ----------- |
| `value1` | 要比较的第一个值。 |
| `value2` | 要比较的第二个值。 |
| `operator` | 表示要使用的比较运算符的整数。 |

**示例**

```sql
{%= ampCompare(profile.person.age, 18, 4) %}
```

### 子字符串范围{#amp-substr}

`ampSubstr`函数返回指定开始索引和结束索引之间的字符串的一部分。

**语法**

```sql
{%= ampSubstr(string, startIndex, endIndex) %}
```

| 参数 | 描述 |
| --------- | ----------- |
| `string` | 源字符串。 |
| `startIndex` | 子字符串的开始索引（整数）。 |
| `endIndex` | 子字符串的结束索引（整数）。 |

**示例**

以下表达式返回字符串“Hello World”的前五个字符。

```sql
{%= ampSubstr("Hello World", 0, 5) %}
```

返回`Hello`。

### 比较{#compare-to}

`compareTo`函数以词典方式比较两个字符串。 如果第一个字符串在第二个字符串之前，则返回负整数；如果第一个字符串在第二个字符串之后，则返回零；如果第一个字符串在第二个字符串之后，则返回正整数。

**语法**

```sql
{%= compareTo(string1, string2) %}
```

| 参数 | 描述 |
| --------- | ----------- |
| `string1` | 要比较的第一个字符串。 |
| `string2` | 要比较的第二个字符串。 |

**示例**

```sql
{%= compareTo("apple", "banana") %}
```
