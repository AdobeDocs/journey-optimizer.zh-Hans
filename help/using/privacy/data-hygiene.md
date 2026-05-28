---
solution: Journey Optimizer
product: journey optimizer
title: 执行数据生命周期操作
description: 了解如何执行数据生命周期操作
feature: Privacy, Monitoring
role: User
level: Intermediate
exl-id: 8045b559-bf5e-4b5f-9da4-accd44641a68
TQID: https://experienceleague.adobe.com/-zue9aNrWtfL3MGs7OjH-1CF436mzPh50fsru8OSEq8
product_v2:
  - id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2:
  - id: aeebb91a-f216-4d5f-8da1-3a7e6f696ed0
  - id: bb359667-ec7d-4d4b-8663-5850fc219d32
subfeature_v2:
  - id: a9cf78bf-e9e4-4836-85a5-b6b3cf93bf56
  - id: f365ec33-2b99-4b7f-b4ee-c743dd7f615f
  - id: c8d5f2ce-ba44-43e9-a2bf-94a3d7d85ec3
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
topic_v2:
  - id: aa2f3246-cb95-4b30-8899-fdf7d73550cc
  - id: d095671a-1355-40aa-8b5f-06c33c68080b
  - id: f4e6943a-c91a-4134-a2c7-f4f20cfff2f0
source-git-commit: 0ee10a0689d38c22b1180b197796b08a10c286cf
workflow-type: tm+mt
source-wordcount: 235
ht-degree: 100%

---

# 执行数据生命周期操作 {#data-hygiene}

>[!AVAILABILITY]
>
>目前，数据生命周期功能仅适用于已购买 **Healthcare Shield** 和 **Privacy and Security Shield** 附加产品的组织。

随着数据不断被摄取到 Adobe Experience Platform 中，确保根据组织策略按预期使用数据、在必要时更新数据和删除数据至关重要。

这些任务可以借助&#x200B;**[!UICONTROL 数据生命周期]**&#x200B;菜单完成，您可以通过它配置和计划数据生命周期操作，以确保正确维护记录。

![](assets/data-hygiene.png)


## 推荐做法 {#data-hygiene-recommendations}

执行数据卫生操作（如删除身份或数据集）时，请注意，与已删除身份关联的历史投放事件将不再出现在标准报告或数据湖查询中。 这可能会导致收件人收件箱中报告为&#x200B;**已投放**&#x200B;的电子邮件数量与&#x200B;**已接收**&#x200B;的电子邮件数量存在差异，尤其是对于较旧的历程而言。

在执行大规模删除操作之前，请验证并导出任何所需的投放或报告数据。 如果在执行数据卫生操作之后需要协调，请与 Adobe 支持人员联系以访问存档的日志，或者使用“消息反馈事件数据集”查询最近的数据。

## 了解详情 {#data-hygiene-learn-more}

有关 Privacy Service 以及如何执行数据生命周期操作的更多信息，请参阅 Adobe Experience Platform 文档：

* [Privacy Service 概述](https://experienceleague.adobe.com/docs/experience-platform/privacy/home.html?lang=zh-Hans)
* [Adobe Experience Platform 中的数据生命周期](https://experienceleague.adobe.com/docs/experience-platform/hygiene/home.html?lang=zh-Hans)
