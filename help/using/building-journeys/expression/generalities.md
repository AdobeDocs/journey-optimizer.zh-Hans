---
solution: Journey Optimizer
product: journey optimizer
title: 语法
description: 了解高级表达式编辑器
feature: Journeys
role: Data Engineer, Architect
level: Experienced
keywords: 语法，编辑器，历程
exl-id: c9434b28-2750-4a53-985e-c4a3f940472c
source-git-commit: d3f0adab52ed8e44a6097c5079396d1e9c06e0a7
workflow-type: tm+mt
source-wordcount: '231'
ht-degree: 3%

---

# 高级表达式编辑器语法 {#syntax}

## 括号和表达式优先级{#parentheses-and-expression-priority}

可使用括号使复杂表达式更易读。 _(&lt;expression>)_ 等同于 _&lt;expression>_. 括号也可用于定义评估顺序和关联性。

将按从左到右的顺序计算表达式。 必须应用算术运算符的相关性：乘法和除优先于加法和减法。 为了限定特定的顺序，必须添加括号以分隔操作。 例如：

<!--```5 + 2 * 10 = 25, and (5 + 2) * 10 = 70```-->

| 表达式 | 评估 |
|--- |--- |
| `4 + 2 * 10` | <ul><li>“*”的优先级高于“+”：2 * 10的计算→20</li><li>4 + 20 → 24</li></ul> |
| `(4 + 2) * 10` | <ul><li>括号将更改优先级： (4 + 2)→6计算</li><li> 6 * 10 → 60</li></ul> |

## 区分大小写{#case-sensitivity}

以下是不同的区分大小写规则：

* 所有运算符（and、or等） 应该写成小写。 例如， _`<expression1>`和`<expression2>`_ 是有效表达式，但表达式 _`<expression1>`和`<expression2>`_ 不是。
* 所有函数名称都区分大小写。 例如， _inAudience()_ 有效，但函数 _INAUDIENCE()_ 不是。
* 字段引用和常量值区分大小写：它们不是语言的内置元素（与运算符和函数相反），而是由最终用户创作。

## 返回的表达式类型{#returned-expression-type}

根据使用上下文，表达式编辑器可以返回不同的值。

| 高级表达式编辑器用法 | 预期返回表达式类型 |
|--- |--- |
| 条件（数据源条件、日期条件） | 布尔 |
| 自定义计时器 | dateTimeOnly |
| 操作参数映射 | 任何 |
