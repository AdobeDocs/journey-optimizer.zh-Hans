---
title: 版面数据集
description: 此部分列表了导出数据集中用于版面的所有字段。
translation-type: tm+mt
source-git-commit: d96a2b179ce652a119b6008e02b1409666f36402
workflow-type: tm+mt
source-wordcount: '393'
ht-degree: 4%

---

# 版面数据集{#placements-dataset}

每次修改优惠时，都会更新版面的自动生成数据集。

![](../assets/dataset-placements.png)

数据集中最近成功的批处理显示在右侧。 数据集模式的层次视图显示在左窗格中。

>[!NOTE]
>
>了解如何访问[本节](../export-catalog/access-dataset.md)中优惠库每个对象的导出数据集。

位置描述了个性化信息中的位置或位置。 它用于为个性化决策提供的内容设置技术限制。 该放置还表示在产生涉及此放置的体验事件时生成某些类型量度的请求。 例如，该位置便于在向最终用户显示的电子邮件中提供个性化的可点击图像。 例如，放置可以从组合体验中请求，在体验事件中，单击其图像会报告该量度https://ns.adobe.com/xdm/data/metrics/web/linkclicks和对此放置的引用。

以下是可在&#x200B;**[!UICONTROL Decision Object Repository - Placements]**&#x200B;数据集中使用的所有字段的列表。

## 标识符

记录的唯一标识符。

类型：字符串

## _experience（体验）

### 决策

#### 版面的渠道标识符

提出建议的渠道。 该值是有效的渠道URI。 请参阅https://ns.adobe.com/xdm/channels/channel。

类型：字符串

#### 内容组件类型

一个枚举的URI集，其中每个值映射到给予内容组件的类型。 内容表示的某些用户希望@type值是对描述内容组件其他属性的模式的引用。

类型：字符串

#### MIME媒体类型

在该位置中预期的元件的媒体类型的约束。 一个组件可能有多个媒体类型，如不同的图像格式。

类型：字符串

#### 位置说明

它用于传达用户可读的意图，即动态内容在整体消息投放中的使用方式。 网页中的特定空间是\&quot;横幅\&quot;通常通过描述而不是通过正式方法来传达。

类型：字符串

#### 版面名称

在人类交互中引用该位置的指定名称。

类型：字符串

## _repo

### 放置ETag

拍摄快照时决策选项对象所在的修订版本。

类型：字符串
