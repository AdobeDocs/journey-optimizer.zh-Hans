---
title: 内容卡配置
description: 内容卡渠道先决条件
feature: Channel Configuration
topic: Content Management
role: Admin
level: Experienced
badge: label="限量发布版" type="Informative"
hide: true
hidefromtoc: true
source-git-commit: 8a902298bbbac5689b4f84266dd9c9027e45fad5
workflow-type: tm+mt
source-wordcount: '305'
ht-degree: 7%

---

# 内容卡先决条件 {#content-card-configuration-prereq}

>[!BEGINSHADEBOX]

**目录**

* [内容卡片入门](get-started-content-card.md)
* **内容卡先决条件**
* [在Journey Optimizer中配置内容卡渠道](content-card-configuration.md)
* [创建内容卡片](create-content-card.md)
* [设计内容卡片](design-content-card.md)
* [内容卡报表](content-card-report.md)

>[!ENDSHADEBOX]

>[!AVAILABILITY]
>
>内容卡当前仅适用于一组组织（限量发布）。 要获得访问权限，请与 Adobe 代表联系。

要让Adobe Journey Optimizer正确显示内容卡片，您必须配置以下Adobe Experience Platform设置：

* **Adobe Experience Platform数据收集**

  [创建数据流](https://experienceleague.adobe.com/en/docs/experience-platform/datastreams/configure)并[添加Experience Platform服务](https://experienceleague.adobe.com/en/docs/experience-platform/datastreams/configure#aep)。 启用&#x200B;**[!UICONTROL Edge分段]**&#x200B;和&#x200B;**[!UICONTROL Adobe Journey Optimizer]**&#x200B;选项。 这可确保Journey Optimizer事件由Adobe Experience PlatformEdge Network处理。 有关如何配置数据流的详细信息，请参阅[数据流文档](https://experienceleague.adobe.com/en/docs/experience-platform/datastreams/configure)。

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

  使用&#x200B;**Edge Delivery保证**&#x200B;中的&#x200B;**Adobe Experience Platform**&#x200B;视图对移动体验进行故障诊断。 它可以检查请求、验证边缘调用以及检查配置文件数据。 [了解详情](https://experienceleague.adobe.com/zh-hans/docs/experience-platform/assurance/view/edge-delivery)

* **内容实验**

  确保在应用程序的[数据流](https://experienceleague.adobe.com/en/docs/experience-platform/datastreams/overview#_blank)中使用的数据集也包含在内容试验报告配置中。 如果数据集不匹配，应用程序数据将不会显示在报表中。

  在[本节](../content-management/reporting-configuration.md)中了解如何为内容试验报告添加数据集。
