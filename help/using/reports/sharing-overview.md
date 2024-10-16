---
solution: Journey Optimizer
product: journey optimizer
title: 历程步骤共享概述
description: 历程步骤共享概述
feature: Journeys, Reporting
topic: Content Management
role: Data Engineer, Data Architect, Admin
level: Experienced
exl-id: 29d6b881-35a3-4c62-9e7d-d0aeb206ea77
source-git-commit: 47482adb84e05fe41eb1c50479a8b50e00469ec4
workflow-type: tm+mt
source-wordcount: '521'
ht-degree: 3%

---

# 创建历程报告 {#design-jo-reports}

除了[实时报表](live-report.md)和内置[报表功能](report-gs-cja.md)之外，[!DNL Journey Optimizer]还可以自动将历程性能数据发送到Adobe Experience Platform，以便将其与其他数据结合进行分析。

>[!NOTE]
>
>默认情况下，历程步骤事件的所有实例都会激活此功能。 您无法修改或更新在预配步骤事件期间创建的架构和数据集。 默认情况下，这些架构和数据集处于只读模式。

例如，您已设置发送多封电子邮件的历程。 此功能允许您将[!DNL Journey Optimizer]数据与下游事件数据相结合，如发生了多少转化、网站上发生了多少参与或存储中发生了多少事务。 历程信息可与Adobe Experience Platform上的其他数字资产或离线资产中的数据相结合，以更全面地查看性能。

[!DNL Journey Optimizer]会自动创建必要的架构，并针对个人在旅程中执行的每个步骤，将数据集流式传输到Adobe Experience Platform。 步骤事件对应于在历程中从某个节点移动到另一个节点的个人。 例如，在包含事件、条件和操作的历程中，会将三个步骤事件发送到Adobe Experience Platform。

在某些情况下，可以为同一节点创建多个事件。 例如，在等待活动的情况下：

* 配置文件进入wait时生成一个事件（journeyNodeProcessed属性等于false）
* 当配置文件退出时会生成一个事件（journeyNodeProcessed属性等于true）

传递的XDM字段列表是全面的。 有些包含系统生成的代码，而其他则具有易于用户识别的友好名称。 示例包括历程活动的标签或步骤状态：操作超时或出错的次数。

>[!CAUTION]
>
>无法为实时配置文件服务打开数据集。 请确保已关闭&#x200B;**[!UICONTROL 配置文件]**&#x200B;切换开关。

[!DNL Journey Optimizer]在发生数据时以流式方式发送数据。 您可以使用查询服务查询此数据。 您可以连接到Customer Journey Analytics或其他BI工具，以查看与这些步骤相关的数据。

将创建以下架构：

* [!DNL Journey Orchestration]的历程步骤事件架构 — 与历程元数据绑定的历程步骤事件。
* 具有[!DNL Journey Orchestration]的历程字段的历程架构 — 描述历程的历程元数据。

![](assets/sharing1.png)

![](assets/sharing2.png)

传递以下数据集：

* 历程步骤事件
* 历程

![](assets/sharing3.png)

此处详细列出了传递到Adobe Experience Platform的XDM字段列表：

* [步骤事件字段列表](../reports/sharing-field-list.md)
* [旧版步骤事件字段](../reports/sharing-legacy-fields.md)

## 与Customer Journey Analytics集成 {#integration-cja}

[!DNL Journey Optimizer]步骤事件可以链接到[Adobe Customer Journey Analytics](https://experienceleague.adobe.com/docs/analytics-platform/using/cja-overview/cja-overview.html?lang=zh-Hans){target="_blank"}中的其他数据集。

一般工作流程为：

* [!DNL Customer Journey Analytics]摄取“历程步骤事件”数据集。
* 关联的“Journey Orchestration的历程步骤事件架构”中的&#x200B;**profileID**&#x200B;字段被定义为标识字段。 在[!DNL Customer Journey Analytics]中，您可以将此数据集链接到与基于人员的标识符具有相同值的任何其他数据集。
* 要在[!DNL Customer Journey Analytics]中使用此数据集，对于跨渠道历程分析，请参阅[Customer Journey Analytics文档](https://experienceleague.adobe.com/docs/analytics-platform/using/cja-usecases/cross-channel.html){target="_blank"}。

➡️[使用Customer Journey Analytics](cja-ajo.md){target="_blank"}
