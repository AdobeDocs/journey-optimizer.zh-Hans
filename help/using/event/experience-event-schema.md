---
title: 关于历程事件的ExperienceEvent架构
description: 了解旅程事件的ExperienceEvent模式
feature: 架构
topic: 管理
role: Administrator
level: Intermediate
source-git-commit: 8f77802fcaa23790f9de4e8f15e593643b13fb1e
workflow-type: tm+mt
source-wordcount: '320'
ht-degree: 1%

---

# 关于[!DNL Journey Optimizer]事件的ExperienceEvent架构

[!DNL Journey Optimizer] 事件是通过流摄取发送到Adobe Experience Platform的XDM体验事件。

因此，为[!DNL Journey Optimizer]设置事件的一个重要先决条件是，您熟悉Adobe Experience Platform的体验数据模型（或XDM）、如何构建XDM体验事件架构，以及如何将XDM格式的数据流式传输到Adobe Experience Platform。

## [!DNL Journey Optimizer]事件的架构要求

为[!DNL Journey Optimizer]设置事件的第一步是确保您定义了一个用于表示该事件的XDM架构，并创建了一个数据集，用于记录该事件在Adobe Experience Platform上的实例。 并非完全需要为事件创建一个数据集，但将事件发送到特定数据集将允许您维护用户的事件历史记录以供将来参考和分析，因此始终都是一个好主意。 如果您还没有适用于事件的架构和数据集，则可以在Adobe Experience Platform Web界面中完成这两项任务。

![](../assets/schema1.png)

任何将用于[!DNL Journey Optimizer]事件的XDM架构都应满足以下要求：

* 架构必须是XDM ExperienceEvent类的。

   ![](../assets/schema2.png)

* 对于系统生成的事件，架构必须包含Orchestration eventID字段组。 [!DNL Journey Optimizer] 使用此字段标识历程中使用的事件。

   ![](../assets/schema3.png)

* 声明用于标识事件主题的标识字段。 如果未指定身份，则可以使用身份映射。 不建议采取此做法。

   ![](../assets/schema4.png)

* 如果希望此数据稍后在历程中可供查找，请标记配置文件的架构和数据集。

   ![](../assets/schema5.png)

   ![](../assets/schema6.png)

* 您可以随时包含数据字段，以捕获要随事件一起包含的任何其他上下文数据，例如有关用户、从中生成事件的设备的信息、位置，或与事件相关的任何其他有意义的环境。

   ![](../assets/schema7.png)

   ![](../assets/schema8.png)
