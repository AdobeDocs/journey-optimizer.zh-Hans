---
title: 优惠投放 API 入门
description: 深入瞭解可用於提供個人化優惠的API。
feature: Offers
topic: Integrations
role: Data Engineer
level: Experienced
exl-id: 7bc1a4ec-113c-4af7-b549-ee17b843b818
source-git-commit: bf738ebac09d5c852872a8ea85f6532ad9d4222d
workflow-type: tm+mt
source-wordcount: '442'
ht-degree: 6%

---

# 优惠投放 API 入门 {#about-decisioning-apis}

您可以使用以下任一專案傳遞優惠方案： **決策** 或 **邊緣決策** API。 此外， **批次決策** API可讓您透過一次呼叫，將優惠傳送至指定區段中的所有設定檔。 區段中每個設定檔的選件內容都會放在Adobe Experience Platform資料集中，可用於自訂批次工作流程。

在本頁中，您會找到特定功能的相關資訊，這些功能包括 **決策** 和 **邊緣決策** API。 雖然兩者皆可讓您將優惠方案傳送給客戶，我們建議您使用 **邊緣決策** API儘可能用於傳入使用案例，並確保平台上有更好的延遲和輸送量。

|  | 要求數/秒 | 延迟 |
|---|---|---|
| Decisioning API | 2000 | &lt;500 毫秒 |
| Edge Decisioning API | 5000 | &lt;250 毫秒 |

如需如何使用API的詳細資訊，請參閱下列章節：
* [Decisioning API](decisioning-api.md)
* [Edge Decisioning API](edge-decisioning-api.md)
* [Batch Decisioning API](batch-decisioning-api.md)

## Edge Decisioning API功能 {#edge}

**體驗事件和決策請求的不重複請求**

有了Edge Decisioning API，您可以在單一請求中傳送體驗事件本身與決策請求，而不是有兩個不同的請求。

例如，如果客戶造訪您的網站，要求會包含體驗事件（客戶造訪頁面的次數），並傳回選件以填入造訪的頁面。

**將內容資料儲存至Adobe Experience Platform**

內容資料是指您只有在要取回優惠方案時才知道的資料。 例如，所購買文章的顏色、購買時的天氣等。

使用Edge Decisioning API請求傳遞內容資料時，資料會儲存至Adobe Experience Platform設定檔，以便日後重複使用。

>[!NOTE]
>
>為了儲存內容資料，您需要設定專用的XDM結構描述。

## 決策API功能 {#decisioning}

下列功能僅適用於Decisioning API。 如果您需要運用其中一個符合需求，請使用Decisioning API。 否則，我們建議使用Edge Decisioning API。

* **體驗事件**：運用體驗事件來建立您的決策規則。
* **選件內容和特性**：您可以選擇不使用專用選項傳回選件的內容和特徵。
* **優惠中繼資料**：啟用一個選項以傳回選件的中繼資料。
* **合併原則**：在您的請求中使用與沙箱關聯的不同合併原則。
* **決策事件和頻率限定**：封鎖決策事件，不讓發生的任何頻率上限計算在內。
* **重複的主張**：啟用不重複主張的選項。
