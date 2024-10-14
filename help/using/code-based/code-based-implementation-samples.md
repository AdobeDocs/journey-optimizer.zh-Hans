---
title: 基于代码的实施示例
description: 本页显示了Journey Optimizer基于代码的功能实施方法示例
feature: Code-based Experiences
topic: Content Management
role: Developer
level: Experienced
exl-id: e5ae8b4e-7cd2-4a1d-b2c0-8dafd5c4cdfd
source-git-commit: e3c597f66436e8e0e22d06f1905fc7ca9a9dd570
workflow-type: tm+mt
source-wordcount: '786'
ht-degree: 2%

---

# 基于代码的实施方法示例 {#implementation-samples}

基于代码的体验支持任何类型的客户实施。 在此页上，您可以找到每种实施方法的示例：

* [客户端](#client-side-implementation)
* [服务器端](#server-side-implementation)
* [混合](#hybrid-implementation)

>[!IMPORTANT]
>
>按照[此链接](https://github.com/adobe/alloy-samples/tree/main/ajo){target="_blank"}查找不同个性化和试验用例的示例实施。 查看并运行这些扩展，以便更好地了解所需的实施步骤以及端到端个性化流程的工作方式。

## 客户端实施 {#client-side-implementation}

如果您有客户端实施，则可以使用以下其中一个AEP客户端SDK：AEP Web SDK或AEP Mobile SDK。

* 下面的步骤[描述在示例&#x200B;**Web SDK**&#x200B;实现中获取基于代码的体验营销活动在边缘上发布的内容并显示个性化内容的过程。](#client-side-how)

* [本教程](https://developer.adobe.com/client-sdks/edge/adobe-journey-optimizer/code-based/tutorial/){target="_blank"}中介绍了使用&#x200B;**Mobile SDK**&#x200B;实施基于代码的通道的步骤。

  >[!NOTE]
  >
  >移动使用案例的示例实施适用于[iOS应用程序](https://github.com/adobe/aepsdk-messaging-ios/tree/main/TestApps/MessagingDemoAppSwiftUI){target="_blank"}和[Android应用程序](https://github.com/adobe/aepsdk-messaging-android/tree/main/code/testapp){target="_blank"}。

### 工作原理 — Web SDK {#client-side-how}

1. [Web SDK](https://experienceleague.adobe.com/docs/experience-platform/edge/home.html){target="_blank"}已包含在此页面中。

1. 您需要使用`sendEvent`命令并指定[表面URI](code-based-configuration.md#surface-definition)<!--( or location/path)-->来获取个性化内容。

   ```javascript
   alloy("sendEvent", {
   renderDecisions: true,
   personalization: {
       surfaces: ["#sample-json-content"],
   },
   }).then(applyPersonalization("#sample-json-content"));
   ```

1. 基于代码的体验项应由实现代码（使用[`applyPersonalization`](https://github.com/adobe/alloy-samples/blob/ac83b6927d007dc456caad2c6ce0b324c99c26c9/ajo/personalization-client-side/public/script.js){target="_blank"}方法）手动应用，以根据决策更新DOM。

1. 对于基于代码的体验营销活动，必须手动发送显示事件以指示何时显示内容。 这是通过`sendEvent`命令完成的。

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

1. 对于基于代码的体验营销活动，必须手动发送交互事件以指示用户何时与内容交互。 这是通过`sendEvent`命令完成的。

   ```javascript
   function sendInteractEvent(label, proposition) {
     const { id, scope, scopeDetails = {} } = proposition;
   
     alloy("sendEvent", {
   
       xdm: {
         eventType: "decisioning.propositionInteract",
         _experience: {
           decisioning: {
             propositions: [
               {
                 id: id,
                 scope: scope,
                 scopeDetails: scopeDetails,
               },
             ],
             propositionEventType: {
               interact: 1
             },
             propositionAction: {
               label: label
             },
           },
         },
       },
     });
   }
   ```

### 主要意见

**Cookie**

Cookie用于保留用户标识和群集信息。 使用客户端实施时，Web SDK会在请求生命周期中自动处理这些Cookie的存储和发送。

| Cookie | 目的 | 存储者 | 发送者 |
| ------------------------ | -------------------------------------------------------------------------- | --------- | ------- |
| kndctr_AdobeOrg_identity | 包含用户身份详细信息 | Web SDK | Web SDK |
| kndctr_AdobeOrg_cluster | 指示应使用哪个体验边缘群集来完成请求 | Web SDK | Web SDK |

**请求放置**

需要向Adobe Experience Platform API发出请求才能获取建议并发送显示通知。 在使用客户端实施时，Web SDK会在使用`sendEvent`命令时发出这些请求。

| 请求 | 创建者 |
| ---------------------------------------------- | ----------------------------------- |
| interact请求以获取建议 | 使用sendEvent命令的Web SDK |
| interact请求发送显示通知 | 使用sendEvent命令的Web SDK |

**流程图**

![](assets/code-based-client-side-implementation.png)

## 服务器端实施 {#server-side-implementation}

如果您有服务器端实施，则可以使用一个AEPEdge NetworkAPI。

以下步骤在示例网页的Edge NetworkAPI实现中描述了获取由基于代码的体验营销活动在Edge上发布的内容并显示个性化内容的过程。

### 工作原理

1. 已请求该网页，并且包含以前由浏览器存储的以`kndctr_`为前缀的所有Cookie。
1. 从应用服务器请求该页面时，会向[交互式数据收集终结点](https://experienceleague.adobe.com/docs/experience-platform/edge-network-server-api/data-collection/interactive-data-collection.html)发送一个事件以获取个性化内容。 此示例应用程序使用一些帮助程序方法来简化生成请求并将请求发送到API（请参阅[aepEdgeClient.js](https://github.com/adobe/alloy-samples/blob/ac83b6927d007dc456caad2c6ce0b324c99c26c9/common/aepEdgeClient.js){target="_blank"}）。 但请求只是具有包含事件和查询的有效负载的`POST`。 上一步骤中的Cookie（如果可用）包含在`meta>state>entries`数组的请求中。

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

| Cookie | 目的 | 存储者 | 发送者 |
| ------------------------ | -------------------------------------------------------------------------- | ------------------ | ------------------ |
| kndctr_AdobeOrg_identity | 包含用户身份详细信息 | 应用程序服务器 | 应用程序服务器 |
| kndctr_AdobeOrg_cluster | 指示应使用哪个体验边缘群集来完成请求 | 应用程序服务器 | 应用程序服务器 |

**请求放置**

需要向Adobe Experience Platform API发出请求才能获取建议并发送显示通知。 在使用客户端实施时，Web SDK会在使用`sendEvent`命令时发出这些请求。

| 请求 | 创建者 |
| ---------------------------------------------- | ------------------------------------------------------------ |
| interact请求以获取建议 | 应用程序服务器调用Adobe Experience Platform API |
| interact请求发送显示通知 | 应用程序服务器调用Adobe Experience Platform API |

**流程图**

![](assets/code-based-server-side-implementation.png)

## 混合实现 {#hybrid-implementation}

如果您有混合实施，请查看以下链接。

* Adobe技术博客：Adobe Experience Platform Web SDK中的[Hybrid Personalization](https://blog.developer.adobe.com/hybrid-personalization-in-the-adobe-experience-platform-web-sdk-6a1bb674bf41){target="_blank"}
* SDK文档：[使用Web SDK和Edge Network服务器API的混合个性化](https://experienceleague.adobe.com/docs/experience-platform/edge/personalization/hybrid-personalization.html){target="_blank"}
