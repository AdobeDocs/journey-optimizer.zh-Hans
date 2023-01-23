---
solution: Journey Optimizer
product: journey optimizer
title: Adobe Experience Platform 数据源
description: 了解如何配置Adobe Experience Platform数据源
feature: Data Sources
topic: Administration
role: Admin, Developer
level: Intermediate
keywords: 内置，源，数据，平台，集成
exl-id: 9083e355-15e3-4d1f-91ae-03095e08ad16
source-git-commit: b8065a68ed73102cb2c9da2c2d2675ce8e5fbaad
workflow-type: tm+mt
source-wordcount: '425'
ht-degree: 14%

---

# Adobe Experience Platform 数据源 {#adobe-experience-platform-data-source}

>[!CONTEXTUALHELP]
>id="ajo_journey_data_source_built_in"
>title="Adobe Experience Platform 数据源"
>abstract="Adobe Experience Platform数据源定义与Adobe实时客户资料的连接。 此数据源已内置并预配置，无法删除。 它旨在从实时客户资料服务中检索和使用数据（例如，检查进入旅程的人员是否为女性）。 该数据源允许您使用用户档案数据和体验事件数据。"

Adobe Experience Platform数据源定义与Adobe实时客户资料的连接。 此数据源已内置并预配置，无法删除。 此数据源旨在从实时客户资料服务中检索和使用数据（例如，检查进入旅程的人员是否为女性）。 该数据源允许您使用用户档案数据和体验事件数据。有关Adobe实时客户资料的更多信息，请参阅 [Adobe Experience Platform文档](https://experienceleague.adobe.com/docs/experience-platform/profile/home.html?lang=zh-Hans){target="_blank"}.


要允许连接到实时客户资料服务，我们必须使用键来标识人员，以及将键关联到的命名空间。 因此，仅当您的历程以包含键和命名空间的事件开头时，才能使用此数据源。 [了解详情](../building-journeys/journey.md)。

您可以编辑名为“ProfileFieldGroup”的预配置字段组，添加新字段组并删除未在任何草稿或实时历程中使用的字段组。 [了解详情](../datasource/configure-data-sources.md#define-field-groups)。


>[!NOTE]
>
>您可以检索不到一年前创建的1000个最新体验事件。

以下是向内置数据源添加字段组的主要步骤。

1. 从数据源列表中，选择内置的Adobe Experience Platform数据源。

   这将打开屏幕右侧的数据源配置窗格。

   ![](assets/journey23.png)

1. 单击 **[!UICONTROL 添加新字段组]** 定义要检索的一系列新字段。 [了解详情](../datasource/configure-data-sources.md#define-field-groups)。

   ![](assets/journey24.png)

1. 从 **[!UICONTROL 架构]** 下拉菜单。 此字段列出了Adobe Experience Platform中提供的配置文件和体验事件架构。 未在中执行架构创建 [!DNL Journey Optimizer]. 在Adobe Experience Platform演。
1. 选择要使用的字段。
1. 单击 **[!UICONTROL 保存]**.

将光标放在字段组的名称上时，您将在右侧看到两个图标。 利用字段组，可删除和复制字段组。 请注意， **[!UICONTROL 删除]** 图标仅在字段组未用于任何实时或草稿历程时可用(信息显示在 **[!UICONTROL 在]** 字段。
