---
title: 排名方法
description: 了解如何使用排名方法
feature: Offers
topic: Integrations
role: User
level: Intermediate
hide: true
hidefromtoc: true
badge: label="Beta 版"
exl-id: c1d69bc9-4486-4037-b218-f4f704b2ba9c
source-git-commit: c4ab97999d000d969f6f09f4d84be017d1288f94
workflow-type: tm+mt
source-wordcount: '179'
ht-degree: 25%

---

# 排名方法 {#rankings}

>[!BEGINSHADEBOX]

本文档指南包括以下内容：

* [开始使用 Experience Decisioning](gs-experience-decisioning.md)
* 管理您的决策项目
   * [配置项目目录](catalogs.md)
   * [创建决策项目](items.md)
   * [管理项目集合](collections.md)
* 配置项目的选择
   * [创建决策规则](rules.md)
   * **[创建排名方法](ranking.md)**
* [创建选择策略](selection-strategies.md)
* [创建决策策略](create-decision.md)

>[!ENDSHADEBOX]

排名方法允许您为要针对给定配置文件显示的项目排名。 创建排名方法后，您可以将其分配给决策策略以定义应首先选择哪些项目。

排名方法可从以下位置访问 **[!UICONTROL 配置]** / **[!UICONTROL 排名方法]** 菜单。 提供了两种类型的排名方法：

* **公式** 允许您定义规则以确定应首先显示哪个项目，而不是考虑项目的优先级分数。

* **AI模型** 允许您使用经过训练的模型系统，这些系统将利用多个数据点来确定应该首先显示哪个项目。

![](assets/ranking-create.png)

有关每种类型的排名方法以及如何创建这些方法的详细信息，请参阅可从此处访问的决策管理文档：

* [排名公式](../offers/ranking/create-ranking-formulas.md)
* [AI 模型](../offers/ranking/ai-models.md)
