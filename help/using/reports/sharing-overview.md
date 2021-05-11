---
title: 历程步骤共享概述
description: 历程步骤共享概述
translation-type: tm+mt
source-git-commit: 55b9e5d8ed259ec6ed7746e835691d7d6261a8a4
workflow-type: tm+mt
source-wordcount: '423'
ht-degree: 6%

---

# 创建旅程报告{#design-jo-reports}

![](../assets/do-not-localize/badge.png)

除了[实时报告](live-report.md)和内置[全局报告功能](global-report.md)之外，[!DNL Journey Optimizer]还可以自动将旅程性能数据发送到Adobe Experience Platform，以便与其他数据组合以用于分析目的。

>[!NOTE]
>
>默认情况下，不会对所有新部署的实例激活此功能。 激活应要求提供。

例如，您已设置了发送多个电子邮件的旅程。 此功能允许您将[!DNL Journey Optimizer]数据与下游事件数据相结合，例如发生了多少转换、网站上发生了多少参与，或商店中发生了多少事务。 旅程信息可以与Adobe Experience Platform上的数据相结合，无论是从其他数字资产还是从离线资产，都可以提供更全面的性能视图。

[!DNL Journey Optimizer] 为个人在旅程中执行的每个步骤，自动创建必要的模式和流到数据集中。步骤事件对应于在旅程中从一个节点移动到另一个节点的个人。 例如，在具有事件、条件和动作的旅程中，将向Adobe Experience Platform发送三步事件。

传递的XDM字段的列表是全面的。 有些代码包含系统生成的代码，而有些代码则有易读的易读名称。 示例包括旅程活动的标签或步骤状态：操作超时或以错误结束的次数。

>[!CAUTION]
>
>无法打开数据集以用于实时用户档案服务。 请确保&#x200B;**[!UICONTROL Profile]**&#x200B;切换关闭。

历程在数据出现时以流方式发送数据。 您可以使用查询服务来查询此数据。 您可以连接到Customer Journey Analytics或其他BI工具，以视图与这些步骤相关的数据。

将创建以下模式:

* [!DNL Journey Orchestration]的历程步骤用户档案事件模式 — 体验事件，了解在历程中执行的步骤以及用于映射到单个历程参与者的身份映射。
* [!DNL Journey Orchestration]的历程步骤事件模式 — 与历程元数据绑定的历程步骤事件。
* 历程模式[!DNL Journey Orchestration]的历程字段 — 用于描述历程的历程元数据。

![](../assets/sharing1.png)

![](../assets/sharing2.png)

传递了以下数据集：

* [!DNL Journey Orchestration]的历程步骤用户档案事件模式
* 历程步骤事件
* 历程

![](../assets/sharing3.png)

传递到Adobe Experience Platform的XDM字段的列表在以下位置有详细说明：

* [journeySteps 事件常用字段](../reports/sharing-common-fields.md)
* [journeyStep 事件操作执行字段](../reports/sharing-execution-fields.md)
* [journeyStep 事件数据提取字段](../reports/sharing-fetch-fields.md)
* [journeyStep 事件身份字段](../reports/sharing-identity-fields.md)
* [历程场](../reports/sharing-journey-fields.md)

有关将步骤事件报告到Adobe Experience Platform的详细信息，请观看此[教程视频](https://experienceleague.adobe.com/docs/journey-orchestration-learn/tutorials/reporting-step-events-to-adobe-experience-platform.html)。
