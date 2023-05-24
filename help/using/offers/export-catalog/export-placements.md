---
title: 投放位置数据集
description: 本節列出匯出的資料集中用於版位的所有欄位
feature: Offers
topic: Integrations
role: User
level: Intermediate
exl-id: 3e45f3cf-e17e-43a6-8424-98afef07aaa3
source-git-commit: 78675ca22d8ee9a93d9af128d5708c305523da78
workflow-type: tm+mt
source-wordcount: '369'
ht-degree: 5%

---

# 投放位置数据集 {#placements-dataset}

每次修改選件時，都會更新自動產生的版位資料集。

![](../assets/dataset-placements.png)

資料集中最近成功的批次顯示在右側。 資料集的結構描述階層檢視會顯示在左窗格中。

>[!NOTE]
>
>瞭解如何在中存取優惠資料庫每個物件的匯出資料集 [本節](../export-catalog/access-dataset.md).

以下為可用於以下專案的所有欄位清單： **[!UICONTROL 決定物件存放庫 — 位置]** 資料集。

<!--A placement describes a location or place in a personalized message. It is used to set technical constraints for content that the personalization decision supplies. The placement also represents a request to produce certain types of metrics when an experience event is produced where this placement is involved. For instance, the placement facilitates a personalized clickable image inside an email shown to an end-user. The placement may for instance request from the assembled experience that the click on its image gets reported in an experience event with a metric https://ns.adobe.com/xdm/data/metrics/web/linkclicks and a reference to this placement.-->

+++ 标识符

**欄位：** _id
**標題：** 識別碼
**說明：** 記錄的唯一識別碼。
**类型：**&#x200B;字符串

+++

+++ _experience（体验）

**欄位：** 體驗(_E)
**型別：** 物件

+++

+++ 體驗>決策(_E)

**欄位：** 決策
**型別：** 物件

+++

+++ _experience >決策>刊登版位的頻道識別碼

**欄位：** channelid
**標題：** 刊登版位的頻道識別碼
**說明：** 提出主張的管道。 值是有效的管道URI。 請參閱https://ns.adobe.com/xdm/channels/channel。
**类型：**&#x200B;字符串

+++

+++ _experience >決策>內容元件型別

**欄位：** componentType
**標題：** 內容元件型別
**說明：** 列舉的一組URI，其中每個值對應到指定給內容元件的型別。 內容表示的某些消費者期望@type值是描述內容元件其他屬性的結構描述的參考。
**类型：**&#x200B;字符串

+++

+++ _experience >決策> contentTypes

**欄位：** contentType
**型別：** 陣列

+++

+++_體驗>決策>內容型別> MIME媒體型別

**標題：** MIME媒體型別
**說明：** 該位置中預期會出現的元件媒體型別限制。 一個元件可能有多種媒體型別，例如不同的影像格式。
**类型：**&#x200B;字符串

+++

+++ _experience >決策>位置說明

**欄位：** 說明
**標題：** 位置說明
**說明：** 它可用來傳達人類對於如何在整體訊息傳送中使用動態內容的可讀取意圖。 特定空間是網頁中的\&quot;Banner\&quot;通常透過說明而不是正式方法傳遞。
**类型：**&#x200B;字符串

+++

+++ _experience >決策>位置名稱

**欄位：** 名稱
**標題：** 位置名稱
**說明：** 用於放置的指派名稱，可在人與人之間的互動中參照。
**类型：**&#x200B;字符串

+++

+++ 存放庫(_R)

**欄位：** 存放庫(_R)
**型別：** 物件

+++

+++ _repo >版位ETag

**欄位：** etag
**標題：** 刊登ETag
**說明：** 決定選項物件拍攝快照時的修訂版本。
**类型：**&#x200B;字符串

+++
