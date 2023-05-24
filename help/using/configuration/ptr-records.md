---
solution: Journey Optimizer
product: journey optimizer
title: PTR記錄
description: 瞭解如何管理PTR記錄
feature: Application Settings
topic: Administration
role: Admin
level: Intermediate
keywords: 子網域， PTR，記錄， DNS，網域，郵件
exl-id: 4c930792-0677-4ad5-a46c-8d40fc3c4d3a
source-git-commit: b8065a68ed73102cb2c9da2c2d2675ce8e5fbaad
workflow-type: tm+mt
source-wordcount: '785'
ht-degree: 9%

---

# PTR記錄 {#ptr-records}

>[!CONTEXTUALHELP]
>id="ajo_admin_ptr_record"
>title="子域的 PTR 记录"
>abstract="指针记录 (PTR) 是一种 DNS 记录，它提供链接到 IP 地址的域名，帮助接收邮件服务器验证发件人的 IP 地址。您只有在与送达率专家进行讨论并充分考虑后，才能编辑 PTR 记录。"

>[!CONTEXTUALHELP]
>id="ajo_admin_ptr_record_header"
>title="子域的 PTR 记录"
>abstract="在 Journey Optimizer 中将子域委派给 Adobe 后，将自动创建 PTR 记录并将其与此子域相关联。"

## 關於PTR記錄 {#about-ptr-records}

指標籤錄(PTR)是一種網域名稱系統(DNS)記錄，提供連結至IP位址的網域名稱。

透過PTR記錄，接收郵件伺服器可透過識別其IP位址是否對應到伺服器連線的名稱，來檢查傳送郵件伺服器的真實性。

## 存取子網域的PTR記錄 {#access-ptr-records}

一次 [子網域已委派](delegate-subdomain.md) 在Adobe Journey Optimizer中，會自動建立PTR記錄並與此子網域相關聯。 您可以從 **[!UICONTROL 管理]** > **[!UICONTROL 頻道]** > **[!UICONTROL 電子郵件設定]** > **[!UICONTROL PTR記錄]** 功能表。

![](assets/ptr-records.png)

清單會使用下列語法，顯示為每個委派子網域產生的PTR記錄：

* 「r」代表記錄，
* 「xx」代表IP位址的最後兩個數字，
* 子網域名稱。

您可以從清單中開啟PTR記錄，以顯示相關聯的子網域名稱和IP位址。

## 編輯PTR記錄 {#edit-ptr-record}

您可以修改PTR記錄，以編輯與IP位址相關聯的子網域。

>[!CAUTION]
>
>PTR記錄在所有環境中都是通用的。 因此，對PTR記錄的任何修改也會影響生產沙箱。
>
>編輯PTR記錄時請格外小心。 如有疑問，請聯絡傳遞能力專家。

### 完全委派的子網域 {#fully-delegated-subdomains}

若要編輯具有下列子網域的PTR記錄： [已完全委派](delegate-subdomain.md#full-subdomain-delegation) 若要Adobe，請遵循下列步驟。

1. 從清單中，按一下PTR記錄名稱以開啟。

   ![](assets/ptr-record-select.png)

1. 選取子網域 [已完全委派](delegate-subdomain.md#full-subdomain-delegation) 以從清單中Adobe。

   ![](assets/ptr-record-subdomain.png)

1. 按一下 **[!UICONTROL 儲存]** 以確認您的變更。

>[!NOTE]
>
>您無法修改 **[!UICONTROL IP]** 和 **[!UICONTROL PTR記錄]** 欄位。

### 使用CNAME方法委派的子網域 {#edit-ptr-subdomains-cname}

若要編輯子網域委派給Adobe的PTR記錄，請使用 [CNAME方法](delegate-subdomain.md#cname-subdomain-delegation)，請遵循下列步驟。

1. 從清單中，按一下PTR記錄名稱以開啟。

   ![](assets/ptr-record-select-cname.png)

1. 選擇委派給Adobe的子網域，使用 [CNAME方法](delegate-subdomain.md#cname-subdomain-delegation) 從清單中。

   ![](assets/ptr-record-subdomain-cname.png)

1. 您需要在您的代管平台上建立新的轉送DNS記錄。 若要這麼做，請複製Adobe產生的記錄。 完成後，核取「我確認……」方塊。

   ![](assets/ptr-record-subdomain-confirm.png)

   >[!NOTE]
   >
   >如果您收到此訊息：「請先建立轉送DNS，然後再試一次」，請遵循下列步驟：
   >   * 如果成功建立轉送DNS記錄，請檢查DNS提供者。
   >   * DNS上的記錄可能不會立即同步。 請等候幾分鐘，然後再試一次。


1. 按一下 **[!UICONTROL 儲存]** 以確認您的變更。

>[!NOTE]
>
>您無法修改 **[!UICONTROL IP]** 和 **[!UICONTROL PTR記錄]** 欄位。

## 檢查PTR記錄更新詳細資料 {#check-ptr-record-update}

確認PTR記錄編輯後， **[!UICONTROL 處理中]** 圖示會顯示在清單中PTR記錄的名稱旁。

![](assets/ptr-record-updating.png)

>[!NOTE]
>
>此 [更新處理](#processing) 最多可能需要3小時。

若要檢查PTR記錄更新詳細資訊，請按一下其旁的圖示。 進一步瞭解中與不同圖示相關聯的狀態 [本節](#ptr-record-update-statuses).

![](assets/ptr-record-recent-update.png)

您可以檢視更新狀態和請求的變更等資訊。

![](assets/ptr-record-updates.png)

## PTR記錄更新狀態 {#ptr-record-update-statuses}

PTR記錄更新可以有下列狀態：

* ![](assets/do-not-localize/ptr-record-processing.png) **[!UICONTROL 處理中]**：PTR記錄更新已提交，並正在執行驗證程式。
* ![](assets/do-not-localize/ptr-record-success.png) **[!UICONTROL 成功]**：更新的PTR記錄已經過驗證，新的子網域現在與IP位址相關聯。
* ![](assets/do-not-localize/ptr-record-failed.png) **[!UICONTROL 已失敗]**：在PTR記錄更新驗證期間，一個或多個檢查失敗。

### 处理时间 {#processing}

將會執行數個傳遞能力檢查，以確認要與IP位址關聯的新子網域是否有效。 這最多可能需要3小時的時間。

>[!NOTE]
>
>進行更新時，您無法修改PTR記錄。 您仍然可以按一下其名稱，但是 **[!UICONTROL 子網域]** 欄位會變成灰色。 更新成功後才會反映變更。

在驗證程式期間，舊的子網域仍與IP位址相關聯。

### 成功 {#success}

一旦驗證程式成功，新的子網域就會自動與IP位址相關聯。

### 失败 {#failes}

如果驗證程式失敗，則會顯示較舊的PTR記錄。 先前與IP位址關聯的有效子網域維持不變。

可能的更新錯誤型別如下：
* 無法為PTR記錄建立新的轉送DNS
* 無法更新記錄
* 無法重新加入相關性

更新失敗時，PTR記錄會再次變為可編輯。 您可以按一下其名稱，然後再次更新子網域。
