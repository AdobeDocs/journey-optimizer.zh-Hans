---
solution: Journey Optimizer
product: journey optimizer
title: 可投放性入门
description: 瞭解傳遞能力准則
feature: Deliverability
topic: Content Management
role: User
level: Intermediate
exl-id: 8f33dda7-9bd5-4293-8d0d-222205cbc7d5
source-git-commit: 020c4fb18cbd0c10a6eb92865f7f0457e5db8bc0
workflow-type: tm+mt
source-wordcount: '693'
ht-degree: 2%

---

# 可投放性入门 {#manage-deliverability}

傳遞能力是衡量傳遞成功送達收件者收件匣的指標。

>[!NOTE]
>
>對於授權Healthcare Shield的客戶，Adobe會使用傳輸層安全性(TLS) 1.2來保護使用者的系統（收件者）和Journey Optimizer（傳送者）之間的資料交換。 如果接收郵件伺服器不支援TLS 1.2，客戶將會遇到傳遞能力問題，包括電子郵件退回給原始寄件者。

**電子郵件傳遞能力** 指一組特性，可決定訊息在短時間內透過個人電子郵件地址達到其目的地的能力，且內容和格式符合預期品質。 這些特性分為四大類：資料品質、訊息和內容、傳送基礎結構和信譽。 這些共同點為成功的電子郵件傳遞計畫奠定了基礎。

此 **傳遞率** 相較於已傳遞的訊息數，點選收件者收件匣的訊息數。 這取決於許多因素，特別是：

* 垃圾郵件投訴數量有限
* 低硬跳出率
* 目標地址的品質
* 訊息內容
* 寄件者信譽

最佳化您的 [!DNL Journey Optimizer] 體驗，我們建議您使用本節所列的最佳實務。 傳遞能力問題通常與網際網路服務提供者(ISP)和郵件伺服器管理員實施的垃圾郵件防護相關聯。

如需深入瞭解什麼是傳遞能力，並深入瞭解傳遞能力的重要術語、概念和方法，請參閱 [Adobe傳遞性最佳實務指南](https://experienceleague.adobe.com/docs/deliverability-learn/deliverability-best-practice-guide/introduction.html?lang=zh-Hans){target="_blank"}.

## 降低投訴率 {#reduce-complaint-rate}

ISP通常具有將收到的訊息報告為垃圾訊息的顯著方法。 這樣就可以識別不可靠的來源。 透過快速接受選擇退出請求並顯示您是可靠的寄件者，您可以降低投訴率。 [進一步瞭解選擇退出管理](../privacy/opt-out.md#opt-out-management).

一般而言，請勿透過要求收件者填寫電子郵件地址或名稱等欄位，來妨礙想要選擇退出的收件者。 取消訂閱登入頁面應該只有一個驗證按鈕。

請求其他確認時請格外小心：使用者可能有兩個電子郵件地址會重新導向至相同的方塊(例如：firstname.lastname@club.com和firstname.lastname@internet-club.com)。 如果設定檔只能記住第一個地址，並希望透過傳送給另一個的訊息取消訂閱，則表單將拒絕此操作，因為加密的識別碼和輸入的電子郵件地址不匹配。

## 利用隱藏清單 {#suppression-lists}

[!DNL Journey Optimizer] 管理隱藏清單，收集持續發生的垃圾郵件投訴、硬跳出和軟跳出。

為了保護您的傳遞能力，根據預設，地址在隱藏清單中的收件者將從所有未來的傳遞中排除，因為傳送給這些聯絡人可能會損害您的傳送信譽。

[進一步瞭解隱藏清單](suppression-list.md).

## 使用監控工具 {#monitoring-tools}

使用所提供的功能 [!DNL Journey Optimizer] 以監控您的傳遞能力。

此 **[!UICONTROL 執行]** 訊息清單的索引標籤可讓您透過一組即時指標檢查傳送的執行方式。 除其他外，此標籤會顯示：
* 成功執行、傳送及傳遞的訊息數。
* 已開啟的訊息數以及已點按的訊息/連結數。

## 調整訊息內容 {#adapt-message-content}

在較小程度上，某些訊息的內容可能會被偵測為垃圾訊息。

若要提高傳遞率並確保電子郵件可送達收件者，請在設計訊息內容時遵循下列原則：

* **寄件者名稱和地址**：地址必須明確識別寄件者。 網域必須由寄件者擁有並註冊。 網域登入不得為私用。

* **取消訂閱連結和登陸頁面**：取消訂閱連結至關重要。 它必須是可見且有效的，而且表單必須是功能性的。

[進一步瞭解設計電子郵件內容](../email/get-started-email-design.md).

## 建立您作為寄件者的信譽

如果您最近移至其他電子郵件服務提供者、IP位址或電子郵件網域或子網域，您必須建立您作為寄件者的信譽。 否則，您的傳遞可能會被封鎖或移至收件者信箱的垃圾郵件資料夾。

若要讓IP暖和，您可以逐步增加傳送數量。 檢視此 [使用案例](../building-journeys/ramp-up-deliveries-uc.md).
