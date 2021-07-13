---
title: 沙盒管理
description: 了解如何管理沙箱
feature: 对照组
topic: 管理
role: Admin
level: Intermediate
source-git-commit: 63de381ea3a87b9a77bc6f1643272597b50ed575
workflow-type: tm+mt
source-wordcount: '335'
ht-degree: 69%

---

# 沙盒管理 {#sandboxes}

## 使用沙箱 {#using-sandbox}

[!DNL Journey Optimizer] 允许您将实例分区为称为沙箱的分隔虚拟环境。
沙箱通过 Admin Console 中的产品用户档案进行分配。[了解如何分配沙箱](permissions.md#create-product-profile)。

[!DNL Journey Optimizer] 反映为给定组织创建的 Adobe Experience Platform 沙箱。
可以从 Adobe Experience Platform 实例创建或重置 Adobe Experience Platform 沙箱。[请参阅沙盒用户指南](https://experienceleague.adobe.com/docs/experience-platform/sandbox/ui/user-guide.html?lang=zh-Hans){target=&quot;_blank&quot;}以了解更多信息。

您可以在屏幕左上角找到沙箱切换器控件。要从一个沙箱切换到另一个沙箱，请单击切换器中当前活动的沙箱，然后从下拉列表中选择另一个沙箱。

## 分配沙箱 {#assign-sandboxes}

>[!IMPORTANT]
>
> 沙箱管理只能由&#x200B;**[!UICONTROL Product]**&#x200B;或&#x200B;**[!UICONTROL System]**&#x200B;管理员执行。 有关此内容的更多信息，请参阅[管理控制台文档](https://helpx.adobe.com/enterprise/admin-guide.html/enterprise/using/admin-roles.ug.html){target=&quot;_blank&quot;}。

您可以选择为现成或自定义&#x200B;**[!UICONTROL Product profiles]**&#x200B;分配不同的沙箱。

要分配沙箱，请执行以下操作：

1. 在[!DNL Admin Console]的&#x200B;**[!UICONTROL Products]**&#x200B;选项卡中，选择&#x200B;**[!UICONTROL Adobe Experience Platform Apps]**&#x200B;产品。

1. 选择 **[!UICONTROL Product profile]**。

   ![](../assets/sandbox_1.png)

1. 选择 **[!UICONTROL Permissions]** 选项卡。

1. 选择&#x200B;**[!UICONTROL Sandboxes]**&#x200B;功能。

   ![](../assets/sandbox_2.png)

1. 在 **[!UICONTROL Available Permissions Items]** 下，单击加号 (+) 图标，将沙箱分配给用户档案。[了解有关沙箱](https://experienceleague.adobe.com/docs/experience-platform/sandbox/home.html?lang=zh-Hans){target=&quot;_blank&quot;}的更多信息。

   ![](../assets/sandbox_3.png)

1. 如果需要，在&#x200B;**[!UICONTROL Included Permission Items]**&#x200B;下，单击删除沙箱对&#x200B;**[!UICONTROL Product profile]**&#x200B;的访问权限旁边的X图标。

   ![](../assets/sandbox_4.png)

1. 单击 **[!UICONTROL Save]**。

## 访问内容 {#content-access}

要配置内容辅助功能，您需要为每个沙箱分配一个内容共享文件夹。您可以在 [!DNL Admin Console] 中显示的 **[!UICONTROL Storage]** 选项卡中为管理员创建和配置共享文件夹。如果您对 [!DNL Admin Console] 拥有系统管理员访问权限，则可以创建共享文件夹并向它们添加具有不同访问级别的代表。

![](../assets/do-not-localize/content_access.png)

请注意，要使内容与正确的沙箱同步，您必须遵循与沙箱相同的语法，例如，如果沙箱命名为“development”，则共享文件夹应具有相同的名称。

[了解如何管理共享文件夹](https://helpx.adobe.com/enterprise/admin-guide.html/enterprise/using/manage-adobe-storage.ug.html){target=&quot;_blank&quot;}。
