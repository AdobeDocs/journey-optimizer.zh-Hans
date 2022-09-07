---
title: 使用Edge Decisioning API提供优惠
description: Adobe Experience Platform Web SDK允许您检索和渲染使用API或选件库创建的个性化选件。
feature: Offers
topic: Integrations
role: Data Engineer
level: Experienced
exl-id: 4e2dc0d6-4610-4a2f-8388-bc58182b227f
source-git-commit: c530905eacbdf6161f6449d7a0b39c8afaf3a321
workflow-type: tm+mt
source-wordcount: '1054'
ht-degree: 2%

---

# 使用Edge Decisioning API提供优惠 {#edge-decisioning-api}

## 入门指南和先决条件 {#edge-overview-and-prerequisites}

的 [Adobe Experience Platform Web SDK](https://experienceleague.adobe.com/docs/experience-platform/edge/home.html#video-overview) 是一个客户端JavaScript库，它允许Adobe Experience Cloud客户通过Experience Platform边缘网络与Experience Cloud中的各种服务进行交互。

Experience PlatformWeb SDK支持在Adobe中查询个性化解决方案（包括决策管理），从而允许您检索和渲染使用API或选件库创建的个性化选件。 有关更多详细说明，请参阅 [创建优惠](../../get-started/starting-offer-decisioning.md).

可使用以下两种方式实施决策管理： [平台Web SDK](https://experienceleague.adobe.com/docs/experience-platform/edge/home.html#video-overview). 一种方法是面向开发人员，需要了解网站和编程知识。 另一种方法是使用Adobe Experience Platform用户界面设置选件，该选件只需在HTML页面的标题中引用一个小脚本即可。

请参阅 [决策管理](https://experienceleague.adobe.com/docs/experience-platform/edge/personalization/offer-decisioning/offer-decisioning-overview.html?lang=en#enabling-offer-decisioning) 有关如何使用Platform Web SDK提供个性化优惠的更多信息。

>[!NOTE]
>
>Adobe Experience Platform Web SDK中的决策管理仅适用于一组组织（有限可用性）。 如果要利用此功能，请联系您的Adobe客户经理。

## Adobe Experience Platform Web SDK {#aep-web-sdk}

Platform Web SDK取代了以下SDK:

* Visitor.js
* AppMeasurement.js
* AT.js
* DIL.js

SDK未合并这些库，而是从头开始的一项新实施。 要使用它，您必须首先执行以下步骤：

1. 确保贵组织具有使用SDK的适当权限，并且您已正确配置了这些权限。

   <!-- For more detailed instructions, refer to the documentation on using the [Adobe Experience Platform Web SDK](). -->

1. [配置数据流](https://experienceleague.adobe.com/docs/experience-platform/edge/fundamentals/datastreams.html?lang=en) (位于您帐户的Adobe Experience Cloud中的数据收集选项卡中)。

1. 安装SDK。 可以使用多种方法来执行此操作，详情请参阅 [安装SDK页面](https://experienceleague.adobe.com/docs/experience-platform/edge/fundamentals/installing-the-sdk.html?lang=en). 本页将继续介绍每种不同的实施方法。

要使用SDK，您必须具有 [模式](../../../start/get-started-schemas.md) 和 [数据流](../../../start/get-started-datasets.md) 定义。

<!-- ****TODO - Configure schema**** -->

要个性化选件，您必须单独配置个性化/配置文件。

<!-- Refer to the [doc](www.link.com) for detailed instructions.  -->

要配置SDK以进行决策管理，请执行以下两个步骤之一：

## 选项1 — 使用Launch安装标记扩展和实施

对于编码体验可能较少的用户而言，此选项更易于使用。

1. [创建标记属性](https://experienceleague.adobe.com/docs/experience-platform/tags/admin/companies-and-properties.html?lang=en)

1. [添加嵌入代码](https://experienceleague.adobe.com/docs/core-services-learn/implementing-in-websites-with-launch/configure-launch/launch-add-embed.html?lang=en)

1. 使用您通过从“Datastream”下拉菜单中选择配置而创建的数据流，安装和配置Platform Web SDK扩展。 请参阅 [扩展](https://experienceleague.adobe.com/docs/experience-platform/tags/ui/extensions/overview.html?lang=en).

   ![Adobe Experience Platform Web SDK](../../assets/installed-catalog-web-sdk.png)

   ![配置扩展](../../assets/configure-sdk-extension.png)

1. 创建必需的 [数据元素](https://experienceleague.adobe.com/docs/experience-platform/tags/ui/data-elements.html?lang=en). 您至少必须创建Platform Web SDK身份映射和Platform Web SDK XDM对象数据元素。

   ![标识映射](../../assets/sdk-identity-map.png)

   ![XDM 对象](../../assets/xdm-object.png)

1. 创建 [规则](https://experienceleague.adobe.com/docs/experience-platform/tags/ui/rules.html?lang=en):

   添加Platform Web SDK发送事件操作，并将相关决策作用域添加到该操作的配置中

   ![渲染选件](../../assets/rule-render-offer.png)

   ![请求选件](../../assets/rule-request-offer.png)

1. [创建和发布](https://experienceleague.adobe.com/docs/experience-platform/tags/publish/libraries.html?lang=en) 包含您配置的所有相关规则、数据元素和扩展的库。

## 选项2 — 使用预建的独立版本手动实施

以下是使用预建的独立安装Web SDK来使用决策管理所需的步骤。 本指南假定这是您首次实施SDK，因此所有步骤可能不适用于您。 本指南还假定具有一些开发经验。

在选项2中包含以下JavaScript代码片段：上预建的独立版本 [本页](https://experienceleague.adobe.com/docs/experience-platform/edge/fundamentals/installing-the-sdk.html?lang=en) 在 `<head>` HTML页面的部分。

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

您需要Adobe帐户中的两个ID来设置SDK配置 — 您的edgeConfigId和您的orgId。 edgeConfigId与您的数据流ID相同，您应该在先决条件中配置该ID。

要查找您的edgeConfigID/数据流ID，请转到“数据收集”并选择您的数据流。 要查找您的orgId，请转到您的用户档案。

按照本页中的说明在JavaScript中配置SDK。 您将始终在配置函数中使用您的edgeConfigId和orgId。 本文档还介绍了配置中存在的可选参数。 您的最终配置可能会如下所示：

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

安装要与调试结合使用的Debugger Chrome扩展。 可在此处找到： <https://chrome.google.com/webstore/detail/adobe-experience-platform/bfnnokhpnncpkdmbokanobigaccjkpob>

接下来，在调试器中登录您的帐户。 然后，转到日志，并确保您已连接到正确的工作区。 现在，从您的选件中复制决策范围的base64编码版本。

在编辑网站时，请包含具有配置的脚本，以及 `sendEvent` 函数将决策范围发送到Adobe。

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

您可以使用调试器验证您是否已成功连接到边缘网络。

>[!NOTE]
>
>如果您在日志中未看到与边缘的连接，则可能需要禁用广告拦截器。

请参阅创建选件的方式和使用的格式。 根据决策中满足的条件，您将收到一个选件，其中包含您在Adobe Experience Platform中创建该选件时指定的信息。

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

处理响应对象并解析所需的数据。 因为您可以在一个中发送多个决策范围 `sendEvent` 呼叫，您的响应可能看起来会略有不同。

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

在此示例中，处理和使用网页中特定于选件的详细信息所需的路径是： `result['decisions'][0]['items'][0]['data']['content']`

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

## 限制

移动设备体验边缘工作流程当前不支持某些选件约束，例如上限。 上限字段值指定选件在所有用户中可显示的次数。 有关更多详细信息，请参阅 [向选件添加约束](../../offer-library/add-constraints.md#capping).
