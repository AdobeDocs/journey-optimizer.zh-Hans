---
title: 报表配置
description: 了解如何设置报表数据源
feature: Data Sources
topic: Administration
role: Admin
level: Intermediate
hide: true
hidefromtoc: true
exl-id: 327a0c45-0805-4f64-9bab-02d67276eff8
source-git-commit: 711fdf1dce0688d2e21d405a4e3e8777612b2f3b
workflow-type: tm+mt
source-wordcount: '573'
ht-degree: 4%

---

# 报表配置 {#reporting-configuration}

>[!CONTEXTUALHELP]
>id="ajo_admin_reporting_config"
>title="设置报表数据集"
>abstract="报表配置允许您定义与系统的连接，以检索要在报表中使用的其他自定义信息。 必须由技术用户执行。"

>[!CONTEXTUALHELP]
>id="ajo_admin_reporting_dataset"
>title="选择数据集"
>abstract="您只能选择一个事件类型数据集，该数据集必须至少包含一个受支持的字段组：experienceevent-web， experienceevent-application， experienceevent-commerce。"

报表数据源配置允许您定义与系统的连接，以检索将在您的报表中使用的其他信息。

>[!NOTE]
>
>数据源配置必须由技术用户执行。 <!--Rights?-->

对于此配置，您需要添加一个或多个包含要用于报表的属性的数据集。 为此，请执行以下步骤：

>[!CAUTION]
>
>必须先创建数据集，然后才能将数据集添加到报表配置。 了解 [Adobe Experience Platform文档](https://experienceleague.adobe.com/docs/experience-platform/catalog/datasets/user-guide.html?lang=en#create){target=&quot;_blank&quot;}。
>
>您只能添加事件类型数据集，该数据集必须至少包含一个受支持的 [字段组](https://experienceleague.adobe.com/docs/experience-platform/xdm/tutorials/create-schema-ui.html#field-group){target=&quot;_blank&quot;}: **experienceevent-web**, **experienceevent-application**, **experienceevent-commerce**.

<!--
➡️ [Discover this feature in video](#video)
-->

例如，如果您想要了解电子邮件促销活动对商务数据（如购买或订购）的影响，则需要使用 **experienceevent-commerce** 字段组。 同样，如果要报告移动设备交互情况，您需要使用 **experienceevent-application** 字段组。 <!--If you want to report on web interactions then you need to include the web field group.--> 您可以将这些字段组添加到一个或多个架构中，这些架构将用于一个数据集或不同数据集。

>[!NOTE]
>
>在 [XDM系统概述文档](https://experienceleague.adobe.com/docs/experience-platform/xdm/home.html?lang=zh-Hans){target=&quot;_blank&quot;}。

1. 从 **[!UICONTROL ADMINISTRATION]** 菜单，选择 **[!UICONTROL Configurations]**. 在  **[!UICONTROL Reporting]** ，单击 **[!UICONTROL Manage]**.

   ![](assets/reporting-config-menu.png)

   此时会显示已添加的数据集列表。

1. 在选项卡 **[!UICONTROL Dataset]** 中，单击 **[!UICONTROL Add dataset]**。

   ![](assets/reporting-config-add.png)

   >[!NOTE]
   >
   >如果您选择 **[!UICONTROL System dataset]** 选项卡中，将仅显示由系统创建的数据集。 您将无法添加其他数据集。

1. 从 **[!UICONTROL Dataset]** 下拉列表中，选择要用于报表的数据集。

   >[!CAUTION]
   >
   >您只能选择事件类型数据集，该数据集必须至少包含一个受支持的 [字段组](https://experienceleague.adobe.com/docs/experience-platform/xdm/tutorials/create-schema-ui.html#field-group){target=&quot;_blank&quot;}: **experienceevent-web**, **experienceevent-application**, **experienceevent-commerce**. 如果您选择的数据集与这些条件不匹配，您将无法保存所做更改。

   ![](assets/reporting-config-datasets.png)

   了解有关 [Adobe Experience Platform文档](https://experienceleague.adobe.com/docs/experience-platform/catalog/datasets/overview.html){target=&quot;_blank&quot;}。

1. 从 **[!UICONTROL Profile ID]** 下拉列表中，选择用于标识报表中每个配置文件的数据集字段属性。

   ![](assets/reporting-config-profile-id.png)

   >[!NOTE]
   >
   >只显示可用于报表的ID。

1. 的 **[!UICONTROL Use Primary ID namespace]** 选项。 如果选定 **[!UICONTROL Profile ID]** is **[!UICONTROL Identity Map]**，则可以禁用此选项，然后从显示的下拉列表中选择其他命名空间。

   ![](assets/reporting-config-namespace.png)

   了解有关 [Adobe Experience Platform文档](https://experienceleague.adobe.com/docs/experience-platform/identity/namespaces.html?lang=zh-Hans){target=&quot;_blank&quot;}。

1. 保存您所做的更改，以将选定的数据集添加到报表配置列表。

   >[!CAUTION]
   >
   >如果您选择了非事件类型的数据集，则将无法继续。

现在，在构建投放的报表时，您可以使用此数据集中的数据来检索其他自定义信息，并更好地优化报表。 [了解详情](content-experiment.md#objectives-global)

>[!NOTE]
>
>如果添加多个数据集，则所有数据集中的所有数据都将可用于报告。


<!--
## How-to video {#video}

Understand how to configure Experience Platform reporting data sources.

>[!VIDEO]()
-->
