---
title: Batch Decisioning API
description: 了解如何使用Batch Decisioning API在预定义的决策范围内为受众配置文件选择最佳优惠。
feature: Decision Management, API
topic: Integrations
role: Data Engineer
level: Experienced
exl-id: 1ed01a6b-5e42-47c8-a436-bdb388f50b4e
source-git-commit: bab4cd8065830e36fd6188d3ebf0bd62a63947f3
workflow-type: tm+mt
source-wordcount: '729'
ht-degree: 3%

---


# 使用交付优惠 [!DNL Batch Decisioning] API {#deliver-offers-batch}

此 [!DNL Batch Decisioning] API允许组织在一次调用中对给定受众中的所有用户档案使用决策功能。 受众中每个用户档案的选件内容都放在Adobe Experience Platform数据集中，可用于自定义批量工作流。

使用 [!DNL Batch Decisioning] API之后，您可以在数据集中填充用于决策范围的Adobe Experience Platform受众中所有用户档案的最佳选件。 例如，组织可能希望运行 [!DNL Batch Decisioning] 以便他们向消息投放供应商发送选件。 这些选件随后将用作发送出去、以批量消息方式发送给相同用户受众的内容。

为此，本组织将：

* 运行 [!DNL Batch Decisioning] API，其中包含两个请求：

   1. A **批量POST请求** 启动工作负载以批处理选件选择。

   2. A **批量GET请求** 获取批处理工作负载状态。

* 将数据集导出到消息投放供应商API。

<!-- (Refer to the [export jobs endpoint documentation](https://experienceleague.adobe.com/docs/experience-platform/segmentation/api/export-jobs.html) to learn more about exporting audiences.) -->

>[!NOTE]
>
>也可以使用Journey Optimizer界面执行批量决策。 有关更多信息，请参阅 [本节](../../batch-delivery.md)，其中提供了在使用批量决策时要考虑的全局先决条件和限制的信息。

* **每个数据集运行的批处理作业数**：每个数据集一次最多可以运行五个批处理作业。 具有相同输出数据集的任何其他批处理请求都将添加到队列中。 一旦前一个作业运行完成，系统会选取已排队作业进行处理。
* **频率封顶**：批处理每天运行一次的配置文件快照。 此 [!DNL Batch Decisioning] API会限制频率并始终从最新快照加载配置文件。

## 快速入门 {#getting-started}

在使用此API之前，请确保完成以下先决步骤。

### 准备决策 {#prepare-decision}

要准备一个或多个决策，请确保已创建数据集、受众和决策。 有关这些先决条件的详情，请参见 [本节](../../batch-delivery.md).

### API要求 {#api-requirements}

全部 [!DNL Batch Decisioning] 除了中提到的标头外，请求还需要以下标头 [Decision Management API开发人员指南](../getting-started.md)：

* `Content-Type`：`application/json`
* `x-request-id`：标识请求的唯一字符串。
* `x-sandbox-name`：沙盒名称。

## 启动批处理 {#start-a-batch-process}

POST要启动工作负载以批量处理决策，请向 `/workloads/decisions` 端点。

>[!NOTE]
>
>有关批处理作业处理时间的详细信息，请参阅 [本节](../../batch-delivery.md).

**API格式**

```https
POST {ENDPOINT_PATH}/workloads/decisions
```

| 参数 | 描述 | 示例 |
| --------- | ----------- | ------- |
| `{ENDPOINT_PATH}` | 存储库API的端点路径。 | `https://platform.adobe.io/data/core/dwm` |

**请求**

```shell
curl -X POST 'https://platform.adobe.io/data/core/dwm/workloads/decisions' \
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
| `xdm:segmentIds` | 该值是一个包含受众唯一标识符的数组。 它只能包含一个值。 | `609028e4-e66c-4776-b0d9-c782887e2273` |
| `xdm:dataSetId` | 可写入决策事件的输出数据集。 | `6196b4a1a63bd118dafe093c` |
| `xdm:propositionRequests` | 包含 `placementId` 和 `activityId` |  |
| `xdm:activityId` | 决策的唯一标识符。 | `xcore:offer-activity:1410cdcda196707b` |
| `xdm:placementId` | 唯一投放位置标识符。 | `xcore:offer-placement:1410c4117306488a` |
| `xdm:itemCount` | 这是一个可选字段，显示决策范围请求的选项等项目的数量。 默认情况下，API会为每个范围返回一个选项，但您可以通过指定此字段来明确要求提供更多选项。 每个范围可以请求至少1个和最多30个选项。 | `1` |
| `xdm:includeContent` | 这是一个可选字段，它是 `false` 默认情况下。 如果 `true`时，选件内容包含在数据集的决策事件中。 | `false` |

请参阅 [决策管理文档](../../get-started/starting-offer-decisioning.md) 有关主要概念和属性的概述。

**响应**

```json
{
    "@id": "47efef25-4bcf-404f-96e2-67c4f784a1f5",
    "xdm:imsOrgId": "9GTO98D5F@AdobeOrg",
    "ode:createDate": 1648078924834,
    "ode:status": "QUEUED"
}
```

| 属性 | 描述 | 示例 |
| -------- | ----------- | ------- |
| `@id` | 决策管理生成的UUID，用于标识单个工作负载。 | `5d0ffb5e-dfc6-4280-99b6-0bf3131cb8b8` |
| `xdm:imsOrgId` | 组织ID。 | `9GTO98D5F@AdobeOrg` |
| `ode:createDate` | 创建决策工作负载请求的时间。 | `1648078924834` |
| `ode:status` | 工作负载的状态。 | `ode:status: "QUEUED"` |

## 检索有关批次决策的信息 {#retrieve-information-on-a-batch-decision}

GET要检索有关特定决策的信息，请向 `/workloads/decisions` 端点，同时为您的决策提供相应的工作负载ID值。

**API格式**

```https
GET {ENDPOINT_PATH}/workloads/decisions/{WORKLOAD_ID}
```

| 参数 | 描述 | 示例 |
| --------- | ----------- | ------- |
| `{ENDPOINT_PATH}` | 存储库API的端点路径。 | `https://platform.adobe.io/data/core/dwm` |
| `{WORKLOAD_ID}` | 决策管理生成的UUID，用于标识单个工作负载。 | `47efef25-4bcf-404f-96e2-67c4f784a1f5` |

**请求**

```shell
curl -X GET 'https://platform.adobe.io/data/core/dwm/workloads/decisions/f395ab1f-dfaf-48d4-84c9-199ad6354591' \
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
    "ode:createDate": 1648076994405,
    "ode:status": "COMPLETED"
}
```

| 属性 | 描述 | 示例 |
| -------- | ----------- | ------- |
| `@id` | 决策管理生成的UUID，用于标识单个工作负载。 | `5d0ffb5e-dfc6-4280-99b6-0bf3131cb8b8` |
| `xdm:imsOrgId` | 组织ID | `9GTO98D5F@AdobeOrg` |
| `ode:createDate` | 创建决策工作负载请求的时间。 | `1648076994405` |
| `ode:status` | 工作负载的状态以“已排队”开始，并更改为“正在处理”、“正在摄取”、“已完成”或“错误”。 | `ode:status: "COMPLETED"` |
| `ode:statusDetail` | 这将显示更多详细信息，例如，如果状态为“PROCESSING”或“INGESTING”，则显示sparkJobId和batchID。 如果状态为“ERROR”，则显示错误详细信息。 |  |

## 后续步骤 {#next-steps}

通过遵循此API指南，您已使用[！DNL]检查工作负荷状态和提供的选件 [!DNL Batch Decisioning]] API。 欲了解更多信息，请参见 [决策管理概述](../../get-started/starting-offer-decisioning.md).