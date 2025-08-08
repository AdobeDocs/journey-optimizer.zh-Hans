---
solution: Journey Optimizer
product: journey optimizer
title: 配置步骤
description: 了解如何通过上传DDL在Adobe Experience Platform中创建关系架构
exl-id: 327597f6-8a53-42dc-966a-baae49b58bb3
source-git-commit: 7fc03d15c63789a2c35e3d517ca0c63f93545d4c
workflow-type: tm+mt
source-wordcount: '152'
ht-degree: 3%

---


# 关系架构和数据集入门{#gs-schemas}

本指南将指导您完成以下过程：创建关系架构、为编排的营销活动配置数据集以及摄取数据。

![](assets/do-not-localize/schema_admin.png)

1. 使用DDL文件[手动创建](manual-schema.md)关系架构[或](file-upload-schema.md)

   定义数据模型的结构，包括表、属性和关系。 选择在用户界面中手动构建架构，或上传DDL文件以加快设置。

   手动创建架构时，还必须手动创建和启用数据集。 使用DDL文件时，数据集创建和启用是自动的。

1. [关联架构](file-upload-schema.md)

   在架构之间建立关系以确保数据一致性并启用跨实体查询。 例如，将忠诚度交易关联到收件人，或将奖励关联到品牌。

1. [摄取数据](ingest-data.md)

   将来自受支持源（如SFTP、云存储或数据库）的数据引入Adobe Experience Platform。

