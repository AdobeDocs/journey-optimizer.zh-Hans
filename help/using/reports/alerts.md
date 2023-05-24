---
solution: Journey Optimizer
product: journey optimizer
title: 警报
description: 瞭解如何管理警報
feature: Alerts
topic: Administration
role: Admin
level: Intermediate
exl-id: 0855ca5b-c7af-41c4-ad51-bed820ae5ecf
source-git-commit: 1832f3395b07580e62f32c886a0a4256267b2970
workflow-type: tm+mt
source-wordcount: '258'
ht-degree: 6%

---

# 開始使用警示 {#alerts}

Journey Optimizer會利用Adobe Experience Platform警報功能。 這可讓您透過使用者介面存取系統警示。 您可以查看可用的警报并订阅它们。

當達到您操作中的特定條件集時（例如系統違反臨界值時會發生潛在問題），系統會傳送警報訊息給組織中訂閱警報訊息的任何使用者。 這些訊息可在預先定義的時間間隔內重複，直到警報解決為止。

進一步瞭解Adobe Experience Platform中的警示 [檔案](https://experienceleague.adobe.com/docs/experience-platform/observability/alerts/overview.html?lang=zh-Hans).
若要瞭解如何訂閱及設定警示，請參閱此 [頁面](https://experienceleague.adobe.com/docs/experience-platform/observability/alerts/ui.html).

>[!AVAILABILITY]
>
>「讀取區段觸發失敗」警報的部分設計變更正在進行中，因此此警報目前已暫停，並從使用者介面中暫時移除。 這些變更發佈後，警報將再次顯示，您可以訂閱。

在左側選單中的 **管理**，按一下 **警報**.

<!--A pre-configured alert for Journey Optimizer is available. This alert will warn you if a read segment node has not processed any profile during the defined time frame.

![](assets/alerts1.png)-->

如果發生非預期的行為，會透過介面右上角的電子郵件，將警報通知傳送給警報的訂閱者。

<!--![](assets/alerts2.png)-->


時間 [在Adobe Experience Platform UI中檢視警報規則](https://experienceleague.adobe.com/docs/experience-platform/observability/alerts/ui.html)，您可以個別訂閱每個規則。 透過訂閱警報時 [I/O事件通知](https://experienceleague.adobe.com/docs/experience-platform/observability/alerts/subscribe.html)不過，警報規則會整理成不同的訂閱套件。

<!--The I/O event subscription name corresponding to the Read segment alert is: "Journey read segment Delays, Failures and Errors".

>[!WARNING]
>
>These alerts apply only to live journeys. Alerts will not be triggered for journeys in test mode.-->
