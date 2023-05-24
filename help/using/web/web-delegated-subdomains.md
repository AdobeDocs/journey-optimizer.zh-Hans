---
solution: Journey Optimizer
product: journey optimizer
title: 配置 Web 子域
description: 瞭解如何使用Journey Optimizer設定網頁子網域
role: Admin
level: Intermediate
keywords: 網路、子網域、設定
exl-id: 6503d9e6-6c6c-4a6d-ad3d-1d81eb3b4698
source-git-commit: 40cdcace9788206ad32dc6ae1e5f70c66e684bcb
workflow-type: tm+mt
source-wordcount: '413'
ht-degree: 27%

---

# 配置 Web 子域 {#web-subdomains}

>[!CONTEXTUALHELP]
>id="ajo_admin_subdomain_web_header"
>title="委派 Web 子域"
>abstract="您将设置您的子域以供 Web 渠道使用。请从已委派给 Adobe 的子域中进行选择。"

>[!CONTEXTUALHELP]
>id="ajo_admin_subdomain_web"
>title="委派 Web 子域"
>abstract="如果您将来自 Adobe Experience Manager Assets Essentials 的内容添加到您的 Web 体验，则必须设置将用于发布此内容的子域。请从已委派给 Adobe 的子域中进行选择。"

>[!CONTEXTUALHELP]
>id="ajo_admin_subdomain_web_default"
>title="设置 Web 子域"
>abstract="从委派给 Adobe 的子域的列表中选择一个子域。可将此 Web 子域设置为默认子域，但一次只能使用一个默认子域。"

在製作網頁體驗時，如果您新增來自 [Adobe Experience Manager Assets Essentials](../email/assets-essentials.md) 程式庫，您必須設定用於發佈此內容的子網域。

若要這麼做，您必須從已委派給Adobe的子網域清單中選擇。 進一步瞭解將子網域委派至Adobe於 [本節](../configuration/delegate-subdomain.md).

>[!CAUTION]
>
>Web子網域設定對所有環境都是通用的。 因此：
>
>* 若要存取和編輯Web子網域，您必須擁有 **[!UICONTROL 管理Web子網域]** 生產沙箱的許可權。
>
> * 對Web子網域所做的任何修改也會影響生產沙箱。


您可以建立多個網頁子網域，但僅限 **預設** 將使用子網域。 您可以變更預設的網頁子網域，但一次只能使用一個子網域。

1. 存取 **[!UICONTROL 管理]** > **[!UICONTROL 頻道]** 功能表，然後選取 **[!UICONTROL Web設定]** > **[!UICONTROL Web子網域]**.

   ![](assets/web-access-subdomains.png)

1. 按一下 **[!UICONTROL 設定子網域]**.

1. 從清單中選取委派的子網域。

   ![](assets/web-subdomain-details.png)

   >[!NOTE]
   >
   >您無法選取已用作Web子網域的子網域。

1. 將會自動新增顯示在網頁URL中的前置詞。 您無法變更。

1. 若要將此子網域設定為預設值，請選取對應的選項。

   ![](assets/web-subdomain-details-default.png)

   >[!NOTE]
   >
   >僅限 **預設** 將使用子網域。

1. 单击&#x200B;**[!UICONTROL 提交]**. 子網域取得 **[!UICONTROL 成功]** 狀態。 已準備好用於您的Web體驗。

   >[!NOTE]
   >
   >在極少數的情況下，子網域設定可能會失敗。 在此情況下，您可以刪除 **[!UICONTROL 已失敗]** 子網域，以使用清除清單 **[!UICONTROL 刪除]** 按鈕來自 **[!UICONTROL 更多動作]** 圖示。

1. 此 **[!UICONTROL 預設]** 徽章會顯示在目前預設使用的子網域旁邊。 若要變更預設子網域，請選取 **[!UICONTROL 設定為預設值]** 從 **[!UICONTROL 更多動作]** 按鈕來設定所要的子網域。

   ![](assets/web-subdomain-default.png)

   >[!NOTE]
   >
   >您可以變更預設的網頁子網域，但一次只能使用一個子網域。

   <!--Only a subdomain with the **[!UICONTROL Success]** status can be set as default.

    You cannot delete a subdomain with the **[!UICONTROL Processing]** status.-->
