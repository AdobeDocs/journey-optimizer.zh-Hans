---
title: 回退优惠数据集
description: 此部分列表导出数据集中用于回退优惠的所有字段。
translation-type: tm+mt
source-git-commit: 70c172e19d5900c898d4850801468a2e186e682d
workflow-type: tm+mt
source-wordcount: '1003'
ht-degree: 3%

---

# 回退优惠数据集{#fallback-dataset}

每次修改优惠时，都会更新自动生成的回退优惠数据集。

![](../../assets/dataset-fallback.png)

数据集中最近成功的批处理显示在右侧。 数据集模式的层次视图显示在左窗格中。

>[!NOTE]
>
>了解如何访问[本节](../export-catalog/access-dataset.md)中优惠库每个对象的导出数据集。

以下是可在&#x200B;**[!UICONTROL Decision Object Repository - Fallback Offers]**&#x200B;数据集中使用的所有字段的列表。

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

#### 特征

**字段：特** 性标
**题：决策** 选项特性
**描述：属** 于此特定决策选项的其他属性或属性。不同的实例可能具有不同的特性（映射中的键）。 特征是用于区分一个决策选项和其他决策选项的名称值对。 特征用作表示此决策选项的内容中的值，并用作分析和优化选项性能的功能。 当每个实例具有相同的属性或属性时，该方面应建模为派生自决策选项详细信息的扩展模式。
**类型：对** 象

<!--Field under Characteristics without title = additionalProperties? Desc = Value of the property. Type: string-->

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
         **描述：** 资源的物理或数字表现。通常，格式应包括资源的媒体类型。 格式可用于确定显示或操作资源所需的软件、硬件或其他设备。 建议的最佳做法是从受控词汇中选择一个值(例如，[定义计算机媒体格式的](http://www.iana.org/分配/媒体类型/)的列表)。
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

#### 标记

**字段：** 标记
**标题：** 标
**签** 描述：与此实体关联的标签集。这些标记用于筛选表达式，以将整体库存限制为子集(类别)。
**类型：数** 组

<!--Field without name under tags: Description: An identifier of a tag object. The value is the @id of the tag that is referenced. See tag schema: https://ns.adobe.com/experience/decisioning/tag. Type: string-->

## _repo

### 决策选项ETag

**字段：** 标
**题：** 决策选项ETag
**描述：** 决策选项对象在拍摄快照时所在的修订版本。**类型：**&#x200B;字符串
