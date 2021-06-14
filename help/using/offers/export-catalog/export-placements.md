---
title: 投放位置数据集
description: 此部分列出了在导出的数据集中用于版面的所有字段。
feature: 优惠
topic: 集成
role: User
level: Intermediate
source-git-commit: b58c5b527e594c03f3b415549e6b7cd15b050139
workflow-type: tm+mt
source-wordcount: '367'
ht-degree: 5%

---

# 投放位置数据集 {#placements-dataset}

每次修改选件时，都会更新自动生成的版面数据集。

![](../../assets/dataset-placements.png)

数据集中最近一次成功的批处理将显示在右侧。 数据集架构的分层视图将显示在左窗格中。

>[!NOTE]
>
>了解如何在[此部分](../export-catalog/access-dataset.md)中访问选件库每个对象的导出数据集。

以下是可在&#x200B;**[!UICONTROL Decision Object Repository - Placements]**&#x200B;数据集中使用的所有字段的列表。

<!--A placement describes a location or place in a personalized message. It is used to set technical constraints for content that the personalization decision supplies. The placement also represents a request to produce certain types of metrics when an experience event is produced where this placement is involved. For instance, the placement facilitates a personalized clickable image inside an email shown to an end-user. The placement may for instance request from the assembled experience that the click on its image gets reported in an experience event with a metric https://ns.adobe.com/xdm/data/metrics/web/linkclicks and a reference to this placement.-->

## 标识符

**字段：** _id标
**题：** 标识
**符描述：** 记录的唯一标识符。**类型：**&#x200B;字符串

## _experience（体验）

**字段：** _experience类
**型：** 对象

### _experience > decisioning

**字段：** 决策
**类型：** 对象

#### _experience > decisioning >版面的渠道标识符

**字段：** channelID 
**标题：** 版面的渠道标
**识符描述：** 提出建议的渠道。值是有效的渠道URI。 请参阅https://ns.adobe.com/xdm/channels/channel。
**类型：**&#x200B;字符串

#### _experience > decisioning >内容组件类型

**字段：** componentType 
**Title:** 内容组件类型
**描述：** 一个枚举的URI集，其中每个值映射到给定给内容组件的类型。内容表示的某些用户希望@type值作为对描述内容组件其他属性的架构的引用。
**类型：**&#x200B;字符串

#### _experience > decisioning > contentTypes

**字段：** contentTypes
**类型：** 数组

**_experience > decisioning > contentTypes > MIME媒体类型**

**标题：** MIME媒体类
**型描述：** 在该位置中预期的组件的媒体类型的约束。一个组件可能有多个媒体类型，如不同的图像格式。
**类型：**&#x200B;字符串

#### _experience > decisioning >版面描述

**字段：** 描述
**标题：** 版面描述
**描述：** 用于传达人类可读的意图，了解动态内容如何用于整体消息投放。网页中的某个空间是\&quot;横幅\&quot;通常通过描述而不是正式方法来传达。
**类型：**&#x200B;字符串

#### _experience > decisioning >版面名称

**字段：** 名称
**标题：** 版面名称
**描述：** 在人类交互中引用版面的分配名称。**类型：**&#x200B;字符串

## _repo

**字段：** _repo
**类型：** 对象

### _repo >放置集

**字段：** 标
**题：** 放置ETag
**描述：** 拍摄快照时决策选项对象所在的修订版本。**类型：**&#x200B;字符串
