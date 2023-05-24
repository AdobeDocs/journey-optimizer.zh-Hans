---
solution: Journey Optimizer
product: journey optimizer
title: 向订阅者发送消息
description: 瞭解如何建立歷程，以傳送訊息給清單的訂閱者
feature: Journeys
topic: Content Management
role: User
level: Intermediate
keywords: 歷程，使用案例，訊息，訂閱者，清單，讀取
exl-id: 2540938f-8ac7-43fa-83ff-fed59f6bc417
source-git-commit: 803c9f9f05669fad0a9fdeeceef58652b6dccf70
workflow-type: tm+mt
source-wordcount: '331'
ht-degree: 17%

---

# 使用案例：傳送訊息給清單的訂閱者{#send-a-message-to-the-subscribers-of-a-list}

此使用案例的目的是建立歷程，向清單的訂閱者傳送訊息。

在此範例中， **[!UICONTROL 同意和偏好設定詳細資料]** 欄位群組來源 [!DNL Adobe Experience Platform] 已使用。 若要尋找此欄位群組，請從 **[!UICONTROL 資料管理]** 功能表，選擇 **[!UICONTROL 結構描述]**. 於 **[!UICONTROL 欄位群組]** 索引標籤中，在搜尋欄位中輸入欄位群組的名稱。

![此欄位群組包含訂閱元素](assets/consent-and-preference-details-field-group.png)

若要設定此歷程，請遵循下列步驟：

1. 建立以「 」開始的歷程 **[!UICONTROL 讀取]** 活動。 [了解更多信息](journey-gs.md)。
1. 新增 **[!UICONTROL 電子郵件]** 歷程的動作活動。 [了解更多信息](journeys-message.md)。
1. 在 **[!UICONTROL 電子郵件引數]** 部分 **[!UICONTROL 電子郵件]** 活動設定，取代預設電子郵件地址(`PersonalEmail.adress`)，並加上訂閱者的電子郵件地址：

   1. 按一下 **[!UICONTROL 啟用引數覆寫]** 圖示右側 **[!UICONTROL 地址]** 欄位，然後按一下 **[!UICONTROL 編輯]** 圖示。

      ![](assets/message-to-subscribers-uc-1.png)

   1. 在運算式編輯器中，輸入運算式以擷取訂閱者的電子郵件地址。 [了解更多信息](expression/expressionadvanced.md)。

      此範例顯示包含對應欄位參照的運算式：

      ```json
      #{ExperiencePlatform.Subscriptions.profile.consents.marketing.email.subscriptions.entry('daily-email').subscribers.firstEntryKey()}
      ```

      在此範例中，會使用下列函式：

      | 函数 | 描述 | 示例 |
      | --- | --- | --- |
      | `entry` | 根據選取的名稱空間參考對應元素 | 請參閱特定訂閱清單 |
      | `firstEntryKey` | 擷取對應的第一個專案索引鍵 | 擷取訂閱者的第一個電子郵件地址 |

      在此範例中，訂閱清單名為 `daily-email`. 電子郵件地址在中定義為金鑰 `subscribers` 對應，此對應會連結至訂閱清單對應。

      深入瞭解 [欄位參考](expression/field-references.md) 在運算式中。

      ![](assets/message-to-subscribers-uc-2.png)

   1. 在 **[!UICONTROL 新增運算式]** 對話方塊中，按一下 **[!UICONTROL 確定]**.

>[!CAUTION]
>
>仅应针对特定用例使用电子邮件地址覆盖。大多数情况下，无需更改电子邮件地址，应使用&#x200B;**[!UICONTROL 执行字段]**&#x200B;中定义为主地址的值。[了解详情](../configuration/primary-email-addresses.md)
