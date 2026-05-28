---
solution: Journey Optimizer
product: journey optimizer
title: 忠诚度数据和数据集
description: 了解忠诚度挑战需要哪些Adobe Experience Platform用户档案数据和数据集，以及数据集生存时间(TTL)如何影响保留。
feature: Journeys
topic: Content Management
role: Admin, Developer
level: Intermediate
hide: true
badge: label="私人测试版" type="Informative"
mini-toc-levels: 1
exl-id: a7c4e1b2-8f3d-4a6c-9e0b-1d2e3f4a5b6c
feature_v2: []
subfeature_v2: []
source-git-commit: 2e01cd1880b8527911376d94188d0204f7649541
workflow-type: tm+mt
source-wordcount: 538
ht-degree: 5%

---

# 忠诚度数据和数据集 {#loyalty-data-and-datasets}

>[!BEGINSHADEBOX]

**目录**

[忠诚度挑战入门](get-started.md)

<table style="table-layout:fixed">
<tr style="border: 0;">
<td style="vertical-align:top;">

**创建和管理挑战**

* [访问和管理挑战和任务](access-loyalty-challenges.md)
* [创建挑战](create-challenges.md)
* [创建任务](create-tasks.md)
* [监测忠诚度挑战表现](loyalty-reporting.md)

</td>
<td style="vertical-align:top;">

**配置并集成**

* [配置忠诚度挑战](loyalty-admin.md)
* **忠诚度数据和数据集** ◀︎ **您在这里**
* [忠诚度挑战API参考](https://developer.adobe.com/journey-optimizer-apis/references/loyalty-challenges){target="_blank"}

</td>
</tr>
</table>

>[!ENDSHADEBOX]

>[!AVAILABILITY]
>
>此功能当前处于&#x200B;**私人测试版**&#x200B;中。 有关发行周期和可用性阶段的完整详细信息，请参阅 [Journey Optimizer 发行周期](../rn/releases.md)。

## 概述 {#overview}

忠诚度挑战依赖于Adobe Experience Platform的身份标识、配置文件属性、体验事件和受众。 使用此页面可了解要准备哪些数据、涉及哪些数据集以及&#x200B;**生存时间(TTL)**&#x200B;在您创作挑战或使用忠诚度挑战API之前对保留率有何影响。

请联系Adobe管理员以设置Journey Optimizer，或在&#x200B;**[!UICONTROL 忠诚度管理员]**&#x200B;菜单中配置奖励履行和事件映射。 [了解如何配置忠诚度挑战](loyalty-admin.md)。 有关REST端点和身份验证，请参阅[忠诚度挑战API参考](https://developer.adobe.com/journey-optimizer-apis/references/loyalty-challenges){target="_blank"}。

## Adobe Experience Platform数据 {#aep-data}

### 轮廓属性 {#profile-attributes}

在&#x200B;**[!DNL XDM Individual Profile]**&#x200B;类中挑战受众、个性化和报告使用配置文件。 将您用于会员挑战的身份标识[命名空间](https://experienceleague.adobe.com/zh-hans/docs/experience-platform/identity/features/namespaces){target="_blank"}与您在个人资料数据中的成员标识方式以及在&#x200B;**[!UICONTROL 会员管理员]**&#x200B;菜单的&#x200B;**[!UICONTROL 全局设置]**&#x200B;中选择的命名空间保持一致。

对于配置文件上的标准忠诚度属性（积分、层、计划、状态和相关字段），请使用Experience Platform **[忠诚度详细信息](https://experienceleague.adobe.com/zh-hans/docs/experience-platform/xdm/field-groups/profile/loyalty-details){target="_blank"}**&#x200B;架构字段组。 该字段组定义`loyalty`对象及其属性（例如`points`、`tier`、`program`和`status`）。

➡️ [忠诚度详细信息架构字段组](https://experienceleague.adobe.com/zh-hans/docs/experience-platform/xdm/field-groups/profile/loyalty-details){target="_blank"}

### 体验事件 {#experience-events}

**[!UICONTROL 购买]**、**[!UICONTROL 支出]**&#x200B;和&#x200B;**[!UICONTROL 自定义事件]**&#x200B;任务依赖于摄取到Adobe Experience Platform中的体验事件。 对于&#x200B;**[!UICONTROL 自定义事件]**&#x200B;任务，必须在&#x200B;**[!UICONTROL 忠诚度管理员]**&#x200B;菜单中配置匹配的事件定义（标识符路径、可选XDM架构ID、架构和转换器），然后营销人员才能在任务生成器中输入自定义事件值。 [了解如何配置事件定义](loyalty-admin.md#event-definitions)

确保事件有效负载使用与“忠诚度挑战”配置相同的身份命名空间，以便将进度归因于正确的配置文件。

### 受众和报表 {#audiences-reporting}

营销人员在配置挑战资格时选择Platform [受众](../audience/about-audiences.md)。 忠诚度报表功能板使用Adobe Customer Journey Analytics。 [了解如何监测忠诚度挑战绩效](loyalty-reporting.md)

## 数据集生存时间(TTL) {#dataset-ttl}

忠诚度挑战将操作和报表数据存储在Adobe Experience Platform数据集中（包括为您的项目创建的事件和个性化相关数据集）。 数据集&#x200B;**生存时间(TTL)**&#x200B;控制数据在数据湖中保留多长时间，如果适用，在配置文件存储中保留多长时间。

Journey Optimizer将TTL护栏应用于许多系统生成的数据集。 与忠诚度相关的数据集遵循与沙盒相同的平台保留模型。

在Journey Optimizer中➡️ [数据集生存时间(TTL)护栏](../data/datasets-ttl.md)

>[!NOTE]
>
>组织级别的忠诚度配置可以包括通过忠诚度元数据服务管理的存档和保留设置（例如存档持续时间）。 如果需要调整私人测试版环境的维系情况，请与Adobe管理员联系。
