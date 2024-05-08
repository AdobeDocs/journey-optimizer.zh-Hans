---
title: 排名方法
description: 了解如何使用排名方法
feature: Experience Decisioning, Ranking
topic: Integrations
role: User
level: Intermediate
badge: label="有限发布版"
exl-id: c1d69bc9-4486-4037-b218-f4f704b2ba9c
source-git-commit: 5ce388e5d86950e5cc6b173aab48225825f1c648
workflow-type: tm+mt
source-wordcount: '308'
ht-degree: 12%

---

# 排名方法 {#rankings}

>[!CONTEXTUALHELP]
>id="ajo_exd_config_formulas"
>title="创建排名公式"
>abstract="通过公式可定义规则，这些规则将确定应首先显示哪项，而非考虑该项的优先级分数。创建排名方法后，您可以将其分配给选择策略，以定义应首先选择哪些项目。"

排名方法允许您为要针对给定配置文件显示的项目排名。 创建排名方法后，您可以将其分配给选择策略，以定义应首先选择哪些项目。

提供了两种类型的排名方法：

* **公式** 允许您定义规则以确定应首先显示哪个项目，而不是考虑项目的优先级分数。

* **AI模型** 允许您使用经过训练的模型系统，这些系统将利用多个数据点来确定应该首先显示哪个项目。

## 创建排名方法 {#create}

要创建排名方法，请执行以下步骤：

1. 导航至 **[!UICONTROL 策略设置]** 菜单，然后选择 **[!UICONTROL 公式]** 或 **[!UICONTROL AI模型]** 菜单，具体取决于您要使用的排名类型。

1. 单击 **[!UICONTROL 创建公式]** 或 **[!UICONTROL 创建AI模型]** 按钮来打开屏幕。

   ![](assets/ranking-create.png)

1. 根据您的需要配置公式或AI模型，然后保存。

   有关如何创建排名公式和AI模型的详细信息，请参阅决策管理文档：

   * [排名公式](../offers/ranking/create-ranking-formulas.md)
   * [AI模型](../offers/ranking/ai-models.md)


## 在公式中利用决策项目属性 {#items}

排名公式表示为 **PQL语法** 和可以利用各种属性，如配置文件属性， [上下文数据](context-data.md) 和与决策项目相关的属性。

要在公式中利用与决策项目相关的属性，请确保遵循排名公式代码中的以下语法。 展开每个部分以了解更多信息：

+++利用决策项目标准属性

![](assets/formula-attribute.png)

+++

+++利用决策项目自定义属性

![](assets/formula-attribute-custom.png)

+++
