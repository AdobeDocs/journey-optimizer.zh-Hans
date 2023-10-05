---
solution: Journey Optimizer
product: journey optimizer
title: 配置 Web 子域
description: 了解如何使用Journey Optimizer设置Web子域
role: Admin
level: Intermediate
keywords: Web、子域、配置
exl-id: 6e00466d-4ce5-4d80-89ff-c7331a5ab158
source-git-commit: c4ab97999d000d969f6f09f4d84be017d1288f94
workflow-type: tm+mt
source-wordcount: '843'
ht-degree: 21%

---

# 配置 Web 子域 {#web-subdomains}

>[!CONTEXTUALHELP]
>id="ajo_admin_subdomain_web_header"
>title="委派 Web 子域"
>abstract="您将设置您的子域以供 Web 渠道使用。可使用已委派给 Adobe 的子域或配置另一子域。"

>[!CONTEXTUALHELP]
>id="ajo_admin_subdomain_web"
>title="委派 Web 子域"
>abstract="如果您将来自 Adobe Experience Manager Assets Essentials 的内容添加到您的 Web 体验，则必须设置将用于发布此内容的子域。在已委派给 Adobe 的子域中进行选择或配置新的子域。"

>[!CONTEXTUALHELP]
>id="ajo_admin_subdomain_web_default"
>title="设置 Web 子域"
>abstract="从委派给 Adobe 的子域的列表中选择一个子域。可将此 Web 子域设置为默认子域，但一次只能使用一个默认子域。"

在创作Web体验时，如果您添加来自 [Adobe Experience Manager Assets Essentials](../content-management/assets-essentials.md) 库中，您必须设置用于发布此内容的子域。

您可以使用已委派给Adobe的子域，也可以配置另一个子域。 了解有关委派子域以在中进行Adobe的更多信息 [本节](../configuration/delegate-subdomain.md).

>[!CAUTION]
>
>Web子域配置对所有环境都是通用的。 因此：
>
>* 要访问和编辑Web子域，您必须具有 **[!UICONTROL 管理Web子域]** 生产沙盒的权限。
>
> * 对Web子域的任何修改也将影响生产沙箱。

您可以创建多个Web子域，但只能创建 **默认** 将使用子域。 您可以更改默认的Web子域，但一次只能使用一个子域。

## 访问和管理Web子域 {#access-web-subdomains}

1. 转到 **[!UICONTROL 管理]** > **[!UICONTROL 渠道]** 菜单，然后选择 **[!UICONTROL Web配置]** > **[!UICONTROL Web子域]**. 此时将显示使用当前沙盒设置的所有子域。

   ![](assets/web-access-subdomains.png)

1. 您可以筛选委派每个子域的用户或一个委派状态(**[!UICONTROL 草稿]**， **[!UICONTROL 正在处理]**， **[!UICONTROL 成功]** 或 **[!UICONTROL 失败]**)。

   ![](assets/web-filter-subdomains.png)

1. 此 **[!UICONTROL 默认]** 徽章显示在当前用作默认的子域旁边。 要更改默认子域，请选择 **[!UICONTROL 设置为默认值]** 从 **[!UICONTROL 更多操作]** 按钮来填充所需的子域。

   ![](assets/web-subdomain-default.png)

   >[!NOTE]
   >
   >您可以更改默认的Web子域，但一次只能使用一个子域。

## 使用现有子域 {#web-use-existing-subdomain}

要使用已委派给Adobe的子域，请执行以下步骤。

1. 访问 **[!UICONTROL 管理]** > **[!UICONTROL 渠道]** 菜单，然后选择 **[!UICONTROL Web配置]** > **[!UICONTROL Web子域]**.

1. 单击 **[!UICONTROL 设置子域]**.

1. 选择 **[!UICONTROL 使用委派的子域]** 选项来自 **[!UICONTROL 配置类型]** 部分，并从列表中选择已委派的子域。

   ![](assets/web-subdomain-details.png)

   >[!NOTE]
   >
   >您不能选择已用作Web子域的子域。

1. 将自动添加将显示在Web URL中的前缀。 您无法更改它。

1. 要将此子域设置为默认值，请选择相应的选项。

   ![](assets/web-subdomain-details-default.png)

   >[!NOTE]
   >
   >仅 **默认** 将使用子域。

1. 单击&#x200B;**[!UICONTROL 提交]**. 子域将获取 **[!UICONTROL 成功]** 状态。 它可供您的Web体验使用。

   >[!NOTE]
   >
   >在极少数情况下，子域设置可能会失败。 在这种情况下，您可以删除 **[!UICONTROL 失败]** 子域，以使用清除列表 **[!UICONTROL 删除]** 按钮来自 **[!UICONTROL 更多操作]** 图标。

## 配置新子域 {#web-configure-new-subdomain}

>[!CONTEXTUALHELP]
>id="ajo_admin_web_subdomain_dns"
>title="生成匹配的 DNS 记录"
>abstract="要配置新的 Web 子域，您需要复制在 Journey Optimizer 界面中显示的 Adobe 名称服务器信息，并将该信息粘贴到域托管解决方案中以生成匹配的 DNS 记录。检查成功后，子域便可用于发布来自 Experience Manager Assets Essentials 库的内容。"

要配置新子域，请执行以下步骤。

1. 访问 **[!UICONTROL 管理]** > **[!UICONTROL 渠道]** 菜单，然后选择 **[!UICONTROL Web配置]** > **[!UICONTROL Web子域]**.

1. 单击 **[!UICONTROL 设置子域]**.

1. 选择 **[!UICONTROL 添加您自己的域]** 从 **[!UICONTROL 配置类型]** 部分。

1. 指定要委派的子域。

   >[!CAUTION]
   >
   >无法使用现有Web子域。
   >
   >子域中不允许使用大写字母。

   ![](assets/web-add-your-own-domain.png)

   不允许将无效子域委派给Adobe。 确保输入贵组织拥有的有效子域，如marketing.yourcompany.com。

   >[!NOTE]
   >
   >支持（同一父域的）多级别子域。 例如，您可以使用“web.marketing.yourcompany.com”。

1. 要将此子域设置为默认值，请选择相应的选项。

   >[!NOTE]
   >
   >仅 **默认** 将使用子域。

1. 将显示要放置在DNS服务器上的记录。 复制此记录或下载CSV文件，然后导航到您的域托管解决方案以生成匹配的DNS记录。

1. 确保已将DNS记录生成到域托管解决方案中。 如果一切配置正确，请选中“我确认……”框，然后单击 **[!UICONTROL 提交]**.

   ![](assets/web-add-your-own-domain-confirm.png)

   >[!NOTE]
   >
   >配置新的Web子域时，它将始终指向CNAME记录。

1. 提交子域委派后，子域将显示在列表中，其中包含 **[!UICONTROL 正在处理]** 状态。 有关子域状态的更多信息，请参阅 [本节](../configuration/about-subdomain-delegation.md#access-delegated-subdomains).<!--Same statuses?-->

   >[!NOTE]
   >
   >在能够使用该子域发送Web消息之前，您必须等待Adobe执行所需的检查，这最多可能需要4小时。

1. 检查成功后，子域将获得 **[!UICONTROL 成功]** 状态。 它随时可用于创建Web渠道界面。

   请注意，该子域将标记为 **[!UICONTROL 失败]** 如果您无法在托管解决方案上创建验证记录。


<!--
Only a subdomain with the **[!UICONTROL Success]** status can be set as default.
You cannot delete a subdomain with the **[!UICONTROL Processing]** status.
-->
