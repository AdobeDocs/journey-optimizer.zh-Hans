---
title: 内容卡配置
description: 内容卡渠道先决条件
feature: Channel Configuration, Content Cards
topic: Content Management
role: Admin
level: Experienced
exl-id: df92e319-1e42-486f-b688-595964a762c9
source-git-commit: 3d5ed7c5efd76616c8dbc89078f7368eedc5f1af
workflow-type: tm+mt
source-wordcount: '430'
ht-degree: 3%

---

# 内容卡片先决条件 {#content-card-configuration-prereq}

要让Adobe Journey Optimizer正确显示内容卡片，您必须配置以下Adobe Experience Platform设置：

* **Adobe Experience Platform数据收集**

  [创建数据流](https://experienceleague.adobe.com/zh-hans/docs/experience-platform/datastreams/configure){target="_blank"}并[添加Experience Platform服务](https://experienceleague.adobe.com/zh-hans/docs/experience-platform/datastreams/configure#aep){target="_blank"}。 启用&#x200B;**[!UICONTROL Edge分段]**&#x200B;和&#x200B;**[!UICONTROL Adobe Journey Optimizer]**&#x200B;选项。 这可确保Journey Optimizer事件由Adobe Experience Platform Edge Network处理。
将&#x200B;**Experience Event - Proposition Interaction**&#x200B;字段组添加到您的数据集以将此数据包含在您的报表中。 [了解有关数据流的更多信息](https://experienceleague.adobe.com/zh-hans/docs/experience-platform/datastreams/configure){target="_blank"}

* **Adobe Experience Platform**

  请确保默认合并策略在&#x200B;**客户** > **[!UICONTROL 配置文件]** > **[!UICONTROL 合并策略]** Experience Platform菜单下启用了&#x200B;**[!UICONTROL Edge上的活动合并策略]**。 [了解详情](https://experienceleague.adobe.com/docs/experience-platform/profile/merge-policies/ui-guide.html?lang=zh-Hans#configure){target="_blank"}

  >[!NOTE]
  >
  >使用自定义&#x200B;**[!UICONTROL 数据集偏好设置]**&#x200B;合并策略时，请确保在指定的合并策略中添加&#x200B;**[!UICONTROL 历程入站]**&#x200B;数据集。

* **Adobe Experience Platform Mobile或Platform Web SDK**

  对于移动和Web应用程序，若要向网页或移动应用程序添加修改，您需要在网站上实施[Adobe Experience Platform Web SDK](https://experienceleague.adobe.com/zh-hans/docs/platform-learn/implement-web-sdk/overview){target="_blank"}，或在移动应用程序上实施[Adobe Experience Platform Mobile SDK](https://developer.adobe.com/client-sdks/home/){target="_blank"}。

* **Journey Optimizer**

  创建[内容卡配置](#content-card-configuration)。

* **疑难解答**

  使用&#x200B;**Edge Delivery**&#x200B;中的&#x200B;**Adobe Experience Platform Assurance**&#x200B;视图对移动体验进行故障诊断。 它可以检查请求、验证边缘调用以及检查配置文件数据。 [了解详情](https://experienceleague.adobe.com/zh-hans/docs/experience-platform/assurance/view/edge-delivery){target="_blank"}

* **内容实验**

  确保在应用程序的[数据流](https://experienceleague.adobe.com/zh-hans/docs/experience-platform/datastreams/overview#_blank){target="_blank"}中使用的数据集也包含在内容试验报告配置中。 如果数据集不匹配，应用程序数据将不会显示在报表中。

  在[本节](../reports/reporting-configuration.md)中了解如何为内容试验报告添加数据集。

## 配置文件管理护栏 {#profile-management-guardrail}

[!DNL Journey Optimizer]内容卡可以定位假名配置文件，这意味着配置文件尚未经过身份验证或未知，因为它们之前未在其他渠道上参与。 例如，当基于临时ID（如ECID）定位所有访客或受众时，就是这种情况。

这会增加您的可参与用户档案总数，如果超出您购买的可参与用户档案的合同数量，则可能会带来成本影响。 [Journey Optimizer产品说明](https://helpx.adobe.com/cn/legal/product-descriptions/adobe-journey-optimizer.html){target="_blank"}页面上列出了每个包的许可证指标。 您可以在[许可证使用情况仪表板](../audience/license-usage.md)中检查可参与的配置文件数。

要将可参与的用户档案保持在合理范围内，Adobe建议设置生存时间(TTL)，以便在特定时间范围内未看到或未参与匿名用户档案时，自动从实时客户档案中删除这些用户档案。

>[!NOTE]
>
>请参阅[Experience Platform文档](https://experienceleague.adobe.com/zh-hans/docs/experience-platform/profile/pseudonymous-profiles){target="_blank"}以了解如何为假名配置文件配置数据过期时间。

Adobe建议将TTL值设置为14天，以匹配当前的Edge配置文件TTL。