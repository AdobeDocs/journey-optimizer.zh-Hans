---
title: 版面数据集
description: 此部分列表了导出数据集中用于版面的所有字段。
translation-type: tm+mt
source-git-commit: 70c172e19d5900c898d4850801468a2e186e682d
workflow-type: tm+mt
source-wordcount: '350'
ht-degree: 4%

---

# 版面数据集{#placements-dataset}

每次修改优惠时，都会更新版面的自动生成数据集。

![](../../assets/dataset-placements.png)

数据集中最近成功的批处理显示在右侧。 数据集模式的层次视图显示在左窗格中。

>[!NOTE]
>
>了解如何访问[本节](../export-catalog/access-dataset.md)中优惠库每个对象的导出数据集。

以下是可在&#x200B;**[!UICONTROL Decision Object Repository - Placements]**&#x200B;数据集中使用的所有字段的列表。

<!--A placement describes a location or place in a personalized message. It is used to set technical constraints for content that the personalization decision supplies. The placement also represents a request to produce certain types of metrics when an experience event is produced where this placement is involved. For instance, the placement facilitates a personalized clickable image inside an email shown to an end-user. The placement may for instance request from the assembled experience that the click on its image gets reported in an experience event with a metric https://ns.adobe.com/xdm/data/metrics/web/linkclicks and a reference to this placement.-->

## 标识符

**Field:_id** Title:Identifier 
**Description:** 记录
**** 的唯一标识符。**类型：**&#x200B;字符串

## _experience（体验）

**Field:** _experience 
**Type:** object

### 决策

**字段：** 决策
**类型：对** 象

#### 版面的渠道标识符

**字段：** channelID
**标题：** 放置的渠道标
**识符** 描述：提出建议的渠道。该值是有效的渠道URI。 请参阅https://ns.adobe.com/xdm/channels/channel。
**类型：**&#x200B;字符串

#### 内容组件类型

**Field:component** Type 
**Title:Content Component Type** Description:
**** 每个值映射到给定给内容组件的类型的枚举的URI集。内容表示的某些用户希望@type值是对描述内容组件其他属性的模式的引用。
**类型：**&#x200B;字符串

#### contentTypes

**字段：** contentTypes 
**Type:** array

* **MIME媒体类型**

   **标题：** MIME媒体类型
   **描述：** 在该位置中预期的组件的媒体类型的约束。一个组件可能有多个媒体类型，如不同的图像格式。
   **类型：**&#x200B;字符串

#### 位置说明

**字段：** 说明
**标题：** 放置描述
**描述说明：** 它用于传达关于动态内容在整体消息投放中如何使用的可读意图。网页中的特定空间是\&quot;横幅\&quot;通常通过描述而不是通过正式方法来传达。
**类型：**&#x200B;字符串

#### 版面名称

**字段：** 名称
**标题：** 版面名
**称说明：** 在人机交互中引用该版面的指定名称。**类型：**&#x200B;字符串

## _repo

**Field:** _repo 
**Type:** object

### 放置ETag

**字段：** etag标
**题：** 放置ETag
**描述：** 拍摄快照时决策选项对象所在的修订版本。**类型：**&#x200B;字符串
