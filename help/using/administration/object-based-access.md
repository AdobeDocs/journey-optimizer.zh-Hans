---
solution: Journey Optimizer
product: journey optimizer
title: 对象级访问控制
description: 了解对象级访问控制，它允许您定义管理对所选对象的数据访问的授权
feature: Access Management
topic: Administration
role: Admin, Developer, Architect
level: Experienced
keywords: 对象，级别，访问，控制，标签， olac，授权
exl-id: 02ccdd95-426c-4b61-9834-7f2dcd5abdbb
source-git-commit: 1a2c6e97fcd30245cff1bf08fd5771ce8bc84ddc
workflow-type: tm+mt
source-wordcount: '480'
ht-degree: 13%

---

# 对象级访问控制 {#object-level-access}

>[!CONTEXTUALHELP]
>id="ajo_olac_manage_access"
>title="访问管理标签"
>abstract="您可以根据访问标签限制对对象的访问。此方法可保护敏感的数字资产免受未经授权用户的侵害，并确保进一步保护个人数据。 **确保仅选择您有权限的标签。**"

您可以根据访问标签限制对对象的访问。此方法可保护敏感的数字资产免受未经授权用户的侵害，并确保进一步保护个人数据。

对象级访问控制(OLAC)功能允许您定义用于管理所选对象的数据访问的授权：

* 历程
* Campaign
* 模板
* 片段
* 登陆页面
* 产品建议
* 静态优惠收藏集
* 优惠决策
* 渠道配置
* IP预热计划


## 先决条件 {#prereq-labels}

要[创建标签](#create-labels)，您必须属于具有&#x200B;**[!UICONTROL 管理使用标签]**&#x200B;权限的角色。

要能够[分配标签](#assign-labels)，您必须属于具有&#x200B;**管理**&#x200B;权限的角色，即[!DNL Manage journeys]、[!DNL Manage Campaigns]或[!DNL Manage decisions]。 如果没有此权限，**[!UICONTROL 管理访问权限]**&#x200B;按钮将灰显。

可在[此部分](../administration/permissions.md)中详细了解权限。

## 创建标签 {#create-labels}

**[!UICONTROL 标签]**&#x200B;允许您根据应用于该数据的使用策略对数据集和字段进行分类。 **[!UICONTROL 标签]**&#x200B;可以随时应用，从而灵活地管理数据。

使用标签为用户提供访问权限，并强制实施数据治理和同意策略。 这些治理标签可能会影响下游消费。

您可以在[!DNL Permissions]产品中创建标签。 有关详细信息，请参阅[Adobe Experience Platform文档](https://experienceleague.adobe.com/docs/experience-platform/access-control/abac/permissions-ui/labels.html?lang=zh-Hans){target="_blank"}。

您也可以直接在Journey Optimizer中创建&#x200B;**[!UICONTROL 标签]**。 要创建标签，请执行以下步骤：

1. 从Adobe Journey Optimizer对象（例如新创建的&#x200B;**[!UICONTROL 营销活动]**）中，单击&#x200B;**[!UICONTROL 管理访问权限]**&#x200B;按钮。

   Adobe Journey Optimizer中的![管理访问权限按钮](assets/olac_1.png)

1. 在&#x200B;**[!UICONTROL 管理访问权限]**&#x200B;窗口中，单击&#x200B;**[!UICONTROL 创建标签]**。

   ![](assets/olac_2.png)

1. 配置您的标签。 您必须指定：

   * **[!UICONTROL 名称]**
   * **[!UICONTROL 友好名称]**
   * **[!UICONTROL 描述]**

   ![标签配置字段](assets/olac_3.png)

1. 单击&#x200B;**[!UICONTROL 创建]**&#x200B;以保存您的&#x200B;**[!UICONTROL 标签]**。

您新创建的&#x200B;**[!UICONTROL 标签]**&#x200B;现在在列表中可用。 如果需要，您可以在[!DNL Permissions]产品中修改它。

## 分配标签 {#assign-labels}

要将自定义或核心数据使用标签分配给您的Journey Optimizer对象，请执行以下操作：

1. 从Adobe Journey Optimizer对象（例如新创建的&#x200B;**[!UICONTROL 营销活动]**）中，单击&#x200B;**[!UICONTROL 管理访问权限]**&#x200B;按钮。

   Adobe Journey Optimizer中的![管理访问权限按钮](assets/olac_1.png)

1. 从&#x200B;**[!UICONTROL 管理访问权限]**&#x200B;窗口中，选择自定义或核心数据使用标签以管理对此对象的访问权限。

   有关核心数据使用标签的详细信息，请参阅[此页面](https://experienceleague.adobe.com/docs/experience-platform/data-governance/labels/reference.html?lang=zh-Hans){target="_blank"}。

   ![](assets/olac_4.png)

1. 单击&#x200B;**[!UICONTROL 保存]**&#x200B;以应用此标签限制。

要访问此对象，用户必须在其&#x200B;**[!UICONTROL 角色]**&#x200B;中包含特定的&#x200B;**[!UICONTROL 标签]**。 例如，具有C1标签的用户将只能访问带有C1标签或未标签的对象。

有关如何将&#x200B;**[!UICONTROL 标签]**&#x200B;分配给&#x200B;**[!UICONTROL 角色]**&#x200B;的详细信息，请参阅[此页面](https://experienceleague.adobe.com/docs/experience-platform/access-control/abac/permissions-ui/permissions.html?lang=zh-Hans#manage-labels-for-a-role){target="_blank"}。
