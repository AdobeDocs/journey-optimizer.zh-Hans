---
title: 数据收集
description: 了解关于决策管理反馈数据收集的更多信息
feature: Offers
topic: Integrations
role: User
level: Intermediate
source-git-commit: b06b545d377fcd1ffe6ed218badeb94c1bb85ef2
workflow-type: tm+mt
source-wordcount: '441'
ht-degree: 1%

---

# 决策管理数据收集 {#data-collection}

## 了解数据收集

您可以在Adobe Experience Platform中收集offer decisioning反馈，包括显示哪些选件以及用户如何与它们进行交互。 此数据可用于：
* 撰写 [决策管理报告](../reports/get-started-events.md)；
* 使用 [频率封顶](../offer-library/add-constraints.md#capping) 规则；
* 构建 [AI模型](../ranking/create-ranking-strategies.md) 可以用作排名方法。

## 事件类型

收集数据的方式因您要捕获的事件类型而异。

### 决策事件

每次Decision Management做出决策时，与该决策事件相关的信息都是 **自动** 已发送到所有渠道的Adobe Experience Platform。 [了解详情](../reports/get-started-events.md)

### 展示和点击事件

决策管理展示次数和点击次数定义如下：

* An **印象** 事件是指向用户显示选件时。

* A **点击** 事件是指用户单击选件或与选件交互时。

系统会根据以下内容捕获展示次数和点击次数的反馈： [!DNL Journey Optimizer] 使用的渠道。

1. 一方面，一些渠道 **自动** 跟踪展示次数和点击次数。 具体情况如下：

   * 电子邮件创作人 [!DNL Journey Optimizer]
   * 由创作的移动推送通知 [!DNL Journey Optimizer]
   * 使用的移动设备应用程序 [Adobe Experience Platform Web SDK](https://experienceleague.adobe.com/docs/experience-platform/edge/web-sdk-faq.html#what-is-adobe-experience-platform-web-sdk%3F){target="_blank"} 或Mobile SDK<!--TBC--> 渲染选件 <!--need more info + link-->

   >[!NOTE]
   >
   >如果Adobe在渠道上向最终用户直观地呈现选件，您可以假设Adobe将在反馈中自动发送。

1. Adobe Experience Platform另一方面，某些渠道要求将展示次数和点击次数数据作为 **体验事件**.

   使用移动应用程序的除外 [Adobe Experience Platform Web SDK](https://experienceleague.adobe.com/docs/experience-platform/edge/web-sdk-faq.html#what-is-adobe-experience-platform-web-sdk%3F){target="_blank"} 或Mobile SDK<!--TBC-->，所有使用决策API请求接收优惠的渠道都需要将反馈作为体验事件发送。 这包括：

   * 网页
   * 信息亭
   * 通过第三方应用程序发送的消息

   >[!NOTE]
   >
   >如果选件需要有关如何渲染的说明，则可以假设您应将反馈作为体验事件发送。

### 自定义事件

您可根据自己的偏好将有关与优惠绑定的自定义事件的反馈发送到Adobe Experience Platform。 例如，如果选件具有多个按钮，例如 *感兴趣*， *不感兴趣*&#x200B;等等，您可能希望单独发送这些事件，但这些事件也可以作为体验事件发送。 <!--Not sure to get that part. How feedback is collected in the first case, i.e. when events are sent in separately? Does it mean the customer just handles it the wau he wants?-->

## 发送反馈数据

要发送反馈数据，您需要创建一个数据集以收集事件，并针对每个事件类型定义一个将发送到Adobe Experience Platform中的体验事件。

* 了解如何创建将在其中收集体验事件的数据集 [本节](create-dataset.md).

* 了解如何定义要在中发送反馈数据的体验事件 [本节](schema-requirement.md).

