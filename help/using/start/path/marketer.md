---
solution: Journey Optimizer
product: journey optimizer
title: Journey Optimizer 营销人员快速入门
description: 作为历程实践者，了解有关如何使用 Journey Optimizer 的更多信息
level: Beginner
feature: Get Started
Role: User
exl-id: 34304142-3ee8-4081-94b9-e914968c75ba
source-git-commit: e86fa9f6e62aea9dd1f7e6d35e7cf4b20f79aaa6
workflow-type: tm+mt
source-wordcount: '1192'
ht-degree: 6%

---

# 营销人员快速入门 {#get-started-marketers}

作为&#x200B;**营销人员**&#x200B;或&#x200B;**历程实践者**，您负责创建产品建议和历程以及设计内容。[系统管理员](administrator.md)和[数据工程师](data-engineer.md)向您授予访问权限并准备好环境后，您即可开始使用 [!DNL Adobe Journey Optimizer]。

## 开始使用要点

Journey Optimizer允许您通过电子邮件、短信、推送、应用程序内、Web、内容卡等创建个性化的连接客户体验。 与您的[管理员](administrator.md)合作以获取访问权限，并与[数据工程师](data-engineer.md)合作设置受众和数据。

请按照以下核心步骤开始构建体验：

1. **创建受众**。通过区段定义构建受众、上传CSV文件或使用受众合成。 Journey Optimizer提供了多种方法来定位合适的客户。 了解有关[受众](../../audience/about-audiences.md)和[创建区段定义](../../audience/creating-a-segment-definition.md)的更多信息。

1. **设计内容**。 跨渠道创建引人注目的消息：
   * 使用&#x200B;**AI助手**&#x200B;根据您的品牌指南生成电子邮件内容、主题行和图像。 [了解AI内容生成](../../content-management/gs-generative.md)
   * 使用客户数据、动态内容和条件逻辑&#x200B;**个性化消息**。 [了解个性化](../../personalization/personalize.md)
   * **对上下文数据进行迭代**&#x200B;以显示来自事件、自定义操作和数据集查找的动态列表。 [了解如何迭代上下文数据](../../personalization/iterate-contextual-data.md)
   * 创建可重复使用的&#x200B;**内容模板**&#x200B;和&#x200B;**片段**&#x200B;以保持品牌一致性。 [使用模板](../../content-management/content-templates.md)
   * 通过&#x200B;**Adobe Experience Manager Assets**&#x200B;集成管理资源。 [了解资源](../../integrations/assets.md)

   ![](../assets/perso_ee2.png)

1. **添加优惠和决策**。 使用AI支持的决策在适当的时间为每位客户提供最佳选件。 了解[决策管理](../../offers/get-started/starting-offer-decisioning.md)和[Experience Decisioning](../../experience-decisioning/gs-experience-decisioning.md)。

   ![](../assets/offers-e2e-offers-displayed.png)

1. **测试和验证**。发送前预览和测试内容：
   * 使用&#x200B;**测试用户档案**&#x200B;预览个性化并检查跨设备渲染
   * 使用CSV/JSON文件中的示例数据&#x200B;**进行测试**
   * 在常用电子邮件客户端上预览&#x200B;**电子邮件渲染**
   * 为营销活动和历程设置&#x200B;**审批工作流**（需要额外的许可证）

   了解如何[测试和验证消息](../../content-management/preview-test.md)。

1. **构建客户历程**。 使用历程画布创建实时、个性化的体验：

   * 触发包含&#x200B;**事件** （客户操作）或&#x200B;**受众** （批次发送）的历程
   * 添加&#x200B;**条件**&#x200B;以根据客户数据创建个性化路径
   * 使用&#x200B;**等待活动**&#x200B;创建消息之间的完美计时
   * 在一个历程中跨&#x200B;**多个渠道**&#x200B;发送消息
   * 应用&#x200B;**A/B测试**&#x200B;以优化历程有效性
   * 使用&#x200B;**数据集查找**&#x200B;利用Adobe Experience Platform中的实时数据扩充历程。 [了解数据集查找](../../building-journeys/dataset-lookup.md)
   * 利用&#x200B;**补充标识符**&#x200B;允许同一配置文件输入多个历程实例（例如，不同的订单或预订）。 [了解补充标识符](../../building-journeys/supplemental-identifier.md)

   ![](../assets/journey-design.png)

   了解如何[设计和执行历程](../../building-journeys/journey-gs.md)并探索[历程用例](../../building-journeys/jo-use-cases.md)。 了解[进入/退出条件](../../building-journeys/entry-exit-criteria-guide.md)以控制配置文件流。

1. **监视和优化**。 随时间推移跟踪性能并改进结果：
   * 监视&#x200B;**实时历程**&#x200B;性能并识别瓶颈
   * 分析&#x200B;**消息投放**&#x200B;率和参与量度
   * 将&#x200B;**报告功能板**&#x200B;与Customer Journey Analytics集成一起使用
   * 跟踪&#x200B;**转化**&#x200B;和业务影响

   了解如何[监视性能](../../reports/report-gs-cja.md)。

## 利用最新功能

Journey Optimizer不断推出新功能，以增强您的营销效果：

* **内容卡**：在移动应用和网站中传递用户方便时可与之交互的永久性、非侵入性消息。 与推送通知不同，内容卡保持可见状态，直到被取消。 [了解内容卡片](../../content-card/create-content-card.md)

* **冲突管理和优先化**：使用高级上限规则控制消息频率并防止过度通信。 设置优先级得分以确保最重要的消息首先到达客户。 [了解冲突管理](../../conflict-prioritization/gs-conflict-prioritization.md)

* **AI支持的发送时间优化**：让AI根据每个客户的历史参与模式预测其最佳发送时间，使打开率和点击率最多增加10%。 [了解发送时间优化](../../building-journeys/send-time-optimization.md)

* **多臂老虎机试验**：在测试时自动为实时获胜变体分配更多流量，从而最大化结果，而无需等待测试完成。 [了解试验](../../content-management/content-experiment.md)

* **审批工作流**：在营销活动和历程上线之前实施其审核流程（附带附加许可证）。 [了解审批](../../test-approve/gs-approval.md)

## 获得成功的最佳实践

### 内容创建

* **从模板开始**：使用预建模板和内容片段加快创建并维护一致性
* **提前测试，经常测试**：始终跨设备预览内容并使用测试配置文件验证个性化
* **明智地利用AI**：将AI助手用于初始草稿和变体，但始终针对您的品牌声音进行审查和优化
* **保持简单**：具有强大行动号召的简明清晰邮件比复杂布局表现更好

### 历程设计

* **定义明确的目标**：在构建历程之前建立成功量度
* **映射客户体验**：在实施之前可视化整个历程
* **策略性地使用等待活动**：在发送跟进信息之前给客户时间进行参与
* **规划退出策略**：定义客户应退出历程的时间和原因
* **在草稿模式下测试**：在激活之前通过试运行验证历程逻辑

[了解历程最佳实践](../../building-journeys/entry-exit-criteria-guide.md#best-practices)

### 受众定位

* **仔细细分**：根据明确的条件创建特定的、可操作的受众区段
* **定期刷新**：通过设置适当的评估计划，确保受众保持最新
* **平衡大小和精度**：目标受众足够大，具有足够的统计意义，但足够具体，具有相关性
* **使用扩充属性**：利用计算属性和扩充数据实现更深入的个性化

### 频率管理

* **尊重客户首选项**：尊重选择退出和通信首选项
* **设置频率上限**：使用规则集防止跨渠道的消息疲劳
* **协调营销活动**：使用冲突管理以确保客户在正确的时间收到正确的消息
* **监测参与度**：观察疲劳迹象（打开率下降，取消订阅次数增加）

[了解频率封顶](../../conflict-prioritization/channel-capping.md)

## 探索用例

从演示Journey Optimizer功能的实际示例中学习：

**常见用例：**

* **欢迎系列**：通过个性化的多步骤历程载入新客户。 [查看用例](https://experienceleague.adobe.com/zh-hans/docs/journey-optimizer-learn/tutorials/use-cases/customer-onboarding)
* **放弃的购物车恢复**：重新吸引将商品留在购物车中的客户。 [查看用例](https://experienceleague.adobe.com/zh-hans/docs/journey-optimizer-learn/tutorials/use-cases/abandoned-cart)
* **重新参与营销活动**：通过有针对性的优惠赢回不活跃的客户。 [查看用例](https://experienceleague.adobe.com/zh-hans/docs/experience-platform/rtcdp/use-cases/personalization-insights-engagement/use-cases-luma)
* **生日营销活动**：发送包含特殊优惠的个性化生日消息
* **产品推荐**：根据浏览和购买历史记录推荐相关产品
* **事件驱动消息传递**：实时响应客户操作

**历程模式：**

* [向订阅者发送邮件](../../building-journeys/message-to-subscribers-uc.md)：具有个性化内容的Target订阅列表
* [多渠道消息传递](../../building-journeys/journeys-uc.md)：将电子邮件和推送与反应事件相结合
* [仅限工作日的电子邮件](../../building-journeys/weekday-email-uc.md)：使用基于时间的条件安排通信

浏览完整的[历程用例库](../../building-journeys/jo-use-cases.md)以了解更多模式和实施。

## 与其他角色协作

您的营销工作与其他团队相关联：

* **与[数据工程师合作](data-engineer.md)**：请求新的计算属性，提供有关受众质量的反馈，并协调数据要求
* **与[开发人员合作](developer.md)**：调整事件触发器、测试移动实施并验证跟踪
* **与[管理员](administrator.md)**&#x200B;合作：请求渠道配置、报告权限问题并协调新功能启用

## 保持最新

了解最新的Journey Optimizer功能和营销特性：

* **[发行说明](../../rn/release-notes.md)**：查看每月发布的新功能、渠道更新和增强功能
* **[文档更新](../../rn/documentation-updates.md)**：跟踪最近的更改，包括新用例、最佳实践和功能文档
* **产品通知**：在[Adobe Experience Cloud配置文件](https://experience.adobe.com/preferences){target="_blank"}中启用通知，以接收有关以下内容的提醒：
   * 您可用的新渠道和功能
   * 即将推出的功能和Beta版计划
   * 最佳实践和培训机会
   * 影响营销活动的重要公告

  要启用通知，请单击Adobe Experience Cloud右上角的配置文件图标，转到&#x200B;**首选项>通知**，然后配置您的Journey Optimizer通知首选项。

## 后续步骤

1. **从小处开始**：创建简单的欢迎历程或单消息营销活动以了解平台
2. **利用AI**：使用AI助手提问并加快内容创建
3. **加入社区**：与[Journey Optimizer社区中的其他Experience League用户建立联系](https://experienceleaguecommunities.adobe.com/t5/journey-optimizer/ct-p/journey-optimizer){target="_blank"}
4. **浏览教程**：观看[Experience League](https://experienceleague.adobe.com/docs/journey-optimizer-learn/tutorials/overview.html?lang=zh-Hans){target="_blank"}上的分步视频
