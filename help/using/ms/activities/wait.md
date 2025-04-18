---
solution: Journey Optimizer
product: journey optimizer
title: 在编排的活动中使用等待活动
description: 了解如何在编排的活动中使用等待活动
badge: label="Alpha"
hide: true
hidefromtoc: true
exl-id: 11ef095b-77ec-4e2e-ab4d-49a248354f08
source-git-commit: bdc584c1aae0c735d81dfc95e11f96f755bea26a
workflow-type: tm+mt
source-wordcount: '169'
ht-degree: 78%

---

# 等待 {#wait}

>[!CONTEXTUALHELP]
>id="ajo_orchestration_wait"
>title="等待活动"
>abstract="**等待**&#x200B;活动用于将过渡从一个活动推迟另一个活动。"

**等待**&#x200B;活动是&#x200B;**流量控制**&#x200B;活动。它可为两个执行的活动之间添加一段等待的时间。例如，在执行电子邮件投放活动后，等待几天，再分析这期间产生的打开次数和点击次数，然后再执行所有后续操作（提醒电子邮件、创建受众等）。

## 配置{#wait-configuration}

请按照以下步骤操作，配置&#x200B;**等待**&#x200B;活动：

1. 将&#x200B;**等待**&#x200B;活动添加到您的编排营销活动中。

1. 指定集客过渡和叫客过渡之间等待的&#x200B;**持续时间**。

1. 在&#x200B;**期间**&#x200B;字段中选择时间单位：秒、分钟、小时、天。

## 示例{#wait-example}

下面的示例展示了典型用例中的&#x200B;**等待**&#x200B;活动。发送某个活动的电子邮件邀请。发送邀请 24 小时后，短信投放会发送给同一群体。

![](../assets/workflow-wait-example.png)
