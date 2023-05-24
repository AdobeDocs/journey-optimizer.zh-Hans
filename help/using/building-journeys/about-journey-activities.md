---
solution: Journey Optimizer
product: journey optimizer
title: 历程活动入门
description: 历程活动入门
feature: Journeys
topic: Content Management
role: User
level: Intermediate
keywords: 歷程，活動，開始，事件，動作
exl-id: 239b3d72-3be0-4a82-84e6-f219e33ddca4
source-git-commit: 803c9f9f05669fad0a9fdeeceef58652b6dccf70
workflow-type: tm+mt
source-wordcount: '507'
ht-degree: 18%

---

# 历程活动入门 {#about-journey-activities}

结合不同的事件、编排和操作活动，构建多步跨渠道方案。

## 事件活动 {#event-activities}

事件會觸發個人化歷程，例如線上購買。 當某人進入歷程時，就會以個人身分穿過，而且不會有兩個人以相同的速度或路徑穿過。 當您使用事件開始您的歷程時，歷程會在收到事件時觸發。 接著，歷程中的每個人都個別遵循歷程中定義的後續步驟。

技術使用者設定的事件(請參閱 [此頁面](../event/about-events.md))都會顯示在畫面左側的浮動視窗第一個類別中。 可使用下列事件活動：

* [一般事件](../building-journeys/general-events.md)
* [反应](../building-journeys/reaction-events.md)
* [區段資格](../building-journeys/segment-qualification-events.md)

![](assets/journey43.png)

拖放事件活動以開始您的歷程。 您也可以連按兩下它。

![](assets/journey44.png)

## 编排活动 {#orchestration-activities}

協調活動是不同的條件，可協助判斷歷程的下一步。 可能是此人是否擁有未解決的支援案例、目前所在位置的天氣預報、是否完成購買或達到10,000點忠誠度。

從浮動視窗的畫面左側，提供下列協調活動：

* [条件](../building-journeys/condition-activity.md)
* [等待](../building-journeys/wait-activity.md)
* [讀取區段](../building-journeys/read-segment.md)

![](assets/journey49.png)

## 操作活动 {#action-activities}

動作是您希望因某種觸發而發生的動作，例如傳送訊息。 這是客戶體驗的歷程。

從浮動視窗的熒幕左側，下方的 **[!UICONTROL 事件]** 和 **[!UICONTROL 協調流程]**，您可以找到 **[!UICONTROL 動作]** 類別。 可使用下列動作活動：

* [电子邮件、短信、推送](../building-journeys/journeys-message.md)
* [自定义操作](../building-journeys/using-custom-actions.md)
* [跳转](../building-journeys/jump.md)

![](assets/journey58.png)

这些活动代表各种的可用通信渠道。您可以結合這些案例來建立跨管道情境。

如果您已設定自訂動作，它們也會顯示在這裡。 [了解详情](../building-journeys/using-custom-actions.md)).

## 最佳实践 {#best-practices}

### 新增標籤

大部分活動都可讓您定義 **[!UICONTROL 標籤]**. 這會在名稱中新增尾碼，該名稱會出現在畫布中的活動下方。 如果您在歷程中多次使用相同的活動，且想要更輕鬆地識別它們，這會很有用。 它也會讓發生錯誤時的偵錯更容易，並讓報表更易於閱讀。 您也可以新增選用的 **[!UICONTROL 說明]**.

![](assets/journey-action-label.png)

### 管理進階引數 {#advanced-parameters}

大多數活動會顯示許多您無法修改的進階和/或技術引數。

![](assets/journey-advanced-parameters.png)

為了提高可讀性，您可以使用 **[!UICONTROL 隱藏唯讀欄位]** 按鈕。

![](assets/journey-hide-read-only-fields.png)

在某些特定內容中，您可以覆寫這些引數的值以供特定使用。 要强制使用某个值，请单击字段右侧的&#x200B;**[!UICONTROL 启用参数覆盖]**&#x200B;图标。[了解详情](../configuration/primary-email-addresses.md#journey-parameters)

![](assets/journey-enable-parameter-override.png)

### 新增替代路徑

当操作或条件中发生错误时，个人历程将停止。唯一能讓它繼續的方法就是勾選方塊 **[!UICONTROL 在逾時或錯誤的情況下新增替代路徑]**. 请参阅[此小节](../building-journeys/using-the-journey-designer.md#paths)。

![](assets/journey42.png)
