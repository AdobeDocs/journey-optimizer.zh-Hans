---
solution: Journey Optimizer
product: journey optimizer
title: 移动端加入快速入门工作流程
description: 了解如何使用移动入门快速入门工作流
topic: Mobile
feature: Push
role: Admin
level: Intermediate
badge: label="Beta" type="Informative"
exl-id: 82477d40-cfea-456b-a7b1-9cfebd76db35
source-git-commit: 04f96fa1ad815b380cf33c7706e39094a1bca1c3
workflow-type: tm+mt
source-wordcount: '368'
ht-degree: 10%

---

# 移动端加入快速入门工作流程 {#mobile-wf}

新 **移动载入快速入门工作流** 是一项新产品功能，用于快速配置Adobe Experience Platform Mobile SDK、开始收集和验证移动事件数据，以及发送推送通知 [!DNL Journey Optimizer].

此功能可通过 **[!DNL Adobe Experience Platform Data Collection]** 作为公共测试版面向所有客户的主页。

## 快速入门{#gs-mobile-wf}

此新工作流通过减少总点击量并加快Journey Optimizer的移动配置速度，实现了数据收集设置的自动化。 此快速入门工作流将引导您完成四个简单步骤，以便 [设置](##setup-mobile-wf)， [实施](#implement-mobile-wf)， [验证](#valid-mobile-wf)、和 [审核](#review-mobile-wf) 您的移动配置。

要访问新的移动载入快速入门工作流，请浏览 **[!DNL Data Collection]** 从解决方案切换器中。 然后选择 **[!DNL Start Collecting Mobile Data]** 信息卡在主页上。

![](assets/mobile-wf-home.png)

以下是一些附加功能：

* 简单的四步工作流程和用户界面。
* 提供基本设置，以便开始通过收集移动事件数据 [Adobe Experience Platform Mobile SDK](https://developer.adobe.com/client-sdks/documentation/){target="_blank"} 几分钟内。
* 能够利用测试和验证基本移动推送事件 [Adobe Experience Platform Assurance](https://experienceleague.adobe.com/docs/experience-platform/assurance/home.html){target="_blank"}.
* 自动创建和配置所有必需的数据收集和Journey Optimizer资源。
* 在产品指南和工具提示中。
* 如果需要，为更高级的实施提供自然过渡。

## 设置 {#setup-mobile-wf}

此工作流程的第一步是自动创建和配置所有必需的数据收集和Journey Optimizer资源，例如移动资产、移动扩展、Journey Optimizer扩展、规则、数据元素等。

接受Beta版条款与条件后，输入移动应用程序的名称并单击 **[!DNL Next]**.

![](assets/mobile-wf-setup.png)

提供iOS和Android平台的信息，包括您的应用程序ID和身份验证密钥或密钥文件。

## 实施{#implement-mobile-wf}

下一步提供了将代码安装到移动设备应用程序的分步指南。

![](assets/mobile-wf-add-code.png)


## 验证{#valid-mobile-wf}

查看并检查实施以验证它。 您可以发送测试推送通知。

![](assets/mobile-wf-valid.png)


## 请查看 {#review-mobile-wf}

自动化设置已完成。 您现在可以访问标记移动资产，配置规则或数据元素，并开始使用Adobe Journey Optimizer发送推送通知。

![](assets/mobile-wf-done.png)


**相关主题**

* [推送通知入门](get-started-push.md)
* [推送通知数据流和组件](push-gs.md)
* [配置推送渠道](push-configuration.md)
* [推送通知报告](../reports/journey-global-report.md#push-global)
* [创建推送通知](create-push.md)
