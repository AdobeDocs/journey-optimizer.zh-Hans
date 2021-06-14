---
title: 字符串函数库
description: 字符串函数库
feature: 个性化
topic: 个性化
role: Data Engineer
level: Experienced
source-git-commit: b58c5b527e594c03f3b415549e6b7cd15b050139
workflow-type: tm+mt
source-wordcount: '1201'
ht-degree: 7%

---

# 字符串函数 {#string}

![](../../assets/do-not-localize/badge.png)

了解如何在表达式编辑器中使用字符串函数。

## 驼峰 {#camelCase}

`camelCase`函数大写字符串每个单词的第一个字母。

**格式**

```sql
{%= camelCase(string)%}
```

**示例**

以下函数将大写用户档案街道地址中的第一个单词字母。

```sql
{%= camelCase(profile.homeAddress.street) %}
```

## Concat {#concate}

`concat`函数将两个字符串合并为一个。

**格式**

```sql
{%= concat(string,string) %}
```

**示例**

以下函数将用户档案的城市和国家/地区合并到一个字符串中。

```sql
{%= concat(profile.homeAddress.city,profile.homeAddress.country) %}
```

## Contains {#contains}

`contains`函数用于确定字符串是否包含指定的子字符串。

**格式**

```sql
{%= contains(STRING_1, STRING_2, CASE_SENSITIVE) %}
```

| 参数 | 描述 |
| --------- | ----------- |
| `STRING_1` | 要执行检查的字符串。 |
| `STRING_2` | 要在第一个字符串中搜索的字符串。 |
| `CASE_SENSITIVE` | 用于确定检查是否区分大小写的可选参数。 可能值：true（默认）/ false。 |

**示例**

* 以下函数将检查用户档案的名字是否包含字母A（在大写或小写中）。 如果是这种情况，它将返回“true”，否则将返回“false”。

   ```sql
   {%= contains(profile.person.name.firstName, "A", false) %}
   ```

* 以下查询区分大小写地确定人员的电子邮件地址是否包含字符串“2010@gm”。

   ```sql
   {%= contains(profile.person.emailAddress,"2010@gm") %}
   ```

## 不包含{#doesNotContain}

`doesNotContain`函数用于确定字符串是否不包含指定的子字符串。

**格式**

```sql
{%= doesNotContain(STRING_1, STRING_2, CASE_SENSITIVE)%}
```

| 参数 | 描述 |
| --------- | ----------- |
| `STRING_1` | 要执行检查的字符串。 |
| `STRING_2` | 要在第一个字符串中搜索的字符串。 |
| `CASE_SENSITIVE` | 用于确定检查是否区分大小写的可选参数。 可能值：true（默认）/ false。 |

**示例**

以下查询区分大小写地确定人员的电子邮件地址是否不包含字符串“2010@gm”。

```sql
{%= doesNotContain(profile.person.emailAddress,"2010@gm")%}
```


## 不以结尾{#doesNotEndWith}

`doesNotEndWith`函数用于确定字符串是否以指定的子字符串结尾。

**格式**

```sql
{%= doesNotEndWith(STRING_1, STRING_2, CASE_SENSITIVE)%}
```

| 参数 | 描述 |
| --------- | ----------- |
| `{STRING_1}` | 要执行检查的字符串。 |
| `{STRING_2}` | 要在第一个字符串中搜索的字符串。 |
| `{CASE_SENSITIVE}` | 用于确定检查是否区分大小写的可选参数。 可能值：true（默认）/ false。 |

**示例**

以下查询会区分大小写地确定人员的电子邮件地址是否以“.com”结尾。

```sql
doesNotEndWith(person.emailAddress,".com")
```

## 开头不为{#doesNotStartWith}

`doesNotStartWith`函数用于确定字符串是否不以指定的子字符串开头。

**格式**

```sql
{%= doesNotStartWith(STRING_1, STRING_2, CASE_SENSITIVE)%}
```

| 参数 | 描述 |
| --------- | ----------- |
| `{STRING_1}` | 要执行检查的字符串。 |
| `{STRING_2}` | 要在第一个字符串中搜索的字符串。 |
| `{CASE_SENSITIVE}` | 用于确定检查是否区分大小写的可选参数。 可能值：true（默认）/ false。 |

**示例**

以下查询区分大小写确定人员姓名不以“Joe”开头。

```sql
{%= doesNotStartWith(person.name,"Joe")%}
```

## 编码64{#encode64}

例如，如果要包含在URL中，则`encode64`函数用于对字符串进行编码以保留个人信息(PI)。

**格式**

```sql
{%= encode64(string) %}
```

## 结束于{#endsWith}

`endsWith`函数用于确定字符串是否以指定的子字符串结尾。

**格式**

```sql
{%= endsWith(STRING_1, STRING_2, CASE_SENSITIVE) %}
```

| 参数 | 描述 |
| --------- | ----------- |
| `{STRING_1}` | 要执行检查的字符串。 |
| `{STRING_2}` | 要在第一个字符串中搜索的字符串。 |
| `{CASE_SENSITIVE}` | 用于确定检查是否区分大小写的可选参数。 可能值：true（默认）/ false。 |

**示例**

以下查询区分大小写地确定人员的电子邮件地址是否以“.com”结尾。

```sql
{%= endsWith(person.emailAddress,".com") %}
```


## 等于{#equals}

`equals`函数用于确定字符串是否等于指定的字符串（区分大小写）。

**格式**

```sql
{%= equals(STRING_1, STRING_2) %}
```

| 参数 | 描述 |
| --------- | ----------- |
| `{STRING_1}` | 要执行检查的字符串。 |
| `{STRING_2}` | 要与第一个字符串比较的字符串。 |

**示例**

以下查询区分大小写地确定人员的姓名是否为“John”。

```sql
{%=equals(profile.person.name,"John") %}
```

## 等于忽略大小写{#equalsIgnoreCase}

`equalsIgnoreCase`函数用于确定字符串是否等于指定的字符串，而不区分大小写。

**格式**

```sql
{%= equalsIgnoreCase(STRING_1, STRING_2) %}
```

| 参数 | 描述 |
| --------- | ----------- |
| `{STRING_1}` | 要执行检查的字符串。 |
| `{STRING_2}` | 要与第一个字符串比较的字符串。 |

**示例**

以下查询可在不区分大小写的情况下确定人员的姓名是否为“John”。

```sql
{%= equalsIgnoreCase(profile.person.name,"John") %}
```

## 提取电子邮件域 {#extractEmailDomain}

`extractEmailDomain`函数用于提取电子邮件地址的域。

**格式**

```sql
{%= extractEmailDomain(string) %}
```

**示例**

以下查询会提取个人电子邮件地址的电子邮件域。

```sql
{%= extractEmailDomain(profile.personalEmail.address) %}
```

## 为空 {#isEmpty}

`isEmpty`函数用于确定字符串为空。

**格式**

```sql
{%= isEmpty(string) %}
```

**示例**

如果用户档案的手机号码为空，则以下函数会返回“true”。 否则，将返回“false”。

```sql
{%= isEmpty(profile.mobilePhone.number) %}
```

## 左裁切 {#leftTrim}

`leftTrim`函数用于从字符串的开头删除空格。

**格式**

```sql
{%= leftTrim(string) %}
```

## Length {#length}

`length`函数用于获取字符串或表达式中的字符数。

**格式**

```sql
{%= length(string) %}
```

**示例**

以下函数返回用户档案的城市名称长度。

```sql
{%= length(profile.homeAddress.city) %}
```

## 赞{#like}

`like`函数用于确定字符串是否与指定模式匹配。

**格式**

```sql
{%= like(STRING_1, STRING_2) %}
```

| 参数 | 描述 |
| --------- | ----------- |
| `{STRING_1}` | 要执行检查的字符串。 |
| `{STRING_2}` | 要与第一个字符串匹配的表达式。 创建表达式时，有两个受支持的特殊字符：`%`和`_`。 <ul><li>`%` 用于表示零个或多个字符。</li><li>`_` 仅用于表示一个字符。</li></ul> |

**示例**

以下查询可检索用户档案所在的所有城市，其中包含模式“es”。

```sql
{%= like(profile.homeAddress.city, "%es%")%}
```

## 小写{#lower}

`lowerCase`函数将字符串转换为小写字母。

**语法**

```sql
{%= lowerCase(string) %}
```

**示例**

此函数可将用户档案的名字转换为小写字母。

```sql
{%= lowerCase(profile.person.name.firstName) %}
```

## 匹配{#matches}

`matches`函数用于确定字符串是否与特定正则表达式匹配。 有关正则表达式中匹配模式的详细信息，请参阅[本文档](https://docs.oracle.com/javase/8/docs/api/java/util/regex/Pattern.html)。

**格式**

```sql
{%= matches(STRING_1, STRING_2) %}
```

**示例**

以下查询可在不区分大小写的情况下确定人员姓名是否以“John”开头。

```sql
{%= matches(person.name.,"(?i)^John") %}
```

## 不等于{#notEqualTo}

`notEqualTo`函数用于确定字符串是否不等于指定的字符串。

**格式**

```sql
{%= notEqualTo(STRING_1, STRING_2) %}
```

| 参数 | 描述 |
| --------- | ----------- |
| `{STRING_1}` | 要执行检查的字符串。 |
| `{STRING_2}` | 要与第一个字符串比较的字符串。 |

**示例**

以下查询会区分大小写地确定人员姓名是否不是“John”。

```sql
{%= notEqualTo(profile.person.name,"John") %}
```

## 正则表达式组{#regexGroup}

`Group`函数用于根据提供的正则表达式提取特定信息。

**格式**

```sql
{%= regexGroup(STRING, EXPRESSION, GROUP) %}
```

| 参数 | 描述 |
| --------- | ----------- |
| `{STRING}` | 要执行检查的字符串。 |
| `{EXPRESSION}` | 要与第一个字符串匹配的正则表达式。 |
| `{GROUP}` | 要匹配的表达式组。 |

**示例**

以下查询用于从电子邮件地址提取域名。

```sql
{%= regexGroup(emailAddress,"@(\w+)", 1) %}
```

## Replace {#replace}

`replace`函数用于将字符串中的给定子字符串替换为另一个子字符串。

**格式**

```sql
{%= replace(string,string,string) %}
```

**示例**

以下函数。

```sql

```


## 全部替换{#replaceAll}

`replaceAll`函数用于将与“target”匹配的文本的所有子字符串替换为指定的文字“replacement”字符串。 替换从字符串的开头到结尾，例如，将字符串“aaa”中的“aa”替换为“b”将生成“ba”而不是“ab”。

**格式**

```sql
{%= replaceAll(string,string,string) %}
```


## 右修剪 {#rightTrim}

使用`rightTrim`函数时，会从字符串的末尾删除空格。


**格式**

```sql
{%= rightTrim(string) %}
```

## 拆分 {#split}

`split`函数用于按给定字符拆分字符串。

**格式**

```sql
{%= split(string,string) %}
```

<!--
**Example**

The following function .

```sql

```

-->

## 开始于{#startsWith}

`startsWith`函数用于确定字符串是否以指定的子字符串开头。

**格式**

```sql
{%= startsWith(STRING_1, STRING_2, CASE_SENSITIVE) %}
```

| 参数 | 描述 |
| --------- | ----------- |
| `{STRING_1}` | 要执行检查的字符串。 |
| `{STRING_2}` | 要在第一个字符串中搜索的字符串。 |
| `{CASE_SENSITIVE}` | 用于确定检查是否区分大小写的可选参数。 默认情况下，此参数设置为true。 |

**示例**

以下查询区分大小写地确定人员姓名是否以“Joe”开头。

```sql
{%= startsWith(person.name,"Joe") %}
```

## 标题大小写{#titleCase}

**titleCase**&#x200B;函数用于大写字符串中每个单词的前几个字母。

**语法**

```sql
{%= titleCase(string) %}
```

**示例**

如果这人住在华盛顿大街，这个功能将返回华盛顿大街。

```sql
{%= titleCase(profile.person.location.Street) %}
```

## 裁切{#trim}

**trim**&#x200B;函数删除字符串开头和结尾的所有空格。

**语法**

```sql
{%= trim(string) %}
```

## 大写{#upper}

**upperCase**&#x200B;函数将字符串转换为大写字母。

**语法**

```sql
{%= upperCase(string) %}
```

**示例**

此函数可将用户档案的姓氏转换为大写字母。

```sql
{%= upperCase(profile.person.name.lastName) %}
```
