---
solution: Journey Optimizer
product: journey optimizer
title: 查看和激活营销活动
description: 了解如何在Journey Optimizer中查看和激活营销活动
feature: Campaigns
topic: Content Management
role: User
level: Intermediate
keywords: 营销活动，审阅，验证，激活，激活，优化器
exl-id: 86f35987-f0b7-406e-9ae6-0e4a2e651610
source-git-commit: a5d8f10c8751d6be47f5423aea576e16590b86d6
workflow-type: tm+mt
source-wordcount: '514'
ht-degree: 1%

---


# 执行API触发的营销活动 {#execute}

激活营销活动后，您需要检索生成的示例cURL请求，并将其用于API中以构建有效负载并触发营销活动。

## 必读 {#must-read}

* **促销活动开始/结束日期** — 如果您在创建促销活动时配置了特定的开始和/或结束日期，则不会在这些日期之外执行，并且API调用将失败。

* **调用超时** — 对交互式消息执行REST API的调用超时60秒。 但是，如果意外超时，则进行内部重试以确保投放。

## 触发活动 {#trigger}

1. 打开营销活动，然后从&#x200B;**[!UICONTROL cURL请求]**&#x200B;部分复制并粘贴有效负载请求。 此有效负载包含消息中使用的所有个性化（用户档案和上下文）变量。 活动开始后，即可使用该功能。

   ![](assets/api-triggered-curl.png)

   >[!IMPORTANT]
   >
   >cURL部分中的端点在标准和[高吞吐量营销活动](../campaigns/api-triggered-high-throughput.md)之间有所不同。

1. 将此cURL请求用到API中以构建有效负载并触发营销活动。 有关详细信息，请参阅[交互式消息执行API文档](https://developer.adobe.com/journey-optimizer-apis/references/messaging/#tag/execution)，其中列出了标准和高吞吐量营销活动的所有端点。

   [此页面](https://developer.adobe.com/journey-optimizer-apis/references/messaging-samples/)上也提供了API调用示例。

## 故障排除 {#troubleshooting}

### 电子邮件投放延迟 {#delivery-delays}

如果电子邮件投放时间超过预期，请调查外部服务（如云基础架构提供商或电子邮件服务提供商）的潜在中断或性能问题。 Journey Optimizer日志记录消息出发时间戳，这有助于确定投放管道中下游是否发生了延迟。

### Azure Cosmos DB身份验证错误（500内部服务器错误） {#cosmosdb-auth-errors}

如果您在触发API触发的营销活动时遇到&#x200B;**500内部服务器错误**，并且系统日志显示来自Azure Cosmos DB的&#x200B;**403 Forbidden**&#x200B;错误，并显示一条消息，例如：

_“由于Azure Cosmos DB服务无法获取帐户默认身份的AAD身份验证令牌，因此对您帐户的访问当前被撤销”_

此错误通常发生在Cosmos DB身份验证所需的Azure服务主体已禁用、删除或配置错误时。

+++如何解决此问题

1. **验证您的Azure服务主体** — 确保您的Azure服务主体或托管标识已启用，并且尚未在Azure Active Directory中禁用或删除。

1. **检查权限** — 确认服务主体具有访问Azure Key Vault和Cosmos DB资源的必要权限。 服务主体必须具有适当的角色分配，才能通过Azure Cosmos DB进行身份验证。

1. **查看Azure Cosmos DB CMK配置** — 如果您使用的是客户管理的密钥(CMK)，请查阅[Azure Cosmos DB CMK疑难解答指南](https://learn.microsoft.com/en-us/azure/cosmos-db/cmk-troubleshooting-guide#azure-active-directory-token-acquisition-error){target="_blank"}，以了解恢复AAD令牌获取的详细步骤。

1. **重新启用并测试** — 更正配置后，重新启用服务主体（如果已禁用），并重新测试事务性营销活动API调用，以确认身份验证成功且消息已投放。

>[!NOTE]
>
>此问题通常是由错误配置或意外禁用Cosmos DB身份验证所需的Azure服务主体导致的。 保持服务主体已启用且配置正确将防止将来出现此错误。

+++
