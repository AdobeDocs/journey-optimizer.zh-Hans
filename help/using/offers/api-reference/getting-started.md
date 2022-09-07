---
title: 快速入门
description: 了解如何开始使用优惠库API来使用决策引擎执行关键操作。
feature: Offers
topic: Integrations
role: User
level: Intermediate
exl-id: 773bee50-849f-4b07-9423-67de5279ad28
source-git-commit: c530905eacbdf6161f6449d7a0b39c8afaf3a321
workflow-type: tm+mt
source-wordcount: '638'
ht-degree: 5%

---

# 决策管理API开发人员指南 {#decision-management-api-developer-guide}

本开发人员指南提供了帮助您开始使用 [!DNL Offer Library] API。 然后，该指南提供了用于使用决策引擎执行关键操作的示例API调用。

➡️ [在此视频中了解有关决策管理组件的更多信息](#video)

## 先决条件 {#prerequisites}

本指南要求您对Adobe Experience Platform的以下组件有一定的了解：

* [[!DNL Experience Data Model (XDM) System]](https://experienceleague.adobe.com/docs/experience-platform/xdm/home.html?lang=zh-Hans){target=&quot;_blank&quot;}:标准化框架， [!DNL Experience Platform] 组织客户体验数据。
   * [架构组合的基础知识](https://experienceleague.adobe.com/docs/experience-platform/xdm/schema/composition.html?lang=zh-Hans){target=&quot;_blank&quot;}:了解XDM模式的基本构建块。
* [决策管理](../../../using/offers/get-started/starting-offer-decisioning.md):解释Experience Decisioning的一般概念和组件，特别是决策管理。 说明了在客户体验期间选择要显示的最佳选项时所使用的策略。
* [[!DNL Profile Query Language (PQL)]](https://experienceleague.adobe.com/docs/experience-platform/segmentation/pql/overview.html){target=&quot;_blank&quot;}:PQL是一种用于通过XDM实例编写表达式的强大语言。 PQL用于定义决策规则。

## 读取示例API调用 {#reading-sample-api-calls}

本指南提供了示例API调用，以演示如何设置请求的格式。 这包括路径、所需标头以及格式正确的请求负载。 还提供了API响应中返回的示例JSON。 有关示例API调用文档中使用的约定的信息，请参阅 [如何阅读示例API调用](https://experienceleague.adobe.com/docs/experience-platform/landing/troubleshooting.html#how-do-i-format-an-api-request){target=&quot;_blank&quot;}(位于 [!DNL Experience Platform] 疑难解答指南。

## 收集所需标题的值 {#gather-values-for-required-headers}

为了调用 [!DNL Adobe Experience Platform] API，您必须先完成 [身份验证教程](https://experienceleague.adobe.com/docs/experience-platform/landing/platform-apis/api-authentication.html){target=&quot;_blank&quot;}。 完成身份验证教程将为所有中每个所需标头提供值 [!DNL Experience Platform] API调用，如下所示：

* `Authorization: Bearer {ACCESS_TOKEN}`
* `x-api-key: {API_KEY}`
* `x-gw-ims-org-id: {IMS_ORG}`

所有包含有效负载(POST、PUT、PATCH)的请求都需要额外的标头：

* `Content-Type: application/json`

## 管理对容器的访问 {#manage-access-to-container}

容器是一种隔离机制，可以分开不同的关注。 容器ID是所有存储库API的第一个路径元素。 所有决策对象都驻留在容器中。

管理员可以将类似的承担者、资源和访问权限分组到用户档案中。 这减轻了管理负担，并受 [Adobe Admin Console](https://adminconsole.adobe.com/). 您必须是组织中Adobe Experience Platform的产品管理员，才能创建用户档案并为其分配用户。 只需在一次性步骤中创建与特定权限匹配的产品配置文件，然后只需将用户添加到这些配置文件即可。 用户档案充当已获得权限的组，该组中的每个实际用户或技术用户都会继承这些权限。

您可以通过 [Adobe Admin Console](https://adminconsole.adobe.com/){target=&quot;_blank&quot;}。 有关更多信息，请参阅 [访问控制概述](https://experienceleague.adobe.com/docs/experience-platform/access-control/home.html?lang=zh-Hans){target=&quot;_blank&quot;}。

### 列出用户和集成可访问的容器 {#list-containers-accessible-to-users-and-integrations}

**API格式**

```http
GET /{ENDPOINT_PATH}?product={PRODUCT_CONTEXT}&property={PROPERTY}==decisioning
```

| 参数 | 描述 | 示例 |
| --------- | ----------- | ------- |
| `{ENDPOINT_PATH}` | 存储库API的端点路径。 | `https://platform.adobe.io/data/core/xcore/` |
| `{PRODUCT_CONTEXT}` | 按容器与产品上下文的关联过滤容器列表。 | `acp` |
| `{PROPERTY}` | 过滤返回的容器类型。 | `_instance.containerType==decisioning` |

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

成功的响应会返回有关决策管理容器的信息。 这包括 `instanceId` 属性，其值是容器ID。

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

本文档介绍了调用 [!DNL Offer Library] API，包括获取容器ID。 您现在可以继续阅读本开发人员指南中提供的示例调用并按照其说明进行操作。

>[!NOTE]
>
> Adobe Journey Optimizer中的应用程序内消息传送渠道使用决策管理对象。 如果贵组织使用应用程序内消息传送渠道，则对象的API列表请求将包含由应用程序内消息传送服务创建的对象，在决策管理用例中可以忽略这些对象。 为应用程序内消息创建的对象将具有 `createdBy = “Mobile_Sheliak”`.

## 操作方法视频 {#video}

以下视频旨在支持您对决策管理组件的了解。

>[!VIDEO](https://video.tv.adobe.com/v/329919?quality=12)

