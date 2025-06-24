---
title: 决策规则
description: 了解如何使用决策规则
feature: Decisioning
topic: Integrations
role: User
level: Intermediate
exl-id: 033a11b8-c848-4e4a-b6f0-62fa0a2152bf
source-git-commit: ebefeb59a19e831ec7f86cee690a35fe71e14554
workflow-type: tm+mt
source-wordcount: '515'
ht-degree: 20%

---

# 决策规则 {#rules}

>[!CONTEXTUALHELP]
>id="ajo_exd_config_rules"
>title="创建决策规则"
>abstract="决策规则使您可通过直接在决策项级别或在特定选择策略中应用约束而定义决策项的受众。这样可精确地控制应向谁显示哪些项。"

## 关于决策规则 {#about}

决策规则使您可通过直接在决策项级别或在特定选择策略中应用约束而定义决策项的受众。这样可精确地控制应向谁显示哪些项。

例如，我们考虑一个方案，其中您的决策项包含为女性设计的瑜伽相关产品。 通过决策规则，您可以指定只向性别为“女性”并在“瑜伽”中指定了“兴趣点”的用户档案显示这些项目。

>[!NOTE]
>
>除了项目和选择策略级别决策规则之外，您还可以在营销活动级别定义预期受众。 [了解详情](../campaigns/create-campaign.md#audience)

决策规则列表可在&#x200B;**[!UICONTROL 策略设置]**&#x200B;菜单中访问。

![](assets/decision-rules-list.png)

## 创建决策规则 {#create}

要创建决策规则，请执行以下步骤：

1. 导航到&#x200B;**[!UICONTROL 策略设置]** / **[!UICONTROL 决策规则]**，然后单击&#x200B;**[!UICONTROL 创建规则]**&#x200B;按钮。

   >[!NOTE]
   >
   >您还可以使用来自Adobe Experience Platform的数据通过外部数据扩充您的决策逻辑。 这对于经常更改的属性（如产品可用性或实时定价）特别有用。 此功能目前为公开 Beta 版，可供所有客户使用。如果您希望获得访问权限，请联系您的客户代表。 [了解如何将Adobe Experience Platform数据用于决策](../experience-decisioning/aep-data-exd.md)

1. 此时将打开决策规则创建屏幕。 命名规则并提供描述。

1. 使用Adobe Experience Platform区段生成器构建决策规则以满足您的需求。 为此，您可以利用各种数据源，例如：
   * 配置文件和决策项目属性，
   * 受众，
   * 上下文数据来自Adobe Experience Platform。 [了解如何利用上下文数据](context-data.md)

   ![](assets/decision-rules-build.png)

   >[!NOTE]
   >
   >与Adobe Experience Platform Segmentation服务中使用的区段生成器相比，为创建决策规则而提供的区段生成器具有一些特性。 但是，文档中描述的全球流程对于构建决策规则仍然有效。 [了解如何生成区段定义](../audience/creating-a-segment-definition.md)

1. 在工作区中添加和配置新字段时，**[!UICONTROL 受众属性]**&#x200B;窗格显示有关属于受众的估计配置文件的信息。 单击&#x200B;**[!UICONTROL 刷新估算]**&#x200B;以更新数据。

   >[!NOTE]
   >
   >当规则参数包含不在配置文件中的数据（如上下文数据）时，配置文件估计不可用。

1. 决策规则准备就绪后，单击&#x200B;**[!UICONTROL 保存]**。 创建的规则将显示在列表中，并可用于决策项和选择策略中，以控制将决策项呈现给用户档案。

   >[!NOTE]
   >
   >资格规则中的嵌套深度限制为30个级别。 这是通过计数PQL字符串中的`)`个右括号来测量的。 对于UTF-8编码字符，规则字符串的大小最多可达15KB。 这相当于15,000个ASCII字符（每个1字节），或3,750-7,500个非ASCII字符（每个2-4字节）。 [了解有关Decisioning护栏和限制的更多信息](gs-experience-decisioning.md#guardrails)
