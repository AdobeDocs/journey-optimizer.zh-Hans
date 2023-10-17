---
title: 创建基于代码的体验
description: 了解如何在Journey Optimizer中创建基于代码的体验
feature: Offers
topic: Content Management
role: User
level: Experienced
hide: true
hidefromtoc: true
badge: label="Beta 版"
exl-id: 25c2c448-9380-47b0-97c5-16d9afb794c5
source-git-commit: 0eec7788aa8292843812eba0282ea5219b5711df
workflow-type: tm+mt
source-wordcount: '1009'
ht-degree: 11%

---

# 创建基于代码的体验 {#create-code-based}

>[!BEGINSHADEBOX]

本文档指南包括以下内容：

* [开始使用基于代码的渠道](get-started-code-based.md)
* [基于代码的先决条件](code-based-prerequisites.md)
* [基于代码的实施示例](code-based-implementation-samples.md)
* **[创建基于代码的体验](create-code-based.md)**

>[!ENDSHADEBOX]

>[!AVAILABILITY]
>
>基于代码的渠道目前仅作为 Beta 版供部分用户使用。要加入 Beta 版计划，请联系 Adobe 客户关怀团队。

## 创建基于代码的营销活动 {#create-code-based-campaign}

要通过营销活动开始构建基于代码的体验，请执行以下步骤。

>[!CAUTION]
>
>当前位置 [!DNL Journey Optimizer] 您只能使用以下方式创建基于代码的体验 **营销活动**.

1. 创建营销活动. [了解详情](../campaigns/create-campaign.md)

1. 选择 **[!UICONTROL 基于代码的体验（测试版）]** 操作。

1. 输入基于代码的体验平面。 [了解详情](#surface-definition)

   ![](assets/code-based-campaign-surface.png)

   >[!CAUTION]
   >
   >确保在基于代码的营销活动中使用的表面URI与您自己的实施中使用的表面URI相匹配。 否则，将不会交付更改。

1. 选择&#x200B;**[!UICONTROL 创建]**。

1. 完成创建营销策划的步骤，如营销策划属性， [受众](../audience/about-audiences.md)、和 [计划](../campaigns/create-campaign.md#schedule).

   >[!NOTE]
   >
   >有关如何配置营销活动的更多信息，请参阅 [此页面](../campaigns/get-started-with-campaigns.md).

1. 使用表达式编辑器根据需要编辑内容。 [了解详情](#edit-code)

   ![](assets/code-based-campaign-edit-content.png)

## 编辑代码内容 {#edit-code}

>[!CONTEXTUALHELP]
>id="ajo_code_based_experience"
>title="使用表达式编辑器"
>abstract="插入和编辑要作为此基于代码的体验操作的一部分提供的代码。"
>additional-url="https://experienceleague.adobe.com/docs/journey-optimizer/using/content-management/personalization/expression-editor/personalization-build-expressions.html" text="开始使用表达式编辑器"

1. 从促销活动版本屏幕中，选择 **[!UICONTROL 编辑代码]**.

   ![](assets/code-based-campaign-edit-code.png)

1. 此 [表达式编辑器](../personalization/personalization-build-expressions.md) 打开。 它是一个非可视化体验创建界面，允许您创作代码。

1. 您可以将创作模式从HTML切换到JSON，反之亦然。

   >[!CAUTION]
   >
   >更改创作模式将导致当前代码全部丢失，因此，请确保在开始创作之前切换模式。

1. 根据需要输入代码。 您可以利用 [!DNL Journey Optimizer] 具有所有个性化和创作功能的表达式编辑器。 [了解详情](../personalization/personalization-build-expressions.md)

   ![](assets/code-based-campaign-code-editor.png)

1. 在基于代码的营销活动中，您可以使用Experience Decisioning功能。 选择 **[!UICONTROL 决策]** 图标，然后单击 **[!UICONTROL 创建决策]**. [了解详情](../experience-decisioning/create-decision.md)

   ![](assets/code-based-campaign-create-decision.png)

   >[!NOTE]
   >
   >experience decisioning功能目前仅作为测试版向部分用户提供。

1. 单击 **[!UICONTROL 保存并关闭]** 以确认更改。

现在，开发人员执行API或SDK调用以获取所选表面的内容后，更改将立即应用于您的网页或应用程序。

## 测试基于代码的营销活动 {#test-code-based-campaign}

>[!CONTEXTUALHELP]
>id="ajo_code_based_preview"
>title="预览基于代码的体验"
>abstract="模拟基于代码的体验将看起来是什么样。"

要显示已修改的基于代码的体验的预览，请执行以下步骤。

>[!CAUTION]
>
>您必须具有可用的测试用户档案，以模拟将向他们投放哪些优惠。 了解如何 [创建测试用户档案](../audience/creating-test-profiles.md).

1. 从表达式编辑器或编辑内容屏幕中，选择 **[!UICONTROL 模拟内容]**.

   ![](assets/code-based-campaign-simulate.png)

1. 单击 **[!UICONTROL 管理测试用户档案]** 选择一个或多个测试用户档案。

1. 此时将显示已修改的基于代码的体验预览。

<!--
    ![](assets/code-based-designer-preview.png)

    You can also open it in the default browser, or copy the test URI to paste it in any browser. This allows you to share the link with your team and stakeholders who will be able to preview the new web experience in any browser before the campaign goes live.

    When copying the test URI, the content displayed is the one personalized for the test profile used when the content simulation was generated in [!DNL Journey Optimizer].-->

## 激活基于代码的营销活动 {#activate-code-based-campaign}

定义基于代码的营销活动并根据需要使用 [基于代码的编辑器](#edit-code)，您可以查看并激活它。 请按照以下步骤操作。

>[!NOTE]
>
>您还可以在激活促销活动内容之前对其进行预览。 [了解详情](#test-code-based-campaign)

1. 从基于代码的营销活动中，选择 **[!UICONTROL 审查以激活]**.

   ![](assets/code-based-campaign-review.png)

1. 检查并编辑内容、属性、界面、受众和计划（如果需要）。

1. 选择 **[!UICONTROL 激活]**.

   ![](assets/code-based-campaign-activate.png)

   >[!NOTE]
   >
   >单击之后 **[!UICONTROL 激活]**，基于代码的营销活动更改可能最多需要1分钟才能在您的网站上实时可用。

您的基于代码的营销活动会采用 **[!UICONTROL 实时]** 状态，并且现在对选定的受众可见。 营销活动的每个收件人都可以看到您的修改。

>[!NOTE]
>
>如果您为基于代码的促销活动定义了计划，则它具有 **[!UICONTROL 已计划]** 状态直到达到开始日期和时间。
>
>如果您激活的基于代码的活动与另一个已上线的活动影响相同的位置，则所有更改都将应用于您的位置。

了解更多有关在中激活营销活动的信息 [本节](../campaigns/review-activate-campaign.md).

## 停止基于代码的营销活动 {#stop-code-based-campaign}

当基于代码的营销活动处于实时状态时，您可以停止它以防止受众看到您的修改。 请按照以下步骤操作。

1. 从列表中选择一个实时营销活动。

1. 从顶部菜单中，选择 **[!UICONTROL 停止营销活动]**.

   ![](assets/code-based-campaign-stop.png)

1. 您添加的修改将不再对您定义的受众可见。

>[!NOTE]
>
>基于代码的营销活动一旦停止，您就无法再次编辑或激活它。 您只能复制它并激活重复的行销活动。

## 基于代码的营销活动报表

您可以从营销活动摘要屏幕访问基于代码的营销活动报表。

全局报告显示至少两个小时前发生的事件，并涵盖选定时间段内的事件。 相比之下，实时报表侧重于过去24小时内发生的事件，距事件发生的最小时间间隔为2分钟。

### 基于代码的实时报告 {#live-report-code-based}

来自您的营销活动 **[!UICONTROL 实时报告]**， **[!UICONTROL 基于代码的体验]** 选项卡详细介绍与您的应用程序或网页相关的主要信息。 [了解有关实时报告的更多信息](../reports/campaign-live-report.md)

+++了解有关基于代码的体验报表可用的不同量度和小组件的更多信息。

此 **[!UICONTROL 基于代码的体验性能]** KPI可详细列出与访客参与基于代码的体验相关的主要信息，例如：

* **[!UICONTROL 展示次数]**：交付给所有用户的体验总数。

* **[!UICONTROL 交互]**：与应用程序/页面的互动总数。 这包括用户执行的任何操作，例如点击或任何其他交互。

此 **[!UICONTROL 基于代码的体验摘要]** 图表显示过去24小时内您的体验（展示次数、独特展示次数和交互）的演变。

<!--The **[!UICONTROL Interactions by element]** table details the main information relative to your visitors' engagement with the various elements on your app/pages.-->
+++

### 基于代码的全局报告 {#global-report-code-based}

您可以使用直接从营销活动中访问基于代码的营销活动全局报表 **[!UICONTROL 查看报告]** 按钮。 [了解关于全局报告的更多信息](../reports/campaign-global-report.md)

来自您的营销活动 **[!UICONTROL 全局报告]**， **[!UICONTROL 基于代码的体验]** 选项卡详细介绍与您的应用程序或网页相关的主要信息。

![](assets/code-based-campaign-global-report.png)

<!--image-->

+++了解有关基于代码的体验报表可用的不同量度和小组件的更多信息。

此 **[!UICONTROL 基于代码的体验性能]** KPI可详细列出与访客对您体验的参与度相关的主要信息，例如：

* **[!UICONTROL 独特展示次数]**：将体验交付给的独特用户数。

* **[!UICONTROL 展示次数]**：交付给所有用户的体验总数。

* **[!UICONTROL 交互]**：与您的应用程序/页面互动的百分比。 这包括用户执行的任何操作，例如点击或任何其他交互。

此 **[!UICONTROL 基于代码的体验摘要]** 图形可显示相关时间段内您的体验（独特展示次数、展示次数和交互）的演变。

<!--The **[!UICONTROL Interactions by element]** table details the main information relative to your visitors' engagement with the various elements on your apps/pages.-->
+++

<!--
## How-to video{#video}

The video below shows how to create a code-based campaign, configure its properties, review, and publish it.

>[!VIDEO]()

-->
