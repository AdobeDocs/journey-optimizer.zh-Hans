---
title: 使用Edge Decisioning API提供优惠
description: Adobe Experience Platform Web SDK允许您检索和渲染使用API或优惠库创建的个性化优惠。
feature: Offers
topic: Integrations
role: Data Engineer
level: Experienced
exl-id: 4e2dc0d6-4610-4a2f-8388-bc58182b227f
source-git-commit: 59499dec7d15dd4565c7910d7b454d82243ff011
workflow-type: tm+mt
source-wordcount: '993'
ht-degree: 4%

---

# 使用Edge Decisioning API提供优惠 {#edge-decisioning-api}

## 入门指南和先决条件 {#edge-overview-and-prerequisites}

此 [Adobe Experience Platform Web SDK](https://experienceleague.adobe.com/docs/experience-platform/edge/home.html#video-overview) 是一个客户端JavaScript库，它允许Adobe Experience Cloud客户通过Experience Platform边缘网络与Experience Cloud中的各种服务进行交互。

Experience PlatformWeb SDK支持在Adobe查询个性化解决方案，包括决策管理，从而允许您检索和渲染使用API或优惠库创建的个性化优惠。 有关更多详细说明，请参阅以下文档： [创建优惠](../../get-started/starting-offer-decisioning.md).

有两种方法可以通过实施决策管理 [平台Web SDK](https://experienceleague.adobe.com/docs/experience-platform/edge/home.html#video-overview). 一种方法是面向开发人员的，需要了解网站和编程。 另一种方法是使用Adobe Experience Platform用户界面设置选件，该选件只需要在HTML页面的标头中引用一个小型脚本。

请参阅以下文档： [决策管理](https://experienceleague.adobe.com/docs/experience-platform/edge/personalization/offer-decisioning/offer-decisioning-overview.html#enabling-offer-decisioning) 有关如何使用Adobe Experience Platform Web SDK提供个性化优惠的更多信息。

>[!NOTE]
>
>Adobe Experience Platform Web SDK中的决策管理仅适用于一组组织（限量发布）。 如果要利用此功能，请与您的Adobe客户经理联系。

## Adobe Experience Platform Web SDK {#aep-web-sdk}

Platform Web SDK取代了以下SDK：

* Visitor.js
* AppMeasurement.js
* AT.js
* DIL.js

SDK未组合这些库，并且是从头开始的新实施。 要使用它，您必须首先执行以下步骤：

1. 确保贵组织具有使用SDK的相应权限，并且您已正确配置这些权限。

   <!-- For more detailed instructions, refer to the documentation on using the [Adobe Experience Platform Web SDK](). -->

1. [配置数据流](https://experienceleague.adobe.com/docs/experience-platform/edge/fundamentals/datastreams.html) 在Adobe Experience Cloud帐户的“数据收集”选项卡中。

1. 安装SDK。 执行此操作的方法有多种，请参见 [安装SDK页面](https://experienceleague.adobe.com/docs/experience-platform/edge/fundamentals/installing-the-sdk.html?lang=zh-Hans). 本页将继续介绍每种不同的实施方法。

要使用SDK，您必须拥有 [架构](../../../data/get-started-schemas.md) 和 [数据流](../../../data/get-started-datasets.md) 已定义。

<!-- ****TODO - Configure schema**** -->

要个性化优惠，您必须单独配置个性化/用户档案。

<!-- Refer to the [doc](www.link.com) for detailed instructions.  -->

要配置SDK以进行决策管理，请执行以下两个步骤之一：

## 选项1 — 使用Launch安装标记扩展和实施

此选项对于编码体验可能较少的用户更友好。

1. [创建标记属性](https://experienceleague.adobe.com/docs/experience-platform/tags/admin/companies-and-properties.html)

1. [添加嵌入代码](https://experienceleague.adobe.com/docs/core-services-learn/implementing-in-websites-with-launch/configure-launch/launch-add-embed.html)

1. 通过从“数据流”下拉列表中选择配置，使用您创建的数据流安装和配置Adobe Experience Platform Web SDK扩展。 请参阅相关文档 [扩展](https://experienceleague.adobe.com/docs/experience-platform/tags/ui/extensions/overview.html).

   ![Adobe Experience Platform Web SDK](../../assets/installed-catalog-web-sdk.png)

   ![配置扩展](../../assets/configure-sdk-extension.png)

1. 创建必要的 [数据元素](https://experienceleague.adobe.com/docs/experience-platform/tags/ui/data-elements.html?lang=zh-Hans). 您至少必须创建一个Platform Web SDK标识映射和一个Platform Web SDK XDM对象数据元素。

   ![标识映射](../../assets/sdk-identity-map.png)

   ![XDM 对象](../../assets/xdm-object.png)

1. 创建您的 [规则](https://experienceleague.adobe.com/docs/experience-platform/tags/ui/rules.html)：

   添加Platform Web SDK发送事件操作，并将相关的decisionScopes添加到该操作的配置中

   ![渲染选件](../../assets/rule-render-offer.png)

   ![请求优惠](../../assets/rule-request-offer.png)

1. [创建并发布](https://experienceleague.adobe.com/docs/experience-platform/tags/publish/libraries.html) 一个库，其中包含您配置的所有相关规则、数据元素和扩展。

## 选项2 — 使用预建的独立版本手动实施

以下是使用Web SDK预建独立安装来使用决策管理所需的步骤。 本指南假定这是您首次实施SDK，因此所有步骤可能不适用于您。 本指南还假定您有一些开发经验。

包括选项2中的以下JavaScript代码片段：上的预建独立版本 [此页面](https://experienceleague.adobe.com/docs/experience-platform/edge/fundamentals/installing-the-sdk.html?lang=zh-Hans) 在 `<head>` HTML部分。

```
javascript
    <script>
        !function(n,o){o.forEach(function(o){n[o]||((n.__alloyNS=n.__alloyNS||
        []).push(o),n[o]=function(){var u=arguments;return new Promise(
        function(i,l){n[o].q.push([i,l,u])})},n[o].q=[])})}
        (window,["alloy"]);
    </script>
    <script src="https://cdn1.adoberesources.net/alloy/2.6.4/alloy.js" async></script>
```

您需要在Adobe帐户中拥有两个ID才能设置SDK配置 — 您的edgeConfigId和您的orgId。 edgeConfigId与您的数据流ID相同，您应在先决条件中配置此数据流ID。

要查找edgeConfigID/数据流ID，请转到数据收集并选择您的数据流。 要查找您的orgId，请转到您的个人资料。

按照此页面上的说明，在JavaScript中配置SDK。 在配置函数中，您将始终使用edgeConfigId和orgId。 此文档还介绍了您的配置中存在的可选参数。 最终配置可能如下所示：

```
javascript
    alloy("configure", {
        "edgeConfigId": "12345678-0ABC-DEF-GHIJ-KLMNOPQRSTUV",                            
        "orgId":"ABCDEFGHIJKLMNOPQRSTUVW@AdobeOrg",
        "debugEnabled": true,
        "edgeDomain": "edge.adobedc.net",
        "clickCollectionEnabled": true,
        "idMigrationEnabled": true,
        "thirdPartyCookiesEnabled": true,
        "defaultConsent":"in"  
    });
```

安装调试器Chrome扩展以用于调试。 可在此处找到： <https://chrome.google.com/webstore/detail/adobe-experience-platform/bfnnokhpnncpkdmbokanobigaccjkpob>

接下来，在Debugger中登录到您的帐户。 然后，转到日志并确保已连接到正确的工作区。 现在，从优惠中复制决策范围的base64编码版本。

编辑网站时，请包含脚本以及配置和 `sendEvent` 用于将决策范围发送到Adobe的函数。

**示例**:

```
javascript
    alloy("sendEvent", {
        "decisionScopes": 
        [
        "eyJ4ZG06YWN0aXZpdHlJZCI6Inhjb3JlOm9mZmVyLWFjdGl2aXR5OjE0ZWE4MDhhZjJjZDM1NzQiLCJ4ZG06cGxhY2VtZW50SWQiOiJ4Y29yZTpvZmZlci1wbGFjZW1lbnQ6MTRjNGFmZDI2OTXXXXXXXXXX"
        ]
    });
```

有关如何处理响应的示例，请参阅以下内容：

```
javascript
    alloy("sendEvent", {
        "decisionScopes":
        [
        "eyJ4ZG06YWN0aXZpdHlJZCI6Inhjb3JlOm9mZmVyLWFjdGl2aXR5OjE0ZWE4MDhhZjJjZDM1NzQiLCJ4ZG06cGxhY2VtZW50SWQiOiJ4Y29yZTpvZmZlci1wbGFjZW1lbnQ6MTRjNGFmZDI2OTXXXXXXXXXX"
        ]
    }).then(function(result) {
        Object.entries(result).forEach(([key, value]) => {
            console.log(key, value);
        });
    });
```

您可以使用调试器验证是否已成功连接到Edge网络。

>[!NOTE]
>
>如果您在日志中未看到与边缘的连接，则可能需要禁用广告拦截器。

请参阅如何创建选件和使用的格式。 根据决策中符合的标准，系统会向您返回一个选件，其中包含您在Adobe Experience Platform中创建该选件时指定的信息。

在此示例中，要返回的JSON是：

```
json
{
   "name":"ABC Test",
   "description":"This is a test offer", 
   "link":"https://sampletesting.online/",
   "image":"https://sample-demo-URL.png"
}
```

处理响应对象并解析所需的数据。 因为您可以在一个决策范围中发送多个决策范围 `sendEvent` 调用，您的响应可能略有不同。

```
json
    {
        "id": "abrxgl843d913",
        "scope": "eyJ4ZG06YWN0aXZpdHlJZCI6Inhjb3JlOm9mZmVyLWFjdGl2aXR5OjE0ZWE4MDhhZjJjZDM1NzQiLCJ4ZG06cGxhY2VtZW50SWQiOiJ4Y29yZTpvZmZlci1wbGFjZW1lbnQ6MTRjNGFmZDI2OTVlNWRmOSJ9",
        "items": 
        [
            {
                "id": "xcore:fallback-offer:14ea7f1ea26ebd0a",
                "etag": "1",
                "schema": "https://ns.adobe.com/experience/offer-management/content-component-json",
                "data": {
                    "id": "xcore:fallback-offer:14ea7f1ea26ebd0a",
                    "format": "application/json",
                    "language": [
                        "en-us"
                    ],
                    "content": "{\"name\":\"ABC Test\",\"description\":\"This is a test offer\", \"link\":\"https://sampletesting.online/\",\"image\":\"https://sample-demo-URL.png\"}"
                }
            }
        ]
    }
]
}
```

```
json
{
    "propositions": 
    [
    {
        "renderAttempted": false,
        "id": "e15ecb09-993e-4b66-93d8-0a4c77e3d913",
        "scope": "eyJ4ZG06YWN0aXZpdHlJZCI6Inhjb3JlOm9mZmVyLWFjdGl2aXR5OjE0ZWE4MDhhZjJjZDM1NzQiLCJ4ZG06cGxhY2VtZW50SWQiOiJ4Y29yZTpvZmZlci1wbGFjZW1lbnQ6MTRjNGFmZDI2OTVlNWRmOSJ9",
        "items": 
        [
            {
                "id": "xcore:fallback-offer:14ea7f1ea26ebd0a",
                "etag": "1",
                "schema": "https://ns.adobe.com/experience/offer-management/content-component-json",
                "data": {
                    "id": "xcore:fallback-offer:14ea7f1ea26ebd0a",
                    "format": "application/json",
                    "language": [
                        "en-us"
                    ],
                    "content": "{\"name\":\"Claire Hubacek Test\",\"description\":\"This is a test offer\", \"link\":\"https://sampletesting.online/\",\"image\":\"https://sample-demo-URL.png\"}"
                }
            }
        ]
    }
    ]
}
```

在此示例中，在网页中处理和使用特定于选件的详细信息所需的路径是： `result['decisions'][0]['items'][0]['data']['content']`

要设置JS变量，请执行以下操作：

```
javascript
const offer = JSON.parse(result['decisions'][0]['items'][0]['data']['content']);

let offerURL = offer['link'];
let offerDescription = offer['description'];
let offerImageURL = offer['image'];

document.getElementById("offerDescription").innerHTML = offerDescription;
document.getElementById('offerImage').src = offerImageURL;
```

<!--## Limitations

Some offer constraints are currently not supported with the mobile Experience Edge workflows, for example Capping. The Capping field value specifies the number of times an offer can be presented across all users. For more details, see [Add constraints to an offer](../../offer-library/add-constraints.md#capping).-->
