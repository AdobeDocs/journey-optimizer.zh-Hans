---
solution: Journey Optimizer
product: journey optimizer
title: 步骤事件字段列表
description: 步骤事件字段列表
feature: Reporting
topic: Content Management
role: User
level: Intermediate
exl-id: e96efa67-ee47-40b9-b680-f5119d8c3481
source-git-commit: 63c52f04da9fd1a5fafc36ffb5079380229f885e
workflow-type: tm+mt
source-wordcount: '306'
ht-degree: 18%

---

# 步骤事件字段列表 {#sharing-field-list}

步驟事件欄位會依類別組織。

* 除錯資訊欄位
* 历程字段
* 設定檔欄位
* 服務事件欄位

## debugInfo {#debuginfo-field}

| 字段名称 | 类型 | 描述 |
|---|---|------------|
| requestId | 字符串 | Journey Optimizer用來追蹤請求流程的請求ID。 |

## 歷程 {#journey-field}

此欄位群組用於歷程綱要（與journeyStepEvent相關）。 它包含下列欄位：

| 字段名称 | 类型 | 描述 |
|---|---|------------|
| ID | 字符串 | 指定歷程的識別碼 |
| VersionID | 字符串 | 歷程版本的ID。 此ID代表歷程的身分 |
| name | 字符串 | 歷程名稱 |
| 描述 | 字符串 | 歷程描述 |
| version | 字符串 | 版本，表示為 `major`.`minor` |

## 設定檔 {#profile-field}

此欄位群組是journeyStepEvent的專屬群組：此事件與歷程有關，且沒有identityMap，說明設定檔身分（如有）。

若為journeyStepEvent，我們還需要新增與身分相關的欄位：

| 字段名称 | 类型 | 描述 |
|---|---|------------|
| ID | 字符串 | 設定檔識別碼會識別歷程中傳送/使用的設定檔。 例如： foo@adobe.com。 |
| namespace | 字符串 | 此欄位說明歷程中使用的設定檔所參考的名稱空間。 例如：電子郵件、ECID |

## serviceEvents {#servicevents-field}

此Mixin包含與設定檔匯出作業對應的所有欄位。

| 字段名称 | 类型 | 描述 |
|---|---|------------|
| ID | 字符串 | 已觸發區段匯出作業的識別碼 |
| 狀態 | 字符串 | 區段匯出工作的狀態：已排入佇列、已啟動、已完成 |
| exportCountTotal | 整数 | 區段匯出作業的最大可能值 |
| exportCountRealized | 整数 | 透過工作匯出的實際區段數 |
| exportCountFailed | 整数 | 透過工作匯出時失敗的區段數 |
| exportSegmentID | 字符串 | 正在匯出的區段識別碼 |
| 事件型別 | 字符串 | 表示它是否為資訊事件的錯誤事件的事件型別：資訊、錯誤 |
| eventcode | 字符串 | 指示對應eventType原因的錯誤代碼 |

## stepEvents {#stepevents-field}

此類別包含原始步驟事件欄位。 请参阅此[章节](../reports/sharing-legacy-fields.md)。
