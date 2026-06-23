---
product: journey optimizer
title: 数学函数
description: 了解数学函数
feature: Journeys
role: Developer
level: Experienced
keywords: 数学，函数，表达式，历程，计算，数字
version: Journey Orchestration
exl-id: da710b22-3112-41fe-8b91-2b6563b79f27
TQID: https://experienceleague.adobe.com/POIbPCZrqtqGjHqn3ehGonxwv9KhKWlgg2igdN8Y4yw
product_v2:
  - id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2:
  - id: d998adac-2f81-400b-a669-d07bb196e4eb
role_v2:
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
subfeature_v2: []
source-git-commit: bf5866b0e7437f93936f573fd83ada8526fe004d
workflow-type: tm+mt
source-wordcount: 475
ht-degree: 2%

---

# 数学函数 {#math-functions}

数学函数为历程表达式中的数值计算提供基本的数学运算。 利用这些函数，可以对数据执行精确的数字计算和转换。

当您需要执行以下操作时，请使用数学函数：

* 生成用于测试、取样或随机化([random](#random))的随机值
* 将小数位四舍五入到最接近的整数，以便显示更干净的数据([round](#round))
* 对数值字段执行数学计算
* 转换数值以实现业务逻辑和决策

数学函数处理十进制和整数类型，自动管理类型转换以确保历程表达式中的结果准确。

## random {#random}

生成一个介于0和1之间的随机数。

+++句法

`random()`

+++

+++签名和返回的类型

`random()`

返回小数。

+++

## round {#round}

返回与参数最接近的整数值，并将四舍五入设置为正无限。

+++句法

`round(<parameters>)`

+++

+++参数

* 小数
* 整数

+++

+++签名和返回的类型

`round(<decimal>)`

`round(<integer>)`

返回整数。

+++

+++示例

`round(3.14)`

返回3。

`round(3.54)`

返回4。

`round(-3.14)`

返回–3。

`round(3)`

返回3。

+++

+++ AI知识参考

本节包含结构化知识，用于支持与本主题相关的解释、检索和问答。

要全面了解相关信息，应将此信息与本页上的文档相结合。 这两个源都不是独立的；页面描述了功能，而本节提供了其他上下文来帮助消除术语、意图、适用性和约束条件的歧义。

* **TL；DR：**&#x200B;本页记录了AJO历程表达式中可用的两个数学函数 — `random`用于生成介于0和1之间的随机小数，而`round`用于将小数或整数四舍五入到最接近的整数。

**意图：**
* 使用`random`生成介于0和1之间的随机十进制值，用于采样或随机化逻辑
* 使用`round`将十进制数字四舍五入到最接近的整数
* 在业务逻辑中应用舍入，其中小数计算需要整数

**术语表：**
* **random**：返回伪随机十进制值的函数，该值从0 （包含）到1 （排除） *（特定于产品）*
* **round**：返回与输入最接近的整数的函数，其中半值将四舍五入到正无穷大

**护栏：**
* `random()`不使用参数
* `round`接受十进制或整数输入并始终返回整数
* `round`中的系结通过舍入到正无穷大来解决（例如，3.5舍入到4，-3.5舍入到–3）

**术语：**
* 规范名称：数学函数 — 首字母缩略词：none — 变体：数学函数，数字函数
* 同义词： &quot;round&quot; = &quot;round to nearest integer&quot;
* 请勿混淆：“四舍五入”（四舍五入到最接近的整数）≠转换函数，如`toInteger`（不四舍五入就截断小数部分）

**常见问题解答：**
* **问：`random()`返回了什么？**  — 返回一个介于0和1之间的随机十进制数。
* **问：`round`如何处理负数？**  — 它四舍五入到正无穷大，因此`round(-3.14)`返回–3，`round(-3.54)`也返回–3（最接近正无穷大的整数）。
* **问：`round`与`toInteger`之间有何区别？** — `round`舍入到最接近的整数（3.7变为4），而`toInteger`在不舍入的情况下截断小数部分（3.7变为3）。
* **问：`random`是否接受任何参数？**  — 否，`random()`不需要参数，并且始终返回介于0和1之间的小数。

+++
