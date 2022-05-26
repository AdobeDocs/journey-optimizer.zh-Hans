---
title: 对Journey Optimizer资源的审计行动
description: 了解如何跟踪在Journey Optimizer资源上执行的操作。
feature: Monitoring
role: User
level: Intermediate
source-git-commit: 336a2a4d28ce1738cc664861291fdc1f39b3ab29
workflow-type: tm+mt
source-wordcount: '297'
ht-degree: 1%

---

# 对Journey Optimizer资源的审计行动 {#track-changes}

## 关于审核日志 {#audit-logs}

通过Journey Optimizer，您可以识别系统中的用户对各种服务和功能（如历程、消息、登陆页面等）执行的操作。

这样，您就可以提高系统中所执行活动的可见性、对问题进行故障诊断，并帮助您的企业遵守法规和公司数据管理政策。

每个操作都会在“审核日志”中记录元数据，该日志可在Adobe Experience Platform中访问。 有关审核日志（包括如何在UI或API中查看和管理这些日志）的更多信息，请参阅 [Adobe Experience Platform文档](https://experienceleague.adobe.com/docs/experience-platform/landing/governance-privacy-security/audit-logs/overview.html).

![](assets/audit-logs.png)

## 由审核日志捕获的事件类型 {#events}

下表概述了审计日志记录Journey Optimizer资源的哪些操作。

>[!NOTE]
>
>在审核日志中捕获的操作的完整列表可在 [Adobe Experience Platform文档](https://experienceleague.adobe.com/docs/experience-platform/landing/governance-privacy-security/audit-logs/overview.html#category).

| 资源 | 操作 |
|-----------|------------------|
| 字段组 | 创建/删除/更新 |
| AJO子域 | 创建/删除/更新 |
| CJM禁止列表 | 创建/删除/下载CSV |
| AJO消息预设 | 创建/删除/更新 |
| AJO PTR记录 | 创建/删除/更新 |
| 排名策略 | 创建/删除/更新 |
| 历程自定义操作 | 创建/删除/更新 |
| AJO登陆页面HTML模板 | 创建/删除/更新 |
| AJO IP池 | 创建/删除/更新 |
| AJO登陆页面子域 | 创建/删除/更新 |
| AJO SMS API凭据 | 创建/删除/更新 |
| AJO登陆页面预设 | 创建/删除/更新 |
| 历程数据源 | 创建/删除/更新 |
| 历程事件 | 创建/删除/更新 |
| AJO保存的表达式模板 | 创建/删除/更新 |
| 消息频率规则 | 创建/删除/更新 |
| AJO登陆页面 | 创建/删除/更新/发布/取消发布 |
| 历程 | 创建/删除/更新/停止/发布 |
| AJO消息 | 创建/删除/更新/发布 |
| AJO渠道常规设置 | 创建/删除/更新 |
