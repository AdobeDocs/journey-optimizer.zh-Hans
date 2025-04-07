---
solution: Journey Optimizer
product: journey optimizer
title: 高级表达式编辑器语法
description: 了解高级表达式编辑器中使用的语法
feature: Journeys
role: Data Engineer, Architect
level: Experienced
keywords: 语法，编辑器，历程
exl-id: c9434b28-2750-4a53-985e-c4a3f940472c
source-git-commit: 47185cdcfb243d7cb3becd861fec87abcef1f929
workflow-type: tm+mt
source-wordcount: '262'
ht-degree: 5%

---

# 高级表达式编辑器语法 {#syntax}

下面列出了使用[高级表达式编辑器](expressionadvanced.md)时的语法基础知识。 在[此页](advanced-editor-use-cases.md)上提供了高级表达式编辑器的使用示例。

## 括号和表达式优先级 {#parentheses-and-expression-priority}

可使用括号使复杂表达式更易读。 _（&lt;表达式>）_&#x200B;等同于&#x200B;_&lt;表达式>_。 括号也可用于定义评估顺序和关联性。

将按从左到右的顺序计算表达式。 必须应用算术运算符的相关性：乘法和除优先于加法和减法。 为了限定特定的顺序，必须添加括号以分隔操作。 例如：

<!--```5 + 2 * 10 = 25, and (5 + 2) * 10 = 70```-->

| 表达式 | 评估 |
|--- |--- |
| `4 + 2 * 10` | <ul><li>“*”的优先级高于“+”：2 * 10的计算→20</li><li>4 + 20 → 24</li></ul> |
| `(4 + 2) * 10` | <ul><li>括号将更改优先级： (4 + 2)→6计算</li><li> 6 * 10 → 60</li></ul> |

## 区分大小写 {#case-sensitivity}

以下是不同的区分大小写规则：

* 所有运算符（和、或等）都应小写。 例如，_`<expression1>`和`<expression2>`_&#x200B;是有效的表达式，而表达式&#x200B;_`<expression1>`AND`<expression2>`_&#x200B;则无效。
* 所有函数名称都区分大小写。 例如，_inAudience()_&#x200B;有效，而函数&#x200B;_INAUDIENCE()_&#x200B;无效。
* 字段引用和常量值区分大小写：它们不是语言的内置元素（与运算符和函数相反），而是由最终用户创作。

## 返回的表达式类型 {#returned-expression-type}

根据使用上下文，表达式编辑器可以返回不同的值。

| 高级表达式编辑器用法 | 预期返回表达式类型 |
|--- |--- |
| 条件（数据源条件、日期条件） | 布尔 |
| 自定义计时器 | dateTimeOnly |
| 操作参数映射 | 任何 |
