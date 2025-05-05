---
solution: Journey Optimizer
product: journey optimizer
title: 受众组合入门
description: 了解有关受众构图的更多信息
feature: Audiences, Profiles
topic: Content Management
role: User
level: Beginner
exl-id: af71d24d-77eb-44df-8216-b0aeaf4c4fa4
source-git-commit: 060d65e8d3fb1442b04626170a35d463d1faa514
workflow-type: tm+mt
source-wordcount: '1030'
ht-degree: 51%

---

# 受众组合入门 {#get-start-audience-composition}

>[!CONTEXTUALHELP]
>id="ajo_ao_create_composition"
>title="创建构成"
>abstract="创建一个构成工作流程，将现有的 Adobe Experience Platform 受众组合到一个可视画布中，并利用各种活动（拆分、排除等）来创建新的受众。"

>[!CONTEXTUALHELP]
>id="ajo_ao_publish"
>title="发布受众"
>abstract="发布您的构成，将生成的受众保存到 Adobe Experience Platform 中。"

>[!CONTEXTUALHELP]
>id="ajo_ao_audience"
>title="受众活动"
>abstract="受众活动让您可以在构成中包括属于现有受众的轮廓。"

>[!CONTEXTUALHELP]
>id="ajo_ao_merge_types"
>title="合并类型"
>abstract="指定应如何合并所选受众的轮廓。"

>[!CONTEXTUALHELP]
>id="ajo_ao_exclude_type"
>title="排除类型"
>abstract="使用“排除受众类型”排除属于现有受众的轮廓。“使用属性类型排除”让您可以根据特定属性来排除轮廓。"

>[!CONTEXTUALHELP]
>id="ajo_ao_exclude"
>title="排除活动"
>abstract="排除活动让您可以通过选择现有受众或使用规则，从构成中排除轮廓。"

>[!CONTEXTUALHELP]
>id="ajo_ao_enrich"
>title="扩充活动"
>abstract="使用“扩充活动”通过来自 Adobe Experience Platform 数据集的其他属性来扩充您的受众。例如，您可以添加与所购买产品相关的信息（例如名称、价格或制造商 ID），并利用这些信息对发送给受众的投放内容进行个性化设置。"

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
>abstract="从扩充数据集中选择一个或多个属性以关联到受众。构成在发布之后，这些属性就会与受众相关联，并且可以在 Journey Optimizer 营销活动中用来提供个性化的投放。"

>[!CONTEXTUALHELP]
>id="ajo_ao_ranking"
>title="排名活动"
>abstract="排名活动允许您根据特定属性对轮廓进行排名并将它们包含在构成中。例如，包含忠诚度积分最高的 50 个轮廓。"

>[!CONTEXTUALHELP]
>id="ajo_ao_rank_profilelimit_text"
>title="添加轮廓限制"
>abstract="打开此选项以指定要包含在构成中的轮廓最大数量。"

<!-- [!CONTEXTUALHELP]
>id="ajo_ao_control_group_text"
>title="Control Group"
>abstract="Use control groups to isolate a portion of the profiles. This allows you to measure the impact of a marketing activity and make a comparison with the behavior of the rest of the population."-->

>[!CONTEXTUALHELP]
>id="ajo_ao_split"
>title="拆分活动"
>abstract="拆分活动让您可以将构成拆分成多个路径。在发布构成时，一个受众将在 Adobe Experience Platform 针对每个路径进行保存。"

>[!CONTEXTUALHELP]
>id="ajo_ao_split_type"
>title="拆分类型"
>abstract="使用“百分比拆分类型”可将轮廓随机拆分到多个路径中。“属性拆分类型”让您可以根据特定属性来拆分轮廓。"

>[!CONTEXTUALHELP]
>id="ajo_ao_split_otherprofiles_text"
>title="其他轮廓"
>abstract="打开此选项可以创建一个附加路径，其中包含与其他路径中指定的任意条件都不匹配的剩余轮廓。"

>[!BEGINSHADEBOX]

此文档提供了有关如何在 Adobe Journey Optimizer 中使用受众组合的详细信息。如果您仅是 Real-time Customer Profile 客户并且没有使用 Adobe Journey Optimizer，请[单击此处](https://experienceleague.adobe.com/docs/experience-platform/segmentation/ui/audience-composition.html?lang=zh-Hans){target="_blank"}。

>[!ENDSHADEBOX]

受众组合允许您创建&#x200B;**组合工作流**，您可以在其中将现有Adobe Experience Platform受众组合到可视画布中，并利用各种活动（拆分、排除……）来创建新受众。

完成后，生成的&#x200B;**受众**&#x200B;将与现有受众一起保存到Adobe Experience Platform中，可以在Journey Optimizer营销活动和历程中利用它来定位客户。 了解如何在Journey Optimizer中定位受众
![](assets/audiences-process.png)

>[!IMPORTANT]
>
>* 受众构成中的受众和属性当前不能用于Healthcare Shield或Privacy and Security Shield。
>
>* 扩充属性尚未与策略实施服务集成。 因此，您应用于扩充属性的任何数据使用标签都不会在Journey Optimizer营销活动或历程中强制执行。

可通过 Adobe Journey Optimizer **[!UICONTROL 受众]**&#x200B;菜单访问受众组合：

![](assets/audiences-browse.png)

* **[!UICONTROL 概述]**&#x200B;选项卡提供了专用仪表板，其中包含与贵组织受众数据相关的关键量度。要了解更多信息，请参阅 [Adobe Experience Platform 仪表板指南](https://experienceleague.adobe.com/docs/experience-platform/dashboards/guides/segments.html?lang=zh-Hans)。

* **[!UICONTROL 浏览]**&#x200B;选项卡列出了存储到 Adobe Experience Platform 中的所有现有受众。

* 通过&#x200B;**[!UICONTROL 组合]**&#x200B;选项卡，您可以创建组合工作流程，并在其中合并和排列受众以创建新受众。

## 创建合成工作流 {#create}

要创建合成工作流，请执行以下步骤：

1. 访问&#x200B;**[!UICONTROL 受众]**&#x200B;菜单并选择&#x200B;**[!UICONTROL 创建受众]**。

1. 选择&#x200B;**[!UICONTROL 撰写受众]**。

   ![](assets/audiences-create.png)

1. 组合画布显示有两个默认活动：

   * **[!UICONTROL 受众]**：合成的起点。 此活动允许您选择一个或多个受众作为工作流的基础，

   * **[!UICONTROL 保存]**：合成的最后一步。 此活动用于将工作流结果保存到新受众中。

1. 打开合成属性以指定标题和描述。

   如果未在属性中定义标题，则排版标签将设置为“排版”，其后跟其创建日期和时间。

   ![](assets/audiences-properties.png)

1. 在&#x200B;**[!UICONTROL 受众]**&#x200B;和&#x200B;**[!UICONTROL 保存]**&#x200B;活动之间添加所需数量的活动，以配置合成。 有关如何创建合成的详细信息，请参阅[受众合成文档](https://experienceleague.adobe.com/en/docs/experience-platform/segmentation/ui/audience-composition)。

   ![](assets/audiences-publish.png)

1. 合成就绪后，单击&#x200B;**[!UICONTROL 发布]**&#x200B;按钮以发布合成并将生成的受众保存到Adobe Experience Platform中。

   >[!IMPORTANT]
   >
   >您最多可以在给定沙盒中发布10个合成。 如果您已达到此阈值，则需要删除组合以释放空间，然后才能发布新组合。

   如果在发布期间发生任何错误，将显示警报，其中包含有关如何解决该问题的信息。

   ![](assets/audiences-alerts.png)

1. 组合已发布。 生成的受众将保存到Adobe Experience Platform中，并准备好在Journey Optimizer中定位。 [了解如何在Journey Optimizer中定位受众](../audience/about-audiences.md#segments-in-journey-optimizer)

>[!NOTE]
>
>**受众合成**&#x200B;中的受众每天都会执行，因此您可能需要等待最多24小时才能在Journey Optimizer中使用它们。 受众构成受众中的丰富属性与上次构成运行一样新，过去最长可达24小时。

## 访问组合 {#access}

所有创建的合成都可以从&#x200B;**[!UICONTROL 合成]**&#x200B;选项卡访问。 您可以使用列表中的省略号按钮随时复制或删除现有合成。

构成可以有多种状态：

* **[!UICONTROL 草稿]**：构成正在进行中，尚未发布。
* **[!UICONTROL 已发布]**：构成已发布，生成的受众已保存并可使用。

![](assets/audiences-compositions.png)

>[!NOTE]
>
>受众合成当前未与沙盒重置功能集成。 在启动沙盒重置之前，您需要手动删除合成，以确保正确清理关联的受众数据。 有关详细信息，请参阅Adobe Experience Platform [沙盒文档](https://experienceleague.adobe.com/docs/experience-platform/sandbox/ui/user-guide.html#delete-audience-compositions)
