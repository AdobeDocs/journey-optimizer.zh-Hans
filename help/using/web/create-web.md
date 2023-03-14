---
title: 创建 Web 体验
description: 了解如何在Journey Optimizer中创作网页并编辑其内容
feature: Web Channel
topic: Content Management
role: User
level: Beginner
hide: true
hidefromtoc: true
exl-id: e28c038b-49ed-4685-bfe6-514116eb0711
badge: label="Beta" type="Informational"
source-git-commit: 160e4ce03d3be975157c30fbe511875a85b00551
workflow-type: tm+mt
source-wordcount: '1041'
ht-degree: 8%

---

# 创建 Web 体验 {#create-web}

>[!BEGINSHADEBOX]

您将在本文档中找到以下内容：

* [Web 渠道入门](get-started-web.md)
* **[创建 Web 体验](create-web.md)**
* [创建 Web 页面](author-web.md)
* [可视化编辑帮助程序扩展](visual-editing-helper.md)
* [Web 报告](web-report.md)

>[!ENDSHADEBOX]

[!DNL Journey Optimizer] 允许您通过入站Web营销活动为客户提供Web体验，从而实现个性化。

>[!CAUTION]
>
>当前位置 [!DNL Journey Optimizer] 您只能使用以下方式创建Web体验 **营销活动**.

## 先决条件 {#prerequesites}

能够访问和创作中的网页 [!DNL Journey Optimizer] 用户界面，请遵循以下先决条件：

* 要向网站添加修改，您需要实施 [Adobe Experience Platform Web SDK](https://experienceleague.adobe.com/docs/platform-learn/implement-web-sdk/overview.html?lang=zh-Hans){target="_blank"} 网站上的。

* 要访问 [!DNL Journey Optimizer] web designer中，您必须下载 [Adobe Experience Cloud可视化编辑帮助程序](https://chrome.google.com/webstore/detail/adobe-experience-cloud-vi/kgmjjkfjacffaebgpkpcllakjifppnca){target="_blank"} Chrome上的浏览器扩展。 [了解详情](visual-editing-helper.md)

>[!CAUTION]
>
>Google Chrome是目前唯一支持在中创作网页的浏览器 [!DNL Journey Optimizer].

要正确交付Web体验，必须定义以下设置：

* 在 [Adobe Experience Platform数据收集](https://experienceleague.adobe.com/docs/experience-platform/edge/datastreams/overview.html){target="_blank"}，确保您有定义的数据流，例如 **[!UICONTROL Adobe Experience Platform]** 服务，您拥有 **[!UICONTROL 边缘分段]** 和 **[!UICONTROL Adobe Journey Optimizer]** 选项已启用。

   这可确保Adobe Experience Platform Edge正确处理Journey Optimizer入站事件。 [了解详情](https://experienceleague.adobe.com/docs/experience-platform/edge/datastreams/configure.html?lang=zh-Hans){target="_blank"}

   ![](assets/web-aep-datastream-ajo.png)

   >[!NOTE]
   >
   >此 **[!UICONTROL Adobe Journey Optimizer]** 选项仅可在 **[!UICONTROL 边缘分段]** 选项已启用。

* In [Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/profile/home.html?lang=zh-Hans){target="_blank"}, make sure you have one merge policy with the **[!UICONTROL Active-On-Edge Merge Policy]** option enabled. To do this, select a policy under the **[!UICONTROL Customer]** > **[!UICONTROL Profiles]** > **[!UICONTROL Merge Policies]** Experience Platform menu. [Learn more](https://experienceleague.adobe.com/docs/experience-platform/profile/merge-policies/ui-guide.html#configure){target="_blank"}

   此合并策略的使用者 [!DNL Journey Optimizer] 入站渠道，用于在边缘上正确激活和发布入站营销活动。 [了解详情](https://experienceleague.adobe.com/docs/experience-platform/profile/merge-policies/ui-guide.html){target="_blank"}

   ![](assets/web-aep-merge-policy.png)

## 创建Web活动 {#create-web-campaign}

>[!CONTEXTUALHELP]
>id="ajo_web_surface"
>title="定义Web表面"
>abstract="一个Web表面可以与单个页面URL或多个页面匹配，从而允许您跨一个或多个网页提交内容修改。"

要开始通过营销活动构建Web体验，请执行以下步骤。

1. 创建营销活动. [了解详情](../campaigns/create-campaign.md)

1. 选择 **[!UICONTROL Web]** 操作。

   ![](assets/web-create-campaign.png)

1. 定义Web表面。

   >[!NOTE]
   >
   >Web表面是由要交付内容的URL标识的Web属性。 它可以匹配单个页面URL或多个页面，从而允许您跨一个或多个网页进行修改。

   您可以输入 **[!UICONTROL 页面URL]** （如果要将更改仅应用于单个页面）。

   ![](assets/web-campaign-surface.png)

1. 或者，您可以构建 **[!UICONTROL 页面匹配规则]** 定位多个匹配同一规则的URL — 例如，如果您想对整个网站上的主页横幅应用更改，或添加一个显示在网站所有产品页面上的顶部图像。

   要执行此操作，请选择 **[!UICONTROL 页面匹配规则]** 并单击 **[!UICONTROL 创建规则]**.

   ![](assets/web-campaign-matching-rule.png)

1. 定义您的标准 **[!UICONTROL 域]** 和 **[!UICONTROL 页面]** 字段。

   例如，如果您要编辑显示在Luma网站的所有女性产品页面上的元素，请选择 **[!UICONTROL 域]** > **[!UICONTROL 开头为]** > `luma` 和 **[!UICONTROL 页面]** > **[!UICONTROL 包含]** > `women`.

   ![](assets/web-pages-matching-rule.png)

1. 保存更改。该规则显示在 **[!UICONTROL 创建营销活动]** 屏幕。

   ![](assets/web-pages-matching-rule-example.png)

1. 定义Web曲面后，选择 **[!UICONTROL 创建]**. 您现在可以配置Campaign属性和设置。

## 配置Web活动 {#configure-web-campaign}

1. 在 **[!UICONTROL 属性]** 选项卡，您可以根据需要编辑营销活动名称并添加描述。

   ![](assets/web-campaign-properties.png)

1. 要将自定义或核心数据使用标签分配给Web营销活动，请选择 **[!UICONTROL 管理访问权限]** 按钮进行调试。 [了解有关对象级访问控制(OLAC)的更多信息](../administration/object-based-access.md)

1. 您可以选择 **[!UICONTROL 内容试验]** 测试部分受众的内容处理，以确定哪个处理在特定量度方面表现最佳。 [了解详情](../campaigns/content-experiment.md)

   >[!AVAILABILITY]
   >
   >此 **内容试验** 功能目前仅适用于一组组织（限量发布）。 有关更多信息，请与您的 Adobe 代表联系。

1. 从 **[!UICONTROL 操作]** 选项卡，选择 **[!UICONTROL 编辑内容]** 以开始创作您的Web营销活动。 [了解详情](author-web.md)

   ![](assets/web-edit-content.png)

1. 从 **[!UICONTROL Audience]** 选项卡，定义能够查看您的Web营销活动的用户。 默认情况下，所有访客都可看到Web营销活动。

   ![](assets/web-campaign-audience.png)

   您还可以选择特定受众。 使用 **[!UICONTROL 选择受众]** 按钮以显示可用Adobe Experience Platform区段的列表。 [了解有关区段的更多信息](../segment/about-segments.md)

   >[!NOTE]
   >
   >对于API触发的营销活动，需要通过API调用设置受众。 [了解详情](../campaigns/api-triggered-campaigns.md)

   ![](assets/web-campaign-select-audience.png)

1. 在 **[!UICONTROL 身份命名空间]** 字段，选择要使用的命名空间，以标识所选区段中的个人。 [了解有关命名空间的更多信息](../event/about-creating.md#select-the-namespace)

1. 定义 **[!UICONTROL 计划]** 用于您的Web营销活动。 [了解详情](../campaigns/create-campaign.md#schedule)

   ![](assets/web-campaign-schedule.png)

   默认情况下，它从手动激活时开始，到手动停止时结束，但您也可以定义特定的日期和时间，使修改可见。

   ![](assets/web-campaign-schedule-start.png)

## 激活Web活动 {#activate-web-campaign}

一旦您定义了 [Web营销活动设置](#configure-web-campaign) 并且您根据需要使用 [Web设计器](author-web.md)，您可以查看和激活您的Web营销活动。 请按照以下步骤操作。

>[!NOTE]
>
>您还可以在激活Web营销活动内容之前对其进行预览。 [了解详情](author-web.md#test-web-campaign)

1. 在Web营销活动中，选择 **[!UICONTROL 查看以激活]**.

   ![](assets/web-campaign-review.png)

1. 根据需要查看和编辑内容、属性、界面、受众和计划。

1. 选择 **[!UICONTROL 激活]**.

   ![](assets/web-campaign-activate.png)

   >[!NOTE]
   >
   >单击之后 **[!UICONTROL 激活]**，网站营销活动更改最多可能需要15分钟才能实时发布。

您的Web营销活动会获取 **[!UICONTROL 实时]** 状态，并且现在对选定的受众可见。 营销活动的每个收件人均可以使用查看您添加到网站的修改 [!DNL Journey Optimizer] Web设计器。

>[!NOTE]
>
>如果您为Web营销活动定义了计划，则它具有 **[!UICONTROL 已计划]** 状态直到达到开始日期和时间。
>
>如果您激活的Web营销活动与另一个已上线的营销活动影响相同的页面，则所有更改将应用于您的网页。

了解更多有关在中激活营销活动的信息 [本节](../campaigns/review-activate-campaign.md).

## 停止Web活动 {#stop-web-campaign}

当Web营销活动处于实时状态时，您可以停止它以防止受众看到您的修改。 请按照以下步骤操作。

1. 从列表中选择一个实时营销活动。

1. 从顶部菜单中，选择 **[!UICONTROL 停止营销活动]**.

   ![](assets/web-campaign-stop.png)

1. 您添加的修改将不再对您定义的受众可见。

>[!NOTE]
>
>停止Web营销活动后，您将无法再次编辑或激活它。 您只能复制它并激活重复的行销活动。
