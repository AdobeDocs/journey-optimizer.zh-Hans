---
solution: Journey Optimizer, Experience Platform
product: Journey Optimizer
title: 快速入门
description: 了解如何开始使用产品建议库 API，使用决策引擎执行关键操作。
badge: label="旧版" type="Informative"
feature: Decision Management, API
topic: Integrations
role: Developer
level: Experienced
exl-id: 773bee50-849f-4b07-9423-67de5279ad28
version: Journey Orchestration
TQID: https://experienceleague.adobe.com/LZVllKIbmPvNnT0wCskFj3mcNYcKRmvAT85UqWlsztA
product_v2:
  - id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2:
  - id: a4cb03e1-327e-499d-9de8-e0c0db8a63a2
  - id: ad78185d-8f79-40ad-9bad-cbde74af74ee
role_v2:
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2:
  - id: bce87dde-a4ab-44c9-8a18-ad66e4ddb377
  - id: c1579802-ddd4-4214-8a91-97b2066abe11
subfeature_v2:
  - id: a7a194a0-75e2-4913-8a83-14714fbf68e6
  - id: eb547372-2a95-4d13-b0fd-f720c9895880
  - id: e30b0a1a-b594-47b8-af94-1e3a2be6df11
source-git-commit: 0ee10a0689d38c22b1180b197796b08a10c286cf
workflow-type: tm+mt
source-wordcount: 447
ht-degree: 100%

---

# 决策管理 API 开发人员指南 {#decision-management-api-developer-guide}

>[!TIP]
>
>决策是 [!DNL Adobe Journey Optimizer] 的全新决策功能，现已通过基于代码的体验和电子邮件渠道提供！ [了解详情](../../experience-decisioning/gs-experience-decisioning.md)

>[!CONTEXTUALHELP]
>id="od_api_support"
>title="新的决策管理 API"
>abstract="用于创建和管理决策管理对象的新 API 现已推出。 旧版 API 支持的截止日期为 2024 年 3 月 27 日。"

>[!CONTEXTUALHELP]
>id="ajo_decisioning_api_support"
>title="新的决策管理 API"
>abstract="用于创建和管理决策管理对象的新 API 现已推出。 旧版 API 支持的截止日期为 2024 年 3 月 27 日。"

本开发人员指南提供了帮助您开始使用 [!DNL Offer Library] API 的步骤。 此外，该指南提供了使用决策引擎执行关键操作的示例 API 调用。

➡️ [在此视频中了解更多关于决策管理组件的信息](#video)

## 先决条件 {#prerequisites}

本指南要求您对 Adobe Experience Platform 的以下组件有一定了解：

* [[!DNL Experience Data Model (XDM) System]](https://experienceleague.adobe.com/docs/experience-platform/xdm/home.html?lang=zh-Hans){target="_blank"}：[!DNL Experience Platform]用于组织客户体验数据的标准化框架。
   * [架构组合基础知识](https://experienceleague.adobe.com/docs/experience-platform/xdm/schema/composition.html?lang=zh-Hans){target="_blank"}：了解 XDM 架构的基本构建块。
* [决策管理](../../../using/offers/get-started/starting-offer-decisioning.md)：介绍在一般情况下用于决策和专门用于决策管理的概念和组件。 说明在客户体验期间用于选择最佳呈现选项的策略。
* [[!DNL Profile Query Language (PQL)]](https://experienceleague.adobe.com/docs/experience-platform/segmentation/pql/overview.html?lang=zh-Hans){target="_blank"}：PQL 是一种功能强大的语言，可用于通过 XDM 实例编写表达式。 PQL 用于定义决策规则。

## 正在读取示例 API 调用 {#reading-sample-api-calls}

本指南提供了示例 API 调用来演示如何格式化请求。 这些包括路径、必需的标头和格式正确的请求负载。 还提供了在 API 响应中返回的示例 JSON。 有关示例 API 调用的文档中所用惯例的信息，请参阅故障排除指南中的[如何读取示例 API 调用](https://experienceleague.adobe.com/docs/experience-platform/landing/troubleshooting.html?lang=zh-Hans#how-do-i-format-an-api-request){target="_blank"}[!DNL Experience Platform]。

## 收集所需标头的值 {#gather-values-for-required-headers}

为调用 [!DNL Adobe Experience Platform] API，您必须先完成[身份验证教程](https://experienceleague.adobe.com/docs/experience-platform/landing/platform-apis/api-authentication.html?lang=zh-Hans){target="_blank"}。 完成身份验证教程会提供所有 [!DNL Experience Platform] API 调用中每个所需标头的值，如下所示：

* `Authorization: Bearer {ACCESS_TOKEN}`
* `x-api-key: {API_KEY}`
* `x-gw-ims-org-id: {IMS_ORG}`
* `x-sandbox-name: {SANDBOX_NAME}`

包含负载 (POST、PUT、PATCH) 的所有请求都需要额外的标头：

* `Content-Type: application/json`

>[!NOTE]
>
>权限检查根据分配的产品配置文件强制执行。 只有关联产品配置文件中授予的权限，才能决定可通过 API 访问或管理哪些资源。

## 后续步骤 {#next-steps}

本文档介绍了调用 [!DNL Offer Library] API 所需的必备知识。 您现在可以继续进行本开发人员指南中提供的示例调用，并按照其说明进行操作。
<!--
>[!NOTE]
>
> The In-app messaging channel in Adobe Journey Optimizer uses decision management objects. If your organization uses the in-app messaging channel, then API list requests for objects will include objects created by the in-app messaging service and can be ignored for decision management use cases. Objects created for in-app messages will have `createdBy = "Mobile_Sheliak"`.
-->

<!--
 
## How-to video {#video}

The following video is intended to support your understanding of the components of Decision Management.

>[!VIDEO](https://video.tv.adobe.com/v/329919?quality=12)
-->
