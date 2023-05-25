---
solution: Journey Optimizer
product: journey optimizer
title: 为试验配置Journey Optimizer报表
description: 了解如何设置报表数据源
feature: Data Sources
topic: Administration
role: Admin
level: Intermediate
keywords: 配置，试验，报告，优化器
hide: true
hidefromtoc: true
exl-id: 327a0c45-0805-4f64-9bab-02d67276eff8
badge: label="Beta" type="Informative"
source-git-commit: 160e4ce03d3be975157c30fbe511875a85b00551
workflow-type: tm+mt
source-wordcount: '749'
ht-degree: 32%

---

# 为试验配置报表 {#reporting-configuration}

>[!CONTEXTUALHELP]
>id="ajo_admin_reporting_config"
>title="设置报表数据集"
>abstract="报告配置让您可以检索将在营销活动报告的“目标”选项卡中使用的其他指标。该操作必须由技术用户执行。"

>[!CONTEXTUALHELP]
>id="ajo_admin_reporting_dataset"
>title="选择数据集"
>abstract="您只能选择一个事件类型的数据集，该数据集必须至少包含一个支持的字段组：应用程序详细信息、商务详细信息、Web 详细信息。"

>[!BEGINSHADEBOX]

本文档包括以下内容：

* [内容体验入门](get-started-experiment.md)
* [创建内容试验](content-experiment.md)
* [了解统计计算](experiment-calculations.md)
* **[配置实验报表](reporting-configuration.md)**
* [实验报表中的统计计算](experiment-report-calculations.md)

>[!ENDSHADEBOX]

<!--The reporting data source configuration allows you to define a connection to a system in order to retrieve additional information that will be used in your reports.-->

通过报表数据源配置，可检索将用于 **[!UICONTROL 目标]** 选项卡中。 [了解详情](content-experiment.md#objectives-global)

>[!NOTE]
>
>报告配置必须由技术用户执行。 <!--Rights?-->

对于此配置，您需要添加一个或多个数据集，其中包含要用于报表的其他元素。 为此，请执行以下步骤 [以下](#add-datasets).

<!--
➡️ [Discover this feature in video](#video)
-->

## 先决条件


必须先创建该数据集，然后才能将数据集添加到报表配置。 了解如何在 [Adobe Experience Platform文档](https://experienceleague.adobe.com/docs/experience-platform/catalog/datasets/user-guide.html?lang=zh_Hans#create){target="_blank"}.

* 您只能添加事件类型数据集。

* 这些数据集必须至少包含以下项之一 [字段组](https://experienceleague.adobe.com/docs/experience-platform/xdm/tutorials/create-schema-ui.html?lang=zh_Hans#field-group){target="_blank"}： **应用程序详细信息**， **商业详细信息**， **Web详细信息**.

   >[!NOTE]
   >
   >当前仅支持这些字段组。

   例如，如果您想了解电子邮件营销活动对商业数据（如购买或订单）的影响，则需要使用创建体验事件数据集 **商业详细信息** 字段组。

   同样，如果要报告移动交互，则需要使用创建体验事件数据集 **应用程序详细信息** 字段组。

   将列出与每个字段组对应的量度 [此处](#objective-list).

* 您可以将这些字段组添加到一个或多个架构中，这些架构将用于一个或多个数据集。

>[!NOTE]
>
>在中了解有关XDM架构和字段组的更多信息 [XDM系统概述文档](https://experienceleague.adobe.com/docs/experience-platform/xdm/home.html?lang=zh_Hans){target="_blank"}.

## 对应于每个字段组的目标 {#objective-list}

下表显示了要将哪些指标添加到 **[!UICONTROL 目标]** 每个字段组的促销活动报告的选项卡。

| 字段组 | 目标 |
|--- |--- |
| 商业详细信息 | 总价<br>付款金额<br>（唯一）结账<br>（唯一）产品列表添加次数<br>（唯一）产品列表打开<br>（唯一）产品列表移除<br>（唯一）产品列表查看次数<br>（唯一）产品查看次数<br>（独特）购买<br>（唯一）保存以备后用<br>产品价格总计<br>产品数量 |
| 应用程序详细信息 | （独特）应用程序启动次数<br>应用程序首次启动次数<br>（唯一）应用程序安装次数<br>（唯一）应用程序升级 |
| Web详细信息 | （唯一）页面查看次数 |

## 添加数据集 {#add-datasets}

1. 从 **[!UICONTROL 管理]** 菜单，选择 **[!UICONTROL 配置]**. 在  **[!UICONTROL 报告]** 部分，单击 **[!UICONTROL 管理]**.

   ![](assets/reporting-config-menu.png)

   此时会显示已添加的数据集列表。

1. 从 **[!UICONTROL 数据集]** 选项卡，单击 **[!UICONTROL 添加数据集]**.

   ![](assets/reporting-config-add.png)

   >[!NOTE]
   >
   >如果您选择 **[!UICONTROL 系统数据集]** 选项卡，仅显示由系统创建的数据集。 您将无法添加其他数据集。

1. 从 **[!UICONTROL 数据集]** 从下拉列表中，选择要用于报表的数据集。

   >[!CAUTION]
   >
   >您只能选择事件类型数据集，该数据集必须至少包含一个受支持的 [字段组](https://experienceleague.adobe.com/docs/experience-platform/xdm/tutorials/create-schema-ui.html?lang=zh_Hans#field-group){target="_blank"}： **应用程序详细信息**， **商业详细信息**， **Web详细信息**. 如果选择的数据集与这些条件不匹配，您将无法保存所做的更改。

   ![](assets/reporting-config-datasets.png)

   了解更多有关数据集的信息，请参见 [Adobe Experience Platform文档](https://experienceleague.adobe.com/docs/experience-platform/catalog/datasets/overview.html?lang=zh_Hans){target="_blank"}.

1. 从 **[!UICONTROL 配置文件ID]** 从下拉列表中，选择用于标识报表中每个配置文件的数据集字段属性。

   ![](assets/reporting-config-profile-id.png)

   >[!NOTE]
   >
   >只显示可用于报表的 ID。

1. 此 **[!UICONTROL 使用主ID命名空间]** 选项默认处于启用状态。 如果选定了 **[!UICONTROL 配置文件ID]** 是 **[!UICONTROL 身份映射]**，您可以禁用此选项，然后从显示的下拉列表中选择其他命名空间。

   ![](assets/reporting-config-namespace.png)

   在中了解关于命名空间的更多信息 [Adobe Experience Platform文档](https://experienceleague.adobe.com/docs/experience-platform/identity/namespaces.html?lang=zh-Hans){target="_blank"}.

1. 保存您所做的更改，以将选定的数据集添加到报表配置列表。

   >[!CAUTION]
   >
   >如果您选择了非事件类型的数据集，则将无法继续。

在构建营销活动报表时，您现在可以看到与所添加数据集中使用的字段组对应的量度。 转到 **[!UICONTROL 目标]** 选项卡，然后选择您选择的量度以更好地优化报表。 [了解详情](content-experiment.md#objectives-global)

![](assets/reporting-config-objectives.png)

>[!NOTE]
>
>如果添加多个数据集，则所有数据集中的所有数据都将可用于报表。

<!--
## How-to video {#video}

Understand how to configure Experience Platform reporting data sources.

>[!VIDEO]()
-->
