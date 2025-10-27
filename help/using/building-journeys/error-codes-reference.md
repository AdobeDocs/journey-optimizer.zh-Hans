---
solution: Journey Optimizer
product: journey optimizer
title: 错误代码引用
description: 了解Adobe Journey Optimizer中的常见错误代码以及如何对其进行故障排除
feature: Journeys, Monitoring
topic: Content Management
role: User
level: Intermediate
keywords: 错误，代码，故障排除，历程，营销活动，消息
source-git-commit: d9d0ca98d5f86a32653c9cb73197873cb31a2c6f
workflow-type: tm+mt
source-wordcount: '1532'
ht-degree: 1%

---


# 错误代码引用 {#error-codes}

Adobe Journey Optimizer使用标准化的错误代码，帮助您快速识别并解决历程、营销活动和消息配置中的问题。 了解这些错误代码可以显着减少故障排除时间，并帮助您保持最佳营销活动性能。

## 了解错误代码结构 {#error-code-structure}

Adobe Journey Optimizer错误代码遵循一致的命名模式，这有助于识别组件和问题类型：

* **服务前缀**：指示哪个Adobe Journey Optimizer服务生成了错误(例如，推送/传输服务的CJMPTS、历程运行时的CJMRT、消息创作服务的CJMMAS)
* **错误号**：特定错误条件的唯一标识符
* **HTTP状态代码**：标准HTTP状态代码（例如，400、403、422、500）

示例： `CJMRT-030012-422`表示错误号为030012且HTTP状态为422（无法处理的实体）的历程运行时错误(CJMRT)。

## 在何处查找错误代码 {#find-error-codes}

错误代码显示在Adobe Journey Optimizer的多个位置：

* 历程执行报告和日志
* Campaign激活屏幕
* 消息验证警告
* 系统通知和警报
* API响应（使用REST API时）

发生错误时，请注意完整的错误代码以及随附的任何请求ID，因为这对于故障排除和支持升级至关重要。

## 按服务划分的常见错误代码 {#error-codes-by-service}

### CJMPTS：推送和传输服务错误 {#cjmpts-errors}

这些错误发生在推送通知投放和消息传输操作期间。

| 错误代码 | 描述 | 根本原因 | 解决方法 |
|------------|-------------|-----------|-----------|
| **CJMPTS-1510-500** | 推送渠道发送时出现内部服务器错误 | 后端推送/传输故障；提供商或基础设施错误 | 1.检查通道设置设置<br/>2。 验证推送凭据是否有效<br/>3。 请重试操作<br/>4。 如果是永久性的，请使用请求ID <br/><br/>**相关文档**&#x200B;联系Adobe支持： [推送配置](../push/push-configuration.md) |
| **CJMPTS-1023-500** | 推送发送/处理期间出现内部服务器错误（第三方网关） | 临时云功能故障或未知的服务错误 | 1.验证提供程序/通道配置<br/>2。 检查第三方网关状态<br/>3。 请在几分钟后重试<br/>4。 查看日志以获取其他上下文&#x200B;<br/><br/>**相关文档**： [推送通知](../push/create-push.md) |
| **CJMPTS-1310-500** | 渲染服务（预览或实时发送）中的内部错误 | 下游模板呈现器失败，通常是由于JSON/模板语法问题 | 1.验证模板语法和结构<br/>2。 检查所有个性化变量是否有效<br/>3。 使用测试有效负载识别问题<br/>4。 如果需要，简化模板复杂度&#x200B;<br/><br/>**相关文档**： [消息模板](../content-management/content-templates.md)，[Personalization语法](../personalization/personalization-syntax.md) |

### CJMRT：历程运行时和API错误 {#cjmrt-errors}

这些错误发生在历程执行、事件处理和API操作期间。

| 错误代码 | 描述 | 根本原因 | 解决方法 |
|------------|-------------|-----------|-----------|
| **CJMRT-030012-422** | 无法处理的实体 — 操作失败、事件无效或有效负载无效 | 输入数据无效（例如，不存在的受众、事件或属性） | 1.仔细检查输入/事件有效负荷结构<br/>2。 验证引用的对象（受众、数据集）是否存在并且处于活动状态<br/>3。 验证所有必填字段是否都存在<br/>4。 使用已知良好的有效负载进行测试&#x200B;<br/><br/>**相关文档**： [历程故障排除](troubleshooting.md)，[事件配置](../event/about-events.md) |
| **CJMRT-130004-400** | 错误请求 — 历程节点或渠道配置中的输入格式不正确 | 历程有效负载或配置引用已删除/无效的资源 | 1.查看历程节点配置<br/>2。 验证所有引用的资源（消息、受众、操作）是否存在<br/>3。 修复或更新损坏的引用<br/>4。 如有必要，重新构建历程配置&#x200B;<br/><br/>**相关文档**： [历程创建](journey-gs.md)，[自定义操作](../action/about-custom-action-configuration.md) |
| **CJMRT-000032-409** | 冲突 — 资源已存在 | 尝试创建具有重复ID或名称的资源 | 1.对所有资源<br/>2使用唯一ID和名称。 检查具有相同标识符<br/>3的现有资源。 删除或重命名冲突的对象<br/>4。 查看命名惯例&#x200B;<br/><br/>**相关文档**： [历程版本](journey-gs.md#journey-versions) |
| **CJMRT-170016-400** | 历程配置/预览期间请求无效 | 有效负载缺少所需的依赖项或断开的模板链接 | 1.验证所有必需资源是否处于活动状态<br/>2。 确保模板和内容块已发布<br/>3。 检查所有依赖项是否正确链接<br/>4。 查看历程测试模式结果&#x200B;<br/><br/>**相关文档**： [测试历程](testing-the-journey.md)，[历程依赖项](journey-gs.md) |
| **CJMRT-080608-400** | 域/渠道/委派中的请求无效 | 缺少所需的DNS记录或电子邮件/短信配置 | 1.完成电子邮件域<br/>2的DNS配置。 验证子域委派是否已完成<br/>3。 再次运行配置向导<br/>4。 允许DNS传播的时间（最多72小时）<br/><br/>**相关文档**： [渠道平面](../configuration/channel-surfaces.md)，[子域委派](../configuration/delegate-subdomain.md) |
| **CJMRT-110100-500** | 有效负载上的内部错误 | 后端数据/配置错误或不支持的配置 | 1.重试操作<br/>2。 如果使用高级功能，请简化配置<br/>3。 使用请求ID和确切有效负载<br/>4上报给Adobe支持。 查看发行说明&#x200B;<br/><br/>**相关文档**&#x200B;中的已知问题： [历程疑难解答](troubleshooting.md) |

### CJMAS：消息创作服务错误 {#cjmmas-errors}

创建、编辑或发布消息、预设和内容时，会发生这些错误。

| 错误代码 | 描述 | 根本原因 | 解决方法 |
|------------|-------------|-----------|-----------|
| **CJMMAS-1149-400** | 保存消息、预设或变体时请求无效 | 消息中缺少必填字段或配置错误 | 1.完成所有必填字段（标有星号）<br/>2。 验证消息/预设配置<br/>3。 检查字段值格式和约束<br/>4。 查看UI <br/><br/>**相关文档**&#x200B;中的验证消息： [电子邮件渠道](../email/get-started-email.md)，[渠道界面](../configuration/channel-surfaces.md) |
| **CJMMAS-2073-422** | 消息预设编辑中无法处理的实体 | 验证错误、不支持的字段或不正确的语法 | 1.更正语法/字段错误，如指示所示<br/>2。 与已知良好的配置<br/>3比较。 在保存<br/>4之前使用消息UI验证。 查看文档&#x200B;<br/><br/>**相关文档**&#x200B;中的字段要求： [消息预设](../configuration/channel-surfaces.md)，[电子邮件设置](../email/email-settings.md) |
| **CJMMAS-1300-500** | 消息创作过程中出现内部错误 | 由于基础架构问题、大型内容或服务停机导致后端崩溃 | 1.简化模板/内容（减小大小/复杂性）<br/>2。 请重试操作<br/>3。 增量保存工作<br/>4。 如果是永久性的，请升级至Adobe支持&#x200B;<br/><br/>**相关文档**： [内容模板](../content-management/content-templates.md) |
| **CJMMAS-2001-200** | 成功状态但错误横幅：缺少选择退出链接 | 电子邮件变体中缺少所需的取消订阅链接 | 1.向所有电子邮件变体添加选择退出/取消订阅链接<br/>2。 确保链接存在于每个语言版本<br/>3中。 使用个性化帮助程序插入选择退出链接<br/>4。 在发布&#x200B;<br/><br/>**相关文档**&#x200B;之前测试所有变体： [选择退出管理](../privacy/opt-out.md)，[电子邮件设计](../email/content-from-scratch.md) |
| **CJMMAS-1603-403** | 更新/发布模板或预设时禁止 | 用户缺少所需的权限/角色，或者在当前状态下不允许执行操作 | 1.验证用户是否具有适当的权限（消息管理器、作者等）<br/>2. 检查预设/模板状态（草稿、已发布、已存档）<br/>3。 如果需要，向管理员请求访问权限<br/>4。 查看产品配置文件分配&#x200B;<br/><br/>**相关文档**： [权限](../administration/permissions.md)，[访问控制](../administration/permissions-overview.md) |

### CJMCMP：营销活动错误 {#cjmcmp-errors}

在营销活动创建、配置和激活期间发生这些错误。

| 错误代码 | 描述 | 根本原因 | 解决方法 |
|------------|-------------|-----------|-----------|
| **CJMCMP-2050-400** | 活动激活或审批中的请求无效 | 营销活动引用无效/缺少策略或区段 | 1.审核所有营销活动节点配置<br/>2。 验证策略/区段链接当前是否有效<br/>3。 使用正确的配置<br/>4进行更新。 在激活之前重新测试营销活动&#x200B;<br/><br/>**相关文档**： [营销活动创建](../campaigns/create-campaign.md)，[营销活动审批](../test-approve/gs-approval.md) |

## 一般故障排除方法 {#troubleshooting-approach}

遇到错误代码时，请遵循这种系统化方法：

1. **识别错误**：请注意完整的错误代码、HTTP状态以及任何随附的消息或请求ID。

2. **查找服务**：使用服务前缀(CJMPTS、CJMRT、CJMMAS、CJMCMP)来标识受影响的组件。

3. **检查状态代码**：
   * **400（错误请求）**：查看输入数据和配置
   * **403（禁止访问）**：检查权限和访问权限
   * **409（冲突）**：查找重复或冲突的资源
   * **422 （无法处理的实体）**：根据架构要求验证数据
   * **500（内部服务器错误）**：重试并可能升级至支持部门

4. **查看最近的更改**：考虑最近修改的内容（历程更新、新营销活动、配置更改等）。

5. **查阅文档**：使用本指南中提供的链接访问受影响功能的详细文档。

6. **在适当时重试**：对于500系列错误，几分钟后进行简单重试通常可以解决暂时性问题。

7. **需要时上报**：如果在执行解决步骤后错误仍然存在，请联系Adobe支持，联系方式为：
   * 完整错误代码
   * 请求ID（如果可用）
   * 重现问题的步骤
   * 相关配置详细信息

## 避免常见错误的最佳实践 {#best-practices}

### 历程激活前 {#journey-best-practices}

* **验证所有资源**：确保所有引用的受众、事件、数据源和自定义操作均已正确配置
* **彻底测试**：使用测试模式在发布之前识别问题（[了解更多](testing-the-journey.md)）
* **验证卷**：在上线之前，使用模拟运行验证受众覆盖范围和分支逻辑（[了解详情](journey-dry-run.md)）
* **检查权限**：验证您对所有组件具有必要的访问权限
* **查看依赖项**：确保已发布所有链接的消息和内容

### 创建消息时 {#message-best-practices}

* **填写必填字段**：保存之前请始终填写所有必填字段
* **包含选择退出链接**：将取消订阅链接添加到所有电子邮件变体（[了解详情](../privacy/opt-out.md)）
* **验证个性化**：使用示例配置文件测试所有动态内容（[了解更多](../personalization/personalization-build-expressions.md)）
* **保持模板可管理**：避免过于复杂的模板，以免导致呈现问题

### 用于营销活动管理 {#campaign-best-practices}

* **验证受众数据**：确保正确配置和填充目标受众
* **检查审批状态**：在尝试激活之前，了解审批要求（[了解更多](../test-approve/gs-approval.md)）
* **监视配置**：定期检查渠道表面和预设的有效性
* **计划DNS更改**：在更新域时留出足够的时间进行DNS传播

## 其他资源 {#additional-resources}

* [历程疑难解答](troubleshooting.md)
* [执行疑难解答](troubleshooting-execution.md)
* [入站活动疑难解答](troubleshooting-inbound.md)
* [自定义操作疑难解答](../action/troubleshoot-custom-action.md)
* [历程常见问题解答](journey-faq.md)
* [护栏和限制](../start/guardrails.md)

## 获取支持 {#getting-support}

如果您遇到使用本指南无法解决的持续错误：

1. **收集信息**：收集错误代码、请求ID、时间戳以及要再现的步骤
2. **检查系统状态**：访问[Adobe状态](https://status.adobe.com/){target="_blank"}以了解已知的服务问题
3. **搜索文档**：查看[Adobe Experience League](https://experienceleague.adobe.com/docs/journey-optimizer.html?lang=zh-Hans){target="_blank"}以了解解决方案
4. **参与社区**：在[Adobe Journey Optimizer社区](https://experienceleaguecommunities.adobe.com/t5/journey-optimizer/ct-p/journey-optimizer){target="_blank"}中发布问题
5. **联系Adobe支持部门**：提交支持票证并包含所有相关详细信息

>[!NOTE]
>
>此错误代码引用将随着识别和记录新代码而不断更新。 有关最新信息，请定期查看[Adobe Journey Optimizer社区博客](https://experienceleaguecommunities.adobe.com/t5/journey-optimizer-blogs/bg-p/journey-optimizer-blogs){target="_blank"}。

**相关主题**

* [揭露Adobe Journey Optimizer错误代码：第1部分](https://experienceleaguecommunities.adobe.com/t5/journey-optimizer-blogs/demystifying-adobe-journey-optimizer-error-codes-root-causes-and/ba-p/760884){target="_blank"}
* [揭露Adobe Journey Optimizer错误代码：第2部分](https://experienceleaguecommunities.adobe.com/t5/journey-optimizer-blogs/demystifying-adobe-journey-optimizer-error-codes-root-causes-and/bc-p/782661){target="_blank"}

