---
title: 基于代码的体验先决条件
description: 要使用Journey Optimizer基于代码的功能编辑应用程序和网页，请遵循此页面上的先决条件
feature: Code-based Experiences
topic: Content Management
role: Admin
level: Experienced
hide: true
hidefromtoc: true
badge: label="Beta 版"
exl-id: ac901f88-5fde-4220-88c6-fe05433866cc
source-git-commit: 07b1f9b885574bb6418310a71c3060fa67f6cac3
workflow-type: tm+mt
source-wordcount: '514'
ht-degree: 19%

---

# 先决条件和护栏 {#web-prerequisites}

>[!BEGINSHADEBOX]

本文档指南包括以下内容：

* [开始使用基于代码的渠道](get-started-code-based.md)
* **[基于代码的先决条件](code-based-prerequisites.md)**
* [基于代码的实施示例](code-based-implementation-samples.md)
* [创建基于代码的体验](create-code-based.md)

>[!ENDSHADEBOX]

能够在中使用基于代码的体验操作 [!DNL Journey Optimizer] 并交付应用程序可以使用的代码内容有效负载，请遵循以下先决条件：

* 要向应用程序添加修改，您需要具有特定的实施。 [了解详情](#implementation-prerequisites)

* 要正确交付基于代码的体验，请确保您详细定义了Adobe Experience Platform设置 [此处](#delivery-prerequisites).

## 警告说明 {#caution-notes-web}

* 基于代码的渠道目前仅作为 Beta 版供部分用户使用。要加入 Beta 版计划，请联系 Adobe 客户关怀团队。

* 当前位置 [!DNL Journey Optimizer] 您只能在中创建基于代码的体验 **营销活动**. [了解详情](../campaigns/create-campaign.md#configure)

## 实施先决条件 {#implementation-prerequisites}

基于代码的体验支持任何类型的客户实施，如以下选项中所示。 可以为属性使用客户端、服务器端或混合实施方法：

* 仅限客户端 — 要向网页或移动应用程序添加修改，您需要实施 [Adobe Experience Platform Web SDK](https://experienceleague.adobe.com/docs/platform-learn/implement-web-sdk/overview.html?lang=zh-Hans){target="_blank"} on your website or [Adobe Experience Platform Mobile SDK](https://developer.adobe.com/client-sdks/documentation/){target="_blank"} 在你的移动应用程序上。

* 混合模式 — 您可以使用 [AEP Edge Network服务器API](https://experienceleague.adobe.com/docs/experience-platform/edge-network-server-api/data-collection/interactive-data-collection.html){target="_blank"} to request for personalization server-side; the response is provided to the Adobe Experience Platform Web SDK to render the modifications client-side. Learn more in the Adobe Experience Platform [Edge Network Server API documentation](https://experienceleague.adobe.com/docs/experience-platform/edge-network-server-api/overview.html?lang=zh-Hans){target="_blank"}. You can find out more about the hybrid mode and check some implementation samples in [this blog post](https://blog.developer.adobe.com/hybrid-personalization-in-the-adobe-experience-platform-web-sdk-6a1bb674bf41){target="_blank"}.

* 服务器端 — 您可以使用 [AEP Edge Network服务器API](https://experienceleague.adobe.com/docs/experience-platform/edge-network-server-api/data-collection/interactive-data-collection.html){target="_blank"} 以请求服务器端个性化。 您的开发团队必须处理响应并在应用程序实施中在客户端渲染修改。

您可以在中找到上述每种实施方法的示例 [本节](code-based-implementation-samples.md).

## 投放先决条件 {#delivery-prerequisites}

要正确交付基于代码的体验，必须定义以下设置：

* 在 [Adobe Experience Platform数据收集](https://experienceleague.adobe.com/docs/experience-platform/edge/datastreams/overview.html?lang=zh-Hans){target="_blank"}，确保您有定义的数据流，例如 **[!UICONTROL Adobe Experience Platform]** 服务 **[!UICONTROL Adobe Journey Optimizer]** 选项已启用。

  这可确保Adobe Experience Platform Edge正确处理Journey Optimizer入站事件。 [了解详情](https://experienceleague.adobe.com/docs/experience-platform/edge/datastreams/configure.html?lang=zh-Hans){target="_blank"}

  ![](../web/assets/web-aep-datastream-ajo.png)

* 在 [Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/profile/home.html?lang=zh-Hans){target="_blank"}, make sure you have one merge policy with the **[!UICONTROL Active-On-Edge Merge Policy]** option enabled. To do this, select a policy under the **[!UICONTROL Customer]** > **[!UICONTROL Profiles]** > **[!UICONTROL Merge Policies]** Experience Platform menu. [Learn more](https://experienceleague.adobe.com/docs/experience-platform/profile/merge-policies/ui-guide.html#configure){target="_blank"}

  此合并策略的使用者为 [!DNL Journey Optimizer] 入站渠道，用于在边缘上正确激活和发布入站营销活动。 [了解详情](https://experienceleague.adobe.com/docs/experience-platform/profile/merge-policies/ui-guide.html?lang=zh-Hans){target="_blank"}

  ![](../web/assets/web-aep-merge-policy.png)

## 内容试验先决条件 {#experiment-prerequisites}

要为基于代码的渠道启用内容实验，您需要确保 [数据集](../data/get-started-datasets.md) 在应用程序实施中使用 [数据流](https://experienceleague.adobe.com/docs/experience-platform/datastreams/overview.html?lang=zh-Hans){target="_blank"} 也包含在您的报表配置中。

换言之，在配置实验报告时，如果添加的数据集不在应用程序数据流中，则应用程序数据将不会显示在内容实验报告中。

了解如何在中为内容实验报告添加数据集 [本节](../campaigns/reporting-configuration.md#add-datasets).

>[!NOTE]
>
>数据集由 [!DNL Journey Optimizer] 并且不影响数据收集或数据摄取。
