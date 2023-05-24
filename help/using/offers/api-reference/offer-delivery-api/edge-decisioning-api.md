---
title: 使用Edge Decisioning API提供優惠方案
description: Adobe Experience Platform Web SDK可讓您擷取及轉譯您使用API或優惠資料庫建立的個人化優惠。
feature: Offers
topic: Integrations
role: Data Engineer
level: Experienced
exl-id: 4e2dc0d6-4610-4a2f-8388-bc58182b227f
source-git-commit: 7347bb56eb2785b2d9f3f641cbe3b7c1ae2d078f
workflow-type: tm+mt
source-wordcount: '1013'
ht-degree: 4%

---

# 使用Edge Decisioning API提供優惠方案 {#edge-decisioning-api}

## 快速入門與必要條件 {#edge-overview-and-prerequisites}

此 [Adobe Experience Platform Web SDK](https://experienceleague.adobe.com/docs/experience-platform/edge/home.html#video-overview) 是使用者端JavaScript程式庫，可讓Adobe Experience Cloud客戶透過Experience PlatformEdge Network與Experience Cloud中的各種服務互動。

Experience PlatformWeb SDK支援在Adobe查詢個人化解決方案，包括決定管理，可讓您擷取並轉譯您使用API或優惠資料庫建立的個人化優惠。 如需詳細指示，請參閱以下檔案： [建立優惠方案](../../get-started/starting-offer-decisioning.md).

有兩種方式可透過實施決策管理 [平台Web SDK](https://experienceleague.adobe.com/docs/experience-platform/edge/home.html#video-overview). 一種方式是針對開發人員，需要網站和程式設計知識。 另一種方式是使用Adobe Experience Platform使用者介面來設定選件，該選件只需要在HTML頁面的標頭中參照小型指令碼。

請參閱以下檔案： [決策管理](https://experienceleague.adobe.com/docs/experience-platform/edge/personalization/offer-decisioning/offer-decisioning-overview.html?lang=en#enabling-offer-decisioning) 有關如何使用Adobe Experience Platform Web SDK提供個人化優惠方案的詳細資訊。

>[!NOTE]
>
>Adobe Experience Platform Web SDK中的決定管理僅適用於一組組織（可用性限制）。 如果您想要運用此功能，請聯絡您的Adobe客戶主管。

## Adobe Experience Platform Web SDK {#aep-web-sdk}

Platform Web SDK會取代下列SDK：

* Visitor.js
* AppMeasurement.js
* AT.js
* DIL.js

SDK並未合併這些程式庫，而是全新實施。 若要使用它，您必須先執行下列步驟：

1. 確保您的組織具有使用SDK的適當許可權，且您已正確設定許可權。

   <!-- For more detailed instructions, refer to the documentation on using the [Adobe Experience Platform Web SDK](). -->

1. [設定您的資料串流](https://experienceleague.adobe.com/docs/experience-platform/edge/fundamentals/datastreams.html?lang=zh-Hans) (位於您在Adobe Experience Cloud帳戶中的「資料收集」標籤內)。

1. 安裝SDK。 有多種方法可以做到，詳見 [安裝SDK頁面](https://experienceleague.adobe.com/docs/experience-platform/edge/fundamentals/installing-the-sdk.html?lang=en). 本頁將繼續顯示各種不同的實作方法。

若要使用SDK，您必須擁有 [綱要](../../../data/get-started-schemas.md) 和 [資料串流](../../../data/get-started-datasets.md) 已定義。

<!-- ****TODO - Configure schema**** -->

若要個人化優惠方案，您必須個別設定個人化/設定檔。

<!-- Refer to the [doc](www.link.com) for detailed instructions.  -->

若要設定SDK以進行決策管理，請遵循下列兩個步驟之一：

## 選項1 — 使用Launch安裝標籤擴充功能和實施

此選項對編碼體驗較差的人來說更容易使用。

1. [建立標籤屬性](https://experienceleague.adobe.com/docs/experience-platform/tags/admin/companies-and-properties.html?lang=zh-Hans)

1. [新增內嵌程式碼](https://experienceleague.adobe.com/docs/core-services-learn/implementing-in-websites-with-launch/configure-launch/launch-add-embed.html?lang=en)

1. 使用您從「資料流」下拉式選單中選取設定而建立的資料流，安裝並設定Adobe Experience Platform Web SDK擴充功能。 請參閱以下說明檔案： [擴充功能](https://experienceleague.adobe.com/docs/experience-platform/tags/ui/extensions/overview.html?lang=en).

   ![Adobe Experience Platform Web SDK](../../assets/installed-catalog-web-sdk.png)

   ![設定擴充功能](../../assets/configure-sdk-extension.png)

1. 建立必要的 [資料元素](https://experienceleague.adobe.com/docs/experience-platform/tags/ui/data-elements.html?lang=zh-Hans). 您至少必須建立Platform Web SDK身分對應和Platform Web SDK XDM物件資料元素。

   ![标识映射](../../assets/sdk-identity-map.png)

   ![XDM 对象](../../assets/xdm-object.png)

1. 建立您的 [規則](https://experienceleague.adobe.com/docs/experience-platform/tags/ui/rules.html?lang=en)：

   新增Platform Web SDK傳送事件動作，並將相關decisionScopes新增至該動作的設定

   ![演算選件](../../assets/rule-render-offer.png)

   ![請求優惠](../../assets/rule-request-offer.png)

1. [建立並發佈](https://experienceleague.adobe.com/docs/experience-platform/tags/publish/libraries.html?lang=en) 包含所有已設定相關規則、資料元素和擴充功能的程式庫。

## 選項2 — 使用預先建立的獨立版本手動實作

以下是使用Web SDK預先建立的獨立安裝來使用決定管理所需的步驟。 本指南假設這是您首次實作SDK，因此所有步驟可能不適用於您。 本指南也假定您有一些開發經驗。

包含選項2的以下JavaScript程式碼片段：上的預先建立獨立版本 [此頁面](https://experienceleague.adobe.com/docs/experience-platform/edge/fundamentals/installing-the-sdk.html?lang=en) 在 `<head>` HTML部分。

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

您需要Adobe帳戶中的兩個ID才能設定SDK設定：edgeConfigId和orgId。 edgeConfigId與您的資料串流ID相同，您應在「先決條件」中設定該ID。

若要尋找您的edgeConfigID/資料串流ID，請前往「資料收集」並選取您的「資料串流」。 若要尋找您的orgId，請前往您的設定檔。

依照本頁面的指示，在JavaScript中設定SDK。 您一律會在設定函式中使用edgeConfigId和orgId。 本檔案也會說明您的設定有哪些可選引數。 您的最終設定可能如下所示：

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

安裝用於偵錯的Debugger Chrome擴充功能。 您可在下列位置找到： <https://chrome.google.com/webstore/detail/adobe-experience-platform/bfnnokhpnncpkdmbokanobigaccjkpob>

接下來，在除錯程式中登入您的帳戶。 接著，前往「記錄檔」 ，確認您已連線至正確的工作區。 現在，從您的優惠方案複製決定範圍的base64編碼版本。

編輯您的網站時，請包含具有設定的指令碼，以及 `sendEvent` 將決定範圍傳送至Adobe的函式。

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

如需如何處理回應的範例，請參閱下列內容：

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

您可以使用Debugger來確認您已成功連線至Edge網路。

>[!NOTE]
>
>如果您在記錄檔中看不到與邊緣的連線，則可能需要停用廣告封鎖程式。

請參閱如何建立優惠方案及使用的格式。 系統會根據決定中所符合的條件，傳回優惠給您，其中包含您在Adobe Experience Platform中建立優惠時指定的資訊。

在此範例中，要傳回的JSON為：

```
json
{
   "name":"ABC Test",
   "description":"This is a test offer", 
   "link":"https://sampletesting.online/",
   "image":"https://sample-demo-URL.png"
}
```

處理回應物件並剖析您需要的資料。 因為您可以在一個傳送多個決定範圍 `sendEvent` 呼叫，您的回應可能會稍有不同。

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

在此範例中，在網頁中處理和使用選件特定詳細資料所需的路徑為： `result['decisions'][0]['items'][0]['data']['content']`

若要設定JS變數：

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
