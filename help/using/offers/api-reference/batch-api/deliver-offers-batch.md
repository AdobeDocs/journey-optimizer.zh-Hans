---
title: 批量决策API
description: 了解如何使用Batch Decisioning API为预定义决策范围内的分段用户档案选择最佳选件。
feature: Offers
topic: Integrations
role: Data Engineer
level: Experienced
exl-id: 1ed01a6b-5e42-47c8-a436-bdb388f50b4e
source-git-commit: 817a77c5717804ccae36db3dd8920008ab127684
workflow-type: tm+mt
source-wordcount: '813'
ht-degree: 2%

---

# 使用 [!DNL Batch Decisioning] API

的 [!DNL Batch Decisioning] API允许组织在一次调用中对给定区段中的所有用户档案使用offer decisioning功能。 区段中每个用户档案的选件内容都放置在Adobe Experience Platform数据集中，该数据集可用于自定义批量工作流。

使用 [!DNL Batch Decisioning] API中，您可以使用决策范围内Adobe Experience Platform区段中所有用户档案的最佳选件填充数据集。 例如，组织可能希望运行批量决策，以便他们能够向消息投放供应商发送选件。 然后，这些选件将用作发出的内容，以便将批量消息交付到同一用户区段。

为此，组织将：

* 运行 [!DNL Batch Decisioning] API，其中包含两个请求：

   1. A **批量GET请求** 以获取批处理工作负载状态。

   2. A **批量POST请求** 启动工作量以批量处理选件选择。

* 将数据集导出到消息传递供应商API。

<!-- (Refer to the [export jobs endpoint documentation](https://experienceleague.adobe.com/docs/experience-platform/segmentation/api/export-jobs.html?lang=en) to learn more about exporting segments.) -->

## 快速入门 {#getting-started}

使用此API之前，请确保完成以下先决条件步骤。

### 准备决策

请按照以下步骤准备决策：

* 要导出决策结果，请使用“ODE决策事件”架构创建数据集。

* 创建一个应进行评估并更新的平台区段。 请参阅 [分段文档](http://www.adobe.com/go/segmentation-overview-en) 以了解有关如何更新区段成员资格评估的更多信息。

* 在Adobe Journey Optimizer中创建决策（其决策范围包含决策ID和版面ID）。 请参阅 [定义决策范围一节](../../offer-activities/create-offer-activities.md) 指南的“创建决策”以了解更多信息。

### API要求

所有批量决策请求都需要以下额外的标头：

* `Content-Type`: `application/json`
* `x-request-id`:标识请求的唯一字符串。
* `x-sandbox-name`:沙盒名称。
* `x-sandbox-id`:沙盒ID。

## 检索有关批量决策的信息 {#retrieve-information-on-a-batch-decision}

要检索有关特定决策的信息，请向 `/workloads/decisions` 端点，同时为您的决策提供相应的工作负载ID值。

**API格式**

```https
GET  {ENDPOINT_PATH}/{CONTAINER_ID}/workloads/decisions/{WORKLOAD_ID}
```

| 参数 | 描述 | 示例 |
| --------- | ----------- | ------- |
| `{ENDPOINT_PATH}` | 存储库API的端点路径。 | `https://platform.adobe.io/data/core/ode` |
| `{CONTAINER_ID}` | 决策所在的容器。 | `e0bd8463-0913-4ca1-bd84-6309134ca1f6` |
| `{WORKLOAD_ID}` | 由Offer decisioning生成的UUID，用于标识单个工作负载。 | `47efef25-4bcf-404f-96e2-67c4f784a1f5` |

**请求**

```shell
curl -X GET 'https://platform.adobe.io/data/core/ode/0948b1c5-fff8-3b76-ba17-909c6b93b5a2/workloads/decisions/f395ab1f-dfaf-48d4-84c9-199ad6354591' \
-H 'x-request-id: 7832a42a-d4e5-413b-98e8-e49bef056436' \
-H 'Content-Type: application/json' \
-H 'x-api-key: {API_KEY}' \
-H 'x-gw-ims-org-id: {IMS_ORG}' \
-H 'x-sandbox-name: {SANDBOX_NAME}' \
-H'x-sandbox-id: {SANDBOX_ID}' \
-H 'Authorization: {ACCESS_TOKEN}'
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
| `@id` | 由Offer decisioning生成的UUID，用于标识单个工作负载。 | `5d0ffb5e-dfc6-4280-99b6-0bf3131cb8b8` |
| `xdm:imsOrgId` | IMS组织ID | `9GTO98D5F@AdobeOrg` |
| `xdm:containerId` | 容器ID | `0948b1c5-fff8-3b76-ba17-909c6b93b5a2` |
| `ode:createDate` | 创建决策工作量请求的时间。 | `1648076994405` |
| `ode:status` | 工作负载的状态以“QUEUED”开头，并更改为“PROCESSING”、“INGESTING”、“COMPLETED”或“ERROR”。 | `ode:status: "COMPLETED"` |
| `ode:statusDetail` | 如果状态为“正在处理”或“正在摄取”，则会显示更多详细信息，如sparkJobId和batchID。 如果状态为“ERROR”，则会显示错误详细信息。 |  |

## 启动批处理 {#start-a-batch-process}

要启动工作负载以批量处理决策，请向 `/workloads/decisions` 端点。

**API格式**

```https
POST {ENDPOINT_PATH}/{CONTAINER_ID}/workloads/decisions
```

| 参数 | 描述 | 示例 |
| --------- | ----------- | ------- |
| `{ENDPOINT_PATH}` | 存储库API的端点路径。 | `https://platform.adobe.io/data/core/ode` |
| `{CONTAINER_ID}` | 决策所在的容器。 | `e0bd8463-0913-4ca1-bd84-6309134ca1f6` |

**请求**

```shell
curl -X POST 'https://platform.adobe.io/data/core/ode/0948b1c5-fff8-3b76-ba17-909c6b93b5a2/workloads/decisions' \
-H 'x-request-id: f671a589-eb7b-432f-b6b9-23d5b796b4dc' \
-H 'Content-Type: application/json' \
-H 'x-api-key: {API_KEY}' \
-H 'x-gw-ims-org-id: {IMS_ORG}' \
-H 'x-sandbox-name: {SANDBOX_NAME}' \
-H 'x-sandbox-id: {SANDBOX_ID}' \
-H 'Authorization: {ACCESS_TOKEN}' \
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
| `xdm:segmentIds` | 区段的唯一标识符。 它只能包含一个值。 | `609028e4-e66c-4776-b0d9-c782887e2273` |
| `xdm:dataSetId` | 可将决策事件写入的输出数据集。 | `6196b4a1a63bd118dafe093c` |
| `xdm:propositionRequests` | 包含placementId和activityId的包装器 |  |
| `xdm:activityId` | 决策的唯一标识符。 | `xcore:offer-activity:1410cdcda196707b` |
| `xdm:placementId` | 唯一版面标识符。 | `xcore:offer-placement:1410c4117306488a` |
| `xdm:itemCount` | 这是一个可选字段，其中显示了为决策范围请求的选项等项目数。 默认情况下，API会为每个范围返回一个选项，但您可以通过指定此字段明确地请求更多选项。 每个范围最少可请求1个选项，最多可请求30个选项。 | `1` |
| `xdm:includeContent` | 这是一个可选字段，为 `false` 默认情况下。 如果 `true`，则选件内容会包含在数据集的决策事件中。 | `false` |

请参阅 [决策管理文档](../../get-started/starting-offer-decisioning.md) 以了解主要概念的概述。

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
| `@id` | 由Offer decisioning生成的UUID，用于标识单个工作负载。 | `5d0ffb5e-dfc6-4280-99b6-0bf3131cb8b8` |
| `xdm:imsOrgId` | 您的IMS组织的ID。 | `9GTO98D5F@AdobeOrg` |
| `xdm:containerId` | 您的容器ID。 | `0948b1c5-fff8-3b76-ba17-909c6b93b5a2` |
| `ode:createDate` | 创建决策工作量请求的时间。 | `1648078924834` |
| `ode:status` | 工作负载的状态。 | `ode:status: "QUEUED"` |

## 服务级别 {#service-levels}

每个批量决策的端到端时间是指从创建工作量到输出数据集中可用决策结果的持续时间。 POST请求有效负载中的区段大小是影响端到端批量决策时间的主要因素。 以下是针对不同区段大小的一些观察：

* 区段大小&lt;= 10K:6分钟
* 区段大小&lt;= 1M:10分钟
* 区段大小&lt;= 15M:75分钟

## 限制 {#limitations}

以下限制 [!DNL Batch Decisioning] API:

* **单批作业**:当前，每个数据集一次只能运行一个批处理作业。 任何其他请求都将通过HTTP 429（请求过多）做出响应。
* **频率封顶**:每天发生一次的配置文件快照的批处理运行。 的 [!DNL Batch Decisioning] API会限制频率，并始终从最新快照加载用户档案。

## 后续步骤 {#next-steps}

按照本API指南，您已检查工作负载状态，并使用 [!DNL Batch Decisioning] API。 有关更多信息，请参阅 [决策管理概述](../../get-started/starting-offer-decisioning.md).
