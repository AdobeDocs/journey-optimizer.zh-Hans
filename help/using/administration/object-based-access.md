---
solution: Journey Optimizer
product: journey optimizer
title: 对象级访问控制
description: 了解对象级访问控制，该访问控制允许您定义管理对所选对象的数据访问的授权
feature: Access Management
topic: Administration
role: Admin, Developer, Architect
level: Experienced
keywords: 对象，级别，访问，控制，标签， olac，授权
exl-id: 02ccdd95-426c-4b61-9834-7f2dcd5abdbb
source-git-commit: a2a5c081ee9a8ab04bf4c7b97097c0121ef8e4f8
workflow-type: tm+mt
source-wordcount: '459'
ht-degree: 14%

---

# 对象级访问控制 {#object-level-access}

>[!CONTEXTUALHELP]
>id="ajo_olac_manage_access"
>title="对象级访问控制"
>abstract="如果应用了任何您无权访问的标签，那么您对此对象的访问权限将被撤销。"

>[!IMPORTANT]
>
>对象级访问控制的使用当前仅限于选定客户，将在未来版本中部署到所有环境。

对象级访问控制(OLAC)允许您定义管理对所选对象的数据访问的授权：

* 历程
* Campaign
* 片段
* 登陆页面
* 选件
* 优惠收藏集
* offer decisioning
* 模板

其目的是保护敏感的数字资产免受未经授权用户的侵害，从而进一步保护个人数据。

在Adobe Journey Optimizer中，OLAC允许您保护数据并授予对特定对象的特定访问权限。

## 创建标签 {#create-assign-labels}

>[!IMPORTANT]
>
>要能够创建标签，您必须属于具有以下特征的角色： **[!UICONTROL 管理使用标签]** 许可。

**[!UICONTROL 通过标签，可根据适用于数据的使用策略将数据集和字段分类。]****[!UICONTROL 标签]** 可以随时应用，从而灵活地选择管理数据的方式。

您可以在中创建标签 [!DNL Permissions] 产品。 有关详细信息，请参见[此页面](https://experienceleague.adobe.com/docs/experience-platform/access-control/abac/permissions-ui/labels.html)。

**[!UICONTROL 标签]** 也可以直接在Journey Optimizer中创建：

1. 从Adobe Journey Optimizer对象，此处为新创建的 **[!UICONTROL Campaign]**，单击 **[!UICONTROL 管理访问权限]** 按钮。

   ![](assets/olac_1.png)

1. 从 **[!UICONTROL 管理访问权限]** 窗口，单击 **[!UICONTROL 创建标签]**.

   ![](assets/olac_2.png)

1. 配置标签，必须指定：
   * **[!UICONTROL 名称]**
   * **[!UICONTROL 友好名称]**
   * **[!UICONTROL 描述]**

   ![](assets/olac_3.png)

1. 单击 **[!UICONTROL 创建]** 保存您的 **[!UICONTROL 标签]**.

您新创建的 **[!UICONTROL 标签]** 现在可在列表中找到。 如果需要，您可以在以下位置对其进行修改： [!DNL Permissions] 产品。

## 分配标签 {#assign-labels}

>[!IMPORTANT]
>
>要分配标签，您必须是具有管理权限的角色的一部分，即 [!DNL Manage journeys]， [!DNL Manage Campaigns] 或 [!DNL Manage decisions]. 如果没有此权限， **[!UICONTROL 管理访问权限]** 按钮将灰显。

要将自定义或核心数据使用标签分配给您的Journey Optimizer对象，请执行以下操作：

1. 从Adobe Journey Optimizer对象，此处为新创建的 **[!UICONTROL Campaign]**，单击 **[!UICONTROL 管理访问权限]** 按钮。

   ![](assets/olac_1.png)

1. 从 **[!UICONTROL 管理访问权限]** 窗口中，选择自定义或核心数据使用标签以管理对此对象的访问。

   有关核心数据使用标签的更多信息，请参阅 [此页面](https://experienceleague.adobe.com/docs/experience-platform/data-governance/labels/reference.html).

   ![](assets/olac_4.png)

1. 单击 **[!UICONTROL 保存]** 以应用此标签限制。

要访问此对象，用户需要具有 **[!UICONTROL 标签]** 包含在其中 **[!UICONTROL 角色]**.
例如，具有C1标签的用户只能访问C1标签或未标签的对象。

有关如何分配的详细信息 **[!UICONTROL 标签]** 到 **[!UICONTROL 角色]**，请参阅 [此页面](https://experienceleague.adobe.com/docs/experience-platform/access-control/abac/permissions-ui/permissions.html#manage-labels-for-a-role).
