---
title: 基于代码的体验先决条件
description: 要使用Journey Optimizer基于代码的功能编辑应用程序和网页，请遵循此页面上的先决条件
feature: Code-based Experiences
topic: Content Management
role: Admin
level: Experienced
exl-id: ac901f88-5fde-4220-88c6-fe05433866cc
source-git-commit: 3d5ed7c5efd76616c8dbc89078f7368eedc5f1af
workflow-type: tm+mt
source-wordcount: '833'
ht-degree: 2%

---

# 基于代码的体验先决条件 {#code-based-prerequisites}

要在[!DNL Journey Optimizer]中使用基于代码的体验操作并交付应用程序可以使用的代码内容有效负载，请遵循以下先决条件：

* 要向应用程序添加修改，您必须具有特定的实施。 [了解详情](#implementation-prerequisites)

* 为了正确交付基于代码的体验，请确保在[此处](#delivery-prerequisites)详细定义Adobe Experience Platform设置。

* 要使数据显示在基于代码的体验报表中，请确保遵循以下[报告先决条件](#reporting-prerequisites)。

* 创建基于[代码的体验渠道配置](code-based-configuration.md)时，请确保输入的字符串/路径或表面URI与您自己的实施中声明的字符串/路径或表面URI匹配。 这可确保将内容交付到指定应用程序或页面内的所需位置。 否则，将无法交付更改。 [了解详情](code-based-surface.md)

>[!NOTE]
>
>将假名配置文件（未经身份验证的访客）与基于代码的体验进行定位时，请考虑为自动删除配置文件设置生存时间(TTL)，以管理可参与配置文件计数和相关成本。 [了解详情](#profile-management-guardrail)

## 实施先决条件 {#implementation-prerequisites}

基于代码的体验支持任何类型的客户实施，如以下选项中所示。 可以为属性使用客户端、服务器端或混合实施方法：

* 仅客户端 — 若要向网页或移动应用程序添加修改，您需要在网站上实施[Adobe Experience Platform Web SDK](https://experienceleague.adobe.com/docs/platform-learn/implement-web-sdk/overview.html?lang=zh-Hans){target="_blank"}，或在移动应用程序上实施[Adobe Experience Platform Mobile SDK](https://developer.adobe.com/client-sdks/documentation/){target="_blank"}。

* 混合模式 — 您可以使用[AEP Edge Network服务器API](https://experienceleague.adobe.com/docs/experience-platform/edge-network-server-api/data-collection/interactive-data-collection.html?lang=zh-Hans){target="_blank"}来请求在服务器端进行个性化；响应将提供给Adobe Experience Platform Web SDK以渲染客户端所做的修改。 请参阅Adobe Experience Platform [Edge Network Server API文档](https://experienceleague.adobe.com/docs/experience-platform/edge-network-server-api/overview.html?lang=zh-Hans){target="_blank"}以了解详情。 您可以在[这篇博客文章](https://blog.developer.adobe.com/hybrid-personalization-in-the-adobe-experience-platform-web-sdk-6a1bb674bf41){target="_blank"}中找到有关混合模式的详细信息并查看一些实施示例。

* 服务器端 — 您可以使用[AEP Edge Network服务器API](https://experienceleague.adobe.com/docs/experience-platform/edge-network-server-api/data-collection/interactive-data-collection.html?lang=zh-Hans){target="_blank"}来请求在服务器端进行个性化。 您的开发团队必须处理响应并在应用程序实施中在客户端渲染修改。

您可以在[此部分](code-based-implementation-samples.md)中找到上述每个实现方法的示例。

## 投放先决条件 {#delivery-prerequisites}

要正确交付基于代码的体验，必须定义以下设置：

* 在[Adobe Experience Platform数据收集](https://experienceleague.adobe.com/docs/experience-platform/edge/datastreams/overview.html?lang=zh-Hans){target="_blank"}中，确保您定义了数据流，例如在&#x200B;**[!UICONTROL Adobe Experience Platform]**&#x200B;服务下启用了&#x200B;**[!UICONTROL Adobe Journey Optimizer]**&#x200B;选项。

  这可确保Adobe Experience Platform Edge正确处理Journey Optimizer入站事件。 [了解详情](https://experienceleague.adobe.com/docs/experience-platform/edge/datastreams/configure.html?lang=zh-Hans){target="_blank"}

  ![](../web/assets/web-aep-datastream-ajo.png)

* 在[Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/profile/home.html?lang=zh-Hans){target="_blank"}中，确保您有一个启用了&#x200B;**[!UICONTROL Edge上活动合并策略]**&#x200B;选项的合并策略。 为此，请在&#x200B;**[!UICONTROL 客户]** > **[!UICONTROL 配置文件]** > **[!UICONTROL 合并策略]** Experience Platform菜单下选择一个策略。 [了解详情](https://experienceleague.adobe.com/docs/experience-platform/profile/merge-policies/ui-guide.html?lang=zh-Hans#configure){target="_blank"}

  [!DNL Journey Optimizer]入站渠道使用此合并策略在边缘上正确激活和发布入站营销活动。 [了解详情](https://experienceleague.adobe.com/docs/experience-platform/profile/merge-policies/ui-guide.html?lang=zh-Hans){target="_blank"}

  ![](../web/assets/web-aep-merge-policy.png)

* 要对Journey Optimizer Web体验的交付进行故障诊断，您可以使用&#x200B;**Edge Delivery**&#x200B;中的&#x200B;**Adobe Experience Platform Assurance**&#x200B;视图。 利用此插件，您可以详细检查请求调用，验证预期的边缘调用是否按预期发生，并检查配置文件数据，包括身份映射、区段成员资格和同意设置。 此外，您还可以查看请求符合条件的活动，并识别未符合条件的活动。

  使用&#x200B;**Edge Delivery**&#x200B;插件可帮助您获得所需的见解，以便有效了解入站实施并排除其故障。

  [了解有关Edge Delivery视图的更多信息](https://experienceleague.adobe.com/zh-hans/docs/experience-platform/assurance/view/edge-delivery){target="_blank"}

## 报告先决条件 {#reporting-prerequisites}

要为基于代码的渠道启用报告，您需要确保在应用程序实施[数据流](../data/get-started-datasets.md)中使用的[数据集](https://experienceleague.adobe.com/docs/experience-platform/datastreams/overview.html?lang=zh-Hans){target="_blank"}也包含在报告配置中。

换言之，在配置报表时，如果添加的数据集不在应用程序数据流中，则应用程序数据将不会显示在报表中。

在[本节](../reports/reporting-configuration.md#add-datasets)中了解如何添加用于报告的数据集。

>[!NOTE]
>
>该数据集由[!DNL Journey Optimizer]报表系统以只读方式使用，不影响数据收集或数据摄取。

## 配置文件管理护栏 {#profile-management-guardrail}

[!DNL Journey Optimizer]基于代码的体验可以定位假名配置文件，这意味着配置文件尚未通过身份验证或未知，因为它们之前尚未在其他渠道上参与。 例如，当基于临时ID（如ECID）定位所有访客或受众时，就是这种情况。

这会增加您的可参与用户档案总数，如果超出您购买的可参与用户档案的合同数量，则可能会带来成本影响。 [Journey Optimizer产品说明](https://helpx.adobe.com/cn/legal/product-descriptions/adobe-journey-optimizer.html){target="_blank"}页面上列出了每个包的许可证指标。 您可以在[许可证使用情况仪表板](../audience/license-usage.md)中检查可参与的配置文件数。

要将可参与的用户档案保持在合理范围内，Adobe建议设置生存时间(TTL)，以便在特定时间范围内未看到或未参与匿名用户档案时，自动从实时客户档案中删除这些用户档案。

>[!NOTE]
>
>请参阅[Experience Platform文档](https://experienceleague.adobe.com/zh-hans/docs/experience-platform/profile/pseudonymous-profiles){target="_blank"}以了解如何为假名配置文件配置数据过期时间。

Adobe建议将TTL值设置为14天，以匹配当前的Edge配置文件TTL。
