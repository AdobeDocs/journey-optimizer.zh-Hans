---
title: Batch Decisioning API
description: 瞭解如何使用批次決策API為預先定義的決策範圍內的分段設定檔選取最佳優惠。
feature: Offers
topic: Integrations
role: Data Engineer
level: Experienced
exl-id: 1ed01a6b-5e42-47c8-a436-bdb388f50b4e
source-git-commit: 34ab78408981d2b53736b31c94412da06cb860c4
workflow-type: tm+mt
source-wordcount: '750'
ht-degree: 3%

---


# 使用傳遞優惠方案 [!DNL Batch Decisioning] API {#deliver-offers-batch}

此 [!DNL Batch Decisioning] API可讓組織在一次呼叫中對特定區段中的所有設定檔使用決策功能。 區段中每個設定檔的選件內容都會放在Adobe Experience Platform資料集中，可用於自訂批次工作流程。

使用 [!DNL Batch Decisioning] api後，您可以在資料集中填入決策範圍之Adobe Experience Platform區段中所有設定檔的最佳選件。 例如，組織可能想要執行 [!DNL Batch Decisioning] 以便他們將優惠方案傳送給訊息傳遞廠商。 然後，這些選件會用作傳送以進行批次訊息傳送給相同使用者區段的內容。

為此，組織將：

* 執行 [!DNL Batch Decisioning] API，其中包含兩個請求：

   1. A **批次POST請求** 啟動工作負載以批次處理選件選擇。

   2. A **批次GET請求** 以取得批次工作負載狀態。

* 將資料集匯出至訊息傳遞供應商API。

<!-- (Refer to the [export jobs endpoint documentation](https://experienceleague.adobe.com/docs/experience-platform/segmentation/api/export-jobs.html?lang=en) to learn more about exporting segments.) -->

>[!NOTE]
>
>也可以使用Journey Optimizer介面執行批次決策。 如需詳細資訊，請參閱 [本節](../../batch-delivery.md)，提供在使用批次決定時要考慮的全球先決條件和限制的相關資訊。

* **每個資料集執行中的批次工作數目**：每個資料集一次最多可以執行五個批次工作。 具有相同輸出資料集的任何其他批次請求都會新增至佇列。 前一個工作執行完畢後，系統會擷取已排入佇列的工作進行處理。
* **頻率限定**：批次會以一天一次的設定檔快照執行。 此 [!DNL Batch Decisioning] API會限制頻率，並一律從最近的快照載入設定檔。

## 快速入门 {#getting-started}

使用此API之前，請務必完成以下必要步驟。

### 準備決定 {#prepare-decision}

若要準備一或多個決定，請確定您已建立資料集、區段和決定。 這些先決條件詳見 [本節](../../batch-delivery.md).

### API需求 {#api-requirements}

全部 [!DNL Batch Decisioning] 除了在下列標題外，請求還需要下列標題： [Decision Management API開發人員指南](../getting-started.md)：

* `Content-Type`： `application/json`
* `x-request-id`：識別請求的唯一字串。
* `x-sandbox-name`：沙箱名稱。
* `x-sandbox-id`：沙箱ID。

## 開始批次處理 {#start-a-batch-process}

若要啟動工作負載以批次處理決策，請向以下發出POST請求： `/workloads/decisions` 端點。

>[!NOTE]
>
>有關批次工作處理時間的詳細資訊，請參閱 [本節](../../batch-delivery.md).

**API格式**

```https
POST {ENDPOINT_PATH}/{CONTAINER_ID}/workloads/decisions
```

| 参数 | 描述 | 示例 |
| --------- | ----------- | ------- |
| `{ENDPOINT_PATH}` | 存放庫API的端點路徑。 | `https://platform.adobe.io/data/core/ode` |
| `{CONTAINER_ID}` | 決策所在的容器。 | `e0bd8463-0913-4ca1-bd84-6309134ca1f6` |

**请求**

```shell
curl -X POST 'https://platform.adobe.io/data/core/ode/0948b1c5-fff8-3b76-ba17-909c6b93b5a2/workloads/decisions' \
-H 'x-request-id: f671a589-eb7b-432f-b6b9-23d5b796b4dc' \
-H 'Content-Type: application/json' \
-H 'x-api-key: {API_KEY}' \
-H 'x-gw-ims-org-id: {IMS_ORG}' \
-H 'x-sandbox-name: {SANDBOX_NAME}' \
-H 'x-sandbox-id: {SANDBOX_ID}' \
-H 'Authorization: Bearer {ACCESS_TOKEN}' \
-d '{
  "xdm:segmentIds": [
    "609028e4-e66c-4776-b0d9-c782887e2273"
  ],
  "xdm:dataSetId": "6196b4a1a63bd118dafe093c",
  "xdm:propositionRequests": [
        {
            "xdm:activityId": "xcore:offer-activity:1410cdcda196707b",
            "xdm:placementId": "xcore:offer-placement:1410c4117306488a",
            "xdm:itemCount": 1
        }
  ],
  "xdm:includeContent": false
}'
```

| 属性 | 描述 | 示例 |
| -------- | ----------- | ------- |
| `xdm:segmentIds` | 值是包含區段唯一識別碼的陣列。 它只能包含一個值。 | `609028e4-e66c-4776-b0d9-c782887e2273` |
| `xdm:dataSetId` | 可寫入決定事件的輸出資料集。 | `6196b4a1a63bd118dafe093c` |
| `xdm:propositionRequests` | 包含 `placementId` 和 `activityId` |  |
| `xdm:activityId` | 決定的唯一識別碼。 | `xcore:offer-activity:1410cdcda196707b` |
| `xdm:placementId` | 唯一位置識別碼。 | `xcore:offer-placement:1410c4117306488a` |
| `xdm:itemCount` | 此選擇性欄位會顯示專案數量，例如為決定範圍要求的選項。 依預設，API會針對每個範圍傳回一個選項，但您可以指定此欄位來明確要求更多選項。 每個範圍最多可請求30個選項，最少為1個。 | `1` |
| `xdm:includeContent` | 此為選擇性欄位，且 `false` 依預設。 若 `true`，選件內容會包含在資料集的決定事件中。 | `false` |

請參閱 [決策管理檔案](../../get-started/starting-offer-decisioning.md) 主要概念和屬性的概述。

**响应**

```json
{
    "@id": "47efef25-4bcf-404f-96e2-67c4f784a1f5",
    "xdm:imsOrgId": "9GTO98D5F@AdobeOrg",
    "xdm:containerId": "0948b1c5-fff8-3b76-ba17-909c6b93b5a2",
    "ode:createDate": 1648078924834,
    "ode:status": "QUEUED"
}
```

| 属性 | 描述 | 示例 |
| -------- | ----------- | ------- |
| `@id` | 決策管理產生的UUID，可識別單一工作負載。 | `5d0ffb5e-dfc6-4280-99b6-0bf3131cb8b8` |
| `xdm:imsOrgId` | 組織識別碼。 | `9GTO98D5F@AdobeOrg` |
| `xdm:containerId` | 容器ID。 | `0948b1c5-fff8-3b76-ba17-909c6b93b5a2` |
| `ode:createDate` | 決定工作負載請求的建立時間。 | `1648078924834` |
| `ode:status` | 工作負荷的狀態。 | `ode:status: "QUEUED"` |

## 擷取批次決定的資訊 {#retrieve-information-on-a-batch-decision}

若要擷取特定決定的相關資訊，請向以下網站提出GET請求： `/workloads/decisions` 端點，同時提供對應的工作負載ID值給您的決定。

**API格式**

```https
GET  {ENDPOINT_PATH}/{CONTAINER_ID}/workloads/decisions/{WORKLOAD_ID}
```

| 参数 | 描述 | 示例 |
| --------- | ----------- | ------- |
| `{ENDPOINT_PATH}` | 存放庫API的端點路徑。 | `https://platform.adobe.io/data/core/ode` |
| `{CONTAINER_ID}` | 決策所在的容器。 | `e0bd8463-0913-4ca1-bd84-6309134ca1f6` |
| `{WORKLOAD_ID}` | 決策管理產生的UUID，可識別單一工作負載。 | `47efef25-4bcf-404f-96e2-67c4f784a1f5` |

**请求**

```shell
curl -X GET 'https://platform.adobe.io/data/core/ode/0948b1c5-fff8-3b76-ba17-909c6b93b5a2/workloads/decisions/f395ab1f-dfaf-48d4-84c9-199ad6354591' \
-H 'x-request-id: 7832a42a-d4e5-413b-98e8-e49bef056436' \
-H 'Content-Type: application/json' \
-H 'x-api-key: {API_KEY}' \
-H 'x-gw-ims-org-id: {IMS_ORG}' \
-H 'x-sandbox-name: {SANDBOX_NAME}' \
-H'x-sandbox-id: {SANDBOX_ID}' \
-H 'Authorization: Bearer {ACCESS_TOKEN}'
```

**响应**

```json
{
    "@id": "f395ab1f-dfaf-48d4-84c9-199ad6354591",
    "xdm:imsOrgId": "{IMS_ORG}",
    "xdm:containerId": "0948b1c5-fff8-3b76-ba17-909c6b93b5a2",
    "ode:createDate": 1648076994405,
    "ode:status": "COMPLETED"
}
```

| 属性 | 描述 | 示例 |
| -------- | ----------- | ------- |
| `@id` | 決策管理產生的UUID，可識別單一工作負載。 | `5d0ffb5e-dfc6-4280-99b6-0bf3131cb8b8` |
| `xdm:imsOrgId` | 組織ID | `9GTO98D5F@AdobeOrg` |
| `xdm:containerId` | 容器ID | `0948b1c5-fff8-3b76-ba17-909c6b93b5a2` |
| `ode:createDate` | 決定工作負載請求的建立時間。 | `1648076994405` |
| `ode:status` | 工作負荷的狀態從「已排入佇列」開始，並變更為「正在處理」、「正在擷取」、「已完成」或「錯誤」。 | `ode:status: "COMPLETED"` |
| `ode:statusDetail` | 如果狀態為「PROCESSING」或「INGING」，這會顯示更多詳細資料，例如sparkJobId和batchID。 如果狀態為「ERROR」，則顯示錯誤詳細資料。 |  |

## 后续步骤 {#next-steps}

依照本API指南，您已使用[！DNL]檢查工作負荷狀態和傳送的優惠 [!DNL Batch Decisioning]] API。 如需詳細資訊，請參閱 [決策管理概觀](../../get-started/starting-offer-decisioning.md).
