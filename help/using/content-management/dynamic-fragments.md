---
solution: Journey Optimizer
product: journey optimizer
title: 使用动态片段
description: 了解如何在Adobe Journey Optimizer中使用动态片段解析，根据配置文件属性、数据集查找或上下文数据在运行时选择并插入片段。
feature: Fragments
topic: Content Management
role: User, Developer
level: Intermediate, Experienced
keywords: 动态，片段，表达式，个性化，运行时
source-git-commit: b4affc5b905236419928a65cd173173b49058827
workflow-type: tm+mt
source-wordcount: '1317'
ht-degree: 2%

---

# 使用动态片段 {#dynamic-fragments}

>[!BEGINSHADEBOX]

**在此页面上：**&#x200B;了解如何在Adobe Journey Optimizer中使用动态片段解析，根据在发送时传递的配置文件属性、数据集查找或上下文数据，选择在运行时插入到消息中的已发布片段。

>[!ENDSHADEBOX]

[!DNL Adobe Journey Optimizer]在运行时支持&#x200B;**动态片段解析**，允许您根据在发送时传递的配置文件属性、数据集查找或上下文数据选择将哪个已发布的片段插入到消息中。 这样可以在不复制营销活动或历程逻辑的情况下实现高度个性化的内容。

## 概述 {#overview}

**在设计时嵌入消息中的静态片段** — 每个收件人都使用相同的片段。 **动态片段**&#x200B;在运行时为每个收件人解析片段ID，这意味着不同的配置文件可以在同一营销活动或历程中接收完全不同的内容块。

动态片段ID可以来自三个源：

* **数据集查找** — 例如，按样式或产品键的推荐数据集
* 存储在Adobe Experience Platform中的&#x200B;**配置文件属性**
* 在发送时直接在API请求中传递了&#x200B;**上下文数据**

>[!NOTE]
>
>目前在表达式片段中使用`datasetLookup`帮助程序函数仅适用于有限的一组客户。 要获得访问权限，请与 Adobe 代表联系。

## 先决条件 {#prerequisites}

在使用动态片段之前，请确保已具备以下条件：

* 您具有在[!DNL Journey Optimizer]中创建和发布片段所需的权限。 [了解详情](../administration/ootb-product-profiles.md#content-library-manager)
* 您打算引用的片段是&#x200B;**已发布** （状态： **实时**）。 运行时无法解析草稿片段。
* 如果从数据集解析片段ID，则数据集架构包含存储片段ID的字段，并且数据集已[启用查找](../data/lookup-aep-data.md)。
* 动态片段本身引用的所有用户档案属性都包含在消息导出路径中，或者在发送时可在用户档案中使用。

>[!CAUTION]
>
>在动态片段流中跳过与片段相关的验证。 片段ID无效显示为运行时投放失败，而不是预先验证错误。 在激活营销活动之前，请始终验证引用的片段ID是否有效且已发布。

## 步骤1：创建和发布片段 {#create-fragment}

在动态引用片段之前，必须在[!DNL Journey Optimizer]中发布该片段。

1. 在[!DNL Journey Optimizer]中，导航到&#x200B;**[!UICONTROL 内容管理]** > **[!UICONTROL 片段]**。

1. 选择&#x200B;**[!UICONTROL 创建片段]**&#x200B;并创作内容。 [了解如何创建片段](create-fragments.md)

1. 内容就绪后，单击&#x200B;**[!UICONTROL 发布]**。 发布是异步的，可能需要几秒钟。 在继续之前，请确认片段状态更改为&#x200B;**实时**。

1. 记下片段详细信息视图或片段API响应中的&#x200B;**片段ID**。 您将在消息中引用此ID。

>[!NOTE]
>
>您可以使用`GET /fragments` API以编程方式检索所有已发布的片段ID。 有关详细信息，请参阅[Journey Optimizer API文档](https://developer.adobe.com/journey-optimizer-apis/references/content){target="_blank"}。

## 步骤2：使用动态片段引用创作消息 {#author-message}

在个性化编辑器中，使用以下语法插入动态片段占位符：

```handlebars
{{fragment id=dynamic_fragment_id}}
```

标识符`dynamic_fragment_id`是变量名称。 必须在进行片段查找之前解析其值。 您可以使用数据集查找表达式、配置文件属性或上下文数据解决此问题。

### 从数据集查找中解析 {#resolve-from-dataset}

如果片段ID存储在AEP数据集中（例如，样式到片段映射表），请使用`datasetLookup`帮助程序函数进行解析：

```handlebars
{{
  {datasetLookup datasetId="<your-dataset-id>" key=profile.style attribute="fragmentId"}
}}

{{fragment id=dynamic_fragment_id}}
```

在此示例中，数据集包含由样式值（如`style1`）键入的行。 对于给定的配置文件，查找将检索相应的`fragmentId`列值并将其分配给`dynamic_fragment_id`，然后使用该值解析片段。

>[!NOTE]
>
>目前在表达式片段中使用`datasetLookup`帮助程序函数仅适用于有限的一组客户。 要获得访问权限，请与 Adobe 代表联系。 有关个性化中的数据集查找的更多信息，请参阅[使用Adobe Experience Platform数据](../data/lookup-aep-data.md)。

### 从上下文数据解析 {#resolve-from-context}

如果片段ID在发送时作为API请求上下文的一部分提供，请使用`context`命名空间引用它：

```handlebars
{{fragment id=context.audiencePayload.fragmentId}}
```

路径`context.audiencePayload`是所有属性的必需前缀，这些属性来自CSV受众文件或通过API请求上下文传递。 CSV中的列名称（例如，`fragmentId`）在前缀之后。

### 从配置文件属性中解析 {#resolve-from-profile}

如果片段ID作为配置文件属性存储在Adobe Experience Platform中，请直接引用它：

```handlebars
{{fragment id=profile.mi.fragmentId}}
```

## 步骤3：为查找方法配置数据集 {#configure-dataset}

如果您使用数据集查找方法，请更新您的数据集架构和数据以携带片段ID。

1. 在推荐或映射数据集中，添加列（例如，`fragmentId`）以存储每行的已发布AJO片段ID。

1. 对于每个样式或变体（例如，`style1`、`style2`），使用相应的片段ID填充`fragmentId`列。

1. 确保已将数据集摄取到Adobe Experience Platform并[启用查找](../data/lookup-aep-data.md)。

1. 确认在动态片段中引用的所有配置文件属性都捕获在消息中或静态片段中，以防止在导出时呈现为空。

**示例数据集结构：**

| 列 | 示例值 |
|---|---|
| 样式 | style1 |
| fragmentId | &lt;fragment-id-1> |
| 样式 | style2 |
| fragmentId | &lt;fragment-id-2> |

## 步骤4：在发送时传递上下文数据 {#pass-context-data}

如果您要从上下文数据解析片段ID（例如，从CSV受众推荐文件），请在API请求中用所需的上下文前缀传递片段ID。

使用营销活动验证API时，请在`context`对象中包含片段ID：

```json
{
  "recipients": [
    {
      "userId": "<profile-email>",
      "namespace": "email"
    }
  ],
  "inChannelData": {
    "channel": "email",
    "emailAddresses": ["<delivery-address>"]
  },
  "context": {
    "audiencePayload": {
      "fragmentId": "<published-fragment-id>",
      "systemSource": "<optional-system-value>"
    }
  }
}
```

需要前缀`context.audiencePayload`。 运行实时营销活动时，嵌套在此键下的属性直接映射到CSV受众文件中的列。

## 步骤5：验证和验证 {#proof-validate}

在激活营销活动之前，请使用营销活动验证API来验证动态片段是否正确解析，以及呈现的电子邮件输出是否与预期一致。

1. 使用`POST /campaigns/{id}/proofs`终结点触发验证作业。 在验证请求中，传递您要在`context.audiencePayload.fragmentId`下测试的片段ID。

1. 使用`GET /campaigns/{id}/proofs/{proofId}`终结点轮询校对作业状态，直到状态为`Submitted`或`Failed`。

1. 检查已投放的电子邮件，验证是否呈现了正确的片段内容。

1. 如果片段内容缺失或不正确，请验证片段ID是否有效，片段是否已发布，以及所有必需的配置文件属性是否存在。

有关Campaign API的更多信息，请参阅[Journey Optimizer API文档](https://developer.adobe.com/journey-optimizer-apis/references/campaigns-retrieve){target="_blank"}。

## 护栏和限制 {#guardrails}

>[!CAUTION]
>
>没有为动态片段模型中的片段强制使用OLAC（对象级访问控制）。 确保在营销活动和受众级别考虑您的访问控制要求。

以下限制适用于使用动态片段的情况：

* **导出时的配置文件属性覆盖率**：在运行时为每个配置文件选择片段。 动态片段所需的配置文件属性事先未知。 如果动态片段所依赖的用户档案属性不在原始消息或消息引用的任何静态片段中，则该字段可能会在导出路径中呈现为空。

* **无前端片段验证**：此流中跳过与片段相关的验证。 不正确或未发布的片段ID显示为运行时投放失败，而不是UI中显示的验证错误。

* **数据集方法所需的架构更改**：使用lookup-by-ID路径需要更新数据集架构以存储和传递片段ID，以及将其馈送到消息管道所需的管道。

* 用于导出的&#x200B;**属性捕获**：确保在消息或静态片段中捕获动态片段中使用的所有属性，以防止导出路径中的呈现为空。

[此部分](../start/guardrails.md#fragments-guardrails)中有更多适用于片段的护栏。

## 错误处理 {#error-handling}

如果动态片段在运行时无法解析，则会为受影响的配置文件生成排除事件。 目前，所有片段渲染失败都归类为单个一揽子错误类型。

要调试片段解析失败，请执行以下操作：

1. 检查活动投放报告以了解排除事件。
1. 验证运行时传递的片段ID是否与发布的片段匹配。
1. 确认在发送时，片段所需的所有配置文件属性都存在于配置文件中。
1. 在激活营销活动之前，使用[验证API](#proof-validate)测试特定片段ID。
