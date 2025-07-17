---
solution: Journey Optimizer
product: journey optimizer
title: 配置步骤
description: 了解如何通过上传DDL在Adobe Experience Platform中创建关系架构
badge: label="Alpha"
hide: true
hidefromtoc: true
source-git-commit: 1aa4f3e24a4cb7594232c0b25da8c9fd2e62c1de
workflow-type: tm+mt
source-wordcount: '804'
ht-degree: 1%

---

# 文件上传 {#file-upload-schema}

+++ 目录

| 欢迎使用编排的营销活动 | 启动第一个精心策划的营销活动 | 查询数据库 | 精心策划的营销活动 |
|---|---|---|---|
| [开始使用编排的营销活动](gs-orchestrated-campaigns.md)<br/><br/>创建和管理关系架构和数据集：</br> <ul><li>[手动架构](manual-schema.md)</li><li>[文件上载架构](file-upload-schema.md)</li><li>[摄取数据](ingest-data.md)</li></ul><br/><br/>[访问和管理编排的营销活动](access-manage-orchestrated-campaigns.md)<br/><br/>[创建编排的营销活动的关键步骤](gs-campaign-creation.md) | [创建和计划营销活动](create-orchestrated-campaign.md)<br/><br/>[编排活动](orchestrate-activities.md)<br/><br/>[启动并监视营销活动](start-monitor-campaigns.md)<br/><br/>[报告](reporting-campaigns.md) | [使用规则生成器](orchestrated-rule-builder.md)<br/><br/>[生成您的第一个查询](build-query.md)<br/><br/>[编辑表达式](edit-expressions.md)<br/><br/>[重新定位](retarget.md) | [开始使用活动](activities/about-activities.md)<br/><br/>活动：<br/>[并加入](activities/and-join.md) - [生成受众](activities/build-audience.md) - [更改维度](activities/change-dimension.md) - [渠道活动](activities/channels.md) - [组合](activities/combine.md) - [重复数据删除](activities/deduplication.md) - [扩充](activities/enrichment.md) - [分支](activities/fork.md) - [协调](activities/reconciliation.md) - [保存受众](activities/save-audience.md) - [拆分](activities/split.md) - [等待](activities/wait.md) |

{style="table-layout:fixed"}

+++

</br>

>[!BEGINSHADEBOX]

此页面上的内容不是最终内容，可能会发生变化。

>[!ENDSHADEBOX]

通过创建架构（如&#x200B;**忠诚度会员资格**、**忠诚度交易**&#x200B;和&#x200B;**忠诚度奖励**）来定义编排营销活动所需的关系数据模型。 每个架构必须包含一个主键、一个版本控制属性和适当的关系，以引用实体，如&#x200B;**收件人**&#x200B;或&#x200B;**品牌**。

可以通过界面手动创建架构，或使用DDL文件批量导入架构。

本节提供了有关如何通过上传DDL（数据定义语言）文件在Adobe Experience Platform中创建关系模式的分步指南。 使用DDL文件，您可以预先定义数据模型的结构，包括表、属性、键和关系。

## DDL文件上载 {#ddl-upload}

1. 登录到Adobe Experience Platform。

1. 导航到&#x200B;**数据管理** > **架构**。

1. 单击&#x200B;**创建架构**。

1. 系统将提示您选择以下两种架构类型：

   * **标准**
   * **关系**，专门用于编排的营销活动

   ![](assets/admin_schema_1.png)

1. 选择&#x200B;**上传DDL文件**&#x200B;以定义实体关系图并创建架构。

   表结构必须包含：
   * 至少一个主键
   * 版本标识符，如`lastmodified`或`datetime`类型的`number`字段。

1. 拖放您的DDL文件并单击&#x200B;**[!UICONTROL 下一步]**。

1. 键入您的&#x200B;**[!UICONTROL 架构名称]**。

1. 设置每个架构及其列，确保指定了主键。

   必须指定一个属性（如`lastmodified`）作为版本描述符。 此属性（通常为`datetime`、`long`或`int`类型）对于摄取过程至关重要，可确保使用最新数据版本更新数据集。

   ![](assets/admin_schema_2.png)

1. 完成后，单击&#x200B;**[!UICONTROL 完成]**。

您现在可以在画布中验证表和字段定义。 [在下面的部分了解详情](#entities)

## 定义关系 {#relationships}

要定义架构内各表之间的逻辑连接，请执行以下步骤。

1. 访问数据模型的画布视图，然后选择要链接的两个表

1. 单击Source联接旁边的![](assets/do-not-localize/Smock_AddCircle_18_N.svg)按钮，然后拖动箭头并引导至Target联接以建立连接。

   ![](assets/admin_schema_5.png)

1. 填写给定表单以定义链接，配置完毕后单击&#x200B;**应用**。

   ![](assets/admin_schema_3.png)

   **基数**：

   * **1-N**：源表格的一个存在可以拥有目标表格的多个对应存在，但目标表格的一个存在最多可以拥有源表格的一个对应存在。

   * **N-1**：目标表的一个存在可以具有源表的多个对应存在，但源表的一个存在最多可以具有目标表的一个对应存在。

   * **1-1**：源表格的一个存在最多可以具有目标表格的一个对应存在。

1. 数据模型中定义的所有链接在画布视图中均表示为箭头。 单击两个表之间的箭头可查看详细信息、进行编辑或根据需要删除链接。

   ![](assets/admin_schema_6.png)

1. 使用工具栏自定义和调整画布。

   ![](assets/toolbar.png)

   * **放大**：放大画布以更清楚地查看数据模型的详细信息。

   * **缩小**：缩小画布大小，以便更全面地查看数据模型。

   * **适合视图**：调整缩放以适合可见区域中的所有架构。

   * **筛选器**：选择要在画布中显示的架构。

   * **强制自动布局**：自动排列架构以便更好地进行组织。

   * **显示地图**：切换小型地图覆盖以帮助更轻松地导航大型或复杂的架构布局。

1. 完成后，单击&#x200B;**保存**。 此操作创建架构和关联的数据集，并启用数据集以用于编排的营销活动。

1. 单击&#x200B;**[!UICONTROL 打开作业]**&#x200B;以监视创建作业的进度。 此过程可能需要几分钟时间，具体取决于DDL文件中定义的表数。

   ![](assets/admin_schema_4.png)

## 链接架构 {#link-schema}

在&#x200B;**忠诚度交易**&#x200B;架构和&#x200B;**收件人**&#x200B;架构之间建立关系，以将每个交易与正确的客户记录相关联。

1. 导航到&#x200B;**[!UICONTROL 架构]**&#x200B;并打开您之前创建的&#x200B;**忠诚度交易记录**。

1. 单击客户&#x200B;**[!UICONTROL 字段属性]**&#x200B;中的&#x200B;**[!UICONTROL 添加关系]**。

   ![](assets/schema_1.png)

1. 选择&#x200B;**[!UICONTROL 多对一]**&#x200B;作为关系&#x200B;**[!UICONTROL 类型]**。

1. 链接到现有&#x200B;**收件人**&#x200B;架构。

   ![](assets/schema_2.png)

1. 输入来自当前架构&#x200B;**[!UICONTROL 的]**&#x200B;关系名称以及来自引用架构&#x200B;**[!UICONTROL 的]**&#x200B;关系名称。

1. 单击&#x200B;**[!UICONTROL 应用]**&#x200B;以保存更改。

继续在&#x200B;**忠诚度奖励**&#x200B;架构和&#x200B;**品牌**&#x200B;架构之间创建关系，将每个奖励条目与相应的品牌关联。

![](assets/schema_3.png)

<!--### Setting Up Change data capture ingestion {#cdc-ingestion}

If you need to change the data source, you must delete the existing dataflow and create a new one pointing to the same dataset with the new source.

When using Change Data Capture (CDC), it is essential that the source and dataset remain in sync to ensure accurate incremental updates. Follow the steps below:

1. **Schema Requirements**
   - Your schema must include:
     - A **primary key** (e.g., `transaction_id`)
     - A **versioning field** (e.g., `lastmodified` or an incrementing `version_id`)
   - Enable the dataset for **Orchestrated Campaigns** if needed.

2. **CDC Dataflow Setup**
   - During dataflow creation, after choosing your source and files:
     - **Enable the CDC option**
     - Select your CDC-ready dataset
     - Confirm field mappings (especially version field)

3. **Keep Source and Target in Sync**
   - The source system must consistently update the version field so the platform can detect changes accurately.

Once set up, the platform will automatically ingest **only changed or new records** each time the flow runs.
-->