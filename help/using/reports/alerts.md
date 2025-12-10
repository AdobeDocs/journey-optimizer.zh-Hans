---
solution: Journey Optimizer
product: journey optimizer
title: 访问和订阅系统警报
description: 了解如何访问和订阅系统警报
feature: Journeys, Alerts, Monitoring
topic: Administration
role: User
level: Intermediate
exl-id: 0855ca5b-c7af-41c4-ad51-bed820ae5ecf
source-git-commit: 619db0a371b96fbe9480300a874839b7b919268d
workflow-type: tm+mt
source-wordcount: '2216'
ht-degree: 2%

---

# 访问和订阅系统警报 {#alerts}

在构建历程和营销活动时，使用&#x200B;**警报**&#x200B;按钮在执行或发布之前检查和解决错误。

* 在[此页面](../building-journeys/troubleshooting.md)上了解如何对您的历程进行故障排除

* 了解如何查看和激活您的营销活动： [操作营销活动](../campaigns/review-activate-campaign.md) | [API触发的营销活动](../campaigns/review-activate-api-triggered-campaign.md) | [编排的营销活动](../orchestrated/start-monitor-campaigns.md)


除上述情况外，当达到特定条件集时，还会向组织中订阅了警报消息的任何用户发送警报消息。 这些警报可从专用的&#x200B;**[!UICONTROL 警报]**&#x200B;菜单中获取。 Adobe Experience Platform提供了多个预定义警报规则，您可以为组织启用这些规则。 此外，您可以订阅此页面上详述的特定于[!DNL Adobe Journey Optimizer]的系统警报。

>[!NOTE]
>
>在[Adobe Experience Platform文档](https://experienceleague.adobe.com/docs/experience-platform/observability/alerts/overview.html?lang=zh-Hans){target="_blank"}中了解有关Adobe Experience Platform中警报的更多信息。

在左侧菜单的&#x200B;**[!UICONTROL 管理]**&#x200B;下，单击&#x200B;**[!UICONTROL 警报]**。 **浏览**&#x200B;选项卡中有几个预先配置的Journey Optimizer警报。

![](assets/updated-alerts-list.png){width=50%}

* 特定于历程的警报：

   * [读取受众触发器失败](#alert-read-audiences)警报
   * [超出自定义操作错误率](#alert-custom-action-error-rate)警报(替换以前的历程自定义操作失败警报)
   * [超过配置文件丢弃率](#alert-discard-rate)警报
   * [超出配置文件错误率](#alert-profile-error-rate)警报
   * [历程已发布](#alert-journey-published)警报
   * [历程已完成](#alert-journey-finished)个警报
   * 已触发[自定义操作上限](#alert-custom-action-capping)警报

* 特定于渠道配置的警报：

   * [AJO域DNS记录缺失](#alert-dns-record-missing)警报
   * [AJO渠道配置失败](#alert-channel-config-failure)警报
     <!--* the [AJO domain certificates renewal unsuccessful](#alert-certificates-renewal) alert-->

## 订阅警报 {#subscribe-alerts}

如果发生意外行为，并且/或者您的操作中达到了一组特定条件（例如，当系统违反阈值时可能会出现问题），则将警报通知发送给组织中订阅这些通知的任何用户。

您可以从用户界面单独订阅每个警报，可以从&#x200B;**[!UICONTROL 警报]**&#x200B;菜单全局订阅（请参阅[全局订阅](#global-subscription)），也可以统一特定历程（请参阅[统一订阅](#unitary-subscription)）。

根据订阅者的首选项，警报会通过电子邮件发送和/或直接在用户界面右上角的Journey Optimizer通知中心发送（应用程序内通知）。 在[!DNL Adobe Experience Cloud] **[!UICONTROL 首选项]**&#x200B;中选择您希望如何接收这些警报。 [了解详情](../start/user-interface.md#in-product-uc)

警报解决后，订阅者会收到“已解决”通知。 警报会在1小时后解决，以防止切换值。


### 全局订阅 {#global-subscription}

要订阅/取消订阅所有历程和营销活动的警报，请执行以下步骤：

1. 从左侧菜单浏览到&#x200B;**[!UICONTROL 警报]**&#x200B;仪表板，为要订阅的警报选择&#x200B;**[!UICONTROL 订阅]**&#x200B;选项。

   ![订阅警报](assets/alert-subscribe.png){width=80%}

   >[!NOTE]
   >
   >订阅仅适用于特定沙盒。 您必须分别为每个沙盒订阅警报。

1. 使用相同的方法&#x200B;**[!UICONTROL 取消订阅]**。

您还可以通过[I/O事件通知](https://experienceleague.adobe.com/docs/experience-platform/observability/alerts/subscribe.html){target="_blank"}进行订阅。 警报规则将整理到不同的订阅包中。 与特定Journey Optimizer警报对应的事件订阅在[下面](#journey-alerts)有详细的说明。

### 单一订阅 {#unitary-subscription}

要订阅/取消订阅特定历程的警报，请执行以下步骤：

1. 浏览到历程清单，并为特定历程选择&#x200B;**[!UICONTROL 订阅警报]**&#x200B;选项。

   ![订阅特定历程的警报](assets/subscribe-journey-alert.png){width=75%}

1. 选择警报。 以下警报可用：[超过配置文件丢弃率](#alert-discard-rate)、[超过自定义操作错误率](#alert-custom-action-error-rate)、[超过配置文件错误率](#alert-profile-error-rate)、[已发布历程](#alert-journey-published)、[历程已完成](#alert-journey-finished)以及[已触发自定义操作上限](#alert-custom-action-capping)。

1. 要取消订阅警报，请从同一屏幕取消选择警报。

1. 单击&#x200B;**[!UICONTROL 保存]**&#x200B;确认。

<!--To enable email alerting, refer to [Adobe Experience Platform documentation](https://experienceleague.adobe.com/docs/experience-platform/observability/alerts/ui.html#enable-email-alerts){target="_blank"}.-->

## 历程警报 {#journey-alerts}


下面列出了用户界面中可用的所有历程通知。

>[!CAUTION]
>
>Adobe Journey Optimizer特定警报仅适用于&#x200B;**实时**&#x200B;历程。 在测试模式下，历程不会触发警报。

### 读取受众触发器不成功 {#alert-read-audiences}

如果&#x200B;**读取受众**&#x200B;活动在计划执行时间后的10分钟内未处理任何配置文件，则此警报会警告您。 此故障可能是由技术问题或受众为空导致的。 如果这种失败是由技术问题引起的，请注意，根据问题的类型，重试仍然可能发生（例如：如果导出作业创建失败，我们将每10mn重试一次，最长为1h）。

有关&#x200B;**读取受众**&#x200B;活动的警报仅适用于定期历程。 **实时历程中的读取受众**&#x200B;活动计划运行&#x200B;**一次**&#x200B;或&#x200B;**尽快**&#x200B;被忽略。

当配置文件进入&#x200B;**读取受众**&#x200B;节点时或在1小时后解决&#x200B;**读取受众**&#x200B;上的警报。

与&#x200B;**读取受众触发器失败**&#x200B;警报对应的I/O事件订阅名称为&#x200B;**历程读取受众延迟、失败和错误**。

要对&#x200B;**读取受众**&#x200B;警报进行故障排除，请在Experience Platform界面中检查您的受众计数。

### 超出了轮廓丢弃率 {#alert-discard-rate}

如果过去5分钟内放弃的配置文件与输入的配置文件的比率超过阈值，此警报将发出警告。 默认阈值设置为20%，但您可以[定义自定义阈值](#custom-threshold)。

单击警报的名称以检查警报详细信息和配置。

![](assets/profile-discard-alert.png)

配置文件可能会被丢弃的原因有多种，这有助于了解故障排除方法。 下面列出了一些常见原因：

* 配置文件在进入时已被丢弃，因为它已位于该单一历程中。 要解决此问题，请确保配置文件有足够的时间退出历程，以免该配置文件的下一个事件到达。
* 未为配置文件设置标识，或读取受众历程使用的命名空间未在该配置文件中使用。 要解决此问题，请确保历程中的命名空间与用户档案使用的身份命名空间匹配。
* 超出事件吞吐率。 要解决此问题，请确保进入系统的事件不超过这些限制。


### 超出了自定义操作错误率 {#alert-custom-action-error-rate}

如果自定义操作错误与过去5分钟内成功HTTP调用的比率超过阈值，此警报将发出警告。 默认阈值设置为20%，但您可以[定义自定义阈值](#custom-threshold)。

>[!NOTE]
>
>此警报取代了以前的&#x200B;**历程自定义操作失败**&#x200B;警报。

单击警报的名称以检查警报详细信息和配置。

由于各种原因，可能会发生自定义操作错误。 要排除这些错误，您可以：

* 在另一个历程中使用[测试模式](../building-journeys/testing-the-journey.md)检查您的自定义操作。
* 检查您的[历程报告](../reports/journey-live-report.md)以查看操作的错误原因。
* 检查您的历程stepEvents以查找有关“failureReason”的更多信息。
* 检查自定义操作是否配置正确，并验证身份验证是否仍然有效。 例如，使用Postman执行手动检查。
* 检查端点是否可访问，以及自定义操作是否可以通过自定义操作连接检查器到达端点。
* 验证验证凭证、检查Internet连接等。

### 超出了轮廓错误率 {#alert-profile-error-rate}

如果过去5分钟内出错的配置文件与输入的配置文件的比率超过阈值，此警报将警告您。 默认阈值设置为20%，但您可以[定义自定义阈值](#custom-threshold)。

单击警报的名称以检查警报详细信息和配置。

要排除配置文件错误，您可以在步骤事件中查询数据，以了解配置文件在历程中失败的位置和原因。

### 已发布历程 {#alert-journey-published}

>[!AVAILABILITY]
>
>此警报当前功能有限。 虽然您可以订阅此警报，但通知尚未完全运行。

此警报会在从业者在历程画布中发布历程时通知您。

这是一个信息性警报，可帮助您跟踪组织中的历程生命周期事件。 没有解决标准，因为这是一次性通知。

### 历程已完成 {#alert-journey-finished}

>[!AVAILABILITY]
>
>此警报当前功能有限。 虽然您可以订阅此警报，但通知尚未完全运行。

此警报会在历程完成后通知您。 “已完成”的定义因旅程类型而异：

| 历程类型 | 周期性？ | 有结束日期吗？ | “已完成”的定义 |
|--------------|------------|---------------|--------------------------|
| 读取受众 | 否 | 不适用 | 执行开始后91天 |
| 读取受众 | 是 | 否 | 执行开始后91天 |
| 读取受众 | 是 | 是 | 达到结束日期时 |
| 事件触发的历程 | 不适用 | 是 | 达到结束日期时 |
| 事件触发的历程 | 不适用 | 否 | 在UI中或通过API关闭时 |

这是一个信息性警报，可帮助您跟踪历程的完成情况。 没有解决标准，因为这是一次性通知。

### 已触发自定义操作上限 {#alert-custom-action-capping}

>[!AVAILABILITY]
>
>此警报当前功能有限。 虽然您可以订阅此警报，但通知尚未完全运行。

当自定义操作触发上限时，此警报会警告您。 上限用于限制发送到外部端点的调用的数量，以防止端点过多。

单击警报的名称以检查警报详细信息和配置。

触发上限时，这意味着在定义的时间段内已达到API调用的最大数量，并且正在限制或排队更多调用。 了解有关[此页面](../action/about-custom-action-configuration.md#custom-action-enhancements-best-practices)上的自定义操作上限的更多信息。

当上限不再处于活动状态或在评估期间没有用户档案达到自定义操作时，此警报将得以解决。

要对上限问题进行故障诊断，请执行以下操作：

* 查看自定义操作上的上限配置，确保这些限制适合您的用例。
* 检查API调用的量是否高于预期，并考虑调整历程设计或设置上限。
* 监控外部端点，以确保其能够处理预期的负载。

## 配置警报 {#configuration-alerts}

下面列出了用户界面中可用的通道配置监视警报。

### AJO域DNS记录缺失 {#alert-dns-record-missing}

当缺少正确可投放性配置所需的关键DNS记录（NS或CNAME）或配置错误时，此警报会通知您。 如果没有这些记录，电子邮件可投放性可能会受损。

>[!NOTE]
>
>* NS记录对于将子域完全委派给Adobe至关重要。 [了解详情](../configuration/about-subdomain-delegation.md#full-subdomain-delegation)
>
>* CNAME记录支持CNAME子域设置。 [了解详情](../configuration/about-subdomain-delegation.md#cname-subdomain-setup)

当系统检测到所需的NS或CNAME记录不存在或不符合配置标准时，会触发&#x200B;**AJO域DNS记录缺失**&#x200B;警报。

1. 单击警报以定向到[界面中受影响的](../configuration/delegate-subdomain.md)子域[!DNL Journey Optimizer]。

   <!--For guidance on editing delegated subdomains, see [this section](../configuration/delegate-subdomain.md).-->

1. 通过正确设置记录来修复DNS配置，并再次[提交子域](../configuration/delegate-subdomain.md#submit-subdomain)委派。

   >[!NOTE]
   >
   >在继续之前，请确保已在您的域托管解决方案上正确创建了所有记录。

1. 如果不确定正确的值，则可以在[!DNL Journey Optimizer]中创建一个与受影响的子域同名的新子域。 [了解如何设置新的子域](../configuration/delegate-subdomain.md#set-up-subdomain)

如果更改无法解决问题，第二天将再次触发同一警报。

<!--The I/O event subscription name corresponding to this alert is xx. > Do we need to mention this?-->

### AJO渠道配置失败 {#alert-channel-config-failure}

>[!IMPORTANT]
>
>此警报仅适用于使用&#x200B;**自定义子域**&#x200B;委派类型的[电子邮件](../configuration/delegate-custom-subdomain.md)渠道配置。<!--Other channel types (such as SMS, push, or in-app) are not covered by this alert.-->

如果系统审核检测到电子邮件渠道配置问题，则会触发此警报。 这些问题可能包括渠道设置配置错误、DNS配置无效、禁止列表问题、IP不一致或任何其他可能影响电子邮件投放的错误。

如果收到此类警报，请执行以下解决步骤：

1. 单击警报以定向到[界面中受影响的](../email/get-started-email-config.md)电子邮件渠道配置[!DNL Journey Optimizer]。

   有关编辑渠道配置的指导，请参阅[此部分](../configuration/channel-surfaces.md#edit-channel-surface)。

1. 查看提供的配置详细信息和错误消息。 常见失败原因包括：

   * SPF验证失败
   * DKIM验证失败
   * MX记录验证失败
   * DNS记录无效

   >[!NOTE]
   >
   >[此部分](../configuration/channel-surfaces.md)列出了可能的配置失败原因。

1. 解决问题：

   * 根据需要更新渠道配置。
   * 您可能需要修复警报中提到的特定DNS问题。

   >[!NOTE]
   >
   >由于单个域可以与多个渠道配置关联，因此为一个渠道配置解决DNS问题可能会自动修复多个配置中的相关问题。

如果更改未解决问题，第二天将再次触发同一警报。

在解决电子邮件配置问题时，请牢记以下列出的最佳实践：

* 迅速采取行动 — 一旦检测到配置故障，请立即解决这些故障，以避免电子邮件投放中断。
* 检查所有配置 — 如果警报指示多个受影响的电子邮件配置，请查看和修复每个配置。

<!--### AJO domain certificates renewal unsuccessful {#alert-certificates-renewal}

This alert warns you if a domain certificate (CDN, tracking URL) renewal failed for a specific Journey Optimizer subdomain.-->

## 管理警报 {#manage-alerts}

### 编辑警报

您可以通过单击警报行来查看其详细信息。 名称、状态和通知渠道会显示在左侧面板中。
对于历程警报，请使用**[!UICONTROL 更多操作]**&#x200B;按钮编辑它们。 然后，您可以为这些警报定义[自定义阈值](#custom-threshold)。

![](assets/alert-more-actions.png){width=60%}

### 定义自定义阈值 {#custom-threshold}

您可以为[历程警报](#journey-alerts)设置阈值。 阈值警报高于默认值的20%。

要更改阈值，请执行以下操作：

1. 浏览到&#x200B;**警报**&#x200B;屏幕
1. 单击要更新的警报的&#x200B;**[!UICONTROL 更多操作]**&#x200B;按钮
1. 输入新阈值并进行确认。 新阈值适用于&#x200B;**所有**&#x200B;历程


![](assets/alert-threshold.png){width=60%}

>[!CAUTION]
>
>阈值级别在所有历程中都是全局的，无法为每个历程单独进行修改。

### 禁用警报

默认情况下，将启用所有警报。 要禁用警报，请选择&#x200B;**[!UICONTROL 禁用警报]**&#x200B;选项：此警报的所有订阅者将不再收到相关通知。


### 警报状态

下面列出了可能的警报状态：

* **[!UICONTROL 已启用]** — 警报已启用，当前正在监视触发条件。
* **[!UICONTROL 已禁用]** — 警报已禁用，当前未监视触发条件。 您将不会收到此警报的通知。
* **[!UICONTROL 已触发]** — 当前满足警报的触发条件。


### 查看和更新订阅者 {#manage-subscribers}

选择&#x200B;**[!UICONTROL 管理警报订阅者]**&#x200B;以查看订阅了警报的用户列表。

![](assets/alert-subscribers.png){width=80%}

若要添加更多订阅者，请输入其电子邮件（以逗号分隔），然后选择&#x200B;**[!UICONTROL 更新]**。

要删除订阅者，请从当前订阅者中删除其电子邮件地址，然后选择&#x200B;**[!UICONTROL 更新]**。

## 其他资源 {#additional-resources-alerts}

* 在[此页面](../building-journeys/troubleshooting.md)上了解如何对您的历程进行故障排除。
* 在[此页面](../campaigns/review-activate-campaign.md)上了解如何查看营销活动。
