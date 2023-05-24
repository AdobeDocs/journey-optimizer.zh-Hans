---
solution: Journey Optimizer
product: journey optimizer
title: 條件式指令(if、then、else)
description: 瞭解條件式指令
feature: Journeys
role: Data Engineer, Architect
level: Experienced
keywords: 進階，條件，動作，歷程
exl-id: 5a5b35a7-e3b5-4dc0-8a87-e985956b04a4
source-git-commit: 1d30c6ae49fd0cac0559eb42a629b59708157f7d
workflow-type: tm+mt
source-wordcount: '168'
ht-degree: 0%

---

# 條件式指令(if、then、else) {#conditional-instruction}

進階編輯器支援條件式指令(if、then、else)。 它可讓您定義更複雜的運算式。 它由下列元素組成：

* **[!UICONTROL 如果]**：要先評估的條件。
* **[!UICONTROL 則]**：條件評估結果為true時要評估的運算式。
* **[!UICONTROL 否則]**：條件評估結果為false時要評估的運算式。

>[!NOTE]
>
>所有運算式都必須加上括弧。

```json
if  (<expression1>)
then
   (<expression2>)
else
   (<expression3>)
```

`<expression1>` 必須傳回 **布林值**.

`<expression2>` 和 `<expression3>` 必須有相同型別或相容型別。 支援的簽章和傳回的型別包括：

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

條件式指示可讓您透過減少條件活動的數量來最佳化歷程工作流程。 例如，在相同動作活動中，您僅需使用一個條件運算式，即可為欄位定義指定兩個替代專案。

動作活動的範例（適用於預期字串為條件式指令結果的欄位）：

```json
if (startWithIgnoreCase(@{eventiOSPushPermissionAllowed.device.model}, 'iPad') or startWithIgnoreCase(@{eventiOSPushPermissionAllowed.device.model}, 'iOS'))
then
   ('apns')
else
   ('fcm')
```
