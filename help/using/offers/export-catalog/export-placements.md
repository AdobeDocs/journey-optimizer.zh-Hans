---
title: 投放位置数据集
description: 此部分列出了导出数据集中用于投放位置的所有字段
feature: Offers
topic: Integrations
role: User
level: Intermediate
exl-id: 3e45f3cf-e17e-43a6-8424-98afef07aaa3
source-git-commit: 78675ca22d8ee9a93d9af128d5708c305523da78
workflow-type: tm+mt
source-wordcount: '369'
ht-degree: 5%

---

# 投放位置数据集 {#placements-dataset}

每次修改选件时，都会更新自动生成的投放位置数据集。

![](../assets/dataset-placements.png)

数据集中最近成功的批次显示在右侧。 数据集的架构的分层视图显示在左窗格中。

>[!NOTE]
>
>了解如何在中访问选件库每个对象的导出数据集 [本节](../export-catalog/access-dataset.md).

以下是可在该字段中使用的所有字段的列表 **[!UICONTROL 决策对象存储库 — 投放位置]** 数据集。

<!--A placement describes a location or place in a personalized message. It is used to set technical constraints for content that the personalization decision supplies. The placement also represents a request to produce certain types of metrics when an experience event is produced where this placement is involved. For instance, the placement facilitates a personalized clickable image inside an email shown to an end-user. The placement may for instance request from the assembled experience that the click on its image gets reported in an experience event with a metric https://ns.adobe.com/xdm/data/metrics/web/linkclicks and a reference to this placement.-->

+++ 标识符

**字段：** _id
**标题：** 标识符
**描述：** 记录的唯一标识符。
**类型：**&#x200B;字符串

+++

+++ _experience（体验）

**字段：** 体验(_E)
**类型：** 对象

+++

+++ 体验>决策(_E)

**字段：** 决策
**类型：** 对象

+++

+++ _experience > decisioning >投放位置的渠道标识符

**字段：** channelId
**标题：** 投放的渠道标识符
**描述：** 提出建议的渠道。 该值为有效的渠道URI。 请参阅https://ns.adobe.com/xdm/channels/channel。
**类型：**&#x200B;字符串

+++

+++ _experience >决策>内容组件类型

**字段：** componenttype
**标题：** 内容组件类型
**描述：** 一组URI的枚举，其中每个值映射到为内容组件给定的类型。 内容表示的一些使用者期望@type值是对描述内容组件的其他属性的架构的引用。
**类型：**&#x200B;字符串

+++

+++ 体验>决策>内容类型(_E)

**字段：** contentType
**类型：** 数组

+++

+++_体验>决策>内容类型> MIME媒体类型

**标题：** MIME媒体类型
**描述：** 该投放位置中预期组件的媒体类型限制。 一个组件可能有多种媒体类型，例如不同的图像格式。
**类型：**&#x200B;字符串

+++

+++ _experience >决策>投放位置描述

**字段：** 描述
**标题：** 投放位置描述
**描述：** 它用于传达关于如何在整体消息投放中使用动态内容的可读意图。 网页中的特定空间是\“横幅\”，通常是通过描述而不是通过正式方法传达的。
**类型：**&#x200B;字符串

+++

+++ _experience >决策>投放位置名称

**字段：** name
**标题：** 版面名称
**描述：** 在人际交互中引用该投放位置的分配名称。
**类型：**&#x200B;字符串

+++

+++ 存储库(_R)

**字段：** 存储库(_R)
**类型：** 对象

+++

+++ _repo >版面ETag

**字段：** etag
**标题：** 投放ETag
**描述：** 拍摄快照时决策选项对象所处的修订版本。
**类型：**&#x200B;字符串

+++
