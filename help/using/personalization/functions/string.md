---
title: 字符串函数库
description: 字符串函数库
feature: Personalization
topic: Personalization
role: Data Engineer
level: Experienced
exl-id: 8674ef9e-261b-49d9-800e-367f9f7ef979
source-git-commit: 284d95976ab1b58aaea2a4c41db20a3ea5a9b761
workflow-type: tm+mt
source-wordcount: '1686'
ht-degree: 7%

---

# 字符串函数 {#string}

了解如何在表达式编辑器中使用字符串函数。

## 驼峰 {#camelCase}

的 `camelCase` 函数会大写字符串每个单词的第一个字母。

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

的 `concat` 函数将两个字符串组合为一个。

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

的 `contains` 函数来确定字符串是否包含指定的子字符串。

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

的 `doesNotContain` 函数来确定字符串是否不包含指定的子字符串。

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

的 `doesNotEndWith` 函数来确定字符串是否不以指定的子字符串结尾。

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

的 `doesNotStartWith` 函数来确定字符串是否不以指定的子字符串开头。

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

的 `encode64` 函数用于对字符串进行编码，以保留个人信息(PI)（如果要包含在URL中）。

**格式**

```sql
{%= encode64(string) %}
```

## 结束于{#endsWith}

的 `endsWith` 函数来确定字符串是否以指定的子字符串结尾。

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

的 `equals` 函数来确定字符串是否等于指定的字符串（区分大小写）。

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

的 `equalsIgnoreCase` 函数确定字符串是否等于指定的字符串，而不区分大小写。

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

的 `extractEmailDomain` 函数来提取电子邮件地址的域。

**格式**

```sql
{%= extractEmailDomain(string) %}
```

**示例**

以下查询会提取个人电子邮件地址的电子邮件域。

```sql
{%= extractEmailDomain(profile.personalEmail.address) %}
```

## 获取URL主机 {#get-url-host}

的 `getUrlHost` 函数用于检索URL的主机名。

**格式**

```sql
{%= getUrlHost(string) %}: string
```

**示例**

```sql
{%= getUrlHost("http://www.myurl.com/contact") %}
```

返回&quot;www.myurl.com&quot;

## 获取URL路径 {#get-url-path}

的 `getUrlPath` 函数用于检索URL域名后的路径。

**格式**

```sql
{%= getUrlPath(string) %}: string
```

**示例**

```sql
{%= getUrlPath("http://www.myurl.com/contact.html") %}
```

返回&quot;/contact.html&quot;

## 获取URL协议 {#get-url-protocol}

的 `getUrlProtocol` 函数来检索URL的协议。

**格式**

```sql
{%= getUrlProtocol(string) %}: string
```

**示例**

```sql
{%= getUrlProtocol("http://www.myurl.com/contact.html") %}
```

返回“http”

## 索引 {#index-of}

的 `indexOf` 函数用于返回（在第一参数中）第二参数第一次出现的位置。 如果没有匹配项，则返回–1。

**格式**

```sql
{%= indexOf(STRING_1, STRING_2) %}: integer
```

| 参数 | 描述 |
| --------- | ----------- |
| `{STRING_1}` | 要执行检查的字符串。 |
| `{STRING_2}` | 要在第一个参数中搜索的字符串 |

**示例**

```sql
{%= indexOf("hello world","world" ) %}
```

返回6。

## 为空 {#isEmpty}

的 `isEmpty` 函数来确定字符串是否为空。

**格式**

```sql
{%= isEmpty(string) %}
```

**示例**

如果用户档案的手机号码为空，则以下函数会返回“true”。 否则，将返回“false”。

```sql
{%= isEmpty(profile.mobilePhone.number) %}
```

## 不为空 {#is-not-empty}

的 `isNotEmpty` 函数来确定字符串是否不为空。

**格式**

```sql
{= isNotEmpty(string) %}: boolean
```

**示例**

如果用户档案的手机号码不为空，则以下函数会返回“true”。 否则，将返回“false”。

```sql
{%= isNotEmpty(profile.mobilePhone.number) %}
```

## 最后一个索引 {#last-index-of}

的 `lastIndexOf` 函数用于返回（在第一个参数中）第二个参数最后一个实例的位置。 如果没有匹配项，则返回–1。

**格式**

```sql
{= lastIndexOf(STRING_1, STRING_2) %}: integer
```

| 参数 | 描述 |
| --------- | ----------- |
| `{STRING_1}` | 要执行检查的字符串。 |
| `{STRING_2}` | 要在第一个参数中搜索的字符串 |

**示例**

```sql
{%= lastIndexOf("hello world","o" ) %}
```

返回7。

## 左裁切 {#leftTrim}

的 `leftTrim` 函数从字符串的开头删除空格。

**格式**

```sql
{%= leftTrim(string) %}
```

## Length {#length}

的 `length` 函数，用于获取字符串或表达式中的字符数。

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

的 `like` 函数来确定字符串是否与指定的模式匹配。

**格式**

```sql
{%= like(STRING_1, STRING_2) %}
```

| 参数 | 描述 |
| --------- | ----------- |
| `{STRING_1}` | 要执行检查的字符串。 |
| `{STRING_2}` | 要与第一个字符串匹配的表达式。 创建表达式时，有两个受支持的特殊字符： `%` 和 `_`. <ul><li>`%` 用于表示零个或多个字符。</li><li>`_` 仅用于表示一个字符。</li></ul> |

**示例**

以下查询可检索用户档案所在的所有城市，其中包含模式“es”。

```sql
{%= like(profile.homeAddress.city, "%es%")%}
```

## 小写{#lower}

的 `lowerCase` 函数将字符串转换为小写字母。

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

的 `matches` 函数来确定字符串是否与特定正则表达式匹配。 请参阅 [本文档](https://docs.oracle.com/javase/8/docs/api/java/util/regex/Pattern.html) 有关正则表达式中匹配模式的更多信息。

**格式**

```sql
{%= matches(STRING_1, STRING_2) %}
```

**示例**

以下查询可在不区分大小写的情况下确定人员姓名是否以“John”开头。

```sql
{%= matches(person.name.,"(?i)^John") %}
```

## 蒙版(#mask)

的 `Mask` 函数将字符串的一部分替换为“X”字符。

**格式**

```sql
{%= mask(string,integer,integer) %}
```

**示例**

以下查询会将“123456789”字符串替换为“X”字符，但前两个和后两个字符除外。

```sql
{%= mask("123456789",1,2) %}
```

查询会返回 `1XXXXXX89`.

## MD5 {#md5}

的 `md5` 函数计算并返回字符串的md5哈希。

**格式**

```sql
{%= md5(string) %}: string
```

**示例**

```sql
{%= md5("hello world") %}
```

返回“5eb63bbe01eeed093cb22bb8f5acdc3”

## 不等于{#notEqualTo}

的 `notEqualTo` 函数来确定字符串是否不等于指定的字符串。

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

## 不等于忽略大小写 {#not-equal-with-ignore-case}

的 `notEqualWithIgnoreCase` 函数来比较两个忽略大小写的字符串。

**格式**

```sql
{= notEqualWithIgnoreCase(STRING_1,STRING_2) %}: boolean
```

| 参数 | 描述 |
| --------- | ----------- |
| `{STRING_1}` | 要执行检查的字符串。 |
| `{STRING_2}` | 要与第一个字符串比较的字符串。 |

**示例**

以下查询可确定人员姓名是否不是“john”（不区分大小写）。

```sql
{%= notEqualTo(profile.person.name,"john") %}
```

## 正则表达式组{#regexGroup}

的 `Group` 函数用于根据提供的正则表达式提取特定信息。

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

## 替换 {#replace}

的 `replace` 函数将字符串中的给定子字符串替换为其他子字符串。

**格式**

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

返回“Hello Mark，这是您的月度快讯！”

## 全部替换{#replaceAll}

的 `replaceAll` 函数将匹配“target”的文本的所有子字符串替换为指定的文字“replacement”字符串。 替换从字符串的开头到结尾，例如，将字符串“aaa”中的“aa”替换为“b”将生成“ba”而不是“ab”。

**格式**

```sql
{%= replaceAll(string,string,string) %}
```

## 右修剪 {#rightTrim}

的 `rightTrim` 函数会从字符串的末尾删除空格。

**格式**

```sql
{%= rightTrim(string) %}
```

## 拆分 {#split}

的 `split` 函数将字符串按给定字符拆分。

**格式**

```sql
{%= split(string,string) %}
```

## 开始于{#startsWith}

的 `startsWith` 函数来确定字符串是否以指定的子字符串开头。

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

## 字符串到整数 {#string-to-integer}

的 `string_to_integer` 函数将字符串值转换为整数值。

**格式**

```sql
{= string_to_integer(string) %}: int
```

## 字符串到数字 {#string-to-number}

的 `stringToNumber` 函数将字符串转换为数字。 它会返回与无效输入输出相同的字符串。

**格式**

```sql
{%= stringToNumber(string) %}: double
```

## 子字符串 {#sub-string}

的 `Count string` 函数用于返回介于开始索引和结束索引之间的字符串表达式的子字符串。
**格式**

```sql
{= substr(string, integer, integer) %}: string
```

## 标题大小写{#titleCase}

的 **titleCase** 函数用于大写字符串中每个单词的首字母。

**语法**

```sql
{%= titleCase(string) %}
```

**示例**

如果这人住在华盛顿大街，这个功能将返回华盛顿大街。

```sql
{%= titleCase(profile.person.location.Street) %}
```

## 至布尔 {#to-bool}

的 `toBool` 函数将参数值转换为布尔值，具体取决于其类型。

**格式**

```sql
{= toBool(string) %}: boolean
```

## 截止时间 {#to-date-time}

的 `toDateTime` 函数将字符串转换为日期。 它返回纪元日期作为无效输入的输出。

**格式**

```sql
{%= toDateTime(string, string) %}: date-time
```

## 仅截止日期时间 {#to-date-time-only}

的 `toDateTimeOnly` 函数将参数值转换为仅限日期时间的值。 它返回纪元日期作为无效输入的输出。

**格式**

```sql
{%= toDateTimeOnly(string) %}: date-time
```

## 修剪{#trim}

的 **trim** 函数会删除字符串开头和结尾的所有空格。

**语法**

```sql
{%= trim(string) %}
```

## 大写{#upper}

的 **upperCase** 函数将字符串转换为大写字母。

**语法**

```sql
{%= upperCase(string) %}
```

**示例**

此函数可将用户档案的姓氏转换为大写字母。

```sql
{%= upperCase(profile.person.name.lastName) %}
```

## url解码 {#url-decode}

的 `urlDecode` 函数对url编码的字符串进行解码。

**格式**

```sql
{%= urlDecode(string) %}: string
```

## Url编码 {#url-encode}

的 `Count only null` 函数用于对字符串进行url编码。

**格式**

```sql
{%= urlEncode(string) %}: string
```
