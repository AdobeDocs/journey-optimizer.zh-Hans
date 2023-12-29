---
solution: Journey Optimizer
product: journey optimizer
title: 使用计算属性
description: 了解如何使用计算属性。
feature: Audiences, Profiles
role: User
level: Intermediate
exl-id: 5402a179-263f-46a7-bddf-5b7017cf0f82
source-git-commit: 3f96cc0037b5bcdb2ce94e2721b02ba13b3cff36
workflow-type: tm+mt
source-wordcount: '540'
ht-degree: 4%

---

# 使用计算属性 {#computed-attributes}

计算属性允许您将各个行为事件汇总到Adobe Experience Platform上可用的计算配置文件属性中。 这些计算属性基于提取到Adobe Experience Platform中的支持配置文件的体验事件数据集，并充当存储在客户配置文件中的聚合数据点。

每个计算属性是一个配置文件属性，您可以在历程和营销活动中利用它进行分段、个性化和激活。 这种简化增强了向客户提供及时且有意义的个性化体验的能力。


![](../rn/assets/do-not-localize/computed-attributes.gif)


>[!NOTE]
>
>要访问计算属性，您需要具有适当的权限(**查看计算属性** 和 **管理计算属性**)。

## 创建计算属性 {#manage}

要创建计算属性，请导航至 **[!UICONTROL 计算属性]** 选项卡 **[!UICONTROL 配置文件]** 菜单的左侧。

在此屏幕中，您可以通过构建规则来构造计算属性，这些规则将事件属性、聚合函数与指定的回顾期间一起组合。 例如，您可以计算过去三个月中进行的购买总数，确定上周未购买的用户档案查看的最新项目，或统计每个用户档案累计的总奖励积分。

![](assets/computed-attributes.png)

规则准备就绪后，发布计算属性以将其用于其他下游服务，包括Journey Optimizer。

有关如何创建和管理计算属性的详细信息，请参阅 [计算属性文档](https://experienceleague.adobe.com/docs/experience-platform/profile/computed-attributes/overview.html?lang=zh-Hans)

## 将计算属性添加到Adobe Experience Platform数据源 {#source}

为了能够利用Journey Optimizer中的计算属性，您首先需要将它们添加到Journey Optimizer **Experience Platform** 数据源。

Adobe Experience Platform 数据源定义与 Adobe 实时客户配置文件的连接。此数据源旨在从实时客户档案服务中检索档案数据和体验事件数据。

要将计算属性添加到数据源，请执行以下步骤：

1. 导航至 **[!UICONTROL 配置]** 左侧菜单，然后单击 **[!UICONTROL 数据源]** 卡片。

1. 选择 **[!UICONTROL Experience Platform]** 数据源。

   ![](assets/computed-attributes-add.png)

1. 添加 **[!UICONTROL SystemComputedAttribute]** 包含所有已创建计算属性的字段组。

   ![](assets/computed-attributes-fieldgroup.png)

计算属性现在可以在Journey Optimizer中使用。 [了解如何在Journey Optimizer中使用计算属性](#use)

有关如何将字段组添加到Adobe Experience Platform数据源的详细信息，请参阅 [本节](../datasource/adobe-experience-platform-data-source.md).

## 在Journey Optimizer中使用计算属性 {#use}

>[!NOTE]
>
>开始之前，请确保已将计算属性添加到Adobe Experience Platform数据源。 [在本节中了解详情](#source).

计算属性在历程优化器中提供了一组通用的功能。 您可以将它们用于各种目的，例如个性化消息内容、创建新受众或根据特定计算属性拆分历程。 例如，您可以通过在Condition活动中添加单个计算属性，根据用户档案在最近三周内的总购买量拆分历程路径。 您还可以通过显示每个用户档案最近查看的项目来个性化电子邮件。

由于计算属性是在配置文件合并架构中创建的配置文件属性字段，因此您可以从中的表达式编辑器访问它们。 **SystemComputedAttribute** 字段组。 从此处，您可以将计算属性添加到表达式中，将它们视为任何其他配置文件属性来执行所需的操作。

![](assets/computed-attributes-ajo.png)
