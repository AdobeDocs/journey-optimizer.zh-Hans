---
title: 收藏集
description: 了解如何使用收藏集
feature: Offers
topic: Integrations
role: User
level: Intermediate
hide: true
hidefromtoc: true
source-git-commit: 4aea5c1434caa07aad26445c49a3d5c6274502ec
workflow-type: tm+mt
source-wordcount: '261'
ht-degree: 5%

---

# 收藏集 {#collections}

>[!BEGINSHADEBOX]

本文档指南包括以下内容：

* [Experience Decisioning入门](gs-experience-decisioning.md)
* 管理您的决策项目
   * [配置物料目录](catalogs.md)
   * [创建决策项目](items.md)
   * **[管理物料集合](collections.md)**
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
