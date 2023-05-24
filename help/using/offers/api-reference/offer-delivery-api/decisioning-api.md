---
title: 傳遞優惠方案
description: 決定管理是服務和UI程式的集合，可讓行銷人員使用商業邏輯和決定規則，跨頻道和應用程式建立和提供一般使用者個人化優惠體驗。
feature: Offers
topic: Integrations
role: Data Engineer
level: Experienced
exl-id: 692d0aae-6fa1-40b8-a35f-9845d78317a3
source-git-commit: a2f4a7f7b08cce3980eab71fea0b2704975087ca
workflow-type: tm+mt
source-wordcount: '1058'
ht-degree: 3%

---

# 使用Decisioning API傳遞優惠方案 {#decisioning-api}

透過決定管理，您可以使用商業邏輯和決定規則，跨管道和應用程式建立並提供使用者個人化的優惠體驗。 優惠方案是行銷訊息，其中可能包含與其關聯的規則，以指定誰有資格檢視優惠方案。

您可以透過向以下傳送POST要求來建立及傳遞優惠方案： [!DNL Decisioning] API。

本教學課程需要實際瞭解API，尤其是與決策管理有關的內容。 如需詳細資訊，請參閱 [Decision Management API開發人員指南](../getting-started.md). 本教學課程也要求您有唯一版位ID和決定ID值可用。 如果您尚未取得這些值，請參閱以下教學課程： [建立位置](../offers-api/placements/create.md) 和 [建立決定](../activities-api/activities/create.md).

➡️  [在视频中发现此功能](#video)

## Accept和Content-Type標題 {#accept-and-content-type-headers}

下表顯示包含 *Content-Type* 和 *Accept* 請求標頭中的欄位：

| 標頭名稱 | 值 |
| ----------- | ----- |
| Accept | `application/vnd.adobe.xdm+json; schema="https://ns.adobe.com/experience/offer-management/decision-response;version=1.0"` |
| Content-Type | `application/vnd.adobe.xdm+json; schema="https://ns.adobe.com/experience/offer-management/decision-request;version=1.0"` |

## API要求 {#request}

### API格式

```https
POST /{ENDPOINT_PATH}/{CONTAINER_ID}/decisions
```

| 参数 | 描述 | 示例 |
| --------- | ----------- | ------- |
| `{ENDPOINT_PATH}` | 存放庫API的端點路徑。 | `https://platform.adobe.io/data/core/ode/` |
| `{CONTAINER_ID}` | 決策所在的容器。 | `e0bd8463-0913-4ca1-bd84-6309134ca1f6` |

### 请求

```shell
curl -X POST \
  'https://platform.adobe.io/data/core/ode/e0bd8463-0913-4ca1-bd84-6309134ca1f6/decisions' \
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
| `xdm:propositionRequests` | 此物件包含位置與決定識別碼。 |
| `xdm:propositionRequests.xdm:placementId` | 唯一位置識別碼。 | `"xdm:placementId": "xcore:offer-placement:ffed0456"` |
| `xdm:propositionRequests.xdm:activityId` | 唯一決定識別碼。 | `"xdm:activityId": "xcore:offer-activity:ffed0123"` |
| `xdm:itemCount` | 要傳回的優惠方案數量。 最大數目為30。 | `"xdm:itemCount": 2` |
| `xdm:profiles` | 此物件保有請求決策的設定檔相關資訊。 對於API請求，這將包含一個設定檔。 |
| `xdm:profiles.xdm:identityMap` | 此物件根據身分的名稱空間整合程式碼，保留一組一般使用者身分。 身分對應可攜帶每個名稱空間多個身分。 有关命名空间的更多信息，请参阅[此页面](../../../segment/get-started-identity.md)。 | `Email: [{"xdm:id": "123@abc.com"}]` |
| `xdm:profiles.xdm:decisionRequestId` | 使用者端產生的ID，可用於唯一識別設定檔決定請求。 此ID會回應回來，不會影響決策的結果。 | `"xdm:decisionRequestId": "0AA00002-0000-1224-c0de-cjf98Csj43"` |
| `xdm:allowDuplicatePropositions` | 此物件是去重複化規則的控制結構。 它包含一系列旗標，指示在特定維度中是否可以建議相同的選項。 若標幟設為true，表示允許重複專案，且此標幟指示的類別中不應移除重複專案。 設為false的標幟表示決定引擎不應跨維度提出相同主張，而應為其中一個子決定挑選下一個最佳選項。 |
| `xdm:allowDuplicatePropositions.xdm:acrossActivities` | 若設為true，系統可能會將相同選項指派給多個決策。 | `"xdm:acrossActivities": true` |
| `xdm:allowDuplicatePropositions.xdm:acrossPlacements` | 若設為true，系統可能會將相同選項指派給多個版位。 | `"xdm:acrossPlacements": true` |
| `xdm:mergePolicy.xdm:id` | 識別用來控管設定檔存取服務傳回資料的合併原則。 如果未在請求中指定，決策管理將不會傳遞任何設定檔存取服務，否則會傳遞呼叫者提供的ID。 | `"xdm:id": "5f3ed32f-eaf1-456c-b0f0-7b338c4cb18a"` |
| `xdm:responseFormat` | 設定回應內容格式的一組標幟。 |
| `xdm:responseFormat.xdm:includeContent` | 布林值，如果設為 `true`，包含回應的內容。 | `"xdm:includeContent": true` |
| `xdm:responseFormat.xdm:includeMetadata` | 用來指定傳回其他中繼資料的物件。 如果此屬性未包含，則 `xdm:id` 和 `repo:etag` 預設會傳回。 | `name` |
| `xdm:responseFormat.xdm:activity` | 此旗標會識別傳回的特定中繼資料資訊 `xdm:activity`. | `name` |
| `xdm:responseFormat.xdm:option` | 此旗標會識別傳回的特定中繼資料資訊 `xdm:option`. | `name`、`characteristics` |
| `xdm:responseFormat.xdm:placement` | 此旗標會識別傳回的特定中繼資料資訊 `xdm:placement`. | `name`、`channel`、`componentType` |

### 响应

成功的回應會傳回有關您主張的資訊，包括其獨一無二的 `xdm:propositionId`.

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
| `xdm:propositionId` | 與XDM DecisionEvent相關聯之主張實體的唯一識別碼。 | `"xdm:propositionId": "5d0ffb5e-dfc6-4280-99b6-0bf3131cb8b8"` |
| `xdm:propositions` | 此物件包含單一決定主張。 可針對決定傳回多個選項。 如果找不到選項，則會傳回決定的遞補優惠。 單一決策主張一律包含 `options` 屬性或 `fallback` 屬性。 當出現時， `options` 屬性不得為空白。 |
| `xdm:propositions.xdm:activity` | 此物件包含決定的唯一識別碼。 | `"xdm:id": "xcore:activity:ffed0123"` |
| `xdm:propositions.xdm:placement` | 此物件包含優惠方案位置的唯一識別碼。 | `"xdm:id": "xcore:placement:ffed0456"` |
| `xdm:propositions.xdm:options` | 此物件包含單一選項，包括其唯一識別碼。 如果存在，此物件不得為空白。 | `xdm:id": "xcore:personalized-option:ccc0111` |
| `xdm:propositions.xdm:options.@type` | 定義元件的型別。 `@type` 充當使用者端的處理合約。 組裝體驗時，撰寫器會尋找具有特定型別的元件。 | `https://ns.adobe.com/experience/offer-management/content-component-imagelink` |
| `xdm:propositions.xdm:content` | 回應內容的格式。 | 回應內容可以是： `text`， `html block`，或 `image link` |
| `xdm:score` | 根據與選項或決定相關聯的排名函式計算出的選項分數。 如果排名功能涉及在排名期間判斷優惠方案的分數，API會傳回此欄位。 | `"xdm:score": 45.65` |
| `xdm:propositions.xdm:fallback` | 此物件包含單一遞補優惠，包括其唯一識別碼。 | `"xdm:id": "xcore:fallback:ccc0222"` |
| `xdm:propositions.xdm:fallback.dc:format` | 資源的實體或數位表現形式。 通常，格式應包含資源的媒體型別。 格式可用於決定顯示或操作資源所需的軟體、硬體或其他裝置。 建議從受控辭彙表中選取值，例如 [網際網路媒體型別](http://www.iana.org/assignments/media-types/) 定義電腦媒體格式。 | `"dc:format": "image/png"` 或 `"image/jpeg"` |
| `xdm:propositions.xdm:fallback.xdm:deliveryURL` | 從內容傳遞網路或服務端點讀取資產的可選URL。 此URL用於從使用者代理程式公開存取資產。 | `https://d37yhxrr0p3l3l.cloudfront.net/0fd0f090-a148-11ea-89e3-f1f2ad52f7e8/urn:aaid:sc:US:a68c86a6-9295-4940-a083-11916b665500/0/40d78a12-f8b6-3f07-8e67-7cb8ae2cc7ec` |
| `ode:createDate` | 建立決定回應訊息的時間。 以紀元時間表示。 | `"ode:createDate": 1566497582038` |

**响应代码**

下表列出回應中可傳回的所有程式碼：

| 代码 | 描述 |
|  ---  |  ---  |
| 200 | 成功. 已針對指定活動做出決定 |
| 400 | 無效的請求引數。 由於語法錯誤，伺服器無法理解該請求。 |
| 403 | 已禁止，許可權不足。 |
| 422 | 無法處理的實體。 請求語法正確，但由於語義錯誤而無法處理。 |
| 429 | 請求太多。 使用者在指定時間內已傳送過多請求。 |
| 500 | 內部伺服器錯誤。 伺服器發生未預期的情況，無法完成要求。 |
| 503 | 由於伺服器超載，服務無法使用。 伺服器目前無法處理要求，因為暫時超載。 |

## 教學課程影片 {#video}

以下影片旨在協助您了解決定管理的元件。

>[!NOTE]
>
>此影片適用於以Adobe Experience Platform為基礎建立的Offer decisioning應用程式服務。 不過，它為在Journey Optimizer環境中使用選件提供了一般指南。

>[!VIDEO](https://video.tv.adobe.com/v/329919/?quality=12)

## 后续步骤 {#next-steps}

依照本API指南，您已使用建立並傳遞優惠方案 [!DNL Decisions] API。 如需詳細資訊，請參閱 [決策管理概觀](../../../offers/get-started/starting-offer-decisioning.md).
