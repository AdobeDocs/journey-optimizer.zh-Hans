---
solution: Journey Optimizer
product: journey optimizer
title: 配置数据源
description: 了解如何配置数据源
feature: Journeys, Data Sources
topic: Administration
role: Data Engineer, Data Architect, Admin
level: Intermediate, Experienced
keywords: 数据，源，配置，字段
exl-id: 9b0dcffb-f543-4066-850c-67ec33f74a31
source-git-commit: e45ec5f0e1bbcc73892f9cde5923627886f44ef6
workflow-type: tm+mt
source-wordcount: '570'
ht-degree: 15%

---

# 配置数据源 {#configure-data-source}

>[!NOTE]
>
>数据源配置操作必须始终由&#x200B;**技术用户**&#x200B;执行。

要配置数据源，请执行以下步骤：

1. 在“管理”菜单部分中，选择 **[!UICONTROL 配置]**. 在  **[!UICONTROL 数据源]** 部分，单击 **[!UICONTROL 管理]**. 将显示数据源列表。有关该界面的更多信息，请参阅[此页面](../start/user-interface.md)。

   ![](assets/journey18.png)

1. 然后，您可以将字段组添加到内置数据源（请参阅[此页面](../datasource/adobe-experience-platform-data-source.md)）或创建新的外部数据源（请参阅[此页面](../datasource/external-data-sources.md)）和关联的字段组（请参阅](../datasource/configure-data-sources.md#define-field-groups)此页面[）。

   ![](assets/journey23.png)

1. 单击&#x200B;**[!UICONTROL 保存]**。

   数据源现已配置完毕，可随时用于您的历程。

## 定义字段组 {#define-field-groups}

字段组是可从数据源检索并在历程中使用的一组字段。

对于每个数据源，您可以定义多个字段组。

例如，您可以创建一个字段组，其中包含电话号码、电子邮件、名字和个人资料的地址。 然后，您便能够在历程中使用此数据来创建条件。 例如，您可以决定仅在客户安装了移动应用程序时才发送推送通知。 如果为空，您可以发送电子邮件。

即使自动添加了默认名称，我们仍建议您为字段组提供一个名称。 事实上，字段组名称将对中的其他用户可见。 [!DNL Journey Optimizer]. 为字段组指定相关名称是一种最佳实践。

在历程中使用数据源字段时，系统将检索为该字段组定义的所有字段。 因此，最佳实践是仅选择历程所需的字段。 这将减少历程中的请求延迟，从而提高性能。 请注意，您可以稍后在字段组中轻松添加更多字段。

使用字段组的旅程数显示在 **[!UICONTROL 使用位置]** 字段。 您可以单击 **[!UICONTROL 查看历程]** 按钮以显示使用此字段组的旅程列表。

>[!NOTE]
>
>请注意，如果字段组没有字段，则不会显示在表达式编辑器中。

![](assets/journey3bis.png)

## 字段组生命周期 {#field-group-lifecycle}

您可以从未在任何草稿或实时历程中使用的字段组中添加或删除字段。

您可以添加，但无法从一个或多个草稿或实时历程中使用的字段组中删除字段。 这将避免中断历程。

要从一个或多个历程中使用的字段组中删除字段，请执行以下步骤。 让我们举一个名为“字段组A”的字段组为例。

1. 在字段组列表中，将光标置于“字段组A”上，然后单击 **[!UICONTROL 复制]** 图标（位于右侧）。 例如，将复制的字段组命名为“字段组B”。
1. 在“字段组B”中，删除您不再需要的字段。
1. 在“字段组A”中，检查在何处使用此字段组。 此信息显示在 **[!UICONTROL 使用位置]** 字段。
1. 打开所有使用“字段组A”的历程。
1. 创建每个历程的新版本。 使用“字段组A”编辑所有活动并选择“字段组B”。
1. 停止使用“字段组A”的旧版本历程。 然后，您应该没有使用“字段组A”的历程。
1. 删除“字段组A”，因为它已不再使用。
