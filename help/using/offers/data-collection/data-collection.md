---
title: 数据收集
description: 了解关于决策管理反馈数据收集的更多信息
feature: Offers
topic: Integrations
role: User
level: Intermediate
exl-id: 278cb255-439c-4ce8-ab59-07df79774b98
source-git-commit: 803c9f9f05669fad0a9fdeeceef58652b6dccf70
workflow-type: tm+mt
source-wordcount: '397'
ht-degree: 3%

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

**电子邮件** 创作者 [!DNL Journey Optimizer] **自动** 跟踪展示次数和点击次数。

但是， **大多数渠道** Adobe Experience Platform要求将展示次数和点击次数数据作为 **体验事件**. 这包括：

* 使用的网页 [Adobe Experience Platform Web SDK](https://experienceleague.adobe.com/docs/experience-platform/edge/home.html?lang=zh-Hans){target="_blank"} 渲染选件

* 使用的移动设备应用程序 [Adobe Experience Platform Mobile SDK](https://experienceleague.adobe.com/docs/platform-learn/data-collection/mobile-sdk/overview.html){target="_blank"} to render offers - [Learn more](https://developer.adobe.com/client-sdks/documentation/adobe-journey-optimizer-decisioning/#ab-sj-tracking-servers){target="_blank"}
* 信息亭
* 通过第三方应用程序发送的消息
   <!--Mobile push notifications authored by [!DNL Journey Optimizer] - [Learn more](https://developer.adobe.com/client-sdks/documentation/adobe-journey-optimizer/api-reference/#handlenotificationresponse){target="_blank"}-->

>[!NOTE]
>
>使用决策API请求接收优惠的渠道需要作为体验事件发送反馈。 换言之，如果选件需要有关如何渲染的说明，则可以假设您应将反馈作为体验事件发送。

### 自定义事件

您可根据自己的偏好将有关与优惠绑定的自定义事件的反馈发送到Adobe Experience Platform。 例如，如果选件具有多个按钮，例如 *感兴趣*， *不感兴趣*&#x200B;等等，您可能希望单独发送这些事件，但这些事件也可以作为体验事件发送。

## 发送反馈数据

要发送反馈数据，您需要创建一个数据集以收集事件，并针对每个事件类型定义一个将发送到Adobe Experience Platform中的体验事件。

* 了解如何创建将在其中收集体验事件的数据集 [本节](create-dataset.md).

* 了解如何定义要在中发送反馈数据的体验事件 [本节](schema-requirement.md).
