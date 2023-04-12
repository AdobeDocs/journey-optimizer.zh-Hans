---
title: 数据收集
description: 了解有关决策管理反馈数据收集的更多信息
feature: Offers
topic: Integrations
role: User
level: Intermediate
source-git-commit: c9e970bc231fc3d19f0243b71256ea0f5a981af7
workflow-type: tm+mt
source-wordcount: '397'
ht-degree: 3%

---

# 决策管理数据收集 {#data-collection}

## 了解数据收集

您可以在Adobe Experience Platform中收集offer decisioning反馈，包括显示哪些选件以及用户与这些选件的交互方式。 此数据可用于：
* 合成 [决策管理报告](../reports/get-started-events.md);
* 使用 [频率封顶](../offer-library/add-constraints.md#capping) 规则；
* 建筑 [AI模型](../ranking/create-ranking-strategies.md) 可用作排名方法。

## 事件类型

数据收集的方式因您要捕获的事件类型而异。

### 决策事件

每次决策管理人员做出决策时，与该决策事件相关的信息是 **自动** 已发送到Adobe Experience Platform（所有渠道）。 [了解详情](../reports/get-started-events.md)

### 展示和点击事件

决策管理展示次数和点击次数的定义如下：

* 安 **印象** 事件是指向用户显示选件时。

* A **单击** 事件是指用户单击或与选件交互时。

根据 [!DNL Journey Optimizer] 使用的渠道。

**电子邮件** 由创作者 [!DNL Journey Optimizer] **自动** 跟踪展示次数和点击次数。

但是， **最多渠道** 需要将展示次数和点击次数数据作为 **体验事件**. 这包括：

* 网页使用 [Adobe Experience Platform Web SDK](https://experienceleague.adobe.com/docs/experience-platform/edge/home.html?lang=zh-Hans){target="_blank"} 渲染选件

* 移动设备应用程序使用 [Adobe Experience Platform Mobile SDK](https://experienceleague.adobe.com/docs/platform-learn/data-collection/mobile-sdk/overview.html){target="_blank"} to render offers - [Learn more](https://developer.adobe.com/client-sdks/documentation/adobe-journey-optimizer-decisioning/#ab-sj-tracking-servers){target="_blank"}
* 网亭
* 通过第三方应用程序发送的消息
   <!--Mobile push notifications authored by [!DNL Journey Optimizer] - [Learn more](https://developer.adobe.com/client-sdks/documentation/adobe-journey-optimizer/api-reference/#handlenotificationresponse){target="_blank"}-->

>[!NOTE]
>
>使用决策API请求接收选件的渠道需要将反馈作为体验事件发送到。 换言之，如果选件需要有关如何渲染的说明，您可以假定您应当作为体验事件发送反馈。

### 自定义事件

有关与选件绑定的自定义事件的反馈，可根据您自己的偏好发送到Adobe Experience Platform。 例如，如果选件具有多个按钮，例如 *感兴趣*, *不感兴趣*&#x200B;等，则您可能希望单独发送这些事件，但这些事件也可以作为体验事件发送。 <!--Not sure to get that part. How feedback is collected in the first case, i.e. when events are sent in separately? Does it mean the customer just handles it the wau he wants?-->

## 发送反馈数据

要发送反馈数据，您需要创建一个数据集以收集事件，并为每个事件类型定义一个将发送到Adobe Experience Platform的体验事件。

* 了解如何创建将在其中收集体验事件的数据集 [此部分](create-dataset.md).

* 了解如何定义体验事件以在 [此部分](schema-requirement.md).

