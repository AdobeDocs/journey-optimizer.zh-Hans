---
title: 个性化优惠数据集
description: 此部分列表导出的优惠数据集中使用的所有字段。
translation-type: tm+mt
source-git-commit: 70c172e19d5900c898d4850801468a2e186e682d
workflow-type: tm+mt
source-wordcount: '1943'
ht-degree: 3%

---

# 个性化优惠数据集{#offers-dataset}

每次修改优惠时，都会更新为个性化内容优惠自动生成的数据集。

![](../../assets/dataset-offers.png)

数据集中最近成功的批处理显示在右侧。 数据集模式的层次视图显示在左窗格中。

>[!NOTE]
>
>了解如何访问[本节](../export-catalog/access-dataset.md)中优惠库每个对象的导出数据集。

以下是可在&#x200B;**[!UICONTROL Decision Object Repository - Personalized Offers]**&#x200B;数据集中使用的所有字段的列表。

<!--Personalized offers form the set of choices for a decision. The objective for decisioning is to take a large inventory of items and apply numerous constraint rules to that inventory to narrow it down and then to rank the qualifying options according to a criteria. The resulting propositions assemble and personalize the experience for specific individuals.-->

## 标识符

**Field:_id** Title:Identifier 
**Description:** 记录
**** 的唯一标识符。**类型：**&#x200B;字符串

## _experience（体验）

**Field:** _experience 
**Type:** object

### 决策

**字段：** 决策
**类型：对** 象

#### calendarConstraints

**字段：日** 历约束
**标题：日** 历约束详细
**信息说明：** 日历约束决定决策选项在给定日期范围内是否有效。在该日期范围之外，无法建议该选项。
**类型：对** 象

* **结束日期和时间**

   **字段：** endDate
   **标题：** 结束日期和时间
   **说明：** 决策选项有效性的结束日期。在决策过程中，已超过其结束日期的选项不再建议。
   **类型：**&#x200B;字符串

* **开始日期和时间**

   **字段：** startDate
   **标题：** 开始日期和时间
   **说明：** 决策选项有效性的开始日期。尚未达到其开始日期的选项尚未在决策过程中提出。
   **类型：**&#x200B;字符串

#### 特征

**字段：特** 性标
**题：决策** 选项特性
**描述：属** 于此特定决策选项的其他属性或属性。不同的实例可能具有不同的特性（映射中的键）。 特征是用于区分一个决策选项和其他决策选项的名称值对。 特征用作表示此决策选项的内容中的值，并用作分析和优化选项性能的功能。 当每个实例具有相同的属性或属性时，该方面应建模为派生自决策选项详细信息的扩展模式。
**类型：对** 象

#### 内容

**字段：内** 容
**标题：内** 容详
**细信** 息描述：用于以不同上下文呈现决策项的内容项。单个决策选项可以具有多个内容变体。 内容是指面向（数字）体验中消费受众的信息。 内容通过渠道交付到特定位置。
**类型：数** 组

* **组件**

   **字段：组** 件
   **说明：** 表示决策选项的内容的组件，包括其所有语言变体。通过“dx:format”、“dc:subject”和“dc:language”或其组合找到特定组件。 此元数据用于定位或表示与优惠关联的内容，并根据放置合同对其进行集成。
   **类型：数** 组
   **必需：** &quot;_type&quot;, &quot;_dc&quot;  <!--TBC?-->

   * **内容组件类型**

      **字段：** _type
      **标题：内** 容组件类型
      **描述：** URI的枚举集，其中每个值映射到给定内容组件的类型。内容表示的某些用户希望@type值是对描述内容组件其他属性的模式的引用。
      **类型：**&#x200B;字符串

   * **_dc**

      **字段：** _dc
      **类型：对** 象
      **必需：** &quot;format&quot;

      * **格式**

         **字段：格** 式
         **标题：格** 式
         **描述：** 资源的物理或数字表现。通常，格式应包括资源的媒体类型。 格式可用于确定显示或操作资源所需的软件、硬件或其他设备。 建议的最佳做法是从受控词汇中选择一个值(例如，[定义计算机媒体格式的Internet媒体类型](http://www.iana.org/assignments/media-types/)的列表)。
         **类型：**字符串
         **示例** :&quot;application/vnd.adobe.photoshop&quot;

      * **语言**
         **字段：语** 言
         **标题：语** 言
         **说明：** 资源的语言或语言。\n语言在语言代码中指定，如[IETF RFC 3066](https://www.ietf.org/rfc/rfc3066.txt)中所定义，它是BCP 47的一部分，XDM的其他位置也使用该组件。
         **类型：数** 组
         **示例** :&quot;\n&quot;、&quot;pt-BR&quot;、&quot;es-ES&quot;
   * **_repo**

      **字段：** _repo
      **类型：对** 象

      * **id**

         **字段：** id
         **描述：用** 于在内容存储库中引用资产的可选唯一标识符。当使用平台API检索表示形式时，客户端可以期望额外的属性\&quot;repo:resolveUrl\&quot;检索资产。
         **类型：**字符串
         **示例** :&quot;urn:aaid:sc:US:6dc33479-13ca-4b19-b25d-c805eff8a69e&quot;

      * **name**

         **字段：** 名称
         **说明：** 有关使用\&quot;repo:id\&quot;查找存储外部资产的存储库的位置的提示。
         **类型：**&#x200B;字符串

      * **repositoryID**

         **字段：** repositoryID
         **描述：用** 于在内容存储库中引用资产的可选唯一标识符。当使用平台API检索表示形式时，客户端可以期望额外的属性\&quot;repo:resolveUrl\&quot;检索资产。
         **类型：**字符串
         **示例** :&quot;C87932A55B06F7070A49412D@AdobeOrg&quot;

      * **resolveURL**

         **字段：** resolveURL
         **描述：用** 于在内容存储库中读取资产的可选唯一资源定位器。这样，在客户端不了解资产的管理位置和要调用的API的情况下，获取资产会更加容易。 这与HAL链接类似，但语义更简单、更具针对性。
         **类型：**字符串
         **示例** :&quot;https://plaftform.adobe.io/resolveByPath?path=&quot;/mycorp/content/projectx/fragment/prod/herobanners/banner14.html3&quot;&quot;
   * **content**

      **字段：内** 容
      **说明：** 用于直接保存内容的可选字段。组件可以直接保存简单内容，而不是在资产存储库中引用内容。 此字段不用于合成、复杂和二进制内容资源。
      **类型：**&#x200B;字符串

   * **deliveryURL**

      **字段：** deliveryURL
      **描述：** 用于从内容投放网络或服务端点获取资产的可选唯一资源定位器。此URL用于由用户代理公开访问资产。
      **类型：**字符串
      **示例** :&quot;https://cdn.adobe.io/content/projectx/fragment/prod/static/1232324wd32.jpeg&quot;

   * **linkURL**

      **字段：** linkURL
      **说明：用** 户交互的可选唯一资源定位器。此URL用于将最终用户引用到用户代理中，并可以跟踪。
      **类型：**字符串
      **示例** :&quot;https://cdn.adobe.io/tracker?code=23432&amp;redirect=/content/projectx/fragment/prod/static/1232324wd32.jpeg&quot;



* **版面**

   **字段：位** 置
   **标题：放** 置
   **说明：** 要符合的位置。该值是引用的优惠放置的URI(@id)。 请参阅模式 https://ns.adobe.com/experience/decisioning/placement。
   **类型：**&#x200B;字符串

#### 生命周期状态

**Field:lifecycleStatus** Title:Lifecycle 
**Status** Description:Lifecycle 
**** status允许对对象执行工作流。状态可能会影响对象可见或被认为相关的位置。 状态更改由使用对象的客户端或服务驱动。
**类型：** 字
**符串可** 能值：&quot;Draft&quot;、&quot;Approved&quot;、&quot;Live&quot;、&quot;Completed&quot;、&quot;Archived&quot; 
**默认值：** &quot;Draft&quot;

#### 决策选项名称

**字段：名** 称标
**题：决** 策选项名
**称描述：** 在各种用户界面中显示的选项名称。**类型：**&#x200B;字符串

#### profileConstraints

**字段：配** 置文件约
**束标题：** 用户档案约束详细
**信息说** 明：用户档案约束决定某个选项此时是否适合此用户档案标识在此上下文中。如果用户档案约束不需要考虑每个选项的值，即它是选项选择中的选项的不变量，则计算为“false”的用户档案约束将取消整个选项选择。 另一方面，将为选项选择的每个限定选项评估以选项为参数的用户档案约束规则。
**类型：对** 象

* **描述**

   **字段：说** 明
   **标题：说** 明
   **描述：** 用户档案约束描述。它用于传达人类可读的意图，说明该用户档案约束是如何构建的、为什么构建的和/或该约束将包括或排除哪个选项。
   **类型：**&#x200B;字符串

* **合格规则**

   **字段：** ivilityRule
   **标题：** 合格规则
   **描述：** 对决策规则的引用，该规则对给定用户档案和/或其他给定的上下文XDM对象的计算结果为true或false。该规则用于确定该选项是否符合给定用户档案。 该值是引用的决策规则的URI(@id)。 请参阅模式 https://ns.adobe.com/experience/decisioning/rule。
   **类型：**&#x200B;字符串

* **用户档案约束类型**

   **字段：** profileConstraintType
   **标题：** 用户档案约束类型
   **描述：** 确定当前是否设置了任何约束以及约束的表示方式。可以通过规则或通过一个或多个区段成员资格进行。
   **类型：**字符串
   **可能的值：**
   * &quot;无&quot;
   * “vicialRule”：&quot;用户档案约束表示为一个规则，在允许约束操作之前，该规则必须求值为true。&quot;
   * “anySegments”：“用户档案约束表示为一个或多个段，在允许约束操作之前，用户档案必须是其中至少一个段的成员。”
   * “allSegments”：“用户档案约束表示为一个或多个区段，用户档案必须是所有区段的成员，才允许执行受约束的操作。”
   * “规则”：“用户档案约束表示为许多不同的规则，例如资格、适用性、适用性，在允许约束操作之前，所有规则都必须评估为true。”
      **默认值** :&quot;none&quot;

* **区段标识符**

   **字段：** segmentIdentities
   **标题：区** 段标识符
   **说明：** 区段的标识符
   **类型：数** 组

   * **标识符**

      **字段：** _id
      **标题：标** 识符
      **说明：** 相关命名空间中区段的标识。
      **类型：**&#x200B;字符串

   * **命名空间**

      **字段：** 命名空间
      **标题：** 命名空间
      **说明：** 与属性关联的 `xid` 命名空间。
      **类型：对** 象
      **必需：** &quot;code&quot;

      * **代码**

         **字段：** 代码
         **标题：代** 码
         **描述：** 代码是命名空间的可读标识符，可用于请求用于标识图处理的技术命名空间ID。
         **类型：**&#x200B;字符串
   * **体验标识符**

      **字段：** xid
      **标题：体** 验标识符
      **描述：** 当存在时，此值表示跨命名空间标识符，该标识符在所有命名空间中所有命名空间范围的标识符中都是唯一的。
      **类型：**&#x200B;字符串


#### 排名

**字段：** 排名
**标题：** 排名详
**细信** 息描述：排名（优先级）。定义给定决策标准上下文的\&quot;最佳操作\&quot;。 在符合资格约束的所有选定选项中，排名顺序将决定要建议的前（或前N）个选项。
**类型：对** 象

* **订单评估**

   **字段：** 顺序
   **标题：订** 单评估
   **描述：** 评估一个或多个决策选项的相对顺序。在具有较低序数值的任何选项上，都会选择具有较高序数值的选项。 该方法确定的值可以排序，但它们之间的距离不能测量，且不能求和或求积。 中值和模式是衡量序数数据中心趋势的唯一指标。
   **类型：对** 象

   * **评分功能**

      **字段：函** 数
      **标题：** 评分函数
      **描述：** 对用于计算此决策选项的数值得分的函数的引用。然后，将按该分数对决策选项进行排序（排名）。 此属性的值是每次使用on选项调用的函数的URI(@id)。 请参阅模式 https://ns.adobe.com/experience/decisioning/function。
      **类型：**&#x200B;字符串

   * **订单评估类型**

      **字段：** orderEvaluationType
      **标题：订** 单评估类型
      **说明：指** 定使用哪个订单评估机制、决策选项的静态优先级、计算每个选项的数值的评分函数或接收列表进行排序的排名策略。
      **类型：**字符串
      **可能的值** :&quot;static&quot;、&quot;scoringFunction&quot;、&quot;rankingStrategy&quot;

   * **排名策略**

      **字段：** rankingStrategy
      **标题：** 排名策略
      **描述：** 对决策选项列表进行排名的策略的引用。决策选项将以有序列表返回。 此属性的值是每次使用on选项调用的函数的URI(@id)。 请参阅模式 https://ns.adobe.com/experience/decisioning/rankingStrategy。
      **类型：**&#x200B;字符串

* **优先级**

   **字段：优** 先
   **标题：优** 先级
   **说明：** 单个决策选项相对于所有其他选项的优先级。使用此属性，将优先选择不给定顺序函数的选项。 优先级值较高的选项在优先级较低的选项之前被选择。 如果两个或更多符合条件的期权具有最高优先级值，则以统一随机方式选择一个期权并用于决策建议。
   **类型：整** 数
   **最小值：** 0
   **默认值：** 0

#### 标记

**字段：** 标记
**标题：** 标
**签** 描述：与此实体关联的标签集。这些标记用于筛选表达式，以将整体库存限制为子集(类别)。
**类型：数** 组

<!--Field without name under tags: Description: An identifier of a tag object. The value is the @id of the tag that is referenced. See tag schema: https://ns.adobe.com/experience/decisioning/tag. Type: string-->

## _repo

**Field:** _repo 
**Type:** object

### 决策选项ETag

**字段：** 标
**题：** 决策选项ETag
**描述：** 决策选项对象在拍摄快照时所在的修订版本。**类型：**&#x200B;字符串



