---
title: 后备优惠数据集
description: 此部分列出了导出数据集中用于备用选件的所有字段。
feature: 优惠
topic: 集成
role: User
level: Intermediate
source-git-commit: a25264cb43f77671c29f18522110fd85d0155697
workflow-type: tm+mt
source-wordcount: '1047'
ht-degree: 3%

---

# 后备优惠数据集 {#fallback-dataset}

每次修改选件时，都会更新备用选件自动生成的数据集。

![](../../assets/dataset-fallback.png)

数据集中最近一次成功的批处理将显示在右侧。 数据集架构的分层视图将显示在左窗格中。

>[!NOTE]
>
>了解如何在[此部分](../export-catalog/access-dataset.md)中访问选件库每个对象的导出数据集。

以下是可在&#x200B;**[!UICONTROL Decision Object Repository - Fallback Offers]**&#x200B;数据集中使用的所有字段的列表。

## 标识符

**字段：** _id标
**题：** 标识
**符描述：** 记录的唯一标识符。**类型：**&#x200B;字符串

## _experience（体验）

**字段：** _experience类
**型：** 对象

### _experience > decisioning

**字段：** 决策
**类型：** 对象

#### _experience > decisioning >特征

**字段：** 特征
**标题：** 决策选项特征
**描述：** 属于此特定决策选项的其他属性或属性。不同的实例可能具有不同的特性（映射中的键）。 特征是用于区分一个决策选项与其他决策选项的名称值对。 特征用作表示此决策选项的内容中的值，以及用作分析和优化选项性能的功能。 当每个实例具有相同的属性或属性时，应将该方面建模为从决策选项详细信息派生的扩展架构。
**类型：** 对象

<!--Field under Characteristics without title = additionalProperties? Desc = Value of the property. Type: string-->

#### _experience > decisioning >内容

**字段：** 内容
**标题：** 内容详细信
**息描述：** 在不同上下文中呈现决策项的内容项。单个决策选项可以具有多个内容变体。 内容是指面向受众以便在（数字）体验中使用的信息。 通过渠道将内容交付到特定版面中。
**类型：** 数组

**_experience > decisioning > contents > components**

**字段：** 组件
**描述：** 表示决策选项的内容的组件，包括其所有语言变体。特定组件可通过“dx:format”、“dc:subject”和“dc:language”或其组合找到。 此元数据用于查找或表示与选件关联的内容，并根据版面合同对其进行集成。
**类型：** 数
**组必需：** &quot;_type&quot;、&quot;_dc&quot;  <!--TBC?-->

* **_experience > decisioning > contents > components >内容组件类型**

   **字段：** _type
   **标题：** 内容组件类型
   **描述：** 枚举的URI集，其中每个值都映射到给定给内容组件的类型。内容表示的某些用户希望@type值作为对描述内容组件其他属性的架构的引用。
   **类型：**&#x200B;字符串

* **_experience > decisioning >内容>组件> _dc**

   **字段：** _dc
   **类型：** 对象
   **必需：** &quot;format&quot;

   * **格式**

      **字段：** 格式
      **标题：** 格式
      **描述：** 资源的物理或数字显示。通常，格式应包括资源的媒体类型。 格式可用于确定显示或操作资源所需的软件、硬件或其它设备。 建议的最佳做法是从受控词汇中选择一个值(例如，定义计算机媒体格式的[Internet媒体类型](http://www.iana.org/分配/media-types/)列表)。
      **类型：**字符串
      **示例：** &quot;application/vnd.adobe.photoshop&quot;

   * **语言**

      **字段：** 语言
      **标题：** 语言
      **描述：** 资源的语言或语言。\n语言在语言代码中指定，如[IETF RFC 3066](https://www.ietf.org/rfc/rfc3066.txt)中定义，该代码是BCP 47的一部分，在XDM的其他位置使用。
      **类型：** 数组
      **示例：** &quot;\n&quot;、&quot;pt-BR&quot;、&quot;es-ES&quot;

* **_experience > decisioning >内容>组件> _repo**

   **字段：** _repo
   **类型：** 对象

   * **id**

      **字段：** id
      **描述：** 用于引用内容存储库中资产的可选唯一标识符。当使用Platform API检索表示形式时，客户端可能需要额外的属性\&quot;repo:resolveUrl\&quot;来检索资产。
      **类型：**字符串
      **示例：** &quot;:aaid:urnsc:US:6dc33479-13ca-4b19-b25d-c805eff8a69e&quot;

   * **name**

      **字段：** 名称
      **描述：** 有关在何处查找通过\&quot;repo:id\&quot;存储外部资产的存储库的一些提示。
      **类型：**&#x200B;字符串

   * **repositoryID**

      **字段：** repositoryID
      **描述：** 用于引用内容存储库中资产的可选唯一标识符。当使用Platform API检索表示形式时，客户端可能需要额外的属性\&quot;repo:resolveUrl\&quot;来检索资产。
      **类型：**字符串
      **示例：** &quot;C87932A55B06F7070A49412D@AdobeOrg&quot;

   * **resolveURL**

      **字段：** resolveURL
      **描述：** 用于在内容存储库中读取资产的可选唯一资源定位器。这样，客户就无需了解资产的管理位置以及要调用的API，即可更轻松地获取资产。 这类似于HAL链接，但语义更简单、目的更明确。
      **类型：**字符串
      **示例：** &quot;https://plaftform.adobe.io/resolveByPath?path=&quot;/mycorp/content/projectx/fragment/prod/herobanners/banner14.html3&quot;&quot;

* **_experience > decisioning >内容>组件>内容**

   **字段：** 内容
   **描述：** 可直接保存内容的可选字段。组件可以直接保存简单内容，而不是在资产存储库中引用内容。 此字段不用于复合、复杂和二进制内容资产。
   **类型：**&#x200B;字符串

* **_experience > decisioning > contents > components > deliveryURL**

   **字段：** deliveryURL
   **描述：** 用于从内容交付网络或服务端点获取资产的可选唯一资源定位器。此URL用于由用户代理公开访问资产。
   **类型：**字符串
   **示例：** &quot;https://cdn.adobe.io/content/projectx/fragment/prod/static/1232324wd32.jpeg&quot;

* **_experience > decisioning > contents > components > linkURL**

   **字段：** linkURL
   **描述：** 用户交互的可选唯一资源定位器。此URL用于在用户代理中将最终用户引荐至，并可进行跟踪。
   **类型：**字符串
   **示例：** &quot;https://cdn.adobe.io/tracker?code=23432&amp;redirect=/content/projectx/fragment/prod/static/1232324wd32.jpeg&quot;

**_experience > decisioning > contents > placement**

**字段：** 版面
**标题：** 版面
**描述：** 要符合的版面。值是所引用的选件版面的URI(@id)。 请参阅架构https://ns.adobe.com/experience/decisioning/placement 。
**类型：**&#x200B;字符串

#### _experience >决策>生命周期状态

**字段：** lifecycleStatus标
**题：** 生命周期状
**态描述：** 生命周期状态允许使用对象执行工作流。当某个对象可见或被认为相关时，状态可能会受到影响。 状态更改由使用对象的客户端或服务驱动。
**类型：** 字符串
**可能值：** “草稿”（默认）、“已批准”、“实时”、“已完成”、“已存档”

#### _experience > decisioning >决策选项名称

**字段：** 名称
**标题：** 决策选项名称
**描述：** 在各种用户界面中显示的选项名称。**类型：**&#x200B;字符串

#### _experience > decisioning > tag

**字段：** 标记
**标题：** 标记
**描述：** 与此实体关联的标记集。标记在过滤器表达式中使用，用于将整体库存限制为子集（类别）。
**类型：** 数组

<!--Field without name under tags: Description: An identifier of a tag object. The value is the @id of the tag that is referenced. See tag schema: https://ns.adobe.com/experience/decisioning/tag. Type: string-->

## _repo

**字段：** _repo
**类型：** 对象

### _repo >决策选项ETag

**字段：** 标
**题：** 决策选项ETag
**描述：** 拍摄快照时决策选项对象所在的修订版本。**类型：**&#x200B;字符串
