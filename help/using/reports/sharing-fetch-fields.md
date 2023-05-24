---
solution: Journey Optimizer
product: journey optimizer
title: journeyStep 事件数据提取字段
description: journeyStep 事件数据提取字段
feature: Reporting
topic: Content Management
role: User
level: Intermediate
exl-id: 948fe843-47cf-4b20-976a-48069eb9cf5c
source-git-commit: 63c52f04da9fd1a5fafc36ffb5079380229f885e
workflow-type: tm+mt
source-wordcount: '371'
ht-degree: 7%

---

# journeyStep 事件数据提取字段 {#sharing-fetch-fields}

此欄位群組將由journeyStepEvent和journeyStepProfileEvent共用。

在步驟處理期間，我們可以在欄位群組中擷取N筆資料。

## fetchTotalTime {#fetchtotaltime-field}

在步驟處理期間，花費在資料擷取上的總時間（毫秒）。

型別： long

## fetchTypeInError {#fetchtypeinerror-field}

定義發生錯誤的擷取作業是在Adobe Experience Platform上還是在自訂資料來源上。

类型：字符串

值：
* aep
* 自訂

## fetchError {#fetcherror-field}

處理資料擷取時發生的錯誤型別。

类型：字符串

值：
* http
* 上限
* 逾時
* error

## fetchErrorCode {#fetcherrorcode-field}

擷取錯誤的程式碼。 如果錯誤有程式碼（例如HTTP程式碼），則會出現。 例如，如果actionExecError是http，則代碼404代表HTTP 404錯誤。

类型：字符串

## fetchOriginError {#fetchoriginerror-field}

在以下兩種情況下，可能會發生逾時：

* 在第一次嘗試執行動作時。 在此情況下，執行尚未完成，因此沒有基礎錯誤
* 重試：在此情況下，actionExecOrigError/actionExecOrigErrorCode會說明在重試之前嘗試遇到的錯誤。

例如，正在從統一設定檔服務擷取資料，第一次嘗試時會傳回HTTP 500錯誤。 會重試擷取，但2次嘗試的持續時間超過逾時。 然後該動作執行會標籤為逾時。 動作部分看起來會像這樣：

```
    ...
    "fetchTypeInError": "aep",
    "fieldgroupIdInError": "MyProfileFieldgroup",
    "fetchError": "timedout",
    "fetchOrigError": "http",
    "fetchOrigErrorCode": "500"
```

类型：字符串

## fetchOriginErrorCode {#fetchoriginerrorcode-field}

系統提供的錯誤代碼 [!DNL Journey Optimizer] 正在查詢。 例如，可以是404、500等。

类型：字符串

## fetchCount {#fetchcount-field}

擷取資料的次數，無論來源型別為何。

型別： long

## fetchPlatformTotalTime {#fetchplatformtotaltime-field}

從Adobe Experience Platform擷取資料所需的總時間（以毫秒為單位）。 備註：此時間長度是從引擎將擴充事件傳送至擴充服務並接收回應時算起。

型別： long

## fetchPlatformCount {#fetchplatformcount-field}

從Adobe Experience Platform擷取資料的次數。

型別： long

## fetchCustomTotaltime {#fetchcustomtotaltime-field}

擷取自訂資料的時間長度（以毫秒為單位）。 備註：此時間長度是從引擎將擴充事件傳送至擴充服務並接收回應時算起

型別： long

## fetchCustomCount {#fetchcustomcount-field}

從外部系統擷取自訂資料的次數。

型別： long
