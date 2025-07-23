---
solution: Journey Optimizer
product: journey optimizer
title: 配置步骤
description: 了解如何将数据从受支持的源（如SFTP、云存储或数据库）引入Adobe Experience Platform。
badge: label="Alpha"
hide: true
hidefromtoc: true
exl-id: 7f1e7985-b68e-43d6-9c8f-fea2469f8af9
source-git-commit: 6447f5d1a060037c0ceaa374db20966097585f9c
workflow-type: tm+mt
source-wordcount: '561'
ht-degree: 38%

---

# 摄取数据 {#ingest-data}

+++ 目录

| 欢迎了解精心策划的营销活动 | 启动第一个精心策划的营销活动 | 查询数据库 | 精心策划的营销活动 |
|---|---|---|---|
| [开始使用编排的营销活动](gs-orchestrated-campaigns.md)<br/><br/>创建和管理关系架构和数据集</br> <ul><li>[架构和数据集入门](gs-schemas.md)</li><li>[手动架构](manual-schema.md)</li><li>[文件上载架构](file-upload-schema.md)</li><li>[摄取数据](ingest-data.md)</li></ul>[访问和管理编排的营销活动](access-manage-orchestrated-campaigns.md)<br/><br/>[创建编排的营销活动的关键步骤](gs-campaign-creation.md) | [创建和计划营销活动](create-orchestrated-campaign.md)<br/><br/>[精心策划活动](orchestrate-activities.md)<br/><br/>[启动和监控营销活动](start-monitor-campaigns.md)<br/><br/>[报告](reporting-campaigns.md) | [使用规则生成器](orchestrated-rule-builder.md)<br/><br/>[生成您的第一个查询](build-query.md)<br/><br/>[编辑表达式](edit-expressions.md)<br/><br/>[重定向](retarget.md) | [活动快速入门](activities/about-activities.md)<br/><br/>活动：<br/>[并行汇聚](activities/and-join.md) - [生成受众](activities/build-audience.md) - [更改维度](activities/change-dimension.md) - [渠道活动](activities/channels.md) - [合并](activities/combine.md) - [重复数据删除](activities/deduplication.md) - [扩充](activities/enrichment.md) - [分叉](activities/fork.md) - [协调](activities/reconciliation.md) - [保存受众](activities/save-audience.md) - [拆分](activities/split.md) - [等待](activities/wait.md) |

{style="table-layout:fixed"}

+++

</br>

>[!BEGINSHADEBOX]

</br>

此页面上的内容不是最终内容，可能会发生变化。

>[!ENDSHADEBOX]

>[!IMPORTANT]
>
>要更改数据集的数据源，必须先删除现有数据流，然后才能创建新数据流，以引用同一数据集和新源。
>
>Adobe Experience Platform在数据流和数据集之间实施严格的一对一关系。 这样，您就可以保持源和数据集之间的同步，以便进行准确的增量摄取。

Adobe Experience Platform 允许从外部源摄取数据，同时让您能够使用 Experience Platform 服务来构建、标记和增强传入数据。您可以从各种源中摄取数据，如 Adobe 应用程序、基于云的存储、数据库和许多其他源。

## 编排的营销活动支持的源 {#supported}

以下源支持与编排的营销活动一起使用：

<table>
  <thead>
    <tr>
      <th>类型</th>
      <th>来源</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td rowspan="3">云存储</td>
      <td><a href="https://experienceleague.adobe.com/zh-hans/docs/experience-platform/sources/ui-tutorials/create/cloud-storage/s3">Amazon S3</a></td>
    </tr>
    <tr>
      <td><a href="https://experienceleague.adobe.com/zh-hans/docs/experience-platform/sources/ui-tutorials/create/cloud-storage/google-cloud-storage">Google 云存储</a></td>
    </tr>
    <tr>
      <td><a href="https://experienceleague.adobe.com/zh-hans/docs/experience-platform/sources/ui-tutorials/create/cloud-storage/sftp">SFTP</a></td>
    </tr>
      <td rowspan="4">云数据仓库</td>
      <td><a href="https://experienceleague.adobe.com/zh-hans/docs/experience-platform/sources/ui-tutorials/create/databases/snowflake">Snowflake</a></td>
    </tr>
    <tr>
      <td><a href="https://experienceleague.adobe.com/zh-hans/docs/experience-platform/sources/ui-tutorials/create/databases/bigquery">Google BigQuery</a></td>
    </tr>
    <tr>
      <td><a href="https://experienceleague.adobe.com/zh-hans/docs/experience-platform/sources/ui-tutorials/create/cloud-storage/data-landing-zone">数据登陆区<a></td>
    </tr>
    <tr>
      <td><a href="https://experienceleague.adobe.com/zh-hans/docs/experience-platform/sources/ui-tutorials/create/databases/databricks">Azure Databricks</a></td>
    </tr>
    <tr>
      <td rowspan="3">基于文件的上传</td>
      <td><a href="https://experienceleague.adobe.com/zh-hans/docs/experience-platform/sources/ui-tutorials/create/local-system/local-file-upload">本地文件上传<a></td>
    </tr>

</tbody>
</table>

## 配置数据流

此示例演示了如何配置将数据结构化摄取到Adobe Experience Platform的数据流。 配置的数据流支持自动、计划的摄取并支持实时更新。

1. 在&#x200B;**[!UICONTROL 连接]**&#x200B;菜单中，访问&#x200B;**[!UICONTROL 源]**&#x200B;菜单。

1. 根据编排的营销活动的[支持的源](#supported)选择您的源。

   ![](assets/admin_sources_1.png)

1. 如果您选择基于云的源，请连接您的Cloud Storage或Google Cloud Storage帐户。

   ![](assets/admin_sources_2.png)

1. 选择要摄取到Adobe Experience Platform中的数据。

   ![](assets/S3_config_1.png)

1. 从&#x200B;**[!UICONTROL 数据集详细信息]**&#x200B;页面，选中&#x200B;**[!UICONTROL 启用更改数据捕获]**&#x200B;以仅显示映射到关系架构并包含主键和版本描述符的数据集。

   >[!IMPORTANT]
   >
   > 仅对于&#x200B;**基于文件的源**，数据文件中的每一行必须包含值为`_change_request_type` (upsert)或`U` (delete)的`D`列。 如果没有此列，系统将不会将数据识别为支持更改跟踪，并且不会显示“编排的营销活动”切换开关，从而阻止选择数据集进行定位。

   ![](assets/S3_config_6.png)

1. 选择您之前创建的数据集并单击&#x200B;**[!UICONTROL 下一步]**。

   ![](assets/S3_config_3.png)

1. 如果仅使用基于文件的源，请从&#x200B;**[!UICONTROL 选择数据]**&#x200B;窗口中上载本地文件并预览其结构和内容。

   请注意，支持的最大大小为100MB。

1. 在&#x200B;**[!UICONTROL 映射]**&#x200B;窗口中，验证每个源文件属性是否正确映射到目标架构中的相应字段。

   完成后，单击&#x200B;**[!UICONTROL 下一步]**。

   ![](assets/S3_config_4.png)

1. 根据所需频率，配置数据流&#x200B;**[!UICONTROL 计划]**。

1. 单击&#x200B;**[!UICONTROL 完成]**&#x200B;以创建数据流。这将按照定义的计划自动执行。

1. 从&#x200B;**[!UICONTROL 连接]**&#x200B;菜单中，选择&#x200B;**[!UICONTROL 源]**&#x200B;并访问&#x200B;**[!UICONTROL 数据流]**&#x200B;选项卡，即可跟踪流程执行状态、检查摄取的记录并对任何错误进行排查。

   ![](assets/S3_config_5.png)

