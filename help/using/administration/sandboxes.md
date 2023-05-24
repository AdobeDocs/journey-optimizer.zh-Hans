---
solution: Journey Optimizer
product: journey optimizer
title: 沙盒管理
description: 瞭解如何管理沙箱
feature: Sandboxes
topic: Administration
role: Admin, Architect, Developer
level: Experienced
keywords: 沙箱，虛擬，環境，組織，平台
exl-id: 14f80d5d-0840-4b79-9922-6d557a7e1247
source-git-commit: 16738786e4ebeef3417fd0f6e5be741b348c2744
workflow-type: tm+mt
source-wordcount: '387'
ht-degree: 54%

---

# 沙盒管理 {#sandboxes}

## 使用沙箱 {#using-sandbox}

[!DNL Journey Optimizer] 允许您将实例分区为称为沙盒的分隔虚拟环境。
沙盒通过 Admin Console 中的产品用户档案进行分配。[了解如何分配沙盒](permissions.md#create-product-profile)。

[!DNL Journey Optimizer] 反映为给定组织创建的 Adobe Experience Platform 沙盒。
可以从 Adobe Experience Platform 实例创建或重置 Adobe Experience Platform 沙盒。[進一步瞭解sandbox使用手冊](https://experienceleague.adobe.com/docs/experience-platform/sandbox/ui/user-guide.html?lang=zh-Hans){target="_blank"}.

您可以在熒幕右上角組織名稱旁找到沙箱切換器控制項。 要从一个沙盒切换到另一个沙盒，请单击切换器中当前活动的沙盒，然后从下拉列表中选择另一个沙盒。

![](assets/sandbox_5.png)

➡️ [在本影片中進一步瞭解沙箱](#video)

## 指派沙箱 {#assign-sandboxes}

>[!IMPORTANT]
>
> 沙箱管理只能由 **[!UICONTROL 產品]** 或 **[!UICONTROL 系統]** 管理員。 如需詳細資訊，請參閱 [Admin Console檔案](https://helpx.adobe.com/enterprise/admin-guide.html/enterprise/using/admin-roles.ug.html){target="_blank"}.

您可以選擇將不同的沙箱指派給現成可用的或自訂的 **[!UICONTROL 產品設定檔]**.

若要指派沙箱：

1. 在 [!DNL Admin Console]，來自 **[!UICONTROL 產品]** 索引標籤中，選取 **[!UICONTROL Adobe Experience Platform應用程式]** 產品。

1. 選取 **[!UICONTROL 產品設定檔]**.

   ![](assets/sandbox_1.png)

1. 選取 **[!UICONTROL 許可權]** 標籤。

1. 選取 **[!UICONTROL 沙箱]** 功能。

   ![](assets/sandbox_2.png)

1. 下 **[!UICONTROL 可用的許可權專案]**，按一下加號(+)圖示，將沙箱指派給您的設定檔。 [進一步瞭解sandbox](https://experienceleague.adobe.com/docs/experience-platform/sandbox/home.html?lang=zh-Hans){target="_blank"}.

   ![](assets/sandbox_3.png)

1. 如有需要，在 **[!UICONTROL 包含的許可權專案]**，按一下旁邊的X圖示，以移除對您的 **[!UICONTROL 產品設定檔]**.

   ![](assets/sandbox_4.png)

1. 单击&#x200B;**[!UICONTROL 保存]**。

## 访问内容 {#content-access}

要配置内容辅助功能，您需要为每个沙盒分配一个内容共享文件夹。您可以在「 」中建立和設定共用資料夾 **[!UICONTROL 儲存]** 標籤中顯示 [!DNL Admin Console] 適用於管理員。 如果您对 [!DNL Admin Console] 拥有系统管理员访问权限，则可以创建共享文件夹并向它们添加具有不同访问级别的代表。

![](assets/do-not-localize/content_access.png)

请注意，要使内容与正确的沙盒同步，您必须遵循与沙盒相同的语法，例如，如果沙盒命名为“development”，则共享文件夹应具有相同的名称。

[瞭解如何管理共用資料夾](https://helpx.adobe.com/cn/enterprise/admin-guide.html/enterprise/using/manage-adobe-storage.ug.html){target="_blank"}.

## 操作方法视频{#video}

了解沙盒是什么以及如何区分开发沙盒和生产沙盒。了解如何创建、重置和删除沙盒。

>[!VIDEO](https://video.tv.adobe.com/v/334355?quality=12)
