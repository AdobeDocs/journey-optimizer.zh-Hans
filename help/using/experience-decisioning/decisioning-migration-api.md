---
title: Decisioning 迁移 API
description: 了解如何使用Decisioning迁移服务API在具有自动依赖项解析和回滚支持的沙盒之间迁移决策管理对象。
feature: Decisioning
topic: Integrations
role: Developer
level: Experienced
exl-id: 3ec084ca-af9e-4b5e-b66f-ec390328a9d6
feature_v2: id: a4cb03e1-327e-499d-9de8-e0c0db8a63a2id: a984631b-2bae-4860-9b15-69c41a799dcb
subfeature_v2: id: a7a194a0-75e2-4913-8a83-14714fbf68e6id: eb547372-2a95-4d13-b0fd-f720c9895880
source-git-commit: bf147566ac63bce11f4413a2450b55d436f01d7a
workflow-type: tm+mt
source-wordcount: 3211
ht-degree: 2%

---

# Decisioning 迁移 API {#decisioning-migration-api}

>[!BEGINSHADEBOX]

**在此页面上：**&#x200B;使用Decisioning迁移服务API在具有自动依赖性分析和回滚支持的沙盒之间移动决策管理对象，以便您可以跨环境转换决策内容，同时保持数据完整性。

>[!ENDSHADEBOX]

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

>[!NOTE]
>
>目标沙盒可以与源沙盒相同。 迁移过程可处理此方案并确保数据完整性，无论对象是迁移至同一沙盒还是另一个沙盒。

### 跨沙盒迁移先决条件 {#cross-sandbox-prerequisites}

当源沙盒≠目标沙盒时，需要以下项：

* **配置文件属性** — 必须存在于目标沙盒中或具有预定义的映射
* **区段ID** — 必须在具有旧→新ID映射的目标沙盒中预先创建
* **标识映射** — 必须配置为一致的标识解析

## API 基础知识 {#api-basics}

### 基础 URL {#base-url}

使用以下基本URL：

* **生产**： `https://decisioning-migration.adobe.io`

### 身份验证 {#authentication}

所有API请求都需要以下标头：

* `Authorization: Bearer <IMS_ACCESS_TOKEN>`
* `x-gw-ims-org-id: <IMS_ORG_ID>`
* `Content-Type: application/json`

有关设置身份验证的详细说明，请参阅[Journey Optimizer身份验证指南](https://developer.adobe.com/journey-optimizer-apis/references/authentication){target="_blank"}。

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
  --url "https://decisioning-migration.adobe.io/workflows/generate-dependencies?request-level=sandbox" \
  --header "Authorization: Bearer <IMS_ACCESS_TOKEN>" \
  --header "x-gw-ims-org-id: <IMS_ORG_ID>" \
  --header "Content-Type: application/json" \
  --data '{
    "imsOrgId": "<IMS_ORG_ID>",
    "sourceSandboxDetails": { "sandboxName": "<SOURCE_SANDBOX_NAME>" },
    "targetSandboxDetails": { "sandboxName": "<TARGET_SANDBOX_NAME>" }
  }'
```

**选件级别的依赖项**

要仅分析特定选件的依赖关系，请在查询字符串中使用`request-level=offer`调用同一端点，并在正文中提供包含要分析的选件ID的`offersList`数组。

**决策级依赖关系**

要仅分析特定决策的依赖关系，请在查询字符串中使用`request-level=decision`，并在正文中提供一个`decisionsList`数组以及要分析的决策ID。

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
* **区段** — 将每个源区段键映射到目标区段标识符(`{namespace, id}`)
* **datasetName** — 用于迁移的目标体验事件数据集。 必须将其附加到为Journey Optimizer Edge (Web SDK)调用启用的数据流；其架构用于添加迁移的上下文属性。

您在步骤2中迁移请求的`dependency`对象中提供这些映射。

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
  --url 'https://decisioning-migration.adobe.io/workflows/migration?request-level=sandbox' \
  --header 'Authorization: Bearer <IMS_ACCESS_TOKEN>' \
  --header 'Content-Type: application/json' \
  --header 'x-gw-ims-org-id: <IMS_ORG_ID>' \
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
    }
  }'
```

**选件级别的迁移**

要仅迁移特定选件，请在查询字符串中使用`request-level=offer`并将`offersList`数组添加到正文中：

```json
"offersList": ["offer-id-1", "offer-id-2"]
```

**决策级迁移**

要仅迁移特定决策，请在查询字符串中使用`request-level=decision`并将`decisionsList`数组添加到正文中：

```json
"decisionsList": ["decision-id-1", "decision-id-2"]
```

**请求字段**

* **请求级别** （查询） — 迁移范围： `sandbox`、`offer`或`decision`。
* **imsOrgId**（必需） — 您的IMS组织ID。
* **sourceSandboxDetails.sandboxName**（必需） — 包含决策管理实体的Source沙盒。
* **targetSandboxDetails.sandboxName**（必需） — 在其中创建决策实体的目标沙盒。
* **dependency.datasetName**（必需） - Target体验事件数据集。 必须将其附加到为Journey Optimizer Edge (Web SDK)调用启用的数据流；其架构用于添加迁移的上下文属性。
* **createDataStream** - `true`创建新的启用Journey Optimizer的数据流；`false`重复使用`dependency.datasetName`中已附加到数据集的数据流。
* **dependency.profileAttributes** — 源→目标配置文件属性的映射。
* **dependency.contextAttributes** — 源→目标上下文属性的映射。
* **dependency.segments** — 源区段键→目标区段(`{namespace, id}`)的映射。
* **offersList[]** / **decisionsList[]** — 要迁移的优惠或决策ID；当`request-level`分别为`offer`或`decision`时需要。

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

每个工作流（依赖项、迁移和回滚）返回相同的资源字段：

* **id** — 工作流标识符(UUID)；用匹配的`GET /{id}`轮询其状态。
* **状态** — 生命周期状态： `New`、`Running`、`Completed`或`Failed`。
* **结果** — 出现在`Completed`上；工作流输出（例如，已迁移对象的映射和任何警告）。
* **错误[]** - `Failed`上存在；结构化错误详细信息（另请参阅`result.error`）。
* **_links.self** — 工作流资源的URL。

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

## 迁移范围和覆盖范围 {#migration-scope}

了解迁移的范围可帮助您规划和验证从决策管理到决策的过渡。 此部分概述了迁移过程涵盖的内容以及需要手动操作的内容。

### 范围：涵盖的内容 {#in-scope}

迁移API处理以下项目和功能：

* **用例** — 仅入站/Edge决策用例在范围内。 Journey Optimizer电子邮件渠道迁移中的出站或OD受支持，但需要手动更新。
* **基于代码的体验营销活动** — 在迁移期间自动创建，目标沙盒中每个迁移决策范围一个营销活动。
* **渠道配置/界面** — 每个决策管理位置创建的渠道配置/界面，确保决策响应的正确路由。
* **选件内容类型** — 仅当选件的内容类型为JSON或文本时，才会迁移这些选件。 其他内容类型需要手动重新创建。
* **优惠特征** — 保留在“个性化优惠项目 — Experience Decisioning”架构的`offer_item_custom_attributes`字段组中，维护自定义元数据。
* **上下文属性** — 已添加到`custom_context_attributes`字段组中的Experience Event架构以进行跟踪和个性化。
* **决策范围** — 一个决策管理决策范围映射到决策中的一个选择策略+一个决策策略+一个营销活动，以确保正确的实体层次结构。
* **仅限API的资格规则** — 仅限通过API创建的资格规则（不在决策管理UI中）已迁移并在Decisioning中保持仅限API。 UI创建的规则也会迁移。

### 范围外：未涵盖或需要手动操作的内容 {#out-of-scope}

以下项目需要手动操作或迁移工具不支持这些项目：

* **决策版面** — 迁移工具未创建任何版面。 您必须在迁移之前或之后，根据您的架构，在Decisioning中手动创建这些内容。
* **投放级别上限** — 未迁移投放级别频率上限。
* **非JSON/文本选件内容** — 不迁移内容类型为JSON或文本以外的选件（例如HTML、图像），并且需要在Decisioning中手动重新创建。
* **配置文件属性和区段** — 迁移工具从不会创建或编辑配置文件属性和区段成员资格。 在运行迁移之前，这些必须已存在于目标沙盒中。
* **区段ID映射** — 必须在目标沙盒中预先创建区段ID。 您必须在迁移API请求中提供新→旧ID映射，以便进行区段解析。
* **数据收集代码更改** — 客户端和服务器端事件跟踪代码更改未自动。 您的实施团队必须更新事件收集才能使用决策请求/响应格式和决策事件架构。

## 实体映射引用 {#entity-mapping}

从Decision management迁移到Decisioning时，实体将根据下表进行映射。 映射包括主要决策实体以及在迁移期间创建或使用的其他关联实体。

### 决策管理到决策实体映射

| 决策管理实体 | 决策实体 | 其他实体 |
|-----------|--------------|-------------------|
| 决策 | 选择策略 | 物料收集、资格规则、排名公式 |
| | 决策策略 | 项目计数、选择策略、后备优惠项目 |
| | 基于代码的体验营销活动 | 决策策略、内容、渠道配置、Journey Optimizer片段 |
| 放置环境 | 渠道配置 | — |
| 收藏集 | 项目收藏集 | 统一标记、优惠项目 |
| 集合限定符 | 统一标记 | — |
| 规则 | 决策规则 | — |
| 排名公式 | 决策排名公式 | — |
| 产品建议 | 选件项目 | 资格规则、Journey Optimizer片段、统一标记、频度上限 |
| | 选件项架构 | — |
| | Journey Optimizer Fragments | — |

### 命名约定

迁移过程使用`ExD_`前缀应用命名约定，以确保一致性并防止命名冲突。

| Source对象 | 决策管理名称模式 | 决策名称模式 |
|---------------|-----------------|-------------------|
| 产品建议 | `<offerName>` | `ExD_<offerName>` |
| 合格规则 | `<ruleName>` | `ExD_<ruleName>` |
| 排名公式 | `<formulaName>` | `ExD_<formulaName>` |
| 收藏集 | `<collectionName>` | `ExD_<collectionName>_<placementName>` |
| 决策→选择策略 | `<decisionName>` | `ExD_<decisionName>_selection_strategy_<index>` |
| 决策→决策政策 | `<decisionName>` | `ExD_<decisionName>_<placementName>` |
| Journey Optimizer片段 | `<offerName>` | `ExD_<offerName>_<placementName>_<index>` |
| 放置→面 | `<placementName>` | `ExD_<placementName>` *（空间/点转换为下划线）* |
| 统一标记 | `<sourceName>, <targetName>` | `ExDMigration_<sourceName>_<targetName>` |
| CBE营销活动 | `<decisionName>, <placementName>` | `Campaign for <decisionName> : <placementName>` |

### 其他属性

| Source属性 | 目标位置 |
|-----------------|-----------------|
| 产品建议属性 | 个性化优惠项目架构中的“migratedofferattributes”字段 |
| 上下文属性 | 在迁移期间提供的数据集所附加的架构中的“migratedcontextattributes”字段 |

## 请求和响应模型 {#request-response-model}

从Decision management迁移到Decisioning时，必须更新您的应用程序代码才能使用新的请求和响应格式。 两个系统都使用Edge Network端点，但有效负载结构和字段名称有所不同。

### 决策管理Edge请求（当前） {#dm-request}

当前的决策管理Edge请求遵循以下结构：

**终结点：**

```
POST https://edge.adobedc.net/ee/v2/interact
```

**标头：**
- `Authorization: Bearer <IMS_ACCESS_TOKEN>`
- `x-api-key: <API_KEY>` （来自Developer Console）
- `x-gw-ims-org-id: <IMS_ORG_ID>` （格式： `{ORG_ID}@AdobeOrg`）
- `x-request-id: <UNIQUE_REQUEST_ID>` （用于跟踪和重复数据删除）
- `Content-Type: application/vnd.adobe.xdm+json; schema="…/decision-request;version=1.0"`
- `Accept: application/vnd.adobe.xdm+json; schema="…/decision-response;version=1.0"`
- `x-sandbox-name: <SANDBOX_NAME>` （例如，prod、dev）

**请求正文参数：**
- `xdm:dryRun` (true/false) — 测试请求而不污染报告
- `xdm:propositionRequests[]` — 决策请求数组：
  - `activityId` — 决策活动标识符
  - `placementId` — 投放位置标识符
  - `itemCount` — 要返回的最大优惠数量
- `xdm:profiles[].xdm:identityMap` — 身份映射（电子邮件、ECID等）
- `xdm:validateContextData` — 严格的上下文数据验证标志
- `xdm:responseFormat.xdm:includeContent` — 仅包含实际内容与ID

**示例请求正文：**

```json
{
  "xdm": {
    "dryRun": false,
    "propositionRequests": [
      { "activityId": "<ACTIVITY_ID>", "placementId": "<PLACEMENT_ID>", "itemCount": 3 }
    ],
    "profiles": [
      { "identityMap": { "ECID": [ { "id": "<ECID>", "primary": true } ] } }
    ],
    "validateContextData": true,
    "responseFormat": { "includeContent": true }
  }
}
```

>[!NOTE]
>有关完整的决策管理(OD)请求/响应引用，请参阅[Edge Decisioning API](https://experienceleague.adobe.com/en/docs/journey-optimizer/using/decisioning/offer-decisioning/api-reference/offer-delivery-api/edge-decisioning-api)（Web SDK / Edge变体，它使用base64编码的`decisionScopes`，带有`activityId`和`placementId`）。

### Decisioning Edge请求（迁移后） {#decisioning-request}

迁移后，通过同一Edge Network端点使用Decisioning请求格式。

**终结点：**

```
POST https://edge.adobedc.net/ee/v2/interact
```

**键请求字段：**
- `query.identity.fetch` — 要解析的标识类型数组（例如，`["ECID"]`）
- `event.xdm.environment.type` — 环境类型： `"browser"`、`"app"`或`"server"`
- `event.xdm.environment.browserDetails` — 浏览器元数据(`viewportWidth`， `viewportHeight`， `userAgent`)
- `event.xdm.identityMap` — 与决策管理相同的标识映射
- `event.xdm.timestamp` - ISO 8601时间戳
- `query.personalization.surfaces` — 目标表面数组（例如，`["web://site.com/homepage"]`） — 替换`decisionScope`
- `query.personalization.schemas` — 要返回的内容架构（例如，`["json-content-item", "html-content-item"]`）
- `data.__adobe.ajo.allowDuplicateDecisionItems` — 重复数据删除控件（默认为`true`；设置`false`，以便仅返回一次符合多个曲面的项，而其他曲面接收回退/空项）。 替换决策管理`allowDuplicatePropositions`。
- `data.__adobe.ajo.dryRun` — 测试标志；隐藏报告和上限计数器的反馈事件。 替换决策管理`xdm:dryRun`。 在生产之前删除。

**示例请求正文（服务器端）：**

```json
{
  "events": [
    {
      "query": {
        "identity": { "fetch": ["ECID"] },
        "personalization": {
          "surfaces": ["web://my-web/IP_NLI_HP_GET_LOAN_WIDGET"],
          "schemas": [
            "https://ns.adobe.com/personalization/json-content-item",
            "https://ns.adobe.com/personalization/html-content-item"
          ]
        }
      },
      "xdm": {
        "eventType": "decisioning.propositionFetch",
        "environment": {
          "type": "browser",
          "browserDetails": { "viewportWidth": 1280, "viewportHeight": 900, "userAgent": "<USER_AGENT>" }
        },
        "identityMap": {
          "ECID": [ { "id": "<ECID>", "authenticatedState": "ambiguous", "primary": true } ]
        },
        "timestamp": "2025-09-08T12:00:00.000Z"
      },
      "data": {
        "__adobe": { "ajo": { "allowDuplicateDecisionItems": false } }
      }
    }
  ],
  "meta": {
    "state": {
      "domain": "my-web",
      "cookiesEnabled": true,
      "entries": [
        { "key": "kndctr_<ORG>_AdobeOrg_identity", "value": "<identity-cookie>" },
        { "key": "kndctr_<ORG>_AdobeOrg_cluster", "value": "<cluster-cookie>" }
      ]
    }
  }
}
```

>[!NOTE]
>有关完整的Journey Optimizer Decisioning Web SDK / Edge参考，请参阅[基于代码的体验：决策实施](https://experienceleague.adobe.com/en/docs/journey-optimizer/using/channels/code-based-experience/configure-code-based-channel/code-based-decisioning-implementations)。

### Decisioning Edge响应 {#decisioning-response}

决策响应包含多个按关注点类型组织的句柄：`personalization:decisions`（选件）、`locationHint:result`和`state:store`（要保留的Cookie）。

**响应结构：**

```json
{
  "requestId": "<REQUEST_ID>",
  "handle": [
    {
      "type": "personalization:decisions",
      "eventIndex": 0,
      "payload": [
        {
          "id": "103ae599-e6d8-4631-baf3-51dd8c6ed4c1",
          "scope": "web://my-web/IP_NLI_HP_GET_LOAN_WIDGET",
          "scopeDetails": {
            "decisionProvider": "AJO",
            "correlationID": "<CORRELATION_ID>",
            "characteristics": {
              "eventToken": "<base64 message-level event token>",
              "subPropositions": "<base64-encoded array of decision items>"
            },
            "rank": 1,
            "activity": {
              "id": "<campaignId>#<actionId>",
              "priority": 0,
              "matchedSurfaces": ["web://my-web/IP_NLI_HP_GET_LOAN_WIDGET"]
            }
          },
          "items": [
            {
              "id": "36646bab-af1b-44c6-b632-bbfb9c357919",
              "schema": "https://ns.adobe.com/personalization/json-content-item",
              "data": { "content": "{ ...offer JSON... }" }
            }
          ]
        }
      ]
    },
    {
      "type": "locationHint:result",
      "payload": [
        { "scope": "EdgeNetwork", "hint": "ind1", "ttlSeconds": 1800 }
      ]
    },
    {
      "type": "state:store",
      "payload": [
        { "key": "kndctr_<ORG>_AdobeOrg_cluster", "value": "<cluster-cookie>", "maxAge": 1800 },
        { "key": "kndctr_<ORG>_AdobeOrg_identity", "value": "<identity-cookie>", "maxAge": 34128000 }
      ]
    }
  ]
}
```

**键响应字段：**
- `handle[].type` — 句柄类型(`personalization:decisions`， `locationHint:result`， `state:store`)
- `payload[].id` — 唯一建议实例ID — 回显显示/交互事件
- `payload[].scope` — 建议已解析的表面URI
- `payload[].scopeDetails.decisionProvider` — 确认引擎为`AJO`
- `payload[].scopeDetails.correlationID` — 将决策实例链接到服务事件
- `payload[].scopeDetails.rank` / `payload[].scopeDetails.activity` — 建议的排名和营销活动/操作元数据
- `payload[].scopeDetails.characteristics.eventToken` — 消息级跟踪令牌
- `payload[].scopeDetails.characteristics.subPropositions` — 决策项&#x200B;**的Base64编码**&#x200B;数组；每个项都有自己的每个项`token`。 这些按项目令牌是您在显示/交互事件中传递到`propositionAction.tokens`的内容
- `payload[].items[].schema` / `payload[].items[].data.content` — 要呈现的内容架构和实际选件内容(JSON/HTML)
- `state:store`有效负载 — 要在后续请求中保留和转发的身份和群集Cookie（服务器端）

`characteristics.subPropositions`字符串base64解码为提供的项数组，每个项都具有其每项`token`：

```json
[
  {
    "id": "1ae75277-8832-4c23-bbbc-09f01cfe6c8b",
    "scope": "web://my-web/IP_NLI_HP_GET_LOAN_WIDGET",
    "scopeDetails": { "decisionProvider": "EXD", "correlationID": "<CORRELATION_ID>-0", "rank": 1 },
    "items": [
      { "id": "dps:<schema>:1be64ff83a612488", "name": "ExD_Personal Loan Offer", "score": 997.0, "token": "CLaefQnVLcLbCtzEXV3Jeg" },
      { "id": "dps:<schema>:1be6516838e1248c", "name": "ExD_Home Loan Offer",     "score": 995.0, "token": "ALlB5KV1B0e+CpHoahi7Ew" },
      { "id": "dps:<schema>:1be650da3cd06e98", "name": "ExD_Auto Loan Offer",     "score": 994.0, "token": "koJTRQcwFkR92AqbZ88ytQ" },
      { "id": "dps:<schema>:1be65612d5a1248d", "name": "ExD_Fallback Offer",      "itemSelection": { "selectionDetail": { "selectionType": "fallback" } }, "token": "GHo4ow7h6iCzBOhYR1+6jg" }
    ]
  }
]
```

## 实施模式 {#implementation-patterns}

Decisioning支持三种实施方法：

### 客户端实施（Web SDK/移动SDK） {#client-side}

Web SDK或Mobile SDK会自动处理所有请求和Cookie管理。 SDK通过每个请求存储和转发身份和群集Cookie。

**Cookie处理：**&#x200B;自动 — Web SDK管理`kndctr_<OrgId>_identity`和`kndctr_<OrgId>_cluster` Cookie。

### 服务器端实施(Edge Network API) {#server-side}

应用程序服务器直接向Edge Network执行POST，并且必须手动管理Cookie转发。 服务器从传入请求中提取浏览器Cookie并通过`meta.state.entries[]`将它们转发到Edge Network，然后在响应中返回Cookie。

**Cookie处理：**&#x200B;手动 — 应用服务器必须从浏览器请求中提取Cookie，在请求正文中转发到Edge Network，并设置为响应。 为了标识一致性，必须在`meta.state.entries`中显式转发Cookie。

### 混合实施 {#hybrid}

将服务器端渲染（初始页面加载）与客户端SDK（后续交互）结合使用。 服务器通过Edge Network呈现初始内容，然后Web SDK接管后续个性化请求。

**Cookie处理：**&#x200B;混合 — 服务器端需要手动将Cookie转发到Edge Network；客户端由Web SDK自动处理。 确保服务器端渲染中的身份令牌可供客户端SDK使用，以实现一致的身份解析。

## 事件跟踪和数据收集 {#event-tracking}

要正确归因决策结果、启用频率封顶以及进行基于人工智能的排名优化，您必须使用决策事件架构实施事件跟踪。

### 必需事件字段 {#event-fields}

`eventType`和`_experience.decisioning.propositionEventType`都是必需的。 如果缺少任一计数器，则相应的display/interact计数器将不会递增。

* **`eventType`** — 指定事件类别：
  - `decisioning.propositionDisplay` — 展示事件（向用户显示的优惠）
  - `decisioning.propositionInteract` — 交互事件（用户已点击或参与优惠）

* **`_experience.decisioning.propositionEventType`** — 标记事件子类型。 恰好包括设置为`1`的&#x200B;**一个**&#x200B;事件类型键（每个值为`1`或`0`；不要在同一对象中将多个事件类型设置为`1`）：
  - `{ "display": 1 }` — 展示事件
  - `{ "interact": 1 }` — 交互事件
  - 如果所有`display`/`interact`/`dismiss`都是`0`，或者`eventType`是`decisioning.proposition<Display|Interact|Dismiss>`以外的任何值，则该事件将被视为&#x200B;**自定义事件**。

* **`_experience.decisioning.propositionAction.tokens[]`** — 每个项目的令牌用于标识为以下项目递增计数器的服务项目：
  - 从已解码的`subPropositions`数组 — **非** `scopeDetails.characteristics.eventToken`中复制每个项的`token`，这是不同的消息级令牌。
  - 完全按照收到的令牌传递，未修改。
  - **Interact事件：**&#x200B;只提供&#x200B;**一个**&#x200B;令牌（点击项）。
  - **显示事件：**&#x200B;可选 — 提供令牌以递增特定项，或&#x200B;**省略** `tokens`以递增`subPropositions`中&#x200B;**所有**&#x200B;项的计数器。

* **`_experience.decisioning.propositions[]`** — 从响应（包含`characteristics.subPropositions`并需要`decisionProvider`）回显已提供的建议，包括`id`、`scope`和完整的`scopeDetails`。 您不需要生成显式`items[]`数组。

### 架构要求 {#schema-requirements}

在迁移之前，将Decisioning字段组关联到事件数据集架构：

1. 在Experience Platform中，打开您的事件数据集架构
2. 添加`Experience Event - Proposition Details`字段组
3. 确保映射以下字段：
   - `_experience.decisioning.*`字段
   - `_experience.decisioning.propositionAction.tokens`
   - `_experience.decisioning.propositionEventType`

### 跟踪令牌处理 {#tracking-token}

必须按照以下要求处理跟踪令牌：

* **每个项目的令牌驱动计数器** — `propositionAction.tokens`中的值是来自`subPropositions`的每个服务项目的`token`，而不是消息级别`characteristics.eventToken`。
* **Interact事件** — 只提供一个令牌（点击项）。
* **显示事件** — 令牌是可选的；省略以递增`subPropositions`中的所有项，或者提供特定令牌以仅递增这些项。
* **不修改令牌** — 将值与收到的值完全传递；不对其进行编码、解析或更改。

## 决策事件示例 {#event-examples}

每个示例都回溯已提供的建议（包括其带有`characteristics.subPropositions`的`scopeDetails`），并设置`eventType`和`propositionEventType`。 计数器针对`subPropositions`中的项目递增；`propositionAction.tokens`选择哪些项目。

### 显示事件

向用户显示选件时，显示事件通知Decisioning 。 提供显示项的令牌，或省略`tokens`以递增`subPropositions`中所有项的显示计数器：

```json
{
  "header": {
    "imsOrgId": "YOUR_ORG_ID",
    "sandboxId": "sandbox-id",
    "sandboxName": "sandbox-name",
    "source": { "name": "ajo-inbound" }
  },
  "body": {
    "xdmEntity": {
      "identityMap": {
        "ECID": [ { "id": "ecid-123", "primary": true } ]
      },
      "eventType": "decisioning.propositionDisplay",
      "_experience": {
        "decisioning": {
          "propositionEventType": { "display": 1 },
          "propositionAction": {
            "id": "b96f842b-5dd9-4c55-9dae-647d96250028",
            "tokens": ["CLaefQnVLcLbCtzEXV3Jeg", "ALlB5KV1B0e+CpHoahi7Ew"]
          },
          "propositions": [
            {
              "id": "103ae599-e6d8-4631-baf3-51dd8c6ed4c1",
              "scope": "web://my-web/IP_NLI_HP_GET_LOAN_WIDGET",
              "scopeDetails": {
                "decisionProvider": "AJO",
                "characteristics": {
                  "eventToken": "<base64 eventToken from response>",
                  "subPropositions": "<base64 subPropositions from response>"
                }
              }
            }
          ]
        }
      }
    }
  }
}
```

### Interact（点击）事件

交互事件会在用户单击或参与显示的选件时进行跟踪。 您&#x200B;**必须**&#x200B;恰好提供一个&#x200B;**标识所点击项目的**&#x200B;令牌：

```json
{
  "header": {
    "imsOrgId": "YOUR_ORG_ID",
    "sandboxId": "sandbox-id",
    "sandboxName": "sandbox-name",
    "source": { "name": "ajo-inbound" }
  },
  "body": {
    "xdmEntity": {
      "identityMap": {
        "ECID": [ { "id": "ecid-123", "primary": true } ]
      },
      "eventType": "decisioning.propositionInteract",
      "_experience": {
        "decisioning": {
          "propositionEventType": { "interact": 1 },
          "propositionAction": {
            "id": "b96f842b-5dd9-4c55-9dae-647d96250028",
            "tokens": ["CLaefQnVLcLbCtzEXV3Jeg"]
          },
          "propositions": [
            {
              "id": "103ae599-e6d8-4631-baf3-51dd8c6ed4c1",
              "scope": "web://my-web/IP_NLI_HP_GET_LOAN_WIDGET",
              "scopeDetails": {
                "decisionProvider": "AJO",
                "characteristics": {
                  "eventToken": "<base64 eventToken from response>",
                  "subPropositions": "<base64 subPropositions from response>"
                }
              }
            }
          ]
        }
      }
    }
  }
}
```

### 自定义事件

自定义事件使用客户定义的`eventType`（除`decisioning.proposition<Display|Interact|Dismiss>`之外的任何值），并在`propositionEventType`中将所有`display`/`interact`/`dismiss`设置为`0`（分类为`OTHER`）。 自定义事件将像针对`subPropositions`的显示事件（多令牌筛选）一样进行解码，并通过配置的PQL进行评估：

```json
{
  "header": {
    "imsOrgId": "YOUR_ORG_ID",
    "sandboxId": "sandbox-id",
    "sandboxName": "sandbox-name",
    "originalTimestamp": 1700000
  },
  "body": {
    "xdmEntity": {
      "identityMap": {
        "ECID": [ { "id": "ecid-123", "primary": true } ]
      },
      "eventType": "add-to-cart",
      "_experience": {
        "decisioning": {
          "propositionEventType": { "display": 0, "interact": 0, "dismiss": 0 },
          "propositionAction": {
            "id": "b96f842b-5dd9-4c55-9dae-647d96250028",
            "tokens": ["CLaefQnVLcLbCtzEXV3Jeg"]
          },
          "propositions": [
            {
              "id": "103ae599-e6d8-4631-baf3-51dd8c6ed4c1",
              "scope": "web://my-web/IP_NLI_HP_GET_LOAN_WIDGET",
              "scopeDetails": {
                "decisionProvider": "AJO",
                "characteristics": {
                  "eventToken": "<base64 eventToken from response>",
                  "subPropositions": "<base64 subPropositions from response>"
                }
              }
            }
          ]
        }
      }
    }
  }
}
```

这些事件支持在Decisioning中进行频率封顶、现成报告和AI驱动的排名优化。 有关使用Web SDK发送建议事件，请参阅[基于代码的体验：决策实施](https://experienceleague.adobe.com/en/docs/journey-optimizer/using/channels/code-based-experience/configure-code-based-channel/code-based-decisioning-implementations)。

## 端到端迁移过程 {#migration-process}

1. 验证先决条件 — 确保在开始迁移之前，已准备目标沙盒并已识别所有先决条件依赖项（配置文件属性、区段ID、ID映射）。

1. 调用迁移API — 执行迁移API，使用您准备的先决条件和映射将决策管理对象迁移到决策。

1. 草稿决策实体生成 — 工具在每个实体映射中以草稿状态创建营销活动、决策策略、选择策略、优惠项等。 查看目标沙盒中所有生成的决策对象。 验证命名、实体类型和引用是否正确。 目前暂无面向客户的情况，决策管理仍持续为实时流量提供服务。

1. 更新客户端和服务器代码 — 实施所需的代码更改以使用新的Decisioning请求/响应格式，并使用必填字段实施事件跟踪。

1. 激活和切换 — 激活决策对象（策略、策略、营销活动、界面），并在您自己的时间线上将流量从决策管理中移开。

## 相关主题 {#related-topics}

* [从决策管理迁移到Decisioning](migrate-to-decisioning.md) — 了解迁移到Decisioning的好处和功能
* [决策快速入门](gs-experience-decisioning.md)
* [Decisioning护栏和限制](decisioning-guardrails.md)
* [决策 API 入门](api-reference/getting-started.md)