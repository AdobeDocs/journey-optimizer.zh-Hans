---
title: 个性化优惠数据集
description: 此部分列出在导出的优惠数据集中使用的所有字段
feature: Decision Management, Datasets
topic: Integrations
role: User, Data Engineer
level: Intermediate
exl-id: c7f691aa-8f89-4f23-b897-53211863eb6d
source-git-commit: 07b1f9b885574bb6418310a71c3060fa67f6cac3
workflow-type: tm+mt
source-wordcount: '1962'
ht-degree: 0%

---

# 个性化优惠数据集 {#offers-dataset}

每次修改优惠时，都会更新自动生成的个性化内容优惠数据集。

![](../assets/dataset-offers.png)

数据集中最近成功的批次显示在右侧。 数据集的架构的分层视图显示在左窗格中。

>[!NOTE]
>
>在[本节](../export-catalog/access-dataset.md)中了解如何访问选件库每个对象的导出数据集。

以下是可用于&#x200B;**[!UICONTROL 决策对象存储库 — 个性化优惠]**&#x200B;数据集中的所有字段的列表。

<!--Personalized offers form the set of choices for a decision. The objective for decisioning is to take a large inventory of items and apply numerous constraint rules to that inventory to narrow it down and then to rank the qualifying options according to a criteria. The resulting propositions assemble and personalize the experience for specific individuals.-->

+++ 标识符

**字段：**&#x200B;_id
**标题：**&#x200B;标识符
**描述：**&#x200B;记录的唯一标识符。
**类型：**&#x200B;字符串

+++

+++ 体验{#experience}(_E)

**字段：**&#x200B;体验(_E)
**类型：**&#x200B;对象

+++

+++ _experience > decisioning

**字段：**&#x200B;决策
**类型：**&#x200B;对象

+++

+++ _experience >决策>日历约束

**字段：**&#x200B;日历约束
**标题：**&#x200B;日历约束详细信息
**描述：**&#x200B;日历约束决定在给定日期范围内决策选项是否有效。 在该日期范围外，无法建议该选项。
**类型：**&#x200B;对象

* **结束日期和时间**

  **字段：**&#x200B;结束日期
  **标题：**&#x200B;结束日期和时间
  **描述：**&#x200B;决策选项有效期的结束日期。 不能再在决策过程中建议已超过其结束日期的选项。
  **类型：**&#x200B;字符串

* **开始日期和时间**

  **字段：**&#x200B;开始日期
  **标题：**&#x200B;开始日期和时间
  **描述：**&#x200B;决策选项有效期的开始日期。 尚未达到开始日期的选项尚无法在决策过程中建议。
  **类型：**&#x200B;字符串

+++

+++ _experience >决策>特征

**字段：**&#x200B;特性
**标题：**&#x200B;决策选项特性
**描述：**&#x200B;属于此特定决策选项的其他属性或特性。 不同的实例可以具有不同的特征（映射中的键）。 这些特征是用于区分一个决策选项和其他决策选项的名称值对。 特征会用作内容中表示此决策选项的值，并用作分析和优化选项性能的功能。 当每个实例具有相同的属性或属性时，该方面应建模为从决策选项详细信息派生的扩展模式。
**类型：**&#x200B;对象

+++

+++ _experience > decisioning >内容

**字段：**&#x200B;内容
**标题：**&#x200B;内容详细信息
**描述：**&#x200B;在不同上下文中呈现决策项的内容项。 单个决策选项可以具有多个内容变体。 内容是定向到受众以供在（数字）体验中使用的信息。 通过渠道将内容投放到特定投放位置。
**类型：**&#x200B;数组

+++

+++_experience > decisioning >内容>组件

**字段：**&#x200B;组件
**描述：**&#x200B;表示决策选项的内容组件，包括其所有语言变体。 特定组件通过“dx：format”、“dc：subject”和“dc：language”或其组合找到。 此元数据用于定位或表示与选件关联的内容，并根据版面合同对其进行集成。
**类型：**&#x200B;数组
**必需：** &quot;_type&quot;， &quot;_dc&quot; <!--TBC?-->

* **_experience >决策>内容>组件>内容组件类型**

  **字段：**&#x200B;类型(_T)
  **标题：**&#x200B;内容组件类型
  **描述：**&#x200B;枚举的URI集，其中每个值映射到为内容组件指定的类型。 内容表示的一些使用者希望@type值是对描述内容组件的其他属性的架构的引用。
  **类型：**&#x200B;字符串

* **_experience > decisioning >内容>组件> _dc**

  **字段：** _dc
  **类型：**&#x200B;对象
  **必需：** &quot;format&quot;

   * **格式**

     **字段：**&#x200B;格式
     **标题：**&#x200B;格式
     **描述：**&#x200B;资源的物理或数字形式。 通常，格式应包含资源的媒体类型。 格式可用于确定显示或操作资源所需的软件、硬件或其他设备。 建议的最佳做法是从受控词汇表中选择一个值（例如，定义计算机媒体格式的[Internet媒体类型](https://www.iana.org/assignments/media-types/)的列表）。
     **类型：**&#x200B;字符串
     **示例：** &quot;application/vnd.adobe.photoshop&quot;

   * **语言**

     **字段：**&#x200B;语言
     **标题：**&#x200B;语言
     **描述：**&#x200B;资源的语言。 \n语言是以[IETF RFC 3066](https://www.ietf.org/rfc/rfc3066.txt)中定义的语言代码指定的，它是BCP 47的一部分，在XDM中的其他位置使用。
     **类型：**&#x200B;数组
     **示例：** &quot;\n&quot;、&quot;pt-BR&quot;、&quot;es-ES&quot;

* **_experience > decisioning >内容>组件> _repo**

  **字段：**&#x200B;_repo
  **类型：**&#x200B;对象

   * **id**

     **字段：** ID
     **描述：**&#x200B;在内容存储库中引用资源的可选唯一标识符。 当使用平台API检索表示法时，客户端需要一个额外的属性\&quot;repo：resolveUrl\&quot;来检索资产。
     **类型：**&#x200B;字符串
     **示例：** &quot;urn:aaid:sc:US:6dc33479-13ca-4b19-b25d-c805eff8a69e&quot;

   * **name**

     **字段：**&#x200B;名称
     **描述：**&#x200B;有关在\&quot;repo：id\&quot;中查找存储外部资源的存储库的位置的一些提示。
     **类型：**&#x200B;字符串

   * **repositoryID**

     **字段：**&#x200B;存储库ID
     **描述：**&#x200B;在内容存储库中引用资源的可选唯一标识符。 当使用平台API检索表示法时，客户端需要一个额外的属性\&quot;repo：resolveUrl\&quot;来检索资产。
     **类型：**&#x200B;字符串
     **示例：** &quot;C87932A55B06F7070A49412D@AdobeOrg&quot;

   * **resolveURL**

     **字段：** resolveURL
     **描述：**&#x200B;用于读取内容存储库中资产的可选唯一资源定位器。 这样，无需客户了解资产的管理位置以及要调用的API，即可更轻松地获取资产。 这类似于HAL链接，但语义更简单，更有针对性。
     **类型：**&#x200B;字符串
     **示例：** &quot;https://plaftform.adobe.io/resolveByPath?path=&quot;/mycorp/content/projectx/fragment/prod/herobanners/banner14.html3&quot;

* **_experience > decisioning >内容>组件>内容**

  **字段：**&#x200B;内容
  **描述：**&#x200B;用于直接保存内容的可选字段。 组件可以直接保存简单的内容，而不是引用资产存储库中的内容。 此字段不适用于复合、复杂和二进制内容资产。
  **类型：**&#x200B;字符串

* **_experience > decisioning >内容>组件> deliveryURL**

  **字段：** deliveryURL
  **描述：**&#x200B;从内容交付网络或服务终结点获取资源的可选唯一资源定位器。 用户代理使用此URL公开访问资产。
  **类型：**&#x200B;字符串
  **示例：** &quot;https://cdn.adobe.io/content/projectx/fragment/prod/static/1232324wd32.jpeg&quot;

* **_experience > decisioning >内容>组件> linkURL**

  **字段：** linkURL
  **描述：**&#x200B;用于用户交互的可选唯一资源定位器。 此URL用于在用户代理中将最终用户引荐至，并且可以对其进行跟踪。
  **类型：**&#x200B;字符串
  **示例：** &quot;https://cdn.adobe.io/tracker?code=23432&amp;redirect=/content/projectx/fragment/prod/static/1232324wd32.jpeg&quot;

+++_体验>决策>内容>投放位置

**字段：**&#x200B;投放位置
**标题：**&#x200B;投放位置
**描述：**&#x200B;要遵循的位置。 该值是被引用的优惠投放位置的URI (@id)。 请参阅架构https://ns.adobe.com/experience/decisioning/placement 。
**类型：**&#x200B;字符串

+++

+++ _experience > decisioning >生命周期状态

**字段：**&#x200B;生命周期状态
**标题：**&#x200B;生命周期状态
**描述：**&#x200B;生命周期状态允许使用对象执行工作流。 当对象可见或被视为相关时，状态可能会受到影响。 状态更改由使用对象的客户端或服务驱动。
**类型：**&#x200B;字符串
**可能的值：**“草稿”（默认值）、“已批准”、“实时”、“已完成”、“已存档”

+++

+++ _experience >决策>决策选项名称

**字段：**&#x200B;名称
**标题：**&#x200B;决策选项名称
**描述：**&#x200B;显示在各种用户界面中的选项名称。
**类型：**&#x200B;字符串

+++

+++ _experience > decisioning > profileConstraints

**字段：**&#x200B;配置文件约束
**标题：**&#x200B;配置文件约束详细信息
**描述：**&#x200B;配置文件约束决定此时在此上下文中某个选项是否有资格使用此配置文件标识。 如果轮廓约束不需要考虑每个选项的值，即它对于选项选择中的选项是不变的，则计算为“false”的轮廓约束将取消整个选项选择。 另一方面，系统会为选件选择的每个合格选件评估将选件作为参数的配置文件约束规则。
**类型：**&#x200B;对象

+++

+++_experience > decisioning > profileConstraints >描述

**字段：**&#x200B;描述
**标题：**&#x200B;描述
**描述：**&#x200B;配置文件约束描述。 用于传达关于如何或为何构建此配置文件限制以及/或其将包含或排除哪些选项的可读意图。
**类型：**&#x200B;字符串

+++

+++_experience > decisioning > profileConstraints >资格规则

**字段：**&#x200B;合格规则
**标题：**&#x200B;资格规则
**描述：**&#x200B;对决策规则的引用，对于给定的配置文件和/或其他给定的上下文XDM对象，其计算结果为true或false。 该规则用于确定该选项是否符合给定配置文件的条件。 该值是被引用的决策规则的URI (@id)。 请参阅架构https://ns.adobe.com/experience/decisioning/rule 。
**类型：**&#x200B;字符串

+++

+++_体验>决策> profileConstraints >配置文件约束类型

**字段：** profileConstraintType
**标题：**&#x200B;配置文件约束类型
**描述：**&#x200B;确定当前是否设置了任何约束以及如何表示约束。 它可以通过规则或通过一个或多个受众成员资格实现。
**类型：**&#x200B;字符串
**可能的值：**
* “无”（默认）
* “eligibilityRule”：“配置文件约束表示为单个规则，在允许约束活动之前必须评估为true。”
* “anySegments”：“用户档案约束表示为一个或多个受众，并且用户档案必须是其中至少一个受众的成员，才能进行约束操作。”
* “allSegments”：“用户档案约束表示为一个或多个受众，并且用户档案必须是所有这些受众的成员，然后才能执行约束操作。”
* “规则”：“配置文件约束表示为许多不同的规则，例如适用性、适用性、适用性，在允许约束操作之前，所有这些规则都必须评估为true。”

+++

+++_experience > decisioning > profileConstraints >区段标识符

**字段：** segmentIdentities
**标题：**&#x200B;区段标识符
**描述：**&#x200B;受众的标识符
**类型：**&#x200B;数组

* **标识符**

  **字段：**&#x200B;_id
  **标题：**&#x200B;标识符
  **描述：**&#x200B;相关命名空间中的受众标识。
  **类型：**&#x200B;字符串

* **命名空间**

  **字段：**&#x200B;命名空间
  **标题：**&#x200B;命名空间
  **描述：**&#x200B;与`xid`属性关联的命名空间。
  **类型：**&#x200B;对象
  **必需：**“代码”

   * **代码**

     **字段：**&#x200B;代码
     **标题：**&#x200B;代码
     **描述：**&#x200B;代码是易于用户识别的命名空间标识符，可用于请求用于标识图处理的技术命名空间ID。
     **类型：**&#x200B;字符串

* **体验标识符**

  **字段：** xid
  **标题：**&#x200B;体验标识符
  **描述：**&#x200B;如果存在，此值表示跨命名空间标识符，该标识符在所有命名空间中的所有命名空间范围内的标识符中是唯一的。
  **类型：**&#x200B;字符串

+++

+++ _experience >决策>排名

**字段：**&#x200B;排名
**标题：**&#x200B;排名详细信息
**描述：**&#x200B;排名（优先级）。 定义在决策标准上下文中视为“最佳操作\”的内容。 在满足资格约束的所有选定选项中，排名顺序将决定要建议的前（或前N个）选项。
**类型：**&#x200B;对象

+++

+++_体验>决策>排名>订单评估

**字段：**&#x200B;顺序
**标题：**&#x200B;订单评估
**描述：**&#x200B;一个或多个决策选项的相对顺序的评估。 在顺序值较低的选项上，会选择顺序值较高的选项。 用这种方法求出的值可以排序，但无法测量它们之间的距离，也不能求和或计算乘积。 中间值和模式是唯一可用于顺序数据的中心趋势指标。
**类型：**&#x200B;对象

* **评分函数**

  **字段：**&#x200B;函数
  **标题：**&#x200B;评分函数
  **描述：**&#x200B;对此决策选项计算数值分数的函数的引用。 然后，决策选项将按该得分排序（排名）。 此属性的值是每次使用on选项调用的函数的URI (@id)。 请参阅架构https://ns.adobe.com/experience/decisioning/function 。
  **类型：**&#x200B;字符串

* **订单评估类型**

  **字段：** orderEvaluationType
  **标题：**&#x200B;订单评估类型
  **描述：**&#x200B;指定使用哪种顺序评估机制、决策选项的静态优先级、为每个选项计算数值的评分函数或接收排序列表的AI模型。
  **类型：**&#x200B;字符串
  **可能的值：**“静态”、“scoringFunction”、“rankingStrategy”

* **排名策略**

  **字段：**&#x200B;排名策略
  **标题：**&#x200B;排名策略
  **描述：**&#x200B;对决策选项列表进行排名的策略的引用。 决策选项将按顺序返回。 此属性的值是每次使用on选项调用的函数的URI (@id)。 请参阅架构https://ns.adobe.com/experience/decisioning/rankingStrategy 。
  **类型：**&#x200B;字符串

+++

+++_体验>决策>排名>优先级

**字段：**&#x200B;优先级
**标题：**&#x200B;优先级
**描述：**&#x200B;单个决策选项相对于所有其他选项的优先级。 未给出订单函数的选项将使用此属性进行优先排序。 在优先级较低的选项之前，会先选择优先级值较高的选项。 如果两个或更多合格选项共享最高优先级值，则以统一的随机方式选择一个选项用于决策建议。
**类型：**&#x200B;整数
**最小值：** 0
**默认值：** 0

+++

+++ _experience > decisioning >标记

**字段：**&#x200B;标记
**标题：**&#x200B;标记
**描述：**&#x200B;与此实体关联的集合限定符集（以前称为“标记”）。 集合限定符用在过滤器表达式中，以将整个库存限制为子集（类别）。
**类型：**&#x200B;数组

+++

<!--Field without name under tags: Description: An identifier of a collection qualifier object. The value is the @id of the collection qualifier that is referenced. See tag schema: https://ns.adobe.com/experience/decisioning/tag. Type: string-->

+++_repo

**字段：**&#x200B;_repo
**类型：**&#x200B;对象

+++

+++ _repo >决策选项ETag

**字段：** etag
**标题：**&#x200B;决策选项ETag
**描述：**&#x200B;拍摄快照时决策选项对象所处的修订版本。
**类型：**&#x200B;字符串

+++
