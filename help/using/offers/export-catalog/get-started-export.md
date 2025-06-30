---
title: 导出产品建议目录入门
description: 了解如何将产品建议目录导出为数据集
badge: label="旧版" type="Informative"
feature: Decision Management, Datasets
topic: Integrations
role: User, Data Engineer
level: Intermediate
exl-id: f30abea1-b204-4470-9836-75fae916bbb1
source-git-commit: 87f3da0a1d73f9aa26c7420d260778286bacdf0c
workflow-type: tm+mt
source-wordcount: '115'
ht-degree: 99%

---

# 导出产品建议目录入门 {#export-catalog}

Journey Optimizer 允许您自动将产品建议目录导出到 Adobe Experience Platform。

导出会为产品建议库的每个对象创建一个数据集（请参阅[访问导出的数据集](../export-catalog/access-dataset.md)）。其包括：

* 个性化产品建议
* 后备产品建议
* 放置环境
* 决策

每次在产品建议库中修改其中一个对象时，都会自动执行新的导出作业来更新数据集。

>[!NOTE]
>
>默认情况下，此功能处于启用状态。您无需执行任何其他激活步骤即可开始使用该功能。启用后，将自动进行导出作业，无需您采取任何操作。

<!--
>[!NOTE]
>
>This feature is not enabled by default. If you want to use it, reach out to your Adobe contact to have it activated for your catalog. Once it is enabled, export jobs will be automated and will require no action from your side.
-->
