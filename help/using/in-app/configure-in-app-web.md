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

* 确保您使用的是最新版本的 **Adobe Experience Platform Web SDK** 扩展。

* 安装 **Adobe Experience Platform Web SDK** 中的扩展 **标记属性** 并启用 **个性化存储** 选项。

  此配置对于在客户端上存储事件历史记录至关重要，这是在规则生成器中实施频率规则的先决条件。 [了解详情](https://experienceleague.adobe.com/docs/experience-platform/tags/extensions/client/web-sdk/web-sdk-extension-configuration.html?lang=en)

  ![](assets/configure_web_inapp_1.png)

## 配置发送数据到平台规则 {#configure-sent-data-trigger}

1. 访问 **Adobe Experience Platform数据收集** 实例并导航到 **标记属性** 已使用 **Adobe Experience Platform Web SDK** 扩展。

1. 从 **创作** 菜单，选择 **规则** 则 **创建新规则** 或 **添加规则**.

   ![](assets/configure_web_inapp_2.png)

1. 在 **活动** 部分，单击 **添加** 并按照以下方式对其进行配置：

   * **扩展名**：核心

   * **事件类型**：Library Loaded (Page Top)。

   ![](assets/configure_web_inapp_3.png)

1. 单击 **保留更改** 以保存事件配置。

1. 在 **操作** 部分，单击 **添加** 并按照以下方式对其进行配置：

   * **扩展名**：Adobe Experience Platform Web SDK

   * **操作类型**：发送事件

   ![](assets/configure_web_inapp_4.png)

1. 在 **个性化** 部分 **操作** 类型，启用 **呈现可视化个性化决策** 选项。

   ![](assets/configure_web_inapp_5.png)

1. 在 **决策上下文** 部分，定义 **键** 和 **值** 确定要投放的体验的对。

   ![](assets/configure_web_inapp_6.png)

1. 保存您的 **操作** 通过单击 **保留更改**.

1. 导航至 **发布流** 菜单。 新建 **库** 或选择现有 **库** 并添加您新创建的 **规则** 敬它。 [了解详情](https://experienceleague.adobe.com/docs/experience-platform/tags/publish/libraries.html?lang=en#create-a-library)

1. 来自您的 **库**，选择 **保存并构建到开发环境**.

   ![](assets/configure_web_inapp_7.png)

## 配置手动规则 {#configure-manual-trigger}

1. 访问 **Adobe Experience Platform数据收集** 实例并导航到 **标记属性** 已使用 **Adobe Experience Platform Web SDK** 扩展。

1. 从 **创作** 菜单，选择 **规则** 则 **创建新规则** 或 **添加规则**.

   ![](assets/configure_web_inapp_8.png)

1. 在 **活动** 部分，单击 **添加** 并按照以下方式对其进行配置：

   * **扩展名**：核心

   * **事件类型**：单击

   ![](assets/configure_web_inapp_9.png)

1. 在 **单击配置**，定义 **选择器** 将会被评估。

   ![](assets/configure_web_inapp_10.png)

1. 单击 **保留更改** 以保存 **事件** 配置。

1. 在 **操作** 部分，单击 **添加** 并按照以下方式对其进行配置：

   * **扩展名**：Adobe Experience Platform Web SDK

   * **操作类型**：评估规则集

   ![](assets/configure_web_inapp_11.png)

1. 在 **评估规则集操作** 部分 **操作** 类型，启用 **呈现可视化个性化决策** 选项。

   ![](assets/configure_web_inapp_13.png)

1. 在 **决策上下文** 部分，定义 **键** 和 **值** 确定要投放的体验的对。

1. 访问 **发布流** 菜单，新建 **库** 或选择现有 **库** 并添加您新创建的 **规则**. [了解详情](https://experienceleague.adobe.com/docs/experience-platform/tags/publish/libraries.html?lang=en#create-a-library)

1. 来自您的 **库**，选择 **保存并构建到开发环境**.

   ![](assets/configure_web_inapp_14.png)

