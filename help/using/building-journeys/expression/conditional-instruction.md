---
solution: Journey Optimizer
product: journey optimizer
title: 条件指令(if， then， else)
description: 了解条件指令
feature: Journeys
role: Data Engineer
level: Experienced
exl-id: 5a5b35a7-e3b5-4dc0-8a87-e985956b04a4
source-git-commit: d17e64e03d093a8a459caef2fb0197a5710dfb7d
workflow-type: tm+mt
source-wordcount: '161'
ht-degree: 0%

---

# 条件指令(if， then， else) {#conditional-instruction}

高级编辑器支持条件指令（如果，则为else）。 它允许定义更复杂的表达式。 它由以下元素组成：

* **[!UICONTROL if]**:要先评估的条件。
* **[!UICONTROL then]**:在条件评估结果为true时要评估的表达式。
* **[!UICONTROL else]**:条件评估结果为false时要评估的表达式。

>[!NOTE]
>
>所有表达式周围都需要括号。

```json
if  (<expression1>)
then
   (<expression2>)
else
   (<expression3>)
```

`<expression1>` 必须返回 **布尔**.

`<expression2>` 和 `<expression3>` 必须具有相同类型或兼容类型。 支持的签名和返回的类型包括：

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

**使用情况**

条件说明允许您通过减少条件活动的数量来优化历程工作流。 例如，在同一操作活动中，您只能使用一个条件表达式为字段定义指定两个替换项。

操作活动的示例（对于条件指令结果需要字符串的字段）：

```json
if (startWithIgnoreCase(@{eventiOSPushPermissionAllowed.device.model}, 'iPad') or startWithIgnoreCase(@{eventiOSPushPermissionAllowed.device.model}, 'iOS'))
then
   ('apns')
else
   ('fcm')
```
