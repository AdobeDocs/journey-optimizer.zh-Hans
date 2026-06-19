---
solution: Journey Optimizer
product: journey optimizer
title: 载入项目指南 |Adobe Journey Optimizer
description: 跨管理员、数据、开发人员和营销人员角色规划和管理Adobe Journey Optimizer入门项目。
feature: Get Started
topic: Content Management
role: Admin
level: Intermediate
keywords: journey optimizer，入门，载入项目，推出，实施计划，管理员， csm，实施合作伙伴，分阶段清单
source-git-commit: 6a653e1dbb00f68ff689ea3e0dc0b15abda1e21e
workflow-type: tm+mt
source-wordcount: '428'
ht-degree: 4%

---

# 载入项目指南 {#onboarding-hub}

>[!BEGINSHADEBOX]

**在此页面上：**&#x200B;计划和协调完整的Adobe Journey Optimizer推出，其中包含一个跨管理员、数据工程师、开发人员和营销人员角色的分阶段核对清单。

>[!ENDSHADEBOX]

本页面向负责协调完整Journey Optimizer推出的&#x200B;**系统管理员和实施合作伙伴**。 它提供涵盖所有角色的分阶段核对清单，以及指向特定于角色的详细指南的链接。

>[!NOTE]
>
>如果您是个人特定角色快速入门，请转到[开始使用Journey Optimizer](../../rp_landing_pages/get-started-landing-page.md)。

## 阶段1 — 环境设置（管理员） {#phase-1}

请先完成这些基本任务，以便其他角色可以开始工作：

* [ ]配置沙盒（开发、暂存、生产）
* [ ]在Adobe Admin Console中配置用户角色和权限
* [ ]设置产品配置文件和对象级访问控制
* [ ]委派子域并配置IP池
* [ ]配置渠道配置（电子邮件、短信、推送、Web、应用程序内、直邮）
* [ ]设置禁止列表和同意策略

➡️查看完整的详细信息：[管理员入门](path/administrator.md)

## 第2阶段 — 数据基础（数据工程师） {#phase-2}

构建支持用户档案、受众和历程触发器的数据层：

* [ ]定义身份命名空间
* [ ]创建XDM架构（配置文件、体验事件、关系）
* [ ]为实时客户个人资料设置和启用数据集
* [ ]配置数据摄取（批次和流式传输）
* [ ]创建计算属性
* [ ]配置历程事件和数据源

➡️查看完整的详细信息：[数据工程师入门](path/data-engineer.md)

## 阶段3 — 技术集成（开发人员） {#phase-3}

连接您的应用程序，以便历程能够在实时数据上运行：

* [ ]将Mobile SDK (iOS/Android)与推送设置集成
* [ ]为Web体验和Web推送实施Web SDK
* [ ]实现从应用程序发送事件
* [ ]为外部系统集成生成自定义操作端点
* [ 使用Adobe Experience Platform Assurance进行]验证

➡️查看完整的详细信息：[开发人员入门](path/developer.md)

## 阶段4 — 第一个体验（营销人员） {#phase-4}

通过启动您的第一个历程和营销活动，奠定良好的基础：

* [ ]生成第一个受众（区段定义或CSV上传）
* [ ]通过电子邮件操作创建测试历程
* [ ]设置内容模板和片段
* [ ]发布和监测营销活动
* [ ]查看实时报告

➡️查看完整的详细信息：[营销人员快速入门](path/marketer.md)

## 入门核对清单（可打印） {#checklist}

| 阶段 | 所有者 | 状态 |
|-------|-------|--------|
| 环境设置 | 管理员 | |
| 数据基础 | 数据工程师 | |
| 技术集成 | Developer | |
| 首次体验 | 营销人员 | |

## 相关资源 {#related-resources}

* [角色和职责](quick-start.md) — 这四个角色如何协作以及推荐的实施顺序。
* [Journey Optimizer教程](https://experienceleague.adobe.com/zh-hans/docs/journey-optimizer-learn/tutorials/overview){target="_blank"} — 每个角色的分步视频和引导式演练。
* [数据管理入门](../data/gs-data.md) — 如何摄取、统一和激活数据。
