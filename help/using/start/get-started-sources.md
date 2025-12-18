---
solution: Journey Optimizer
product: journey optimizer
title: Journey Optimizer 源连接器入门
description: 了解如何在 Adobe Journey Optimizer 中从外部源摄取数据
feature: Integrations, Data Ingestion
role: User
level: Beginner
exl-id: 359ea3c6-7746-469e-8a24-624f9726f2d8
source-git-commit: 52b58d18cdbbff79f4dcb7af2817b178a4a0b429
workflow-type: tm+mt
source-wordcount: '584'
ht-degree: 11%

---

# 源连接器入门 {#sources-gs}

## 什么是源？ {#what-is-source}

**源**&#x200B;是将外部数据引入Adobe Journey Optimizer的连接器。 通过源，您可以从已使用的系统（如CRM平台、云存储或数据库）导入客户信息，并提供这些数据用于创建个性化的客户历程。

请将源视为Journey Optimizer与外部数据系统之间的桥梁。 它们会自动同步数据，以便您始终拥有最新的客户信息来支持您的营销活动。

## 来源为何重要 {#why-sources-matter}

源对于在Journey Optimizer中创建个性化、数据驱动型客户体验至关重要。 原因如下：

* **统一客户视图** — 合并来自多个系统的数据以查看每个客户的完整信息
* **实时个性化** — 使用最新数据在您的历程中及时投放相关消息
* **自动数据同步** — 无需手动数据导入即可使客户信息保持最新
* **高效的工作流** — 连接一次，然后数据会自动流入您的历程

例如，您可以使用源从电子商务平台导入购买历史记录，然后创建根据客户已购买的内容发送个性化产品推荐的历程。

## 您可以使用源做什么 {#sources-use-cases}

Journey Optimizer中的源的常见用例包括：

* **从CRM系统导入客户数据** — 从Salesforce或Microsoft Dynamics等平台同步联系人信息、偏好设置和参与历史记录
* **连接购买数据** — 从电子商务平台引入订单历史记录和产品偏好设置以个性化优惠
* **集成忠诚度计划数据** — 访问点余额和分层信息以奖励您参与度最高的客户
* **同步行为数据** — 导入网站交互和应用程序使用模式以触发相关历程
* **更新配置文件属性** — 使客户配置文件与来自云存储或数据库的数据保持最新

## 常见源类型 {#source-types}

Journey Optimizer支持与现有系统连接的各种源类型：

**Adobe应用程序：**
* Adobe Analytics
* Adobe Audience Manager
* Adobe Campaign
* Adobe Commerce

**云存储：**
* Amazon S3
* Azure Blob Storage
* Google 云存储
* SFTP

**数据库：**
* Amazon Redshift
* Google BigQuery
* Microsoft SQL Server
* MySQL
* PostgreSQL

**CRM和营销自动化：**
* Microsoft Dynamics
* Salesforce
* Salesforce Marketing Cloud

➡️在[Experience Platform源目录](https://experienceleague.adobe.com/docs/experience-platform/sources/home.html?lang=zh-Hans#sources-catalog){target="_blank"}中查看完整列表

## 开始之前 {#prerequisites}

在配置源之前，请确保您具有：

* **适当的权限** — 在Adobe Experience Platform中管理源的访问权限
* **Source系统凭据** — 要连接的外部系统的身份验证详细信息
* **了解您的数据** — 了解您需要哪些数据字段以及它们如何映射到Journey Optimizer配置文件

➡️了解[访问控制和权限](../../administration/permissions.md)

## 源的工作方式 {#how-sources-work}

Adobe Journey Optimizer使用Adobe Experience Platform中的源框架。 以下是基本的工作流程：

1. **连接** — 设置对外部数据系统的身份验证
2. **选择数据** — 选择要导入的数据以及同步频率
3. **映射字段** — 定义外部数据字段如何与Journey Optimizer配置文件属性相对应
4. **计划** — 设置自动数据刷新间隔
5. **监视器** — 跟踪数据流并解决任何同步问题

配置完毕后，源将在后台自动运行，保持客户数据刷新并可在历程中使用。

## 了解详情 {#learn-more}

![](assets/sources-home.png)

观看以下视频，了解源连接器以及如何在Journey Optimizer中配置它们：

>[!VIDEO](https://video.tv.adobe.com/v/3422581?captions=chi_hans&quality=12)

有关配置和管理源的详细信息，请参阅[Adobe Experience Platform源文档](https://experienceleague.adobe.com/docs/experience-platform/sources/home.html?lang=zh-Hans){target="_blank"}。

## 后续步骤 {#next-steps}

现在您已经了解了什么是来源以及它们为什么重要：

* 浏览[源目录](https://experienceleague.adobe.com/docs/experience-platform/sources/home.html?lang=zh-Hans#sources-catalog){target="_blank"}以查找系统的连接器
* 了解如何[创建源连接](https://experienceleague.adobe.com/docs/experience-platform/sources/ui-tutorials/create/overview.html){target="_blank"}
* 了解[数据映射和转换](https://experienceleague.adobe.com/docs/experience-platform/sources/ui-tutorials/dataflow/overview.html){target="_blank"}
* 了解如何[在历程中使用导入的数据](../building-journeys/journey-gs.md)
