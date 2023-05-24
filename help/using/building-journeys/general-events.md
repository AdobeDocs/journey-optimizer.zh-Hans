---
solution: Journey Optimizer
product: journey optimizer
title: 一般事件
description: 瞭解如何使用一般事件
feature: Journeys
topic: Content Management
role: User
level: Intermediate
keywords: 自訂，一般，事件，歷程
exl-id: b1813122-7031-452e-9ac5-a4ea7c6dc57c
source-git-commit: 1d30c6ae49fd0cac0559eb42a629b59708157f7d
workflow-type: tm+mt
source-wordcount: '441'
ht-degree: 20%

---

# 一般事件 {#general-events}

>[!CONTEXTUALHELP]
>id="ajo_journey_event_custom"
>title="一般事件"
>abstract="事件允许您统一触发历程，向流入历程的个人实时发送消息。对于此类事件，只能添加标签和描述。事件配置由数据工程师执行，不可编辑。"

事件允许您统一触发历程，向流入历程的个人实时发送消息。

对于此类事件，只能添加标签和描述。無法編輯其餘的設定。 它由技術使用者執行。 请参阅[此页](../event/about-events.md)。

![](assets/general-events.png)

當您刪除業務事件時，它會自動新增 **讀取區段** 活動。 有關業務事件的詳細資訊，請參閱 [本節](../event/about-events.md)

## 在特定時間接聽事件 {#events-specific-time}

位於歷程中的事件活動會無限期地監聽事件。 若要只在特定時間監聽事件，您必須為事件設定逾時。

然後，歷程將在逾時中指定的時間內接聽事件。 如果在該時段內收到事件，則人員將流經事件路徑。 如果沒有，客戶會進入逾時路徑，或結束其歷程。

若要設定事件逾時，請遵循下列步驟：

1. 啟動 **[!UICONTROL 定義事件逾時]** 事件屬性中的選項。

1. 指定歷程將等候事件的時間長度。

1. 如果在指定的逾時內未收到任何事件時，您要將個人傳送到逾時路徑中，請啟用 **[!UICONTROL 設定逾時路徑]** 選項。 如果未啟用此選項，則一旦達到逾時，個人的歷程將結束。

   ![](assets/event-timeout.png)

在此範例中，歷程會傳送第一個歡迎推播給客戶。 然後，只有在客戶隔天進入餐廳時，它才會傳送餐點折扣推送。 因此，我們將餐廳事件設定為1天逾時：

* 如果在歡迎推播後不到1天收到餐廳事件，則會傳送餐點折扣推播活動。
* 如果在隔天未收到餐廳事件，則人員會流經逾時路徑。

請注意，如果您想要在之後放置的多個事件上設定逾時 **[!UICONTROL 等待]** 活動，您只需要針對這些事件之一設定逾時。

逾時將會套用至位在之後的所有事件。 **[!UICONTROL 等待]** 活動。 如果在指定的逾時前未收到任何事件，則個人會進入單一逾時路徑，或結束其歷程。

![](assets/event-timeout-group.png)
