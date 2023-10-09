---
title: 快速入门
description: 了解如何开始使用优惠库 API，使用决策引擎执行关键操作。
feature: Offers
topic: Integrations
role: User
level: Intermediate
exl-id: 773bee50-849f-4b07-9423-67de5279ad28
source-git-commit: 7e9984aee1eba29a2757b025ca0aa1092d95a761
workflow-type: tm+mt
source-wordcount: '373'
ht-degree: 93%

---

# 决策管理 API 开发人员指南 {#decision-management-api-developer-guide}

>[!CONTEXTUALHELP]
>id="od_api_support"
>title="新的决策管理API"
>abstract="现已提供用于创建和管理决策管理对象的新API。 旧版api的支持将持续到2024年3月27日。"

本开发人员指南提供了帮助您开始使用 [!DNL Offer Library] API 的步骤。此外，该指南提供了使用决策引擎执行关键操作的示例 API 调用。

➡️ [通过本视频进一步了解决策管理的组件](#video)

## 先决条件 {#prerequisites}

本指南要求您对 Adobe Experience Platform 的以下组件有一定了解：

* [[!DNL Experience Data Model (XDM) System]](https://experienceleague.adobe.com/docs/experience-platform/xdm/home.html?lang=zh-Hans){target="_blank"}：[!DNL Experience Platform] 用于组织客户体验数据的标准化框架。
   * [架构组合基础知识](https://experienceleague.adobe.com/docs/experience-platform/xdm/schema/composition.html?lang=zh-Hans){target="_blank"}：了解 XDM 架构的基本构建块。
* [决策管理](../../../using/offers/get-started/starting-offer-decisioning.md)：介绍在一般情况下用于 Experience Decisioning 和专门用于决策管理的概念和组件。说明在客户体验期间用于选择最佳呈现选项的策略。
* [[!DNL Profile Query Language (PQL)]](https://experienceleague.adobe.com/docs/experience-platform/segmentation/pql/overview.html?lang=zh-Hans){target="_blank"}：PQL 是一种功能强大的语言，可用于通过 XDM 实例编写表达式。PQL 用于定义决策规则。

## 正在读取示例 API 调用 {#reading-sample-api-calls}

本指南提供了示例 API 调用来演示如何格式化请求。这些包括路径、必需的标头和格式正确的请求负载。还提供了在 API 响应中返回的示例 JSON。有关示例 API 调用的文档中使用的惯例信息，请参阅 [!DNL Experience Platform] 故障排除指南中的[如何读取示例 API 调用](https://experienceleague.adobe.com/docs/experience-platform/landing/troubleshooting.html?lang=zh-Hans#how-do-i-format-an-api-request){target="_blank"}。

## 收集所需标头的值 {#gather-values-for-required-headers}

为调用 [!DNL Adobe Experience Platform] API，您必须先完成[身份验证教程](https://experienceleague.adobe.com/docs/experience-platform/landing/platform-apis/api-authentication.html?lang=zh-Hans){target="_blank"}。完成身份验证教程会提供所有 [!DNL Experience Platform] API 调用中每个所需标头的值，如下所示：

* `Authorization: Bearer {ACCESS_TOKEN}`
* `x-api-key: {API_KEY}`
* `x-gw-ims-org-id: {IMS_ORG}`
* `x-sandbox-name: {SANDBOX_NAME}`

包含负载 (POST、PUT、PATCH) 的所有请求都需要额外的标头：

* `Content-Type: application/json`

## 后续步骤 {#next-steps}

本文档介绍了调用 [!DNL Offer Library] API 所需的必备知识。您现在可以继续进行本开发人员指南中提供的示例调用，并按照其说明进行操作。
<!--
>[!NOTE]
>
> The In-app messaging channel in Adobe Journey Optimizer uses decision management objects. If your organization uses the in-app messaging channel, then API list requests for objects will include objects created by the in-app messaging service and can be ignored for decision management use cases. Objects created for in-app messages will have `createdBy = “Mobile_Sheliak”`.
-->

## 操作方法视频 {#video}

以下视频旨在帮助您了解决策管理的各个组件。

>[!VIDEO](https://video.tv.adobe.com/v/329919?quality=12)

