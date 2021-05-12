---
title: 入门指南
description: 了解如何使用优惠库API开始，以使用决策管理引擎执行关键操作。
translation-type: tm+mt
source-git-commit: db7fd318b14d01a0369c934a3e01c6e368d7658d
workflow-type: tm+mt
source-wordcount: '608'
ht-degree: 7%

---

# 决策管理API开发人员指南

此开发人员指南提供了帮助您使用[!DNL Offer Library] API进行开始的步骤。 然后，该指南提供了使用决策管理引擎执行关键操作的示例API调用。

![](../../assets/do-not-localize/how-to-video.png) [在视频中发现此功能](#video)

## 先决条件

本指南要求对Adobe Experience Platform的以下组件有充分的了解：

* [[!DNL Experience Data Model (XDM) System]](https://docs.adobe.com/content/help/zh-Hans/experience-platform/xdm/home.html):组织客户体验数 [!DNL Experience Platform] 据的标准化框架。
   * [模式合成的基础](https://docs.adobe.com/content/help/zh-Hans/experience-platform/xdm/schema/composition.html):了解XDM模式的基本构建块。
* [决策管理](../../../using/offers/get-started/starting-offer-decisioning.md):概括介绍用于体验决策的概念和组件，特别是Offer decisioning。说明了在客户体验期间选择最佳展示选项时使用的策略。
* [[!DNL Profile Query Language (PQL)]](https://docs.adobe.com/content/help/en/experience-platform/segmentation/pql/overview.html):PQL是一种功能强大的语言，用于编写XDM实例的表达式。PQL用于定义决策规则。

## 读取示例API调用

本指南提供示例API调用，以演示如何设置请求的格式。 这包括路径、必需的标头和格式正确的请求负载。 还提供API响应中返回的示例JSON。 有关示例API调用文档中使用的约定的信息，请参阅[!DNL Experience Platform]疑难解答指南中关于如何读取示例API调用](https://docs.adobe.com/content/help/en/experience-platform/landing/troubleshooting.html#how-do-i-format-an-api-request)的部分。[

## 收集所需标题的值

要调用[!DNL Platform] API，您必须首先完成[身份验证教程](https://docs.adobe.com/content/help/en/experience-platform/tutorials/authentication.html)。 完成身份验证教程后，将为所有[!DNL Experience Platform] API调用中每个所需标头提供值，如下所示：

* `Authorization: Bearer {ACCESS_TOKEN}`
* `x-api-key: {API_KEY}`
* `x-gw-ims-org-id: {IMS_ORG}`

所有包含有效负荷(POST、PUT、PATCH)的请求都需要额外的标头：

* `Content-Type: application/json`

## 管理对容器的访问

容器是一种隔离机制，可以将不同的问题分开。 容器ID是所有存储库API的第一个路径元素。 所有决策对象都驻留在容器中。

管理员可以将类似的承担者、资源和访问权限分组到用户档案中。 这减轻了管理负担，并受[Adobe Admin Console](https://adminconsole.adobe.com/)支持。 您必须是组织中Adobe Experience Platform的产品管理员，才能创建用户档案并为其分配用户。 只需一次性创建与某些权限匹配的产品用户档案，然后只需将用户添加到这些用户档案即可。 用户档案充当被授予权限的组，该组中的每个实际用户或技术用户都继承了这些权限。

授予管理员权限后，您可以通过[Adobe Admin Console](https://adminconsole.adobe.com/)向用户授予或撤销权限。 有关详细信息，请参阅[访问控制概述](https://docs.adobe.com/content/help/zh-Hans/experience-platform/access-control/home.html)。

### 列表容器可供用户访问和集成

**API格式**

```http
GET /{ENDPOINT_PATH}?product={PRODUCT_CONTEXT}&property={PROPERTY}==decisioning
```

| 参数 | 描述 | 示例 |
| --------- | ----------- | ------- |
| `{ENDPOINT_PATH}` | 存储库API的终结点路径。 | `https://platform.adobe.io/data/core/xcore/` |
| `{PRODUCT_CONTEXT}` | 过滤器容器与产品上下文的关联。 | `acp` |
| `{PROPERTY}` | 过滤器返回的容器类型。 | `_instance.containerType==decisioning` |

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

成功的响应会返回有关决策管理容器的信息。 这包括`instanceId`属性，其值是您的容器ID。

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

## 后续步骤

此文档涵盖了对[!DNL Offer Library] API进行调用所需的必备知识，包括获取您的容器ID。 您现在可以继续查看本开发人员指南中提供的示例调用，并按照其说明进行操作。

## 教程视频{#video}

以下视频旨在帮助您了解决策管理的各个组件。

>[!NOTE]
>
>此视频适用于在Adobe Experience Platform上构建的Offer Decisioning应用程序服务。 但是，它提供了在Journey Optimizer环境中使用优惠的通用指导。

>[!VIDEO](https://video.tv.adobe.com/v/329919?quality=12)
