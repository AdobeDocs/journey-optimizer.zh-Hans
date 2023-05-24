---
title: 快速入门
description: 瞭解如何開始使用Offer Library API，使用決策引擎執行關鍵操作。
feature: Offers
topic: Integrations
role: User
level: Intermediate
exl-id: 773bee50-849f-4b07-9423-67de5279ad28
source-git-commit: e7431d1b69e460471b01439c9bd2577fd69944ed
workflow-type: tm+mt
source-wordcount: '565'
ht-degree: 6%

---

# Decision Management API開發人員指南 {#decision-management-api-developer-guide}

本開發人員指南提供步驟，協助您開始使用 [!DNL Offer Library] API。 接著，指南會提供範例API呼叫，以利使用決策引擎執行關鍵作業。

➡️ [在本影片中進一步了解決定管理的元件](#video)

## 先决条件 {#prerequisites}

本指南需要您實際瞭解下列Adobe Experience Platform元件：

* [[!DNL Experience Data Model (XDM) System]](https://experienceleague.adobe.com/docs/experience-platform/xdm/home.html?lang=zh-Hans){target="_blank"}：作為依據的標準化架構 [!DNL Experience Platform] 組織客戶體驗資料。
   * [結構描述組合基本概念](https://experienceleague.adobe.com/docs/experience-platform/xdm/schema/composition.html?lang=zh-Hans){target="_blank"}：瞭解XDM結構描述的基本建置組塊。
* [決定管理](../../../using/offers/get-started/starting-offer-decisioning.md)：說明用於一般體驗決策，尤其是決策管理的概念和元件。 說明用於選擇在客戶體驗期間呈現的最佳選項的策略。
* [[!DNL Profile Query Language (PQL)]](https://experienceleague.adobe.com/docs/experience-platform/segmentation/pql/overview.html){target="_blank"}： PQL是一種強大的語言，可透過XDM執行個體寫入運算式。 PQL可用來定義決定規則。

## 讀取範例API呼叫 {#reading-sample-api-calls}

本指南提供範例API呼叫，示範如何格式化您的請求。 這些包括路徑、必要的標頭，以及正確格式化的請求裝載。 此外，也提供API回應中傳回的範例JSON。 如需檔案中用於範例API呼叫的慣例相關資訊，請參閱以下章節： [如何讀取範例API呼叫](https://experienceleague.adobe.com/docs/experience-platform/landing/troubleshooting.html#how-do-i-format-an-api-request){target="_blank"} 在 [!DNL Experience Platform] 疑難排解指南。

## 收集必要標題的值 {#gather-values-for-required-headers}

為了呼叫 [!DNL Adobe Experience Platform] API，您必須先完成 [驗證教學課程](https://experienceleague.adobe.com/docs/experience-platform/landing/platform-apis/api-authentication.html){target="_blank"}. 完成驗證教學課程後，會在所有標題中提供每個必要標題的值 [!DNL Experience Platform] API呼叫，如下所示：

* `Authorization: Bearer {ACCESS_TOKEN}`
* `x-api-key: {API_KEY}`
* `x-gw-ims-org-id: {IMS_ORG}`

包含裝載(POST、PUT、PATCH)的所有請求都需要額外的標頭：

* `Content-Type: application/json`

## 管理對容器的存取 {#manage-access-to-container}

容器是一種隔離機制，可將不同的關注點分開。 容器ID是所有存放庫API的第一個路徑元素。 所有決策物件都位於容器內。

管理員可以將類似的主體、資源和存取許可權分組到設定檔中。 這能減輕管理負擔，並由 [Adobe Admin Console](https://adminconsole.adobe.com/). 您必須是組織中Adobe Experience Platform的產品管理員，才能建立設定檔並將使用者指派給設定檔。 只要在一次性步驟中建立符合特定許可權的產品設定檔，然後只需將使用者新增到這些設定檔就足夠了。 設定檔會作為已授與許可權的群組，而該群組中的每個實際使用者或技術使用者都會繼承這些許可權。

授予管理員許可權，您可以透過授予或撤銷使用者許可權 [Adobe Admin Console](https://adminconsole.adobe.com/){target="_blank"}. For more information, see the [Access control overview](https://experienceleague.adobe.com/docs/experience-platform/access-control/home.html?lang=zh-Hans){target="_blank"}.

### 使用者和整合功能可存取的清單容器 {#list-containers-accessible-to-users-and-integrations}

**API格式**

```http
GET /{ENDPOINT_PATH}?product={PRODUCT_CONTEXT}&property={PROPERTY}==decisioning
```

| 参数 | 描述 | 示例 |
| --------- | ----------- | ------- |
| `{ENDPOINT_PATH}` | 存放庫API的端點路徑。 | `https://platform.adobe.io/data/core/xcore/` |
| `{PRODUCT_CONTEXT}` | 依照容器與產品前後關聯的關聯來篩選容器清單。 | `acp` |
| `{PROPERTY}` | 篩選傳回的容器型別。 | `_instance.containerType==decisioning` |

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

成功的回應會傳回與決策管理容器相關的資訊。 這包括 `instanceId` 屬性，其值是您的容器ID。

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

本檔案說明呼叫「 」所需的必要條件知識。 [!DNL Offer Library] API，包括取得您的容器ID。 您現在可以繼續本開發人員指南中提供的範例呼叫，並依照其指示操作。
<!--
>[!NOTE]
>
> The In-app messaging channel in Adobe Journey Optimizer uses decision management objects. If your organization uses the in-app messaging channel, then API list requests for objects will include objects created by the in-app messaging service and can be ignored for decision management use cases. Objects created for in-app messages will have `createdBy = “Mobile_Sheliak”`.
-->

## 操作方法视频 {#video}

以下影片旨在協助您了解決定管理的元件。

>[!VIDEO](https://video.tv.adobe.com/v/329919?quality=12)

