---
solution: Journey Optimizer, Experience Platform
product: Journey Optimizer
title: 产品建议目录导出快速入门
description: 了解如何将产品建议目录导出为数据集
badge: label="旧版" type="Informative"
feature: Decision Management, Datasets
topic: Integrations
role: User, Developer
level: Intermediate
exl-id: f30abea1-b204-4470-9836-75fae916bbb1
version: Journey Orchestration
TQID: https://experienceleague.adobe.com/71W86v7R-wgsa7JDTE3d6Lddc71MOcTxrY5l0Ts600o
product_v2: id: cb954087-f4fc-4456-afb9-e939cabcdc79id: edbd1a0e-46c8-49da-8c10-dba9ec80bba9
feature_v2: id: ed0d8d0e-04b9-4326-be72-a0fbca265377id: fe338112-e2ce-4876-8989-fc4d497613f1id: fe96aceb-8194-4a8a-a6b0-75302d02804d
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
level_v2: id: b5a62a22-46f7-4f0d-b151-3fc640bef588
source-git-commit: f9b8e1590f14cdcd00432295c653769f753b9b40
workflow-type: tm+mt
source-wordcount: 133
ht-degree: 100%

---

# 产品建议目录导出快速入门 {#export-catalog}

>[!TIP]
>
>决策是 [!DNL Adobe Journey Optimizer] 的全新决策功能，现已通过基于代码的体验和电子邮件渠道提供！ [了解详情](../../experience-decisioning/gs-experience-decisioning.md)

Journey Optimizer 允许您自动将产品建议目录导出到 Adobe Experience Platform。

导出会为产品建议库的每个对象创建一个数据集（请参阅[访问导出的数据集](../export-catalog/access-dataset.md)）。 其包括：

* 个性化产品建议
* 后备产品建议
* 投放位置
* 决策

每次在产品建议库中修改其中一个对象时，都会自动执行新的导出作业来更新数据集。

>[!NOTE]
>
>默认情况下，此功能处于启用状态。 您无需执行任何其他激活步骤即可开始使用该功能。 启用后，将自动进行导出作业，无需您采取任何操作。

<!--
>[!NOTE]
>
>This feature is not enabled by default. If you want to use it, reach out to your Adobe contact to have it activated for your catalog. Once it is enabled, export jobs will be automated and will require no action from your side.
-->
