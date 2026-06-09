---
solution: Journey Optimizer
product: journey optimizer
title: 使用计算属性
description: 了解如何使用计算属性。
feature: Audiences, Profiles
role: User
level: Intermediate
exl-id: 5402a179-263f-46a7-bddf-5b7017cf0f82
TQID: https://experienceleague.adobe.com/bH8UDdjWsh1Kle1ltVP2ltgXcNJDfVIdTuFdGWSZv6Y
product_v2:
  - id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2:
  - id: baecb07f-ce89-4ebb-9cd9-0f7c053f944f
subfeature_v2:
  - id: f42b4d14-fe8a-428b-b62e-e7995eaab1b3
  - id: b32bb433-f8c6-4931-8e52-e657230a3bf2
  - id: e95b6013-acbe-46e9-a3b5-b80e14088d7d
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
topic_v2:
  - id: e0eb8757-182f-49f3-94a4-1587d16f5094
  - id: fd2e3797-f2ea-4b36-a9af-52acf5e90513
source-git-commit: 80e67d5a60b6427ff87e106e37bf6794ac76a210
workflow-type: tm+mt
source-wordcount: 927
ht-degree: 1%

---

# 使用计算属性 {#computed-attributes}

计算属性将各个行为事件汇总到Adobe Experience Platform上可用的计算配置文件属性中。 这些属性基于摄取到Adobe Experience Platform中的启用配置文件的体验事件数据集，并充当存储在客户配置文件中的聚合数据点。

每个计算属性是一个配置文件属性，您可以在历程和营销活动中利用它进行分段、个性化和激活。 这种简化增强了向客户提供及时且有意义的个性化体验的能力。


![](../rn/assets/do-not-localize/computed-attributes.gif)


>[!NOTE]
>
>要访问计算属性，请确保您具有适当的权限（**查看计算属性**&#x200B;和&#x200B;**管理计算属性**）。

## 创建计算属性 {#manage}

要创建计算属性，请浏览到左侧的&#x200B;**[!UICONTROL 配置文件]**&#x200B;菜单中的&#x200B;**[!UICONTROL 计算属性]**&#x200B;选项卡。

在此屏幕中，您可以通过构建规则来构建计算属性，这些规则将事件属性、聚合函数与指定的回顾期间结合使用。 例如，您可以计算过去三个月中进行的购买总数，确定上周未购买的用户档案查看的最新项目，或统计每个用户档案累计的总奖励积分。

![](assets/computed-attributes.png)

规则准备就绪后，发布计算属性以将其用于其他下游服务，包括Journey Optimizer。

有关创建和管理计算属性的详细信息，请参阅[计算属性文档](https://experienceleague.adobe.com/docs/experience-platform/profile/computed-attributes/overview.html?lang=zh-Hans)

## 将计算属性添加到Adobe Experience Platform数据源 {#source}

要利用Journey Optimizer中的计算属性，请将其添加到Journey Optimizer **Experience Platform**&#x200B;数据源。

Adobe Experience Platform数据源定义与Adobe实时客户个人资料的连接。 此数据源从实时客户资料服务中检索资料数据和体验事件数据。

要将计算属性添加到数据源，请执行以下步骤：

1. 浏览至左侧的&#x200B;**[!UICONTROL 配置]**&#x200B;菜单，然后单击&#x200B;**[!UICONTROL 数据源]**&#x200B;卡。

1. 选择&#x200B;**[!UICONTROL Experience Platform]**&#x200B;数据源。

   ![](assets/computed-attributes-add.png)

1. 添加包含所有已创建的计算属性的&#x200B;**[!UICONTROL SystemComputedAttributes]**&#x200B;字段组。

   ![](assets/computed-attributes-fieldgroup.png)

计算属性现在可以在Journey Optimizer中使用。 [了解如何在Journey Optimizer中使用计算属性](#use)

有关将字段组添加到Adobe Experience Platform数据源的详细信息，请参阅[此部分](../datasource/adobe-experience-platform-data-source.md)。

## 在Journey Optimizer中使用计算属性 {#use}

>[!NOTE]
>
>开始之前，请确保已将计算属性添加到Adobe Experience Platform数据源。 [在本节](#source)中了解详情。

计算属性在Journey Optimizer中提供多种功能。 将它们用于各种目的，例如个性化消息内容、创建新受众或根据特定计算属性拆分历程。 例如，通过在Condition活动中添加单个计算属性，根据用户档案在最近三周内的总购买量拆分历程路径。 您还可以通过显示每个用户档案最近查看的项目来个性化电子邮件。

由于计算属性是在您的配置文件合并架构上创建的配置文件属性字段，请从&#x200B;**SystemComputedAttributes**&#x200B;字段组中的个性化编辑器访问它们。 从此处，将计算属性添加到表达式中，将其视为任何其他配置文件属性来执行所需的操作。

![](assets/computed-attributes-ajo.png)

+++AI助手 — 页面上下文

- **TL；DR：**&#x200B;了解如何在Adobe Experience Platform上创建计算属性，并在Journey Optimizer中利用这些属性进行分段、个性化和历程逻辑。

**意图：**
- 了解什么是计算属性以及它们与标准配置文件属性的差异
- 通过组合事件属性、聚合函数和回顾期间来创建计算属性
- 将SystemComputedAttributes字段组添加到AJO中的Experience Platform数据源
- 在历程条件、受众构建和消息个性化中使用计算属性

**术语表：**
- **计算属性**：从聚合行为事件数据派生的配置文件属性，存储在客户配置文件&#x200B;*（产品特定）*&#x200B;中
- **回顾时段**：计算计算属性的聚合规则（例如“过去3个月”）时应用的时间范围&#x200B;*（产品特定）*
- **SystemComputedAttributes字段组**： AJO Experience Platform数据源中的字段组，该字段组公开所有已发布的计算属性，以供在历程和个性化&#x200B;*（产品特定）*&#x200B;中使用
- **配置文件合并架构**：合并了给定标识的所有配置文件片段的合并架构，其中存储了计算属性

**护栏：**
- 需要&#x200B;**查看计算属性**&#x200B;和&#x200B;**管理计算属性**&#x200B;权限才能访问该功能
- 计算属性必须在AEP中&#x200B;**发布**，然后才能在Journey Optimizer下游使用
- 计算属性必须先显式添加到AJO中的&#x200B;**Experience Platform数据源**，然后才能在历程或个性化中使用
- 计算属性基于引入到Adobe Experience Platform中的启用配置文件的体验事件数据集

**术语：**
- 规范名称：Adobe Journey Optimizer — 缩写：AJO — 变体：Journey Optimizer、A-JO
- 规范名称：Adobe Experience Platform — 缩写：AEP
- 同义词：“计算属性”=“计算配置文件属性”
- 请勿混淆：“计算属性”（AEP/AJO特定的聚合功能）≠通用“配置文件属性”

**常见问题解答：**
- **问：什么是计算属性？**  — 在AEP中存储为配置文件属性并在AJO中可用的汇总行为事件数据（例如，总购买次数、上次查看的项目）。
- **问：我需要特殊权限吗？**  — 是：“查看计算属性”和“管理计算属性”都是必需的。
- **问：如何使计算属性在Journey Optimizer中可用？**  — 在Configurations > Data sources下将`SystemComputedAttributes`字段组添加到Experience Platform数据源。
- **问：在AJO中，可在何处使用计算属性？**  — 在条件活动（历程拆分）、受众创建和个性化编辑器中。
- **问：什么是回顾期间？**  — 用于限定聚合规则范围的时间窗口，例如“过去3周内的购买总和”。
- **问：能否在实时历程中使用计算属性？**  — 是，发布并添加到数据源后，即可像访问任何其他配置文件属性一样访问它们。

+++
