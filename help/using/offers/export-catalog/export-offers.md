---
title: 个性化优惠数据集
description: 此部分列出了选件导出数据集中使用的所有字段
feature: Offers
topic: Integrations
role: User
level: Intermediate
exl-id: c7f691aa-8f89-4f23-b897-53211863eb6d
source-git-commit: 0545cda9f91ff18791310a4ee2463b2287ac7557
workflow-type: tm+mt
source-wordcount: '2003'
ht-degree: 3%

---

# 个性化优惠数据集 {#offers-dataset}

每次修改选件时，都会更新为个性化内容选件自动生成的数据集。

![](../../assets/dataset-offers.png)

数据集中最近一次成功的批处理将显示在右侧。 数据集架构的分层视图将显示在左窗格中。

>[!NOTE]
>
>了解如何在 [此部分](../export-catalog/access-dataset.md).

以下是可在 **[!UICONTROL Decision Object Repository - Personalized Offers]** 数据集。

<!--Personalized offers form the set of choices for a decision. The objective for decisioning is to take a large inventory of items and apply numerous constraint rules to that inventory to narrow it down and then to rank the qualifying options according to a criteria. The resulting propositions assemble and personalize the experience for specific individuals.-->

## 标识符 {#identifier}

**字段：** _id
**标题：** 标识符
**描述：** 记录的唯一标识符。
**类型：**&#x200B;字符串

## _experience（体验） {#experience}

**字段：** _体验
**类型：** 对象

### _experience > decisioning

**字段：** 决策
**类型：** 对象

#### _experience > decisioning > calendarConstraints

**字段：** calendarConstraints
**标题：** 日历约束详细信息
**描述：** 日历约束决定在给定日期范围时决策选项是否有效。 在该日期范围之外，无法建议使用选项。
**类型：** 对象

* **结束日期和时间**

   **字段：** endDate
   **标题：** 结束日期和时间
   **描述：** 决策选项有效期的结束日期。 在决策过程中，无法再建议已超过其结束日期的选项。
   **类型：**&#x200B;字符串

* **开始日期和时间**

   **字段：** startDate
   **标题：** 开始日期和时间
   **描述：** 决策选项有效期的开始日期。 尚未达到其开始日期的选项在决策过程中尚无法提议。
   **类型：**&#x200B;字符串

#### _experience > decisioning >特征

**字段：** 特征
**标题：** 决策选项特性
**描述：** 属于此特定决策选项的其他属性或属性。 不同的实例可能具有不同的特性（映射中的键）。 特征是用于区分一个决策选项与其他决策选项的名称值对。 特征用作表示此决策选项的内容中的值，以及用作分析和优化选项性能的功能。 当每个实例具有相同的属性或属性时，应将该方面建模为从决策选项详细信息派生的扩展架构。
**类型：** 对象

#### _experience > decisioning >内容

**字段：** 内容
**标题：** 内容详细信息
**描述：** 在不同上下文中呈现决策项的内容项。 单个决策选项可以具有多个内容变体。 内容是指面向受众以便在（数字）体验中使用的信息。 通过渠道将内容交付到特定版面中。
**类型：** 阵列

**_experience > decisioning > contents > components**

**字段：** 组件
**描述：** 代表决策选项的内容的组件，包括其所有语言变体。 特定组件可通过“dx:format”、“dc:subject”和“dc:language”或其组合找到。 此元数据用于查找或表示与选件关联的内容，并根据版面合同对其进行集成。
**类型：** 阵列
**必需：** &quot;_type&quot;, &quot;_dc&quot; <!--TBC?-->

* **_experience > decisioning > contents > components >内容组件类型**

   **字段：** _type
   **标题：** 内容组件类型
   **描述：** 枚举的URI集，其中每个值映射到给定给内容组件的类型。 内容表示的某些用户希望@type值作为对描述内容组件其他属性的架构的引用。
   **类型：**&#x200B;字符串

* **_experience > decisioning >内容>组件> _dc**

   **字段：** _dc
   **类型：** 对象
   **必需：** &quot;format&quot;

   * **格式**

      **字段：** 格式
      **标题：** 格式
      **描述：** 资源的物理或数字显示。 通常，格式应包括资源的媒体类型。 格式可用于确定显示或操作资源所需的软件、硬件或其它设备。 建议的最佳做法是从受控词汇中选择一个值(例如， [Internet媒体类型](http://www.iana.org/assignments/media-types/) 定义计算机媒体格式)。
      **类型：**字符串
      **示例：** &quot;application/vnd.adobe.photoshop&quot;

   * **语言**
      **字段：** 语言
      **标题：** 语言
      **描述：** 资源的语言或语言。 \n语言在语言代码中指定，定义如 [IETF RFC 3066](https://www.ietf.org/rfc/rfc3066.txt),BCP 47的一部分，BCP 47在XDM的其他位置使用。
      **类型：** 阵列
      **示例：** &quot;\n&quot;, &quot;pt-BR&quot;, &quot;es-ES&quot;

* **_experience > decisioning >内容>组件> _repo**

   **字段：** _repo
   **类型：** 对象

   * **id**

      **字段：** id
      **描述：** 用于引用内容存储库中资产的可选唯一标识符。 当使用Platform API检索表示形式时，客户端可能需要额外的属性\&quot;repo:resolveUrl\&quot;来检索资产。
      **类型：**字符串
      **示例：** “urn”:aaid:sc:US:6dc33479-13ca-4b19-b25d-c805eff8a69e”

   * **name**

      **字段：** name
      **描述：** 有关在何处查找通过\&quot;repo:id\&quot;存储外部资产的存储库的一些提示。
      **类型：**&#x200B;字符串

   * **repositoryID**

      **字段：** repositoryID
      **描述：** 用于引用内容存储库中资产的可选唯一标识符。 当使用Platform API检索表示形式时，客户端可能需要额外的属性\&quot;repo:resolveUrl\&quot;来检索资产。
      **类型：**字符串
      **示例：** &quot;C87932A55B06F7070A49412D@AdobeOrg&quot;

   * **resolveURL**

      **字段：** resolveURL
      **描述：** 用于在内容存储库中读取资产的可选唯一资源定位器。 这样，客户就无需了解资产的管理位置以及要调用的API，即可更轻松地获取资产。 这类似于HAL链接，但语义更简单、目的更明确。
      **类型：**字符串
      **示例：** &quot;https://plaftform.adobe.io/resolveByPath?path=&quot;/mycorp/content/projectx/fragment/prod/herobanners/banner14.html3&quot;&quot;

* **_experience > decisioning >内容>组件>内容**

   **字段：** 内容
   **描述：** 可直接保存内容的可选字段。 组件可以直接保存简单内容，而不是在资产存储库中引用内容。 此字段不用于复合、复杂和二进制内容资产。
   **类型：**&#x200B;字符串

* **_experience > decisioning > contents > components > deliveryURL**

   **字段：** deliveryURL
   **描述：** 用于从内容交付网络或服务端点获取资产的可选唯一资源定位器。 此URL用于由用户代理公开访问资产。
   **类型：**字符串
   **示例：** &quot;https://cdn.adobe.io/content/projectx/fragment/prod/static/1232324wd32.jpeg&quot;

* **_experience > decisioning > contents > components > linkURL**

   **字段：** linkURL
   **描述：** 用户交互的可选唯一资源定位器。 此URL用于在用户代理中将最终用户引荐至，并可进行跟踪。
   **类型：**字符串
   **示例：** &quot;https://cdn.adobe.io/tracker?code=23432&amp;redirect=/content/projectx/fragment/prod/static/1232324wd32.jpeg&quot;

**_experience > decisioning > contents > placement**

**字段：** 投放
**标题：** 版面
**描述：** 要符合的版面。 值是所引用的选件版面的URI(@id)。 请参阅架构https://ns.adobe.com/experience/decisioning/placement 。
**类型：**&#x200B;字符串

#### _experience >决策>生命周期状态

**字段：** lifecycleStatus
**标题：** 生命周期状态
**描述：** 生命周期状态允许使用对象执行工作流。 当某个对象可见或被认为相关时，状态可能会受到影响。 状态更改由使用对象的客户端或服务驱动。
**类型：** 字符串
**可能值：** “草稿”（默认）、“已批准”、“实时”、“已完成”、“已存档”

#### _experience > decisioning >决策选项名称

**字段：** name
**标题：** 决策选项名称
**描述：** 各种用户界面中显示的选项名称。
**类型：**&#x200B;字符串

#### _experience > decisioning > profileConstraints

**字段：** profileConstraints
**标题：** 配置文件约束详细信息
**描述：** 此时，配置文件约束将决定在此上下文中某个选项是否符合此配置文件标识的条件。 如果配置文件约束不需要考虑每个选项的值，即选项选择中的选项不变，则计算为“false”的配置文件约束会取消整个选项选择。 另一方面，将为选项选择的每个限定选项评估以选项作为参数的配置文件约束规则。
**类型：** 对象

**_experience > decisioning > profileConstraints >描述**

**字段：** 描述
**标题：** 描述
**描述：** 配置文件约束描述。 它用于传达人类可读的意图，说明如何构建此用户档案约束以及/或该用户档案约束将包含或排除哪个选项。
**类型：**&#x200B;字符串

**_experience > decisioning > profileConstraints >资格规则**

**字段：** igilityRule
**标题：** 资格规则
**描述：** 对决策规则的引用，该规则对给定配置文件和/或其他给定上下文XDM对象的计算结果为true或false。 该规则用于确定选项是否符合给定用户档案的条件。 该值是引用的决策规则的URI(@id)。 请参阅架构https://ns.adobe.com/experience/decisioning/rule 。
**类型：**&#x200B;字符串

**_experience > decisioning > profileConstraints >配置文件约束类型**

**字段：** profileConstraintType
**标题：** 轮廓约束类型
**描述：** 确定当前是否设置了任何约束以及约束的表示方式。 可以通过规则或通过一个或多个区段成员关系实现。
**类型：** 字符串
**可能值：**
* &quot;none&quot;（默认）
* &quot;igilityRule&quot;:“配置文件约束以单个规则表示，在允许约束操作之前，必须将其计算为true。”
* &quot;anySegments&quot;:“配置文件约束表示为一个或多个区段，且配置文件必须是其中至少一个区段的成员，才允许执行约束操作。”
* &quot;allSegments&quot;:“配置文件约束以一个或多个区段表示，并且配置文件必须是所有区段的成员，然后才能允许约束操作。”
* &quot;rules&quot;:“用户档案约束以许多不同的规则表示，例如资格、适用性、适用性，所有规则都必须在允许约束操作之前评估为true。”

**_experience > decisioning > profileConstraints >区段标识符**

**字段：** segmentIdentities
**标题：** 区段标识符
**描述：** 区段的标识符
**类型：** 阵列

* **标识符**

   **字段：** _id
   **标题：** 标识符
   **描述：** 相关命名空间中区段的标识。
   **类型：**&#x200B;字符串

* **命名空间**

   **字段：** 命名空间
   **标题：** 命名空间
   **描述：** 与 `xid` 属性。
   **类型：** 对象
   **必需：** &quot;code&quot;

   * **代码**

      **字段：** 代码
      **标题：** 代码
      **描述：** 该代码是命名空间的人类可读标识符，可用于请求用于身份图处理的技术命名空间ID。
      **类型：**&#x200B;字符串

* **体验标识符**

   **字段：** xid
   **标题：** 体验标识符
   **描述：** 如果存在，则此值表示跨命名空间标识符，该标识符在所有命名空间中所有命名空间范围内的标识符都是唯一的。
   **类型：**&#x200B;字符串

#### _experience >决策>排名

**字段：** 排名
**标题：** 排名详细信息
**描述：** 排名（优先级）。 定义在决策标准的上下文下被视为\&quot;最佳操作\&quot;的内容。 在符合资格约束的所有选定选项中，排名顺序将决定要建议的排名前（或排名前N）的选项。
**类型：** 对象

**_experience > decisioning >排名>订单评估**

**字段：** 订购
**标题：** 订单评估
**描述：** 一个或多个决策选项的相对顺序的评估。 对于具有较低序数值的任何选项，都会选择具有较高序数值的选项。 该方法确定的值可以按顺序排列，但它们之间的距离无法测量，并且既不能求和也不能计算乘积。 中值和模式是唯一可用于顺序数据的中心趋势度量。
**类型：** 对象

* **评分功能**

   **字段：** 函数
   **标题：** 评分功能
   **描述：** 对函数的引用，该函数计算此决策选项的数值分数。 然后，将根据该分数对决策选项进行排序（排名）。 此属性的值是要一次通过on选项调用的函数的URI(@id)。 请参阅架构https://ns.adobe.com/experience/decisioning/function 。
   **类型：**&#x200B;字符串

* **订单评估类型**

   **字段：** orderEvaluationType
   **标题：** 订单评估类型
   **描述：** 指定使用哪种顺序评估机制、决策选项的静态优先级、计算每个选项的数值的评分函数或接收列表以对其进行排序的排名策略。
   **类型：**字符串
   **可能值：** &quot;static&quot;、&quot;scoringFunction&quot;、&quot;rankingStrategy&quot;

* **排名策略**

   **字段：** rankingStrategy
   **标题：** 排名策略
   **描述：** 对决策选项列表进行排名的策略的引用。 决策选项将在有序列表中返回。 此属性的值是要一次通过on选项调用的函数的URI(@id)。 请参阅架构https://ns.adobe.com/experience/decisioning/rankingStrategy 。
   **类型：**&#x200B;字符串

**_experience > decisioning >排名>优先级**

**字段：** 优先级
**标题：** 优先级
**描述：** 单个决策选项相对于所有其他选项的优先级。 使用此属性时，将按优先顺序排列未提供订单函数的选项。 优先级值较高的选项会在优先级较低的选项之前选择。 如果两个或多个合格期权具有最高优先级值，则一个期权以统一随机方式选择并用于决策建议。
**类型：** 整数
**最小值：** 0
**默认值：** 0

#### _experience > decisioning > tag

**字段：** 标记
**标题：** 标记
**描述：** 与此实体关联的标记集。 标记用在过滤器表达式中，用于将整体库存限制为子集（类别）。
**类型：** 阵列

<!--Field without name under tags: Description: An identifier of a tag object. The value is the @id of the tag that is referenced. See tag schema: https://ns.adobe.com/experience/decisioning/tag. Type: string-->

## _repo {#repo}

**字段：** _repo
**类型：** 对象

### _repo >决策选项ETag

**字段：** etag
**标题：** 决策选项ETag
**描述：** 拍摄快照时，决策选项对象所在的修订版本。
**类型：**&#x200B;字符串
