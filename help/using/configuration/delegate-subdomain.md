---
solution: Journey Optimizer
product: journey optimizer
title: 委派子域
description: 瞭解如何委派子網域。
feature: Application Settings
topic: Administration
role: Admin
level: Intermediate
keywords: 子網域、委派、網域、DNS
exl-id: 8021f66e-7725-475b-8722-e6f8d74c9023
source-git-commit: 54ea3573e4fb6e24c3e56349292528bc6da42d67
workflow-type: tm+mt
source-wordcount: '1757'
ht-degree: 23%

---

# 委派子域 {#delegate-subdomain}

>[!CONTEXTUALHELP]
>id="ajo_admin_subdomainname"
>title="子域委派"
>abstract="Journey Optimizer 让您可以将子域委派给 Adobe。您可以将子域完全委派给 Adobe，这是推荐的方法。您也可以使用 CNAME 创建子域，将其指向特定于 Adobe 的记录，但这种方法需要您自行维护和管理 DNS 记录。"
>additional-url="https://experienceleague.adobe.com/docs/journey-optimizer/using/configuration/delegate-subdomains/about-subdomain-delegation.html#subdomain-delegation-methods" text="子域配置方法"

>[!CONTEXTUALHELP]
>id="ajo_admin_subdomainname_header"
>title="子域委派"
>abstract="要开始发送电子邮件，您需要将子域委派给 Adobe。委派完成后，将为您配置 DNS 记录、收件箱、发件人、回复地址和退回地址。"

網域名稱委派是一種方法，可讓網域名稱（技術上稱為DNS區域）的擁有者將其細分（技術上稱為DNS區域，也可以稱為子區域）委派給另一個實體。 基本上，身為客戶，如果您處理&quot;example.com&quot;區域，您可以將子網區&quot;marketing.example.com&quot;委派給Adobe。 進一步瞭解 [子網域委派](about-subdomain-delegation.md)

>[!NOTE]
>
>依預設， [!DNL Journey Optimizer] 授權合約可讓您委派最多10個子網域。 如果您想要提高此限制，請聯絡您的Adobe聯絡人。

您可以完全委派子網域，或使用CNAME建立子網域以指向Adobe特定記錄。

>[!CAUTION]
>
>建議使用完全子網域委派方法。 進一步瞭解兩者之間的差異 [子網域設定方法](about-subdomain-delegation.md#subdomain-delegation-methods).
>
>子網域設定對所有環境都是通用的。 因此，對子網域所做的任何修改也會影響生產沙箱。

## 完全子域委派 {#full-subdomain-delegation}

>[!CONTEXTUALHELP]
>id="ajo_admin_subdomain_dns"
>title="生成匹配的 DNS 记录"
>abstract="要将新的子域完全委派给 Adobe，您需要将 Journey Optimizer 界面中显示的 Adobe 名称服务器信息，复制粘贴到您的域托管解决方案中，以生成匹配的 DNS 记录。要使用 CNAME 委派子域，您还需要复制粘贴 SSL CDN URL 验证记录。检查成功后，子域就可以用来传递消息了。"
>additional-url="https://experienceleague.adobe.com/docs/journey-optimizer/using/configuration/delegate-subdomains/delegate-subdomain.html#cname-subdomain-delegation" text="CNAME 子域委派"

[!DNL Journey Optimizer] 可讓您直接從產品介面將子網域完全委派給Adobe。 透過這樣做，Adobe將能夠控制並維護傳遞、演算及追蹤電子郵件行銷活動所需的DNS的各個層面，以受管理的方式傳遞訊息。

您可以仰賴Adobe來維護所需的DNS基礎架構，以符合電子郵件行銷傳送網域的產業標準傳遞能力要求，同時繼續維護和控制內部電子郵件網域的DNS。

若要將新子網域完全委派給Adobe，請執行以下步驟：

1. 存取 **[!UICONTROL 管理]** > **[!UICONTROL 頻道]** > **[!UICONTROL 子網域]** 功能表，然後按一下 **[!UICONTROL 設定子網域]**.

   ![](assets/subdomain-delegate.png)

1. 選取 **[!UICONTROL 已完全委派]** 從 **[!UICONTROL 設定方法]** 區段。

   ![](assets/subdomain-method-full.png)

1. 指定要委派的子網域名稱。

   ![](assets/subdomain-name.png)

   >[!CAUTION]
   >
   >不允許將無效的子網域委派給Adobe。 請務必輸入貴組織所擁有的有效子網域，例如marketing.yourcompany.com。

   <!--Capital letters are not allowed in subdomains. TBC by PM-->

1. 此时将显示要放入您的 DNS 服务器中的记录列表。逐个复制这些记录，或者下载 CSV 文件，然后导航到您的域托管解决方案以生成匹配的 DNS 记录。

1. 請確定所有DNS記錄皆已產生至您的網域託管解決方案。 如果所有專案皆已正確設定，請勾選「我確認……」方塊，然後按一下 **[!UICONTROL 提交]**.

   ![](assets/subdomain-submit.png)

   >[!NOTE]
   >
   >您可以建立記錄，並在稍後使用提交子網域設定 **[!UICONTROL 另存為草稿]** 按鈕。 然後，您就可以從子網域清單中開啟子網域委派，以繼續子網域委派。

1. 提交完整子網域委派後，子網域會顯示在清單中，並包含 **[!UICONTROL 處理中]** 狀態。 如需子網域狀態的詳細資訊，請參閱 [本節](about-subdomain-delegation.md#access-delegated-subdomains).

   ![](assets/subdomain-processing.png)

   在能夠使用該子網域來傳送訊息之前，您必須等待Adobe執行所需的檢查，這可能最多需要3小時。 有关详细信息，请参阅[此部分](#subdomain-validation)。

   >[!NOTE]
   >
   >任何遺失的記錄（代表尚未在您的託管解決方案上建立的記錄）都會列出。

1. 檢查成功後，子網域會取得 **[!UICONTROL 成功]** 狀態。 已準備好用於傳遞訊息。

   >[!NOTE]
   >
   >子網域將標示為 **[!UICONTROL 已失敗]** 如果您無法在託管解決方案上建立驗證記錄。

一旦將子網域委派給中的Adobe [!DNL Journey Optimizer]，系統會自動建立PTR記錄並與其建立關聯。 [了解详情](ptr-records.md)

>[!CAUTION]
>
>目前不支援並行執行子網域 [!DNL Journey Optimizer]. 如果您嘗試提交子網域以進行委派，但另一個子網域具有 **[!UICONTROL 處理中]** 狀態，您會收到錯誤訊息。

## CNAME 子域委派 {#cname-subdomain-delegation}

>[!CONTEXTUALHELP]
>id="ajo_admin_subdomain_dns_cname"
>title="生成匹配的 DNS 和验证记录"
>abstract="要使用 CNAME 委派子域，您需要将 Journey Optimizer 界面中显示的 Adobe 名称服务器信息和 SSL CDN URL 验证记录，复制粘贴到您的托管平台中。检查成功后，子域就可以用来传递消息了。"

>[!CONTEXTUALHELP]
>id="ajo_admin_subdomain_cdn_cname"
>title="复制验证记录"
>abstract="Adobe 生成验证记录。您需要在托管平台上创建对应的记录，用于 CDN URL 验证。"

如果您有網域特定的限制原則，並且您希望Adobe只對DNS有部分控制權，您可以選擇在自己這邊執行所有與DNS相關的活動。

CNAME 子域委派允许您创建子域，并使用 CNAME 指向特定于 Adobe 的记录。使用此配置，您和 Adobe 共同负责维护 DNS，以设置用于发送、渲染和跟踪电子邮件的环境。

>[!CAUTION]
>
>如果您組織的原則限制了完整子網域委派方法，則建議使用CNAME方法。 此方法需要您自行維護和管理DNS記錄。 Adobe將無法協助變更、維護或管理透過CNAME方法設定的子網域的DNS。

➡️ [在本影片中瞭解如何使用CNAME建立子網域以指向Adobe特定記錄](#video)

若要使用CNAME委派子網域，請遵循下列步驟：

1. 存取 **[!UICONTROL 管理]** > **[!UICONTROL 頻道]** > **[!UICONTROL 子網域]** 功能表，然後按一下 **[!UICONTROL 設定子網域]**.

1. 選取 **[!UICONTROL CNAME設定]** 方法。

   ![](assets/subdomain-method-cname.png)

1. 指定要委派的子網域名稱。

   >[!CAUTION]
   >
   >不允許將無效的子網域委派給Adobe。 請務必輸入貴組織所擁有的有效子網域，例如marketing.yourcompany.com。

   <!--Capital letters are not allowed in subdomains. TBC by PM-->

1. 此时将显示要放入您的 DNS 服务器中的记录列表。逐个复制这些记录，或者下载 CSV 文件，然后导航到您的域托管解决方案以生成匹配的 DNS 记录。

1. 請確定所有DNS記錄皆已產生至您的網域託管解決方案。 如果所有專案皆已正確設定，請勾選「我確認……」方塊。

   ![](assets/subdomain-create-dns-confirm.png)

   >[!NOTE]
   >
   >您稍後可以使用 **[!UICONTROL 另存為草稿]** 按鈕。 然後，您就可以在此階段從子網域清單中開啟子網域委派，以繼續子網域委派。

1. 等到Adobe驗證這些記錄是在您的託管解決方案上沒有錯誤的情況下產生。 此程式最多可能需要2分鐘。

   >[!NOTE]
   >
   >任何遺失的記錄（代表尚未在您的託管解決方案上建立的記錄）都會列出。

1. Adobe會產生SSL CDN URL驗證記錄。 將此驗證記錄複製到您的託管平台。 如果您已在代管解決方案上正確建立此記錄，請核取「我確認……」方塊，然後按一下 **[!UICONTROL 提交]**.

   <!--![](assets/subdomain-cdn-url-validation.png)-->

   >[!NOTE]
   >
   >您也可以建立驗證記錄，並在稍後使用提交子網域設定。 **[!UICONTROL 另存為草稿]** 按鈕。 然後，您就可以從子網域清單中開啟子網域委派，以繼續子網域委派。

1. 提交CNAME子網域委派後，子網域會顯示在清單中，並附上 **[!UICONTROL 處理中]** 狀態。 如需子網域狀態的詳細資訊，請參閱 [本節](about-subdomain-delegation.md#access-delegated-subdomains).

   ![](assets/subdomain-cname-processing.png)

   在能夠使用該子網域來傳送訊息之前，您必須等待Adobe執行所需的檢查，這通常需要2到3小時。 有关详细信息，请参阅[此部分](#subdomain-validation)。

1. 檢查成功後<!--i.e Adobe validates the record you created and installs it-->，子網域會取得 **[!UICONTROL 成功]** 狀態。 已準備好用於傳遞訊息。

   >[!NOTE]
   >
   >子網域將標示為 **[!UICONTROL 已失敗]** 如果您無法在託管解決方案上建立驗證記錄。

在驗證記錄並安裝憑證後，Adobe會自動建立CNAME子網域的PTR記錄。 [了解详情](ptr-records.md)

>[!CAUTION]
>
>目前不支援並行執行子網域 [!DNL Journey Optimizer]. 如果您嘗試提交子網域以進行委派，但另一個子網域具有 **[!UICONTROL 處理中]** 狀態，您會收到錯誤訊息。

## 子網域驗證 {#subdomain-validation}

將執行下面的檢查和動作，直到驗證子網域並可用於傳送訊息為止。

>[!NOTE]
>
>這些步驟由Adobe執行，最多可能需要3小時。

1. **預先驗證**：Adobe會檢查子網域是否已委派給AdobeDNS （NS記錄、SOA記錄、區域設定、所有權記錄）。 如果預先驗證步驟失敗，則會傳回錯誤及相應原因，否則Adobe會進行到下一個步驟。

1. **設定網域的DNS**：

   * **MX記錄**：郵件交換記錄 — 處理傳送到子網域之傳入電子郵件的郵件伺服器記錄。
   * **SPF記錄**：寄件者原則架構記錄 — 列出可從子網域傳送電子郵件的郵件伺服器IP。
   * **DKIM記錄**： DomainKeys Identified Mail標準記錄 — 使用公開私密金鑰加密來驗證郵件以避免詐騙。
   * **A**：預設IP對應。
   * **CNAME**：正式名稱或CNAME記錄是一種DNS記錄，將別名對應到真實或正式網域名稱。

1. **建立追蹤和映象URL**：如果網域為email.example.com，追蹤/映象網域將為data.email.example.com。 安裝SSL憑證即可確保安全性。

1. **布建CDN CloudFront**：如果尚未設定CDN，則Adobe會將其布建為您組織的ID。

1. **建立CDN網域**：如果網域為email.example.com，則CDN網域將為cdn.email.example.com。

1. **建立並附加CDN SSL憑證**：Adobe會為CDN網域建立CDN憑證，並將憑證附加至CDN網域。

1. **建立轉送DNS**：如果您所委派的第一個子網域，Adobe會建立轉送DNS （建立PTR記錄所需） — 每個IP各一個。

1. **建立PTR記錄**：ISP需要PTR記錄（也稱為反向DNS記錄），才能將電子郵件標示為垃圾郵件。 Gmail也建議每個IP都有PTR記錄。 Adobe只會在您第一次委派子網域時建立PTR記錄，每個IP各一個，所有IP都指向該子網域。 例如，如果IP為 *192.1.2.1* 而子網域為 *email.example.com*，PTR記錄會是： *192.1.2.1 PTR r1.email.example.com*. 您之後可以更新PTR記錄，以指向新的委派網域。 [深入瞭解PTR記錄](ptr-records.md)

## 操作方法视频{#video}

了解如何使用 CNAME 创建子域以指向特定于 Adobe 的记录。

>[!VIDEO](https://video.tv.adobe.com/v/339484?quality=12)
