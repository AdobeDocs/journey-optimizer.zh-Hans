---
solution: Journey Optimizer
product: journey optimizer
title: 在编排的营销活动中使用等待活动
description: 了解如何在编排的活动中使用等待活动
exl-id: 11ef095b-77ec-4e2e-ab4d-49a248354f08
version: Campaign Orchestration
TQID: https://experienceleague.adobe.com/-AI0PuvH2o43jG3d6cpP9-IwD6LxL37nzFv19R-wkcQ
product_v2:
  - id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2:
  - id: b3538224-471e-4c63-a444-9b19d89ae29c
  - id: b423a773-0a58-4a77-b65d-3dd4ae6ef841
subfeature_v2:
  - id: b5e335a9-0e5f-4dda-8845-c4ac5dca2be4
source-git-commit: 0ee10a0689d38c22b1180b197796b08a10c286cf
workflow-type: tm+mt
source-wordcount: 233
ht-degree: 55%

---

# 等待 {#wait}

>[!CONTEXTUALHELP]
>id="ajo_orchestration_wait"
>title="等待活动"
>abstract="**等待**&#x200B;活动用于将过渡从一个活动推迟另一个活动。"

**[!UICONTROL 等待]**&#x200B;活动是一个&#x200B;**[!UICONTROL 流量控制]**&#x200B;组件，用于在编排的营销活动中的两个活动之间引入延迟。 这有助于确保在更合适的时间进行后续行动，并且使后续行动对用户参与度的影响更大。

例如，您可以在投放电子邮件后等待几天，以便跟踪打开数和点击数，然后再发送后续消息。

## 配置{#wait-configuration}

>[!IMPORTANT]
>
>临时表中的数据在&#x200B;**5天**&#x200B;之后不再保留。 当您使用&#x200B;**[!UICONTROL 持续时间]**&#x200B;或&#x200B;**[!UICONTROL 固定时间]**&#x200B;等待时，请确保直至下一个活动在该限制内完成所用的时间，以便中间数据保持可用。

请按照以下步骤操作，配置&#x200B;**[!UICONTROL 等待]**&#x200B;活动：

1. 将&#x200B;**[!UICONTROL 等待]**&#x200B;活动添加到您的编排营销活动中。

1. 选择最适合您需求的等待类型：

   * **[!UICONTROL 持续时间]**：以秒、分钟、小时或天为单位指定延迟，然后再进行下一个活动。

   * **[!UICONTROL 固定时间]**：设置下一个活动开始的特定日期和时间。

   ![](../assets/wait_activity.png)

## 示例{#wait-example}

下面的示例展示了典型用例中的&#x200B;**[!UICONTROL 等待]**&#x200B;活动。  将会发送包含促销代码的电子邮件给庆祝生日的轮廓。 2天后，将向同一组发送短信，提醒其生日促销代码即将过期。

![](../assets/wait-example.png)
