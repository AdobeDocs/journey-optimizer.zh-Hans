---
title: 导出产品建议目录入门
description: 了解如何将产品建议目录导出为数据集
feature: Decision Management, Datasets
topic: Integrations
role: User, Data Engineer
level: Intermediate
exl-id: f30abea1-b204-4470-9836-75fae916bbb1
source-git-commit: 91584f394d956df4b69a885feacc40435360dae3
workflow-type: tm+mt
source-wordcount: '114'
ht-degree: 72%

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
>此功能默认处于启用状态。 您无需执行任何其他激活步骤即可开始使用该功能。 启用后，导出作业将自动完成，无需您执行任何操作。

<!--
>[!NOTE]
>
>This feature is not enabled by default. If you want to use it, reach out to your Adobe contact to have it activated for your catalog. Once it is enabled, export jobs will be automated and will require no action from your side.
-->
