---
solution: Journey Optimizer
product: journey optimizer
title: 架构入门
description: 了解如何在 Adobe Journey Optimizer 中使用 Adobe Experience Platform 架构
feature: Data Model, Datasets, Data Management
role: Developer, Admin
level: Experienced
keywords: 架构, 平台, 数据, 结构
exl-id: c2a8df2e-ff94-4f9a-a53e-bbf9f663cc81
TQID: https://experienceleague.adobe.com/fWsW9Rvyd8L4nphczzc7GF1rbO7HuYsjqDBBpy3uoGU
product_v2:
  - id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2:
  - id: d556b755-390a-43f0-be32-a08cf6236126
subfeature_v2:
  - id: b3a93754-a8b8-46eb-9421-7eccaeeb3dff
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2:
  - id: b23e006f-0a29-4f1d-8fd0-77aa56f3d12b
  - id: e0eb8757-182f-49f3-94a4-1587d16f5094
  - id: ebde5b41-29c9-4f5e-9ef6-1197e85409e3
source-git-commit: f9b8e1590f14cdcd00432295c653769f753b9b40
workflow-type: tm+mt
source-wordcount: 440
ht-degree: 100%

---

# 架构入门 {#schemas-gs}

[!DNL Adobe Journey Optimizer] 依赖&#x200B;**Adobe Experience Platform 架构**，以一致且可重用的方式描述数据结构。 架构为现实世界对象（如人物）提供抽象定义，并规定该对象的每个实例应包含的数据（如姓名、生日等）。 当数据被摄取到 Experience Platform 时，始终按照 **XDM 架构**&#x200B;进行结构化处理。

## 标准与关系架构

Adobe Experience Platform 中有两种类型的架构：

* **标准架构**&#x200B;是使用类和字段组的层级式架构，用于捕获记录或时间序列数据。

  标准架构由以下部分组成：

   * 一个&#x200B;**类**（用于定义数据行为：记录型或时间序列型）。
   * 一个或多个&#x200B;**字段组**（用于向架构添加特定字段）。

  在 Journey Optimizer 中，标准架构通常用于呈现&#x200B;**单个用户及其属性**、捕获&#x200B;**时间序列交互**（如点击、购买或登录）以及驱动&#x200B;**实时客户轮廓**&#x200B;以实现细分与个性化。

  ➡️ [通过此视频学习如何创建和配置标准架构](#video-schema)（视频）

* **关系架构**&#x200B;是扁平化、非层级式的架构，不使用类或字段组。 它们被用于捕获关系实体的记录数据，主要用在[!DNL Journey Optimizer]**编排的营销活动**&#x200B;中。

  关系实体的示例包括：
   * 预订、合同或订阅
   * 产品或目录
   * 商店、位置或合作伙伴

  通过关系架构，您可为每个实体（如每次预订、每项订阅）发送一条消息，基于实体属性（如产品类别、门店位置）创建细分群体，并通过触达与实体关联的所有联系人来提升可寻址能力。

  关系架构的工作原理：

   1. **手动创建架构或通过 DDL 导入**
   1. **关联架构**&#x200B;以定义实体与人员之间的关系（例如：与会员关联的忠诚度交易、与品牌关联的奖励）。
   1. 从支持的数据源&#x200B;**将数据摄取**&#x200B;至数据集中。

  ➡️[了解如何管理关系架构和数据集](../orchestrated/gs-schemas.md)
➡️[编排的营销活动快速入门](../orchestrated/gs-schemas.md)

## 操作说明视频{#video-schema}

了解如何创建标准架构、添加字段组、创建并配置自定义字段组。

>[!VIDEO](https://video.tv.adobe.com/v/3416868?captions=chi_hans&quality=12)

>[!MORELIKETHIS]
>
>* [Journey Optimizer 中的数据管理入门](gs-data.md)
>* [创建架构、数据集并摄取数据，以在 Journey Optimizer 中添加测试轮廓](../audience/creating-test-profiles.md)
>* [XDM 系统概述](https://experienceleague.adobe.com/docs/experience-platform/xdm/home.html?lang=zh-Hans){target="_blank"}
>* [数据建模的最佳做法](https://experienceleague.adobe.com/docs/experience-platform/xdm/schema/best-practices.html?lang=zh-Hans){target="_blank"}
>* [使用架构注册表 API 创建架构](https://experienceleague.adobe.com/docs/experience-platform/xdm/tutorials/create-schema-api.html?lang=zh-Hans){target="_blank"}
>* [使用架构编辑器定义两个架构之间的关系](https://experienceleague.adobe.com/docs/experience-platform/xdm/tutorials/relationship-ui.html?lang=zh-Hans){target="_blank"}
