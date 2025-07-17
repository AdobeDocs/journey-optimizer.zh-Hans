---
solution: Journey Optimizer
product: journey optimizer
title: 配置步骤
description: 了解如何将数据从受支持的源（如SFTP、云存储或数据库）引入Adobe Experience Platform。
badge: label="Alpha"
hide: true
hidefromtoc: true
source-git-commit: ea5ef4005be90973046d3f94ea4c2b92eb89ffb4
workflow-type: tm+mt
source-wordcount: '456'
ht-degree: 7%

---

# 引入数据 {#ingest-data}

+++ 目录

| 欢迎使用编排的营销活动 | 启动第一个精心策划的营销活动 | 查询数据库 | 精心策划的营销活动 |
|---|---|---|---|
| [开始使用编排的营销活动](gs-orchestrated-campaigns.md)<br/><br/>创建和管理关系架构和数据集</br> <ul><li>[架构和数据集入门](gs-schemas.md)</li><li>[手动架构](manual-schema.md)</li><li>[文件上载架构](file-upload-schema.md)</li><li>[摄取数据](ingest-data.md)</li></ul>[访问和管理编排的营销活动](access-manage-orchestrated-campaigns.md)<br/><br/>[创建编排的营销活动的关键步骤](gs-campaign-creation.md) | [创建和计划营销活动](create-orchestrated-campaign.md)<br/><br/>[编排活动](orchestrate-activities.md)<br/><br/>[启动并监视营销活动](start-monitor-campaigns.md)<br/><br/>[报告](reporting-campaigns.md) | [使用规则生成器](orchestrated-rule-builder.md)<br/><br/>[生成您的第一个查询](build-query.md)<br/><br/>[编辑表达式](edit-expressions.md)<br/><br/>[重新定位](retarget.md) | [开始使用活动](activities/about-activities.md)<br/><br/>活动：<br/>[并加入](activities/and-join.md) - [生成受众](activities/build-audience.md) - [更改维度](activities/change-dimension.md) - [渠道活动](activities/channels.md) - [组合](activities/combine.md) - [重复数据删除](activities/deduplication.md) - [扩充](activities/enrichment.md) - [分支](activities/fork.md) - [协调](activities/reconciliation.md) - [保存受众](activities/save-audience.md) - [拆分](activities/split.md) - [等待](activities/wait.md) |

{style="table-layout:fixed"}

+++

</br>

>[!BEGINSHADEBOX]

</br>

内容

此页面上的内容不是最终内容，可能会发生变化。

>[!ENDSHADEBOX]

Adobe Experience Platform允许从外部源摄取数据，同时让您能够使用Experience Platform服务来构建、标记和增强传入数据。 您可以从各种源中摄取数据，如 Adobe 应用程序、基于云的存储、数据库和许多其他源。

## 使用云存储 {#ingest}

<!--
>[!IMPORTANT]
>
>Each dataset in Adobe Experience Platform supports only one active dataflow at a time. For detailed setup guidance on how to switch data sources, refer to this [section](#cdc-ingestion).
-->

您可以配置数据流以将数据从Amazon S3源摄取到Adobe Experience Platform中。 配置完毕后，该数据流即支持自动、计划地摄取结构化数据，并支持实时更新。

1. 从&#x200B;**[!UICONTROL 连接]**&#x200B;菜单中，访问&#x200B;**[!UICONTROL 源]**&#x200B;菜单。

1. 选择&#x200B;**[!UICONTROL 云存储]**&#x200B;类别，然后选择Amazon S3，然后单击&#x200B;**[!UICONTROL 添加数据]**。

   ![](assets/admin_sources_1.png)

1. 连接您的S3帐户：

   * 使用现有帐户

   * 使用新帐户

   [请参阅Adobe Experience Platform文档以了解详情](https://experienceleague.adobe.com/zh-hans/docs/experience-platform/destinations/catalog/cloud-storage/amazon-s3#connect)

   ![](assets/admin_sources_2.png)

1. 选择您的文件夹&#x200B;**[!UICONTROL 数据格式]**、**[!UICONTROL 分隔符]**&#x200B;和&#x200B;**[!UICONTROL 压缩类型]**。

1. 浏览连接的S3源，直到找到之前创建的两个文件夹，即&#x200B;**忠诚度奖励**&#x200B;和&#x200B;**忠诚度交易**。

1. 选择包含您的数据的文件夹。

   选择文件夹可确保自动处理具有相同结构的所有当前和未来文件。 但是，选择单个文件需要手动上传每个新的数据增量。

   ![](assets/S3_config_2.png)

1. 选择您的文件夹&#x200B;**[!UICONTROL 数据格式]**、**[!UICONTROL 分隔符]**&#x200B;和&#x200B;**[!UICONTROL 压缩类型]**。 检查样本数据的准确性，然后单击&#x200B;**[!UICONTROL 下一步]**。

   ![](assets/S3_config_1.png)

1. 选中&#x200B;**[!UICONTROL 启用变更数据捕获]**&#x200B;以从映射到关系架构且同时定义了主键和版本描述符的数据集中进行选择。

1. 选择您的[之前创建的数据集](#entities)，然后单击&#x200B;**[!UICONTROL 下一步]**。

   ![](assets/S3_config_3.png)

1. 在&#x200B;**[!UICONTROL 映射]**&#x200B;窗口中，验证每个源文件属性是否正确映射到目标架构中的相应字段。

   完成后，单击&#x200B;**[!UICONTROL 下一步]**。

   ![](assets/S3_config_4.png)

1. 根据所需频率配置数据流&#x200B;**[!UICONTROL 计划]**。

1. 单击&#x200B;**[!UICONTROL 完成]**&#x200B;以创建数据流。 那个按照规定的日程表自动执行。

1. 从&#x200B;**[!UICONTROL 连接]**&#x200B;菜单中，选择&#x200B;**[!UICONTROL 源]**&#x200B;并访问&#x200B;**[!UICONTROL 数据流]**&#x200B;选项卡，以跟踪流执行、查看摄取的记录并解决任何错误。

   ![](assets/S3_config_5.png)

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