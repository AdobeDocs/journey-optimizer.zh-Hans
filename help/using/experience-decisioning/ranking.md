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
ht-degree: 27%

---

# 排名方法 {#rankings}

>[!CONTEXTUALHELP]
>id="ajo_exd_config_formulas"
>title="创建排名公式"
>abstract="通过公式可定义规则，这些规则将确定应首先显示哪项，而非考虑该项的优先级分数。创建排名方法后，即可将它分配给选择策略以定义应首先选择哪些项。"

排名方法允许您为要针对给定配置文件显示的项目排名。 创建排名方法后，即可将它分配给选择策略以定义应首先选择哪些项。

提供了两种类型的排名方法：

* **公式**&#x200B;允许您定义规则，这些规则将确定应首先显示哪个项目，而不是考虑项目的优先级分数。

* **AI模型**&#x200B;允许您使用经过训练的模型系统，这些系统将利用多个数据点来确定应该首先显示哪些项目。

## 创建排名方法 {#create}

要创建排名方法，请执行以下步骤：

1. 导航到&#x200B;**[!UICONTROL 策略设置]**&#x200B;菜单，然后根据要使用的排名类型选择&#x200B;**[!UICONTROL 公式]**&#x200B;或&#x200B;**[!UICONTROL AI模型]**&#x200B;菜单。

1. 单击屏幕右上角的&#x200B;**[!UICONTROL 创建公式]**&#x200B;或&#x200B;**[!UICONTROL 创建AI模型]**&#x200B;按钮。

   ![](assets/ranking-create.png)

1. 根据您的需要配置公式或AI模型，然后保存。

   有关如何创建排名公式和AI模型的详细信息，请参阅决策管理文档：

   * [排名公式](../offers/ranking/create-ranking-formulas.md)
   * [AI 模型](../offers/ranking/ai-models.md)


## 在公式中利用决策项目属性 {#items}

排名公式以&#x200B;**PQL语法**&#x200B;表示，并且可以利用各种属性，例如配置文件属性、[上下文数据](context-data.md)以及与决策项目相关的属性。

要在公式中利用与决策项目相关的属性，请确保遵循排名公式代码中的以下语法。 展开每个部分以了解更多信息：

+++利用决策项目标准属性

![](assets/formula-attribute.png)

+++

+++利用决策项目自定义属性

![](assets/formula-attribute-custom.png)

+++
