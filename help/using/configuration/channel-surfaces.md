---
solution: Journey Optimizer
product: journey optimizer
title: 设置渠道平面
description: 瞭解如何設定和監控管道表面
feature: Application Settings, Surface
topic: Administration
role: Admin
level: Intermediate
keywords: 管道，表面，技術，引數，最佳化工具
exl-id: 9038528f-3da0-4e0e-9b82-b72c67b42391
source-git-commit: 9555c37f8bac295a668f64990e229c6e0e5ceb8d
workflow-type: tm+mt
source-wordcount: '1607'
ht-degree: 8%

---

# 设置渠道平面 {#set-up-channel-surfaces}

>[!CONTEXTUALHELP]
>id="ajo_admin_channel_surfaces"
>title="表面"
>abstract="平面是由系统管理员定义的配置。它包含用于发送消息的所有技术参数，如标头参数、子域、移动应用程序等。"

替換為 [!DNL Journey Optimizer]，您可以設定頻道介面（即訊息預設集），定義訊息所需的所有技術引數：電子郵件型別、寄件者電子郵件和名稱、行動應用程式、簡訊設定等。

>[!CAUTION]
>
> * 若要建立、編輯和刪除管道曲面，您必須擁有 [管理管道表面](../administration/high-low-permissions.md#manage-channel-surface) 許可權。
>
> * 您必須執行 [電子郵件設定](../email/get-started-email-config.md)， [推送設定](../push/push-configuration.md) 和 [簡訊設定](../sms/sms-configuration.md) 建立管道曲面之前的步驟。


設定頻道介面後，您就可以在從歷程或行銷活動建立訊息時選取它們。

<!--
➡️ [Learn how to create and use email surfaces in this video](#video-presets)
-->

## 建立管道表面 {#create-channel-surface}

>[!CONTEXTUALHELP]
>id="ajo_admin_message_presets_header"
>title="渠道表面设置"
>abstract="设置渠道表面时，选择它适用的渠道，并定义在您发送电子邮件时需要的所有技术参数，例如电子邮件类型、发件人姓名、移动应用程序、短信配置等。"

>[!CONTEXTUALHELP]
>id="ajo_admin_message_presets"
>title="渠道表面设置"
>abstract="为了能够从历程或营销活动创建诸如发送电子邮件等操作，您必须首先创建一个渠道表面，用于定义消息所需的全部技术设置。您必须具有管理渠道表面权限才能创建、编辑和删除渠道表面。"

若要建立管道曲面，請遵循下列步驟：

1. 存取 **[!UICONTROL 頻道]** > **[!UICONTROL 品牌化]** > **[!UICONTROL 管道表面]** 功能表，然後按一下 **[!UICONTROL 建立管道表面]**.

   ![](assets/preset-create.png)

1. 輸入表面的名稱和說明（選擇性），然後選取要設定的管道。

   ![](assets/preset-general.png)

   >[!NOTE]
   >
   > 名稱必須以字母(A-Z)開頭。 它只能包含英數字元。 您也可以使用底線 `_`，點`.` 和連字型大小 `-` 個字元。

1. 如果您已選取 **[!UICONTROL 電子郵件]** 頻道，請依照中的說明進行設定 [本節](../email/email-settings.md).

   ![](assets/preset-email.png)

1. 對於 **[!UICONTROL 推播通知]** 頻道，請至少選取一個平台 —   **iOS** 和/或 **Android**  — 以及每個平台要使用的行動應用程式。

   ![](assets/preset-push.png)

   >[!NOTE]
   >
   >有關如何設定環境以傳送推播通知的詳細資訊，請參閱 [本節](../push/push-gs.md).

1. 對於 **[!UICONTROL 簡訊]** 管道，定義您的設定，如所述 [本節](../sms/sms-configuration.md#message-preset-sms).

   ![](assets/preset-sms.png)

   >[!NOTE]
   >
   >有關如何設定環境以傳送SMS訊息的詳細資訊，請參閱 [本節](../sms/sms-configuration.md).

1. 設定好所有引數後，按一下 **[!UICONTROL 提交]** 以確認。 您也可以將管路曲面儲存為拔模，並在稍後恢復其組態。

   ![](assets/preset-submit.png)

   >[!NOTE]
   >
   >當選取的IP集區位於下方時，您無法繼續建立表面 [版本](ip-pools.md#edit-ip-pool) (**[!UICONTROL 處理中]** 狀態)，且從未與所選子網域建立關聯。 [了解详情](#subdomains-and-ip-pools)
   >
   >將表面儲存為草稿，並等待IP集區具有 **[!UICONTROL 成功]** 繼續建立曲面的狀態。

1. 建立管道曲面後，它會顯示於清單中，並具有 **[!UICONTROL 處理中]** 狀態。

   在此步驟中，將會執行數個檢查以確認其已正確設定。 <!--The processing time is around **48h-72h**, and can take up to **7-10 business days**.-->

   >[!NOTE]
   >為指定子網域建立第一個電子郵件介面時，可能需要處理時間 **10分鐘到10天**. 如果選取的子網域已用於其他電子郵件介面，則最多只需3小時。

   這些檢查包括Adobe團隊執行的設定和技術測試：

   * SPF驗證
   * DKIM驗證
   * MX記錄驗證
   * 檢查IP封鎖清單
   * Helo主機檢查
   * IP集區驗證
   * A/PTR記錄，t/m/res子網域驗證
   * FBL註冊（此檢查只會在第一次為指定子網域建立電子郵件曲面時執行）

   >[!NOTE]
   >
   >如果檢查未成功，請在中進一步瞭解可能的失敗原因 [本節](#monitor-channel-surfaces).

1. 檢查成功後，管道表面會取得 **[!UICONTROL 作用中]** 狀態。 已準備好用於傳遞訊息。

   ![](assets/preset-active.png)

## 監視頻道介面 {#monitor-channel-surfaces}

您的所有管道表面都會顯示在 **[!UICONTROL 頻道]** > **[!UICONTROL 管道表面]** 功能表。 篩選器可協助您瀏覽清單（頻道、使用者、狀態）。

![](assets/preset-filters.png)

建立之後，管道表面可以有下列狀態：

* **[!UICONTROL 草稿]**：管道表面已儲存為草稿，但尚未提交。 開啟以繼續設定。
* **[!UICONTROL 處理中]**：管道表面已提交，且正在執行數個驗證步驟。
* **[!UICONTROL 作用中]**：管道表面已經過驗證，可以選取它來建立訊息。
* **[!UICONTROL 已失敗]**：在管道表面驗證期間，一項或多項檢查失敗。
* **[!UICONTROL 已停用]**：管道表面已停用。 無法用來建立新訊息。

如果管道曲面建立失敗，下文將說明每個可能失敗原因的詳細資訊。

如果發生這些錯誤之一，請連絡 [Adobe客戶服務](https://helpx.adobe.com/enterprise/admin-guide.html/enterprise/using/support-for-experience-cloud.ug.html){target="_blank"} 以取得協助。

* **SPF驗證失敗**： SPF (Sender Policy Framework)是電子郵件驗證通訊協定，允許指定可從指定子網域傳送電子郵件的授權IP。 SPF驗證失敗表示SPF記錄中的IP位址不符合用來傳送電子郵件給信箱提供者的IP位址。

* **DKIM驗證失敗**： DKIM (DomainKeys Identified Mail)可讓收件者伺服器驗證所收到的郵件是由相關網域的真正寄件者傳送，且原始郵件的內容並未在傳送途中變更。 DKIM驗證失敗表示接收郵件伺服器無法驗證郵件內容的真實性及其與傳送網域的關聯：

* **MX記錄驗證失敗**： MX (Mail eXchange)記錄驗證失敗表示負責代表指定子網域接受傳入電子郵件的郵件伺服器未正確設定。

* **傳遞能力設定失敗**：傳遞能力設定失敗的可能原因如下：
   * 已配置IP的封鎖清單
   * 無效 `helo` 名稱
   * 從對應介面的IP集區中指定之IP以外的IP傳送電子郵件
   * 無法將電子郵件傳遞至主要ISP的收件匣

## 編輯管道表面 {#edit-channel-surface}

若要編輯管道曲面，請遵循下列步驟。

>[!NOTE]
>
>您無法編輯 **[!UICONTROL 推播通知設定]**. 如果管道表面僅設定為推播通知管道，則無法編輯。

1. 從清單中，按一下管道曲面名稱以開啟。

   ![](assets/preset-name.png)

1. 視需要編輯其屬性。

   >[!NOTE]
   >
   >如果管道表面具有 **[!UICONTROL 作用中]** 狀態， **[!UICONTROL 名稱]**， **[!UICONTROL 選取頻道]** 和 **[!UICONTROL 子網域]** 欄位會變灰且無法編輯。

1. 按一下 **[!UICONTROL 提交]** 以確認您的變更。

   >[!NOTE]
   >
   >您也可以將管路曲面儲存為拔模，並在稍後繼續更新。

提交變更後，管道表面將經歷一個驗證週期，類似於以下情形下的驗證週期： [建立管道表面](#create-channel-surface). 版本處理時間最多可能需要 **3小時**.

>[!NOTE]
>
>如果您只編輯 **[!UICONTROL 說明]**， **[!UICONTROL 電子郵件型別]** 和/或 **[!UICONTROL 電子郵件重試引數]** 欄位，更新即時。

### 更新詳細資料 {#update-details}

對於具有下列專案的管道表面： **[!UICONTROL 作用中]** 狀態，您可以檢查更新的詳細資訊。 为实现此操作，请执行以下步骤：

按一下 **[!UICONTROL 最近更新]** 顯示在活動曲面名稱旁的圖示。

![](assets/preset-recent-update-icon.png)

<!--You can also access the update details from an active channel surface while update is in progress.-->

於 **[!UICONTROL 最近更新]** 熒幕中，您可以看到更新狀態和請求變更清單等資訊。

<!--![](assets/preset-recent-update-screen.png)-->

### 更新狀態 {#update-statuses}

管道表面更新可以具有以下狀態：

* **[!UICONTROL 處理中]**：管道表面更新已提交，並正在執行數個驗證步驟。
* **[!UICONTROL 成功]**：已驗證更新的管道表面，並可選取它來建立訊息。
* **[!UICONTROL 已失敗]**：在管道表面更新驗證期間，一項或多項檢查失敗。

每個狀態都詳列於下方。

#### 处理时间 {#surface-processing}

將會執行數個傳遞能力檢查，以確認曲面已正確更新。

>[!NOTE]
>
>如果您只編輯 **[!UICONTROL 說明]**， **[!UICONTROL 電子郵件型別]** 和/或 **[!UICONTROL 電子郵件重試引數]** 欄位，更新即時。

處理時間最多可能需要 **3小時**. 瞭解更多有關驗證週期期間執行的檢查，請參閱 [本節](#create-channel-surface).

如果您編輯已啟動的曲面：

* 其狀態維持不變 **[!UICONTROL 作用中]** 驗證程式進行時。

* 此 **[!UICONTROL 最近更新]** 圖示會顯示在「管道曲面」清單中的曲面名稱旁。

* 在驗證程式期間，使用此介面設定的訊息仍使用舊版介面。

>[!NOTE]
>
>更新進行中時，您無法修改管道表面。 您仍然可以按一下其名稱，但所有欄位都顯示為灰色。 更新成功後才會反映變更。

#### 成功 {#success}

一旦驗證程式成功，使用此表面的所有訊息都會自動使用表面的新版本。 不過，您可能必須等待：
* 幾分鐘後，單一訊息便會使用，
* 直到下一個批次，讓曲面在批次訊息中生效。

#### 失败 {#failed}

如果驗證程式失敗，仍會使用舊版曲面。

進一步瞭解中可能出現的失敗原因 [本節](#monitor-channel-surfaces).

更新失敗時，表面將再次變為可編輯。 您可以按一下其名稱並更新需要修正的設定。

## 停用管道表面 {#deactivate-a-surface}

若要建立 **[!UICONTROL 作用中]** 頻道介面無法用來建立新訊息，您可以將其停用。 但是，目前使用此表面的歷程訊息將不會受到影響，並將繼續運作。

>[!NOTE]
>
>處理更新時，您無法停用管道表面。 您必須等候更新成功或失敗。 進一步瞭解 [編輯頻道介面](#edit-channel-surface) 並在 [更新狀態](#update-statuses).

1. 存取管道表面清單。

1. 對於您選擇的活動曲面，按一下 **[!UICONTROL 更多動作]** 按鈕。

1. 選取 **[!UICONTROL 停用]**.

   ![](assets/preset-deactivate.png)

>[!NOTE]
>
>無法刪除已停用的管道表面，以避免使用這些表面傳送訊息的歷程中出現任何問題。

您無法直接編輯已停用的管道表面。 但是，您可以複製它並編輯副本，以建立用於建立新訊息的新版本。 您也可以再次啟動它，然後等到更新成功後再進行編輯。

![](assets/preset-activate.png)

<!--
## How-to video{#video-presets}

Learn how to create channel surfaces, how to use them and how to delegate a subdomain and create an IP pool.

>[!VIDEO](https://video.tv.adobe.com/v/334343?quality=12)
-->
