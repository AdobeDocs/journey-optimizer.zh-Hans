---
title: 创建 Web 体验
description: 了解如何在Journey Optimizer中创作网页并编辑其内容
feature: Web Channel
topic: Content Management
role: User
level: Beginner
exl-id: e28c038b-49ed-4685-bfe6-514116eb0711
source-git-commit: dd4173698d7034173b7ae9f44afec397d62a6f78
workflow-type: tm+mt
source-wordcount: '791'
ht-degree: 18%

---

# 创建 Web 体验 {#create-web}

[!DNL Journey Optimizer]允许您通过入站Web营销活动个性化您向客户提供的Web体验。

>[!CAUTION]
>
>这当前位于 [!DNL Journey Optimizer] 中，您只能使用&#x200B;**营销活动**&#x200B;创建 Web 体验。

[在此视频中了解如何创建Web营销活动](#video)

## 创建 Web 营销活动 {#create-web-campaign}

>[!CONTEXTUALHELP]
>id="ajo_web_surface"
>title="定义 Web 配置"
>abstract="Web 配置可以匹配单个页面 URL 或多个页面，这让您可以在一个或多个网页上传递内容修改。"

>[!CONTEXTUALHELP]
>id="ajo_web_surface_rule"
>title="构建页面匹配规则"
>abstract="一条页面匹配规则即可针对多个匹配同一规则的 URL - 例如，如果要将更改应用于跨越整个网站的主图横幅或添加在网站的所有产品页面上显示的置顶图像。"

要通过营销活动开始构建Web体验，请执行以下步骤。

>[!NOTE]
>
>如果您是首次创建 Web 体验，请确保遵循[此部分](web-prerequisites.md)中叙述的先决条件。

1. 访问&#x200B;**[!UICONTROL 营销活动]**&#x200B;菜单，然后单击&#x200B;**[!UICONTROL 创建营销活动]**。[了解详情](../campaigns/create-campaign.md)


1. 选择要执行的营销活动类型

   * **已计划 — 营销**：立即或在指定日期执行营销活动。 计划的营销活动旨在发送营销消息。 它们从用户界面配置和执行。

   * **API触发 — 营销/事务性**：使用API调用执行营销活动。 API触发的营销活动旨在发送营销或事务型消息，即，在个人执行操作（密码重置、购物车购买等）之后发送的消息。

1. 完成创建Web营销活动的步骤，例如营销活动属性、[受众](../audience/about-audiences.md)和[计划](../campaigns/create-campaign.md#schedule)。

1. 选择&#x200B;**[!UICONTROL Web]**&#x200B;操作。

1. 选择或创建新配置。 [了解有关Web配置的更多信息](web-configuration.md)

   ![](assets/web-campaign-steps.png)

有关如何配置营销活动的详细信息，请参阅[此页面](../campaigns/get-started-with-campaigns.md)。

## 测试 Web 营销活动 {#test-web-campaign}

>[!CONTEXTUALHELP]
>id="ajo_web_designer_preview"
>title="预览 Web 体验"
>abstract="模拟您将获得的 Web 体验。"

在使用Web设计器[创作Web体验](edit-web-content.md)后，您可以使用测试配置文件预览修改后的网页。 如果插入个性化内容，则可以使用测试配置文件数据检查此内容的显示方式。

为此，请从Web促销活动编辑内容屏幕或Web设计器中单击&#x200B;**[!UICONTROL 模拟内容]**，然后添加测试配置文件以使用测试配置文件数据检查网页。

![](assets/web-designer-preview.png)

您还可以在默认浏览器中打开它，或复制测试URL以将其粘贴到任何浏览器中。 这样，您就可以与团队和利益相关者共享链接，这些利益相关者将能够在营销活动上线之前在任何浏览器中预览新的Web体验。

>[!NOTE]
>
>在复制测试URL时，显示的内容是在[!DNL Journey Optimizer]中生成内容模拟时所使用的测试配置文件的个性化内容。

有关如何选择测试用户档案和预览内容的详细信息，请参阅[内容管理](../content-management/preview-test.md)部分。

## 激活Web活动 {#activate-web-campaign}

>[!IMPORTANT]
>
>从9月版开始，您可以通过新的营销活动和历程激活体验管理整个审批流程，确保营销活动和历程在正式启用之前由相应的利益相关者彻底审查和批准。 此功能在“有限可用”中可用。 [了解详情](../test-approve/gs-approval.md)

定义[Web营销活动设置](#configure-web-campaign)并根据需要使用[Web设计器](edit-web-content.md#work-with-web-designer)编辑内容后，您可以查看和激活您的Web营销活动。 请按照以下步骤操作。

<!--
>[!NOTE]
>
>You can also preview your web campaign content before activating it. [Learn more](#test-web-campaign)-->

1. 从您的Web营销活动中，选择&#x200B;**[!UICONTROL 审阅以激活]**。

1. 检查并编辑内容、属性、配置、受众和计划（如果需要）。

1. 选择&#x200B;**[!UICONTROL 激活]**。

   ![](assets/web-campaign-activate.png)

   >[!NOTE]
   >
   >单击“**[!UICONTROL 激活]**”后，可能需要长达15分钟时间，网站营销活动更改才能在您的网站上实时可用。

您的Web营销活动处于&#x200B;**[!UICONTROL 上线]**&#x200B;状态，现在对所选受众可见。 营销活动的每个收件人都可以使用[!DNL Journey Optimizer] Web设计器查看您添加到网站的修改。

>[!NOTE]
>
>如果您为Web营销活动定义了计划，则在到达开始日期和时间之前，其状态为&#x200B;**[!UICONTROL 已计划]**。
>
>如果您激活的Web营销活动与另一个已上线的营销活动影响相同的页面，则所有更改将应用于您的网页。

在[此部分](../campaigns/review-activate-campaign.md)中了解关于激活营销活动的更多信息。

## 停止Web活动 {#stop-web-campaign}

在Web营销活动处于实时状态时，您可以停止它以防止受众看到您的修改。 请按照以下步骤操作。

1. 从列表中选择一个实时营销活动。

1. 从顶部菜单中选择&#x200B;**[!UICONTROL 停止营销活动]**。

   ![](assets/web-campaign-stop.png)

1. 您添加的修改将不再对您定义的受众可见。

>[!NOTE]
>
>停止Web营销活动后，您将无法再次编辑或激活它。 您只能复制它并激活重复的行销活动。

## 操作方法视频{#video}

以下视频介绍了如何创建Web营销活动、配置其属性、审查和发布它。

>[!VIDEO](https://video.tv.adobe.com/v/3418800/?quality=12&learn=on)