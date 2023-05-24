---
solution: Journey Optimizer
product: journey optimizer
title: 歷程限制
description: 進一步瞭解歷程限制
feature: Journeys
topic: Content Management
role: User
level: Intermediate
keywords: 歷程，限制
exl-id: 5d59f21c-f76e-45a9-a839-55816e39758a
source-git-commit: 1d30c6ae49fd0cac0559eb42a629b59708157f7d
workflow-type: tm+mt
source-wordcount: '511'
ht-degree: 60%

---

# 限制 {#journey-limitations}

以下是有關使用歷程的限制。

## 一般動作限制

* 无发送限制。 
* 如果出现错误，系统将执行三次重试。无法根据收到的错误消息调整重试次数。 
* 內建 **反應** 事件可讓您對開箱即用的動作做出反應(請參閱此 [頁面](../building-journeys/reaction-events.md))。 如果您想要對透過自訂動作傳送的訊息做出反應，則需要設定專用事件。 
* 无法同时设置两个操作，必须先添加一个，然后再添加另一个操作。

## 歷程版本限制 {#journey-versions-limitations}

* v1 中以事件活动开始的历程，在后续版本中无法以事件之外的其他内容开始。无法以&#x200B;**区段资格**&#x200B;事件开始历程。
* v1 中以&#x200B;**区段资格**&#x200B;活动开始的历程在后续版本中必须始终以&#x200B;**区段资格**&#x200B;开始。
* 在中選擇的區段和名稱空間 **區段資格** （第一個節點）無法在新版本中變更。
* 在所有历程版本中，重新进入规则必须相同。
* 以&#x200B;**读取区段**开始的历程，在后续版本中无法以其他事件开头。
 

## 自訂動作限制

* 自定义操作 URL 不支持动态参数。 
* 仅支持 POST 和 PUT 调用方法. 
* 查询参数或标头的名称不得以“.”或“$”开始。 
* 不允许使用 IP 地址. 
* 不允许使用内部 Adobe 地址 (.adobe.)。 

## 事件限制

* 对于系统生成的事件，必须先在 Journey Optimizer 中配置用于启动客户历程的流数据，才能获取唯一的编排 ID。 此協調流程ID必須附加至傳入Adobe Experience Platform的串流裝載。 此限制不适用于基于规则的事件。 

## 資料來源限制

* 可在客戶歷程中利用外部資料來源即時查詢外部資料。 這些來源必須可透過REST API使用、支援JSON並能夠處理大量請求。

## 在建立設定檔的同時開始的歷程 {#journeys-limitation-profile-creation}

在 Adobe Experience Platform 中，创建/更新基于 API 的配置文件存在延迟。延迟方面的服务水平目标 (SLT) 是在每秒请求量 (RPS) 为 20K 的情况下，从摄取到统一配置文件的第 95% 的请求的延迟小于 1 分钟。

如果在建立設定檔的同時觸發歷程，並立即從設定檔服務檢查/擷取資訊，則可能無法正常運作。

您可以从以下两种解决方案中选择一种：

* 在第一个事件后添加等待活动，以便给 Adobe Experience Platform 提供向用户档案服务执行摄取所需的时间。

* 设置不会立即利用用户档案的历程。例如，如果歷程的設計是要確認帳戶的建立，則體驗事件可能包含傳送第一個確認訊息（名字、姓氏、電子郵件地址等）所需的資訊。

## 讀取區段限制

* 流式处理区段始终是最新的，但在检索时间中不会计算批处理区段。它们每天仅在每日批量评估时间中进行评估。
