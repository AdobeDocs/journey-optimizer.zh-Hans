---
title: Decisioning迁移API
description: 了解如何使用Decisioning迁移服务API在具有自动依赖项解析和回滚支持的沙盒之间迁移决策管理对象。
feature: Decisioning
topic: Integrations
role: Developer
level: Experienced
exl-id: 3ec084ca-af9e-4b5e-b66f-ec390328a9d6
source-git-commit: aca4e62faa7aa09a60eef661c0732a8b0b1fa36e
workflow-type: tm+mt
source-wordcount: '1105'
ht-degree: 3%

---

# Decisioning迁移API {#decisioning-migration-api}

通过Decisioning迁移服务API，可将决策管理对象从一个沙盒迁移到另一个沙盒。 迁移过程以异步工作流运行，包括依赖关系分析、执行和可选回滚功能。

此API允许您在环境<!--(e.g., from development to staging, or staging to production) -->之间无缝转换决策内容，同时保持数据完整性和关系。

要了解与决策管理相比，决策的优点和功能，请参阅[此页面](migrate-to-decisioning.md)。

## 功能 {#capabilities}

Decisioning迁移服务API提供以下功能：

* **依赖关系分析** — 识别源沙盒和目标沙盒之间所有必需的依赖关系，包括属性、区段和数据集要求。
* **灵活的迁移范围** — 根据您的需求，在沙盒、选件或决策级别运行迁移。
* **回滚支持** — 如果在验证期间发现问题，则还原已完成的迁移。

## 先决条件 {#prerequisites}

### 所需的权限 {#permissions}

要使用迁移API，您需要在源沙盒和目标沙盒中具有适当的权限：

**Source沙盒** — 对决策管理对象的读取访问权限

**Target沙盒** — 创建和编辑对Decisioning对象的访问权限

典型权限包括：

* 管理/查看决策
* 管理/查看决策
* 管理产品建议
* 管理排名策略
* 管理营销活动（如果迁移与营销活动相关的构件）
* 管理/查看数据流（如果创建数据流）
* 管理/查看架构

>[!NOTE]
>
>在[此部分](gs-experience-decisioning.md#steps)中了解如何分配Decisioning权限。 有关权限的完整列表，请参阅[内置权限](../administration/ootb-permissions.md#ootb-permissions)页面。

### 准备您的目标沙盒 {#target-sandbox-preparation}

运行迁移之前，请确保已正确配置Target沙盒：

* **属性** — 验证目标沙盒中是否存在所需的配置文件属性和上下文属性，或为其准备映射。
* **区段** — 确保目标沙盒中存在所需的区段，或计划使用命名空间和ID来映射它们。
* **数据集** — 标识要用于迁移的数据集名称(`dependency.datasetName`)。
* **数据流** — 决定迁移是否应创建数据流(`createDataStream`)。

有关沙盒管理的详细信息，请参阅[使用和分配沙盒](../administration/sandboxes.md)。

## API 基础知识 {#api-basics}

### 基本 URL {#base-url}

使用以下基本URL：

* **生产**： `https://decisioning-migration.adobe.io`
  <!--* **Staging**: `https://decisioning-migration-stage.adobe.io`-->

### 身份验证 {#authentication}

所有API请求都需要以下标头：

* `Authorization: Bearer <IMS_ACCESS_TOKEN>`
* `x-gw-ims-org-id: <IMS_ORG_ID>`
* `Content-Type: application/json`

有关设置身份验证的详细说明，请参阅[Journey Optimizer身份验证指南](https://developer.adobe.com/journey-optimizer-apis/references/authentication/){target="_blank"}。

### 工作流模型 {#workflow-model}

每个API调用都会创建或检索工作流资源。 工作流是异步操作，用于跟踪迁移任务的进度和结果。

工作流具有以下属性：

* `id` — 唯一工作流标识符(UUID)
* `status` — 当前工作流状态：`New`、`Running`、`Completed`或`Failed`
* `result` — 完成时输出工作流（包括迁移结果和警告）
* `errors` — 失败时的结构化错误详细信息
* `_links.self` — 用于检索状态的工作流URL
  <!--* `_etag` - Version identifier used for delete operations (service users only)-->

## 迁移工作流 {#migration-workflow}

迁移过程包括两个主要步骤：分析依赖项和执行迁移。 请按照以下步骤操作，以确保成功迁移。

### 步骤1：分析依赖关系 {#analyze-dependencies}

在迁移之前，请使用依赖关系工作流确定需要在目标沙盒中从Decision management映射到Decisioning的内容。 此分析可帮助您了解对象之间的关系并准备必要的映射。

#### 创建依赖关系工作流 {#create-dependency-workflow}

使用以下API调用创建依赖关系分析工作流。

**API格式**

```http
POST /workflows/generate-dependencies
```

**沙盒级依赖项（建议首先使用）**

从沙盒级别分析开始，全面了解所有依赖关系：

```shell
curl --request POST \
  --url "https://decisioning-migration.adobe.io/workflows/generate-dependencies" \
  --header "Authorization: Bearer <IMS_ACCESS_TOKEN>" \
  --header "x-gw-ims-org-id: <IMS_ORG_ID>" \
  --header "Content-Type: application/json" \
  --data '{
    "imsOrgId": "<IMS_ORG_ID>",
    "sourceSandboxDetails": { "sandboxName": "<SOURCE_SANDBOX_NAME>" },
    "targetSandboxDetails": { "sandboxName": "<TARGET_SANDBOX_NAME>" },
    "requestLevel": "sandbox"
  }'
```

**选件级别的依赖项**

要仅分析特定选件的依赖项，请设置`requestLevel: "offer"`并提供具有要分析的选件ID的`offersList`数组。

**决策级依赖关系**

要仅分析特定决策的依赖关系，请设置`requestLevel: "decision"`并提供`decisionsList`数组以及要分析的决策ID。

#### 检查依赖项工作流状态 {#poll-dependency-status}

轮询依赖关系工作流以检查分析何时完成。

**API格式**

```http
GET /workflows/generate-dependencies/{id}
```

**请求**

```shell
curl --request GET \
  --url "https://decisioning-migration.adobe.io/workflows/generate-dependencies/<WORKFLOW_ID>" \
  --header "Authorization: Bearer <IMS_ACCESS_TOKEN>" \
  --header "x-gw-ims-org-id: <IMS_ORG_ID>"
```

当`status`字段显示`Completed`时，依赖关系分析已准备就绪。 使用工作流输出构建迁移依赖项映射：

* **profileAttributes** — 将源配置文件属性映射到目标配置文件属性
* **contextAttributes** — 将源上下文属性映射到目标上下文属性
* **区段** — 将源区段键映射到目标区段标识符(`{namespace, id}`)
* **datasetName** — 为迁移指定目标数据集名称

### 步骤2：执行迁移 {#execute-migration}

分析依赖项并准备映射后，即可执行迁移。

#### 创建迁移工作流 {#create-migration-workflow}

使用步骤1中的依赖项映射来配置和执行迁移。

**API格式**

```http
POST /workflows/migration
```

**沙盒级迁移**

要将所有决策对象从一个沙盒迁移到另一个沙盒，请执行以下操作：

```shell
curl --request POST \
  --url "https://decisioning-migration.adobe.io/workflows/migration" \
  --header "Authorization: Bearer <IMS_ACCESS_TOKEN>" \
  --header "x-gw-ims-org-id: <IMS_ORG_ID>" \
  --header "Content-Type: application/json" \
  --data '{
    "imsOrgId": "<IMS_ORG_ID>",
    "sourceSandboxDetails": { "sandboxName": "<SOURCE_SANDBOX_NAME>" },
    "targetSandboxDetails": { "sandboxName": "<TARGET_SANDBOX_NAME>" },
    "createDataStream": true,
    "dependency": {
      "profileAttributes": {
        "sourceAttr1": "targetAttr1"
      },
      "segments": {
        "sourceSegmentKey1": {
          "namespace": "<TARGET_SEGMENT_NAMESPACE>",
          "id": "<TARGET_SEGMENT_ID>"
        }
      },
      "contextAttributes": {
        "sourceCtx1": "targetCtx1"
      },
      "datasetName": "<TARGET_DATASET_NAME>"
    },
    "requestLevel": "sandbox"
  }'
```

**选件级别的迁移**

要仅迁移特定选件，请使用`requestLevel: "offer"`并添加`offersList`数组：

```json
"offersList": ["offer-id-1", "offer-id-2"]
```

**决策级迁移**

要仅迁移特定决策，请使用`requestLevel: "decision"`并添加`decisionsList`数组：

```json
"decisionsList": ["decision-id-1", "decision-id-2"]
```

#### 监视迁移状态 {#poll-migration-status}

轮询迁移工作流以跟踪其进度。

**API格式**

```http
GET /workflows/migration/{id}
```

**请求**

```shell
curl --request GET \
  --url "https://decisioning-migration.adobe.io/workflows/migration/<WORKFLOW_ID>" \
  --header "Authorization: Bearer <IMS_ACCESS_TOKEN>" \
  --header "x-gw-ims-org-id: <IMS_ORG_ID>"
```

**迁移结果**

当`status`字段显示`Completed`时，迁移成功。 工作流`result`包括：
* 已迁移对象的映射
* 迁移期间遇到的任何警告

当`status`字段显示`Failed`时，请查看`errors[]`数组和`result.error`字段以了解有关所发生错误的详细信息。

## 验证迁移 {#validate-migration}

成功完成迁移后，请验证所有对象是否已正确迁移。

### 验证核对清单 {#validation-checklist}

1. **区段** — 验证所有引用的区段是否根据您的映射在目标沙盒中正确解析。
2. **属性** — 确认所有配置文件属性和上下文属性都存在于目标沙盒中并已正确映射。
3. **决策对象** — 在Journey Optimizer用户界面中查看迁移的对象：
   * 优惠（决策项目）
   * 资格规则
   * 排名公式
   * 选择策略
   * 决策策略
4. **数据流测试** — 如果创建了数据流，请使用Edge Interact API测试运行时交付。

### 示例 {#test-runtime-delivery}

如果您的迁移创建了数据流，则可以使用以下示例测试选件交付：

```shell
curl --request POST \
  --url "https://edge.adobedc.net/ee/or2/v1/interact?configId=<DATASTREAM_ID>" \
  --header "Content-Type: application/json" \
  --header "x-request-id: <uuid>" \
  --data '{ "events": [ ... ] }'
```

## 回滚迁移 {#rollback}

如果您在验证期间发现问题，则可以回滚已完成的迁移，以将目标沙盒恢复到其以前的状态。

### 创建回滚工作流 {#create-rollback-workflow}

通过创建引用要还原的迁移的回滚工作流来启动回滚。

**API格式**

```http
POST /workflows/rollback
```

**请求**

```shell
curl --request POST \
  --url "https://decisioning-migration.adobe.io/workflows/rollback" \
  --header "Authorization: Bearer <IMS_ACCESS_TOKEN>" \
  --header "x-gw-ims-org-id: <IMS_ORG_ID>" \
  --header "Content-Type: application/json" \
  --data '{ "rollbackWorkflowId": "<MIGRATION_WORKFLOW_ID>" }'
```

将`<MIGRATION_WORKFLOW_ID>`替换为您要回滚的迁移工作流的ID。

### 监视回滚状态 {#poll-rollback-status}

轮询回滚工作流以跟踪其进度。

**API格式**

```http
GET /workflows/rollback/{rollbackWorkflowId}
```

**请求**

```shell
curl --request GET \
  --url "https://decisioning-migration.adobe.io/workflows/rollback/<ROLLBACK_WORKFLOW_ID>" \
  --header "Authorization: Bearer <IMS_ACCESS_TOKEN>" \
  --header "x-gw-ims-org-id: <IMS_ORG_ID>"
```

## 处理并发工作流 {#handle-concurrency}

迁移API每次只允许每个组织运行一个工作流。 如果您尝试在另一个工作流正在进行时创建新工作流，您将收到&#x200B;**409冲突**&#x200B;错误响应（“某个工作流已在进行中……”）。

在这种情况下，请等待进行中的工作流完成，或检索工作流ID并轮询其状态。 当前工作流完成后，您可以创建一个新工作流。

## 实体映射引用 {#entity-mapping}

从Decision management迁移到Decisioning时，实体映射如下：

| 决策管理 | 决策 |
|-------------------|-------------|
| 产品建议 | 决策项目 |
| 优惠收藏集 | 项目收藏集 |
| 合格规则 | 合格规则 |
| 排名公式 | 排名公式 |
| 决策 | 选择策略+决策策略 |
| 促销活动 | 促销活动&#x200B;*（仅限基本内容）* |
| 投放 | 表面+渠道配置 |
| 标记 | 统一标记 |

## 工作流清理 {#cleanup}

<!--Workflow resources can be deleted by service users only. Delete operations require an `If-Match` header with the workflow's `_etag` value.

**Available delete operations:**

* `DELETE /workflows/generate-dependencies/{id}`
* `DELETE /workflows/migration/{id}`
* `DELETE /workflows/rollback/{id}`-->

工作流删除功能不公开。 如果需要删除工作流资源，请与系统管理员联系。

## 相关主题 {#related-topics}

* [从决策管理迁移到Decisioning](migrate-to-decisioning.md) — 了解迁移到Decisioning的好处和功能
* [决策快速入门](gs-experience-decisioning.md)
* [Decisioning护栏和限制](decisioning-guardrails.md)
* [决策 API 入门](api-reference/getting-started.md)
