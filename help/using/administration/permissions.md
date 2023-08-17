---
solution: Journey Optimizer
product: journey optimizer
title: 管理用户和角色
description: 了解如何管理用户和角色
exl-id: 85fd386a-45fa-4f9a-89d1-cecc0749b90d
feature: Access Management
topic: Administration
role: Admin
level: Intermediate
keywords: 产品、配置文件、沙盒
source-git-commit: 417eea2a52d4fb38ae96cf74f90658f87694be5a
workflow-type: tm+mt
source-wordcount: '786'
ht-degree: 6%

---

# 管理用户和角色 {#manage-permissions}

>[!IMPORTANT]
>
> 以下详述的每个程序只能通过 **[!UICONTROL 产品]** 或 **[!UICONTROL 系统]** 管理员。 有关详情，请参阅 [Admin console文档](https://helpx.adobe.com/enterprise/admin-guide.html/enterprise/using/admin-roles.ug.html).

**[!UICONTROL 角色]** 请参阅共享相同权限和沙盒的用户集合。 利用这些角色，可轻松管理组织中不同用户组的访问和权限。

使用 [!DNL Journey Optimizer] 产品，您能够在一系列预先存在的 **[!UICONTROL 角色]**，每个用户具有不同的权限级别，可分配给您的用户。 欲知关于 **[!UICONTROL 角色]**，请参阅此 [页面](ootb-product-profiles.md).

当用户属于 **[!UICONTROL 角色]**&#x200B;中，授予他们访问产品中包含的Adobe应用程序和服务的权限。

如果预先存在的角色不符合您组织的特定需求，您还可以创建自定义 **[!UICONTROL 角色]** 微调对界面中特定功能或对象的访问。 这样，您就可以确保每个用户只能访问高效执行任务所需的资源和工具。

## 分配角色 {#assigning-role}

您可以选择分配现成或自定义的 **[!UICONTROL 角色]** 发送给您的用户。

每个具有已分配权限的现成角色列表都可在以下网站中找到： [内置角色](ootb-product-profiles.md) 部分。

要分配 **[!UICONTROL 角色]**：

1. 在中为用户分配角色 [!DNL Permissions] 产品，导航到 **[!UICONTROL 角色]** 选项卡并选择所需的角色。

   ![](assets/do-not-localize/access_control_2.png)

1. 从 **[!UICONTROL 用户]** 选项卡，单击 **[!UICONTROL 添加用户]**.

   ![](assets/do-not-localize/access_control_3.png)

1. 键入用户名或电子邮件地址，或从列表中选择用户并单击 **[!UICONTROL 保存]**.

   如果用户之前未在 [!DNL Admin Console]，请参阅 [添加用户文档](https://helpx.adobe.com/enterprise/admin-guide.html/enterprise/using/manage-users-individually.ug.html#add-users).

   ![](assets/do-not-localize/access_control_4.png)

随后，您的用户将收到一封重定向到您的实例的电子邮件。

有关用户管理的详细信息，请参阅 [Admin Console文档](https://helpx.adobe.com/enterprise/admin-guide.html/enterprise/using/manage-users-individually.ug.html).

在访问实例时，您的用户将看到特定视图，具体取决于中分配的权限 **[!UICONTROL 角色]**. 如果用户无权访问某个功能，则会显示以下消息：

`You don't have permission to access this feature. Permission needed: XX.`

## 编辑现有角色 {#edit-product-profile}

对于现成或自定义 **[!UICONTROL 角色]**，您可以随时决定添加或删除权限。

在本例中，我们要添加 **[!UICONTROL 权限]** 与相关 **[!UICONTROL 历程]** 分配给用户查看器的历程的资源 **[!UICONTROL 角色]**. 随后，用户将能够发布历程。

请注意，如果您修改了现成或自定义的 **[!UICONTROL 角色]**，它将会影响分配给此的每位用户 **[!UICONTROL 角色]**.

1. 在中为用户分配角色 [!DNL Permissions] 产品，导航到 **[!UICONTROL 角色]** 选项卡并选择所需的角色，此处为历程查看器 **[!UICONTROL 角色]**.
   ![](assets/do-not-localize/access_control_5.png)

1. 来自您的 **[!UICONTROL 角色]** 仪表板，单击 **[!UICONTROL 编辑]**.

   ![](assets/do-not-localize/access_control_6.png)

1. 此 **[!UICONTROL 资源]** 菜单显示应用于 **[!UICONTROL Experience Cloud — 平台支持的应用程序]** 产品。 拖放资源以分配权限。

   从 **[!UICONTROL 历程]** resource下拉列表，我们在此处选择发布历程 **[!UICONTROL 权限]**.

   ![](assets/do-not-localize/access_control_14.png)

1. 如果需要，在 **[!UICONTROL 包含的权限项]**，单击将权限或资源移除到角色旁边的X图标。

1. 完成后，单击&#x200B;**[!UICONTROL 保存]**。

如果需要，您还可以创建具有特定权限的新角色。 有关详细信息，请参见 [创建新角色](#create-product-profile).

## 创建新角色 {#create-product-profile}

[!DNL Journey Optimizer] 允许您创建自己的 **[!UICONTROL 角色]** 并为用户分配一组权限和沙箱。 替换为 **[!UICONTROL 角色]**&#x200B;中，您可以授权或拒绝对界面中特定功能或对象的访问。

有关如何创建和管理沙箱的详细信息，请参阅 [Adobe Experience Platform文档](https://experienceleague.adobe.com/docs/experience-platform/sandbox/ui/user-guide.html?lang=zh-Hans){target="_blank"}.

在本例中，我们将创建一个名为的角色 **只读历程** 其中，我们将授予历程功能的只读权限。 用户将只能访问和查看历程，而无法访问其他功能，例如 **[!DNL  Decision management]** 在 [!DNL Journey Optimizer].

创建我们的 **只读历程** **[!UICONTROL 角色]**：

1. 在中为用户分配角色 [!DNL Permissions] 产品，导航到 **[!UICONTROL 角色]** 选项卡，然后单击 **[!UICONTROL 创建角色]**.

   ![](assets/do-not-localize/access_control_9.png)

1. 添加 **[!UICONTROL 名称]** 和 **[!UICONTROL 描述]** （对于您的新用户） **[!UICONTROL 角色]**. 然后，单击 **[!UICONTROL 确认]**.

   ![](assets/do-not-localize/access_control_10.png)

1. 从 **[!UICONTROL 沙盒]** 从“资源”下拉列表中，选择要分配给您的项目的沙盒 **[!UICONTROL 角色]**. [进一步了解沙盒](sandboxes.md)。

   ![](assets/do-not-localize/access_control_13.png)

1. 在不同的资源之间选择，例如 **[!DNL Journeys]**， **[!DNL Segments]** 或 **[!DNL Decision management]** 可用位置 [!DNL Journey Optimizer] 在左侧菜单中列出。

   在此处，我们选择 **[!UICONTROL 历程]** 资源。

   ![](assets/do-not-localize/access_control_11.png)

1. 从 **[!UICONTROL 历程]** 下拉列表中，选择要分配给您的的权限 **[!UICONTROL 角色]**.

   在此我们选择 **[!DNL View journeys]**， **[!DNL View journeys report]**  和 **[!DNL View journeys event, data sources, actions]**.

   ![](assets/do-not-localize/access_control_12.png)

1. 完成后，单击&#x200B;**[!UICONTROL 保存]**。

您的 **[!UICONTROL 角色]** 现已创建并配置。 您现在需要将其分配给用户。

有关角色创建与管理的详细信息，请参阅 [Admin Console文档](https://experienceleague.adobe.com/docs/experience-platform/access-control/abac/permissions-ui/roles.html?lang=zh-Hans).