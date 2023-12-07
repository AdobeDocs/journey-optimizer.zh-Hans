---
title: 决策规则
description: 了解如何使用决策规则
feature: Experience Decisioning
topic: Integrations
role: User
level: Intermediate
hide: true
hidefromtoc: true
badge: label="Beta 版"
exl-id: 033a11b8-c848-4e4a-b6f0-62fa0a2152bf
source-git-commit: c13cd73229b2fab80722663afae9fe24b660c0f9
workflow-type: tm+mt
source-wordcount: '323'
ht-degree: 31%

---

# 决策规则 {#rules}

>[!CONTEXTUALHELP]
>id="ajo_exd_config_rules"
>title="创建决策规则"
>abstract="决策规则使您可通过直接在决策项级别或在特定选择策略中应用约束而定义决策项的受众。这样可精确地控制应向谁显示哪些项。"

>[!BEGINSHADEBOX “您将在本文档指南中找到什么”]

* [开始使用 Experience Decisioning](gs-experience-decisioning.md)
* 管理您的决策项目： [配置物料目录](catalogs.md) - [创建决策项目](items.md) - [管理物料集合](collections.md)
* 配置项目的选择： **[创建决策规则](rules.md)** - [创建排名方法](ranking.md)
* [创建选择策略](selection-strategies.md)
* [创建决策策略](create-decision.md)

>[!ENDSHADEBOX]

决策规则使您可通过直接在决策项级别或在特定选择策略中应用约束而定义决策项的受众。这样可精确地控制应向谁显示哪些项。

例如，我们考虑一个方案，其中您的决策项包含为女性设计的瑜伽相关产品。 通过决策规则，您可以指定只向性别为“女性”并在“瑜伽”中指定了“兴趣点”的用户档案显示这些项目。

>[!NOTE]
>
>除了项目和选择策略级别决策规则之外，您还可以在营销活动级别定义预期受众。 [了解详情](../campaigns/create-campaign.md#audience)


决策规则的列表可在 **[!UICONTROL 配置]** / **[!UICONTROL 决策规则]** 菜单。

<!--![](assets/decision-rules-list.png)-->

>[!IMPORTANT]
>
>目前，决策规则使用Journey Optimizer的 **决策管理** 菜单。 因此， **[!UICONTROL 决策规则]** Experience Decisioning中的列表包含从两个Journey Optimizer创建的规则 **[!UICONTROL 决策管理]** 或 **[!UICONTROL Experience Decisioning]** 菜单。

要创建规则，请执行以下步骤：

1. 导航到 **[!UICONTROL 配置]** / **[!UICONTROL 决策规则]**.
1. Journey Optimizer的决策管理用户界面显示在中心区域。 请按照 [决策管理文档](../offers/offer-library/creating-decision-rules.md) 以根据您的需求构建规则。

1. 创建规则后，该规则将显示在列表中，并可用于决策项和选择策略，以控制将决策项呈现给用户档案。
