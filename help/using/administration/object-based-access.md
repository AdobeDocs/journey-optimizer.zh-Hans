---
solution: Journey Optimizer
product: journey optimizer
title: 对象级访问控制
description: 了解对象级别访问控制
feature: Access Management
topic: Administration
role: Admin
level: Intermediate
exl-id: 02ccdd95-426c-4b61-9834-7f2dcd5abdbb
source-git-commit: 8d56e3060e78422b028ced17f415497789908ff9
workflow-type: tm+mt
source-wordcount: '383'
ht-degree: 0%

---

# 对象级访问控制 {#object-level-access}

>[!CONTEXTUALHELP]
>id="ajo_olac_manage_access"
>title="对象级访问控制"
>abstract="如果您应用了您无权访问的任何标签，则您对此对象的访问权限将被撤消。"

>[!IMPORTANT]
>
>对象级别访问控制的使用当前仅限于选定的客户，并且将在未来版本中部署到所有环境。

对象级别访问控制(OLAC)允许您定义用于管理对所选对象的数据访问权限的授权：

* 历程
* Campaign
* 登陆页面
* 选件
* 选件集合
* Offer Decisioning

其目的是保护敏感数字资产免受未经授权用户的侵害，从而进一步保护个人数据。

在Adobe Journey Optimizer中，OLAC允许您保护数据并授予对特定对象的特定访问权限。

## 创建标签 {#create-assign-labels}

>[!IMPORTANT]
>
>要创建标签，您必须是 **[!UICONTROL Manage usage labels]** 权限。

**[!UICONTROL Labels]** 允许您根据应用于该数据的使用策略对数据集和字段进行分类。 **[!UICONTROL Labels]** 可以随时应用，从而在选择如何管理数据方面提供了灵活性。

您可以在 [!DNL Permissions] 产品。 有关更多信息，请参阅 [本页](https://experienceleague.adobe.com/docs/experience-platform/access-control/abac/permissions-ui/labels.html).

**[!UICONTROL Labels]** 也可以直接在Journey Optimizer中创建：

1. 从Adobe Journey Optimizer对象中，此处是新创建的 **[!UICONTROL Campaign]**，请单击 **[!UICONTROL Manage access]** 按钮。

   ![](assets/olac_1.png)

1. 从 **[!UICONTROL Manage access]** 窗口，单击 **[!UICONTROL Create label]**.

   ![](assets/olac_2.png)

1. 配置标签时，必须指定：
   * **[!UICONTROL Name]**
   * **[!UICONTROL Friendly name]**
   * **[!UICONTROL Description]**

   ![](assets/olac_3.png)

1. 单击 **[!UICONTROL Create]** 保存 **[!UICONTROL Label]**.

您新创建的 **[!UICONTROL Label]** 现在可在列表中使用。 如果需要，您可以在 [!DNL Permissions] 产品。

## 分配标签 {#assign-labels}

>[!IMPORTANT]
>
>要能够分配标签，您必须是具有“管理”权限的角色的一部分，例如， [!DNL Manage journeys], [!DNL Manage Campaigns] 或 [!DNL Manage decisions]. 如果没有这项许可， **[!UICONTROL Manage access]** 按钮将灰显。

要将自定义或核心数据使用标签分配给Journey Optimizer对象，请执行以下操作：

1. 从Adobe Journey Optimizer对象中，此处是新创建的 **[!UICONTROL Campaign]**，请单击 **[!UICONTROL Manage access]** 按钮。

   ![](assets/olac_1.png)

1. 从 **[!UICONTROL Manage access]** 窗口中，选择自定义或核心数据使用标签以管理对此对象的访问。

   有关核心数据使用标签的更多信息，请参阅 [本页](https://experienceleague.adobe.com/docs/experience-platform/data-governance/labels/reference.html).

   ![](assets/olac_4.png)

1. 单击 **[!UICONTROL Save]** 以应用此标签限制。

要访问此对象，用户需要具有 **[!UICONTROL Label]** 包含在 **[!UICONTROL Roles]**.
例如，具有C1标签的用户将只能访问C1标记或未标记的对象。

有关如何分配的详细信息 **[!UICONTROL Label]** 至 **[!UICONTROL Role]**，请参阅 [本页](https://experienceleague.adobe.com/docs/experience-platform/access-control/abac/permissions-ui/permissions.html?lang=en#manage-labels-for-a-role).
