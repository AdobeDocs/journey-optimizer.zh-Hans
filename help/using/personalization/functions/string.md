---
title: 函数库
description: 函数库
translation-type: tm+mt
source-git-commit: 55b9e5d8ed259ec6ed7746e835691d7d6261a8a4
workflow-type: tm+mt
source-wordcount: '696'
ht-degree: 7%

---

# 字符串函数{#string}

![](../../assets/do-not-localize/badge.png)


TBC CJM字符串函数

## 喜欢

`like`函数用于确定字符串是否与指定的模式匹配。

**格式**

```sql
like ({STRING_1},{STRING_2})
```

| 参数 | 描述 |
| --------- | ----------- |
| `{STRING_1}` | 要执行检查的字符串。 |
| `{STRING_2}` | 要与第一个字符串匹配的表达式。 有两个支持的特殊字符用于创建表达式:`%`和`_`。 <ul><li>`%` 用于表示零个或多个字符。</li><li>`_` 仅用于表示一个字符。</li></ul> |

**示例**

以下查询将检索包含模式“es”的所有城市。

```sql
like (city ,"%es%")
```

## 开始于

`startsWith`函数用于确定字符串是否开始了指定的子字符串。

**格式**

```sql
startsWith({STRING_1},{STRING_2}, {BOOLEAN})
```

| 参数 | 描述 |
| --------- | ----------- |
| `{STRING_1}` | 要执行检查的字符串。 |
| `{STRING_2}` | 要在第一个字符串内搜索的字符串。 |
| `{BOOLEAN}` | 用于确定检查是否区分大小写的可选参数。 默认情况下，此值设置为true。 |

**示例**

以下查询区分大小写确定此人的姓名开始是否为“Joe”。

```sql
startsWith(person.name,"Joe")
```

## 不开始

`doesNotStartWith`函数用于确定字符串是否不与指定的子字符串开始。

**格式**

```sql
doesNotStartWith({STRING_1},{STRING_2}, {BOOLEAN})
```

| 参数 | 描述 |
| --------- | ----------- |
| `{STRING_1}` | 要执行检查的字符串。 |
| `{STRING_2}` | 要在第一个字符串内搜索的字符串。 |
| `{BOOLEAN}` | 用于确定检查是否区分大小写的可选参数。 默认情况下，此值设置为true。 |

**示例**

以下查询区分大小写确定人员姓名不与“Joe”开始。

```sql
doesNotStartWith(person.name,"Joe")
```

## 结束于

`endsWith`函数用于确定字符串是否以指定的子字符串结尾。

**格式**

```sql
endsWith({STRING_1},{STRING_2}, {BOOLEAN})
```

| 参数 | 描述 |
| --------- | ----------- |
| `{STRING_1}` | 要执行检查的字符串。 |
| `{STRING_2}` | 要在第一个字符串内搜索的字符串。 |
| `{BOOLEAN}` | 用于确定检查是否区分大小写的可选参数。 默认情况下，此值设置为true。 |

**示例**

以下查询区分大小写确定人员的电子邮件地址是否以“.com”结尾。

```sql
endsWith(person.emailAddress,".com")
```

## 不以

`doesNotEndWith`函数用于确定字符串是否不以指定的子字符串结尾。

**格式**

```sql
doesNotEndWith({STRING_1},{STRING_2}, {BOOLEAN})
```

| 参数 | 描述 |
| --------- | ----------- |
| `{STRING_1}` | 要执行检查的字符串。 |
| `{STRING_2}` | 要在第一个字符串内搜索的字符串。 |
| `{BOOLEAN}` | 用于确定检查是否区分大小写的可选参数。 默认情况下，此值设置为true。 |

**示例**

以下查询区分大小写确定人员的电子邮件地址是否以“.com”结尾。

```sql
doesNotEndWith(person.emailAddress,".com")
```

## Contains

`contains`函数用于确定字符串是否包含指定的子字符串。

**格式**

```sql
contains({STRING_1},{STRING_2}, {BOOLEAN})
```

| 参数 | 描述 |
| --------- | ----------- |
| `{STRING_1}` | 要执行检查的字符串。 |
| `{STRING_2}` | 要在第一个字符串内搜索的字符串。 |
| `{BOOLEAN}` | 用于确定检查是否区分大小写的可选参数。 默认情况下，此值设置为true。 |

**示例**

以下查询区分大小写确定人员的电子邮件地址是否包含字符串“2010@gm”。

```sql
contains(person.emailAddress,"2010@gm")
```

## 不包含

`doesNotContain`函数用于确定字符串是否不包含指定的子字符串。

**格式**

```sql
doesNotContain({STRING_1},{STRING_2}, {BOOLEAN})
```

| 参数 | 描述 |
| --------- | ----------- |
| `{STRING_1}` | 要执行检查的字符串。 |
| `{STRING_2}` | 要在第一个字符串内搜索的字符串。 |
| `{BOOLEAN}` | 用于确定检查是否区分大小写的可选参数。 默认情况下，此值设置为true。 |

**示例**

以下查询区分大小写确定人员的电子邮件地址不包含字符串“2010@gm”。

```sql
doesNotContain(person.emailAddress,"2010@gm")
```

## 等于

`equals`函数用于确定字符串是否等于指定的字符串。

**格式**

```sql
equals({STRING_1},{STRING_2})
```

| 参数 | 描述 |
| --------- | ----------- |
| `{STRING_1}` | 要执行检查的字符串。 |
| `{STRING_2}` | 要与第一个字符串进行比较的字符串。 |

**示例**

以下查询区分大小写确定人员的姓名是否为“John”。

```sql
equals(person.name,"John")
```

## 不等于

`notEqualTo`函数用于确定字符串是否不等于指定的字符串。

**格式**

```sql
notEqualTo({STRING_1},{STRING_2})
```

| 参数 | 描述 |
| --------- | ----------- |
| `{STRING_1}` | 要执行检查的字符串。 |
| `{STRING_2}` | 要与第一个字符串进行比较的字符串。 |

**示例**

以下查询区分大小写确定人员的姓名不是“John”。

```sql
notEqualTo(person.name,"John")
```

## 匹配

`matches`函数用于确定字符串是否与特定常规表达式匹配。 请参阅[此文档](https://docs.oracle.com/javase/8/docs/api/java/util/regex/Pattern.html)以了解有关常规表达式中匹配模式的详细信息。

**格式**

```sql
matches({STRING_1},STRING_2})
```

**示例**

以下查询将确定此人的姓名开始为“John”（约翰）时是否区分大小写。

```sql
matches(person.name.,"(?i)^John")
```

## 常规表达式组

`regexGroup`函数用于根据提供的常规表达式提取特定信息。

**格式**

```sql
regexGroup({STRING},{EXPRESSION})
```

**示例**

以下查询用于从电子邮件地址提取域名。

```sql
regexGroup(emailAddress,"@(\w+)", 1)
```
