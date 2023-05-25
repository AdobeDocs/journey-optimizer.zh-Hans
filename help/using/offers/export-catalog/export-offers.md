---
title: 个性化优惠数据集
description: 此部分列出在导出的优惠数据集中使用的所有字段
feature: Offers
topic: Integrations
role: User
level: Intermediate
exl-id: c7f691aa-8f89-4f23-b897-53211863eb6d
source-git-commit: 835e4bf227ce330b1426a9a4331fdf533fc757e3
workflow-type: tm+mt
source-wordcount: '2014'
ht-degree: 3%

---

# 个性化优惠数据集 {#offers-dataset}

每次修改优惠时，都会更新自动生成的个性化内容优惠数据集。

![](../assets/dataset-offers.png)

数据集中最近成功的批次显示在右侧。 数据集的架构的分层视图显示在左窗格中。

>[!NOTE]
>
>了解如何在中访问选件库每个对象的导出数据集 [本节](../export-catalog/access-dataset.md).

以下是可在该字段中使用的所有字段的列表 **[!UICONTROL 决策对象存储库 — 个性化优惠]** 数据集。

<!--Personalized offers form the set of choices for a decision. The objective for decisioning is to take a large inventory of items and apply numerous constraint rules to that inventory to narrow it down and then to rank the qualifying options according to a criteria. The resulting propositions assemble and personalize the experience for specific individuals.-->

+++ 标识符

**字段：** _id
**标题：** 标识符
**描述：** 记录的唯一标识符。
**类型：**&#x200B;字符串

+++

+++ _experience（体验） {#experience}

**字段：** 体验(_E)
**类型：** 对象

+++

+++ 体验>决策(_E)

**字段：** 决策
**类型：** 对象

+++

+++ 体验>决策>日历约束(_E)

**字段：** calendarConstraints
**标题：** 日历约束详细信息
**描述：** 日历约束决定给定日期范围的决策选项是否有效。 在该日期范围外，无法建议该选项。
**类型：** 对象

* **结束日期和时间**

   **字段：** endDate
   **标题：** 结束日期和时间
   **描述：** 决策选项有效性的结束日期。 不能再在决策过程中建议已超过其结束日期的选项。
   **类型：**&#x200B;字符串

* **开始日期和时间**

   **字段：** startDate
   **标题：** 开始日期和时间
   **描述：** 决策选项有效性的开始日期。 尚未到达其开始日期的选项尚无法在决策过程中建议。
   **类型：**&#x200B;字符串

+++

+++ _experience > decisioning >特征

**字段：** 特征
**标题：** 决策选项特性
**描述：** 属于此特定决策选项的其他特性或属性。 不同的实例可以具有不同的特征（映射中的键）。 特征是用于区分一个决策选项与其他决策选项的名称值对。 特征用作表示此决策选项的内容中的值，并用作分析和优化选项性能的功能。 当每个实例具有相同的属性或属性时，该方面应建模为从决策选项详细信息派生的扩展模式。
**类型：** 对象

+++

+++ 体验>决策>内容(_E)

**字段：** 目录
**标题：** 内容详细信息
**描述：** 在不同上下文中呈现决策项的内容项。 单个决策选项可以有多个内容变体。 内容是定向到受众以供在（数字）体验中使用的信息。 内容通过渠道投放到特定投放位置。
**类型：** 数组

+++

+++_体验>决策>内容>组件

**字段：** 组件
**描述：** 表示决策选项的内容组件，包括其所有语言变体。 特定组件通过“dx：format”、“dc：subject”和“dc：language”或其组合找到。 此元数据用于定位或表示与优惠关联的内容，并根据版面合同对其进行集成。
**类型：** 数组
**必需：** “_type”、“_dc” <!--TBC?-->

* **_experience >决策>内容>组件>内容组件类型**

   **字段：** _type
   **标题：** 内容组件类型
   **描述：** 一组URI的枚举，其中每个值映射到为内容组件给定的类型。 内容表示的一些使用者期望@type值是对描述内容组件的其他属性的架构的引用。
   **类型：**&#x200B;字符串

* **_experience > decisioning >内容>组件> _dc**

   **字段：** _dc
   **类型：** 对象
   **必需：** &quot;format&quot;

   * **格式**

      **字段：** 格式
      **标题：** 格式
      **描述：** 资源的物理或数字表现形式。 通常，格式应包含资源的媒体类型。 格式可用于确定显示或操作资源所需的软件、硬件或其他设备。 建议的最佳做法是从受控词汇(例如， [Internet媒体类型](http://www.iana.org/assignments/media-types/) 定义计算机媒体格式)。
      **类型：**字符串
      **示例：** &quot;application/vnd.adobe.photoshop&quot;

   * **语言**
      **字段：** 语言
      **标题：** 语言
      **描述：** 资源的一种或多种语言。 \n语言是在中定义的语言代码中指定的 [IETF RFC 3066](https://www.ietf.org/rfc/rfc3066.txt)，它是XDM中的其他位置使用的BCP 47的一部分。
      **类型：** 数组
      **示例：** “\n”、“pt-BR”、“es-ES”

* **_experience > decisioning >内容>组件> _repo**

   **字段：** 存储库(_R)
   **类型：** 对象

   * **id**

      **字段：** id
      **描述：** 在内容存储库中引用资产的可选唯一标识符。 当使用平台API检索表示法时，客户端需要额外的属性\&quot;repo：resolveUrl\&quot;来检索资产。
      **类型：**字符串
      **示例：** &quot;urn:aaid:sc:US:6dc33479-13ca-4b19-b25d-c805eff8a69e”

   * **name**

      **字段：** name
      **描述：** 有关通过\&quot;repo：id\&quot;查找存储外部资产的存储库的位置的一些提示。
      **类型：**&#x200B;字符串

   * **repositoryID**

      **字段：** repositoryID
      **描述：** 在内容存储库中引用资产的可选唯一标识符。 当使用平台API检索表示法时，客户端需要额外的属性\&quot;repo：resolveUrl\&quot;来检索资产。
      **类型：**字符串
      **示例：** &quot;C87932A55B06F7070A49412D@AdobeOrg&quot;

   * **resolveURL**

      **字段：** resolveURL
      **描述：** 可选的唯一资源定位器，用于读取内容存储库中的资产。 这样，无需客户了解资产的管理位置以及要调用的API，即可更轻松地获取资产。 这类似于HAL链接，但语义更简单、更有意义。
      **类型：**字符串
      **示例：** &quot;https://plaftform.adobe.io/resolveByPath?path=&quot;/mycorp/content/projectx/fragment/prod/herobanners/banner14.html3&quot;

* **_experience >决策>内容>组件>内容**

   **字段：** 内容
   **描述：** 直接保存内容的可选字段。 组件可以直接保存简单的内容，而不是引用资产存储库中的内容。 此字段不适用于复合、复杂和二进制内容资产。
   **类型：**&#x200B;字符串

* **_experience > decisioning > contents > components > deliveryURL**

   **字段：** deliveryURL
   **描述：** 用于从内容交付网络或服务端点获取资源的可选唯一资源定位器。 用户代理使用此URL公开访问资产。
   **类型：**字符串
   **示例：** &quot;https://cdn.adobe.io/content/projectx/fragment/prod/static/1232324wd32.jpeg&quot;

* **_experience > decisioning >内容>组件> linkURL**

   **字段：** linkURL
   **描述：** 用于用户交互的可选唯一资源定位器。 此URL用于将最终用户引荐到用户代理中，并且可以对其进行跟踪。
   **类型：**字符串
   **示例：** &quot;https://cdn.adobe.io/tracker?code=23432&amp;redirect=/content/projectx/fragment/prod/static/1232324wd32.jpeg&quot;

+++_体验>决策>内容>投放位置

**字段：** 投放
**标题：** 投放
**描述：** 要遵循的位置。 该值是被引用的优惠投放位置的URI (@id)。 请参阅架构https://ns.adobe.com/experience/decisioning/placement 。
**类型：**&#x200B;字符串

+++

+++ _experience >决策>生命周期状态

**字段：** lifecycleStatus
**标题：** 生命周期状态
**描述：** 生命周期状态允许使用对象执行工作流。 状态可能会影响对象可见或被视为相关的位置。 状态更改由使用对象的客户端或服务驱动。
**类型：** 字符串
**可能的值：** &quot;草稿&quot;（默认）、&quot;已批准&quot;、&quot;实时&quot;、&quot;已完成&quot;、&quot;已存档&quot;

+++

+++ _experience >决策>决策选项名称

**字段：** name
**标题：** 决策选项名称
**描述：** 显示在各种用户界面中的选项名称。
**类型：**&#x200B;字符串

+++

+++ _experience > decisioning > profileConstraints

**字段：** profileConstraint
**标题：** 配置文件约束详细信息
**描述：** 此时，配置文件约束将决定某个选项是否适用于此配置文件标识。 如果轮廓约束不需要考虑每个选项的值（即，它对于选项选择中的选项具有不变性），则计算为“false”的轮廓约束将取消整个选项选择。 另一方面，系统会为选件选择的每个合格选件评估将选件作为参数的配置文件约束规则。
**类型：** 对象

+++

+++_体验>决策> profileConstraints >描述

**字段：** 描述
**标题：** 描述
**描述：** 配置文件约束描述。 它用于传达关于如何或为何构建此配置文件约束以及/或它将包含或排除什么选项的人类可读意图。
**类型：**&#x200B;字符串

+++

+++_experience > decisioning > profileConstraints >资格规则

**字段：** 合格规则
**标题：** 资格规则
**描述：** 对决策规则的引用，对于给定的配置文件和/或其他给定的上下文XDM对象，其计算结果为true或false。 该规则用于确定该选项是否符合给定配置文件的条件。 该值是被引用的决策规则的URI (@id)。 请参阅架构https://ns.adobe.com/experience/decisioning/rule 。
**类型：**&#x200B;字符串

+++

+++_体验>决策> profileConstraints >配置文件约束类型

**字段：** profileConstraintType
**标题：** 配置文件约束类型
**描述：** 确定当前是否设置了任何约束以及如何表示约束。 它可以通过规则或通过一个或多个区段成员资格进行。
**类型：** 字符串
**可能的值：**
* “无”（默认）
* &quot;eligibilityRule&quot;：&quot;配置文件约束表示为单个规则，在允许约束活动之前必须评估为true。&quot;
* “anySegments”：“配置文件约束表示为一个或多个区段，在允许约束操作之前，配置文件必须是至少一个区段的成员。”
* “allSegments”：“配置文件约束表示为一个或多个区段，在允许约束操作之前，配置文件必须是所有这些区段的成员。”
* &quot;rules&quot;：&quot;profile constraint表示为许多不同的规则，例如适用性、适用性、适用性，在允许约束操作之前，所有这些规则都必须评估为true。&quot;

+++

+++_体验>决策> profileConstraints >区段标识符

**字段：** segmentIdentities
**标题：** 区段标识符
**描述：** 区段的标识符
**类型：** 数组

* **标识符**

   **字段：** _id
   **标题：** 标识符
   **描述：** 区段在相关命名空间中的身份。
   **类型：**&#x200B;字符串

* **命名空间**

   **字段：** 命名空间
   **标题：** 命名空间
   **描述：** 与关联的命名空间 `xid` 属性。
   **类型：** 对象
   **必需：** &quot;code&quot;

   * **代码**

      **字段：** 代码
      **标题：** 代码
      **描述：** 该代码是易于用户识别的命名空间标识符，可用于请求用于标识图处理的技术命名空间ID。
      **类型：**&#x200B;字符串

* **体验标识符**

   **字段：** xid
   **标题：** 体验标识符
   **描述：** 如果存在，则此值表示跨命名空间标识符，该标识符在所有命名空间中的所有命名空间范围内的标识符中是唯一的。
   **类型：**&#x200B;字符串

+++

+++ 体验>决策>排名(_E)

**字段：** 排名
**标题：** 排名详细信息
**描述：** 排名（优先级）。 定义在决策标准上下文中视为\“最佳操作\”的内容。 在满足资格约束的所有选定选项中，排名顺序将决定要建议的前（或前N个）选项。
**类型：** 对象

+++

+++_体验>决策>排名>订单评估

**字段：** 订购
**标题：** 订单评估
**描述：** 一个或多个决策选项的相对顺序的评估。 在顺序值较低的任意选项上，选择顺序值较高的选项。 用这种方法确定的值可以排序，但无法测量它们之间的距离，也不能求和或计算乘积。 中间值和模式是唯一可用于顺序数据的中心趋势指标。
**类型：** 对象

* **评分功能**

   **字段：** 函数
   **标题：** 评分功能
   **描述：** 对此决策选项计算数值分数的函数的引用。 然后，决策选项将按该得分排序（排名）。 此属性的值是每次使用on选项调用的函数的URI (@id)。 请参阅架构https://ns.adobe.com/experience/decisioning/function 。
   **类型：**&#x200B;字符串

* **订单评估类型**

   **字段：** orderEvaluationType
   **标题：** 订单评估类型
   **描述：** 指定使用哪种顺序评估机制、决策选项的静态优先级、为每个选项计算数值的评分函数或接收排序列表的排名策略。
   **类型：**字符串
   **可能的值：** &quot;static&quot;、&quot;scoringFunction&quot;、&quot;rankingStrategy&quot;

* **排名策略**

   **字段：** 排名策略
   **标题：** 排名策略
   **描述：** 对决策选项列表进行排名的策略参考。 决策选项将按有序列表返回。 此属性的值是每次使用on选项调用的函数的URI (@id)。 请参阅架构https://ns.adobe.com/experience/decisioning/rankingStrategy 。
   **类型：**&#x200B;字符串

+++

+++_体验>决策>排名>优先级

**字段：** 优先级
**标题：** 优先级
**描述：** 相对于所有其他选项的单个决策选项的优先级。 未给出订单函数的选项将使用此属性进行优先排序。 在优先级较低的选项之前，会先选择优先级值较高的选项。 如果两个或多个合格选项共享最高优先级值，则以统一的随机方式选择一个选项以用于决策建议。
**类型：** 整数
**最小值：** 0
**默认值：** 0

+++

+++ _experience >决策>标记

**字段：** 标记
**标题：** 标记
**描述：** 与此实体关联的一组收藏集限定符（以前称为“标记”）。 集合限定符用在过滤器表达式中，以将整个库存限制为子集（类别）。
**类型：** 数组

+++

<!--Field without name under tags: Description: An identifier of a collection qualifier object. The value is the @id of the collection qualifier that is referenced. See tag schema: https://ns.adobe.com/experience/decisioning/tag. Type: string-->

+++_repo

**字段：** 存储库(_R)
**类型：** 对象

+++

+++ _repo >决策选项ETag

**字段：** etag
**标题：** 决策选项ETag
**描述：** 拍摄快照时决策选项对象所处的修订版本。
**类型：**&#x200B;字符串

+++
