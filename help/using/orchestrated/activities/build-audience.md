---
solution: Journey Optimizer
product: journey optimizer
title: 使用“生成受众”活动
description: 了解如何在编排的活动中使用构建受众活动
exl-id: 3959b5fa-0c47-42a5-828f-4d7ca9b7e72d
version: Campaign Orchestration
TQID: https://experienceleague.adobe.com/9hEr5kAHco1iq8arv-FddaG3vm54CS-cPFUA63soeAg
product_v2: id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2: id: b3538224-471e-4c63-a444-9b19d89ae29c
subfeature_v2: id: b5e335a9-0e5f-4dda-8845-c4ac5dca2be4
source-git-commit: 18f6b23dbbe53e486e5af76ef7cc61fa1784475d
workflow-type: tm+mt
source-wordcount: 338
ht-degree: 56%

---

# 构建受众 {#build-audience}

>[!CONTEXTUALHELP]
>id="ajo_orchestration_build_audience"
>title="生成受众活动"
>abstract="您可以使用&#x200B;**构建受众**&#x200B;活动，定义哪些受众将进入精心编排的营销活动。 在精心编排的营销活动的上下文中发送消息时，消息受众不是在渠道活动中定义的，而是在&#x200B;**构建受众**&#x200B;活动中定义的。"

作为营销人员，您可以通过直观的界面创建复杂的受众区段，从而根据各种标准和行为来选择目标用户，从而更有效地定制营销活动。

为此，请使用&#x200B;**[!UICONTROL 生成受众]**&#x200B;目标选择活动。 此活动定义进入编排营销活动的受众。 在协调营销活动中发送消息时，受众是在&#x200B;**[!UICONTROL 构建受众]**&#x200B;活动中定义的，而不是在协调营销活动中定义的。

## 配置生成受众活动 {#build-audience-configuration}

>[!CONTEXTUALHELP]
>id="ajo_orchestration_build_audience_audienceselector"
>title="受众"
>abstract="选择您的受众，就像设计新投放时使用受众一样。"

请按照以下步骤配置&#x200B;**[!UICONTROL 生成受众]**&#x200B;活动：

1. 添加一个&#x200B;**[!UICONTROL 生成受众]**&#x200B;活动。

   ![](../assets/build-audience.png)

1. 定义一个&#x200B;**[!UICONTROL 标签]**。

1. 按照以下选项卡中详述的步骤配置受众。

1. 选择&#x200B;**[!UICONTROL 定位维度]**。 通过定向维度，您可以定义操作定向的群体：收件人、合同受益人、操作员、订阅者等。默认情况下，将从收件人中选择目标。

1. 单击&#x200B;**[!UICONTROL 继续]**。

1. 使用规则生成器定义查询。 [在本节中了解有关规则生成器的更多信息](../orchestrated-rule-builder.md)

1. 指定在受众为空时是否应生成出站过渡。

## 示例{#build-audience-examples}

以下是包含两个&#x200B;**[!UICONTROL 构建受众]**&#x200B;活动的编排营销活动的示例。 第一个以其购物车中放有商品的轮廓为目标，然后投放电子邮件。 第二个活动以具有心愿清单的轮廓为目标选择，随后投放短信。

![](../assets/build-audience-2.png)

在下面的示例中，**[!UICONTROL 构建受众]**&#x200B;活动使用规则生成器按其订阅计划筛选用户档案。 对`plan`属性设置了条件，以仅包含`plan = "basic"`的用户档案，从而在将受众传递给下一个活动之前，将受众范围缩小为基本层订阅者。

![](../assets/build-audience-plan.png){width="50%" align="left"}
