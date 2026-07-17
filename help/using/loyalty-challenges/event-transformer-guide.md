---
solution: Journey Optimizer
product: journey optimizer
title: Event Transformer指南
description: 了解如何在Adobe Journey Optimizer中为忠诚度挑战事件定义配置架构和转换器设置。
feature: Journeys
topic: Content Management
role: Admin
level: Intermediate
hide: true
badge: label="私人测试版" type="Informative"
mini-toc-levels: 1
exl-id: d3ad85f0-7f7e-40ab-b8c4-fc0c1234be87
feature_v2: []
subfeature_v2: []
source-git-commit: 762afe791cc1fa826b7a9f35f6f54591590bab7c
workflow-type: tm+mt
source-wordcount: 2015
ht-degree: 1%

---

# Event Transformer指南 {#event-transformer-guide}

>[!CONTEXTUALHELP]
>id="ajo_loyalty_event_transformer"
>title="Event Transformer指南"
>abstract="使用本指南为忠诚度挑战事件定义配置架构验证和转换器表达式。"

>[!BEGINSHADEBOX]

**目录**

[忠诚度挑战入门](get-started.md)

<table style="table-layout:fixed">
<tr style="border: 0;">
<td style="vertical-align:top;">

**创建和管理挑战**

* [访问和管理挑战和任务](access-loyalty-challenges.md)
* [创建挑战](create-challenges.md)
* [创建任务](create-tasks.md)
* [监测忠诚度挑战表现](loyalty-reporting.md)

</td>
<td style="vertical-align:top;">

**配置并集成**

* [配置忠诚度挑战](loyalty-admin.md)
* [奖励定义指南](reward-definition-guide.md)
* **事件转换器指南** ◀&rbrace;︎**您在这里**
* [忠诚度数据和数据集](loyalty-data-and-datasets.md)
* [忠诚度挑战API参考](https://developer.adobe.com/journey-optimizer-apis/references/loyalty-challenges){target="_blank"}

</td>
</tr>
</table>

>[!ENDSHADEBOX]

>[!AVAILABILITY]
>
>此功能当前处于&#x200B;**私人测试版**&#x200B;中。 有关[!DNL Journey Optimizer]中发行周期和可用性阶段的完整详细信息，请参阅[发行周期](../rn/releases.md)。

在将客户交易记录应用于忠诚度质询之前，它必须采用质询服务理解的&#x200B;**Adobe忠诚度事件**&#x200B;格式。 客户事件（来自POS系统、移动应用程序、电子商务平台或任何其他源）通常使用客户自己的数据架构。 **事件转换器**&#x200B;无需对上游系统进行任何更改即可弥合此间隙。

## 概述

**事件定义**&#x200B;告知平台以下两点：

* **要声明的事件** — 如何识别传入的事件属于此定义（匹配）
* **如何重新设置其形状** — 将客户的字段映射到忠诚度事件格式（转换）的[JSONata](https://docs.jsonata.org/overview)表达式

每个组织可以配置多个事件定义。 平台会按顺序评估它们，并应用匹配的第一个。 不符合任何定义的事件会落入本机引入的陷阱（请参阅[后备 — 本机忠诚度事件](#fallback--native-loyalty-events)）。

## Adobe忠诚度事件格式

每个事件定义都必须生成一个采用以下格式的JSON对象。 这是挑战服务流程的输入。

```json
{
  "_id":              "string — optional; used for duplicate detection if enabled",
  "event_name":       "string — used for internal metrics and reporting only (e.g. 'purchase', 'visit')",
  "timestamp":        "ISO 8601 date-time string — when the event occurred",
  "utc_offset":       "string — UTC offset of the store or device (e.g. '-07:00'); required for daypart matching",
  "location_id":      "string — optional; store or location identifier",
  "transaction_id":   "string — optional; dedup key for the transaction",
  "loyalty_identity": {
    "id": "string — the member's loyalty ID"
  },
  "item_list": [
    {
      "item_set":   ["string", "..."],  // one or more identifiers — SKU, category, event code, etc.
      "item_name":  "string — optional human-readable label",
      "quantity":   1,                  // integer; how many units
      "unit_price": 4.99,               // float; price per unit
      "sub_total":  4.99                // float; line total (quantity × unit_price)
    }
  ]
}
```

### 字段注释

| 字段 | 必需 | 注释 |
|--------------------------------|--------------------|-------|
| `loyalty_identity` | **是** | 必须包含`id` — 成员的忠诚度ID。 |
| `item_list` | **是** | 必须至少包含一个项目。 空`item_list`导致该事件被拒绝为无效。 |
| `item_set` | **是**（每项） | 此数组中的标识符是挑战任务包含/排除列表所匹配的对象。 包括每个相关标识符（SKU、产品类别、部门代码、事件名称），以便任务筛选器正常工作。 |
| `timestamp` | **是** | 用于日期窗口评估。 必须为ISO 8601。 |
| `utc_offset` | 推荐 | 对于白天窗口匹配和计算连续日条纹是必需的。 如果忽略，将跳过时段评估和连续日期计数。 |
| `_id` | 否 | 如果为组织启用了重复检测，则质询服务会拒绝已处理`_id`的事件。 |
| `sub_total` | 否 | 由支出阈值任务使用。 如果忽略，则该项目的贡献为零。 |

## 事件定义字段

| 字段 | 类型 | 必需 | 描述 |
|--------------------------------|------------------|----------------------|-------------|
| `guid` | 字符串 | 否（系统分配） | 创建时分配的唯一标识符。 只读。 |
| `name` | 字符串 | **是** | 易于用户识别的标签，例如`"Starbucks POS Purchase"`。 |
| `xdmSchemaId` | 字符串 | 否* | XDM架构ID用于匹配通过&#x200B;**DCCS摄取路由**&#x200B;到达的事件。 平台读取传入事件中嵌入的架构引用，并将其与此值进行比较。 |
| `identifierPath` | 字符串 | 否* | 事件JSON中的点表示法路径，用于匹配通过&#x200B;**直接HTTP路由(adobe.io)**&#x200B;到达的事件。 平台读取此路径上的值并根据`identifier`对其进行检查。 |
| `identifier` | 字符串数组 | 否 | `identifierPath`处应为值。 如果提供了并且非空，则路径上的值必须匹配这些值之一。 如果为空，则匹配路径中具有值的任何事件。 |
| `schema` | 字符串 | 否 | [JSON架构](https://json-schema.org/)文档（作为JSON字符串）用于在转换之前验证传入事件。 如果验证失败，则事件会因描述性错误而被拒绝。 |
| `transformer` | 字符串 | **是** | 将传入事件映射到Adobe忠诚度事件格式的JSONata表达式。 |

\*必须至少提供`xdmSchemaId`或`identifierPath`之一。

## 匹配的工作方式

匹配策略取决于事件到达平台的方式：

**DCCS摄取路由** — 通过数据收集核心服务(DCCS)到达的事件在其信封中带有XDM架构引用。 平台从`/body/xdmMeta/schemaRef/id`中读取架构ID，并将其与每个定义的`xdmSchemaId`进行比较。 针对此路由的定义配置`xdmSchemaId`。

**直接HTTP路由(adobe.io)** — 通过adobe.io API直接发布到平台的事件不包含XDM架构引用。 平台改为使用`identifierPath`遍历事件JSON并检查在那里找到的值：
* 如果`identifier`非空：该值必须与配置的字符串之一匹配。
* 如果`identifier`为空：路径中有非null值的所有事件均匹配。

根据此路由的定义配置`identifierPath` （也可以选择`identifier`）。

平台按&#x200B;**的顺序遍历组织的事件定义**&#x200B;并应用第一个匹配。 找到匹配项后，`xdmEntity`正文（用于DCCS事件）或完整事件正文（用于直接HTTP事件）将传递到转换器。

## 编写转换器

`transformer`字段是[JSONata](https://docs.jsonata.org/overview)表达式。 它接收传入事件JSON作为其输入，并且必须返回有效的Adobe会员事件对象。

+++基本映射模式

将目标格式的每个顶级字段映射到源事件中的相应路径：

```jsonata
{
  "_id":            sourceEvent._id,
  "event_name":     sourceEvent.eventType,
  "timestamp":      sourceEvent.timestamp,
  "utc_offset":     sourceEvent.storeInfo.utcOffset,
  "location_id":    sourceEvent.storeInfo.storeId,
  "transaction_id": sourceEvent.transaction.id,
  "loyalty_identity": {
    "id": sourceEvent.member.loyaltyId
  },
  "item_list": sourceEvent.transaction.items.{
    "item_set":   [itemSku, itemCategory],
    "item_name":  itemDescription,
    "quantity":   quantity,
    "unit_price": unitPrice,
    "sub_total":  lineTotal
  }
}
```

+++

+++对事件名称进行硬编码

如果与此定义匹配的所有事件都表示相同的逻辑活动，请对`event_name`进行硬编码：

```jsonata
{
  "event_name": "in-store-purchase",
  ...
}
```

`event_name`用于内部量度和报告。 未用作任务筛选器 — 任务资格由`item_set`内容决定，而不是由事件名称决定。

+++

+++映射DCCS/XDM事件的标识

对于通过DCCS路由到达的事件，成员的身份通常包含在标准XDM `identityMap`字段中，而不是自定义租户属性中。 `identityMap`是一个由命名空间键控的映射 — 键本身就是命名空间名称，值是一个标识对象数组。

```jsonata
"loyalty_identity": {
  "id": identityMap.Email[0].id
}
```

* **命名空间替换：**&#x200B;使用您的组织用于忠诚度会员的任何命名空间替换`Email`— `Loyalty`、`ECID`、`CRMID`等。始终从包含主要会员配置文件标识的命名空间中读取。

* **始终使用`[0]`：** `identityMap.Email`是一个数组。 如果没有索引，如果存在多个标识，则JSONata将返回序列而不是单个值，并且`loyalty_identity.id`将变为列表。 将其固定到带有`[0]`的第一个元素。

* **避免自定义租户标识字段：**&#x200B;自定义字段组有时会公开电子邮件形式的字段（例如`_yourtenant.identification.core.email`）。 在示例数据中，这将返回一个值并看起来是正确的，但在生产事件中，它通常为空。 可靠的身份来源始终为`identityMap`。

+++

+++正在生成`item_set`

`item_set`是字符串标识符的数组。 包括您的挑战任务可能过滤的每个字段：

```jsonata
"item_set": [itemSku, productCategory, departmentCode]
```

对于非事务性事件（签入、调查完成、自定义触发器），单个标识符就足够了：

```jsonata
"item_set": [eventName]
```

+++

+++映射`unit_price`

`unit_price`应为单价。 某些源架构存储的是行总计（价格×数量）。 如果来源字段为行合计，则除以数量以获取单价：

```jsonata
"unit_price": priceTotal / quantity
```

> 仅当源字段为行总计时才相除。 如果它已经存储了单位价格，则直接映射它 — 将单位价格除以数量将会自动产生错误的值。

+++

+++派生`transaction_id`

如果源事件不包括事务标识符，则可以从时间戳派生稳定标识符：

```jsonata
"transaction_id": "txn_" & $string($toMillis(timestamp))
```

这会将ISO时间戳转换为epoch毫秒，并为给定事件生成确定性值。 使用您平台自己的ID生成函数（如果可用）。

+++

+++使用JSONata函数

提供了完整的JSONata函数库。 有用的示例：

```jsonata
/* String concatenation */
"item_set": [skuId & ':' & categoryId]

/* Number formatting */
"item_set": ["spend:" & $formatNumber(totalAmount, '0.00')]

/* Conditional field */
"event_name": eventType ? eventType : "unknown"

/* Array transformation */
"item_list": items.{ "item_set": [sku], "quantity": qty, "sub_total": price * qty }
```

+++

## 示例

+++示例1 — 简单自定义事件（非事务性）

**方案：**&#x200B;移动应用发送签入事件。 没有行项目 — 事件本身是符合条件的活动。

**传入事件：**

```json
{
  "_id":       "evt-001",
  "eventName": "store-checkin",
  "timestamp": "2025-10-15T14:22:00Z",
  "storeId":   "STORE-042",
  "member": {
    "loyaltyId": "LM-8827361"
  }
}
```

**事件定义：**

```json
{
  "name":           "Mobile Store Check-In",
  "identifierPath": "eventName",
  "identifier":     ["store-checkin"],
  "transformer":    "{\"_id\": _id, \"event_name\": eventName, \"timestamp\": timestamp, \"location_id\": storeId, \"loyalty_identity\": {\"id\": member.loyaltyId}, \"item_list\": [{\"item_set\": [eventName], \"quantity\": 1}]}"
}
```

**格式化的转换器（用于可读性）：**

```jsonata
{
  "_id":        _id,
  "event_name": eventName,
  "timestamp":  timestamp,
  "location_id": storeId,
  "loyalty_identity": {
    "id": member.loyaltyId
  },
  "item_list": [
    {
      "item_set": [eventName],
      "quantity": 1
    }
  ]
}
```

**输出Adobe忠诚度事件：**

```json
{
  "_id":        "evt-001",
  "event_name": "store-checkin",
  "timestamp":  "2025-10-15T14:22:00Z",
  "location_id": "STORE-042",
  "loyalty_identity": { "id": "LM-8827361" },
  "item_list": [{ "item_set": ["store-checkin"], "quantity": 1 }]
}
```

没有包含/排除限制的挑战任务会将此事件计为符合条件的访问 — 单个`item_set`条目`["store-checkin"]`与允许所有项目的任何任务匹配。

+++

+++示例2 — 包含行项目的POS购买

**方案：**&#x200B;销售点系统发送事务负载。 每个行项目都有一个SKU并且属于一个类别。 挑战任务使用SKU和类别来确定符合条件。

**传入事件：**

```json
{
  "_id":       "txn-20251015-4492",
  "timestamp": "2025-10-15T14:35:00Z",
  "storeInfo": {
    "storeId":   "STORE-042",
    "utcOffset": "-07:00"
  },
  "transaction": {
    "transactionId": "4492",
    "items": [
      { "sku": "COFFEE-001", "category": "BEVERAGE", "qty": 2, "unitPrice": 4.50, "lineTotal": 9.00 },
      { "sku": "MUFFIN-007", "category": "FOOD",     "qty": 1, "unitPrice": 3.25, "lineTotal": 3.25 }
    ]
  },
  "member": {
    "loyaltyId": "LM-8827361"
  }
}
```

**事件定义：**

```json
{
  "name":           "Retail POS Purchase",
  "identifierPath": "transaction.transactionId",
  "identifier":     [],
  "transformer":    "{\"_id\": _id, \"event_name\": \"purchase\", \"timestamp\": timestamp, \"utc_offset\": storeInfo.utcOffset, \"location_id\": storeInfo.storeId, \"transaction_id\": transaction.transactionId, \"loyalty_identity\": {\"id\": member.loyaltyId}, \"item_list\": transaction.items.{\"item_set\": [sku, category], \"quantity\": qty, \"unit_price\": unitPrice, \"sub_total\": lineTotal}}"
}
```

**格式化的转换器：**

```jsonata
{
  "_id":            _id,
  "event_name":     "purchase",
  "timestamp":      timestamp,
  "utc_offset":     storeInfo.utcOffset,
  "location_id":    storeInfo.storeId,
  "transaction_id": transaction.transactionId,
  "loyalty_identity": {
    "id": member.loyaltyId
  },
  "item_list": transaction.items.{
    "item_set":   [sku, category],
    "quantity":   qty,
    "unit_price": unitPrice,
    "sub_total":  lineTotal
  }
}
```

**输出Adobe忠诚度事件：**

```json
{
  "_id":            "txn-20251015-4492",
  "event_name":     "purchase",
  "timestamp":      "2025-10-15T14:35:00Z",
  "utc_offset":     "-07:00",
  "location_id":    "STORE-042",
  "transaction_id": "4492",
  "loyalty_identity": { "id": "LM-8827361" },
  "item_list": [
    { "item_set": ["COFFEE-001", "BEVERAGE"], "quantity": 2, "unit_price": 4.50, "sub_total": 9.00 },
    { "item_set": ["MUFFIN-007", "FOOD"],     "quantity": 1, "unit_price": 3.25, "sub_total": 3.25 }
  ]
}
```

具有`include: ["BEVERAGE"]`的质询任务将看到咖啡行项目符合条件（其`item_set`包含`"BEVERAGE"`）并累计9.00美元用于该任务。 将排除松饼行项目。

+++

+++示例3 — AEP Experience Event（XDM模式匹配）

**方案：**&#x200B;事件通过Adobe Journey Optimizer。 传入事件是具有已知架构ID的XDM体验事件。 平台使用架构ID进行匹配，而不是路径/值检查。

**传入XDM实体主体**（从AJO事件提取的`xdmEntity`）：

```json
{
  "_brandname": {
    "identities": {
      "loyaltyId": "LM-8827361"
    },
    "transactions": {
      "transactionId": "TXN-9901",
      "storeNumber":   "042",
      "utcOffset":     "-07:00",
      "lineItems": [
        { "skuNumber": "11143053", "priceAmount": 345, "qty": 1, "category": "BEVERAGE" },
        { "skuNumber": "11161387", "priceAmount": 495, "qty": 1, "category": "FOOD" }
      ],
      "totalAmount": 840
    }
  },
  "_id":       "87c0cccf-5809-38e0-a703-3994e80173ab",
  "timestamp": "2025-07-04T16:03:32.000Z"
}
```

**事件定义：**

```json
{
  "name":        "AJO Brand Purchase",
  "xdmSchemaId": "https://ns.adobe.com/brandname/schemas/purchase-event-v1",
  "transformer":  "{\"_id\": _id, \"event_name\": \"purchase\", \"timestamp\": timestamp, \"utc_offset\": _brandname.transactions.utcOffset, \"location_id\": _brandname.transactions.storeNumber, \"transaction_id\": _brandname.transactions.transactionId, \"loyalty_identity\": {\"id\": _brandname.identities.loyaltyId}, \"item_list\": _brandname.transactions.lineItems.{\"item_set\": [skuNumber, category], \"quantity\": qty, \"unit_price\": priceAmount, \"sub_total\": priceAmount * qty}}"
}
```

**格式化的转换器：**

```jsonata
{
  "_id":            _id,
  "event_name":     "purchase",
  "timestamp":      timestamp,
  "utc_offset":     _brandname.transactions.utcOffset,
  "location_id":    _brandname.transactions.storeNumber,
  "transaction_id": _brandname.transactions.transactionId,
  "loyalty_identity": {
    "id": _brandname.identities.loyaltyId
  },
  "item_list": _brandname.transactions.lineItems.{
    "item_set":   [skuNumber, category],
    "quantity":   qty,
    "unit_price": priceAmount,
    "sub_total":  priceAmount * qty
  }
}
```

> **注意：**&#x200B;当事件按XDM架构ID匹配时，转换器仅接收事件的`xdmEntity`部分，而不是外部AJO信封。 转换器表达式中的所有路径都相对于XDM实体主体。

+++

## 添加JSON架构验证（可选）

如果您希望平台在尝试转换之前验证传入事件的结构，请将`schema`字段设置为编码为JSON字符串的[JSON架构](https://json-schema.org/draft-04)文档。

架构验证失败的事件会在转换运行之前被拒绝。 错误响应包括特定的验证失败，因此很容易诊断格式错误的上游事件。

+++模式示例（例如上面的2个）

```json
{
  "$schema": "http://json-schema.org/draft-04/schema#",
  "type": "object",
  "required": ["_id", "timestamp", "transaction", "member"],
  "properties": {
    "_id":       { "type": "string" },
    "timestamp": { "type": "string", "format": "date-time" },
    "member": {
      "type": "object",
      "required": ["loyaltyId"],
      "properties": {
        "loyaltyId": { "type": "string" }
      }
    },
    "transaction": {
      "type": "object",
      "required": ["items"],
      "properties": {
        "transactionId": { "type": "string" },
        "items": {
          "type": "array",
          "items": {
            "type": "object",
            "required": ["sku", "qty", "lineTotal"],
            "properties": {
              "sku":       { "type": "string" },
              "category":  { "type": "string" },
              "qty":       { "type": "number" },
              "unitPrice": { "type": "number" },
              "lineTotal": { "type": "number" }
            }
          }
        }
      }
    }
  }
}
```

+++

在事件定义的`schema`字段中将此架构作为缩小的JSON字符串传递。

## 回退 — 本机忠诚度事件

如果没有事件定义与传入事件匹配，则平台会尝试将其直接摄取为本机Adobe忠诚度事件。 如果有效负载已符合上述忠诚度事件格式，则无需转换器，并且事件会按原样应用。 这允许已预格式化其事件的客户完全绕过转换。

## API 参考

所有事件定义操作都使用基本路径`/loyalty/metadata/config/events`。

+++创建事件定义

```http
POST /loyalty/metadata/config/events
x-gw-ims-org-id: {ORG_ID}
x-sandbox-name: {SANDBOX}
Content-Type: application/json

{
  "name":           "Retail POS Purchase",
  "identifierPath": "transaction.transactionId",
  "identifier":     [],
  "transformer":    "{ ... }"
}
```

+++

+++列出事件定义

```http
GET /loyalty/metadata/config/events
x-gw-ims-org-id: {ORG_ID}
x-sandbox-name: {SANDBOX}
```

+++

+++更新事件定义

```http
PUT /loyalty/metadata/config/events/{eventId}
x-gw-ims-org-id: {ORG_ID}
x-sandbox-name: {SANDBOX}
Content-Type: application/json

{
  "name":        "Retail POS Purchase (v2)",
  "transformer": "{ ... updated expression ... }"
}
```

+++

+++删除事件定义

```http
DELETE /loyalty/metadata/config/events/{eventId}
x-gw-ims-org-id: {ORG_ID}
x-sandbox-name: {SANDBOX}
```

+++

## 转换器验证

在保存事件定义时，将验证JSONata表达式的语法。 如果表达式无效，则API返回包含分析失败说明的`422`错误。

要在部署之前测试转换器，请使用[JSONata Exerciser](https://try.jsonata.org/) — 将源事件粘贴为输入，并粘贴转换器表达式以验证输出是否与预期的忠诚度事件格式匹配。

## 常见陷阱

这些错误都在一个简单的单项测试有效载荷上无错误地运行，这正是它们滑过未被检测到的原因。 在部署之前，请始终根据包含两个或更多产品的负载测试转换器。

+++构建一个对象而不是在数组上映射

最常见的错误。 将单个对象文字与`productListItems.SKU`结合使用会将每个SKU和每个数量提取到集总序列中，而不是为每个产品生成一个行项目。

**✗将所有项折叠为一个：**

```jsonata
"item_list": [
  {
    "item_set": [ productListItems.SKU ],
    "quantity": productListItems.quantity
  }
]
```

使用两个产品，`item_set`同时保存两个SKU，`quantity`将变为`[1, 4]`等数组。

**✓每个产品一个行项目：**

```jsonata
"item_list": [
  productListItems.{
    "item_set": [SKU],
    "quantity": quantity
  }
]
```

每个产品运行一次`.{ }`映射，因此每个产品都会成为自己的条目。

+++

+++忘记标识上的数组索引

`identityMap.Email`是一个数组。 如果没有`[0]`，则当配置文件在该命名空间中有多个标识时，`id`将变为值列表而不是单个字符串。

**✗** `identityMap.Email.id`

**✓** `identityMap.Email[0].id`

+++

+++从自定义租户字段获取身份

自定义字段组有时会公开电子邮件形式的字段，例如`_yourtenant.identification.core.email`。 在示例数据中，它会返回一个值并且看起来是正确的，但在生产事件中，它通常为空，从而导致`loyalty_identity.id`输出为null。 始终使用`identityMap`作为标识的来源。

+++

+++嵌套数组泄漏到`item_set`

将类别字段添加到`item_set`看起来很简单，但如果`productCategories`本身是一个数组，则结果将以不可预测的方式展开。

**✗生成的条目可能多于预期：**

```jsonata
"item_set": [SKU, productCategories.categoryID]
```

具有三个类别的产品会生成具有四个值的`item_set`。

**✓对嵌套数组编制索引，以仅获取一个值：**

```jsonata
"item_set": [SKU, productCategories[0].categoryID]
```

+++

+++`item_list`为空或缺失

具有空或不存在`item_list`的事件被拒绝为无效。 对于非事务性事件（签入、自定义触发器），不存在自然的行项目，因此请生成一个合成的行项目：

```jsonata
"item_list": [{ "item_set": [eventName], "quantity": 1 }]
```

+++

+++`timestamp`作为Unix纪元整数，而不是ISO 8601

该平台需要一个ISO 8601字符串。 如果您的源事件带有自纪元以来的毫秒数，请将其转换为：

```jsonata
"timestamp": $fromMillis(timestamp)
```

+++

+++已忽略`utc_offset`

如果没有`utc_offset`，则会跳过时段匹配和连续日期连续计数。 将存储或设备UTC偏移量映射到任何可用的源事件。

+++

+++DCCS事件中相对于AJO信封的转换器路径

对于DCCS事件，转换器仅接收`xdmEntity`主体，而不接收外部AJO信封。 所有路径都必须相对于XDM实体根。 如果表达式引用位于外部信封中的字段（例如`/body/xdmMeta/...`），则未找到这些字段，并将静默生成null。

+++
