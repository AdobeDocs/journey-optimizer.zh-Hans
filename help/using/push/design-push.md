---
solution: Journey Optimizer
product: journey optimizer
title: 設計推播通知
description: 瞭解如何在Journey Optimizer中設計推播通知
feature: Overview
topic: Content Management
role: User
level: Beginner
exl-id: 6f6d693d-11f2-48b7-82a8-171829bf8045
source-git-commit: d1c11881654580247e8d7c92237cad130f11f749
workflow-type: tm+mt
source-wordcount: '1260'
ht-degree: 12%

---

# 設計推播通知 {#design-push-notification}

## 標題與內文 {#push-title-body}

若要撰寫訊息，請按一下 **[!UICONTROL 標題]** 和 **[!UICONTROL 內文]** 欄位。 使用運算式編輯器來定義內容、個人化資料及新增動態內容。 進一步瞭解 [個人化](../personalization/personalize.md) 和 [動態內容](../personalization/get-started-dynamic-content.md) 在運算式編輯器中。

使用裝置預覽區段來視覺化推播通知在iOS和Android裝置上的顯示方式。

## 单击行为 {#on-click-behavior}

>[!CONTEXTUALHELP]
>id="ajo-message-push-onclick"
>title="关于单击行为"
>abstract="选择收件人单击推送通知正文时的行为。"

您可以選取使用者點按推播通知內文時的行為。

![](assets/title-body-push.png)

* 若要開啟應用程式，請選取 **[!UICONTROL 開啟應用程式]** 選項。 與通知相關聯的應用程式定義於 [管道表面](../configuration/channel-surfaces.md) （即訊息預設集）。
* 若要將使用者重新導向至應用程式內的特定內容，請選取 **[!UICONTROL 深層連結]** 選項。  特定內容可以是特定檢視、頁面的特定區段或特定標籤。 選取選項後，請在相關欄位中輸入深層連結。
* 若要將使用者重新導向至外部URL，請使用 **[!UICONTROL 網頁URL]** 選項。 選取選項後，請在相關欄位中輸入URL。

## 新增媒體 {#add-media-push}

在推播通知的iOS版本中，您可以新增將顯示在通知中的影像、影片或GIF。

在Android版本中，您只能新增影像圖示，以及用於展開通知的影像。

![](assets/push-config-add-media.png)

有兩個可用選項。 您可以：

* 使用 **[!UICONTROL 新增媒體]** 按鈕以選取中的資產 **[!DNL Adobe Experience Manager Assets Essentials]**.

   瞭解如何使用 **[!DNL Adobe Experience Manager Assets Essentials]** 在 [此頁面](../email/assets-essentials.md).

* 或者，在中輸入媒體URL **[!UICONTROL 新增媒體]** 欄位。 在這種情況下，您可以將個人化新增至URL。

新增後，媒體會顯示在通知內文的右側。

## 新增按鈕 {#add-buttons-push}

將按鈕新增至推播內容，以建立可操作通知。

如果裝置熒幕已鎖定，則不會顯示這些按鈕：只會顯示 **標題** 和 **訊息** 通知的可見部分。 如果解除鎖定其裝置，收件者將會看到按鈕。

在iOS版本中，您最多可以新增四個按鈕。 在Android版本中，您最多可以新增三個按鈕。

>[!NOTE]
>
>若為iOS，請使用 **[!UICONTROL iOS類別]** 將作業與通知類別產生關聯的欄位。

1. 使用 **[!UICONTROL 新增按鈕]** 若要定義設定：標籤和相關聯的動作。 可能的動作與相同。 [點按行為](#on-click-behavior).

1. 使用 **[!UICONTROL 展開檢視]** 圖示來預覽您的個人化按鈕。

![](assets/push_buttons.png)

## 发送静默通知 {#silent-notification}

>[!CONTEXTUALHELP]
>id="ajo_message_push_silent_notification"
>title="关于静默通知"
>abstract="发送通知但不打扰用户，通知中心或通知栏中不显示通知。"

無訊息推播通知（或背景通知）是傳送至應用程式的隱藏指示。 例如，它可用來通知您的應用程式新內容是否可用，或在背景啟動下載。

選取 **[!UICONTROL 無訊息通知]** 無訊息通知應用程式的選項：在此情況下，通知會直接傳輸到應用程式。 裝置畫面上不會顯示任何警示。

使用 **[!UICONTROL 自訂資料]** 區段來新增索引鍵/值組。

## 自定义数据

在 **[!UICONTROL 自訂資料]** 區段，您可以根據您的行動應用程式設定，將自訂變數新增至裝載。 如需如何在Adobe Experience Platform和Adobe Launch中設定推播通知的詳細資訊，請參閱 [本節](push-gs.md)

## 進階選項 {#advanced-options-push}

您可以設定 **[!UICONTROL 進階選項]** 用於您的推播通知。 可用的引數列示如下：

| 参数 | 描述 |
|---------|---------|
| **[!UICONTROL 可摺疊]** (iOS / Android) | 可收合訊息是訊息，如果訊息已過時，則可由新訊息取代。 可摺疊訊息的常見使用案例是用來指示行動應用程式從伺服器同步資料的訊息。 例如，使用最新分數更新使用者的運動應用程式。 只有最近的訊息才相關。 另一方面，對於不可收合的訊息而言，非常訊息對於使用者端應用程式而言非常重要，需要加以傳送。 |
| **[!UICONTROL 自訂音效]** (iOS / Android) | 在收到通知時，由行動終端機播放的聲音。 應用程式中需要隨附此音效。 |
| **[!UICONTROL 徽章]** (iOS / Android) | 标记用于直接在应用程序图标上显示新的未读信息数。<br/>当用户打开或从应用程序中读取新内容时，标记值将消失。在设备上收到通知时，可能会刷新或增加相关应用程序的标记值。<br/>例如，如果您儲存客戶的未讀文章數量，您可以運用個人化，為每個客戶傳送唯一的未讀文章徽章值。 如需更多個人化資訊，請參閱 [本節](../personalization/personalize.md). |
| **[!UICONTROL 通知群組]**  (僅限iOS) | 將通知群組關聯至推播通知。<br/>從iOS 12開始，通知群組可讓您將訊息執行緒和通知主題整合到執行緒ID中。 例如，品牌可能會以一個群組ID傳送行銷通知，而以一個或多個不同的ID保留更多營運型別通知。<br/>舉例來說，您可以有groupID： 123 「看看新的春季毛衣系列」和groupID： 456 「您的包裹已送達」通知群組。 在此範例中，所有傳送通知都會整合在群組ID： 456底下。 |
| **[!UICONTROL 通知頻道]** （僅限Android） | 將通知頻道與推播通知建立關聯。<br/>從Android 8.0 （API層級26）開始，所有通知都必須指派給管道才能顯示。 如需詳細資訊，請參閱 [Android開發人員檔案](https://developer.android.com/guide/topics/ui/notifiers/notifications#ManageChannels). |
| **[!UICONTROL 新增內容可用性旗標]** (僅限iOS) | 傳送推播裝載中的可用內容旗標，以確保應用程式在收到推播通知時立即喚醒，這表示應用程式將能夠存取裝載資料。<br/> 即使應用程式在背景執行，且不需要任何使用者互動（例如點選推播通知），此功能仍可運作。不過，如果應用程式未執行，則不適用。 有关更多信息，请参阅 [Apple 开发人员文档](https://developer.apple.com/library/content/documentation/NetworkingInternet/Conceptual/RemoteNotificationsPG/CreatingtheNotificationPayload.html)。 |
| **[!UICONTROL 新增可變內容旗標]** (僅限iOS) | 在推播裝載中傳送可變內容旗標，並允許推播通知內容由iOS SDK中提供的通知服務應用程式擴充功能修改。 有关更多信息，请参阅 [Apple 开发人员文档](https://developer.apple.com/library/content/documentation/NetworkingInternet/Conceptual/RemoteNotificationsPG/ModifyingNotifications.html)。<br/>然後，您可以運用行動應用程式擴充功能，進一步修改所傳送推播通知的內容或簡報 [!DNL Journey Optimizer]. 例如，使用者可以善用此選項來解密資料、變更通知的正文或標題文字、將執行緒識別碼新增到通知等。 |
| **[!UICONTROL 通知可見性]** （僅限Android） | 定義推播通知的可見度。 <br/><b>私人</b> 會在所有鎖定熒幕上顯示通知，但在安全鎖定熒幕隱藏敏感或私人資訊。 <br/><b>公用</b> 會在所有鎖定熒幕上顯示完整通知。 <br/><b>密碼</b> 將不會在安全鎖定熒幕上顯示通知的任何部分。 <br/>如需詳細資訊，請參閱 [Android開發人員檔案](https://developer.android.com/reference/android/app/Notification). |
| **[!UICONTROL 通知優先順序]** （僅限Android） | 定義推播通知的重要性從低到高。 這會決定推播通知傳送時「干擾性」如何。 如需詳細資訊，請參閱 [Android開發人員檔案](https://developer.android.com/guide/topics/ui/notifiers/notifications#importance) |
| **[!UICONTROL 傳遞優先順序]** （僅限Android） | 設定推播通知的高優先順序或一般優先順序。 有关消息优先级的更多信息，请参阅 [Google 开发人员文档](https://firebase.google.com/docs/cloud-messaging/concept-options#setting-the-priority-of-a-message)。 |
