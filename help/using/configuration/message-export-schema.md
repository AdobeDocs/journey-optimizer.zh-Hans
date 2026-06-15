---
solution: Journey Optimizer
product: journey optimizer
title: AJO消息导出架构
description: 了解AJO消息导出数据集中可用的字段
feature: Channel Configuration
topic: Administration
role: Admin
level: Experienced
keywords: 导出，消息，数据集，架构，电子邮件，短信
feature_v2: []
subfeature_v2: id: cf64c7f6-7428-4ae5-b158-8df9771f38f4
source-git-commit: 0d9c480cc48c4352e82d1f4624c65fc16a60b959
workflow-type: tm+mt
source-wordcount: 447
ht-degree: 3%

---

# AJO消息导出架构 {#ajo-message-export-schema}

>[!BEGINSHADEBOX]

**在此页面上：**&#x200B;浏览AJO消息导出数据集的结构和各个字段，该数据集在Adobe Experience Platform中存储已发送的电子邮件和短信消息内容。

>[!ENDSHADEBOX]

在电子邮件或短信渠道配置上启用&#x200B;**消息导出**&#x200B;后，已发送的消息内容将写入[!DNL Adobe Experience Platform]中的&#x200B;**AJO消息导出数据集**。

此部分列出了导出数据集中的可用字段。

## 数据集字段

+++ 体验(_E)

**字段：** `_experience`\
**类型：**&#x200B;对象

+++

+++ _experience > customerJourneyManagement

**字段：** `customerJourneyManagement`\
**类型：**&#x200B;对象

+++

+++ _experience > customerJourneyManagement > messageDeliveryMetadata

**字段：** `messageDeliveryMetadata`\
**类型：**&#x200B;对象

+++

+++ _experience > customerJourneyManagement > messageDeliveryMetadata > emailMetadata

**字段：** `emailMetadata`\
**类型：**&#x200B;对象

* 收件人

  **字段：** `recipient`\
  **类型：**&#x200B;对象

   * bcc

     **字段：** `bcc`\
     **类型：**&#x200B;字符串数组

   * 抄送

     **字段：** `cc`\
     **类型：**&#x200B;字符串数组

   * 电子邮件

     **字段：** `email`\
     **类型：**&#x200B;字符串

   * name

     **字段：** `name`\
     **类型：**&#x200B;字符串

* 发件人

  **字段：** `sender`\
  **类型：**&#x200B;对象

   * 电子邮件

     **字段：** `email`\
     **类型：**&#x200B;字符串

   * errorEmail

     **字段：** `errorEmail`\
     **类型：**&#x200B;字符串

   * name

     **字段：** `name`\
     **类型：**&#x200B;字符串

   * replyToEmail

     **字段：** `replyToEmail`\
     **类型：**&#x200B;字符串

   * replyToName

     **字段：** `replyToName`\
     **类型：**&#x200B;字符串

+++

+++ _experience > customerJourneyManagement > messageDeliveryMetadata > smsMetadata

**字段：** `smsMetadata`\
**类型：**&#x200B;对象

* 收件人

  **字段：** `recipient`\
  **类型：**&#x200B;对象

   * 数字

     **字段：** `number`\
     **类型：**&#x200B;字符串

* 发件人

  **字段：** `sender`\
  **类型：**&#x200B;对象

   * 数字

     **字段：** `numbers`\
     **类型：**&#x200B;字符串数组

+++

+++ _experience > customerJourneyManagement > messageExecution

**字段：** `messageExecution`\
**类型：**&#x200B;对象

* 受众

  **字段：** `audience`\
  **类型：**&#x200B;对象

   * ID

     **字段：** `id`\
     **类型：**&#x200B;字符串

   * 类型

     **字段：** `type`\
     **类型：**&#x200B;字符串

* fragmentPublicationIDs

  **字段：** `fragmentPublicationIDs`\
  **类型：**&#x200B;字符串数组

* 元数据

  **字段：** `metadata`\
  **类型：**&#x200B;映射

   * [映射键]

     **类型：**&#x200B;字符串

* parentSourceMeta

  **字段：** `parentSourceMeta`\
  **类型：**&#x200B;对象

   * sourceActionId

     **字段：** `sourceActionID`\
     **类型：**&#x200B;字符串

   * sourceID

     **字段：** `sourceID`\
     **类型：**&#x200B;字符串

   * 源类型

     **字段：** `sourceType`\
     **类型：**&#x200B;字符串

   * 源版本ID

     **字段：** `sourceVersionID`\
     **类型：**&#x200B;字符串

* batchinstanceid

  **字段：** `batchInstanceID`\
  **类型：**&#x200B;字符串

* campaignActionID

  **字段：** `campaignActionID`\
  **类型：**&#x200B;字符串

* campaignID

  **字段：** `campaignID`\
  **类型：**&#x200B;字符串

* campaignVersionID

  **字段：** `campaignVersionID`\
  **类型：**&#x200B;字符串

* journeyActionId

  **字段：** `journeyActionID`\
  **类型：**&#x200B;字符串

* journeyVersionID

  **字段：** `journeyVersionID`\
  **类型：**&#x200B;字符串

* journeyVersionInstanceID

  **字段：** `journeyVersionInstanceID`\
  **类型：**&#x200B;字符串

* journeyVersionNodeID

  **字段：** `journeyVersionNodeID`\
  **类型：**&#x200B;字符串

* messageExecutionID

  **字段：** `messageExecutionID`\
  **类型：**&#x200B;字符串

* 消息ID

  **字段：** `messageID`\
  **类型：**&#x200B;字符串

* messagePublicationID

  **字段：** `messagePublicationID`\
  **类型：**&#x200B;字符串

* messageType

  **字段：** `messageType`\
  **类型：**&#x200B;字符串

* waveID

  **字段：** `waveID`\
  **类型：**&#x200B;字符串

+++

+++ _experience > customerJourneyManagement > messageProfile

**字段：** `messageProfile`\
**类型：**&#x200B;对象

* 渠道

  **字段：** `channel`\
  **类型：**&#x200B;对象

   * contentType

     **字段：** `contentTypes`\
     **类型：**&#x200B;字符串数组

   * 位置类型

     **字段：** `locationTypes`\
     **类型：**&#x200B;字符串数组

   * metricType

     **字段：** `metricTypes`\
     **类型：**&#x200B;字符串数组

   * _id

     **字段：** `_id`\
     **类型：**&#x200B;字符串

   * _type

     **字段：** `_type`\
     **类型：**&#x200B;字符串

   * mediaAction

     **字段：** `mediaAction`\
     **类型：**&#x200B;字符串

   * mediaType

     **字段：** `mediaType`\
     **类型：**&#x200B;字符串

   * 模式

     **字段：** `mode`\
     **类型：**&#x200B;字符串

   * referringSource

     **字段：** `referringSource`\
     **类型：**&#x200B;字符串

   * typeAtSource

     **字段：** `typeAtSource`\
     **类型：**&#x200B;字符串

* isSendTimeOptimized

  **字段：** `isSendTimeOptimized`\
  **类型：**&#x200B;布尔值

* isTestExecution

  **字段：** `isTestExecution`\
  **类型：**&#x200B;布尔值

* messageProfileID

  **字段：** `messageProfileID`\
  **类型：**&#x200B;字符串

* messageProfileTrackingID

  **字段：** `messageProfileTrackingID`\
  **类型：**&#x200B;字符串

* requestID

  **字段：** `requestID`\
  **类型：**&#x200B;字符串

* secondaryDimensionID

  **字段：** `secondaryDimensionID`\
  **类型：**&#x200B;字符串

* secondaryDimensionName

  **字段：** `secondaryDimensionName`\
  **类型：**&#x200B;字符串

* 变量

  **字段：** `variant`\
  **类型：**&#x200B;字符串

+++

+++ _experience > customerJourneyManagement > messageRenderedContent

**字段：** `messageRenderedContent`\
**类型：**&#x200B;对象

* 电子邮件内容

  **字段：** `emailContent`\
  **类型：**&#x200B;对象

   * html

     **字段：** `html`\
     **类型：**&#x200B;字符串

   * 主题

     **字段：** `subject`\
     **类型：**&#x200B;字符串

   * 文本

     **字段：** `text`\
     **类型：**&#x200B;字符串

* smsContent

  **字段：** `smsContent`\
  **类型：**&#x200B;对象

   * 媒体

     **字段：** `media`\
     **类型：**&#x200B;字符串

   * message

     **字段：** `message`\
     **类型：**&#x200B;字符串

   * 标题

     **字段：** `title`\
     **类型：**&#x200B;字符串

+++

+++ identityMap

**字段：** `identityMap`\
**类型：**&#x200B;映射

* [映射键]

  **类型：**&#x200B;对象数组

   * authenticatedState

     **字段：** `authenticatedState`\
     **类型：**&#x200B;字符串

   * ID

     **字段：** `id`\
     **类型：**&#x200B;字符串

   * 主要

     **字段：** `primary`\
     **类型：**&#x200B;布尔值

+++

+++ 事件类型

**字段：** `eventType`\
**类型：**&#x200B;字符串

+++

+++ productedBy

**字段：** `producedBy`\
**类型：**&#x200B;字符串

+++

+++ 时间戳

**字段：** `timestamp`\
**类型：**&#x200B;日期时间

+++

