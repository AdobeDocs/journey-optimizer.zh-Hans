---
solution: Journey Optimizer
product: journey optimizer
title: 配置步骤
description: 了解如何通过上传DDL在Adobe Experience Platform中创建关系架构
exl-id: 88eb1438-0fe5-4a19-bfb6-2968a427e9e8
version: Campaign Orchestration
source-git-commit: 059670c143595b9cacdf7e82a8a5c3efda78f30b
workflow-type: tm+mt
source-wordcount: '1084'
ht-degree: 48%

---


# 使用DDL文件创建关系架构 {#file-upload-schema}

通过创建架构（如&#x200B;**忠诚度会员资格**、**忠诚度交易**&#x200B;和&#x200B;**忠诚度奖励**）来定义编排营销活动所需的关系数据模型。 每个架构必须包含一个主键、一个版本控制属性和适当的关系以引用实体，如&#x200B;**收件人**&#x200B;或&#x200B;**品牌**。

可以通过界面手动创建架构，或使用DDL文件批量导入架构。

本部分提供分步指导，说明如何通过上传 DDL（数据定义语言）文件在 Adobe Experience Platform 中创建关系型架构。可使用 DDL 文件预先定义数据模型的结构，包括表、属性、键和关系。

1. [上传DDL文件](#ddl-upload)以创建关系架构并定义其结构。

1. [定义数据模型中表之间的关系](#relationships)。

1. [链接架构](#link-schema)以将关系数据与现有的配置文件实体（如收件人或品牌）连接。

1. 从支持的数据源[将数据摄取](ingest-data.md)至数据集中。

➡️ [在Adobe Experience Platform文档中了解有关关系架构的更多信息](https://experienceleague.adobe.com/zh-hans/docs/experience-platform/xdm/schema/relational)

## 上载DDL文件{#ddl-upload}

通过上传DDL文件，您可以预先定义数据模型的结构，包括表、属性、键和关系。

支持基于Excel的架构文件上传。 下载[提供的模板](assets/template.zip)以轻松准备架构定义。

+++在Adobe Experience Platform中创建关系架构时支持以下功能

* **枚举**\
  基于DDL的架构和手动架构创建均支持ENUM字段，从而允许您定义具有一组固定的允许值的属性。
示例如下：

  ```
  CREATE TABLE orders (
  order_id     INT NOT NULL,
  product_id   INT NOT NULL,
  order_date   DATE NOT NULL,
  customer_id  INT NOT NULL,
  quantity     INT NOT NULL,
  order_status enum ('PENDING', 'SHIPPED', 'DELIVERED', 'CANCELLED'),
  PRIMARY KEY (order_id, product_id)
  );
  ```

* 用于数据管理的&#x200B;**架构标签**\
  架构字段级别支持标签设置，以强制执行数据管理策略，例如访问控制和使用限制。 有关详细信息，请参阅[Adobe Experience Platform文档](https://experienceleague.adobe.com/docs/experience-platform/xdm/home.html?lang=zh-Hans)。

+++

1. 登录到Adobe Experience Platform。

1. 导航到&#x200B;**数据管理** > **架构**&#x200B;菜单。

1. 单击&#x200B;**创建架构**。

1. 选择&#x200B;**[!UICONTROL 关系]**&#x200B;作为&#x200B;**架构类型**。

   ![](assets/admin_schema_1.png)

1. 选择&#x200B;**[!UICONTROL 上传 DDL 文件]**&#x200B;以定义实体关系图并创建架构。

   表结构必须包含：
   * 至少一个主键。
   * 版本标识符，如 `datetime` 或 `number` 类型的 `lastmodified` 字段。
   * 对于变更数据捕获(CDC)摄取，为名为`_change_request_type`且类型为`String`的特殊列，它指示数据变更的类型（例如，插入、更新、删除）并启用增量处理。
   * DDL文件不能定义超过200个表。


   >[!IMPORTANT]
   >
   > 用于定位的任何架构必须至少包含一个类型为`String`且具有关联&#x200B;**标识命名空间**&#x200B;的标识字段。\
   >这可确保与Adobe Journey Optimizer的定位和身份解析功能兼容。

1. 拖放您的 DDL 文件并单击&#x200B;**[!UICONTROL 下一步]**。

   请注意，支持DDL文件的最大大小为10MB。

1. 键入您的&#x200B;**[!UICONTROL 架构名称]**。

1. 设置每个架构及其列，确保指定了主键和版本描述符。

   必须指定一个属性（如`lastmodified`）作为版本描述符（类型`datetime`、`long`或`int`），以确保使用最新数据更新数据集。 用户可以更改版本描述符，一旦设置，版本描述符将变为必需。 属性不能同时是主键(PK)和版本描述符。

   ![](assets/admin_schema_2.png)

1. 将属性标记为`identity`并将其映射到定义的身份命名空间。

1. 重命名、删除每个表或向每个表添加说明。

1. 完成后，单击&#x200B;**[!UICONTROL 完成]**。

您现在可以在画布中验证表和字段定义。[在下面的部分中了解更多信息](#entities)

## 定义关系 {#relationships}

创建架构时，可以直接在DDL文件中指定关系。 如果您希望定义文件外部的关系，可以在界面中按照以下步骤定义关系。

1. 访问数据模型的画布视图，然后选择要关联的两个表

1. 单击“源联接”旁边的 ![](assets/do-not-localize/Smock_AddCircle_18_N.svg) 按钮，然后拖动箭头指向“目标联接”连接以建立关联。

   >[!NOTE]
   >
   >如果在DDL文件中定义，则支持复合键。

   ![](assets/admin_schema_5.png)

1. 填写给定表单以定义链接，配置完毕后单击&#x200B;**应用**。

   ![](assets/admin_schema_3.png)

   **基数**：

   * **1-N**：源表的一个项可以对应目标表的多个项，但目标表的一个项最多对应源表的一个项。

   * **N-1**：目标表的一个项可以对应源表的多个项，但源表的一个项最多对应目标表的一个项。

   * **1-1**：源表的一个项最多对应目标表的一个项。

1. 数据模型中定义的所有链接在画布视图中均表示为箭头。单击两个表之间的箭头可查看详细信息、进行编辑或根据需要移除链接。

   ![](assets/admin_schema_6.png)

1. 使用工具栏自定义和调整画布。

   ![](assets/toolbar.png)

   * **放大**：放大画布，更清楚地查看数据模型的详细信息。

   * **缩小**：缩小画布大小，以便更全面地查看数据模型。

   * **适应视图**：调整缩放，适应可见区域内的所有架构。

   * **筛选**：选择要在画布中显示的架构。

   * **强制自动布局**：自动排列架构以便更好地进行组织。

   * **显示映射**：切换小映射叠加，有助于更轻松地浏览大型或复杂的架构布局。

   * **全部展开/折叠全部**：快速展开或折叠所有架构节点以显示或隐藏其属性。

   * **下载**：以.png文件格式下载ER图。

1. 完成后，单击&#x200B;**保存**。此操作将创建架构和关联的数据集，并启用数据集以用于精心策划的营销活动。

1. 单击&#x200B;**[!UICONTROL 打开作业]**，监控创建作业的进度。此过程可能需要几分钟时间，具体取决于 DDL 文件中的表数量。

   您还可以通过打开&#x200B;**[!UICONTROL 上传DDL文件]**&#x200B;窗口并选择&#x200B;**[!UICONTROL 查看所有DDL导入作业]**&#x200B;来访问DDL导入作业。

   ![](assets/admin_schema_4.png)

## 链接架构 {#link-schema}

>[!IMPORTANT]
>
> 系统只识别在DDL文件中明确定义的关系。 存在于DDL文件外部的任何实体关系将被忽略并且不会进行处理。

在&#x200B;**忠诚度交易**&#x200B;架构和&#x200B;**收件人**&#x200B;架构之间建立关系，使每个交易与正确的客户记录相关联。

1. 导航到&#x200B;**[!UICONTROL 架构]**，然后打开您之前创建的&#x200B;**忠诚度交易**。

1. 单击客户&#x200B;**[!UICONTROL 字段属性]**&#x200B;中的&#x200B;**[!UICONTROL 添加关系]**。

   ![](assets/schema_1.png)

1. 选择&#x200B;**[!UICONTROL 多对一]**&#x200B;作为关系&#x200B;**[!UICONTROL 类型]**。

1. 与现有的&#x200B;**收件人**&#x200B;架构相关联。

   ![](assets/schema_2.png)

1. 输入&#x200B;**[!UICONTROL 当前架构中的关系名称]**&#x200B;以及&#x200B;**[!UICONTROL 引用架构中的关系名称]**。

1. 单击&#x200B;**[!UICONTROL 应用]**&#x200B;保存更改。

继续在&#x200B;**忠诚度奖励**&#x200B;架构和&#x200B;**品牌**&#x200B;架构之间创建关系，将每个奖励条目与相应的品牌关联。

![](assets/schema_3.png)
