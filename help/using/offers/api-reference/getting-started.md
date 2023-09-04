---
title: 快速入门
description: 了解如何开始使用优惠库API以使用决策引擎执行关键操作。
feature: Offers
topic: Integrations
role: User
level: Intermediate
exl-id: 773bee50-849f-4b07-9423-67de5279ad28
source-git-commit: e7431d1b69e460471b01439c9bd2577fd69944ed
workflow-type: tm+mt
source-wordcount: '565'
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

包含有效负载(POST、PUT、PATCH)的所有请求都需要额外的标头：

* `Content-Type: application/json`

## 管理对容器的访问 {#manage-access-to-container}

容器是一种隔离机制，用于隔离不同的关注点。 容器ID是所有存储库API的第一个路径元素。 所有决策对象都驻留在容器中。

管理员可以将相似的主体、资源和访问权限分组到配置文件中。 这减轻了管理负担，并受 [Adobe Admin Console](https://adminconsole.adobe.com/). 您必须是组织中Adobe Experience Platform的产品管理员，才能创建配置文件并将用户分配给这些配置文件。 只需一次性创建符合特定权限的产品配置文件即可，然后只需将用户添加到这些配置文件中。 用户档案充当已授予权限的组，该组中的每个实际用户或技术用户都会继承这些权限。

授予管理员权限，您可以通过授予或撤销用户权限 [Adobe Admin Console](https://adminconsole.adobe.com/){target="_blank"}. For more information, see the [Access control overview](https://experienceleague.adobe.com/docs/experience-platform/access-control/home.html?lang=zh-Hans){target="_blank"}.

### 列出用户和集成可访问的容器 {#list-containers-accessible-to-users-and-integrations}

**API格式**

```http
GET /{ENDPOINT_PATH}?product={PRODUCT_CONTEXT}&property={PROPERTY}==decisioning
```

| 参数 | 描述 | 示例 |
| --------- | ----------- | ------- |
| `{ENDPOINT_PATH}` | 存储库API的端点路径。 | `https://platform.adobe.io/data/core/xcore/` |
| `{PRODUCT_CONTEXT}` | 按容器与产品上下文的关联过滤容器列表。 | `acp` |
| `{PROPERTY}` | 筛选返回的容器类型。 | `_instance.containerType==decisioning` |

**请求**

```shell
curl -X GET \
  'https://platform.adobe.io/data/core/xcore/?product=acp&property=_instance.containerType==decisioning' \
  -H 'Authorization: Bearer {ACCESS_TOKEN}' \
  -H 'x-api-key: {API_KEY}' \
  -H 'x-gw-ims-org-id: {IMS_ORG}' \
  -H 'x-sandbox-name: {SANDBOX_NAME}'
```

**响应**

成功的响应会返回有关决策管理容器的信息。 这包括 `instanceId` 属性，其值是您的容器ID。

```json
{
    "_embedded": {
        "https://ns.adobe.com/experience/xcore/container": [
            {
                "instanceId": "{INSTANCE_ID}",
                "schemas": [
                    "https://ns.adobe.com/experience/xcore/container;version=0.5"
                ],
                "productContexts": [
                    "acp"
                ],
                "repo:etag": 2,
                "repo:createdDate": "2020-09-16T07:54:28.319959Z",
                "repo:lastModifiedDate": "2020-09-16T07:54:32.098139Z",
                "repo:createdBy": "{CREATED_BY}",
                "repo:lastModifiedBy": "{MODIFIED_BY}",
                "repo:createdByClientId": "{CREATED_CLIENT_ID}",
                "repo:lastModifiedByClientId": "{MODIFIED_CLIENT_ID}",
                "_instance": {
                    "containerType": "decisioning",
                    "repo:name": "{REPO_NAME}",
                    "dataCenter": "{DATA_CENTER}",
                    "parentName": "{PARENT_NAME}",
                    "parentId": "{PARENT_ID}"
                },
                "_links": {
                    "self": {
                        "href": "/containers/{INSTANCE_ID}"
                    }
                }
            }
        ]
    },
    "_links": {
        "self": {
            "href": "/?product=acp&property=_instance.containerType==decisioning",
            "@type": "https://ns.adobe.com/experience/xcore/hal/home"
        }
    }
}
```

## 后续步骤 {#next-steps}

本文档介绍了调用 [!DNL Offer Library] API，包括获取容器ID。 您现在可以继续本开发人员指南中提供的示例调用，并按照其说明进行操作。
<!--
>[!NOTE]
>
> The In-app messaging channel in Adobe Journey Optimizer uses decision management objects. If your organization uses the in-app messaging channel, then API list requests for objects will include objects created by the in-app messaging service and can be ignored for decision management use cases. Objects created for in-app messages will have `createdBy = “Mobile_Sheliak”`.
-->

## 操作方法视频 {#video}

以下视频旨在支持您了解决策管理的各个组件。

>[!VIDEO](https://video.tv.adobe.com/v/329919?quality=12)

