---
title: 决策规则
description: 了解如何使用决策规则
feature: Experience Decisioning
topic: Integrations
role: User
level: Intermediate
hide: true
hidefromtoc: true
badge: label="Beta 版"
exl-id: 033a11b8-c848-4e4a-b6f0-62fa0a2152bf
source-git-commit: 29228a17176421ccf29598d6ebba815b800db7a2
workflow-type: tm+mt
source-wordcount: '652'
ht-degree: 16%

---

# 决策规则 {#rules}

>[!CONTEXTUALHELP]
>id="ajo_exd_config_rules"
>title="创建决策规则"
>abstract="决策规则使您可通过直接在决策项级别或在特定选择策略中应用约束而定义决策项的受众。这样可精确地控制应向谁显示哪些项。"

>[!BEGINSHADEBOX “您将在本文档指南中找到什么”]

* [开始使用 Experience Decisioning](gs-experience-decisioning.md)
* 管理您的决策项目： [配置物料目录](catalogs.md) - [创建决策项目](items.md) - [管理物料集合](collections.md)
* 配置项目的选择： **[创建决策规则](rules.md)** - [创建排名方法](ranking.md)
* [创建选择策略](selection-strategies.md)
* [创建决策策略](create-decision.md)

>[!ENDSHADEBOX]

决策规则使您可通过直接在决策项级别或在特定选择策略中应用约束而定义决策项的受众。这样可精确地控制应向谁显示哪些项。

例如，我们考虑一个方案，其中您的决策项包含为女性设计的瑜伽相关产品。 通过决策规则，您可以指定只向性别为“女性”并在“瑜伽”中指定了“兴趣点”的用户档案显示这些项目。

>[!NOTE]
>
>除了项目和选择策略级别决策规则之外，您还可以在营销活动级别定义预期受众。 [了解详情](../campaigns/create-campaign.md#audience)

决策规则的列表可在 **[!UICONTROL 配置]** / **[!UICONTROL 决策规则]** 菜单。

![](assets/decision-rules-list.png)

## 创建决策规则 {#create}

要创建决策规则，请执行以下步骤：

1. 导航到 **[!UICONTROL 配置]** / **[!UICONTROL 决策规则]** 然后单击 **[!UICONTROL 创建规则]** 按钮。

1. 此时将打开决策规则创建屏幕。 命名规则并提供描述。

1. 使用Adobe Experience Platform区段生成器构建决策规则以满足您的需求。 为此，Tou可以利用各种数据源，例如来自Adobe Experience Platform的用户档案属性、受众或上下文数据。 [了解如何在决策规则中利用上下文数据](#context-data)

   ![](assets/decision-rules-build.png)

   >[!NOTE]
   >
   >与Adobe Experience Platform Segmentation服务中使用的区段生成器相比，为创建决策规则而提供的区段生成器具有一些特性。  但是，文档中描述的全球流程对于构建决策规则仍然有效。 [了解如何构建区段定义](../audience/creating-a-segment-definition.md)

1. 当您在工作区中添加和配置新字段时， **[!UICONTROL 受众属性]** 窗格显示有关属于受众的预计用户档案的信息。 单击 **[!UICONTROL 刷新估计]** 以更新数据。

   >[!NOTE]
   >
   >当规则参数包含不在配置文件中的数据（如上下文数据）时，配置文件估计不可用。

1. 决策规则就绪后，单击 **[!UICONTROL 保存]**. 创建的规则将显示在列表中，并可用于决策项和选择策略中，以控制将决策项呈现给用户档案。

## 在决策规则中利用上下文数据 {#context-data}

通过Experience Decisioning规则创建屏幕，可利用Adobe Experience Platform中的任何可用信息来创建决策规则。 例如，您可以设计一个决策规则，要求当前天气为≥80度。

为此，您首先需要定义要在Experience Decisioning中可用的数据。 完成后，此数据将无缝集成到中的Experience Decisioning **[!UICONTROL 上下文数据]** 选项卡创建决策规则时可用。

![](assets/decision-rules-context.png)

使用Adobe Experience Platform数据馈送Experience Decisioning的步骤如下：

1. 创建 **体验事件架构**  Adobe Experience Platform及其关联的 **数据集**. [了解如何创建架构](https://experienceleague.adobe.com/en/docs/experience-platform/xdm/ui/resources/schemas){target="_blank"}

1. 创建新的Adobe Experience Platform数据流：

   1. 导航至 **[!UICONTROL 数据流]** 菜单并选择 **[!UICONTROL 新建数据流]**.

   1. 在 **[!UICONTROL 事件架构]** 从下拉列表中，选择之前创建的Experience Event架构，然后单击 **[!UICONTROL 保存]**.

      ![](assets/decision-rule-context-datastream.png)

   1. 单击 **[!UICONTROL 添加服务]** 并选择“Adobe Experience Platform”作为服务。 在 **[!UICONTROL 事件数据集]** 下拉列表中，选择之前创建的事件数据集，并启用 **[!UICONTROL Adobe Journey Optimizer]** 选项。

      ![](assets/decision-rules-context-datastream-service.png)

保存数据流后，所选数据集的信息将自动获取并集成到Experience Decisioning中，通常在大约24小时内变为可用。

有关如何使用Adobe Experience Platform的进一步指导，请探索以下资源：

* [体验数据模型(XDM)架构](https://experienceleague.adobe.com/en/docs/experience-platform/xdm/schema/composition){target="_blank"}
* [数据集](https://experienceleague.adobe.com/en/docs/experience-platform/catalog/datasets/overview){target="_blank"}
* [数据流](https://experienceleague.adobe.com/en/docs/experience-platform/datastreams/overview){target="_blank"}
