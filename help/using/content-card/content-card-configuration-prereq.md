---
title: 内容卡配置
description: 内容卡渠道先决条件
feature: Channel Configuration, Content Cards
topic: Content Management
role: Admin
level: Experienced
exl-id: df92e319-1e42-486f-b688-595964a762c9
source-git-commit: b6fd60b23b1a744ceb80a97fb092065b36847a41
workflow-type: tm+mt
source-wordcount: '265'
ht-degree: 5%

---

# 内容卡片先决条件 {#content-card-configuration-prereq}

要让Adobe Journey Optimizer正确显示内容卡片，您必须配置以下Adobe Experience Platform设置：

* **Adobe Experience Platform数据收集**

  [创建数据流](https://experienceleague.adobe.com/en/docs/experience-platform/datastreams/configure)并[添加Experience Platform服务](https://experienceleague.adobe.com/en/docs/experience-platform/datastreams/configure#aep)。 启用&#x200B;**[!UICONTROL Edge分段]**&#x200B;和&#x200B;**[!UICONTROL Adobe Journey Optimizer]**选项。 这可确保Journey Optimizer事件由Adobe Experience Platform Edge Network处理。
将**Experience Event - Proposition Interaction**&#x200B;字段组添加到您的数据集以将此数据包含在您的报表中。 [了解有关数据流的更多信息](https://experienceleague.adobe.com/en/docs/experience-platform/datastreams/configure)

* **Adobe Experience Platform**

  请确保默认合并策略在&#x200B;**[!UICONTROL 客户]** > **[!UICONTROL 配置文件]** > **[!UICONTROL 合并策略]** Experience Platform菜单下启用了&#x200B;**Edge上的活动合并策略**。 [了解详情](https://experienceleague.adobe.com/docs/experience-platform/profile/merge-policies/ui-guide.html#configure){target="_blank"}

  >[!NOTE]
  >
  >使用自定义&#x200B;**[!UICONTROL 数据集偏好设置]**&#x200B;合并策略时，请确保在指定的合并策略中添加&#x200B;**[!UICONTROL 历程入站]**&#x200B;数据集。

* **Adobe Experience Platform Mobile或Platform Web SDK**

  对于移动和Web应用程序，若要向网页或移动应用程序添加修改，您需要在网站上实施[Adobe Experience Platform Web SDK](https://experienceleague.adobe.com/zh-hans/docs/platform-learn/implement-web-sdk/overview)，或在移动应用程序上实施[Adobe Experience Platform Mobile SDK](https://developer.adobe.com/client-sdks/home/)。

* **Journey Optimizer**

  创建[内容卡配置](#content-card-configuration)。

* **疑难解答**

  使用&#x200B;**Edge Delivery**&#x200B;中的&#x200B;**Adobe Experience Platform Assurance**&#x200B;视图对移动体验进行故障诊断。 它可以检查请求、验证边缘调用以及检查配置文件数据。 [了解详情](https://experienceleague.adobe.com/zh-hans/docs/experience-platform/assurance/view/edge-delivery)

* **内容实验**

  确保在应用程序的[数据流](https://experienceleague.adobe.com/en/docs/experience-platform/datastreams/overview#_blank)中使用的数据集也包含在内容试验报告配置中。 如果数据集不匹配，应用程序数据将不会显示在报表中。

  在[本节](../reports/reporting-configuration.md)中了解如何为内容试验报告添加数据集。
