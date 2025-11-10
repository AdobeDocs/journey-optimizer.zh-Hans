---
title: 集合
description: 了解如何使用收藏集
feature: Decisioning
topic: Integrations
role: User
level: Intermediate
exl-id: 099d1439-34f7-47fe-9181-0e9ce2032a01
version: Journey Orchestration
source-git-commit: 0b94bfeaf694e8eaf0dd85e3c67ee97bd9b56294
workflow-type: tm+mt
source-wordcount: '518'
ht-degree: 36%

---

# 集合 {#collections}

>[!CONTEXTUALHELP]
>id="ajo_exd_item_collections"
>title="创建收藏集"
>abstract="您可以使用集合根据自己的喜好对决策项进行分类和分组。通过制定利用决策项属性的规则而创建这些类别。"

>[!CONTEXTUALHELP]
>id="ajo_exd_item_collection_rules"
>title="为您的集合定义规则"
>abstract="添加一项或多项规则以确定要包含在集合中的项目。选择要用作标准的项属性。选择所需的运算符并输入要过滤的值。添加所需数量的规则。"

>[!CONTEXTUALHELP]
>id="ajo_exd_strategy_collection"
>title="选择一个集合。"
>abstract="选择包含要考虑的产品建议的收藏集。创建选择策略时必须执行此步骤。您可以使用集合根据自己的喜好对决策项进行分类和分组。例如，您可以创建一个集合，其中包含“类别”自定义属性中具有“瑜伽”值的所有决策项。"

您可以使用集合根据自己的喜好对决策项进行分类和分组。通过制定利用决策项属性的规则而创建这些类别。

例如，假设您向决策项目的目录架构添加了“类别”自定义属性。 这允许您创建一个集合，该集合包含具有“类别”属性中的“瑜伽”值的所有决策项。

可从&#x200B;**[!UICONTROL 目录]**&#x200B;菜单访问收藏集列表。

要创建收藏集，请执行以下步骤：

1. 导航到&#x200B;**[!UICONTROL 目录]** > **[!UICONTROL 集合]**，然后单击&#x200B;**[!UICONTROL 创建集合]**。
1. 提供收藏集的名称和描述。
1. 添加一项或多项规则以确定要包含在集合中的项目。操作步骤：

   1. 选择要用作标准的项属性。属性列表包含在目录架构中定义的所有标准和自定义属性。 [了解有关项目目录的更多信息](catalogs.md)
   1. 选择所需的运算符并输入要筛选的值。明确筛选每个选件名称，或创建一个“luma-summer”标记并将其分配给每个选件。

      >[!NOTE]
      >
      >**CONTAINS**&#x200B;运算符不支持部分匹配或通配符匹配。 它的工作方式类似于&#x200B;**IN**&#x200B;运算符，这意味着您必须为特性提供精确值的数组。
      >
      >例如，假设您有多个夏季优惠要包含在收藏中：*&quot;luma-summer-yoga&quot;*、*&quot;luma-summer-fitness&quot;*&#x200B;和&#x200B;*&quot;luma-summer-running&quot;*。 要包含这些项目，您需要定义一个规则，例如“优惠名称” CONTAINS“luma-summer-yoga”、“luma-summer-fitness”、“luma-summer-running”。 此规则仅返回与列表中的某个名称完全匹配的选件。
      >
      >如果您需要部分匹配（例如，包含&#x200B;*&quot;luma-summer&quot;*&#x200B;的所有选件），则当前不支持此功能。 您需要显式指定每个选件名称，或为每个选件分配一个&#x200B;*&quot;luma-summer&quot;*&#x200B;标记，并在规则中使用该标记。

   1. 重复这些步骤以根据需要添加任意数量的规则。 添加多个规则后，您可以在&#x200B;**And**&#x200B;和&#x200B;**Or**&#x200B;运算符之间进行选择以组合它们。 要执行此操作，请单击运算符徽章以在两个选项之间切换。
   1. 单击&#x200B;**[!UICONTROL 预览收藏集]**&#x200B;按钮以显示符合您定义的规则的项目。

   ![](assets/collection-create.png)

1. 定义集合规则后，单击&#x200B;**[!UICONTROL 创建]**。 收藏集现在显示在列表中。

>[!NOTE]
>
>每个项目收藏集最多可包含500个选件项目。 [了解有关Decisioning护栏和限制的更多信息](gs-experience-decisioning.md#guardrails)
