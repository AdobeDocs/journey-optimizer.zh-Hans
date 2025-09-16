---
solution: Journey Optimizer
product: journey optimizer
title: 架构入门
description: 了解如何在 Adobe Journey Optimizer 中使用 Adobe Experience Platform 架构
feature: Data Model, Datasets, Data Management
role: Data Engineer, Data Architect, Admin
level: Experienced
keywords: 架构, 平台, 数据, 结构
exl-id: c2a8df2e-ff94-4f9a-a53e-bbf9f663cc81
source-git-commit: 70f647cf4e95c1152a5c16395b88b11a6b72865c
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---

# 架构入门 {#schemas-gs}

[!DNL Adobe Journey Optimizer]依赖&#x200B;**Adobe Experience Platform架构**&#x200B;以一致且可重用的方式描述数据结构。 模式提供了真实世界对象（如人）的抽象定义，并概述了该对象的每个实例中应包含哪些数据（如名称、生日等）。 将数据摄取到Experience Platform中时，其结构始终遵循&#x200B;**XDM架构**。

## 标准和关系架构

Adobe Experience Platform中有两种类型的架构：

* **标准架构**&#x200B;是使用类和字段组捕获记录或时间序列数据的分层架构。

  标准模式由以下部分组成：

   * **类**（定义数据行为：记录或时间序列）。
   * 一个或多个&#x200B;**字段组** （用于向架构添加特定字段）。

  在Journey Optimizer中，标准架构通常用于表示&#x200B;**个人及其属性**，捕获&#x200B;**时间序列交互**（例如点击、购买或登录），以及用于分段和个性化的强大的&#x200B;**实时客户个人资料**。

  ➡️ [在此视频中了解如何创建和配置标准架构](#video-schema)（视频）

* **关系架构**&#x200B;是不使用类或字段组的平面非分层架构。 它们用于捕获关系实体的记录数据，主要用于[!DNL Journey Optimizer] **编排的营销活动**。

  关系实体的示例包括：
   * 预订、合同或订阅
   * 产品或目录
   * 商店、位置或合作伙伴

  使用关系架构时，您可以为每个实体发送一条消息（例如，每个预订、每个订阅），根据实体属性（例如，产品类别、商店位置）创建区段，并通过联系链接到实体的所有联系人来提高可寻址性。

  关系架构的工作方式：

   1. **手动创建架构或通过DDL导入**
   1. **链接架构**&#x200B;以定义实体和人员之间的关系（例如，与成员关联的忠诚度交易，与品牌关联的奖励）。
   1. **从支持的源将数据摄取**&#x200B;到您的数据集中。

  ➡️ [了解如何管理关系架构和数据集](../orchestrated/gs-schemas.md)
➡️ [开始使用编排的营销活动](../orchestrated/gs-schemas.md)

## 操作说明视频{#video-schema}

了解如何创建标准架构、添加字段组、创建和配置自定义字段组。

>[!VIDEO](https://video.tv.adobe.com/v/334461?quality=12)

>[!MORELIKETHIS]
>
>* [创建架构、数据集并摄取数据，以在 Journey Optimizer 中添加测试轮廓](../audience/creating-test-profiles.md)
>* [XDM 系统概述](https://experienceleague.adobe.com/docs/experience-platform/xdm/home.html?lang=zh-Hans){target="_blank"}
>* [数据建模的最佳做法](https://experienceleague.adobe.com/docs/experience-platform/xdm/schema/best-practices.html?lang=zh-Hans){target="_blank"}
>* [使用架构注册表 API 创建架构](https://experienceleague.adobe.com/docs/experience-platform/xdm/tutorials/create-schema-api.html?lang=zh-Hans){target="_blank"}
>* [使用架构编辑器定义两个架构之间的关系](https://experienceleague.adobe.com/docs/experience-platform/xdm/tutorials/relationship-ui.html?lang=zh-Hans){target="_blank"}
