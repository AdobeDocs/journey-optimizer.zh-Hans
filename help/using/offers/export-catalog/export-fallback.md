---
title: 后备优惠数据集
description: 此部分列出了在导出数据集中用于后备优惠的所有字段
badge: label="旧版" type="Informative"
feature: Decision Management, Datasets
topic: Integrations
role: User, Data Engineer
level: Intermediate
exl-id: 73bfdc24-28cf-4cfd-bac9-a4ff1ea543e3
source-git-commit: 87f3da0a1d73f9aa26c7420d260778286bacdf0c
workflow-type: tm+mt
source-wordcount: '1017'
ht-degree: 0%

---

# 后备优惠数据集 {#fallback-dataset}

每次修改选件时，都会更新自动生成的备用选件数据集。

![](../assets/dataset-fallback.png)

数据集中最近成功的批次显示在右侧。 数据集的架构的分层视图显示在左窗格中。

>[!NOTE]
>
>在[本节](../export-catalog/access-dataset.md)中了解如何访问选件库每个对象的导出数据集。

以下是可用于&#x200B;**[!UICONTROL 决策对象存储库 — 后备优惠]**&#x200B;数据集中的所有字段的列表。

+++ 标识符

**字段：**_id
**标题：**标识符
**描述：**记录的唯一标识符。
**类型：**&#x200B;字符串

+++

+++ 体验(_E)

**字段：**体验(_E)
**类型：**&#x200B;对象

+++

+++ _experience > decisioning

**字段：**决策
**类型：**&#x200B;对象

+++

+++ _experience >决策>特征

**字段：**特性
**标题：**决策选项特性
**描述：**属于此特定决策选项的其他属性或特性。 不同的实例可以具有不同的特征（映射中的键）。 这些特征是用于区分一个决策选项和其他决策选项的名称值对。 特征会用作内容中表示此决策选项的值，并用作分析和优化选项性能的功能。 当每个实例具有相同的属性或属性时，该方面应建模为从决策选项详细信息派生的扩展模式。
**类型：**&#x200B;对象

+++

<!--Field under Characteristics without title = additionalProperties? Desc = Value of the property. Type: string-->

+++ _experience > decisioning >内容

**字段：**内容
**标题：**内容详细信息
**描述：**在不同上下文中呈现决策项的内容项。 单个决策选项可以具有多个内容变体。 内容是定向到受众以供在（数字）体验中使用的信息。 通过渠道将内容投放到特定投放位置。
**类型：**&#x200B;数组

+++

+++_experience > decisioning >内容>组件

**字段：**组件
**描述：**表示决策选项的内容组件，包括其所有语言变体。 特定组件通过“dx：format”、“dc：subject”和“dc：language”或其组合找到。 此元数据用于定位或表示与选件关联的内容，并根据版面合同对其进行集成。
**类型：**数组
**必需：** &quot;_type&quot;， &quot;_dc&quot; <!--TBC?-->

* **_experience >决策>内容>组件>内容组件类型**

  **字段：**类型(_T)
  **标题：**内容组件类型
  **描述：**枚举的URI集，其中每个值映射到为内容组件指定的类型。 内容表示的一些使用者希望@type值是对描述内容组件的其他属性的架构的引用。
  **类型：**&#x200B;字符串

* **_experience > decisioning >内容>组件> _dc**

  **字段：** _dc
  **类型：**对象
  **必需：** &quot;format&quot;

   * **格式**

     **字段：**格式
     **标题：**格式
     **描述：**&#x200B;资源的物理或数字形式。 通常，格式应包含资源的媒体类型。 格式可用于确定显示或操作资源所需的软件、硬件或其他设备。 建议的最佳做法是从受控词汇表中选择一个值(例如，定义计算机媒体格式的[Internet媒体类型]&#x200B;(https://www.iana.org/ assignments/media-types/)的列表)。
     **类型：**字符串
     **示例：** &quot;application/vnd.adobe.photoshop&quot;

   * **语言**

     **字段：**语言
     **标题：**语言
     **描述：**&#x200B;资源的语言。 \n语言是以[IETF RFC 3066](https://www.ietf.org/rfc/rfc3066.txt)中定义的语言代码指定的，它是BCP 47的一部分，在XDM中的其他位置使用。
     **类型：**数组
     **示例：** &quot;\n&quot;、&quot;pt-BR&quot;、&quot;es-ES&quot;

* **_experience > decisioning >内容>组件> _repo**

  **字段：**_repo
  **类型：**&#x200B;对象

   * **id**

     **字段：** ID
     **描述：**在内容存储库中引用资源的可选唯一标识符。 当使用平台API检索表示法时，客户端需要一个额外的属性\&quot;repo：resolveUrl\&quot;来检索资产。
     **类型：**字符串
     **示例：** &quot;urn:aaid:sc:US:6dc33479-13ca-4b19-b25d-c805eff8a69e&quot;

   * **name**

     **字段：**名称
     **描述：**有关在\&quot;repo：id\&quot;中查找存储外部资源的存储库的位置的一些提示。
     **类型：**&#x200B;字符串

   * **repositoryID**

     **字段：**存储库ID
     **描述：**在内容存储库中引用资源的可选唯一标识符。 当使用平台API检索表示法时，客户端需要一个额外的属性\&quot;repo：resolveUrl\&quot;来检索资产。
     **类型：**字符串
     **示例：** &quot;C87932A55B06F7070A49412D@AdobeOrg&quot;

   * **resolveURL**

     **字段：** resolveURL
     **描述：**用于读取内容存储库中资产的可选唯一资源定位器。 这样，无需客户了解资产的管理位置以及要调用的API，即可更轻松地获取资产。 这类似于HAL链接，但语义更简单，更有针对性。
     **类型：**字符串
     **示例：** &quot;https://plaftform.adobe.io/resolveByPath?path=&quot;/mycorp/content/projectx/fragment/prod/herobanners/banner14.html3&quot;

* **_experience > decisioning >内容>组件>内容**

  **字段：**内容
  **描述：**用于直接保存内容的可选字段。 组件可以直接保存简单的内容，而不是引用资产存储库中的内容。 此字段不适用于复合、复杂和二进制内容资产。
  **类型：**&#x200B;字符串

* **_experience > decisioning >内容>组件> deliveryURL**

  **字段：** deliveryURL
  **描述：**从内容交付网络或服务终结点获取资源的可选唯一资源定位器。 用户代理使用此URL公开访问资产。
  **类型：**字符串
  **示例：** &quot;https://cdn.adobe.io/content/projectx/fragment/prod/static/1232324wd32.jpeg&quot;

* **_experience > decisioning >内容>组件> linkURL**

  **字段：** linkURL
  **描述：**用于用户交互的可选唯一资源定位器。 此URL用于在用户代理中将最终用户引荐至，并且可以对其进行跟踪。
  **类型：**字符串
  **示例：** &quot;https://cdn.adobe.io/tracker?code=23432&amp;redirect=/content/projectx/fragment/prod/static/1232324wd32.jpeg&quot;

+++

+++ _experience > decisioning >内容>投放位置

**字段：**投放位置
**标题：**投放位置
**描述：**要遵循的位置。 该值是被引用的优惠投放位置的URI (@id)。 请参阅架构https://ns.adobe.com/experience/decisioning/placement 。
**类型：**&#x200B;字符串

+++

+++ _experience > decisioning >生命周期状态

**字段：**生命周期状态
**标题：**生命周期状态
**描述：**生命周期状态允许使用对象执行工作流。 当对象可见或被视为相关时，状态可能会受到影响。 状态更改由使用对象的客户端或服务驱动。
**类型：**字符串
**可能的值：**“草稿”（默认值）、“已批准”、“实时”、“已完成”、“已存档”

+++

+++ _experience >决策>决策选项名称

**字段：**名称
**标题：**决策选项名称
**描述：**显示在各种用户界面中的选项名称。
**类型：**&#x200B;字符串

+++

+++ _experience > decisioning >标记

**字段：**标记
**标题：**标记
**描述：**与此实体关联的集合限定符集（以前称为“标记”）。 集合限定符用在过滤器表达式中，以将整个库存限制为子集（类别）。
**类型：**&#x200B;数组

+++

<!--Field without name under collection qualifiers: Description: An identifier of a collection qualifier object. The value is the @id of the collection qualifier that is referenced. See tag schema: https://ns.adobe.com/experience/decisioning/tag. Type: string-->

+++ _repo

**字段：**_repo
**类型：**&#x200B;对象

+++

+++ _repo >决策选项ETag

**字段：** etag
**标题：**决策选项ETag
**描述：**拍摄快照时决策选项对象所处的修订版本。
**类型：**&#x200B;字符串

+++
