---
solution: Journey Optimizer
product: journey optimizer
title: 配置步骤
description: 了解如何将数据从受支持的源（如SFTP、云存储或数据库）引入Adobe Experience Platform。
exl-id: 7f1e7985-b68e-43d6-9c8f-fea2469f8af9
version: Campaign Orchestration
source-git-commit: c584ce48029bd298b503a342a1e663eeeedbba42
workflow-type: tm+mt
source-wordcount: '699'
ht-degree: 21%

---


# 摄取数据 {#ingest-data}

>[!IMPORTANT]
>
>要更改数据集的数据源，必须先删除现有数据流，然后才能创建新数据流，以引用同一数据集和新源。
>
>Adobe Experience Platform在数据流和数据集之间实施严格的一对一关系。 这样，您就可以保持源和数据集之间的同步，以便进行准确的增量摄取。

Adobe Experience Platform 允许从外部源摄取数据，同时让您能够使用 Experience Platform 服务来构建、标记和增强传入数据。您可以从各种源中摄取数据，如 Adobe 应用程序、基于云的存储、数据库和许多其他源。

数据集是用于数据集合的存储和管理结构，通常是表格，其中包含架构（列）和字段（行）。成功引入Experience Platform的数据将作为数据集存储在数据湖中。

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
      <td><a href="https://experienceleague.adobe.com/en/docs/experience-platform/sources/ui-tutorials/create/cloud-storage/s3">Amazon S3</a></td>
    </tr>
    <tr>
      <td><a href="https://experienceleague.adobe.com/en/docs/experience-platform/sources/ui-tutorials/create/cloud-storage/google-cloud-storage">Google 云存储</a></td>
    </tr>
    <tr>
      <td><a href="https://experienceleague.adobe.com/en/docs/experience-platform/sources/ui-tutorials/create/cloud-storage/sftp">SFTP</a></td>
    </tr>
      <td rowspan="4">云数据仓库</td>
      <td><a href="https://experienceleague.adobe.com/en/docs/experience-platform/sources/ui-tutorials/create/databases/snowflake">Snowflake</a></td>
    </tr>
    <tr>
      <td><a href="https://experienceleague.adobe.com/en/docs/experience-platform/sources/ui-tutorials/create/databases/bigquery">Google BigQuery</a></td>
    </tr>
    <tr>
      <td><a href="https://experienceleague.adobe.com/en/docs/experience-platform/sources/ui-tutorials/create/cloud-storage/data-landing-zone">数据登陆区<a></td>
    </tr>
    <tr>
      <td><a href="https://experienceleague.adobe.com/en/docs/experience-platform/sources/ui-tutorials/create/databases/databricks">Azure Databricks</a></td>
    </tr>
    <tr>
      <td rowspan="3">基于文件的上传</td>
      <td><a href="https://experienceleague.adobe.com/en/docs/experience-platform/sources/ui-tutorials/create/local-system/local-file-upload">本地文件上传<a></td>
    </tr>

</tbody>
</table>

## 基于模型的架构数据卫生指南 {#cdc}

对于通过&#x200B;**[!UICONTROL 更改数据捕获]**&#x200B;启用的数据集，所有数据更改（包括删除）都会自动从源系统镜像到Adobe Experience Platform中。

由于Adobe Journey Optimizer促销活动要求使用&#x200B;**[!UICONTROL 变更数据捕获]**&#x200B;启用所有已载入的数据集，因此客户有责任管理源中的删除操作。 任何从源系统中删除的记录都将自动从Adobe Experience Platform中的相应数据集中删除。

要通过基于文件的摄取删除记录，客户的数据文件应使用`D`字段中的`Change Request Type`值标记记录。 这表示应在Adobe Experience Platform中删除该记录，以镜像源系统。

如果客户希望仅从Adobe Experience Platform中删除记录而不影响原始源数据，则可以使用以下选项：

* 用于变更数据捕获复制的&#x200B;**代理或经过清理的表**

  客户可以创建一个代理或经过清理的源表，以控制将哪些记录复制到Adobe Experience Platform。 然后，可以从该中间表中选择性地管理删除。

* **通过数据Distiller删除**

  如果获得许可，**数据Distiller**&#x200B;可用于直接在Adobe Experience Platform中支持删除操作，而不依赖于源系统。

  [了解有关数据Distiller的更多信息](https://experienceleague.adobe.com/en/docs/experience-platform/query/data-distiller/overview)

## 配置数据流

此示例演示了如何配置将数据结构化摄取到Adobe Experience Platform的数据流。 配置的数据流支持自动、计划的摄取并支持实时更新。

1. 在&#x200B;**[!UICONTROL 连接]**&#x200B;菜单中，访问&#x200B;**[!UICONTROL 源]**&#x200B;菜单。

1. 根据编排的营销活动的[支持的源](#supported)选择您的源。

   ![](assets/admin_sources_1.png)

1. 如果您选择基于云的源，请连接您的Cloud Storage或Google Cloud Storage帐户。

   ![](assets/admin_sources_2.png)

1. 选择要提取到Adobe Experience Platform中的数据。

   ![](assets/S3_config_1.png)

1. 从&#x200B;**[!UICONTROL 数据集详细信息]**&#x200B;页面，选中&#x200B;**[!UICONTROL 启用更改数据捕获]**&#x200B;以仅显示映射到基于模型的架构并包含主键和版本描述符的数据集。

[了解有关基于模型的架构数据卫生准则的更多信息](#cdc)

   >[!IMPORTANT]
   >
   > 仅对于&#x200B;**基于文件的源**，数据文件中的每一行必须包含值为`_change_request_type` (upsert)或`U` (delete)的`D`列。 如果没有此列，系统将不会将数据识别为支持更改跟踪，并且不会显示“编排的营销活动”切换开关，从而阻止选择数据集进行定位。

   ![](assets/S3_config_6.png)

1. 选择您之前创建的数据集并单击&#x200B;**[!UICONTROL 下一步]**。

   ![](assets/S3_config_3.png)

1. 如果仅使用基于文件的源，请从&#x200B;**[!UICONTROL 选择数据]**&#x200B;窗口中上载本地文件并预览其结构和内容。

   请注意，支持的最大大小为100MB。

1. 在&#x200B;**[!UICONTROL 映射]**&#x200B;窗口中，验证每个源文件属性是否正确映射到目标架构中的相应字段。 [了解有关定向维度的更多信息](target-dimension.md)。

   完成后，单击&#x200B;**[!UICONTROL 下一步]**。

   ![](assets/S3_config_4.png)

1. 根据所需频率，配置数据流&#x200B;**[!UICONTROL 计划]**。

1. 单击&#x200B;**[!UICONTROL 完成]**&#x200B;以创建数据流。这将按照定义的计划自动执行。

1. 从&#x200B;**[!UICONTROL 连接]**&#x200B;菜单中，选择&#x200B;**[!UICONTROL 源]**&#x200B;并访问&#x200B;**[!UICONTROL 数据流]**&#x200B;选项卡，即可跟踪流程执行状态、检查摄取的记录并对任何错误进行排查。

   ![](assets/S3_config_5.png)


