---
title: 排名方法
description: 了解如何使用排名方法
feature: Decisioning, Ranking
topic: Integrations
role: User
level: Intermediate
exl-id: c1d69bc9-4486-4037-b218-f4f704b2ba9c
version: Journey Orchestration
TQID: https://experienceleague.adobe.com/1qUj05fLaRqqJGfaoL-y5uwtknp7HDkWKocHMde-8lc
product_v2:
  - id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2:
  - id: a4cb03e1-327e-499d-9de8-e0c0db8a63a2
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
subfeature_v2:
  - id: a7a194a0-75e2-4913-8a83-14714fbf68e6
  - id: eb547372-2a95-4d13-b0fd-f720c9895880
source-git-commit: 0ee10a0689d38c22b1180b197796b08a10c286cf
workflow-type: tm+mt
source-wordcount: 205
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


