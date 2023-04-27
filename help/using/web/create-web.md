---
title: 创建 Web 体验
description: 了解如何在Journey Optimizer中创作网页并编辑其内容
feature: Web Channel
topic: Content Management
role: User
level: Beginner
exl-id: e28c038b-49ed-4685-bfe6-514116eb0711
source-git-commit: 803c9f9f05669fad0a9fdeeceef58652b6dccf70
workflow-type: tm+mt
source-wordcount: '662'
ht-degree: 8%

---

# 创建 Web 体验 {#create-web}

[!DNL Journey Optimizer] 允许您通过入站web营销活动将您交付给客户的web体验个性化。

>[!CAUTION]
>
>当前位于 [!DNL Journey Optimizer] 您只能使用 **营销活动**.

[在此视频中了解如何创建Web营销活动](#video)

## 创建Web营销活动 {#create-web-campaign}

>[!CONTEXTUALHELP]
>id="ajo_web_surface"
>title="定义 Web 表面"
>abstract="Web 表面可以匹配单个页面 URL 或多个页面，这让您可以在一个或多个网页上传递内容修改。"

>[!CONTEXTUALHELP]
>id="ajo_web_surface_rule"
>title="构建页面匹配规则"
>abstract="使用页面匹配规则可以定位与同一规则匹配的多个URL — 例如，如果您要将更改应用于整个网站的主页横幅，或添加显示在网站所有产品页面上的顶部图像。"

要开始通过营销活动构建Web体验，请执行以下步骤。

>[!NOTE]
>
>如果您是首次创建Web体验，请确保遵循 [此部分](web-prerequisites.md).

1. 创建营销活动. [了解详情](../campaigns/create-campaign.md)

1. 选择 **[!UICONTROL Web]** 操作。

1. 定义 Web 表面.

   >[!NOTE]
   >
   >Web表面是由将要交付内容的URL标识的Web属性。 它可以匹配单个页面URL或多个页面，从而允许您在一个或多个网页之间交付修改。

   您可以输入 **[!UICONTROL 页面URL]** 如果您只想将更改应用到单个页面，请执行以下操作：

   ![](assets/web-campaign-surface.png)

1. 或者，您可以构建 **[!UICONTROL 页面匹配规则]** 要定位与同一规则匹配的多个URL — 例如，如果您要将所做的更改应用到整个网站的主页横幅，或添加显示在网站所有产品页面上的热门图像。

   要执行此操作，请选择 **[!UICONTROL 页面匹配规则]** 单击 **[!UICONTROL 创建规则]**.

   ![](assets/web-campaign-matching-rule.png)

1. 为 **[!UICONTROL 域]** 和 **[!UICONTROL 页面]** 字段。

   例如，如果要编辑Luma网站所有女产品页面上显示的元素，请选择 **[!UICONTROL 域]** > **[!UICONTROL 开始于]** > `luma` 和 **[!UICONTROL 页面]** > **[!UICONTROL 包含]** > `women`.

   ![](assets/web-pages-matching-rule.png)

1. 保存更改。规则显示在 **[!UICONTROL 创建营销活动]** 屏幕。

   ![](assets/web-pages-matching-rule-example.png)

1. 定义网页曲面后，选取 **[!UICONTROL 创建]**.

1. 完成创建Web营销活动的步骤，如营销活动属性、 [受众](../segment/about-segments.md)和 [计划](../campaigns/create-campaign.md#schedule).

   ![](assets/web-campaign-steps.png)

有关如何配置营销活动的详细信息，请参阅 [本页](../campaigns/get-started-with-campaigns.md).

## 激活Web营销活动 {#activate-web-campaign}

定义 [网站营销活动设置](#configure-web-campaign) 并根据需要使用 [网站设计工具](author-web.md)，您可以查看并激活Web营销活动。 按照以下步骤操作。

>[!NOTE]
>
>您还可以在激活Web营销活动内容之前对其进行预览。 [了解详情](author-web.md#test-web-campaign)

1. 在您的Web营销活动中，选择 **[!UICONTROL 查看以激活]**.

1. 根据需要，检查和编辑内容、属性、表面、受众和计划。

1. 选择 **[!UICONTROL 激活]**.

   ![](assets/web-campaign-activate.png)

   >[!NOTE]
   >
   >在单击 **[!UICONTROL 激活]**，则网站上可能最多需要15分钟才能实时显示web促销活动更改。

您的Web营销活动将 **[!UICONTROL 实时]** 状态，现在对选定受众可见。 营销活动的每个收件人都可以通过 [!DNL Journey Optimizer] web设计器。

>[!NOTE]
>
>如果您为Web营销活动定义了计划，则它具有 **[!UICONTROL 已计划]** 状态，直到达到开始日期和时间。
>
>如果激活一个与另一个已上线营销活动相同的网页相同的Web营销活动，则所有更改都将应用于您的网页。

了解有关在中激活营销活动的更多信息 [此部分](../campaigns/review-activate-campaign.md).

## 停止Web营销活动 {#stop-web-campaign}

Web营销活动上线后，您可以停止该活动以阻止受众看到您所做的修改。 按照以下步骤操作。

1. 从列表中选择一个实时营销活动。

1. 从顶部菜单中，选择 **[!UICONTROL 停止营销活动]**.

   ![](assets/web-campaign-stop.png)

1. 您添加的修改将不再对您定义的受众可见。

>[!NOTE]
>
>Web营销活动停止后，您将无法再次编辑或激活它。 您只能复制并激活复制的营销活动。

## 操作方法视频{#video}

以下视频演示如何创建Web营销活动、配置其属性、查看和发布该营销活动。

>[!VIDEO](https://video.tv.adobe.com/v/3418800/?quality=12&learn=on)