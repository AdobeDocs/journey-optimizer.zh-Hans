---
solution: Journey Optimizer
product: journey optimizer
title: 設定SMS子網域
description: 瞭解如何使用Journey Optimizer設定SMS子網域
role: Admin
level: Intermediate
keywords: 簡訊、子網域、設定
exl-id: 08a546d1-060c-43e8-9eac-4c38945cc3e1
source-git-commit: c823d1a02ca9d24fc13eaeaba2b688249e61f767
workflow-type: tm+mt
source-wordcount: '741'
ht-degree: 24%

---

# 設定SMS子網域 {#lp-subdomains}

>[!CONTEXTUALHELP]
>id="ajo_admin_subdomain_sms_header"
>title="委派 SMS 子域"
>abstract="您将设置您的子域以使用 SMS。可使用已委派给 Adobe 的子域或配置另一子域。"

>[!CONTEXTUALHELP]
>id="ajo_admin_subdomain_sms"
>title="委派 SMS 子域"
>abstract="您必须配置一个子域以用于 SMS 消息，因为您需要此子域才能创建 SMS 表面。您必须配置子域以用于登陆页面，因为您需要此子域才能创建登陆页面预设。 您可以使用已委派的子域来 Adobe 或配置新的子域。"
>additional-url="https://experienceleague.adobe.com/docs/journey-optimizer/using/sms/sms-configuration.html#message-preset-sms" text="创建 SMS 表面"

>[!CONTEXTUALHELP]
>id="ajo_admin_config_sms_subdomain"
>title="选择 SMS 子域"
>abstract="要可创建 SMS 表面，请确保您以前已配置至少一个 SMS 表面，以供从子域名称列表中选择。"
>additional-url="https://experienceleague.adobe.com/docs/journey-optimizer/using/sms/sms-configuration.html#message-preset-sms" text="创建 SMS 表面"

若要能夠縮短新增至SMS訊息的URL，您必須設定將在下列情況下選取的子網域： [建立SMS表面](sms-configuration.md#message-preset-sms).

您可以使用已委派給Adobe的子網域，也可以設定其他子網域。 進一步瞭解將子網域委派至Adobe於 [本節](../configuration/delegate-subdomain.md).

>[!CAUTION]
>
>SMS子網域設定對所有環境都是通用的。 因此：
>
>* 若要存取和編輯SMS子網域，您必須擁有 **[!UICONTROL 管理SMS子網域]** 生產沙箱的許可權。
>
> * 對SMS子網域所做的任何修改也會影響生產沙箱。


## 使用現有的子網域 {#sms-use-existing-subdomain}

若要使用已委派給Adobe的子網域，請遵循下列步驟。

1. 存取 **[!UICONTROL 管理]** > **[!UICONTROL 頻道]** 功能表，然後選取 **[!UICONTROL 簡訊設定]** > **[!UICONTROL SMS子網域]**.

   ![](assets/sms_access-subdomains.png)

1. 按一下 **[!UICONTROL 設定子網域]**.

   ![](assets/sms_set-up-subdomain.png)

1. 選取 **[!UICONTROL 使用委派的子網域]** 從 **[!UICONTROL 設定型別]** 區段。

   ![](assets/sms_use-delegated-subdomain.png)

1. 輸入將顯示在簡訊URL中的前置詞。

   >[!NOTE]
   >
   >僅允許使用英數字元和連字型大小。

1. 從清單中選取委派的子網域。

   >[!NOTE]
   >
   >您無法選取已用作SMS子網域的子網域。

   <!--Capital letters are not allowed in subdomains. TBC by PM-->

   ![](assets/sms_prefix-and-subdomain.png)

   <!--Note that you cannot use multiple delegated subdomains of the same parent domain. For example, if 'marketing1.yourcompany.com' is already delegated to Adobe for your SMS messages, you will not be able to use 'marketing2.yourcompany.com'. However, multi-level subdomains being supported for SMS, you may proceed using a subdomain of 'marketing1.yourcompany.com' (such as 'email.marketing1.yourcompany.com'), or a different parent domain.-->

   >[!CAUTION]
   >
   >如果您選取的網域已委派給Adobe，請使用 [CNAME方法](../configuration/delegate-subdomain.md#cname-subdomain-delegation)，您必須在您的代管平台上建立DNS記錄。 若要產生DNS記錄，程式與您設定新的SMS子網域時相同。 瞭解如何在 [本節](#sms-configure-new-subdomain).

1. 单击&#x200B;**[!UICONTROL 提交]**。

1. 提交後，子網域會顯示在清單中，並附上 **[!UICONTROL 處理中]** 狀態。 如需子網域狀態的詳細資訊，請參閱 [本節](../configuration/about-subdomain-delegation.md#access-delegated-subdomains).<!--Same statuses?-->

   >[!NOTE]
   >
   >在能夠使用該子網域來傳送訊息之前，您必須等待Adobe執行所需的檢查，這可能需要4小時。<!--Learn more in [this section](delegate-subdomain.md#subdomain-validation).-->

1. 檢查成功後，子網域會取得 **[!UICONTROL 成功]** 狀態。 它可用來建立SMS頻道介面。

## 設定新的子網域 {#sms-configure-new-subdomain}

>[!CONTEXTUALHELP]
>id="ajo_admin_sms_subdomain_dns"
>title="生成匹配的 DNS 记录"
>abstract="要配置新的 SMS 子域，您需要复制在 Journey Optimizer 界面中显示的 Adobe 名称服务器信息，将它粘贴到您的域托管解决方案中以生成匹配的 DNS 记录。检查成功后，该子域即可用于创建 SMS 表面。"

若要設定新的子網域，請遵循下列步驟。

1. 存取 **[!UICONTROL 管理]** > **[!UICONTROL 頻道]** 功能表，然後選取 **[!UICONTROL 簡訊設定]** > **[!UICONTROL SMS子網域]**.

1. 按一下 **[!UICONTROL 設定子網域]**.

1. 選取 **[!UICONTROL 新增您自己的網域]** 從 **[!UICONTROL 設定型別]** 區段。

   ![](assets/sms_add-your-own-subdomain.png)

1. 指定要委派的子網域。

   >[!CAUTION]
   >
   >您無法使用現有的SMS子網域。
   >
   >子網域中不允許使用大寫字母。

   不允許將無效的子網域委派給Adobe。 請務必輸入貴組織所擁有的有效子網域，例如marketing.yourcompany.com。

   >[!NOTE]
   >
   >支援（相同父項網域的）多層級子網域。 例如，您可以使用「sms.marketing.yourcompany.com」。

1. 將會顯示要放置在DNS伺服器中的記錄。 複製此記錄或下載CSV檔案，然後導覽至您的網域託管解決方案，以產生相符的DNS記錄。

1. 請確定已在您的網域託管解決方案中產生DNS記錄。 如果所有專案皆已正確設定，請勾選「我確認……」方塊，然後按一下 **[!UICONTROL 提交]**.

   ![](assets/sms_add-your-own-subdomain-confirm.png)

   >[!NOTE]
   >
   >當您設定新的SMS子網域時，它始終會指向CNAME記錄。

1. 提交子網域委派後，子網域會顯示在清單中，並包含 **[!UICONTROL 處理中]** 狀態。 如需子網域狀態的詳細資訊，請參閱 [本節](../configuration/about-subdomain-delegation.md#access-delegated-subdomains).<!--Same statuses?-->

   >[!NOTE]
   >
   >在能夠使用該子網域來傳送SMS訊息之前，您必須等待Adobe執行所需的檢查，這可能最多需要4小時。<!--Learn more in [this section](#subdomain-validation).-->

1. 檢查成功後，子網域會取得 **[!UICONTROL 成功]** 狀態。 它可用來建立SMS頻道介面。

   請注意，子網域將標示為 **[!UICONTROL 已失敗]** 如果您無法在託管解決方案上建立驗證記錄。
