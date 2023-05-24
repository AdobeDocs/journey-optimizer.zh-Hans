---
solution: Journey Optimizer
product: journey optimizer
title: 回應事件
description: 瞭解反應事件
feature: Journeys
topic: Content Management
role: User
level: Intermediate
keywords: 歷程，事件，反應，追蹤，平台
exl-id: 235384f3-0dce-4797-8f42-1d4d01fa42d9
source-git-commit: 1d30c6ae49fd0cac0559eb42a629b59708157f7d
workflow-type: tm+mt
source-wordcount: '375'
ht-degree: 21%

---

# 反应事件 {#reaction-events}

>[!CONTEXTUALHELP]
>id="ajo_journey_event_reaction"
>title="反应事件"
>abstract="您可以通过此活动，对在同一历程中与所发送消息相关的跟踪数据做出反应。我们在与 Adobe Experience Platform 共享时实时捕获此信息。"

在浮動視窗中可用的不同事件活動中，您會找到內建的 **[!UICONTROL 回應]** 事件。 您可以通过此活动，对在同一历程中与所发送消息相关的跟踪数据做出反应。我们在与 Adobe Experience Platform 共享时实时捕获此信息。

您可以對點按或開啟的訊息做出反應。

您也可以使用此機制，在訊息沒有反應時執行動作。 若要這麼做，請建立與反應活動平行的第二個路徑，並新增等待活動。 如果在等待活動中定義的期間內沒有反應，將選擇第二個路徑。 例如，您可以選擇傳送後續追蹤訊息。

請注意，您只能在畫布中使用回應活動，前提是在之前有管道動作活動（電子郵件和推播）。

另請參閱 [關於動作活動](../building-journeys/about-journey-activities.md#action-activities).

![](assets/journey45.png)

以下是設定反應事件的不同步驟：

1. 新增 **[!UICONTROL 標籤]** 以作出反應。 此步骤是可选的。
1. 從下拉式清單中，選取您要回應的動作活動。 您可以選取位於路徑先前步驟中的任何動作活動。
1. 根據您選取的動作，選擇要回應的專案。
1. 您可以定義事件逾時（40秒至30天之間）和逾時路徑。 這將為未在定義的期間內回應的個人建立第二個路徑。 測試使用反應事件的歷程時，測試模式 **[!UICONTROL 等待時間]** 預設值及最小值為40秒。 请参阅[此小节](../building-journeys/testing-the-journey.md)。

>[!NOTE]
>
>
>反應事件無法追蹤發生在不同歷程中的訊息。
>
>反應事件會追蹤「已追蹤」型別連結上的點按。 未考慮取消訂閱和映象頁面連結。

>[!IMPORTANT]
>
>電子郵件使用者端（例如Gmail）允許影像封鎖。 系統會使用電子郵件中包含的0畫素影像來追蹤電子郵件開啟次數。 如果影像遭到封鎖，則不會將電子郵件開啟次數列入考量。
