---
solution: Journey Optimizer
product: journey optimizer
title: 角色和责任
description: 了解 Adobe Journey Optimizer 中涉及的不同角色及其职责
feature: Get Started
role: Admin, Developer, User
level: Beginner
exl-id: 71ab7369-fd84-46eb-95d2-941bd887d565
redpen-status: PASS_||_2025-04-28_15-13-07
source-git-commit: 5ff7987c00afda3263cb97654967c5b698f726c2
workflow-type: tm+mt
source-wordcount: '1177'
ht-degree: 20%

---


# 角色和责任

Adobe Journey Optimizer使品牌厂商能够在整个客户生命周期中提供互联、情境化的客户历程。 它能让团队大规模实现个性化互动，并使客户期望与业务目标保持一致。本文档介绍了高效利用 Journey Optimizer 时所涉及的关键角色及其对应职责，并提供了快速入门指南。

**重要说明：** Adobe Journey Optimizer 为不同角色设定了明确的职责。根据组织架构的不同，可由单人兼任多个或全部角色。

## 基于角色的快速入门指南

为简化实施过程，Adobe Journey Optimizer会根据专业知识将任务整理到特定的职位中。 每个角色专注于提供无缝客户体验所需的基本任务。

| 角色 | 主要职责 | 关键技能 | 典型任务 |
|-------------------|----------------------------------|--------------------------------|-----------------------------------------------|
| **管理员** | 环境设置和访问管理 | 系统配置、用户管理、安全性 | 配置沙盒、管理权限、设置渠道配置 |
| **数据工程师** | 数据基础和体系结构 | 数据建模、 XDM架构、数据质量 | 创建架构和数据集，配置数据摄取，管理数据生命周期 |
| **开发人员** | 技术实施和集成 | 移动/Web SDK、API、事件驱动型架构 | 集成SDK、实施事件、构建自定义操作端点 |
| **营销人员** | 客户体验设计和执行 | 历程设计、内容创建、数据分析 | 构建历程、创建个性化内容、优化活动 |

每个角色负责解决Adobe Journey Optimizer实施的特定阶段问题，并确保结构化和高效的部署过程。

## 实施顺序与角色依赖关系

成功的 Journey Optimizer 实施通常遵循以下顺序，该顺序体现了角色之间的依赖关系：

1. **管理员**：配置环境\
   管理员通过配置沙箱、设置访问控制以及准备渠道配置来奠定基础。 必须先实现此目标，才能使其他团队正常工作。
   * 配置开发、暂存和生产沙箱
   * 设置角色、权限和对象级访问控制(OLAC)
   * 配置渠道配置（电子邮件、短信、推送、应用程序内、Web、内容卡片）
   * 委派子域并设置IP池
   * 配置禁止列表和同意策略

2. **数据工程师**：创建数据基础\
   数据工程师构建支持个性化的数据基础架构，定义客户数据如何进入和通过系统。
   * 创建用于客户识别的身份命名空间
   * 设计XDM架构（用户档案、体验事件、关系）
   * 设置数据集并为实时客户资料启用它们
   * 配置数据摄取（批量处理和流式处理）
   * 为复杂计算创建计算属性
   * 为历程配置事件和数据源

3. **开发人员**：实现技术集成\
   开发人员通过集成SDK、发送事件和构建API端点，将应用程序连接到Journey Optimizer。 这些实施使历程能够触发和执行。
   * 将Mobile SDK (iOS/Android)与推送通知设置相集成
   * 为Web体验实施Web SDK
   * 从应用程序发送事件以触发历程
   * 为外部系统集成构建自定义操作端点
   * 使用Adobe Experience Platform Assurance测试实施

4. **营销人员**：设计和执行客户体验\
   营销人员利用所有基础工作来构建历程、创建内容并优化所有渠道的客户体验。
   * 使用分段、CSV上传或受众构成构建受众
   * 使用AI助手和模板设计个性化内容
   * 使用事件和受众触发器创建多渠道历程
   * 在启动之前使用审批工作流进行测试
   * 监控性能并根据报表见解进行优化

**注意：**&#x200B;虽然这是常规的顺序，但可以并行开展某些活动。例如，开发人员可以在数据工程师配置架构期间处理应用程序集成。

## 角色快速入门

在开始阶段，每个角色都要执行根据其职责重心定制的具体任务。完成这些初始步骤可确保更顺利地加入并与整体实施流程保持一致：

### 面向营销人员 {#for-marketers}

专注于跨所有渠道创建个性化的客户体验。

**您将使用的关键功能：**

* 使用多种方法（区段定义、CSV上传、受众构成）创建受众和构建区段
* 使用AI助手设计内容，用于文本和图像生成
* 使用拖放设计器构建多渠道客户历程
* 利用发送时间优化和冲突管理最大限度地提高参与度
* 在发布之前测试内容并使用审批工作流
* 使用集成的报告功能板监控性能

**开始于：**&#x200B;使用预建模板创建一个简单的欢迎历程或放弃的购物车恢复营销活动。

[营销人员入→](path/marketer.md)

### 面向数据工程师 {#for-data-engineers}

建立支持个性化体验的数据基础。

**主要职责：**

* 创建身份命名空间并配置身份解析
* 为配置文件和事件数据（标准和关系）设计XDM架构
* 设置数据集并为实时客户资料启用它们
* 为批量摄取和流式摄取数据配置源连接器
* 创建计算属性以简化分段
* 配置历程执行的事件和数据源
* 管理数据质量、治理和生命周期

**开始于：**&#x200B;设置身份命名空间并使用必填字段组创建您的第一个配置文件架构。

[数据工程师入门→](path/data-engineer.md)

### 适用于管理员 {#for-administrators}

为您的组织设置和管理Journey Optimizer环境。

**主要职责：**

* 创建和管理用于开发、测试和生产的沙箱
* 使用现成或自定义角色配置角色和权限
* 应用对象级访问控制(OLAC)来保护资源
* 设置电子邮件、短信、推送、应用程序内、Web和内容卡的渠道配置
* 委派子域并创建用于电子邮件可投放性的IP池
* 管理禁止列表和允许列表
* 配置同意策略和数据治理（使用Healthcare/Privacy Shield）

**开始于：**&#x200B;配置沙盒，设置基本角色和权限，然后与您的团队合作进行渠道配置。

[管理员→入门](path/administrator.md)

### 面向开发人员 {#for-developers}

实施技术集成，将Journey Optimizer连接到您的应用程序。

**主要职责：**

* 集成Adobe Experience Platform Mobile SDK (iOS/Android)
* 为Web体验和Web推送通知实施Web SDK
* 配置推送通知凭据和证书
* 从应用程序发送事件以触发历程
* 生成Journey Optimizer通过自定义操作调用的API端点
* 为Web、移动设备和其他表面实施基于代码的体验
* 使用Adobe Experience Platform Assurance测试和调试实现
* 使用Journey Optimizer API进行编程访问

**开始于：**&#x200B;集成Mobile或Web SDK，然后实施您的第一个事件以触发历程。

[开发人员入门→](path/developer.md)

## 跨角色Collaboration

成功的Journey Optimizer实施需要跨所有角色进行协作：

* **管理员**&#x200B;通过设置沙盒、权限和渠道配置来启用其他角色
* **数据工程师**&#x200B;提供开发人员和营销人员基于的数据基础
* **开发人员**&#x200B;实施营销人员用于触发历程的技术集成
* **营销人员**&#x200B;就数据质量、功能请求和用户体验向所有团队提供反馈

**最佳实践：**&#x200B;定期举行跨职能会议，以调整优先级、共享进度并解决跨团队的阻止程序问题。

## 操作说明视频 {#video}

要了解有关 Journey Optimizer 的关键功能和用户画像的更多信息，请观看说明视频。该视频对用户界面进行了详细介绍，并重点说明以特定于角色的工作流为基础的主要功能。

>[!VIDEO](https://video.tv.adobe.com/v/3424995?quality=12)

## 其他资源

要获取更深入的知识和更新，请浏览以下资源：

**学习与文档：**

* [教程视频](https://experienceleague.adobe.com/docs/journey-optimizer-learn/tutorials/overview.html?lang=zh-Hans){target="_blank"} — 所有角色的分步视频教程
* [历程用例库](../building-journeys/jo-use-cases.md) — 实际示例和实施模式
* [AI和智能功能](ai-features.md) — 了解AI助手、发送时间优化和内容生成
* [用户界面指南](user-interface.md) — 有效地导航Journey Optimizer

**保持更新：**

* [发行说明](../rn/release-notes.md) — 最新功能、改进和修复
* [文档更新](../rn/documentation-updates.md) — 跟踪最近的文档更改
* **产品通知** — 在[Adobe Experience Cloud配置文件](https://experience.adobe.com/preferences){target="_blank"}中启用警报，以接收有关新版本、维护时段和重要公告的通知。 单击您的配置文件图标>首选项>通知以进行配置。

**社区和支持：**

* [Experience League社区](https://experienceleaguecommunities.adobe.com/t5/journey-optimizer/ct-p/journey-optimizer){target="_blank"} — 与其他用户和专家联系
* [产品论坛](https://experienceleaguecommunities.adobe.com/t5/journey-optimizer/ct-p/journey-optimizer){target="_blank"} — 提问并共享知识
