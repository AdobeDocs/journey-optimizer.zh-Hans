---
title: 排名方法
description: 了解如何使用排名方法
feature: Decisioning, Ranking
topic: Integrations
role: User
level: Intermediate
exl-id: c1d69bc9-4486-4037-b218-f4f704b2ba9c
source-git-commit: 58f4fdf8ec3cdb609efebf5b8713f6b770ef5414
workflow-type: tm+mt
source-wordcount: '204'
ht-degree: 16%

---

# 排名方法 {#rankings}

排名方法允许您为要针对给定配置文件显示的项目排名。 创建排名方法后，即可将它分配给选择策略以定义应首先选择哪些项。

提供了两种类型的排名方法：

* **公式**&#x200B;允许您定义规则，这些规则将确定应首先显示哪个项目，而不是考虑项目的优先级分数。

* **AI模型**&#x200B;允许您使用经过训练的模型系统，这些系统将利用多个数据点来确定应该首先显示哪些项目。

## 创建排名方法 {#create}

要创建排名方法，请执行以下步骤：

1. 导航到&#x200B;**[!UICONTROL 策略设置]**&#x200B;菜单，然后根据要使用的排名类型选择&#x200B;**[!UICONTROL 公式]**&#x200B;或&#x200B;**[!UICONTROL AI模型]**&#x200B;菜单。

   ![](../assets/ranking-create.png)

1. 单击屏幕右上角的&#x200B;**[!UICONTROL 创建公式]**&#x200B;或&#x200B;**[!UICONTROL 创建AI模型]**&#x200B;按钮。

   有关如何创建排名公式和AI模型的详细信息，请参阅以下部分：

   * [排名公式](ranking-formulas.md)
   * [AI 模型](ai-models.md)

1. 根据您的需要配置公式或AI模型，然后保存。

您的排名方法现在可以在[选择策略](../selection-strategies.md)中使用来对符合条件的决策项排名。


