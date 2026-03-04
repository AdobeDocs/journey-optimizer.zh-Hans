---
solution: Journey Optimizer
product: journey optimizer
title: 管理品牌
description: 了解如何创建和管理创新型模型
topic: Content Management
role: User
level: Beginner, Intermediate
exl-id: 9ef6b02c-0a17-4b46-bcd3-8e922eef059a
source-git-commit: 7873c333cbe5002695a11d1edaaf9e15f74a6d3f
workflow-type: tm+mt
source-wordcount: '477'
ht-degree: 0%

---

# 创建和管理创成模型 {#generative-models}

通过内置模型、自定义Firefly模型和第三方图像生成提供商扩展您的AI图像创建功能，以满足您的特定需求并改善品牌一致性。

根据您的需求选择合适的模型：

- **[!UICONTROL Adobe模型]**&#x200B;由Firefly Image Model 4提供支持，现成可用，无需其他设置即可立即生成图像。
- 由Gemini 2.5 Flash支持的&#x200B;**[!UICONTROL 合作伙伴模型]**&#x200B;提供了针对特定用例的专门功能。
- **[!UICONTROL 自定义模型]**&#x200B;是在您自己的资产上训练并由您的组织添加的特定于品牌的模型。

  在&#x200B;**[!UICONTROL Adobe Firefly文档]**&#x200B;中了解有关[自定义模型](https://helpx.adobe.com/firefly/web/work-with-enterprise-features/train-custom-models/custom-models-overview.html)的更多信息

配置完毕后，即可在内容中创建图像时选择任何创成模型。 [了解有关生成图像的更多信息](generative-image.md)。

## 管理创成模型

从集中位置管理您的创成模型。 查看所有可用模型，进行筛选和搜索以查找特定模型，并为您的品牌配置其设置。

1. 从&#x200B;**[!UICONTROL 品牌]**&#x200B;菜单中，选择&#x200B;**[!UICONTROL 生成模型]**&#x200B;选项卡。

   ![](assets/gen-model-manage-1.png){zoomable="yes"}

1. 单击![](assets/do-not-localize/Smock_Filter_18_N.svg)图标以访问筛选器菜单。 按&#x200B;**[!UICONTROL 类型]**&#x200B;或&#x200B;**[!UICONTROL 状态]**&#x200B;筛选模型。

   ![](assets/gen-model-manage-2.png){zoomable="yes"}

1. 使用搜索栏按名称查找特定的生成模型。

1. 单击![](assets/do-not-localize/Smock_More_18_N.svg)图标可访问高级菜单，您可以在其中启用或禁用模型，或者删除模型。

   请注意，只能删除&#x200B;**[!UICONTROL 自定义模型]**。

   ![](assets/gen-model-manage-6.png){zoomable="yes"}

1. 单击&#x200B;**[!UICONTROL 添加模型]**&#x200B;从头开始创建新的生成模型。

现在，在内容中创建图像时，可以选择任何创成模型。 [了解有关生成图像的更多信息](generative-image.md)。

## 添加生成模型

>[!IMPORTANT]
>
>创建自定义Firefly模型需要Firefly ETLA协议。

自定义Firefly模型是在您自己的资产上经过训练的特定于品牌的AI模型，使您能够生成与您的品牌标识、风格和视觉准则完全一致的图像。

通过创建自定义Firefly模型提供程序，您可以将AI功能扩展到默认模型之外，并确保生成的内容始终反映您品牌独特的美学和要求。

➡️ [了解如何训练您的自定义模型](https://helpx.adobe.com/firefly/web/work-with-enterprise-features/train-custom-models/train-firefly-custom-models.html)

1. 从&#x200B;**[!UICONTROL 品牌]**&#x200B;菜单中，访问&#x200B;**[!UICONTROL 生成模型]**&#x200B;选项卡，然后单击&#x200B;**[!UICONTROL 添加模型]**。

   ![](assets/gen-model-manage-4.png){zoomable="yes"}

1. 输入模型的&#x200B;**[!UICONTROL 名称]**。

1. 输入您的&#x200B;**[!UICONTROL 模型ID]**。

   +++ 查找您的Firefly模型ID

   1. 访问Firefly网站并导航到经过训练的模型。
   1. 访问[预览和测试](https://helpx.adobe.com/firefly/web/work-with-enterprise-features/train-custom-models/train-firefly-custom-models.html#preview-and-test)菜单。
   1. 在URL中，找到`customModelId=`之后的值。 复制此值以用作模型ID。

   有关详细信息，请参阅[Firefly自定义模型文档](https://helpx.adobe.com/firefly/web/work-with-enterprise-features/train-custom-models/manage-custom-models.html)。

   ![](assets/gen-model-manage-10.png){zoomable="yes"}

   +++

   </br>

   ![](assets/gen-model-manage-5.png){zoomable="yes"}

1. 或者，输入&#x200B;**[!UICONTROL 描述]**&#x200B;以帮助识别模型。

1. 单击&#x200B;**[!UICONTROL 测试连接]**&#x200B;以验证模型配置。

1. 连接测试成功后，单击&#x200B;**[!UICONTROL 保存]**&#x200B;以保存模型配置。

   ![](assets/gen-model-manage-7.png){zoomable="yes"}

1. 保存后，您的自定义模型将添加到模型列表。 您可以随时禁用或删除它。

   ![](assets/gen-model-manage-8.png){zoomable="yes"}

<!--
1. Once the connection test is successful, choose whether to enable the model for selected brands.

1. Enable or disable the option to connect the model to all brands.

    If disabled, select which brands this model should be applied to.
-->

配置完毕后，您可以在内容中创建图像时选择任何自定义生成模型。 [了解有关生成图像的更多信息](generative-image.md)。

![](assets/gen-model-manage-9.png){zoomable="yes"}
