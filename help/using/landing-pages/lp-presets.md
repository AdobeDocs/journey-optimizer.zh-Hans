---
solution: Journey Optimizer
product: journey optimizer
title: 定义登陆页面预设
description: 瞭解如何設定您的環境，以透過Journey Optimizer建立和使用登入頁面
role: Admin
level: Intermediate
keywords: 登陸，登陸頁面，設定，環境，子網域，預設集
exl-id: 7cf1f083-bef0-40b5-8ddd-920a9d108eca
source-git-commit: c0afa3e2bc6dbcb0f2f2357eebc04285de8c5773
workflow-type: tm+mt
source-wordcount: '347'
ht-degree: 17%

---

# 定义登陆页面预设 {#lp-presets}

>[!CONTEXTUALHELP]
>id="ajo_admin_config_lp_subdomain_header"
>title="创建登陆页面预设"
>abstract="为了构建登陆页面并通过 Journey Optimizer 使用它，您必须创建一个登陆页面预设，在其中包含要使用的子域。"

時間 [建立登入頁面](../landing-pages/create-lp.md#create-a-lp)，您必須選取登入頁面預設集，才能建置登入頁面並透過它運用 **[!DNL Journey Optimizer]**.

## 存取登陸頁面預設集 {#access-lp-presets}

若要存取登入頁面預設集，請遵循下列步驟。

1. 存取 **[!UICONTROL 管理]** > **[!UICONTROL 頻道]** 功能表。

1. 選取 **[!UICONTROL 品牌化]** > **[!UICONTROL 登陸頁面預設集]**.

   ![](assets/lp_presets-access.png)

1. 按一下任何預設集標籤以存取登陸頁面預設集詳細資料。

   ![](assets/lp_preset-details.png)

## 创建登陆页面预设 {#lp-create-preset}

若要建立登入頁面預設集，請遵循下列步驟。

>[!NOTE]
>
>若要建立預設集，請確定您先前已設定至少一個登陸頁面子網域。 [了解如何操作](lp-subdomains.md)

1. 存取 **[!UICONTROL 管理]** > **[!UICONTROL 頻道]** 功能表，然後選取 **[!UICONTROL 品牌化]** > **[!UICONTROL 登陸頁面預設集]**.

1. 選取 **[!UICONTROL 建立登陸頁面預設集]**.

   ![](assets/lp_create-preset-temp.png)

1. 輸入預設集的名稱和說明。

   >[!NOTE]
   >
   > 名稱必須以字母(A-Z)開頭。 它只能包含英數字元。 您也可以使用底線 `_`，點`.` 和連字型大小 `-` 個字元。

1. 從下拉式清單中選取登入頁面子網域。

   ![](assets/lp_preset-subdomain.png)

   >[!NOTE]
   >
   >若要能夠選取子網域，請確定您先前已設定至少一個登陸頁面子網域。 [了解如何操作](#lp-subdomains)

   與所選子網域對應的設定隨即顯示。

1. 如果您想要選取追蹤URL的登陸頁面子網域，請核取 **[!UICONTROL 與登陸頁面子網域相同]** 選項。 [進一步瞭解追蹤](../email/message-tracking.md)

   ![](assets/lp_preset-subdomain-settings-same.png)

   例如，如果登陸頁面URL是「pages.mail.luma.com」，而追蹤URL是「data.mail.luma.com」，您可以選擇使用「pages.mail.luma.com」做為追蹤子網域。

1. 按一下 **[!UICONTROL 提交]** 以確認建立登入頁面預設集。 <!--You can also save the preset as draft and resume its configuration later on.-->

   <!--![](assets/lp_preset-subdomain-settings-submit.png)-->

1. 建立登入頁面預設集後，它會顯示在清單中 **[!UICONTROL 作用中]** 狀態。 已準備好用於您的登入頁面。

   ![](assets/lp-preset-active-temp.png)

您現在已準備就緒 [建立登入頁面](../landing-pages/create-lp.md) 在 [!DNL Journey Optimizer].
<!--
>[!NOTE]
>
>Learn how to create channel surfaces for push notifications and emails in [this section](channel-surfaces.md).-->

**相关主题**：

* [登陆页面入门](../landing-pages/get-started-lp.md)
* [创建登陆页面](../landing-pages/create-lp.md#create-a-lp)
