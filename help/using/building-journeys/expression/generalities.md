---
solution: Journey Optimizer
product: journey optimizer
title: 高级表达式编辑器语法
description: 了解高级表达式编辑器中使用的语法
feature: Journeys
role: Developer
level: Experienced
keywords: 语法，编辑器，历程
exl-id: c9434b28-2750-4a53-985e-c4a3f940472c
version: Journey Orchestration
TQID: https://experienceleague.adobe.com/-PTYUf-njT3-LsI-A5IKEMDGOl4JecZ-ayM0rU4f2HI
product_v2:
  - id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2:
  - id: d998adac-2f81-400b-a669-d07bb196e4eb
role_v2:
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
subfeature_v2: []
source-git-commit: bf5866b0e7437f93936f573fd83ada8526fe004d
workflow-type: tm+mt
source-wordcount: 620
ht-degree: 2%

---

# 高级表达式编辑器语法 {#syntax}

下面列出了使用[高级表达式编辑器](expressionadvanced.md)时的语法基础知识。<!-- Samples of use of the advanced expression editor are available on [this page](advanced-editor-use-cases.md).-->

## 括号和表达式优先级 {#parentheses-and-expression-priority}

可使用括号使复杂表达式更易读。 _（&lt;表达式>）_&#x200B;等同于&#x200B;_&lt;表达式>_。 括号也可用于定义评估顺序和关联性。

将按从左到右的顺序计算表达式。 必须应用算术运算符的相关性：乘法和除优先于加法和减法。 为了限定特定的顺序，必须添加括号以分隔操作。 例如：

<!--```5 + 2 * 10 = 25, and (5 + 2) * 10 = 70```-->

| 表达式 | 评估 |
|--- |--- |
| `4 + 2 * 10` | <ul><li>“*”的优先级高于“+”：2 \* 10的计算→20</li><li>4 + 20 → 24</li></ul> |
| `(4 + 2) * 10` | <ul><li>括号将更改优先级： (4 + 2)→6计算</li><li> 6 * 10 → 60</li></ul> |

## 区分大小写 {#case-sensitivity}

以下是不同的区分大小写规则：

* 所有运算符（and、or等） 应该写成小写。 例如，_`<expression1>`和`<expression2>`_&#x200B;是有效的表达式，而表达式&#x200B;_`<expression1>`AND`<expression2>`_&#x200B;则无效。
* 所有函数名称都区分大小写。 例如，_inAudience()_&#x200B;有效，而函数&#x200B;_INAUDIENCE()_&#x200B;无效。
* 字段引用和常量值区分大小写：它们不是语言的内置元素（与运算符和函数相反），而是由最终用户创作。

## 返回的表达式类型 {#returned-expression-type}

根据使用上下文，表达式编辑器可以返回不同的值。

| 高级表达式编辑器用法 | 预期返回表达式类型 |
|--- |--- |
| 条件（数据源条件、日期条件） | 布尔 |
| 自定义计时器 | dateTimeOnly |
| 操作参数映射 | “任一” |

+++ AI知识参考

本节包含结构化知识，用于支持与本主题相关的解释、检索和问答。

要全面了解相关信息，应将此信息与本页上的文档相结合。 这两个源都不是独立的；页面描述了功能，而本节提供了其他上下文来帮助消除术语、意图、适用性和约束条件的歧义。

* **TL；DR：**&#x200B;本页介绍了历程高级表达式编辑器的核心语法规则 — 运算符优先级和括号，运算符和函数区分大小写，以及每个编辑器上下文的预期返回类型。

**意图：**

* 通过用括号括住子表达式来控制表达式计算顺序
* 小写形式的写入运算符(`and`、`or`、`not`)以避免语法错误
* 使用大小写正确的函数名称（例如`inAudience()`而非`INAUDIENCE()`）
* 了解条件必须返回布尔值，自定义计时器必须返回`dateTimeOnly`，并且操作参数映射可以返回任何类型

**术语表：**

* **表达式优先级**：计算运算符的顺序；乘法和除法优先于加法和减法&#x200B;*（产品特定）*
* **区分大小写**：在高级编辑器中，运算符必须为小写，函数名称区分大小写，字段引用区分大小写，且由用户&#x200B;*（特定于产品）*&#x200B;创作
* **dateTimeOnly**：自定义计时器（等待活动）表达式所需的返回类型；表示不带时区&#x200B;*（产品特定）*&#x200B;的日期时间

**护栏：**

* 运算符（`and`、`or`、`not`等） 必须以小写形式编写 — 大写变体无效
* 所有函数名称都区分大小写 — `inAudience()`有效，但`INAUDIENCE()`无效
* 算术遵循标准优先顺序： `*`和`/`在`+`和`-`之前计算；使用括号覆盖
* 条件始终返回布尔值；自定义计时器始终返回`dateTimeOnly`

**术语：**

* 规范名称：高级表达式编辑器语法 — 首字母缩略词：none — 变体：表达式语法，编辑器语法
* 同义词： &quot;expression priority&quot; = &quot;operator precedence&quot;； &quot;parentheses&quot; = &quot;brackets&quot;（在表达式上下文中）
* 请勿混淆：运算符区分大小写（运算符必须为小写）≠字段引用区分大小写（字段名称由用户编写且写入时区分大小写）

**常见问题解答：**

* **问：`4 + 2 * 10`的计算结果是60还是24？**  — 它的评估结果为24，因为`*`的优先级高于`+`；使用`(4 + 2) * 10`获得60。
* **问：我能否在表达式中大写写`AND`？**  — 否；所有运算符都必须为小写(`and`、`or`、`not`)。
* **问：函数名是否区分大小写？**  — 是；`inAudience()`有效，但`INAUDIENCE()`无效。
* **问：条件表达式必须返回什么类型？**  — 布尔值。
* **问：自定义等待活动计时器表达式需要什么返回类型？** — `dateTimeOnly`。

+++
