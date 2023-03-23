---
solution: Journey Optimizer
product: journey optimizer
title: 使用组合画布
description: 了解如何使用合成画布
feature: Journeys
topic: Content Management
role: User
level: Intermediate
hide: true
hidefromtoc: true
exl-id: 3eb9466e-9d88-4470-a22f-5e24a29923ae
badge: label="Beta" type="Informitive"
source-git-commit: 160e4ce03d3be975157c30fbe511875a85b00551
workflow-type: tm+mt
source-wordcount: '1353'
ht-degree: 27%

---

# 使用组合画布 {#composition-canvas}

>[!BEGINSHADEBOX]

您将在本文档中找到的内容：

* [受众组合入门](get-started-audience-orchestration.md)
* [创建您的第一个合成工作流](create-compositions.md)
* **[使用组合画布](composition-canvas.md)**
* [访问和管理受众](access-audiences.md)

>[!ENDSHADEBOX]

受众组合提供了一个可视化画布，允许您创建受众并使用各种活动（拆分、扩充等）。

在画布中构建受众的步骤如下：

1. [定义起始受众](#starting-audience)
1. [添加一个或多个活动](#action-activities)
1. [将结果保存到新受众中](#save)

## 选择起始受众 {#starting-audience}

创建合成的第一步是选择一个或多个现有受众作为合成的基础。

1. 选择 **[!UICONTROL 受众]** 活动，然后为活动提供标签。

1. 选择要定位的受众：

   * 单击 **[!UICONTROL 添加受众]** 按钮选择一个或多个现有受众，
   * 单击 **[!UICONTROL 生成规则]** 按钮以使用 [Segmentation Service](https://experienceleague.adobe.com/docs/experience-platform/segmentation/ui/overview.html).

   ![](assets/audiences-choose-audience.png)

1. 如果选择了多个受众，请指定这些受众的用户档案应如何合并：

* **[!UICONTROL 并集]**:包含来自选定受众的所有用户档案，
* **[!UICONTROL 交集]**:包括所有选定受众共有的用户档案，
* **[!UICONTROL 排除重叠]**:包括仅属于其中一个受众的用户档案。 将不包含属于多个受众的用户档案。

在此示例中，我们要定位属于金牌和银牌受众的所有用户档案。

![](assets/audiences-starting-audience.png)

选择受众后，预计用户档案数会显示在活动底部。

## 添加活动 {#action-activities}

选择起始受众后添加活动以优化您的选择。

要实现此目的，请单击合成路径上的+按钮，然后选择所需的活动。 此时会打开右侧窗格，用于配置新添加的活动。

![](assets/audiences-select-activity.png)

可用的活动包括：

* [受众](#audience):包括属于一个或多个现有受众的其他用户档案，
* [排除](#exclude):排除属于现有受众的用户档案，或根据特定属性排除用户档案，
* [丰富]{#enrich}:通过来自Adobe Experience Platform数据集的其他属性来丰富受众，
* [排名](#rank):根据特定属性对用户档案进行排名，指定要保留的用户档案数并将其包含在您的构成中，
* [拆分](#split):根据随机百分比或属性将您的构图划分为多个路径。

您可以添加任意数量的 **[!UICONTROL 受众]** 和 **[!UICONTROL 排除]** 活动。 但是，在 **[!UICONTROL 排名]** 和 **[!UICONTROL 拆分]** 活动。

您可以随时通过单击右侧窗格中的删除按钮，从画布中删除活动。  如果要删除的活动是组合中其他活动的父活动，则会显示一条消息，允许您指定是仅删除所选活动还是删除其所有子活动。

### 受众活动 {#audience}

>[!CONTEXTUALHELP]
>id="ajo_ao_audience"
>title="受众活动"
>abstract="“受众活动”让您可以在组合中包括属于现有受众的配置文件。"

>[!CONTEXTUALHELP]
>id="ajo_ao_merge_types"
>title="合并类型"
>abstract="指定应如何合并所选受众的配置文件。"

的 **[!UICONTROL 受众]** 活动允许您在合成中包含属于现有受众的其他用户档案。

此活动的配置与开始 [受众活动](#starting-audience).

### 排除活动 {#exclude}

>[!CONTEXTUALHELP]
>id="ajo_ao_exclude_type"
>title="排除类型"
>abstract="使用“排除受众类型”排除属于现有受众的配置文件。“使用属性类型排除”让您可以根据特定属性来排除配置文件。"

>[!CONTEXTUALHELP]
>id="ajo_ao_exclude"
>title="排除活动"
>abstract="“排除活动”让您可以通过选择现有受众或使用规则，从组合中排除配置文件。"

的 **[!UICONTROL 排除]** 活动，可将用户档案从构图中排除。 可以使用两种类型的排除：

* **[!UICONTROL 排除受众]**:排除属于现有受众的用户档案。

   单击 **[!UICONTROL 添加受众]** 按钮，然后选择要排除的受众。

   ![](assets/audiences-exclude-audience.png)

* **[!UICONTROL 使用属性排除]**:根据特定属性排除用户档案。

   选择要查找的属性，然后指定要排除的值。 在本例中，我们从其家庭地址位于日本的合成用户档案中排除。

   ![](assets/audiences-exclude-attribute.png)

### 丰富 {#enrich}

>[!CONTEXTUALHELP]
>id="ajo_ao_enrich"
>title="扩充活动"
>abstract="使用“扩充活动”排除属于现有受众的配置文件。“使用属性类型”排除让您可以根据特定属性来排除配置文件。"

>[!CONTEXTUALHELP]
>id="ajo_ao_enrich_dataset"
>title="扩充数据集"
>abstract="选择包含要与受众关联的数据的扩充数据集。"

>[!CONTEXTUALHELP]
>id="ajo_ao_enrich_criteria"
>title="扩充标准"
>abstract="选择要用作源数据集（即受众）与扩充数据集之间的合并关键项的字段。"

>[!CONTEXTUALHELP]
>id="ajo_ao_enrich_attributes"
>title="扩充属性"
>abstract="从扩充数据集中选择一个或多个属性以关联到受众。组合在发布之后，这些属性就会与受众相关联，并且可以在营销活动中用来提供个性化的投放。"

的 **[!UICONTROL 丰富]** 活动允许您使用来自Adobe Experience Platform数据集的其他属性来扩充受众。 例如，您可以添加与所购买产品相关的信息（如其名称、价格或制造商ID），并利用这些信息将发送给受众的投放个性化。

>[!IMPORTANT]
>
>目前，数据集上的标签（无论是在数据集级别还是在字段级别）不会传播到新创建的受众。 这可能会影响结果受众的访问控制和/或数据管理。 因此，在合成受众时请仅使用测试数据。

要配置活动，请执行以下步骤：

1. 选择 **[!UICONTROL 扩充数据集]** 包含要与受众关联的数据。

1. 在 **[!UICONTROL 扩充标准]** 部分，选择要用作源数据集（即受众）和扩充数据集之间协调键值的字段。 在此示例中，我们使用已购买产品的ID作为对帐密钥。

1. 单击 **[!UICONTROL 添加属性]** 按钮，然后从扩充数据集中选择一个或多个要与受众关联的属性。

   ![](assets/audiences-enrich-activity.png)

发布组合后，所选属性将与受众关联，并可在营销活动中利用这些属性来个性化投放。

### 排名活动 {#rank}

>[!CONTEXTUALHELP]
>id="ajo_ao_ranking"
>title="排名活动"
>abstract="“排名活动”允许您根据特定属性对配置文件进行排名并将它们包含在组合中。例如，包含忠诚度积分最高的 50 个配置文件。"

>[!CONTEXTUALHELP]
>id="ajo_ao_rank_profilelimit_text"
>title="添加配置文件限制"
>abstract="打开此选项以指定要包含在组合中的配置文件最大数量。"

的 **[!UICONTROL 排名]** 利用活动，可根据特定属性对用户档案进行排名，并将其包含在您的构图中。 例如，您可以包含50个用户档案，其中会员积分数量最多。

1. 选择要查找的属性并指定排名顺序（升序或降序）。

   >[!NOTE]
   >
   >您可以选择具有以下数据类型的属性：整数，数字，短 <!--(other?)-->

1. 切换 **[!UICONTROL 添加配置文件限制]** 选项，并指定要包含在组合中的配置文件的最大数量。

   ![](assets/audiences-rank.png)

### 拆分活动 {#split}

<!-- [!CONTEXTUALHELP]
>id="ajo_ao_control_group_text"
>title="Control Group"
>abstract="Use control groups to isolate a portion of the profiles. This allows you to measure the impact of a marketing activity and make a comparison with the behavior of the rest of the population."-->

>[!CONTEXTUALHELP]
>id="ajo_ao_split"
>title="拆分活动"
>abstract="“拆分活动”让您可以将组合拆分成多个路径。在发布组合时，一个受众将在 Adobe Experience Platform 针对每个路径进行保存。"

>[!CONTEXTUALHELP]
>id="ajo_ao_split_type"
>title="拆分类型"
>abstract="使用“百分比拆分类型”可将配置文件随机拆分到多个路径中。“属性拆分类型”让您可以根据特定属性来拆分配置文件。"

>[!CONTEXTUALHELP]
>id="ajo_ao_split_otherprofiles_text"
>title="其他配置文件"
>abstract="打开此选项可以创建一个附加路径，其中包含与其他路径中指定的任意条件都不匹配的剩余配置文件。"

的 **[!UICONTROL 拆分]** 活动，可将构图划分为多个路径。

此操作会自动添加 **[!UICONTROL 保存]** 活动。 在发布组合时，一个受众将在 Adobe Experience Platform 针对每个路径进行保存。

可以使用两种类型的拆分操作：

* **[!UICONTROL 百分比拆分]**:将用户档案随机拆分为两个或多个路径。 例如，您可以将用户档案拆分为2个不同的路径，每个路径50%。 <!--and add an additional path for control group.-->

   ![](assets/audiences-split-percentage.png)

* **[!UICONTROL 属性拆分]**:根据特定属性拆分用户档案。 在此示例中，我们将根据用户档案的文件室类型首选项来拆分用户档案。

   ![](assets/audiences-split.png)

   >[!NOTE]
   >
   >的 **[!UICONTROL 其他用户档案]** 选项允许您使用其余配置文件创建其他路径，这些路径与其他路径中指定的任何条件都不匹配。

## 保存受众 {#save}

配置将保存到Adobe Experience Platform中的结果受众。

为此，请选择 **[!UICONTROL 保存受众]** 活动，然后指定要创建的新受众的名称。

![](assets/audiences-publish.png)

合成准备就绪后，即可发布它。 [了解如何创建合成](create-compositions.md)
