---
solution: Journey Optimizer
product: journey optimizer
title: 历程报告
description: 了解如何使用历程报告中的电子邮件数据
feature: Reporting, Journeys
topic: Content Management
role: User
level: Intermediate
exl-id: 82558447-9d42-4fac-8fc1-fded9bf4bfcc
source-git-commit: 32f34b6e2a5cd3eda6de9177c5a4b5c2be7b8058
workflow-type: tm+mt
source-wordcount: '1037'
ht-degree: 2%

---

# 电子邮件历程报告 {#journey-global-report}

>[!BEGINSHADEBOX]

由于Apple为其本机邮件应用程序引入了新的隐私保护功能（包括邮件隐私保护），发件人将无法再使用跟踪像素来收集有关已启用Apple邮件隐私保护的用户档案的数据。 因此，Adobe Journey Optimizer使用跟踪像素跟踪电子邮件打开次数的功能可能会受到影响。 [了解更多](https://experienceleaguecommunities.adobe.com/t5/adobe-campaign-classic-blogs/the-impact-of-apple-ios-privacy-changes-on-email-marketing-and/ba-p/699780)有关Apple iOS隐私更改对电子邮件营销的影响。

我们建议将重点放在点击量和转化量度上，而不是放在打开率上，以获取更准确的见解。

>[!ENDSHADEBOX]

## 已交付与点击趋势 {#delivered-click}

![](assets/cja-journey-email-delivered.png)

**[!UICONTROL 已投放与点击趋势]**&#x200B;图显示您的用户档案与电子邮件交互的详细分析，提供了有关各种域如何与您的内容交互的宝贵见解。

+++ 了解更多有关已交付与点击趋势量度的信息

* **[!UICONTROL 已投放]**：成功发送的电子邮件数与已发送的电子邮件总数相关。

* **[!UICONTROL 点击次数]**：内容在电子邮件中的点击次数。

+++

## 投放状态 {#delivery-status}

![](assets/cja-journey-email-delivery-stat.png)

**[!UICONTROL 投放状态]**&#x200B;图表让您一目了然地查看电子邮件的执行情况。 跟踪关键量度，如投放和退回，让您快速了解电子邮件历程的效率。

+++ 了解有关投放状态量度的更多信息

* **[!UICONTROL 已投放]**：成功发送的电子邮件数与已发送的电子邮件总数相关。

* **[!UICONTROL 出站渠道的跳出次数]**：发送进程和自动返回处理期间累计的错误总数与已发送消息的总数之比。

* **[!UICONTROL 出站错误]**：发送过程中发生的阻止将错误发送到配置文件的错误总数。

* **[!UICONTROL 已排除]**： Adobe Journey Optimizer已排除的用户档案数。

+++

## 发送统计信息 {#email-sending-statistics}

![](assets/cja-journey-email-sending-stat.png)

**[!UICONTROL 发送统计数据]**&#x200B;表清晰地显示了您的电子邮件在历程中的执行情况。 它跟踪投放率和交互等关键量度，为您提供宝贵的见解以优化电子邮件策略以实现更好的触及率和参与度。

+++ 了解有关发送统计量度的更多信息

* **[!UICONTROL 人员]**：符合消息目标用户档案资格的用户档案数。

* **[!UICONTROL 目标]**：发送过程中处理的电子邮件总数。

* **[!UICONTROL 发送]**：您的电子邮件的发送总数。

* **[!UICONTROL 已投放]**：成功发送的电子邮件数与已发送的邮件总数相关。

* **[!UICONTROL 跳出次数]**：在发送进程和自动返回处理期间累计的错误总数与已发送消息的总数之比。

* **[!UICONTROL 出站错误]**：发送过程中发生的阻止将错误发送到配置文件的错误总数。

* **[!UICONTROL 出站排除]**： Adobe Journey Optimizer已排除的用户档案数。

+++

## 电子邮件 - 跟踪统计数据 {#email-tracking}

![](assets/cja-journey-email-track-stat.png)

**[!UICONTROL 电子邮件 — 跟踪统计数据]**&#x200B;表提供与历程中包含的电子邮件相关的配置文件活动的详细帐户。 其中包括打开次数、点击次数和其他相关参与指示器的指标，可全面了解用户档案与电子邮件内容的交互方式。

+++ 了解有关跟踪统计量度的更多信息

* **[!UICONTROL 点进率(CTR)]**：与电子邮件交互的用户百分比。

* **[!UICONTROL 点进打开率(CTOR)]**：电子邮件的打开次数。

* **[!UICONTROL 点击次数]**：内容在电子邮件中的点击次数。

* **[!UICONTROL 唯一点击次数]**：点击电子邮件中内容的用户档案数。

* **[!UICONTROL 电子邮件打开次数]**：您的电子邮件在历程中打开的次数。

* **[!UICONTROL 独特电子邮件打开次数]**：已打开电子邮件的百分比。

* **[!UICONTROL 垃圾邮件投诉次数]**：将邮件声明为垃圾邮件或垃圾邮件的次数。

* **[!UICONTROL 取消订阅]**：取消订阅链接的点击次数。

+++

## 电子邮件域 {#email-domains}

![](assets/cja-journey-email-domain.png)

**[!UICONTROL 电子邮件域]**&#x200B;表提供了按域分类的电子邮件的深入细分，提供了对电子邮件历程性能指标的广泛分析。 通过这种全面的分析，您可以了解不同域在响应电子邮件内容时的行为。

+++ 了解有关电子邮件域指标的更多信息

* **[!UICONTROL 发送]**：您的电子邮件的发送总数。

* **[!UICONTROL 已投放]**：成功发送的电子邮件数与已发送的电子邮件总数相关。

* **[!UICONTROL 电子邮件打开次数]**：您的电子邮件在历程中打开的次数。

* **[!UICONTROL 点击次数]**：内容在电子邮件中的点击次数。

* **[!UICONTROL 出站渠道的跳出次数]**：发送进程和自动返回处理期间累计的错误总数与已发送电子邮件的总数相关。

* **[!UICONTROL 出站错误]**：发送过程中发生的阻止将错误发送到配置文件的错误总数。
+++

## 跟踪关联标签 {#track-link-label}

![](assets/cja-journey-tracked-link-labels.png)

**[!UICONTROL 跟踪的链接标签]**&#x200B;表提供了电子邮件中链接标签的全面概述，突出显示生成最高访客流量的那些标签。 此功能使您能够识别最受欢迎的链接并确定其优先级。

+++ 了解有关跟踪链接标签量度的更多信息

* **[!UICONTROL 唯一点击次数]**：点击电子邮件中内容的用户档案数。

* **[!UICONTROL 点击次数]**：内容在电子邮件中的点击次数。

+++

## 跟踪关联 URL {#track-link-url}

![](assets/cja-journey-tracked-link-urls.png)

**[!UICONTROL 跟踪的链接URL]**&#x200B;表提供了您的电子邮件中吸引最高访客流量的URL的全面概述。 这使您能够识别最受欢迎的链接并排定其优先级，从而加深您对电子邮件中特定内容的用户档案参与情况的了解。

+++ 了解有关跟踪的链接URL量度的更多信息

* **[!UICONTROL 唯一点击次数]**：点击电子邮件中内容的用户档案数。

* **[!UICONTROL 点击次数]**：内容在电子邮件中的点击次数。

* **[!UICONTROL 显示]**：消息的打开次数。

* **[!UICONTROL 独特显示]**：消息的打开次数，一个用户档案的多个交互未考虑在内。

+++

## 电子邮件主题 {#email-subject}

![](assets/cja-journey-email-subjects.png)

**[!UICONTROL 电子邮件主题]**&#x200B;表全面概述了吸引最多访客流量的电子邮件主题。 此资源提供了有关受众参与动态的有价值见解。

+++ 了解有关电子邮件主题量度的更多信息

* **[!UICONTROL 人员]**：有资格作为电子邮件目标配置文件的用户配置文件数。

+++

## 退回原因 {#email-bounce-reasons}

**[!UICONTROL 退回原因]**&#x200B;表编译与退回邮件相关的可用数据，提供关于电子邮件退回具体原因的详细见解。

有关退回的详细信息，请参阅[禁止显示列表](../reports/suppression-list.md)页面。

## 排除的原因 {#email-excluded}

**[!UICONTROL 排除的原因]**&#x200B;表提供了导致从目标受众中排除用户个人资料导致未收到该消息的各种因素的综合视图。

有关排除原因的完整列表，请参阅[此页面](exclusion-list.md)。

## 错误原因 {#email-errors}

**[!UICONTROL 错误原因]**&#x200B;表提供了在发送过程中发生的特定错误的可见性，提供了有关错误性质和发生情况的宝贵信息。
