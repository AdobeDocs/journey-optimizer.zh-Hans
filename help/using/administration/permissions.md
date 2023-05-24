---
solution: Journey Optimizer
product: journey optimizer
title: 管理用户和产品配置文件
description: 瞭解如何管理使用者和產品設定檔
exl-id: 85fd386a-45fa-4f9a-89d1-cecc0749b90d
feature: Access Management
topic: Administration
role: Admin
level: Intermediate
keywords: 產品，設定檔，沙箱
source-git-commit: 16738786e4ebeef3417fd0f6e5be741b348c2744
workflow-type: tm+mt
source-wordcount: '838'
ht-degree: 6%

---

# 管理用户和产品配置文件 {#manage-permissions}

>[!IMPORTANT]
>
> 以下詳述的每個程式只能由 **[!UICONTROL 產品]** 或 **[!UICONTROL 系統]** 管理員。 如需詳細資訊，請參閱 [Admin Console檔案](https://helpx.adobe.com/enterprise/admin-guide.html/enterprise/using/admin-roles.ug.html).

**[!UICONTROL 產品設定檔]** 是貴組織內共用相同許可權和沙箱的使用者集。

此 [!DNL Journey Optimizer] product可讓您在不同的現成可用之間選取 **[!UICONTROL 產品設定檔]** 指派不同的許可權層級給使用者。 如需更多可用的 **[!UICONTROL 產品設定檔]**，請參閱此 [頁面](ootb-product-profiles.md).

每個使用者屬於一個 **[!UICONTROL 產品設定檔]** 有權使用產品中包含的Adobe應用程式和服務。

您也可以建立自己的 **[!UICONTROL 產品設定檔]** 如果您想要微調使用者對介面中特定功能或物件的存取權。

## 分配产品用户档案 {#assigning-product-profile}

您可以選擇指派現成可用的或自訂的 **[!UICONTROL 產品設定檔]** 給您的使用者。

每個具有指派許可權的現成可用產品設定檔清單可在以下網址找到： [內建產品設定檔](ootb-product-profiles.md) 區段。

若要指派 **[!UICONTROL 產品設定檔]**：

1. 在 [!DNL Admin Console]，來自 **[!UICONTROL 產品]** 索引標籤中，選取 **[!UICONTROL Experience Cloud — 平台支援的應用程式]** 產品。

1. 選取 **[!UICONTROL 產品設定檔]**.

   ![](assets/do-not-localize/access_control_2.png)

1. 從 **[!UICONTROL 使用者]** 標籤，按一下 **[!UICONTROL 新增使用者]**.

   ![](assets/do-not-localize/access_control_3.png)

1. 輸入使用者的名稱或電子郵件地址，然後選取使用者。

   如果使用者先前不是在 [!DNL Admin Console]，請參閱 [新增使用者檔案](https://helpx.adobe.com/enterprise/admin-guide.html/enterprise/using/manage-users-individually.ug.html#add-users).

   ![](assets/do-not-localize/access_control_4.png)

1. 執行與上述步驟相同的步驟，將其他使用者新增至 **[!UICONTROL 產品設定檔]**. 然後，按一下 **[!UICONTROL 儲存]**.

随后，您的用户将收到一封重定向到您的实例的电子邮件。

如需使用者管理的詳細資訊，請參閱 [Admin Console檔案](https://helpx.adobe.com/enterprise/admin-guide.html/enterprise/using/manage-users-individually.ug.html).

存取執行個體時，您的使用者將會看到特定檢視，具體取決於中指派的許可權 **[!UICONTROL 產品設定檔]**. 如果使用者沒有功能的正確存取權，將會出現以下訊息：

`You don't have permission to access this feature. Permission needed: XX.`

## 編輯現有產品設定檔 {#edit-product-profile}

適用於現成可用或自訂的 **[!UICONTROL 產品設定檔]**，您隨時可以決定新增或刪除許可權。

在此範例中，我們要新增 **[!UICONTROL 許可權]** 與 **[!UICONTROL 歷程]** 指派給Journey Viewer的使用者功能 **[!UICONTROL 產品設定檔]**. 之後，使用者將能夠發佈歷程。

請注意，如果您修改現成可用的或自訂的 **[!UICONTROL 產品設定檔]**，它將會影響指派給此專案的每個使用者 **[!UICONTROL 產品設定檔]**.

1. 在 [!DNL Admin Console]，來自 **[!UICONTROL 產品]** 索引標籤中，選取 **[!UICONTROL Experience Cloud — 平台支援的應用程式]** 產品。

1. 選取歷程檢視器 **[!UICONTROL 產品設定檔]**.

1. 選取 **[!UICONTROL 許可權]** 標籤。

   此 **[!UICONTROL 許可權]** 標籤顯示套用至 **[!UICONTROL Experience Cloud — 平台支援的應用程式]** 產品。

   ![](assets/do-not-localize/access_control_5.png)

1. 選取 **[!UICONTROL 歷程]** 功能。

   ![](assets/do-not-localize/access_control_6.png)

1. 從 **[!UICONTROL 可用的許可權專案]** 清單中，選取要指派給您的使用者的許可權 **[!UICONTROL 產品設定檔]** 按一下加號(+)圖示。

   在此，我們新增 **[!UICONTROL 發佈歷程]** 許可權。

1. 如有需要，在 **[!UICONTROL 包含的許可權專案]**，按一下旁邊的X圖示，以移除產品設定檔的許可權。

1. 完成后，单击&#x200B;**[!UICONTROL 保存]**。

如有需要，您也可以建立具有特定許可權的新產品設定檔。 有關詳細資訊，請參閱 [建立產品設定檔](#create-product-profile).

## 创建产品用户档案 {#create-product-profile}

[!DNL Journey Optimizer] 可讓您建立自己的 **[!UICONTROL 產品設定檔]** 並將一組許可權和沙箱指派給您的使用者。 替換為 **[!UICONTROL 產品設定檔]**，您可以授權或拒絕存取介面中的特定功能或物件。

有關如何建立和管理沙箱的詳細資訊，請參閱 [Adobe Experience Platform檔案](https://experienceleague.adobe.com/docs/experience-platform/sandbox/ui/user-guide.html?lang=zh-Hans){target="_blank"}.

在此範例中，我們將建立名為的產品設定檔 **歷程唯讀** 我們將在此授與歷程功能的唯讀許可權。 使用者將只能存取和檢視歷程，而無法存取其他功能，例如 **[!DNL  Decision management]** 在 [!DNL Journey Optimizer].

若要建立我們的 **歷程唯讀** **[!UICONTROL 產品設定檔]**：

1. 存取 [!DNL Admin Console].

1. 從 **[!UICONTROL 產品]** 索引標籤中，選取 **[!UICONTROL Experience Cloud — 平台支援的應用程式]** 產品。

1. 单击&#x200B;**[!UICONTROL 新建配置文件]**。

   ![](assets/do-not-localize/access_control_9.png)

1. 新增 **[!UICONTROL 產品設定檔名稱]**， **[!UICONTROL 顯示名稱]** 和 **[!UICONTROL 說明]** （針對您的新） **[!UICONTROL 產品設定檔]**.

   ![](assets/do-not-localize/access_control_10.png)

1. 在 **[!UICONTROL 通知]** 類別，選擇從此產品設定檔新增或移除使用者時，使用者是否會收到電子郵件通知。

1. 完成後，按一下 **[!UICONTROL 儲存]** 並選取您新建立的 **[!UICONTROL 產品設定檔]**.

1. 若要新增使用者存取不同功能的許可權，請選取 **[!UICONTROL 許可權]** 標籤。

1. 在不同的功能之間選取，例如 **[!DNL Journeys]**， **[!DNL Segments]** 或 **[!DNL Decision management]** 提供於 [!DNL Journey Optimizer] 列於左側功能表中。

   在此處，我們選取 **[!UICONTROL 歷程]** 功能。

   ![](assets/do-not-localize/access_control_11.png)

1. 從 **[!UICONTROL 可用的許可權專案]** 清單中，選取要指派給您的使用者的許可權 **[!UICONTROL 產品設定檔]** 按一下加號(+)圖示。

   我們在這裡選取 **[!DNL View journeys]** 和 **[!DNL View journeys event, data sources, actions]**.

   ![](assets/do-not-localize/access_control_12.png)

1. 選取 **[!UICONTROL 沙箱存取]** 能夠選擇要指派給您的哪個沙箱 **[!UICONTROL 產品設定檔]**.

   ![](assets/do-not-localize/access_control_13.png)

1. 下 **[!UICONTROL 可用的許可權專案]**，按一下加號(+)圖示，將沙箱指派給您的設定檔。 [进一步了解沙盒](sandboxes.md)。

1. 完成后，单击&#x200B;**[!UICONTROL 保存]**。

您的 **[!UICONTROL 產品設定檔]** 現在已建立並設定。 您現在需要將其指派給使用者。

如需有關產品設定檔建立與管理的詳細資訊，請參閱 [Admin Console檔案](https://helpx.adobe.com/enterprise/admin-guide.html/enterprise/using/manage-product-profiles.ug.html).
