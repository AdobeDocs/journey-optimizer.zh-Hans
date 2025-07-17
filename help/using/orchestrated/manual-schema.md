---
solution: Journey Optimizer
product: journey optimizer
title: 配置步骤
description: 了解如何直接通过用户界面创建关系架构。
badge: label="Alpha"
hide: true
hidefromtoc: true
exl-id: 8c785431-9a00-46b8-ba54-54a10e288141
source-git-commit: aefc95b755074dfa043bad7dfd4acbd8dfb8e939
workflow-type: tm+mt
source-wordcount: '300'
ht-degree: 7%

---

# 手动模式 {#manual-schema}

+++ 目录

| 欢迎使用编排的营销活动 | 启动第一个精心策划的营销活动 | 查询数据库 | 精心策划的营销活动 |
|---|---|---|---|
| [开始使用编排的营销活动](gs-orchestrated-campaigns.md)<br/><br/>创建和管理关系架构和数据集：</br><ul><li>[手动架构](manual-schema.md)</li><li>[文件上载架构](file-upload-schema.md)</li><li>[摄取数据](ingest-data.md)</li></ul><br/><br/>[访问和管理编排的营销活动](access-manage-orchestrated-campaigns.md)<br/><br/>[创建编排的营销活动的关键步骤](gs-campaign-creation.md) | [创建和计划营销活动](create-orchestrated-campaign.md)<br/><br/>[编排活动](orchestrate-activities.md)<br/><br/>[启动并监视营销活动](start-monitor-campaigns.md)<br/><br/>[报告](reporting-campaigns.md) | [使用规则生成器](orchestrated-rule-builder.md)<br/><br/>[生成您的第一个查询](build-query.md)<br/><br/>[编辑表达式](edit-expressions.md)<br/><br/>[重新定位](retarget.md) | [开始使用活动](activities/about-activities.md)<br/><br/>活动：<br/>[并加入](activities/and-join.md) - [生成受众](activities/build-audience.md) - [更改维度](activities/change-dimension.md) - [渠道活动](activities/channels.md) - [组合](activities/combine.md) - [重复数据删除](activities/deduplication.md) - [扩充](activities/enrichment.md) - [分支](activities/fork.md) - [协调](activities/reconciliation.md) - [保存受众](activities/save-audience.md) - [拆分](activities/split.md) - [等待](activities/wait.md) |

{style="table-layout:fixed"}

+++

</br>

>[!BEGINSHADEBOX]

此页面上的内容不是最终内容，可能会发生变化。

>[!ENDSHADEBOX]

关系模式可以直接通过用户界面创建，从而能够对属性、主键、版本控制字段和关系进行详细配置。

以下示例手动定义忠诚度成员资格架构，以说明编排的营销活动所需的结构。

1. 登录到Adobe Experience Platform。

1. 导航到&#x200B;**数据管理** > **架构**。

1. 单击&#x200B;**创建架构**。

1. 系统将提示您选择以下两种架构类型：

   * **标准**
   * **关系**，专门用于编排的营销活动

   ![](assets/admin_schema_1.png)

1. 提供&#x200B;**架构名称**（例如，`test_demo_ck001`）。
1. 选择&#x200B;**架构类型**：
   **记录类型** （AGO营销活动需要）
   **时间序列**（此处不适用）
1. 单击&#x200B;**完成**&#x200B;以继续架构设计画布。

## 选择要导入的实体和字段

1. 在画布中，将属性（字段）添加到架构。
1. 添加&#x200B;**主键** （必需）。
1. 添加&#x200B;**版本描述符**&#x200B;属性（用于CDC支持）：
此类型必须为&#x200B;**日期时间**&#x200B;或&#x200B;**数值** （整数、长、短、字节）。
常见示例： `last_modified`

> **为什么？** **主键**&#x200B;唯一标识每个记录，**版本描述符**&#x200B;跟踪更改，支持CDC（更改数据捕获）和数据镜像。

1. 将相应的字段标记为&#x200B;**主键**&#x200B;和&#x200B;**版本描述符**。
1. 单击&#x200B;**保存**。


<!--

## 5. Creating a Dataset

1. Navigate to **Datasets**.
1. Click on **Create Dataset**.
1. Select the schema you just created.
1. Assign a **Dataset Name** (same as schema is fine).
1. Optionally, add tags (e.g., `AGO_campaigns`).
6. Ensure the checkbox **"Relational Schema"** is checked.
7. Click **Finish**.

> **Note:** Only one dataset can be created per relational schema.


## 6. Enabling the Dataset

1. Click **Enable** for the dataset.
1. Wait a few moments for the status to show **Enabled**.

> **Why?** Without enabling, the dataset cannot be used in orchestrated campaigns or ingest data.

## 7. Creating a Data Source (S3)

1. Navigate to **Sources**.
1. Click **Create Source**.
1. Choose the source type (e.g., **S3 Bucket**).
1. Provide connection details:
    - Bucket Path (optionally include subfolder path)
1. Save the source.

## 8. Preparing and Uploading Data

1. Prepare your CSV file with:
    - Column headers matching your schema attributes
    - `last_modified` column
    - `change_type` column (`U`/`DU` for upsert, `D` for delete)

> **Important:** `change_type` is required but does not need to be defined in the schema.

1. Save the file as `.csv`.

1. Upload the file to the specified folder in your S3 bucket.


## 9. Ingesting Data from S3

1. Go to **Sources** and find your S3 source.
1. Click **Add Data**.
1. Select the uploaded file.
1. Specify the file format as **CSV** and any compression type if applicable.
1. Review the data preview (ensure `change_type`, `last_modified`, and primary key are visible).
1. Click **Next**.

### Enable Change Data Capture (CDC)

- Check **Enable Change Data Capture**.
- Select the dataset enabled for AGO campaigns.

### Field Mapping

- Fields are auto-mapped (note that `change_type` is not mapped and that's expected).
- Click **Next**.

### Scheduling

- Schedule ingestion frequency (minute, hour, day, week).
- Set start time (immediate or future).
- Click **Finish** to create the data flow.

## 10. Monitoring Data Flow

1. Navigate back to **Sources > Data Flows**.
1. Wait 4–5 minutes for the first run (initial overhead).
1. Monitor:
    - Status (Started, Completed)
    - Number of records ingested
    - Errors (if any)

> **Tip:** Ingested data first lands in the **Data Lake**.

## 11. Data Replication to Data Store

The **Data Store** is updated:

- Every **15 minutes**, or

- If **Data Lake size exceeds 5MB**

This is a background replication process.


## 12. Querying the Dataset

1. Navigate to **Query Services**.
1. Click **Create Query**.
1. Example query:

   ```sql
   SELECT * FROM test_demo_ck001;
   ```

1. Run the query.

> **Note:** If ingestion is incomplete, query will return an error. Check data flow status.

-->