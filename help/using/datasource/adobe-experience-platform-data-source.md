---
solution: Journey Optimizer
product: journey optimizer
title: Adobe Experience Platform 数据源
description: 了解如何配置Adobe Experience Platform数据源
feature: Journeys, Data Sources
topic: Administration
role: Data Engineer, Data Architect, Admin
level: Intermediate, Experienced
keywords: 内置，源，数据，平台，集成
exl-id: 9083e355-15e3-4d1f-91ae-03095e08ad16
source-git-commit: 07b1f9b885574bb6418310a71c3060fa67f6cac3
workflow-type: tm+mt
source-wordcount: '421'
ht-degree: 31%

---

# Adobe Experience Platform 数据源 {#adobe-experience-platform-data-source}

>[!CONTEXTUALHELP]
>id="ajo_journey_data_source_built_in"
>title="Adobe Experience Platform 数据源"
>abstract="Adobe Experience Platform 数据源定义与 Adobe 实时客户配置文件的连接。此数据源是内置数据源，经过预先配置，无法删除。它设计用于从实时客户配置文件服务中检索并使用数据（例如，检查进入历程的人是否为女性）。该数据源允许您使用配置文件数据和体验事件数据。"

Adobe Experience Platform 数据源定义与 Adobe 实时客户配置文件的连接。此数据源是内置数据源，经过预先配置，无法删除。此数据源旨在检索和使用来自Real-time Customer Profile Service的数据（例如，检查进入历程的人员是否为女性）。 该数据源允许您使用用户档案数据和体验事件数据。有关Adobe实时客户个人资料的更多信息，请参阅 [Adobe Experience Platform文档](https://experienceleague.adobe.com/docs/experience-platform/profile/home.html?lang=zh-Hans){target="_blank"}.


要允许与Real-time Customer Profile Service的连接，我们必须使用键来识别人员，并使用命名空间来将键进行上下文化。 因此，仅当历程以包含键和命名空间的事件开始时，才能使用此数据源。 [了解详情](../building-journeys/journey.md)。

您可以编辑名为“ProfileFieldGroup”的预配置字段组、添加新字段组并删除任何草稿或实时历程中未使用的字段组。 [了解详情](../datasource/configure-data-sources.md#define-field-groups)。


>[!NOTE]
>
>您可以检索在不到一年前创建的1000个最新体验事件。

以下是向内置数据源添加字段组的主要步骤。

1. 从数据源列表中，选择内置的Adobe Experience Platform数据源。

   这将打开屏幕右侧的数据源配置窗格。

   ![](assets/journey23.png)

1. 单击 **[!UICONTROL 添加新字段组]** 以定义要检索的一系列新字段。 [了解详情](../datasource/configure-data-sources.md#define-field-groups)。

   ![](assets/journey24.png)

1. 从中选择架构 **[!UICONTROL 架构]** 下拉菜单。 此字段列出Adobe Experience Platform中可用的配置文件和Experience Events架构。 架构创建不在中执行 [!DNL Journey Optimizer]. 它在Adobe Experience Platform中执行。
1. 选择要使用的字段。
1. 单击 **[!UICONTROL 保存]**.

将光标放在字段组的名称上时，您会在右侧看到两个图标。 它们允许您删除和复制字段组。 请注意 **[!UICONTROL 删除]** 仅当字段组未在任何实时或草稿历程中使用时，图标才可用(信息显示在 **[!UICONTROL 使用位置]** 字段)。
