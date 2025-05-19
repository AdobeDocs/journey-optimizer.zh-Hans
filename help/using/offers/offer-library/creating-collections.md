---
title: 创建收藏集
description: 了解如何使用收藏集整理优惠
feature: Decision Management, Collections
topic: Integrations
role: User
level: Intermediate
exl-id: 0c8808e3-9148-4a33-9fd5-9218e02c2dfd
source-git-commit: b6fd60b23b1a744ceb80a97fb092065b36847a41
workflow-type: tm+mt
source-wordcount: '462'
ht-degree: 31%

---

# 创建收藏集 {#create-collections}

>[!CONTEXTUALHELP]
>id="ajo_decisioning_decision_collection"
>title="关于优惠收藏集"
>abstract="借助优惠收藏集，可通过将产品建议重新分组为所选的类别而整理您的产品建议。"

>[!CONTEXTUALHELP]
>id="ajo_decisioning_collection_dynamic"
>title="动态集合"
>abstract="使用集合限定符来动态地限定集合中的产品建议。"

>[!CONTEXTUALHELP]
>id="ajo_decisioning_collection_static"
>title="静态集合"
>abstract="使用状态、集合限定符、日期和渠道等条件手动选择产品建议并进行分组。"

>[!CONTEXTUALHELP]
>id="ajo_decisioning_collection_static_select"
>title="静态集合预览"
>abstract="静态集合是通过手动选择要纳入集合中的单个产品建议来生成的。只能通过手动添加更多产品建议来更新集合。"

>[!CONTEXTUALHELP]
>id="ajo_decisioning_collection_dynamic_select"
>title="动态集合预览"
>abstract="动态集合根据集合限定符来收集产品建议。这些集合会自动更新。例如，如果使用“体育”集合限定符创建了新的产品建议，则它会自动添加到相应的集合中。"

收藏集允许您通过将优惠重组到您选择的类别来整理优惠。 例如，您可以创建一个“sport”收藏集，其中仅包含与体育相关的选件。

➡️ [通过观看视频了解此功能](#video)

可在&#x200B;**[!UICONTROL 优惠]**&#x200B;菜单中访问优惠收藏集列表。

![](../assets/collections_list.png)

您可以创建两种类型的收藏集：

* **动态集合**&#x200B;是基于集合限定符（以前称为“标记”）的优惠集合。 这些集合会自动更新。例如，如果使用选定的收藏集限定符创建新选件，则会自动将其添加到收藏集。

* **静态收藏集**&#x200B;是通过手动选择要包含在收藏集中的单个优惠而构建的收藏集。 只能通过手动添加更多产品建议来更新集合。

要创建收藏集，请执行以下步骤：

1. 转到&#x200B;**[!UICONTROL 收藏集]**&#x200B;选项卡，然后单击&#x200B;**[!UICONTROL 创建收藏集]**。

1. 指定要创建的集合的名称和类型。

   ![](../assets/collection_create.png)

1. 要创建动态集合，请使用左窗格选择要添加到集合中的优惠的集合限定符，然后单击&#x200B;**[!UICONTROL 保存]**。 具有选定收藏集限定符的所有优惠都将保存在收藏集中。

   有关集合限定符创建的详细信息，请参阅[创建集合限定符](../offer-library/creating-tags.md)。

   ![](../assets/dynamic_collection.png)

1. 要创建静态收藏集，请使用左窗格筛选优惠列表（状态、收藏集限定符、日期、渠道、内容类型），然后选择要添加到收藏集的优惠。

   ![](../assets/static_collection.png)

   >[!NOTE]
   >
   >静态收藏集不会自动更新。 要将选件添加到静态收藏集，您需要编辑它并手动添加它们。

1. 要将自定义或核心数据使用标签分配给静态集合，请选择&#x200B;**[!UICONTROL 管理访问权限]**。 [了解有关对象级访问控制(OLAC)的更多信息](../../administration/object-based-access.md)

   >[!NOTE]
   >
   >OLAC不适用于动态收藏集。 它必须在选件级别进行管理。 因此，如果您无权访问任何这些选件，则可能无法在动态收藏集中看到任何选件。

1. 创建收藏集后，该收藏集将显示在列表中。 您可以选择它来编辑或删除它。

   ![](../assets/collection_created.png)

## 操作说明视频 {#video}

>[!VIDEO](https://video.tv.adobe.com/v/346685?quality=12&captions=chi_hans)


