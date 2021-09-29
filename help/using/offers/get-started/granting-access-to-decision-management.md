---
product: experience platform
solution: Experience Platform
title: 授予访问 Offer Decisioning 的权限
description: 了解如何通过Adobe Admin Console管理Offer Decisioning服务的用户权限。
feature: Collections
role: User
level: Intermediate
exl-id: 2a2fece9-1ad5-498e-b0ee-5bb0b73a2cd5
source-git-commit: 43fb98a08555e6b889ad537e79dba78286dafeb9
workflow-type: tm+mt
source-wordcount: '273'
ht-degree: 7%

---

# 授予对决策管理的访问权限 {#granting-acess-to-decision-management}

使用[Adobe Admin Console](https://helpx.adobe.com/cn/enterprise/managing/user-guide.html){target=&quot;_blank&quot;}管理访问和使用offer decisioning功能的权限。

要授予对决策管理功能的访问权限，您需要创建&#x200B;**[!UICONTROL Product profile]**&#x200B;并将相应的权限分配给用户。 了解有关在[此部分](../../administration/permissions.md)中管理[!DNL Journey Optimizer]用户和权限的更多信息。

[此部分](../../administration/high-low-permissions.md#manage-decisioning)中列出了特定于决策管理的权限。

<!--If you are a [!DNL Journey Optimizer] user leveraging the **Decision Management** functionality, you need to have the [Decision management permissions](../../administration/high-low-permissions.md#decisions-permissions) enabled to acces all related capabilities. Learn more on managing [!DNL Journey Optimizer] users and permissions in [this section](../../administration/permissions.md).

If you are an [Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/landing/home.html){target="_blank"} user leveraging the **Offer Decisioning** application service, follow the steps [below](#granting-acess-to-offer-decisioning) to grant access to [!DNL Offer Decisioning].

Grant access to Offer Decisioning

The steps below only apply to **Experience Platform users** leveraging the [!DNL Offer Decisioning] service.-->

1. 打开[Admin Console](https://helpx.adobe.com/enterprise/managing/user-guide.html)，然后选择&#x200B;**[!UICONTROL Adobe Experience Platform]**。

   <!--![](../../assets/offers_admin_console.png)-->

1. 将显示服务的产品配置文件。 要创建新的产品配置文件，请单击&#x200B;**[!UICONTROL New Profile]**&#x200B;按钮。

   ![](../../assets/offers_rights_productprofile.png)

   >[!NOTE]
   >
   >您可以拥有所需数量的产品配置文件，这些配置文件与您要为组织设置的各种角色相对应。

1. 指定产品配置文件的名称和描述，然后单击&#x200B;**[!UICONTROL Next]**。

   ![](../../assets/create-product-profile.png)

   <!--To access the product profile’s permissions, select the **[!UICONTROL Permissions]** line.-->

1. 选择要为产品配置文件启用的服务。 默认情况下，会选择所有服务，这是为了确保所有Experience Platform功能都可用而建议的。

   ![](../../assets/enable-services.png)

1. 在&#x200B;**[!UICONTROL Decision Management]**&#x200B;部分中，单击&#x200B;**+**&#x200B;按钮以分配产品配置文件的权限，然后单击&#x200B;**[!UICONTROL Save]**。

   ![](../../assets/configure-profile.png)

   可用权限包括：

   **[!UICONTROL Manage Decisioning Activities]**：

   * 读取、写入、删除选件
   * 读取、写入、删除决策（以前称为选件活动）
   * 读、写、删除版面

   **[!UICONTROL Execute Decisioning Activities]**：

   * 读取选件
   * 阅读决策
   * 阅读版面

   **[!UICONTROL Manage Decisioning Options]**：

   * 读取、写入、删除选件
   * 阅读决策
   * 读、写、删除版面



1. 此时会显示产品用户档案权限的摘要。 您现在可以将用户分配到产品配置文件，以便他们访问这些权限。

   ![](../../assets/product-profile-created.png)

>[!NOTE]
>
>有关如何管理用户权限的更多详细信息，请参阅[Admin Console文档](https://helpx.adobe.com/enterprise/managing/user-guide.html){target=&quot;_blank&quot;}。

