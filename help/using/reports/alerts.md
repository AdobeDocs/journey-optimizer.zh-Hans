---
solution: Journey Optimizer
product: journey optimizer
title: 访问和订阅系统警报
description: 了解如何访问和订阅系统警报
feature: Journeys, Alerts
topic: Administration
role: User
level: Intermediate
exl-id: 0855ca5b-c7af-41c4-ad51-bed820ae5ecf
source-git-commit: 3aa3203ae7763d81288cb70a2984d017b0006bb3
workflow-type: tm+mt
source-wordcount: '977'
ht-degree: 1%

---

# 访问和订阅系统警报 {#alerts}

构建历程和营销活动时，请使用&#x200B;**警报**&#x200B;按钮在执行或发布错误之前检查和解决错误：

* 在[此页面](../building-journeys/troubleshooting.md)上了解如何对您的历程进行故障排除。
* 在[此页面](../campaigns/review-activate-campaign.md)上了解如何查看营销活动。

通过专用的&#x200B;**[!UICONTROL 警报]**&#x200B;菜单，您还可以订阅此页面上详细介绍的[!DNL Adobe Journey Optimizer]系统警报。

## 访问警报 {#access-alerts}

发生失败时，您可以在Journey Optimizer通知中心获取系统警报（应用程序内警报）和/或接收电子邮件。 要访问这些警报，请执行以下步骤。

<!--These messages can repeat over a pre-defined time interval until the alert has been resolved.-->

>[!NOTE]
>
>在[Adobe Experience Platform文档](https://experienceleague.adobe.com/docs/experience-platform/observability/alerts/overview.html?lang=zh-Hans){target="_blank"}中了解有关Adobe Experience Platform中警报的更多信息。

在左侧菜单的&#x200B;**[!UICONTROL 管理]**&#x200B;下，单击&#x200B;**[!UICONTROL 警报]**。 提供了多个预配置的Journey Optimizer警报。

这些警报的列表如下，每个警报的详细信息如下。

* 特定于历程的警报：

   * [历程自定义操作失败](#alert-custom-actions)警报
   * [读取受众触发器失败](#alert-read-audiences)警报

* 特定于渠道配置的警报：

   * [AJO域DNS记录缺失](#alert-dns-record-missing)警报
  <!--* the [AJO channel configuration failure](#alert-channel-config-failure) alert
   * the [AJO domain certificates renewal unsuccessful](#alert-certificates-renewal) alert-->

## 订阅警报 {#subscribe-alerts}

1. 您可以通过选择&#x200B;**[!UICONTROL 订阅]**&#x200B;选项，从用户界面中单独订阅每个警报。

   ![](assets/alert-subscribe.png){width=80%}

   >[!NOTE]
   >
   >订阅仅适用于特定沙盒。 您必须分别为每个沙盒订阅警报。

1. 使用相同的方法&#x200B;**[!UICONTROL 取消订阅]**。

1. 您还可以通过[I/O事件通知](https://experienceleague.adobe.com/docs/experience-platform/observability/alerts/subscribe.html){target="_blank"}订阅警报。 警报规则将整理到不同的订阅包中。 与特定Journey Optimizer警报对应的事件订阅在[下面](#journey-alerts)有详细的说明。

1. 如果发生意外行为，并且/或者您的操作中达到了一组特定条件（例如，当系统违反阈值时可能会出现问题），则将警报通知发送给组织中订阅这些通知的任何用户。

根据订阅者的首选项，警报会通过电子邮件发送和/或直接在用户界面右上角的Journey Optimizer通知中心发送（应用程序内通知）。 在[!DNL Adobe Experience Cloud] **[!UICONTROL 首选项]**&#x200B;中选择您希望如何接收这些警报。 [了解详情](../start/user-interface.md#in-product-alerts)

>[!NOTE]
>
>默认情况下，仅启用应用程序内警报。

<!--To enable email alerting, refer to [Adobe Experience Platform documentation](https://experienceleague.adobe.com/docs/experience-platform/observability/alerts/ui.html#enable-email-alerts){target="_blank"}.-->

警报解决后，订阅者会收到“已解决”通知。

## 管理警报 {#manage-alerts}

若要管理警报，请选择一个项目并使用&#x200B;**[!UICONTROL 其他操作]**&#x200B;按钮。

![](assets/alert-more-actions.png){width=80%}

默认情况下，将启用所有警报。 要禁用警报，请从&#x200B;**[!UICONTROL 更多操作]**&#x200B;菜单中选择&#x200B;**[!UICONTROL 禁用警报]**&#x200B;选项。 此警报的所有订阅者将不再收到相关通知。

选择&#x200B;**[!UICONTROL 管理警报订阅者]**&#x200B;以查看订阅了警报的用户列表。 使用空白字段添加更多订阅者。

![](assets/alert-subscribers.png){width=80%}

下面列出了可能的警报状态：

* **[!UICONTROL 已启用]** — 警报已启用，当前正在监视触发条件。
* **[!UICONTROL 已禁用]** — 警报已禁用，当前未监视触发条件。 您将不会收到此警报的通知。
* **[!UICONTROL 已触发]** — 当前满足警报的触发条件。

## 历程警报 {#journey-alerts}

>[!CAUTION]
>
>Adobe Journey Optimizer特定警报仅适用于&#x200B;**实时**&#x200B;历程。 在测试模式下，历程不会触发警报。

### 历程自定义操作失败 {#alert-custom-actions}

如果自定义操作失败，此警报将警告您。 我们认为，过去5分钟内在特定自定义操作中发生超过1%的错误属于故障。 每30秒评估一次。

![](assets/alerts-custom-action.png)

过去5分钟内，出现以下情况时，将会解决自定义操作警报：

* 该自定义操作没有任何错误（或低于1%阈值的错误），

* 或者，没有任何配置文件达到该自定义操作。

与自定义操作警报对应的I/O事件订阅名称为&#x200B;**历程自定义操作失败**。

要对&#x200B;**自定义操作**&#x200B;警报进行故障排除，请执行以下操作：

* 使用其他历程上的测试模式检查您的自定义操作：

  ![](assets/alert-troubleshooting-2.png)

* 检查您的历程报告以查看操作中的错误原因。

  ![](assets/alert-troubleshooting-3.png)

* 检查您的历程stepEvents以查找有关“failureReason”的更多信息。

* 检查您的自定义操作配置，并验证身份验证是否仍然正常。 例如，使用Postman执行手动检查。

### 读取受众触发器不成功 {#alert-read-audiences}

如果&#x200B;**读取受众**&#x200B;活动在计划执行时间后的10分钟内未处理任何配置文件，则此警报会警告您。 此故障可能是由技术问题或受众为空导致的。 如果这种失败是由技术问题引起的，请注意，根据问题的类型，重试仍然可能发生（例如：如果导出作业创建失败，我们将每10mn重试一次，最长为1h）。

![](assets/alerts1.png)

有关&#x200B;**读取受众**&#x200B;活动的警报仅适用于定期历程。 **实时历程中的读取受众**&#x200B;活动计划运行&#x200B;**一次**&#x200B;或&#x200B;**尽快**&#x200B;被忽略。

当配置文件进入&#x200B;**读取受众**&#x200B;节点时，已解决&#x200B;**读取受众**&#x200B;上的警报。

与&#x200B;**读取受众触发器失败**&#x200B;警报对应的I/O事件订阅名称为&#x200B;**历程读取受众延迟、失败和错误**。

要对&#x200B;**读取受众**&#x200B;警报进行故障排除，请在Experience Platform界面中检查您的受众计数。

![](assets/alert-troubleshooting-0.png)

![](assets/alert-troubleshooting-1.png)

## 配置警报 {#configuration-alerts}

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

<!--The I/O event subscription name corresponding to this alert is xx. > Do we need to mention this?

### AJO channel configuration failure {#alert-channel-config-failure}

>[!IMPORTANT]
>
>This alert applies only to **email** channel configurations using the [custom subdomain](../configuration/delegate-custom-subdomain.md) delegation type. ///Other channel types (such as SMS, push, or in-app) are not covered by this alert.///

This alert is triggered in case the system audit detects email channel configuration issues. These issues may include misconfigured channel settings, invalid DNS configuration, suppression list issue, IP inconsistency, or any other errors that can impact email delivery.

If you receive such an alert, the resolution steps are listed below:

1. Click the alert to be directed to the impacted [email channel configuration](../email/get-started-email-config.md) in the [!DNL Journey Optimizer] interface.

   For guidance on editing channel configurations, see [this section](../configuration/channel-surfaces.md#edit-channel-surface).

1. Review the configuration details and error messages provided. Common failure reasons include:

   * SPF validation failed
   * DKIM validation failed
   * MX record validation failed
   * Invalid DNS records

   >[!NOTE]
   >
   >The possible configuration failure reasons are listed in [this section](../configuration/channel-surfaces.md).

1. Resolve the issue:

   * Update the channel configuration as needed.
   * You may need to fix specific DNS issues mentioned in the alert.

   >[!NOTE]
   >
   >As a single domain can be associated with multiple channel configurations, resolving DNS issues for one channel configuration may automatically fix related issues across several configurations.

If the change does not resolve the issue, the same alert will be triggered again the next day.

When resolving email configuration issues, keep in mind the best practices listed below:

* Act promptly - Address configuration failures as soon as they are detected to avoid disruptions in email delivery.
* Check all configurations - If the alert indicates multiple impacted email configurations, review and fix each of them.

### AJO domain certificates renewal unsuccessful {#alert-certificates-renewal}

This alert warns you if a domain certificate (CDN, tracking URL) renewal failed for a specific Journey Optimizer subdomain.-->





