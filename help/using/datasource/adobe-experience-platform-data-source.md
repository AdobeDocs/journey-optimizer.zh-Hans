---
title: 'Adobe Experience Platform 数据源 '
description: 了解如何配置Adobe Experience Platform数据源
translation-type: tm+mt
source-git-commit: 55b9e5d8ed259ec6ed7746e835691d7d6261a8a4
workflow-type: tm+mt
source-wordcount: '350'
ht-degree: 9%

---

# Adobe Experience Platform 数据源 {#concept_zrb_nqt_52b}

![](../assets/do-not-localize/badge.png)

Adobe Experience Platform数据源定义与实时客户用户档案服务的连接。 此数据源已内置并预配置。 无法删除。 此数据源旨在从实时客户用户档案服务中检索和使用数据（例如，检查进入旅程的人是否为女性）。 它允许您使用用户档案数据和体验事件数据。 有关实时客户用户档案服务的详细信息，请参阅此[页面](https://experienceleague.adobe.com/docs/experience-platform/profile/home.html)。

>[!NOTE]
>
>您可以检索不到一年前创建的1000个最新体验事件。

要允许与实时客户用户档案服务建立连接，我们必须使用一个键来识别一个人，以及一个将该键情境化的命名空间。 因此，仅当您的旅程开始包含一个键和一个命名空间的事件时，才能使用此数据源。 请参阅[此页](../building-journeys/journey.md)。

您可以编辑名为“ProfileFieldGroup”的预配置字段组，添加新字段组，并删除任何草稿或实时旅程中未使用的字段组。 请参阅[此页](../datasource/configure-data-sources.md#define-field-groups)。

以下是向内置数据源添加字段组的主要步骤。

1. 从数据源列表中，选择内置的Adobe Experience Platform数据源。

   这将打开屏幕右侧的数据源配置窗格。

   ![](../assets/journey23.png)

1. 单击&#x200B;**[!UICONTROL Add a New Field Group]**&#x200B;定义要检索的新系列字段。 请参阅[此页](../datasource/configure-data-sources.md#define-field-groups)。

   ![](../assets/journey24.png)

1. 从&#x200B;**[!UICONTROL Schema]**&#x200B;下拉菜单中选择模式。 此字段列表Adobe Experience Platform中提供的用户档案和体验事件模式。 模式创建不在[!DNL Journey Optimizer]中执行。 在Adobe Experience Platform演。
1. 选择要使用的字段。
1. 定义缓存持续时间。
1. 单击&#x200B;**[!UICONTROL Save]**。

将光标放在字段组的名称上时，您会在右侧看到两个图标。 它们允许您删除和重复字段组。 请注意，**[!UICONTROL Delete]**&#x200B;图标仅在字段组未用于任何实时或草稿旅程（显示在&#x200B;**[!UICONTROL Used in]**&#x200B;字段中的信息）时才可用。
