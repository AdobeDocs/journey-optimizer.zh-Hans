---
solution: Journey Optimizer
product: journey optimizer
title: 历程属性
description: 了解历程属性
feature: Journeys
role: Developer
level: Experienced
keywords: 历程，表达式，编辑器，属性
exl-id: eb1ab0ed-90bd-4613-b63d-b28693947db2
version: Journey Orchestration
TQID: https://experienceleague.adobe.com/f2FVDYuWN9tawdgRdCffwnXNXoI-e-ZAuYAaozoHd3g
product_v2:
  - id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2:
  - id: d998adac-2f81-400b-a669-d07bb196e4eb
subfeature_v2:
  - id: fa683eda-48de-4558-af32-2673edcd44fe
role_v2:
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2:
  - id: aa2f3246-cb95-4b30-8899-fdf7d73550cc
source-git-commit: bf5866b0e7437f93936f573fd83ada8526fe004d
workflow-type: tm+mt
source-wordcount: 1103
ht-degree: 1%

---

# 历程属性属性 {#journey-properties}

在[简单表达式编辑器](../conditions.md#about_condition)以及[高级表达式编辑器](../expression/expressionadvanced.md)中，**Event**&#x200B;和&#x200B;**数据源**&#x200B;类别下方，您可以访问&#x200B;**历程属性**&#x200B;类别。 此类别包含与给定用户档案的历程相关的技术字段。 这是系统从实时历程中检索到的信息，例如历程ID或遇到的特定错误。

![](../assets/journey-properties.png)

它包含有关以下内容的信息：

* 历程版本：历程uid、历程版本uid、实例uid等。
* 错误：数据提取、操作执行等。
* 当前步骤、上一个当前步骤等。
* 已丢弃的配置文件

  字段列表在此部分[&#128279;](#journey-properties-fields)中可用。

您可以使用这些字段构建表达式。 在历程执行期间，直接从历程中检索值。

以下是一些用例示例：

* **记录丢弃的用户档案**：您可以将从消息中排除的所有用户档案按照上限规则发送到第三方系统以进行记录。 为此，您可以设置超时和错误时的路径，并添加条件以筛选特定错误类型，例如“通过设置规则上限来放弃人员”。 然后，您可以通过自定义操作将已丢弃的用户档案推送到第三方系统。

* **发生错误时发送警报**：每次消息发生错误时，您都可以向第三方系统发送通知。 为此，您可以设置路径以防出错，还可以添加条件和自定义操作。 例如，您可以通过Slack渠道发送包含所遇到错误说明的通知。

* **优化报表中的错误** ：您可以为每个错误类型定义条件，而不是让出错的消息只有一个路径。 这将允许您优化报告并查看所有错误类型数据。

## 字段列表 {#journey-properties-fields}

| 类别 | 字段名称 | 标签 | 描述 |
|---|---|---|------------|
| 历程版本 | journeyUID | 历程标识符 | |
| | journeyVersionUID | 历程版本标识符 | |
| | journeyVersionName | 历程版本名称 | |
| | journeyVersionDescription | 历程版本描述 | |
| | journeyVersion | 历程版本 | |
| 历程实例 | instanceUID | 历程实例标识符 | 实例的ID |
| | externalkey | 外部密钥 | 触发历程的单个标识符 |
| | organizationId | 组织标识符 | 品牌组织 |
| | sandboxName | 沙盒名称 | 沙盒的名称 |
| 身份标识 | profileId | 配置文件身份标识符 | 历程中用户档案的标识符 |
| | namespace | 配置文件身份命名空间 | 历程中配置文件的命名空间（示例：ECID） |
| 当前节点 | currentNodeId | 当前节点标识符 | 当前活动（节点）的标识符 |
| | currentNodeName | 当前节点名称 | 当前活动的名称（节点） |
| 上一个节点 | previousNodeId | 上一节点标识符 | 上一个活动（节点）的标识符 |
| | previousNodeName | 上一个节点名称 | 上一个活动的名称（节点） |
| 错误 | lastNodeUIDInError | 上一出错的节点标识符 | 出错的最新活动（节点）的标识符 |
| | lastNodeNameInError | 上一出错的节点名称 | 出错的最新活动（节点）的名称 |
| | lastNodeTypeInError | 上一出错的节点类型 | 出错的最新活动（节点）的错误类型。 可能的类型：<ul><li>事件：事件、反应、SQ（示例：受众资格）</li><li>流量控制：结束、条件、等待</li><li>操作：ACS操作、跳转、自定义操作</li></ul> |
| | lastErrorcode | 上一错误代码 | 最新活动（节点）的错误代码出错。 可能的错误： <ul><li>HTTP错误代码</li><li>上限</li><li>timedout</li><li>错误(示例：发生意外错误时的默认值。 不应该/极少数发生)</li></ul> |
| | lastExecutedActionErrorCode | 上次执行的操作产生的错误代码 | 最新出错操作的错误代码 |
| | lastDataFetchErrorCode | 上次数据获取产生的错误代码 | 从数据源获取最新数据的错误代码 |
| 时间 | lastActionExecutionElapsedTime | 执行上一个操作占用的时间 | 执行最新操作所花费的时间 |
| | lastDataFetchElapsedTime | 上次获取数据占用的时间 | 执行从数据源获取的最新数据所花费的时间 |

+++ AI知识参考

本节包含结构化知识，用于支持与本主题相关的解释、检索和问答。

要全面了解相关信息，应将此信息与本页上的文档相结合。 这两个源都不是独立的；页面描述了功能，而本节提供了其他上下文来帮助消除术语、意图、适用性和约束条件的歧义。

* **TL；DR：**&#x200B;本页介绍了表达式编辑器中的“历程属性”类别 — 这是一组关于实时Journey实例的技术字段（ID、错误、当前/以前的节点、运行时间），可用于构建用于日志记录、警报和特定于错误的报表的表达式。

**意图：**

* 在简单或高级表达式编辑器中访问历程属性字段以引用实时历程元数据
* 构建一个条件，用于按错误类型筛选已放弃的用户档案，以将其路由到第三方日志记录系统
* 通过引用自定义操作中的最后一个错误代码和节点名称，将错误警报发送到外部渠道（例如Slack）
* 通过使用`lastNodeTypeInError`和`lastErrorCode`为每个错误类型创建单独的条件路径来优化历程错误报告
* 在用于跟踪和审核的表达式中引用历程版本标识符、实例标识符和沙盒名称

**术语表：**

* **历程属性**：表达式编辑器中的类别，包含当前历程执行实例&#x200B;*（产品特定）*&#x200B;的技术元数据字段
* **instanceUID**：给定配置文件执行&#x200B;*（产品特定）*&#x200B;的历程实例的唯一标识符
* **lastErrorCode**：历程中最近失败活动的错误代码；可能的值包括HTTP代码、`capped`、`timedOut`和`error` *（产品特定）*
* **lastNodeTypeInError**：遇到错误的最后一个活动的类型；可以是事件、流程控制或操作&#x200B;*（产品特定）*
* **externalKey**：触发历程实例&#x200B;*（产品特定）*&#x200B;的单个标识符（例如配置文件ID）

**护栏：**

* 历程属性字段值在执行时直接从实时历程中检索 — 它们不可用于执行前验证
* `lastErrorCode`字段使用预定义的值： HTTP错误代码、`capped`、`timedOut`和`error`
* 历程属性在简单表达式编辑器和高级表达式编辑器中均可用，位于历程属性类别下

**术语：**

* 规范名称：历程属性 — 首字母缩略词：none — 变体：旅程技术字段，旅程元数据字段
* 同义词：“历程属性”=“历程技术字段”；“instanceUID”=“历程实例标识符”
* 请勿混淆： journeyUID（标识历程定义）≠instanceUID（标识特定用户档案的历程执行）

**常见问题解答：**

* **问：在表达式编辑器中，可在何处找到历程属性字段？**  — 它们显示在简单表达式编辑器和高级表达式编辑器中的“历程属性”类别下，位于“事件”和“数据源”下。
* **问：如何记录上限规则丢弃的配置文件？**  — 在`lastErrorCode == "capped"`上添加错误路径条件筛选，并通过自定义操作将这些配置文件推送到第三方系统。
* **问：`journeyUID`与`instanceUID`之间有何区别？** — `journeyUID`标识历程定义；`instanceUID`标识给定配置文件的特定执行实例。
* **问：系统意外错误返回了什么错误代码？** — `error`代码，该代码用作意外错误的默认值，应当很少发生。
* **问：我能否使用“历程属性”字段在操作失败时发送Slack警报？**  — 是；在自定义操作中引用`lastNodeNameInError`和`lastErrorCode`以在Slack通知中包含错误详细信息。

+++
