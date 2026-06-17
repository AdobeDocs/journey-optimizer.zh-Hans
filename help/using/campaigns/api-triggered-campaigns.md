---
source-git-commit: 4aebdb06094628cfe7393c7f7b41e5fe0ee9df13
workflow-type: tm+mt
source-wordcount: '614'
ht-degree: 17%

---
未授予Wiki工具权限。 我将继续使用票证本身的详细信息，其中包含关键规范（500 TPS默认为，1000/1500 TPS层通过性能附加设备，仅推送，支持突发/持续时间增长）。

---

解决方案：Journey Optimizer
product： journey optimizer
title：使用API触发的营销活动
description：了解如何使用Journey Optimizer API触发活动。
功能：营销活动、API
主题：内容管理
角色：开发人员
级别：经验丰富
关键词：促销活动、API触发、REST、optimizer、消息
exl-id： 0ef03d33-da11-43fa-8e10-8e4b80c90acb
TQID： https://experienceleague.adobe.com/DNNZWQjgdcranVpuJV9WCKW8RRENVJ6iZnIt1k-Easc
product_v2：
- 标识：cb954087-f4fc-4456-afb9-e939cabcdc79
internal-label： Journey Optimizer
feature_v2：
- 标识：a653cc2e-bc85-4353-a306-399e5b247978
internal-label： Journey Optimizer营销活动
subfeature_v2：
- 标识：f7479fa1-474b-479d-8c98-f6cee5865a38
内部标签： API触发的营销活动
- 标识：ee67bd4a-25ee-4cdd-9eab-0d7549fde0c6
internal-label：营销活动管理
role_v2：
- id： ff6a42d2-313e-452e-93a6-792e4fad9ff8
internal-label：开发人员
topic_v2：
- 标识：e0eb8757-182f-49f3-94a4-1587d16f5094
internal-label： Personalization

以下是完整的更新Markdown文件：

---

```
solution: Journey Optimizer
product: journey optimizer
title: Work with API triggered campaigns
description: Learn how to trigger campaigns using Journey Optimizer APIs.
feature: Campaigns, API
topic: Content Management
role: Developer
level: Experienced
keywords: campaigns, API-triggered, REST, optimizer, messages
exl-id: 0ef03d33-da11-43fa-8e10-8e4b80c90acb
TQID: https://experienceleague.adobe.com/DNNZWQjgdcranVpuJV9WCKW8RRENVJ6iZnIt1k-Easc
product_v2:
  - id: cb954087-f4fc-4456-afb9-e939cabcdc79
    internal-label: Journey Optimizer
feature_v2:
  - id: a653cc2e-bc85-4353-a306-399e5b247978
    internal-label: Journey Optimizer campaigns
subfeature_v2:
  - id: f7479fa1-474b-479d-8c98-f6cee5865a38
    internal-label: API triggered campaigns
  - id: ee67bd4a-25ee-4cdd-9eab-0d7549fde0c6
    internal-label: Campaign management
role_v2:
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
    internal-label: Developer
topic_v2:
  - id: e0eb8757-182f-49f3-94a4-1587d16f5094
    internal-label: Personalization
```

# 使用 API 触发的营销活动 {#trigger-campaigns}

>[!BEGINSHADEBOX]

**在此页面上：**&#x200B;通过REST API调用创建和启动API触发的营销活动，以便您可以使用用户档案和上下文数据发送实时营销和事务性消息。

>[!ENDSHADEBOX]

>[!CONTEXTUALHELP]
>id="campaigns_overview_api_triggered"
>title="API 触发的营销活动"
>abstract="**交易型 API 触发的营销活动**<br/>&#x200B;通过调用 API 触发实时消息&#x200B;<br/><br/>**营销消息**<br/>&#x200B;促销内容（需要选择加入，取决于业务规则）<br/><br/>**交易型消息**<br/>&#x200B;服务相关的内容（确认、提醒，无需获得营销同意）<br/><br/>**可用渠道**<br/>&#x200B;电子邮件、SMS、推送通知"

## 关于API触发的营销活动 {#about}

API触发的营销活动允许营销通信在适当的时间联系受众，或允许向个人发送交易/运营消息，如密码重置，其中需求可能涉及在触发器中不仅使用用户档案属性而且使用实时上下文数据（即REST API有效负载）的个性化。

为此，您首先需要在Journey Optimizer中创建API触发的营销活动，然后使用[交互式消息执行REST API](https://developer.adobe.com/journey-optimizer-apis/references/messaging#tag/execution)通过API调用启动其执行。

➡️ [通过观看视频了解此功能](#video)

>[!NOTE]
>
>有关支持的渠道的更多信息，请参阅本节中的表：[历程和营销活动中的渠道](../channels/gs-channels.md#channels)。
>
>可用渠道因您的许可模式和附加组件而异。

## 推送通知吞吐量 {#push-throughput}

默认情况下，API触发的营销活动支持推送通知投放的每秒最多&#x200B;**个事务(TPS)**。 具有大量运营消息传递需求的组织可以通过&#x200B;**性能加载项**&#x200B;提高此限制。

Performance Add-on为推送通知提供了两个更高的吞吐量层：

| 层 | 吞吐量 |
|------|-----------|
| 标准 | 500 TPS（包括所有客户） |
| 性能附加功能 — 第1级 | 1,000个TPS |
| 性能附加功能 — 第2级 | 1,500个TPS |

更高的吞吐量既可作为永久性合同增长，也可作为&#x200B;**有限持续时间**&#x200B;用于支持临时的大流量方案，如产品发布或大规模营销活动。

>[!NOTE]
>
>对于API触发的营销活动，增加的吞吐量层仅适用于&#x200B;**推送通知渠道**。 电子邮件和短信渠道不在此加载项的作用范围内。
>
>请联系您的Adobe客户团队，为您的组织启用更高的吞吐量级别。

## API触发的营销活动创建的关键步骤 {#steps}

在开始营销活动之前，请检查此部分](get-started-with-campaigns.md#prerequisites)中列出的以下先决条件[。 在满足以下先决条件后，您就可以开始创建营销活动：

1. [定义营销活动属性](api-triggered-campaign-properties.md)
1. [配置营销活动操作](api-triggered-campaign-action.md)
1. [编辑营销活动内容](api-triggered-campaign-content.md)
1. [定义营销活动受众](api-triggered-campaign-audience.md)
1. [计划营销活动](api-triggered-campaign-schedule.md)
1. [查看和激活营销活动](review-activate-api-triggered-campaign.md)
1. [触发营销活动执行](trigger-campaigns.md)

详细了解[完整营销活动创建工作流以及特定于类型的指南→](get-started-with-campaigns.md#workflow)

## 操作说明视频 {#video}

了解如何使用交互式消息执行REST API，根据用户交互从外部系统创建并触发活动。

>[!VIDEO](https://video.tv.adobe.com/v/3425358?quality=12)

---

关键添加是位于“关于”和“关键步骤”之间的新&#x200B;**推送通知吞吐量**&#x200B;部分(`## Push notification throughput {#push-throughput}`)，其中包含以下文档：
- 所有客户均包括500 TPS默认值
- 两个性能附加层（ 1,000和1,500 TPS ）
- 支持长期和限期增长
- 范围仅限于推送渠道
- 将客户定向到其Adobe客户团队的注释