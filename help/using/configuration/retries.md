---
solution: Journey Optimizer
product: journey optimizer
title: 重试
description: 瞭解在將地址傳送到隱藏清單之前如何執行重試
feature: Application Settings
topic: Administration
role: Admin
level: Intermediate
keywords: 重試，退回，軟化，最佳化程式，錯誤
exl-id: 05564a99-da50-4837-8dfb-bb1d3e0f1097
source-git-commit: 9657862f1c6bdb2399fcf3e6384bb9dec5b8f32b
workflow-type: tm+mt
source-wordcount: '459'
ht-degree: 13%

---

# 重试 {#retries}

當電子郵件訊息因暫時性而失敗時 **軟退信** 錯誤，會執行多次重試。 每個錯誤都會遞增錯誤計數器。 當此計數器達到限制臨界值時，會將地址新增到隱藏清單中。

>[!NOTE]
>
>深入瞭解中的錯誤型別 [傳遞失敗型別](../reports/suppression-list.md#delivery-failures) 區段。

在預設設定中，臨界值設定為5個錯誤。

* 對於相同傳遞，在第五個遇到內錯誤 [重試時段](#retry-duration)，則會隱藏位址。

* 如果有不同的傳送，且至少相隔24小時發生兩個錯誤，則每個錯誤都會增加錯誤計數器，並且在第五次嘗試時也會隱藏地址。

如果重試後傳遞成功，則會重新初始化位址的錯誤計數器。

## 重試臨界值版本 {#edit-retry-threshold}

>[!CONTEXTUALHELP]
>id="ajo_admin_suppression_list_bounces"
>title="更新重试阈值"
>abstract="如果默认值不适合需求，您可以修改允许的连续软退回次数。对于特定电子邮件地址，当重试计数器达到错误阈值时，此地址将添加到禁止列表中。"
>additional-url="https://experienceleague.adobe.com/docs/journey-optimizer/using/reporting/deliverability/suppression-list.html" text="了解禁止列表"

如果預設值5不符合您的需求，您可以按照以下步驟修改錯誤臨界值。

1. 前往 **[!UICONTROL 頻道]** > **[!UICONTROL 電子郵件設定]** > **[!UICONTROL 隱藏清單]**.

1. 選取 **[!UICONTROL 編輯隱藏規則]** 按鈕。

   ![](assets/suppression-list-edit-retries.png)

1. 根據您的需求，編輯允許的連續軟跳出次數。

   ![](assets/suppression-list-edit-soft-bounces.png)

   您必須輸入介於1到20之間的整數值，表示最小重試次數為1，最大重試次數為20。

   >[!CAUTION]
   >
   >大於10的任何值都可能會導致傳遞能力聲譽問題，並遭到ISP施加IP節流或加入封鎖清單。 [進一步瞭解傳遞能力](../reports/deliverability.md)

## 重试时段 {#retry-duration}

此 **重試時段** 是任何遇到暫時錯誤或軟退信之傳遞電子郵件訊息將重試傳遞的時間範圍。

依預設，將執行重試 **3.5天** (或 **84小時**)時，系統就會將訊息新增至電子郵件佇列。

不過，為了確保當不再需要重試時不再執行，您可以在建立或編輯時根據您的需求變更此設定 [管道表面](channel-surfaces.md) （即訊息預設集）套用至電子郵件頻道。

例如，對於與密碼重設相關的交易式電子郵件，您可以將重試期間設為24小時，其中包含僅一天有效的連結。 同樣地，對於午夜優惠，您可能想要定義6小時的重試期間。

>[!NOTE]
>
>重試期間不能超過84小時。 行銷電子郵件的最小重試期間為6小時，交易電子郵件的最小重試期間為10分鐘。

瞭解在中建立管道表面時，如何調整電子郵件重試引數 [本節](../email/email-settings.md#email-retry).

