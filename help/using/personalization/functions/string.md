---
title: 字符串函数库
description: 字符串函数库
feature: Personalization
topic: Personalization
role: Data Engineer
level: Experienced
exl-id: 8674ef9e-261b-49d9-800e-367f9f7ef979
source-git-commit: 8a1ec5acef067e3e1d971deaa4b10cffa6294d75
workflow-type: tm+mt
source-wordcount: '1846'
ht-degree: 9%

---

# 字符串函数 {#string}

了解如何在个性化编辑器中使用字符串函数。

## 驼峰式大小写 {#camelCase}

此 `camelCase` 函数将字符串中每个单词的第一个字母转换为大写。

**语法**

```sql
{%= camelCase(string)%}
```

**示例**

以下函数会将用户档案的街道地址中的第一个单词变为大写。

```sql
{%= camelCase(profile.homeAddress.street) %}
```

## 字符代码位于 {#char-code-at}

此 `charCodeAt` 函数返回字符的ASCII值，与JavaScript中的charCodeAt函数类似。 它采用字符串和整数（定义字符的位置）作为输入参数，并返回相应的ASCII值。

**语法**

```sql
{%= charCodeAt(string,int) %}: int
```

**示例**

以下函数返回o的ASCII值，即111。

```sql
{%= charCodeAt("some", 1)%}
```

## Concat {#concate}

此 `concat` 函数将两个字符串组合在一起。

**语法**

```sql
{%= concat(string,string) %}
```

**示例**

以下函数将用户档案城市和国家/地区组合在一个字符串中。

```sql
{%= concat(profile.homeAddress.city,profile.homeAddress.country) %}
```

## Contains {#contains}

此 `contains` 函数用于确定一个字符串是否包含指定的子字符串。

**语法**

```sql
{%= contains(STRING_1, STRING_2, CASE_SENSITIVE) %}
```

| 参数 | 描述 |
| --------- | ----------- |
| `STRING_1` | 要检查的字符串。 |
| `STRING_2` | 要在第一个字符串中搜索的字符串。 |
| `CASE_SENSITIVE` | 用于确定检查是否区分大小写，的可选参数。 可能的值： true （默认） / false。 |

**示例**

* 以下函数将检查用户档案名字是否包含字母A（大写或小写）。 如果是这种情况，将返回“true”，否则将返回“false”。

  ```sql
  {%= contains(profile.person.name.firstName, "A", false) %}
  ```

* 以下查询区分大小写确定人员的电子邮件地址是否包含字符串“2010@gm”。

  ```sql
  {%= contains(profile.person.emailAddress,"2010@gm") %}
  ```

## 不包含{#doesNotContain}

此 `doesNotContain` 函数用于确定一个字符串是否不包含指定的子字符串。

**语法**

```sql
{%= doesNotContain(STRING_1, STRING_2, CASE_SENSITIVE)%}
```

| 参数 | 描述 |
| --------- | ----------- |
| `STRING_1` | 要检查的字符串。 |
| `STRING_2` | 要在第一个字符串中搜索的字符串。 |
| `CASE_SENSITIVE` | 用于确定检查是否区分大小写，的可选参数。 可能的值： true （默认） / false。 |

**示例**

以下查询区分大小写确定人员的电子邮件地址是否不包含字符串“2010@gm”。

```sql
{%= doesNotContain(profile.person.emailAddress,"2010@gm")%}
```


## Does not end with{#doesNotEndWith}

此 `doesNotEndWith` 函数用于确定一个字符串是否不以指定的子字符串结尾。

**语法**

```sql
{%= doesNotEndWith(STRING_1, STRING_2, CASE_SENSITIVE)%}
```

| 参数 | 描述 |
| --------- | ----------- |
| `{STRING_1}` | 要检查的字符串。 |
| `{STRING_2}` | 要在第一个字符串中搜索的字符串。 |
| `{CASE_SENSITIVE}` | 用于确定检查是否区分大小写，的可选参数。 可能的值： true （默认） / false。 |

**示例**

以下查询区分大小写确定人员的电子邮件地址是否不以“.com”结尾。

```sql
doesNotEndWith(person.emailAddress,".com")
```

## Does not start with{#doesNotStartWith}

此 `doesNotStartWith` 函数用于确定一个字符串是否不以指定的子字符串开头。

**语法**

```sql
{%= doesNotStartWith(STRING_1, STRING_2, CASE_SENSITIVE)%}
```

| 参数 | 描述 |
| --------- | ----------- |
| `{STRING_1}` | 要检查的字符串。 |
| `{STRING_2}` | 要在第一个字符串中搜索的字符串。 |
| `{CASE_SENSITIVE}` | 用于确定检查是否区分大小写，的可选参数。 可能的值： true （默认） / false。 |

**示例**

以下查询区分大小写确定人员的姓名是否不以“Joe”开头。

```sql
{%= doesNotStartWith(person.name,"Joe")%}
```

## 编码64{#encode64}

此 `encode64` 函数用于对字符串进行编码，以保留个人信息(PI)（例如，如果包含在URL中）。

**语法**

```sql
{%= encode64(string) %}
```

## 结束于{#endsWith}

此 `endsWith` 函数用于确定一个字符串是否以指定的子字符串结尾。

**语法**

```sql
{%= endsWith(STRING_1, STRING_2, CASE_SENSITIVE) %}
```

| 参数 | 描述 |
| --------- | ----------- |
| `{STRING_1}` | 要检查的字符串。 |
| `{STRING_2}` | 要在第一个字符串中搜索的字符串。 |
| `{CASE_SENSITIVE}` | 用于确定检查是否区分大小写，的可选参数。 可能的值： true （默认） / false。 |

**示例**

以下查询区分大小写确定人员的电子邮件地址是否以“.com”结尾。

```sql
{%= endsWith(person.emailAddress,".com") %}
```


## 等于{#equals}

此 `equals` 函数用于确定一个字符串是否等于指定的字符串（区分大小写）。

**语法**

```sql
{%= equals(STRING_1, STRING_2) %}
```

| 参数 | 描述 |
| --------- | ----------- |
| `{STRING_1}` | 要检查的字符串。 |
| `{STRING_2}` | 要与第一个字符串进行比较的字符串。 |

**示例**

以下查询区分大小写确定人员姓名是否为“John”。

```sql
{%=equals(profile.person.name,"John") %}
```

## Equals Ignore Case{#equalsIgnoreCase}

此 `equalsIgnoreCase` 函数用于确定一个字符串是否等于指定的字符串，不区分大小写。

**语法**

```sql
{%= equalsIgnoreCase(STRING_1, STRING_2) %}
```

| 参数 | 描述 |
| --------- | ----------- |
| `{STRING_1}` | 要检查的字符串。 |
| `{STRING_2}` | 要与第一个字符串进行比较的字符串。 |

**示例**

以下查询在不区分大小写的情况下确定人员姓名是否为“John”。

```sql
{%= equalsIgnoreCase(profile.person.name,"John") %}
```

## 提取电子邮件域 {#extractEmailDomain}

此 `extractEmailDomain` 函数用于提取电子邮件地址的域。

**语法**

```sql
{%= extractEmailDomain(string) %}
```

**示例**

以下查询提取个人电子邮件地址的电子邮件域。

```sql
{%= extractEmailDomain(profile.personalEmail.address) %}
```

## 设置货币格式 {#format-currency}

此 `formatCurrency` 函数用于将任何数字转换为相应的语言敏感型货币表示形式，具体取决于在第二个参数中作为字符串传递的区域设置。

**语法**

```sql
{%= formatCurrency(number/double,string) %}: string
```

**示例**

此查询返回56.00英镑

```sql
{%= formatCurrency(56L,"en_GB") %}
```

## Get url host {#get-url-host}

此 `getUrlHost` 函数用于检索URL的主机名。

**语法**

```sql
{%= getUrlHost(string) %}: string
```

**示例**

```sql
{%= getUrlHost("https://www.myurl.com/contact") %}
```

返回“www.myurl.com”

## Get url path {#get-url-path}

此 `getUrlPath` 函数用于检索URL的域名之后的路径。

**语法**

```sql
{%= getUrlPath(string) %}: string
```

**示例**

```sql
{%= getUrlPath("https://www.myurl.com/contact.html") %}
```

返回“/contact.html”

## Get url protocol {#get-url-protocol}

此 `getUrlProtocol` 函数用于检索URL的协议。

**语法**

```sql
{%= getUrlProtocol(string) %}: string
```

**示例**

```sql
{%= getUrlProtocol("https://www.myurl.com/contact.html") %}
```

返回“http”

## Index Of {#index-of}

此 `indexOf` 函数用于返回第二个参数在第一个参数中第一次出现的位置。 如果没有匹配项，则返回–1。

**语法**

```sql
{%= indexOf(STRING_1, STRING_2) %}: integer
```

| 参数 | 描述 |
| --------- | ----------- |
| `{STRING_1}` | 要检查的字符串。 |
| `{STRING_2}` | 要在第一个参数中搜索的字符串 |

**示例**

```sql
{%= indexOf("hello world","world" ) %}
```

返回6。

## 为空 {#isEmpty}

此 `isEmpty` 函数用于确定一个字符串是否为空。

**语法**

```sql
{%= isEmpty(string) %}
```

**示例**

如果个人资料的手机号码为空，则以下函数返回“true”。 否则，将返回“false”。

```sql
{%= isEmpty(profile.mobilePhone.number) %}
```

## Is Not Empty {#is-not-empty}

此 `isNotEmpty` 函数用于确定一个字符串是否不为空。

**语法**

```sql
{= isNotEmpty(string) %}: boolean
```

**示例**

如果个人资料的手机号码不为空，则以下函数返回“true”。 否则，将返回“false”。

```sql
{%= isNotEmpty(profile.mobilePhone.number) %}
```

## Last Index Of {#last-index-of}

此 `lastIndexOf` 函数用于返回第二个参数在第一个参数中最后一次出现的位置。 如果没有匹配项，则返回–1。

**语法**

```sql
{= lastIndexOf(STRING_1, STRING_2) %}: integer
```

| 参数 | 描述 |
| --------- | ----------- |
| `{STRING_1}` | 要检查的字符串。 |
| `{STRING_2}` | 要在第一个参数中搜索的字符串 |

**示例**

```sql
{%= lastIndexOf("hello world","o" ) %}
```

返回7。

## Left trim {#leftTrim}

此 `leftTrim` 函数用于去除字符串开头的空格。

**语法**

```sql
{%= leftTrim(string) %}
```

## Length {#length}

此 `length` 函数用于获取字符串或表达式中的字符数。

**语法**

```sql
{%= length(string) %}
```

**示例**

以下函数返回用户档案的城市名称的长度。

```sql
{%= length(profile.homeAddress.city) %}
```

## 喜欢{#like}

此 `like` 函数用于确定一个字符串是否与指定的模式匹配。

**语法**

```sql
{%= like(STRING_1, STRING_2) %}
```

| 参数 | 描述 |
| --------- | ----------- |
| `{STRING_1}` | 要检查的字符串。 |
| `{STRING_2}` | 要与第一个字符串匹配的表达式。 创建表达式时支持使用两个特殊字符： `%` 和 `_`. <ul><li>`%` 用于表示零个或更多字符。</li><li>`_` 用于恰好表示一个字符。</li></ul> |

**示例**

以下查询检索用户档案所在的所有城市，其中包含“es”模式。

```sql
{%= like(profile.homeAddress.city, "%es%")%}
```

## 小写{#lower}

此 `lowerCase` 函数将字符串转换为小写字母。

**语法**

```sql
{%= lowerCase(string) %}
```

**示例**

此函数将用户档案的名字转换为小写字母。

```sql
{%= lowerCase(profile.person.name.firstName) %}
```

## Matches{#matches}

此 `matches` 函数用于确定一个字符串是否与特定的正则表达式匹配。 请参阅 [本文档](https://docs.oracle.com/javase/8/docs/api/java/util/regex/Pattern.html) 有关正则表达式中匹配模式的详细信息。

**语法**

```sql
{%= matches(STRING_1, STRING_2) %}
```

**示例**

以下查询在不区分大小写的情况下确定人员的姓名是否以“John”开头。

```sql
{%= matches(person.name.,"(?i)^John") %}
```

## 掩码 {#mask}

此 `Mask` 函数可将字符串的一部分替换为“X”字符。

**语法**

```sql
{%= mask(string,integer,integer) %}
```

**示例**

以下查询将“123456789”字符串替换为“X”字符，但前两个字符和后两个字符除外。

```sql
{%= mask("123456789",1,2) %}
```

查询返回 `1XXXXXX89`.

## MD5 {#md5}

此 `md5` 函数用于计算和返回字符串的md5哈希值。

**语法**

```sql
{%= md5(string) %}: string
```

**示例**

```sql
{%= md5("hello world") %}
```

返回“5eb63bbe01eeed093cb22bb8f5acdc3”

## 不等于{#notEqualTo}

此 `notEqualTo` 函数用于确定一个字符串是否不等于指定的字符串。

**语法**

```sql
{%= notEqualTo(STRING_1, STRING_2) %}
```

| 参数 | 描述 |
| --------- | ----------- |
| `{STRING_1}` | 要检查的字符串。 |
| `{STRING_2}` | 要与第一个字符串进行比较的字符串。 |

**示例**

以下查询区分大小写确定人员姓名是否为“John”。

```sql
{%= notEqualTo(profile.person.name,"John") %}
```

## Not Equal With Ignore Case {#not-equal-with-ignore-case}

此 `notEqualWithIgnoreCase` 函数用于比较两个字符串，忽略大小写。

**语法**

```sql
{= notEqualWithIgnoreCase(STRING_1,STRING_2) %}: boolean
```

| 参数 | 描述 |
| --------- | ----------- |
| `{STRING_1}` | 要检查的字符串。 |
| `{STRING_2}` | 要与第一个字符串进行比较的字符串。 |

**示例**

以下查询确定人员姓名是否为“john”，不区分大小写。

```sql
{%= notEqualTo(profile.person.name,"john") %}
```

## 正则表达式组{#regexGroup}

此 `Group` 函数用于根据提供的正则表达式提取特定信息。

**语法**

```sql
{%= regexGroup(STRING, EXPRESSION, GROUP) %}
```

| 参数 | 描述 |
| --------- | ----------- |
| `{STRING}` | 要检查的字符串。 |
| `{EXPRESSION}` | 要与第一个字符串匹配的正则表达式。 |
| `{GROUP}` | 要匹配的表达式组。 |

**示例**

以下查询用于从电子邮件地址中提取域名。

```sql
{%= regexGroup(emailAddress,"@(\\w+)", 1) %}
```

## 更换 {#replace}

此 `replace` 函数用于将字符串中的给定子字符串替换为另一个子字符串。

**语法**

```sql
{%= replace(STRING_1,STRING_2,STRING_3) %}:string
```

| 参数 | 描述 |
| --------- | ----------- |
| `{STRING_1}` | 必须替换子字符串的字符串。 |
| `{STRING_2}` | 要替换的子字符串。 |
| `{STRING_3}` | 替换子字符串。 |

**示例**

```sql
{%= replace("Hello John, here is your monthly newsletter!","John","Mark") %}
```

返回“Hello Mark，这是您每月的新闻稿！”

## Replace All{#replaceAll}

此 `replaceAll` 函数用于将匹配“regex”表达式的文本的所有子字符串替换为指定的文本“replacement”字符串。 正则表达式对“\”和“+”有特殊处理，所有正则表达式都遵循PQL转义策略。 例如，替换操作从字符串的开头到结尾进行，将字符串“aaa”中的“aa”替换为“b”将导致“ba”而不是“ab”。

**语法**

```sql
{%= replaceAll(string,string,string) %}
```

>[!NOTE]
>
> 当用作第二个参数的表达式是特殊正则表达式时，请使用双反斜杠(`//`)。  特殊正则表达式字符包括：[.， +， *， ？， ^， $， (， )， [，]，{， }， |， \.]
> 
> 了解详情，请参阅 [oracle文档](https://docs.oracle.com/javase/7/docs/api/java/util/regex/Pattern.html){_blank}.
>

## Right trim {#rightTrim}

此 `rightTrim` 函数去除字符串末尾的空格。

**语法**

```sql
{%= rightTrim(string) %}
```

## 拆分 {#split}

此 `split` 函数用于按给定字符拆分字符串。

**语法**

```sql
{%= split(string,string) %}
```

## 开始于{#startsWith}

此 `startsWith` 函数用于确定一个字符串是否以指定的子字符串开头。

**语法**

```sql
{%= startsWith(STRING_1, STRING_2, CASE_SENSITIVE) %}
```

| 参数 | 描述 |
| --------- | ----------- |
| `{STRING_1}` | 要检查的字符串。 |
| `{STRING_2}` | 要在第一个字符串中搜索的字符串。 |
| `{CASE_SENSITIVE}` | 用于确定检查是否区分大小写，的可选参数。 默认情况下，该参数设置为true。 |

**示例**

以下查询区分大小写确定人员的姓名是否以“Joe”开头。

```sql
{%= startsWith(person.name,"Joe") %}
```

## String to date {#string-to-date}

此 `stringToDate` 函数将一个字符串值转换为日期时间值。 它采用两个参数：日期时间的字符串表示和格式化器的字符串表示。

**语法**

```sql
{= stringToDate("date-time value","formatter" %}
```

**示例**

```sql
{= stringToDate("2023-01-10 23:13:26", "yyyy-MM-dd HH:mm:ss") %}
```

## String to integer {#string-to-integer}

此 `string_to_integer` 函数用于将字符串值转换为整数值。

**语法**

```sql
{= string_to_integer(string) %}: int
```

## String to number {#string-to-number}

此 `stringToNumber` 函数用于将字符串转换为数字。 对于无效的输入，它返回相同的字符串作为输出。

**语法**

```sql
{%= stringToNumber(string) %}: double
```

## Sub string {#sub-string}

此 `Count string` 函数用于返回字符串表达式在开始索引和结束索引之间的子字符串。
**语法**

```sql
{= substr(string, integer, integer) %}: string
```

## 字首大写{#titleCase}

此 **titleCase** 函数用于将字符串中每个单词的首字母大写。

**语法**

```sql
{%= titleCase(string) %}
```

**示例**

如果该人住在华盛顿高街，则此函数将返回华盛顿高街。

```sql
{%= titleCase(profile.person.location.Street) %}
```

## To Bool {#to-bool}

此 `toBool` 函数用于将参数值转换为布尔值，具体取决于其类型。

**语法**

```sql
{= toBool(string) %}: boolean
```

## To Date Time {#to-date-time}

此 `toDateTime` 函数用于将字符串转换为日期。 对于无效的输入，它返回纪元日期作为输出。

**语法**

```sql
{%= toDateTime(string, string) %}: date-time
```

## To Date Time Only {#to-date-time-only}

此 `toDateTimeOnly` 函数用于将参数值转换为仅日期时间值。 对于无效的输入，它返回纪元日期作为输出。 此函数接受字符串、日期、长整型和int字段类型。

**语法**

```sql
{%= toDateTimeOnly(string/date/long/int) %}: date-time
```

## Trim {#trim}

此 **trim** 函数删除字符串开始和结束位置的所有空格。

**语法**

```sql
{%= trim(string) %}
```

## 大写{#upper}

此 **大写** 函数将字符串转换为大写字母。

**语法**

```sql
{%= upperCase(string) %}
```

**示例**

此函数将用户档案的姓氏转换为大写字母。

```sql
{%= upperCase(profile.person.name.lastName) %}
```

## Url decode {#url-decode}

此 `urlDecode` 函数用于对url编码的字符串进行解码。

**语法**

```sql
{%= urlDecode(string) %}: string
```

## Url encode {#url-encode}

此 `Count only null` 函数用于对字符串进行url编码。

**语法**

```sql
{%= urlEncode(string) %}: string
```
