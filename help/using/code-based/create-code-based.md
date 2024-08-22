---
title: 创建基于代码的体验
description: 了解如何在Journey Optimizer中创建基于代码的体验
feature: Code-based Experiences
topic: Content Management
role: User
level: Experienced
exl-id: 25c2c448-9380-47b0-97c5-16d9afb794c5
source-git-commit: b9208544b08b474db386cce3d4fab0a4429a5f54
workflow-type: tm+mt
source-wordcount: '1083'
ht-degree: 9%

---

# 创建基于代码的体验 {#create-code-based}

当前在[!DNL Journey Optimizer]中，您只能在&#x200B;**营销活动**&#x200B;中创建基于代码的体验。

要详细了解有关基于代码的体验的特定护栏和建议，请参阅[此页面](code-based-prerequisites.md)。

## 创建基于代码的营销活动 {#create-code-based-campaign}

要通过营销活动开始构建基于代码的体验，请执行以下步骤。

1. 访问&#x200B;**[!UICONTROL 营销活动]**&#x200B;菜单，然后单击&#x200B;**[!UICONTROL 创建营销活动]**。 [了解详情](../campaigns/create-campaign.md)

1. 选择要执行的营销活动类型

   * **已计划 — 营销**：立即或在指定日期执行营销活动。 计划的营销活动旨在发送营销消息。 它们从用户界面配置和执行。

   * **API触发 — 营销/事务性**：使用API调用执行营销活动。 API触发的营销活动旨在发送营销或事务型消息，即，在个人执行操作（密码重置、购物车购买等）之后发送的消息。

1. 完成步骤以创建营销活动，如营销活动属性、[受众](../audience/about-audiences.md)和[计划](../campaigns/create-campaign.md#schedule)。 有关如何配置营销活动的详细信息，请参阅[此页面](../campaigns/get-started-with-campaigns.md)。

1. 选择&#x200B;**[!UICONTROL 基于代码的体验]**&#x200B;操作。

1. 选择或创建基于代码的体验配置。 [了解详情](code-based-configuration.md)

   ![](assets/code-based-campaign-surface.png)

1. 使用个性化编辑器，根据需要编辑您的内容。 [了解详情](#edit-code)

   ![](assets/code-based-campaign-edit-content.png)

## 编辑代码内容 {#edit-code}

>[!CONTEXTUALHELP]
>id="ajo_code_based_experience"
>title="使用个性化编辑器"
>abstract="插入和编辑要作为此基于代码的体验操作的一部分提供的代码。"
>additional-url="https://experienceleague.adobe.com/docs/journey-optimizer/using/content-management/personalization/expression-editor/personalization-build-expressions.html?lang=zh-Hans" text="开始使用个性化编辑器"

1. 从促销活动版本屏幕中，选择&#x200B;**[!UICONTROL 编辑代码]**。

   ![](assets/code-based-campaign-edit-code.png)

1. [个性化编辑器](../personalization/personalization-build-expressions.md)打开。 它是一个非可视化体验创建界面，允许您创作代码。

1. 您可以将创作模式从HTML切换到JSON，反之亦然。

   ![](assets/code-based-campaign-code-editor.png)

   >[!CAUTION]
   >
   >更改创作模式将导致当前代码全部丢失，因此，请确保在开始创作之前切换模式。

1. 根据需要输入代码。 您可以利用[!DNL Journey Optimizer]个性化编辑器及其所有个性化和创作功能。 [了解详情](../personalization/personalization-build-expressions.md)

1. 您可以根据需要添加HTML或JSON表达式片段。 [了解如何操作](../personalization/use-expression-fragments.md)

   您还可以将部分代码内容另存为片段。 [了解如何操作](../content-management/fragments.md#save-as-expression-fragment)

1. 在基于代码的营销活动中，您可以使用Experience Decisioning功能。 从左栏中选择&#x200B;**[!UICONTROL 决策]**&#x200B;图标，然后单击&#x200B;**[!UICONTROL 创建决策]**。 [了解详情](../experience-decisioning/create-decision.md)

   ![](assets/code-based-campaign-create-decision.png)

   >[!NOTE]
   >
   >目前，体验决策功能仅面向一部分组织提供（限量发布版）。要获得访问权限，请与 Adobe 代表联系。


1. 单击&#x200B;**[!UICONTROL 保存并关闭]**&#x200B;以确认更改。

现在，一旦您的开发人员进行API或SDK调用以获取渠道配置中定义的表面的内容，更改就会应用于您的网页或应用程序。

## 测试基于代码的营销活动 {#test-code-based-campaign}

>[!CONTEXTUALHELP]
>id="ajo_code_based_preview"
>title="预览基于代码的体验"
>abstract="模拟基于代码的体验将看起来是什么样。"

要显示已修改的基于代码的体验的预览，请执行以下步骤。 有关如何选择测试用户档案和预览内容的详细信息，请参阅[预览和测试内容页面](../content-management/preview-test.md)。

>[!CAUTION]
>
>您必须具有可用的测试用户档案，以模拟将向他们投放哪些优惠。 了解如何[创建测试配置文件](../audience/creating-test-profiles.md)。

1. 从个性化编辑器或编辑内容屏幕中，选择&#x200B;**[!UICONTROL 模拟内容]**。

   ![](assets/code-based-campaign-simulate.png)

1. 单击&#x200B;**[!UICONTROL 管理测试配置文件]**&#x200B;以选择一个或多个测试配置文件。

1. 此时将显示已修改的基于代码的体验预览。

<!--
    ![](assets/code-based-designer-preview.png)

    You can also open it in the default browser, or copy the test URI to paste it in any browser. This allows you to share the link with your team and stakeholders who will be able to preview the new web experience in any browser before the campaign goes live.

    When copying the test URI, the content displayed is the one personalized for the test profile used when the content simulation was generated in [!DNL Journey Optimizer].-->

## 激活基于代码的营销活动 {#activate-code-based-campaign}

定义基于代码的营销活动并根据需要使用[基于代码的编辑器](#edit-code)编辑内容后，您可以查看和激活该营销活动。 请按照以下步骤操作。

>[!NOTE]
>
>您还可以在激活促销活动内容之前对其进行预览。 [了解详情](#test-code-based-campaign)

1. 从基于代码的营销活动中，选择&#x200B;**[!UICONTROL 审阅以激活]**。

   ![](assets/code-based-campaign-review.png)

1. 检查并编辑内容、属性、配置、受众和计划（如果需要）。

1. 选择&#x200B;**[!UICONTROL 激活]**。

   ![](assets/code-based-campaign-activate.png)

   >[!NOTE]
   >
   >单击&#x200B;**[!UICONTROL 激活]**&#x200B;后，可能需要长达1分钟时间，基于代码的营销活动更改才可在您的位置上实时可用。

您的基于代码的营销活动处于&#x200B;**[!UICONTROL 实时]**&#x200B;状态，现在对所选受众可见。 营销活动的每个收件人都可以看到您的修改。

>[!NOTE]
>
>如果您为基于代码的营销活动定义了计划，则在到达开始日期和时间之前，该计划的状态为&#x200B;**[!UICONTROL 已计划]**。
>
>如果您激活的基于代码的活动与另一个已上线的活动影响相同的位置，则所有更改都将应用于您的位置。

在[此部分](../campaigns/review-activate-campaign.md)中了解关于激活营销活动的更多信息。

## 停止基于代码的营销活动 {#stop-code-based-campaign}

当基于代码的营销活动处于实时状态时，您可以停止它以防止受众看到您的修改。 请按照以下步骤操作。

1. 从列表中选择一个实时营销活动。

1. 从顶部菜单中选择&#x200B;**[!UICONTROL 停止营销活动]**。

   ![](assets/code-based-campaign-stop.png)

1. 您添加的修改将不再对您定义的受众可见。

>[!NOTE]
>
>基于代码的营销活动一旦停止，您就无法再次编辑或激活它。 您只能复制它并激活重复的行销活动。

## 基于代码的营销活动报表

您可以从营销活动摘要屏幕访问基于代码的营销活动报表。

全局报告显示至少两个小时前发生的事件，并涵盖选定时间段内的事件。 相比之下，实时报表侧重于过去24小时内发生的事件，距事件发生的最小时间间隔为2分钟。

### 基于代码的实时报告 {#live-report-code-based}

在营销活动&#x200B;**[!UICONTROL 实时报告]**&#x200B;中，**[!UICONTROL 基于代码的体验]**&#x200B;选项卡详细介绍了与您的应用程序或网页相关的主要信息。 [了解有关实时报告的更多信息](../reports/campaign-live-report.md)

+++了解有关基于代码的体验报表可用的不同量度和小组件的更多信息。

**[!UICONTROL 基于代码的体验效果]** KPI详细列出了与访客与基于代码的体验的参与度相关的主要信息，例如：

* **[!UICONTROL 展示次数]**：交付给所有用户的体验总数。

* **[!UICONTROL 交互]**：与应用程序/页面的预订总数。 这包括用户执行的任何操作，例如点击或任何其他交互。

**[!UICONTROL 基于代码的体验摘要]**&#x200B;图形显示了过去24小时内您的体验（展示次数、唯一展示次数和交互）的演变。

<!--The **[!UICONTROL Interactions by element]** table details the main information relative to your visitors' engagement with the various elements on your app/pages.-->
+++

### 基于代码的全局报告 {#global-report-code-based}

使用&#x200B;**[!UICONTROL 查看报告]**&#x200B;按钮，可以直接从营销活动访问基于代码的营销活动全局报告。 [了解有关全局报告的更多信息](../reports/campaign-global-report.md)

在促销活动&#x200B;**[!UICONTROL 全局报告]**&#x200B;中，**[!UICONTROL 基于代码的体验]**&#x200B;选项卡详细介绍了与您的应用程序或网页相关的主要信息。

![](assets/code-based-campaign-global-report.png)

<!--image-->

+++了解有关基于代码的体验报表可用的不同量度和小组件的更多信息。

**[!UICONTROL 基于代码的体验效果]** KPI详细列出了与访客与您的体验的参与度相关的主要信息，例如：

* **[!UICONTROL 独特展示次数]**：体验交付给的独特用户数。

* **[!UICONTROL 展示次数]**：交付给所有用户的体验总数。

* **[!UICONTROL 交互]**：与您的应用程序/页面的互动百分比。 这包括用户执行的任何操作，例如点击或任何其他交互。

**[!UICONTROL 基于代码的体验摘要]**&#x200B;图形显示了相关时间段内您的体验（独特展示次数、展示次数和交互）的演变。

<!--The **[!UICONTROL Interactions by element]** table details the main information relative to your visitors' engagement with the various elements on your apps/pages.-->
+++

<!--
## How-to video{#video}

The video below shows how to create a code-based campaign, configure its properties, review, and publish it.

>[!VIDEO]()

-->
