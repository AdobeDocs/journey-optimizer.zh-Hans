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
source-git-commit: c4ab97999d000d969f6f09f4d84be017d1288f94
workflow-type: tm+mt
source-wordcount: '357'
ht-degree: 9%

---

# 移动端加入快速入门工作流程 {#mobile-wf}

新的&#x200B;**移动入门快速入门工作流**&#x200B;是一项新产品功能，可用于快速配置Adobe Experience Platform Mobile SDK、开始收集和验证移动事件数据以及通过[!DNL Journey Optimizer]发送推送通知。

此功能可通过&#x200B;**[!DNL Adobe Experience Platform Data Collection]**&#x200B;主页作为公共Beta供所有客户访问。

## 快速入门{#gs-mobile-wf}

此新工作流通过减少总点击量和加快Journey Optimizer的移动配置来自动化数据收集设置。 此快速入门工作流将引导您完成四个简单步骤，即[设置](##setup-mobile-wf)、[实施](#implement-mobile-wf)、[验证](#valid-mobile-wf)和[查看](#review-mobile-wf)您的移动设备配置。

要访问新的移动设备载入快速入门工作流，请从解决方案切换器浏览到&#x200B;**[!DNL Data Collection]**。 然后选择主页上的&#x200B;**[!DNL Start Collecting Mobile Data]**&#x200B;卡。

![](assets/mobile-wf-home.png)

以下是一些附加功能：

* 简单的四步工作流程和用户界面。
* 提供基本设置，以便在几分钟内开始通过[Adobe Experience Platform Mobile SDK](https://developer.adobe.com/client-sdks/documentation/){target="_blank"}收集移动事件数据。
* 能够利用[Adobe Experience Platform保证](https://experienceleague.adobe.com/docs/experience-platform/assurance/home.html){target="_blank"}测试和验证基本移动推送事件。
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


## 审查 {#review-mobile-wf}

自动化设置已完成。 您现在可以访问标记移动资产，配置规则或数据元素，并开始使用Adobe Journey Optimizer发送推送通知。

![](assets/mobile-wf-done.png)


**相关主题**

* [推送通知入门](get-started-push.md)
* [推送通知数据流和组件](push-gs.md)
* [配置推送渠道](push-configuration.md)
* [推送通知报告](../reports/journey-global-report.md#push-global)
* [创建推送通知](create-push.md)
