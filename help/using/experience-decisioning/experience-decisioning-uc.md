---
title: Decisioning用例
description: 了解如何使用基于代码的渠道的实验创建决策
feature: Decisioning
topic: Integrations
role: User
level: Intermediate, Experienced
source-git-commit: 616e1dd9fbfd029f7209356d5c19cfff9d4b4f06
workflow-type: tm+mt
source-wordcount: '342'
ht-degree: 6%

---

# Decisioning用例 {#experience-decisioning-uc}

在此使用案例中，您将创建一个营销活动，在该活动中定义两个投放处理，每个处理都包含不同的决策策略，以衡量哪个策略对目标受众的表现最好。

## 创建决策项和选择策略

您首先需要创建项目，在收藏集中将其分组，设置规则和排名方法。 这些元素将允许您构建选择策略。

1. 导航到&#x200B;**[!UICONTROL 决策]** > **[!UICONTROL 目录]**&#x200B;并创建多个决策项。 使用受众或规则设置约束，将每个项目限制为仅访问特定用户档案。 [了解详情](items.md)

   <!--
   1. From the items list, click the **[!UICONTROL Edit schema]** button  and edit the custom attributes if needed. [Learn how to work with catalogs](catalogs.md)-->

1. 创建&#x200B;**收藏集**&#x200B;以根据您的首选项对决策项进行分类和分组。 [了解详情](collections.md)

1. 创建&#x200B;**决策规则**&#x200B;以确定可向谁显示决策项。 [了解详情](rules.md)

1. 创建&#x200B;**排名方法**&#x200B;并在决策策略中应用它们以确定选择决策项的优先级顺序。 [了解详情](ranking.md)

1. 生成&#x200B;**选择策略**，该策略利用集合、决策规则和排名方法来识别适合显示到用户档案的决策项目。 [了解详情](selection-strategies.md)

## 创建决策策略

要在您的网站或移动应用程序上向访客展示最佳的动态选件和体验，请向基于代码的营销活动添加决策策略。

<!--Define two delivery treatments each containing a different decision policy.-->

1. 创建营销活动，然后选择&#x200B;**[!UICONTROL 基于代码的体验]**&#x200B;操作。 [了解详情](../code-based/create-code-based.md)

1. 从&#x200B;**[!UICONTROL 编辑内容]**&#x200B;窗口，开始个性化处理A。

1. 选择&#x200B;**[!UICONTROL 决策]**&#x200B;图标，单击&#x200B;**[!UICONTROL 创建决策]**&#x200B;并填写决策详细信息。 [了解详情](create-decision.md)

   ![](assets/decision-code-based-create.png)

1. 为您的决策定义选择策略。 单击&#x200B;**[!UICONTROL 添加策略]**。

1. 单击&#x200B;**[!UICONTROL 创建]**。新决策已添加到&#x200B;**[!UICONTROL 决策]**&#x200B;下。

   ![](assets/decision-code-based-decision-added.png)

1. 单击“更多操作”图标（三个圆点）并选择&#x200B;**[!UICONTROL 添加]**。 现在，您可以向其中添加所需的所有决策属性。

   ![](assets/decision-code-based-add-decision.png)

1. 您还可以添加个性化编辑器中可用的任何其他属性，例如配置文件属性。

   ![](assets/decision-code-based-decision-profile-attribute.png)

1. 在营销活动摘要页面中，单击&#x200B;**[!UICONTROL 创建试验]**&#x200B;以开始配置内容试验。 [了解详情](../content-management/content-experiment.md)

1. 从&#x200B;**[!UICONTROL 编辑内容]**&#x200B;窗口中，选择您的处理B以更改内容，并重复上述步骤以创建另一个决策。

1. 保存您的内容。


