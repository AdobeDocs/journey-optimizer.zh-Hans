---
title: 在历程中使用补充标识符
description: 了解如何在历程中使用补充标识符。
exl-id: f6ebd706-4402-448a-a538-e9a4c2cf0f8b
version: Journey Orchestration
TQID: https://experienceleague.adobe.com/ABOlJ-ZF0a3xLNY-hH6jjFqu53ph4PynNalGkgQ6P8k
product_v2:
  - id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2:
  - id: b3538224-471e-4c63-a444-9b19d89ae29c
  - id: d998adac-2f81-400b-a669-d07bb196e4eb
subfeature_v2:
  - id: d08afb72-92f6-4856-88e3-11ec34313c2f
  - id: fa683eda-48de-4558-af32-2673edcd44fe
topic_v2:
  - id: c7d04a2c-412a-4c9d-9d7a-4456eaa5adeb
  - id: e0eb8757-182f-49f3-94a4-1587d16f5094
source-git-commit: a5d9be4fcfcb52bb1ee65096262e18feaa2ce4b1
workflow-type: tm+mt
source-wordcount: 2041
ht-degree: 3%

---

# 在历程中使用补充标识符 {#supplemental-id}

>[!BEGINSHADEBOX]

**在此页面上：**&#x200B;了解如何使用补充标识符（订单或预订ID等辅助标识符）为每个标识符运行单独的历程实例，并使用其属性个性化消息。

>[!ENDSHADEBOX]

>[!CONTEXTUALHELP]
>id="ajo_journey_parameters_supplemental_identifier"
>title="使用补充标识符"
>abstract="补充标识符是辅助标识符，可为历程的执行提供额外的背景信息。 要定义该标识符，请从受众或事件中选择任意非身份属性（或非个人身份标识）作为补充标识符。"

<table style="border-collapse: collapse; width: 100%;">
  <tr>
    <td style="vertical-align: top; padding-right: 20px; border: none;">
      <p>默认情况下，历程在<b>配置文件ID</b>的上下文中执行。这意味着，只要用户档案在给定历程中处于活动状态，它就无法重新进入另一个历程。为防止出现这种情况，Journey Optimizer允许您在配置文件ID之外捕获<b>补充标识符</b>，例如订单ID、订阅ID、处方ID。  
      <p>在此示例中，我们已添加<b>预订ID</b>作为补充标识符。</p>
      <p>这样，历程会在与补充标识符关联的用户档案ID（此处为预订ID）的上下文中执行。 为补充标识符的每个迭代执行历程的一个实例。 如果访客进行了不同的预订，这将允许历程中出现多个相同用户档案ID的入口。</p>
      <p>此外，Journey Optimizer允许您利用补充标识符的属性（例如，预订编号、处方续订日期、产品类型）进行消息自定义，从而确保高度相关的通信。</p>
    </td>
    <td style="vertical-align: top; border: none; text-align: center; width: 40%;">
      <img src="assets/event-supplemental-id.png" alt="补充标识符示例" style="max-width:100%;" />
    </td>
  </tr>
</table>

➡️ [通过观看视频了解此功能](#video)

## 护栏和限制 {#guardrails}

* **支持的历程**： **事件触发的**&#x200B;和&#x200B;**读取受众**&#x200B;历程支持补充标识符。 对于受众资格历程（即以受众资格活动开始的历程），它们&#x200B;**不支持**。

* **入站操作**：当前不支持对入站操作（如应用程序内操作和Web操作）使用补充标识符。

* **并发实例限制**：配置文件不能包含超过10个并发历程实例。

* **数据类型和架构结构**：补充标识符的类型必须为`string`。 它可以是独立的字符串属性，也可以是对象数组中的字符串属性。 独立的字符串属性将生成单个历程实例，而对象数组中的字符串属性将生成每个对象数组的迭代的唯一历程实例。 不支持字符串数组和映射。

* **历程重新进入**

  补充标识符的历程重入行为遵循现有的重入策略：

   * 如果历程是非可重新进入的，则相同的配置文件ID +补充ID组合无法重新进入历程。
   * 如果历程通过时间窗口重新进入，则可以在定义的时间窗口后重新输入相同的配置文件ID +补充ID组合。

* **数据使用标签和执行(DULE)** — 不对补充ID执行DULE验证检查。 这意味着在历程查找数据治理策略违规时，不会考虑此属性。

* **下游事件配置**

  如果您在历程的下游使用另一个事件，则必须使用相同的补充ID并具有相同的ID命名空间。

* **读取受众历程**

   * **业务事件**：如果您使用业务事件，则补充数据ID被禁用。
   * **事件和上下文字段**：补充标识符不能来自事件或历程上下文字段。
   * **属性选择**：任何非标识属性（或非人员标识）都可以用作所有受众类型（统一配置文件服务、CSV导入和联合受众合成）的补充ID。 不允许基于人员的身份属性。 对于外部受众，请参阅[外部受众的补充标识符](#external-audiences)以了解支持的数据模式和配置要求。
   * **读取率**：对于使用数组类型补充ID字段的读取受众历程，读取受众活动的读取率限制为每秒500个配置文件的最大值。

## 具有补充ID的退出标准行为 {#exit-criteria}

前提条件：为补充ID启用了历程（通过单一事件或读取受众活动）

下表说明了配置退出标准时，配置文件在启用了ID的补充历程中的行为：

| 退出标准配置 | 满足退出条件时的行为 |
| ---------------------------- | ---------------------------------- |
| 基于非补充ID事件 | 将退出该历程中相应用户档案的所有实例。 |
| 基于补充ID事件&#x200B;<br/>*注意：补充ID命名空间必须与初始节点的命名空间匹配。* | 仅退出匹配的配置文件+补充ID实例。 |
| 基于受众 | 将退出该历程中相应用户档案的所有实例。 |

## 添加补充标识符并在历程中利用它 {#add}

>[!BEGINTABS]

>[!TAB 事件触发的历程]

要在事件触发的历程中使用补充标识符，请执行以下步骤：

1. **将补充ID添加到事件**

   1. 创建或编辑所需的事件。 [了解如何配置单一事件](../event/about-creating.md)

   1. 在事件配置屏幕中，选中&#x200B;**[!UICONTROL Use supplemental identifier]**&#x200B;选项。

      具有补充标识符选项的![事件配置](assets/supplemental-ID-event.png)

   1. 使用表达式编辑器选择要用作补充ID的字段（例如，预订ID、订阅ID）。

      >[!NOTE]
      >
      >确保在&#x200B;**[!UICONTROL 高级模式]**&#x200B;中使用表达式编辑器来选择属性。

1. **将事件添加到历程**

   将已配置事件拖到历程画布上。 它会根据用户档案ID和补充ID触发历程条目。

   ![历程使用补充标识符触发](assets/supplemental-ID-journey.png)

>[!TAB 读取受众历程]

要在读取受众历程中使用补充标识符，请执行以下步骤：

1. **在历程中添加和配置读取受众活动**

   1. 在历程中拖动&#x200B;**[!UICONTROL 读取受众]**&#x200B;活动。

   1. 在活动属性窗格中，打开&#x200B;**[!UICONTROL 使用补充标识符]**&#x200B;选项。

      ![读取具有补充标识符配置的受众活动](assets/supplemental-ID-read-audience.png)

   1. 在&#x200B;**[!UICONTROL 补充标识符]**&#x200B;字段中，使用表达式编辑器选择补充标识符属性。

   对于从CSV文件[&#128279;](https://experienceleague.adobe.com/docs/experience-platform/segmentation/ui/overview.html#import-audience){target="_blank"}导入的受众，如果您的CSV受众在每个配置文件ID中包含多行，请确保首先启用Express激活 — 请参阅[外部受众的补充标识符](#external-audiences)。

       >[！NOTE]
       >
       >请确保在&#x200B;**[!UICONTROL 高级模式]**&#x200B;中使用表达式编辑器来选择属性。
   
>[!ENDTABS]

## 利用补充ID属性

使用表达式编辑器和个性化编辑器为个性化或条件逻辑引用补充标识符的属性。 可从&#x200B;**[!UICONTROL 上下文属性]**&#x200B;菜单访问属性。

![Personalization编辑器显示内容的补充标识符字段](assets/supplemental-ID-perso.png)

对于事件触发的历程，如果您使用数组（例如，多个处方或策略），请使用公式来提取特定元素。

+++ 查看示例

在补充ID为`bookingNum`且属性位于同一级别`bookingCountry`的对象数组中，历程将根据bookingNum遍历数组对象，并为每个对象创建历程实例。

* 条件活动中的以下表达式将遍历对象数组，并检查`bookingCountry`的值是否等于“FR”：

  ```
  @event{<event_name>.<object_path>.<object_array_name>.all(currentEventField.<attribute_path>.bookingNum==${supplementalId}).at(0).<attribute_path>.bookingCountry}=="FR"
  ```

* 电子邮件个性化编辑器中的以下表达式将遍历对象数组，提取适用于当前历程实例的`bookingCountry`，并将其显示在内容中：

  ```
  {{#each context.journey.events.<event_ID>.<object_path>.<object_array_name> as |l|}} 
  
  {%#if l.<attribute_path>.bookingNum = context.journey.technicalProperties.supplementalId%} {{l.<attribute_path>.bookingCountry}}  {%/if%}
  
  {{/each}}
  ```

* 用于触发历程的事件示例：

  ```
  "bookingList": [
        {
            "bookingInfo": {
                "bookingNum": "x1",
                      "bookingCountry": "US"
            }
        },
        {
            "bookingInfo": {
                "bookingNum": "x2",
                "bookingCountry": "FR"
            }
        }
    ]
  ```

+++

## 补充ID和历程仲裁 {#arbitration}

历程仲裁（包括规则集中的并发上限和条目计数）在配置文件ID级别而非（配置文件ID、补充数据ID）对级别运行。 这意味着并发数量上限为1可能会阻止同一配置文件的第二个历程实例，即使它包含不同的补充ID值也是如此。

在依赖生产中的特定仲裁设置之前，请与Adobe代表联系以获取有关仲裁行为的指导。

**相关文档：**

* [历程上限和仲裁](../conflict-prioritization/journey-capping.md)
* [使用规则集](../conflict-prioritization/rule-sets.md)
* [冲突管理和优先级排序](../conflict-prioritization/gs-conflict-prioritization.md)

## 外部受众的补充标识符 {#external-audiences}

外部受众支持补充ID，包括从CSV文件[&#128279;](https://experienceleague.adobe.com/docs/experience-platform/segmentation/ui/overview.html#import-audience){target="_blank"}导入的受众和使用[联合受众合成](../audience/get-started-audience-orchestration.md)创建的受众。 配置从CSV或联合受众构成受众读取的历程时，您可以将该受众中的任何非标识属性指定为补充ID。 然后，Journey Optimizer会为每个独特配置文件和补充ID组合创建一个单独的历程实例。

* 用例1：每个唯一配置文件一行+补充ID对

  这是CSV和联合受众组合受众的主要用例。 受众包含多行，其中每一行表示用户档案（例如，客户）和补充ID（例如，帐户或订单ID）的唯一组合。 每一行都被视为独立的激活记录。

  | profile_id | account_id *（补充ID）* | other_attributes |
  | --- | --- | --- |
  | customer_001 | ACC-1001 | ... |
  | customer_001 | ACC-1002 | ... |
  | customer_002 | ACC-2001 | ... |

  在此示例中，`customer_001`有两个帐户。 Journey Optimizer为每个唯一的配置文件+ `account_id`对创建单独的历程实例。

* 用例2：每个配置文件一行，具有补充ID数组

  此用例适用于支持数组的受众类型。 受众中的单行包含一个配置文件，该配置文件具有包含多个补充ID值的数组属性。 Journey Optimizer在数组中为每个值创建一个历程实例。

  | profile_id | account_ids *（数组，补充ID）* | other_attributes |
  | --- | --- | --- |
  | customer_001 | [ACC-1001， ACC-1002] | ... |
  | customer_002 | [ACC-2001] | ... |

  在此示例中，Journey Optimizer为`customer_001`生成两个历程实例（每个帐户ID一个）以及`customer_002`一个实例。 这与Supplemental ID在Unified Profile Service受众中的工作方式一致。

### 如何配置 {#external-configuration}

对于使用用例1的CSV受众（其中受众有意包含同一配置文件ID的多行），必须在配置历程之前启用“快速激活”。 请参阅下面的先决条件。 对于所有其他情况，请直接配置旅程。

+++ 先决条件：通过API对CSV受众启用Express激活

>[!IMPORTANT]
>
>此先决条件仅适用于受众有意包含同一配置文件ID的多行的CSV受众（用例1）。 默认情况下，联合受众组合受众已启用快速激活，因此无需执行此步骤。 受众门户UI不支持设置`expressActivation` — 您必须使用外部受众API。

创建时必须启用受众上的`expressActivation`。 这告知Journey Optimizer独立激活每条记录，而无需按配置文件ID删除重复项。 创建受众后，无法更改此标记。

创建受众时，请使用以下API调用：

端点：

```http
POST https://platform.adobe.io/data/core/ais/external-audience
```

必需的标头：

```http
Authorization: Bearer {ACCESS_TOKEN}
Content-Type: application/json
x-api-key: {API_KEY}
x-gw-ims-org-id: {IMS_ORG}
x-sandbox-name: {SANDBOX_NAME}
```

请求正文（设置`expressActivation: true`）：

```json
{
  "name": "my_audience_name",
  "fields": [ ... ],
  "sourceSpec": { ... },
  "audienceType": "people",
  "namespace": "CustomerAudienceUpload",
  "expressActivation": true
}
```

>[!NOTE]
>
>`expressActivation`默认为`false`。 它必须在创建受众时设置，在创建后无法更改。 默认情况下，所有联合受众合成受众都启用了Express激活，因此不需要此标记。

有关完整参考，请参阅[创建外部受众API文档](https://experienceleague.adobe.com/en/docs/experience-platform/segmentation/tutorials/create-external-audience#create){target="_blank"}。

+++

要配置历程，请执行以下操作：

1. 打开或创建具有&#x200B;**[!UICONTROL 读取受众]**&#x200B;节点的历程。
1. 在&#x200B;**[!UICONTROL 读取受众]**&#x200B;节点设置中，选择您的CSV或联合受众组合受众。
1. 打开&#x200B;**[!UICONTROL 使用补充标识符]**&#x200B;选项，然后在&#x200B;**[!UICONTROL 补充标识符]**&#x200B;字段中，在&#x200B;**[!UICONTROL 高级模式]**&#x200B;中使用表达式编辑器选择要用作辅助标识符的属性（例如，`account_id`，`order_number`）。
1. 选定的属性将被视为历程的补充ID — 无需进行身份注册。

### 重复数据删除行为 {#external-dedup}

当受众启用了Express Activation（对于联合受众构成始终为true — 必须为CSV显式设置）时，Journey Optimizer会根据历程的配置方式处理重复数据删除：

| 场景 | 示例受众行 | 行为 |
| --- | --- | --- |
| **具有补充ID的历程 — 无重复（配置文件ID、补充ID）对** | (P1、S1)、(P1、S2) | 目标用例。 Journey Optimizer会为每个唯一配置文件和补充ID组合创建一个单独的历程实例。 允许所有行。 |
| **具有补充ID的历程 — 存在重复的（配置文件ID、补充ID）对** | (P1、S1)、(P1、S1)、(P1、S2) | 共享相同（用户档案ID、补充数据ID）组合的行会被正常的历程重新进入逻辑过滤掉。 仅允许每个唯一组合的第一个匹配行。 |
| **历程未配置补充ID** | (P1、S1)、(P1、S2) | 如果没有补充ID，Journey Optimizer会将同一配置文件ID的所有行视为同一配置文件。 每个用户档案ID只允许一个历程实例；丢弃同一用户档案的其他行。 |

## 示例用例

这些示例显示了补充标识符如何支持多个相关记录。

### **策略续订通知**

* **方案**：保险公司向客户持有的每个有效保单发送续订提醒。
* **执行**：
   * 个人资料： “John”。
   * 补充ID： `"AutoPolicy123", "HomePolicy456"`。
   * 历程针对每个策略单独执行，并提供个性化的续订日期、服务范围详细信息和高级信息。

### **订阅管理**

* **方案**：当触发订阅的事件时，订阅服务会为每个订阅发送定制的消息。
* **执行**：
   * 个人资料： “Jane”。
   * 补充ID： `"Luma Yoga Program ", "Luma Fitness Program"`。
   * 每个事件都包含订阅ID以及有关该订阅的详细信息。 历程针对每个事件/订阅单独执行，从而允许每个订阅提供个性化的续订优惠。

### **产品推荐**

* **情景**：电子商务平台根据客户购买的特定产品发送推荐。
* **执行**：
   * 个人资料：“Alex”。
   * 补充ID： `"productID1234", "productID5678"`。
   * 历程针对每个产品单独执行，并提供个性化的追加销售机会。

## 操作方法视频 {#video}

了解如何在[!DNL Adobe Journey Optimizer]中启用并应用补充标识符。

>[!VIDEO](https://video.tv.adobe.com/v/3464792?quality=12)
