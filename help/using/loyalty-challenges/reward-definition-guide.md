---
solution: Journey Optimizer
product: journey optimizer
title: 奖励定义指南
description: 了解如何在Adobe Journey Optimizer中为“忠诚度挑战”奖励提供商配置奖励定义。
feature: Journeys
topic: Content Management
role: Admin
level: Intermediate
hide: true
badge: label="私人测试版" type="Informative"
mini-toc-levels: 1
exl-id: 9b0fd9d8-18d1-4a51-8b6f-b2e2a4c6f1d7
feature_v2: []
subfeature_v2: []
source-git-commit: 00c24e9b97b4f6597048731858f3bfbcb39a0030
workflow-type: tm+mt
source-wordcount: 1206
ht-degree: 3%

---

# 奖励定义指南 {#reward-definition-guide}

>[!CONTEXTUALHELP]
>id="ajo_loyalty_reward_definition"
>title="奖励定义指南"
>abstract="使用本指南配置忠诚度奖励提供商的奖励定义，包括默认定义行为和履行有效负荷字段。"

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
* **奖励定义指南** ◀&rbrace;︎**您在这里**
* [Event Transformer指南](event-transformer-guide.md)
* [忠诚度数据和数据集](loyalty-data-and-datasets.md)
* [忠诚度挑战API参考](https://developer.adobe.com/journey-optimizer-apis/references/loyalty-challenges){target="_blank"}

</td>
</tr>
</table>

>[!ENDSHADEBOX]

>[!AVAILABILITY]
>
>此功能当前处于&#x200B;**私人测试版**&#x200B;中。 有关[!DNL Journey Optimizer]中发行周期和可用性阶段的完整详细信息，请参阅[发行周期](../rn/releases.md)。

当质询任务、里程碑或质询完成&#x200B;**并配置奖励值**&#x200B;时，平台将通过使用JSON有效负载调用奖励提供商的HTTP端点来发出奖励。 **奖励定义**&#x200B;描述了问题的奖励，并提供了一个[JSONata](https://docs.jsonata.org/overview)表达式 — `rewardJsonata` — 该表达式可形成您的提供商期望的确切有效负载。

本指南介绍如何配置奖励提供者、创建奖励定义、编写`rewardJsonata`表达式以及了解在评估时可供其使用的上下文。

## 两级模型

奖励分为两个级别：

```
Reward Provider  (endpoint, auth, headers)
└── Reward Definition  (denomination, rewardJsonata)
└── Reward Definition
└── ...
```

**奖励提供程序**&#x200B;表示单个外部奖励系统 — 它包含投放端点URL、身份验证和任何自定义HTTP标头。 一个提供商可以保存多个&#x200B;**奖励定义**，每个定义描述该提供商提供的不同奖励类型或面额（例如“50颗星”、“双颗星”、“免费项目”）。

质询通过GUID引用提供程序和定义。 当发出奖励时，平台将评估定义的`rewardJsonata`表达式，并将结果POST到提供程序的端点。

## 奖励提供者和定义字段

+++奖励提供者字段

<table>
<colgroup>
<col style="width:160px">
<col style="width:80px">
<col style="width:160px">
<col>
</colgroup>
<tr><th>字段</th><th>类型</th><th>必需</th><th>描述</th></tr>
<tr><td><code>guid</code></td><td><code>String</code></td><td>否（系统分配）</td><td>唯一标识符。 只读。</td></tr>
<tr><td><code>name</code></td><td><code>String</code></td><td><strong>是</strong></td><td>显示名称，在组织内唯一。</td></tr>
<tr><td><code>desc</code></td><td><code>String</code></td><td>否</td><td>易于用户识别的提供商描述。</td></tr>
<tr><td><code>enabled</code></td><td><code>Boolean</code></td><td>否</td><td>当<code>false</code>时，已针对此提供程序下的所有定义暂停奖励投放<br>。</td></tr>
<tr><td><code>url</code></td><td><code>String</code></td><td><strong>是</strong></td><td>接收奖励有效负载的HTTP端点。<br>平台POST将评估的<br><code>rewardJsonata</code>输出输出输出输出到此URL。</td></tr>
<tr><td><code>additionalHeaders</code></td><td><code>Object</code></td><td>否</td><td>要包含在每<br>个投放请求中的自定义HTTP标头（例如API密钥、<br>内容类型覆盖）。</td></tr>
<tr><td><code>maxRatePerSecond</code></td><td><code>Integer</code></td><td>否</td><td>可选的每提供程序速率限制(1-5000)。<br>Null表示无限制。</td></tr>
<tr><td><code>enableMTLS</code></td><td><code>Boolean</code></td><td>否</td><td>端点是否需要双向TLS。</td></tr>
</table>

+++

+++奖励定义字段

<table>
<colgroup>
<col style="width:160px">
<col style="width:80px">
<col style="width:160px">
<col>
</colgroup>
<tr><th>字段</th><th>类型</th><th>必需</th><th>描述</th></tr>
<tr><td><code>guid</code></td><td><code>String</code></td><td>否（系统分配）</td><td>唯一标识符。 只读。</td></tr>
<tr><td><code>name</code></td><td><code>String</code></td><td><strong>是</strong></td><td>显示名称，在提供程序中唯一。</td></tr>
<tr><td><code>denomination</code></td><td><code>String</code></td><td>否</td><td>奖励的单位，用于显示<br>，在表达式中为<br><code>reward.denomination</code><br>（例如<code>"Stars"</code>、<code>"Points"</code>、<code>"Miles"</code>）。</td></tr>
<tr><td><code>desc</code></td><td><code>String</code></td><td>否</td><td>奖励的说明，在表达式中以<code>reward.desc</code>形式提供<br>。</td></tr>
<tr><td><code>enabled</code></td><td><code>Boolean</code></td><td>否</td><td>当<code>false</code>时，此定义处于非活动状态<br>并且不会发出奖励。</td></tr>
<tr><td><code>isDefault</code></td><td><code>Boolean</code></td><td>否</td><td>将此项标记为沙盒范围的默认<br>奖励定义。 一次只能对所有提供程序使用一个定义<br>作为默认值；<br>设置新的默认值会清除上一个定义。<br>用于在发布时自动填充<br>个性化挑战的奖励详细信息。</td></tr>
<tr><td><code>rewardJsonata</code></td><td><code>String</code></td><td><strong>是</strong></td><td>JSONata表达式在<br>reward-issue时间进行计算。 接收完整的<br>奖励上下文，并且必须将JSON<br>有效负载返回给POST提供程序。</td></tr>
</table>

+++

## 奖励上下文

评估`rewardJsonata`时，它会收到一个包含奖励事件已知所有内容的根对象。 表达式中的所有路径都与此根相关。

```json
{
  "rewardContext": {
    "rewardValue": "50",
    "source":      "challenge"
  },
  "reward": {
    "name":         "500 Stars",
    "desc":         "Issue 500 Stars to the member",
    "denomination": "Stars",
    "enabled":      true
  },
  "task": { ... },
  "milestone": { ... },
  "challenge": { ... },
  "timestamp": "2026-02-10T00:29:22.538+00:00"
}
```

+++ 上下文字段

| 字段 | 描述 |
|----------------------------------------|-------------|
| `rewardContext.rewardValue` | 在触发此发布的挑战、任务或里程碑上配置的奖励值字符串。 |
| `rewardContext.source` | 触发奖励的内容： `"task"`、`"challenge"`或`"milestone"`。 |
| `reward` | RewardDefinition本身 — `name`、`desc`、`denomination`。 |
| `task` | 正在完成任务，包括其`accumulators`、`schedule`和`reward`。 |
| `task.accumulators.spend` | 任务累计的符合条件的总支出。 |
| `task.accumulators.qty` | 任务累计的合格项目总数。 |
| `task.accumulators.item_list` | 应用于任务的所有符合条件的项目。 每个条目都有`item`、`transactionId`、`timestamp`、`utcOffset`、`locationId`。 |
| `task.accumulators.item_list[-1]` | 应用的最新项目（JSONata负索引）。 对于来源补充最后一个交易ID或时间戳非常有用。 |
| `task.schedule.currentStreak` | 当前连续访问连续计数（针对连续挑战）。 |
| `task.schedule.currentVisits` | 总访问计数（针对访问挑战）。 |
| `milestone` | 触发此奖励的里程碑，或者`null`（如果不是里程碑奖励）。 包括`count`和`reward.rewardValue`。 |
| `challenge.profileId` | 成员的忠诚度ID。 |
| `challenge.kvpCustom` | 在挑战中配置的自定义键值对。 用于传递促销活动ID、产品名称或特定于提供商的元数据的常见模式。 |
| `challenge.name` | 质询名称。 |
| `challenge._id` | 挑战ID。 |
| `timestamp` | 奖励发放的ISO 8601时间戳。 |

+++

## 编写rewardJsonata表达式

表达式接收奖励上下文作为其输入，并且必须返回一个JSON对象，该对象有效负载已发布到提供程序的端点。 该对象的形状完全取决于提供程序的API；您可以将上下文字段映射到提供程序期望的任何结构。

+++简单固定负载

最简单的情况是：提供程序需要点数和成员ID，两者均从上下文知道。

```jsonata
{
  "memberId":   challenge.profileId,
  "points":     $number(rewardContext.rewardValue),
  "currency":   reward.denomination
}
```

**输出：**

```json
{
  "memberId": "ADB-0000030",
  "points":   50,
  "currency": "Stars"
}
```

> `rewardContext.rewardValue`始终为字符串。 如果您的提供商需要数字值，请使用`$number()`进行转换。

+++

+++将`kvpCustom`用于特定于提供商的元数据

提供商通常需要活动ID或源代码等字段，这些字段特定于每个质询运行。 创作挑战时将这些内容存储在`challenge.kvpCustom`中，然后在表达式中引用它们 — 保持表达式可跨营销活动重复使用。

```jsonata
{
  "memberId":         challenge.profileId,
  "points":           $number(rewardContext.rewardValue),
  "campaignId":       challenge.kvpCustom.campaignId,
  "transactionSource": "AJO"
}
```

您还可以将`reward.kvpCustom`用于固定为给定奖励类型而不是每个质询的常量。

+++

+++使用任务累加器数据

任务累计器保存每个合格事件的记录。 使用`item_list[-1]`访问最近应用的项 — 它的`transactionId`和`timestamp`对于提供程序端的审核跟踪和重复数据删除非常有用。

```jsonata
{
  "memberId":       challenge.profileId,
  "points":         $number(rewardContext.rewardValue),
  "transactionId":  task.accumulators.item_list[-1].transactionId,
  "transactionDate": task.accumulators.item_list[-1].timestamp
}
```

+++

+++构造文本消息

对于基于通知的提供商（Slack、短信、电子邮件），您可以使用JSONata的`&`连接运算符直接构建消息字符串：

```jsonata
{
  "text": "You just earned " & rewardContext.rewardValue & " " & reward.denomination & "!"
}
```

**输出：**

```json
{
  "text": "You just earned 50 Stars!"
}
```

+++

## 示例

+++示例1 — 简单点提供程序

**方案：**&#x200B;基本会员积分API需要成员ID和点数。

**奖励定义：**

```json
{
  "name":         "Standard Points",
  "denomination": "Points",
  "desc":         "Award loyalty points",
  "enabled":      true,
  "rewardJsonata": "{\"memberId\": challenge.profileId, \"pointQuantity\": $number(rewardContext.rewardValue), \"denomination\": reward.denomination}"
}
```

**格式化的表达式：**

```jsonata
{
  "memberId":      challenge.profileId,
  "pointQuantity": $number(rewardContext.rewardValue),
  "denomination":  reward.denomination
}
```

**有效负载发布到提供程序：**

```json
{
  "memberId":      "ADB-0000030",
  "pointQuantity": 50,
  "denomination":  "Points"
}
```

+++

+++示例2 — 包含营销活动元数据的提供程序有效负载

**方案：**&#x200B;提供商需要包含审核字段、营销活动引用和成员描述的结构化奖励记录。 促销活动特定的值存储在`challenge.kvpCustom`中，因此相同的奖励定义可以在促销活动之间使用，而无需编辑表达式。

**挑战`kvpCustom`**（创作挑战时设置）：

```json
{
  "parentCampaignId": "CAMP-2026-Q1",
  "productName":      "Loyalty Program"
}
```

**奖励定义：**

```json
{
  "name":         "Stars — Campaign Award",
  "denomination": "Stars",
  "desc":         "Issue Stars for completing a qualifying purchase",
  "enabled":      true,
  "rewardJsonata": "{\"awardPoints\":[{\"idType\":\"externalId\",\"id\":challenge.profileId,\"transactionId\":task.accumulators.item_list[-1].transactionId,\"transactionDate\":task.accumulators.item_list[-1].timestamp,\"originalTransactionId\":task.accumulators.item_list[-1].transactionId,\"transactionSource\":\"AJO\",\"channelSource\":\"Web\",\"parentCampaignId\":challenge.kvpCustom.parentCampaignId,\"productName\":challenge.kvpCustom.productName,\"memberAwardDescription\":reward.desc,\"pointQuantity\":$number(rewardContext.rewardValue)}]}"
}
```

**格式化的表达式：**

```jsonata
{
  "awardPoints": [
    {
      "idType":                "externalId",
      "id":                    challenge.profileId,
      "transactionId":         task.accumulators.item_list[-1].transactionId,
      "transactionDate":       task.accumulators.item_list[-1].timestamp,
      "originalTransactionId": task.accumulators.item_list[-1].transactionId,
      "transactionSource":     "AJO",
      "channelSource":         "Web",
      "parentCampaignId":      challenge.kvpCustom.parentCampaignId,
      "productName":           challenge.kvpCustom.productName,
      "memberAwardDescription": reward.desc,
      "pointQuantity":         $number(rewardContext.rewardValue)
    }
  ]
}
```

**有效负载发布到提供程序：**

```json
{
  "awardPoints": [
    {
      "idType":                "externalId",
      "id":                    "ADB-0000030",
      "transactionId":         "b4fa0e89-f4bb-41ce-b370-fb97f9c52f1a",
      "transactionDate":       "2026-02-08T00:12:00.000+00:00",
      "originalTransactionId": "b4fa0e89-f4bb-41ce-b370-fb97f9c52f1a",
      "transactionSource":     "AJO",
      "channelSource":         "Web",
      "parentCampaignId":      "CAMP-2026-Q1",
      "productName":           "Loyalty Program",
      "memberAwardDescription": "Issue Stars for completing a qualifying purchase",
      "pointQuantity":         50
    }
  ]
}
```

+++

+++示例3 — 里程碑奖励

**情景：** Streak质询每N次访问就发出一个里程碑式奖励。 表达式包括里程碑计数和提供程序端上下文的当前条纹。

**格式化的表达式：**

```jsonata
{
  "memberId":       challenge.profileId,
  "points":         $number(rewardContext.rewardValue),
  "milestoneCount": milestone.count,
  "currentStreak":  task.schedule.currentStreak,
  "denomination":   reward.denomination,
  "source":         rewardContext.source
}
```

**有效负载发布到提供程序**（在第2次访问里程碑）：

```json
{
  "memberId":       "ADB-0000030",
  "points":         20,
  "milestoneCount": 2,
  "currentStreak":  2,
  "denomination":   "Stars",
  "source":         "milestone"
}
```

> 当`rewardContext.source`为`"milestone"`时，`milestone`对象已填充`count`和`reward.rewardValue`。 当源为`"task"`或`"challenge"`时，`milestone`为`null`。

+++

## API 参考

+++奖励提供者

```http
POST   /loyalty/metadata/config/rewards/providers
GET    /loyalty/metadata/config/rewards/providers
GET    /loyalty/metadata/config/rewards/providers/{providerId}
PUT    /loyalty/metadata/config/rewards/providers/{providerId}
DELETE /loyalty/metadata/config/rewards/providers/{providerId}
```

所有请求都需要`x-gw-ims-org-id`和`x-sandbox-name`标头。

**创建提供程序：**

```http
POST /loyalty/metadata/config/rewards/providers
x-gw-ims-org-id: {ORG_ID}
x-sandbox-name: {SANDBOX}
Content-Type: application/json

{
  "name":    "My Points Provider",
  "desc":    "Issues loyalty points via REST",
  "enabled": true,
  "url":     "https://rewards.example.com/award",
  "additionalHeaders": {
    "x-api-key": "YOUR_API_KEY"
  }
}
```

+++

+++奖励定义

```http
POST   /loyalty/metadata/config/rewards/definitions/{providerId}
GET    /loyalty/metadata/config/rewards/definitions/{providerId}
GET    /loyalty/metadata/config/rewards/definitions/{providerId}/{rewardId}
PUT    /loyalty/metadata/config/rewards/definitions/{providerId}/{rewardId}
DELETE /loyalty/metadata/config/rewards/definitions/{providerId}/{rewardId}
```

**创建奖励定义：**

```http
POST /loyalty/metadata/config/rewards/definitions/{providerId}
x-gw-ims-org-id: {ORG_ID}
x-sandbox-name: {SANDBOX}
Content-Type: application/json

{
  "name":         "50 Stars",
  "denomination": "Stars",
  "desc":         "Award 50 Stars on task completion",
  "enabled":      true,
  "rewardJsonata": "{ \"memberId\": challenge.profileId, \"points\": $number(rewardContext.rewardValue) }"
}
```

+++

## 表达式验证

`rewardJsonata`表达式在发布时进行了语法验证。 如果表达式无效，则API返回包含分析失败说明的`422`错误。

若要在发布之前开发和测试表达式，请使用[JSONata Exerciser](https://try.jsonata.org/)。 将奖励上下文JSON粘贴为输入文档和您的表达式，以验证输出是否与提供商的期望相匹配。 上述示例中显示了每个触发器类型(`task`、`milestone`、`challenge`)的代表性奖励上下文。

## 常见错误

| 错误 | 效果 | 修复 |
|---------|--------|-----|
| `rewardContext.rewardValue`用作无转换的数字 | 如果提供程序验证字段是否为数字，则类型不匹配 | 使用`$number(rewardContext.rewardValue)`换行 |
| `challenge.kvpCustom.someKey`返回空值 | 创作时未对质询设置键 | 确保在使用此定义的每个质询上的`kvpCustom`中存在密钥 |
| `task.accumulators.item_list[-1]`为空 | 在发放奖励之前没有应用任何项目（非购买事件） | 带条件的护卫或改用上下文中的`timestamp` |
| `milestone`在源为`"task"`或`"challenge"`时访问 | `milestone`为null；表达式抛出或生成null字段 | 在访问`milestone`之前检查`rewardContext.source`，或仅在附加到里程碑奖励的定义中使用`milestone` |
| 表达式返回数组而不是对象 | 提供程序接收意外的负载结构 | 将返回数组的表达式包装在外对象中： `{ "items": [...] }` |
