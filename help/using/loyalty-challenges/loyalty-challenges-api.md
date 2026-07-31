---
solution: Journey Optimizer
product: journey optimizer
title: 忠诚度挑战API
description: 了解如何使用忠诚度挑战REST API以编程方式管理Adobe Journey Optimizer中的挑战并查询用户档案参与状态。
feature: Journeys
topic: Content Management
role: Developer
level: Intermediate
exl-id: a1b2c3d4-e5f6-7890-abcd-ef1234567890
feature_v2: []
subfeature_v2: []
source-git-commit: 3756e104086c83bbca88b2fe770a40a8e9f39ef3
workflow-type: tm+mt
source-wordcount: 315
ht-degree: 8%

---


# 忠诚度挑战API {#loyalty-challenges-api}

>[!BEGINSHADEBOX]

**在此页面上：**&#x200B;了解如何使用忠诚度挑战REST API以编程方式创建和管理挑战，以及查询和更新个人档案的挑战参与状态。

>[!ENDSHADEBOX]

## 快速访问 {#quick-access}

有两个REST API可用于解决忠诚度难题：

* **[忠诚度挑战元数据API](https://developer.adobe.com/journey-optimizer-apis/references/loyalty-challenges){target="_blank"}** — 以编程方式创建、检索、更新、发布、存档和重复挑战。
* **[忠诚度质询状态API](https://developer.adobe.com/journey-optimizer-apis/references/loyalty-challenges-state){target="_blank"}** — 查询和更新个人档案的质询参与状态。

## 忠诚度挑战元数据API {#metadata-api}

忠诚度挑战元数据API允许您在Journey Optimizer UI之外管理挑战的整个生命周期。 使用它可以自动执行挑战操作，或将忠诚度计划管理集成到您自己的工具和工作流程中。 例如，您可以创建、发布和存档挑战，通过筛选和排序检索所有挑战，或复制现有挑战（包括其历程元数据和营销活动）。

➡️ [忠诚度挑战元数据API引用](https://developer.adobe.com/journey-optimizer-apis/references/loyalty-challenges){target="_blank"}

## 忠诚度挑战状态API {#state-api}

忠诚度挑战状态API允许您在配置文件级别与挑战参与记录进行交互。 使用它查询用户档案的当前参与状态、进度和任务完成 — 例如，检索用户档案的所有挑战参与记录，检查挑战中特定任务的状态，或从一个或多个挑战中撤销用户档案。

➡️ [忠诚度挑战状态API参考](https://developer.adobe.com/journey-optimizer-apis/references/loyalty-challenges-state){target="_blank"}

## 身份验证 {#authentication}

所有忠诚度挑战API调用都需要以下标头：

| 标头 | 描述 |
|---|---|
| `Authorization` | IMS访问令牌中的持有者令牌 |
| `x-gw-ims-org-id` | 您的IMS组织ID |
| `x-api-key` | 您的客户端ID（API密钥） |
| `x-sandbox-name` | 要定位的沙盒的名称 |

按照[身份验证教程](https://developer.adobe.com/journey-optimizer-apis/references/authentication){target="_blank"}来检索这些凭据。
