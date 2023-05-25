---
solution: Journey Optimizer
product: journey optimizer
title: 管理用户和产品配置文件
description: 了解如何管理用户和产品配置文件
exl-id: 85fd386a-45fa-4f9a-89d1-cecc0749b90d
feature: Access Management
topic: Administration
role: Admin
level: Intermediate
keywords: 产品、配置文件、沙盒
source-git-commit: 16738786e4ebeef3417fd0f6e5be741b348c2744
workflow-type: tm+mt
source-wordcount: '838'
ht-degree: 6%

---

# 管理用户和产品配置文件 {#manage-permissions}

>[!IMPORTANT]
>
> 以下详述的每个程序只能通过 **[!UICONTROL 产品]** 或 **[!UICONTROL 系统]** 管理员。 有关详情，请参阅 [Admin console文档](https://helpx.adobe.com/enterprise/admin-guide.html/enterprise/using/admin-roles.ug.html).

**[!UICONTROL 产品配置文件]** 是组织内共享相同权限和沙盒的用户集。

此 [!DNL Journey Optimizer] product允许您在不同的现成选项之间进行选择 **[!UICONTROL 产品配置文件]** 具有不同级别的权限以分配给用户。 欲知关于可用的 **[!UICONTROL 产品配置文件]**，请参阅此 [页面](ootb-product-profiles.md).

每个用户属于一个 **[!UICONTROL 产品配置文件]** 有权使用产品中包含的Adobe应用程序和服务。

您还可以创建自己的 **[!UICONTROL 产品配置文件]** 如果您希望微调用户对界面中特定功能或对象的访问权限。

## 分配产品用户档案 {#assigning-product-profile}

您可以选择分配现成或自定义的 **[!UICONTROL 产品配置文件]** 发送给您的用户。

每个具有已分配权限的现成产品配置文件的列表都可在中找到 [内置产品配置文件](ootb-product-profiles.md) 部分。

要分配 **[!UICONTROL 产品配置文件]**：

1. 在 [!DNL Admin Console]，来自 **[!UICONTROL 产品]** 选项卡，选择 **[!UICONTROL Experience Cloud — 平台支持的应用程序]** 产品。

1. 选择 **[!UICONTROL 产品配置文件]**.

   ![](assets/do-not-localize/access_control_2.png)

1. 从 **[!UICONTROL 用户]** 选项卡，单击 **[!UICONTROL 添加用户]**.

   ![](assets/do-not-localize/access_control_3.png)

1. 键入用户名或电子邮件地址，然后选择用户。

   如果用户之前未在 [!DNL Admin Console]，请参阅 [添加用户文档](https://helpx.adobe.com/enterprise/admin-guide.html/enterprise/using/manage-users-individually.ug.html#add-users).

   ![](assets/do-not-localize/access_control_4.png)

1. 执行与上述步骤相同的步骤，将其他用户添加到 **[!UICONTROL 产品配置文件]**. 然后，单击 **[!UICONTROL 保存]**.

随后，您的用户将收到一封重定向到您的实例的电子邮件。

有关用户管理的更多信息，请参阅 [Admin Console文档](https://helpx.adobe.com/enterprise/admin-guide.html/enterprise/using/manage-users-individually.ug.html).

在访问实例时，您的用户将看到特定视图，具体取决于中分配的权限 **[!UICONTROL 产品配置文件]**. 如果用户无权访问某个功能，则会显示以下消息：

`You don't have permission to access this feature. Permission needed: XX.`

## 编辑现有产品配置文件 {#edit-product-profile}

对于开箱即用或自定义 **[!UICONTROL 产品配置文件]**，您可以随时决定添加或删除权限。

在本例中，我们要添加 **[!UICONTROL 权限]** 与 **[!UICONTROL 历程]** 分配给历程查看器的用户的功能 **[!UICONTROL 产品配置文件]**. 随后，用户将能够发布历程。

请注意，如果您修改了现成或自定义的 **[!UICONTROL 产品配置文件]**，它将会影响分配给此的每个用户 **[!UICONTROL 产品配置文件]**.

1. 在 [!DNL Admin Console]，来自 **[!UICONTROL 产品]** 选项卡，选择 **[!UICONTROL Experience Cloud — 平台支持的应用程序]** 产品。

1. 选择历程查看器 **[!UICONTROL 产品配置文件]**.

1. 选择 **[!UICONTROL 权限]** 选项卡。

   此 **[!UICONTROL 权限]** 选项卡显示应用于 **[!UICONTROL Experience Cloud — 平台支持的应用程序]** 产品。

   ![](assets/do-not-localize/access_control_5.png)

1. 选择 **[!UICONTROL 历程]** 功能。

   ![](assets/do-not-localize/access_control_6.png)

1. 从 **[!UICONTROL 可用权限项]** 列表中，选择要分配给您的的权限 **[!UICONTROL 产品配置文件]** 单击加号(+)图标。

   在此，我们添加 **[!UICONTROL 发布历程]** 许可。

1. 如果需要，在 **[!UICONTROL 包含的权限项]**，单击旁边的X图标以删除对产品配置文件的权限。

1. 完成后，单击&#x200B;**[!UICONTROL 保存]**。

如果需要，您还可以创建具有特定权限的新产品配置文件。 有关更多信息，请参阅 [创建产品配置文件](#create-product-profile).

## 创建产品用户档案 {#create-product-profile}

[!DNL Journey Optimizer] 允许您创建自己的 **[!UICONTROL 产品配置文件]** 并为用户分配一组权限和沙箱。 替换为 **[!UICONTROL 产品配置文件]**&#x200B;中，您可以授权或拒绝对界面中特定功能或对象的访问。

有关如何创建和管理沙箱的详细信息，请参阅 [Adobe Experience Platform文档](https://experienceleague.adobe.com/docs/experience-platform/sandbox/ui/user-guide.html?lang=zh-Hans){target="_blank"}.

在本例中，我们将创建一个名为的产品配置文件 **历程只读** 其中，我们将授予历程功能的只读权限。 用户将只能访问和查看历程，而无法访问其他功能，例如 **[!DNL  Decision management]** 在 [!DNL Journey Optimizer].

创建我们的 **历程只读** **[!UICONTROL 产品配置文件]**：

1. 访问 [!DNL Admin Console].

1. 从 **[!UICONTROL 产品]** 选项卡，选择 **[!UICONTROL Experience Cloud — 平台支持的应用程序]** 产品。

1. 单击&#x200B;**[!UICONTROL 新建配置文件]**。

   ![](assets/do-not-localize/access_control_9.png)

1. 添加 **[!UICONTROL 产品配置文件名称]**， **[!UICONTROL 显示名称]** 和 **[!UICONTROL 描述]** （对于您的新存储库） **[!UICONTROL 产品配置文件]**.

   ![](assets/do-not-localize/access_control_10.png)

1. 在 **[!UICONTROL 通知]** 类别中，选择在添加用户或从此产品配置文件中删除用户时，是否会通过电子邮件通知用户。

1. 完成后，单击 **[!UICONTROL 保存]** 并选择您新创建的 **[!UICONTROL 产品配置文件]**.

1. 要添加用户访问不同功能的权限，请选择 **[!UICONTROL 权限]** 选项卡。

1. 在不同的功能之间选择，例如 **[!DNL Journeys]**， **[!DNL Segments]** 或 **[!DNL Decision management]** 可用位置 [!DNL Journey Optimizer] 列在左侧菜单中。

   在此处，我们选择 **[!UICONTROL 历程]** 功能。

   ![](assets/do-not-localize/access_control_11.png)

1. 从 **[!UICONTROL 可用权限项]** 列表中，选择要分配给您的的权限 **[!UICONTROL 产品配置文件]** 单击加号(+)图标。

   在此，我们选择 **[!DNL View journeys]** 和 **[!DNL View journeys event, data sources, actions]**.

   ![](assets/do-not-localize/access_control_12.png)

1. 选择 **[!UICONTROL 沙盒访问]** 能够选择要分配给您的环境的沙盒 **[!UICONTROL 产品配置文件]**.

   ![](assets/do-not-localize/access_control_13.png)

1. 下 **[!UICONTROL 可用权限项]**，单击加号(+)图标以将沙箱分配给您的配置文件。 [进一步了解沙盒](sandboxes.md)。

1. 完成后，单击&#x200B;**[!UICONTROL 保存]**。

您的 **[!UICONTROL 产品配置文件]** 现已创建并配置。 您现在需要将其分配给用户。

有关产品用户档案创建与管理的更多信息，请参阅 [Admin Console文档](https://helpx.adobe.com/enterprise/admin-guide.html/enterprise/using/manage-product-profiles.ug.html).
