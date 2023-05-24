---
solution: Journey Optimizer
product: journey optimizer
title: 配置登陆页面子域
description: 瞭解如何使用Journey Optimizer設定登陸頁面子網域
role: Admin
level: Intermediate
keywords: 登陸、登陸頁面、子網域、設定
exl-id: dd1af8dc-3920-46cb-ae4d-a8f4d4c26e89
source-git-commit: 4f3d22c9ce3a5b77969a2a04dafbc28b53f95507
workflow-type: tm+mt
source-wordcount: '807'
ht-degree: 24%

---

# 配置登陆页面子域 {#lp-subdomains}

>[!CONTEXTUALHELP]
>id="ajo_admin_subdomain_lp_header"
>title="委派登陆页面子域"
>abstract="您需要设置子域以供登陆页面使用。可使用已委派给 Adobe 的子域或配置另一子域。"

>[!CONTEXTUALHELP]
>id="ajo_admin_subdomain_lp"
>title="委派登陆页面子域"
>abstract="您必须配置子域以用于登陆页面，因为您需要此子域才能创建登陆页面预设。您必须配置子域以用于登陆页面，因为您需要此子域才能创建登陆页面预设。 您可以使用已委派的子域来 Adobe 或配置新的子域。"
>additional-url="https://experienceleague.adobe.com/docs/journey-optimizer/using/landing-pages/lp-configuration/lp-presets.html#lp-create-preset" text="创建登陆页面预设"

>[!CONTEXTUALHELP]
>id="ajo_admin_config_lp_subdomain"
>title="创建登陆页面预设"
>abstract="要想创建登陆页面预设，请确保您之前至少配置了一个登陆页面子域，可以从子域名称列表中选择。"
>additional-url="https://experienceleague.adobe.com/docs/journey-optimizer/using/landing-pages/lp-configuration/lp-presets.html#lp-create-preset" text="创建登陆页面预设"

能夠 [建立登陸頁面預設集](lp-presets.md)，您必須設定用於登入頁面的子網域。

您可以使用已委派給Adobe的子網域，也可以設定其他子網域。 進一步瞭解將子網域委派至Adobe於 [本節](../configuration/delegate-subdomain.md).

>[!CAUTION]
>
>登陸頁面子網域設定對所有環境都是通用的。 因此，對登陸頁面子網域所做的任何修改也會影響生產沙箱。

## 使用現有的子網域 {#lp-use-existing-subdomain}

若要使用已委派給Adobe的子網域，請遵循下列步驟。

1. 存取 **[!UICONTROL 管理]** > **[!UICONTROL 頻道]** 功能表，然後選取 **[!UICONTROL 電子郵件設定]** > **[!UICONTROL 登陸頁面子網域]**.

   ![](assets/lp_access-subdomains.png)

1. 按一下 **[!UICONTROL 設定子網域]**.

   ![](assets/lp_set-up-subdomain.png)

1. 選取 **[!UICONTROL 使用委派網域]** 從 **[!UICONTROL 設定型別]** 區段。

   ![](assets/lp_use-delegated-subdomain.png)

1. 輸入將顯示在登陸頁面URL的前置詞。

   >[!NOTE]
   >
   >僅允許使用英數字元和連字型大小。

1. 從清單中選取委派的子網域。

   >[!NOTE]
   >
   >您無法選取已用作登陸頁面子網域的子網域。

   <!--Capital letters are not allowed in subdomains. TBC by PM-->

   ![](assets/lp_prefix-and-subdomain.png)

   請注意，您無法使用相同上層網域的多個委派子網域。 例如，如果登入頁面的「marketing1.yourcompany.com」已委派給Adobe，則您將無法使用「marketing2.yourcompany.com」。 不過，登陸頁面支援多層級子網域，因此您可以使用「marketing1.yourcompany.com」的子網域（例如「email.marketing1.yourcompany.com」）或不同的父網域繼續操作。

   >[!CAUTION]
   >
   >如果您選取的網域已委派給Adobe，請使用 [CNAME方法](../configuration/delegate-subdomain.md#cname-subdomain-delegation)，您必須在您的代管平台上建立DNS記錄。 若要產生DNS記錄，程式與您設定新登陸頁面子網域時的程式相同。 瞭解如何在 [本節](#lp-configure-new-subdomain).

1. 单击&#x200B;**[!UICONTROL 提交]**。

1. 提交後，子網域會顯示在清單中，並附上 **[!UICONTROL 處理中]** 狀態。 如需子網域狀態的詳細資訊，請參閱 [本節](../configuration/about-subdomain-delegation.md#access-delegated-subdomains).<!--Same statuses?-->

   ![](assets/lp_subdomain-processing.png)

   >[!NOTE]
   >
   >在能夠使用該子網域來傳送訊息之前，您必須等待Adobe執行所需的檢查，這可能需要4小時。<!--Learn more in [this section](delegate-subdomain.md#subdomain-validation).-->

1. 檢查成功後，子網域會取得 **[!UICONTROL 成功]** 狀態。 已準備好用來建立登入頁面預設集。

## 設定新的子網域 {#lp-configure-new-subdomain}

>[!CONTEXTUALHELP]
>id="ajo_admin_lp_subdomain_dns"
>title="生成匹配的 DNS 记录"
>abstract="要配置新的登陆页面子域，您需要复制 Journey Optimizer 界面中显示的 Adobe 名称服务器信息，将其粘贴到您的域托管解决方案中，以生成匹配的 DNS 记录。检查成功后，子域就可以用来创建登陆页面预设了。"

若要設定新的子網域，請遵循下列步驟。

1. 存取 **[!UICONTROL 管理]** > **[!UICONTROL 頻道]** 功能表，然後選取 **[!UICONTROL 電子郵件設定]** > **[!UICONTROL 登陸頁面子網域]**.

1. 按一下 **[!UICONTROL 設定子網域]**.

1. 選取 **[!UICONTROL 新增您自己的網域]** 從 **[!UICONTROL 設定型別]** 區段。

   ![](assets/lp_add-your-own-subdomain.png)

1. 指定要委派的子網域。

   >[!CAUTION]
   >
   >您無法使用現有的登陸頁面子網域。
   >
   >子網域中不允許使用大寫字母。

   不允許將無效的子網域委派給Adobe。 請務必輸入貴組織所擁有的有效子網域，例如marketing.yourcompany.com。

   >[!NOTE]
   >
   >對於登入頁面，支援多層級子網域。 例如，您可以使用「email.marketing.yourcompany.com」。

1. 將會顯示要放置在DNS伺服器中的記錄。 複製此記錄或下載CSV檔案，然後導覽至您的網域託管解決方案，以產生相符的DNS記錄。

1. 請確定已在您的網域託管解決方案中產生DNS記錄。 如果所有專案皆已正確設定，請勾選「我確認……」方塊，然後按一下 **[!UICONTROL 提交]**.

   ![](assets/lp_add-your-own-subdomain-confirm.png)

   >[!NOTE]
   >
   >當您設定新的登陸頁面子網域時，它始終會指向CNAME記錄。

1. 提交子網域委派後，子網域會顯示在清單中，並包含 **[!UICONTROL 處理中]** 狀態。 如需子網域狀態的詳細資訊，請參閱 [本節](../configuration/about-subdomain-delegation.md#access-delegated-subdomains).<!--Same statuses?-->

   >[!NOTE]
   >
   >您必須等到Adobe執行必要的檢查（最多可能需要4小時）後，才能將該子網域用於登入頁面。<!--Learn more in [this section](#subdomain-validation).-->

1. 檢查成功後，子網域會取得 **[!UICONTROL 成功]** 狀態。 已準備好用來建立登入頁面預設集。

   請注意，子網域將標示為 **[!UICONTROL 已失敗]** 如果您無法在託管解決方案上建立驗證記錄。
