---
title: 提供优惠
description: 决策管理是服务和UI程序的集合，通过该集合，营销人员可使用业务逻辑和决策规则跨渠道和应用程序创建并提供最终用户个性化优惠体验。
feature: Decision Management, API
topic: Integrations
role: Data Engineer
level: Experienced
exl-id: 692d0aae-6fa1-40b8-a35f-9845d78317a3
source-git-commit: ae0bd349b6287002f264ed716b6454fb9d8357c9
workflow-type: tm+mt
source-wordcount: '1018'
ht-degree: 3%

---

# 使用Decisioning API提供优惠 {#decisioning-api}

借助决策管理，您可以使用业务逻辑和决策规则跨渠道和应用程序创建并提供最终用户个性化优惠体验。 优惠是营销消息，其中可能包含与其关联的规则，用于指定有资格查看优惠的人员。

您可以通过向以下网站发出POST请求来创建和提供优惠： [!DNL Decisioning] API。

本教程需要对各种API有一定的了解，尤其是有关决策管理的知识。 欲了解更多信息，请参见 [Decision Management API开发人员指南](../getting-started.md). 此外，本教程还要求您提供唯一的版面ID和决策ID值。 如果您尚未获得这些值，请参阅以下教程 [创建投放位置](../offers-api/placements/create.md) 和 [创建决策](../activities-api/activities/create.md).

➡️  [在视频中发现此功能](#video)

## 必需的标头 {#required-headers}

下表显示了包含 *Content-Type* 和 *Accept* 请求标头中的字段：

| 标题名称 | 值 |
| ----------- | ----- |
| 接受 | `application/vnd.adobe.xdm+json; schema="https://ns.adobe.com/experience/offer-management/decision-response;version=1.0"` |
| Content-Type | `application/vnd.adobe.xdm+json; schema="https://ns.adobe.com/experience/offer-management/decision-request;version=1.0"` |
| Authorization | `Bearer {ACCESS_TOKEN}` |
| x-gw-ims-org-id | `{IMS_ORG}` |
| x-sandbox-name | `{SANDBOX_NAME}` |
| x-api-key | `{API_KEY}` |

* 包含有效负载(POST、PUT、PATCH)的所有请求都需要使用content-type标头

## API请求 {#request}

### API格式

```https
POST /{ENDPOINT_PATH}/decisions
```

| 参数 | 描述 | 示例 |
| --------- | ----------- | ------- |
| `{ENDPOINT_PATH}` | 存储库API的端点路径。 | `https://platform.adobe.io/data/core/ods` |

### 请求

```shell
curl -X POST \
  'https://platform.adobe.io/data/core/ods/decisions' \
  -H 'Accept: application/vnd.adobe.xdm+json; schema="https://ns.adobe.com/experience/offer-management/decision-response;version=1.0"' \
  -H 'Content-Type: application/vnd.adobe.xdm+json; schema="https://ns.adobe.com/experience/offer-management/decision-request;version=1.0"'
  -H 'Authorization: Bearer {ACCESS_TOKEN}' \
  -H 'x-api-key: {API_KEY}' \
  -H 'x-gw-ims-org-id: {IMS_ORG}' \
  -H 'x-sandbox-name: {SANDBOX_NAME}'
  -d '{
        "xdm:propositionRequests": [
            {
              "xdm:placementId": "xcore:offer-placement:ffed0456",
              "xdm:activityId": "xcore:offer-activity:ffed0123",
              "xdm:itemCount": 2
            },
            {
              "xdm:placementId": "xcore:offer-placement:ffed0012",
              "xdm:activityId": "xcore:offer-activity:fffc0789"
            }
        ],
        "xdm:profiles": [
            {
              "xdm:identityMap": {
                "SWCUSTID": [
                {
                    "xdm:id": "123@abc.com"
                }
                ]
            },
            "xdm:decisionRequestId": "0AA00002-0000-1224-c0de-cjf98Csj43"
            }
        ],
        "xdm:allowDuplicatePropositions": {
            "xdm:acrossActivities": true,
            "xdm:acrossPlacements": true
        },
        "xdm:mergePolicy": {
            "xdm:id": "5f3ed32f-eaf1-456c-b0f0-7b338c4cb18a"
        },
        "xdm:responseFormat": {
            "xdm:includeContent": true,
            "xdm:includeMetadata": {
            "xdm:activity": [
                "name"
            ],
            "xdm:option": [
                "name"
            ],
            "xdm:placement": [
                "name"
            ]
            }
        }
      }'
```

| 属性 | 描述 | 示例 |
| -------- | ----------- | ------- |
| `xdm:propositionRequests` | 此对象包含投放位置和决策标识符。 |
| `xdm:propositionRequests.xdm:placementId` | 唯一投放位置标识符。 | `"xdm:placementId": "xcore:offer-placement:ffed0456"` |
| `xdm:propositionRequests.xdm:activityId` | 唯一决策标识符。 | `"xdm:activityId": "xcore:offer-activity:ffed0123"` |
| `xdm:itemCount` | 要返回的优惠数量。 最大数量为30。 | `"xdm:itemCount": 2` |
| `xdm:profiles` | 此对象保存有关为其请求决策的用户档案的信息。 对于API请求，这将包含一个配置文件。 |
| `xdm:profiles.xdm:identityMap` | 此对象根据标识的命名空间集成代码保留一组最终用户标识。 身份映射可以携带每个命名空间的多个身份。 有关命名空间的更多信息，请参阅[此页面](../../../audience/get-started-identity.md)。 | `Email: [{"xdm:id": "123@abc.com"}]` |
| `xdm:profiles.xdm:decisionRequestId` | 客户端生成的ID，可用于唯一标识配置文件决策请求。 此ID会在响应中响应，并且不会影响决策的结果。 | `"xdm:decisionRequestId": "0AA00002-0000-1224-c0de-cjf98Csj43"` |
| `xdm:allowDuplicatePropositions` | 此对象是重复数据消除规则的控制结构。 它包含一系列标志，指示在特定维度中是否可以建议相同的选项。 设置为true的标记表示允许存在重复项，不应在该标记所指示的类别中移除重复项。 被设置为false的标志意味着决策引擎不应在整个维度中提出相同的建议，而是应为其中一个子决策选择下一个最佳选项。 |
| `xdm:allowDuplicatePropositions.xdm:acrossActivities` | 如果设置为true，则可能会为多个决策分配相同的选项。 | `"xdm:acrossActivities": true` |
| `xdm:allowDuplicatePropositions.xdm:acrossPlacements` | 如果设置为true，则可能会为多个投放位置分配相同的选项。 | `"xdm:acrossPlacements": true` |
| `xdm:mergePolicy.xdm:id` | 标识用于管理配置文件访问服务返回的数据的合并策略。 如果未在请求中指定任何配置文件访问服务，决策管理将不会传递任何配置文件访问服务，否则将传递调用方提供的ID。 | `"xdm:id": "5f3ed32f-eaf1-456c-b0f0-7b338c4cb18a"` |
| `xdm:responseFormat` | 一组用于设置响应内容格式的标记。 |
| `xdm:responseFormat.xdm:includeContent` | 一个布尔值，如果设置为 `true`，包括响应内容。 | `"xdm:includeContent": true` |
| `xdm:responseFormat.xdm:includeMetadata` | 用于指定返回哪些其他元数据的对象。 如果未包含此属性，则 `xdm:id` 和 `repo:etag` 默认返回。 | `name` |
| `xdm:responseFormat.xdm:activity` | 此标记标识针对以下对象返回的特定元数据信息 `xdm:activity`. | `name` |
| `xdm:responseFormat.xdm:option` | 此标记标识针对以下对象返回的特定元数据信息 `xdm:option`. | `name`、`characteristics` |
| `xdm:responseFormat.xdm:placement` | 此标记标识针对以下对象返回的特定元数据信息 `xdm:placement`. | `name`、`channel`、`componentType` |

### 响应

成功的响应将返回有关您的建议的信息，包括其独特的 `xdm:propositionId`.

```json
{
  "xdm:propositionId": "5d0ffb5e-dfc6-4280-99b6-0bf3131cb8b8",
  "xdm:propositions": [
    {
      "xdm:activity": {
        "xdm:id": "xcore:activity:ffed0123",
        "repo:etag": 4
      },
      "xdm:placement": {
        "xdm:id": "xcore:placement:ffed0456",
        "repo:etag": 1
      },
      "xdm:options": [
        {
          "xdm:id": "xcore:personalized-option:ccc0111",
          "repo:etag": 3,
          "@type": "https://ns.adobe.com/experience/decisioning/content-component-html-template",
          "xdm:content": "<html>some html</html>"
        },
        {
          "xdm:id": "xcore:personalized-option:ccc0222",
          "repo:etag": 5,
          "@type": "https://ns.adobe.com/experience/decisioning/content-component-html-template",
          "xdm:content": "<html>hello, world</html>",
          "xdm:score": 45.65
        }
      ]
    },
    {
      "xdm:activity": {
        "xdm:id": "xcore:activity:ffed0123",
        "repo:etag": 4
      },
      "xdm:placement": {
        "xdm:id": "xcore:placement:ffed0789",
        "repo:etag": 2
      },
      "xdm:fallback": {
        "xdm:id": "xcore:fallback:ccc0222",
        "repo:etag": 5,
        "@type": "https://ns.adobe.com/experience/decisioning/content-component-imagelink",
        "dc:format": "image/png",
        "xdm:deliveryURL": "https://cdn.adobe.com/content/1445323-1134331.png",
        "xdm:content": "https://www.adobe.com/index2.html"
      }
    }
  ],
  "ode:createDate": 1566497582038
}
```

| 属性 | 描述 | 示例 |
| -------- | ----------- | ------- |
| `xdm:propositionId` | 与XDM DecisionEvent关联的优惠实体的唯一标识符。 | `"xdm:propositionId": "5d0ffb5e-dfc6-4280-99b6-0bf3131cb8b8"` |
| `xdm:propositions` | 此对象包含单个决策建议。 可以为决策返回多个选项。 如果未找到任何选项，则会返回该决策的备用选件。 单个决策建议始终包括 `options` 属性或 `fallback` 属性。 如果存在，则 `options` 属性不能为空。 |
| `xdm:propositions.xdm:activity` | 此对象包含决策的唯一标识符。 | `"xdm:id": "xcore:activity:ffed0123"` |
| `xdm:propositions.xdm:placement` | 此对象包含优惠投放位置的唯一标识符。 | `"xdm:id": "xcore:placement:ffed0456"` |
| `xdm:propositions.xdm:options` | 此对象包含单个选项，其中包括其唯一标识符。 如果存在，则此对象不能为空。 | `xdm:id": "xcore:personalized-option:ccc0111` |
| `xdm:propositions.xdm:options.@type` | 定义组件的类型。 `@type` 充当客户的处理合同。 组装体验时，编辑器将查找具有特定类型的元件。 | `https://ns.adobe.com/experience/offer-management/content-component-imagelink` |
| `xdm:propositions.xdm:content` | 响应内容的格式。 | 响应内容可以是： `text`， `html block`，或 `image link` |
| `xdm:score` | 作为与选项或决策关联的排名函数的结果而计算的选项分数。 如果排名过程中涉及排名函数来确定优惠的分数，则API将返回此字段。 | `"xdm:score": 45.65` |
| `xdm:propositions.xdm:fallback` | 此对象包含单个备用选件，包括其唯一标识符。 | `"xdm:id": "xcore:fallback:ccc0222"` |
| `xdm:propositions.xdm:fallback.dc:format` | 资源的物理或数字表现形式。 通常，格式应包含资源的媒体类型。 该格式可用于确定显示或操作该资源所需的软件、硬件或其他设备。 建议从受控词汇表中选择一个值，例如 [Internet媒体类型](https://www.iana.org/assignments/media-types/) 定义计算机媒体格式。 | `"dc:format": "image/png"` 或 `"image/jpeg"` |
| `xdm:propositions.xdm:fallback.xdm:deliveryURL` | 用于从内容交付网络或服务端点读取资源的可选URL。 此URL用于从用户代理公开访问资产。 | `https://d37yhxrr0p3l3l.cloudfront.net/0fd0f090-a148-11ea-89e3-f1f2ad52f7e8/urn:aaid:sc:US:a68c86a6-9295-4940-a083-11916b665500/0/40d78a12-f8b6-3f07-8e67-7cb8ae2cc7ec` |
| `ode:createDate` | 创建决策响应消息的时间。 以纪元时间表示。 | `"ode:createDate": 1566497582038` |

**响应代码**

下表列出了可在响应中返回的所有代码：

| 代码 | 描述 |
|  ---  |  ---  |
| 200 | 成功。 已针对特定活动做出决策 |
| 400 | 请求参数无效。 由于语法错误，服务器无法理解该请求。 |
| 403 | 权限被禁止，不足。 |
| 422 | 无法处理的实体。 请求语法正确，但由于语义错误而无法处理。 |
| 429 | 请求过多。 用户在给定时间段内发送的请求过多。 |
| 500 | 内部服务器错误。 服务器遇到意外情况，无法完成请求。 |
| 503 | 由于服务器过载，服务不可用。 由于临时过载，服务器当前无法处理该请求。 |

<!-- ## Tutorial video {#video}

The following video is intended to support your understanding of the components of Decision Management.

>[!NOTE]
>
>This video applies to the Offer Decisioning application service built on Adobe Experience Platform. However, it provides generic guidance to use Offer in the context of Journey Optimizer.

>[!VIDEO](https://video.tv.adobe.com/v/329919/?quality=12) -->

## 后续步骤 {#next-steps}

通过遵循本API指南，您已使用创建并交付选件 [!DNL Decisions] API。 欲了解更多信息，请参见 [决策管理概述](../../../offers/get-started/starting-offer-decisioning.md).
