---
solution: Journey Optimizer
product: journey optimizer
title: 条件指令(if， then， else)
description: 了解条件指令
feature: Journeys
role: Developer
level: Experienced
keywords: 高级，条件，操作，历程
exl-id: 5a5b35a7-e3b5-4dc0-8a87-e985956b04a4
version: Journey Orchestration
TQID: https://experienceleague.adobe.com/SObpEvgu0D-pcoLVaKM7iRffLTSP1stp1zcg4Ygs-vQ
product_v2:
  - id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2:
  - id: b3538224-471e-4c63-a444-9b19d89ae29c
  - id: d998adac-2f81-400b-a669-d07bb196e4eb
subfeature_v2:
  - id: cce82f05-fc3c-4af7-85ff-8bba603861a7
  - id: d8353d85-5da7-453d-bd68-40ad33fa0ab7
role_v2:
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: bf5866b0e7437f93936f573fd83ada8526fe004d
workflow-type: tm+mt
source-wordcount: 576
ht-degree: 0%

---

# 条件指令(if， then， else) {#conditional-instruction}

高级编辑器中支持条件指令(if， then， else)。 它允许定义更复杂的表达式。 它由以下元素组成：

* **[!UICONTROL if]**：首先要计算的条件。
* **[!UICONTROL then]**：条件评估结果为true时要评估的表达式。
* **[!UICONTROL else]**：条件评估结果为false时要评估的表达式。

>[!NOTE]
>
>所有表达式均需要括号。

```json
if  (<expression1>)
then
   (<expression2>)
else
   (<expression3>)
```

`<expression1>`必须返回&#x200B;**布尔值**。

`<expression2>`和`<expression3>`必须具有相同的类型或兼容的类型。 支持的签名和返回的类型包括：

```json
boolean,boolean : boolean
dateTime,dateTime : dateTime
dateTimeOnly,dateTimeOnly : dateTimeOnly
decimal,integer : decimal
integer,decimal : integer
integer,decimal : decimal
duration,duration : duration
string,string : string
listBoolean,listBoolean : listBoolean
listDateTime,listDateTime : listDateTime
listDateTimeOnly,listDateTimeOnly : listDateTimeOnly
listDateOnly,listDateOnly : listDateOnly
listDecimal,listDecimal : listDecimal
listInteger,listInteger : listInteger
listString,listString : listString
```

**用法**

条件指令允许您通过减少条件活动的数量来优化历程工作流。 例如，在同一操作活动中，您可以仅使用一个条件表达式为字段定义指定两个替代项。

操作活动的示例（用于预期字符串作为条件指令结果的字段）：

```json
if (startWithIgnoreCase(@event{eventiOSPushPermissionAllowed.device.model}, 'iPad') or startWithIgnoreCase(@event{eventiOSPushPermissionAllowed.device.model}, 'iOS'))
then
   ('apns')
else
   ('fcm')
```

+++ AI知识参考

本节包含结构化知识，用于支持与本主题相关的解释、检索和问答。

要全面了解相关信息，应将此信息与本页上的文档相结合。 这两个源都不是独立的；页面描述了功能，而本节提供了其他上下文来帮助消除术语、意图、适用性和约束条件的歧义。

* **TL；DR：**&#x200B;本页介绍历程高级表达式编辑器中可用的`if / then / else`条件指令，包括语法规则、支持的类型组合和实用用法示例。

**意图：**

* 使用`if`、`then`和`else`编写条件表达式，以根据布尔条件返回不同的值
* 通过在单个操作活动中嵌入内联条件逻辑，减少历程中的条件活动数
* 确定哪些数据类型组合对`then`和`else`分支有效
* 应用条件指令，根据设备型号将推送通知令牌路由到APNS或FCM

**术语表：**

* **条件指令**：高级编辑器中的`if / then / else`表达式构造，它计算布尔值并返回两个表达式&#x200B;*（产品特定）*&#x200B;之一
* **高级表达式编辑器**：用于编写在条件、等待活动和操作参数映射&#x200B;*（产品特定）*&#x200B;中使用的复杂表达式的Journey Optimizer接口

**护栏：**

* `if`、`then`和`else`子句中的所有表达式都必须有括号
* `if`子句(`<expression1>`)必须返回布尔类型
* `then`和`else`表达式（`<expression2>`和`<expression3>`）必须具有相同的类型或兼容的类型（例如，`decimal`和`integer`兼容，`string`和`integer`不兼容）
* 并非所有类型组合都受支持 — 只有支持签名表中列出的组合才有效

**术语：**

* 规范名称：条件指令 — 首字母缩略词：none — 变体：if/then/else，三元样式条件
* 同义词： &quot;conditional instruction&quot; = &quot;inline condition&quot; = &quot;if-then-else expression&quot;
* 请勿混淆：条件指令（内联表达式）≠条件活动（历程画布节点）

**常见问题解答：**

* **问：`if`子句是否需要用括号括起来？**  — 是，所有表达式（包括`if`子句中的条件）都必须有括号。
* **问：我能否使用`if / then / else`返回一个分支中的数字和另一个分支中的字符串？**  — 否；`<expression2>`和`<expression3>`必须具有相同或兼容的类型。
* **问：条件指令如何降低历程复杂度？**  — 它让您可以使用一个表达式在单个操作活动中指定两个字段值替代项，从而避免在画布上单独显示Condition活动节点。
* **问：如果两个分支都是字符串，条件指令会返回什么类型？**  — 返回`string`。
* **问：`if / then / else`是否可用于选择推送通知渠道？**  — 是；例如，评估设备模型以返回Apple设备的`'apns'`或其他设备的`'fcm'`。

+++
