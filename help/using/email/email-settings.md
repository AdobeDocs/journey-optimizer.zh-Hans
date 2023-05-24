---
solution: Journey Optimizer
product: journey optimizer
title: 配置电子邮件设置
description: 瞭解如何在頻道介面層級設定電子郵件設定
feature: Surface
topic: Administration
role: Admin
level: Intermediate
keywords: 設定，電子郵件，設定
exl-id: 13536962-7541-4eb6-9ccb-4f97e167734a
source-git-commit: 4ce00b4a709c23284148dfffb0187767fcecbe8a
workflow-type: tm+mt
source-wordcount: '1779'
ht-degree: 8%

---

# 配置电子邮件设置 {#email-settings}

若要開始建立電子郵件，您必須設定電子郵件通道介面，以定義訊息所需的所有技術引數。 [瞭解如何建立表面](../configuration/channel-surfaces.md)

在管道表面設定的專用區段中定義電子郵件設定。

![](assets/preset-email-settings.png)

系統會擷取電子郵件表面設定，以便依照下列邏輯傳送通訊：

* 對於批次和成組分解歷程，這不適用於在建立電子郵件表面設定之前已啟動的批次或成組分解執行。 變更將在下次循環或新執行時擷取。

* 對於交易式訊息，變更會被立即擷取以供下次通訊使用（最多延遲5分鐘）。

>[!NOTE]
>
>更新的電子郵件表面設定將在使用表面的歷程或行銷活動中自動擷取。

## 電子郵件型別 {#email-type}

>[!CONTEXTUALHELP]
>id="ajo_admin_presets_emailtype"
>title="定义电子邮件类别"
>abstract="选择使用此表面时将发送的电子邮件类型：营销性的促销电子邮件，此时需要用户同意；或者事务性的非商业电子邮件，此时在特定上下文中，也可以发送到未订阅的配置文件。"

在 **電子郵件型別** 區段，選取將與介面一起傳送的訊息型別： **行銷** 或 **異動**.

* 選擇 **行銷** 促銷電子郵件：這些訊息需要使用者同意。

* 選擇 **異動** 非商業電子郵件，例如訂單確認、密碼重設通知或傳遞資訊。

>[!CAUTION]
>
>**異動** 電子郵件可以傳送給從行銷通訊取消訂閱的設定檔。 這些訊息只能在特定內容中傳送。

建立訊息時，您必須選擇符合您為電子郵件選取之類別的有效管道表面。

## 子網域和IP集區 {#subdomains-and-ip-pools}

在 **子網域和IP集區** 區段，您必須：

1. 選取要用來傳送電子郵件的子網域。 [了解详情](../configuration/about-subdomain-delegation.md)

1. 選取要與表面關聯的IP集區。 [了解详情](../configuration/ip-pools.md)

![](assets/preset-subdomain-ip-pool.png)

當選取的IP集區位於下方時，您無法繼續建立表面 [版本](../configuration/ip-pools.md#edit-ip-pool) (**[!UICONTROL 處理中]** 狀態)，且從未與選取的子網域建立關聯。 否則，仍會使用最舊版本的IP集區/子網域關聯。 如果是這種情況，請將表面另存為草稿，並在IP池具有 **[!UICONTROL 成功]** 狀態。

>[!NOTE]
>
>對於非生產環境，Adobe不會建立立即可用的測試子網域，也不會授與共用傳送IP集區的存取權。 您需要 [委派您自己的子網域](../configuration/delegate-subdomain.md) 並使用指派給貴組織的集區中的IP。

選取IP集區後，當游標停留在IP集區下拉式清單下方顯示的IP位址上時，會顯示PTR資訊。 [深入瞭解PTR記錄](../configuration/ptr-records.md)

![](assets/email-surface-ptr-record.png)

>[!NOTE]
>
>如果未設定PTR記錄，請聯絡您的Adobe代表。

## 清單 — 取消訂閱 {#list-unsubscribe}

於 [選取子網域](#subdomains-and-ip-pools) 從清單中， **[!UICONTROL 啟用清單取消訂閱]** 選項隨即顯示。

![](assets/preset-list-unsubscribe.png)

默认启用选项。

如果您將其保留為啟用，則取消訂閱連結會自動包含在電子郵件標題中，例如：

![](assets/preset-list-unsubscribe-header.png)

如果停用此選項，電子郵件標頭中不會顯示取消訂閱連結。

取消訂閱連結包含兩個元素：

* 一個 **取消訂閱電子郵件地址**，所有取消訂閱的請求都會傳送至。

   在 [!DNL Journey Optimizer]，預設為取消訂閱電子郵件地址 **[!UICONTROL Mailto （取消訂閱）]** 頻道介面中顯示的地址，根據 [選取的子網域](#subdomains-and-ip-pools).

   ![](assets/preset-list-unsubscribe-mailto.png)

* 此 **取消訂閱URL**，這是登陸頁面的URL，取消訂閱後，會將使用者重新導向。

   如果您新增 [一鍵選擇退出連結](../privacy/opt-out.md#one-click-opt-out) 對於使用此介面建立的訊息，取消訂閱URL將為一鍵選擇退出連結定義的URL。

   ![](assets/preset-list-unsubscribe-opt-out-url.png)

   >[!NOTE]
   >
   >如果您未在訊息內容中新增一鍵退出連結，則不會向使用者顯示登陸頁面。

進一步瞭解在中新增訊息的標頭取消訂閱連結 [本節](../privacy/opt-out.md#unsubscribe-header).

<!--Select the **[!UICONTROL Custom List-Unsubscribe]** option to enter your own Unsubscribe URL and/or your own Unsubscribe email address.(to add later)-->

## 標頭引數 {#email-header}

在 **[!UICONTROL 標頭引數]** 區段，輸入與該介面所傳送電子郵件型別相關聯的寄件者名稱和電子郵件地址。

* **[!UICONTROL 寄件者名稱]**：寄件者的名稱，例如您的品牌名稱。

* **[!UICONTROL 寄件者電子郵件]**：您要用於通訊的電子郵件地址。

* **[!UICONTROL 回覆（姓名）]**：收件者按一下 **回覆** 電子郵件使用者端軟體中的「 」按鈕。

* **[!UICONTROL 回覆（電子郵件）]**：收件者按一下 **回覆** 電子郵件使用者端軟體中的「 」按鈕。 [了解详情](#reply-to-email)

* **[!UICONTROL 錯誤電子郵件]**：在此位址上收到ISP在傳送郵件幾天後產生的所有錯誤（非同步退信）。

>[!CAUTION]
>
>此 **[!UICONTROL 寄件者電子郵件]** 和 **[!UICONTROL 錯誤電子郵件]** 位址必須使用目前選取的位址 [委派的子網域](../configuration/about-subdomain-delegation.md). 例如，如果委派的子網域為 *marketing.luma.com*，您可以使用 *contact@marketing.luma.com* 和 *error@marketing.luma.com*.

![](assets/preset-header.png)

>[!NOTE]
>
>位址必須以字母(A-Z)開頭，並且只能包含英數字元。 您也可以使用底線 `_`，點`.` 和連字型大小 `-` 個字元。

### 回覆電子郵件 {#reply-to-email}

定義 **[!UICONTROL 回覆（電子郵件）]** 位址，您可以指定任何電子郵件地址，但前提是地址有效、格式正確，且不含任何拼寫錯誤。

若要確保正確管理回覆，請遵循下列建議：

* 用於回覆的收件匣將收到所有回覆電子郵件，包括休假通知和質詢回覆，因此請確保您有手動或自動化流程來處理登入此收件匣的電子郵件。

* 確保專用收件匣有足夠的接收容量，可接收使用電子郵件介面傳送的所有回覆電子郵件。 如果收件匣傳回跳出，則可能無法收到客戶的部分回覆。

* 處理回覆時，請牢記隱私權與法規遵循義務，因為回覆可能包含個人識別資訊(PII)。

* 請勿在回覆收件匣中將郵件標示為垃圾訊息，因為這會影響傳送至此地址的所有其他回覆。

此外，在定義 **[!UICONTROL 回覆（電子郵件）]** 位址，請確定使用具有有效MX記錄設定的子網域，否則電子郵件表面處理將失敗。

如果您在提交電子郵件介面時發生錯誤，表示您輸入地址的子網域尚未設定MX記錄。 請連絡您的管理員以設定對應的MX記錄，或使用具有有效MX記錄設定的其他位址。

>[!NOTE]
>
>如果您輸入之位址的子網域是 [已完全委派](../configuration/delegate-subdomain.md#full-subdomain-delegation) 若要Adobe，請聯絡您的Adobe客戶主管。

### 轉寄電子郵件 {#forward-email}

如果您想要轉寄至特定的電子郵件地址，則所有收到的電子郵件都會由 [!DNL Journey Optimizer] 如需委派的子網域，請聯絡Adobe客戶服務。 您必須提供：

* 您所選擇的轉寄電子郵件地址。 請注意，轉寄電子郵件地址網域無法與委派給Adobe的任何子網域相符。
* 您的沙箱名稱。
* 將使用轉寄電子郵件地址的表面名稱。
* 目前 **[!UICONTROL 回覆（電子郵件）]** 在管道表面層級設定的地址。

>[!NOTE]
>
>每個子網域只能有一個轉寄電子郵件地址。 因此，如果多個曲面使用相同的子網域，則必須對所有曲面使用相同的轉寄電子郵件地址。

轉寄電子郵件地址將由Adobe設定。 這可能需要3到4天的時間。

## 密件副本電子郵件 {#bcc-email}

您可以傳送所傳送電子郵件的相同復本（或密件副本） [!DNL Journey Optimizer] 至密件副本收件匣，並儲存以供合規性或封存之用。

若要這麼做，請啟用 **[!UICONTROL 密件副本電子郵件]** 通道曲面層級的可選特徵。 [了解详情](../configuration/archiving-support.md#bcc-email)

![](assets/preset-bcc.png)

此外，在定義 **[!UICONTROL 密件副本電子郵件]** 位址，請確定使用具有有效MX記錄設定的子網域，否則電子郵件表面處理將失敗。

如果您在提交電子郵件介面時發生錯誤，表示您輸入地址的子網域尚未設定MX記錄。 請連絡您的管理員以設定對應的MX記錄，或使用具有有效MX記錄設定的其他位址。

## 電子郵件重試引數 {#email-retry}

>[!CONTEXTUALHELP]
>id="ajo_admin_presets_retryperiod"
>title="调整重试时段"
>abstract="当电子邮件投放由于临时软退回错误失败时，将重试 3.5 天（84 小时）。您可以调整此默认重试时段以更好地满足您的需求。"
>additional-url="https://experienceleague.adobe.com/docs/journey-optimizer/using/configuration/monitor-reputation/retries.html" text="关于重试"

您可以設定 **電子郵件重試引數**.

![](assets/preset-retry-parameters.png)

根據預設， [重試時段](../configuration/retries.md#retry-duration) 設為84小時，但您可以調整此設定以更符合您的需求。

您必須輸入下列範圍內的整數值（以小時或分鐘為單位）：

* 若是行銷電子郵件，最小重試期間為6小時。
* 對於異動電子郵件，最小重試時間為10分鐘。
* 對於這兩種電子郵件型別，最大重試時間為84小時（或5040分鐘）。

進一步瞭解中的重試 [本節](../configuration/retries.md).

## URL追蹤 {#url-tracking}

>[!CONTEXTUALHELP]
>id="ajo_admin_preset_utm"
>title="定义 URL 跟踪参数"
>abstract="使用此部分可自动将跟踪参数附加到在电子邮件内容中提供的 URL。此功能属于可选功能。"

>[!CONTEXTUALHELP]
>id="ajo_admin_preset_url_preview"
>title="预览 URL 跟踪参数"
>abstract="查看如何对电子邮件内容中出现的 URL 附加跟踪参数。"

您可以使用 **[!UICONTROL URL追蹤引數]** 評估您跨管道行銷工作的有效性。 此功能属于可选功能。

本節中定義的引數將會附加至電子郵件內容中所包含的URL結尾。 接著，您就可以在Adobe Analytics或Google Analytics等網站分析工具中擷取這些引數，並建立各種效能報表。

您可使用新增最多10個追蹤引數 **[!UICONTROL 新增引數]** 按鈕。

![](assets/preset-url-tracking.png)

若要設定URL追蹤引數，您可以直接在 **[!UICONTROL 名稱]** 和 **[!UICONTROL 值]** 欄位。

您也可以編輯每個 **[!UICONTROL 值]** 欄位使用 [運算式編輯器](../personalization/personalization-build-expressions.md). 按一下版本圖示以開啟編輯器。 從那裡，您可以選取可用的內容屬性和/或直接編輯文字。

![](assets/preset-url-tracking-editor.png)

下列預先定義的值可透過「運算式編輯器」使用：

* **來源動作ID**：新增至歷程或行銷活動的電子郵件動作ID。

* **來源動作名稱**：新增至歷程或行銷活動的電子郵件動作名稱。

* **來源ID**：傳送電子郵件的伴隨歷程或行銷活動的ID。

* **來源名稱**：傳送電子郵件的伴隨歷程或行銷活動的名稱。

* **來源版本ID**：傳送電子郵件的伴隨歷程或行銷活動版本的ID。

* **優惠方案ID**：電子郵件中使用的選件ID。

>[!NOTE]
>
>您可以從運算式編輯器結合輸入文字值和使用內容屬性。 每個 **[!UICONTROL 值]** 欄位可包含最多5 KB的字元數。

<!--You can drag and drop the parameters to reorder them.-->

以下是與Adobe Analytics和Google Analytics相容的URL範例。

* 與Adobe Analytics相容的URL： `www.YourLandingURL.com?cid=email_AJO_{{context.system.source.id}}_image_{{context.system.source.name}}`

* 與Google Analytics相容的URL： `www.YourLandingURL.com?utm_medium=email&utm_source=AJO&utm_campaign={{context.system.source.id}}&utm_content=image`

您可以動態預覽產生的追蹤URL。 每次新增、編輯或移除引數時，預覽都會自動更新。

![](assets/preset-url-tracking-preview.png)

>[!NOTE]
>
>您也可以將動態個人化追蹤引數新增至電子郵件內容中存在的連結，但這在介面層級無法進行。 使用電子郵件設計工具製作訊息時，您必須執行此動作。 [了解详情](message-tracking.md#url-tracking)
