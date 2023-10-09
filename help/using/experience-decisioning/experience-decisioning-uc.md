---
title: Experience Decisioning用例
description: 了解如何使用基于代码的渠道的实验创建决策
feature: Offers
topic: Integrations
role: User
level: Intermediate
hide: true
hidefromtoc: true
badge: label="Beta 版"
source-git-commit: 69a2ef17b6f5ccd40c08858f7b434029964d544d
workflow-type: tm+mt
source-wordcount: '399'
ht-degree: 18%

---

# Experience Decisioning用例 {#experience-decisioning-uc}

>[!BEGINSHADEBOX]

本文档指南包括以下内容：

* [开始使用 Experience Decisioning](gs-experience-decisioning.md)
* 管理您的决策项目
   * [配置项目目录](catalogs.md)
   * [创建决策项目](items.md)
   * [管理项目集合](collections.md)
* 配置项目的选择
   * [创建决策规则](rules.md)
   * [创建排名方法](ranking.md)
* [创建选择策略](selection-strategies.md)
* [创建决策策略](create-decision.md)
* **[通过用例学习](experience-decisioning-uc.md)**

>[!ENDSHADEBOX]

在此使用案例中，您定义了两种投放处理，每种处理包含不同的决策策略，以便衡量哪种策略对目标受众的表现最好。

## 创建项目和策略

您首先需要创建项目，在收藏集中将其分组，设置规则和排名方法。 这些元素将允许您构建选择策略。

1. 导航到 **[!UICONTROL Experience Decisioning]** > **[!UICONTROL 项目]** 并创建多个选件项目。 使用受众或规则设置约束，将每个项目限制为仅访问特定用户档案。 [了解详情](items.md)

   <!--
   1. From the items list, click the **[!UICONTROL Edit schema]** button  and edit the custom attributes if needed. [Learn how to work with catalogs](catalogs.md)-->

1. 创建 **收藏集** 根据您的偏好对决策项目进行分类和分组。 [了解详情](collections.md)

1. 创建 **决策规则** 以确定可以向谁显示决策项。 [了解详情](rules.md)

1. 创建 **排名方法** 并将其应用于决策策略中，以确定选择决策项目的优先顺序。 [了解详情](ranking.md)

1. 生成 **选择策略** 它利用收藏集、决策规则和排名方法来确定适合显示给用户档案的决策项目。 [了解详情](selection-strategies.md)

## 创建决策策略

要在您的网站或移动应用程序上向访客展示最佳的动态选件和体验，请向基于代码的营销活动添加决策策略。

定义两个投放处理，每个处理包含不同的决策策略。

1. 创建营销策划并选择 **[!UICONTROL 代码库体验(Beta)]** 操作。 [了解详情](../code-based/create-code-based.md)

   >[!NOTE]
   >
   >基于代码的体验功能目前作为测试版提供，仅限部分用户使用。 要加入 Beta 版计划，请联系 Adobe 客户关怀团队。

1. 在营销活动摘要页面中，单击 **[!UICONTROL 创建试验]** 以开始配置内容体验。 [了解详情](../campaigns/content-experiment.md)

1. 选择 **[!UICONTROL 决策]** 图标，单击 **[!UICONTROL 创建决策]** 并填写决策详细信息。 [了解详情](create-decision.md)

   ![](assets/decision-code-based-create.png)

1. 为您的决策定义选择策略。 单击 **[!UICONTROL 添加策略]**.

1. 单击&#x200B;**[!UICONTROL 创建]**。新决策将添加在 **[!UICONTROL 决策]**.

   ![](assets/decision-code-based-decision-added.png)

1. 单击更多操作图标（三个圆点）并选择 **[!UICONTROL 添加]**. 现在，您可以向其中添加所需的所有决策属性。

   ![](assets/decision-code-based-add-decision.png)

1. 您还可以添加表达式编辑器中可用的任何其他属性，如配置文件属性。

   ![](assets/decision-code-based-decision-profile-attribute.png)

1. 构建处理B并重复上述步骤以创建另一个决策。

1. 保存您的内容。


