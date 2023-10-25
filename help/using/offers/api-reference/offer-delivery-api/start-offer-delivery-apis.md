---
title: 优惠投放 API 入门
description: 了解可用于提供个性化优惠的API的更多信息。
feature: Decision Management, API
topic: Integrations
role: Data Engineer
level: Experienced
exl-id: 7bc1a4ec-113c-4af7-b549-ee17b843b818
source-git-commit: 91f52af0c2e42556c4456be9b6b0cb84378c2a23
workflow-type: tm+mt
source-wordcount: '631'
ht-degree: 5%

---

# 优惠投放 API 入门 {#about-decisioning-apis}

您可以使用以下任一方式交付优惠： **决策** 或 **边缘决策** API。 此外， **批量决策** API允许您在一次调用中将选件交付给给定受众中的所有配置文件。 受众中每个用户档案的选件内容都放在Adobe Experience Platform数据集中，可用于自定义批量工作流。

在此页面中，您可以找到随提供的有关特定功能的信息。 **决策** 和 **边缘决策** API。 虽然这两种方法都允许您向客户提供选件，但我们建议使用 **边缘决策** API适用于入站用例，并确保提高平台的延迟和吞吐量。

有关如何使用API的更多信息，请参阅以下章节：
* [Decisioning API](decisioning-api.md)
* [Edge Decisioning API](edge-decisioning-api.md)
* [Batch Decisioning API](batch-decisioning-api.md)

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

## Edge Decisioning API功能 {#edge}

**体验事件和决策请求的独特请求**

借助Edge Decisioning API，您可以将体验事件本身与决策请求一起发送到一个请求中，而不是发送两个不同的请求。

例如，如果客户访问您的网站，则请求将包括体验事件（客户对页面的访问），并获取选件以填充所访问的页面。

**将上下文数据存储到Adobe Experience Platform**

上下文数据是指您仅在需要恢复选件时知道的数据。 例如，所购买物品的颜色、购买时的天气等。

使用Edge Decisioning API请求传递上下文数据时，数据会存储在Adobe Experience Platform配置文件中，以便将来重复使用。

>[!NOTE]
>
>为了存储上下文数据，您需要配置专用的XDM架构。

## 决策API功能 {#decisioning}

以下列出的功能仅在Decisioning API中可用。 如果您需要利用其中一个应用程序来满足您的要求，请使用Decisioning API。 否则，我们建议使用Edge Decisioning API。

* **选件内容和特征**：您可以选择不使用专用选项返回选件的内容和特征。
* **优惠元数据**：启用一个选项以返回选件的元数据。
* **合并策略**：在请求中使用与沙盒关联的合并策略不同的合并策略。
* **决策事件和频率封顶**：阻止将决策事件计数为所发生的任何频率上限。
* **复制建议**：启用一个不删除重复建议的选项。
