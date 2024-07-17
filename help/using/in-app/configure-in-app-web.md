---
title: 在Journey Optimizer中创建Web应用程序内消息
description: 了解如何在Journey Optimizer中创建Web应用程序内消息
feature: In App
topic: Content Management
role: User
level: Beginner
keywords: 应用程序内、消息、创建、入门
source-git-commit: d3f0adab52ed8e44a6097c5079396d1e9c06e0a7
workflow-type: tm+mt
source-wordcount: '408'
ht-degree: 2%

---


# 配置Web应用程序内渠道 {#configure-in-app-web}

## 先决条件 {#prerequisites}

* 确保您使用的是适用于您的&#x200B;**Adobe Experience Platform Web SDK**&#x200B;扩展的最新版本。

* 在&#x200B;**标记属性**&#x200B;中安装&#x200B;**Adobe Experience Platform Web SDK**&#x200B;扩展并启用&#x200B;**Personalization Storage**&#x200B;选项。

  此配置对于在客户端上存储事件历史记录至关重要，这是在规则生成器中实施频率规则的先决条件。 [了解详情](https://experienceleague.adobe.com/docs/experience-platform/tags/extensions/client/web-sdk/web-sdk-extension-configuration.html?lang=en)

  ![](assets/configure_web_inapp_1.png)

## 配置发送数据到平台规则 {#configure-sent-data-trigger}

1. 访问您的&#x200B;**Adobe Experience Platform数据收集**&#x200B;实例，并导航到配置了&#x200B;**Adobe Experience Platform Web SDK**&#x200B;扩展的&#x200B;**标记属性**。

1. 从&#x200B;**创作**&#x200B;菜单中，选择&#x200B;**规则**，然后选择&#x200B;**创建新规则**&#x200B;或&#x200B;**添加规则**。

   ![](assets/configure_web_inapp_2.png)

1. 在&#x200B;**事件**&#x200B;部分中，单击&#x200B;**添加**&#x200B;并按如下方式进行配置：

   * **扩展**：核心

   * **事件类型**：已加载库（页面顶部）。

   ![](assets/configure_web_inapp_3.png)

1. 单击&#x200B;**保留更改**&#x200B;以保存事件配置。

1. 在&#x200B;**操作**&#x200B;部分中，单击&#x200B;**添加**&#x200B;并按如下方式进行配置：

   * **扩展**： Adobe Experience Platform Web SDK

   * **操作类型**：发送事件

   ![](assets/configure_web_inapp_4.png)

1. 在&#x200B;**操作**&#x200B;类型的&#x200B;**Personalization**&#x200B;部分中，启用&#x200B;**呈现可视化个性化决策**&#x200B;选项。

   ![](assets/configure_web_inapp_5.png)

1. 在&#x200B;**决策上下文**&#x200B;部分中，定义用于确定要交付的体验的&#x200B;**键**&#x200B;和&#x200B;**值**&#x200B;对。

   ![](assets/configure_web_inapp_6.png)

1. 通过单击&#x200B;**保留更改**&#x200B;保存您的&#x200B;**操作**&#x200B;配置。

1. 导航到&#x200B;**发布流**&#x200B;菜单。 创建新的&#x200B;**库**&#x200B;或选择现有的&#x200B;**库**，并将新创建的&#x200B;**规则**&#x200B;添加到其中。 [了解详情](https://experienceleague.adobe.com/docs/experience-platform/tags/publish/libraries.html?lang=en#create-a-library)

1. 从您的&#x200B;**库**&#x200B;中，选择&#x200B;**保存并生成到开发**。

   ![](assets/configure_web_inapp_7.png)

## 配置手动规则 {#configure-manual-trigger}

1. 访问您的&#x200B;**Adobe Experience Platform数据收集**&#x200B;实例，并导航到配置了&#x200B;**Adobe Experience Platform Web SDK**&#x200B;扩展的&#x200B;**标记属性**。

1. 从&#x200B;**创作**&#x200B;菜单中，选择&#x200B;**规则**，然后选择&#x200B;**创建新规则**&#x200B;或&#x200B;**添加规则**。

   ![](assets/configure_web_inapp_8.png)

1. 在&#x200B;**事件**&#x200B;部分中，单击&#x200B;**添加**&#x200B;并按如下方式进行配置：

   * **扩展**：核心

   * **事件类型**：单击

   ![](assets/configure_web_inapp_9.png)

1. 在&#x200B;**Click配置**&#x200B;中，定义将评估的&#x200B;**选择器**。

   ![](assets/configure_web_inapp_10.png)

1. 单击&#x200B;**保留更改**&#x200B;以保存&#x200B;**事件**&#x200B;配置。

1. 在&#x200B;**操作**&#x200B;部分中，单击&#x200B;**添加**&#x200B;并按如下方式进行配置：

   * **扩展**： Adobe Experience Platform Web SDK

   * **操作类型**：评估规则集

   ![](assets/configure_web_inapp_11.png)

1. 在&#x200B;**操作**&#x200B;类型的&#x200B;**评估规则集操作**&#x200B;部分中，启用&#x200B;**呈现可视化个性化决策**&#x200B;选项。

   ![](assets/configure_web_inapp_13.png)

1. 在&#x200B;**决策上下文**&#x200B;部分中，定义用于确定要交付的体验的&#x200B;**键**&#x200B;和&#x200B;**值**&#x200B;对。

1. 访问&#x200B;**发布流**&#x200B;菜单，创建新的&#x200B;**库**，或选择现有的&#x200B;**库**&#x200B;并添加新创建的&#x200B;**规则**。 [了解详情](https://experienceleague.adobe.com/docs/experience-platform/tags/publish/libraries.html?lang=en#create-a-library)

1. 从您的&#x200B;**库**&#x200B;中，选择&#x200B;**保存并生成到开发**。

   ![](assets/configure_web_inapp_14.png)

