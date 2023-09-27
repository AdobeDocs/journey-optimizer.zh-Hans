---
title: 快速入门
description: 了解如何开始使用优惠库API以使用决策引擎执行关键操作。
feature: Offers
topic: Integrations
role: User
level: Intermediate
exl-id: 773bee50-849f-4b07-9423-67de5279ad28
source-git-commit: 805f7bdc921c53f63367041afbb6198d0ec05ad8
workflow-type: tm+mt
source-wordcount: '349'
ht-degree: 7%

---

# Decision Management API开发人员指南 {#decision-management-api-developer-guide}

本开发人员指南提供了帮助您开始使用 [!DNL Offer Library] API。 然后，该指南提供了使用决策引擎执行关键操作的示例API调用。

➡️ [通过本视频进一步了解决策管理的组件](#video)

## 先决条件 {#prerequisites}

本指南要求您对Adobe Experience Platform的以下组件有一定的了解：

* [[!DNL Experience Data Model (XDM) System]](https://experienceleague.adobe.com/docs/experience-platform/xdm/home.html?lang=zh-Hans){target="_blank"}：用于实现此目标的标准化框架 [!DNL Experience Platform] 组织客户体验数据。
   * [模式组合基础](https://experienceleague.adobe.com/docs/experience-platform/xdm/schema/composition.html?lang=zh-Hans){target="_blank"}：了解XDM架构的基本构建块。
* [决策管理](../../../using/offers/get-started/starting-offer-decisioning.md)：说明用于一般Experience Decisioning和特定决策管理的概念和组件。 说明用于选择在客户体验期间呈现的最佳选项的策略。
* [[!DNL Profile Query Language (PQL)]](https://experienceleague.adobe.com/docs/experience-platform/segmentation/pql/overview.html){target="_blank"}：PQL是一种功能强大的语言，可用于通过XDM实例编写表达式。 pql用于定义决策规则。

## 正在读取示例API调用 {#reading-sample-api-calls}

本指南提供了示例API调用来演示如何格式化请求。 这些资源包括路径、必需的标头和格式正确的请求负载。 还提供了在API响应中返回的示例JSON。 有关文档中用于示例API调用的惯例的信息，请参阅 [如何读取示例API调用](https://experienceleague.adobe.com/docs/experience-platform/landing/troubleshooting.html#how-do-i-format-an-api-request){target="_blank"} 在 [!DNL Experience Platform] 疑难解答指南。

## 收集所需标题的值 {#gather-values-for-required-headers}

为了调用 [!DNL Adobe Experience Platform] API，您必须先完成 [身份验证教程](https://experienceleague.adobe.com/docs/experience-platform/landing/platform-apis/api-authentication.html){target="_blank"}. 完成身份验证教程将为所有标头中的每个标头提供值 [!DNL Experience Platform] API调用，如下所示：

* `Authorization: Bearer {ACCESS_TOKEN}`
* `x-api-key: {API_KEY}`
* `x-gw-ims-org-id: {IMS_ORG}`
* `x-sandbox-name: {SANDBOX_NAME}`

包含有效负载(POST、PUT、PATCH)的所有请求都需要额外的标头：

* `Content-Type: application/json`

## 后续步骤 {#next-steps}

本文档介绍了调用 [!DNL Offer Library] API。 您现在可以继续本开发人员指南中提供的示例调用，并按照其说明进行操作。
<!--
>[!NOTE]
>
> The In-app messaging channel in Adobe Journey Optimizer uses decision management objects. If your organization uses the in-app messaging channel, then API list requests for objects will include objects created by the in-app messaging service and can be ignored for decision management use cases. Objects created for in-app messages will have `createdBy = “Mobile_Sheliak”`.
-->

## 操作方法视频 {#video}

以下视频旨在支持您了解决策管理的各个组件。

>[!VIDEO](https://video.tv.adobe.com/v/329919?quality=12)

