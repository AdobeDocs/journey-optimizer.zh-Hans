---
solution: Journey Optimizer
product: journey optimizer
title: 用户管理概述
description: 了解如何定义和管理权限
feature: Access Management
topic: Administration
role: Admin, Architect
level: Intermediate
keywords: 权限，权限，限制，访问，沙盒
exl-id: b8e266b1-d8eb-4c77-9341-9761b82609b0
source-git-commit: fbcddcf10974f16eb6885ebb38b7be41f2e53639
workflow-type: tm+mt
source-wordcount: '437'
ht-degree: 3%

---

# 访问控制入门 {#permissions-overview}

[!DNL Journey Optimizer]允许您定义和管理分配给不同用户的权限。 权限是授权或拒绝访问产品内特性和功能的一组权限和限制。

[!DNL Journey Optimizer]的访问控制是通过Adobe Experience Cloud中的&#x200B;**权限**&#x200B;提供的。 此功能利用角色和策略，将用户与权限和沙盒关联起来。

要配置Journey Optimizer的访问控制，您必须拥有组织的系统或产品管理员权限。 可以授予或撤销权限的最低角色是产品管理员。 可以管理权限的其他管理员角色是系统管理员（无限制）。 有关详细信息，请参阅有关管理角色的[Adobe帮助中心文章](https://helpx.adobe.com/cn/enterprise/using/admin-roles.html){target="_blank"}。

<!-- A high-level workflow for gaining and assigning access permissions can be summarized as follows:

* After licensing [!DNL Journey Optimizer], an email is sent to the administrator specified during licensing.
* The administrator logs in to Adobe Admin Console and selects [!DNL Journey Optimizer] from the list of products on the overview page.
* To grant access to [!DNL Journey Optimizer], it is recommended that the administrator add users to the default product profile
* In Experience Platform Permissions, the administrator can create new roles or edit the permissions and users for any existing roles.
* When creating or editing a role, the administrator adds users to the role using the users tab, and grants permissions to these users (such as "Read Datasets" or "Manage Schemas") by editing the role's permissions. Similarly, the administrator can assign access to sandboxes using the same editing option.
* When users log in to the Journey Optimizer user interface, their access to capabilities is driven by the permissions that have been granted to them from the previous step. For example, if a user does not have the View Datasets permission, the Datasets tab in the side menu will not be visible to that user.-->


[!DNL Journey Optimizer]中的用户管理基于以下关键概念：

* **[!UICONTROL 角色]**：角色是指共享相同权限和沙盒的用户集合。 利用这些角色，可轻松管理组织中不同用户组的访问和权限。 角色附带一组统一权限，允许用户访问界面中的特定功能或对象。
通过[!DNL Journey Optimizer]，您可以从预先存在的&#x200B;**[!UICONTROL 角色]**&#x200B;范围中进行选择，每个角色都具有各种级别的权限，以便分配给您的用户。 详细了解[此页面](ootb-product-profiles.md)上可用的&#x200B;**内置角色**。

* **[!UICONTROL 权限]**：权限是单一权限，允许您定义分配给&#x200B;**[!UICONTROL 角色]**&#x200B;的授权。 每个权限都集中在资源(例如历程或优惠)下，代表[!DNL Journey Optimizer]中的不同功能或对象。 在[权限级别](high-low-permissions.md)部分了解详情。

  ![](assets/do-not-localize/permissions_2.png)

* **[!UICONTROL 沙盒]**：虚拟沙盒将实例分区为单独的独立虚拟环境。 沙盒通过权限中的角色进行分配。 了解有关[使用沙盒](sandboxes.md)的更多信息。

* **基于对象的访问控制**：用于限制对象访问权限的标签。 此方法可保护敏感的数字资产免受未经授权用户的侵害，并确保进一步保护个人数据。 了解有关[基于对象的访问管理](object-based-access.md)的详细信息。

* **基于属性的访问控制**：管理特定团队或用户组的数据访问权限的授权。 基于属性的访问控制使管理员能够根据属性控制对特定对象和/或权能的访问。 属性可以是添加到对象的元数据，例如添加到架构字段或区段的标签。 管理员定义包括管理用户访问权限的属性的访问策略。 了解有关[基于属性的访问管理](attribute-based-access.md)的详细信息。


## 让我们深入探究

现在，您已了解&#x200B;**[!DNL Journey Optimizer]**&#x200B;中的访问控制概念，接下来该深入了解这些文档部分以开始配置权限。


<table style="table-layout:fixed"><tr style="border: 0;">
<td>
<a href="permissions.md">
<img alt="权限" src="assets/do-not-localize/role.jpg">
</a>
<div>
<a href="permissions.md"><strong>授予访问权限</strong></a>
</div>
<p>
</td>
<td>
<a href="ootb-permissions.md">
<img alt="内置权限" src="assets/do-not-localize/select.jpg">
</a>
<div>
<a href="ootb-permissions.md"><strong>内置权限</strong></a>
</div>
<p>
</td>
<td>
<a href="sandboxes.md">
<img alt="管理沙盒" src="assets/do-not-localize/sandboxes.jpg">
</a>
<div>
<a href="sandboxes.md"><strong>管理沙盒</strong></a>
</div>
<p></td>
<td>
<a href="attribute-based-access.md">
<img alt="基于属性的访问控制" src="assets/do-not-localize/data-access.jpeg">
</a>
<div>
<a href="attribute-based-access.md"><strong>基于属性的访问控制</strong></a>
</div>
<p>
</td>
</tr></table>