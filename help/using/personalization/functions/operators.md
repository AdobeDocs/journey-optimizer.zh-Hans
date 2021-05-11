---
title: 函数库
description: 函数库
translation-type: tm+mt
source-git-commit: 55b9e5d8ed259ec6ed7746e835691d7d6261a8a4
workflow-type: tm+mt
source-wordcount: '561'
ht-degree: 9%

---

# 运算符 {#operators}

![](../../assets/do-not-localize/badge.png)

## 和

`and`函数用于创建逻辑连接。

**格式**

```sql
{QUERY} and {QUERY}
```

**示例**

以下PQL查询将返回所有以加拿大为母国的人和1985年出生年。

```sql
homeAddress.countryISO = "CA" and person.birthYear = 1985
```

## 或

`or`函数用于创建逻辑分离。

**格式**

```sql
{QUERY} or {QUERY}
```

**示例**

以下PQL查询将返回所有以加拿大或1985年出生年为母国的人。

```sql
homeAddress.countryISO = "CA" or person.birthYear = 1985
```

## 非

`not`（或`!`）函数用于创建逻辑取反。

**格式**

```sql
not ({QUERY})
!({QUERY})
```

**示例**

以下PQL查询将返回所有没有加拿大作为母国的人员。

```sql
not (homeAddress.countryISO = "CA")
```

## 如果

`if`函数用于根据指定的条件是否为true来解析表达式。

**格式**

```sql
if ({TEST_EXPRESSION}, {TRUE_EXPRESSION}, {FALSE_EXPRESSION})
```

| 参数 | 描述 |
| --------- | ----------- |
| `{TEST_EXPRESSION}` | 正在测试的布尔表达式。 |
| `{TRUE_EXPRESSION}` | 如果`{TEST_EXPRESSION}`为true，将使用其值的表达式。 |
| `{FALSE_EXPRESSION}` | `{TEST_EXPRESSION}`为false时将使用其值的表达式。 |

**示例**

如果母国为加拿大，则以下PQL查询将该值设置为`1`；如果母国不是加拿大，则设置为`2`。

```sql
if (homeAddress.countryISO = "CA", 1, 2)
```

## 等于

`=`(equals)函数检查一个值或表达式是否等于另一个值或表达式。

**格式**

```sql
{EXPRESSION} = {VALUE}
```

**示例**

以下PQL查询检查主地址国家/地区是否位于加拿大。

```sql
homeAddress.countryISO = "CA"
```

## 不等于

`!=`（不相等）函数检查一个值或表达式是否&#x200B;**不**&#x200B;等于另一个值或表达式。

**格式**

```sql
{EXPRESSION} != {VALUE}
```

**示例**

以下PQL查询检查主地址国家/地区是否不在加拿大。

```sql
homeAddress.countryISO != "CA"
```

## 大于

`>`（大于）函数用于检查第一值是否大于第二值。

**格式**

```sql
{EXPRESSION} > {EXPRESSION} 
```

**示例**

以下PQL查询定义生日不在1月或2月的人。

```sql
person.birthMonth > 2
```

## 大于或等于

`>=`（大于或等于）函数用于检查第一值是否大于或等于第二值。

**格式**

```sql
{EXPRESSION} >= {EXPRESSION} 
```

**示例**

以下PQL查询定义生日不在1月或2月的人。

```sql
person.birthMonth >= 3
```

## 小于

使用`<`（小于）比较函数检查第一值是否小于第二值。

**格式**

```sql
{EXPRESSION} < {EXPRESSION} 
```

**示例**

以下PQL查询定义生日在1月的人。

```sql
person.birthMonth < 2
```

## 小于或等于

使用`<=`（小于或等于）比较函数检查第一值是否小于或等于第二值。

**格式**

```sql
{EXPRESSION} <= {EXPRESSION} 
```

**示例**

以下PQL查询定义生日在1月或2月的人。

```sql
person.birthMonth <= 2
```

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
