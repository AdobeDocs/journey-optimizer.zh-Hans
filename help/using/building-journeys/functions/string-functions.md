---
product: journey optimizer
title: 字符串函数
description: 了解字符串函数
feature: Journeys
role: Developer
level: Experienced
keywords: 字符串，函数，表达式，历程，文本，操作
version: Journey Orchestration
source-git-commit: bb47ca4957129a4d05aa3d7286409eef0cb62143
workflow-type: tm+mt
source-wordcount: '1127'
ht-degree: 15%

---

# 字符串函数 {#string-functions}

字符串函数允许您处理和处理历程表达式中的文本值。 这些功能对于客户历程中的文本处理、验证、转换和分析至关重要。

在需要时，请使用字符串函数：

* 连接和组合多个文本值（[连接](#concat)）
* 搜索特定的文本模式或子字符串([contain](#contain)，[containIgnoreCase](#containIgnoreCase)，[indexOf](#indexOf)，[lastIndexOf](#lastIndexOf)，[matchRegExp](#matchRegExp))
* 比较具有区分大小写或不区分大小写匹配的字符串([equalIgnoreCase](#equalIgnoreCase)，[notEqualIgnoreCase](#notEqualIgnoreCase))
* 检查字符串的开始和结束([startWith](#startWith)，[startWithIgnoreCase](#startWithIgnoreCase)，[endWith](#endWith)，[endWithIgnoreCase](#endWithIgnoreCase))
* 使用子字符串操作([substr](#substr))提取部分文本
* 将文本转换为大写或小写([upper](#upper)， [lower](#lower)， [trim](#trim))
* 检查字符串是否为空或包含特定值([isEmpty](#isEmpty)，[isNotEmpty](#isNotEmpty))
* 用新值替换文本模式([replace](#replace)，[replaceAll](#replaceAll))
* 将字符串拆分为数组，以便进一步处理（[拆分](#split)）
* 获取字符串长度([length](#length))或生成唯一标识符([uuid](#uuid))

字符串函数提供全面的文本操作功能，从而可以根据历程表达式中的文本内容进行复杂的数据处理和条件逻辑。

## concat {#concat}

连接两个字符串参数或一个字符串列表。

+++句法

`concat(<parameters>)`

+++

+++参数

| 参数 | 类型 |
|-----------|------------------|
| 列表 | listString |
| 字符串 | 字符串 |

+++

+++签名和返回的类型

`concat(<string>,<string>)`

`concat(<listString>)`

返回字符串。

+++

+++示例

`concat("Hello","World")`

返回“HelloWorld”。

`concat(["Hello"," ","World"])`

返回“Hello World”。

+++

## contain {#contain}

检查第二个参数字符串是否包含在第一个参数字符串中。

+++句法

`contain(<parameters>)`

+++

+++参数

* 字符串

+++

+++签名和返回的类型

`contain(<string>,<string>)`

返回布尔值。

+++

+++示例

`contain("rowing is great", "great")`

返回真。

+++

## containIgnoreCase {#containIgnoreCase}

检查第二个参数字符串是否包含在第一个参数字符串中，而不考虑大小写。

+++句法

`containIgnoreCase(<parameters>)`

+++

+++参数

| 参数 | 类型 |
|-----------|------------------|
| 字符串 | 字符串 |
| 搜索字符串 | 字符串 |

+++

+++签名和返回的类型

`containIgnoreCase(<string>,<string>)`

返回布尔值。

+++

+++示例

`containIgnoreCase("rowing is great", "GREAT")`

返回真。

+++

## endWith {#endWith}

如果第二个参数是第一个参数的后缀，则返回true。

+++句法

`endWith(<parameters>)`

+++

+++参数

| 参数 | 类型 |
|-----------|------------------|
| 字符串 | 字符串 |
| 后缀 | 字符串 |

+++

+++签名和返回的类型

`endWith(<string>,<string>)`

返回布尔值。

+++

+++示例

`endWith("Hello World", "World")`

返回真。

`endWith("Hello World", "Hello")`

返回假。

+++

## endWithIgnoreCase {#endWithIgnoreCase}

检查第一个参数字符串是否以特定字符串（第二个参数字符串）结尾，而不考虑大小写。

+++句法

`endWithIgnoreCase(<parameters>)`

+++

+++参数

| 参数 | 类型 |
|-----------|------------------|
| 字符串 | 字符串 |
| 后缀 | 字符串 |

+++

+++签名和返回的类型

`endWithIgnoreCase(<string>,<string>)`

返回布尔值。

+++

+++示例

`endWithIgnoreCase("rowing is great", "AT")`

返回真。

+++

## equalIgnoreCase {#equalIgnoreCase}

将第一个参数字符串与第二个参数字符串进行比较，忽略大小写注意事项。

+++句法

`equalIgnoreCase(<parameters>)`

+++

+++参数

* 字符串

+++

+++签名和返回的类型

`equalIgnoreCase(<string>,<string>)`

返回布尔值。

+++

+++示例

`equalIgnoreCase("rowing is great", "rowing is GREAT")`

返回真。

+++

## indexOf {#indexOf}

返回第二个参数在第一个参数中第一次出现的位置。 如果没有匹配项，则返回–1。

+++句法

`indexOf(<parameters>)`

+++

+++参数

| 参数 | 类型 |
|-----------|------------------|
| 字符串 | 字符串 |
| 指定值 | 字符串 |

+++

+++签名和返回的类型

`indexOf(<string>,<string>)`

返回整数。

+++

+++示例

`indexOf("Hello", "l")`

返回2。

说明：

在“Hello”中，“l”的第一个实例位于位置2。

+++

## isEmpty {#isEmpty}

如果参数中的字符串不含字符，则返回true。

+++句法

`isEmpty(<parameters>)`

+++

+++参数

* 字符串

+++

+++签名和返回的类型

`isEmpty(<string>)`

返回布尔值。

+++

+++示例

`isEmpty("")`

返回真。

`isEmpty("Hello World")`

返回假。

+++

## isNotEmpty {#isNotEmpty}

如果参数中的字符串不为空，则返回真。

+++句法

`isNotEmpty(<parameters>)`

+++

+++参数

* 字符串

+++

+++签名和返回的类型

`isNotEmpty(<string>)`

返回布尔值。

+++

+++示例

`isNotEmpty("")`

返回假。

`isNotEmpty("hello")`

返回真。

+++

## lastIndexOf {#lastIndexOf}

返回第二个参数在第一个参数中最后一次出现的位置。 如果没有匹配项，则返回–1。

+++句法

`lastIndexOf(<parameters>)`

+++

+++参数

| 参数 | 类型 |
|-----------|------------------|
| 字符串 | 字符串 |
| 指定值 | 字符串 |

+++

+++签名和返回的类型

`lastIndexOf(<string>,<string>)`

返回整数。

+++

+++示例

`lastIndexOf("Hello", "l")`

返回3。

说明：

在“Hello”中，“l”的最后一次出现在位置3。

+++

## 长度 {#length}

返回参数中字符串表达式的字符数。

+++句法

`length(<parameters>)`

+++

+++参数

* 字符串

+++

+++签名和返回的类型

`length(<string>)`

返回整数。

+++

+++示例

`length("Hello World")`

返回11。

+++

## lower {#lower}

返回参数的小写版本。

+++句法

`lower(<parameter>)`

+++

+++参数

* 字符串

+++

+++签名和返回的类型

`lower(<string>)`

返回字符串。

+++

+++示例

`lower("A")`

返回“a”。

+++

## matchRegExp {#matchRegExp}

如果第一个参数中的字符串与第二个参数中的正则表达式匹配，则返回true。 有关详细信息，请参阅[此页面](https://docs.oracle.com/javase/7/docs/api/java/util/regex/Pattern.html)。

+++句法

`matchRegExp(<parameters>)`

+++

+++参数

| 参数 | 类型 |
|--- |--- |
| 字符串 | 字符串 |
| regexp | 字符串 |

+++

+++签名和返回的类型

`matchRegExp(<string>,<string>)`

返回布尔值。

+++

+++示例

`matchRegExp("12345", "\\d+")`

返回真。

+++

## notEqualIgnoreCase {#notEqualIgnoreCase}

检查第一个参数字符串与第二个参数字符串是否不同，忽略大小写注意事项。

+++句法

`notEqualIgnoreCase(<parameters>)`

+++

+++参数

* 字符串

+++

+++签名和返回的类型

`notEqualIgnoreCase(<string>,<string>)`

返回布尔值。

+++

+++示例

`notEqualIgnoreCase(@event{iOSPushPermissionAllowed.device.model}, "iPad")`

+++

## replace {#replace}

使用基本字符串中的替换字符串替换匹配目标字符串的第一个匹配项。

例如，替换操作从字符串的开头到结尾进行，将字符串“aaa”中的“aa”替换为“b”将导致“ba”而不是“ab”。

+++句法

`replace(<parameters>)`

+++

+++参数

| 参数 | 类型 |
|-----------|--------------|
| 基础 | 字符串 |
| Target | 字符串(RegExp) |
| 替换 | 字符串 |

+++

+++签名和返回的类型

`replace(<base>,<target>,<replacement>)`

返回字符串。

+++

+++示例

`replace("Hello World", "l", "x")`

返回“Hexlo World”。

**RegExp示例：**

由于target参数是RegExp，因此根据要替换的字符串，您可能需要转义某些字符。 示例如下：

* 要计算的字符串：`|OFFER_A|OFFER_B`
* 由配置文件属性`#{ExperiencePlatform.myFieldGroup.profile.myOffers}`提供
* 要替换的字符串： `|OFFER_A`
* 字符串替换为： `''`
* 您需要在`\\`字符之前添加`|`。

表达式为：

`replace(#{ExperiencePlatform.myFieldGroup.profile.myOffers}, '\\|OFFER_A', '')`

返回的字符串是： `|OFFER_B`

您还可以构建要替换给定属性的字符串：

`replace(#{ExperiencePlatform.myFieldGroup.profile.myOffers}, '\\|' + #{ExperiencePlatform.myFieldGroup.profile.myOfferCode}, '')`

+++

## replaceAll {#replaceAll}

使用基本字符串中的替换字符串替换匹配目标字符串的所有匹配项。

例如，替换操作从字符串的开头到结尾进行，将字符串“aaa”中的“aa”替换为“b”将导致“ba”而不是“ab”。

+++句法

`replaceAll(<parameters>)`

+++

+++参数

| 参数 | 类型 |
|-----------|--------------|
| 基础 | 字符串 |
| Target | 字符串(RegExp) |
| 替换 | 字符串 |

+++

+++签名和返回的类型

`replaceAll(<baseString>,<sourceString>,<replacementString>)`

返回字符串。

+++

+++示例

`replaceAll("Hello World", "l", "x")`

返回“Hexxo Worxd”。

由于target参数是RegExp，因此根据要替换的字符串，您可能需要转义某些字符。 请参阅[replace](#replace)函数中的示例。

+++

## split {#split}

使用分隔符字符串（第二个参数字符串，可以是正则表达式）拆分第一个参数字符串以生成字符串（令牌）列表。

+++句法

`split(<parameters>)`

+++

+++参数

| 参数 | 类型 |
|-----------|------------------|
| 输入字符串 | 字符串 |
| 分隔符字符串 | 字符串 |

+++

+++签名和返回的类型

`split(<input string>, <separator string>)`

返回listString。

+++

+++示例

`split("A_B_C", "_")`

返回`["A","B","C"]`

具有事件字段“event.appVersion”且值为“20.45.2.3434”的示例

`split(@event{event.appVersion}, "\\.")`

返回`["20", "45", "2", "3434"]`

+++

## startWith {#startWith}

如果第二个参数是第一个参数的前缀，则返回true。

+++句法

`startWith(<parameters>)`

+++

+++参数

| 参数 | 类型 |
|-------------|--------|
| 字符串 | 字符串 |
| 前缀 | 字符串 |

+++

+++签名和返回的类型

`startWith(<string>,<string>)`

返回布尔值。

+++

+++示例

`startWith("Hello World", "Hello")`

返回真。

`startWith("Hello World", "World")`

返回假。

+++

## startWithIgnoreCase {#startWithIgnoreCase}

如果第二个参数是第一个参数的前缀而不考虑大小写，则返回true。

+++句法

`startWithIgnoreCase(<parameters>)`

+++

+++参数

| 参数 | 类型 |
|-------------|--------|
| 字符串 | 字符串 |
| 前缀 | 字符串 |

+++

+++签名和返回的类型

`startWithIgnoreCase(<string>,<string>)`

返回布尔值。

+++

+++示例

`startWithIgnoreCase("rowing is great", "RO")`

返回真。

+++

## substr {#substr}

返回字符串表达式在开始索引和结束索引之间的子字符串。 如果未定义结束索引，则它介于开始索引和结束索引之间。

+++句法

`substr(<parameters>)`

+++

+++参数

| 参数 | 类型 |
|-------------|----------|
| 字符串 | 字符串 |
| beginindex | 整数 |
| endIndex | 整数 |

+++

+++签名和返回的类型

`substr(<string>,<beginIndex>)`

`substr(<string>,<beginIndex>,<endIndex>)`

返回字符串。

+++

+++示例

`substr("Hello World",6)`

返回“World”。

`substr("Hello World", 0, 5)`

返回“Hello”。

+++

## trim {#trim}

删除起始和结束空格。

+++句法

`trim(<parameters>)`

+++

+++参数

| 参数 | 类型 |
|-----------|------------------|
| 字符串 | 字符串 |

+++

+++签名和返回的类型

`trim(<string>)`

返回字符串。

+++

+++示例

`trim(" Hello ")`

返回“Hello”。

+++

## upper {#upper}

返回参数的大写版本。

+++句法

`upper(<parameters>)`

+++

+++签名和返回的类型

`upper(<string>)`

返回字符串。

+++

+++示例

`upper("b")`

返回“B”。

+++

## uuid {#uuid}

生成随机UUID（通用唯一标识符）。

+++句法

`uuid()`

+++

+++参数 

此函数不需要参数。

+++

+++签名和返回的类型

`uuid()`

返回字符串。

+++

+++示例

`uuid()`

返回“79e70b7f-8a85-400b-97a1-9f9826121553”。

+++

