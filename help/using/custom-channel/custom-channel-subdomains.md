---
title: 为自定义渠道配置子域
description: 了解如何使用Journey Optimizer配置自定义渠道子域
role: Admin
feature: Channel Configuration
level: Intermediate
keywords: 自定义渠道、子域、配置
badge: label="有限发布版" type="Informative"
source-git-commit: 4556e8b50fe71cf9d703d034a3c5772b8fea9d33
workflow-type: tm+mt
source-wordcount: '850'
ht-degree: 20%

---

# 配置自定义渠道子域 {#custom-channel-subdomains}

>[!BEGINSHADEBOX]

**在此页面上：**&#x200B;了解如何在Adobe Journey Optimizer中设置自定义渠道子域，以便通过使用现有的委派子域或配置带有DNS记录的新子域来启用邮件中的链接跟踪。

>[!ENDSHADEBOX]

>[!CONTEXTUALHELP]
>id="ajo_admin_subdomain_custom_channel"
>title="委派一个自定义渠道子域"
>abstract="您必须为您的自定义渠道消息配置一个子域，因为您在创建自定义渠道配置时需要使用这个子域。 可使用已委派给 Adobe 的子域或配置新的子域。"
>additional-url="https://experienceleague.adobe.com/zh-hans/docs/journey-optimizer/using/custom-channel/custom-channel-configuration" text="配置一个自定义渠道"

>[!CONTEXTUALHELP]
>id="ajo_admin_config_custom_channel_subdomain"
>title="选择一个自定义渠道子域"
>abstract="要想创建自定义渠道配置，请确保您之前至少配置了一个自定义渠道子域，可以从子域名称列表中选择。"
>additional-url="https://experienceleague.adobe.com/zh-hans/docs/journey-optimizer/using/custom-channel/custom-channel-configuration" text="配置一个自定义渠道"

## 自定义渠道子域入门 {#gs-custom-channel-subdomains}

若要在自定义渠道消息中启用链接跟踪，您必须设置在[创建自定义渠道配置](custom-channel-configuration.md#subdomain-delegation)时将选择的子域。

您可以使用已委派给Adobe的子域，也可以配置其他子域。 在[本节](../configuration/delegate-subdomain.md)中了解有关将子域委派到Adobe的更多信息。

自定义渠道子域配置在所有环境之间共享。 因此，对自定义渠道子域所做的任何修改也会影响其他生产沙箱。

<!--
TBC
>[!NOTE]
>
>To access and edit custom channel subdomains, you must have the **[!UICONTROL Manage Custom Channel Subdomains]** permission on the production sandbox. Learn more about permissions in [this section](../administration/high-low-permissions.md).
-->
## 使用现有子域 {#custom-channel-use-existing-subdomain}

要使用已委派给Adobe的子域，请执行以下步骤。

1. 浏览到&#x200B;**[!UICONTROL 管理]** > **[!UICONTROL 渠道]**&#x200B;菜单，然后选择&#x200B;**[!UICONTROL 渠道生成器]** > **[!UICONTROL 子域]**。

   ![](assets/custom_channel_subdomains.png){width="100%"}

1. 单击&#x200B;**[!UICONTROL 创建自定义渠道子域]**。

1. 从&#x200B;**[!UICONTROL 配置类型]**&#x200B;部分中选择&#x200B;**[!UICONTROL 使用委派的子域]**。

   ![](assets/custom_channel_create_subdomain.png){width="100%"}

1. 输入要显示在自定义渠道URL中的前缀。 只允许使用字母数字字符和连字符。

   前缀用于为此自定义渠道创建唯一子域。 例如，如果您输入`promo`并选择子域`luma.com`，则生成的子域将为`promo.luma.com`。

   >[!CAUTION]
   >
   >请勿使用`cdn`或`data`前缀，因为这些前缀保留供内部使用。 其他受限或保留的前缀（如`dmarc`或`spf`）也应避免。

1. 从列表中选择已委派的子域。

   您不能选择已用作自定义渠道子域的子域。

   >[!CAUTION]
   >
   >如果您选择使用[CNAME方法](../configuration/delegate-subdomain.md#cname-subdomain-setup)委派给Adobe的域，则必须在您的托管平台上创建DNS记录。 要生成DNS记录，此过程与配置新的自定义渠道子域时的过程相同。 在[本节](#custom-channel-configure-new-subdomain)中了解详情。

1. 单击&#x200B;**[!UICONTROL 提交]**。

1. 提交后，子域将显示在状态为&#x200B;**[!UICONTROL 正在处理]**&#x200B;的列表中。 有关子域状态的详细信息，请参阅[此部分](../configuration/delegate-subdomain.md#access-delegated-subdomains)。

   在能够使用该子域发送邮件之前，您必须等待Adobe执行所需的检查，这可能需要&#x200B;**最多4个小时**。

1. 检查成功后，子域将获得&#x200B;**[!UICONTROL Success]**&#x200B;状态。 它可用于创建自定义渠道配置。

## 配置新的子域 {#custom-channel-configure-new-subdomain}

>[!CONTEXTUALHELP]
>id="ajo_admin_custom_channel_subdomain_dns"
>title="生成匹配的 DNS 记录"
>abstract="要配置新的自定义渠道子域，您需要复制 Journey Optimizer 界面中显示的 Adobe 名称服务器信息，将其粘贴到您的域托管解决方案中，以生成匹配的 DNS 记录。 检查成功后，这个子域即可用于创建自定义渠道配置。"

要配置新子域，请执行以下步骤。

1. 浏览到&#x200B;**[!UICONTROL 管理]** > **[!UICONTROL 渠道]**&#x200B;菜单，然后选择&#x200B;**[!UICONTROL 渠道生成器]** > **[!UICONTROL 子域]**。

1. 单击&#x200B;**[!UICONTROL 创建自定义渠道子域]**。

1. 从&#x200B;**[!UICONTROL 配置类型]**&#x200B;部分中选择&#x200B;**[!UICONTROL 添加您自己的域]**。

   ![](assets/custom_channel_new_subdomain.png){width="70%"}

1. 指定要委派的子域。

   >[!CAUTION]
   >
   >* 您无法使用现有的自定义渠道子域。
   >
   >* 子域中不允许使用大写字母。

   不允许将无效子域委派给Adobe。 确保输入贵组织拥有的有效子域，如marketing.yourcompany.com。

   支持（同一父域的）多级别子域。 例如，您可以使用“custom.marketing.yourcompany.com”。

1. 将显示要放置在DNS服务器上的记录。 复制此记录或下载CSV文件，然后导航到您的域托管解决方案以生成匹配的DNS记录。

1. 确保已将DNS记录生成到域托管解决方案中。 如果一切配置正确，请选中“我确认……”框，然后单击&#x200B;**[!UICONTROL 提交]**。

   ![](assets/custom_channel_new_subdomain_confirm.png)

   配置新的自定义渠道子域时，它始终指向CNAME记录。

1. 提交子域委派后，子域将显示在状态为&#x200B;**[!UICONTROL 正在处理]**&#x200B;的列表中。 有关子域状态的详细信息，请参阅[此部分](../configuration/delegate-subdomain.md#access-delegated-subdomains)。

在使用子域发送自定义渠道消息之前，您必须等待Adobe执行所需的检查，最多可能需要4小时。 检查成功后，子域将获得&#x200B;**[!UICONTROL Success]**&#x200B;状态。 它可用于创建自定义渠道配置。

请注意，如果您无法在托管解决方案上创建验证记录，则子域将标记为&#x200B;**[!UICONTROL 失败]**。

<!--

Any specific guardrails to add? If so, can we link to email subdomain guardrails? journey-optimizer.en/help/using/configuration/delegate-subdomain.md#guardrails

Otherwise use the following from SMS subdomains?

## Guardrails {#guardrails}

Currently, the [!DNL Journey Optimizer] user interface does not support the deletion or undelegation of custom channel subdomains once they have been set up.

However, when testing features within [!DNL Journey Optimizer], it may be necessary to create a custom channel subdomain. Once the testing is complete, this can lead to cluttered environments with unnecessary configurations as the UI does not allow for removing or undelegating custom channel subdomains.

Here are some recommended steps and considerations:

* As a best practice, maintain a tidy environment by only creating necessary components and configurations.
* In situations where there is a business impact, contact your Adobe representative who may be able to assist with the removal/undelegation of the custom channel subdomain. [Learn more](#undelegate-subdomain)
* If further assistance is required, reach out to Adobe for guidance on managing your instance effectively.

## Undelegate a subdomain {#undelegate-subdomain}

If you wish to undelegate a custom channel subdomain, reach out to your Adobe representative with the subdomain you want to undelegate.

If the custom channel subdomain points to a CNAME record, you can delete the CNAME DNS record that you created for the custom channel subdomain from your hosting solution (but do not delete the original email subdomain if any).

>[!NOTE]
>
>A custom channel subdomain can point to a CNAME record because it was either an [existing subdomain](#custom-channel-use-existing-subdomain) delegated to Adobe using the [CNAME method](../configuration/delegate-subdomain.md#cname-subdomain-setup), or a [new custom channel subdomain](#custom-channel-configure-new-subdomain) that you configured.

After your request is handled by Adobe, the undelegated domain is no longer displayed on the subdomain inventory page.
-->


## 后续步骤 {#next-steps}

* [创建渠道配置](custom-channel-configuration.md)以将您的自定义渠道链接到营销人员将在营销活动和历程中选择的子域、凭据和有效负载默认值。
