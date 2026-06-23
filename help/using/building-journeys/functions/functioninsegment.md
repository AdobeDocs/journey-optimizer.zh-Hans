---
product: journey optimizer
title: inSegment
description: 了解inSegment中的函数
feature: Journeys
role: Developer
level: Experienced
keywords: inSegment，函数，表达式，历程
exl-id: 8417af75-6e97-4ad4-86b4-3ecd264a5560
version: Journey Orchestration
feature_v2: []
subfeature_v2: []
source-git-commit: bf5866b0e7437f93936f573fd83ada8526fe004d
workflow-type: tm+mt
source-wordcount: 521
ht-degree: 2%

---

# inSegment {#inSegment}

检查个人是否属于给定受众。

>[!NOTE]
>
>您最多可以检索100个受众。

受众名称必须是字符串常量。 它不能是字段引用，也不能是表达式。

受众是在[Adobe Experience Platform](https://platform.adobe.com/audience/overview)中定义的。 表达式编辑器提供自动完成的受众列表。

受众可以有两种状态：

* 已实现：实体符合区段定义的条件。
* 退出：实体正在退出区段定义。

只有具有&#x200B;**已实现**&#x200B;受众参与状态的个人才会被视为受众的成员。 有关如何评估受众的更多信息，请参阅[分段服务文档](https://experienceleague.adobe.com/docs/experience-platform/segmentation/tutorials/evaluate-a-segment.html#interpret-segment-results)。

`inSegment('segmentName') == true`表示您拥有segmentMembership且状态为entered/existing。

`inSegment('segmentName') == false`表示您具有已退出状态的segmentMembership。

## 类别

Adobe Experience Platform

## 函数语法

`inSegment(<parameter>)`

## 参数

| 参数 | 说明 | 类型 |
|--- |--- |--- |
| 区段 | 受众名称 | `<string>` |

## 签名和返回的类型

`inSegment(<string>)`

返回布尔值。

## 示例

`inSegment("men over 50")`

说明：

如果历程实例中的个人是名为“50岁以上的男性”的Adobe Experience Platform受众的一部分，则函数将返回&#x200B;**[!UICONTROL true]**，否则返回&#x200B;**[!UICONTROL false]**。

+++ AI知识参考

本节包含结构化知识，用于支持与本主题相关的解释、检索和问答。

要全面了解相关信息，应将此信息与本页上的文档相结合。 这两个源都不是独立的；页面描述了功能，而本节提供了其他上下文来帮助消除术语、意图、适用性和约束条件的歧义。

* **TL；DR：**&#x200B;此页面记录旧版`inSegment`函数，该函数检查历程配置文件是否属于指定的Adobe Experience Platform受众并返回布尔值。

**意图：**
* 使用`inSegment`检查个人资料是否为指定受众的活动成员
* 使用`inSegment('name') == true`确认历程条件中已实现（活动）的受众成员资格
* 使用`inSegment('name') == false`确认退出（非活动）的受众成员资格

**术语表：**
* **已实现**：受众参与状态，这意味着实体当前符合区段定义&#x200B;*（产品特定）*&#x200B;的条件
* **已退出**：受众参与状态，表示实体正在离开或已经离开区段定义&#x200B;*（产品特定）*

**护栏：**
* 在单个历程中最多可以检索100个受众
* 受众名称必须是字符串常量；不支持将字段引用和表达式作为参数

**术语：**
* 规范名称：inSegment — 首字母缩略词：none — 变体：inAudience （当前首选函数）
* 同义词： &quot;inSegment&quot; = &quot;audience membership check&quot;（旧版）
* 请勿混淆：“inSegment”（旧版/已弃用的函数）≠“inAudience”（当前推荐的函数）
* 请勿混淆：“已实现”（活动成员）≠“已退出”（不再是成员）

**常见问题解答：**
* **问：`inSegment`与`inAudience`之间有何区别？** — `inSegment`是旧函数名称；`inAudience`是当前推荐的函数。 两者都检查受众成员资格，但`inAudience`具有更完整的文档，包括护栏和传播时间详细信息。
* **问：`inSegment('name') == true`是什么意思？**  — 这意味着用户档案具有“已实现”segmentMembership状态，即个人是受众的活动成员。
* **问：能否将动态表达式作为受众名称传递？**  — 否，受众名称必须是字符串常量；不支持字段引用和表达式。
* **问：在一个历程中可以评估多少个受众？**  — 在单个历程中最多可检索100个受众。

+++
