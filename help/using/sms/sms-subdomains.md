---
solution: Journey Optimizer
product: journey optimizer
title: 为文本消息（短信/彩信）配置子域
description: 了解如何使用Journey Optimizer配置短信子域
role: Admin
feature: SMS, Channel Configuration
level: Intermediate
keywords: 短信、子域、配置
exl-id: 08a546d1-060c-43e8-9eac-4c38945cc3e1
source-git-commit: 19f127c2abc81239abda8ebd38bdcacee796a1b0
workflow-type: tm+mt
source-wordcount: '928'
ht-degree: 20%

---

# 配置短信子域 {#sms-mms-subdomains}

>[!CONTEXTUALHELP]
>id="ajo_admin_subdomain_sms_header"
>title="委派 SMS/MMS 子域"
>abstract="设置短信 (SMS/MMS) 的子域。可使用已委派给 Adobe 的子域或配置新的子域。"

>[!CONTEXTUALHELP]
>id="ajo_admin_subdomain_sms"
>title="委派 SMS/MMS 子域"
>abstract="必须配置用于短信的子域，因为需要此子域才能创建短信配置。可使用已委派给 Adobe 的子域或配置新的子域。"
>additional-url="https://experienceleague.adobe.com/zh-hans/docs/journey-optimizer/using/channels/sms/configure-sms/sms-configuration-surface" text="创建短信配置"

>[!CONTEXTUALHELP]
>id="ajo_admin_config_sms_subdomain"
>title="选择 SMS/MMS 子域"
>abstract="为了能够创建短信配置，请确保您之前已至少配置了一个短信子域，以便从子域名称列表中选择。"
>additional-url="https://experienceleague.adobe.com/zh-hans/docs/journey-optimizer/using/channels/sms/configure-sms/sms-configuration-surface" text="创建短信配置"

## 短信子域入门 {#gs-sms-mms-subdomains}

若要能够缩短添加到SMS/MMS消息的URL，您必须设置在[创建SMS配置](sms-configuration.md#message-preset-sms)时将选择的子域。

您可以使用已委派给Adobe的子域，也可以配置其他子域。 在[本节](../configuration/delegate-subdomain.md)中了解有关将子域委派到Adobe的更多信息。

SMS子域配置在所有环境&#x200B;**之间共享**。 因此，对短信子域的任何修改也会影响其他生产沙盒。

要访问和编辑SMS子域，您必须对生产沙盒具有&#x200B;**[!UICONTROL 管理SMS子域]**&#x200B;权限。 可在[此部分](../administration/high-low-permissions.md)中详细了解权限。

## 使用现有子域 {#sms-use-existing-subdomain}

要使用已委派给Adobe的子域，请执行以下步骤。

1. 浏览到&#x200B;**[!UICONTROL 管理]** > **[!UICONTROL 渠道]**&#x200B;菜单，然后选择&#x200B;**[!UICONTROL SMS设置]** > **[!UICONTROL SMS子域]**。

1. 单击&#x200B;**[!UICONTROL 设置子域]**。

   ![](assets/sms_set-up-subdomain.png)

1. 从&#x200B;**[!UICONTROL 配置类型]**&#x200B;部分中选择&#x200B;**[!UICONTROL 使用委派的子域]**。

   ![](assets/sms_use-delegated-subdomain.png)

1. 输入将在短信URL中显示的前缀。

   只允许使用字母数字字符和连字符。

1. 从列表中选择已委派的子域。

   您不能选择已用作短信子域的子域。

   <!--Capital letters are not allowed in subdomains. TBC by PM-->

   ![](assets/sms_prefix-and-subdomain.png)

   <!--Note that you cannot use multiple delegated subdomains of the same parent domain. For example, if 'marketing1.yourcompany.com' is already delegated to Adobe for your SMS messages, you will not be able to use 'marketing2.yourcompany.com'. However, multi-level subdomains being supported for SMS, you may proceed using a subdomain of 'marketing1.yourcompany.com' (such as 'email.marketing1.yourcompany.com'), or a different parent domain.-->

   >[!CAUTION]
   >
   >如果您选择使用[CNAME方法](../configuration/delegate-subdomain.md#cname-subdomain-delegation)委派给Adobe的域，则必须在您的托管平台上创建DNS记录。 要生成DNS记录，此过程与配置新的短信子域时的过程相同。 在[本节](#sms-configure-new-subdomain)中了解详情。

1. 单击&#x200B;**[!UICONTROL 提交]**。

1. 提交后，子域将显示在状态为&#x200B;**[!UICONTROL 正在处理]**&#x200B;的列表中。 有关子域状态的详细信息，请参阅[此部分](../configuration/about-subdomain-delegation.md#access-delegated-subdomains).<!--Same statuses?-->

   在能够使用该子域发送邮件之前，您必须等待Adobe执行所需的检查，这可能需要&#x200B;**最多4个小时**。<!--Learn more in [this section](delegate-subdomain.md#subdomain-validation).-->

1. 检查成功后，子域将获得&#x200B;**[!UICONTROL Success]**&#x200B;状态。 它可用于创建短信渠道配置。

## 配置新的子域 {#sms-configure-new-subdomain}

>[!CONTEXTUALHELP]
>id="ajo_admin_sms_subdomain_dns"
>title="生成匹配的 DNS 记录"
>abstract="要配置新的短信子域，您需要复制在 Journey Optimizer 界面中显示的 Adobe 名称服务器信息，将它粘贴到您的域托管解决方案中以生成匹配的 DNS 记录。检查成功后，该子域即可用于创建短信配置。"

要配置新子域，请执行以下步骤。

1. 浏览到&#x200B;**[!UICONTROL 管理]** > **[!UICONTROL 渠道]**&#x200B;菜单，然后选择&#x200B;**[!UICONTROL SMS设置]** > **[!UICONTROL SMS子域]**。

1. 单击&#x200B;**[!UICONTROL 设置子域]**。

   ![](assets/sms_set-up-subdomain.png)

1. 从&#x200B;**[!UICONTROL 配置类型]**&#x200B;部分中选择&#x200B;**[!UICONTROL 添加您自己的域]**。

   ![](assets/sms_add-your-own-subdomain.png)

1. 指定要委派的子域。

   >[!CAUTION]
   >
   >* 您无法使用现有的短信子域。
   >
   >* 子域中不允许使用大写字母。

   不允许将无效子域委派给Adobe。 确保输入贵组织拥有的有效子域，如marketing.yourcompany.com。

   支持（同一父域的）多级别子域。 例如，您可以使用“sms.marketing.yourcompany.com”。

1. 将显示要放置在DNS服务器上的记录。 复制此记录或下载CSV文件，然后导航到您的域托管解决方案以生成匹配的DNS记录。

1. 确保已将DNS记录生成到域托管解决方案中。 如果一切配置正确，请选中“我确认……”框，然后单击&#x200B;**[!UICONTROL 提交]**。

   ![](assets/sms_add-your-own-subdomain-confirm.png)

   配置新的短信子域时，它始终指向CNAME记录。

1. 提交子域委派后，子域将显示在状态为&#x200B;**[!UICONTROL 正在处理]**&#x200B;的列表中。 有关子域状态的详细信息，请参阅[此部分](../configuration/about-subdomain-delegation.md#access-delegated-subdomains).<!--Same statuses?-->

在使用子域发送短信消息之前，您必须等待Adobe执行所需的检查，最长可能需要4小时。<!--Learn more in [this section](#subdomain-validation).-->检查成功后，子域将获得&#x200B;**[!UICONTROL Success]**&#x200B;状态。 它可用于创建短信渠道配置。

请注意，如果您无法在托管解决方案上创建验证记录，则子域将标记为&#x200B;**[!UICONTROL 失败]**。

## 取消委派子域 {#undelegate-subdomain}

如果要取消委派短信子域，请联系您的Adobe代表。

但是，在与Adobe联系之前，您需要在用户界面中执行多个步骤。

>[!NOTE]
>
>您只能取消委派状态为&#x200B;**[!UICONTROL 成功]**&#x200B;的子域。 可以从用户界面中删除具有&#x200B;**[!UICONTROL 草稿]**&#x200B;和&#x200B;**[!UICONTROL 失败]**&#x200B;状态的子域。

首先，在[!DNL Journey Optimizer]中执行以下步骤：

1. 取消激活与子域关联的所有渠道配置。 [了解如何操作](../configuration/channel-surfaces.md#deactivate-a-surface)

<!--
1. If the SMS subdomain is using an email subdomain that was [already delegated](#lp-use-existing-subdomain) to Adobe, undelegate the email subdomain. [Learn how](../configuration/delegate-subdomain.md#undelegate-subdomain)-->

1. 停止与子域关联的活动营销活动。 [了解如何操作](../campaigns/modify-stop-campaign.md#stop)

1. 停止与子域关联的活动历程。 [了解如何操作](../building-journeys/end-journey.md#stop-journey)

1. 如果SMS子域是[新委派的子域](#sms-configure-new-subdomain)，请删除与该子域关联的DNS条目。

完成后，联系Adobe代表，告知您要取消委派的子域。

Adobe处理您的请求后，未委派域不再显示在子域清单页面上。

>[!CAUTION]
>
>取消委派子域后：
>
>   * 您无法重新激活使用该子域的渠道配置。
>   * 您不能通过用户界面再次委派确切的子域。 如果您希望这样做，请联系您的Adobe代表。
