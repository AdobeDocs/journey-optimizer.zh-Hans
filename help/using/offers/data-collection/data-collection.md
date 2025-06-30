---
title: 数据收集
description: 了解有关决策管理反馈数据收集的更多信息
feature: Decision Management, Datasets
topic: Integrations
role: User, Data Engineer, Developer
level: Experienced
exl-id: 278cb255-439c-4ce8-ab59-07df79774b98
source-git-commit: 07b1f9b885574bb6418310a71c3060fa67f6cac3
workflow-type: tm+mt
source-wordcount: '386'
ht-degree: 1%

---

# 决策管理数据收集 {#data-collection}

## 了解数据收集

您可以在Adobe Experience Platform中收集Offer Decisioning反馈，包括显示了哪些选件以及用户如何与它们进行交互。 此数据可用于：
* 构成[决策管理报告](../reports/get-started-events.md)；
* 使用[频率封顶](../offer-library/add-constraints.md#capping)规则；
* 正在生成可用作排名方法的[AI模型](../ranking/create-ranking-strategies.md)。

## 事件类型

数据收集的方式因您要捕获的事件类型而异。

### 决策事件

每次决策管理做出决策时，与该决策事件相关的信息都&#x200B;**自动**&#x200B;发送到所有渠道的Adobe Experience Platform。 [了解详情](../reports/get-started-events.md)

### 展示和点击事件

决策管理展示次数和点击次数定义如下：

* 向用户显示选件时出现&#x200B;**展示**&#x200B;事件。

* **click**&#x200B;事件是指用户点击选件或与选件交互时。

根据使用的[!DNL Journey Optimizer]渠道，捕获展示次数和点击次数的反馈。

**电子邮件**&#x200B;由[!DNL Journey Optimizer] **创作**&#x200B;自动跟踪展示次数和点击次数。

但是，**大多数渠道**&#x200B;要求将展示次数和点击次数数据作为&#x200B;**体验事件**&#x200B;发送到Adobe Experience Platform。 这包括：

* 使用[Adobe Experience Platform Web SDK](https://experienceleague.adobe.com/docs/experience-platform/edge/home.html?lang=zh-Hans){target="_blank"}呈现选件的网页

* 使用[Adobe Experience Platform Mobile SDK](https://experienceleague.adobe.com/docs/platform-learn/data-collection/mobile-sdk/overview.html?lang=zh-Hans){target="_blank"}呈现选件的移动应用 — [了解更多](https://developer.adobe.com/client-sdks/documentation/adobe-journey-optimizer-decisioning/#ab-sj-tracking-servers){target="_blank"}
* 信息亭
* 通过第三方应用程序发送的消息
  <!--Mobile push notifications authored by [!DNL Journey Optimizer] - [Learn more](https://developer.adobe.com/client-sdks/documentation/adobe-journey-optimizer/api-reference/#handlenotificationresponse){target="_blank"}-->

>[!NOTE]
>
>使用决策API请求接收优惠的渠道需要以体验事件的形式发送反馈。 换言之，如果选件需要有关如何呈现的说明，您可以假设应将反馈作为体验事件发送。

### 自定义事件

您可根据自己的偏好将关于与选件关联的自定义事件的反馈发送到Adobe Experience Platform。 例如，如果选件具有多个按钮（如&#x200B;*感兴趣*、*不感兴趣*&#x200B;等），您可能希望单独发送这些事件，但这些事件也可以作为体验事件发送。

## 发送反馈数据

要发送反馈数据，您需要创建一个数据集以收集事件，并针对每种事件类型定义一个将发送到Adobe Experience Platform的体验事件。

* 了解如何在[此部分](create-dataset.md)中创建将收集体验事件的数据集。

* 在[本节](schema-requirement.md)中了解如何定义体验事件以发送反馈数据。
