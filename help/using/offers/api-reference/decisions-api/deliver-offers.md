---
title: 提供优惠
description: 决策管理是服务和UI项目的集合，使营销人员能够使用业务逻辑和决策规则跨渠道和应用程序创建和提供最终用户个性化的优惠体验。
translation-type: tm+mt
source-git-commit: b527186d0722492f5f509f1ae0a5315b9a9f771e
workflow-type: tm+mt
source-wordcount: '947'
ht-degree: 3%

---

# 使用决策API提供优惠

通过决策管理，您可以使用业务逻辑和决策规则跨渠道和应用程序创建和提供最终用户个性化优惠体验。 优惠是营销消息，其中可能包含与其关联的规则，用于指定谁有资格查看优惠。

您可以通过向[!DNL Decisions] API发出POST请求来创建和传送优惠。

本教程要求对API（尤其是与决策管理相关的API）有有效的了解。 有关详细信息，请参阅[Decision Management API开发人员指南](../getting-started.md)。 本教程还要求您有唯一的位置ID和决策ID值可用。 如果尚未获取这些值，请参阅有关[创建位置](../offers-api/placements/create.md)和[创建决策](../activities-api/activities/create.md)的教程。

![](../../../assets/do-not-localize/how-to-video.png) [在视频中发现此功能](#video)

## 接受和内容类型标题

下表显示了在请求标头中包含&#x200B;*Content-Type*&#x200B;和&#x200B;*Accept*&#x200B;字段的有效值：

| 标题名称 | 值 |
| ----------- | ----- |
| Accept | `application/vnd.adobe.xdm+json; schema="https://ns.adobe.com/experience/offer-management/decision-response;version=1.0"` |
| Content-Type | `application/vnd.adobe.xdm+json; schema="https://ns.adobe.com/experience/offer-management/decision-request;version=1.0"` |

**API格式**

```https
POST /{ENDPOINT_PATH}/{CONTAINER_ID}/decisions
```

| 参数 | 描述 | 示例 |
| --------- | ----------- | ------- |
| `{ENDPOINT_PATH}` | 存储库API的终结点路径。 | `https://platform.adobe.io/data/core/ode/` |
| `{CONTAINER_ID}` | 决策所在的容器。 | `e0bd8463-0913-4ca1-bd84-6309134ca1f6` |

**请求**

```shell
curl -X POST \
  'https://platform.adobe.io/data/core/ode/e0bd8463-0913-4ca1-bd84-6309134ca1f6/decisions' \
  -H 'Accept: application/vnd.adobe.xdm+json; schema="https://ns.adobe.com/experience/offer-management/decision-response;version=1.0"' \
  -H 'Content-Type: application/vnd.adobe.xdm+json; schema="https://ns.adobe.com/experience/offer-management/decision-request;version=1.0'
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
            "xdm:decisionRequestId": "0AA00002-0000-1337-c0de-c0fefec0fefe"
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
| `xdm:propositionRequests` | 此对象包含放置和决策标识符。 |
| `xdm:propositionRequests.xdm:placementId` | 唯一位置标识符。 | `"xdm:placementId": "xcore:offer-placement:ffed0456"` |
| `xdm:propositionRequests.xdm:activityId` | 唯一决策标识符。 | `"xdm:activityId": "xcore:offer-activity:ffed0123"` |
| `xdm:itemCount` | 要返回的优惠数。 最大数为30。 | `"xdm:itemCount": 2` |
| `xdm:profiles` | 此对象保存有关请求决定的用户档案的信息。 对于API请求，此将包含一个用户档案。 |
| `xdm:profiles.xdm:identityMap` | 此对象基于标识的命名空间集成代码保存一组最终用户标识。 该身份映射可承载每个命名空间的多个身份。 有关命名空间的详细信息，请参阅[身份命名空间概述](https://docs.adobe.com/content/help/zh-Hans/experience-platform/identity/namespaces.html)。 | `Email: [{"xdm:id": "123@abc.com"}]` |
| `xdm:profiles.xdm:decisionRequestId` | 由客户端生成的ID，可用于唯一标识用户档案决策请求。 该ID在答复中得到回应，不影响决定结果。 | `"xdm:decisionRequestId": "0AA00002-0000-1337-c0de-c0fefec0fefe"` |
| `xdm:allowDuplicatePropositions` | 此对象是重复数据消除规则的控制结构。 它由一系列标志组成，这些标志指示是否可以在某个维度上建议同一选项。 设置为true的标志表示允许重复，不应在标志指示的类别上删除。 设置为false的标志表示决策引擎不应在维度上做出相同的命题，而应为某个子决策选择下一个最佳选项。 |
| `xdm:allowDuplicatePropositions.xdm:acrossActivities` | 如果设置为true，则可能会为多个决策分配相同的选项。 | `"xdm:acrossActivities": true` |
| `xdm:allowDuplicatePropositions.xdm:acrossPlacements` | 如果设置为true，则可能会为多个版面分配相同的选项。 | `"xdm:acrossPlacements": true` |
| `xdm:mergePolicy.xdm:id` | 标识用于管理用户档案访问服务返回的数据的合并策略。 如果未在请求中指定，则Decision Management不会传递任何用户档案访问服务，否则将传递调用方提供的id。 | `"xdm:id": "5f3ed32f-eaf1-456c-b0f0-7b338c4cb18a"` |
| `xdm:responseFormat` | 设置响应内容格式的一组标志。 |
| `xdm:responseFormat.xdm:includeContent` | 一个布尔值，如果设置为`true`，则包含响应的内容。 | `"xdm:includeContent": true` |
| `xdm:responseFormat.xdm:includeMetadata` | 用于指定返回哪些附加元数据的对象。 如果未包含此属性，则默认情况下将返回`xdm:id`和`repo:etag`。 | `name` |
| `xdm:responseFormat.xdm:activity` | 此标志标识为`xdm:activity`返回的特定元数据信息。 | `name` |
| `xdm:responseFormat.xdm:option` | 此标志标识为`xdm:option`返回的特定元数据信息。 | `name`、`characteristics` |
| `xdm:responseFormat.xdm:placement` | 此标志标识为`xdm:placement`返回的特定元数据信息。 | `name`、`channel`、`componentType` |

**响应**

成功的响应会返回您的主张的相关信息，包括其唯一`xdm:propositionId`。

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
| `xdm:propositionId` | 与XDM DecisionEvent关联的命题实体的唯一标识符。 | `"xdm:propositionId": "5d0ffb5e-dfc6-4280-99b6-0bf3131cb8b8"` |
| `xdm:propositions` | 此对象包含单个决策主张。 可以返回多个选项供决策使用。 如果未找到任何选项，则返回决定的回退优惠。 单个决策命题始终包括`options`属性或`fallback`属性。 如果存在，`options`属性不能为空。 |
| `xdm:propositions.xdm:activity` | 此对象包含决策的唯一标识符。 | `"xdm:id": "xcore:activity:ffed0123"` |
| `xdm:propositions.xdm:placement` | 此对象包含优惠放置的唯一标识符。 | `"xdm:id": "xcore:placement:ffed0456"` |
| `xdm:propositions.xdm:options` | 此对象包含单个选项，包括其唯一标识符。 如果存在，则此对象不能为空。 | `xdm:id": "xcore:personalized-option:ccc0111` |
| `xdm:propositions.xdm:options.@type` | 定义组件的类型。 `@type` 作为客户端的处理合同。组合体验后，书写器将查找具有特定类型的组件。 | `https://ns.adobe.com/experience/offer-management/content-component-imagelink` |
| `xdm:propositions.xdm:content` | 响应内容的格式。 | 响应内容可以是：`text`、`html block`或`image link` |
| `xdm:score` | 作为与选项或决策相关联的排名函数的结果计算的选项的分数。 如果在排名过程中涉及排名函数来确定优惠的得分，则API将返回此字段。 | `"xdm:score": 45.65` |
| `xdm:propositions.xdm:fallback` | 此对象包含单个回退优惠，包括其唯一标识符。 | `"xdm:id": "xcore:fallback:ccc0222"` |
| `xdm:propositions.xdm:fallback.dc:format` | 资源的物理或数字表现。 通常，格式应包括资源的媒体类型。 该格式可用于确定显示或操作资源所需的软件、硬件或其他设备。 建议从受控词汇中选择一个值，例如，定义计算机媒体格式的[Internet媒体类型](http://www.iana.org/assignments/media-types/)的列表。 | `"dc:format": "image/png"` 或 `"image/jpeg"` |
| `xdm:propositions.xdm:fallback.xdm:deliveryURL` | 用于从内容投放网络或服务端点读取资产的可选URL。 此URL用于从用户代理公开访问资产。 | `https://d37yhxrr0p3l3l.cloudfront.net/0fd0f090-a148-11ea-89e3-f1f2ad52f7e8/urn:aaid:sc:US:a68c86a6-9295-4940-a083-11916b665500/0/40d78a12-f8b6-3f07-8e67-7cb8ae2cc7ec` |
| `ode:createDate` | 创建决策响应消息的时间。 这表示为纪元时间。 | `"ode:createDate": 1566497582038` |

## 教程视频{#video}

以下视频旨在帮助您了解决策管理的各个组件。

>[!NOTE]
>
>此视频适用于在Adobe Experience Platform上构建的Offer Decisioning应用程序服务。 但是，它提供了在Journey Optimizer环境中使用优惠的通用指导。

>[!VIDEO](https://video.tv.adobe.com/v/329919/?quality=12)

## 后续步骤

按照本API指南，您已使用[!DNL Decisions] API创建并交付优惠。 有关详细信息，请参阅有关Decision Management](../../../offers/get-started/starting-offer-decisioning.md)的[概述。
