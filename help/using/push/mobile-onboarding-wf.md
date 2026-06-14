---
solution: Journey Optimizer
product: journey optimizer
title: 移动端加入快速入门工作流程
description: 了解如何使用移动设备载入快速入门工作流
topic: Mobile
feature: Push
role: Admin
level: Intermediate
badge: label="Beta 版" type="Informative"
exl-id: 364ef926-3f92-4297-acbd-a283668106ac
TQID: https://experienceleague.adobe.com/bqHcFNTpsuA6--8RiSjygD-8wsx4uwLeWqw9MBtby-4
product_v2: id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2: id: d0a62d3c-b79e-47e4-929e-40ef3cffa037
role_v2: id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
level_v2: id: b5a62a22-46f7-4f0d-b151-3fc640bef588
topic_v2: id: aa2f3246-cb95-4b30-8899-fdf7d73550ccid: b5ce8718-c3af-4fdb-a1a9-fca32f83a87cid: d3cdead0-685a-4489-9250-4bb709942f66
subfeature_v2: id: c96d2aa5-76a2-443d-8d23-5de95577c909
source-git-commit: 28eeed0d2b5dc3054c57004ead01de32151ab743
workflow-type: tm+mt
source-wordcount: 401
ht-degree: 9%

---

# 移动端加入快速入门工作流程 {#mobile-wf}

>[!BEGINSHADEBOX]

**在此页面上：**&#x200B;了解如何使用移动入门快速入门工作流来快速配置Adobe Experience Platform Mobile SDK、收集和验证移动事件数据并发送推送通知。

>[!ENDSHADEBOX]

新的&#x200B;**Mobile入门快速入门工作流**&#x200B;是一项新产品功能，可用于快速配置Adobe Experience Platform Mobile SDK、开始收集和验证移动事件数据以及通过[!DNL Journey Optimizer]发送推送通知。

此功能可通过&#x200B;**[!DNL Adobe Experience Platform Data Collection]**&#x200B;主页作为公共Beta供所有客户访问。

## 快速入门{#gs-mobile-wf}

此新工作流通过减少总点击量和加快Journey Optimizer的移动配置来自动化数据收集设置。 此快速入门工作流将引导您完成四个简单步骤，即[设置](#gs-mobile-wf)、[实施](#implement-mobile-wf)、[验证](#valid-mobile-wf)和[查看](#review-mobile-wf)您的移动设备配置。

要访问新的移动设备载入快速入门工作流，请从解决方案切换器浏览到&#x200B;**[!DNL Data Collection]**。 然后选择主页上的&#x200B;**[!DNL Start Collecting Mobile Data]**&#x200B;卡。

![](assets/mobile-wf-home.png)

以下是一些附加功能：

* 简单的四步工作流程和用户界面。
* 提供基本设置，以便在几分钟内开始通过[Adobe Experience Platform Mobile SDK](https://developer.adobe.com/client-sdks/documentation){target="_blank"}收集移动事件数据。
* 能够测试和验证利用[Adobe Experience Platform Assurance](https://experienceleague.adobe.com/docs/experience-platform/assurance/home.html?lang=zh-Hans){target="_blank"}的基本移动推送事件。
* 自动创建和配置所有必需的数据收集和Journey Optimizer资源。
* 在产品指导和工具提示中。
* 如果需要，为更高级的实施提供自然过渡。

## 设置 {#setup-mobile-wf}

此工作流程的第一步自动创建和配置所有必需的数据收集和Journey Optimizer资源，例如移动资产、移动扩展、Journey Optimizer扩展、规则、数据元素等。

接受Beta条款和条件后，输入移动应用程序的名称并单击&#x200B;**[!DNL Next]**。

![](assets/mobile-wf-setup.png)

提供iOS和Android平台的信息，包括您的应用程序ID和身份验证密钥或密钥文件。

## 实施{#implement-mobile-wf}

下一步提供了将代码安装到移动应用程序的分步指南。

![](assets/mobile-wf-add-code.png)


## 验证{#valid-mobile-wf}

查看并检查实施以验证它。 您可以发送测试推送通知。

![](assets/mobile-wf-valid.png)


## 审阅 {#review-mobile-wf}

自动化设置已完成。 您现在可以访问标记移动资产，配置规则或数据元素，并开始使用Adobe Journey Optimizer发送推送通知。

![](assets/mobile-wf-done.png)


**相关主题**

* [推送通知入门](../../rp_landing_pages/push-landing-page.md)
* [推送通知数据流和组件](push-gs.md)
* [配置推送渠道](push-configuration.md)
* [推送通知报告](../reports/journey-global-report-cja-push.md#track-link-url-push)
* [创建推送通知](create-push.md)
