---
solution: Journey Optimizer
product: journey optimizer
title: 营销活动报告
description: 了解如何使用营销活动报告中的实时活动数据
feature: Reporting
topic: Content Management
role: User
level: Intermediate
hide: true
hidefromtoc: true
exl-id: 58034ec4-62dc-406c-99c4-d6b7aa107140
source-git-commit: 2fc4b1ee34b44fb6c5bcddb13f1b2b02f7094ff1
workflow-type: tm+mt
source-wordcount: '651'
ht-degree: 1%

---

# 实时活动营销活动报告 {#campaign-global-report-cja-activity}

>[!BEGINSHADEBOX]

您可以通过单击营销活动中的&#x200B;**[!UICONTROL 报告]**&#x200B;按钮，然后选择&#x200B;**[!UICONTROL 查看所有时间报告]**&#x200B;来访问实时活动营销活动报告。 [了解详情](report-gs-cja.md)

![](assets/report-access.png)

>[!ENDSHADEBOX]

## 发送统计数据 {#sending-statistics-mobile}

![](assets/sending-statistics-mobile-live.png)

**[!UICONTROL 发送统计数据]**&#x200B;表提供与实时活动营销活动相关的关键量度的详细概述。 它会显示诸如目标受众规模以及成功交付的实时活动数量等重要信息，以帮助您评估实时活动的整体影响范围和性能。

+++ 了解有关发送统计信息量度的更多信息

* **[!UICONTROL 目标]**：在应用排除、禁止或同意移除之前，符合受众条件的配置文件数。

* **[!UICONTROL 发送]**：尝试发送到目标用户档案的实时活动总数。

* **[!UICONTROL 已投放]**：成功传递到设备的实时活动数，与尝试发送的次数总数相关。

* **[!UICONTROL 发送错误]**：由于错误（例如，无效令牌或连接问题）而无法发送的实时活动总数。

* **[!UICONTROL 发送排除项]**： Adobe Journey Optimizer不发送的用户档案数（例如，由于选择退出状态或资格规则）。

+++

## 实时活动生命周期 {#lifecycle}

**[!UICONTROL 实时活动生命周期]**&#x200B;表提供了实时活动随时间变化的全面视图。 它提供对关键事件（如活动何时开始、更新或结束）的可见性，帮助您更好地了解用户参与和实时活动营销活动的整个生命周期。

根据您使用的是事务型营销活动还是营销活动，报表会有所不同。

### 事务性实时活动

![](assets/activity-lifecycle.png)

对于事务型营销活动，实时活动营销活动报表会显示所有生命周期事件，包括远程启动、本地启动、更新和结束。

+++ 了解有关事务性营销活动的实时活动生命周期量度的更多信息

* **[!UICONTROL 远程启动]**：远程启动的实时活动启动事件总数，通常由服务器或后端系统触发。

* **[!UICONTROL 本地启动]**：在用户设备上本地启动的实时活动启动事件总数，通常由用户交互或客户端触发引起。

* **[!UICONTROL 更新]**：发送到设备的实时活动更新总数。 更新可以包括状态更改、新内容或进度通知。

* **[!UICONTROL 结束]**：发送到设备的实时活动结束事件总数。

* **[!UICONTROL 总数计数]**：所有实时活动生命周期事件的总数，包括开始、更新和结束，提供了实时活动量的完整衡量标准。

+++

### 营销实时活动

![](assets/activity-lifecycle-broadcast.png)

营销活动将实时活动用于广播用例，同时将更新发送到多个设备。

对于营销活动中的iOS Live活动，报表仅显示开始时的&#x200B;**[!UICONTROL 远程启动]**&#x200B;事件和&#x200B;**[!UICONTROL 远程启动错误]**。 未跟踪&#x200B;**[!UICONTROL 更新]**&#x200B;和&#x200B;**[!UICONTROL 结束]**&#x200B;事件，因为APN将更新分发到所有设备而不提供反馈。 要查看&#x200B;**[!UICONTROL 更新]**&#x200B;和&#x200B;**[!UICONTROL 结束]**&#x200B;事件，请使用[Apple的推送通知控制台](https://developer.apple.com/notifications/push-notifications-console/)。

+++ 了解有关活动生命周期量度与营销活动的更多信息

* **[!UICONTROL 远程启动]**：远程启动的实时活动启动事件总数，通常由服务器或后端系统触发。

* **[!UICONTROL 远程启动错误]**：尝试远程启动实时活动时发生的总错误数（例如，无效令牌或连接问题）。

+++

#### 通过API检索更新和结束计数 {#retrieving-updates-end-api}

作为使用Apple推送通知控制台的替代方法，更新和结束计数可通过Headless API调用获取。

在执行广播用例的更新或结束API调用时，响应包含`controlBreakdown`部分，该部分提供指示为实时活动执行执行了多少更新和结束调用的计数器。 没有生命周期数据的旧版执行不存在此块。 如果需要，还可以使用GET端点显式检索执行状态。

**更新/结束响应(200 OK)**

```json
{
  "executionId": "HA-exec-abc",
  "campaignId": "campaign-abc-123",
  "campaignVersionId": "v1",
  "audienceId": "audience-segment-id",
  "status": "processing",
  "targetedProfileCount": 150000,
  "createdAt": "2026-02-27T10:00:00Z",
  "executionLifecycle": {
    "lastControlAt": "2026-02-27T10:45:00Z",
    "controlBreakdown": {
      "update": 5,
      "end": 1
    }
  }
}
```

**执行状态(GET)**

```
GET /im/executions/audience/{executionId}
```

## 错误原因 {#error-reasons}

![](assets/error-reasons-activity.png)

**[!UICONTROL 错误原因]**&#x200B;表允许您识别在实时活动发送过程中发生的特定错误，从而便于彻底分析遇到的任何问题。

## 排除的原因 {#excluded-reasons}

![](assets/excluded-activity.png)

**[!UICONTROL 排除的原因]**&#x200B;表直观地描述了导致从目标受众中排除用户配置文件，阻止他们接收您的实时活动的各种因素。
