---
solution: Journey Optimizer
product: journey optimizer
title: 配置登陆页面子域
description: 了解如何使用Journey Optimizer配置登陆页面子域
feature: Landing Pages, Subdomains
role: Admin
level: Experienced
keywords: 登陆、登陆页面、子域、配置
exl-id: dd1af8dc-3920-46cb-ae4d-a8f4d4c26e89
source-git-commit: 25b1e6050e0cec3ae166532f47626d99ed68fe80
workflow-type: tm+mt
source-wordcount: '971'
ht-degree: 19%

---

# 配置登陆页面子域 {#lp-subdomains}

>[!CONTEXTUALHELP]
>id="ajo_admin_subdomain_lp_header"
>title="委派登陆页面子域"
>abstract="您需要设置子域以供登陆页面使用。可使用已委派给 Adobe 的子域或配置另一子域。"

>[!CONTEXTUALHELP]
>id="ajo_admin_subdomain_lp"
>title="委派登陆页面子域"
>abstract="您必须配置子域以用于登陆页面，因为您需要此子域才能创建登陆页面预设。您必须配置子域以用于登陆页面，因为您需要此子域才能创建登陆页面预设。 您可以使用已委派的子域来 Adobe 或配置新的子域。"
>additional-url="https://experienceleague.adobe.com/docs/journey-optimizer/using/content-management/landing-pages/lp-configuration/lp-presets.html#lp-create-preset" text="创建登陆页面预设"

>[!CONTEXTUALHELP]
>id="ajo_admin_config_lp_subdomain"
>title="创建登陆页面预设"
>abstract="要想创建登陆页面预设，请确保您之前至少配置了一个登陆页面子域，可以从子域名称列表中选择。"
>additional-url="https://experienceleague.adobe.com/docs/journey-optimizer/using/content-management/landing-pages/lp-configuration/lp-presets.html#lp-create-preset" text="创建登陆页面预设"

## 登陆页面子域入门 {#gs-lp-subdomains}

要[创建登陆页面预设](lp-presets.md)，您必须设置将用于登陆页面的子域。

您可以使用已委派给Adobe的子域，也可以配置其他子域。 在[本节](../configuration/delegate-subdomain.md)中了解有关将子域委派到Adobe的更多信息。

登陆页面子域配置是&#x200B;**所有环境通用的配置**。 因此：

* 要访问和编辑登陆页面子域，您必须对生产沙盒具有&#x200B;**[!UICONTROL 管理登陆页面子域]**&#x200B;权限。

* 对登陆页面子域的任何修改也会影响生产沙箱。

## 使用现有子域 {#lp-use-existing-subdomain}

要使用已委派给Adobe的子域，请执行以下步骤：

1. 访问&#x200B;**[!UICONTROL 管理]** > **[!UICONTROL 渠道]**&#x200B;菜单，然后选择&#x200B;**[!UICONTROL 登陆页面设置]** > **[!UICONTROL 登陆页面子域]**。

1. 单击&#x200B;**[!UICONTROL 设置子域]**。

   ![](assets/lp_set-up-subdomain.png)

1. 从&#x200B;**[!UICONTROL 配置类型]**&#x200B;部分中选择&#x200B;**[!UICONTROL 使用委派域]**。

   ![](assets/lp_use-delegated-subdomain.png)

1. 输入要显示在登陆页面URL中的前缀。

   只允许使用字母数字字符和连字符。

   >[!CAUTION]
   >
   >请勿使用`cdn`或`data`前缀，因为这些前缀保留供内部使用。 其他受限或保留的前缀（如`dmarc`或`spf`）也应避免。

1. 从列表中选择已委派的子域。

   您不能选择已用作登陆页子域的子域。

   <!--Capital letters are not allowed in subdomains. TBC by PM-->

   ![](assets/lp_prefix-and-subdomain.png)

   请注意，您不能使用同一父域的多个已委派子域。 例如，如果已经为您的登陆页面将“marketing1.yourcompany.com”委派给Adobe，则将无法使用“marketing2.yourcompany.com”。 但是，登陆页面支持多级别子域，您可以继续使用“marketing1.yourcompany.com”的子域（如“email.marketing1.yourcompany.com”）或其他父域。

   >[!CAUTION]
   >
   >如果您选择使用[CNAME方法](../configuration/delegate-subdomain.md#cname-subdomain-delegation)委派给Adobe的域，则必须在您的托管平台上创建DNS记录。 要生成DNS记录，此过程与配置新登陆页面子域时的过程相同。 在[本节](#lp-configure-new-subdomain)中了解详情。

1. 单击&#x200B;**[!UICONTROL 提交]**。

1. 提交后，子域将显示在状态为&#x200B;**[!UICONTROL 正在处理]**&#x200B;的列表中。 有关子域状态的详细信息，请参阅[此部分](../configuration/about-subdomain-delegation.md#access-delegated-subdomains).<!--Same statuses?-->

   ![](assets/lp_subdomain-processing.png)

   在能够使用该子域发送邮件之前，您必须等待Adobe执行所需的检查，这可能需要&#x200B;**最多4个小时**。<!--Learn more in [this section](delegate-subdomain.md#subdomain-validation).-->

1. 检查成功后，子域将获得&#x200B;**[!UICONTROL Success]**&#x200B;状态。 它可用于创建登陆页面预设。

## 配置新的子域 {#lp-configure-new-subdomain}

>[!CONTEXTUALHELP]
>id="ajo_admin_lp_subdomain_dns"
>title="生成匹配的 DNS 记录"
>abstract="要配置新的登陆页面子域，您需要复制 Journey Optimizer 界面中显示的 Adobe 名称服务器信息，将其粘贴到您的域托管解决方案中，以生成匹配的 DNS 记录。检查成功后，子域就可以用来创建登陆页面预设了。"

要配置新子域，请执行以下步骤。

1. 访问&#x200B;**[!UICONTROL 管理]** > **[!UICONTROL 渠道]**&#x200B;菜单，然后选择&#x200B;**[!UICONTROL 登陆页面设置]** > **[!UICONTROL 登陆页面子域]**。

1. 单击&#x200B;**[!UICONTROL 设置子域]**。

1. 从&#x200B;**[!UICONTROL 配置类型]**&#x200B;部分中选择&#x200B;**[!UICONTROL 添加您自己的域]**。

   ![](assets/lp_add-your-own-subdomain.png)

1. 指定要委派的子域。

   >[!CAUTION]
   >
   >* 您无法使用现有的登陆页面子域。
   >
   >* 子域中不允许使用大写字母。

   不允许将无效子域委派给Adobe。 确保输入贵组织拥有的有效子域，如marketing.yourcompany.com。

   对于登陆页面，支持多级子域。 例如，您可以使用“email.marketing.yourcompany.com”。

1. 将显示要放置在DNS服务器上的记录。 复制此记录或下载CSV文件，然后导航到您的域托管解决方案以生成匹配的DNS记录。

1. 确保已将DNS记录生成到域托管解决方案中。 如果一切配置正确，请选中“我确认……”框，然后单击&#x200B;**[!UICONTROL 提交]**。

   ![](assets/lp_add-your-own-subdomain-confirm.png)

   配置新登陆页面子域时，它始终指向CNAME记录。

1. 提交子域委派后，子域将显示在状态为&#x200B;**[!UICONTROL 正在处理]**&#x200B;的列表中。 有关子域状态的详细信息，请参阅[此部分](../configuration/about-subdomain-delegation.md#access-delegated-subdomains).<!--Same statuses?-->

   在能够将该子域用于登陆页面之前，您必须等待Adobe执行所需的检查，这可能需要&#x200B;**最多4个小时**。<!--Learn more in [this section](#subdomain-validation).-->

1. 检查成功后，子域将获得&#x200B;**[!UICONTROL Success]**&#x200B;状态。 它可用于创建登陆页面预设。

   请注意，如果您无法在托管解决方案上创建验证记录，则子域将标记为&#x200B;**[!UICONTROL 失败]**。

## 取消委派子域 {#undelegate-subdomain}

如果要取消委派登陆页面子域，请执行以下步骤。

1. 在[!DNL Journey Optimizer]中，取消发布与子域关联的所有登陆页面。 [了解如何操作](create-lp.md#access-landing-pages)

1. 如果登陆页面子域指向CNAME记录，则可以从托管解决方案中删除您为登陆页面子域创建的CNAME DNS记录（但不删除原始电子邮件子域，如果有的话）。

   >[!NOTE]
   >
   >登陆页面子域可以指向CNAME记录，因为它可能是使用[CNAME方法](../configuration/delegate-subdomain.md#cname-subdomain-delegation)委派给Adobe的[现有子域](#lp-use-existing-subdomain)，或者是您配置的[新登陆页面子域](#lp-configure-new-subdomain)。

1. 联系您的Adobe代表，告知您要取消委派的子域。

Adobe处理您的请求后，未委派域不再显示在子域清单页面上。
