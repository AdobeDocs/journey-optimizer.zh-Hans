---
solution: Journey Optimizer
product: journey optimizer
title: 对Journey Optimizer资源执行审核操作
description: 了解如何跟踪在Journey Optimizer资源上执行的操作。
feature: Monitoring
role: User
level: Intermediate
exl-id: 759b014a-c834-4331-bffd-5bc159ec555d
source-git-commit: 63c52f04da9fd1a5fafc36ffb5079380229f885e
workflow-type: tm+mt
source-wordcount: '289'
ht-degree: 0%

---

# 对Journey Optimizer资源执行审核操作 {#track-changes}

## 关于审核日志 {#audit-logs}

通过Journey Optimizer，您可以识别系统中的用户对各种服务和功能（如历程、消息、登陆页面等）执行的操作。

这样，您就可以提高系统中所执行活动的可见性、对问题进行故障诊断，并帮助您的企业遵守法规和公司数据管理政策。

每项操作均会在“审核日志”中记录元数据，该日志可在Adobe Experience Platform中访问。 有关审核日志（包括如何在UI或API中查看和管理这些日志）的更多信息，请参阅 [Adobe Experience Platform文档](https://experienceleague.adobe.com/docs/experience-platform/landing/governance-privacy-security/audit-logs/overview.html).

![](assets/audit-logs.png)

## 由审核日志捕获的事件类型 {#events}

下表概述了审核日志记录哪些Journey Optimizer资源的操作。

>[!NOTE]
>
>在审核日志中捕获的操作的完整列表可在 [Adobe Experience Platform文档](https://experienceleague.adobe.com/docs/experience-platform/landing/governance-privacy-security/audit-logs/overview.html#category).

| 资源 | 操作 |
|-----------|------------------|
| AJO营销活动 | 创建/删除/更新/激活/停止 |
| AJO渠道常规设置 | 创建/删除/更新 |
| AJO IP池 | 创建/删除/更新 |
| AJO登陆页面 | 创建/删除/更新/发布/取消发布 |
| AJO登陆页面HTML模板 | 创建/删除/更新 |
| AJO登陆页面预设 | 创建/删除/更新 |
| AJO登陆页面子域 | 创建/删除/更新 |
| AJO消息 | 创建/删除/更新/发布 |
| AJO消息预设 | 创建/删除/更新 |
| AJO PTR记录 | 创建/删除/更新 |
| AJO保存的表达式模板 | 创建/删除/更新 |
| AJO SMS API凭据 | 创建/删除/更新 |
| AJO子域 | 创建/删除/更新 |
| AJO禁止列表 | 创建/删除/下载CSV |
| 字段组 | 创建/删除/更新 |
| 历程 | 创建/删除/更新/停止/发布 |
| 历程自定义操作 | 创建/删除/更新 |
| 历程数据源 | 创建/删除/更新 |
| 历程事件 | 创建/删除/更新 |
| 消息频率规则 | 创建/删除/更新 |
| 排名策略 | 创建/删除/更新 |
