---
title: 收藏集
description: 了解如何使用收藏集
feature: Experience Decisioning
topic: Integrations
role: User
level: Intermediate
hide: true
hidefromtoc: true
badge: label="Beta 版"
exl-id: 099d1439-34f7-47fe-9181-0e9ce2032a01
source-git-commit: f92e3882d3b5e515e672a4af8e787813d4d939ce
workflow-type: tm+mt
source-wordcount: '393'
ht-degree: 12%

---

# 收藏集 {#collections}

>[!CONTEXTUALHELP]
>id="ajo_exd_item_collections"
>title="创建收藏集"
>abstract="收藏集允许您根据自己的偏好对决策项目进行分类和分组。 这些类别是通过构建利用决策项目属性的规则创建的。"

>[!CONTEXTUALHELP]
>id="ajo_exd_item_collection_rules"
>title="定义收藏集的规则"
>abstract="添加一个或多个规则以确定要包含在收藏集中的项目。 选择要用作条件的物料属性。 选择所需的运算符并输入要过滤的值。 根据需要添加任意数量的规则。"

>[!CONTEXTUALHELP]
>id="ajo_exd_strategy_collection"
>title="选择收藏集"
>abstract="选择包含要考虑的选件的集合。 创建选择策略时，必须执行此步骤。 收藏集允许您根据自己的偏好对决策项目进行分类和分组。 例如，您可以创建一个集合，该集合包含具有“类别”自定义属性中的“瑜伽”值的所有决策项。"

>[!BEGINSHADEBOX]

本文档指南包括以下内容：

* [开始使用 Experience Decisioning](gs-experience-decisioning.md)
* 管理您的决策项目
   * [配置项目目录](catalogs.md)
   * [创建决策项目](items.md)
   * **[管理项目集合](collections.md)**
* 配置项目的选择
   * [创建决策规则](rules.md)
   * [创建排名方法](ranking.md)
* [创建选择策略](selection-strategies.md)
* [创建决策策略](create-decision.md)

>[!ENDSHADEBOX]

收藏集允许您根据自己的偏好对决策项目进行分类和分组。 这些类别是通过构建利用决策项目属性的规则创建的。

例如，假设您向决策项目的目录架构添加了“类别”自定义属性。 这允许您创建一个集合，该集合包含具有“类别”属性中的“瑜伽”值的所有决策项。

集合列表可从以下位置访问： **[!UICONTROL 项目]** 菜单。

要创建收藏集，请执行以下步骤：

1. 导航到 **[!UICONTROL 项目]** > **[!UICONTROL 收藏集]** 并单击 **[!UICONTROL 创建收藏集]**.
1. 提供收藏集的名称和描述。
1. 添加一个或多个规则以确定要包含在收藏集中的项目。 请按以下步骤执行此操作：

   1. 选择要用作条件的物料属性。 属性列表包含在目录架构中定义的所有标准和自定义属性。 [了解有关项目目录的更多信息](catalogs.md)
   1. 选择所需的运算符并输入要过滤的值。
   1. 重复这些步骤以根据需要添加任意数量的规则。 添加多个规则后，您可以选择 **和** 和 **或** 运算符以组合它们。 要执行此操作，请单击运算符徽章以在两个选项之间切换。

   ![](assets/collection-create.png)

1. 定义收藏集规则后，单击 **[!UICONTROL 创建]**. 收藏集现在显示在列表中。
