---
title: 基于代码的实施示例
description: 本页显示了Journey Optimizer基于代码的功能实施方法示例
feature: Offers
topic: Content Management
role: User
level: Experienced
hide: true
hidefromtoc: true
badge: label="Beta 版"
source-git-commit: f271aa457d2f8b7e66e58692b613d80c6e6b3adb
workflow-type: tm+mt
source-wordcount: '825'
ht-degree: 5%

---

# 基于代码的实施方法示例 {#implementation-samples}

>[!BEGINSHADEBOX]

本文档指南包括以下内容：

* [基于代码的渠道入门](get-started-code-based.md)
* [基于代码的先决条件](code-based-prerequisites.md)
* **[基于代码的实施示例](code-based-implementation-samples.md)**
* [创建基于代码的体验](create-code-based.md)

>[!ENDSHADEBOX]

基于代码的体验支持任何类型的客户实施。 在此页上，您可以找到每种实施方法的示例：

* [客户端](#client-side-implementation)
* [服务器端](#server-side-implementation)
* [混合](#hybrid-implementation)

您也可以关注 [此链接](https://github.com/adobe/alloy-samples/tree/main/ajo){target="_blank"} 查找不同个性化和实验用例的示例实施。 查看并运行这些扩展，以便更好地了解所需的实施步骤以及端到端个性化流程的工作方式。

## 客户端实施 {#client-side-implementation}

如果您有客户端实施，则可以使用以下其中一个AEP客户端SDK：AEP Web SDK或AEP Mobile SDK。 以下步骤描述在示例Web SDK实施中获取由基于代码的体验营销活动在Edge上发布的内容并显示个性化内容的过程。

### 工作原理

1. [Web SDK](https://experienceleague.adobe.com/docs/experience-platform/edge/home.html?lang=zh-Hans){target="_blank"} 将包含在页面中。

1. 您需要使用 `sendEvent` 命令并指定用于获取个性化内容的表面URI。

   ```javascript
   alloy("sendEvent", {
   renderDecisions: true,
   personalization: {
       surfaces: ["#sample-json-content"],
   },
   }).then(applyPersonalization("#sample-json-content"));
   ```

1. 基于代码的体验项目应由实施代码手动应用(使用 [`applyPersonalization`](https://github.com/adobe/alloy-samples/blob/ac83b6927d007dc456caad2c6ce0b324c99c26c9/ajo/personalization-client-side/public/script.js){target="_blank"} 方法)根据决策更新DOM。

1. 对于基于代码的体验营销活动，必须手动发送显示事件以指示何时显示内容。 这可以通过以下方式实现 `sendEvent` 命令。

```javascript
function sendDisplayEvent(decision) {
  const { id, scope, scopeDetails = {} } = decision;

  alloy("sendEvent", {

    xdm: {
      eventType: "decisioning.propositionDisplay",
      _experience: {
        decisioning: {
          propositions: [
            {
              id: id,
              scope: scope,
              scopeDetails: scopeDetails,
            },
          ],
        },
      },
    },
  });
}
```

### 主要意见

**Cookie**

Cookie用于保留用户标识和群集信息。 使用客户端实施时，Web SDK会在请求生命周期中自动处理这些Cookie的存储和发送。

| Cookie | 用途 | 存储者 | 发送者 |
| ------------------------ | -------------------------------------------------------------------------- | --------- | ------- |
| kndctr_AdobeOrg_identity | 包含用户身份详细信息 | Web SDK | Web SDK |
| kndctr_AdobeOrg_cluster | 指示应使用哪个体验边缘群集来完成请求 | Web SDK | Web SDK |

**请求投放**

需要向Adobe Experience Platform API发出请求才能获取建议并发送显示通知。 在使用客户端实施时，Web SDK在以下情况下发出这些请求： `sendEvent` 命令。

| 请求 | 创建者 |
| ---------------------------------------------- | ----------------------------------- |
| interact请求以获取建议 | 使用sendEvent命令的Web SDK |
| interact请求发送显示通知 | 使用sendEvent命令的Web SDK |

**流程图**

![](assets/code-based-client-side-implementation.png)

## 服务器端实施 {#server-side-implementation}

如果您有服务器端实施，则可以使用一个AEP Edge Network API。 以下步骤在示例网页的Edge Network API实施中描述了获取由基于代码的体验营销活动在Edge上发布的内容并显示个性化内容的过程。

### 工作原理

1. 将请求网页，以及浏览器之前存储的以为前缀的任何Cookie `kndctr_` 中包含。
1. 当从应用程序服务器请求该页面时，会将事件发送到 [交互式数据收集端点](https://experienceleague.adobe.com/docs/experience-platform/edge-network-server-api/data-collection/interactive-data-collection.html?lang=en) 以获取个性化内容。 此示例应用程序使用一些帮助程序方法来简化构建请求并将请求发送到API(请参阅 [aepEdgeClient.js](https://github.com/adobe/alloy-samples/blob/ac83b6927d007dc456caad2c6ce0b324c99c26c9/common/aepEdgeClient.js){target="_blank"})。 但要求只是 `POST` 有效负载中包含事件和查询。 上一步骤中的Cookie（如果可用）包含在中的请求中 `meta>state>entries` 数组。

   ```javascript
   fetch(
     "https://edge.adobedc.net/ee/v2/interact?dataStreamId=abc&requestId=123",
     {
       headers: {
         accept: "*/*",
         "accept-language": "en-US,en;q=0.9",
         "cache-control": "no-cache",
         "content-type": "text/plain; charset=UTF-8",
         pragma: "no-cache",
         "sec-fetch-dest": "empty",
         "sec-fetch-mode": "cors",
         "sec-fetch-site": "cross-site",
         "sec-gpc": "1",
         "Referrer-Policy": "strict-origin-when-cross-origin",
         Referer: "https://localhost/",
       },
       body: JSON.stringify({
         event: {
           xdm: {
             eventType: "decisioning.propositionFetch",
             web: {
               webPageDetails: {
                 URL: "https://localhost/",
               },
               webReferrer: {
                 URL: "",
               },
             },
             identityMap: {
               FPID: [
                 {
                   id: "xyz",
                   authenticatedState: "ambiguous",
                   primary: true,
                 },
               ],
             },
             timestamp: "2022-06-23T22:21:00.878Z",
           },
           data: {},
         },
         query: {
           identity: {
             fetch: ["ECID"],
           },
           personalization: {
             schemas: [
               "https://ns.adobe.com/personalization/default-content-item",
               "https://ns.adobe.com/personalization/html-content-item",
               "https://ns.adobe.com/personalization/json-content-item",
               "https://ns.adobe.com/personalization/redirect-item",
               "https://ns.adobe.com/personalization/dom-action",
             ],
             surfaces: ["web://localhost/","web://localhost/#sample-json-content"],
           },
         },
         meta: {
           state: {
             domain: "localhost",
             cookiesEnabled: true,
             entries: [
               {
                 key: "kndctr_XXX_AdobeOrg_identity",
                 value: "abc123",
               },
               {
                 key: "kndctr_XXX_AdobeOrg_cluster",
                 value: "or2",
               },
             ],
           },
         },
       }),
       method: "POST",
     }
   ).then((res) => res.json());
   ```

1. 从响应中读取基于代码的体验营销活动中的JSON体验，并在生成HTML响应时使用。
1. 对于基于代码的体验营销活动，必须在实施中手动发送显示事件，以指示何时显示营销活动内容。 在此示例中，通知在请求生命周期期间在服务器端发送。

   ```javascript
   function sendDisplayEvent(aepEdgeClient, req, propositions, cookieEntries) {
     const address = getAddress(req);
   
     aepEdgeClient.interact(
       {
         event: {
           xdm: {
             web: {
               webPageDetails: { URL: address },
               webReferrer: { URL: "" },
             },
             timestamp: new Date().toISOString(),
             eventType: "decisioning.propositionDisplay",
             _experience: {
               decisioning: {
                 propositions: propositions.map((proposition) => {
                   const { id, scope, scopeDetails } = proposition;
   
                   return {
                     id,
                     scope,
                     scopeDetails,
                   };
                 }),
               },
             },
           },
         },
         query: { identity: { fetch: ["ECID"] } },
         meta: {
           state: {
             domain: "",
             cookiesEnabled: true,
             entries: [...cookieEntries],
           },
         },
       },
       {
         Referer: address,
       }
     );
   }
   ```

1. 当返回HTML响应时，应用服务器将在响应中设置标识和群集Cookie。

### 主要意见

**Cookie**

Cookie用于保留用户标识和群集信息。 在使用服务器端实施时，应用程序服务器必须在请求生命周期内处理这些Cookie的存储和发送。

| Cookie | 用途 | 存储者 | 发送者 |
| ------------------------ | -------------------------------------------------------------------------- | ------------------ | ------------------ |
| kndctr_AdobeOrg_identity | 包含用户身份详细信息 | 应用程序服务器 | 应用程序服务器 |
| kndctr_AdobeOrg_cluster | 指示应使用哪个体验边缘群集来完成请求 | 应用程序服务器 | 应用程序服务器 |

**请求投放**

需要向Adobe Experience Platform API发出请求才能获取建议并发送显示通知。 在使用客户端实施时，Web SDK在以下情况下发出这些请求： `sendEvent` 命令。

| 请求 | 创建者 |
| ---------------------------------------------- | ------------------------------------------------------------ |
| interact请求以获取建议 | 应用程序服务器调用Adobe Experience Platform API |
| interact请求发送显示通知 | 应用程序服务器调用Adobe Experience Platform API |

**流程图**

![](assets/code-based-server-side-implementation.png)

## 混合实施 {#hybrid-implementation}

如果您有混合实施，请查看以下链接。

* Adobe技术博客： [Adobe Experience Platform Web SDK中的混合个性化](https://blog.developer.adobe.com/hybrid-personalization-in-the-adobe-experience-platform-web-sdk-6a1bb674bf41){target="_blank"}
* SDK文档： [使用Web SDK和边缘网络服务器API的混合个性化](https://experienceleague.adobe.com/docs/experience-platform/edge/personalization/hybrid-personalization.html){target="_blank"}

