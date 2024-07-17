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
source-git-commit: 342b9210f79266cb11628dcdc411f90844a84e37
workflow-type: tm+mt
source-wordcount: '413'
ht-degree: 11%

---

# 对象级访问控制 {#object-level-access}

>[!CONTEXTUALHELP]
>id="ajo_olac_manage_access"
>title="对象级访问控制"
>abstract="为了保持对此对象的访问权限，请仅应用您有权限的标签。"

对象级访问控制(OLAC)允许您定义管理对所选对象的数据访问的授权：

* 历程
* Campaign
* 模板
* 片段
* 登陆页面
* 选件
* 静态优惠收藏集
* 优惠决策
* 渠道平面
* IP预热计划

其目的是保护敏感的数字资产，使其免遭未经授权的用户的侵害，从而进一步保护个人数据。

在Adobe Journey Optimizer中，OLAC允许您保护数据并授予特定对象的特定访问权限。

## 创建标签 {#create-assign-labels}

>[!IMPORTANT]
>
>要创建标签，您必须属于具有&#x200B;**[!UICONTROL 管理使用标签]**&#x200B;权限的角色。

**[!UICONTROL 标签]**&#x200B;允许您根据应用于该数据的使用策略对数据集和字段进行分类。 **[!UICONTROL 标签]**&#x200B;可以随时应用，从而灵活地选择管理数据的方式。

您可以在[!DNL Permissions]产品中创建标签。 有关详细信息，请参见[此页面](https://experienceleague.adobe.com/docs/experience-platform/access-control/abac/permissions-ui/labels.html)。

**[!UICONTROL 标签]**&#x200B;也可以直接在Journey Optimizer中创建：

1. 在Adobe Journey Optimizer对象中，单击新创建的&#x200B;**[!UICONTROL 营销活动]** **[!UICONTROL 管理访问权限]**&#x200B;按钮。

   ![](assets/olac_1.png)

1. 在&#x200B;**[!UICONTROL 管理访问权限]**&#x200B;窗口中，单击&#x200B;**[!UICONTROL 创建标签]**。

   ![](assets/olac_2.png)

1. 配置标签，您必须指定：
   * **[!UICONTROL 名称]**
   * **[!UICONTROL 友好名称]**
   * **[!UICONTROL 描述]**

   ![](assets/olac_3.png)

1. 单击&#x200B;**[!UICONTROL 创建]**&#x200B;以保存您的&#x200B;**[!UICONTROL 标签]**。

您新创建的&#x200B;**[!UICONTROL 标签]**&#x200B;现在在列表中可用。 如果需要，您可以在[!DNL Permissions]产品中修改它。

## 分配标签 {#assign-labels}

>[!IMPORTANT]
>
>要分配标签，您必须是具有管理权限（即[!DNL Manage journeys]、[!DNL Manage Campaigns]或[!DNL Manage decisions]）的角色的一部分。 如果没有此权限，**[!UICONTROL 管理访问权限]**&#x200B;按钮将灰显。

要将自定义或核心数据使用标签分配给您的Journey Optimizer对象，请执行以下操作：

1. 在Adobe Journey Optimizer对象中，单击新创建的&#x200B;**[!UICONTROL 营销活动]** **[!UICONTROL 管理访问权限]**&#x200B;按钮。

   ![](assets/olac_1.png)

1. 从&#x200B;**[!UICONTROL 管理访问权限]**&#x200B;窗口中，选择自定义或核心数据使用标签以管理对此对象的访问权限。

   有关核心数据使用标签的详细信息，请参阅[此页面](https://experienceleague.adobe.com/docs/experience-platform/data-governance/labels/reference.html)。

   ![](assets/olac_4.png)

1. 单击&#x200B;**[!UICONTROL 保存]**&#x200B;以应用此标签限制。

要访问此对象，用户需要在&#x200B;**[!UICONTROL 角色]**&#x200B;中包含特定的&#x200B;**[!UICONTROL 标签]**。
例如，具有C1标签的用户只能访问C1标签或未标签的对象。

有关如何将&#x200B;**[!UICONTROL 标签]**&#x200B;分配给&#x200B;**[!UICONTROL 角色]**&#x200B;的详细信息，请参阅[此页面](https://experienceleague.adobe.com/docs/experience-platform/access-control/abac/permissions-ui/permissions.html#manage-labels-for-a-role)。