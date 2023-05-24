---
solution: Journey Optimizer
product: journey optimizer
title: 创建订阅列表
description: 瞭解如何在Journey Optimizer中設定訂閱清單
feature: Landing Pages
topic: Content Management
role: User
level: Beginner
keywords: 登陸，登陸頁面，清單，訂閱，服務
exl-id: 5e5419a0-5121-4aa7-a975-b1f08e2918c9
source-git-commit: c0afa3e2bc6dbcb0f2f2357eebc04285de8c5773
workflow-type: tm+mt
source-wordcount: '426'
ht-degree: 12%

---

# 订阅列表 {#create-subscription-list}

## 什麼是訂閱清單？ {#subscription-list-definition}

>[!CONTEXTUALHELP]
>id="ajo_subscription_list"
>title="设置订阅列表"
>abstract="创建订阅列表，用于收集已选择接收特定主题或事件通信的配置文件。 "
>additional-url="https://experienceleague.adobe.com/docs/journey-optimizer/using/landing-pages/subscription-list.html#define-subscription-list" text="创建订阅列表"

訂閱服務是指為已選擇接收特定主題/事件/興趣/等通訊的客戶提供的行銷商品和服務。 持續進行。 在 [!DNL Journey Optimizer]，這些選擇加入的客戶會收集到訂閱清單中。

訂閱服務可以是：

* 電子報，例如：「執行系列」
* 事件，例如：「Summit 2021」
* 網路研討會，例如：「進一步瞭解crypto」
* 對特定產品/運動/服務/等的興趣，例如：「有興趣在未來12個月內買房」
* 關於如何收到通知的偏好設定，例如：「通過電子郵件接收新歌曲通知」

設定檔可透過新增至訂閱清單 [登陸頁面](create-lp.md). 範例顯示於 [本節](lp-use-cases.md#subscription-to-a-service).

## 创建订阅列表 {#define-subscription-list}

若要建立訂閱清單，請遵循下列步驟。

1. 若要存取訂閱清單，請選取 **[!UICONTROL 客戶]** > **[!UICONTROL 訂閱清單]**.

   ![](assets/lp_subscription-lists.png)

1. 選取 **[!UICONTROL 建立訂閱清單]** 按鈕。

   ![](assets/lp_create-subscription-list.png)

1. 新增標題和說明。 這些欄位為必填欄位。

   ![](assets/lp_subscription-list-name.png)

   >[!CAUTION]
   >
   >目前您無法使用間距，或輸入中其他訂閱清單已經存在的名稱。 **[!UICONTROL 標題]** 欄位。

1. 您可以定義開始日期和結束日期。

   ![](assets/lp_subscription-list-dates.png)

1. 单击&#x200B;**[!UICONTROL 保存]**。

清單會顯示所有已建立的訂閱清單。 您可以根據建立日期或修改日期及其狀態來篩選它們。

![](assets/lp_subscription-filters.png)

可能的狀態如下：

* **[!UICONTROL 尚未開始]**：您定義的開始日期晚於當天。 訂閱的設定檔將不會收到與此訂閱清單相關的通訊。
* **[!UICONTROL 即時]**：當天的組成介於訂閱清單開始日期和結束日期之間，或者您未定義結束/開始日期，這表示訂閱清單永遠是即時的。
* **[!UICONTROL 已過期]**：結束日期已過，因此訂閱清單不再有效。 任何訂閱的設定檔都不會再收到與此訂閱清單相關的通訊。

建立訂閱清單後，您即可在登入頁面中加以使用。 選擇通過登入頁面表單的設定檔將新增至清單。 [了解详情](design-lp.md)

在以下情況下，您也可以使用訂閱清單作為區段： [建立歷程](../building-journeys/journey-gs.md#jo-build) 以及新增個人化。

>[!NOTE]
>
>您可以透過特定報告監控您的訂閱清單影響。 [了解详情](../reports/subscription-report-live.md)
